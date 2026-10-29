# Search Europe PMC publication database

This is the main function to search Europe PMC RESTful Web Service
(<https://europepmc.org/RestfulWebService>). It fully supports the
comprehensive Europe PMC query language. Simply copy & paste your query
terms to R. To get familiar with the Europe PMC query syntax, check the
Advanced Search Query Builder <https://europepmc.org/advancesearch>.

## Usage

``` r
epmc_search(
  query = NULL,
  output = "parsed",
  synonym = TRUE,
  verbose = TRUE,
  limit = 100,
  sort = NULL
)
```

## Arguments

- query:

  character, search query. For more information on how to build a search
  query, see <https://europepmc.org/Help>

- output:

  character, what kind of output should be returned. One of 'parsed',
  'id_list' or 'raw' As default, parsed key metadata will be returned as
  data.frame. 'id_list' returns a list of IDs and sources. Use 'raw' to
  get full metadata as list. Please be aware that these lists can become
  very large.

- synonym:

  logical, synonym search. If TRUE, synonym terms from MeSH terminology
  and the UniProt synonym list are queried, too. In order to replicate
  results from the website, with the Rest API you need to turn synonyms
  ON!

- verbose:

  logical, print progress bar. Activated by default.

- limit:

  integer, limit the number of records you wish to retrieve. By default,
  100 are returned.

- sort:

  character, relevance ranking is used by default. Use `sort = 'cited'`
  for sorting by the number of citations, or `sort = 'date'` by the most
  recent publications.

## Value

tibble

## See also

<https://europepmc.org/Help>

## Examples

``` r
if (FALSE) { # \dontrun{
#Search articles for 'Gabi-Kat'
my.data <- epmc_search(query='Gabi-Kat')

#Get article metadata by DOI
my.data <- epmc_search(query = 'DOI:10.1007/bf00197367')

#Get article metadata by PubMed ID (PMID)
my.data <- epmc_search(query = 'EXT_ID:22246381')

#Get only PLOS Genetics article with EMBL database references
my.data <- epmc_search(query = 'ISSN:1553-7404 HAS_EMBL:y')
#Limit search to 250 PLOS Genetics articles
my.data <- epmc_search(query = 'ISSN:1553-7404', limit = 250)

# exclude MeSH synonyms in search
my.data <- epmc_search(query = 'aspirin', synonym = FALSE)

# get 100 most cited atricles from PLOS ONE publsihed in 2014
epmc_search(query = '(ISSN:1932-6203) AND FIRST_PDATE:2014', sort = 'cited')

# print number of records found
attr(my.data, "hit_count")

# change output

} # }
```
