# Fruit Classification from Images 🔍

This program focuses on feature selection and classification using various machine learning techniques. It demonstrates the process of identifying relevant features, reducing dimensionality, and building a classification model.

## Setup and Data Loading 📥

The program requires the following dependencies to be installed:

- `scikit-learn` library (`sklearn`)
- `pandas` library (`pd`)
- `numpy` library (`np`)
- `matplotlib` library (`plt`)

The provided code performs the following steps:

1. Import the necessary libraries and modules.
2. Load the training and test data from CSV files (`train.csv` and `test.csv`). <br> You can download train.csv from here : https://drive.google.com/file/d/1jx7a6tw_kGvj0s5pYsmj2AJ5l6um-Oan/view?usp=sharing
3. Separate the target variable (`category`) from the features in the training data.
4. Convert the data into NumPy arrays for further processing.

## Feature Engineering and Preprocessing 🔧

The code includes optional feature engineering and preprocessing steps that are commented out by default. You can uncomment and modify these steps as needed. The provided code includes the following preprocessing techniques:

- Feature Engineering: Uncommented code to perform feature engineering by applying mathematical operations to the features.
- Standardization: Code to standardize the data using z-score normalization.

## Outlier Detection and Removal 🚫📊

The code uses the Local Outlier Factor (LOF) algorithm to detect and remove outliers from the training data. The following steps are performed:

1. Create an instance of the LOF algorithm with specified parameters.
2. Fit the LOF algorithm on the training data.
3. Identify outliers using the `fit_predict` method.
4. Remove outliers from both the feature matrix and target variable.

## Feature Selection using Correlation 📈🎯

The code calculates the correlation matrix of the remaining features after outlier removal. It performs the following steps:

1. Calculate the correlation matrix using NumPy's `corrcoef` function.
2. Extract the correlations between the features and the target variable.
3. Sort the correlations in descending order to identify the top n features.
4. Print the top n features based on their correlation with the target variable.

## Dimensionality Reduction using PCA and LDA 📉🔍

The code applies Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA) for dimensionality reduction. It includes the following steps:

1. Configure the desired number of components to keep or the desired explained variance ratio for PCA.
2. Create instances of PCA and LDA with the specified parameters.
3. Fit PCA on the training data after outlier removal and transform both the training and test data.
4. Print the shape of the transformed training data and the variance explained by PCA.
5. Fit LDA on the transformed training data and transform both the training and test data.
6. Print the shape of the transformed training data and the variance explained by LDA.

## Ensemble Classification using Voting Classifier 🤝✅

The code demonstrates ensemble classification using the Voting Classifier algorithm. It performs the following steps:

1. Create multiple instances of Logistic Regression classifiers with different hyperparameters.
2. Create a Voting Classifier with the logistic regression classifiers as estimators and specify the voting strategy and weights.
3. Fit the Voting Classifier on the transformed training data.
4. Predict the class labels for the transformed test data.
5. Evaluate the accuracy of the ensemble model (commented out).
6. Save the predictions to a CSV file (`submission.csv`) in the required format.

Please note that some code sections are commented out and may need to be uncommented and modified based on your specific needs.

Feel free to modify and experiment with the code to explore different feature selection techniques, classification algorithms, and preprocessing steps. If you encounter any issues or have any questions, please let us know.
