# Airline Customer Satisfaction Prediction Using Logistic Regression

## Project Overview

This project applies **Logistic Regression** to predict whether an airline passenger is **Satisfied** or **Dissatisfied** based on demographic information, travel characteristics, and service quality ratings.

The objective is not only to build a classification model, but also to identify the factors that most strongly influence customer satisfaction and translate those findings into practical business recommendations that can improve customer retention.

---

## Business Problem

Customer satisfaction is a key performance indicator in the airline industry. Understanding which aspects of the passenger experience contribute most to satisfaction enables airlines to prioritize investments that improve customer loyalty and overall service quality.

This project answers the following question:

> **Which airline services have the greatest influence on passenger satisfaction, and how accurately can satisfaction be predicted using Logistic Regression?**

---

# Dataset Overview

The dataset contains passenger survey responses covering:

* Customer demographics
* Travel characteristics
* Service quality ratings
* Flight delay information
* Customer satisfaction outcome

### Target Variable

* **Satisfied (1)**
* **Dissatisfied (0)**

---

# Project Objectives

This project aims to:

* Explore and understand the airline passenger dataset.
* Preprocess the data for classification modeling.
* Encode categorical variables into numerical form.
* Train a Logistic Regression classifier.
* Evaluate model performance using:

  * Confusion Matrix
  * Accuracy
  * Precision
  * Recall
* Identify the strongest drivers of customer satisfaction.
* Provide evidence-based recommendations for improving airline services.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# Methodology

## 1. Data Exploration

The dataset was inspected to understand:

* Dataset dimensions
* Feature types
* Missing values
* Duplicate records
* Target class distribution

---

## 2. Data Preprocessing

Several categorical variables were encoded into numerical values, including:

* Customer Type
* Type of Travel
* Class
* Satisfaction (Target)

The dataset was then divided into **80% training data** and **20% testing data** for unbiased model evaluation.

---

## 3. Logistic Regression Model

A Logistic Regression classifier was trained using the processed features to estimate the probability that a passenger belongs to the **Satisfied** class.

---

## 4. Model Evaluation

The trained model was evaluated using a confusion matrix together with classification metrics that provide deeper insight than accuracy alone.

### Model Performance

| Metric    | Score     |
| --------- | --------- |
| Accuracy  | **81.4%** |
| Precision | **82.3%** |
| Recall    | **84.3%** |

### Confusion Matrix

| Actual / Predicted | Dissatisfied |  Satisfied |
| ------------------ | -----------: | ---------: |
| Dissatisfied       |   **16,846** |  **3,630** |
| Satisfied          |    **3,605** | **19,895** |

### Interpretation

The model correctly classified:

* **19,895 satisfied passengers**
* **16,846 dissatisfied passengers**

while misclassifying:

* **3,630 dissatisfied passengers** as satisfied.
* **3,605 satisfied passengers** as dissatisfied.

Overall, the classifier demonstrates strong predictive performance and balanced error rates across both classes.

---

# Key Drivers of Customer Satisfaction

The Logistic Regression coefficients reveal which features most strongly influence customer satisfaction.

### Strongest Positive Drivers

| Rank | Feature                | Coefficient |
| ---- | ---------------------- | ----------: |
| 1    | Inflight entertainment |   **0.610** |
| 2    | Seat comfort           |   **0.303** |
| 3    | Ease of Online booking |   **0.288** |
| 4    | On-board service       |   **0.279** |
| 5    | Check-in service       |   **0.228** |

These variables increase the likelihood that a passenger reports being satisfied.

---

### Strongest Negative Drivers

| Rank | Feature                            | Coefficient |
| ---- | ---------------------------------- | ----------: |
| 1    | Customer Type                      |  **-2.520** |
| 2    | Class                              |  **-0.793** |
| 3    | Type of Travel                     |  **-0.616** |
| 4    | Departure/Arrival Time Convenience |  **-0.281** |
| 5    | Food and Drink                     |  **-0.192** |

These features were associated with lower satisfaction relative to their reference categories or lower ratings.

---

# Business Insights

The model indicates that **overall customer experience has a stronger influence on passenger satisfaction than operational factors such as flight delays.**

The most influential positive factors include:

* Inflight entertainment
* Seat comfort
* Online booking experience
* On-board service
* Check-in service

Interestingly, **arrival delay** and **departure delay** showed relatively small coefficients, suggesting that passengers place greater emphasis on service quality and comfort than on minor scheduling disruptions.

---

# Recommendations

Based on the model findings, the airline should prioritize investments in areas that most strongly influence passenger satisfaction.

### Improve Inflight Entertainment

Inflight entertainment produced the largest positive coefficient (**0.610**), making it the strongest predictor of customer satisfaction.

Possible improvements include:

* Expanding movie and TV selections.
* Improving entertainment system reliability.
* Offering personalized entertainment recommendations.

---

### Enhance Passenger Comfort

Seat comfort was the second strongest predictor (**0.303**).

Potential improvements include:

* Better seating ergonomics.
* Increased legroom where possible.
* Improved cabin comfort for long-haul flights.

---

### Simplify Digital Customer Experience

Ease of online booking (**0.288**) and online boarding (**0.086**) positively influenced satisfaction.

The airline should continue investing in:

* Mobile booking applications.
* Faster online check-in.
* User-friendly booking interfaces.

---

### Strengthen Customer Service

Higher ratings for:

* On-board service
* Check-in service

were consistently associated with higher satisfaction.

Investing in staff training and customer service quality could significantly improve passenger experience.

---

### Investigate At-Risk Customer Segments

Customer Type and Type of Travel exhibited strong negative coefficients.

Further analysis should identify which customer groups are less satisfied so that targeted loyalty programs and personalized service improvements can be developed.

---

# Project Visualizations

The notebook includes several visualizations to support the analysis.

## Dataset Exploration

Replace with your screenshot.

```text
images/
└── target_distribution.png
```

---

## Missing Value Analysis

Replace with your screenshot.

```text
images/
└── missing_values.png
```

---

## Confusion Matrix

Replace with your screenshot.

```text
images/
└── confusion_matrix.png
```

---

## Logistic Regression Coefficients

Replace with your coefficient bar chart.

```text
images/
└── logistic_coefficients.png
```

---

# Limitations

Although Logistic Regression provides interpretable coefficients, it assumes a linear relationship between predictors and the log-odds of customer satisfaction.

Future work could include:

* Hyperparameter tuning
* Feature selection
* Cross-validation
* Tree-based ensemble models such as Random Forest or XGBoost for performance comparison

---

# Conclusion

The Logistic Regression model achieved strong predictive performance, correctly classifying the majority of passengers while providing interpretable insights into the factors that influence customer satisfaction.

The analysis demonstrates that improving the **overall passenger experience**—particularly inflight entertainment, seat comfort, online services, and onboard service—is likely to have a greater impact on customer satisfaction than focusing solely on operational delay reductions.

---

## Author

**Latifah Bashir**

Completed as part of the **3MTT Data Science Program** to demonstrate the practical application of Logistic Regression for customer satisfaction prediction and data-driven business decision-making.
