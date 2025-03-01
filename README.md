# Prédiction-des-blessures-majeures-des-footballeurs
This project aims to predict whether a football player will suffer a major injury using machine learning. The project employs the XGBoost model to predict the risk based on various features such as physical conditions, game statistics, and player characteristics.

Table of Contents
Introduction
Dataset
Modeling Approach
Results
Installation
Usage
License
Introduction
In the world of football, player injuries are a critical concern. This project uses machine learning to predict if a football player is likely to sustain a major injury during a season. By using the XGBoost algorithm, the model predicts the likelihood of injury based on features like player age, speed, fitness, FIFA rating, injury history, and match statistics.

Dataset
The dataset used in this project contains information about various football players, including:

Age
Height
Weight
FIFA Rating
Speed
Minutes Played
Injury History
Physical Condition
Match Statistics
The dataset was sourced from Kaggle, and it can be found here.

Modeling Approach
XGBoost Algorithm
XGBoost (Extreme Gradient Boosting) is used for this classification task. The algorithm employs the concept of boosting to combine multiple weak models (decision trees) into a strong one. Hyperparameters are tuned using RandomizedSearchCV to find the best model configuration.

Data Preprocessing
Missing Value Handling: The dataset is checked for missing values and appropriately imputed.
Feature Engineering: Features like age, height, weight, and match statistics are used to train the model.
Categorical Feature Encoding: Categorical features (such as nationality) are encoded for model input.
Model Optimization
The model’s hyperparameters, such as learning_rate, max_depth, and subsample, are optimized using RandomizedSearchCV to ensure the best performance.

Model Evaluation
The model’s performance is evaluated using metrics like precision, recall, F1-score, and accuracy.

Results
The model achieved good performance in predicting whether a player will suffer a major injury, with a precision of 0.84 and recall of 0.84. The results show that the model is quite reliable in predicting injury risks for football players.

Key Findings:
The best hyperparameters for the XGBoost model were:

learning_rate: 0.0687
max_depth: 3
n_estimators: 89
subsample: 0.8378
colsample_bytree: 0.5354
Feature Importance: The model highlighted the importance of features such as age, minutes played, and FIFA rating in predicting injuries.

Installation
To run this project locally, follow these steps:

Clone the repository:
git clone https://github.com/hanelo/Pr-diction-des-blessures-majeures-des-footballeurs.git
cd predicting-football-injuries
Install the required libraries:

pip install -r requirements.txt
Make sure you have Python 3.x installed on your system.

Usage
After setting up the environment, you can run the project by executing:
python main.py
This will train the model and print the results to the console.

License
This project is licensed under the MIT License - see the LICENSE file for details.

