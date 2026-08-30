# Retrieve external database entities referenced in a given publication

This function returns EBI database entities referenced in a publication
from Europe PMC RESTful Web Service.

## Usage

``` r
epmc_db(
  ext_id = NULL,
  data_src = "med",
  db = NULL,
  limit = 100,
  verbose = TRUE
)
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

- db:

  character, specify database:

  'ARXPR'

  :   Array Express, a database of functional genomics experiments

  'CHEBI'

  :   a database and ontology of chemical entities of biological
      interest

  'CHEMBL'

  :   a database of bioactive drug-like small molecules

  'EMBL'

  :   now ENA, provides a comprehensive record of the world's nucleotide
      sequencing information

  'INTACT'

  :   provides a freely available, open source database system and
      analysis tools for molecular interaction data

  'INTERPRO'

  :   provides functional analysis of proteins by classifying them into
      families and predicting domains and important sites

  'OMIM'

  :   a comprehensive and authoritative compendium of human genes and
      genetic phenotypes

  'PDB'

  :   European resource for the collection, organisation and
      dissemination of data on biological macromolecular structures

  'UNIPROT'

  :   comprehensive and freely accessible resource of protein sequence
      and functional information

  'PRIDE'

  :   PRIDE Archive - proteomics data repository

- limit:

  integer, number of results. By default, this function returns 100
  records.

- verbose:

  logical, print some information on what is going on.

## Value

Cross-references as data.frame

## Examples

``` r
  if (FALSE) { # \dontrun{
  epmc_db("12368864", db = "uniprot", limit = 150)
  epmc_db("25249410", db = "embl")
  epmc_db("14756321", db = "uniprot")
  epmc_db("11805837", db = "pride")
  } # }
```
