# ML Pipeline for Short-Term Rental Price Prediction

## Overview
This project builds an end-to-end machine learning pipeline for predicting short-term rental prices in New York City. The pipeline automates data collection, cleaning, modeling, and evaluation, allowing for weekly retraining with new data. The goal is to accurately estimate rental prices based on historical data and property features, enabling property management companies to optimize pricing strategies.

The project uses Python, Scikit-learn, MLflow, and [Weights & Biases](https://wandb.ai/) (W&B) to create a reproducible workflow that integrates data versioning, model tracking, and hyperparameter optimization.

## Key Skills and Technologies:
- **Python**: Data manipulation, pipeline construction, testing, and modeling
- **MLflow**: Managing the pipeline, tracking experiments, and deploying models
- **Weights & Biases (W&B)**: Artifact storage and tracking
- **Scikit-learn**: Data preprocessing and Random Forest modeling
- **Pandas**: Data analysis and manipulation
- **Jupyter Notebooks**: Exploratory data analysis
- **Hydra**: Configuration management
- **Git**: Version control and pipeline release
- **Conda**: Environment management

## Project Overview

The pipeline is structured into the following steps:

1. **Exploratory Data Analysis (EDA)**: Conducting EDA on the sample dataset and uploading the sample to W&B.
2. **Data Cleaning**: Cleaning the dataset by removing outliers and null values.
3. **Data Testing**: Ensuring data integrity through testing row count and price range.
4. **Train-Test Split**: Splitting the data into training and validation sets.
5. **Model Training**: Training a Random Forest model with hyperparameter tuning.
6. **Model Testing**: Testing the model and selecting the best performing model.
7. **Pipeline Release and Updates**: Visualizing, releasing the pipeline, and running the model on new data.

## Installation

To run this project, clone the repository and follow the setup instructions below.

### Steps
1. **Clone the Repository:**
   ```
   git clone https://github.com/liz-2450/ML-Pipeline-Rental-Prices.git
   cd ML-Pipeline-Rental-Prices
   ```

2. **Create and Activate the Conda Environment:**
   Make sure to have [conda](https://docs.conda.io/en/latest/) installed and then create a new environment:
   ```
   conda env create -f environment.yml
   conda activate nyc_airbnb_dev
   ```

3. **Set Up Weights & Biases (W&B):**
   Log in to your [W&B](https://wandb.ai/) account to get your API key.
   ```
   wandb login <your-api-key>
   ```
   
4. **Run the Pipeline:**
   Use MLflow to run the entire pipeline:
   ```
   mlflow run .
   ```

   To run specific steps, such as downloading data and basic cleaning, use:
   ```
   mlflow run . -P steps=download,basic_cleaning
   ```

Visualization of the Pipeline, including steps run and artifacts generated
![random_forest_export](https://github.com/user-attachments/assets/f69321de-fd15-44cc-a5e4-4054b0415bb5)

## Future Work
Potential improvements include:
- **Scalability:** Implementing the pipeline on larger datasets with cloud computing resources.
- **Additional Features:** Incorporating more property features like guest reviews or seasonal trends

## License

[License](LICENSE.txt)
