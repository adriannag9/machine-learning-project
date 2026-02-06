Russian Texts Sentiment Classification
Project Overview
This project aims to classify the sentiment of texts in Russian using classical Machine Learning techniques. The dataset consists of nearly 290,458 records, making it a robust benchmark for evaluating different Natural Language Processing (NLP) workflows.

Tech Stack

Language: Python 3.12

Environment: Google Colab / Jupyter Notebook

NLP Libraries: NLTK, Pymystem3 (Mystem)/Pymorphy2, Scikit-learn

ML Algorithms: Logistic Regression, Linear SVM, Random Forest

Workflow & Key Features
1. Data Cleaning & Analysis
Removed punctuation, special characters, and Russian stop-words to reduce noise.
Performed exploratory data analysis (EDA) on word counts and character lengths.

2. Advanced Lemmatization
Mystem Integration: After comparative testing against Pymorphy2, Mystem was chosen for its better accuracy in handling Russian morphological context (e.g., correctly lemmatizing "могу" to "мочь"). 
Efficiency: Implemented batch processing to handle the large dataset volume efficiently in a cloud environment.

3. Feature Engineering
Used TF-IDF Vectorization with a limit of 5,000 features.
Implemented a linguistic filter (min_df=2) to automatically ignore over 800,000 rare words (Hapax legomena), significantly optimizing model performance and memory usage.

4. Model Training & Evaluation
Evaluated three models using a 75/25 train-test split:
- Logistic Regression: Robust baseline for text classification.
- Linear SVM: Optimized for high-dimensional sparse data.
- Random Forest: Ensemble method for capturing non-linear patterns.
