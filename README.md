
# Circadian Rhythm Analysis Using R

**Authors:** Renato Barboza and Maria Nathalia Moraes

## Overview

This repository provides an R Markdown-based workflow for circadian rhythm analysis using the R package `circacompare`.

The script is designed to assist researchers in analyzing measured variables associated with circadian rhythms, including gene expression data, and generating reports with statistical results and graphical representations.

## Authors

- **Renato Barboza** — ORCID: [0000-0002-6441-7513](https://orcid.org/0000-0002-6441-7513)
- **Maria Nathalia Moraes** — ORCID: [0000-0003-2479-4477](https://orcid.org/0000-0003-2479-4477)

## Repository

[GitHub – rhythm-analysis](https://github.com/renatorbz/rhythm-analysis)

## Requirements

- R
- RStudio (recommended)
- R package `circacompare`
- Additional packages required by the R Markdown script.

Install the principal package using:

```r
install.packages("circacompare")
```

Check the R Markdown document for the complete list of dependencies.

## How to use

1. Clone or download this repository.
2. Open the R Markdown file (`.Rmd`) in RStudio.
3. Install the required packages.
4. Configure the input data file and its location.
5. Check the variable names and data structure.
6. Select the variable to be analyzed, when applicable.
7. Run the code chunks or render the R Markdown document.

The input-data structure and analysis parameters must follow the specifications provided in the script.

## Analysis and results

The workflow uses the `circacompare` package to perform circadian rhythm analysis.

Depending on the selected analysis, the generated report may include:

- Statistical assessment of rhythmicity;
- Model parameter estimates;
- Circadian phase and peak-time estimates;
- Comparisons between experimental groups;
- Graphical representations of the results.

Results should be interpreted in consideration of the experimental design, sampling schedule, sample size, biological variability, and statistical assumptions.

Statistical significance alone does not establish a biological circadian mechanism.

For information about the statistical methods and the package citation, run:

```r
citation("circacompare")
```

## Reproducibility

For reproducible research, users should:

- Cite the specific software version used;
- Report the R version and relevant package versions;
- Preserve the original input data;
- Document data preprocessing and modifications;
- Retain the analysis settings used to generate the results.

Do not upload confidential, identifiable, or restricted data to this public repository.

## How to cite

If you use this software in a scientific publication, presentation, or other research output, please cite the specific version archived in Zenodo.

Suggested citation:

Barboza, R., & Moraes, M. N. (YEAR). *Circadian Rhythm Analysis Using R* (Version VERSION) [Computer software]. Zenodo. https://doi.org/DOI

Replace YEAR, VERSION, and DOI with the information assigned to the corresponding Zenodo release.

The `CITATION.cff` file provides machine-readable citation metadata and allows GitHub to display the repository citation information.

## License

This project is intended to be distributed under the MIT License.

See the `LICENSE` file for the complete license terms.

The license applies to the original material provided in this repository. Third-party software and packages remain subject to their respective licenses.

## Disclaimer

This software is provided for research and educational purposes.

Users are responsible for checking their data, verifying model assumptions, and interpreting the results appropriately.
