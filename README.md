# Solar-Power-Prediction
☀️ A predictive modeling project to forecast solar power generation using weather data and Linear Regression. Includes EDA, feature engineering, and a Power BI dashboard.


# ☀️ Solar Power Generation Prediction

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg?logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0%2B-orange?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-1.3%2B-150458?logo=pandas)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 🎯 Project Overview

Forecasting solar power generation is a critical task for optimizing power grid management and promoting the adoption of renewable energy. This project aims to develop a highly accurate predictive model that forecasts the DC and AC power output of solar power plants using weather sensor data.

This end-to-end data science project demonstrates data integration, feature engineering, exploratory data analysis, and the development of predictive models using Linear Regression, achieving an R² score of over 95%.

## 📊 The Datasets

The analysis utilizes two types of data from two separate solar power plants in India:
1.  **Power Generation Data:** Time-series data of DC and AC power output, along with daily and total yield.
2.  **Weather Sensor Data:** Time-series data from plant-site sensors, including `AMBIENT_TEMPERATURE`, `MODULE_TEMPERATURE`, and `IRRADIATION`.

## 🛠️ Methodology & Workflow

The project was executed through a systematic data science pipeline:

1.  **Data Integration & Cleaning:** The power generation and weather sensor datasets for each plant were loaded, cleaned, and merged based on the `DATE_TIME` key.
2.  **Feature Engineering:** New time-based features (`hour`, `minutes`) and a `temp_diff` feature (Module Temperature - Ambient Temperature) were created to enhance the model's predictive power.
3.  **Exploratory Data Analysis (EDA):**
    -   An interactive **Power BI dashboard** was developed for high-level data exploration.
    -   Python libraries (Matplotlib, Seaborn) were used to visualize relationships between variables. A correlation heatmap confirmed that **Solar Irradiation** has the strongest linear relationship with power output.
4.  **Model Training:**
    -   **Linear Regression** was chosen as the modeling algorithm due to the strong linear correlation observed between the features and the target variables (`AC_POWER` and `DC_POWER`).
    -   Separate models were trained for each solar plant to account for plant-specific characteristics.
5.  **Model Evaluation:** The models were evaluated using the **R-squared ($R^2$) metric**, which measures the proportion of the variance in the dependent variable that is predictable from the independent variables.

## 🏆 Results & Key Insights

The Linear Regression models performed exceptionally well, explaining over **95%** of the variance in power generation.

| Plant   | Target Variable | R² Score |
| ------- | :-------------: | :------: |
| Plant 1 |    `AC_POWER`   |  95.5%   |
| Plant 1 |    `DC_POWER`   |  95.5%   |
| Plant 2 |    `AC_POWER`   |  96.4%   |
| Plant 2 |    `DC_POWER`   |  96.4%   |

The most significant insight from the EDA is that **Solar Irradiation is the primary driver of power generation**. The relationship is strongly linear, as shown in the plot below, which explains the high success of the Linear Regression model.

*(You can add a screenshot of your `IRRADIATION` vs. `AC_POWER` scatter plot here)*

## 📊 Power BI Dashboard

An interactive dashboard was created in Power BI for a comprehensive visual analysis of the solar plant data. It provides insights into power generation trends, the impact of weather conditions, and plant performance comparisons. The `.pbix` file is available in the `/dashboard` directory.

*(Add a screenshot of your Power BI dashboard from the presentation here)*

## 🚀 How to Run this Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/PushpakShrimal/Solar-Power-Generation-Prediction.git](https://github.com/PushpakShrimal/Solar-Power-Generation-Prediction.git)
    cd Solar-Power-Generation-Prediction
    ```
2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows: env\Scripts\activate
    ```
3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook notebooks/"Capston_Project (PUSHPAK SHRIMAL).ipynb"
    ```
5.  **View the Dashboard:**
    -   Open the `dashboard/` folder and launch the `Capstone Project.pbix` file using Power BI Desktop.

---
