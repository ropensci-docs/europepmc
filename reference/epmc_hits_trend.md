# Get the yearly number of hits for a query and the total yearly number of hits for a given period

Get the yearly number of hits for a query and the total yearly number of
hits for a given period

## Usage

``` r
epmc_hits_trend(query, synonym = TRUE, data_src = "med", period = 1975:2016)
```

## Arguments

- query:

  query in the Europe PMC syntax

- synonym:

  logical, synonym search. If TRUE, synonym terms from MeSH terminology
  and the UniProt synonym list are queried, too. Disabled by default.

- data_src:

  character, data source, by default Pubmed/MedLine index (`med`) will
  be searched. The following three letter codes represent the sources,
  which are currently supported

  agr

  :   Agricola is a bibliographic database of citations to the
      agricultural literature created by the US National Agricultural
      Library and its co-operators.

  cba

  :   Chinese Biological Abstracts

  ctx

  :   CiteXplore

  eth

  :   EthOs Theses, i.e. PhD theses (British Library)

  hir

  :   NHS Evidence

  med

  :   PubMed/Medline NLM

  nbk

  :   Europe PMC Book metadata

  pat

  :   Biological Patents

  pmc

  :   PubMed Central

  ppr

  :   Preprint records

- period:

  a vector of years (numeric) over which to perform the search

## Value

a data.frame (dplyr tbl_df) with year, total number of hits (all_hits)
and number of hits for the query (query_hits)

## Details

A similar function was used in
<https://masalmon.eu/2017/05/14/evergreenreviewgraph/> where it was
advised to not plot no. of hits over time for a query, but to normalize
it by the total no. of hits.

## Examples

``` r
if (FALSE) { # \dontrun{
# aspirin as query
epmc_hits_trend('aspirin', period = 2006:2016, synonym = FALSE)
# link to cran packages in reference lists
epmc_hits_trend('REF:"cran.r-project.org*"', period = 2006:2016, synonym = FALSE)
# more complex with publication type review
epmc_hits_trend('(REF:"cran.r-project.org*") AND (PUB_TYPE:"Review" OR PUB_TYPE:"review-article")',
period = 2006:2016, synonym = FALSE)
} # }
```
