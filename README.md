# SMS Spam Detection NLP Project

## Project Overview
This project builds a spam/ham SMS classifier using the SMS Spam Collection dataset, containing 5,574 labeled messages collected from free and research-friendly sources. The goal is to accurately distinguish spam messages from legitimate ones.

## Project Steps

### 1. Data Import and Exploration
- Loaded the SMS dataset and inspected its structure.
- Checked class distribution and encoded labels: ham = 0, spam = 1.

### 2. Text Preprocessing
- Cleaned SMS texts by removing usernames, URLs, digits, punctuation, and extra spaces.
- Tokenized texts to keep only meaningful English words, excluding stopwords and gibberish.
- Applied lemmatization to normalize words to their base forms.

### 3. Data Visualization
- Created word clouds to visualize frequent words in spam and ham messages separately.

### 4. Feature Engineering
- Applied TF-IDF vectorization to convert text into numerical features.
- Reduced dimensionality with PCA, choosing 2,100 components to capture most variance.

### 5. Handling Imbalanced Data
- Used RandomOverSampler to balance the minority (spam) class with the majority class.

### 6. Model Training and Selection
- Standardized features and split data into train and test sets.
- Trained and evaluated multiple classifiers: SVC, Logistic Regression, KNN, MultinomialNB, GaussianNB.
- Selected SVC with RBF kernel and C=10 as best performing model.

### 7. Model Evaluation
- Evaluated model performance using accuracy, F1 score, confusion matrix, and detailed classification report.
- Achieved approximately 98% accuracy on the test set.

### 8. Prediction Pipeline
- Developed a function to preprocess new input messages and predict spam or ham using the trained model.

## Usage
- This repo includes scripts for data preprocessing, model training, evaluation, and prediction.
- Can be extended for deployment or integrated into messaging platforms for real-time spam detection.

---
*This README provides a concise overview and stepwise guide to the SMS Spam Detection NLP project.*

