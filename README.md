
<!-- README.md is generated from README.Rmd. Please edit that file -->

# drat dev package hosting

<!-- badges: start -->
<!-- badges: end -->

`drat` ([CRAN](https://cran.r-project.org/package=drat),
[GitHub](https://github.com/eddelbuettel/drat),
[docs](https://eddelbuettel.github.io/drat)) makes it easy to host your
own CRAN-like repositories for packages (or
[data](https://journal.r-project.org/archive/2017/RJ-2017-026/index.html)).

## Step by step:

### Step 1:

Paste .tar package file inside `drat` repo

### Step 2:

From drat repo, execute:

``` r
library(drat)
options(dratBranch="docs")   # to default to using docs/ as we set up
insertPackage(file="dstools_0.1.0.tar.gz", 
              repodir="../drat/")
```

### Step 3:

Now the package can be installed as a non-CRAN dependency with the next
sentence:

``` r
# dstool package example:
install.packages("dstools", repos="https://pablotis.github.io/drat")
#> Installing package into 'C:/Users/pablo/AppData/Local/R/win-library/4.2'
#> (as 'lib' is unspecified)
#> Warning: unable to access index for repository https://pablotis.github.io/drat/bin/windows/contrib/4.2:
#>   no fue posible abrir la URL 'https://pablotis.github.io/drat/bin/windows/contrib/4.2/PACKAGES'
#> installing the source package 'dstools'
```

### Step 4:

This sentence must be added on the DESCRIPTION file:

``` r
Additional_repositories: http://pablotis.github.io/drat
```

Fuente: <https://eddelbuettel.github.io/drat/vignettes/dratstepbystep/>
