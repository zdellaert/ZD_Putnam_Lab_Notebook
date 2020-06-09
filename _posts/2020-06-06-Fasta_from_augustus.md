---
layout: post
title: Extracting fasta from AUGUSTUS output
date: '2020-06-06'
categories: Code
tags: [bioinformatics, genomics]
---

# Goal: extract extract CDS and protein sequences from first transcript in Augustus output files

##### count of genes in gff 
 	grep -c "# start gene" Structural_annotation_abintio.gff
##### gene count = 64558
#### This matches the reported number from the genome (Vidal Dupiol BioRxiv)

## 1. Use this perl script to extract fasta seq file for AUGUSTUS predicted genes and proteins
[Perl Script](https://github.com/nextgenusfs/augustus/blob/master/scripts/getAnnoFasta.pl)

	perl getAnnoFasta.pl Structural_annotation_abintio.gff

#### this results in 2 files:
`Structural_annotation_abintio.aa`
`Structural_annotation_abintio.codingseq`


## 2. Files then need to be parsed for the first transcript only (e.g., g1.t1 ... gn.t1)

	awk '/^>/ {P=index($0,".t1")==0} {if(!P) print} ' Structural_annotation_abintio.aa > Pact_T1_Structural_annotation_abintio.aa
	
	sed 's/\..*$//' Pact_T1_Structural_annotation_abintio.aa > Pact_protein.fa
	
	awk '/^>/ {P=index($0,".t1")==0} {if(!P) print} ' Structural_annotation_abintio.codingseq > Pact_T1_Structural_annotation_abintio.codingseq
		
	sed '/\..*\./s/^[^.]*\./>/' Pact_T1_Structural_annotation_abintio.codingseq > Pact_CDS.fas

	sed 's/\..*$//' Pact_CDS.fas > Pact_CDS.fa
	
### Output Sequence Files
Pact_protein.fa
Pact_CDS.fa

## 3. Sanity Checks
### count of genes in fasta files
	grep -c ">" Pact_protein.fa
	grep -c ">" Pact_CDS.fa
	
	Pact_CDS.fa = 64558
	Pact_protein.fa = 64554

#### 4 protein sequences seem to be missing from protein
#### Is this because some did not generate predicted proteins?

#### Protein file headers
	grep -e ">"  Pact_protein.fa > protein.headers	
#### CDS file headers
	grep -e ">" Pact_CDS.fa > CDS.headers	
#### Check for differences in the headers
	diff protein.headers CDS.headers > diffs


	1243a1244
	> g1244
	12721a12723
	> g12723
	18185a18188
	> g18188
	48165a48169
	> g48169


### this adds up to the 4 missing
#### search these 4 in the augustus ouput

	less Structural_annotation_abintio.gff


	# start gene g1244
	scaffold97cov102        AUGUSTUS        gene    1       570     0.49    +       .       g1244
	scaffold97cov102        AUGUSTUS        transcript      1       570     0.49    +       .       g1244.t1
	scaffold97cov102        AUGUSTUS        terminal        566     570     0.86    +       2       transcript_id "g1244.t1"; gene_id "g1244";
	scaffold97cov102        AUGUSTUS        intron  1       565     0.49    +       .       transcript_id "g1244.t1"; gene_id "g1244";
	scaffold97cov102        AUGUSTUS        CDS     566     570     0.86    +       2       transcript_id "g1244.t1"; gene_id "g1244";
	scaffold97cov102        AUGUSTUS        stop_codon      568     570     .       +       0       transcript_id "g1244.t1"; gene_id "g1244";
	# coding sequence = [aatga]
	# protein sequence = []
	# Evidence for and against this transcript:
	# % of transcript supported by hints (any source): 50
	# CDS exons: 1/1
	#      E:   1
	# CDS introns: 0/1
	# 5'UTR exons and introns: 0/0
	# 3'UTR exons and introns: 0/0
	# hint groups fully obeyed: 0
	# incompatible hint groups: 3
	#      E:   3 (TCONS00004018,TCONS00060351,TCONS00060352)
	# end gene g1244`


	# start gene g12723
	scaffold991cov108       AUGUSTUS        gene    1       1990    0.4     +       .       g12723
	scaffold991cov108       AUGUSTUS        transcript      1       1990    0.4     +       .       g12723.t1
	scaffold991cov108       AUGUSTUS        terminal        1986    1990    1       +       2       transcript_id "g12723.t1"; gene_id "g12723";
	scaffold991cov108       AUGUSTUS        intron  1       1985    0.4     +       .       transcript_id "g12723.t1"; gene_id "g12723";
	scaffold991cov108       AUGUSTUS        CDS     1986    1990    1       +       2       	transcript_id "g12723.t1"; gene_id "g12723";
	scaffold991cov108       AUGUSTUS        stop_codon      1988    1990    .       +       0       transcript_id "g12723.t1"; gene_id "g12723";
	# coding sequence = [tgtag]
	# protein sequence = []
	# Evidence for and against this transcript:
	# % of transcript supported by hints (any source): 50
	# CDS exons: 1/1
	#      E:   1
	# CDS introns: 0/1
	# 5'UTR exons and introns: 0/0
	# 3'UTR exons and introns: 0/0
	# hint groups fully obeyed: 0
	# incompatible hint groups: 31
	#      E:  31 (TCONS00062974,TCONS00010788,TCONS00024921,TCONS00062723,TCONS00046300,TCONS00008149,...)
	# end gene g12723


	# start gene g18188
	scaffold1507cov106      AUGUSTUS        gene    1       979     0.6     +       .       g18188
	scaffold1507cov106      AUGUSTUS        transcript      1       979     0.6     +       .       g18188.t1
	scaffold1507cov106      AUGUSTUS        terminal        976     979     0.6     +       1       transcript_id "g18188.t1"; gene_id "g18188";
	scaffold1507cov106      AUGUSTUS        intron  1       975     0.71    +       .       transcript_id "g18188.t1"; gene_id "g18188";
	scaffold1507cov106      AUGUSTUS        CDS     976     979     0.6     +       1       transcript_id "g18188.t1"; gene_id "g18188";
	scaffold1507cov106      AUGUSTUS        stop_codon      977     979     .       +       0       transcript_id "g18188.t1"; gene_id "g18188";
	# coding sequence = [ctag]
	# protein sequence = []
	# Evidence for and against this transcript:
	# % of transcript supported by hints (any source): 50
	# CDS exons: 1/1
	#      E:   1
	# CDS introns: 0/1
	# 5'UTR exons and introns: 0/0
	# 3'UTR exons and introns: 0/0
	# hint groups fully obeyed: 0
	# incompatible hint groups: 29
	#      E:  29 (TCONS00047370,TCONS00028284,TCONS00036554,TCONS00012242,TCONS00056347,TCONS00050834,...)
	# end gene g18188


	# start gene g48169
	scaffold9876cov105      AUGUSTUS        gene    1       180     0.99    +       .       g48169
	scaffold9876cov105      AUGUSTUS        transcript      1       180     0.99    +       .       g48169.t1
	scaffold9876cov105      AUGUSTUS        terminal        176     180     0.99    +       2       transcript_id "g48169.t1"; gene_id "g48169";
	scaffold9876cov105      AUGUSTUS        intron  1       175     0.99    +       .       transcript_id "g48169.t1"; gene_id "g48169";
	scaffold9876cov105      AUGUSTUS        CDS     176     180     0.99    +       2       transcript_id "g48169.t1"; gene_id "g48169";
	scaffold9876cov105      AUGUSTUS        stop_codon      178     180     .       +       0       transcript_id "g48169.t1"; gene_id "g48169";
	# coding sequence = [aataa]
	# protein sequence = []
	# Evidence for and against this transcript:
	# % of transcript supported by hints (any source): 50
	# CDS exons: 1/1
	#      E:   1
	# CDS introns: 0/1
	# 5'UTR exons and introns: 0/0
	# 3'UTR exons and introns: 0/0
	# hint groups fully obeyed: 0
	# incompatible hint groups: 25
	#      E:  25 (TCONS00029265,TCONS00001086,TCONS00052623,TCONS00019793,TCONS00046668,TCONS00025937,...)
	# end gene g48169

# Yes, 4 genes did not have predicted proteins

# Yes we can move forward with this perl script, followed by cleaning of sequence names to remove extra header information (e.g., .t1)

[Perl Script](https://github.com/nextgenusfs/augustus/blob/master/scripts/getAnnoFasta.pl)










# Compare this to script written by Tejashree Modak
[August Extract Script by Tejashree Modak](https://github.com/tejashree1modak/AUGUSTUS-helpers/blob/master/get-fasta.sh)


	#!/bin/bash
	PROG="${0##*/}"

	help() {
    echo -e "$PROG [options] <Agustus gff>\n"
    echo "Options:"
    echo "-c <coding file>    Output file for CDS fasta"
    echo "-p <coding file>    Output file for protein fasta"
    exit 0
	}

	while getopts "c:p:h" arg ; do
    case "$arg" in
        c)  cfile="$OPTARG" ;;
        p)  pfile="$OPTARG" ;;
        *)  help ;;
    esac
	done

	shift $((OPTIND-1))

	# pre-process the file to "join" all coding and protein sequences
	# output will be
	# >gene1
	# coding <coding-sequence>
	# protein <protein-sequence>
	# coding <coding-sequence>
	# protein <protein-sequence>
	# ....
	# >gene2
	# ...
	awk '/^# start gene g/ {
    print ">" $NF
    f = ""
	}

	/^# (coding|protein) sequence/ {
    f = $NF
    t = $2
	}

	length(f) && $1 == "#" && NF == 2 {
    f = f $NF
    if ($NF ~ /\]$/) {
        print t, f; f = ""
    }
	} ' $1  | tr -d '[]' > preprocessed

	# after that Pick the gene line and the first two coding and protein lines
	# and write then out
	awk -v pfile="$pfile" -v cfile="$cfile" 'BEGIN {
    pfile = !length(pfile) ? "protein.fasta" : pfile;
    printf "" > pfile
    cfile = !length(cfile) ? "coding.fasta" : cfile;
    printf "" > cfile
	}

	NF == 1 {
    gene = $1
    c = p = 0
	}

	$1 == "coding" && c == 0 {
    print gene "\n" $NF >> cfile
    c++;
	}

	$1 == "protein" && p == 0 {
    if (c == 0) {
        print "WARNING: Protein sequence with no coding sequence for", substr(gene,2), "ignoring.." > "/dev/stderr"
    } else {
        print  gene "\n" $NF >> pfile
        p++;
    }
	} ' preprocessed


## 1. Run extraction script 
	bash get-augustus-fasta.sh Structural_annotation_abintio.gff

## 2. Output Files
coding.fasta
protein.fasta

## 3. Sanity check against sequence number
#### - 64558    

	grep -c ">" coding.fasta
##### 63867

	grep -c ">" protein.fasta
##### 53452

	grep -e ">" coding.fasta | awk 'sub(/>/, "")' > TM_coding.headers
	
	grep -e ">" protein.fasta | awk 'sub(/>/, "")' > TM_protein.headers
		
	diff TM_coding.headers TM_protein.headers > TM_diffs

