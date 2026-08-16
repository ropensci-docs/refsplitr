# Extracts the lat and long for each address from authors_clean

`authors_georef` This function takes the final author list from
refine_authors, and calculates the lat long of the city, country, and
postal code (for USA addresses) or city and country (for addresses
outside the USA).

## Usage

``` r
authors_georef(data, address_column = "address", google_api = FALSE)
```

## Arguments

- data:

  dataframe from
  [`authors_refine()`](https://docs.ropensci.org/refsplitr/reference/authors_refine.md)

- address_column:

  name of column in quotes where the addresses are

- google_api:

  if `google_api = FALSE` georeferencing is carried out with the
  `tidygeocoder` package (option
  [`geocode()`](https://rdrr.io/pkg/ggmap/man/geocode.html) with
  `method = 'osm'`). If `google_api = TRUE`, then geocoding is done with
  the Google Maps API. Defaults to `FALSE`.

## Details

The output is a list of three data.frames `addresses` All info from
'refine_authors' plus new columns with lat & long. It includes ALL
addresses, including those that could not be geocoded.
`missing_addresses` A data frame of the addresses that could NOT be
geocoded. `no_missing_addresses` the `addresses` data frame with ONLY
the addresses that were geocoded.

## Examples

``` r
if (FALSE) { # \dontrun{
BITR_georef_df <- authors_georef(BITR_refined, address_column = "address",
google_api=FALSE)
} # }
```
