# Heart Disease Risk Analysis 

Explore whether clinical and demographic attributes can reliably predict the presence of heart disease using logistic regression.

## 📊 Overview & Data 

- **Source:** UCI Heart Disease dataset (Cleveland Database,303 patients, donated in 1988).

- **Features:** 14 columns covering patient demographics, vital signs, and diagnostic test results (e.g.,age,sex,chest pain type, resting blood pressure,cholesterol,max heart rate).

- **Data Issue & Resolution:** During exploratory data analysis, I discovered that the target column (*target* / presence of heart disease) in my downloaded copy was coded inversely compared to the original documentation (0s and 1s were flipped). I confirmed this by cross-referencing feature correlations (like maximum heart rate vs. disease presence) and corrected the encoding before proceeding with modeling.

## 🛠️ Methods 

- **Data Cleaning & Preprocessing:** Handled missing values, encoded categorical variables, and normalized numerical features.

- **Exploratory Data Analysis (EDA):** Built SQL queries and visual charts (using Matplotlib/Seaborn) to uncover feature distributions and correlations.

- **Modeling:** Trained a Logistic Regression classifier using an 80/20 train-test split.

## 📉 Key Findings 

- **Model Performance:** Initial iterations yielded a baseline test accuracy of 77%. After correcting the target encoding bug and refining feature selection, test accuracy improved to 82%.

- **Evaluation vs. Baseline:** The final model comfortably outperforms the naive majority-class baseline.

- **Key Predictors:** Chest pain type, maximum heart rate achieved (*thalach*), and exercise-induced angina emerged as the strongest predictors for heart disease risk.

- **Clinical Balance:** The model achieved a strong balance of sensitivity and specificity, minimizing false negatives where possible (critical in a medical context).

## ⚠️ Limitations

- **Sample Size:** Limited to a relatively small test set of 61 patients.

- **Generalizability:** Data originates from a single hospital (Cleveland Clinic) in the 1980s, meaning it may not reflect modern patient demographics or diverse populations.

- **Causality:** As an observational dataset, correlation does not imply causation.

- *📌 NOTE* For learning purposes and portfolio purposes only. Not intended for actual medical diagnosis.
