# Creates a network diagram of coauthors' addresses linked by reference, and with nodes arranged geographically

This function takes an addresses data.frame, links it to an
authors\_\_references dataset and plots a network diagram generated for
individual points of co-authorship.

## Usage

``` r
plot_net_address(
  data,
  mapRegion = "world",
  lineResolution = 10,
  lineAlpha = 0.5
)
```

## Arguments

- data:

  the `address` element from the list outputted from the
  [`authors_georef()`](https://docs.ropensci.org/refsplitr/reference/authors_georef.md)
  function, containing geocoded address latitude and longitude
  locations.

- mapRegion:

  what portion of the world map to show. possible values include
  `"world"`, `"North America"`, `"South America"`, `"Australia"`,
  `"Africa"`, `"Antarctica"`, `"Eurasia"`

- lineResolution:

  the resolution of the lines drawn, higher numbers will make smoother
  curves default is 10.

- lineAlpha:

  transparency of the lines, fed into ggplots alpha value. Number
  between 0 - 1.

## Examples

``` r
## Using the output of authors_georef (e.g., BITR_geocode)
data(BITR_geocode)
## Plots the whole world
output <- plot_net_address(BITR_geocode)

## Just select North America
output <- plot_net_address(BITR_geocode, mapRegion = 'North America')

## Change the transparency of lines by modifying the lineAlpha parameter
output <- plot_net_address(BITR_geocode, lineAlpha = 0.2)
                 
## Change the curvature of lines by modifying the lineResolution paramater
output <- plot_net_address(BITR_geocode, lineResolution = 30 )
                 
output <- plot_net_address(BITR_geocode, mapRegion = 'North America', lineAlpha = 0.2,
                 lineResolution = 30)

```
