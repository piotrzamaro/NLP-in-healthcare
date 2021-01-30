---
title: "Mierniki efektywnosci kosztowej"
output:
   rmarkdown::html_document:
    theme: lumen
---
```{r echo =F}
require(dplyr)
require(pubmed.mineR)
require(RISmed)
require(quanteda)
require(bibliometrix)
require(ggplot2)
require(quanteda.textmodels)
require(tidyverse)  
```


```{query = "cost AND DALY[Title/Abstract]"

q <- pubmedR::pmQueryTotalCount(query)
D <- pubmedR::pmApiRequest(q = query, api_key = api_key, limit = q$total_count)

``` 

> # COST-EFFECT


Vignettes are long form documentation commonly included in packages. Because
they are part of the distribution of the package, they need to be as compact as
possible. The `html_pretty` output format in package
[**prettydoc**](https://github.com/yixuan/prettydoc/) , an alternative
to `html_document` and `html_vignette` contained in the `rmarkdown` package,
is able to generate small and nice HTML pages.


> # METODOLOGIA


#### **WSTĘPNE ZAŁOŻENIA**


```{r)
query
```


#### ZBIÓR ABSTRAKTÓW

```{r eval=FALSE}
n
```


#### CHARAKTERYSTYKA OTRZYMANEGO ZBIORU


```{r eval=FALSE}
u
```


####



> # ANALIZA SEMANTYCZNA


#### STRUKTURA KORPUSU
``` 


#### STATYSTYKI


**Czestosc wystapien**


**Wspolwystepowania**


**Czestotliwosc wzgledna**



**Kolokacje**


#### KLASTFIKACJE


**NnAIWNY KLASYFIKATOR BAYESA**


**ANALIZA KORESPONDENCJI**


**MODELE TEMATYCZNE**


**UTAJONE SKALOWANIE SEMANTYCZE**   
















Currently `html_pretty` supports three page themes, `cayman` (the default),
`tactile`, and `architect`. And there are also two syntax highlight styles:
`github` to mimic the syntax highlight on Github, and `vignette` that is used by
`html_vignette`. If no highlight parameter is given, the default style created
by Pandoc will be used.

The theme and highlight styles can be given in the document metadata,
for example:

```yaml
output:
  prettydoc::html_pretty:
    theme: cayman
    highlight: github
```

## Happy Knitting!

Feel free to use the `knitr` infrastructure with dozens of tunable options in
your package vignette.

```{r fig.width=6, fig.height=6, fig.align='center'}
set.seed(123)
n <- 1000
x1  <- matrix(rnorm(n), ncol = 2)
x2  <- matrix(rnorm(n, mean = 3, sd = 1.5), ncol = 2)
x   <- rbind(x1, x2)
head(x)
smoothScatter(x, xlab = "x1", ylab = "x2")
```

You can also include code snippets of languages other than R, but note that
the block header has no curly brackets around the language name.

```cpp
// [[Rcpp::export]]
NumericVector timesTwo(NumericVector x) {
    return x * 2;
}
```

You can write math expressions, e.g. $Y = X\beta + \epsilon$,
footnotes^[A footnote here.], and tables, e.g. using `knitr::kable()`.

```{r, echo=FALSE, results='asis'}
knitr::kable(head(iris, 10))
```

## Stay Tuned

Please visit the [development page](https://github.com/yixuan/prettydoc/) of the 
`prettydoc` package for latest updates and news. Comments, bug reports and
pull requests are always welcome.

