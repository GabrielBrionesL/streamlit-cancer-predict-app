# Breast Cancer Predictor deployed on Streamlit

This code consists of two parts: a Python script for training a logistic regression model on breast cancer data, and a Streamlit web app for predicting breast cancer diagnosis based on user input.

### Part 1: Model Training

The script begins by importing necessary libraries, including Pandas for data manipulation, scikit-learn for machine learning operations, and Pickle for model serialization.

#### Function `get_clean_data()`:
- [Reads a CSV file containing breast cancer data.](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
- Drops unnecessary columns ('Unnamed: 32', 'id').
- Maps the 'diagnosis' column values ('M' for malignant and 'B' for benign) to numerical values (1 and 0).

#### Function `create_model(data)`:
- Takes cleaned data as input.
- Splits the data into features (X) and target labels (y).
- Standardizes the features using `StandardScaler`.
- Divides the dataset into training and testing sets.
- Creates a logistic regression model, trains it on the training set, and evaluates its accuracy on the test set.
- Returns the trained model and scaler.

#### Function `main()`:
- Calls `get_clean_data()` to obtain the cleaned dataset.
- Calls `create_model(data)` to train the logistic regression model.
- Serializes the trained model and scaler using Pickle and saves them to files.

### Part 2: Streamlit Web App

The Streamlit web app is designed to predict breast cancer diagnosis based on user input through sliders. It uses the trained logistic regression model and scaler from the saved files.

#### Functions `add_sidebar()` and `get_scaled_values(input_dict)`:
- `add_sidebar()` sets up a sidebar in the Streamlit app with sliders for different features.
- `get_scaled_values(input_dict)` scales the user input values based on the scaling applied during model training.

#### Function `get_radar_chart(input_data)`:
- Creates a radar chart using Plotly to visualize the scaled input values in different categories (mean, standard error, worst values).

#### Function `add_predictions(input_data)`:
- Loads the trained model and scaler.
- Predicts the diagnosis based on the scaled user input.
- Displays the predicted diagnosis (benign or malignant) along with probabilities.
  
#### Function `main()`:
- Sets up the Streamlit app configuration.
- Loads a custom CSS style for formatting.
- Calls `add_sidebar()` to obtain user input.
- Displays information about the breast cancer predictor.
- Uses `get_radar_chart()` to show a radar chart of user input.
- Calls `add_predictions()` to display the predicted diagnosis and probabilities.

### Conclusion
This integrated solution allows users to interact with a web app, input relevant data through sliders, and receive predictions about breast cancer diagnosis using a logistic regression model trained on historical data.
