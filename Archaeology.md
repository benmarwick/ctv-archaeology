---
name: Archaeology
topic: Archaeology
maintainer: Ben Marwick, Bjørn Peare Bartholdy, Nicolas Frerebeau, Sam Leggett, Sarah Pederzani, Joe Roe, Sophie C. Schmidt, Laure Spake, Lisa Steinmann, Liying Wang
email: benmarwick@gmail.com
version: 2023-09-19
source: https://github.com/cran-task-views/Archaeology
---

This task view is a list of packages useful for archaeological science. It includes packages for working with distinctive types of archaeological data, such as radiocarbon ages, various types of artefacts (lithics, pottery, etc.), faunal remains, geoarchaeological and landscape data, packages containing archaeological datasets, and packages from closely related sciences, such as environmental science, that are widely used by archaeologists. This is a list to help archaeologists in their search for packages relevant to their research. It does not include packages for general purpose tasks such as importing/exporting data, data manipulation, common forms of data analysis and visualization, and doing reproducible research. These may be found in other CRAN Task Views, especially `r view("Environmetrics")`, `r view("Spatial")`, `r view("Multivariate")`, `r view("Phylogenetics")`, `r view("Cluster")`, `r view("ReproducibleResearch")`, `r view("WebTechnologies")`, `r view("MachineLearning")`, and `r view("SpatioTemporal")`. To minimise overlap we do not include those packages in this list. This list assumes some familiarity with using R and is not an introduction to using R in archaeology (see the links below for introductory resources). 

If you have any questions feel free to reach out to the task view maintainers or the maintainers of specific packages. If there is an archaeological science package on CRAN or elsewhere that we have missed, please let us know. Contributions are always welcome, and encouraged -- please see the linked GitHub repository for details.

### Analysis of dates and chronological patterns

#### Radiometric Dating

Radiocarbon ages can be calibrated using many of the packages in this section:

- `r pkg("rcarbon", priority = "core")` is useful for calibration, and also contains extensively documented functions for hypothesis testing and modelling radiocarbon ages. See Crema and Bevan ([2021](https://doi.org/10.1017/RDC.2020.95)) for an introduction. Basic calibration is also possible with `r pkg("rintcal")` and `r pkg("ArchaeoChron")`.
- `r pkg("Bchron")` adds various calibration curves (including user generated ones); also does age-depth modelling, relative sea level rate estimation incorporating time uncertainty in polynomial regression models, and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM). `r pkg("clam")` similarly does 'classical' age-depth modelling of deposits.
- Bayesian age-depth modelling of radiocarbon dates is available in `r pkg("nimbleCarbon")` and `r pkg("rbacon")`.
- `r pkg("coffee")` uses Bayesian methods to enforce the chronological ordering of radiocarbon and other dates, for example for trees with multiple radiocarbon dates spaced at exactly known intervals.
- `r pkg("oxcAAR")` allows you to use R to connect to a local installation of the OxCal software to calibrate radiocarbon dates and a variety of other OxCal operations.
- `r pkg("ArchaeoPhases")` allows you to post-process Markov Chain Monte Carlo (MCMC) simulations from [ChronoModel](https://chronomodel.com/), [Oxcal](https://c14.arch.ox.ac.uk/oxcal.html) or [BCal](https://bcal.shef.ac.uk/). It provides statistical tools to analyze and to estimate archaeological phases from the posterior distribution of a sequence of dates and includes testing procedures to check the presence of a gap between two successive phases.
- `r pkg("spDates")` allows analysis of spatial gradients in radiocarbon dates.
- `r pkg("IsoplotR")` offers a statistical toolbox for radiometric geochronology.

- `r github("ropensci/c14bazAAR")` facilitates retrieval and preparation of large radiocarbon datasets.
- `r github("joeroe/c14")` provides basic classes and functions for radiocarbon data in R. It makes it easier to combine methods from several existing packages (e.g. `rcarbon`, `Bchron`, `oxcAAR`, `c14bazAAR`, `ArchaeoPhases`, `stratigraphr`) together and work with them in a tidy data workflow.
- `r github("tonydoss/UThwigl")` computes closed- and open-system uranium-thorium (U-Th) ages of geological and archaeological samples.
- The `r github("UCL/ADMUR")` package provides tools to directly model underlying population dynamics using chronological datasets (radiocarbon and other) with a variety of models, including Continuous Piecewise Linear (CPL) model framework, and model comparison framework using BIC.

#### Luminescence Dating

- Various R functions for Luminescence Dating data analysis are in the `r pkg("Luminescence")` and `r pkg("numOSL")` packages, including equivalent dose calculation, annual dose rate determination, growth curve fitting, decay curve decomposition, statistical age model optimization, and statistical plot visualization.
- `r pkg("BayLum")` provides chronological bayesian models integrating Optically Stimulated Luminescence and radiocarbon age dating.

#### Paleoenvironmental Proxies

- `r pkg("tidypaleo")` provides a set of functions for age-depth model management, stratigraphic visualization, and common statistical transformations.
- `r pkg("shoredate")` offers methods to shoreline date coastal sites based on their present-day elevation and the trajectory of past relative sea-level change.

#### Archaeological Time Series

- `r pkg("era")` provides a consistent representation of year-based time scales as a numeric vector with an associated era. `r pkg("aion")` contains a toolkit for handling archaeological time series.
- `r pkg("aoristic")`, `r pkg("kairos")` and `r github("ISAAKiel/aoristAAR")` provide functions for the aoristic analysis of archaeological data (takes into account the uncertainty of the exact moment that an event occurred when examining the overall incidence of events over time).
- `r pkg("kairos")` provides functions for mean ceramic date estimation.
- `r pkg("SPARTAAS")` and `r pkg("kairos")` provide methods for statistical pattern recognition, time range plotting and seriation plots of archaeological artefacts.
- `r pkg("datplot")` converts date ranges into dating 'steps' to ease the visualization of changes in e.g. pottery consumption, style and other variables over time. 

- The `r github("davidcorton/archSeries")` package makes chronologies from information from multiple entities with varying chronological resolution and overlapping date ranges.

### Artefact analysis

- `r pkg("iconr")` for modeling prehistoric iconographic compositions and preparing for further analysis (clustering, typology tree, Harris diagram, etc.).

- `r github("yesdavid/outlineR")` for the fast and easy extraction of single outline shapes of, for example, stone tools from images containing multiple thereof, such as the ones present in archaeological publications.
- `r github("ISAAKiel/shapAAR")` for the extraction, analysis and classification of (not only) archaeological objects derived from scanned images. Aims especially at the analysis of the shapes/profiles of e.g. ceramic vessels or arrow heads.
- `r github("cornelmpop/Lithics3D")` for working with 3D scans of archaeological lithics (clean triangular meshes and existing landmarks).
- `r github("maciejkasinski/quantatools")` for analysis of quantum (common measurement units) in archaeological data with cosine quantogram and related statistical methods.
- `r github("Johanna-Mestorf-Academy/sdsanalysis")` for exploration and visualization of lithic datasets recorded using the 'Systematic and digital documentation of stone artefacts' recording system.

### Cultural evolutionary analysis

- `r github("ercrema/cTransmission")` for an Approximate Bayesian Computation Framework for inferring patterns of cultural transmission from frequency data.
- `r github("ercrema/HERAChp.KandlerCrema")` enables the reproduction of the analysis and associated figures for the book chapter _Analysing cultural frequency data: neutral theory_ by Anne Kandler and Enrico Crema for the volume _Handbook of Evolutionary Research in Archaeology_, edited by Anna Prentiss. The package contains two main functions for simulating cultural transmission.
- `r github("benmarwick/signatselect")` provides two functions useful for investigating change over time in artefact assemblages (and genetic time-series data).
- `r github("benmarwick/roev")` provide functions for analysing and visualizing rates of evolution following the methods in Philip D. Gingerich’s 2019 book _Rates of Evolution: A Quantitative Synthesis_.

### Quantitative analysis

- `r pkg("tabula")` provides several tests and measures of diversity: heterogeneity and evenness (Brillouin, Shannon, Simpson, etc.), richness and rarefaction (Chao1, Chao2, ACE, ICE, etc.), turnover and similarity (Brainerd-Robinson, etc.). The package make it easy to visualize count data and statistical thresholds: rank vs. abundance plots, heatmaps, Ford (1962) and Bertin (1977) diagrams.
- `r pkg("dimensio")` provides simple Principal Components Analysis (PCA) and Correspondence Analysis (CA) based on the Singular Value Decomposition (SVD). This package provides S4 classes and methods to compute, extract, summarize and visualize results of multivariate data analysis. It also includes methods for partial bootstrap validation.
- `r pkg("skyscapeR")` for data reduction, visualization and analysis in skyscape archaeology, archaeoastronomy and cultural astronomy.
- `r github("ISAAKiel/quantAAR")` contains tidy wrappers and useful utility function for common applications of exploratory statistics in archaeology.

### Zooarchaeological analysis

- `r pkg("zoolog")` to generate and manipulate log-ratios (also known as log size index (LSI) values) from measurements obtained on zooarchaeological material.

### Mortuary analysis

- `r pkg("mortAAR")` calculates a life table based on archaeological demographic data.
- `r github("nevrome/varnastats")` for bi- and multivariate analysis of matrices of archaeological data. Developed and used for the analysis of Varna Necropolis (Bulgaria).

### Geoarchaeological analysis

- `r pkg("aqp")` simplifies the quantitative analysis of soil profile data. It allows soil profile visualization, aggregation, and classification. `r pkg("G2Sd")`, `r github("mauricio-camargo/rysgran")` and `r pkg("EMMAgeo")` can be used for working with sedimentary grain-size data in logarithmic (phi) and geometric (micrometers) scales, based on various methods.
- `r pkg("SIBER")`, `r pgk("MixSIAR")`, `r pkg("simmr")` and `r pkg("IsotopeR")` provide methods for working with isotope data.
- `r pkg("munsell")` provides methods for working with sediment colour.
- `r pkg("nexus")` provides tools for compositional data analysis, chemical fingerprinting and source tracking of ancient materials.
- `r pkg("isopleuros")` allows creation of ternary plots. It also includes common ternary diagrams useful for the archaeologist (e.g. soil texture charts, ceramic phase diagram).

- `r github("ISAAKiel/magAAR")` analyzes geomagnetic data from archaeological contexts.
- `r github("Andros-Spica/cerUB")` for multivariate statistic protocols for integrating archaeometric data (geochemical, mineralogical, petrographic).
 
### Landscape analysis

- `r pkg("leastcostpath")` calculates Least Cost Paths (LCPs) using numerous time- and energy-based cost functions that approximate the difficulty of moving across a landscape.
- `r github("SCSchmidt/percopackage")` implements percolation Analysis as a 2D point pattern analysis technique for identifying clusters of any size and form (e.g. of archaeological sites).
- `r github("ISAAKiel/lecAAR")` for calculating the largest empty circles and estimation of archaeological sites theoretically to be expected in region of interest.
- `r github("ISAAKiel/pathAAR")` to reconstruct paths using archaeological monuments, model parameters of infrastructure, and evaluate those parameters.
- `r github("mrecos/klrfome")` for archaeological site location modeling; maps a single scalar outcome (e.g. presence/absence; 0/1) to a distribution of features. 
- `r github("eScienceCenter/SiteExploitationTerritories")` calculates a non-isotropic spatial relationship by integrating human energy expenditure in terrain based estimations.
- `r github("nevrome/bleiglas")` calculates of three-dimensional Voronoi diagrams from input point clouds for spatiotemporal applications in archaeology.
- `r github("wccarleton/lamap")` calculates the Locally Adaptive Model of Archaeological Potential (LAMAP).

### Survey, excavation, and stratigraphic analysis

- `r pkg("archeoViz")` is a packaged R Shiny application for the 2D and 3D visualization, exploration, and web communication of spatial data from archaeological excavations.
- `r pkg("archeofrag")` for refitting and stratigraphic analysis in archaeology.
- `r pkg("recexcavAAR")` for 3D reconstruction and analysis of excavations, provides methods to reconstruct natural and artificial surfaces based on field measurements. This allows to spatially contextualize documented subunits and features. 
- `r github("joeroe/stratigraphr")` provides a tidy framework for working with archaeological stratigraphy and chronology in R. It includes tools for reading, analysing, and visualising stratigraphies (Harris matrices) and sequences as directed graphs; helper functions for using radiocarbon dates in a tidy data analysis; and an R interface to OxCal's Chronological Query Language (CQL).
- `r github("joeroe/fieldwalkr")` for designing and evaluating sampling strategies in spatial survey (fieldwalking in archaeological jargon). It contains functions for simulating the effect of different survey units, sampling methods and detection functions on the estimation of randomly generated or observed point processes.
- `r github("mrecos/signboardr")` Utilize Google Vision API to extract text from archaeological photos containing a sign board.

### Data management and cleaning
- `r pkg("unstruwwel")` can detect and transform strings containing historic dates (e.g. "3rd century CE") to numeric values.

### Datasets

- `r pkg("archdata")` contains eleven archaeological datasets from around the world reported in published studies. These represent typical forms of archaeological data (and so are useful for teaching).
- `r pkg("binford")` contains more than 200 variables coding aspects of hunter-gatherer subsistence, mobility, and social organization for 339 ethnographically documented groups of hunter-gatherers, as used in Binford (2001) _Constructing Frames of Reference: An Analytical Method for Archaeological Theory Building Using Ethnographic and Environmental Data Sets_.
- `r pkg("folio")` provides several types of data related to broad topics (cultural evolution, radiocarbon dating, paleoenvironments, etc.), which can be used to illustrate statistical methods in the classroom (multivariate data analysis, compositional data analysis, diversity measurement, etc.).
- `r pkg("gsloid")` Contains published data sets for global benthic d18O data for 0-5.3 Myr and global sea levels based on marine sediment core data for 0-800 ka.
- `r pkg("chemometrics")` contains a dataset of elemental concentrations for 180 archaeological glass vessels excavated from 15th - 17th century contexts in Antwerp.
- `r pkg("datplot")` contains a data set on Inscriptions from Bithynia as used in B. Weissova (2019) _Regional Economy, Settlement Patterns and the Road System in Bithynia (4th Century BC-6th Century AD). Spatial and Quantitative Analysis_ suitable for geographical and chronological analysis.

- `r github("geanes/bioanth")` contains three osteometric datasets useful for biological and forensic anthropology.
- `r github("sfsheath/cawd")` contains 15 datasets of ancient Greek, Roman and Persian maps and digital atlas data.
- `r github("benmarwick/evoarchdata")` contains four published datasets widely used in archaeological studies of cultural evolution.
- `r github("joeroe/islay")` includes various datasets relating to the prehistoric archaeology of the Scottish island of Islay and recorded by the ‘Southern Hebrides Mesolithic Project’ (Mithen et al. 2000).
- `r github("DCPollard94/knossoscemeteries")` includes artefacts data from two Early Iron Age Cemeteries at Knossos, Crete.
- `r github("joeroe/swapdata")` a collection of archaeological datasets and tools related to the prehistory of Southwest Asia.
- `r github("benmarwick/mjbnaturepaper")` contains stone artefact and total station data for excavations at Madjedbebe, a rock shelter in northern Australia
- `r github("lsteinmann/clayringsmiletus")` data on clay rings from the Sanctuary of Dionysos in the ancient city of Miletus on the western coast of Anatolia
- `r github("bischrob/Rosegate-Projectile-Points-in-the-Fremont-Region")` contains frequency data for different types of projectile points across 23 sites in the Fremont Region of the American Southwest

#### Radiocarbon datasets and APIs

- `r pkg("BSDA")` contains a dataset of 60 radiocarbon ages of observations taken from an archaeological site with four phases of occupation.
- `r github("ropensci/c14bazAAR")` contains over 20 datasets of radiocarbon ages from around the world.
- `r github("people3k/p3k14c")` contains a global dataset of radiocarbon dates.
- `r github("xronos-ch/xronos.R")` accesses [XRONOS](https://xronos.ch), a global dataset of radiocarbon and other chronometric dates.
- `r github("joeroe/rintchron")` accesses [IntChron](https://www.intchron.org/), an indexing service for chronological information.
- `r github("ArchaeoStat/ArchaeoData")` contains two datasets for chronological modelling with `r pkg("ArchaeoPhases")`.

### Links

- Carlson, D. L. (2017). _Quantitative Methods in Archaeology Using R_. Cambridge: Cambridge University Press. DOI: [10.1017/9781139628730](https://doi.org/10.1017/9781139628730).
- Marwick, B. (2018). R Coding and Modeling. In S.L. López Varela (Ed.), _The Encyclopedia of Archaeological Sciences_, p. 1-5. John Wiley & Sons. DOI: [10.1002/9781119188230.saseas0631](https://doi.org/10.1002/9781119188230.saseas0631).
- [CAA International](https://caa-international.org/) Special Interest Group (SIG) on [Scientific Scripting Languages in Archaeology](https://sslarch.github.io/). This groups focusses on the application of Scripting Languages in archaeological research.
