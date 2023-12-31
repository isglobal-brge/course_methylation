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


|var1     |var2 |         F|   p-value|          R|   p-value|
|:--------|:----|---------:|---------:|----------:|---------:|
|variable |Age  | 0.0001012| 0.9919836| -0.0271044| 0.7119591|

cases


|variable |     mean|      var|  n|     t.stat|   p.value|
|:--------|--------:|--------:|--:|----------:|---------:|
|never    | 52.74747| 156.7621| 99|  0.0101488| 0.9919135|
|current  | 52.73034| 112.8583| 89| -0.0101488| 0.9919135|






![plot of chunk unnamed-chunk-21](figure/unnamed-chunk-21-1.png)


### Covariate Sex


statistics


|var1     |var2 |        R|   p-value|
|:--------|:----|--------:|---------:|
|variable |Sex  | 0.054606| 0.4567064|

frequencies


|        |  F|  M|
|:-------|--:|--:|
|never   | 78| 21|
|current | 66| 23|

enrichment p-values


|        |         F|         M|
|:-------|---------:|---------:|
|never   | 0.2820187| 0.8215467|
|current | 0.8215467| 0.2820187|






![plot of chunk unnamed-chunk-24](figure/unnamed-chunk-24-1.png)


### Covariate Bcell


statistics


|var1     |var2  |         F|   p-value|          R|   p-value|
|:--------|:-----|---------:|---------:|----------:|---------:|
|variable |Bcell | 0.2366181| 0.6272321| -0.1165057| 0.1113357|

cases


|variable |      mean|       var|  n|     t.stat|   p.value|
|:--------|---------:|---------:|--:|----------:|---------:|
|never    | 0.0670116| 0.0004847| 99|  0.4746479| 0.6357655|
|current  | 0.0649121| 0.0013056| 89| -0.4746479| 0.6357655|






![plot of chunk unnamed-chunk-27](figure/unnamed-chunk-27-1.png)


### Covariate CD4T


statistics


|var1     |var2 |        F|   p-value|         R|   p-value|
|:--------|:----|--------:|---------:|---------:|---------:|
|variable |CD4T | 1.708011| 0.1928572| 0.0797971| 0.2763471|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.1828989| 0.0033585| 99| -1.301991| 0.1945799|
|current  | 0.1943523| 0.0038679| 89|  1.301991| 0.1945799|






![plot of chunk unnamed-chunk-30](figure/unnamed-chunk-30-1.png)


### Covariate CD8T


statistics


|var1     |var2 |        F|   p-value|          R|   p-value|
|:--------|:----|--------:|---------:|----------:|---------:|
|variable |CD8T | 3.076023| 0.0811016| -0.1161131| 0.1125543|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.1145895| 0.0023595| 99|  1.766782| 0.0789065|
|current  | 0.1028774| 0.0017899| 89| -1.766782| 0.0789065|






![plot of chunk unnamed-chunk-33](figure/unnamed-chunk-33-1.png)


### Covariate Mono


statistics


|var1     |var2 |        F|   p-value|          R|   p-value|
|:--------|:----|--------:|---------:|----------:|---------:|
|variable |Mono | 6.977278| 0.0089576| -0.1655813| 0.0231534|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.0977469| 0.0004783| 99|  2.660786| 0.0084779|
|current  | 0.0898019| 0.0003635| 89| -2.660786| 0.0084779|






![plot of chunk unnamed-chunk-36](figure/unnamed-chunk-36-1.png)


### Covariate Neu


statistics


|var1     |var2 |        F|   p-value|         R|   p-value|
|:--------|:----|--------:|---------:|---------:|---------:|
|variable |Neu  | 1.790709| 0.1824734| 0.1221984| 0.0948021|

cases


|variable |      mean|       var|  n|    t.stat|  p.value|
|:--------|---------:|---------:|--:|---------:|--------:|
|never    | 0.4952459| 0.0088404| 99| -1.332769| 0.184292|
|current  | 0.5143232| 0.0102878| 89|  1.332769| 0.184292|






![plot of chunk unnamed-chunk-39](figure/unnamed-chunk-39-1.png)


### Covariate NK


statistics


|var1     |var2 |        F|   p-value|          R|   p-value|
|:--------|:----|--------:|---------:|----------:|---------:|
|variable |NK   | 7.140693| 0.0082045| -0.1695074| 0.0200441|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.0908853| 0.0013115| 99|  2.709977| 0.0073742|
|current  | 0.0782160| 0.0007662| 89| -2.709977| 0.0073742|






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
## [1] LC_COLLATE=Spanish_Spain.1252  LC_CTYPE=Spanish_Spain.1252    LC_MONETARY=Spanish_Spain.1252 LC_NUMERIC=C                   LC_TIME=Spanish_Spain.1252    
## 
## attached base packages:
## [1] stats4    parallel  stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
##  [1] karyoploteR_1.20.3    regioneR_1.26.1       GenomicRanges_1.46.1  GenomeInfoDb_1.30.1   IRanges_2.28.0        S4Vectors_0.32.4      ggrepel_0.9.2        
##  [8] qqman_0.1.8           meffil_1.3.6          preprocessCore_1.56.0 SmartSVA_0.1.3        RSpectra_0.16-1       isva_1.9              JADE_2.0-3           
## [15] qvalue_2.26.0         gdsfmt_1.30.0         statmod_1.5.0         quadprog_1.5-8        DNAcopy_1.68.0        fastICA_1.2-3         lme4_1.1-31          
## [22] Matrix_1.5-1          multcomp_1.4-20       TH.data_1.1-1         survival_3.2-13       mvtnorm_1.1-3         matrixStats_0.63.0    markdown_1.4         
## [29] gridExtra_2.3         Cairo_1.6-0           knitr_1.43            reshape2_1.4.4        plyr_1.8.8            ggplot2_3.4.2         sva_3.42.0           
## [36] BiocParallel_1.28.3   genefilter_1.76.0     mgcv_1.8-39           nlme_3.1-155          limma_3.50.3          sandwich_3.0-2        lmtest_0.9-40        
## [43] zoo_1.8-11            MASS_7.3-55           illuminaio_0.36.0     Biobase_2.54.0        BiocGenerics_0.40.0  
## 
## loaded via a namespace (and not attached):
##   [1] backports_1.4.1             Hmisc_5.0-1                 BiocFileCache_2.2.1         lazyeval_0.2.2              splines_4.1.3              
##   [6] digest_0.6.29               ensembldb_2.18.4            htmltools_0.5.4             fansi_1.0.3                 checkmate_2.1.0            
##  [11] magrittr_2.0.3              memoise_2.0.1               BSgenome_1.62.0             cluster_2.1.2               Biostrings_2.62.0          
##  [16] annotate_1.72.0             askpass_1.1                 prettyunits_1.1.1           colorspace_2.1-0            blob_1.2.4                 
##  [21] rappdirs_0.3.3              xfun_0.39                   dplyr_1.1.2                 crayon_1.5.2                RCurl_1.98-1.9             
##  [26] VariantAnnotation_1.40.0    glue_1.6.2                  gtable_0.3.3                zlibbioc_1.40.0             XVector_0.34.0             
##  [31] DelayedArray_0.20.0         scales_1.2.1                bezier_1.1.2                DBI_1.1.3                   edgeR_3.36.0               
##  [36] Rcpp_1.0.9                  htmlTable_2.4.1             xtable_1.8-4                progress_1.2.2              clue_0.3-64                
##  [41] foreign_0.8-82              bit_4.0.5                   Formula_1.2-5               htmlwidgets_1.6.0           httr_1.4.6                 
##  [46] RColorBrewer_1.1-3          calibrate_1.7.7             farver_2.1.1                pkgconfig_2.0.3             XML_3.99-0.13              
##  [51] nnet_7.3-17                 dbplyr_2.3.2                locfit_1.5-9.6              utf8_1.2.2                  labeling_0.4.2             
##  [56] tidyselect_1.2.0            rlang_1.1.1                 AnnotationDbi_1.56.2        munsell_0.5.0               tools_4.1.3                
##  [61] cachem_1.0.6                cli_3.4.1                   generics_0.1.3              RSQLite_2.2.18              evaluate_0.21              
##  [66] stringr_1.5.0               fastmap_1.1.0               yaml_2.3.7                  bit64_4.0.5                 AnnotationFilter_1.18.0    
##  [71] KEGGREST_1.34.0             xml2_1.3.3                  biomaRt_2.50.3              compiler_4.1.3              rstudioapi_0.14            
##  [76] filelock_1.0.2              curl_4.3.3                  png_0.1-8                   tibble_3.2.1                stringi_1.7.6              
##  [81] highr_0.10                  GenomicFeatures_1.46.5      lattice_0.20-45             ProtGenerics_1.26.0         nloptr_2.0.3               
##  [86] vctrs_0.6.3                 pillar_1.9.0                lifecycle_1.0.3             BiocManager_1.30.19         data.table_1.14.8          
##  [91] bitops_1.0-7                rtracklayer_1.54.0          R6_2.5.1                    BiocIO_1.4.0                codetools_0.2-18           
##  [96] dichromat_2.0-0.1           boot_1.3-28                 SummarizedExperiment_1.24.0 openssl_2.0.6               rjson_0.2.21               
## [101] withr_2.5.0                 GenomicAlignments_1.30.0    Rsamtools_2.10.0            GenomeInfoDbData_1.2.7      hms_1.1.3                  
## [106] rpart_4.1.16                grid_4.1.3                  bamsignals_1.26.0           base64_2.0.1                minqa_1.2.5                
## [111] rmarkdown_2.23              MatrixGenerics_1.6.0        biovizBase_1.42.0           base64enc_0.1-3             restfulr_0.0.15
```
