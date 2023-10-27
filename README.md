# SACNAS_RNAseq_Workshop_2023

| Audience | Computational skills required | Duration |
:----------|:----------|:----------|
| SACNAS Attendees | None | 75 minute workshop |

## Description 
This repository has learning materials for a **75 minute**, hands-on **Introduction to RNA-Seq analysis with R/RStudio** workshop. R is a simple programming environment that enables the effective handling of data while providing excellent graphical support. RStudio is a tool that provides a user-friendly environment for working with R. 

These materials are intended to provide a **general overview** of the RNA-Seq data analysis, starting from processed counts files.  

## Learning Objectives 

* **Best practices**: Understand best practices for designing an RNA-seq experiment 
* **Processing steps**: Understand the processing steps from an FASTQ to counts file 
* **R syntax**: Understand general R syntax including variables, functions, and arguments
*  **Using GO terms to explore enriched processes:** Determine pathways for DEGs using Gene Ontology terms
* **Exporting data**: Generate tabular outputs of DEGs to be further investigated and visualized 

### Contents

| Time |  Topic  |  
|:-----------:|:----------| 
| ~10 mins| Module 1: RNAseq experimental setup and considerations| 
| ~10 mins| Module 2: Post sequencing processing steps | 
| ~40 mins | Module 3: Hands-on portion of workshop |
|~15 mins | Questions from attendees | 

### Workshop Slides 

The slides presented in Module 1 and 2 can be found [here](

### Dataset

Download the R project and data for this workshop [here](https://github.com/PRodriguez19/SACNAS_RNAseq_Workshop_2023/blob/main/data/SACNAS-RNAseq-Workshop-2023.zip?raw=true). Decompress and move the folder to the location on your computer where you would like to perform the analysis.

### Installation Requirements

Download R and RStudio for your laptop:

 - [R](http://lib.stat.cmu.edu/R/CRAN/) 
 - [RStudio](https://www.rstudio.com/products/rstudio/download/#download)
 
Install the required R packages by running the following code in RStudio:

```r
# Install CRAN packages
install.packages(c("BiocManager", "RColorBrewer", "tidyverse", "devtools", "pheatmap",  ))

# Install Bioconductor packages
BiocManager::install(c("clusterProfiler", "DESeq2", "org.Hs.eg.db", "EnhancedVolcano", "biomaRt", "enrichplot"))
```

Load the libraries to make sure the packages installed properly:

```r
library(DESeq2) 
library(RColorBrewer)
library(pheatmap)
library(ggplot2)
library(EnhancedVolcano)
library(biomaRt)
library(clusterProfiler)
library(org.Hs.eg.db)
library(enrichplot)
```

> **NOTE:** The library used for the annotations associated with genes (here we are using `org.Hs.eg.db`) will change based on organism (e.g. if studying mouse, would need to install and load `org.Mm.eg.db`). The list of different organism packages are given [here](https://github.com/hbctraining/Training-modules/raw/master/DGE-functional-analysis/img/available_annotations.png).


## Additional Resources

For an overview of bioinformatics, the tools required for RNA-seq analysis and high perfomance computing, see these tutorials (the HPC parts will vary depending on your local cluster):  

[Bioinformatics Training](https://hbctraining.github.io/main/)  
[High Performance Computing](https://jhudatascience.org/Computing_for_Cancer_Informatics/)  
[RNA-seq analysis](https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon-flipped/schedule/links-to-lessons.html)  
[Informatics Technology for Cancer Research Training Network Courses](https://www.itcrtraining.org/resources/courses)  
[R for Data Science](https://r4ds.had.co.nz/introduction.html)  

Need help with Unix?  

[Unix Cheat Sheet](https://www.stationx.net/unix-commands-cheat-sheet/)  
[Vim - command line text editor](https://vim.rtorr.com/)  
[Common commands](https://www.thegeekstuff.com/2010/11/50-linux-commands/)  

Need help with R/RStudio?  

[R/RStudio](https://hbctraining.github.io/Intro-to-R-flipped/schedules/links-to-lessons.html)

[R for Beginners](https://cran.r-project.org/doc/contrib/Paradis-rdebuts_en.pdf) - from CRAN

[Stack Overflow](https://stackoverflow.com/)

[dplyr Cheat Sheet](https://www.rstudio.com/wp-content/uploads/2015/02/data-wrangling-cheatsheet.pdf)

[ggplot2 Cheat Sheet](https://www.maths.usyd.edu.au/u/UG/SM/STAT3022/r/current/Misc/data-visualization-2.1.pdf)

Multiple RNAseq comparisons/ DESeq2:  

[Differential Expression Analysis](https://combine-australia.github.io/RNAseq-R/06-rnaseq-day1.html)  
[Overview](https://hbctraining.github.io/DGE_workshop/lessons/01_DGE_setup_and_overview.html#:~:text=The%20goal%20of%20differential%20expression%20analysis%20is%20to%20determine%2C%20for,observed%20within%20groups%20(replicates).)  

Non-model organisms:  

[Full-length transcriptome assembly from RNA-seq data without a reference genome](https://www.nature.com/articles/nbt.1883)  

FASTQC and multiQC  

[FastQC video](https://www.youtube.com/watch?v=bz93ReOv87Y)

Introduction to Nextflow and workflow management:  

[Nextflow video](https://www.youtube.com/watch?v=wbtMbJTo1xo)
[Nextflow Documentation](https://www.nextflow.io/docs/latest/getstarted.html)

Here are some resources for publically available gene expression data:  

+ for published datasets available through NCBI: [Gene Expression Omnibus (GEO)](https://www.ncbi.nlm.nih.gov/gds/)
+ for tissue specific expression and a GUI to interact with the data: [GTEx Portal](https://gtexportal.org/home/)
+ for cancer specific datasets (with lots of clinical/phenotypic data): [The Cancer Genome Atalas (TCGA)](https://portal.gdc.cancer.gov/exploration?filters=%7B%22op%22%3A%22and%22%2C%22content%22%3A%5B%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.project.program.name%22%2C%22value%22%3A%5B%22TCGA%22%5D%7D%7D%5D%7D) and [the GUI for TCGA data, Xena](https://xena.ucsc.edu/) (you can also upload your own data!)
+ UCSC genome browser allows you to explore gene expression along the genome: [UCSC genome browser](https://genome.ucsc.edu/cgi-bin/hgTracks?db=hg38&lastVirtModeType=default&lastVirtModeExtraState=&virtModeType=default&virtMode=0&nonVirtPosition=&position=chr19:20362090-20371940&hgsid=1712548524_ClekHC2SfK9XMjfyzkayZRNPV8ck)
