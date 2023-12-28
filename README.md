
# 💻 Tech Stack:
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![MySQL](https://img.shields.io/badge/mysql-%2300000f.svg?style=for-the-badge&logo=mysql&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)

# Predicting Carbon Emissions in Rwanda

## Overview
This repository contains code and resources for the Kaggle competition on predicting carbon emissions in Rwanda using open-source emissions data from Sentinel-5P satellite observations. The challenge is to build machine learning models that accurately predict CO2 emissions for the year 2022 through November based on data from 2019 to 2021.

## Dataset
The dataset consists of approximately 497 unique locations across Rwanda, covering farm lands, cities, and power plants. The data is split by time, with training data containing information from 2019 to 2021, and the task is to predict CO2 emissions for 2022 through November.

### Features
Seven main features were extracted weekly from Sentinel-5P, including:

1. Sulphur Dioxide - [Link to data](https://www.kaggle.com/competition/infer-emission/data?select=COPERNICUS%2FS5P%2FNRTI%2FL3_SO2)
2. Carbon Monoxide - [Link to data](https://www.kaggle.com/competition/infer-emission/data?select=COPERNICUS%2FS5P%2FNRTI%2FL3_CO)
3. Nitrogen Dioxide - [Link to data](https://www.kaggle.com/competition/infer-emission/data?select=COPERNICUS%2FS5P%2FNRTI%2FL3_NO2)
4. Formaldehyde - [Link to data](https://www.kaggle.com/competition/infer-emission/data?select=COPERNICUS%2FS5P%2FNRTI%2FL3_HCHO)
5. UV Aerosol Index - [Link to data](https://www.kaggle.com/competition/infer-emission/data?select=COPERNICUS%2FS5P%2FNRTI%2FL3_AER_AI)
6. Ozone - [Link to data](https://www.kaggle.com/competition/infer-emission/data?select=COPERNICUS%2FS5P%2FNRTI%2FL3_O3)
7. Cloud - [Link to data](https://www.kaggle.com/competition/infer-emission/data?select=COPERNICUS%2FS5P%2FOFFL%2FL3_CLOUD)

Each feature includes sub-features, such as `column_number_density`, representing the vertical column density at ground level, calculated using the Differential Optical Absorption Spectroscopy (DOAS) technique.

## Files
- `train.csv`: The training set
- `test.csv`: The test set; the task is to predict the emission target for each week at each location
- `sample_submission.csv`: A sample submission file in the correct format

## Important Note
Please only use the provided data for modeling efforts. Do not incorporate any external data, including additional Sentinel-5P data not provided in this competition.

## Getting Started
To get started with the project, clone this repository and refer to the Jupyter notebooks for data exploration, model development, and evaluation.

```bash
git clone (https://github.com/nitinkc1/Predict_CO2_Emissions_in_Rwanda)
cd predicting-carbon-emissions
```

## Dependencies
Ensure you have the required dependencies installed. You can install them using the following command:

```bash
pip install -r requirements.txt
```

# Model Performance Summary

Below is a summary of the performance of various machine learning models in predicting carbon emissions for the Kaggle competition. The error values are reported to provide insights into the accuracy of each model.

| Model                              | Error       |
| ---------------------------------- | ----------- |
| Random Forest                      | 16.64       |
| Decision Trees                     | 19.49       |
| XGBoost                            | 21.56       |
| Gradient Boosting Machines (GBM)    | 62.32       |
| Support Vector Machines (SVM)      | 124.88      |
| Linear Regression                  | 127.15      |

## Insights

### Best Performing Models
1. **Random Forest:** The Random Forest model exhibits the lowest error, suggesting it provides the most accurate predictions among the models tested.

2. **Decision Trees:** Decision Trees also perform well, with a relatively low error compared to other models.

3. **XGBoost:** XGBoost, while not as accurate as Random Forest, still demonstrates good performance with a moderate error.

### Models to Investigate
1. **Gradient Boosting Machines (GBM):** The GBM model shows a higher error compared to Random Forest, indicating potential areas for improvement or optimization.

2. **Support Vector Machines (SVM):** SVM has a significantly higher error, suggesting it may not be well-suited for this specific task or may require additional tuning.

3. **Linear Regression:** Linear Regression exhibits a high error, indicating that the relationship between features and emissions may not be adequately captured by a linear model.

## Next Steps
1. **Model Tuning:** Explore hyperparameter tuning for the models, especially Gradient Boosting Machines and Support Vector Machines, to potentially improve performance.

2. **Feature Engineering:** Experiment with feature engineering techniques to enhance the predictive power of the models.

3. **Ensemble Methods:** Consider ensemble methods, such as stacking or blending, to combine the strengths of multiple models for improved accuracy.

4. **Data Analysis:** Conduct a detailed analysis of feature importance to understand the factors influencing the model predictions.

5. **Validation Strategies:** Evaluate the models using different validation strategies to ensure robustness and reliability.

## Acknowledgments
-Thank you for your efforts in exploring and experimenting with various machine learning models. Keep iterating and refining your approach to achieve the best possible performance in the Kaggle competition. Good luck! 🚀
- Kaggle for hosting the competition
- Sentinel-5P for providing the emissions data

Happy coding and best of luck with the competition! 🚀
