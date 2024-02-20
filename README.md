# Breast Cancer Predictor - Streamlit Web App

Thank you to [Alejandro AO](https://github.com/alejandro-ao) for the walkthrough!

This repository consists of four parts: 
- `model` folder that contains Python script for training a logistic regression model on breast cancer data
- `app` folder that contains Streamlit web app for predicting breast cancer diagnosis based on user input
- `assets` folder that contains a CSS script to customize the Streamlit web app
- `data` folder that contains the [Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)

### Part 1: Model Training

The script begins by importing necessary libraries, including Pandas for data manipulation, scikit-learn for machine learning operations, and Pickle for model serialization.

### Part 2: Streamlit Web App

The Streamlit web app is designed to predict breast cancer diagnosis based on user input through sliders. It uses the trained logistic regression model and scaler from the saved files.

### Conclusion
This integrated solution allows users to interact with a web app, input relevant data through sliders, and receive predictions about breast cancer diagnosis using a logistic regression model trained on historical data.
