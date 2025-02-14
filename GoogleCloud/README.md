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

The below steps guide you through setting up a virtual machine on Google Cloud Platform, downloading our tutorial files, and running those files. 

Accordingly, before starting, make sure you have a google account and have access to a Google Cloud Platform Project.

Once you have these, you can begin by first navigating to https://console.cloud.google.com/ and logging in with your credentials. Then, in the top left of the screen, navigate to 'select a project', and choose the project you belong to.

This tutorial will cost you just less than $3.00 assuming a n1-standard-8 machine, and assuming you delete the virtual machine and the storage bucket after you finish the tutorial. You can save some time by using an n2 machine, but it will cost a little bit more (thought not that much). 

### Creating a user managed notebook 

* **Python Kernel:** Follow the steps highlighted [here](https://github.com/NIGMS/NIGMS-Sandbox/blob/main/docs/HowToCreateVertexAINotebooks.md) to create a new notebook instance in Vertex AI. Follow steps 1-8 and be especially careful to enable idle shutdown as highlighted in step 8. In step 7 in the Machine type tab, select n1-standard-8 from the dropdown box.

* **R Kernel:** (For Tutorial 3) Follow the steps highlighted in the second part (2. Spin up Instance from a Container) of [here](https://github.com/NIGMS/NIGMS-Sandbox/blob/main/docs/HowToCreateVertexAINotebooks.md) to create a new notebook instance in Vertex AI. Follow steps 1-8, in step 5 select region us-east4 (Northern Virgina) and be especially careful to use custom container `us-east4-docker.pkg.dev/nih-cl-shared-resources/nigms-sandbox/nigms-vertex-r` in step 6 under the Docker container image prompt. In step 7 under the Machine type tab, select n1-standard-8 from the dropdown box.

To clone this repository, use the Git command `git clone https://github.com/NIGMS/RNA-Seq-Differential-Expression-Analysis.git` in the dropdown menu option in Jupyter notebook. Please make sure you only enter the link for the repository that you want to clone. There are other bioinformatics related learning modules available in the [NIGMS Repository](https://github.com/NIGMS). This should download our repo, and the tutorial files inside, into a folder called 'RNA-Seq-Differential-Expression-Analysis'. Double click this folder now. Inside you will find all our tutorial files, which you can double click and run.

### Stopping Your Virtual Machine

When you are finished running code, you can turn off your virtual machine to prevent unneeded billing or resource use by checking your notebook and pushing the **Stop** button.

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


