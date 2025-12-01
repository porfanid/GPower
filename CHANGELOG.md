# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.1.0] - 2025-12-01

### Added

-   **Sensitivity Analysis Chart**: Interactive visualization showing the relationship between Required Sample Size (N) and Effect Size. Features include:
    -   Real-time chart generation using Matplotlib
    -   Cohen's conventions marked as vertical dashed lines (Small/Medium/Large)
    -   Current effect size position highlighted with a red dot
    -   Professional, publication-ready chart output
    -   Base64-encoded PNG images for seamless display

-   **Paired T-Test Analysis**: New analysis type for dependent samples (before/after designs):
    -   New dropdown option: "Paired T-Test (Before/After)"
    -   Correlation slider (ρ) for expected correlation between paired measurements (0.01-0.99)
    -   Adjusted effect size formula: d_adj = d / √(1 - ρ)
    -   Accounts for reduced variance in paired designs, requiring fewer participants

### Changed

-   **Enhanced Python Engine**: Now loads matplotlib in addition to statsmodels for chart generation
-   **Updated Documentation**: README updated with new features and parameters
-   **Improved Chart Styling**: Uses manual matplotlib styling compatible with Pyodide (replaced seaborn styles)

## [2.0.0] - 2025-11-30

### Added

-   **Two Proportions Power Analysis**: New analysis type for calculating sample sizes when comparing two independent proportions (dichotomous outcomes), using Cohen's *h* effect size. Ideal for clinical trials comparing treatment vs. control success rates.
-   **Real-time Cohen's h Display**: Cohen's h effect size is now calculated and displayed in real-time as users adjust the baseline and treatment proportions.
-   **Dropout Rate Adjustment**: New slider (0-50%) to account for expected participant dropouts, available in both Groups and Proportions modes. Sample size is adjusted using the formula: Required Sample = Theoretical Sample / (1 - Dropout Rate).
-   **Analysis Type Selector**: Dropdown menu to switch between "Groups (T-Test / ANOVA)" and "Two Proportions" analysis modes.

### Changed

-   **Updated Labels**: Proportion inputs now use clearer labels: "Baseline Rate / Control Group" and "Expected Treatment Rate".
-   **Enhanced Results Display**: When dropout rate is set, results show both adjusted and theoretical sample sizes.
-   **Updated Documentation**: README, CITATION.cff, and .zenodo.json updated to reflect new features.

## [1.0.0] - 2025-03-15

### Added

-   Initial stable release of the GPower Web Tool.
-   **T-Test Power Analysis**: Added functionality to calculate required sample sizes for independent samples T-tests using Cohen's *d* effect size.
-   **ANOVA Power Analysis**: Added functionality to calculate required sample sizes for one-way ANOVA (3+ groups) using Cohen's *f* effect size.
-   **Real-time Calculation Engine**: Implemented Pyodide (Python in WebAssembly) to run the `statsmodels` power analysis library entirely in the browser.
-   **Documentation**: Included core repository documentation: `README.md`, `CONTRIBUTING.md`, and `CODE_OF_CONDUCT.md`.
-   **Citation Setup**: Added `CITATION.cff` and `.zenodo.json` files to ensure the project is easily citable and archivable with a unique DOI.
-   **Licensing**: The project is released under the **MIT License**.
