# House-price-Prediction-
Predict house prices using property features such as size, bedrooms, and location. Dataset: House Price Prediction Dataset (available on Kaggle)
## **House Price Prediction Project**

### **Introduction**

In this project, I aimed to predict house prices using a dataset that includes features such as area, number of bedrooms, bathrooms, and location. The objective was to build a machine learning pipeline capable of processing raw data and generating accurate price predictions.

---

### **Steps Followed**

#### **1. Data Preprocessing**

I began by cleaning the dataset. The *Id* column was removed because it does not contribute to prediction. I also checked for missing values to ensure the dataset was complete and ready for modeling.

#### **2. Feature Engineering**

To improve model performance, I created additional features:

* **house_age**: Calculated by subtracting the construction year from the current year.
* **total_rooms**: Computed by adding the number of bedrooms and bathrooms.

These features help provide more meaningful information to the model.

#### **3. Handling Categorical Data**

Since machine learning models require numerical input:

* The **Location** column was transformed using One-Hot Encoding.
* The **Condition** column (Poor, Fair, Good, Excellent) was mapped to numerical values.
* The **Garage** column (Yes/No) was converted into binary form (1/0).

#### **4. Model Training**

I trained two different models to compare performance:

* Linear Regression
* Gradient Boosting Regressor

The dataset was split into:

* **80% training data**
* **20% testing data**

---

### **Results**

The model performance was evaluated using standard metrics:

* **MAE (Mean Absolute Error):** ~247,348
* **RMSE (Root Mean Squared Error):** ~285,604
* **R² Score:** -0.048

---

### **Analysis and Conclusion**

Although the implementation and preprocessing steps were correct, the model produced a negative R² score. Upon further analysis, I found that key features such as *Area* and *Bedrooms* have almost zero correlation with the target variable (*Price*).

This indicates that:

* The dataset does not contain meaningful relationships between features and price.
* The price values appear to be randomly distributed.

As shown in the heatmap, the correlation between **Price** and important features is nearly **0.00**, which explains why the model fails to learn any pattern.

---

### **Final Remarks**

Even though the model performance is poor, this project was valuable for understanding the complete machine learning workflow, including:

* Data preprocessing
* Feature engineering
* Encoding techniques
* Model training and evaluation
* Data visualization

---
---
