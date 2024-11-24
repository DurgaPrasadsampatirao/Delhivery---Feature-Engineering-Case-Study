# Delhivery - Feature Engineering Case Study

## Project Overview
This case study focuses on applying feature engineering techniques to improve predictive modeling for Delhivery, a leading logistics and supply chain company. The project involves analyzing Delhivery's data, identifying relevant features, and engineering new ones to enhance the performance of machine learning models. The goal is to improve delivery time predictions, optimize route planning, and provide data-driven insights into logistics operations.

Project link: [Delhivery - Feature Engineering Case Study](https://colab.research.google.com/drive/18mMNGDXet5W7qVBSPwE_Cw_b7eqEUyKP?usp=sharing)

---

## Key Objectives
1. **Data Cleaning**: Handle missing values, outliers, and duplicates to ensure a clean dataset for analysis and modeling.
2. **Feature Extraction**: Extract meaningful features from raw data (e.g., order details, delivery routes, and timestamps).
3. **Feature Transformation**: Apply techniques like normalization, scaling, and encoding to prepare the data for modeling.
4. **Feature Engineering**: Create new features that capture essential patterns, such as delivery speed, distance, and time of day.
5. **Modeling and Evaluation**: Use machine learning algorithms to test the engineered features' impact on model performance.

---

## Insights and Findings

### 1. Data Overview
- **Dataset**: The dataset includes historical delivery data, including order details, delivery times, customer demographics, and route information.
- **Key Features**:
  - `Order_ID`: Unique identifier for each delivery.
  - `Delivery_Time`: Actual delivery time taken to fulfill the order.
  - `Distance`: Distance between the origin and destination.
  - `Package_Size`: Size or weight of the package.
  - `Order_Date`: Date and time when the order was placed.
  - `Delivery_Status`: Status of the delivery (e.g., delivered, delayed).
  
### 2. Data Cleaning
- **Handling Missing Values**: Missing values were imputed using the mean, median, or forward/backward fill based on the data type.
- **Outlier Detection**: Outliers in delivery times and distances were identified using IQR and Z-score methods.
- **Data Transformation**: Timestamps were converted into more meaningful features like day of the week, month, and hour of the day.

### 3. Feature Extraction
- **Time-Based Features**: Created features such as `Day_of_Week` and `Hour_of_Day` to capture patterns in delivery times based on the time of order placement.
- **Distance Features**: Generated features related to the geographical distance between the source and destination (e.g., `Distance_to_City_Center`).
- **Customer Demographics**: Extracted customer location-based features like `Region`, `Urban/Rural`, and `Customer_Type`.

### 4. Feature Transformation
- **Scaling and Normalization**: Applied Min-Max scaling and Standardization techniques to continuous variables like `Distance` and `Package_Size`.
- **Encoding Categorical Variables**: Used one-hot encoding and label encoding for categorical variables like `Delivery_Status` and `Region`.
  
### 5. Feature Engineering
- **Delivery Speed**: Created a new feature `Delivery_Speed` as a ratio of `Distance` to `Delivery_Time`, capturing the efficiency of the delivery process.
- **Time to Delivery**: Created a feature `Time_to_Delivery` by calculating the time difference between the order date and delivery date.
- **Route Optimization**: Created `Route_Optimization_Score`, a custom metric to evaluate the efficiency of the route used for delivery.
  
### 6. Modeling and Evaluation
- **Model Selection**: Machine learning models, including Random Forest, XGBoost, and Gradient Boosting, were trained to predict delivery times and identify factors influencing delays.
- **Model Evaluation**: The performance of the models was evaluated using metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-Squared.

---

## Methodology
1. **Data Collection**: The dataset is sourced from Delhivery's internal logs, containing historical delivery and route data.
2. **Preprocessing**: Data cleaning, outlier handling, and transformation were performed to ensure the dataset was suitable for machine learning models.
3. **Feature Engineering**: Various features were created from raw data, focusing on time, distance, customer demographics, and logistical efficiency.
4. **Modeling**: Multiple machine learning models were tested and evaluated to understand the impact of feature engineering on performance.

---

## Technologies Used
- **Python**: For data cleaning, feature engineering, and building machine learning models.
- **Libraries**: Pandas, Numpy, Scikit-learn, XGBoost, Matplotlib, Seaborn
- **Jupyter Notebooks**: For analysis and model building.
- **SQL**: For querying and extracting data from databases.

