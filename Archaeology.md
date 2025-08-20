---
name: Archaeology
topic: Archaeology
maintainer: Ben Marwick, Bjørn Peare Bartholdy, Nicolas Frerebeau, Sam Leggett, Sarah Pederzani, Joe Roe, Sophie C. Schmidt, Laure Spake, Lisa Steinmann, Liying Wang, Jesse Wolfhagen
email: benmarwick@gmail.com
version: 2025-08-20
source: https://github.com/cran-task-views/Archaeology
---

This task view is a list of packages useful for archaeological science. It includes packages for working with distinctive types of archaeological data, such as radiocarbon ages, various types of artefacts (lithics, pottery, etc.), faunal remains, geoarchaeological and landscape data, packages containing archaeological datasets, and packages from closely related sciences, such as environmental science, that are widely used by archaeologists. This is a list to help archaeologists in their search for packages relevant to their research. It does not include packages for general purpose tasks such as importing/exporting data, data manipulation, common forms of data analysis and visualization, and doing reproducible research. These may be found in other CRAN Task Views, especially `r view("Environmetrics")`, `r view("Spatial")`, `r view("Multivariate")`, `r view("Phylogenetics")`, `r view("Cluster")`, `r view("ReproducibleResearch")`, `r view("WebTechnologies")`, `r view("MachineLearning")`, and `r view("SpatioTemporal")`. To minimise overlap we do not include those packages in this list. This list assumes some familiarity with using R and is not an introduction to using R in archaeology (see the links below for introductory resources).

Within each thematic section, you will find first the packages distributed on CRAN, followed by a selection of code projects in other repositories. Please keep in mind that the order in which packages are listed should not be taken as an indicator of quality or endorsement.

If you have any questions feel free to reach out to the task view maintainers or the maintainers of specific packages. If there is an archaeological science package on CRAN or elsewhere that we have missed, please let us know. Contributions are always welcome, and encouraged -- please see the linked GitHub repository for details.

If you are looking for more open source archaeological software and resources (including R packages), [open-archeo](https://open-archaeo.info/) is the ideal complement to this taks view.

### Analysis of Dates and Chronological Patterns

#### Radiometric Dating

Radiocarbon ages can be calibrated using many of the packages in this section:

- `r pkg("rcarbon", priority = "core")` is useful for calibration, and also contains extensively documented functions for hypothesis testing and modelling radiocarbon ages. See Crema and Bevan ([2021](https://doi.org/10.1017/RDC.2020.95)) for an introduction. Basic calibration is also possible with `r pkg("rintcal")`.
- `r pkg("Bchron")` adds various calibration curves (including user generated ones); also does age-depth modelling, relative sea level rate estimation incorporating time uncertainty in polynomial regression models, and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM). `r pkg("clam")` similarly does 'classical' age-depth modelling of deposits.
- `r pkg("ananke")` allows simple radiocarbon calibration and chronological analysis. It also provides tools for visualising results and estimating statistical summaries.
- Bayesian age-depth modelling of radiocarbon dates is available in `r pkg("nimbleCarbon")` and `r pkg("rbacon")`.
- `r pkg("coffee")` uses Bayesian methods to enforce the chronological ordering of radiocarbon and other dates, for example for trees with multiple radiocarbon dates spaced at exactly known intervals.
- `r pkg("oxcAAR")` allows you to use R to connect to a local installation of the OxCal software to calibrate radiocarbon dates and a variety of other OxCal operations.
- `r pkg("ArchaeoPhases")` allows you to post-process Markov Chain Monte Carlo (MCMC) simulations from [ChronoModel](https://chronomodel.com/), [Oxcal](https://c14.arch.ox.ac.uk/oxcal.html) or [BCal](https://bcal.shef.ac.uk/). It provides statistical tools to analyze and to estimate archaeological phases from the posterior distribution of a sequence of dates and includes testing procedures to check the presence of a gap between two successive phases.
- `r pkg("spDates")` allows analysis of spatial gradients in radiocarbon dates.
- `r pkg("IsoplotR")` offers a statistical toolbox for radiometric geochronology.

- `r github("ropensci/c14bazAAR")` facilitates retrieval and preparation of large radiocarbon datasets.
- `r github("tonydoss/UThwigl")` computes closed- and open-system uranium-thorium (U-Th) ages of geological and archaeological samples.
- The `r github("UCL/ADMUR")` package provides tools to directly model underlying population dynamics using chronological datasets (radiocarbon and other) with a variety of models, including Continuous Piecewise Linear (CPL) model framework, and model comparison framework using BIC.
- `r github("ArchaeoStat/ArchaeoChron")` allows basic radiocarbon calibration and Bayesian combination of radiocarbon dates.

#### Dendrochronology

- `r pkg("dendroNetwork")` allows to create dendrochronological networks based on the similarity between tree-ring series or chronologies.
- `r github("ropensci/fellingdater")` offers a suite of functions designed to assist dendrochronologists in inferring estimates for felling dates, derived from dated tree-ring series.

#### Luminescence Dating

- Various R functions for Luminescence Dating data analysis are in the `r pkg("Luminescence")` and `r pkg("numOSL")` packages, including equivalent dose calculation, annual dose rate determination, growth curve fitting, decay curve decomposition, statistical age model optimization, and statistical plot visualization.
- `r pkg("BayLum")` provides chronological bayesian models integrating Optically Stimulated Luminescence and radiocarbon age dating.

#### Paleoenvironmental Proxies

- `r pkg("rpaleoclim")` provides a simple interface for downloading [PaleoClim](http://www.paleoclim.org/) data in R, with support for caching and filtering retrieved data by period, resolution, and geographic extent.
- `r pkg("shoredate")` offers methods to shoreline date coastal sites based on their present-day elevation and the trajectory of past relative sea-level change.
- `r pkg("tidypaleo")` provides a set of functions for age-depth model management, stratigraphic visualization, and common statistical transformations.

#### Archaeological Time Series

- `r pkg("era")` provides a consistent representation of year-based time scales as a numeric vector with an associated era. `r pkg("aion")` contains a toolkit for handling archaeological time series.
- `r pkg("aoristic")` and `r pkg("kairos")` provide functions for the aoristic analysis of archaeological data (takes into account the uncertainty of the exact moment that an event occurred when examining the overall incidence of events over time).
- `r pkg("kairos")` provides functions for mean ceramic date estimation.
- `r pkg("SPARTAAS")` and `r pkg("kairos")` provide methods for statistical pattern recognition, time range plotting and seriation plots of archaeological artefacts.
- `r pkg("eratosthenes")` provides a coherent foundation for archaeological chronology-building by incorporating, computationally, all relevant sources of information on uncertain archaeological or historical dates.
- `r pkg("datplot")` converts date ranges into dating 'steps' to ease the visualization of changes in e.g. pottery consumption, style and other variables over time.
- `r pkg("chronochrt")` offers an easy way to draw chronological charts from tables.

### Artefact Analysis

- `r pkg("tabula", priority = "core")` provides several tests and measures of diversity: heterogeneity and evenness (Brillouin, Shannon, Simpson, etc.), richness and rarefaction (Chao1, Chao2, ACE, ICE, etc.), turnover and similarity (Brainerd-Robinson, etc.). The package make it easy to visualize count data and statistical thresholds: rank vs. abundance plots, heatmaps, Ford (1962) and Bertin (1977) diagrams.
- `r pkg("lakhesis")` provides an interactive platform and critical measures for seriating binary data matrices through the exploration, selection, and consensus of partially seriated sequences.

- `r github("zoometh/iconr")` for modeling prehistoric iconographic compositions and preparing for further analysis (clustering, typology tree, Harris diagram, etc.).

### Zooarchaeological Analysis

- `r pkg("zoolog", priority = "core")` to generate and manipulate log-ratios (also known as log size index (LSI) values) from measurements obtained on zooarchaeological material.

### Mortuary Analysis

- `r pkg("mortAAR", priority = "core")` calculates a life table based on archaeological demographic data.
- `r pkg("JSDNE")` calculates the age at death from human skeletal remains using the Dirichlet Normal Energy (DNE) on the whole auricular surface and the apex of the auricular surface. The package includes data from the Louis Lopes Collection in Lisbon, the 21st Century Identified Human Remains Collection in Coimbra, and the CAL Milano Cemetery Skeletal Collection in Milan.

### Geoarchaeological Analysis

- `r pkg("aqp")` simplifies the quantitative analysis of soil profile data. It allows soil profile visualization, aggregation, and classification. `r pkg("G2Sd")` and `r pkg("EMMAgeo")` can be used for working with sedimentary grain-size data in logarithmic (phi) and geometric (micrometers) scales, based on various methods.
- `r pkg("SIBER")`, `r pkg("MixSIAR")` and `r pkg("simmr")` provide methods for working with isotope data.
- `r pkg("munsell")` provides methods for working with sediment colour.
- `r pkg("nexus")` provides tools for compositional data analysis, chemical fingerprinting and source tracking of ancient materials.
- `r pkg("isopleuros")` allows creation of ternary plots. It also includes common ternary diagrams useful for the archaeologist (e.g. soil texture charts, ceramic phase diagram).
 
### Landscape Analysis

- `r pkg("leastcostpath", priority = "core")` calculates Least Cost Paths (LCPs) using numerous time- and energy-based cost functions that approximate the difficulty of moving across a landscape.
- `r pkg("skyscapeR")` for data reduction, visualization and analysis in skyscape archaeology, archaeoastronomy and cultural astronomy.

- `r github("SCSchmidt/percopackage")` implements percolation Analysis as a 2D point pattern analysis technique for identifying clusters of any size and form (e.g. of archaeological sites).
- `r github("nevrome/bleiglas")` calculates of three-dimensional Voronoi diagrams from input point clouds for spatiotemporal applications in archaeology.

### Survey, Excavation, and Stratigraphic Analysis

- `r pkg("archeoViz")` is a packaged R Shiny application for the 2D and 3D visualization, exploration, and web communication of spatial data from archaeological excavations.
- `r pkg("archeofrag")` for refitting and stratigraphic analysis in archaeology (`r pkg("archeofrag.gui")` provides a graphical user interface that implements and complements some features of the `archeofrag` package).
- `r pkg("recexcavAAR")` for 3D reconstruction and analysis of excavations, provides methods to reconstruct natural and artificial surfaces based on field measurements. This allows to spatially contextualize documented subunits and features. 

### Data Management and Cleaning

- `r pkg("unstruwwel")` can detect and transform strings containing historic dates (e.g. "3rd century CE") to numeric values.

### Datasets

- `r pkg("archdata")` contains eleven archaeological datasets from around the world reported in published studies. These represent typical forms of archaeological data (and so are useful for teaching).
- `r pkg("binford")` contains more than 200 variables coding aspects of hunter-gatherer subsistence, mobility, and social organization for 339 ethnographically documented groups of hunter-gatherers, as used in Binford (2001) _Constructing Frames of Reference: An Analytical Method for Archaeological Theory Building Using Ethnographic and Environmental Data Sets_.
- `r pkg("clayringsmiletus")` consists of data on clay rings from the Sanctuary of Dionysos in the ancient city of Miletus on the western coast of Anatolia.
- `r pkg("folio")` provides several types of data related to broad topics (cultural evolution, radiocarbon dating, paleoenvironments, etc.), which can be used to illustrate statistical methods in the classroom (multivariate data analysis, compositional data analysis, diversity measurement, etc.).
- `r pkg("gsloid")` Contains published data sets for global benthic d18O data for 0-5.3 Myr and global sea levels based on marine sediment core data for 0-800 ka.
- `r pkg("datplot")` contains a data set on Inscriptions from Bithynia as used in B. Weissova (2019) _Regional Economy, Settlement Patterns and the Road System in Bithynia (4th Century BC-6th Century AD). Spatial and Quantitative Analysis_ suitable for geographical and chronological analysis.

#### Radiocarbon Datasets and APIs

- `r github("people3k/p3k14c")` contains a global dataset of radiocarbon dates.
- `r github("xronos-ch/xronos.R")` accesses [XRONOS](https://xronos.ch), a global dataset of radiocarbon and other chronometric dates.
- `r github("joeroe/rintchron")` accesses [IntChron](https://www.intchron.org/), an indexing service for chronological information.

### Links

- Carlson, D. L. (2017). _Quantitative Methods in Archaeology Using R_. Cambridge: Cambridge University Press. DOI: [10.1017/9781139628730](https://doi.org/10.1017/9781139628730).
- Marwick, B. (2018). R Coding and Modeling. In S.L. López Varela (Ed.), _The Encyclopedia of Archaeological Sciences_, p. 1-5. John Wiley & Sons. DOI: [10.1002/9781119188230.saseas0631](https://doi.org/10.1002/9781119188230.saseas0631).
- [CAA International](https://caa-international.org/) Special Interest Group (SIG) on [Scientific Scripting Languages in Archaeology](https://sslarch.github.io/). This groups focusses on the application of Scripting Languages in archaeological research.
