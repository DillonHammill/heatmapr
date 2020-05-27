
<!-- README.md is generated from README.Rmd. Please edit that file -->

# heatmapr <img src="man/figures/logo.png" align="right" alt="" width="240"/>

<!-- badges: start -->

[![Project Status: Active – The project has reached a stable, usable
state and is being actively
developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![Travis build
status](https://travis-ci.com/DillonHammill/heatmapr.svg?branch=master)](https://travis-ci.com/DillonHammill/heatmapr)
[![Codecov test
coverage](https://codecov.io/gh/DillonHammill/heatmapr/branch/master/graph/badge.svg)](https://codecov.io/gh/DillonHammill/heatmapr?branch=master)
[![lifecycle](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
[![Last-changedate](https://img.shields.io/badge/last%20change-2020--05--27-yellowgreen.svg)](/commits/master)
<!-- badges: end -->

**heatmapr** it a lightweight R package that makes it easy to generate
high quality heatmaps with minimal data preprocessing or manual
customization. Visit the **heatmapr** website to get started
(<https://dillonhammill.github.io/heatmapr/>).

## Availabe Packages for Heatmaps

  - heatmap() in the stats package
  - [qplots](https://cran.r-project.org/web/packages/gplots/index.html)
  - [superheat](https://github.com/rlbarter/superheat)
  - [ggplot2](https://github.com/tidyverse/ggplot2)
  - [plotly](https://github.com/ropensci/plotly)
  - [ComplexHeatmap](https://github.com/jokergoo/ComplexHeatmap)

## Benefits of heatmapr

`heatmapr` has a number of benefits over other heatmap packages:

  - **heatmapr** is built using base graphics, so there is no required
    `ggplot2` knowledge in order to use this package.
  - **heatmapr** is extremely lighweight and therefore there are no
    external dependencies that need to be installed.
  - **heatmapr** is designed under ROpenSci naming guidelines for a
    consistent and intuitive user experience.
  - unlike other heatmap packages that use base graphics, **heatmapr**
    actually returns the plot object instead of an image. This makes it
    easy to arrange multiple plots in complex layouts without
    sacrificing resolution.
  - **heatmapr** is fully customizable and comes with useful saving API
    (`heat_map_save()`) to export high resolution images.
  - **heatmapr** handles datasets that contain non-numeric or missing
    data, which means you don’t have to spend ages formatting and
    pre-processing the data.

## Installation

**heatmapr** can be installed directly from GitHub:

``` r
devtools::install_github("DillonHammill/heatmapr")
```

## Usage

Creating heatmaps is as easy as loading **heatmapr** and supplying your
dataset to the `heat_map()` function. For details on customising your
heatmaps, refer to the package vignette.

``` r
library(heatmapr)
heat_map(mtcars,
         scale = "range",
         dendrogram = "both")
```

<img src="man/figures/README-heatmapr-1.png" width="95%" style="display: block; margin: auto;" />

## Code of Conduct

Please note that the heatmapr project is released with a [Contributor
Code of
Conduct](https://contributor-covenant.org/version/2/0/CODE_OF_CONDUCT.html).
By contributing to this project, you agree to abide by its terms.

## Citation

A **heatmapr** publication is on the way, but in the meantime if you use
**heatmapr** for your work please cite the package as follows:

``` r
citation("heatmapr")
#> 
#> To cite package 'heatmapr' in publications use:
#> 
#>   Dillon Hammill (2020). heatmapr: Create Heatmaps using Base Graphics.
#>   R package version 0.0.1. https://github.com/DillonHammill/heatmapr
#> 
#> A BibTeX entry for LaTeX users is
#> 
#>   @Manual{,
#>     title = {heatmapr: Create Heatmaps using Base Graphics},
#>     author = {Dillon Hammill},
#>     year = {2020},
#>     note = {R package version 0.0.1},
#>     url = {https://github.com/DillonHammill/heatmapr},
#>   }
```
