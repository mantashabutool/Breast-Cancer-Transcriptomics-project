# Breast Cancer Subtype Classification Using Gene Expression Data

An independent bioinformatics and machine learning project exploring whether gene expression profiles can be used to classify recorded breast cancer sample subtypes.

## Project Overview

Breast cancer is a heterogeneous disease with distinct molecular characteristics. In this project, I explored the GSE45827 gene expression dataset from the NCBI Gene Expression Omnibus (GEO) database.

Using Python, I organized and prepared the gene expression data and trained a Random Forest classifier to classify samples into their recorded classes.

The main purpose of this project was to learn how biological datasets can be handled computationally and to explore how machine learning can be applied to transcriptomic data.

## Objectives

- Load and preprocess a public breast cancer gene expression dataset.
- Extract the recorded sample class labels.
- Prepare gene expression data for machine learning.
- Train a Random Forest classification model.
- Evaluate classification performance using multiple metrics.
- Examine which features contribute to the model's classification.

## Dataset

**Dataset:** GSE45827  
**Source:** NCBI Gene Expression Omnibus (GEO)  
**Platform:** Affymetrix Human Genome U133 Plus 2.0 Array  
**Samples:** 155  
**Expression features:** 29,873  
**Recorded classes:** 6

The six recorded classes in the dataset are:

- Basal
- HER2
- Luminal A
- Luminal B
- Normal
- Cell Line

## Methodology

The analysis followed these main steps:

1. Loaded the public GEO expression dataset.
2. Prepared the expression matrix and sample labels.
3. Separated the features from the target labels.
4. Split the data into training and testing sets.
5. Trained a Random Forest classifier.
6. Generated predictions for the held-out test set.
7. Evaluated the model using accuracy, precision, recall, and F1-score.
8. Performed 5-fold cross-validation.
9. Examined Random Forest feature importance.

## Machine Learning Model

A **Random Forest classifier** was used for the classification task.

Random Forest combines multiple decision trees to make predictions and can be useful for exploring high-dimensional datasets such as gene expression data.

## Results

The Random Forest classifier achieved:

- **Test-set accuracy:** 100%
- **5-fold cross-validation mean accuracy:** approximately 97.4%

The classification report showed strong performance across the recorded sample classes in the held-out test set.

These results indicate that the expression profiles in this particular dataset contain patterns that can distinguish the recorded classes.

However, the results should be interpreted within the scope of this dataset and evaluation setup and should not be considered evidence of clinical diagnostic performance.

## Feature Importance

Random Forest feature importance was examined to identify expression features that contributed strongly to the model's predictions.

These features represent predictive importance within the trained model. They do not, by themselves, establish that a particular gene or feature causes a biological difference between cancer subtypes.

## Limitations

- The dataset contains only 155 samples.
- The analysis uses a single public dataset.
- The model was evaluated using a train-test split and cross-validation rather than an independent external dataset.
- External validation on an independent dataset was not performed.
- Feature importance does not establish biological causality.
- The model is intended for educational and exploratory analysis and is not a clinical diagnostic tool.

## Future Work

Possible extensions of this project include:

- Testing the model on independent datasets.
- Comparing Random Forest with other machine learning approaches.
- Performing differential gene expression analysis.
- Investigating biological pathways associated with informative features.
- Exploring additional visualization and dimensionality-reduction techniques.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Google Colab

## Skills Explored

- Bioinformatics
- Transcriptomic data analysis
- Data preprocessing
- Machine learning
- Scientific visualization
- Computational biology
- Python programming

## Repository Contents

- `Breast_Cancer_Subtype_Classification.ipynb` — analysis notebook containing the data processing, machine learning workflow, evaluation, and feature-importance analysis.

## Disclaimer

This is an independent educational project using publicly available data. The model is intended for learning and exploratory analysis and is **not a clinical diagnostic system**.

---

*This project was developed as part of my self-learning journey into bioinformatics and computational biology.*
