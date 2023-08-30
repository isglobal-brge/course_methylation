# EWAS report
- study: Illumina methylation data
- author: Analyst
- date: 30 agosto, 2023

## Parameters


```
## $sig.threshold
## [1] 0.000386
## 
## $max.plots
## [1] 1
## 
## $model
## [1] "sva"
## 
## $qq.inflation.method
## [1] "median"
## 
## $practical.threshold
##   cg21566642 
## 8.297569e-26 
## 
## $winsorize.pct
## [1] 0.05
## 
## $outlier.iqr.factor
## [1] NA
## 
## $rlm
## [1] TRUE
## 
## $most.variable
## [1] 50000
## 
## $random.seed
## [1] 20161123
## 
## $sample.size
## [1] 188
```

## Sample characteristics

For continuous or ordinal variables, the "mean" column provides the mean
and the "var" column the standard deviation of the variable.
For categorical variables, the "mean" column provides the number
of samples with the given "value" and the
"var" column the percentage of samples with the given "value".


|variable             |value   |mean       |var        |
|:--------------------|:-------|:----------|:----------|
|variable of interest |never   |99         |52.7       |
|variable of interest |current |89         |47.3       |
|Age                  |        |52.73936   |11.63027   |
|Sex                  |F       |144        |76.6       |
|Sex                  |M       |44         |23.4       |
|Bcell                |        |0.06601765 |0.02948774 |
|CD4T                 |        |0.188321   |0.06010949 |
|CD8T                 |        |0.1090449  |0.04596973 |
|Mono                 |        |0.09398571 |0.02091805 |
|Neu                  |        |0.5042772  |0.0978032  |
|NK                   |        |0.08488758 |0.03298624 |

## Covariate associations




### Covariate Age


statistics

cases






![plot of chunk unnamed-chunk-21](figure/unnamed-chunk-21-1.png)


### Covariate Sex


statistics

frequencies

enrichment p-values






![plot of chunk unnamed-chunk-24](figure/unnamed-chunk-24-1.png)


### Covariate Bcell


statistics

cases






![plot of chunk unnamed-chunk-27](figure/unnamed-chunk-27-1.png)


### Covariate CD4T


statistics

cases






![plot of chunk unnamed-chunk-30](figure/unnamed-chunk-30-1.png)


### Covariate CD8T


statistics

cases






![plot of chunk unnamed-chunk-33](figure/unnamed-chunk-33-1.png)


### Covariate Mono


statistics

cases






![plot of chunk unnamed-chunk-36](figure/unnamed-chunk-36-1.png)


### Covariate Neu


statistics

cases






![plot of chunk unnamed-chunk-39](figure/unnamed-chunk-39-1.png)


### Covariate NK


statistics

cases






![plot of chunk unnamed-chunk-42](figure/unnamed-chunk-42-1.png)

## QQ plots






![plot of chunk unnamed-chunk-44](figure/unnamed-chunk-44-1.png)






![plot of chunk unnamed-chunk-46](figure/unnamed-chunk-46-1.png)






![plot of chunk unnamed-chunk-48](figure/unnamed-chunk-48-1.png)

## Manhattan plots






![plot of chunk unnamed-chunk-50](figure/unnamed-chunk-50-1.png)






![plot of chunk unnamed-chunk-52](figure/unnamed-chunk-52-1.png)






![plot of chunk unnamed-chunk-54](figure/unnamed-chunk-54-1.png)

## Significant CpG sites

There were 1365
CpG sites with association p-values < 3.86 &times; 10<sup>-4</sup>.
These are listed in the file [associations.csv](associations.csv).



The following table shows overlaps between
associations under different sets of covariates:

|             | p.value.none| p.value.all| p.value.sva|
|:------------|------------:|-----------:|-----------:|
|p.value.none |          661|         367|         114|
|p.value.all  |          367|         931|         135|
|p.value.sva  |          114|         135|         289|



Below are the 1
CpG sites with association p-values < 8.2975685 &times; 10<sup>-26</sup>
in the sva regression model.


|           |chromosome | position| p.value.none| p.value.all| p.value.sva| coefficient.none| coefficient.all| coefficient.sva|
|:----------|:----------|--------:|------------:|-----------:|-----------:|----------------:|---------------:|---------------:|
|cg05575921 |chr5       |   373378|            0|           0|           0|       -0.2458808|      -0.2451238|      -0.1572324|

Plots of these sites follow, one for each covariate set.
"p[lm]" denotes the p-value obtained using a linear model
and "p[beta]" the p-value obtained using beta regression.




### CpG site cg05575921





![plot of chunk unnamed-chunk-55](figure/unnamed-chunk-55-1.png)


![plot of chunk unnamed-chunk-55](figure/unnamed-chunk-55-2.png)




![plot of chunk unnamed-chunk-56](figure/unnamed-chunk-56-1.png)

## Selected CpG sites

Number of CpG sites selected: 1.


|           |chromosome | position| p.value.none| p.value.all| p.value.sva| coefficient.none| coefficient.all| coefficient.sva|
|:----------|:----------|--------:|------------:|-----------:|-----------:|----------------:|---------------:|---------------:|
|cg05575921 |chr5       |   373378|            0|           0|           0|       -0.2458808|      -0.2451238|      -0.1572324|




### CpG site cg05575921





![plot of chunk unnamed-chunk-58](figure/unnamed-chunk-58-1.png)


![plot of chunk unnamed-chunk-58](figure/unnamed-chunk-58-2.png)




![plot of chunk unnamed-chunk-59](figure/unnamed-chunk-59-1.png)

## R session information


```
## R version 4.1.3 (2022-03-10)
## Platform: x86_64-w64-mingw32/x64 (64-bit)
## Running under: Windows 10 x64 (build 19045)
## 
## Matrix products: default
## 
## locale:
## [1] LC_COLLATE=Spanish_Spain.1252  LC_CTYPE=Spanish_Spain.1252    LC_MONETARY=Spanish_Spain.1252 LC_NUMERIC=C                  
## [5] LC_TIME=Spanish_Spain.1252    
## 
## attached base packages:
## [1] stats4    parallel  stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
##  [1] karyoploteR_1.20.3    regioneR_1.26.1       GenomicRanges_1.46.1  GenomeInfoDb_1.30.1   IRanges_2.28.0       
##  [6] S4Vectors_0.32.4      ggrepel_0.9.2         qqman_0.1.8           meffil_1.3.6          preprocessCore_1.56.0
## [11] SmartSVA_0.1.3        RSpectra_0.16-1       isva_1.9              JADE_2.0-3            qvalue_2.26.0        
## [16] gdsfmt_1.30.0         statmod_1.5.0         quadprog_1.5-8        DNAcopy_1.68.0        fastICA_1.2-3        
## [21] lme4_1.1-31           Matrix_1.5-1          multcomp_1.4-20       TH.data_1.1-1         survival_3.2-13      
## [26] mvtnorm_1.1-3         matrixStats_0.63.0    markdown_1.4          gridExtra_2.3         Cairo_1.6-0          
## [31] knitr_1.43            reshape2_1.4.4        plyr_1.8.8            ggplot2_3.4.2         sva_3.42.0           
## [36] BiocParallel_1.28.3   genefilter_1.76.0     mgcv_1.8-39           nlme_3.1-155          limma_3.50.3         
## [41] sandwich_3.0-2        lmtest_0.9-40         zoo_1.8-11            MASS_7.3-55           illuminaio_0.36.0    
## [46] Biobase_2.54.0        BiocGenerics_0.40.0  
## 
## loaded via a namespace (and not attached):
##   [1] backports_1.4.1             Hmisc_5.0-1                 BiocFileCache_2.2.1         lazyeval_0.2.2             
##   [5] splines_4.1.3               digest_0.6.29               ensembldb_2.18.4            htmltools_0.5.4            
##   [9] fansi_1.0.3                 checkmate_2.1.0             magrittr_2.0.3              memoise_2.0.1              
##  [13] BSgenome_1.62.0             cluster_2.1.2               Biostrings_2.62.0           annotate_1.72.0            
##  [17] askpass_1.1                 prettyunits_1.1.1           colorspace_2.1-0            blob_1.2.4                 
##  [21] rappdirs_0.3.3              xfun_0.39                   dplyr_1.1.2                 crayon_1.5.2               
##  [25] RCurl_1.98-1.9              VariantAnnotation_1.40.0    glue_1.6.2                  gtable_0.3.3               
##  [29] zlibbioc_1.40.0             XVector_0.34.0              DelayedArray_0.20.0         scales_1.2.1               
##  [33] bezier_1.1.2                DBI_1.1.3                   edgeR_3.36.0                Rcpp_1.0.9                 
##  [37] htmlTable_2.4.1             xtable_1.8-4                progress_1.2.2              clue_0.3-64                
##  [41] foreign_0.8-82              bit_4.0.5                   Formula_1.2-5               htmlwidgets_1.6.0          
##  [45] httr_1.4.6                  RColorBrewer_1.1-3          calibrate_1.7.7             farver_2.1.1               
##  [49] pkgconfig_2.0.3             XML_3.99-0.13               nnet_7.3-17                 dbplyr_2.3.2               
##  [53] locfit_1.5-9.6              utf8_1.2.2                  labeling_0.4.2              tidyselect_1.2.0           
##  [57] rlang_1.1.1                 AnnotationDbi_1.56.2        munsell_0.5.0               tools_4.1.3                
##  [61] cachem_1.0.6                cli_3.4.1                   generics_0.1.3              RSQLite_2.2.18             
##  [65] evaluate_0.21               stringr_1.5.0               fastmap_1.1.0               yaml_2.3.7                 
##  [69] bit64_4.0.5                 AnnotationFilter_1.18.0     KEGGREST_1.34.0             xml2_1.3.3                 
##  [73] biomaRt_2.50.3              compiler_4.1.3              rstudioapi_0.14             filelock_1.0.2             
##  [77] curl_4.3.3                  png_0.1-8                   tibble_3.2.1                stringi_1.7.6              
##  [81] highr_0.10                  GenomicFeatures_1.46.5      lattice_0.20-45             ProtGenerics_1.26.0        
##  [85] nloptr_2.0.3                vctrs_0.6.3                 pillar_1.9.0                lifecycle_1.0.3            
##  [89] BiocManager_1.30.19         data.table_1.14.8           bitops_1.0-7                rtracklayer_1.54.0         
##  [93] R6_2.5.1                    BiocIO_1.4.0                codetools_0.2-18            dichromat_2.0-0.1          
##  [97] boot_1.3-28                 SummarizedExperiment_1.24.0 openssl_2.0.6               rjson_0.2.21               
## [101] withr_2.5.0                 GenomicAlignments_1.30.0    Rsamtools_2.10.0            GenomeInfoDbData_1.2.7     
## [105] hms_1.1.3                   rpart_4.1.16                grid_4.1.3                  bamsignals_1.26.0          
## [109] base64_2.0.1                minqa_1.2.5                 rmarkdown_2.23              MatrixGenerics_1.6.0       
## [113] biovizBase_1.42.0           base64enc_0.1-3             restfulr_0.0.15
```
