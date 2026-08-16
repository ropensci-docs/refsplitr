# Creates a network diagram of coauthors' countries linked by reference This function takes an addresses data.frame, links it to an authors_references dataset and plots a network diagram generated for co-authorship.

Creates a network diagram of coauthors' countries linked by reference
This function takes an addresses data.frame, links it to an
authors_references dataset and plots a network diagram generated for
co-authorship.

## Usage

``` r
plot_net_coauthor(data)
```

## Arguments

- data:

  the `address` element from the list outputted from the
  \`authors_georef()“ function, containing geocoded address latitude and
  longitude locations.

## Examples

``` r
## Using the output of authors_georef (e.g., BITR_geocode)
data(BITR_geocode)
plot_net_coauthor(BITR_geocode)
#> Warning: vertex attribute frame.color contains NAs. Replacing with default value black

#> IGRAPH b0a0fc2 UNW- 6 9 -- 
#> + attr: name (v/c), label (v/c), label.color (v/c), label.cex (v/n),
#> | size (v/n), frame.color (v/l), color (v/c), weight (e/n)
#> + edges from b0a0fc2 (vertex names):
#> [1] argentina--mexico  argentina--usa     australia--brazil  australia--germany
#> [5] australia--usa     brazil   --germany brazil   --usa     germany  --usa    
#> [9] mexico   --usa    
```
