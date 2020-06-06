---
layout: post
title: Extracting fasta from AUGUSTUS output
date: '2020-06-06'
categories: Code
tags: [bioinformatics, genomics]
---

# Goal: extract extract CDS and protein sequences from first transcript in Augustus output files

[Perl Script](https://github.com/nextgenusfs/augustus/blob/master/scripts/getAnnoFasta.pl)

`perl getAnnoFasta.pl Structural_annotation_abintio.gff`

- this results in 2 files:
 	- Structural_annotation_abintio.aa
 	- Structural_annotation_abintio.codingseq

## Files then need to be parsed for the first transcript only (e.g., g1.t1 ... gn.t1)

`grep -c "# start gene" Structural_annotation_abintio.gff`
### count of genes in gff 64558

`awk '/^>/ {P=index($0,".t1")==0} {if(!P) print} ' Structural_annotation_abintio.aa > Pact_T1_Structural_annotation_abintio.aa`
`grep -c ">" Pact_T1_Structural_annotation_abintio.aa`
### count of genes in fasta 64554
`head Pact_T1_Structural_annotation_abintio.aa`
`tail Pact_T1_Structural_annotation_abintio.aa`
#### last gene name listed g64558.t1
#### 4 protein sequences seem to be missing
#### Is this because some did not generate predicted proteins?


`awk '/^>/ {P=index($0,".t1")==0} {if(!P) print} ' Structural_annotation_abintio.codingseq > Pact_T1_Structural_annotation_abintio.codingseq`
`grep -c ">" Pact_T1_Structural_annotation_abintio.codingseq`
### count of genes in fasta 64558
`head Pact_T1_Structural_annotation_abintio.codingseq`
`tail Pact_T1_Structural_annotation_abintio.codingseq`
#### last gene name listed scaffold159493cov109.g64558.t1
#### sequence counts match for CDS

#### Protein file headers
`grep -e ">" Pact_T1_Structural_annotation_abintio.aa | awk 'sub(/.t1/, "")' | awk 'sub(/>/, "")' > protein.headers`

`grep -e ">" Pact_T1_Structural_annotation_abintio.codingseq | awk 'sub(/.t1/, "")' | sed 's/^[^.]*.//' > CDS.headers`

`diff protein.headers CDS.headers > diffs`

`
1243a1244
> g1244
12721a12723
> g12723
18185a18188
> g18188
48165a48169
> g48169
`

### this adds up to the 4 missing
#### search these 4 in the augustus ouput

`less Structural_annotation_abintio.gff`


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
# Yes we can move forward with this perl script

[Perl Script](https://github.com/nextgenusfs/augustus/blob/master/scripts/getAnnoFasta.pl)
