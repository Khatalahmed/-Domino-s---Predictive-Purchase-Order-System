# 🍕 Domino's Predictive Purchase Order System

## 📈 Problem Statement
This project focuses on optimizing Domino's inventory management by building a predictive system that forecasts pizza sales and generates purchase orders for ingredients. By leveraging historical sales data, the goal is to develop a model that accurately predicts future sales, allowing Domino's to order the right amount of ingredients, minimizing waste, and preventing stockouts.

## 🎯 Objective
- Develop a predictive model to forecast pizza sales.
- Create a purchase order system that calculates the required quantities of ingredients based on the sales forecast.

## 🔍 Dataset Overview
The project involves two datasets: **Pizza Sales** and **Pizza Ingredients**.

### **Pizza Sales Dataset**
- **Total Entries**: 48,620
- **Columns**:  
  - `pizza_id`: Unique identifier for the sale  
  - `order_id`: Links to a specific order  
  - `pizza_name_id`: Unique identifier for each pizza  
  - `quantity`: Number of pizzas sold  
  - `order_date`, `order_time`: When the sale occurred  
  - `unit_price`, `total_price`: Pricing details  
  - `pizza_size`, `pizza_category`: Size and type of pizza  

### **Pizza Ingredients Dataset**
- **Total Entries**: 518
- **Columns**:  
  - `pizza_name_id`: Unique identifier for each pizza  
  - `pizza_name`: Name of the pizza  
  - `pizza_ingredients`: List of ingredients  
  - `Items_Qty_In_Grams`: Quantity of each ingredient used  

📥 **Download Datasets:**  
- [Pizza Sales Dataset](#)  
- [Pizza Ingredients Dataset](#)  

## 📊 Metrics
- **Mean Absolute Percentage Error (MAPE):** Used to evaluate the accuracy of forecasting models. It measures the average absolute percentage error between the predicted values and the actual values.

## 💡 Business Use Cases
- **Inventory Management:** Ensuring optimal stock levels to meet future demand without overstocking.  
- **Cost Reduction:** Minimizing waste and reducing costs associated with expired or excess inventory.  
- **Sales Forecasting:** Accurately predicting sales trends to inform business strategies and promotions.  
- **Supply Chain Optimization:** Streamlining the ordering process to align with predicted sales and avoid disruptions.  

## 🛠️ Approach
### **I. Data Preprocessing**
#### **Data Cleaning:** Ensures dataset accuracy and consistency through:
- **Handling Missing Data:**  
  - Detected missing values.  
  - Replaced missing values using mean, median, mode, or placeholders.  
  - Removed columns or rows with excessive missing data if necessary.  
- **Removing Inconsistent Data:**  
  - Checked for format consistency and valid ranges.  
  - Fixed inconsistencies, such as standardizing text and correcting typos.  
- **Handling Outliers:**  
  - Identified outliers using statistical methods or visualizations.  
  - Removed, transformed, or categorized outliers based on their impact.  

### **II. Exploratory Data Analysis (EDA)**
Exploratory Data Analysis (EDA) helps discover patterns, relationships, and anomalies in the data.  
- **Visualization Techniques:**  
  - Time series plots for sales trends.  
  - Box plots for identifying outliers.  
  - Correlation heatmaps to understand relationships between variables.  
- **Seasonality & Trend Analysis:**  
  - Identified peak sales periods (e.g., weekends, holidays, promotional days).  
  - Detected patterns in ingredient demand.  

### **III. Sales Prediction & Modeling**
- **Feature Engineering:**  
  - Created relevant features like day of the week, month, promotional periods, and holiday effects.  
- **Model Selection:**  
  - Evaluated various forecasting models: **ARIMA, SARIMA, Prophet, LSTM, Regression Models.**  
- **Model Training & Evaluation:**  
  - Trained the model using historical sales data.  
  - Used **Mean Absolute Percentage Error (MAPE)** to evaluate accuracy.  

### **IV. Purchase Order Generation**
- **Sales Forecasting:** Predicted pizza sales for the next week.  
- **Ingredient Calculation:** Determined the required quantities of each ingredient based on the predicted sales and ingredient dataset.  
- **Purchase Order Creation:** Generated a detailed purchase order listing the quantities of each ingredient needed for the predicted sales period.  

## 📜 Results
- **Accurate Sales Predictions:** Improved inventory forecasting.  
- **Efficient Purchase Orders:** Ensured optimal ingredient stocking, reducing waste.  
- **Data-Driven Decision Making:** Improved cost savings and supply chain efficiency.  

## 🏗️ Tech Stack
- **Programming Languages:** Python  
- **Libraries & Frameworks:** Pandas, Scikit-learn, Statsmodels, TensorFlow, Matplotlib, Seaborn  
- **Machine Learning Techniques:** Time Series Forecasting, Regression Modeling, Deep Learning (LSTM)  
- **Tools:** Jupyter Notebook, GitHub, SQL  

## 🚀 Getting Started
### Prerequisites
- Python 3.8+  
- Jupyter Notebook / VS Code  
- Install dependencies:  
  ```sh
  pip install pandas numpy scikit-learn matplotlib seaborn statsmodels tensorflow
