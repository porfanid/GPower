# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-03-15

### Added

-   Initial stable release of the GPower Web Tool.
-   **T-Test Power Analysis**: Added functionality to calculate required sample sizes for independent samples T-tests using Cohen's *d* effect size.
-   **ANOVA Power Analysis**: Added functionality to calculate required sample sizes for one-way ANOVA (3+ groups) using Cohen's *f* effect size.
-   **Real-time Calculation Engine**: Implemented Pyodide (Python in WebAssembly) to run the `statsmodels` power analysis library entirely in the browser.
-   **Documentation**: Included core repository documentation: `README.md`, `CONTRIBUTING.md`, and `CODE_OF_CONDUCT.md`.
-   **Citation Setup**: Added `CITATION.cff` and `.zenodo.json` files to ensure the project is easily citable and archivable with a unique DOI.
-   **Licensing**: The project is released under the **MIT License**.
