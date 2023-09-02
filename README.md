# Course on methylation data analysis from International Summer School in Global Health 2023

## Aim
The aim of this course is to introduce basic concepts and guidelines to conduct epigenome-wide association studies (EWAS) using DNA
methylation data obtained from arrays. The course is a comprehensive program designed to equip participants with the knowledge and practical skills required to effectively analyze and interpret DNA methylation data using the powerful Bioconductor framework. Upon successful completion of the module, participants should be able to conduct:

1) Introduction to epigenetics ([slides introduction](./Slides/ISG_summer_school_EWAS1.pdf), [slides application: transitioning African populations](./Slides/ISGlobal_2023_FPC_Updated.pdf))
2) Pre-processing of DNA methylation data ([slides](./Slides/ISG_summer_school_EWAS2.pdf))
3) Epigenome-wide association studies (EWAS) ([slides](./Slides/ISG_summer_school_EWAS3.pdf))
4) Meta-analysis of EWAS from different studies ([slides](./Slides/ISG_summer_school_EWAS4.pdf))
5) Annotation and functional interpretation of findings ([slides](./Slides/ISG_summer_school_EWAS5.pdf))

To enhance the learning experience, the course will include practical sessions where participants will work on real-world methylation datasets, addressing key research questions and challenges in the field. Participants will receive guidance from experienced instructors who will provide hands-on demonstrations and offer personalized assistance throughout the course.

## Material 
- The data to reproduce the vignettes (input and output files) and data for practical sessions can be downloaded [here](https://mega.nz/folder/Y3EDAD6Y#pQB_HeqEfAYTg6UixU-k5A)
- The R code for practical sessions can be found [here](https://isglobal-brge.github.io/course_methylation/).

## Getting started
We have created the material using R version 4.2.1 (later can also work) - if your R version is lower, we recommend you to update it so everything works properly. We also need you to have RStudio Desktop. If you do not have R installed in your computer, the last version can be easily downloaded [here](https://cran.r-project.org/). RStudio can be downloaded [here](https://posit.co/download/rstudio-desktop/). 

The required package are (you can type this code in your console to install them):

``` 
BiocManager::install(c("GenomicRanges", "GEOquery", "brgedata", "meffil", "Biobase",
                       "ggplot2", "ggrepel", "karyoploteR", "qqman", "metafor", "reshape",
                       "plyr", "IlluminaHumanMethylation450kanno.ilmn12.hg19", "clusterProfiler",
                       "org.Hs.eg.db", "ReactomePA", "enrichplot"))
```
  
If the installation of the package `meffil` throws errors, try this alternative command:

``` 
install.packages("devtools")
devtools::install_github("perishky/meffil")
```
