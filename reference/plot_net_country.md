# Creates a network diagram of coauthors' countries linked by reference, \#and with nodes arranged geographically

This function takes an addresses data.frame, links it to an
authors_references dataset and plots a network diagram generated for
countries of co-authorship.

## Usage

``` r
plot_net_country(
  data,
  lineResolution = 10,
  mapRegion = "world",
  lineAlpha = 0.5
)
```

## Arguments

- data:

  the `address` element from the list outputted from the
  [`authors_georef()`](https://docs.ropensci.org/refsplitr/reference/authors_georef.md)
  function, containing geocoded address latitude and longitude
  locations.

- lineResolution:

  the resolution of the lines drawn, higher numbers will make smoother
  curves default is 10.

- mapRegion:

  what portion of the world map to show. possible values include
  `"world"`, `"North America"`, `"South America"`, `"Australia"`,
  `"Africa"`, `"Antarctica"`, and `"Eurasia"`

- lineAlpha:

  transparency of the lines, fed into ggplots alpha value. Number
  between 0 - 1.

## Examples

``` r
## Using the output of authors_georef (e.g., BITR_geocode)
data(BITR_geocode)
## Plots the whole world
output <- plot_net_country(BITR_geocode)
#> whew! finally done...

## Mapping only North America
output <- plot_net_country(BITR_geocode, mapRegion = 'North America')
#> whew! finally done...

## Change the transparency of lines by modifying the lineAlpha parameter
output <- plot_net_country(BITR_geocode, lineAlpha = 0.2)
#> whew! finally done...
                 
## Change the curvature of lines by modifying the lineResolution paramater
output <- plot_net_country(BITR_geocode, lineResolution = 30 )
#> whew! finally done...
                 
## With all arguments: 
output <- plot_net_country(BITR_geocode, mapRegion = 'North America', lineAlpha = 0.2,
                 lineResolution = 30)
#> whew! finally done...


```
