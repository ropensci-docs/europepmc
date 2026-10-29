# Get search result count

Search over Europe PMC and retrieve the number of results found

## Usage

``` r
epmc_hits(query = NULL, ...)
```

## Arguments

- query:

  query in the Europe PMC syntax

- ...:

  add query parameters from \`epmc_search()\`, e.g. synonym=true

## See also

[`epmc_search`](https://docs.ropensci.org/europepmc/reference/epmc_search.md)

## Examples

``` r
 if (FALSE) { # \dontrun{
 epmc_hits('abstract:"burkholderia pseudomallei"')
 epmc_hits('AUTHORID:"0000-0002-7635-3473"')
 } # }
```
