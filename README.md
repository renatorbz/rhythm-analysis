# Circadian Rhythm Analysis Using R

This R Markdown document provides a workflow for analyzing circadian rhythms based on the expression levels of biological variables associated with circadian regulation. The analysis is performed using the R package *circacompare*, developed by Rex Parsons<sup>1</sup>. It is designed to characterize circadian patterns and estimate key parameters describing the rhythmic profiles of the biological variables under investigation.

## Requirements

To run this analysis, you will need:

- **R**;
- **RStudio**;
- A data table in **.xlsx** format;
- The following R packages installed: `circacompare`, `ggplot2`, `readxl`, and `here`.

If you have no prior experience with R, consider starting [here](https://rpubs.com/Wylliam_alves/1386150).

Please note that this tutorial does not cover the installation or configuration of R, RStudio, or the required packages.

## Data table structure

Your data must be organized according to the following structure:

- **Column A:** Sampling time (time of sample collection);
- **Column B:** Experimental group;
- **Columns C onward:** Measured variables.

The data table must not contain empty cells. If a measurement is missing, enter `NA` in the corresponding cell.

Each row must represent the measurements obtained for a given experimental group at a specific sampling time.

See Figure 1 for an example of the required data structure.

*Figure 1. Example of the data table structure.*

## Running the circadian rhythm analysis

Before running the analysis, make sure that the R Markdown document *rhythm_0.02.Rmd* is saved in a directory of your choice. Within this directory, create a subdirectory named `data` and save your Excel data file there, as illustrated in Figure 2.

*Figure 2. Recommended directory structure.*

In RStudio, open the file *rhythm_0.02.Rmd*.

### 1. Specify the input data file

Locate the following code chunk:

```r
df <- read_excel(
  "data/example.xlsx", sheet = "spreadsheet",
  .name_repair = "minimal"
)
```

Replace `example.xlsx` with the name of your Excel file. Make sure that the worksheet name specified in `sheet` matches the name of the worksheet containing your data.

### 2. Select the variable to be analyzed

Locate the following code chunk:

```r
mv <- "mv1"

cat(
  "Gene to be analyzed: ",
  mv,
  ".\n"
)
```

Replace `mv1` with the name of the variable you wish to analyze, exactly as it appears in the corresponding column header of your data table.

Although the current code uses the object name `gene`, the analysis can be applied to any measured biological variable included in your dataset, provided that the data are suitable for circadian rhythm analysis.

### 3. Generate the analysis report

Once you have specified the input file and the variable of interest, click **Knit** in RStudio to execute the R Markdown document.

The analysis workflow will generate a report in HTML or PDF format, depending on the output format configured in the R Markdown document.

### 4. Reference
1. Rex Parsons, Richard Parsons, Nicholas Garner, Henrik Oster, Oliver Rawashdeh, CircaCompare: a method to estimate and statistically support differences in mesor, amplitude and phase, between circadian rhythms, *Bioinformatics*, Volume 36, Issue 4, February 2020, Pages 1208–1212, <https://doi.org/10.1093/bioinformatics/btz730>
