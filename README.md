# 🚲 Seoul Bike Sharing Demand Prediction

![BDP_Project_image](https://github.com/user-attachments/assets/643d039e-f80e-4f65-9f3c-882b52211d6f)


## 📌 Project Type  

**Supervised Machine Learning – Regression Problem**  

**Author:** Ankesh Aman  


---

## 🧠 Problem Statement

Rental bikes are increasingly being introduced in many urban cities to enhance mobility comfort. One key challenge is ensuring availability by predicting bike demand accurately across different hours of the day.

The goal of this project is to **predict the hourly bike rental demand** based on time-related features and weather conditions. This aids in **resource planning**, **re-balancing bikes**, and **reducing customer waiting times**.

---


## 🗃️ Dataset Description

The dataset used in this project contains records of bike rentals and various contextual features collected from Seoul, South Korea. Key features include:

### 📅 Time Features
- `Date`: The date of observation.
- `Hour`: Hour of the day (0 to 23).
- `Seasons`: Spring, Summer, Autumn, Winter.
- `Holiday`: Whether the day is a holiday.
- `Functioning Day`: Whether bike rentals were functioning on that day.

### 🌦 Weather Features
- `Temperature`, `Humidity`, `Windspeed`, `Visibility`, `Rainfall`, `Snowfall`
- `Dew point temperature`, `Solar Radiation`

### 🎯 Target Variable
- `Rented Bike Count`: The number of rented bikes per hour.

---


## 🧹 Data Cleaning & Preprocessing

- **Datetime Conversion:** Converted string to datetime object for feature extraction.
- **Missing Values:** Dataset had no missing values.
- **Label Encoding:** Categorical features like `Seasons`, `Holiday`, and `Functioning Day` were label encoded.
- **Feature Scaling:** Applied normalization on numerical features using StandardScaler.
- **Outlier Removal:** Identified and handled outliers in weather-related variables.

## 🤖 Model Building & Evaluation

The following regression models were used:

| Model               | MSE       | RMSE     | R² Score | Adjusted R² |
|--------------------|-----------|----------|----------|-------------|
| Linear Regression  | 86.40     | 9.29     | 0.4531   | 0.4506      |
| Ridge Regression   | 86.39     | 9.29     | 0.4531   | 0.4506      |
| Lasso Regression   | 90.61     | 9.52     | 0.4264   | 0.4238      |
| Random Forest      | 51.84     | 7.20     | 0.6718   | 0.6703      |

> ✅ **Random Forest** performed best in terms of both RMSE and R² Score, accurately capturing the complex relationships in the data.

---
## ✅ Final Conclusion

This project successfully explored and implemented various machine learning regression techniques to predict the hourly demand for bike rentals in Seoul. Through a detailed exploratory data analysis and rigorous modeling process, several key insights were uncovered:

- **Bike rentals peak during evening hours (around 6 PM)** and during **summer seasons**.
- **Weather conditions** such as **no rainfall/snowfall**, **temperatures between 15–30°C**, and **moderate humidity (30%–70%)** are ideal for bike rentals.
- Rentals are significantly higher on **non-holidays**, making calendar features an important aspect of demand forecasting.

Among the models tested:
- **Random Forest Regression** performed best with an R² score of **0.6718**, capturing non-linear patterns and feature interactions effectively.
- **Lasso Regression**, being more constrained, underperformed with the lowest R² of **0.4264**.
- **Temperature** and **Hour of the day** consistently emerged as the most impactful features across all models.

Model interpretability was addressed using the **SHAP library**, which provided detailed feature impact analysis and enhanced transparency in decision-making.

### 🧩 Challenges Addressed
- Dealt with **outliers** and cleaned anomalies in weather features.
- Applied **label encoding** to convert categorical variables.
- Tackled **multicollinearity** to ensure stable and interpretable models.
- Chose **SHAP** as the model explainability framework to understand model behavior.

> 🚀 This project not only demonstrates accurate forecasting using ensemble models but also highlights the importance of explainability in machine learning systems—ensuring trust and accountability when such models are deployed in real-world smart city applications.


---

## 🛠 Tools & Technologies Used

| Tool / Library       | Purpose                           |
|----------------------|-----------------------------------|
| Python               | Programming language              |
| Pandas, NumPy        | Data manipulation and analysis    |
| Matplotlib, Seaborn  | Data visualization                |
| Scikit-learn         | Model building and evaluation     |
| XGBoost              | Gradient boosting implementation  |
| Jupyter Notebook     | Interactive development           |

---


## 🚀 How to Run This Project

1. **Clone the Repository**
   ```
   git clone https://github.com/yourusername/Seoul-Bike-Sharing-Demand-Prediction.git
   ```
2. Navigate to Project Folder
   ```
   cd Seoul-Bike-Sharing-Demand-Prediction
   ```
3. Run the Notebook
   ```
   jupyter notebook Bike_Sharing_Demand_Prediction_Capstone_Project_By_Ankesh_Aman.ipynb
   ```
---




