# Package index

## All functions

- [`BITR`](https://docs.ropensci.org/refsplitr/reference/BITR.md) : Data
  from the journal Biotropica (pulled from Web of Knowledge)

- [`BITR_geocode`](https://docs.ropensci.org/refsplitr/reference/BITR_geocode.md)
  : Georeferenced data from the journal Biotropica (pulled from Web of
  Science)

- [`authors_clean()`](https://docs.ropensci.org/refsplitr/reference/authors_clean.md)
  :

  Seperates author information in references files from
  `references_read`

- [`authors_georef()`](https://docs.ropensci.org/refsplitr/reference/authors_georef.md)
  : Extracts the lat and long for each address from authors_clean

- [`authors_refine()`](https://docs.ropensci.org/refsplitr/reference/authors_refine.md)
  : Refines the authors code output from authors_clean()

- [`countries`](https://docs.ropensci.org/refsplitr/reference/countries.md)
  : Names of all the countries in the world

- [`plot_addresses_country()`](https://docs.ropensci.org/refsplitr/reference/plot_addresses_country.md)
  : Plot addresses, the number of which are summed by country_name

- [`plot_addresses_points()`](https://docs.ropensci.org/refsplitr/reference/plot_addresses_points.md)
  : Plot address point locations on world map

- [`plot_net_address()`](https://docs.ropensci.org/refsplitr/reference/plot_net_address.md)
  : Creates a network diagram of coauthors' addresses linked by
  reference, and with nodes arranged geographically

- [`plot_net_coauthor()`](https://docs.ropensci.org/refsplitr/reference/plot_net_coauthor.md)
  : Creates a network diagram of coauthors' countries linked by
  reference This function takes an addresses data.frame, links it to an
  authors_references dataset and plots a network diagram generated for
  co-authorship.

- [`plot_net_country()`](https://docs.ropensci.org/refsplitr/reference/plot_net_country.md)
  : Creates a network diagram of coauthors' countries linked by
  reference, \#and with nodes arranged geographically

- [`references_read()`](https://docs.ropensci.org/refsplitr/reference/references_read.md)
  : Reads Thomson Reuters Web of Knowledge/Science and ISI reference
  export files (both .txt or .ciw format accepted)
