# SMS Spam Detection Model

## Overview
A machine learning model built to classify SMS messages as **spam** or **ham (legitimate)** using the [SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset). This project demonstrates an end-to-end workflow for text classification, including data preprocessing, feature engineering, and model evaluation.

## Key Features
- **Text Preprocessing**: Cleaned raw text data using `NLTK` for **tokenization**, **stopword removal**, and **lemmatization**.
- **Feature Engineering**: Transformed text into numerical features using **TF-IDF vectorization**.
- **Model Training & Evaluation**: Compared performance of multiple classifiers (e.g., Naive Bayes, Logistic Regression, SVM) and validated results using a **train-test split**.
- **Performance Metrics**: Achieved strong results with **accuracy, precision, recall, and F1-score** to address class imbalance.

## Dataset
The dataset contains **5,574 SMS messages** labeled as `spam` or `ham`.  
**Example Entry**:  
`"spam", "Free entry in 2 a wkly comp to win FA Cup final tkts 21st May 2005..."`

## Technical Approach
1. **Data Preprocessing**:  
   - Removed special characters and normalized text.  
   - Applied tokenization and stopword removal using `NLTK`.  
   - Converted text to TF-IDF vectors using `Scikit-learn`.  

2. **Model Development**:  
   - Trained and evaluated **Naive Bayes, Logistic Regression, and SVM** classifiers.  
   - Used **stratified train-test split** to maintain class distribution.  

3. **Evaluation**:  
   - Reported **accuracy, precision, recall, and F1-score** for each model.  
   - Analyzed results using a confusion matrix (optional: add image if available).  

