# 💻 Tech Stack:
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![MySQL](https://img.shields.io/badge/mysql-%2300000f.svg?style=for-the-badge&logo=mysql&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)

# Predicting Carbon Emissions in Rwanda

## Overview
This repository contains code and resources for the Kaggle competition on predicting carbon emissions in Rwanda using open-source emissions data from Sentinel-5P satellite observations. The challenge is to build machine learning models that accurately predict CO2 emissions for the year 2022 through November based on data from 2019 to 2021.

## Dataset
The dataset consists of approximately 497 unique locations across Rwanda, covering farm lands, cities, and power plants. The data is split by time, with training data containing information from 2019 to 2021, and the task is to predict CO2 emissions for 2022 through November.

### Features
Eight main features were extracted weekly from Sentinel-5P, including:

1. Sulphur Dioxide 
2. Carbon Monoxide 
3. Nitrogen Dioxide 
4. Formaldehyde 
5. UV Aerosol Index 
6. Ozone 
7. Cloud
8. Emission

Each feature includes sub-features, such as `column_number_density`, representing the vertical column density at ground level, calculated using the Differential Optical Absorption Spectroscopy (DOAS) technique.

## Files
- `train.csv`: The training set [Link ](https://www.kaggle.com/competitions/playground-series-s3e20/data?select=train.csv)
- `test.csv`: The test set; the task is to predict the emission target for each week at each location [Link ](https://www.kaggle.com/competitions/playground-series-s3e20/data?select=test.csv)
- `sample_submission.csv`: A sample submission file in the correct format [Link](https://www.kaggle.com/competitions/playground-series-s3e20/data?select=sample_submission.csv)

## Important Note
Please only use the provided data for modeling efforts. Do not incorporate any external data, including additional Sentinel-5P data not provided in this competition.

# Evaluation Metrics: Root Mean Squared Error (RMSE)

## Overview

This repository provides insights into the evaluation metric used for assessing predictive models: Root Mean Squared Error (RMSE). RMSE is a widely adopted metric, particularly in regression tasks, measuring the accuracy of a model's predictions by calculating the square root of the mean of squared errors.

## Root Mean Squared Error (RMSE)

RMSE is defined as follows:

![RMSE Formula](https://latex.codecogs.com/svg.latex?RMSE%20=%20\sqrt{\frac{1}{n}%20\sum_{i=1}^{n}%20(y_i%20-%20\hat{y}_i)^2})

- yi is the actual value for the ith observation.
- ŷi is the predicted value for the ith observation.
- n is the number of observations.

## Insights

## Emission Trend Values Over Weeks


![image](https://github.com/nitinkc1/Predict_CO2_Emissions_in_Rwanda/assets/130339748/17ccae8e-5f6e-4b54-a65f-c5be6f49cac0)

## Emission Trend Values By Month

![image](https://github.com/nitinkc1/Predict_CO2_Emissions_in_Rwanda/assets/130339748/9be800f2-52ee-4164-83db-cc2d2955abfb)


## Emission Trend Values Over Years


![image](https://github.com/nitinkc1/Predict_CO2_Emissions_in_Rwanda/assets/130339748/78fa1a60-9415-4099-9add-c2d035dc2dc4)


## EMISSION Values OVER YEARS-MONTH

![image](https://github.com/nitinkc1/Predict_CO2_Emissions_in_Rwanda/assets/130339748/51f37a24-e424-49c1-be7c-2b4b3dffca4d)

### Best Performing Models
1. **Random Forest:** The Random Forest model exhibits the lowest error, suggesting it provides the most accurate predictions among the models tested.

2. **Decision Trees:** Decision Trees also perform well, with a relatively low error compared to other models.


### Models to Investigate
1. **Gradient Boosting Machines (GBM):** The GBM model shows a higher error compared to Random Forest, indicating potential areas for improvement or optimization.

2. **Linear Regression:** Linear Regression exhibits a high error, indicating that the relationship between features and emissions may not be adequately captured by a linear model.

![image](https://github.com/nitinkc1/Predict_CO2_Emissions_in_Rwanda/assets/130339748/eb8dc60a-552b-4388-8086-04e021407704)



## Next Steps
1. **Model Tuning:** Explore hyperparameter tuning for the models, especially Gradient Boosting Machines and Support Vector Machines, to potentially improve performance.

2. **Feature Engineering:** Experiment with feature engineering techniques to enhance the predictive power of the models.

3. **Ensemble Methods:** Consider ensemble methods, such as stacking or blending, to combine the strengths of multiple models for improved accuracy.

4. **Data Analysis:** Conduct a detailed analysis of feature importance to understand the factors influencing the model predictions.

5. **Validation Strategies:** Evaluate the models using different validation strategies to ensure robustness and reliability.

# Model Performance Summary

Below is a summary of the performance of various machine learning models in predicting carbon emissions for the Kaggle competition. The error values are reported to provide insights into the accuracy of each model.

# Machine Learning Models and Errors

# Model Performance Metrics

| Model                    | RMSE                   | R-squared            |
|--------------------------|------------------------|----------------------|
| Linear Regression        | 4.099781875787298      | 0.07111067682647543  |
| Decision Tree            | 1.766124569996646      | 0.827620691797228    |
| Random Forest            | 1.5992133748558037     | 0.858663186651433    |
| Gradient Boosting Machine| 1.6295264374451177     | 0.8532543317180261   |


## Acknowledgments
- Kaggle for hosting the competition
- Sentinel-5P for providing the emissions data
