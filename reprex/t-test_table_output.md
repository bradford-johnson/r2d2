``` r
library(dplyr)
#> 
#> Attaching package: 'dplyr'
#> The following objects are masked from 'package:stats':
#> 
#>     filter, lag
#> The following objects are masked from 'package:base':
#> 
#>     intersect, setdiff, setequal, union
library(broom)
#> Warning: package 'broom' was built under R version 4.1.3
mtcars %>%
  group_by(vs) %>%
  do(tidy(t.test(.$mpg)))
#> # A tibble: 2 x 9
#> # Groups:   vs [2]
#>      vs estimate statistic  p.value parameter conf.low conf.high method  alter~1
#>   <dbl>    <dbl>     <dbl>    <dbl>     <dbl>    <dbl>     <dbl> <chr>   <chr>  
#> 1     0     16.6      18.3 1.32e-12        17     14.7      18.5 One Sa~ two.si~
#> 2     1     24.6      17.1 2.75e-10        13     21.5      27.7 One Sa~ two.si~
#> # ... with abbreviated variable name 1: alternative
```

<sup>Created on 2022-11-02 with [reprex v2.0.2](https://reprex.tidyverse.org)</sup>
