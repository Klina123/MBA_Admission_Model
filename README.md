# MBA Admission Model

This project predicts MBA admission decisions using a synthetic dataset of applicant information. It uses classification models to estimate the probability of admission based on factors such as GPA, GMAT score, undergraduate major, work experience, and demographics.

## 📁 Repository Structure

```

project4.py         # Main script for cleaning, modeling, and plotting
images/             # Output folder for ROC curves and feature importance charts
data/               # Place the CSV file here (not included in the repo)
README.md           # Project overview and instructions
.gitignore          # Prevents large and sensitive files from being uploaded

````

## 📊 Dataset

- **Source**: Kaggle – [MBA Admission Dataset (Synthetic)](https://www.kaggle.com/datasets/taweilo/mba-admission-dataset)  
- **Description**: The dataset simulates MBA applicants with variables such as:
  - `gender`, `international`, `gpa`, `major`, `race`
  - `gmat`, `work_exp`, `work_industry`, and `admission` status
- **Target Variable**: `admission`  
  - Binary format: `1 = Admit`, `0 = Deny/Waitlist/Null`

> ⚠️ The `data/` folder is included in `.gitignore`. You must manually download [`MBA.csv`](https://www.kaggle.com/datasets/taweilo/mba-admission-dataset) and place it in the `data/` folder before running the script.

## 🛠️ How to Run

1. Clone the repo and install dependencies (mainly scikit-learn, pandas, matplotlib, seaborn).
2. Download `MBA.csv` from Kaggle and put it inside the `data/` folder.
3. Run the full pipeline:

```bash
python project4.py
````

This will:

* Load and clean the data
* Train Logistic Regression and Random Forest models
* Output accuracy, ROC AUC, confusion matrix, and classification report
* Save ROC curve and feature importance plots to `images/`

## 📈 Model Performance

| Model               | Accuracy | ROC AUC |
| ------------------- | -------- | ------- |
| Logistic Regression | 0.8563   | 0.8376  |
| Random Forest       | 0.8491   | 0.8482  |

### Notes:

* **Logistic Regression** had higher accuracy but lower recall on the positive class (admitted).
* **Random Forest** slightly improved AUC and recall for admits, but precision remained low, reflecting class imbalance.

## 📌 Key Features

* Logistic Regression as baseline model
* Random Forest for nonlinear modeling and feature importance
* ROC curve comparison across models
* Feature importance plot to explain key predictors

## 📚 Acknowledgments

This dataset was provided on Kaggle as synthetic data simulating admissions to a top business school. It does not represent real applicants.

## 🧑‍💻 Author

Kailing Li

```
