# Predictive-Analysis-Assisngment-6

# Data Generation using Modelling and Simulation
This project simulates a queuing system (like a line at a store) to generate data, uses machine learning models to predict waiting times, and then ranks those models to find the best one.

## Overview
The main goal is to see how well different computer programs (machine learning models) can predict how long someone has to wait in line based on how fast people arrive and how fast they are served.

The project creates its own dataset using a simulation, trains many different models, and then uses a method called TOPSIS to figure out which model is the "winner" based on accuracy and errors.

## Requirements
To run this code, you need Python installed along with these libraries:
* simpy (for the simulation)
* numpy & pandas (for math and data handling)
* matplotlib & seaborn (for making graphs)
* scikit-learn (for the machine learning models)

You can install them using pip:

```bash
pip install simpy numpy pandas matplotlib seaborn scikit-learn
```

## How It Works
The code runs in three main steps:

### 1. Data Generation (Simulation)
We use simpy to simulate a single server queue (like one cashier).

* Input: Random arrival rates and service rates.
* Process: We run the simulation 1000 times with different settings.
* Output: A dataset containing Arrival Rate, Service Rate, and the resulting Mean Wait Time.

### 2. Model Training
We split the data into a "training set" (to teach the models) and a "test set" (to test them). We use several standard regression models, including:

* Linear Regression
* Ridge, Lasso, ElasticNet
* Support Vector Regressor (SVR)
* Decision Trees and Random Forests
* Gradient Boosting and AdaBoost
* K-Nearest Neighbors (KNN)

### 3. Ranking (TOPSIS)
Since different models are good at different things (some have low error, some have high accuracy), we use TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution) to rank them.

* We look at metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), R-squared score, etc.
* The code calculates a "Score" for each model.
* The model with the highest score is considered the best.

## Results
When you run the code, it will:

* Print that it is generating data.
* Print a table showing the ranking of all models from best to worst.

* Show two graphs:

   * A bar chart of the TOPSIS scores.

   * A scatter plot showing how well the best model's predictions match the real data.
<img width="1256" height="944" alt="image" src="https://github.com/user-attachments/assets/0f2a4bcc-96f7-43d5-8710-828c31cb31e6" />


<img width="1132" height="946" alt="image" src="https://github.com/user-attachments/assets/7ec62637-ac42-4185-9c35-1197bcadc97a" />

<img width="1048" height="782" alt="image" src="https://github.com/user-attachments/assets/d4bbc9f9-aa03-4f94-bf1d-ca2da7beb396" />



