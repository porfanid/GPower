# GPower

[![DOI](https://zenodo.org/badge/951497112.svg)](https://doi.org/10.5281/zenodo.15053975)

A web-based sample size calculator for statistical power analysis, supporting ANOVA and T-Test calculations.

## Features

- **T-Test Power Analysis**: Calculate required sample sizes for independent samples t-tests using Cohen's d effect size
- **ANOVA Power Analysis**: Calculate required sample sizes for one-way ANOVA using Cohen's f effect size
- **Interactive Interface**: Real-time calculations with intuitive sliders and input controls
- **Effect Size Presets**: Quick selection of small, medium, and large effect sizes based on Cohen's conventions
- **Mobile Responsive**: Works seamlessly on both desktop and mobile devices
- **No Installation Required**: Runs entirely in your browser using Pyodide (Python in WebAssembly)

## Usage

Simply open `index.html` in a modern web browser. The tool will:

1. Load the Python statistics engine (statsmodels)
2. Present an interactive interface for entering parameters
3. Calculate required sample sizes in real-time

### Parameters

- **Number of Groups**: 2 for T-test, 3+ for ANOVA
- **Effect Size**: Expected magnitude of the effect (Cohen's d for T-test, Cohen's f for ANOVA)
- **Statistical Power**: Probability of detecting an effect if it exists (typically 0.80)
- **Significance Level (alpha)**: Risk of Type I error (typically 0.05)

## Live Demo

Visit the [GPower Web Tool](https://porfanid.github.io/GPower/) to use the calculator online.

## Citation

If you use this tool in your research, please cite it using the following:

> Orfanidis, P. (2025). GPower: Web-based Sample Size Calculator for ANOVA and T-Test (Version 1.0.0) [Computer software]. https://doi.org/10.5281/zenodo.15053975

### BibTeX

```bibtex
@software{orfanidis_gpower_2025,
  author       = {Orfanidis, Pavlos},
  title        = {GPower: Web-based Sample Size Calculator for ANOVA and T-Test},
  year         = 2025,
  publisher    = {Zenodo},
  version      = {1.0.0},
  doi          = {10.5281/zenodo.15053975},
  url          = {https://doi.org/10.5281/zenodo.15053975}
}
```

## License

This project is open source and available under the MIT License.

## Author

**Pavlos Orfanidis**

---

[![DOI](https://zenodo.org/badge/951497112.svg)](https://doi.org/10.5281/zenodo.15053975)
