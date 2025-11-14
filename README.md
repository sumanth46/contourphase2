Dynamic Pricing Modeling with Ridge Regression and MLflow

This repository contains the machine learning pipeline for developing a dynamic pricing model using Ridge Regression. The project focuses on data preparation, comprehensive hyperparameter tuning using GridSearchCV, and meticulous experiment tracking using MLflow.

Project Artifacts

final_model_tracking.ipynb: The main Jupyter Notebook detailing the entire workflow, from data loading and preparation to model training, evaluation, and logging the final model to MLflow.

9e05bb74-2719-45b0-bbc7-0ced2f61a442_dynamicpricingmodelingprepareddata.csv: The prepared dataset used for training the model (uploaded separately).

requirements.txt: A list of all required Python libraries.

.gitignore: Configuration file to exclude development and MLflow artifacts.

Setup and Execution

Clone the repository:

git clone <repository-url>
cd <repository-name>


Install dependencies:

pip install -r requirements.txt


Run MLflow:
Start the MLflow UI to track runs (data is logged locally by default to the mlruns folder):

mlflow ui


Run the Notebook:
Execute the cells in final_model_tracking.ipynb to train the Ridge Regression model, perform Grid Search for the optimal alpha, and log the best model to the running MLflow tracking server.

MLflow Tracking Snapshot

The MLflow integration ensures that all experiments are reproducible and comparable. Key components tracked include:

Parameters: model_type, best_alpha, feature_count, features_list.

Metrics: RMSE, MAE, R2 Score, and Adjusted R2 on the test set.

Artifacts: A Residual Plot to visually check model performance and bias.

Model: The finalized Ridge model is logged with its full signature, ready for deployment.
