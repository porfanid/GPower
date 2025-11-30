# GPower

[![DOI](https://zenodo.org/badge/1106672819.svg)](https://doi.org/10.5281/zenodo.17768003)

A web-based sample size calculator for statistical power analysis, supporting ANOVA and T-Test calculations.

## Usage

Simply visit the [GPower Web Tool](https://porfanid.github.io/GPower/) in a modern web browser. The tool will:

1. Load the Python statistics engine (statsmodels)
2. Present an interactive interface for entering parameters
3. Calculate required sample sizes in real-time

## Features

- **T-Test Power Analysis**: Calculate required sample sizes for independent samples t-tests using Cohen's d effect size
- **ANOVA Power Analysis**: Calculate required sample sizes for one-way ANOVA using Cohen's f effect size
- **Interactive Interface**: Real-time calculations with intuitive sliders and input controls
- **Effect Size Presets**: Quick selection of small, medium, and large effect sizes based on Cohen's conventions
- **Mobile Responsive**: Works seamlessly on both desktop and mobile devices
- **No Installation Required**: Runs entirely in your browser using Pyodide (Python in WebAssembly)

### Parameters

- **Number of Groups**: 2 for T-test, 3+ for ANOVA
- **Effect Size**: Expected magnitude of the effect (Cohen's d for T-test, Cohen's f for ANOVA)
- **Statistical Power**: Probability of detecting an effect if it exists (typically 0.80)
- **Significance Level (alpha)**: Risk of Type I error (typically 0.05)

## Methodological References

The GPower tool's calculations are based on established statistical methods and implemented using a widely-cited, open-source Python library. We recommend citing the following works in your research to validate the methodological approach:

### Foundational Theory (Power Analysis & Effect Sizes)

The principles of power analysis and the conventions for effect sizes (Cohen's *d* and *f*) are based on the seminal work in this field:

> **Cohen, J. (1988). [*Statistical power analysis for the behavioral sciences*](https://doi.org/10.4324/9780203771587) (2nd ed.). Lawrence Erlbaum Associates.**

### Computational Engine

The real-time calculations rely on the statistical models implemented in the Python `statsmodels` library, which is run in the browser via Pyodide.

> **Seabold, S., & Perktold, J. (2010). [*Statsmodels: Econometric and statistical modeling with python*](https://proceedings.scipy.org/articles/Majora-92bf1922-011). *Proceedings of the 9th Python in Science Conference*.**

***

## Citation

To ensure you use the most current and accurate citation for this software, please use the citation feature provided by GitHub.

Click the **"Cite this repository"** button (usually visible on the right sidebar of the GitHub repository page) to find various formats (e.g., APA, BibTeX) generated automatically from the `CITATION.cff` file.

***

## License

This project is open source and available under the MIT License.
