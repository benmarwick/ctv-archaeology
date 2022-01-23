---
name: Archaeology
topic: Archaeology
maintainer: Ben Marwick
email: benmarwick@gmail.com
version: 2022-01-22
source: https://github.com/cran-task-views/Archaeology
---

This task view is a list of packages useful for many kinds of archaeological science. It includes packages widely used by archaeologists, packages for working with distinctive types of archaeological analyses, such as radiocarbon ages, artefact types and faunal remains, packages containing archaeological datasets, and packages from closely related sciences such as environmental science. 

Many relevant packages can also be found in other CRAN Task Views, especially [Environmetrics](https://cran.r-project.org/web/views/Environmetrics.html), [Spatial](https://cran.r-project.org/web/views/Spatial.html) [Multivariate](https://cran.r-project.org/web/views/Multivariate.html), [Phylogenetics](https://cran.r-project.org/web/views/Phylogenetics.html), [Cluster](https://cran.r-project.org/web/views/Cluster.html), and [SpatioTemporal](https://cran.r-project.org/web/views/SpatioTemporal.html) task views.


### Dating

-    Radiocarbon dates can be calibrated using `r pkg("Bchron")` with various calibration curves (including user generated ones); also does Age-depth modelling, relative sea level rate estimation incorporating time uncertainty in polynomial regression models; and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM).
-    `r pkg("rcarbon")` for basic calibration, modelling, hypothesis testing, and 
-    Bayesian age-depth modelling of radiocarbon dates is also available in `r pkg("nimbleCarbon")` and `r pkg("clam")`.
-    `r pkg("c14bazAAR")` for the retrieval and preparation of large radiocarbon datasets.
-    The `r pkg("oxcAAR") package allows you to use R to connect to a local installation of the OxCal software to calibrate radiocarbon dates and a variety of other OxCal operations.
- `r pkg("ArchaeoPhases")` provides statistical tools to analyze and to estimate archaeological phases from the posterior distribution (i.e. MCMC samples) of a sequence of dates. Includes testing procedures to check the presence of a gap between two successive phases or periods.
-    Various R functions for Luminescence Dating data analysis are in the `r pkg("Luminescence")` package (including radial plotting) and in the `r pkg("numOSL")` package, including equivalent dose calculation, annual dose rate determination, growth curve fitting, decay curve decomposition, statistical age model optimization, and statistical plot visualization.
-    The `r github("davidcorton/archSeries")` package makes chronologies from information from multiple entities with varying chronological resolution and overlapping date ranges
-    The r github("UCL/ADMUR")` package provides tools to directly model underlying population dynamics using chronological datasets (radiocarbon and other) with a variety of models, including Continuous Piecewise Linear (CPL) model framework, and model comparison framework using BIC.
- `r pkg("SPARTAAS")` Statistical pattern recognition and dating using archaeological artefacts assemblages.
