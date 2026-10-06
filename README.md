# SWYNEX Data Preparation

## Task 1 – Data Preparation

This project demonstrates the preparation of a publicly available Titanic
dataset for data-science work.

## Dataset

The Titanic dataset contains passenger information including:

- Passenger ID
- Survival status
- Passenger class
- Name
- Sex
- Age
- Number of siblings/spouses
- Number of parents/children
- Ticket
- Fare
- Cabin
- Port of embarkation

## Data Preparation

The following steps were performed:

1. Loaded the raw CSV dataset using Pandas.
2. Inspected the dataset structure and data types.
3. Identified missing values.
4. Checked for duplicate records.
5. Replaced missing `Age` values using the median.
6. Replaced missing `Embarked` values using the mode.
7. Replaced missing `Cabin` values with `Unknown`.
8. Verified the data types of numerical and text columns.
9. Performed a final data-quality check.
10. Saved the cleaned dataset separately.
11. Verified the saved cleaned dataset.
12. Created an age-distribution visualization.

## Missing Value Handling

| Column | Issue | Treatment | Reason |
|---|---|---|---|
| Age | Missing values | Median | Suitable for numerical data and less affected by extreme values |
| Embarked | Missing values | Mode | Suitable for categorical data |
| Cabin | Missing values | `Unknown` | Preserves passenger records without inventing cabin information |

## Data Quality Result

After preprocessing:

- Rows: 891
- Columns: 12
- Missing values: 0
- Duplicate rows: 0
- Data types: Verified

The original raw dataset was preserved and preprocessing was performed on a
separate copy.

## Project Structure

```text
SWYNEX-Data-Preparation/
│
├── data/
│   ├── raw/
│   │   └── train.csv
│   │
│   ├── cleaned/
│   │   └── titanic_cleaned.csv
│   │
│   └── processed/
│
├── notebooks/
│   └── data_preparation.ipynb
│
├── scripts/
│
├── README.md
└── requirements.txt