Here is a comprehensive and professional `README.md` file tailored for your GitHub repository. It documents both the web scraping/analysis task and the predictive modeling task based on the files you provided.

---

# ✈️ British Airways Data Science Project

This repository contains the work for the **British Airways Data Science Virtual Internship** (via Forage). The project focuses on scraping customer review data to uncover insights and building a predictive model to understand factors influencing customer booking behavior.

## 📌 Project Overview

This project is divided into two main tasks:

1. **Web Scraping & Data Analysis:** Scraping customer reviews from Skytrax, cleaning the data, and performing sentiment analysis to identify key themes in customer feedback.
2. **Predictive Modeling:** Analyzing customer booking data to build a machine learning model that predicts whether a customer will complete a booking.

## 📂 Repository Structure

| File | Description |
| --- | --- |
| `BA_Data_Scraping.py` | Python script using `BeautifulSoup` and `requests` to scrape review data from Skytrax. |
| `British_Airways_Data.csv` | The raw dataset containing scraped customer reviews (Output of scraping script). |
| `British_Airways_Task1.ipynb` | Jupyter Notebook for data cleaning, exploratory data analysis (EDA), and sentiment analysis/word clouds. |
| `customer_booking.csv` | Dataset containing customer booking information (purchase lead time, route, baggage, etc.). |
| `British_Airways_Task2.ipynb` | Jupyter Notebook for training a machine learning model to predict booking completion. |

## 🛠️ Installation & Requirements

To run the analysis locally, ensure you have Python installed along with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn requests beautifulsoup4 scikit-learn

```

## 📊 Task 1: Web Scraping & Customer Review Analysis

### **Objective**

Scrape and analyze customer reviews to understand customer sentiment regarding British Airways services.

### **Key Steps**

* **Scraping:** Collected reviews from [Skytrax](https://www.airlinequality.com/) using `BA_Data_Scraping.py`.
* *Data collected:* Reviewer Name, Date, Review Text, Rating, Recommended (Yes/No).


* **Data Cleaning:** Handled missing values and formatted date columns.
* **Analysis:**
* Generated Word Clouds to visualize frequent keywords.
* Analyzed sentiment trends (Positive vs. Negative feedback).



## 🤖 Task 2: Predictive Modeling of Customer Bookings

### **Objective**

Build a high-quality predictive model to predict successful bookings (`booking_complete` = 1) based on customer behavior and flight details.

### **Dataset (`customer_booking.csv`)**

Features include:

* `num_passengers`: Number of travellers.
* `sales_channel`: Internet vs. Mobile.
* `trip_type`: Round Trip, One Way, Circle Trip.
* `purchase_lead`: Days between booking and travel.
* `length_of_stay`, `flight_hour`, `flight_day`.
* `wants_extra_baggage`, `wants_preferred_seat`, `wants_in_flight_meals`.

### **Modeling Approach**

* **Preprocessing:** Encoding categorical variables (e.g., `sales_channel`, `route`) and handling imbalanced data.
* **Algorithm:** Trained a Classification Model (e.g., Random Forest) to classify bookings.
* **Evaluation:**
* Confusion Matrix to visualize True Positives/Negatives.
* Accuracy, Precision, Recall, and F1-Score metrics.
* Feature Importance plot to identify the most critical factors driving bookings.



## 🚀 Usage

1. **Run the Scraper:**
```bash
python BA_Data_Scraping.py

```


2. **Run the Analysis Notebooks:**
Open `British_Airways_Task1.ipynb` or `British_Airways_Task2.ipynb` in Jupyter Notebook or VS Code to reproduce the analysis and model training.

## 📈 Key Insights

* **Reviews:** Service-related keywords (e.g., "Staff", "Service", "Food") are strong drivers of negative sentiment.
* **Bookings:** Factors like `purchase_lead` and `length_of_stay` often play a significant role in predicting whether a user completes a booking.

---

*Disclaimer: This project was completed as part of a virtual experience program and uses public/provided datasets for educational purposes.*
