# GPower

[![DOI](https://zenodo.org/badge/1106672819.svg)](https://doi.org/10.5281/zenodo.17768003)

**[🔗 Launch GPower Web Tool](https://orfanidis.net.gr/GPower/)**

A web-based sample size calculator for statistical power analysis, supporting T-Test, ANOVA, Paired T-Test, and Two Proportions calculations with interactive sensitivity analysis charts.

## Usage

Simply visit the [GPower Web Tool](https://orfanidis.net.gr/GPower/) in a modern web browser. The tool will:

1. Load the Python statistics engine (statsmodels and matplotlib)
2. Present an interactive interface for entering parameters
3. Calculate required sample sizes in real-time
4. Display a sensitivity analysis chart showing N vs. Effect Size

## Features

### Analysis Types

- **Groups (T-Test / ANOVA)**: Calculate required sample sizes for comparing group means
  - T-Test: For comparing 2 independent groups using Cohen's d effect size
  - ANOVA: For comparing 3+ groups using Cohen's f effect size

- **Paired T-Test (Before/After)**: Calculate required sample sizes for dependent samples
  - For comparing paired measurements (e.g., before vs. after intervention)
  - Uses Cohen's d effect size with correlation adjustment
  - Adjusts for reduced variance in paired designs: d_adj = d / √(1 - ρ)
  
- **Two Proportions**: Calculate required sample sizes for comparing two independent proportions (dichotomous outcomes)
  - Uses Cohen's h effect size (displayed in real-time)
  - Ideal for clinical trials comparing treatment vs. control success rates

### Sensitivity Analysis Charts

A key feature that transforms GPower from a single-number calculator into a visual decision-making tool with dual visualization:

- **Dual Chart Layout**: Side-by-side charts showing N vs Effect Size and N vs Power
- **N vs Effect Size Chart**: Shows how sample size requirements change across different effect sizes with your fixed Power and Alpha
- **N vs Power Chart**: Shows how sample size requirements change as you vary statistical power with your fixed Effect Size and Alpha
- **Cohen's Conventions**: Vertical lines mark Small, Medium, and Large effect size thresholds
- **Standard Power Line**: Marks the conventional Power = 0.80 threshold
- **Current Position Indicator**: Red dots show your current parameters and required N
- **Real-time Updates**: Charts regenerate instantly as you adjust parameters
- **Professional Output**: Clean, publication-ready dual charts using Matplotlib

### Additional Features

- **Dropout Rate Adjustment**: Account for expected participant dropouts using the formula:
  $$\text{Required Sample} = \frac{\text{Theoretical Sample}}{1 - \text{Dropout Rate}}$$
- **Interactive Interface**: Real-time calculations with intuitive sliders and input controls
- **Effect Size Presets**: Quick selection of small, medium, and large effect sizes based on Cohen's conventions
- **Mobile Responsive**: Works seamlessly on both desktop and mobile devices
- **No Installation Required**: Runs entirely in your browser using Pyodide (Python in WebAssembly)

### Parameters

#### Groups Mode (T-Test / ANOVA)
- **Number of Groups**: 2 for T-test, 3+ for ANOVA
- **Effect Size**: Expected magnitude of the effect (Cohen's d for T-test, Cohen's f for ANOVA)
- **Statistical Power**: Probability of detecting an effect if it exists (typically 0.80)
- **Significance Level (alpha)**: Risk of Type I error (typically 0.05)
- **Expected Dropout Rate**: Percentage of participants expected to drop out (0-50%)

#### Paired T-Test Mode (Before/After)
- **Effect Size (Cohen's d)**: Standardized difference between paired measurements
- **Expected Correlation (ρ)**: Correlation between paired observations (0.01-0.99, default 0.50)
- **Statistical Power**: Probability of detecting an effect if it exists (typically 0.80)
- **Significance Level (alpha)**: Risk of Type I error (typically 0.05)
- **Expected Dropout Rate**: Percentage of participants expected to drop out (0-50%)

#### Two Proportions Mode
- **Baseline Rate / Control Group**: Expected proportion in the control group (e.g., 0.50)
- **Expected Treatment Rate**: Expected proportion in the treatment group (e.g., 0.70)
- **Cohen's h**: Effect size calculated automatically from the two proportions
- **Statistical Power**: Probability of detecting an effect if it exists (typically 0.80)
- **Significance Level (alpha)**: Risk of Type I error (typically 0.05)
- **Expected Dropout Rate**: Percentage of participants expected to drop out (0-50%)

## Methodological References

The GPower tool's calculations are based on established statistical methods and implemented using a widely-cited, open-source Python library. We recommend citing the following works in your research to validate the methodological approach:

### Foundational Theory (Power Analysis & Effect Sizes)

The principles of power analysis and the conventions for effect sizes (Cohen's *d*, *f*, and *h*) are based on the seminal work in this field:

> **Cohen, J. (1988). [*Statistical power analysis for the behavioral sciences*](https://doi.org/10.4324/9780203771587) (2nd ed.). Lawrence Erlbaum Associates.**

### Computational Engine

The real-time calculations rely on the statistical models implemented in the Python `statsmodels` library, which is run in the browser via Pyodide. This library provides the power functions for Means (T-Test/ANOVA) and Proportions (Normal Approximation).

> **Seabold, S., & Perktold, J. (2010). [*Statsmodels: Econometric and statistical modeling with python*](https://proceedings.scipy.org/articles/Majora-92bf1922-011). *Proceedings of the 9th Python in Science Conference*.**

***

***

## Citation

To ensure you use the most current and accurate citation for this software, please use the citation feature provided by GitHub.

Click the **"Cite this repository"** button (usually visible on the right sidebar of the GitHub repository page) to find various formats (e.g., APA, BibTeX) generated automatically from the `CITATION.cff` file.

***

## License

This project is open source and available under the MIT License.
