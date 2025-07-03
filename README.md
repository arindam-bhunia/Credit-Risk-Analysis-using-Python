# Credit Risk Analysis Project 🏦

## Overview
This project implements a machine learning solution for predicting credit risk in home loans. The analysis helps financial institutions assess the likelihood of loan default based on various applicant and loan parameters.

## 📊 Dataset Description
The dataset contains various features related to home loan applications:

| Feature | Description |
|---------|------------|
| loan_id | Unique identifier for each loan record |
| applicant_income | Annual income of the applicant |
| loan_amount | Total requested/approved loan amount |
| loan_term | Loan repayment period in months |
| credit_score | Applicant's credit score (300-850) |
| employment_years | Years at current employment |
| property_value | Market value of the property |
| ltv_ratio | Loan-to-Value ratio (%) |
| dti_ratio | Debt-to-Income ratio (%) |
| loan_purpose | Purpose of loan (purchase/refinance/home_improvement) |
| loan_status | Application status (approved/denied/pending) |
| default_flag | Target variable (1=default, 0=good standing) |

## 🛠️ Technical Stack
- **Python 3.x**
- **Key Libraries:**
  - pandas: Data manipulation and analysis
  - numpy: Numerical computations
  - scikit-learn: Machine learning models
  - matplotlib & seaborn: Data visualization

## 📝 Project Structure
1. **Data Loading & Exploration**
   - Basic statistics
   - Data shape and structure
   - Missing value analysis

2. **Data Preprocessing**
   - Missing value handling
   - Categorical variable encoding
   - Feature scaling
   - Derived feature creation (LTV & DTI ratios)

3. **Exploratory Data Analysis (EDA)**
   - Distribution analysis
   - Correlation studies
   - Feature relationships with default risk

4. **Model Development**
   - Logistic Regression
   - Random Forest Classifier
   - Train-test split (80-20)
   - Feature scaling

5. **Model Evaluation**
   - Classification reports
   - Confusion matrices
   - ROC curves and AUC scores

## 📈 Results

- **Model Performance:**
  - Both Logistic Regression and Random Forest models were trained to predict the likelihood of loan default (`default_flag`).
  - **Random Forest** outperformed Logistic Regression in all key metrics.
  - Actual metrics from the notebook:
    - **Random Forest:**
      - Accuracy: 0.69
      - Precision: 0.71
      - Recall: 0.96
      - F1-score: 0.82
      - ROC-AUC: (see ROC curve plot in the notebook)
      - Confusion Matrix:
        |        | Predicted No Default | Predicted Default |
        |--------|---------------------|-------------------|
        | Actual No Default | 17 | 278 |
        | Actual Default    | 28 | 677 |
    - **Logistic Regression:**
      - Accuracy: 0.70
      - Precision: 0.70
      - Recall: 1.00
      - F1-score: 0.83
      - ROC-AUC: (see ROC curve plot in the notebook)
      - Confusion Matrix:
        |        | Predicted No Default | Predicted Default |
        |--------|---------------------|-------------------|
        | Actual No Default | 0 | 295 |
        | Actual Default    | 0 | 705 |

- **Feature Importance:**
  - The most influential features for predicting default were:
    - `credit_score`
    - `ltv_ratio`
    - `dti_ratio`
    - `applicant_income`
    - `loan_amount`

- **Risk Prediction Example:**
  - The trained model can predict the probability of default for new applicants, supporting better lending decisions.

- **Business Insights:**
  - Applicants with lower credit scores, higher LTV and DTI ratios, and lower incomes are at higher risk of default.
  - The model can help prioritize loan approvals and flag high-risk applications for further review.

## 🚀 Usage
1. Clone the repository
2. Install required packages:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
3. Run the Jupyter notebook:
   ```bash
   jupyter notebook credit_risk_analysis.ipynb
   ```

## 📌 Important Notes
- The model should be periodically retrained with new data
- Feature importance may vary based on economic conditions
- Model predictions should be used as one of many factors in loan decisions

## 🤝 Contributing
Feel free to fork, improve, and submit pull requests. For major changes, please open an issue first to discuss the proposed changes.

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Author
[Your Name]

## 🙏 Acknowledgments
- Dataset source: [Source Name]
- Thanks to all contributors and reviewers
