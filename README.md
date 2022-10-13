## redguards: Factionalism and the Red Guards under Mao's China: Ideal Point Estimation Using Text Data  <br /> 

[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)
[![R](https://github.com/davidycliao/redguards/actions/workflows/r.yml/badge.svg)](https://github.com/davidycliao/redguards/actions/workflows/r.yml)
[![codecov](https://codecov.io/gh/davidycliao/redguards/branch/master/graph/badge.svg?token=9EWD4E1NCB)](https://codecov.io/gh/davidycliao/redguards)



###  Abstract  

In this paper, we design a new strain of text scaling method, Swordfish (Slogan-featured Wordfish), that takes advantage of the TextRank algorithm to extract the most representative political slogans in a given context and estimates Wordfish with those extracted text variables. We test this method using the case of the Great Proletarian Cultural Revolution in China and the historical archive of handwritten big-character posters and self-printed tabloids from 1966. We estimate student protests' ideal points by analyzing expressed political views in propaganda publications. Our findings point to evidence of factional re(de)alignments within the movement and demonstrate how the students from different educational backgrounds followed Mao Zedong and Xiaohongshu 小紅書 (Little Red Book) and then fell into armed conflicts that divided families, the classes and the society. The results estimated by our approach are shown to be consistent with the representative qualitative literature of factionalism regarding the Cultural Revolution.

**Keywords**：*Text as Data, Textrank, Keyword Extraction,  the Cultural Revolution*  <br>
**Documents**:  [`slides`](https://raw.githack.com/davidycliao/redguards/master/slides/slides.pdf) | [`paper`](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4200926)

<br />

### Replication  

This is a designed package for replicating the estimates and findings in the article of [**Factionalism and the Red Guards under Mao's China: Ideal Point Estimation Using Text Data**](https://raw.githack.com/davidycliao/redguards/master/slides/slides.pdf). In this paper, we design a new strain of text scaling method as we called `SWORDFISH`  (Slogan-based Features Wordfish) that takes advantage of the TextRank algorithm ([Mihalcea and Tarau 2004](https://aclanthology.org/W04-3252/)) to extract the most representative keywords (such as noun collocation phrases) and scale those extracted text variables with Bayesian IRT Generalized Wordfish Model implanted by [Imai, Lo, and Olmsted (2016)](https://imai.fas.harvard.edu/research/files/fastideal.pdf) based on the  [Slapin and Proksch’s “Wordfish”(2008)](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1540-5907.2008.00338.x).



The Red Guard documents analyzed in the paper are archived in [The Databases for The History of Contemporary Chinese Political Movements](http://ccrd.usc.cuhk.edu.hk/Default.aspx?msg=%25u6ca1%25u6709%25u8ba2%25u9605%25uff0c%25u6b22%25u8fce%25u8ba2%25u9605%25uff01) (香港中文大學中國當代運動史數據庫) by The Chinese University of Hong Kong. Please note that replicating the analyses initially requires the access to the original corpus of the textual data. We, as authors and data users, do not fully have the copyright of the sources analyzed in the paper. To comply with the terms of service, we cannot share the textual files publicly. However, we are providing pre-processed textual files parsed on CoNLL-U format and document-term-matrix to replicate the analyses of the last stage. The pre-processed textual materials can be found at [data](https://github.com/davidycliao/redguards/tree/master/data). 


The source code in `replication-code` for replicating the estimates for this paper includes four parts for replication for all tables and figures that appear in both the main paper and the online supplemental materials: 

- __01.tokenization-in-udpipe.R__ (tokenization and part-of-speech tagging on Universal Dependencies via pre-trained model)
- __02.keywords-extraction.R__ (keyword extractions using TextRank)
- __03.pooled-ideal-point-estimates.R__ (textual documents merged by individual participants and estimated by Wordfish scaling method)
- __04.incident-ideal-points-estimates.R__ (textual documents estimated by Wordfish scaling method through time)
- __05.visualization.R__ (data visualization and findings)



Replicating the comparable estimates for this paper is easy. Simply follow the description of [the reference](), folk or download this repo, and run `run_replication()` in the Rstudio console. The results and figures will automatically generated by the source codes and stored in `replication-figures`. The history log of ideal point estimation using `emIRT` will automatically be saved and stored in `misc` folder for further inspection. 



<br />


## Getting started

Install the release version of [_R_](https://cran.r-project.org/mirrors.html) (preferably version 3.6 or above),  [RStudio](https://rstudio.com/products/rstudio/download/#download) and  `usethis` and `devtools` from CRAN with `install.packages(c("usethis", "devtools")) `.

```
install.packages(c("usethis", "devtools"))
library(usethis)
library(devtools)
```

Download the `redguards` repository from GitHub with `use_course` and tick Yes or Definitely, automatically bringing you to the redguards project.

```
usethis::use_course(create_download_url("https://github.com/davidycliao/redguards"))
```

Then, build the project package by `install()` and load it. 
```
devtools::install()
library(redguards)
```
Last, start replication with `run_replication()`. 
```
run_replication()
```

Please note that replicating the figures requires installing `STHeiti font` in local computer beforehand to present Chinese characters.


## Cite
```
@unpublished{liao2022,
  author = {Liao, Yen-Chieh and Tsai, Yi-Nung and Tene, Daniel and Zhang, Dechun},
  title = {Factionalism and the Red Guards under Mao's China: Ideal Point Estimation Using Text Data},
  note={SSRN working paper, Available at SSRN: http://ssrn.com/abstract=4200926 },
  year={2022}
}
```



