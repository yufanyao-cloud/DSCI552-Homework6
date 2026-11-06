# Homework 6 - Tree-Based Methods

**USC ID:** 1450125536  
**Name:** Yufan Yao  
**GitHub:** yufanyao-cloud

## Contents

- `notebook/Homework6_Tree_Based_Methods.ipynb`: APS Failure analysis and required ISLR 6.6.3, 6.6.5, 8.4.5, and 9.7.3 answers.
- `data/`: local APS training/test CSV files and description (not committed because the training CSV exceeds GitHub's recommended file-size limit).

## Data setup

Download and unzip the course-provided **Homework 6 Data** archive. Create a
`data/` folder in the repository root and place these files inside it:

```text
data/
├── aps_failure_training_set.csv
├── aps_failure_test_set.csv
└── aps_failure_description.txt
```

The `data/` folder is listed in `.gitignore`, so the large CSV files remain
available for local execution but are not uploaded to GitHub.

## Run

```bash
pip install -r requirements.txt
jupyter notebook notebook/Homework6_Tree_Based_Methods.ipynb
```

Run all notebook cells from top to bottom. The original APS CSV layout contains 20 text lines before its header; the notebook handles this using `skiprows=20`. Results are intentionally generated at run time rather than hard-coded.

## Method notes

- Median imputation is fit using training data only.
- Random Forest is evaluated both without class compensation and with `class_weight="balanced"`.
- SMOTE is placed inside the cross-validation pipeline to avoid resampling validation/test observations.
- Homework questions marked “Extra Practice” are not part of the required notebook.
