# Georeferenced data from the journal Biotropica (pulled from Web of Science)

A dataset containing 41 authors taken from the Biotropica journal. This
dataset represents the typical formatted output from
[`authors_georef()`](https://docs.ropensci.org/refsplitr/reference/authors_georef.md)
in the refsplitr package. It serves as a useful testing data set for
spatial functions and

## Usage

``` r
BITR_geocode
```

## Format

A data frame with 41 rows and 15 variables:

- authorID:

  ID field populated in authors_clean

- university:

  also can be considered institution for non-universities

- postal_code:

  character, international postcode

- country:

  country name

- lat:

  numeric, latitude populated from authors_georef

- lon:

  numeric, longitude populated from authors_georef

- groupID:

  ID field for what name group the author is identified as from
  authors_clean()

- author_order:

  numeric, order of author from journal article

- address:

  address of references pulled from the original raw WOS file

- department:

  department which is nested within university

- RP_address:

  reprint address, pulled from the original raw WOS file

- RI:

  ResearcherID number, identifier given by web of science only, less
  common than OrcID

- OI:

  OrcID, unique identifier for researcher given by https://orcid.org

- UT:

  unique identifier to each article, given by WOS

- refID:

  unique identifier for each article, given by references_read()
