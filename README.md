# <center> Multiple Linear Regression

### Machine learning and Python 

### TITLE: Sales Advertising Prediction

### AIM: To build and train a multiple linear mode to predict Sales Revenue.

### Problem Statement: To help businesses to allocate their marketing budget more effectively, ultimately maximizing their revenue and optimizing advertising strategies.

### Data Description: This dataset gotten from kaggle.com, comes from the advertising industry and contains information on advertising expenditures across three different media channels: TV, radio, and newspapers, along with the corresponding sales revenue for each record.
- Data Source: [Advertising Dataset | Kaggle](https://www.kaggle.com/datasets/ashydv/advertising-dataset)
- Total Sample: 200 data point
- Number of Columns: 4 columns including TV, Newspaper, Radio and the target variable Sales.

### Development Process:
Data loading and preparation: Libraries such as Pandas, NumPy (for data manipulation), matplotlib.pyplot (for visualization), sklearn.model_selection (for splitting the dataset), and sklearn (model evaluation) are imported.

### Exploratory Data Analysis (EDA):
1. Descriptive Statistics
- Summary statistics were generated to provide insights into each variable, including mean, median, minimum, maximum, and standard deviation.
2. Correlation Analysis
- A correlation matrix was computed to assess the linear relationships between the advertising channels and sales.
- Strong positive correlations were observed between TV and Sales, and moderate correlations between Radio and Sales. Newspaper showed a weak correlation with sales.

![image](https://github.com/user-attachments/assets/0346ef8d-4a49-4161-8e0d-df136adf9b96)

3. Visualization

 Scatter plots were created to visualize the relationship between each advertising channel and sales revenue:

     - TV vs. Sales: Strong positive trend
     - Radio vs. Sales: Moderate positive trend
     - Newspaper vs. Sales: Weak trend
  
  A regression plot was also generated for the variables, confirming the significant influence of TV advertising on sales.

### Model Development: The development of the multiple linear regression models for this project followed an iterative approach, progressing from initial experimentation to more rigorous validation:
  - Initial Model Building (linreg1 to linreg3): In the early stages of the model development, multiple linear regression models were built using the entire dataset without splitting it into training and testing sets. This approach allowed us to;
Explore the relationship between the independent variables and the target variable, and to Establish a baseline model by understanding the contribution of each advertising channel to sales.

      While this phase provided valuable insights, it came with the risk of overfitting, as the models were evaluated on the same data used for training. This meant the initial models were not tested on unseen data, limiting their generalization ability.

  - Train_Test Splitting for Model Validation (linreg4 to linreg6): The dataset was later split into training and testing sets to address overfitting and validate the model's performance. The models were then trained on the training set and evaluated on the testing set. This allowed us to;
Train the multiple linear regression models on some of the data (training set).
Test the models on the unseen data (testing set) to assess their predictive performance.
This stage ensured that the final models not only fit the training data well but also generalized effectively to new data, reducing the risk of overfitting and improving the model's robustness.

### Model Evaluation:
The following key metrics were used to evaluate the models accuracy and predictive capability:

- Root mean Squared Error (RMSE): This metric is used to measure the average difference between the actual sales and the predicted sales by the model.
- R² Score: The R² score was calculated to determine how well the model explains the variability in the sales data.
- Coefficients: The model’s coefficients were analyzed to understand the impact of each advertising channel (TV, Radio, and Newspaper) on sales.
- Intercept: The intercept value was evaluated to determine the predicted sales when all advertising spend is zero.

### Evaluation Result:
Model Performance:
- linreg4: The model shows an average prediction error of 1.54 units (RMSE) and explains 90% of the variance in sales, indicating strong predictive accuracy.
- linreg5: This model achieved the lowest prediction error, with an RMSE of 1.53 units, while also explaining 90% of the variance in sales, demonstrating high precision.
- linreg6: The model has an RMSE of 2.22 units and explains 80% of the variance in sales, performing slightly less accurately compared to linreg4 and linreg5.

### Conclusion:
The multiple linear regression models for the Advertising dataset provide robust predictions, with linreg5 offering the highest accuracy and strongest fit. linreg4 also performs well, while linreg6 captures slightly less variability but still provides meaningful predictions. These results suggest that the models are well-suited for predicting sales based on advertising expenditures.
