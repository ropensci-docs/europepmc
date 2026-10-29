# Search Europe PMC by a DOI name

Please use
[`epmc_search_by_doi`](https://docs.ropensci.org/europepmc/reference/epmc_search_by_doi.md)
instead. It calls this method, returning open access status information
from all your requests.

## Usage

``` r
epmc_search_by_doi_(doi, .pb = NULL, output = NULL)
```

## Arguments

- doi:

  character vector containing DOI names.

- .pb:

  progress bar object

- output:

  character, what kind of output should be returned. One of 'parsed',
  'id_list' or 'raw' As default, parsed key metadata will be returned as
  data.frame. 'id_list' returns a list of IDs and sources. Use 'raw' to
  get full metadata as list. Please be aware that these lists can become
  very large.

## Examples

``` r
if (FALSE) { # \dontrun{
  epmc_search_by_doi_("10.1159/000479962")
} # }
```
