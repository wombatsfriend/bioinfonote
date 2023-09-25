# **note 20230922**

# I. Introduction

## 1) Gene : Coding & Noncoding

### 1.1 why Do Humans Have So Few Genes?

- DNA -> RNA -> protein  /  messenger RNA -> Gene -> Genome
- the largest genome?    
    - human 3 Gbp  /  Amoeba 670 Gbp
    - human 21000 genes / elegans 20000 genes
- coding + noncoding (Canonical ncRNAs, Small ncRNAs, Long ncRNAs)

---

## 2) Method : Sequencing & Computing

### 2.1 Information

- images and sequences
---
### 2.2 Model

- model: A mathematical model is an abstract description of a concrete system using mathematical concepts and language. The process of developing a mathematical model is termed mathematical modeling. (from wikipedia)
- Regression Model: Linear -> Logistic Regression
- Tree Model: Decision Tree -> Random forest
- Neural Network Model -> Deep Learning
---
### 2.3 Algorithm

- algorithm: In mathematics and computer science, an algorithm is a finite sequence of rigorous instructions, typically used to solve a class of specific problems or to perform a computation. Algorithms are used as specifications for performing calculations and data processing. (from wikipedia)
- Number Sorting Algorithm
- Dynamic Programming Algorithm
---

#### *model vs algorithm*

- ***By definition***: A model is an expression that represents a hidden pattern or relationship in the data, and an algorithm is a set of well-defined and well-orderd programs.
- ***By application***: Models can be used to make predictions or reasoning, and algorithms can be used to solve complex problems or complete tasks.
- ***relationship***: A model is the representation of what has already been learned by an algorithm.
---

## 3) Example Studies




# II. Getting Started and Setup

## 1) Document your work

### 1.1 Github

- github / gitee
- repo / `README.md`
- Git

### 1.2 Markdown

- used to write `README.md`
- Good compatibility: HTML friendly / PDF friendly

## 2) Backup your work

### 2.1 Cloud storage: [Tsinghua cloud](https://cloud.tsinghua.edu.cn/)

### 2.2 Backup tool that comes with the system
- Mac: [back up with time machine](https://support.apple.com/en-us/HT201250)
- Win: [back up on win](https://support.microsoft.com/en-us/topic/how-to-back-up-or-transfer-your-data-on-a-windows-based-computer-bd7e1bcf-15ea-078b-922f-6d6fcca76c7e)

### 2.3 Backup your code with GitHub
- Create and edit your repositories (repos.) at [GitHub](https://github.com/) on line.

## 3) How to use Bioinformatics Tutorial

### 3.1 [Teaching Materials](https://book.ncrnalab.org/teaching/appendix/appendix-iv.-teaching)

### 3.2 [Learning Materials](https://book.ncrnalab.org/teaching/appendix/appendix1.keep-learning) 

## 4) Setup

### 4.1 quick start

```
# A Quick Start in Terminal after you installed Docker software in your computer:
docker pull ubuntu # download an image of ubuntu
docker run -i -t ubuntu # run (create) a container of ubuntu
```

### 4.2 Install and Use Docker in Windows

- Setup Windows Subsystem for Linux
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

- update WSL1 to WSL2
    - Download [WSL2 Linux kernel update package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) for x64 machines
```
# enable the Virtual Machine Platform optional feature
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

# Set WSL 2 as your default version
wsl --set-default-version 2
```

- Check the installation
```
docker info
```

- Load a Docker Image
```
docker load -i D:\APPs\docker\images\bioinfo_PartI-PartII-PartIII1-3.tar.gz
```

- Run a container from an Image
```
# Share folder
docker run --name=pangdazhi_linux -dt -h pangdazhi --restart unless-stopped -v D:\APPs\docker\bioinfo_tsinghua_share:/home/test/share xfliu1995/bioinfo_tsinghua:2

# Change access
docker exec -u root pangdazhi_linux chown test:test /home/test/share
```

- Run and exit the container
```
# run
docker exec -it pangdazhi_linux bash

# exit
exit
```



# III. Linux

## 1) linux system

- hardwware
    - device driver
        - kernel
            - system call
                - user application
                - shell
                - GUI

## 2) Shell & Bash

- hardware -> kernel -> shell -> user

## 3) Tips in Bash

- history / Tab / alias / wildcard / bash script 



# **study plan**
# I. Programming Skill
## 1) Weeks 1-5: Linux

- Be able to master basic linux commands and be proficient in using linux systems.
- Understand the basic operating principles of the linux system.
- Master the ability to write bash scripts.
- In my personal scientific research, a large number of sequencing files need to be processed. In the past, I used to manually operate the files one by one. As the number of sequencing samples increased, manual operation became more and more difficult. I want to learn how to *automate batch processing of a large number of sequencing files* using bash scripts.
---
## 2) Weeks 6-16: R

- Master the basic usage of R code.
- I used to use r a little bit, but it was usually just simple commands. I want to master the ability to write *complex loops and complex functions*, simplify my code, and increase the readability of my code.
- The code I have written in the past is not reusable, and often code written for one project is difficult to reuse in another project. I hope to enhance the reusability of my code through learning, making it *more modular, more versatile, and easier to debug*.
---
## 3) Weeks 11-16: Python (optional)

- I have never written python code and would like to understand the basics of python.
- Some sequencing data files are extremely large and time-consuming to process using r code. For example, in my personal scientific research, seurat is relatively slow to process sequencing files, while scanpy is faster. Therefore, I also hope to master some methods of *using python software packages* through learning.
- The sequencing data files of some public data sets are processed and saved by python, and I need to master some methods of processing these files.


# II. NGS Data Analysis

## 1) Weeks 5-11

- Master the basic data *processing flow* of next-generation sequencing
- Be able to independently *process next-generation sequencing files*.
- Be familiar with the use of each parameter of the analysis software, and be able to select the correct parameter according to the actual situation.
- In the past, I may only focus on the smooth operation of pipeline, but now I want to learn as much as possible about the *mathematical principles* behind some software, especially the software algorithms related to single-cell RNA sequencing. For example, how does the mathematical principle of dimensionality reduction, batch removal, and doublet removal work.



# III. Machine Learning

## 1) Weeks 12-16: basics and models

- Able to conduct simple mathematical modeling for research objects.
- I had no previous experience in this area, but I had seen a lot of papers predicting survival from gene expression or gene score. Through learning, I hope to be able to use some biomarkers to build models to predict patient survival.
