## Factionalism and the Red Guards under Mao's China: Ideal Point Estimation Using Text Data <img src="https://avatars3.githubusercontent.com/u/77121644?s=400&amp;u=49ca6038b83b629a86d391bb2e4d19f8995918a5&amp;v=4" width="130" height="145" align="right"/> <br />




<br />

This is a designed package for replicating the estimates and findings in the article of [**Factionalism and the Red Guards under Mao's China: Ideal Point Estimation Using Text Data**](https://raw.githack.com/davidycliao/redgaurds/master/paper/epsa.pdf). In this paper, we design a new strain of text scaling method called (SWORDFISH, Slogan Wordfish) that takes advantage of the facilitation of the TextRank algorithm to extract the most representative keywords (as known as noun collocation phrases) and scale those extracted text variable via  Wordfish developed by Slapin and Proksch (2008).

The Red Guard documents analyzed in the paper are archived in [The Databases for The History of Contemporary Chinese Political Movements](http://ccrd.usc.cuhk.edu.hk/Default.aspx?msg=%25u6ca1%25u6709%25u8ba2%25u9605%25uff0c%25u6b22%25u8fce%25u8ba2%25u9605%25uff01) (香港中文大學中國當代運動史數據庫) by The Chinese University of Hong Kong. We, as authors, do not fully have the copyright of the sources analyzed in the paper. Please note that replicating the analyses requires access to the original corpus of the textual data. We cannot share publicly to comply with the terms of service regulated by The Chinese University of Hong Kong. However, we are providing preprocessed textual files parsed on CoNLL-U format and document-term-matrix to replicate the analyses of the last stage in this paper. The preprocessed textual materials can be found [here](). We encourage you to purchase original textual data from them if interested.

<br /> 

The source code for replicating the estimates for this paper includes three stages: i) tokenization and part-of-speech tagging on Universal Dependencies; ii) keyword extractions; and last iii) scaling the text feature using Wordfish. Replicating the comparable estimates for this paper is easy. Simply run ***run_replication()*** below if **redguard** package is installed. Please see the [replication reference]().


## Installation Replication Package
You will need lastest installation of [_R_](https://cran.r-project.org/mirrors.html) (preferably version 3.6 or above) and [RStudio](https://rstudio.com/products/rstudio/download/#download).  Visit [Installation](articles/installation.html) for further instructions.

```
install.packages("devtools", dependencies=TRUE)
library(devtools)
devtools::install_github("davidycliao/redguards")
library(devtools)
```


You will need the latest installation of [`R`](https://cran.r-project.org/mirrors.html) (preferably version 4.0 or 3.6 above) and [`RStudio`](https://rstudio.com/products/rstudio/download/#download). Some of the analysis might take lots of rams. So it would be better if replicating the results on HPC.

```
library(redguards)
run_replication()
```



##### Note: Please note that replicating the figures requires installing ***STHeiti font*** in the computer beforehand to present Chinese characters.



## Acknowledge

- The authors gratefully acknowledge [Joint Library of Humanities and Social Sciences, Academia Sinica in Taiwan](https://hslib.sinica.edu.tw/eng/frontpage) (台灣中央研究院人文社會科學聯合圖書館) provided us with access to the database and the use of the High Performance Computing Facility (CERES) and its associated support services at [The University of Essex](https://www.essex.ac.uk/student/it-services/high-performance-computing-(hpc)) in the completion of this work.

## Cite:

For citing this work, you can refer to the present GitHub project. For example, with BibTeX:
```
@misc{redgaurds,
      howpublished = {\url{https://github.com/davidycliao/redgaurds}},
      title = {Factionalism and the Red Guards under Mao’s China: Ideal Point Estimation Using Text Data},
      author = {David Yen-Chieh Liao, Yi-Nung Tsai, and Dechun Zhang},
      publisher = {GitHub},
      year = {2021}
}
```