# SMS Spam Detection Model

## Overview
A machine learning model to classify SMS messages as **spam** or **ham (legitimate)**. Built using Python and trained on the [SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset), this project demonstrates a complete workflow from data preprocessing to model evaluation. The dataset (`Dataset.csv`) is included in this repository for reproducibility.

## Key Features
- **Data Cleaning**: Handled duplicates, missing values, and irrelevant columns.
- **Text Preprocessing**: Applied tokenization, stopword removal, stemming, and TF-IDF vectorization.
- **Exploratory Data Analysis (EDA)**: Visualized class distribution, text length patterns, and word frequency.
- **Model Comparison**: Evaluated 7 classifiers, including **Naive Bayes**, **Logistic Regression**, and **XGBoost**.

## Dataset
The dataset (`Dataset.csv`) contains **5,572 SMS messages** labeled as `spam` or `ham`.  
**Columns**:  
- `target`: Label (`spam` or `ham`).  
- `text`: Raw SMS message.  

**Example Entry**:  
`"spam", "Free entry in 2 a wkly comp to win FA Cup final tkts..."`

## Technical Approach
1. **Data Preparation**:  
   - Removed duplicates and renamed columns for clarity.  
   - Encoded labels (`spam` → 1, `ham` → 0) using `LabelEncoder`.  
   - Engineered features: `num_chars`, `num_words`, `num_sentences`.  

2. **Text Transformation**:  
   - Cleaned text using regex, stopword removal, and Porter stemming.  
   - Generated TF-IDF vectors with `Scikit-learn` for model input.  

3. **Model Training**:  
   - Split data into **80% training** and **20% testing** sets.  
   - Trained and compared 7 classifiers, focusing on **accuracy** and **precision**.  

## Results
### Model Performance
| Algorithm               | Accuracy | Precision |
|-------------------------|----------|-----------|
| Multinomial Naive Bayes | 97.0%    | 100.0%    |
| Logistic Regression     | 95.6%    | 97.9%     |
| SVM                     | 97.8%    | 97.5%     |
| XGBoost                 | 97.0%    | 95.0%     |
| K-Neighbors             | 90.5%    | 100.0%    | 
| Random Forest           | 97.3%    | 98.2%     |
| Extra Tree Classifier   | 97.8%    | 97.5%     |      

### EDA Insights
- **Class Distribution**: 87.37% ham vs. 12.63% spam .    
- **Word Frequency**: Common spam terms include "free", "text", and "call".  



