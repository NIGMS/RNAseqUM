# Maine INBRE Google Cloud Training Tutorials



## Table of Contents

[Overview](#overview)  
[Getting Started](#getting-started)  
[Workflows](#workflows)  
   
## Overview

Included here are several tutorials in the form of 'Jupyter notebooks'.

The purpose of these tutorials is to help users familiarize themselves with the cloud computing in the specific context of running bioinformatics workflows. Here is a link to a [YouTube video](https://youtu.be/3ie420Luorc) that gives you an overview of the tutorials.

These tutorials do this by going step-by-step through specific workflows. These workflows cover the start to finish of basic bioinformatics analysis; starting from downloading raw sequence data, and extending to differential gene expression analysis, and producing common plots in R.


## Getting Started

This repository contains several notebook files which serve as bioinformatics workflow tutorials.

The below steps guide you through setting up a notebook instance on Amazon SageMaker AI, downloading our tutorial files, and running those files. 

Accordingly, before starting, make sure you have an Amazon account and have access to it.

Once you have these, you can begin by first navigating to https://aws.amazon.com/ and logging in with your credentials. Then, in the top left of the screen, search for 'SageMaker AI'.

This tutorial will cost you just less than $3.00 assuming a ml.m5.2xlarge notebook instance, and assuming you delete the notebook and the storage bucket after you finish the tutorial. You can save some time by using an ml.m6i.2xlarge instance, but it will cost a little bit more (thought not that much). 

### Creating a notebook instance 

Follow the steps highlighted [here](https://github.com/NIGMS/NIGMS-Sandbox/blob/main/docs/HowToCreateAWSSagemakerNotebooks.md) to create a new notebook instance in Amazon SageMaker. 

+ In step 4, select ml.m5.2xlarge from the dropdown box as the notebook instance type and be especially careful to **enable idle shutdown**.

+ In step 7, after creating a notebook instance and being in JupyterLab screen you will need to download the module content. The easiest way to do this is to clone the repository directly for the NIGMS Github. This can be done by clicking on git symbol in your JupyterLab environment and pasting the following URL `https://github.com/NIGMS/RNA-Seq-Differential-Expression-Analysis.git`. This should download our repo, and the tutorial files inside, into a folder called 'RNA-Seq-Differential-Expression-Analysis'. Double click this folder now. Inside you will find all of the tutorial files, which you can double click and run. You should also see a data file that contains the biomarker and proteomic data to be analyzed.

+ In step 8, you select a Kernel for the notebook. Select R kernel for Tutorial 3 and python for the rest of notebooks. 

+ When you are finished running code, stop your notebook to prevent unneeded billing as illustrated in step 9.

## Workflows

Our tutorials are broken down into 'workflows'. Each notebook file covers a specific workflow, which contains written and visual commentary, as well as the actual step-by-step code for running that workflow analysis. 

These notebooks were designed to be run using a virtual machine on a cloud computing provider. For more information on how to do this; navigate to the [Getting Started](#getting-started) section. Feel free to explore and run the workflows in any order you like. 

![RNA-Seq workflow](images/RNA-Seq_Notebook_Homepage.png)


**[Workflow One](Tutorial_1.ipynb):** A short introduction to downloading and mapping sequences to a transcriptome using Trimmomatic and Salmon. Here is a link to the YouTube video demonstrating the tutorial: <https://youtu.be/ChGfBR4do_Y>.

**[Extended Workflow One](Tutorial_1B_Extended.ipynb):** An extended version of workflow one. Once you have got your feet wet, you can retry workflow one with this extended version that covers the entire dataset, and includes elaboration such as using SRA tools for sequence downloading, and examples of running batches of fastq files through the pipeline. This workflow may take around an hour to run.

**[Workflow One (Using Snakemake)](Tutorial_2_Snakemake.ipynb):** Using Snakemake to run workflow one.

**[Workflow Two (DEG Analysis)](Tutorial_3_DEG_Analysis.ipynb):** Using Deseq2 and R to conduct clustering and differential gene expression analysis.

**[Workflow three (Using Snakemake with Life Sciences API)](Tutorial_4_Snakemake_LS_API.ipynb):** Using Snakemake to run workflow three.

**[Workflow three (Using Nextflow and Google Batch)](Tutorial_4_Nextflow_GBatch.ipynb):** Using Nextflow to run workflow three.

**[Bonus](Tutorial_5_BonusNotebook.ipynb):** Test your knowledge by filling in the blanks for key Cloud and bioinformatic tasks learned in the other submodules.


