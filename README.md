# CHYRON1
Code associated with "Ordered insertional mutagenesis at a single genomic site enables lineage tracing and analog recording in mammalian cells."

We used a simple wrapper to feed the necesary information into pipeline.sh:
$1 = the path to the forward read fastq file
$2 = the path to the reverse read fastq file
$3 = the path to the barcode file with the following format:
	"Sample name"	"forward barcode"	"reverse barcode"	"20bp around cutsite"	"Experiment"
$4 = the path to the reference sequence, with the format:
	"Experiment name"	"reference sequence"
$5 = The name of the experiment, for file naming purposes

You'll need to download:

PEAR, to pair Paired-End Illumina reads: https://sco.h-its.org/exelixis/web/software/pear/

And then compile:

Mapp, an optimal sequence alignment used in Perli et al, 2016. The C++ code is available at: http://www.rle.mit.edu/sbg/resources/stgRNA/
Follow the link to the C++ routine for Implementation of the optimal sequence alignment using affine gap costs by Altschul S.F. and Erickson B.W (1986).

References:
I) Perli, S. D., Cui, C. H. & Lu, T. K. Continuous genetic recording with self-targeting CRISPR-Cas in human cells. Science 353, aag0511 (2016).
II) Zhang, J., Kobert, K., Flouri, T. & Stamatakis, A. PEAR: a fast and accurate Illumina Paired-End reAd mergeR. Bioinformatics 30, 614–620 (2014).
The code was written by Elmira Forouzmand and Mason Schechter. We used Enthought Python 7.3.2 and Python 2.7.15

