
<!-- README.md is generated from README.Rmd. Please edit that file -->

# drat dev package hosting

<!-- badges: start -->
<!-- badges: end -->

`drat` ([CRAN](https://cran.r-project.org/package=drat),
[GitHub](https://github.com/eddelbuettel/drat),
[docs](https://eddelbuettel.github.io/drat)) makes it easy to host your
own CRAN-like repositories for packages (or
[data](https://journal.r-project.org/archive/2017/RJ-2017-026/index.html)).

## Paso a paso:

### Paso 1:

Pegar el archivo .tar del paquete en cuestión dentro del repositorio de
`drat`

### Paso 2:

Desde drat, ejecutar la siguiente sentencia:

``` r
library(drat)
options(dratBranch="docs")   # to default to using docs/ as we set up
insertPackage(file="dstools_0.1.0.tar.gz", 
              repodir="../drat/")
```

# Luego se debería poder instalar un paquete con el siguiente comando:

``` r
install.packages("makeup", repos="https://pablotis.github.io/drat", type="source")
#> Installing package into 'C:/Users/pablo/AppData/Local/R/win-library/4.2'
#> (as 'lib' is unspecified)
```

Fuente: <https://eddelbuettel.github.io/drat/vignettes/dratstepbystep/>
