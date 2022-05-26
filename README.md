# copyseparator_more_examples

# 1. Run the following script first
copy_separate("tetraploid_EGR2B.fasta", 2,300)

# 2. check the alignment file "tetraploid_EGR2B_combined_consensus_2copies_overlap225.txt" and then run the following script
copy_assemble("tetraploid_EGR2B_combined_consensus_2copies_overlap225.txt",2)

# 2. run the following script to get a plot "Distance between neighboring variable sites VS. read length.pdf"
copy_validate("All_final_copies.fasta",2,300)
