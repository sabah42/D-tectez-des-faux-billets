# Fake Currency Detection Project

## Project Description
This project aims to develop an algorithm for detecting counterfeit banknotes using statistical and machine learning techniques. Given a dataset containing the geometric characteristics of banknotes, we analyze the data and apply clustering, dimensionality reduction, and classification methods to build an effective detection model.

## Project Structure
- `data/` - Contains the dataset used for analysis.
- `notebooks/` - Jupyter notebooks with data exploration, preprocessing, and modeling.
- `src/` - Python scripts for preprocessing, modeling, and evaluation.
- `reports/` - Documentation and summary reports.
- `README.md` - Overview of the project.

## Dataset
The dataset consists of several geometric features of banknotes, including:
- Length of the bill (mm)
- Height of the bill (left and right, mm)
- Top and bottom margin width (mm)
- Diagonal length (mm)
- A label indicating whether the bill is real or fake

## Tools and Libraries
The project utilizes the following tools and libraries:
- **Python**: Programming language for analysis and modeling.
- **Pandas & NumPy**: Data manipulation and numerical operations.
- **Matplotlib & Seaborn**: Data visualization.
- **Scikit-learn**: Machine learning models and evaluation.
- **SciPy**: Statistical analysis and clustering.

## Data Cleaning/Preparation
Before analysis, the dataset undergoes several preprocessing steps:
- Handling missing values (if any)
- Standardizing the numerical features
- Identifying and removing outliers
- Splitting data into training and testing sets

## Analysis Methodology
### Hierarchical Clustering
Hierarchical clustering is applied to identify natural groupings within the dataset before labeling. The clustering dendrogram helps visualize potential separations between real and fake banknotes.

### Principal Component Analysis (PCA)
PCA is used to reduce dimensionality while preserving as much variance as possible. The steps include:
- Eigenvalue scree plot analysis to determine the number of components
- Visualizing correlation between variables
- Projection of data onto principal components

## Key Results/Findings
- PCA reveals that most variance in the data can be captured by a few principal components, enabling efficient dimensionality reduction.
- Clustering techniques show a clear distinction between real and fake banknotes based on geometric properties.
- A logistic regression classifier trained on PCA-transformed data achieves high accuracy in detecting counterfeit bills.

## Recommendations
- Further improvements can be achieved by testing more advanced classification models such as Random Forest or Neural Networks.
- Incorporating additional features such as texture or ink analysis could enhance detection accuracy.
- Deploying the model into a real-time application for use in financial institutions or security agencies.






