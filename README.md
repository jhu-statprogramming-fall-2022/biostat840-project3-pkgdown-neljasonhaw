
# nlme

**Linear and Nonlinear Fixed Effects Models**
*with a new vignette by Nel Jason Haw*

Description: Linear and Nonlinear Fixed Effects Models and everything you can do with them

Original Authors: Jose C. Pinheiro and Douglas M. Bates (1997-2005), R Core Team (2005-2022)

<!-- badges: start -->
<!-- badges: end -->

# Location of Original Package
https://github.com/cran/nlme

# Location of Deployed Package Website
https://jhu-statprogramming-fall-2022.github.io/biostat840-project3-pkgdown-neljasonhaw

# Customizations to pkgdown website

* Applied "simplex" bootswatch
* Changed base font to "Source Sans Pro"
* Changed code font to "Source Code Pro"
* Changed theme to "github-light"
* Changed navigation bar background to "light"


# Installation
```r
remotes::install_github(repo = "jhu-statprogramming-fall-2022/biostat840-project2-neljasonhaw")
```

## List of Exported Functions (Used in New Vignette)

Descriptions provided in R Documentation

* `lme`: Linear Mixed-Effects Models: This generic function fits a linear mixed-effects model in the formulation described in Laird and Wre (1982) but allowing for nested random effects. The within-group errors are allowed to be correlated and/or have unequal variances
* `anova.lme`: Compare Likelihoods of Fitted Objects: Likelihood ratio test for two lme model objects

## Example

This is a basic example which shows you how to solve a common problem (from `lme` R Documentation):

``` r
fm1 <- lme(distance ~ age, Orthodont, random = ~ age | Subject)
anova(fm1)
fm2 <- update(fm1, random = pdDiag(~age))
anova(fm1, fm2)
```

