# Statistical and Mathematical Methods for Data Science

## Project: Statistical Analysis of AI Use & its impact on Programmers 

### Overview

This project applies statistical and mathematical methods to survey data related to the use of Artificial Intelligence (AI) tools in computer science education.

The analysis investigates students' AI learning behavior, use of AI tools for programming assignments, assignment-solving time, perceived assignment difficulty, problem-solving skills, programming confidence, AI reliance, and perceptions of the long-term effects of AI on programming skills.

All data preprocessing, statistical analysis, hypothesis testing, visualization, and regression modeling are contained within the Jupyter Notebook included in this repository.

---

## Notebook

The repository contains the following main file:

```text
Statistical-and-Mathematical-Methods-for-Data-Science/
│
└── Statistical_and_Mathematical_Methods_for_Data_Science.ipynb
```

The notebook contains the complete analysis workflow, from data preparation to statistical modeling and interpretation.

---

## Analysis Performed

The notebook includes the following statistical and mathematical methods:

### 1. Data Preprocessing

* Data cleaning
* Handling missing values
* Categorical variable encoding
* Ordinal ranking
* Binary variable transformation
* Preparation of variables for statistical analysis

### 2. Descriptive Statistics

The notebook calculates frequency distributions and percentages for major survey variables, including:

* Age
* Gender
* Degree program
* Academic level
* AI learning frequency
* AI usage frequency
* Assignment-solving time
* Assignment difficulty
* AI-related attitudes and perceptions

### 3. Spearman's Rank Correlation

Spearman's correlation is used to examine the relationship between:

**Time Spent on Programming Assignments**
and
**Perceived Programming Assignment Difficulty**

### 4. Kruskal–Wallis Test

The Kruskal–Wallis test is used to compare AI learning frequency across groups based on students' beliefs about AI's future role in computer science education.

### 5. Chi-Square Tests

Chi-square tests of independence are used to examine relationships between categorical variables, including:

* AI usage and exploration of programming concepts
* AI usage and perceived problem-solving improvement
* AI usage and perceived long-term impact on programming skills
* Primary AI use and ethical acceptability

### 6. One-Way ANOVA

ANOVA is used to examine differences in perceived long-term negative impact across AI usage-frequency groups.

### 7. Logistic Regression

Multiple logistic regression is used to investigate potential predictors of students' perceptions of the long-term negative effects of AI reliance on programming skills.

The analysis includes variables related to:

* Demographics
* Assignment characteristics
* AI usage
* Problem-solving
* Confidence
* AI reliance
* Ethical attitudes
* Learning behavior
* AI-generated submissions
* University AI policies

### 8. Multicollinearity Analysis

Variance Inflation Factor (VIF) is calculated to assess potential multicollinearity among regression predictors.

### 9. LASSO Logistic Regression

LASSO logistic regression is applied for variable selection and comparison with the conventional logistic regression model.

### 10. Model Validation

The logistic regression analysis includes holdout validation and evaluates model performance using measures such as:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC

---

## Visualizations

The notebook includes several visualizations for communicating the statistical results, including:

* AI learning frequency distributions
* AI learning frequency by beliefs about AI's future role
* Assignment-solving time and perceived difficulty
* AI usage frequency and perceived long-term impact
* Other categorical and statistical visualizations related to the research questions

---

## Tools and Libraries

The notebook is developed using Python and commonly used data science libraries:

* **Pandas** — data manipulation and preprocessing
* **NumPy** — numerical operations
* **Matplotlib** — visualization
* **Seaborn** — statistical visualization
* **SciPy** — statistical tests
* **Statsmodels** — statistical modeling
* **Scikit-learn** — machine learning and model validation

---

## How to Run

1. Download or clone this repository.
2. Open the `.ipynb` file using:

   * Jupyter Notebook
   * JupyterLab
   * Google Colab
   * Visual Studio Code
3. Ensure the required Python libraries are installed.
4. Run the notebook cells sequentially.

Install the required libraries with:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn
```

---

## Research Focus

The project demonstrates how statistical and mathematical methods can be applied to survey data to investigate patterns and relationships involving AI in computer science education.

The overall workflow is:

```text
Data Preparation
       ↓
Descriptive Statistics
       ↓
Data Visualization
       ↓
Correlation Analysis
       ↓
Hypothesis Testing
       ↓
Regression Analysis
       ↓
Model Validation
```

---

## Academic Purpose

This notebook was developed as a project for the course:

**Statistical and Mathematical Methods for Data Science**

It demonstrates the practical application of statistical techniques to a data science problem involving AI-assisted learning and programming education.

---

## Note

The results should be interpreted in the context of the survey design, variable coding, sample characteristics, and assumptions associated with each statistical method.

If synthetic data are used in the notebook, they should be considered suitable for demonstration and academic analysis rather than as evidence representing a real-world population.
