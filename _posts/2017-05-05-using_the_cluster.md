# Using the cluster

* Open the terminal 
* ssh into the cluster
* ssh username@seawulf.uri.edu
* ```qsub -I``` = submitting an interactive job
 	- Don't work on the head node... make sure you are in an interactive session
* ```qsub -I -l nodes=1:ppn=2 -lwalltime=2:00:00``` = set job walltime and number of nodes

## Typing on the command line
* ```pwd``` = print working directory
* ```ls``` = list
* ```ls /home/shared/genomes``` = shared home data for example data
* ```history``` = lists all previous command 
* ```!50``` = will repeat 50th command in history list
* ```control-a``` =beginning of line
* ```ls -l``` = all
* ```ls -lh``` = all info human readable
* keep large datafiles in storage. home directories are space limited.
	- may need to ask to get storage folders set up
* ```cd -``` goes back to prior directory
* ```q``` = releases from less back to the prompt
* ```head -10``` = views first 10 lines
* ```head -900 hg38.fa | tail ``` = views first 900 lines and pipes it to view tail 
* ```grep ">" hg38.fa``` = prints all instances of chr in the terminal
* ```grep ">" hg38.fa > number.name.of.chromosomes.txt``` = send the grep output to a new file
* ```mkdir``` = make directory
* typing ```man``` before a command gives you the manual or help page with all options
* ```mv filename /home/username/bridging_wrkshps``` = moves a file to a new folder, or moves it and changes the name if you change the filename
* ```module avail``` = list of programs installed on the cluster, include a letter after the command to see all programs starting with that letters
* ```module load program.name``` = load a specific program
* ```module list``` = shows the loaded programs
* use ```nano``` to generate a txt file
* ```scp filename username@seawulf.uri.edu:bridging_wrkshps```= uploading file to cluster 

## Setting up scripts
* ```nano runbowtie.sh``` = opens nano and names the new nano file as a shell script (.sh)
* add shebang line
* ```#!/bin/bash```
* follow with cluster job info
```#!/bin/bash```
```#PBS -l walltime=5:00:00```
```#PBS -l nodes=2:ppn=16```
* load modules 
```#load modules```
```module load Bowtie2/2.2.9-foss-2016b```
```#run bowtie```
```#-p = processors```
```#-x = reference genome```
```bowtie2 -p 32 -x /home/shared/genomes/fastq/hg38 \
 -1 /home/shared/genomes/fastq/donor1/lane1/dc_buffy_24h_dengue_CTTGTA.R1.fastq.gz \
 -2 /home/shared/genomes/fastq/donor1/lane1/dc_buffy_24h_dengue_CTTGTA.R2.fastq.gz \
 > bowtie_mapping.out```

* ```qsub runbowtie.sh``` = submit file to queue
* ```qstat``` = queue statistics

* $1 = argument 1






