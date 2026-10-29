# Obtain a summary of hit counts

This functions returns the number of results found for your query, and
breaks it down to the various publication types, data sources, and
subsets Europe PMC provides.

## Usage

``` r
epmc_profile(query = NULL, synonym = TRUE)
```

## Arguments

- query:

  character, search query. For more information on how to build a search
  query, see <https://europepmc.org/Help>

- synonym:

  logical, synonym search. If TRUE, synonym terms from MeSH terminology
  and the UniProt synonym list are queried, too. Enabled by default.

## Examples

``` r
if (FALSE) { # \dontrun{
  epmc_profile('malaria')
  # use field search, e.g. query materials and reference section for
  # mentions of "ropensci"
  epmc_profile('(METHODS:"ropensci")')
 } # }
```
