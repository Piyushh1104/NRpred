# NRpred: Classification of Nuclear Receptors Based on Amino Acid and Dipeptide Composition

## Overview

NRpred is a computational method developed for classifying nuclear receptor proteins into their respective subfamilies using Support Vector Machine (SVM)-based machine learning techniques.

The method predicts nuclear receptor subfamilies using:

- Amino acid composition
- Dipeptide composition
- Pseudo-amino acid composition
- Support Vector Machines (SVM)

The study demonstrated that nuclear receptor subfamilies can be accurately classified directly from protein sequences.

Web Server:

http://www.imtech.res.in/raghava/nrpred

---

## Research Paper

**Title:** Classification of Nuclear Receptors Based on Amino Acid Composition and Dipeptide Composition

**Authors:**  
Manoj Bhasin and Gajendra P. S. Raghava

**Journal:** Journal of Biological Chemistry (JBC)

**Volume:** 279  
**Issue:** 22  
**Pages:** 23262–23266

**Published Date:** 28 May 2004

**DOI:**  
https://doi.org/10.1074/jbc.M401932200
https://doi.org/10.5281/zenodo.20136196


---

## Background

Nuclear receptors are important transcription factors involved in:

- Cell growth
- Differentiation
- Homeostasis
- Metabolism
- Development

These receptors regulate pathways associated with major diseases such as:

- Cancer
- Diabetes
- Osteoporosis

Nuclear receptors share a common structural organization containing:

- N-terminal region (A/B domain)
- DNA binding domain (C domain)
- Hinge region (D domain)
- Ligand binding domain (E domain)
- C-terminal region (F domain)

The DNA-binding domain contains zinc finger motifs that are characteristic signatures of nuclear receptors.

---

## Objectives

The study aimed to:

- Classify nuclear receptor proteins into subfamilies
- Develop automated sequence-based prediction methods
- Improve nuclear receptor annotation
- Assist in drug discovery research

---

## Dataset Information

The dataset was collected from:

- NucleaRDB database

### Initial Dataset

- 577 protein sequences

### Final Non-Redundant Dataset

- 282 protein sequences

Redundancy reduction was performed using:

- PROSET software
- Less than 90% sequence identity

Source: :contentReference[oaicite:1]{index=1}

---

## Nuclear Receptor Subfamilies

The method classified receptors into four major subfamilies:

| Subfamily | Examples |
|-----------|-----------|
| Thyroid hormone-like | TR, RAR, ROR |
| HNF4-like | HNF4, RXR, TLL, COUP, USP |
| Estrogen-like | ER, ERR, GR, MR, PR, AR |
| Fushi tarazu-F1-like | SF1, FTF, FTZ-F1 |

---

## Feature Representation

### Amino Acid Composition

Protein sequences were represented using:

- Fraction of 20 amino acids

This generated a fixed-length vector of 20 dimensions.

### Dipeptide Composition

Dipeptide composition captured:

- Amino acid frequency
- Local sequence order

This generated a fixed-length vector of 400 dimensions.

### Pseudo-Amino Acid Composition

The study also evaluated:

- Sequence-order correlated factors
- Hydrophobicity correlation factors

These improved prediction performance.

---

## Machine Learning Approach

The classification models were developed using:

- Support Vector Machines (SVM)
- SVM_light package
- Radial Basis Function (RBF) kernel

Multi-class classification was implemented using:

- One-vs-rest (1-v-r) SVM strategy

Source: :contentReference[oaicite:2]{index=2}

---

## Model Evaluation

Performance evaluation was performed using:

- Five-fold cross-validation

Evaluation parameters included:

- Accuracy
- Matthew’s Correlation Coefficient (MCC)
- Reliability Index (RI)

---

## Amino Acid Composition Performance

### Overall Performance

- Accuracy: 82.6%
- MCC: 0.74

### Subfamily Accuracy

| Subfamily | Accuracy |
|-----------|-----------|
| Thyroid hormone-like | 87.7% |
| HNF4-like | 68.0% |
| Estrogen-like | 89.3% |
| Fushi tarazu-F1-like | 80.9% |

Source: :contentReference[oaicite:3]{index=3}

---

## Dipeptide Composition Performance

The dipeptide composition model significantly improved performance.

### Overall Performance

- Accuracy: 97.5%
- MCC: 0.96

### Subfamily Accuracy

| Subfamily | Accuracy |
|-----------|-----------|
| Thyroid hormone-like | 100% |
| HNF4-like | 95.8% |
| Estrogen-like | 98.7% |
| Fushi tarazu-F1-like | 85.3% |

Source: :contentReference[oaicite:4]{index=4}

---

## Pseudo-Amino Acid Composition

The study evaluated sequence-order information using pseudo-amino acid composition.

### Best Performance

- Accuracy: 90.7%
- MCC: 0.86

The best results were obtained using:

- 30th rank sequence-order correlated factors

---

## Reliability Index (RI)

A reliability index was introduced to estimate prediction confidence.

### Important Observation

For sequences with:

- RI ≥ 3

Prediction accuracy approached nearly:

- 100%

Source: :contentReference[oaicite:5]{index=5}

---

## Important Findings

The study demonstrated that:

- Nuclear receptor subfamilies correlate strongly with sequence composition
- Dipeptide composition performs better than amino acid composition
- Sequence-order information improves classification
- SVM-based methods are highly effective for nuclear receptor classification

---

## Web Server Features

The NRpred server allows users to:

- Submit protein sequences
- Predict nuclear receptor subfamilies
- Choose prediction methods
- Obtain reliability index scores
- View expected prediction accuracy

Input formats supported:

- FASTA
- EMBL
- GCG
- Plain text

Source: :contentReference[oaicite:6]{index=6}

---

## Technologies Used

- SVM_light
- Perl CGI
- Solaris Server
- Readseq
- Radial Basis Function Kernel

---

## Applications

NRpred can be used for:

- Nuclear receptor classification
- Functional annotation
- Genome annotation
- Drug target discovery
- Hormone receptor studies
- Computational biology research

---

## Availability

Web Server:

http://www.imtech.res.in/raghava/nrpred

---

## Contact

### Prof. Gajendra P. S. Raghava

Department of Computational Biology  
Indraprastha Institute of Information Technology Delhi  
New Delhi, India

Email: raghava@iiitd.ac.in

---

## License

Open Access under CC BY License

---

## Source

Generated from the uploaded NRpred research paper. :contentReference[oaicite:7]{index=7}
