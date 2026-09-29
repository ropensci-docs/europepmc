# Get details for individual records

This function returns parsed metadata for a given publication ID
including abstract, full text links, author details including ORCID and
affiliation, MeSH terms, chemicals, grants.

## Usage

``` r
epmc_details(ext_id = NULL, data_src = "med")
```

## Arguments

- ext_id:

  character, publication identifier

- data_src:

  character, data source, by default Pubmed/MedLine index will be
  searched. Other sources Europe PubMed Central supports are:

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

  pat

  :   Biological Patents

  pmc

  :   PubMed Central

  ppr

  :   Preprint records

## Value

list of data frames

## Examples

``` r
if (FALSE) { # \dontrun{
epmc_details(ext_id = "26980001")
epmc_details(ext_id = "24270414")

# PMC record
epmc_details(ext_id = "PMC4747116", data_src = "pmc")

# Other sources:
# Agricolo
epmc_details("IND43783977", data_src = "agr")
# Biological Patents
epmc_details("EP2412369", data_src = "pat")
# Chinese Biological Abstracts
epmc_details("583843", data_src = "cba")
# CiteXplore
epmc_details("C6802", data_src = "ctx")
# NHS Evidence
epmc_details("338638", data_src = "hir")
# Theses
epmc_details("409323", data_src = "eth")
# Preprint
epmc_details("PPR158112", data_src = "ppr")
} # }
```
