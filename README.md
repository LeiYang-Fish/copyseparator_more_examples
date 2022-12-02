1. Put the following input file (you can put more than one) in the working directory:

   tetraploid_EGR2B.fasta

2. Run the following script first

   library(copyseparator)
   sep_assem(copy_number=2,read_length=300,overlap=225, rare_read=10, core_number=7, verbose=1)

3. Run the following script to get a histogram "Distance between neighboring variable sites VS. read length.pdf"

   copy_validate("tetraploid_EGR2B_assembled_2_gene_copies.txt",2,300)
