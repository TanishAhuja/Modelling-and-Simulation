# Simulation-Based Data Generation and Machine Learning Model Comparison

---

## Project Overview

This project demonstrates a complete end-to-end pipeline that integrates **computer simulation** with **machine learning model evaluation**.

A simulation system is used to generate structured synthetic data under varying parameter configurations. The generated dataset is then used to train and compare multiple machine learning models in order to determine the best-performing model.

All graphs, comparison results, and evaluation outputs are stored inside:

main_directory/Outputs/

The entire experimentation workflow was conducted using **Google Colab** and version-controlled using **GitHub** to ensure reproducibility.

---

## Objective

The main objectives of this project are:

1. To design and execute a parameter-driven computer simulation  
2. To identify important simulation parameters and define realistic bounds  
3. To generate large-scale structured data using randomized sampling  
4. To train multiple machine learning regression models  
5. To evaluate and compare model performance using standard metrics  
6. To identify the most accurate model for prediction  

---

## Simulation Framework

The simulation generates structured synthetic data by:

- Randomly sampling parameters within predefined bounds
- Executing simulation logic for each configuration
- Recording relevant output metrics
- Repeating the process multiple times to build a dataset

The final generated dataset is saved as:

simulation_data.csv

---

## Simulation Parameters and Bounds

The following parameters were varied during simulation:

| Parameter        | Description                    | Lower Bound | Upper Bound |
|------------------|--------------------------------|------------|------------|
| Population       | Number of entities/agents      | 50         | 300        |
| Infection Rate   | Probability of spread          | 0.05       | 0.9        |
| Recovery Rate    | Probability of recovery        | 0.01       | 0.5        |
| Initial Infected | Starting infected entities     | 1          | 20         |
| Simulation Steps | Number of iterations           | 50         | 200        |

These bounds ensure diverse but meaningful simulation outcomes.

---

## Data Generation Process

- Random parameter values were sampled uniformly
- Each parameter set was passed into the simulation engine
- Simulation was executed for fixed steps
- Target output (e.g., peak value or final metric) was recorded
- The process was repeated multiple times (e.g., 1000 runs)

This produced a structured dataset used for supervised learning.

---

## Machine Learning Models Evaluated

The following regression models were trained and compared:

1. Linear Regression  
2. Decision Tree Regressor  
3. Random Forest Regressor  
4. Gradient Boosting Regressor  
5. Support Vector Regressor (SVR)  
6. K-Nearest Neighbors Regressor  

---

## Evaluation Metrics

Each model was evaluated using:

- **R² Score** – Goodness of fit  
- **RMSE** – Root Mean Squared Error  
- **MAE** – Mean Absolute Error  

The complete comparison results are stored in:

Outputs/model_comparison.csv

---

## Results and Visualizations

All visualizations and graphs are stored in:

Outputs/

### R² Score Comparison

Outputs/model_r2_comparison.png

### RMSE Comparison

Outputs/model_rmse_comparison.png

These visualizations provide a clear comparison of model performance across multiple evaluation metrics.

---

## Best Performing Model

Based on evaluation results, the **Gradient Boosting Regressor** demonstrated the best overall performance, achieving:

- Highest R² score  
- Lowest RMSE  
- Lowest MAE  

This indicates strong capability in capturing complex non-linear relationships present in the simulation-generated data.

---

## Reproducibility

- Implemented entirely in **Google Colab**
- Controlled parameter bounds ensure consistent experimentation
- Randomized sampling ensures dataset diversity
- Version-controlled with GitHub

---

## Future Scope

This framework can be extended to:

- Larger or real-world datasets  
- Hyperparameter tuning for improved performance  
- Ensemble learning strategies  
- Classification-based prediction tasks  
- Application to domains such as economics, traffic modeling, or crowd dynamics  

---

## Author

**Tanish Ahuja**
