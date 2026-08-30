# Titanic Survival Prediction

## Description

Machine learning project for predicting whether a passenger survived the Titanic disaster.

This project demonstrates a complete basic machine learning workflow, including data exploration, preprocessing, model training, evaluation, and model comparison.

## Dataset

The Titanic dataset contains information about **891 passengers**.

The target variable is `survived`:

* `0` — passenger did not survive
* `1` — passenger survived

### Features used

* `pclass` — passenger class
* `age` — passenger age
* `sibsp` — number of siblings/spouses aboard
* `parch` — number of parents/children aboard
* `fare` — ticket fare
* `alone` — whether the passenger was traveling alone
* `sex` — passenger sex
* `embarked` — port of embarkation

## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

## Project Workflow

1. Data loading
2. Exploratory Data Analysis (EDA)
3. Missing value analysis
4. Data preprocessing
5. Feature encoding
6. Train/test split
7. Logistic Regression
8. Random Forest
9. Model evaluation
10. Model comparison

## Exploratory Data Analysis

The dataset contains 891 passengers and 15 original columns.

Missing values were found in:

* `age` — 177 values
* `embarked` — 2 values
* `deck` — 688 values

The dataset contains 577 male passengers and 314 female passengers.

The `embarked` column represents the port where the passenger boarded the Titanic:

* `S` — Southampton
* `C` — Cherbourg
* `Q` — Queenstown

## Data Preprocessing

Missing values in `age` were filled with the median age.

Missing values in `embarked` were filled with the most frequent value.

Categorical variables such as `sex` and `embarked` were converted into numerical features using one-hot encoding.

Columns that were not required for the machine learning models were removed.

After preprocessing, the dataset contained **891 rows and 11 features** with no missing values.

## Models

Two classification models were trained and compared:

### Logistic Regression

Logistic Regression was used as the baseline model.

Results:

* Accuracy: **79.9%**
* Precision: **77.1%**
* Recall: **73.0%**
* F1-score: **75.0%**

### Random Forest

Random Forest was used as a second model to compare its performance with Logistic Regression.

Results:

* Accuracy: **81.0%**
* Precision: **78.6%**
* Recall: **74.3%**
* F1-score: **76.4%**

## Results

| Model               |  Accuracy | Precision |    Recall |  F1-score |
| ------------------- | --------: | --------: | --------: | --------: |
| Logistic Regression |     79.9% |     77.1% |     73.0% |     75.0% |
| **Random Forest**   | **81.0%** | **78.6%** | **74.3%** | **76.4%** |

Random Forest achieved the best overall performance on the test set.

It improved accuracy from **79.9% to 81.0%** compared with Logistic Regression.

## Conclusion

The project demonstrates a complete machine learning workflow from data exploration to model comparison.

Among the two tested models, **Random Forest performed slightly better** across all evaluated metrics.

The best model achieved an accuracy of **81.0%** and an F1-score of **76.4%**.

Further improvements could include cross-validation, hyperparameter tuning, feature engineering, and testing additional machine learning algorithms.

## How to Run

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd ml-project
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment on Windows

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Start Jupyter Notebook

```bash
jupyter notebook
```

Open `analysis.ipynb` in your browser and run the notebook cells.

## Project Structure

```text
ml-project/
│
├── analysis.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Author

Aigerim Manat
