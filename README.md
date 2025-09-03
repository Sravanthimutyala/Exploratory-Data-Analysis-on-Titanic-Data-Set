# Exploratory-Data-Analysis-on-Titanic-Data-Set

 ## 🛳 Titanic Survival Prediction.

## 📌 Project Overview

This project analyzes the famous **Titanic dataset** to understand which factors influenced passenger survival. It includes:

* **Exploratory Data Analysis (EDA)** → understanding distributions, correlations, and survival patterns.
* **Feature Engineering** → creating new features (age groups, fare groups).
* **Machine Learning Models** → Logistic Regression & Random Forest for survival prediction.

---

## 📂 Dataset Information

The dataset contains **891 passenger records** with the following features:

| Column          | Description                                                          |
| --------------- | -------------------------------------------------------------------- |
| **survived**    | Target variable → 0 = did not survive, 1 = survived                  |
| **pclass**      | Ticket class (1st, 2nd, 3rd)                                         |
| **sex**         | Gender (male/female)                                                 |
| **age**         | Passenger age                                                        |
| **sibsp**       | # of siblings/spouses aboard                                         |
| **parch**       | # of parents/children aboard                                         |
| **fare**        | Ticket fare                                                          |
| **embarked**    | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |
| **age\_group**  | Derived feature: Child, Teenager, Adult, Senior                      |
| **fare\_group** | Derived feature: Low, Medium, High, Very High                        |

---

## 🔍 Exploratory Data Analysis (EDA)

* **Univariate Analysis:**

  * Most passengers were male, adults, and from 3rd class.
  * Fare distribution showed extreme outliers, handled via binning into groups.

* **Bivariate Analysis:**

  * Survival rates were higher for **females**, **1st class**, and **children**.
  * Passengers with **high/very high fares** had higher survival chances.
  * Ports of embarkation showed slight survival differences (C > Q/S).

* **Multivariate Analysis:**

  * Correlation heatmap showed survival strongly linked with **sex** and **pclass**.
  * Feature interactions confirmed "women and children in 1st class" had the best odds.

 * **Handling Missing Values:**
    * Age and Embarked Columns Consists of Missing Values
    * The column "deck" is dropped, since it has high number of missing values.
---

## ⚙️ Feature Engineering

* **Age groups** created: Child, Teenager, Adult, Senior.
* **Fare groups** created using quantile binning: Low, Medium, High, Very High.
* **Encoding:** Applied one-hot encoding for categorical variables (drop\_first=True) and label encoder for the Sex, Embarked.

---

## 🤖 Machine Learning Models

1. **Logistic Regression**

   * Accuracy: \~78% (varies by split).
   * Insights:

     * Being **male** and in **3rd class** strongly decreased survival odds.
     * **Children** and **high-fare passengers** had higher odds.

2. **Random Forest Classifier**

   * Accuracy: \~82% (better performance).
   * Feature Importance:

     * **Sex**, **pclass**, **fare\_group**, and **age\_group** were most important.

---

## 📊 Key Insights

* **Women, children, and 1st-class passengers with high fares** had the best chance of survival.
* **Men, seniors, and 3rd-class passengers** had the lowest survival chances.
* **Socio-economic status (class + fare)** was a critical survival factor.

