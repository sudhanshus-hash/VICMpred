# VICMpred: SVM-Based Prediction of Functional Proteins of Gram-Negative Bacteria Using Amino Acid Patterns and Composition

VICMpred is a computational web server developed for predicting the major functional classes of Gram-negative bacterial proteins from amino acid sequences.

The tool classifies Gram-negative bacterial proteins into four broad functional categories: virulence factors, information molecules, cellular process proteins, and metabolism-related proteins. VICMpred uses support vector machine-based models trained on amino acid composition, dipeptide composition, and class-specific tetrapeptide patterns.

Web Server: https://webs.iiitd.edu.in/raghava/vicmpred/



## Citation

Saha, S., and Raghava, G. P. S. VICMpred: An SVM-based method for the prediction of functional proteins of Gram-negative bacteria using amino acid patterns and composition. Genomics, Proteomics & Bioinformatics, 4(1), 42-47, 2006.

https://doi.org/10.1016/S1672-0229(06)60015-6

The dataset can be also found on Zenodo https://doi.org/10.5281/zenodo.20281963



## About the Research

Functional annotation of proteins is one of the major challenges in the post-genomic era. Due to the rapid growth of protein sequence databases, experimental functional characterization of every newly discovered protein is not practical.

Traditional methods such as BLAST, FASTA, and PSI-BLAST depend on sequence similarity. However, proteins with similar functions may show poor sequence similarity, making direct function prediction difficult.

VICMpred was developed as a direct function prediction method for Gram-negative bacterial proteins. Instead of only predicting subcellular localization, it predicts broad biological functions directly from protein sequence features.

Data Compilation: The final dataset contained 670 non-redundant Gram-negative bacterial proteins. These included 255 cellular process proteins, 60 information molecules, 285 metabolism proteins, and 70 virulence factors.

Methodology: VICMpred uses support vector machine-based models trained on amino acid composition, dipeptide composition, PSI-BLAST similarity search, class-specific tetrapeptide patterns, and hybrid combinations of these features.



## Key Features

### 1. Functional Protein Prediction

Predictive Modeling: Allows users to submit protein sequences and predict their major functional class.

The tool classifies Gram-negative bacterial proteins into:

- Cellular process proteins
- Information molecules
- Metabolism proteins
- Virulence factors

Amino Acid Composition Model: The amino acid composition-based SVM model achieved 52.39% overall accuracy.

Dipeptide Composition Model: The dipeptide composition-based SVM model achieved 47.01% overall accuracy.

Pattern-Based Model: The tetrapeptide pattern-based SVM model achieved 68.66% overall accuracy.

Hybrid Model: The best hybrid model combining amino acid composition, dipeptide composition, and tetrapeptide pattern information achieved 70.75% overall accuracy.



### 2. Tetrapeptide Pattern-Based Classification

Class-Specific Patterns: VICMpred introduced a tetrapeptide-based approach for protein function classification.

Significant Tetrapeptides: The method identified tetrapeptides that occur significantly more often in each functional class.

The number of significant tetrapeptides identified for each class was:

- Cellular process: 1,248 tetrapeptides
- Information molecules: 381 tetrapeptides
- Metabolism: 1,443 tetrapeptides
- Virulence factors: 1,168 tetrapeptides

Pattern-Based Features: For each query protein, the method counts significant tetrapeptides associated with each functional class and uses these counts as features for SVM classification.

Bias Prevention: Significant tetrapeptides were calculated only from training datasets during cross-validation to avoid prediction bias.



### 3. Integrated Web-Bench

Sequence Submission: Users can submit amino acid sequences using copy-paste or file upload.

Function Prediction: The server predicts whether the submitted protein belongs to cellular process, information molecule, metabolism, or virulence factor class.

SVM-Based Backend: The prediction system uses support vector machine classifiers implemented through SVMlight.

User-Friendly Interface: VICMpred provides an online platform for functional prediction of Gram-negative bacterial proteins from primary sequence.



## Applications

Functional Annotation: VICMpred can help assign broad functional categories to Gram-negative bacterial proteins.

Virulence Factor Prediction: The tool can assist in identifying potential virulence-associated proteins important for host-pathogen interaction studies.

Drug Discovery: Prediction of virulence factors can support identification of possible targets for antibacterial drug development.

Vaccine Research: Virulence-associated proteins predicted by VICMpred may help in preliminary screening of vaccine candidate proteins.

Bacterial Genomics: The tool can support genome annotation and functional analysis of newly sequenced Gram-negative bacterial genomes.

Bioinformatics Research: VICMpred provides a sequence-based machine learning framework for protein function prediction.



## Contact and Authors

Prof. G.P.S. Raghava (raghava@iiitd.ac.in)
Department of Computational Biology, Indraprastha Institute of Information Technology (IIIT Delhi), Okhla Phase III, New Delhi-110020, India.





## Support

This work was supported by the Council of Scientific and Industrial Research and the Department of Biotechnology, Government of India.

Grant Number: CMM-17.
