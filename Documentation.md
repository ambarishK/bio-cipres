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

Alignment output -

