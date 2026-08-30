# Retrieve the number of database links from Europe PMC publication database

This function returns the number of EBI database links associated with a
publication.

## Usage

``` r
epmc_db_count(ext_id = NULL, data_src = "med")
```

## Arguments

- ext_id:

  character, publication identifier

- data_src:

  character, data source, by default Pubmed/MedLine index will be
  searched.

## Value

data.frame with counts for each database

## Details

Europe PMC supports cross-references between literature and the
following databases:

- 'ARXPR':

  Array Express, a database of functional genomics experiments

- 'CHEBI':

  a database and ontology of chemical entities of biological interest

- 'CHEMBL':

  a database of bioactive drug-like small molecules

- 'EMBL':

  now ENA, provides a comprehensive record of the world's nucleotide
  sequencing information

- 'INTACT':

  provides a freely available, open source database system and analysis
  tools for molecular interaction data

- 'INTERPRO':

  provides functional analysis of proteins by classifying them into
  families and predicting domains and important sites

- 'OMIM':

  a comprehensive and authoritative compendium of human genes and
  genetic phenotypes

- 'PDB':

  European resource for the collection, organisation and dissemination
  of data on biological macromolecular structures

- 'UNIPROT':

  comprehensive and freely accessible resource of protein sequence and
  functional information

- 'PRIDE':

  PRIDE Archive - proteomics data repository

## Examples

``` r
  if (FALSE) { # \dontrun{
  epmc_db_count(ext_id = "10779411")
  epmc_db_count(ext_id = "PMC3245140", data_src = "PMC")
  } # }
```
