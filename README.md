# Ames Housing Sales- Linear Regression Project

This is my project for predicting house prices using Linear Regression. I used the Ames Housing Sales dataset to see how adding categorical features (like neighborhoods and house styles) affects the model's accuracy.

## The Problem: The 10^19 Error:
While building this, the model's Mean Squared Error (MSE) exploded to $10^{19}$ . This happened because of the **"dummy variable trap."** By keeping every single category, I created perfect multicollinearity, which makes the linear regression math break. I fixed this by using `drop='first'` in my One-Hot Encoder to stabilize the model.



## What I did in the Notebook
* **Encoding:** I converted text categories into numbers using One-Hot Encoding (with the fix mentioned above).
* **Scaling:** I tested `StandardScaler` vs `MinMaxScaler` to see if it improved the fit.
* **Comparison:** I compared a basic numerical model against the optimized version that includes categorical data.
* **Visual Proof:** I made side-by-side scatter plots showing the "Actual vs. Predicted" prices. You can see the optimized model is way more accurate.


* **Dataset:** https://www.kaggle.com/datasets/saurabh0/ames-housing-sales
* **View on Kaggle:** https://www.kaggle.com/code/ishmeetk13/ames-housing-sales-prediction
