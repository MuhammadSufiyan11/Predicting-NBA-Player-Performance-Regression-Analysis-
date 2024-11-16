# Sports Data Analysis and Machine Learning

This repository contains the code for analyzing sports data, specifically focusing on predicting player performance metrics such as points, assists, and rebounds using machine learning models.

## Table of Contents

- [Project Overview](#project-overview)
- [Dependencies](#dependencies)
- [Installation Instructions](#installation-instructions)
- [Data Description](#data-description)
- [Usage](#usage)
  - [Data Loading and Visualization](#data-loading-and-visualization)
  - [Feature Engineering](#feature-engineering)
  - [Model Training and Evaluation](#model-training-and-evaluation)
  - [Hyperparameter Tuning](#hyperparameter-tuning)
  - [Saving and Loading Models](#saving-and-loading-models)
- [License](#license)
- [Contact](#contact)

---

## Project Overview

This project involves analyzing sports data, particularly focusing on metrics such as points, assists, and rebounds. The dataset is used to train various machine learning models to predict player performance based on these statistics. The project explores:

- Data visualization to better understand the distribution of statistics.
- Feature engineering to generate useful features for predictive modeling.
- Training and evaluating machine learning models like Linear Regression, Ridge Regression, and Random Forest.
- Hyperparameter tuning to improve model performance.
- Saving and loading models for future use.

---

## Dependencies

The project uses several Python libraries, which you can install using `pip`. Below is the list of dependencies required to run the code:

```text
pandas
numpy
seaborn
matplotlib
scikit-learn
joblib

You can install them by running:

```bash
pip install -r requirements.txt

---

## Installation Instructions

Follow these steps to set up and run the project on your local machine.

Clone the repository:

```bash

git clone https://github.com/yourusername/sports-data-analysis.git
Navigate to the project directory:

```bash

cd sports-data-analysis
Install dependencies:

```bash

pip install -r requirements.txt
Run the scripts: You can execute different sections of the project by running the respective Python scripts from the terminal.

## Data Description

The dataset used in this project is a CSV file containing performance data for basketball players across multiple seasons. It includes the following columns (examples):

- pts: Points scored by a player.
- ast: Assists made by a player.
- reb: Rebounds grabbed by a player.
- Additional statistical columns may be included, depending on the dataset version.
- The dataset is used for training machine learning models to predict pts (points) based on other performance metrics such as assists and rebounds.

# Usage

## Data Loading and Visualization

The first step in any analysis is to load the data and visualize it to understand its structure. The script data_loading_and_visualization.py loads the dataset and generates visualizations to explore the distribution of statistics such as assists and rebounds, along with a heatmap for correlations between features.

To run this section:

```bash

python data_loading_and_visualization.py
This will:

- Load the dataset from all_seasons.csv.
- Plot the distribution of assists and rebounds.
- Display a heatmap showing the correlation between numerical features.

## Feature Engineering

The next step is feature engineering, which includes generating new features such as rolling averages and scaling the features. The script feature_engineering.py does the following:

- Creates a 5-game rolling average for the points (pts).
- Scales the features like points, assists, and rebounds using StandardScaler.
- Displays the updated dataset after the transformations.

To run this section:

```bash

python feature_engineering.py

This will:

- Generate new features (like rolling averages).
- Standardize the numerical columns (e.g., points, assists, rebounds).

## Model Training and Evaluation

In this section, different machine learning models are trained on the data, including:

- Linear Regression
- Ridge Regression
- Random Forest

The script model_training.py performs the following tasks:

- Splits the data into training and testing sets.
- Imputes missing values in the training and test data.
- Trains the models.
- Evaluates model performance using R-squared and Mean Absolute Error (MAE).

To run this section:

```bash

python model_training.py

This will:

- Train the models on the dataset.
- Print the evaluation metrics for each model.
- Hyperparameter Tuning
- To improve the performance of the Ridge Regression model, hyperparameter tuning is performed using GridSearchCV. The script hyperparameter_tuning.py searches for the best hyperparameters for the Ridge model, such as the regularization strength (alpha), by performing cross-validation.

To run this section:

```bash

python hyperparameter_tuning.py

This will:

- Tune the Ridge model using cross-validation.
- Display the best hyperparameters and evaluation metrics.

##Saving and Loading Models

Once the models are trained and evaluated, you can save them for future use. The script model_saving_loading.py demonstrates how to:

- Save a model (e.g., Ridge Regression) to a file using joblib.
- Load a saved model and use it to make predictions on new data.

To run this section:

```bash

python model_saving_loading.py

This will:

- Save the trained Ridge Regression model to ridge_model.pkl.
- Load the saved model and make predictions.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For any questions or feedback, feel free to reach out:

- Email: your.email@example.com
- GitHub: github.com/yourusername
