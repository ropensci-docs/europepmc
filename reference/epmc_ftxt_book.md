# Fetch Europe PMC books

Use this function to retrieve book XML formatted full text for the Open
Access subset of the Europe PMC bookshelf.

## Usage

``` r
epmc_ftxt_book(ext_id = NULL)
```

## Arguments

- ext_id:

  character, publication identifier. All book full texts are accessible
  either by the PMID or the 'NBK' book number.

## Value

xml_document

## Examples

``` r
  if (FALSE) { # \dontrun{
  epmc_ftxt_book("NBK32884")
  } # }
```
