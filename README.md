1. Put the following input file (you can put more than one) in the working directory:

   tetraploid_EGR2B.fasta

2. Run the following script first

   library(copyseparator)
   sep_assem(copy_number=2,read_length=300,overlap=225, rare_read=10, core_number=7, verbose=1)

You will see the following log on the screen:
   
   
## Begin analyses on: tetraploid_EGR2B.fasta
Total number of reads imported = 25554
Length of the alignment = 886
Read length = 300
Overlap between adjacent subsets = 225
Total number of subsets = 10
Performing clustering analyses for each subset...
Clustering analyses finished
*************************************************************************
Lists of sequences in tetraploid_EGR2B_copies2_overlap225_reduced.txt (if not exist, then its un-reduced form) to be assembled for different gene copies 
Gene_copy_1:  1 3 5 7 9 11 13 15 17 19 
Gene_copy_2:  2 4 6 8 10 12 14 16 18 20 
*************************************************************************
Run finished!
Please check '*_subseqs.fasta' files to see if sequences have been linked correctly. Pay attention to nucleotide overhangs introduced by mistakes.



3. Run the following script to get a histogram "Distance between neighboring variable sites VS. read length.pdf"

   copy_validate("tetraploid_EGR2B_assembled_2_gene_copies.txt",2,300)
