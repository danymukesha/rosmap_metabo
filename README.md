# ROSMAP Metabolomics Dataset Analysis

To perform this analysis, I just downloaded 92 files, ~70 MB total unzipped.

This is complete metabolomics dataset from the ROSMAP study (Religious Orders Study /
 Memory and Aging Project), part of the AMP-AD (Accelerating Medicines Partnership - 
Alzheimer's Disease) consortium.

Key Datasets (by Platform/Lab)

Dataset	Tissue	Samples	Platform
4688 (serum p180)	Serum/Blood	~621	Biocrates p180 (FIA + UPLC)
5236 (brain p180)	DLPFC brain	~116	Biocrates p180 (FIA + UPLC)
Baker Lipidomics Blood450	Serum	~369	Baker Heart Institute LC-MSMS
Baker Lipidomics Brain514	Frontal cortex	~504	Baker Heart Institute LC-MSMS
Metabolon HD4 Brain514	DLPFC brain	~521	Metabolon (Q Exactive)
Metabolon Serum450	Serum	~448	Metabolon
Leiden Serum450 (Oxylipins)	Serum	~445	Leiden LC-MSMS
UC Davis Brain514	Frontal cortex	—	LC-MSMS
Emory Lipidomics (M2OVE-AD)	Brain + Plasma	—	Orbitrap Fusion Lumos
Duke Bile Acids	DLPFC brain	—	Biocrates Bile Acids (Xevo TQ-S)

Metabolite Classes Covered

- Biocrates p180: Acylcarnitines, amino acids, biogenic amines, glycerophospholipids, sphingolipids, bile acids, hexosylceramides, phosphatidylcholines

- Baker Lipidomics: Sphingolipids, phosphatidylcholines, lysophosphatidylcholines, phosphatidylethanolamines, cholesterol, bile acids, fatty acids, acylcarnitines, acylglycerols

- Metabolon: Amino acids, carbohydrates, cofactors/vitamins, fatty acids, nucleotides, peptides, xenobiotics, oxylipins, endocannabinoids

- Leiden: Oxylipins, bile acids, endocannabinoids, fatty acids, sphingolipids, lysophospholipids
Clinical / Metadata Files

- ROSMAP_clinical.csv — 3,584 participants with AD diagnosis, age, sex, education, APOE, Braak, CERAD, cognitive scores, PMI

- ROSMAP_biospecimen_metadata.csv — 13,345 specimen records linking individuals to tissues/assays

- ROSMAP_clinical_codebook.pdf — Clinical variable definitions (I couldn't read this PDF in this session)

- Biospecimen/assay metadata for each lab (sample IDs, visit numbers, batch info)
Quality Control Files

- QC data, LOD values, dilution factors, NIST SRM 1950 reference materials, analyte statistics, and tissue weight/volume data for the Biocrates p180 platform

- Recuration reports and data dictionaries for Metabolon

- individualID — Links across clinical, biospecimen, and assay data (e.g., R5676537)

- projid — Study project ID in clinical data

- specimenID — Biospecimen-level identifier (e.g., DUKE-11514)

- visitNumber — Longitudinal visit tracking

Notable Observations

1. Serum + Brain paired design — Same participants profiled in both blood and brain tissue
2. Multiple curation versions — Original and "re-curated" datasets (Aug 2025) for Metabolon data
3. Batch correction applied — Emory lipidomics data is batch-corrected
4. Units vary — Some data in µM, others in peak area, others in normalized relative intensity
5. Synapse-sourced — All files have Synapse IDs; this appears to be an AMP-AD data download
6. Data dictionary files are present for each platform — check the *_DATA DICTIONARY*.csv and *_Dictionary*.csv files for variable definitions
