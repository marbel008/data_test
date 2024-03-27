# ECI Project

[![DOI](https://sandbox.zenodo.org/badge/777672359.svg)](https://sandbox.zenodo.org/doi/10.5072/zenodo.41515)

This project is about the development of a formula to estimate an embryonic competence index based on the expression of eight biomarker genes

## Project Structure
To run this project, the user needs to input the RNA sequencing file as raw counts. ENSEMBL Gene IDs should be used as Gene IDs.

## Required Dtasets
The function should executed using the "dataTrain.txt" file found in the train folder. An example dataset is inside the Example folder (both inside the data folder)

```
.
├── .gitignore
├── CITATION.cff
├── LICENSE
├── README.md
├── requirements.txt
├── data               <- All project data, ignored by git
│   ├── train          <- The required dataset for training the model
│   ├── example        <- Example datasets
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Jupyter, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── R                  <- Source code for this project (HW)

```

## Required R packages
library(scales)
library(DESeq2)
library(bapred)

Enter the following if (any) of these packages are not installed: 
install.packages("scales")
install.packages("bapred")

if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("DESeq2")



## citation
cff-version: 1.2.0
title: ECI
message: >-
  If you use this software, please cite it using the
  metadata from this file.
type: software
authors:
  - given-names: Belen
    family-names: Rabaglino
    email: m.b.rabaglino@uu.nl
    affiliation: Utrecht University
  - given-names: Peter
    family-names: Hansen
    email: pjhansen@ufl.edu
    affiliation: University of Florida
abstract: >-
  This project is derived from: M. B. Rabaglino, D.
  Salilew-Wondim, A. Zolini, D. Tesfaye, M. Hoelker, P.
  Lonergan, P. Hansen. FASEB J 2023 Vol. 37 Issue 3 Pages
  e22809.

## License

This project is licensed under the terms of the [MIT License](/LICENSE).
