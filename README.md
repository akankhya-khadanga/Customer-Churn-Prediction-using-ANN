# Credit Card Customer Churn Prediction

A deep learning project that uses customer information and banking-related attributes to predict whether a customer is likely to leave a bank.

## Overview

Customer churn is an important business problem for banks because retaining an existing customer is often more valuable than acquiring a new one.

In this project, I explored a customer churn dataset, prepared the data for a neural network, and built a binary classification model using TensorFlow and Keras.

The notebook covers the complete workflow from data preprocessing to model training and evaluation.

## Dataset

The project uses the **Churn Modelling** dataset.

The data contains customer attributes such as:

* Credit Score
* Geography
* Gender
* Age
* Tenure
* Balance
* Number of Products
* Credit Card status
* Active Member status
* Estimated Salary

The target variable is:

* `Exited` — indicates whether the customer left the bank.

## Approach

The project follows these main steps:

1. Load and inspect the dataset
2. Remove unnecessary customer-identification columns
3. Explore categorical variables
4. Convert categorical features into numerical form
5. Separate features and target
6. Split the data into training and testing sets
7. Standardize the input features
8. Build a neural network using Keras
9. Train the model using the Adam optimizer
10. Evaluate the predictions
11. Visualize training and validation performance

## Data Preprocessing

The following columns were removed because they do not provide useful predictive information for the model:

```text
RowNumber
CustomerId
Surname
```

Categorical variables such as `Geography` and `Gender` were converted using one-hot encoding.

The numerical features were then standardized using `StandardScaler`.

## Model

I used a feed-forward neural network built with TensorFlow/Keras.

The architecture consists of:

```text
Input Layer
     ↓
Dense Layer — 11 neurons, Sigmoid
     ↓
Dense Layer — 11 neurons, Sigmoid
     ↓
Output Layer — 1 neuron, Sigmoid
```

The model was compiled using:

* **Optimizer:** Adam
* **Loss:** Binary Cross-Entropy
* **Metric:** Accuracy

The model was trained for 100 epochs with a batch size of 50.

## Training Analysis

Training and validation curves were plotted to observe how the model's:

* Loss changed during training
* Accuracy changed during training

These plots help identify the model's learning behaviour and provide an initial indication of whether the model is learning effectively or showing signs of overfitting.

## Technologies

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* TensorFlow
* Keras
* Jupyter Notebook / Kaggle

## Project Structure

```text
credit-card-customer-churn/
│
├── README.md
└── churn_prediction.ipynb
```

## How to Run

Clone the repository:

```bash
git clone <your-repository-url>
cd credit-card-customer-churn
```

Install the required libraries:

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow
```

Then open the notebook using Jupyter:

```bash
jupyter notebook
```

Or open the notebook directly through JupyterLab or VS Code.

## What I Learned

This project helped me understand the practical workflow involved in applying neural networks to a tabular classification problem.

In particular, I worked with:

* Categorical feature encoding
* Feature scaling
* Train-test splitting
* Neural network architecture
* Activation functions
* Binary cross-entropy
* Adam optimization
* Model training
* Validation performance
* Training and validation curves

## Future Improvements

Some possible improvements for the project include:

* Tune the neural network architecture and hyperparameters
* Compare the neural network with traditional ML models such as Logistic Regression, Random Forest, and XGBoost
* Evaluate the model using precision, recall, F1-score, and ROC-AUC
* Handle class imbalance if required
* Improve the prediction threshold instead of relying only on the default 0.5 threshold
* Deploy the trained model as a web application

## Author

**Akankhya Khadanga**

B.Tech Computer Science Engineering
Data Science & Machine Learning
