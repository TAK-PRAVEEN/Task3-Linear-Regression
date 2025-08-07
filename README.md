# Linear Regrssion
---

**1. What assumptions does linear regression make?**

Linear regression, a powerful statistical method for modeling the relationship between a dependent variable and one or more independent variables, relies on several key assumptions to ensure the validity and reliability of its results. Here are the core assumptions:

1. Linearity:
The relationship between the independent variables and the dependent variable must be linear. This means the model assumes a straight-line relationship, and the change in the dependent variable is proportional to the change in the independent variable. You can often check this assumption visually using scatter plots of the dependent variable against each independent variable.
2. Normality:
The residuals (the differences between the observed and predicted values) must be normally distributed.
![licensed-image](https://github.com/user-attachments/assets/69be579e-95da-4ee2-b495-b9e74e65dfc0)
This is an important assumption, especially for hypothesis testing and constructing confidence intervals. Histograms or Q-Q plots of the residuals are useful tools for checking for normality.
3. Homoscedasticity:
The variance of the residuals should be constant across all levels of the independent variables. In simpler terms, the spread of the residuals should be roughly the same throughout the range of the predicted values. A plot of residuals against fitted values can help detect heteroscedasticity, where the spread of residuals changes.
4. Independence of Errors:
The residuals should be independent of each other. This assumption is often violated in time-series data, where consecutive observations may be correlated. The Durbin-Watson statistic is a common test for checking for autocorrelation (correlated errors).
5. No Multicollinearity:
The independent variables should not be highly correlated with each other. Multicollinearity can make it difficult to determine the individual effect of each independent variable and can lead to unstable coefficient estimates. The Variance Inflation Factor (VIF) is a common metric used to detect multicollinearity. A VIF value greater than 5 or 10 is often a cause for concern.

---

**2. How do you interpret the coefficients?**

Coefficients in a linear regression model represent the change in the dependent variable for a one-unit increase in the corresponding independent variable, assuming all other independent variables are held constant.

For example, in a model predicting house price, a coefficient of 50 for the 'square footage' variable means that for every additional square foot, the house price is expected to increase by $50, holding all other factors (like the number of bedrooms, location, etc.) constant.

---

**3. What is R2 score and its significance?**

The $$R^2$$ score, or the coefficient of determination, is a statistical measure that represents the proportion of the variance in the dependent variable that's predictable from the independent variables. It ranges from 0 to 1, or 0% to 100%.
- An $$R^2$$ of 0.85 means that 85% of the variability in the dependent variable can be explained by the model's independent variables.
- The significance of $$R^2$$ lies in its ability to quantify how well the model fits the data. A higher $$R^2$$ generally indicates a better fit, but it doesn't necessarily mean the model is a good one. It's crucial to consider other factors like the p-values of the coefficients and the overall context of the problem.

---

**4. When would you prefer MSE over MAE?**

- MSE (Mean Squared Error) is the average of the squared differences between the predicted and actual values.
- MAE (Mean Absolute Error) is the average of the absolute differences between the predicted and actual values.
You would prefer MSE over MAE when you want to penalize larger errors more heavily. Because MSE squares the errors, it gives a disproportionately higher weight to outliers. This makes it a good choice if large errors are particularly undesirable or if you have a lot of outliers that you want to highlight.

---

**5. How do you detect multicollinearity?**

Multicollinearity can be detected using the Variance Inflation Factor (VIF). The VIF for a particular independent variable measures how much the variance of the estimated regression coefficient is inflated due to its linear relationship with the other independent variables.
- A VIF value of 1 means there is no correlation among the independent variables.
- A VIF value greater than 5 or 10 is generally considered an indicator of high multicollinearity.

---

**6. What is the difference between simple and multiple regression?**

- Simple linear regression involves one independent variable and one dependent variable. It models the relationship between two variables.
- Multiple linear regression involves two or more independent variables and one dependent variable. It models the relationship between a dependent variable and a set of predictors.
  
---

**7. Can linear regression be used for classification?**

No, linear regression is not used for classification. Linear regression is a supervised learning algorithm designed for regression tasks, where the goal is to predict a continuous numerical value.
![licensed-image](https://github.com/user-attachments/assets/a0789681-9d53-47a6-8afe-b0bb13d13a80)
Classification tasks, where the goal is to predict a categorical label (e.g., 'spam' or 'not spam'), require different algorithms like Logistic Regression or Support Vector Machines (SVMs).
  
---

**8. What happens if you violate regression assumptions?**

Violating the assumptions of linear regression can have several negative consequences:
- Biased or inefficient coefficient estimates: The model's coefficients may not accurately reflect the true relationships between the variables.
- Incorrect hypothesis tests and confidence intervals: The p-values and confidence intervals may be unreliable, leading to false conclusions about the significance of the independent variables.
- Poor predictive performance: The model may not generalize well to new data, leading to inaccurate predictions.
- Incorrect interpretation: The assumptions are the foundation for interpreting the model's coefficients and statistical tests. When they are violated, the interpretations can be misleading.

---
