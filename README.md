# Arabic Hate Speech Detection Using AraBERT v2

An Arabic NLP project focused on detecting hateful and offensive content using transformer-based deep learning.
The project compares a traditional machine learning baseline using TF-IDF and Logistic Regression with AraBERT v2 to evaluate the impact of contextual language models on Arabic hate speech detection.

## About the Project

The project was developed as a binary text classification system for identifying hateful and non-hateful Arabic content.
Arabic text was cleaned and normalized before training. A traditional TF-IDF and Logistic Regression model was first implemented as a baseline then AraBERT v2 was fine-tuned on the same classification task for performance comparison.

## Dataset
The dataset is highly imbalanced so balanced class weights were used in the baseline model to give more importance to the minority hateful class. Precision Recall and F1-score were also considered alongside Accuracy for a more reliable evaluation. 
The project uses the Arabic Hate Speech Superset dataset containing 449,078 Arabic social media samples.
- Non-hateful: 432,532 samples
- Hateful: 16,546 samples
- Total: 449,078 samples

The dataset is highly imbalanced so Precision Recall and F1-score were considered alongside Accuracy when evaluating model performance.

<img width="646" height="430" alt="image" src="https://github.com/user-attachments/assets/781c1f74-0559-4493-8c7a-c86d70a1588e" />

## Text Preprocessing

Arabic text was prepared through several preprocessing steps:
- URL and emoji removal
- Punctuation and special character removal
- Arabic text normalization
- Empty sample removal
- Label encoding

<img width="546" height="760" alt="image" src="https://github.com/user-attachments/assets/ceb129f1-25c5-4a35-9192-6fa1ed3eba52" />

## Models

Two approaches were implemented and compared:
- TF-IDF + Logistic Regression
- AraBERT v2

AraBERT v2 was fine-tuned using Hugging Face Transformers and PyTorch for binary Arabic text classification.

<img width="658" height="1096" alt="image" src="https://github.com/user-attachments/assets/641090f1-12bc-4315-8298-32e8eeaf7ff5" />

## Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| TF-IDF + Logistic Regression | 85% | 95% | 85% | 90% |
| AraBERT v2 | 96.67% | 96% | 97% | 96% |

AraBERT v2 achieved the best overall performance with 96.67% accuracy and an F1-score of 0.96 outperforming the traditional machine learning baseline.

<img width="666" height="716" alt="image" src="https://github.com/user-attachments/assets/d270dfc9-dad8-40ff-a862-ef646a195b4c" />

## AraBERT Performance

The AraBERT model showed a significant improvement over the baseline especially in handling the challenging and highly imbalanced Arabic hate speech dataset.

<img width="636" height="537" alt="image" src="https://github.com/user-attachments/assets/6ee467fc-7bce-4b74-9226-8e2b00d26f89" />

## Tools Used

- Python
- AraBERT v2
- Hugging Face Transformers
- PyTorch
- Pandas
- Scikit-learn
- TF-IDF
- Logistic Regression
- NLP
