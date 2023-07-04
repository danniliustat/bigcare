# Welcome to the GWAS Workshop

This repository is for CSHL 2023 Summer Course on GWAS analysis.

Speaker: Min Zhang, University of California, Irvine

**Before you start, please download this whole repository to your personal laptop. Click "Code"-> Select "Local" tab-> "Download ZIP". A ZIP file (likely with name "bigcare-main") will be saved to your laptop. Unzip the file to access all datasets and materials.**
![Download](./image/download.png)

### Overview
In this course, we will explore the fundamentals of Genome-Wide Association Study (GWAS) analysis using both toy example datasets and a subsetted dataset from a real-world case study. By the end of this course, we hope you will have a basic understanding of GWAS analysis pipeline and be able to carry out similar analysis using your own data. 

The course is divided into five chapters, starting with the initial overview of the tools and pipeline using toy or example datasets. This section will give you a general idea of the different steps involved in GWAS analysis. The subsequent chapters will focus on the breast cancer case study from GEO. These chapters will provide a hands-on experience of analyzing real-world data.

### Programming Language: 
Throughout this course, we will primarily use the programming languages Bash and R. It is essential that you have a working knowledge of both languages before carrying out your own analysis. Please ensure that you have **RStudio** installed on your laptop to actively participate in the course. 

**Install R and RStudio**: You can download R and RStudio at [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/). Choose the installation files that are suitable for your laptop system. You have to install R before installing RStudio. 

After you launch RStudio, locate the bottom left panel which has two tabs "Console" and "Terminal". We will mainly use these two tabs for our course. "Console" window is used to run R codes and "Terminal" window can access your system shell. For macOS users, "Terminal" can run Bash commands directly. You will start by setting your working directory to the downloaded "bigcare-main" folder by typing: `cd /path/to/bigcare-main` (change this path to where you saved it).
  
However, Windows users need to use another "Powershell" App to run Bash codes because the default system shell language for Windows is Windows commands, which is different from Bash. See notes below.

  
> 👉**Special Notes to Windows Users**:
  Windows has two command-line shells, Command shell and Windows Powershell. Command shell is specific to Windows system and can be run in "Command Prompt" App or in RStudio Terminal. But Windows commands are NOT the same as Bash commands! Powershell App is the only place to run Bash commands for Windows users. For example, Bash codes such as "head" or "awk" can't be recogonized from RStudio Terminal, but can be run from Powershell.

  To open Powershell, search for "Powershell" App in Windows menu.(Don't choose 'Command Prompt'.) You can also find it by pressing "windows+X" key and select "Terminal" in the menu appeared. Test whether you can run bash codes by typing `ls` in the terminal window. Then set your working directory to the downloaded "bigcare-main" folder by typing: `cd /path/to/bigcare-main` (change this path to where you saved it).
  
  
In GWAS analysis, we will also use tools likeyou can **ONLY** run PLINK program codes. If you would like to try Bash codes, please open "Windows Powershell" app and follow the same steps to set the paths. Still, Powershell App won't run PLINK codes, so you'll have to switch between Pwershell and RStudio Terminal.



**Below is the folder structure in this repository**:
- **Five .HTML files started with "1_..." to "5_..."**: These are the course materials with instructions, codes and outputs. Double click on them or drag these files to your browser to open.
  - We will begin with two chapters that provide an overview of the tools and pipeline, using toy or example datasets. These small datasets will allow you to grasp the different steps involved in GWAS analysis. Additionally, these toy examples will enable you to explore the data structure and manipulate the results easily, as they are small and can be easily opened.
  - The remaining chapters 3-5 will delve into a detailed case study on breast cancer, utilizing a dataset downloaded from the Gene Expression Omnibus (GEO). To facilitate running the analysis on a personal laptop, we have subsetted the genotype data to include only 1000 Single Nucleotide Polymorphisms (SNPs).

- **Data**: This folder includes the necessary data files, including the toy example datasets, case study data, and the corresponding results. We will read data and write outputs to this folder.

- **Tools**: This folder contains programs that we will use in our course.
  - The primary tools are **PLINK** and **IMPUTE2**, both of which are integral to GWAS analysis. The installation packages for these tools can be found in this folder. To be able to use them, you will need to unzip the corresponding program ZIP files that is suitable for your laptop system. Specically, PLINK is compatible with Windows, macOS, and Linux, while IMPUTE2 is only available for macOS and Linux users. However, Eigensoft, another software used in chapter 2, can only be executed on a Linux operating system. (Bioinformatics analyses are usually run on computational servers with Linux system given the large data volumn and high computational power required. So most bioinformatic programs are developed under Linux and only some of them are available to run on personal laptops. )
    - To call PLINK or IMPUTE2 from terminal, please run this:
    `cd /path/to/bigcare # change this to where you saved "bigcare-main"
    ./Tools/PLINK/plink/plink_mac_20230116/plink --help # change the path to where PLINK program is saved`
    For macOS users, it will prompt you to authorize the program before running. You should open "Setting"-"Privacy and Security", then scroll to the bottom to click "allow" for PLINK to run. After you allow it, it will ask you a second time in the pop-up window whether you want to open it. Click "Open" to run it. You should see the PLINK options appear in the terminal window.
    
