# Fake Banknote Detection Project

## Table of Contents

- [Project Description](#project-description)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Tools and Libraries](#tools-and-libraries)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [Analysis Methodology](#analysis-methodology)
  -[Principal Component Analysis (PCA)](#principal-component-analysis-pca)
  - [K-Means Clustering](#k-means-clustering)
  - [K-Nearest Neighbors (KNN)](#k-nearest-neighbors-knn)
  - [Logistic Regression](#logistic-regression)
- [Key Results/Findings](#key-resultsfindings)
- [Recommendations](#recommendations)

## Project Description

This project aims to develop an algorithm to detect counterfeit banknotes using machine learning techniques. The dataset consists of geometric features of banknotes, and the goal is to classify them as genuine or counterfeit.

## Project Structure

- `data/` - Contains raw and processed data.
- [notebooks](./notebooks): contains the jupyter notebook used in the analysis:
- `src/` - Source code for data processing and modeling.
- `results/` - Saved models and evaluation results.
- `README.md` - Project documentation.

## Dataset

The dataset contains the following features:
- length: Length of the banknote (mm)
- height_left: Height (left side) (mm)
- height_right: Height (right side) (mm)
- margin_up: Upper margin (mm)
- margin_low: Lower margin (mm)
- diagonal: Diagonal length (mm)
- is_genuine: Genuine (1) or Counterfeit (0)

## Tools and Libraries

- Python
- Pandas, NumPy (Data Processing)
- Scikit-learn (Machine Learning Models)
- Matplotlib, Seaborn (Visualization)

## Data Cleaning/Preparation

- Handled missing values
- Standardized numerical features
- Split data into training and test sets

## Analysis Methodology

### Principal Component Analysis (PCA)

PCA reduced the dataset to two main components, explaining 69.4% of the variance.

The height_left, height_right, margin_low and length variables are represented by F1.
The diagonal variable is represented by F2.
The margin_up variable is not well represented by either F1 or F2.

### K-Means Clustering
- Used for exploratory data analysis.
- Clustered banknotes into groups based on geometric features: the optimal number of clusters is 3.
- The groups formed by the kmeans algorithm are not suited to our problem.

### K-Nearest Neighbors (KNN)
- Used as a classification model.
- Trained and tested the model on labeled data (80% of the data is used to train the model and the rest to evaluate its performance).
- Evaluated accuracy ( accuracy_KNN_test:94.11%, accuracy_KNN_entrainement: 100% ), precision, and recall.

### Logistic Regression
- Used as a predictive model.
- Estimated the probability of a banknote being genuine.
- Decision threshold set at 0.5 for classification.
- accuracy_KNN_test:98.52%, accuracy_KNN_entrainement: 100% 

## Key Results/Findings

- Logistic Regression provided a high accuracy in detecting fake banknotes.
- KNN performed well but was sensitive to parameter tuning.
- K-Means clustering showed patterns but was not effective for final classification.

## Recommendations

- Improve model accuracy with feature engineering.
- Experiment with other classification models such as Decision Trees or Random Forests.
- Deploy the model for real-time banknote verification.

---
This project demonstrates how machine learning techniques can be applied to fraud detection. Future work includes improving feature selection and exploring deep learning methods. 🚀

