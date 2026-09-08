
🚨 Public Information Prioritizer Using Natural Language Processing

Project Overview

The Public Information Prioritizer is an NLP-based system designed to analyze public information such as news articles, emergency alerts, government notices, educational announcements, and promotional messages.

 
The system determines:

  -Information category

  -Crisis status

  -Crisis type
  
  -Urgency level

  -Whether action is required

  -Whether the information is promotional

  -Final priority level

Objectives:

1. Classify news articles into appropriate categories.
2. Detect crisis-related information.
3. Classify the type of crisis.
4. Estimate information urgency.
5. Detect whether action is required.
6. Identify promotional content.
7. Assign a final priority level.
8. Compare different NLP and machine-learning approaches.


Datasets:

News Article Categories Dataset

File: news-article-categories.csv

-Initial records: 6,877

-Records after duplicate removal: 6,849

-Categories: 14

-Fields: Category, Title, Body


The title and body are combined for classification.

Crisis Dataset:

-File: crisis.csv

-Records: 2,345

-Crisis types: 7

-Fields include text, crisis type, relevance, urgency, and informative labels.



Due to repeated texts with inconsistent labels, a group-aware evaluation strategy was used.

Technologies Used:

-Python

-Pandas

-NumPy

-Scikit-learn

-Matplotlib

-Seaborn

-Joblib

-TF-IDF

-Logistic Regression

-Multinomial Naive Bayes

-Rule-Based NLP

Methodology:

The project uses a hybrid NLP approach combining machine learning and rule-based techniques.

Machine Learning:

-TF-IDF for text feature extraction

-Logistic Regression for news-category classification

-Logistic Regression for crisis-type classification

-Multinomial Naive Bayes for model comparison


Rule-Based NLP:

-Crisis detection

-Urgency detection

-Action-required detection

-Promotion detection

-Final priority calculation



Results:

-News Category Classification

Model          	           Accuracy	            Macro F1

Multinomial Naive Bayes	    61.31%             	0.6068

Logistic Regression	        79.27%            	0.7849



Selected Model: TF-IDF + Logistic Regression

Crisis Type Classification:

-Accuracy: 100%

-Macro F1: 1.00

-Test samples: 461



Urgency ML Experiment:

-Accuracy: 32.35%

-Macro F1: 0.30



The ML urgency model was not selected for the final system because of its low performance and inconsistent dataset labels.

Example

Input:

A powerful earthquake has struck the region. Residents must evacuate immediately.

Output:

Crisis Status: Crisis

Crisis Type: Earthquake

News Category: N/A

Urgency: High

Action Required: Yes

Promotion: Not Promotional

Final Priority: Critical



Limitations:

-The crisis dataset contains repeated text with inconsistent urgency and relevance labels.

-The crisis dataset is highly structured.

-Rule-based detection depends on predefined keywords.

-Complex language and context-dependent statements may not always be handled correctly.

-Transformer-based models are not currently used.


Future Scope:

-Use transformer models such as BERT.

-Use larger and more diverse datasets.

-Improve multilingual classification.

-Develop semantic crisis detection.

-Add real-time news and public-alert processing.

-Develop a web or mobile interface.

-Add explainable predictions.

-Project Information


Project Title: Public Information Prioritizer Using Natural Language Processing

Language: Python

Project Type: Mini NLP Project

Architecture: Hybrid Machine Learning + Rule-Based NLP
