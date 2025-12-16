# pizza-analysis
pizza analysis using messy data
# 🍕 Pizza Price Prediction using Random Forest

This project analyzes a pizza dataset and builds a **machine learning model** to predict pizza prices based on company, size, toppings, diameter, variants, and extra options.

---

## 📌 Project Overview

The goal of this project is to:

* Perform **data cleaning and preprocessing** on a real-world pizza dataset
* Conduct **exploratory data analysis (EDA)** using visualizations
* Encode categorical variables for machine learning
* Train a **Random Forest Regressor** to predict pizza prices
* Evaluate the model using **MAE** and **R² score**

---

## 📂 Dataset Information

* Total records: **129**
* Total features: **9**

### Columns:

| Column          | Description                                  |
| --------------- | -------------------------------------------- |
| company         | Pizza company (A–E)                          |
| price_rupiah    | Pizza price in Rupiah (target variable)      |
| diameter        | Pizza diameter in inches                     |
| topping         | Type of topping                              |
| variant         | Pizza variant                                |
| size            | Pizza size (small, medium, large, XL, jumbo) |
| extra_sauce     | Extra sauce option                           |
| extra_cheese    | Extra cheese option                          |
| extra_mushrooms | Extra mushrooms option                       |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas & NumPy** – data handling
* **Matplotlib & Seaborn** – visualization
* **Scikit-learn** – preprocessing & modeling

---

## 🧹 Data Preprocessing Steps

1. Removed currency symbols (`Rp`, `,`) from `price_rupiah` and converted it to integer
2. Removed `inch` from `diameter` and converted it to float
3. Encoded `company` using manual mapping
4. Encoded categorical features using **LabelEncoder**:

   * topping
   * variant
   * size
   * extra_sauce
   * extra_cheese
   * extra_mushrooms
5. Checked and confirmed **no missing values**

---

## 📊 Exploratory Data Analysis (EDA)

* Bar plots were used to analyze:

  * Average price by topping
  * Price variation across companies

### Key Insights:

* Certain toppings have higher average prices, indicating premium ingredients
* Larger sizes (XL, Jumbo) are more expensive than smaller sizes
* Variants influence pricing, suggesting premium options cost more

---

## 🤖 Machine Learning Model

* **Model:** RandomForestRegressor
* **Target Variable:** `price_rupiah`
* **Train-Test Split:** 80% training / 20% testing

### Features Used:

All columns except `price_rupiah`

---

## 📈 Model Evaluation

| Metric                    | Value             |
| ------------------------- | ----------------- |
| Mean Absolute Error (MAE) | **11,135 Rupiah** |
| R² Score                  | **0.88**          |

### Interpretation:

* The model predictions are, on average, about **11,135 Rupiah** away from actual prices
* An **R² score of 0.88** means the model explains **88% of the variance** in pizza prices

---

## ✅ Conclusion

* The Random Forest model performs well in predicting pizza prices
* Pricing is strongly influenced by **size, toppings, and variants**
* Visual analysis supports the model’s findings

---

#
## 👤 Author

**Ashim Maharjan**
Data Science Student

---

⭐ If you like this project, feel free to star the repository!
