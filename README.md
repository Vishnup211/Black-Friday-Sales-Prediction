# Predicting Black Friday Sales: A Machine Learning Approach

## Introduction

Black Friday marks one of the most significant shopping events of the year, attracting millions of consumers eager for deals. This project aims to leverage machine learning techniques to predict sales during this event based on customer and product data. Using historical data, we develop a model that can forecast the amount spent by customers, helping retailers optimize their strategies.

## Dataset Overview

The dataset for this project is divided into two parts:
- **Train Data**: Contains historical sales data, customer demographics, and product categories.
- **Test Data**: Provides customer and product information without the purchase amounts, for which we need to make predictions.

### Features of the Dataset

1. **User_ID**: Unique identifier for each customer.
2. **Product_ID**: Unique identifier for each product.
3. **Gender**: Gender of the user.
4. **Age**: Age category of the user.
5. **Occupation**: Occupation code of the user.
6. **City_Category**: Category of the city where the user resides.
7. **Stay_In_Current_City_Years**: Duration the user has lived in the current city.
8. **Marital_Status**: Marital status of the user (0 for unmarried, 1 for married).
9. **Product_Category_1**: Main category of the product.
10. **Product_Category_2**: Secondary product category (with some missing values).
11. **Product_Category_3**: Tertiary product category (also with missing values).
12. **Purchase**: Amount spent by the user (the target variable).

## Methodology

### Data Preprocessing

1. **Loading Data**: We begin by loading the training and testing datasets using pandas.

2. **Handling Missing Values**: The dataset has some missing values in Product_Category_2 and Product_Category_3. We fill these with zeros to maintain consistency.

3. **Encoding Categorical Variables**: To convert categorical variables into a numerical format, we employ one-hot encoding for features like Gender, Age, and City_Category.

4. **Feature Selection**: We select relevant features for training, dropping non-informative columns like User_ID and Product_ID, and separating the target variable (Purchase).

### Model Selection and Training

We opt for the Random Forest Regressor, a robust ensemble learning method that effectively handles regression tasks:

1. **Splitting the Data**: The training data is divided into training and validation sets to evaluate the model’s performance.

2. **Training the Model**: The Random Forest model is trained on the training data. Hyperparameters such as the number of estimators (trees) are set to optimize the model.

3. **Validation**: We calculate the Root Mean Squared Error (RMSE) on the validation set to assess the model's accuracy. The model achieves an RMSE of approximately **3060.32**, indicating the average prediction error in sales.

### Making Predictions

Once the model is trained, we use it to make predictions on the test dataset. The predictions are then structured into a DataFrame for submission.

## Results and Conclusion

The machine learning model successfully predicts sales amounts based on customer and product information. The results show that leveraging historical data can provide valuable insights for retailers during high-stakes shopping events like Black Friday.

This project illustrates the power of data-driven decision-making and highlights the potential of machine learning in retail analytics. By employing similar techniques, retailers can refine their marketing strategies, optimize inventory, and enhance customer satisfaction.

## Future Work

Future enhancements could include:
- Incorporating additional features such as customer purchase history.
- Exploring other machine learning algorithms like Gradient Boosting or Neural Networks.
- Implementing a hyperparameter tuning process for better model optimization.

With continuous advancements in machine learning and data analysis, the opportunities for improving sales prediction models remain vast, paving the way for more sophisticated retail strategies.
