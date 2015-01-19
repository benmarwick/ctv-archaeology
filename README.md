CRAN Task View: Archaeological Science
---------------------------------


**Maintainer:** Ben Marwick  
**Contact:** benmarwick at gmail.com 
**Version:** 2014-12-12  

This CRAN Task View contains a list of packages useful for scientific work in Archaeology, grouped by topic. Note that this is not an official CRAN Task View, just one I have prepared for my own convenience. 

Besides these packages, a very wide variety of functions suitable for scientific work in Archaeology is provided by both the basic R system (and its set of recommended core packages), and a number of other packages on the Comprehensive R Archive Network (CRAN). Consequently, several of the other CRAN Task Views may contain suitable packages, in particular the [SocialSciences](http://cran.rstudio.com/web/views/SocialSciences.html), [Spatial](http://cran.rstudio.com/web/views/Spatial.html)  [Spatio-temporal](http://cran.rstudio.com/web/views/spatioTemporal.html), [Cluster analysis](http://cran.r-project.org/web/views/Cluster.html), [Multivariate Statistics](http://cran.r-project.org/web/views/Multivariate.html), [Bayesian inference](http://cran.r-project.org/web/views/Bayesian.html), [Visualization](http://cran.r-project.org/web/views/Graphics.html),  and [Reproducible research](http://cran.r-project.org/web/views/ReproducibleResearch.html) Task Views. 

Contributions to this Task View are always welcome, and encouraged. The source file for this particular task view file resides in a GitHub repository (see below), and pull requests are the preferred method for contributions. 

**Data acquisition:**

-	[RODBC](http://cran.rstudio.com/web/packages/RODBC/index.html), [RMySQL](http://cran.rstudio.com/web/packages/RMySQL/index.html), [RPostgresSQL](http://cran.rstudio.com/web/packages/RPostgresSQL/index.html), [RSQLite](http://cran.rstudio.com/web/packages/RSQLite/index.html) for connecting R to SQL databases. [RODBC](http://cran.rstudio.com/web/packages/RODBC/index.html) can connect to Microsoft Access databases. 
-	[gdata](http://cran.rstudio.com/web/packages/gdata/index.html), [openxlsx](http://cran.rstudio.com/web/packages/openxlsx/index.html), [XLConnect](http://cran.rstudio.com/web/packages/XLConnect/index.html), [xlsx](http://cran.rstudio.com/web/packages/xlsx/index.html) - These packages help you read and write Microsoft Excel files using R. You can also just export your spreadsheets from Excel as CSVs.
-	[foreign](http://cran.rstudio.com/web/packages/foreign/index.html) for reading and writing Minitab, S, SAS, SPSS, Stata, Systat and Weka files. 
-   ESRI shapefiles can be read using [rgdal](http://cran.rstudio.com/web/packages/rgdal/index.html) or [maptools](http://cran.rstudio.com/web/packages/maptools/index.html)
-	Data can be input to R directly from the web using [httr](http://cran.rstudio.com/web/packages/httr/index.html), [XML](http://cran.rstudio.com/web/packages/XML/index.html), [jsonlite](http://cran.rstudio.com/web/packages/jsonlite/index.html), [rvest](http://cran.rstudio.com/web/packages/rvest/index.html), [rselenium](http://cran.rstudio.com/web/packages/rselenium.index.html). R can be programmed to be a web-scraper using rvest and/or rselenium. 

**Data manipulation:**

-   [dplyr](http://cran.rstudio.com/web/packages/dpylr/index.html) and [data.table](http://cran.rstudio.com/web/packages/data.table/index.html) for splitting the data up by groups, applying some common or custom functions, and combining the output back into a convenient form (ie. typical aggregation, splitting and summarising operations). Both packages are fast on very large datasets. 
-	[reshape2](http://cran.rstudio.com/web/packages/reshape2/index.html) and [tidyr](http://cran.rstudio.com/web/packages/tidyr/index.html) for rearranging the data from long to wide forms, and more complex reshaping. 

**Linear and Generalized Linear Models:**

-	The generic `anova()` function in the [stats](http://cran.rstudio.com/web/packages/stats/index.html) package constructs sequential analysis of variance and analysis of deviance tables, and can compute F and likelihood-ratio tests for nested models. (It is typical for other classes of statistical models in R to have anova methods as well.) The generic Anova function in the [car](http://cran.rstudio.com/web/packages/car/index.html) package (associated with Fox, An R and S-PLUS Companion to Applied Regression, Sage, 2002) constructs so-called "Type-II" and "Type-III" tests for linear and generalized linear models.

**Analysis of Categorical and Count Data:**

-	The table function in the R-base base package and the `xtabs()` and `ftable()` functions in the stats package construct contingency tables.
-	The `chisq.test()` and `fisher.test()` functions in the stats package may be used to test for independence in two-way contingency tables
-   The [coin](http://cran.rstudio.com/web/packages/coin/index.html) package contains several relevant functions that use resampling methods

**Multivariate statistics**

-	[caret](http://cran.rstudio.com/web/packages/caret/index.html), [FactoMiner](http://cran.rstudio.com/web/packages/FactoMiner/index.html), 
-	[aplpack](http://cran.rstudio.com/web/packages/aplpack/index.html) provides `bagplots()`
-	`lda()` and `qda()` within [MASS](http://cran.rstudio.com/web/packages/MASS/index.html) provide linear and quadratic discrimination respectively.
-	 The [Cluster task view] provides a more detailed discussion of available cluster analysis methods and appropriate R functions and packages.

Hierarchical cluster analysis:

-    The recommended package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) provides functions for cluster analysis following the methods described in Kaufman and Rousseeuw (1990) Finding Groups in data: an introduction to cluster analysis , Wiley, New York
-    There are also `hclust()` in the stats package and hcluster() in [amap](http://cran.rstudio.com/web/packages/amap/index.html)
-    [pvclust](http://cran.rstudio.com/web/packages/pvclust/index.html) is a package for assessing the uncertainty in hierarchical cluster analysis. It provides approximately unbiased p-values as well as bootstrap p-values.

Other partitioning methods:

-   `kmeans()` in stats provides k-means clustering and cmeans() in [e1071](http://cran.rstudio.com/web/packages/e1071/index.html) implements a fuzzy version of the k-means algorithm. The recommended package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) also provides functions for various partitioning methodologies.

Mixture models and model-based cluster analysis:

-    [mclust](http://cran.rstudio.com/web/packages/mclust/index.html) and [flexmix](http://cran.rstudio.com/web/packages/flexmix/index.html) provide implementations of model-based cluster analysis.
-	 Principal Components (PCA) is available via the `prcomp()` function (based on svd),  `rda()` (in package [vegan](http://cran.rstudio.com/web/packages/vegan/index.html)), `pca()` (in package [labdsv](http://cran.rstudio.com/web/packages/labdsc/index.html)) and `dudi.pca()` (in package [ade4](http://cran.rstudio.com/web/packages/ade4/index.html)), provide more ecologically-orientated implementations. Plotting of PCA output is available in [ggbiplot](https://github.com/vqv/ggbiplot) and [ggfortify](https://github.com/sinhrks/ggfortify). Redundancy Analysis (RDA) is available via `rda()` in vegan and `pcaiv()` in ade4. Canonical Correspondence Analysis (CCA) is implemented in `cca()` in both vegan and ade4. Detrended Correspondence Analysis (DCA) is implemented in `decorana()` in vegan. Principal coordinates analysis (PCO) is implemented in `dudi.pco()` in ade4, `pco()` in labdsv, `pco()` in [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html), and `cmdscale()` in package [MASS](http://cran.rstudio.com/web/packages/MASS/index.html).
-    Non-Metric multi-Dimensional Scaling (NMDS) is provided by `isoMDS()` in package MASS and `nmds()` in ecodist. `nmds()`, a wrapper function for `isoMDS()`, is also provided by package labdsv. vegan provides helper function `metaMDS()` for `isoMDS()`, implementing random starts of the algorithm and standardised scaling of the NMDS results. The approach adopted by vegan with `metaMDS()` is the recommended approach for ecological data.
-	`corresp()` and `mca()` in MASS provide simple and multiple correspondence analysis respectively. [ca](http://cran.rstudio.com/web/packages/ca/index.html) also provides single, multiple and joint correspondence analysis. `ca()` and `mca()` in ade4 provide correspondence and multiple correspondence analysis respectively, as well as adding homogeneous table analysis with `hta()`. Further functionality is also available within vegan co-correspondence is available from cocorresp. [FactoMineR](http://cran.rstudio.com/web/packages/FactoMineR/index.html) provides `CA()` and `MCA()` which also enable simple and multiple correspondence analysis as well as associated graphical routines.

**Making maps and using R as a GIS:**

-	Making maps: [maps](http://cran.rstudio.com/web/packages/maps/index.html), [mapdata](http://cran.rstudio.com/web/packages/mapdata/index.html), [maptools](http://cran.rstudio.com/web/packages/maptools/index.html), [mapproj](http://cran.rstudio.com/web/packages/mapproj/index.html), [ggplot2](http://cran.rstudio.com/web/packages/ggplot2/index.html), [ggmap](http://cran.rstudio.com/web/packages/ggmap/index.html), [RgoogleMaps](http://cran.rstudio.com/web/packages/RgoogleMaps/index.html), [RColorBrewer](http://cran.rstudio.com/web/packages/RColorBrewer/index.html) 
-   Using R as a GIS for spatial analysis: [sp](http://cran.rstudio.com/web/packages/sp/index.html), [rgdal](http://cran.rstudio.com/web/packages/rgdal/index.html) (uses the GDAL (raster) and OGR (vector) data I/O library, as well as PROJ.4 for CRS (coordinate reference systems) (re)projections), [rgeos](http://cran.rstudio.com/web/packages/rgeos/index.html) (uses the GEOS (Geometry Open Source) library, which powers PostGIS: does the 'usual' geometry operations for features), [raster](http://cran.rstudio.com/web/packages/raster/index.html), [rasterVis](http://cran.rstudio.com/web/packages/rasterVis/index.html), [shapefiles](http://cran.rstudio.com/web/packages/shapefiles/index.html), [spatial](http://cran.rstudio.com/web/packages/spatial/index.html), [spatstat](http://cran.rstudio.com/web/packages/spatstat/index.html), [splancs](http://cran.rstudio.com/web/packages/splancs/index.html)

**Environmental & Geological Analysis:**

-	Transfer function models including weighted averaging (WA), modern analogue technique (MAT), Locally-weighted WA, & maximum likelihood (aka Gaussian logistic) regression (GLR) are provided by [analogue](http://cran.rstudio.com/web/packages/analogue/index.html), [vegan](http://cran.rstudio.com/web/packages/vegan/index.html), [rioja](http://cran.rstudio.com/web/packages/rioja/index.html) for stratigraphic analyses
-	[G2Sd](http://cran.rstudio.com/web/packages/G2Sd/index.html) - full descriptive statistics and a physical description of sediments based on grain-size distributions, [soiltexture](http://cran.rstudio.com/web/packages/soiltexture/index.html) and [ggterm](http://cran.rstudio.com/web/packages/ggterm/index.html) for ternary plots of soil texture
-	 Constrained clustering of stratigraphic data is provided by function `chclust()` in the form of constrained hierarchical clustering in [rioja](http://cran.rstudio.com/web/packages/rioja/index.html).
-    Radiocarbon dates can be calibrated using [BChron](http://cran.rstudio.com/web/packages/BChron/index.html) with various calibration curves (including user generated ones); also does Age-depth modelling as per the algorithm of Haslett and Parnell (2008); Relative sea level rate estimation incorporating time uncertainty in polynomial regression models; and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM).
-    Functions for tree ring analysis can be found in [dplR](http://cran.rstudio.com/web/packages/dplR/index.html)

**Phylogenetics, morphometrics and evolution**

The [Phylogenetics task view] provides more detailed coverage of the subject area and related functions within R. Packages specifically tailored for the analysis of phylogenetic and evolutionary data include: [ape](http://cran.rstudio.com/web/packages/ape/index.html), [phytools](http://cran.rstudio.com/web/packages/phytools/index.html), [phangorn](http://cran.rstudio.com/web/packages/phangorn/index.html), [Rphylip](http://cran.rstudio.com/web/packages/Rphylip/index.html), [ouch](http://cran.rstudio.com/web/packages/ouch/index.html). For plotting trees most of these packages include their own modifications of the base plot() function, and there are also [ggtree](http://cran.rstudio.com/web/packages/ggtree/index.html), [ggdendro](http://cran.rstudio.com/web/packages/ggdendro/index.html), [dendextend](http://cran.rstudio.com/web/packages/dendextend/index.html), and [ggphylo](http://cran.rstudio.com/web/packages/ggphylo/index.html)

Morphometric analyses are provided by [shape](http://cran.rstudio.com/web/packages/shape/index.html) and [Momocs](http://cran.rstudio.com/web/packages/Momocs/index.html).

**Visualising Data:**

-	[ggplot2](http://cran.rstudio.com/web/packages/ggplot2/index.html) produces attractive plots with a highly flexible and logical syntax. Extensions include [ggbiplot](https://github.com/vqv/ggbiplot) (PCA biplots with ellipses), [ggally](https://github.com/ggobi/ggally) (plot matrices), [ggtern](http://www.ggtern.com/) (ternary plots), [gridExtra](http://cran.rstudio.com/web/packages/gridExtra/index.html)  (arranging multiple plots), and [ggfortify](https://github.com/sinhrks/ggfortify) (many methods for plotting PCA, clustering, linear model output, etc., using ggplot2) 
-   [ggmaps](http://cran.rstudio.com/web/packages/ggmaps/index.html) combines the spatial information of static maps from Google Maps, OpenStreetMap, Stamen Maps or CloudMade Maps with the layered grammar of graphics implementation of ggplot2
-	Stratigraphic data plots can be drawn using `Stratiplot()` function in [analogue](http://cran.rstudio.com/web/packages/analogue/index.html) and functions `strat.plot()` and strat.plot.simple in the [rioja](http://cran.rstudio.com/web/packages/rioja/index.html) package.
-	[rgl](http://cran.rstudio.com/web/packages/rgl/index.html) for interactive 3D plots
-   [tabplot](https://github.com/mtennekes/tabplot/) for exploratory data visualisation of tables

**Reproducible Research:**

-	[knitr](http://cran.rstudio.com/web/packages/knitr/index.html) enables R code and text with formatting instructions (eg. markdown or LaTeX) to be executed and combined in a single document that contained plots, analysed data and formatted text. [rlp](https://github.com/yihui/rlp) is a package that lets you write an analysis as a Rmd file and then converts it into a package. [manuscriptPackage](https://github.com/jhollist/manuscriptPackage), [template](https://github.com/cboettig/template), and [template](https://github.com/Pakillo/template) (yes, that's two packages with the same name) are packages that give templates for organising an analysis as an R package (eg. where the manuscript is the package vignette) 
-   [rmarkdown](http://cran.rstudio.com/web/packages/rmarkdown/index.html) is a simple document formatting language with some minor customizations to recognise R code blocks and inline code. Complementary packages include [captioner](https://github.com/adletaw/captioner) and [kfigr](https://github.com/mkoohafkan/kfigr) for figure and table captions and cross-referencing. 
-   [pandoc](http://johnmacfarlane.net/pandoc/) is a universal document format converter, in this context it is used to convert rmarkdown or LaTeX to PDF, MS Word or HTML files. It is included with RStudio but can also be used stand-alone from the command line.
-   [packrat](http://cran.rstudio.com/web/packages/packrat/index.html) supports the development of isolated, stand-alone projects that include all the packages used and their dependencies. 
-   [checkpoint](http://cran.rstudio.com/web/packages/checkpoint/index.html) allows you to install R packages from a specific snapshot date in the past, ensuring that you use the same package version that you started with, not a more recent one. 
-   [rocker](https://github.com/rocker-org/rocker) is a project that provides Docker containers to run R in a lightweight virtual environment, the hadleyverse container includes dplyr, ggplot2, etc. as well as RStudio server and LaTeX

**Developing R software**

-	[devtools](http://cran.rstudio.com/web/packages/devtools/index.html) for easily creating R packages 
-   [roxygen2](http://cran.rstudio.com/web/packages/roxygen2/index.html) for simplifying the creation of documentation for packages,
-   [testthat](http://cran.rstudio.com/web/packages/testthat/index.html) for developing tests of functions in packages
-   [RCpp](http://cran.rstudio.com/web/packages/RCpp/index.html) enables the use of C++ code in R packages for high performance computing

**Places to go for help:**

-	? function, eg. ?mean to get built-in help on the mean function
-	sos::findFn("rose diagram") searches all installed packages for the search term, using the [sos](http://cran.rstudio.com/web/packages/sos/index.html) package
-   Most major packages come with vignettes that narrate typical uses of the package's core functions. 
-	[stackoverflow](http://stackoverflow.com/questions/tagged/r) is an online Q&A website where questions and answers can be voted on to indicate their quality. 
-	Google searches in the form: r help [search terms]
-   A custom search engine of R resources: http://www.rseek.org/
-   All R package documentation (including CRAN, GitHub and Bioconductor packages) is online in an easy-to-ready format at http://www.rdocumentation.org/


### CRAN packages:

### Related links:

-   CRAN Task View: [SocialSciences](http://cran.rstudio.com/web/views/SocialSciences.html)
-   CRAN Task View: [Spatial](http://cran.rstudio.com/web/views/Spatial.html)
-   CRAN Task View: [Spatio-temporal](http://cran.rstudio.com/web/views/spatioTemporal.html)
-   CRAN Task View: [Cluster analysis](http://cran.r-project.org/web/views/Cluster.html)
-   CRAN Task View: [Multivariate Statistics](http://cran.r-project.org/web/views/Multivariate.html) 
-   CRAN Task View: [Bayesian inference](http://cran.r-project.org/web/views/Bayesian.html)
-   CRAN Task View: [Visualization](http://cran.r-project.org/web/views/Graphics.html)
-   CRAN Task View: [Reproducible research](http://cran.r-project.org/web/views/ReproducibleResearch.html) 
-   [David L. Carlson's guides on using R for 'Quantifying Archaeology' by Stephen Shennan 'Statistics for Archaeologists' by Robert Drennan]( http://people.tamu.edu/~dcarlson/quant/index.html)
-   [Matt Peeples' scripts for archaeological statistics]( http://www.mattpeeples.net/resources.html)
-   [GitHub repository for this Task View](https://github.com/benmarwick/ctv-archaeology)
