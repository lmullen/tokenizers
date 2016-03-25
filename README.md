<!-- README.md is generated from README.Rmd. Please edit that file -->
tokenizers
----------

An R package that collects functions with a consistent interface to convert natural language text into tokens.

**Author:** [Lincoln Mullen](http://lincolnmullen.com)<br> **License:** [MIT](http://opensource.org/licenses/MIT)<br> **Status:** In development

[![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/tokenizers)](http://cran.r-project.org/package=tokenizers) [![Travis-CI Build Status](https://travis-ci.org/lmullen/tokenizers.svg?branch=master)](https://travis-ci.org/lmullen/tokenizers)

### Installation

To get the development version from GitHub, use [devtools](https://github.com/hadley/devtools).

``` r
# install.packages("devtools")
devtools::install_github("ropensci/textreuse", build_vignettes = TRUE)
```

### Contributing

Contributions to the package are more than welcome. One way that you can help is by using this package in your R package for natural language processing. If you want to contribute a tokenization function to this package, it should follow the same conventions as the rest of the functions whenever it makes sense to do so.

1.  It should have a function name that begins with `tokenize_*` and which ends with a plural of whatever kind of tokens are going to be generated. For instance, `tokenize_words()` or `tokenize_ngrams()`.
2.  The function should take as its first argument (named `x`) the texts that are to be tokenized. The input should be either a character vector of any length, where each element in the vector is a text to be tokenized, or it should be a list of character vectors where the each character vector in the list is a text to be tokenized with a length of 1.
3.  The output should be either a character vector of tokens, if the input is a character vector of length 1, or a list of character vectors of tokens, with one character vector in the list for each element in the input character vector or list.

Please note that this project is released with a [Contributor Code of Conduct](CONDUCT.md). By participating in this project you agree to abide by its terms.
