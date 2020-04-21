## CIPRES
Understanding the evolutionary history of living organisms. 
CIPRES Science Gateway, a web portal designed to provide researchers with transparent access to the fastest available community codes 
for inference of phylogenetic relationships, and implementation of these codes on scalable computational resources.
In an attempt to meet community needs for access to tools and resources for inferring evolutionary relationships, 
the CIPRES (CyberInfrastructure for Phylogenetic RESearch) project created a prototype web portal. 
The CIPRES Portal V 1.0 permitted users to run the community tree inference tools GARLI [9], RAxML [10], PAUP [11], and MrBayes [12], 
both as standalone tools, and with the tool Rec-I-DCM3, a disc covering method to speed and improve inference of large trees [13]. 
The demand for Tree Inference analyses on the CIPRES Portal quickly exceeded the computational resources available to the project, 
pointing to a need to redesign the CIPRES Portal for greater scalability while minimizing costs for the sake of sustainability

## Phylogenetic Reconstruction
Sequences with less than 20 Kbp were discarded (there are a lot of short sequences).
Steps:
mafft --anysymbol sequences > alignment
iqtree -s alignment -alrt 1000 -nt 4
iTOL tree visualization

## Data description
Genome - 

Genes -

Alignment output (whole genome phylogeny) - 

## Implementation
Perl module and dependencies

https://github.com/naturalis/bio-cipres/tree/master/conda/perl-bio-phylo-cipres/v0.2.1

https://github.com/naturalis/bio-cipres/blob/master/lib/Bio/Phylo/CIPRES.pm

Command-line implementation
cipreusrun is ...

- Aligning sequences

Command-line usage:

```
cipresrun \
     -t MAFFT_XSEDE \
     -p vparam.anysymbol_=1 \
     -i <infile> \
     -y cipres_appinfo.yml \
     -o output.mafft=/path/to/outfile.fasta
```


- Inferring trees 

Command-line usage:

```
cipresrun \
    -t IQTREE_XSEDE \
    -p vparam.specify_runtype_=2 \
    -p vparam.specify_dnamodel_=HKY \
    -p vparam.bootstrap_type_=bb \
    -p vparam.use_bnni_=1 \
    -p vparam.num_bootreps_=1000 \
    -p vparam.specify_numparts_=1 \
    -i /path/to/outfile.fasta \
    -y cipres_appinfo.yml \    
    -o output.contree=/path/to/tree.dnd
```







