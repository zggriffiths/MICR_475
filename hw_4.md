HW 4
================
Zabrenna Griffiths

1.  

``` r
a <-3
b <-2

print(sum(a,b))
```

    ## [1] 5

2.  

``` r
answer <- sum(2,3)
answer
```

    ## [1] 5

3.  

``` r
# loading packages needed
library(nycflights13)
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.1 ──

    ## ✓ ggplot2 3.3.5     ✓ purrr   0.3.4
    ## ✓ tibble  3.1.4     ✓ dplyr   1.0.7
    ## ✓ tidyr   1.1.3     ✓ stringr 1.4.0
    ## ✓ readr   2.0.1     ✓ forcats 0.5.1

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
library(ggplot2)
```

``` r
# filtering out flights for American Airlines
AA_flights <- (filter(nycflights13::flights, carrier == "AA"))
```

``` r
# making scatter plot
flight_plot <- ggplot(data=AA_flights, aes(x=dep_delay, y=arr_delay)) +
  geom_point()
flight_plot
```

    ## Warning: Removed 782 rows containing missing values (geom_point).

![](hw_4_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->
