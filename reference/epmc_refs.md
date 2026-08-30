# Get references for a given publication

This function retrieves all the works listed in the bibliography of a
given article.

## Usage

``` r
epmc_refs(ext_id = NULL, data_src = "med", limit = 100, verbose = TRUE)
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

returns reference section as tibble

## Examples

``` r
if (FALSE) { # \dontrun{
epmc_refs("PMC3166943", data_src = "pmc")
epmc_refs("25378340")
epmc_refs("21753913")
} # }
```
