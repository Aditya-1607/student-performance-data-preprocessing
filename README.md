# Student Performance Data Preparation Pipeline

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Latest-orange.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-green.svg)

A Python-based data preparation project using a Student Performance dataset. The notebook demonstrates dataset inspection, missing-value handling, duplicate removal, exploratory data analysis (EDA), categorical encoding, feature scaling, and CSV export.

---

## Project Overview

The objective of this activity is to convert the raw student dataset into a clean, transformed dataset that can be used for further data analysis and machine learning tasks.

### Objectives

1. Load and inspect the student performance dataset.
2. Identify numerical and categorical features.
3. check missing values and handle them using imputation.
4. Detect and remove duplicate records.
5. Perform EDA using histograms and a correlation heatmap.
6. Convert categorical features into numerical form using One-Hot Encoding.
7. Apply feature scaling using `StandardScaler`.
8. Export the prepared dataset as a CSV file.

---

## Repository Structure

```text
├── README.md
├── Notebook3.ipynb
├── act1_student_performance_raw.csv
└── act1_student_performance_cleaned.csv
```

---

## Dataset Information

- **Dataset:** Student Performance
- **Domain:** Education
- **Raw dataset size:** 203 rows × 13 columns
- **Prepared dataset size:** 200 rows × 12 columns
- **Target/grade field:** `final_grade`

### Features

| Feature | Description |
|---|---|
| `student_id` | Unique student identifier |
| `school` | School attended |
| `age` | Student age |
| `Medu` | Mother's education level |
| `Fedu` | Father's education level |
| `study_time` | Weekly study-time category |
| `failures` | Number of past class failures |
| `school_support` | Whether the student receives school support |
| `internet_access` | Whether the student has internet access |
| `absences` | Number of school absences |
| `G1` | First-period grade |
| `G2` | Second-period grade |
| `final_grade` | Final grade |

---

## Data Preparation Workflow

### 1. Load and Inspect Data
- Load the raw CSV file using Pandas.
- Display the first rows, dataset dimensions, data types, and summary statistics.

### 2. Identify Data Types
- Separate numerical columns from categorical columns.
- Review the features before applying data-cleaning operations.

### 3. Missing Value Analysis
Missing values in the raw dataset:

| Column | Missing Values |
|---|---:|
| `age` | 17 |
| `study_time` | 12 |
| `internet_access` | 10 |

### 4. Handle Missing Values
- Numerical columns: fill missing values using the median.
- Categorical columns: fill missing values using the mode.
- Verify that no missing values remain.

### 5. Remove Duplicate Records
- Check for duplicate rows.
- Remove duplicate records and reset the DataFrame index.
- The raw dataset contains 3 duplicate rows.

### 6. Exploratory Data Analysis (EDA)
- Plot histograms to understand numerical feature distributions.
- Create a correlation heatmap to examine relationships between numerical features.

### 7. Categorical Feature Encoding
- Apply One-Hot Encoding using `pandas.get_dummies()`.
- Use `drop_first=True` to avoid redundant dummy columns.

### 8. Feature Scaling
- Apply `StandardScaler` to numerical features.
- Standardization transforms numerical values to a common scale.

### 9. Export Prepared Dataset
- Export the transformed data to a CSV file.
- The supplied prepared dataset is `act1_student_performance_cleaned.csv`.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Aditya-1607/REPOSITORY-NAME.git
cd REPOSITORY-NAME
```

### 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 3. Open the Notebook

```bash
jupyter notebook Notebook3.ipynb
```

Run the notebook cells in order. Keep `act1_student_performance_raw.csv` in the same directory as the notebook.

---

## Output

The prepared dataset contains:

- 200 rows
- 12 columns
- No missing values
- No duplicate records in the cleaned data
- Encoded categorical features
- Scaled numerical features

The output CSV file can be used for further analysis and machine learning activities.
