# Filtering-Fake-Job-Postings
This project is a full-stack machine learning application designed to detect fake job postings and identify keywords and signals commonly associated with fraudulent listings. The system demonstrates an end-to-end ML pipeline, from data preprocessing and feature engineering to model training, evaluation, and explainability.

Fake Job Posting Detection System
Full-Stack Machine Learning Project

Overview

Fake job postings are increasingly common and can expose job seekers to scams, identity theft, and financial loss. This project builds an end-to-end machine learning system that classifies job postings as authentic or fraudulent and identifies the keywords and structured signals most associated with fake listings.

The project demonstrates the full machine learning lifecycle, including data preprocessing, feature engineering, model training, evaluation, and interpretability through feature importance analysis.

Project Goals

- Predict whether a job posting is real or fake

- Extract key textual and metadata features linked to fraudulent postings

- Build a reproducible and scalable machine learning pipeline

- Provide explainability by identifying influential keywords and signals

Technologies Used

- Python

- pandas and numpy for data processing

- scikit-learn for machine learning and pipelines

- matplotlib and seaborn for visualization

- TF-IDF for natural language processing

- Random Forest for classification

Project Structure

├── expediapostings.py
├── train.csv
├── test.csv
├── submissions.csv
├── top_features_summary.csv
└── README.md


Model Architecture

The model is implemented as a single scikit-learn pipeline:

Text preprocessing using TF-IDF vectorization

Feature combination using ColumnTransformer

Classification using a Random Forest classifier

The pipeline design ensures that preprocessing and modeling steps remain consistent and reproducible.

Model Training and Evaluation

Train-validation split: 80 percent training, 20 percent validation

Stratified sampling to preserve class balance

Evaluation metric: Accuracy

A full classification report is generated, including precision, recall, and F1-score.

Feature Importance and Keyword Analysis

To improve interpretability, feature importance scores are extracted from the trained Random Forest model. The top 20 most influential features are visualized and saved to a CSV file.

This analysis helps identify keywords and metadata signals that commonly appear in fake job postings.

Generated files include:

A bar chart of top features

top_features_summary.csv containing feature importance rankings

How to Run the Project

Install required dependencies:

pip install pandas numpy scikit-learn matplotlib seaborn

Ensure the following files are present in the project directory:

train.csv

test.csv

Run the script:

python expediapostings.py
Output Files

submissions.csv
Contains job posting IDs and predicted authenticity labels.

top_features_summary.csv
Lists the most important textual and structured features used by the model.

Future Improvements

Deploy the model using a REST API (Flask or FastAPI)

Add a frontend interface for real-time job screening

Experiment with deep learning models such as BERT

Integrate SHAP or LIME for enhanced explainability

Expand feature engineering with additional job metadata

Conclusion

This project showcases practical experience in machine learning, natural language processing, and fraud detection. It reflects real-world challenges and demonstrates how interpretable models can be used to improve trust and safety in online job platforms.
