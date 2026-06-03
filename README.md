 Predictive Analysis using Random Forest Classifier
📌 Project Overview
This project demonstrates a complete machine learning pipeline for predictive analysis using a Random Forest Classifier. It includes data loading, preprocessing, feature engineering, model training, evaluation, and visualization.
The goal is to build a model that can accurately predict outcomes based on input features from a dataset.
⚙️ Technologies Used
Python 🐍
Pandas
NumPy
Matplotlib
Scikit-learn
KaggleHub
📂 Dataset
The dataset is downloaded using KaggleHub:
Python
import kagglehub
path = kagglehub.dataset_download("brendan45774/test-file")
The dataset is automatically downloaded and stored locally.
The code dynamically selects the CSV file from the folder.
🔄 Workflow
1. Data Loading
Dataset is loaded using Pandas.
File path is automatically detected.
2. Data Preprocessing
Missing values are removed using:
Python
df = df.dropna()
Categorical variables are converted into numerical form using one-hot encoding:
Python
df = pd.get_dummies(df, drop_first=True)
3. Feature Selection
Independent variables (features):
Python
X = df.iloc[:, :-1]
Dependent variable (target):
Python
y = df.iloc[:, -1]
4. Train-Test Split
Dataset is split into training and testing sets:
Python
train_test_split(test_size=0.2)
5. Feature Scaling
Features are standardized using StandardScaler.
6. Model Training
A Random Forest Classifier is used:
Python
model = RandomForestClassifier()
7. Prediction
Predictions are made on the test dataset.
8. Model Evaluation
The model is evaluated using:
Accuracy Score
Classification Report
Confusion Matrix
9. Feature Importance Visualization
A horizontal bar chart is plotted to show feature importance.# Predictive_Analysis_using_ML.PY
