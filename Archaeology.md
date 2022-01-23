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


### Datasets

-   `r pkg("archdata")` contains eleven archaeological datasets from around the world reported in published studies. These represent typical forms of archaeological data (and so are useful for teaching)
-   `r pkg("binford")` contains more than 200 variables coding aspects of hunter-gatherer subsistence, mobility, and social organization for 339 ethnographically documented groups of hunter-gatherers, as used in Binford (2001) _Constructing Frames of Reference: An Analytical Method for Archaeological Theory Building Using Ethnographic and Environmental Data Sets_
- `r github("geanes/bioanth")` contains three osteometric datasets useful for biological and forensic anthropology.
-  `r pkg("BSDA")` contains a dataset of 60 radiocarbon ages of observations taken from an archaeological site with four phases of occupation.
-  `r github("sfsheath/cawd")` contains 15 datasets of ancient Greek, Roman and Persian maps and digital atlas data
-  `r pkg("chemometrics")` contains a dataset of elemental concentrations for 180 archaeological glass vessels excavated from 15th - 17th century contexts in Antwerp.
-  `r pkg("zooaRch")` contains two zooarchaeological datasets.
-  `r pkg("gsloid")` Contains published data sets for global benthic d18O data for 0-5.3 Myr and global sea levels based on marine sediment core data for 0-800 ka
- `r github("benmarwick/evoarchdata")` contains four published datasets widely used in archaeological studies of cultural evolution
- `r github("tesselle/fasti")` contains two datasets for chronological modelling with `r pkg("ArchaeoPhases")`.
- `r github("ropensci/c14bazAAR")` contains over 20 datasets of radiocarbon ages from around the world. 
-  `r pkg("folio")` provides several types of data related to broad topics (cultural evolution, radiocarbon dating, paleoenvironments, etc.), which can be used to illustrate statistical methods in the classroom (multivariate data analysis, compositional data analysis, diversity measurement, etc.).

### Analysis of dates (radiocarbon, etc.) and chronological patterns

-    Radiocarbon dates can be calibrated using `r pkg("Bchron")` with various calibration curves (including user generated ones); also does Age-depth modelling, relative sea level rate estimation incorporating time uncertainty in polynomial regression models; and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM).
-    `r pkg("rcarbon")` for basic calibration, modelling, hypothesis testing, and 
-    Bayesian age-depth modelling of radiocarbon dates is also available in `r pkg("nimbleCarbon")` and `r pkg("clam")`.
-    `r github("ropensci/c14bazAAR")` for the retrieval and preparation of large radiocarbon datasets.
-    The `r pkg("oxcAAR") package allows you to use R to connect to a local installation of the OxCal software to calibrate radiocarbon dates and a variety of other OxCal operations.
- `r pkg("ArchaeoPhases")` provides statistical tools to analyze and to estimate archaeological phases from the posterior distribution (i.e. MCMC samples) of a sequence of dates. Includes testing procedures to check the presence of a gap between two successive phases or periods.
-    Various R functions for Luminescence Dating data analysis are in the `r pkg("Luminescence")` package (including radial plotting) and in the `r pkg("numOSL")` package, including equivalent dose calculation, annual dose rate determination, growth curve fitting, decay curve decomposition, statistical age model optimization, and statistical plot visualization.
-    The `r github("davidcorton/archSeries")` package makes chronologies from information from multiple entities with varying chronological resolution and overlapping date ranges
-    The r github("UCL/ADMUR")` package provides tools to directly model underlying population dynamics using chronological datasets (radiocarbon and other) with a variety of models, including Continuous Piecewise Linear (CPL) model framework, and model comparison framework using BIC.
- `r pkg("SPARTAAS")` provides statistical pattern recognition and dating using archaeological artefacts assemblages.
- `r pkg("aoristic")`, `r pkg("kairos")` and `r github("ISAAKiel/aoristAAR")` provide functions for the aoristic analysis of archaeological data (takes into account the uncertainty of the exact moment that an event occurred when examining the overall incidence of events over time)
- `r pkg("kairos")` provides functions for mean ceramic date estimation
- `r github("joeroe/c14")` provides basic classes and functions for radiocarbon data in R. It makes it easier to combine methods from several existing packages (e.g. rcarbon, Bchron, oxcAAR, c14bazAAR, ArchaeoPhases, stratigraphr) together and work with them in a tidy data workflow.

### Survey, excavation, and stratigraphic analysis

- `r pkg("archeofrag")` for refitting and stratigraphic analysis in archaeology
- `r pkg("recexcavAAR")` for 3D reconstruction and analysis of excavations, provides methods to reconstruct natural and artificial surfaces based on field measurements. This allows to spatially contextualize documented subunits and features. 
- `r pkg("ISAAKiel/profileAAR")` provides a QGIS plugin to transforms profile control points for photogrammetric rectification from archaeological excavation
- `r github("joeroe/stratigraphr")` provides a tidy framework for working with archaeological stratigraphy and chronology in R. It includes tools for reading, analysing, and visualising stratigraphies (Harris matrices) and sequences as directed graphs; helper functions for using radiocarbon dates in a tidy data analysis; and an R interface to OxCal's Chronological Query Language (CQL).
- `r github("joeroe/fieldwalkr")` for designing and evaluating sampling strategies in spatial survey (fieldwalking in archaeological jargon). It contains functions for simulating the effect of different survey units, sampling methods and detection functions on the estimation of randomly generated or observed point processes.

