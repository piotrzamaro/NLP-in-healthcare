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


```{r echo = F}
{query = "cost AND DALY[Title/Abstract]"

q <- pubmedR::pmQueryTotalCount(query)
D <- pubmedR::pmApiRequest(q = query, api_key = api_key, limit = q$total_count)
``` 

```{r}
cost <- results <- biblioAnalysis(dataset1)
sum <- summary(dataset1, pause=F, width=130)
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


#### CZYSZCZENIE ZBIORU

```{r echo = F, eval=T}
data <- dataset1 %>%
  filter(DT == "JOURNAL ARTICLE",
         LA == "ENG")
```


#### STRUKTURA KORPUSU

```{r echo = F}
datacorp <-  corpus(data, 
         text_field = "AB_TM", 
         docid_field = "PMID",
         unique_docnames = F)

corpus(data, 
         text_field = "TI", 
         docid_field = "PMID",
         unique_docnames = F)
summary(datacorp)
```

```{r echo = F, eval = F}
data %>%
    select(PMID, PY, TI, AB) %>%
          corpus(text_field = "AB", docid_field = "TI",  unique_docnames = F) %>%
    summary() %>%
    head(2)
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












