# Comparing False Discovery Proportion (FDP) Methods

A comparison of three different methods for controlling the False Discovery Rate (FDR) or False Discovery Proportion (FDP) in multiple hypothesis testing.

## Methods Compared

1. **Benjamini-Hochberg (BH)**: The classic FDR control procedure
2. **q-value (Storey)**: An improved FDR estimation method  
3. **permFDP**: A permutation-based approach for controlling FDP

## Simulation Model

The analysis uses the SIMPLYCORRECT realistic model (Model 3), where biological variability determines which features are truly null. This provides a more realistic simulation of quantitative omics experiments compared to simpler models.

### Default Parameters

- **m** = 800 features
- **nc** = 10 control samples
- **nt** = 10 treatment samples
- **effectSD** = 1 (typical effect magnitude)
- **bioVar** = 0.05 (biological variability)
- **bioVGamma** = c(4, 0.5) (gamma distribution parameters)
- **expVar** = 0.03 (technical variability)

## Requirements

### R Packages

```r
install_github("jdstorey/qvalue")
install_github('steven-shuken/permFDP')
install.packages("knitr")
```

### Quarto

This analysis is built with [Quarto](https://quarto.org/). To render the document:

```bash
quarto render compareFDP.qmd --to html
```

### Results
The rendered HTML file is available [here](https://www.mheming.com/compareFDP/).

## Reference

This simulation is based on the [SIMPLYCORRECT](https://github.com/steven-shuken/SIMPLYCORRECT) Shiny application by Steven Shuken, which provides interactive visualization of multiple hypothesis correction methods.
