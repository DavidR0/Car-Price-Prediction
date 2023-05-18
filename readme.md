# Car Price Prediction Project

The Car Price Prediction project utilizes machine learning and regression techniques to determine the potential selling price of a car in Sri Lanka. The project makes use of a dataset obtained from Kaggle, which serves as the basis for analysis and model training. Here's an overview of the project workflow:

## Data Set Inspection and Feature Selection

- **Data Set Inspection**: The project begins with a thorough inspection of the dataset to assess its validity and quality. Various attributes such as price, description, and year are examined to understand the information they provide.

- **Feature Selection**: Based on the information provided by the dataset, a feature selection process is conducted. Relevant features are chosen, taking into consideration their importance and contribution to the final prediction. The goal is to select features that have a strong correlation with the car's selling price.

## Data Cleanup and Feature Engineering

- **Data Cleanup**: The dataset undergoes a cleanup process to remove outliers and anomalies that could negatively impact the learning process. Outliers are identified and eliminated to ensure accurate model training.

- **Feature Engineering**: Feature engineering is performed to create new features by combining existing ones. This step aims to enhance the predictive power of the model. Plots such as heatmaps and scatter plots are used to visualize the correlation between the new features and the existing ones.

## Model Training

- **Data Splitting**: The dataset is split into multiple parts using ShuffleSplit. This allows for hyperparameter tuning and prevents data leakage. The dataset is divided into training (80%) and test (20%) sets. The training set is further split into a validation set (20%) and a final training set (60%) to facilitate parameter tuning and prevent overfitting.

- **Preprocessing**: Custom data classes are created to shape and preprocess the data. An imputer is added to handle any missing values (NaNs). Non-numerical features are encoded using a One Hot Encoder.

- **Model Selection**: Several models are experimented with, including K-Nearest Neighbors (KNN), Random Forest Regressor, and Gradient Boosting Regressor. Each model is trained and evaluated individually to determine its performance.

- **Ensemble Learning**: The models are combined using a Voting Regressor to create an ensemble. This ensemble approach further improves the accuracy and robustness of the predictions.

## Evaluation and Finalization

- **Mean Absolute Error**: The final model's performance is evaluated using a mean absolute error metric. The deviation between the predictions on the development set and the training set is analyzed to assess the model's accuracy.

- **Model Training on Full Dataset**: Once satisfied with the model's performance, it is trained on the entire dataset to leverage the maximum available data for better predictions.

The Car Price Prediction project involves thorough data analysis, feature engineering, model training, and evaluation to estimate the selling price of cars in Sri Lanka. The combination of multiple models using a Voting Regressor ensures a comprehensive and accurate prediction outcome.