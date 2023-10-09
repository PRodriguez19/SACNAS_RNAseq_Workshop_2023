# SACNAS_RNAseq_Workshop_2023

## Description 
This repository has teaching materials for an Introduction to RNA-sequencing data analysis. This unit focuses on teaching basic computational skills to enable the effective use of an high-performance computing environment to implement an RNA-seq data analysis workflow. In addition to running the RNA-seq workflow from FASTQ files to count data, this unit covers best practice guidelines for RNA-seq experimental design and data organization/management.

## Learning Objectives 

1. Understand the necessity for, and use of, the command line interface (bash) and HPC for analyzing high-throughput sequencing data.
2. Understand best practices for designing an RNA-seq experiment and analysis the resulting data.

## Workshop Schedule 
[Workshop schedule](/schedule/README.md)

## Additional Resources

For an overview of bioinformatics, the tools required for RNA-seq analysis and high perfomance computing, see these tutorials (the HPC parts will vary depending on your local cluster):  

    1. [Bioinformatics Training](https://hbctraining.github.io/main/)  
    2. [High Performance Computing](https://jhudatascience.org/Computing_for_Cancer_Informatics/)  
    3. [RNA-seq analysis](https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon-flipped/schedule/links-to-lessons.html)  
    4. [Informatics Technology for Cancer Research Training Network Courses](https://www.itcrtraining.org/resources/courses)  
    5. [R for Data Science](https://r4ds.had.co.nz/introduction.html)  

Need help with Unix?  

    1. [Unix Cheat Sheet](https://www.stationx.net/unix-commands-cheat-sheet/)  
    2. [Vim - command line text editor](https://vim.rtorr.com/)  
    3. [Common commands](https://www.thegeekstuff.com/2010/11/50-linux-commands/)  

Need help with R/RStudio?  

    1. [R/RStudio](https://hbctraining.github.io/Intro-to-R-flipped/schedules/links-to-lessons.html)
    2. [R for Beginners](https://cran.r-project.org/doc/contrib/Paradis-rdebuts_en.pdf) - from CRAN
    3. [Stack Overflow](https://stackoverflow.com/)
    4. [dplyr Cheat Sheet](https://www.rstudio.com/wp-content/uploads/2015/02/data-wrangling-cheatsheet.pdf)
    5. [ggplot2 Cheat Sheet](https://www.maths.usyd.edu.au/u/UG/SM/STAT3022/r/current/Misc/data-visualization-2.1.pdf)

Multiple RNAseq comparisons/ DESeq2:  

    1. [Differential Expression Analysis](https://combine-australia.github.io/RNAseq-R/06-rnaseq-day1.html)  
    2. [Overview](https://hbctraining.github.io/DGE_workshop/lessons/01_DGE_setup_and_overview.html#:~:text=The%20goal%20of%20differential%20expression%20analysis%20is%20to%20determine%2C%20for,observed%20within%20groups%20(replicates).)  

Non-model organisms:  

    1. [Full-length transcriptome assembly from RNA-seq data without a reference genome](https://www.nature.com/articles/nbt.1883)  

FASTQC and multiQC  

    1. [FastQC video](https://www.youtube.com/watch?v=bz93ReOv87Y)

Introduction to Nextflow and workflow management:  

    1. [Nextflow video](https://www.youtube.com/watch?v=wbtMbJTo1xo)
    2. [Nextflow Documentation](https://www.nextflow.io/docs/latest/getstarted.html)

Here are some resources for publically available gene expression data:  

    1. for published datasets available through NCBI: [Gene Expression Omnibus (GEO)](https://www.ncbi.nlm.nih.gov/gds/)
    2. for tissue specific expression and a GUI to interact with the data: [GTEx Portal](https://gtexportal.org/home/)
    3. for cancer specific datasets (with lots of clinical/phenotypic data): [The Cancer Genome Atalas (TCGA)](https://portal.gdc.cancer.gov/exploration?filters=%7B%22op%22%3A%22and%22%2C%22content%22%3A%5B%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22cases.project.program.name%22%2C%22value%22%3A%5B%22TCGA%22%5D%7D%7D%5D%7D) and [the GUI for TCGA data, Xena](https://xena.ucsc.edu/) (you can also upload your own data!)
    4. UCSC genome browser allows you to explore gene expression along the genome: [UCSC genome browser](https://genome.ucsc.edu/cgi-bin/hgTracks?db=hg38&lastVirtModeType=default&lastVirtModeExtraState=&virtModeType=default&virtMode=0&nonVirtPosition=&position=chr19:20362090-20371940&hgsid=1712548524_ClekHC2SfK9XMjfyzkayZRNPV8ck)
