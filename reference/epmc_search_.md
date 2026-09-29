# Get one page of results when searching Europe PubMed Central

In general, use
[`epmc_search`](https://docs.ropensci.org/europepmc/reference/epmc_search.md)
instead. It calls this function, calling all pages within the defined
limit.

## Usage

``` r
epmc_search_(
  query = NULL,
  limit = 100,
  output = "parsed",
  page_token = NULL,
  ...
)
```

## Arguments

- query:

  character, search query. For more information on how to build a search
  query, see <https://europepmc.org/Help>

- limit:

  integer, limit the number of records you wish to retrieve. By default,
  25 are returned.

- output:

  character, what kind of output should be returned. One of 'parsed',
  'id_list' or 'raw' As default, parsed key metadata will be returned as
  data.frame. 'id_list returns a list of IDs and sources. Use 'raw' to
  get full metadata as list. Please be aware that these lists can become
  very large.

- page_token:

  cursor marking the page

- ...:

  further params from
  [`epmc_search`](https://docs.ropensci.org/europepmc/reference/epmc_search.md)

## See also

[epmc_search](https://docs.ropensci.org/europepmc/reference/epmc_search.md)
