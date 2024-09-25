## Project Overview

This project, titled **Finding Donors**, analyzes census data to predict whether an individual earns more than \$50K per year. The project uses data preprocessing and exploratory Data Analysis (EDA). After testing several models, Gradient Boosting was selected, followed by a Bayesian search for hyperparameter tuning.

---

## Project Flow

### 1. **Importing Libraries**

   The project imports the necessary libraries:
   - `pandas` and `numpy` for data handling.
   - `seaborn` and `matplotlib` for data visualization.
   - Warnings are suppressed to keep the output clean.

### 2. **Loading and Copying the Dataset**

   The dataset (`census.csv`) consists of **45,222 rows** and **14 columns**. A copy of the dataset is made for data processing.

### 3. **Data Cleaning and Preprocessing**

   - **Duplicate Removal**: Any duplicates in the dataset are removed to ensure consistency.
   - **Categorical to Numeric Conversion**: 
     - The `sex` column is converted to numeric values (`0` for Female and `1` for Male).
     - Other categorical variables are similarly transformed for modeling.

### 4. **Exploratory Data Analysis (EDA) and Correlation**

   Correlation analysis was conducted during the EDA phase to evaluate the relationships between columns. This analysis helped identify the most relevant features to improve model performance.

### 5. **Modeling Approach**

   After trying several base models, such as Logistic Regression, Decision Trees, and Random Forest, **Gradient Boosting** was chosen as the final model due to its superior performance. To fine-tune the model, **Bayesian search** was used for hyperparameter tuning, optimizing its performance further.

   - The target labels for prediction are:
     - `1`: Represents an individual who donates (income > \$50K).
     - `0`: Represents an individual who does not donate (income ≤ \$50K).

### 6. **Model Testing**

   The model was tested on a random set of donors to validate its ability to generalize beyond the training data. This helped ensure that the predictions were robust and applicable to unseen data.

### Model Performance:
   - **Testing F1 Score**: 69.42 %
   - **Testing Accuracy**: 86.12 %

---

## Mechanism of the Model

The model predicts whether an individual earns more than \$50K (donates) or not, based on demographic and financial data. Correlation analysis was used to select key features. After testing multiple models, **Gradient Boosting** was chosen, and **Bayesian search** was applied to tune its hyperparameters. The model was tested on random donors to confirm its generalization ability.

---

## How to Run the Project

1. Clone the repository and install the necessary dependencies:
   ```bash
   git clone https://github.com/your-repo/finding-donors.git
   cd finding-donors
   pip install -r requirements.txt
   ```

2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook Finding_donors_Final.ipynb
   ```

---
## Testing Section
The model was tested on 50 random donors from the dataset to evaluate its real-world performance. Below are the testing results, showing both predictions and actual outcomes for a subset of customers:

**Sample Predictions**:

Customer 0: Prediction = 0, Actual = 1 <br>
Customer 87: Prediction = 0, Actual = 0 <br>
Customer 348: Prediction = 1, Actual = 1 <br>
Customer 522: Prediction = 1, Actual = 1 <br>
Customer 783: Prediction = 1, Actual = 1 <br>
Customer 957: Prediction = 0, Actual = 0 <br>
Customer 1131: Prediction = 0, Actual = 0 <br>
Customer 1740: Prediction = 1, Actual = 1

**Overall Results**:

Correct Predictions: 45 <br>
Incorrect Predictions: 5 <br>

The model performed with high accuracy on random donor samples, correctly predicting most cases.

----

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). You are free to use, modify, and distribute this code under the terms of this license.

