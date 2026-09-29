# Get citations for a given publication

Finds works that cite a given publication.

## Usage

``` r
epmc_citations(ext_id = NULL, data_src = "med", limit = 100, verbose = TRUE)
```

## Arguments

- ext_id:

  character, publication identifier

- data_src:

  character, data source, by default Pubmed/MedLine index will be
  searched.

  The following three letter codes represent the sources Europe PubMed
  Central supports:

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

- limit:

  integer, number of results. By default, this function returns 100
  records.

- verbose:

  logical, print some information on what is going on.

## Value

Metadata of citing documents as data.frame

## Examples

``` r
if (FALSE) { # \dontrun{
epmc_citations("PMC3166943", data_src = "pmc")
epmc_citations("9338777")
} # }
```
