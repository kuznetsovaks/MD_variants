# Monogenic diabetes associated variants
A systematic mapping of the genomic and proteomic variation associated with monogenic diabetes

![alt text](https://github.com/kuznetsovaks/MD_variants/blob/ed7c7e8cf9e948b452dac5935c6c44213d1d5ef6/figures/mindmap.png?raw=true)

The `input` directory contains all the input files and all the files that were updated 
manually and used further in the pipeline (for more details see the pipeline diagram)

The `source_code` directory contains Python notebooks that can be used to reproduce the pipeline:

 - `1_Reference_Ensembl_table.ipynb` - Takes the list of the genes of interest and returns the table 
of all variants in the exons of these genes filtered by the selected consequence types.
 - `2_Pathogenicity_consequences_type_analysis_Ensembl.ipynb` - Analyses the distribution of 
pathogenicity within every consequence type in Ensembl and ClinVar. This is used to select
 the consequence types for filtereng.
 - `3_ClinVar_mapping.ipynb` - Mapps ClinVar variants associated with MODY, MD and ND to Ensembl
 reference table.
 - `4_Rafique_annotation_mapping.ipynb` - Annotates the variants from Rafique et. al, 2021 
supplementary and finds their rs identifiers, mappes them to the Ensembl reference table.
 - `5_Rafique_PubMed_annotation_mapping.ipynb` - Annotates the rest of the variants from
 Rafique et. al, 2021 supplementary using their PubMed references and mappes them 
 to the Ensembl reference table. 
 - `6_Put_all_together.ipynb` - Analyses all the annotated variants and created Venn diagrams 
and rables for VCF.
 - For creating the VCF files and translation of the sequences to proteins, please, 
use [ProVar](https://github.com/ProGenNo/ProHap.git)
 - `7_Visualization_proteins.ipynb` - Takes the variant tables of two levels and a reference 
FASTA from Ensembl and visualises the positions of the variants on the protein sequences 
for all protein isoforms.
- `MD_variants.yml` - is a file that can be used to create the conda environment for running the pipeline.

The `intermediate` directory contains the intermediate tables created by the code.

The `figures` directory contains the figures created by the code.

The `results` directory contains final variant tables of two levels. The final fasta files with the translated protein sequences can be accessed on [figshare.com](https://figshare.com/articles/dataset/Results_fasta_files_for_A_systematic_mapping_of_the_genomic_and_proteomic_variation_associated_with_monogenic_diabetes_/21444963)

The `HCS` directory contains the example of reproduction of the pipeline on Hajdu-Cheney syndrome (HCS).

