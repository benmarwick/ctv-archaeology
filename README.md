CRAN Task View: Archaeological Science
---------------------------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><strong>Maintainer:</strong>
Ben Marwick</td>
<td align="left"><strong>Contact:</strong>
benmarwick at gmail.com</td>
<td align="left"><strong>Version:</strong>
2017-12-13</td>
</tr>
</tbody>
</table>

This CRAN Task View contains a list of packages useful for scientific work in Archaeology, grouped by topic. Note that this is not an official CRAN Task View, just one I have prepared for my own convenience, so it includes some packages only on GitHub and other non-CRAN resources I find useful. Many of the most highly recommended packages listed here can be installed in a single step by installing the [tidyverse](https://cran.r-project.org/package=tidyverse) package.

Besides these packages, a very wide variety of functions suitable for scientific work in Archaeology is provided by both the basic R system (and its set of recommended core packages), and a number of other packages on the Comprehensive R Archive Network (CRAN) and [GitHub](http://www.rdocumentation.org/packages?type=github). Consequently, several of the other CRAN Task Views may contain suitable packages, in particular the [Social Sciences](http://cran.rstudio.com/web/views/SocialSciences.html), [Spatial](http://cran.rstudio.com/web/views/Spatial.html),  [Spatio-temporal](http://cran.rstudio.com/web/views/SpatioTemporal.html), [Cluster analysis](http://cran.r-project.org/web/views/Cluster.html), [Multivariate Statistics](http://cran.r-project.org/web/views/Multivariate.html), [Bayesian inference](http://cran.r-project.org/web/views/Bayesian.html), [Visualization](http://cran.r-project.org/web/views/Graphics.html), and [Reproducible research](http://cran.r-project.org/web/views/ReproducibleResearch.html) Task Views. 

Contributions to this Task View are always welcome, and encouraged. The source file for this particular task view file resides in a GitHub repository (see below), and pull requests are the preferred method for contributions. 

**Data acquisition**

-  The ideal method is to export your spreadsheets from Excel (or whatever program you made them) as CSVs (comma-separated-values, a simple, non-proprietary plain-text-based format that is very transparent, being human-readable, easily machine-processable and suitable for archival storage) and read them into R using the base function `read.csv()`. Data in other types of plain text files can be read in with `read.table()`.
-  To read Microsoft Excel files into R there are a number of packages: [readxl]( https://github.com/hadley/readxl) (requires Rcpp, which in turn requires Rtools for Windows or XCode for OSX), [gdata](http://cran.rstudio.com/web/packages/gdata/index.html) (requires Perl), [openxlsx](http://cran.rstudio.com/web/packages/openxlsx/index.html) (requires Rcpp, which in turn requires Rtools for Windows or XCode for OSX), [XLConnect](http://cran.rstudio.com/web/packages/XLConnect/index.html) (requires [rJava](http://cran.rstudio.com/web/packages/rJava/index.html) and Java), [xlsx](http://cran.rstudio.com/web/packages/xlsx/index.html) (also requires rJava and Java). OpenDocument Spreadsheet files can be read into R using [readODS](http://cran.rstudio.com/web/packages/readODS/index.html). 
-  For working with untidy and/or complex Excel spreadsheets (i.e. many tables in one sheet, coloured cells, cells with formulas, etc.), use [jailbreakr](https://github.com/rsheets/jailbreakr), [xlsxtractr](https://github.com/hrbrmstr/xlsxtractr), [tidyxl](https://github.com/nacnudus/tidyxl) and [unpivotr](https://github.com/nacnudus/unpivotr)
-  Text data (as in sentences and paragraphs) can be read in and analysed with the [tm](http://cran.rstudio.com/web/packages/tm/index.html) package or [tidytext](https://cran.r-project.org/package=tidytext). If the text is in a PDF file, use [pdftools](https://CRAN.R-project.org/package=pdftools). Text in image files can be extracted with [tesseract](https://cran.r-project.org/package=tesseract)
-   For quickly reading in a very large number of CSV files, or very large CSV files, use `fread()` from the [data.table](http://cran.rstudio.com/web/packages/data.table/index.html) package or functions in the [readr](https://github.com/hadley/readr) package.
-   [RODBC](http://cran.rstudio.com/web/packages/RODBC/index.html), [RMySQL](http://cran.rstudio.com/web/packages/RMySQL/index.html), [RPostgreSQL](http://cran.rstudio.com/web/packages/RPostgreSQL/index.html), [RSQLite](http://cran.rstudio.com/web/packages/RSQLite/index.html) for connecting R to SQL databases. [RODBC](http://cran.rstudio.com/web/packages/RODBC/index.html) can connect to Microsoft Access databases. 
-   The [haven](https://github.com/hadley/haven) and [foreign](http://cran.rstudio.com/web/packages/foreign/index.html) packages can be used for reading and writing files from certain versions of Minitab, S, SAS, SPSS, Stata, Systat and Weka. 
-   ESRI shapefiles can be read using [rgdal](http://cran.rstudio.com/web/packages/rgdal/index.html) or [maptools](http://cran.rstudio.com/web/packages/maptools/index.html)
- R can receive data directly from the web using [httr](http://cran.rstudio.com/web/packages/httr/index.html), [XML](http://cran.rstudio.com/web/packages/XML/index.html), [jsonlite](http://cran.rstudio.com/web/packages/jsonlite/index.html), [rvest](http://cran.rstudio.com/web/packages/rvest/index.html), [RSelenium](http://cran.r-project.org/web/packages/RSelenium/index.html) (requires Selenium 2.0 Remote WebDriver). R can be programmed to be a web-scraper using rvest and/or rselenium. The [Web Technologies](http://cran.r-project.org/web/views/WebTechnologies.html) task view gives more details.
- Google spreadsheets can be read into R using the [googlesheet](https://github.com/jennybc/googlesheet) package
- Tables can be read directly from Microsoft Word documents with [docxtractr](https://cran.r-project.org/web/packages/docxtractr), and from PDF documents with [tabulizer](https://github.com/leeper/tabulizer)
- Datasets from the Open Context repository can be browsed and read into R using the [opencontext](https://github.com/ropensci/opencontext) package

**Data manipulation**

-   [dplyr](http://cran.rstudio.com/web/packages/dplyr/index.html) and [data.table](http://cran.rstudio.com/web/packages/data.table/index.html) for splitting the data up by groups, applying some common or custom functions, and combining the output back into a convenient form (ie. typical aggregation, splitting and summarising operations). Both packages are fast on very large datasets. 
- For cleaning, examining, and making quick summaries of data, [janitor](https://github.com/sfirke/janitor), [skimr](https://github.com/ropenscilabs/skimr), [statar](https://github.com/matthieugomez/statar), and [xda](https://github.com/ujjwalkarn/xda) maybe useful. [tabplot](https://github.com/mtennekes/tabplot/) has functions for exploratory data visualisation of tables
- [tidyr](http://cran.rstudio.com/web/packages/tidyr/index.html) for rearranging the data from long to wide forms, and more complex reshaping. 
- [purrr](http://cran.rstudio.com/web/packages/purrr/index.html) simplifies working with lists, applying functions to list elements and collecting the results
- [broom](http://cran.rstudio.com/web/packages/broom/index.html) takes the output of many built-in functions in R, such as `lm` or `t.test`, and turns them into tidy data frames.
- [measurements](https://cran.r-project.org/web/packages/measurements/), [convertr](https://github.com/ropenscilabs/convertr), and  [units](https://cran.r-project.org/web/packages/units) converts between metric and imperial units, or calculate a dimension's unknown value from other dimensions' measurements.

**Visualising data**

- [ggplot2](http://cran.rstudio.com/web/packages/ggplot2/index.html) produces a very wide variety of attractive plots with a highly flexible and logical syntax. To combine and align multiple ggplot2 plots in one panel, use [cowplot](https://cran.r-project.org/web/packages/cowplot/index.html), [egg](https://CRAN.R-project.org/package=egg), or [gridExtra](http://cran.rstudio.com/web/packages/gridExtra/index.html)
-    Extensions include [ggbiplot](https://github.com/vqv/ggbiplot) (PCA biplots with ellipses),  [GGally](http://cran.r-project.org/web/packages/GGally/index.html) (plot matrices), [ggtern](http://www.ggtern.com/) (ternary plots), [ggfortify](https://github.com/sinhrks/ggfortify) (many methods for plotting PCA, clustering, linear model output, etc., using ggplot2),[ggalt](https://github.com/hrbrmstr/ggalt) (more geoms, coords, stats, scales and fonts, including splines, 1d and 2d densities), [waffle](https://github.com/hrbrmstr/waffle) (for square pie charts), [ggraph](https://github.com/thomasp85/ggraph) for treemaps, [ggfan](https://CRAN.R-project.org/package=ggfan) for fanplots, [tidybayes](https://github.com/mjskay/tidybayes) for plotting output of Bayesian analysies, [ggridges](https://CRAN.R-project.org/package=ggridges) for ridge plots, [ggalt](https://CRAN.R-project.org/package=ggalt) for many additional geoms, and [ggrepel](https://github.com/slowkow/ggrepel) for moving overlapping text labels away from each other.
-    For showing distributions across several categories: [ggforce](https://CRAN.R-project.org/package=ggforce), [ggbeeswarm](https://github.com/eclarke/ggbeeswarm), [vipor](https://github.com/sherrillmix/vipor), [sinaplot](https://cran.r-project.org/web/packages/sinaplot)
-    [plotly](https://github.com/ropensci/plotly) and [ggiraph](https://github.com/davidgohel/ggiraph) make ggplots interactive with mouse-over pop-ups, zooming, click-actions, etc. [scatterD3](https://github.com/juba/scatterD3) makes highly interactive scatter plots
-    [circlize](https://cran.r-project.org/web/packages/circlize/index.html) implements Circos in R for circular and chord plots. Rose plots can be made with [ggplot2](http://cran.rstudio.com/web/packages/ggplot2/index.html), Schmidt diagrams can be made with the `net` function in [RFOC](https://cran.r-project.org/web/packages/RFOC) or the `Stereo*` functions in [RockFab](https://cran.r-project.org/web/packages/RockFab/)
-   [plotrix](http://cran.rstudio.com/web/packages/plotrix/index.html) has the function `battleship.plot()` to make Ford's battleship diagrams. 
-   [ggmaps](http://cran.rstudio.com/web/packages/ggmaps/index.html) combines the spatial information of static maps from Google Maps, OpenStreetMap, Stamen Maps or CloudMade Maps with the layered grammar of graphics implementation of ggplot2
-    Stratigraphic data plots can be drawn using `Stratiplot()` function in [analogue](http://cran.rstudio.com/web/packages/analogue/index.html) and functions `strat.plot()` and strat.plot.simple in the [rioja](http://cran.rstudio.com/web/packages/rioja/index.html) package. The rioja package also includes `chclust()` for stratigraphically constrained clustering, and related dendrogram plotting methods.
-    [rgl](http://cran.rstudio.com/web/packages/rgl/index.html) and [plotly](https://github.com/ropensci/plotly) for interactive 3D plots,and [scatterplot3d](http://cran.rstudio.com/web/packages/scatterplot3d/index.html) also draws 3D point clouds.
-   [tabplot](https://github.com/mtennekes/tabplot/) for exploratory data visualisation of tables
-   For schematic diagrams, such as Harris matrices, [DiagrammeR](https://github.com/rich-iannone/DiagrammeR) is useful.
-   For colour schemes in plots: [viridis](https://github.com/sjmgarnier/viridis) for perfectly perceptually-uniform colours, [RColorBrewer](http://cran.r-project.org/web/packages/RColorBrewer/index.html), [wesanderson](http://cran.r-project.org/web/packages/wesanderson/index.html), and  [munsell](http://cran.r-project.org/web/packages/munsell/index.html) for exploring and using the Munsell colour system, and for some extra themes for ggplot2, including some Tufte-inspired themes, see [ggthemes](http://cran.r-project.org/web/packages/ggthemes/index.html). 

**Analysis in general**

-    Base R, especially the stats package, has a lot of functionality useful for analysing archaeological data. For example, `chisq.test()`, `prop.test()`, `binom.test()`, `t.test()`, `wilcox.test()`, `kruskal.test()`, `mcnemar.test()`, `cor.test()`, `power.t.test()`, `power.prop.test()`, `power.anova.test()` among many others. [Hmisc](http://cran.r-project.org/web/packages/Hmisc/index.html) includes bootstrapping, setting confidence intervals, and power analysis functions, see also [psych](http://cran.r-project.org/web/packages/psych/index.html) for useful descriptive statistics and visualizations.
-    [corrr](https://cran.rstudio.com/web/packages/corrr/) contains many convenient functions for exploring correlations.
-    Bayesian and resampling variants of these also exist, for example in the [MCMCpack](http://cran.r-project.org/web/packages/MCMCpack/index.html), [BEST](http://cran.r-project.org/web/packages/BEST/index.html) (requires JAGS), [Bayesian First Aid](https://github.com/rasmusab/bayesian_first_aid) (also requires JAGS) packages (see the [Bayesian](http://cran.r-project.org/web/views/Bayesian.html) task view for more) and the [coin](http://cran.rstudio.com/web/packages/coin/index.html), [boot](http://cran.r-project.org/web/packages/boot/index.html), and [bootstrap](http://cran.r-project.org/web/packages/bootstrap/index.html) packages (see also [msm](http://cran.r-project.org/web/packages/msm/index.html)).
-    For analysing change over time, [bcp](http://cran.r-project.org/web/packages/bcp/index.html), [changepoint](http://cran.r-project.org/web/packages/changepoint/index.html), [ecp](http://cran.r-project.org/web/packages/ecp/index.html), [AnomalyDetection](https://github.com/twitter/AnomalyDetection) and [BreakoutDetection](https://github.com/twitter/BreakoutDetection) provide functions for detecting distributional changes within time-ordered observations.
-    [abc](http://cran.r-project.org/web/packages/abc/index.html) provides functions for parameter estimation, model selection, and goodness-of-fit.

**Analysis of categorical and count data**

- The `table()` function in the base package and the `xtabs()` and `ftable()` functions in the stats package construct contingency tables.
- The `chisq.test()` and `fisher.test()` functions in the stats package may be used to test for independence in two-way contingency tables
- The `assocstats()` function in the vcd package computes the Pearson chi-Squared test, the Likelihood Ratio chi-Squared test, the phi coefficient, the contingency coefficient and Cramer's V for plain or stratified contingency tables.

**Linear, generalized linear models, and non-linear models**

-  Linear models can be fitted (via OLS) with `lm()` (from stats). The [modelr](https://github.com/hadley/modelr) package has helper functions for pipeable modelling (e.g. cross-validation, bootstrapping). For data from a non-normal population, or when there are apparent outliers, [lmPerm](https://cran.r-project.org/web/packages/lmPerm) computes linear models using permutation tests.
-  Bayesian fitting of linear and non-linear models is possible with [rstanarm](https://cran.r-project.org/web/packages/rstanarm),  [brms](https://github.com/paul-buerkner/brms), and [rethinking](https://github.com/rmcelreath/rethinking).
-  The `nls()` function (from stats) as well as the package [minpack.lm](http://cran.rstudio.com/web/packages/minpack.lm/index.html) allow the solution of nonlinear least squares problems.
- Correlated and/or unequal variances can be modeled using the `gnls()` function of the [nlme](http://cran.rstudio.com/web/packages/nlme/index.html) package and by [nlreg](http://cran.rstudio.com/web/packages/nlreg/index.html). The nlme package is supported by Pinheiro & Bates (2000) Mixed-effects Models in S and S-PLUS, Springer, New York. 
-  The generic `anova()` function in the [stats](http://cran.rstudio.com/web/packages/stats/index.html) package constructs sequential analysis of variance and analysis of deviance tables, and can compute F and likelihood-ratio tests for nested models. (It is typical for other classes of statistical models in R to have anova methods as well.) The generic anova function in the [car](http://cran.rstudio.com/web/packages/car/index.html) package (associated with Fox, An R and S-PLUS Companion to Applied Regression, Sage, 2002) constructs so-called "Type-II" and "Type-III" tests for linear and generalized linear models.

**Multivariate statistics**

-   The [Cluster task view](http://cran.r-project.org/web/views/Cluster.html) provides a more detailed discussion of available cluster analysis methods and appropriate R functions and packages.
-  [caret](http://cran.rstudio.com/web/packages/caret/index.html) and [FactoMiner](http://cran.rstudio.com/web/packages/FactoMiner/index.html) are popular packages with a suite of multivariate methods
- [aplpack](http://cran.rstudio.com/web/packages/aplpack/index.html) provides `bagplots()`
- `lda()` and `qda()` within [MASS](http://cran.rstudio.com/web/packages/MASS/index.html) provide linear and quadratic discrimination respectively.

Model Testing and Validation

- [caret](http://cran.rstudio.com/web/packages/caret/index.html) provides many functions for model training, testing, and validation. There is also Max Kuhn's excellent companion book called "Applied Predictive Modeling" (Springer, also available as an ebook). The [mlr](http://cran.r-project.org/web/packages/mlr/index.html) package also provides classification, regression, and machine learning methods. 
-  Other packages that enable tuning and evaluation of models include bootstrap and [Hmisc](http://cran.rstudio.com/web/packages/Hmisc/index.html)
- The [CVtools](http://cran.rstudio.com/web/packages/CVtools/index.html) and [DAAG](http://cran.rstudio.com/web/packages/DAAD/index.html) packages include cross-validation functions for evaluating the optimality of tuning parameters such as sample sizes or number of predictors etc., in statistical models 
- [rsample](https://CRAN.R-project.org/package=rsample) creates different types of resamples and corresponding classes for their analysis

Hierarchical cluster analysis

-    The package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) provides functions for cluster analysis following the methods described in Kaufman and Rousseeuw (1990) Finding Groups in data: an introduction to cluster analysis, Wiley, New York
-    There are also `hclust()` in the stats package and `hcluster()` in [amap](http://cran.rstudio.com/web/packages/amap/index.html)
-    [pvclust](http://cran.rstudio.com/web/packages/pvclust/index.html) is a package for assessing the uncertainty in hierarchical cluster analysis. It provides approximately unbiased p-values as well as bootstrap p-values. Enhanced plotting is also available through the [dendextend](http://cran.rstudio.com/web/packages/dendextend/index.html) package.
-    [dendextend](http://cran.rstudio.com/web/packages/dendextend/index.html) Offers a set of functions for extending dendrogram objects in R. It allows to both adjust a tree's graphical parameters - the color, size, type, etc of its branches, nodes and labels - as well as visually (and statistically) compare different dendrograms to one another.

Other partitioning methods

-   `kmeans()` in stats provides k-means clustering and cmeans() in [e1071](http://cran.rstudio.com/web/packages/e1071/index.html) implements a fuzzy version of the k-means algorithm. The recommended package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) also provides functions for various partitioning methodologies.
-    To compute the optimum number of clusters there is the `pamk()` function in the [fpc](http://cran.rstudio.com/web/packages/fpc/index.html) package, `cascadeKM()` in [vegan](http://cran.rstudio.com/web/packages/vegan/index.html), `Mclust()` in [mclust](http://cran.rstudio.com/web/packages/mclust/index.html), `apcluster()` in [apcluster](http://cran.rstudio.com/web/packages/apcluster/index.html)
- Self-organising maps can be produced with the [kohonen](https://CRAN.R-project.org/package=kohonen)

Mixture models and model-based cluster analysis

-    [mclust](http://cran.rstudio.com/web/packages/mclust/index.html) and [flexmix](http://cran.rstudio.com/web/packages/flexmix/index.html) provide implementations of model-based cluster analysis.

Principle components and other projection, scaling, and ordination methods

-  Principal Components (PCA) is available via the `prcomp()` function (based on svd),  `rda()` (in package [vegan](http://cran.rstudio.com/web/packages/vegan/index.html)), `pca()` (in package [labdsv](http://cran.rstudio.com/web/packages/labdsc/index.html)) and `dudi.pca()` (in package [ade4](http://cran.rstudio.com/web/packages/ade4/index.html)), provide more ecologically-orientated implementations. Plotting of PCA output is available in [ggbiplot](https://github.com/vqv/ggbiplot) and [ggfortify](https://github.com/sinhrks/ggfortify). 
-   Redundancy Analysis (RDA) is available via `rda()` in vegan and `pcaiv()` in ade4. 
-   Canonical Correspondence Analysis (CCA) is implemented in `cca()` in both vegan and ade4. 
-   Detrended Correspondence Analysis (DCA) is implemented in `decorana()` in vegan. 
-   Principal coordinates analysis (PCO) is implemented in `dudi.pco()` in ade4, `pco()` in labdsv, `pco()` in [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html), and `cmdscale()` in package [MASS](http://cran.rstudio.com/web/packages/MASS/index.html).
-    Non-Metric multi-Dimensional Scaling (NMDS) is provided by `isoMDS()` in package MASS and `nmds()` in [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html). `nmds()`, a wrapper function for `isoMDS()`, is also provided by package [labdsv](http://cran.rstudio.com/web/packages/labdsv/index.html). vegan provides helper function `metaMDS()` for `isoMDS()`, implementing random starts of the algorithm and standardised scaling of the NMDS results. The approach adopted by vegan with `metaMDS()` is the recommended approach for ecological data.
- `corresp()` and `mca()` in MASS provide simple and multiple correspondence analysis respectively. [ca](http://cran.rstudio.com/web/packages/ca/index.html) also provides single, multiple and joint correspondence analysis. `ca()` and `mca()` in ade4 provide correspondence and multiple correspondence analysis respectively, as well as adding homogeneous table analysis with `hta()`. Further functionality is also available within vegan co-correspondence is available from cocorresp. [FactoMineR](http://cran.rstudio.com/web/packages/FactoMineR/index.html) provides `CA()` and `MCA()` which also enable simple and multiple correspondence analysis as well as associated graphical routines. [CAinterprTools](https://github.com/gianmarcoalberti/CAinterprTools) has functions for correspondence analysis and diagnostics. 
-    Seriation methods are available in [seriation](http://cran.rstudio.com/web/packages/seriation/index.html), which includes `bertinplot()` for producing battleship plots, and [CAseriation](https://github.com/gianmarcoalberti/CAseriation) which also has a battleship plotting function. 

Dissimilarity coefficients

- `dist()` in standard package stats, `daisy()` in recommended package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html), `vegdist()` in [vegan](http://cran.rstudio.com/web/packages/vegan/index.html), `dsvdis()` in [labdsv](http://cran.rstudio.com/web/packages/labdsv/index.html), `Dist()` in [amap](http://cran.rstudio.com/web/packages/amap/index.html), `distance()` in [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html), a suite of functions in [ade4](http://cran.rstudio.com/web/packages/ade4/index.html)
- [simba](http://cran.rstudio.com/web/packages/simba/index.html) provides functions for the calculation of similarity and multiple plot similarity measures with binary data (for instance presence/absence data)
- `distance()` in the [analogue](http://cran.rstudio.com/web/packages/analogue/index.html) package can be used to calculate dissimilarity between samples of one matrix and those of a second matrix. The same function can be used to produce pair-wise dissimilarity matrices, though the other functions listed above are faster. `distance()` can also be used to generate matrices based on Gower's coefficient for mixed data (mixtures of binary, ordinal/nominal and continuous variables). Function `daisy()` in package [cluster](http://cran.rstudio.com/web/packages/cluster/index.html) provides a faster implementation of Gower's coefficient for mixed-mode data than `distance()` if a standard dissimilarity matrix is required. Function `gowdis()` in package [FD](http://cran.rstudio.com/web/packages/FD/index.html) also computes Gower's coefficient and implements extensions to ordinal variables.
- [DistatisR](http://cran.rstudio.com/web/packages/DistatisR/index.html) provides functions for three-way multidimensional scaling for the analysis of multiple distance/covariance matrices collected on the same set of observations.
- Simple and partial Mantel tests to compute the Mantel statistic as a matrix correlation between two dissimilarity matrices are available in [vegan](http://cran.rstudio.com/web/packages/vegan/index.html) and [ecodist](http://cran.rstudio.com/web/packages/ecodist/index.html)


**Making maps and using R as a Geographical Information System**

- Making maps: [ggspatial](http://cran.rstudio.com/web/packages/ggspatial/index.html) for easy plotting of most kinds of spatial data, see also: [maps](http://cran.rstudio.com/web/packages/maps/index.html), [rworldmap](http://cran.rstudio.com/web/packages/rworldmap/index.html), [mapdata](http://cran.rstudio.com/web/packages/mapdata/index.html), [maptools](http://cran.rstudio.com/web/packages/maptools/index.html), [mapproj](http://cran.rstudio.com/web/packages/mapproj/index.html), [ggplot2](http://cran.rstudio.com/web/packages/ggplot2/index.html), [ggmap](http://cran.rstudio.com/web/packages/ggmap/index.html), [RgoogleMaps](http://cran.rstudio.com/web/packages/RgoogleMaps/index.html), [cartography](http://cran.rstudio.com/web/packages/cartography/index.html) [RColorBrewer](http://cran.rstudio.com/web/packages/RColorBrewer/index.html) 
- Scale bars and North arrows can be added to maps made with ggplot and ggmap using [GISTools](https://cran.r-project.org/web/packages/GISTools), [ggsn](https://github.com/oswaldosantos/ggsn) or [legendMap] (https://github.com/3wen/legendMap). 
- Interactive mapping of spatial objects with zooming and panning is possible with [leaflet](https://cran.rstudio.com/web/packages/leaflet/index.html) and geo[mapview](http://cran.rstudio.com/web/packages/mapview/index.html)
-   R has many packages that enable it to be used as a GIS for spatial analysis: [sf](http://cran.rstudio.com/web/packages/sf/index.html), [sp](http://cran.rstudio.com/web/packages/sp/index.html), [raster](http://cran.rstudio.com/web/packages/raster/index.html), [rasterVis](http://cran.rstudio.com/web/packages/rasterVis/index.html), [shapefiles](http://cran.rstudio.com/web/packages/shapefiles/index.html), [spatial](http://cran.rstudio.com/web/packages/spatial/index.html), [spatstat](http://cran.rstudio.com/web/packages/spatstat/index.html), [splancs](http://cran.rstudio.com/web/packages/splancs/index.html), [ipdw](http://cran.rstudio.com/web/packages/ipdw/index.html), [geoR](http://cran.rstudio.com/web/packages/geoR/index.html),  [argosfilter](http://cran.rstudio.com/web/packages/argosfilter/index.html), [ads](http://cran.rstudio.com/web/packages/ads/index.html), [spdep](http://cran.rstudio.com/web/packages/spdep/index.html), [gstat](http://cran.rstudio.com/web/packages/gstat/index.html), [GISTools](http://cran.rstudio.com/web/packages/GISTools/index.html)
-   [spgrass6](http://cran.rstudio.com/web/packages/spgrass6/index.html) and [rgrass7](http://cran.rstudio.com/web/packages/rgrass7/index.html) provides facilities for using all [GRASS](http://grass.osgeo.org/) geographical information system commands from the R command line. [RQGIS](https://github.com/jannes-m/RQGIS) establishes an interface between R and QGIS, i.e. it allows the user to access QGIS functionalities from within R.
-   [spdply](https://cran.r-project.org/web/packages/spdplyr) provides methods for dplyr verbs for 'sp' and 'Spatial' class objects.
-   [rgdal](http://cran.rstudio.com/web/packages/rgdal/index.html) uses the GDAL (Geospatial Data Abstraction Library) (raster) and OGR (vector) data I/O library, as well as PROJ.4 for CRS (coordinate reference systems) (re)projections
-   [rgeos](http://cran.rstudio.com/web/packages/rgeos/index.html) uses the GEOS (Geometry Open Source) library, which powers PostGIS: does the 'usual' geometry operations for features
-   The [Spatial](http://cran.r-project.org/web/views/Spatial.html) and [Spatio Temporal](http://cran.r-project.org/web/views/SpatioTemporal.html) task views have more details. 
-  [recexcavAAR](https://cran.r-project.org/web/packages/recexcavAAR/index.html) 3D Reconstruction of Archaeological Excavations

**Environmental & geological analysis**

-    Transfer function models including weighted averaging (WA), modern analogue technique (MAT), Locally-weighted WA, & maximum likelihood (aka Gaussian logistic) regression (GLR) are provided by [analogue](http://cran.rstudio.com/web/packages/analogue/index.html), [vegan](http://cran.rstudio.com/web/packages/vegan/index.html), and [rioja](http://cran.rstudio.com/web/packages/rioja/index.html) for stratigraphic analyses
-   [G2Sd](http://cran.rstudio.com/web/packages/G2Sd/index.html) gives full descriptive statistics and a physical description of sediments based on grain-size distributions, [soiltexture](http://cran.rstudio.com/web/packages/soiltexture/index.html) and [ggtern](http://cran.rstudio.com/web/packages/ggtern/index.html) for ternary plots of soil texture
-    Constrained clustering of stratigraphic data is provided by function `chclust()` in the form of constrained hierarchical clustering in [rioja](http://cran.rstudio.com/web/packages/rioja/index.html).
-    Stratigraphic columns can be plotted and analysed with the the [SDAR](http://run.unl.pt/bitstream/10362/14554/1/TGEO0128.pdf) package. 
-    Benn diagrams can be drawn with [plotrix](http://cran.rstudio.com/web/packages/plotrix/index.html) and Woodcock diagrams with [RFOC](http://cran.rstudio.com/web/packages/RFOC/index.html).
- Function for circular statistics such as the Rayleigh test and many others, can be found in [CircStats](https://cran.r-project.org/web/packages/CircStats/index.html), [RFOC](https://cran.rstudio.com/web/packages/RFOC/index.html), [circular](https://cran.rstudio.com/web/packages/circular/index.html), [Directional](https://cran.r-project.org/web/packages/Directional/), and [heR.Misc](http://exposurescience.org/hosted-projects/inhalation-exposure-simulation-modeling-project/the-her-software-project)
- The [siar](http://cran.rstudio.com/web/packages/siar/index.html) package takes data on organism isotopes and fits a Bayesian model to their dietary habits based upon a Gaussian likelihood with a mixture dirichlet-distributed prior on the mean
-    The [zooaRch](http://cran.r-project.org/web/packages/zooaRch/) package has functions for survival analysis of zooarchaeological datasets
-    Functions for tree ring analysis can be found in [dplR](http://cran.rstudio.com/web/packages/dplR/index.html)
- See the [Environmetrics](http://cran.r-project.org/web/views/Environmetrics.html) task view for more.

**Dating**
-    Radiocarbon dates can be calibrated using [Bchron](http://cran.rstudio.com/web/packages/Bchron/index.html) with various calibration curves (including user generated ones); also does Age-depth modelling, relative sea level rate estimation incorporating time uncertainty in polynomial regression models; and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM). Some of these methods can also be found in [rcarbon](https://github.com/ahb108/rcarbon).
-    Bayesian age-depth modelling of radiocarbon dates is also available in [Bacon](http://chrono.qub.ac.uk/blaauw/bacon.html), and [clam](http://chrono.qub.ac.uk/blaauw/) contains functions for "classical", non-Bayesian age-depth modelling. These are not R packages, but [clam](https://github.com/SimonGoring/clam) has been packaged for easy use.
-    The [oxcAAR](https://github.com/ISAAKiel/oxcAAR) package allows you to use R to connect to a local installation of the OxCal software to calibrate radiocarbon dates and a variety of other OxCal operations. 
- [ArchaeoPhases](https://cran.r-project.org/package=ArchaeoPhases) provides statistical tools to analyze and to estimate archaeological phases from the posterior distribution (i.e. MCMC samples) of a sequence of dates. Includes testing procedures to check the presence of a gap between two successive phases or periods.
-    Various R functions for Luminescence Dating data analysis are in the [Luminescence](http://cran.rstudio.com/web/packages/Luminescence/index.html) package (including radial plotting) and in the [numOSL](https://cran.r-project.org/web/packages/numOSL/index.html) package, including equivalent dose calculation, annual dose rate determination, growth curve fitting, decay curve decomposition, statistical age model optimization, and statistical plot visualization.
-    The [archSeries](https://github.com/davidcorton/archSeries) makes chronologies from information from multiple entities with varying chronological resolution and overlapping date ranges
- For time series analysis using calendar dates, [zoo](https://cran.r-project.org/package=zoo) and [padr](https://cran.r-project.org/package=padr) are useful.
 

**Phylogenetics, morphometrics, evolution and shape analysis**

-  The [Phylogenetics task view](http://cran.r-project.org/web/views/Phylogenetics.html) provides more detailed coverage of the subject area and related functions within R. 
-  Packages specifically tailored for the analysis of phylogenetic and evolutionary data include: [ape](http://cran.rstudio.com/web/packages/ape/index.html), [phytools](http://cran.rstudio.com/web/packages/phytools/index.html), [phangorn](http://cran.rstudio.com/web/packages/phangorn/index.html), [Rphylip](http://cran.rstudio.com/web/packages/Rphylip/index.html) (requires PHYLIP), [ouch](http://cran.rstudio.com/web/packages/ouch/index.html), and [pegas](http://cran.rstudio.com/web/packages/pegas/index.html). 
-  For plotting trees most of these packages include their own modifications of the base `plot()` function, and there are also [ggtree](http://cran.rstudio.com/web/packages/ggtree/index.html), [ggdendro](http://cran.rstudio.com/web/packages/ggdendro/index.html), [dendextend](http://cran.rstudio.com/web/packages/dendextend/index.html), and [ggphylo](http://cran.rstudio.com/web/packages/ggphylo/index.html)
-  Morphometric and shape analysis methods are provided by [shapes](http://cran.rstudio.com/web/packages/shapes/index.html), [geomorph](http://cran.rstudio.com/web/packages/geomorph/index.html), [paleomorph](https://cran.r-project.org/web/packages/paleomorph) and [Momocs](http://cran.rstudio.com/web/packages/Momocs/index.html). Related packages include [shapeR](https://github.com/lisalibungan/shapeR) [Anthropometry](http://cran.rstudio.com/web/packages/Anthropometry/index.html) and [Morpho](http://cran.rstudio.com/web/packages/Morpho/index.html).
- [StereoMorph](http://cran.rstudio.com/web/packages/StereoMorph/index.html) allows users to collect 3D landmarks and curves from objects using two standard digital cameras. 

**Image analysis**

-   [pixmap](http://cran.rstudio.com/web/packages/pixmap/index.html) provides methods for creating, plotting and converting bitmapped images in three different formats: RGB, grey and indexed pixmaps. Similarly, [jpeg](http://cran.rstudio.com/web/packages/jpeg/index.html) provides an easy and simple way to read, write and display bitmap images stored in the JPEG format.
-   [EBImage](http://www.bioconductor.org/packages/release/bioc/html/EBImage.html) (requires ImageMagick) provides general purpose functionality for the reading, writing, processing and analysis of images (and is very well documented). Various functions for image processing and analysis can also be found in [ripa](http://cran.rstudio.com/web/packages/ripa/index.html) and [imager](https://github.com/dahtah/imager)
-   [magick](https://github.com/jeroenooms/magick) provides bindings to the [ImageMagick image-processing library](http://www.imagemagick.org/), the most comprehensive open-source image processing package available.

**Simulations**

- [RNetLogo](http://cran.rstudio.com/web/packages/RNetLogo/index.html) links R and NetLogo
-  [simecol](http://cran.rstudio.com/web/packages/simecol/index.html)  for simulating ecological (and other) dynamic systems. It can be used for differential equations, individual-based (or agent-based) and other models as well.
-  One-dimensional cellular automata are also possible to model with the package [CellularAutomaton](http://cran.rstudio.com/web/packages/CellularAutomaton/index.html).

**Network analysis**

-    The two major packages are [igraph](http://cran.rstudio.com/web/packages/igraph/index.html), which is a generic network analysis and visualisation package, and [sna](http://cran.rstudio.com/web/packages/sna/index.html), which performs social analysis of networks.
-    Other packages include [statnet](http://cran.rstudio.com/web/packages/statnet/index.html), [intergraph](http://cran.rstudio.com/web/packages/intergraph/index.html), [network](http://cran.rstudio.com/web/packages/network/index.html) (manipulates and displays network objects), [ergm](http://cran.rstudio.com/web/packages/ergm/index.html) (a set of tools to analyze and simulate networks based on exponential random graph models exponential random graph models), [hergm](http://cran.rstudio.com/web/packages/hergm/index.html) (implements hierarchical exponential random graph models), and [RSiena](http://cran.rstudio.com/web/packages/RSiena/index.html) (allows the analyses of the evolution of social networks using dynamic actor-oriented models)

**Mortality Analysis**

- [mortAAR](https://cran.r-project.org/web/packages/mortAAR/index.html) Analysis of Archaeological Mortality Data

**Reproducible research**

-   [knitr](http://cran.rstudio.com/web/packages/knitr/index.html) enables R code and text with formatting instructions (eg. markdown or LaTeX) to be combined in a single document and executed to produce a document that contains rendered plots, analysed data and formatted text. The [remake](https://github.com/richfitz/remake) package has functions that enable declarative workflows so that each time an analysis is run, it updates only the parts of the workflow that have changed. 
-   The [rrrpkg](https://github.com/ropensci/rrrpkg) essay explains why the R package is a suitable file-and-folder structure for almost any research project, with real-world examples, and lead to [rrtools](https://github.com/benmarwick/rrtools), a package that provides instructions, templates, and functions for making a basic compendium suitable for doing reproducible research with R. [manuscriptPackage](https://github.com/jhollist/manuscriptPackage), [template](https://github.com/cboettig/template), [template](https://github.com/Pakillo/template) (yes, that's two slightly different packages with the same name), and [prodigenr](https://github.com/lwjohnst86/prodigenr), [makeProject](https://cran.r-project.org/web/packages/makeProject), and [ProjectTemplate](https://cran.r-project.org/web/packages/ProjectTemplate/index.html) are packages that give templates for organising an analysis as an R package (eg. where the manuscript is the package vignette, or similarly bundled with the package). [rlp](https://github.com/yihui/rlp) is a package that lets you write an analysis as a Rmd file and then converts it into a package.
-   The [rmarkdown](http://cran.rstudio.com/web/packages/rmarkdown/index.html) package implements the simple markdown document formatting language with some minor customizations to recognize R code blocks and inline code. The  [bookdown](http://cran.rstudio.com/web/packages/bookdown/index.html) package provides tools for single file and multi-chapter rmarkdown documents with all the usual scholarly accessories: citations, figures, tables, captions and cross-referencing. [captioner](https://github.com/adletaw/captioner) and [kfigr](https://github.com/mkoohafkan/kfigr) also provide functions for figure and table captions and cross-referencing in Rmd documents. 
-   The [rticles](https://github.com/rstudio/rticles) package includes templates for converting markdown documents into PDF files formatted ready for submission for publication, such as in the PLOS journals, the Frontiers In journals, and Elsevier journals. Similarly, the [papaja](https://github.com/crsh/papaja) packge contains a template for converting a markdown file into an APA-formatted PDF. These packages depend on [pandoc](http://johnmacfarlane.net/pandoc/), a universal document format converter (not an R package). In this context it is used to convert rmarkdown or LaTeX to PDF, MS Word or HTML files. It is included with RStudio but can also be used stand-alone from the command line. 
-   [packrat](http://cran.rstudio.com/web/packages/packrat/index.html) supports the development of isolated, stand-alone projects that include all the packages used and their dependencies. [miniCRAN](http://cran.rstudio.com/web/packages/miniCRAN/index.html) has functions to create a local repository to install packages (and their dependancies) from without internet access. Related packages include [rbundler](http://cran.rstudio.com/web/packages/rbundler/index.html) for package development which manages dependencies listed in a package's DESCRIPTION file by storing them in a local project-specific library for installation, and [pkgsnap](https://github.com/MangoTheCat/pkgsnap) for creating a snapshot of your installed CRAN packages with 'snap', and then using 'restore' on another system to recreate exactly the same environment.
-   [checkpoint](http://cran.rstudio.com/web/packages/checkpoint/index.html) allows you to install R packages from a specific snapshot date in the past, ensuring that you use the same package version that you started with, not a more recent one (related: [gRAN](https://github.com/rgmbecker/gRAN) can retrieve and build sources for any version of any non-base package that has ever been released on CRAN or BioConductor).
-   [rocker](https://github.com/rocker-org/rocker) is a project that provides Docker containers to run R in a lightweight virtual environment, the hadleyverse container includes dplyr, ggplot2, etc., as well as RStudio server and LaTeX. The package [harbor](https://github.com/wch/harbor) provides functions for controlling docker containers on local and remote hosts. The [analogsea](https://github.com/sckott/analogsea) package has functions for deploying R and RStudio quickly & easily on DigitalOcean clusters using Docker images for cloud computing. The [dockertest](https://github.com/richfitz/dockertest) package contains functions for generating Dockerfiles from R packages and other R projects, and building Docker containers that contains all the package dependencies. [liftr](https://CRAN.R-project.org/package=liftr) helps with persistent reproducible reporting by containerization of R Markdown documents.

**Developing R code and packages**

-   [devtools](http://cran.rstudio.com/web/packages/devtools/index.html) (requires Rtools for Windows or Xcode for OSX) for easily creating R packages. [usethis](https://CRAN.R-project.org/package=usethis) automates many tasks surrouding package-making, including `use_travis()` and related functions for easily adding continuous integration for automated building and testing during package development. [Mason](https://github.com/metacran/mason) helps you to quickly build R packages using an interactive Q&A to generate metadata files, READMEs with badges, git repositories, etc.
-   [Goodpractice](https://github.com/MangoTheCat/goodpractice) gives advice about good practices when building R packages. Advice includes functions and syntax to avoid, package structure, code complexity, code formatting, etc.
-   [badgecreatr](https://github.com/RMHogervorst/badgecreatr) generates badges for your readme file to signal the quality and current status of your package. 
-   [roxygen2](http://cran.rstudio.com/web/packages/roxygen2/index.html) for simplifying the creation of documentation for packages,
-   [testthat](http://cran.rstudio.com/web/packages/testthat/index.html) for developing tests of functions in packages
-   [Rcpp](http://cran.rstudio.com/web/packages/Rcpp/index.html) enables the use of C++ code in R packages for high performance computing, requires Rtools for Windows or Xcode for OSX
-   [editR](https://github.com/swarm-lab/editR) is a basic Rmarkdown editor with instant previewing of your document. It allows you to create and edit Rmarkdown documents while instantly previewing the result of your writing and coding.
-   [RStudio](http://www.rstudio.com/) is an integrated development environment that simplfies developing R code with numerous built-in conveniences, including vim keyboard shortcuts. There are also packages that make scholarly writing in RStudio easy: [wordcountaddin](https://github.com/benmarwick/wordcountaddin), [citr](https://github.com/crsh/citr). And several for making nice tables: [carpenter)](https://github.com/lwjohnst86/carpenter), [htmlTable)](https://cran.r-project.org/web/packages/htmlTable),  [pixiedust](https://cran.r-project.org/web/packages/pixiedust/index.html), [pander](https://github.com/Rapporter/pander), [simpletable](https://github.com/jalapic/simpletable) [stargazer](https://cran.r-project.org/web/packages/stargazer/)
-   [Emacs](http://www.gnu.org/software/emacs/) is a highly flexible text editor, which when used with the [Emacs Speaks Statistics](http://ess.r-project.org/) package, is a comprehensive R development environment. [Org-mode](http://orgmode.org/) provides a literate programming environment in Emacs similar to knitr. 
-   [Style guide for writing R code](http://adv-r.had.co.nz/Style.html) by Hadley Wickham, and the packages [formatR](http://cran.rstudio.com/web/packages/formatR/index.html) and [rfmt](https://github.com/google/rfmt) which are designed to reformat R code to improve readability. The [lintr](http://cran.r-project.org/web/packages/lintr/) package analyses code to check that it conforms to Hadley Wickham's style guide (this package is built into RStudio)
-   Idioms of R are discussed in the [vignette](http://cran.r-project.org/web/packages/rockchalk/vignettes/Rchaeology.pdf) of the [rockchalk](http://cran.rstudio.com/web/packages/rockchalk/index.html) package, and Pat Burn's essay [the R Inferno](http://www.burns-stat.com/documents/books/the-r-inferno/).

**Datasets**

-   [archdata](http://cran.rstudio.com/web/packages/archdata/index.html) contains eleven archaeological datasets from around the world reported in published studies. These represent typical forms of archaeological data (and so are useful for teaching)
-   [binford](https://github.com/benmarwick/binford) contains more than 200 variables coding aspects of hunter-gatherer subsistence, mobility, and social organization for 339 ethnographically documented groups of hunter-gatherers, as used in Binford (2001) _Constructing Frames of Reference: An Analytical Method for Archaeological Theory Building Using Ethnographic and Environmental Data Sets_
-  [BSDA](http://cran.rstudio.com/web/packages/BSDA/index.html) contains a dataset of 60 radiocarbon ages of observations taken from an archaeological site with four phases of occupation.
-  [cawd](https://github.com/sfsheath/cawd) contains 15 datasets of ancient Greek, Roman and Persian maps and digital atlas data 
-  [chemometrics](http://cran.rstudio.com/web/packages/chemometrics/index.html) contains a dataset of elemental concentrations for 180 archaeological glass vessels excavated from 15th - 17th century contexts in Antwerp.
-  [zooaRch](http://cran.r-project.org/web/packages/zooaRch/) contains two zooarchaeological datasets.
-  [gsloid](https://CRAN.R-project.org/package=gsloid) Contains published data sets for global benthic d18O data for 0-5.3 Myr and global sea levels based on marine sediment core data for 0-800 ka


**Places to go for help**

- `?` function, eg. `?mean` to get built-in help on the mean function
- `sos::findFn("rose diagram")` searches all installed packages for the search term, using the [sos](http://cran.rstudio.com/web/packages/sos/index.html) package
-   Most major packages come with vignettes that narrate typical uses of the package's core functions. Vignettes can be accessed with the command `vignette(packagename)`.
- Google searches in the form: [r help [search terms]](https://www.google.com/?gws_rd=ssl#q=r+help+)
-   A custom search engine of R resources: http://www.rseek.org/
-   [Graphical output from the examples in the documentation for all CRAN packages](http://rgm3.lab.nig.ac.jp/RGM)
-   All R package documentation (including CRAN, GitHub and Bioconductor packages) is online in an easy-to-ready format at http://www.rdocumentation.org/
-   Cheatsheets to print for handy reference: [short one on base](http://cran.r-project.org/doc/contrib/Short-refcard.pdf), [longer one on base](http://cran.r-project.org/doc/contrib/Baggott-refcard-v2.pdf), [ggplot2, dplyr, tidyr, rmarkdown, making packages](http://www.rstudio.com/resources/cheatsheets/), [data.table](https://s3.amazonaws.com/assets.datacamp.com/img/blog/data+table+cheat+sheet.pdf), [using colours](https://www.nceas.ucsb.edu/~frazier/RSpatialGuides/colorPaletteCheatsheet.pdf), [colours](http://research.stowers-institute.org/efg/R/Color/Chart/ColorChart.pdf), [numerous others](http://devcheatsheet.com/tag/r/)
-  [stackoverflow](http://stackoverflow.com/questions/tagged/r) is an online Q&A point-scoring website where questions and answers can be voted on to indicate their quality. Many highly skilled R programmers are active participants. [Cross Validated](http://stats.stackexchange.com/) is a similar Q&A site for questions about statistics
-   You could send a message to the official [r-help email list](https://stat.ethz.ch/mailman/listinfo/r-help), but do be sure to read, follow and cite the [posting guide](http://www.r-project.org/posting-guide.html). The list is also [searchable](https://www.google.com/?gws_rd=ssl#q=site:stat.ethz.ch+pipermail+archaeology).


### Related links:

-   CRAN Task View: [SocialSciences](http://cran.rstudio.com/web/views/SocialSciences.html)
-   CRAN Task View: [Spatial](http://cran.rstudio.com/web/views/Spatial.html)
-   CRAN Task View: [Spatio-temporal](http://cran.rstudio.com/web/views/spatioTemporal.html)
-   CRAN Task View: [Cluster analysis](http://cran.r-project.org/web/views/Cluster.html)
-   CRAN Task View: [Multivariate Statistics](http://cran.r-project.org/web/views/Multivariate.html) 
-   CRAN Task View: [Bayesian inference](http://cran.r-project.org/web/views/Bayesian.html)
-   CRAN Task View: [Phylogenetics](http://cran.r-project.org/web/views/Phylogenetics.html)
-   CRAN Task View: [Robust](http://cran.r-project.org/web/views/Robust.html)
-   CRAN Task View: [Visualization](http://cran.r-project.org/web/views/Graphics.html)
-   CRAN Task View: [Reproducible research](http://cran.r-project.org/web/views/ReproducibleResearch.html) 
-   [David L. Carlson's guides on using R for 'Quantifying Archaeology' by Stephen Shennan 'Statistics for Archaeologists' by Robert Drennan]( http://people.tamu.edu/~dcarlson/quant/index.html)
-   [Matt Peeples' scripts for archaeological statistics]( http://www.mattpeeples.net/resources.html)
-   [Gianmarco Alberti's pages on Correspondence Analysis in Archaeology](http://cainarchaeology.weebly.com/)
-   [Quantitative Archaeology Wiki](http://wiki.iosa.it/doku.php), including [some code for battleship plots](http://wiki.iosa.it/dokuwiki/doku.php?id=contingency_tables)
-  [Michael Baxter's 'Notes on Quantitative Archaeology using R'](http://www.mikemetrics.com/r-chaeology/4568129078)
-   [GitHub repository for this Task View](https://github.com/benmarwick/ctv-archaeology)

#### Publications that include R code

d'Alpoim Guedes J, Jin G, Bocinsky RK (2015) The Impact of Climate on the Spread of Rice to North-Eastern China: A New Look at the Data from Shandong Province. PLOS ONE 10(6): e0130430. doi: <http://dx.doi.org/10.1371/journal.pone.0130430>

Barton, C. M., Tortosa, J. E. A., Garcia-Puchol, O., Riel-Salvatore, J. G., Gauthier, N., Conesa, M. V., & Bouchard, G. P. (2017). Risk and resilience in the late glacial: A case study from the western Mediterranean. _Quaternary Science Reviews_. <https://doi.org/10.1016/j.quascirev.2017.09.015>

Cardillo, Marcelo, Scartascini Federico Luis and Zangrando Atilio Francisco 2015 Combining morphological and metric variations in the study of design and functionality in stone weights. A comparative approach from continental and insular Patagonia, Argentina. _Journal of Archaeological Science: Reports_ 4:578-587. <http://dx.doi.org./10.1016/j.jasrep.2015.10.028>

Clarkson, C., Mike Smith, Ben Marwick, Richard Fullagar, Lynley A. Wallis, Patrick Faulkner, Tiina Manne, Elspeth Hayes, Richard G. Roberts, Zenobia Jacobs, Xavier Carah, Kelsey M. Lowe, Jacqueline Matthews, S. Anna Florin 2015 The archaeology, chronology and stratigraphy of Madjedbebe (Malakunanja II): A site in northern Australia with early occupation. _Journal of Human Evolution_  8, 46–64 [http://dx.doi.org/10.1016/j.jhevol.2015.03.014](http://dx.doi.org/10.1016/j.jhevol.2015.03.014)

Conrad, C., Higham, C., Eda, M. and Marwick, B. (2016) Paleoecology and Forager Subsistence Strategies During the Pleistocene-Holocene Transition: A Reinvestigation of the Zooarchaeological Assemblage from Spirit Cave, Mae Hong Son Province, Thailand. _Asian Perspectives_ 55(1). https://github.com/cylerc/AP_SC

Contreras, Daniel A. and John Meadows. (2014) “Summed radiocarbon calibrations as a population proxy: a critical evaluation using a realistic simulation approach.” Journal of Archaeological Science 52:591-608. [doi:10.1016/j.jas.2014.05.030] (http://www.sciencedirect.com/science/article/pii/S0305440314002088)

Crema, E.R., Kandler, A., Shennan, S., 2016. Revealing patterns of cultural transmission from frequency data: equilibrium and non-equilibrium assumptions, Scientific Reports 6, 39122.

Crema, E. R., J. Habu, K. Kobayashi and M. Madella (2016). "Summed Probability Distribution of <sup>14</sup>C Dates Suggests Regional Divergences in the Population Dynamics of the Jomon Period in Eastern Japan." [PLoS ONE 11(4): e0154809.](http://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0154809), [GitHub repo](https://github.com/ercrema/Jomon_SPD_Comparison), [Zenodo repo](http://dx.doi.org/10.5281/zenodo.47339).

Crema, E.R., K. Edinborough, T. Kerig, S.J. Shennan (2014) An Approximate Bayesian Computation approach for inferring patterns of cultural evolutionary change, Journal of Archaeological Science, Volume 50 Pages 160-170 [http://dx.doi.org/10.1016/j.jas.2014.07.014](http://www.sciencedirect.com/science/article/pii/S0305440314002593)

Drake BL, Wills WH, Hamilton MI, Dorshow W (2014) Strontium Isotopes and the Reconstruction of the Chaco Regional System: Evaluating Uncertainty with Bayesian Mixing Models. PLoS ONE 9(5): e95580. [doi:10.1371/journal.pone.0095580](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0095580)

Drake, Brandon L., David T. Hanson, James L. Boone (2012) The use of radiocarbon-derived Δ13C as a paleoclimate indicator: applications in the Lower Alentejo of Portugal, Journal of Archaeological Science, Volume 39, Issue 9, September 2012, Pages 2888-2896, [http://dx.doi.org/10.1016/j.jas.2012.04.027](http://www.sciencedirect.com/science/article/pii/S0305440312001471)

Drake, Brandon L., (2012) The influence of climatic change on the Late Bronze Age Collapse and the Greek Dark Ages, Journal of Archaeological Science, Volume 39, Issue 6, June 2012, Pages 1862-1870 [http://dx.doi.org/10.1016/j.jas.2012.01.029](http://www.sciencedirect.com/science/article/pii/S0305440312000416)

Drake, Brandon L., WH Wills, and Erik B Erhardt (2012) The 5.1 ka aridization event, expansion of piñon-juniper woodlands, and the introduction of maize (Zea mays) in the American Southwest The Holocene December 2012 22: 1353-1360, first published on July 9, 2012 [doi:10.1177/0959683612449758](http://hol.sagepub.com/content/22/12/1353.short)

Dye, Thomas S. (2011). “A Model-based Age Estimate for Polynesian Colonization of Hawai‘i”. _Archaeology in Oceania_ 46, pp. 130–138 [https://github.com/tsdye/hawaii-colonization](https://github.com/tsdye/hawaii-colonization)

Dye, T. S. (2016). "Long-term rhythms in the development of Hawaiian social stratification." [_Journal of Archaeological Science_]<http://www.sciencedirect.com/science/article/pii/S030544031630053X> 71: 1-9.

Giusti, D., Tourloukis, V., Konidaris, G., Thompson, N., Karkanas, P., Panagopoulou, E., & Harvati, K. (2018). Beyond maps: patterns of formation processes at the Middle Pleistocene open-air site of Marathousa 1, Megalopolis Basin, Greece. _Quaternary International._ <https://doi.org/10.1016/j.quaint.2018.01.041>

Giusti, D. and M. Arzarello, 2016, The need for a taphonomic perspective in spatial analysis: Formation processes at the Early Pleistocene site of Pirro Nord (P13), Apricena, Italy, _Journal of Archaeological Science: Reports_ 8, 235--249 code and data: <https://github.com/dncgst/pirronord_jas-reports>

Huffer, D. and Graham, S. 2017 The Insta-Dead: the rhetoric of the human remains trade on Instagram, _Internet Archaeology_ 45. <https://doi.org/10.11141/ia.45.5>, code & data: <https://zenodo.org/record/546132>

King, C. L., Millard, A. R., Gröcke, D. R., Standen, V. G., Arriaza, B. T., & Halcrow, S. E. (2018). Marine resource reliance in the human populations of the Atacama Desert, northern Chile–A view from prehistory. _Quaternary Science Reviews_, 182, 163-174. <https://doi.org/10.1016/j.quascirev.2017.12.009>

Lightfoot E and O'Connell TC (2016).“On The Use of Biomineral Oxygen Isotope Data to Identify Human Migrants in the Archaeological Record: Intra-Sample Variation, Statistical Methods and Geographical Considerations.” PLoS ONE 11(4). [http://doi:10.1371/journal.pone.0153850](http://doi:10.1371/journal.pone.0153850), code and data: [https://www.repository.cam.ac.uk/handle/1810/252773](https://www.repository.cam.ac.uk/handle/1810/252773)

Lowe, K., Wallis, L., Pardoe, C., Marwick, B., Clarkson, C., Manne, T., Smith, M. and R. Fullagar 2014 Ground-penetrating radar and burial practices in western Arnhem Land, Australia. _Archaeology in Oceania_  49(3): 148–157 [http://onlinelibrary.wiley.com/doi/10.1002/arco.5039/abstract](http://onlinelibrary.wiley.com/doi/10.1002/arco.5039/abstract)

Mackay A, Sumner A, Jacobs Z, Marwick B, Bluff K and Shaw M 2014. Putslaagte 1 (PL1), the Doring River, and the later Middle Stone Age in southern Africa's Winter Rainfall Zone. _Quaternary International_ [http://dx.doi.org/10.1016/j.quaint.2014.05.007](http://dx.doi.org/10.1016/j.quaint.2014.05.007)

Marwick, B., Hiscock, P., Sullivan, M., & Hughes, P. 2017 Landform boundary effects on Holocene forager landscape use in arid South Australia. _Journal of Archaeological Science: Reports_ <http://doi.org/10.1016/j.jasrep.2017.07.004>

Marwick, Ben, Elspeth Hayes, Chris Clarkson and Richard Fullagar 2017 Movement of lithics by trampling: An experiment in the Madjedbebe sediments, northern Australia. _Journal of Archaeological Science_ 79:73-85. <http://dx.doi.org/10.1016/j.jas.2017.01.008>, <https://github.com/benmarwick/mjbtramp>,  <http://dx.doi.org/10.17605/OSF.IO/32A87> 

Marwick, B., Van Vlack, H.G., Conrad, C., Shoocongdej, R., Thongcharoenchaikit, C., Kwak, S. 2016 Adaptations to sea level change and transitions to agriculture at Khao Toh Chong rockshelter, Peninsular Thailand, _Journal of Archaeological Science_  <http://dx.doi.org/10.1016/j.jas.2016.10.010>, <https://github.com/benmarwick/ktc11>, <https://osf.io/axxf8/>

Marwick, B, C. Clarkson, S. O'Connor & S. Collins 2016 "Pleistocene-aged stone artefacts from Jerimalai, East Timor: Long term conservatism in early modern human technology in island Southeast Asia" _Journal of Human Evolution_ DOI: 10.1016/j.jhevol.2016.09.004, <https://github.com/benmarwick/Pleistocene-aged-stone-artefacts-from-Jerimalai--East-Timor>, <https://osf.io/63zey>

Marwick, B. 2017. Computational reproducibility in archaeological research: Basic principles and a case study of their implementation. _Journal of Archaeological Method and Theory_ 1-27. [doi: 10.1007/s10816-015-9272-9](http://dx.doi.org/10.1007/s10816-015-9272-9), [text source repo](https://github.com/benmarwick/basic_computational_reproducibility_case_study)

Marwick, B., 2013. Multiple Optima in Hoabinhian flaked stone artefact palaeoeconomics and palaeoecology at two archaeological sites in Northwest Thailand. _Journal of Anthropological Archaeology_ 32, 553-564.  [http://dx.doi.org/10.1016/j.jaa.2013.08.004](http://dx.doi.org/10.1016/j.jaa.2013.08.004)

Marwick, B. 2013. Discovery of Emergent Issues and Controversies in Anthropology Using Text Mining, Topic Modeling, and Social Network Analysis of Microblog Content. In Yanchang Zhao, Yonghua Cen (eds) _Data Mining Applications with R_ Elsevier. p. 63-93 [https://github.com/benmarwick/AAA2011-Tweets](https://github.com/benmarwick/AAA2011-Tweets)

McPherron SP 2018 Additional statistical and graphical methods for analyzing site formation processes using artifact orientations. _PLOS ONE_ 13(1): e0190195. <https://doi.org/10.1371/journal.pone.0190195>

Nakoinz, O., D. Knitter (2016) _Modelling Human Behaviour in Landscapes. Basic Concepts and Modelling Elements_. Quantitative Archaeology and Archaeological Modelling 1. Springer, New York. <https://github.com/dakni/mhbil>, <https://github.com/ISAAKiel>

Negre, J., Muñoz, F., & Barceló, J. A. (2017). A Cost-Based Ripley’s K Function to Assess Social Strategies in Settlement Patterning. _Journal of Archaeological Method and Theory_, 1-18. <https://doi.org/10.1007/s10816-017-9358-7>
 
Negre, J., Muñoz, F., Lancelotti, C., 2016. Geostatistical modelling of chemical residues on archaeological floors in the presence of barriers, _J Archaeol Sci_ 70, 91-101. https://github.com/famuvie/ArchaeologicalFloors

Orton, D., Gaastra, J., & Vander Linden, M. (2016). Between the Danube and the Deep Blue Sea: Zooarchaeological Meta-Analysis Reveals Variability in the Spread and Development of Neolithic Farming across the Western Balkans. Open Quaternary, 2, 6. DOI: <http://doi.org/10.5334/oq.28> data & code: <http://eprints.whiterose.ac.uk/104121/>

Shennan, SJ, Enrico R. Crema, Tim Kerig, (2014) Isolation-by-distance, homophily, and 'core' vs. 'package' cultural evolution models in Neolithic Europe, _Evolution and Human Behavior_, Available online 2 October 2014,  [http://dx.doi.org/10.1016/j.evolhumbehav.2014.09.006](http://www.sciencedirect.com/science/article/pii/S1090513814001251)

Steele, Teresa E., Alex Mackay, Kathryn E. Fitzsimmons, Marina Igreja, Ben Marwick, Jayson Orton, Steve Schwortz, and Mareike C. Stahlschmidt (2016) "Varsche Rivier 003: A Middle and Later Stone Age Site with Still Bay and Howieson's Poort Assemblages in Southern Namaqualand, South Africa" _PaleoAnthropology_ 2016:100-163 <http://www.paleoanthro.org/media/journal/content/PA20160100.pdf>, < http://dx.doi.org/10.5281/zenodo.31903> 

#### Contributors

[Ben Marwick](https://github.com/benmarwick), Agustin Diez Castillo, Allar Haav, Sebastian Heath, Phil Riris, Tom Brughmans, Lee Drake, Stefano Costa, Enrico Crema, [Domenico Giusti](https://github.com/dncgst), Matt Peeples, Mark Madsen, Daniel Contreras, [Tal Galili](https://github.com/talgalili)
