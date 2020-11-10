---
title: WGCNA Gene Correlation Network Analysis
layout: single
author: Siva Chudalayandi
author_profile: true
header:
  overlay_color: "444444"
  overlay_image: /assets/images/dna.jpg
---

<!--
# The hypothesis

So you have completed an experiment, collecting RNA-seq data across several biological treatments. You may have perfermed differential gene expression analysis (with DESeq2 or similar software) to identify the up and down expressed genes. But how can you relate these up and down expressed genes into a biological story, or gene regulation model?

Assuming that genes that are positively regulating each other will be co-expressed, we can build a hypothesis of a gene-regulation network from a gene correlation network. Warning, the correlation network does not prove co-regulation. Further biological (such as loss-of-function) experiments are required. However, identifying the possible gene-regulation network can indicate which genes to test for co-regulation. 
-->

# Network analysis with WGCNA

<!--
While there are multiple ways to build a co-expression network, we will focus on WGCNA to provide the motivation and framework.--> The WGCNA R package builds “weighted gene correlation networks for
analysis” from expression data. It was originally published in 2008 and continues to be used for many recent papers. Example papers include analyzing gray leaf disease response ([Yu
et
al, 2018](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5072-4#Sec2))
and development/nutrient/metabolism/stress response ([Ma et
al, 2017](https://pubmed.ncbi.nlm.nih.gov/28764653/)). The original
WGCNA publication is below:

  - Langfelder, P. and Horvath, S., 2008. [WGCNA: an R package for
    weighted correlation network
    analysis](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-9-559).
    BMC bioinformatics, 9(1), p.559.
  - Zhang, B. and Horvath, S., 2005. [A general framework for weighted
    gene co-expression network
    analysis](https://pubmed.ncbi.nlm.nih.gov/16646834/). Statistical
    applications in genetics and molecular biology, 4(1).

**More information**

  - [WGCNA
    tutorial](https://horvath.genetics.ucla.edu/html/CoexpressionNetwork/Rpackages/WGCNA/Tutorials/)
  - [Recent PubMed Papers](https://pubmed.ncbi.nlm.nih.gov/?term=wgcna&sort=date)
  - [Video: ISCB Workshop 2016 - Co-expression network analysis using RNA-Seq data (Keith Hughitt)](https://youtu.be/OdqDE5EJSlA)

## Installing WGCNA

Since WGCNA is an R package, we will need to start an R environemnt and install from R's package manager, CRAN.

``` r
# WGCNA is now available on CRAN
install.packages("WGCNA")
```


### Overview ###



