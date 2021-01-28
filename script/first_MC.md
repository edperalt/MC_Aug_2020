---
title: "Montecarlo simulation"
subtitle: "sensitivity to sample size "
date: "8/22/2020"
output: 
  html_document: 
    toc: yes
    toc_float:
      toc_collapsed: yes
    theme: lumen
    keep_md: yes
---







## Description  
This is an excercise to test a montecarlo simulation to estimate the STOOIP of a field, using the [MonteCarlo package](https://cran.r-project.org/web/packages/MonteCarlo/index.html). 
<br>
We will perform simulations increasing the number of runs drawing data from 2 datasets, both with the same distributions for each parameter, however with different number of samples:  
<br>
* Dataset 1 will have 100 samples for each parameter
* Dataset 2 will have 1E6 samples for each parameter  





















































































 






























































## Distributions used

### Area

The area has been  set as an uniform distribution between 5  and 12 km^2^.    


![](first_MC_files/figure-html/unnamed-chunk-19-1.png)<!-- -->

### Thickness


Thickness is defined as a uniform distribution between 8 and 17 meters

![](first_MC_files/figure-html/unnamed-chunk-20-1.png)<!-- -->

### Porosity

Porosity distribution is normal with a mean of 0.2 and 0.03 standard deviation.  

![](first_MC_files/figure-html/unnamed-chunk-21-1.png)<!-- -->


### Water saturation

Water saturation distribution is normal with a mean of 0.22 and 0.04 standard deviation.  

![](first_MC_files/figure-html/unnamed-chunk-22-1.png)<!-- -->


### Bo

Bo distribution is normal with a mean of 1.07 and 0.02 standard deviation.  


![](first_MC_files/figure-html/unnamed-chunk-23-1.png)<!-- -->

## Montecarlo simulations 

The STOOIP is estimated in bbls with the following formula:

$$ STOOIP = Area * Thickness * Porosity * ( 1 - Sw ) / Bo $$  

Blue lines represent p10 and p90 and the red line the p50.

###  100 simulations

![](first_MC_files/figure-html/unnamed-chunk-24-1.png)<!-- -->


### 1,000 simulations

![](first_MC_files/figure-html/unnamed-chunk-25-1.png)<!-- -->


### 10,000 simulations

![](first_MC_files/figure-html/unnamed-chunk-26-1.png)<!-- -->




###  100,000 simulations

![](first_MC_files/figure-html/unnamed-chunk-27-1.png)<!-- -->





###  1,000,000 simulations

![](first_MC_files/figure-html/unnamed-chunk-28-1.png)<!-- -->





