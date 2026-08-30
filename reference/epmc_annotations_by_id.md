# Get annotations by article

Retrieve text-mined annotations contained in abstracts and open access
full-text articles.

## Usage

``` r
epmc_annotations_by_id(ids = NULL)
```

## Arguments

- ids, :

  character vector with publication identifiers following the structure
  "source:ext_id", e.g. \`"MED:28585529"\`

## Value

returns text-mined annotations in a tidy format with the following
variables

- source:

  Publication data source

- ext_id:

  Article Identifier

- pmcid:

  PMCID that locates full-text in Pubmed Central

- prefix:

  Text snipped found before the annotation

- exact:

  Annotated entity

- postfix:

  Text snipped found after the annotation

- name:

  Targeted entity

- uri:

  Uniform link dictionary entry for targeted entity

- id:

  URL to full-text occurence of the annotation

- type:

  Type of annotation like Chemicals

- section:

  Article section mentioning the annotation like Methods

- provider:

  Annotation data provider

- subtype:

  Sub-data provider

## Examples

``` r
if (FALSE) { # \dontrun{
  annotations_by_id("MED:28585529")
  # multiple ids
  annotations_by_id(c("MED:28585529", "PMC:PMC1664601"))
} # }
```
