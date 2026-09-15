# Plot address point locations on world map

This function plots an addresses data.frame object by point overlaid on
the countries of the world.

## Usage

``` r
plot_addresses_points(data, mapCountry = NULL)
```

## Arguments

- data:

  the `address` element from the list output by the \`authors_georef()“
  function, containing geocoded address latitude and longitude
  locations.

- mapCountry:

  What country to map. Possible values include `"USA"`, `"Brazil"`,
  `"Australia",` and `"UK"` use `data(countries)` to see possible names.
  No value defaults to the world map.

## Examples

``` r
## Using the output of authors_georef (e.g., BITR_geocode)
data(BITR_geocode)
## Plots the whole world
plot_addresses_points(BITR_geocode)


## mapCountry names can be querried using:
data(countries)

## Plot only Brazil
plot_addresses_points(BITR_geocode, mapCountry = 'Brazil')

```
