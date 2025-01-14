# PGL-Data-Visualization-Course

This is the repository that holds necessary code and documentation required to learn data visualization inside and outside R environment. You should also familiarize yourself with the basics of R/Rstudio from the [following lecture](https://www.youtube.com/watch?v=dQe3Z7hRG1s) or my personal favourite DataCamp videos [here](https://www.youtube.com/watch?v=gzXsjmhG_VI&list=PLFOq4OXbrQTB7Am7YBDBw02wtfuSRQGwN) (but this doesn't contain the Rstudio as they code in their own webbased Rstudio like environment).

# Prepare R environment
Kindly install the following packages first. If you don't have R or R-Studio download it from here: https://posit.co/download/rstudio-desktop/

```r
if (!require("BiocManager", quietly = TRUE)) install.packages("BiocManager",repos='http://cran.us.r-project.org',dependencies = TRUE)

## Install Biocmanager packages
if (!suppressMessages(require("Biostrings", quietly = TRUE,warn.conflicts = FALSE))) BiocManager::install(c('Biostrings',"S4Vectors","ggtree"))

## Install CRAN packages
packages <- c('dplyr',"BiocManager",'stringr','pacman','tidyr','ggplot2','R3port','ggpubr','plotly','data.table','argparse','ggsci','htmlwidgets','egg',
'remotes','ggplot2',"ggvenn","ggVennDiagram","grafify","esquisse","ggeasy","shinythemes")
install.packages(setdiff(packages, rownames(installed.packages())), repos='http://cran.us.r-project.org',dependencies = TRUE)


devtools::install_github("majkamichal/easyPlot")
devtools::install_github("gertstulp/ggplotgui")
remotes::install_github("giocomai/ganttrify")
remotes::install_github("feddelegrand7/ddplot")
devtools::install_github("alastairrushworth/inspectdf")
remotes::install_gitlab("hrbrmstr/hrbrthemes")
```

# Data Visualisation Shortcuts (By Rohit Satyam)
### A. Daily purpose Graphs using Online services
In this section, we will discuss about some online servers given below and understand different chart types and decision on which we should use on which kind of data. We will also discuss about the Rstudio, its features and plugins at the end.

- Venn Diagrams using [JVenn](https://jvenn.toulouse.inra.fr/app/index.html) or [venny](https://www.biotools.fr/misc/venny) or [interactivenn](https://www.interactivenn.net/index.html) or [Venn](https://bioinformatics.psb.ugent.be/webtools/Venn/) or [others](https://bioinfogp.cnb.csic.es/tools/venny/index2.0.2.html)
- Heatmap using [morpheus](http://www.heatmapper.ca/ or https://software.broadinstitute.org/morpheus/)
- Basic Plots usinf [SRPlot](https://www.bioinformatics.com.cn/srplot), [DataTab](https://datatab.net/statistics-calculator/charts and [RawGraphs](https://app.rawgraphs.io/) or [easyPlot](https://github.com/majkamichal/easyPlot)
- Make Sankey plots using [SankeyMatic](https://sankeymatic.com/)  
- UpSet plots using [intervene](https://intervene.shinyapps.io/intervene/) or [upsetr](https://gehlenborglab.shinyapps.io/upsetr/)
- (not included, only for my own reference) Publication-ready NN-architecture schematics.: https://alexlenail.me/NN-SVG/

### B. Daily purpose Graphs using RStudio
We will then discuss some easy to use R package that have been build upon ggplot2 package to make visualization life hassel free. Often the combinations of 2 or more of these packages are used by us to make plots for your paper. So I have chose these easy ones.

- GGPlot GUI:  https://github.com/gertstulp/ggplotgui
- easyPlot: https://github.com/majkamichal/easyPlot
- gantt Charts: https://github.com/giocomai/ganttrify
- ggpubr: https://rpkgs.datanovia.com/ggpubr/index.html 
- Ddplot: https://feddelegrand7.github.io/ddplot/articles/Start.html 
- ggvenn: https://cran.r-project.org/web/packages/ggvenn/readme/README.html and ggVennDiagram: https://cloud.r-project.org/web/packages/ggVennDiagram/readme/README.html
- grafify: https://grafify-vignettes.netlify.app/two_vars 
- esquisse: https://dreamrs.github.io/esquisse/ 
- ggeasy: https://jonocarroll.github.io/ggeasy/
- Hrbrthemes: https://github.com/hrbrmstr/hrbrthemes
- ggtree (Brief introduction): https://bioconductor.org/packages/release/bioc/vignettes/ggtree/inst/doc/ggtree.html
- Cowplot and ggsave: to save high quality images: https://cran.r-project.org/web/packages/cowplot/vignettes/introduction.html
- S4Vector merge function to merge dataframe in R: https://bioconductor.org/packages/release/bioc/vignettes/S4Vectors/inst/doc/S4VectorsOverview.html
- inspectdf: https://alastairrushworth.com/inspectdf/

We will also discuss briefly about markdown and Rmarkdown format.

### C. Creating Scientific Diagrams using Bioicons:
Here we will discuss the resources you can use to make scientific diagrams when you are deprieved of platforms such as Biorender. This will be a theoretical presentation on the following sources. With few examples, we will show you hot to perform SVG file manipulation as well and different kind of image formats you should use.

- Repository of Scientific Illustrations: https://scidraw.io/
- The Noun Project: https://thenounproject.com/
- Bioicons: https://bioicons.com/ 
- Freehand drawing using AutoDraw: https://www.autodraw.com/
- BioArt by NIH: https://bioart.niaid.nih.gov/
- PhyloPic: https://www.phylopic.org/ 
- Resource: https://r-graph-gallery.com/best-dataviz-packages.html
- Reactome Icon library: https://reactome.org/icon-lib 


### D. Choice of Colors
Finally we will cover about how to choose proper color palette for visualization in R or using online server and A chrome extension ColorPic Eyedropper whose link is given below.
- ggsci: R package to use Journal specific color palette: https://cran.r-project.org/web/packages/ggsci/vignettes/ggsci.html
- Color palette by Adobe: https://color.adobe.com/
- Scientific Journal specific color palette: https://cran.r-project.org/web/packages/ggsci/vignettes/ggsci.html
- Using ColorPick Eyedropper: https://chromewebstore.google.com/detail/colorpick-eyedropper/ohcpnigalekghcmgcdcenkpelffpdolg?hl=en&pli=1

### Brownie points
Data visualization conferences and classes
VIZBI: https://vizbi.org/About
MasterClass: https://visualisingdata.com/
https://ccsb.scripps.edu/cellpaint/
https://github.com/poncest/SWDchallenge

# Plot Manipulation in Adobe Illustrator (By Amit K Subudhi)

