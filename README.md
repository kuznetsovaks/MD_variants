The 'input' directory contains all the input files and all the files that were updated 
manually and used further in the pipeline (for more details see the pipeline diagram)

The 'source_code' directory contains Python notebooks that can be used to reproduce the pipeline:

1_Reference_Ensembl_table.ipynb - Takes the list of the genes of interest and returns the table 
of all variants in the exons of these genes filtered by the selected consequence types.

2_Pathogenicity_consequences_type_analysis_Ensembl.ipynb - Analyses the distribution of 
pathogenicity within every consequence type in Ensembl and ClinVar. This is used to select
 the consequence types for filtereng.

3_ClinVar_mapping.ipynb - Mapps ClinVar variants associated with MODY, MD and ND to Ensembl
 reference table.

4_Rafique_annotation_mapping.ipynb - Annotates the variants from Rafique et. al, 2021 
supplementary and finds their rs identifiers, mappes them to the Ensembl reference table.

5_Rafique_PubMed_annotation_mapping.ipynb - Annotates the rest of the variants from
 Rafique et. al, 2021 supplementary using their PubMed references and mappes them 
 to the Ensembl reference table. 
 
6_Put_all_together.ipynb - Analyses all the annotated variants and created Venn diagrams 
and rables for VCF.

For creating the VCF files and translation of the sequences to proteins, please, 
use https://github.com/ProGenNo/ProHap.git 

8_Visualization_proteins.ipynb - Takes the variant tables of two levels and a reference 
FASTA from Ensembl and visualises the positions of the variants on the protein sequences 
for all protein isoforms.

7_Visualization_cDNA.ipynb - Takes the variant tables of two levels and a reference 
FASTA from Ensembl and visualises the positions of the variants on the cDNA sequences 
for all the transcripts.

The 'intermediate' directory contains the intermediate tables created by the code.

The 'figures' directory contains the figures created by the code.

