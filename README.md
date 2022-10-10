# PLATCOV-Remdesivir-Regeneron

``Clinical antiviral efficacy of remdesivir and casirivimab/imdevimab against the SARS-CoV-2 Delta and Omicron variants''

This repository provides code and data for the analysis of the casirivimab/imdevimab (Regeneron monoclonal antibody) and remdesivir arms of the PLATCOV trial.

The repository is structured as follows:

* *Paper2_analysis.csv* is the dataset
* *Full_Analysis.Rmd* is an RMarkdown file which sets up all analyses and generates all plots
* *run_models_local.R* runs all models (*run_models.R* is written for remote cluster)
* The folder *Stan_models* contains stan code for the linear and nonlinear regression models
* *functions.R* has a bunch of useful functions for making the stan datasets and plotting output.

All the analyses are done in the RMarkdown file *Full_Analysis.Rmd*. There are 7 datasets used (see Supplementary Materials of the paper), and 5 models fitted per data set (total of 35 model fits).

The statistical analysis plan used to guide the analyses is given in *PLATCOV_SAP_v2.2_21092022.pdf*. 

The following R packages are needed:

* *rstan* (compile and fit stan models)
* *loo* (model comparison)
* *RColorBrewer* (nice colors)
* *brms* (sanity check handwritten stan models)
* *plotrix* (gap plots)


Analysis is still work in progress - drop me a message at jwatowatson at gmail dot com if you spot any errors...
