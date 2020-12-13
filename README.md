Climate Modeling package
================

## Installation

    ## Loading required package: data.table

``` r
#devtools::install_github('https://github.com/kazivana/climatemodeling.git')
```

### Examples

# Loading data

``` r
hist_ALADIN <- climatemodeling::historical_ALADIN
hist_rca <- climatemodeling::historical_RCA
```

# Calculating Maxima

``` r
getMX(hist_ALADIN, a = c(2,5,10,20))
```

    ##      year agg        mx
    ##   1: 1951   2  7.984342
    ##   2: 1951   5  7.984342
    ##   3: 1951  10  7.984342
    ##   4: 1951  20  7.984342
    ##   5: 1952   2 11.993943
    ##  ---                   
    ## 876: 2004  20 57.022173
    ## 877: 2005   2 23.688150
    ## 878: 2005   5 23.688150
    ## 879: 2005  10 23.688150
    ## 880: 2005  20 23.688150

# DDF Function

``` r
frequency = c(2,5,10)

hist <- climatemodeling::historical_ALADIN
hist_ddf <- ddff(hist, frequency)
```

    ##     Duration     depth freq hour
    ##  1:       D1  5.467910    2    1
    ##  2:       D1  6.849683    5    1
    ##  3:       D1  7.535927   10    1
    ##  4:       D2  9.964763    2    2
    ##  5:       D2 12.377329    5    2
    ##  6:       D2 13.226612   10    2
    ##  7:       D3 12.988917    2    3
    ##  8:       D3 16.480279    5    3
    ##  9:       D3 17.987438   10    3
    ## 10:       D6 21.211284    2    6
    ## 11:       D6 25.517393    5    6
    ## 12:       D6 28.576816   10    6
    ## 13:      D12 29.551979    2   12
    ## 14:      D12 36.321244    5   12
    ## 15:      D12 43.541245   10   12
    ## 16:      D24 38.116883    2   24
    ## 17:      D24 49.170392    5   24
    ## 18:      D24 59.411640   10   24

# Ploting results
