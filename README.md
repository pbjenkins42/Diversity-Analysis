# Workplace Diversity Analysis

## Overview

This project analyzes internal employee data to evaluate workplace diversity, salary fairness, and organizational structure. It was developed as a data science case study to assess whether employees are being treated fairly across gender, role, and department dimensions.

Using two datasets—employee attributes and reporting hierarchy—the analysis classifies each employee by level, calculates total reports (direct and indirect), builds predictive salary models, and identifies patterns in compensation across various groups.

## Objectives

1. **Classify Employees by Level**
   - Assign each employee to one of six organizational levels:
     - Individual Contributor (IC)
     - Middle Manager (MM)
     - Director (D)
     - Vice President (VP)
     - Executive (E)
     - CEO

2. **Calculate Number of Reports**
   - Compute the total number of employees managed by each employee, including both direct and indirect reports.

3. **Build Salary Prediction Models**
   - Train models to predict salary using employee features such as level, department, degree, experience, and total reports.
   - Compare model performance between Linear Regression and Random Forest.

4. **Evaluate Salary Fairness**
   - Identify which features most strongly influence salary.
   - Investigate disparities in pay by gender, department, and level.
   - Analyze whether salary differences are due to role-based factors or potential bias.

5. **Provide Recommendations**
   - Summarize findings for HR and suggest next steps to promote equity and transparency.

## Data

### 1. `company_hierarchy.csv`
- `employee_id`: Unique identifier for the employee
- `boss_id`: The ID of the employee's direct manager
- `dept`: Department of the employee (e.g., Engineering, Sales, HR, Marketing, CEO)

### 2. `employee.csv`
- `employee_id`: Unique identifier for the employee
- `signing_bonus`: Binary indicator (1 or 0) for signing bonus
- `salary`: Current salary in USD
- `degree_level`: Highest academic degree
- `sex`: Gender of the employee
- `yrs_experience`: Total years of experience

## Tools & Technologies

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Key Results

- **Department** is the strongest predictor of salary, particularly Engineering and HR.
- **Gender** does not significantly predict salary when controlling for department.
- **Years of Experience** shows non-linear impact; higher experience correlates with stronger salary gains only after a threshold.
- **Random Forest** outperformed Linear Regression with:
  - R² ≈ 0.34
  - ~49.6% of predictions within ±25% of actual salary
- **Salary prediction accuracy** was highest in the $200K–$300K range and lowest above $300K.

## Recommendations to HR

1. Rebalance hiring pipelines to increase gender representation in higher-paying departments.
2. Evaluate whether job responsibilities align with compensation and title across teams.
3. Consider salary equity reviews within departments rather than across the entire company.

## Repository Structure

```
.
├── data/
│   ├── company_hierarchy.csv
│   └── employee.csv
├── Diversity_Analysis.ipynb
├── README.md
```

## How to Run

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/workplace-diversity-analysis.git
   cd workplace-diversity-analysis
   ```

2. Open the notebook:
   ```
   jupyter notebook Diversity_Analysis.ipynb
   ```

3. Run all cells to reproduce the analysis.

## License

This project is for educational purposes only. No license is applied.
