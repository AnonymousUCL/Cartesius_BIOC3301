# Cartesius_BIOC3301
Repository of Bash command line batch scripts for the metagenomic analysis of soil samples, run remotely on the Dutch supercomputer, Cartesius, via a Git Bash terminal on a Windows 10 Lenovo ideapad 510 laptop. Map file was downloaded as a tab seperated value (.tsv) file and uploaded to cartesius.

# Workflow of scripts:

  # Analysis Iteration 1:
  
1.  join_paired_ends.pbs
    > Joins forward and reverse sequences.
    Joining paired ends was not possible in previous years. A demonstration of the improved quality of data produced.

2.  split_libraries_fastq.pbs
    > Demultiplexes Fastq sequence data

3.  pick_closed_reference_otus.pbs
    > Produces an OTU table to be used for core diversity analysis and core microbiome
    Closed OTUs were selected as cartesius had issues running denovo and open otu scripts.

4.  closed_core_diversity_analysis.pbs
    > A combination workflow to produce a large number of results, including OTU count, taxonomy, and alpha and beta diversity.
    
    Used to produce fig.8

5.  core_microbiome.pbs
    > Used for group significance statistical tests.

6.  heatmap.pbs

    Used to produce fig.2

At this point processed data was reviewed, it was decided samples 12, 20, and 30 would be excluded from the map file. The map file and scripts were revised with new output directoriesto reflect this second iteration. Scripts were edited directly in the Git Bash terminal using the vim text editor. At this point the second analysis iteration was carried out.

  # Analysis Iteration 2:
  
1.  join_paired_ends.pbs

2.  split_libraries_fastq.pbs

3.  pick_closed_reference_otus.pbs

4.  closed_core_diversity_analysis.pbs

    Used to produce fig.3, 4, 5, 10. Table 1, 2, 3.
    
5.  core_microbiome.pbs

6.  compare_categories_pH.pbs

    Used to produce fig.7
    
    compare_categories_P.pbs
    
    Used to produce fig.7
    
    compare_categories_N.pbs
    
    Used to produce fig.7
    
    compare_categories_K.pbs
    
    Used to produce fig.7
    
7.  groupsig_ph.pbs

    Used to produce fig.6
    
    groupsig_p.pbs
    
    groupsig_n.pbs
    
    groupsig_k.pbs
