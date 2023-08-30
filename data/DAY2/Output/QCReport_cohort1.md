# QC report
- study: Illumina methylation data
- author: Analyst
- date: 30 agosto, 2023

## Parameters used for QC


```
## $colour.code
## NULL
## 
## $control.categories
## NULL
## 
## $sex.outlier.sd
## [1] 3
## 
## $meth.unmeth.outlier.sd
## [1] 3
## 
## $control.means.outlier.sd
## [1] 5
## 
## $detectionp.samples.threshold
## [1] 0.03
## 
## $beadnum.samples.threshold
## [1] 0.05
## 
## $detectionp.cpgs.threshold
## [1] 0.05
## 
## $beadnum.cpgs.threshold
## [1] 0.05
## 
## $snp.concordance.threshold
## [1] 0.9
## 
## $sample.genotype.concordance.threshold
## [1] 0.9
## 
## $detection.threshold
## [1] 0.01
## 
## $bead.threshold
## [1] 3
## 
## $sex.cutoff
## [1] -2
```
## Number of samples

There are 298 samples analysed.

## Sex mismatches

To separate females and males, we use the difference of total median intensity for Y chromosome probes and X chromosome probes. This will give two distinct clusters of intensities. Females will be clustered on the left and males on the right. 
There are 6 sex detection outliers, and 0 sex detection mismatches.

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> sample.name </th>
   <th style="text-align:left;"> predicted.sex </th>
   <th style="text-align:left;"> declared.sex </th>
   <th style="text-align:right;"> xy.diff </th>
   <th style="text-align:left;"> status </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> GSM1051838 </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:right;"> -5.1482735 </td>
   <td style="text-align:left;"> outlier </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GSM1051850 </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:right;"> -5.1034396 </td>
   <td style="text-align:left;"> outlier </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GSM1051844 </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:right;"> -5.0754374 </td>
   <td style="text-align:left;"> outlier </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GSM1051832 </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:right;"> -5.0633302 </td>
   <td style="text-align:left;"> outlier </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GSM1052210 </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:left;"> F </td>
   <td style="text-align:right;"> -3.9973089 </td>
   <td style="text-align:left;"> outlier </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GSM1051906 </td>
   <td style="text-align:left;"> M </td>
   <td style="text-align:left;"> M </td>
   <td style="text-align:right;"> -0.1504136 </td>
   <td style="text-align:left;"> outlier </td>
  </tr>
</tbody>
</table>

This is a plot of the difference between median 
chromosome Y and chromosome X probe intensities ("XY diff").
Cutoff for sex detection was
XY diff = -2. Mismatched samples are shown in red. The dashed lines represent 3 SD from  the mean xy difference. Samples that fall in this interval are denoted as outliers.



![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3-1.png)


## Methylated vs unmethylated
To explore the quality of the samples, it is useful to plot the median methylation intensity against the median unmethylation intensity with the option to color outliers by group.
There are 3 outliers from the meth vs unmeth comparison.
Outliers are samples whose predicted median methylated signal is
more than 3 standard deviations
from the expected (regression line).

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> sample.name </th>
   <th style="text-align:right;"> methylated </th>
   <th style="text-align:right;"> unmethylated </th>
   <th style="text-align:right;"> resids </th>
   <th style="text-align:right;"> methylated.lm </th>
   <th style="text-align:right;"> upper.lm </th>
   <th style="text-align:right;"> lower.lm </th>
   <th style="text-align:left;"> outliers </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> GSM1051809 </td>
   <td style="text-align:right;"> 2924.178 </td>
   <td style="text-align:right;"> 3665.604 </td>
   <td style="text-align:right;"> -741.0952 </td>
   <td style="text-align:right;"> 3665.273 </td>
   <td style="text-align:right;"> 4260.381 </td>
   <td style="text-align:right;"> 3070.165 </td>
   <td style="text-align:left;"> TRUE </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GSM1052037 </td>
   <td style="text-align:right;"> 3162.397 </td>
   <td style="text-align:right;"> 4289.957 </td>
   <td style="text-align:right;"> -711.8287 </td>
   <td style="text-align:right;"> 3874.225 </td>
   <td style="text-align:right;"> 4469.333 </td>
   <td style="text-align:right;"> 3279.117 </td>
   <td style="text-align:left;"> TRUE </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GSM1052049 </td>
   <td style="text-align:right;"> 2947.460 </td>
   <td style="text-align:right;"> 3734.098 </td>
   <td style="text-align:right;"> -740.7364 </td>
   <td style="text-align:right;"> 3688.196 </td>
   <td style="text-align:right;"> 4283.304 </td>
   <td style="text-align:right;"> 3093.088 </td>
   <td style="text-align:left;"> TRUE </td>
  </tr>
</tbody>
</table>

This is a plot of the methylation signals vs unmethylated signals



![plot of chunk unnamed-chunk-5](figure/unnamed-chunk-5-1.png)


## Control probe means

There were 1 outliers detected based on deviations from mean values for control probes. The 450k array contains control probe which can be used to evaluate the quality of specific sample processing steps (staining, extension,target removal, hybridization, bisulfate conversion etc.).  Control probes are grouped in 42 categories of control type. For each category a plot has been generated which shows the control means for each sample. Outliers are deviations from the mean. Some of the control probe categories have a very small number of probes. See Page 222 in this doc: https://support.illumina.com/content/dam/illumina-support/documents/documentation/chemistry_documentation/infinium_assays/infinium_hd_methylation/infinium-hd-methylation-guide-15019519-01.pdf. The most important control probes are the bisulfate1 and bisulfate2 control probes. 

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> sample.name </th>
   <th style="text-align:left;"> colour.code </th>
   <th style="text-align:right;"> id </th>
   <th style="text-align:left;"> variable </th>
   <th style="text-align:right;"> value </th>
   <th style="text-align:left;"> outliers </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> GSM1052210 </td>
   <td style="text-align:left;"> 1 </td>
   <td style="text-align:right;"> 295 </td>
   <td style="text-align:left;"> oob.G.99% </td>
   <td style="text-align:right;"> 7628.54 </td>
   <td style="text-align:left;"> TRUE </td>
  </tr>
</tbody>
</table>

The distribution of sample control means are plotted here:



![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-7-1.png)


## Sample detection p-values

To further explore the quality of each sample the proportion of probes that didn't pass the detection pvalue has been calculated.
There were 1 samples
with a high proportion of undetected probes
(proportion of probes with
detection p-value > 0.01
is > 0.03).

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> sample.name </th>
   <th style="text-align:right;"> prop.badprobes </th>
   <th style="text-align:right;"> colour.code </th>
   <th style="text-align:right;"> id </th>
   <th style="text-align:left;"> outliers </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> GSM1052210 </td>
   <td style="text-align:right;"> 0.0465568 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 295 </td>
   <td style="text-align:left;"> TRUE </td>
  </tr>
</tbody>
</table>

Distribution:



![plot of chunk unnamed-chunk-9](figure/unnamed-chunk-9-1.png)


## Sample bead numbers


To further assess the quality of each sample the proportion of probes that didn't pass the number of beads threshold has been calculated.
There were 0 samples
with a high proportion of probes with low bead number
(proportion of probes with
bead number < 3
is > 0.05).



Distribution:



![plot of chunk unnamed-chunk-11](figure/unnamed-chunk-11-1.png)


## CpG detection p-values

To explore the quality of the probes, the proportion of samples that didn't pass the detection pvalue threshold has been calculated.
There were 1408
probes with only background signal in a high proportion of samples
(proportion of samples with detection p-value > 0.01
is > 0.05).
Manhattan plot shows the proportion of samples.



![plot of chunk unnamed-chunk-12](figure/unnamed-chunk-12-1.png)

## Low number of beads per CpG

To further explore the quality of the probes, the proportion of samples that didn't pass the number of beads threshold has been calculated.
There were 571 CpGs
with low bead numbers in a high proportion of samples
(proportion of samples with bead number < 3
is > 0.05).
Manhattan plot of proportion of samples.



![plot of chunk unnamed-chunk-13](figure/unnamed-chunk-13-1.png)

## Cellular composition estimates




Cell counts were estimated using the blood idoloptimized cell type methylation profile references.

Plot compares methylation levels of CpG sites used to estimate cellular composition
for each sample and reference methylation profile.
Methylation levels of samples should generally overlap with reference methylation levels
otherwise estimation will have simply selected the cell type reference
with the nearest mean methylation level.



![plot of chunk unnamed-chunk-20](figure/unnamed-chunk-20-1.png)

Boxplot shows the distributions of estimated cellular composition for each reference cell type across all samples.



![plot of chunk unnamed-chunk-21](figure/unnamed-chunk-21-1.png)

## SNP probe beta values

The array contains 65 snp probes which can be used to identify sample swaps by comparing these genotypes to genotype calls from a genotype array. First you could check the quality of these snp probes before using them for sample quality.
Distributions of SNP probe beta values are used to determine the quality of the snp probe and should show 3 peaks, one for each genotype probability.


![plot of chunk unnamed-chunk-16](figure/unnamed-chunk-16-1.png)

## Genotype concordance




This section omitted.

## R session information


```
## R version 4.2.1 (2022-06-23 ucrt)
## Platform: x86_64-w64-mingw32/x64 (64-bit)
## Running under: Windows 10 x64 (build 22621)
## 
## Matrix products: default
## 
## locale:
## [1] LC_COLLATE=Spanish_Spain.utf8  LC_CTYPE=Spanish_Spain.utf8   
## [3] LC_MONETARY=Spanish_Spain.utf8 LC_NUMERIC=C                  
## [5] LC_TIME=Spanish_Spain.utf8    
## 
## attached base packages:
## [1] parallel  stats4    stats     graphics  grDevices utils     datasets  methods  
## [9] base     
## 
## other attached packages:
##  [1] reshape_0.8.9               metafor_4.2-0               numDeriv_2016.8-1.1        
##  [4] metadat_1.2-0               data.table_1.14.2           minfi_1.42.0               
##  [7] bumphunter_1.38.0           locfit_1.5-9.6              iterators_1.0.14           
## [10] foreach_1.5.2               Biostrings_2.64.1           XVector_0.36.0             
## [13] SummarizedExperiment_1.26.1 MatrixGenerics_1.8.1        brgedata_1.18.0            
## [16] GEOquery_2.64.2             forcats_0.5.1               stringr_1.5.0              
## [19] purrr_0.3.4                 readr_2.1.2                 tibble_3.2.1               
## [22] tidyverse_1.3.1             meta_6.2-1                  kableExtra_1.3.4           
## [25] dplyr_1.1.2                 tidyr_1.2.0                 karyoploteR_1.22.0         
## [28] regioneR_1.28.0             ggrepel_0.9.3               qqman_0.1.8                
## [31] Biobase_2.56.0              meffil_1.3.6                preprocessCore_1.58.0      
## [34] SmartSVA_0.1.3              RSpectra_0.16-1             isva_1.9                   
## [37] JADE_2.0-3                  qvalue_2.28.0               gdsfmt_1.32.0              
## [40] statmod_1.5.0               quadprog_1.5-8              DNAcopy_1.70.0             
## [43] fastICA_1.2-3               lme4_1.1-30                 Matrix_1.5-1               
## [46] multcomp_1.4-20             TH.data_1.1-1               survival_3.3-1             
## [49] mvtnorm_1.1-3               matrixStats_0.62.0          markdown_1.7               
## [52] gridExtra_2.3               Cairo_1.6-0                 knitr_1.43                 
## [55] reshape2_1.4.4              plyr_1.8.7                  ggplot2_3.4.2              
## [58] sva_3.44.0                  BiocParallel_1.30.3         genefilter_1.78.0          
## [61] mgcv_1.8-40                 nlme_3.1-157                limma_3.52.4               
## [64] sandwich_3.0-2              lmtest_0.9-40               zoo_1.8-11                 
## [67] MASS_7.3-57                 illuminaio_0.38.0           bookdown_0.34              
## [70] GenomicRanges_1.48.0        GenomeInfoDb_1.32.4         IRanges_2.30.1             
## [73] S4Vectors_0.34.0            BiocGenerics_0.42.0        
## 
## loaded via a namespace (and not attached):
##   [1] Hmisc_5.1-0               svglite_2.1.1             ps_1.7.1                 
##   [4] Rsamtools_2.12.0          crayon_1.5.2              rhdf5filters_1.8.0       
##   [7] backports_1.4.1           reprex_2.0.2              GOSemSim_2.22.0          
##  [10] rlang_1.1.1               readxl_1.4.0              nloptr_2.0.3             
##  [13] callr_3.7.3               filelock_1.0.2            rjson_0.2.21             
##  [16] bit64_4.0.5               glue_1.6.2                rngtools_1.5.2           
##  [19] processx_3.7.0            AnnotationDbi_1.58.0      DOSE_3.22.1              
##  [22] haven_2.5.0               tidyselect_1.2.0          usethis_2.2.1            
##  [25] XML_3.99-0.10             calibrate_1.7.7           GenomicAlignments_1.32.1 
##  [28] xtable_1.8-4              magrittr_2.0.3            evaluate_0.21            
##  [31] cli_3.6.1                 zlibbioc_1.42.0           rstudioapi_0.14          
##  [34] doRNG_1.8.6               miniUI_0.1.1.1            bslib_0.5.0              
##  [37] rpart_4.1.19              fastmatch_1.1-3           mathjaxr_1.6-0           
##  [40] ensembldb_2.20.2          treeio_1.20.2             shiny_1.7.4              
##  [43] xfun_0.39                 askpass_1.1               clue_0.3-64              
##  [46] pkgbuild_1.3.1            multtest_2.52.0           cluster_2.1.3            
##  [49] tidygraph_1.2.3           KEGGREST_1.36.3           base64_2.0.1             
##  [52] ape_5.7-1                 biovizBase_1.44.0         scrime_1.3.5             
##  [55] png_0.1-7                 withr_2.5.0               bitops_1.0-7             
##  [58] ggforce_0.4.1             cellranger_1.1.0          AnnotationFilter_1.20.0  
##  [61] pillar_1.9.0              cachem_1.0.6              GenomicFeatures_1.48.4   
##  [64] fs_1.5.2                  clusterProfiler_4.4.4     DelayedMatrixStats_1.18.2
##  [67] vctrs_0.6.3               ellipsis_0.3.2            generics_0.1.3           
##  [70] devtools_2.4.5            tools_4.2.1               foreign_0.8-84           
##  [73] tweenr_2.0.2              munsell_0.5.0             fgsea_1.22.0             
##  [76] DelayedArray_0.22.0       fastmap_1.1.0             compiler_4.2.1           
##  [79] pkgload_1.3.2             httpuv_1.6.6              rtracklayer_1.56.1       
##  [82] sessioninfo_1.2.2         beanplot_1.3.1            GenomeInfoDbData_1.2.8   
##  [85] edgeR_3.38.4              lattice_0.20-45           utf8_1.2.2               
##  [88] later_1.3.0               BiocFileCache_2.4.0       jsonlite_1.8.3           
##  [91] scales_1.2.1              tidytree_0.4.2            sparseMatrixStats_1.8.0  
##  [94] lazyeval_0.2.2            promises_1.2.0.1          checkmate_2.2.0          
##  [97] rmarkdown_2.23            nor1mix_1.3-0             webshot_0.5.5            
## [100] siggenes_1.70.0           dichromat_2.0-0.1         downloader_0.4           
## [103] BSgenome_1.64.0           igraph_1.5.0              HDF5Array_1.24.2         
## [106] yaml_2.3.5                systemfonts_1.0.4         htmltools_0.5.5          
## [109] memoise_2.0.1             VariantAnnotation_1.42.1  profvis_0.3.7            
## [112] BiocIO_1.6.0              graphlayouts_1.0.0        viridisLite_0.4.2        
## [115] digest_0.6.29             commonmark_1.9.0          mime_0.12                
## [118] rappdirs_0.3.3            RSQLite_2.2.17            yulab.utils_0.0.6        
## [121] remotes_2.4.2             urlchecker_1.0.1          blob_1.2.4               
## [124] labeling_0.4.2            splines_4.2.1             Formula_1.2-5            
## [127] Rhdf5lib_1.18.2           ProtGenerics_1.28.0       RCurl_1.98-1.7           
## [130] broom_1.0.5               hms_1.1.3                 modelr_0.1.11            
## [133] rhdf5_2.40.0              colorspace_2.0-3          base64enc_0.1-3          
## [136] BiocManager_1.30.19       aplot_0.1.10              nnet_7.3-19              
## [139] sass_0.4.6                Rcpp_1.0.9                mclust_6.0.0             
## [142] enrichplot_1.16.2         fansi_1.0.3               tzdb_0.3.0               
## [145] R6_2.5.1                  grid_4.2.1                lifecycle_1.0.3          
## [148] curl_4.3.2                minqa_1.2.4               jquerylib_0.1.4          
## [151] DO.db_2.9                 org.Hs.eg.db_3.15.0       RColorBrewer_1.1-3       
## [154] htmlwidgets_1.6.2         bamsignals_1.28.0         polyclip_1.10-4          
## [157] biomaRt_2.52.0            shadowtext_0.1.2          gridGraphics_0.5-1       
## [160] rvest_1.0.3               openssl_2.0.3             patchwork_1.1.2          
## [163] htmlTable_2.4.1           codetools_0.2-19          lubridate_1.8.0          
## [166] GO.db_3.15.0              prettyunits_1.1.1         dbplyr_2.3.2             
## [169] gtable_0.3.3              DBI_1.1.3                 highr_0.10               
## [172] ggfun_0.1.1               httr_1.4.6                stringi_1.7.6            
## [175] progress_1.2.2            farver_2.1.1              viridis_0.6.3            
## [178] annotate_1.74.0           ggtree_3.4.4              xml2_1.3.3               
## [181] bezier_1.1.2              boot_1.3-28.1             restfulr_0.0.15          
## [184] ggplotify_0.1.0           CompQuadForm_1.4.3        bit_4.0.4                
## [187] scatterpie_0.2.1          ggraph_2.1.0              pkgconfig_2.0.3          
## [190] downlit_0.4.3
```
