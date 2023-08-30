
# Normalization performance report
- study: Illumina methylation data
- author: Analyst
- date: 28 agosto, 2023

## Parameters used to test normalization


```
## $variables
## [1] "Slide"   "Sex"     "Age"     "Smoking"
## 
## $control.pcs
## [1] 1 2 3 4 5
## 
## $batch.pcs
## [1] 1 2 3 4 5
## 
## $batch.threshold
## [1] 0.01
## 
## $colours
## NULL
```

## Control probe scree plots

The variance captured by each principal component.




<img src="_main_files/figure-html/unnamed-chunk-41-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-42-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-43-1.png" width="576" style="display: block; margin: auto;" />

## Principal components of the control probes

The following plots show the first 3 principal components of the
control matrix colored by batch variables.
Batch variables with more than 10 levels are omitted.




<img src="_main_files/figure-html/unnamed-chunk-45-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-47-1.png" width="1728" style="display: block; margin: auto;" />

## Control probe associations with measured batch variables

Principal components of the control probes were regressed against batch variables.
Shown are the $-log_{10}$ p-values for these regressions.
The horizontal dotted line denotes $p = 0.05$ in log-scale.




<img src="_main_files/figure-html/unnamed-chunk-49-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-51-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-53-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-55-1.png" width="1728" style="display: block; margin: auto;" />


The following plots show regression coefficients when
each principal component is regressed against each batch variable level
along with 95% confidence intervals.
Cases significantly different from zero are coloured red
(p < 0.01, t-test).




<img src="_main_files/figure-html/unnamed-chunk-56-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-57-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-58-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-59-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-60-1.png" width="576" style="display: block; margin: auto;" />


|batch.variable |batch.value |principal.component |test   |p.value  |estimate |lower   |upper  |r2     |
|:--------------|:-----------|:-------------------|:------|:--------|:--------|:-------|:------|:------|
|Slide          |            |PC1                 |F-test |3.02e-13 |4.137    |        |       |0.4288 |
|Slide          |7800246140  |PC1                 |t-test |1.09e-03 |-5.375   |-9.033  |-1.717 |0.0359 |
|Slide          |7796814016  |PC1                 |t-test |9.08e-05 |6.098    |2.650   |9.546  |0.0512 |
|Slide          |5765205058  |PC1                 |t-test |7.62e-03 |4.978    |0.818   |9.137  |0.0241 |
|Slide          |5765205059  |PC1                 |t-test |9.73e-06 |8.164    |4.092   |12.236 |0.0649 |
|Slide          |5730192048  |PC1                 |t-test |6.36e-05 |5.948    |2.658   |9.237  |0.0534 |
|Slide          |5730053041  |PC1                 |t-test |9.29e-04 |6.157    |2.024   |10.289 |0.0369 |
|Age            |57          |PC1                 |t-test |3.35e-03 |5.465    |1.315   |9.614  |0.0291 |
|Slide          |            |PC2                 |F-test |6.52e-72 |26.578   |        |       |0.8283 |
|Slide          |7800246087  |PC2                 |t-test |6.01e-04 |-2.069   |-3.407  |-0.731 |0.0427 |
|Slide          |7800246140  |PC2                 |t-test |5.42e-05 |-2.537   |-3.926  |-1.148 |0.0583 |
|Slide          |7800246046  |PC2                 |t-test |1.75e-03 |1.797    |0.520   |3.073  |0.0357 |
|Slide          |7512560115  |PC2                 |t-test |8.36e-03 |1.518    |0.235   |2.802  |0.0255 |
|Slide          |5730192053  |PC2                 |t-test |3.73e-03 |2.137    |0.496   |3.777  |0.0307 |
|Slide          |5765205058  |PC2                 |t-test |1.49e-03 |-2.168   |-3.685  |-0.651 |0.0368 |
|Slide          |5730053006  |PC2                 |t-test |2.85e-14 |-7.313   |-9.358  |-5.267 |0.1912 |
|Slide          |5730053010  |PC2                 |t-test |3.12e-19 |-8.698   |-10.719 |-6.678 |0.2546 |
|Slide          |5730053011  |PC2                 |t-test |2.02e-08 |-7.348   |-10.205 |-4.491 |0.1094 |
|Slide          |5730053027  |PC2                 |t-test |9.87e-20 |-8.839   |-10.860 |-6.819 |0.2608 |
|Slide          |5730053037  |PC2                 |t-test |1.11e-12 |-6.721   |-8.744  |-4.698 |0.1690 |
|Slide          |5730192036  |PC2                 |t-test |3.39e-03 |-2.360   |-4.153  |-0.566 |0.0314 |
|Slide          |5730192048  |PC2                 |t-test |1.44e-16 |-4.511   |-5.660  |-3.362 |0.2215 |
|Slide          |5730192057  |PC2                 |t-test |7.68e-05 |-3.531   |-5.506  |-1.555 |0.0564 |
|Slide          |5730053048  |PC2                 |t-test |1.18e-04 |-2.615   |-4.119  |-1.112 |0.0535 |
|Sex            |M           |PC2                 |t-test |9.09e-04 |-1.074   |-1.785  |-0.364 |0.0382 |
|Age            |55          |PC2                 |t-test |1.48e-03 |-1.755   |-2.982  |-0.529 |0.0364 |
|Age            |69          |PC2                 |t-test |7.19e-04 |-1.902   |-3.150  |-0.654 |0.0411 |
|Age            |62          |PC2                 |t-test |5.05e-03 |-1.473   |-2.642  |-0.304 |0.0286 |
|Age            |48          |PC2                 |t-test |8.38e-04 |-2.578   |-4.292  |-0.863 |0.0403 |
|Age            |24          |PC2                 |t-test |6.53e-04 |-6.196   |-10.236 |-2.157 |0.0420 |
|Smoking        |never       |PC2                 |t-test |7.38e-04 |-0.947   |-1.560  |-0.333 |0.0398 |
|Slide          |            |PC3                 |F-test |1.19e-24 |6.959    |        |       |0.5581 |
|Slide          |5730192053  |PC3                 |t-test |6.01e-04 |-2.381   |-3.923  |-0.840 |0.0401 |
|Slide          |5765205058  |PC3                 |t-test |2.96e-10 |-4.166   |-5.599  |-2.733 |0.1277 |
|Slide          |5765205059  |PC3                 |t-test |4.30e-11 |-4.182   |-5.552  |-2.812 |0.1399 |
|Slide          |5730053006  |PC3                 |t-test |2.94e-03 |2.526    |0.634   |4.417  |0.0303 |
|Slide          |5730192048  |PC3                 |t-test |3.12e-07 |-2.613   |-3.733  |-1.494 |0.0870 |
|Slide          |5730053048  |PC3                 |t-test |1.78e-03 |-2.014   |-3.449  |-0.580 |0.0334 |
|Age            |65          |PC3                 |t-test |7.50e-03 |-2.037   |-3.737  |-0.338 |0.0246 |
|Slide          |            |PC4                 |F-test |1.90e-65 |22.811   |        |       |0.8054 |
|Slide          |7800246087  |PC4                 |t-test |2.77e-03 |-1.628   |-2.840  |-0.417 |0.0303 |
|Slide          |7800246140  |PC4                 |t-test |2.38e-05 |-2.282   |-3.475  |-1.089 |0.0596 |
|Slide          |7800246006  |PC4                 |t-test |5.98e-03 |1.692    |0.320   |3.065  |0.0257 |
|Slide          |7800246054  |PC4                 |t-test |6.68e-03 |1.478    |0.264   |2.693  |0.0250 |
|Slide          |7800246034  |PC4                 |t-test |4.43e-03 |1.888    |0.410   |3.367  |0.0275 |
|Slide          |7800246046  |PC4                 |t-test |2.73e-04 |1.875    |0.733   |3.018  |0.0446 |
|Slide          |7800246057  |PC4                 |t-test |2.57e-03 |1.853    |0.485   |3.222  |0.0308 |
|Slide          |7512560103  |PC4                 |t-test |1.92e-03 |-1.604   |-2.753  |-0.454 |0.0326 |
|Slide          |7512560104  |PC4                 |t-test |7.67e-03 |-1.539   |-2.825  |-0.252 |0.0242 |
|Slide          |7512560115  |PC4                 |t-test |9.09e-03 |-1.352   |-2.507  |-0.196 |0.0232 |
|Slide          |7766130166  |PC4                 |t-test |1.07e-03 |-2.683   |-4.507  |-0.860 |0.0361 |
|Slide          |5730053006  |PC4                 |t-test |3.46e-03 |2.367    |0.563   |4.170  |0.0290 |
|Slide          |5730053010  |PC4                 |t-test |3.90e-04 |2.861    |1.070   |4.652  |0.0424 |
|Slide          |5730053027  |PC4                 |t-test |5.08e-03 |2.270    |0.464   |4.075  |0.0267 |
|Slide          |5730053037  |PC4                 |t-test |8.70e-06 |3.566    |1.797   |5.335  |0.0658 |
|Slide          |5730192057  |PC4                 |t-test |6.26e-04 |-2.761   |-4.555  |-0.967 |0.0395 |
|Slide          |5730053048  |PC4                 |t-test |3.19e-05 |-2.540   |-3.889  |-1.190 |0.0578 |
|Slide          |            |PC5                 |F-test |3.17e-57 |18.624   |        |       |0.7717 |
|Slide          |7800246085  |PC5                 |t-test |4.02e-03 |-1.103   |-1.958  |-0.249 |0.0281 |
|Slide          |7800246087  |PC5                 |t-test |1.62e-04 |-1.359   |-2.158  |-0.561 |0.0478 |
|Slide          |7800246123  |PC5                 |t-test |1.08e-06 |-1.657   |-2.403  |-0.910 |0.0786 |
|Slide          |7800246018  |PC5                 |t-test |5.00e-03 |-0.923   |-1.656  |-0.191 |0.0268 |
|Slide          |7800246054  |PC5                 |t-test |9.30e-04 |-1.196   |-1.999  |-0.394 |0.0370 |
|Slide          |7512560104  |PC5                 |t-test |2.49e-04 |1.399    |0.552   |2.245  |0.0451 |
|Slide          |7512560115  |PC5                 |t-test |5.48e-05 |1.379    |0.623   |2.135  |0.0545 |
|Slide          |7512560124  |PC5                 |t-test |2.15e-03 |1.055    |0.290   |1.820  |0.0319 |
|Slide          |5765205058  |PC5                 |t-test |2.81e-09 |2.414    |1.530   |3.299  |0.1141 |
|Slide          |5765205059  |PC5                 |t-test |9.81e-05 |1.585    |0.684   |2.486  |0.0509 |
|Slide          |5730192036  |PC5                 |t-test |1.82e-05 |2.051    |0.994   |3.107  |0.0613 |
|Slide          |5730192048  |PC5                 |t-test |1.28e-04 |-1.252   |-1.976  |-0.528 |0.0492 |
|Sex            |            |PC5                 |F-test |6.68e-04 |11.829   |        |       |0.0389 |
|Sex            |M           |PC5                 |t-test |3.41e-04 |0.493    |0.191   |0.795  |0.0432 |
|Sex            |F           |PC5                 |t-test |6.68e-04 |-0.476   |-0.773  |-0.179 |0.0389 |

## Principal components of the normalized betas

The following plots show the first 3 principal components of the
 most variable
probes colored by batch variables.
Batch variables with more than 10 levels are omitted.




<img src="_main_files/figure-html/unnamed-chunk-62-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-64-1.png" width="1728" style="display: block; margin: auto;" />

## Normalized probe associations with measured batch variables

The most variable normalized probes were extracted, decomposed into
principal components and each component regressed against each batch
variable. If the normalization has performed well then there will be
no associations between normalized probe PCs and batch
variables. Horizontal dotted line denotes $p = 0.05$ in log-scale.




<img src="_main_files/figure-html/unnamed-chunk-66-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-68-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-70-1.png" width="1728" style="display: block; margin: auto;" />




<img src="_main_files/figure-html/unnamed-chunk-72-1.png" width="1728" style="display: block; margin: auto;" />

The following plots show regression coefficients when
each principal component is regressed against each batch variable level
along with 95% confidence intervals.
Cases significantly different from zero are coloured red
(p < 0.01, t-test).




<img src="_main_files/figure-html/unnamed-chunk-73-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-74-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-75-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-76-1.png" width="576" style="display: block; margin: auto;" />


<img src="_main_files/figure-html/unnamed-chunk-77-1.png" width="576" style="display: block; margin: auto;" />


|batch.variable |batch.value |principal.component |test   |p.value  |estimate |lower  |upper  |r2     |
|:--------------|:-----------|:-------------------|:------|:--------|:--------|:------|:------|:------|
|Slide          |            |PC2                 |F-test |2.90e-36 |10.38    |       |       |0.6532 |
|Slide          |7512560104  |PC2                 |t-test |2.42e-03 |-3.28    |-5.687 |-0.875 |0.0331 |
|Slide          |5765205058  |PC2                 |t-test |2.80e-04 |4.18     |1.628  |6.727  |0.0471 |
|Slide          |5730053006  |PC2                 |t-test |2.78e-11 |10.55    |7.133  |13.964 |0.1476 |
|Slide          |5730053010  |PC2                 |t-test |2.35e-12 |11.03    |7.654  |14.406 |0.1629 |
|Slide          |5730053011  |PC2                 |t-test |4.90e-06 |9.92     |5.134  |14.696 |0.0732 |
|Slide          |5730053027  |PC2                 |t-test |3.29e-11 |10.37    |6.999  |13.742 |0.1471 |
|Slide          |5730053037  |PC2                 |t-test |5.31e-11 |10.38    |6.963  |13.790 |0.1437 |
|Slide          |5730192048  |PC2                 |t-test |1.18e-10 |5.91     |3.929  |7.889  |0.1403 |
|Sex            |F           |PC2                 |t-test |2.48e-03 |1.37     |0.412  |2.333  |0.0322 |
|Age            |48          |PC2                 |t-test |2.09e-03 |4.00     |1.108  |6.896  |0.0338 |
|Age            |28          |PC2                 |t-test |7.95e-03 |5.69     |0.907  |10.471 |0.0254 |
|Smoking        |            |PC2                 |F-test |2.87e-03 |5.97     |       |       |0.0394 |
|Smoking        |never       |PC2                 |t-test |8.43e-03 |1.17     |0.194  |2.137  |0.0243 |
|Smoking        |former      |PC2                 |t-test |2.83e-03 |1.26     |0.336  |2.180  |0.0312 |
|Slide          |            |PC3                 |F-test |6.47e-04 |1.96     |       |       |0.2626 |
|Slide          |7512560115  |PC3                 |t-test |2.05e-04 |3.48     |1.401  |5.551  |0.0465 |
|Slide          |7512560124  |PC3                 |t-test |2.04e-04 |3.52     |1.420  |5.622  |0.0464 |
|Slide          |7512560128  |PC3                 |t-test |1.34e-03 |3.36     |1.030  |5.683  |0.0349 |
|Slide          |5730053010  |PC3                 |t-test |1.30e-03 |-4.73    |-7.994 |-1.457 |0.0351 |
|Slide          |5730192048  |PC3                 |t-test |3.52e-03 |-2.62    |-4.621 |-0.622 |0.0290 |
|Age            |            |PC3                 |F-test |3.01e-05 |2.28     |       |       |0.2981 |
|Age            |69          |PC3                 |t-test |5.40e-04 |-2.97    |-4.879 |-1.066 |0.0405 |
|Age            |36          |PC3                 |t-test |1.37e-03 |4.22     |1.287  |7.144  |0.0348 |
|Age            |70          |PC3                 |t-test |6.41e-03 |-4.01    |-7.300 |-0.730 |0.0253 |
|Age            |46          |PC3                 |t-test |3.69e-03 |4.93     |1.145  |8.707  |0.0287 |
|Age            |64          |PC3                 |t-test |7.86e-03 |-3.05    |-5.604 |-0.491 |0.0240 |
|Age            |29          |PC3                 |t-test |4.23e-03 |8.48     |1.870  |15.093 |0.0278 |
|Slide          |            |PC4                 |F-test |2.31e-03 |1.82     |       |       |0.2479 |
|Slide          |7512560103  |PC4                 |t-test |4.50e-03 |-2.25    |-4.019 |-0.487 |0.0275 |
|Slide          |5730053041  |PC4                 |t-test |7.74e-05 |-3.70    |-5.767 |-1.626 |0.0525 |
|Slide          |            |PC5                 |F-test |5.75e-68 |24.23    |       |       |0.8147 |
|Slide          |7800246087  |PC5                 |t-test |2.94e-06 |3.58     |1.896  |5.270  |0.0727 |
|Slide          |7800246123  |PC5                 |t-test |1.87e-07 |3.78     |2.191  |5.367  |0.0896 |
|Slide          |7800246137  |PC5                 |t-test |2.47e-03 |2.13     |0.564  |3.694  |0.0311 |
|Slide          |7800246140  |PC5                 |t-test |1.74e-03 |2.42     |0.703  |4.147  |0.0333 |
|Slide          |7512560104  |PC5                 |t-test |1.67e-03 |-2.58    |-4.401 |-0.753 |0.0335 |
|Slide          |7512560124  |PC5                 |t-test |5.23e-04 |2.55     |0.918  |4.178  |0.0407 |
|Slide          |5730192053  |PC5                 |t-test |3.29e-07 |-4.75    |-6.792 |-2.709 |0.0861 |
|Slide          |5730504015  |PC5                 |t-test |8.89e-03 |-3.48    |-6.451 |-0.512 |0.0234 |
|Slide          |5765205058  |PC5                 |t-test |5.99e-06 |-3.97    |-5.910 |-2.039 |0.0681 |
|Slide          |5765205059  |PC5                 |t-test |3.52e-09 |-5.13    |-7.019 |-3.238 |0.1131 |
|Slide          |5730192036  |PC5                 |t-test |6.25e-05 |-4.11    |-6.380 |-1.837 |0.0539 |
|Slide          |5730053041  |PC5                 |t-test |1.74e-03 |-2.74    |-4.687 |-0.793 |0.0333 |
|Slide          |5730053048  |PC5                 |t-test |3.95e-04 |-3.09    |-5.031 |-1.156 |0.0424 |
|Sex            |            |PC5                 |F-test |4.66e-14 |62.90    |       |       |0.1772 |
|Sex            |M           |PC5                 |t-test |7.71e-15 |-2.23    |-2.835 |-1.628 |0.1877 |
|Sex            |F           |PC5                 |t-test |1.70e-13 |2.13     |1.541  |2.723  |0.1706 |
|Age            |33          |PC5                 |t-test |1.82e-03 |2.94     |0.842  |5.041  |0.0330 |
|Age            |65          |PC5                 |t-test |7.56e-03 |-2.76    |-5.069 |-0.456 |0.0243 |
|Age            |68          |PC5                 |t-test |3.86e-04 |-2.81    |-4.573 |-1.055 |0.0423 |

## R session information


```
## R version 4.2.1 (2022-06-23 ucrt)
## Platform: x86_64-w64-mingw32/x64 (64-bit)
## Running under: Windows 10 x64 (build 22621)
## 
## Matrix products: default
## 
## locale:
## [1] LC_COLLATE=Spanish_Spain.utf8  LC_CTYPE=Spanish_Spain.utf8    LC_MONETARY=Spanish_Spain.utf8 LC_NUMERIC=C                  
## [5] LC_TIME=Spanish_Spain.utf8    
## 
## attached base packages:
## [1] parallel  stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
##  [1] meffil_1.3.6          preprocessCore_1.58.0 SmartSVA_0.1.3        RSpectra_0.16-1       isva_1.9              JADE_2.0-3           
##  [7] qvalue_2.28.0         gdsfmt_1.32.0         statmod_1.5.0         quadprog_1.5-8        DNAcopy_1.70.0        fastICA_1.2-3        
## [13] lme4_1.1-30           Matrix_1.5-1          multcomp_1.4-20       TH.data_1.1-1         survival_3.3-1        mvtnorm_1.1-3        
## [19] matrixStats_0.62.0    markdown_1.7          gridExtra_2.3         Cairo_1.6-0           knitr_1.43            reshape2_1.4.4       
## [25] plyr_1.8.7            ggplot2_3.4.2         sva_3.44.0            BiocParallel_1.30.3   genefilter_1.78.0     mgcv_1.8-40          
## [31] nlme_3.1-157          limma_3.52.4          sandwich_3.0-2        lmtest_0.9-40         zoo_1.8-11            MASS_7.3-57          
## [37] illuminaio_0.38.0     bookdown_0.34        
## 
## loaded via a namespace (and not attached):
##  [1] minqa_1.2.4            colorspace_2.0-3       XVector_0.36.0         fs_1.5.2               base64_2.0.1          
##  [6] clue_0.3-64            rstudioapi_0.14        farver_2.1.1           bit64_4.0.5            AnnotationDbi_1.58.0  
## [11] fansi_1.0.3            xml2_1.3.3             codetools_0.2-19       splines_4.2.1          downlit_0.4.3         
## [16] cachem_1.0.6           jsonlite_1.8.3         nloptr_2.0.3           annotate_1.74.0        cluster_2.1.3         
## [21] png_0.1-7              compiler_4.2.1         httr_1.4.6             fastmap_1.1.0          cli_3.6.1             
## [26] htmltools_0.5.5        tools_4.2.1            gtable_0.3.3           glue_1.6.2             GenomeInfoDbData_1.2.8
## [31] dplyr_1.1.2            Rcpp_1.0.9             Biobase_2.56.0         jquerylib_0.1.4        vctrs_0.6.3           
## [36] Biostrings_2.64.1      xfun_0.39              stringr_1.5.0          mime_0.12              lifecycle_1.0.3       
## [41] XML_3.99-0.10          edgeR_3.38.4           zlibbioc_1.42.0        scales_1.2.1           yaml_2.3.5            
## [46] memoise_2.0.1          sass_0.4.6             stringi_1.7.6          RSQLite_2.2.17         highr_0.10            
## [51] S4Vectors_0.34.0       BiocGenerics_0.42.0    boot_1.3-28.1          GenomeInfoDb_1.32.4    commonmark_1.9.0      
## [56] rlang_1.1.1            pkgconfig_2.0.3        bitops_1.0-7           evaluate_0.21          lattice_0.20-45       
## [61] labeling_0.4.2         bit_4.0.4              tidyselect_1.2.0       magrittr_2.0.3         R6_2.5.1              
## [66] IRanges_2.30.1         generics_0.1.3         DBI_1.1.3              pillar_1.9.0           withr_2.5.0           
## [71] KEGGREST_1.36.3        RCurl_1.98-1.7         tibble_3.2.1           crayon_1.5.2           utf8_1.2.2            
## [76] rmarkdown_2.23         locfit_1.5-9.6         grid_4.2.1             blob_1.2.4             digest_0.6.29         
## [81] xtable_1.8-4           openssl_2.0.3          stats4_4.2.1           munsell_0.5.0          bslib_0.5.0           
## [86] askpass_1.1
```
