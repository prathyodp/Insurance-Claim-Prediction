# Insurance Claim Prediction - Big Data Analytics Capstone Project

## 1. Business Problem & Objective

Insurance companies need to efficiently identify high-risk policyholders who are likely to file claims.

The objective of this project is to analyze customer demographic, health, and financial attributes such as age, BMI, smoking status, and medical charges and build a distributed machine learning pipeline to predict whether an insurance claim will be filed.

The project uses Hadoop HDFS, Hive, Apache Spark and PySpark to store, process, transform and analyze the insurance dataset.

---

## 2. Dataset Description

**Dataset:** Insurance.csv

**Source:** Kaggle / Medical Cost Personal Datasets

**Size:** Approximately 40.7 KB

**Records:** 1,338

**Columns:** 8

### Important Columns

| Column | Description | Data Type |
|---|---|---|
| age | Age of the beneficiary | INT |
| sex | Gender | INT |
| bmi | Body Mass Index | DOUBLE |
| children | Number of children/dependents | INT |
| smoker | Smoking status | INT |
| region | Residential region | INT |
| charges | Medical insurance charges | DOUBLE |
| claim | Target variable: 0 = No, 1 = Yes | INT |

The target variable is `claim`.

- `0` = No insurance claim
- `1` = Insurance claim

---

## 3. Big Data Architecture

```text
                    Insurance.csv
                         |
                         v
                    HDFS Storage
                         |
                         v
                  Hive Database/Table
                         |
                         v
                    Spark / PySpark
                         |
                         v
             Data Cleaning & Transformation
                         |
                         v
                  Feature Assembly
                         |
                         v
                 Logistic Regression
                         |
                         v
                     Predictions
                         |
                         v
                  Model Evaluation
                         |
                         v
                    AUC = 0.9270
                         |
                         v
              Predictions saved to HDFS