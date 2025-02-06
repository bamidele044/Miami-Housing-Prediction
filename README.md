# Miami House Prices Prediction

## Table of Contents

- [Project Overview](#project-overview)
- [Business Understanding](#business-understanding)
- [Dataset Source](#dataset-source)
- [Tool Used](#tool-used)
- [Data Cleaning](#data-cleaning)
- [Data Understanding and Exploration](#data-understanding-and-exploration)
- [Key Visualizations for EDA](#key-visualizations-for-eda)
- [Few interpretation of correlation matric](#few-interpretation-of-correlation-matric)
- [Modeling and Evaluation](#modeling-and-evaluation)
- [Visualization for Models](#visualization-for-models)
- [Conclusion and Recommendations](#conclusion-and-recommendations)
- [Reference](#reference)

### Project Overview
---
In this project, i will utilize the CRISP-DM framework to analyze and model the Miami housing dataset. The primary goal is to predict housing prices using historical data and various property features, thereby assisting stakeholders in making informed pricing decisions.

### Business Understanding
The business objective is to develop a robust predictive model that estimates the sale price of Miami properties. By understanding key factors such as floor area, land area, and additional property features, the model aims to support stakeholders in setting competitive listing prices.

### Dataset Source
The dataset was gotten from kaggle
[Download here](https://www.kaggle.com/datasets/deepcontractor/miami-housing-dataset/data)

### Tool Used
- R Programming

### Data Cleaning
- Columns 1, 2, and 5 were removed from the dataset to exclude unnecessary information and retain relevant features for analysis.
- Duplicates, outliers, and missing values have been addressed to ensure dataset accuracy.

### Data Understanding and Exploration
The Miami housing dataset comprises numerous features including SALE_PRC (sale price), LND_SQFOOT (land area), TOT_LVG_AREA (floor area), and several others. Exploratory Data Analysis (EDA) was conducted to understand the data distribution, relationships, and potential outliers.

### Key Visualizations for EDA
- Histogram of SALE_PRC:
![Screenshot (90)](https://github.com/user-attachments/assets/3307cb32-86e0-4e67-8f38-be585de50062)

The histogram of sale prices illustrates the distribution of property sale prices. It highlights a high concentration of lower-priced sales, with fewer properties in the higher price ranges.

- Histogram of LND_SQFOOT:
![Screenshot (91)](https://github.com/user-attachments/assets/082cfd8a-ea78-469f-9c70-91255acc8b6a)

The histogram illustrates the distribution of land area (LND_SQFOOT), showing that most properties have smaller land sizes, with fewer properties having significantly larger land areas.

- Scatter plot for SALE_PRC and TOT_AREA
![Screenshot (92)](https://github.com/user-attachments/assets/d50505dc-a99a-451d-9126-bda72d1a1c8c)

The scatter plot suggests a positive correlation between sale price and floor area (square feet), as larger floor areas tend to be associated with higher sale prices. However, the relationship is not perfectly linear, and there is some variability in the data.

- Correlation Matrix for Miami Housing Dataset
![Screenshot (93)](https://github.com/user-attachments/assets/7db37e02-9c2d-4698-8b02-86207d9fed55)

The correlation matrix visually and numerically represents pairwise correlations between key features of Miami housing data, illustrating both the strength and direction of relationships through color gradients and correlation values.
### Few interpretation of correlation matric
|Variable Pair|Correlation|Strength|Interpretation|
|-------------|-------------|--------|--------------|
|SALE_PRC & TOT_LVG_AREA|0.67|Strong|Larger floor areas lead to higher sale prices.|
|SALE_PRC & SPEC_FEAT_VAL|0.5|Moderate|Additional features increase house prices.|
|LND_SQFOOT & TOT_LVG_AREA|0.44|Moderate|Bigger land areas tend to have larger living spaces.|

### Modeling and Evaluation
Multiple regression-based models were implemented, including:
- Multiple Linear Regression
- Support Vector Regression (with various kernels)
- Decision Tree Regression
- Random Forest Regression
The dataset was divided into 70% for training and 30% for testing. The Random Forest Regression model with 200 trees achieved the lowest Root Mean Absolute Error (RMAE) of approximately 103,330, and was selected as the final model

### Visualization for Models
![Screenshot (94)](https://github.com/user-attachments/assets/90e7c749-efa3-4d2b-a8c4-3f65bfdd4aa6)

This bar chart compares the RMSE values across various regression models. It clearly demonstrates that the Random Forest Regression model with 200 trees achieved the lowest RMSE, indicating its superior performance in predicting housing prices. 

### Conclusion and Recommendations
The analysis confirms that the Random Forest Regression model with 200 trees provides the most accurate predictions for Miami housing prices. This model can be a valuable tool for stakeholders, enabling them to set more competitive listing prices. Future steps include deploying the model in a real-time environment and periodically updating it with new data.

### Reference
1. Chumbar, S. (2023). [Click here](https://medium.com/@shawn.chumbar/the-crisp-dm-process-a-comprehensive-guide-4d893aecb151)




