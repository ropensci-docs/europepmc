# Summarise links to external sources

With the External Link services, Europe PMC allows third parties to
publish links from Europe PMC to other webpages or tools. Current
External Link providers, which can be selected through Europe PMC's
advanced search, include Wikipedia, Dryad Digital Repository or the
institutional repo of Bielefeld University. For more information, see
<https://europepmc.org/labslink>.

## Usage

``` r
epmc_lablinks_count(ext_id = NULL, data_src = "med")
```

## Arguments

- ext_id:

  publication identifier

- data_src:

  data source, by default Pubmed/MedLine index will be searched. The
  following three letter codes represents the sources Europe PubMed
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

## Value

data.frame with counts for each database

## Examples

``` r
   if (FALSE) { # \dontrun{
   epmc_lablinks_count("24023770")
   epmc_lablinks_count("PMC3986813", data_src = "pmc")
   } # }
```
