# Machine Learning and Cheminformatics-based Augmentation of Enzymatic Reaction Extraction by Large Language Models
This repository contains a series of Jupyter notebooks that support a research project focused on enhancing biochemical reaction extraction from scientific literature using large language models (LLMs) such as GPT, combined with cheminformatics tools and machine learning techniques.

The workflow includes reaction extraction, name-to-structure conversion, reaction validation using molecular fingerprints and atom mapping, and reaction classification using machine learning models.

## Notebooks Overview
`SMILES Conversion.ipynb`
Converts extracted chemical names into SMILES notation by querying multiple chemical structure databases (PubChem, NCI CACTUS, ChemSpider). This standardizes chemical representations for downstream cheminformatics processing.

`Mining with GPT.ipynb`
Uses GPT-based models to extract enzymatic reactions from scientific literature. Includes querying full-text articles via PMCID from the PubMed Central Open Access Subset.

`Comparing GPT and BRENDA.ipynb`
Compares GPT-extracted reactions with entries from the BRENDA enzyme database, using InChI notation to standardize molecule comparisons and identify matches or discrepancies.

`Atom Mapping, Molecular Fingerprints, and Generating Synthetic Invalid Reactions.ipynb`
Generates synthetic invalid reactions via substrate-product permutation.
Computes molecular fingerprint similarity (MACCS, Morgan, Atom Pair).
Performs atom-to-atom mapping using RXNMapper.
Extracts features used for machine learning-based reaction plausibility classification.

`Decision Trees.ipynb`
Benchmarks random forest models against logistic regression, SVM, and Naive Bayes for classifying valid vs. invalid reactions using the features generated above. Also includes testing the trained models on GPT-extracted reactions.
