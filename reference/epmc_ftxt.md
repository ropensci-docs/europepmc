# Fetch Europe PMC full texts

This function loads full texts into R. Full texts are in XML format and
are only provided for the Open Access subset of Europe PMC.

## Usage

``` r
epmc_ftxt(ext_id = NULL)
```

## Arguments

- ext_id:

  character, PMCID. All full text publications have external IDs
  starting 'PMC\_'

## Value

xml_document

## Examples

``` r
  if (FALSE) { # \dontrun{
  epmc_ftxt("PMC3257301")
  epmc_ftxt("PMC3639880")
  } # }
```
