---
layout: post
title: Testing HoloInt ITS2 Amps
date: '2019-12-23'
categories: HoloInt
tags: [ITS2, DNA, Amplicon, bioinformatics]
---




# Running SymPortal

## Create the env as a python 3.6 environment

conda create -n symportal_python python=3.6

## Activate the environment (it can be deactivated with ‘conda deactivate’)

conda activate symportal_python

## Use GitHub to download latest version

git clone https://github.com/didillysquat/SymPortal_framework.git
cd SymPortal_framework

## Then install the remaining python packages

python3 -m pip install numpy==1.17.1
python3 -m pip install biopython==1.71
python3 -m pip install Django==2.2.4
python3 -m pip install matplotlib==2.0.2
python3 -m pip install -r requirements.txt

## Install other dependencies

conda install mothur==1.39.5 (needs version 1.39.5)
conda install mafft
conda install iqtree

## Then follow steps 2a, 2b, and 4 from here:
[SymPortal]https://github.com/didillysquat/SymPortal_framework/wiki/SymPortal-setup


## Test

which mothur
~/miniconda3/envs/symportal_python/bin/mothur

which blastn
/usr/local/bin/blastn

which makeblastdb
/usr/local/bin/makeblastdb

which mafft
~/miniconda3/envs/symportal_python/bin/mafft

which iqtree
~/miniconda3/envs/symportal_python/bin/iqtree


blastn -version
blastn: 2.2.31+
Package: blast 2.2.31, build Jun 12 2018 14:50:12

makeblastdb -version
makeblastdb: 2.2.31+
Package: blast 2.2.31, build Jun 12 2018 14:50:12

mafft --version
v7.455 (2019/Dec/7)


# Running on the 14 HoloInt Test samples
[HoloInt ITS2 Sample Preparation ](https://emmastrand.github.io/EmmaStrand_Notebook/16s,-ITS2,-23s-PCR-Protocol-Testing/)



# Activate Program

conda activate symportal_python

# Load Data

./main.py --load ../ITS2/ --name first_loading --num_proc 3 --data_sheet /home/hputnam/Sym/SymPortal_datasheet_20191223.xlsx

# Running Analysis

./main.py --analyse 1 --name first_analysis --num_proc 3




