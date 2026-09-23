Statistical and mathematical Methods for Data Science

## Statistical Analysis of AI Use and Its Impact on Programmers

## Overview

This project analyzes students' use of Artificial Intelligence (AI) tools in computer science education, with a particular focus on programming assignments, AI-assisted learning, problem-solving skills, confidence, assignment difficulty, and perceptions of the long-term effects of AI reliance.

The dataset contains survey responses collected from students regarding their experiences, attitudes, and behaviors related to AI tools such as chatbots and code assistants.

The analysis combines **descriptive statistics, data visualization, correlation analysis, non-parametric statistical testing, chi-square tests, ANOVA, and logistic regression** to investigate relationships between AI usage patterns and students' perceptions of programming education.

---

## Research Objectives

The project aims to investigate the following areas:

* Students' general awareness and learning frequency regarding AI advancements.
* Students' beliefs about the future role of AI in computer science education.
* The amount of time students spend solving programming assignments.
* Students' perceptions of programming assignment difficulty.
* Frequency of AI use when solving programming assignments.
* The percentage of programming assignments completed with AI assistance.
* The relationship between AI use and problem-solving skills.
* The relationship between AI use and programming confidence.
* Whether AI encourages students to explore concepts beyond the curriculum.
* Students' perceptions of whether AI makes programming too easy.
* Students' attitudes toward the ethical use of AI in assignments.
* Students' reliance on AI tools and concerns about long-term programming skills.
* Students' views regarding institutional policies on AI use.

---

## Dataset

The dataset contains approximately **980 student responses** and includes demographic, educational, behavioral, and attitudinal variables.

### Main Variables

| Category              | Variables                                                   |
| --------------------- | ----------------------------------------------------------- |
| Demographics          | Age, Gender, Degree Program, Academic Level                 |
| AI Awareness          | AI learning frequency, belief in AI's future role           |
| Assignment Experience | Time spent, assignment frequency, difficulty                |
| AI Usage              | AI usage frequency, percentage of assignments using AI      |
| Learning Outcomes     | Problem-solving, confidence, exploration beyond curriculum  |
| AI Interaction        | Understanding AI-generated code, primary use of AI          |
| Attitudes             | Ethical acceptability, AI making programming easier         |
| Reliance              | AI over-reliance and long-term negative impact              |
| Academic Practice     | Discussion with instructors/peers, AI-generated submissions |
| Institutional Policy  | Preferences regarding university AI policies                |

---

## Technologies Used

The analysis was conducted using Python.

### Python Libraries

* **Pandas** — data manipulation and preprocessing
* **NumPy** — numerical operations
* **Matplotlib** — data visualization
* **Seaborn** — statistical visualization
* **SciPy** — statistical hypothesis testing
* **Statsmodels** — logistic regression and statistical modeling
* **Scikit-learn** — machine learning validation and LASSO logistic regression

---

## Data Preprocessing

Before analysis, the dataset was cleaned and standardized.

The preprocessing steps included:

1. Cleaning column names and removing unnecessary whitespace.
2. Standardizing categorical response values.
3. Handling missing observations.
4. Converting ordinal categorical responses into numerical ranks where required.
5. Creating binary variables for selected survey responses.
6. Creating dummy variables for nominal categorical predictors.
7. Preparing complete-case datasets for statistical modeling.

### Example Ordinal Encoding

Programming assignment time was converted into an ordinal scale:

| Response          | Rank |
| ----------------- | ---: |
| Less than 2 hours |    1 |
| 2–5 hours         |    2 |
| More than 5 hours |    3 |

Assignment difficulty was similarly encoded:

| Response | Rank |
| -------- | ---: |
| Easy     |    1 |
| Moderate |    2 |
| Hard     |    3 |

AI learning frequency was ordered as:

| Response     | Rank |
| ------------ | ---: |
| Daily        |    1 |
| Weekly       |    2 |
| Occasionally |    3 |
| Never        |    4 |

---

## Statistical Analysis

### 1. Descriptive Analysis

Frequency distributions and percentages were calculated to summarize:

* Demographic characteristics
* AI learning frequency
* AI usage frequency
* Assignment difficulty
* Assignment-solving time
* Students' perceptions of AI
* Attitudes toward AI policies

---

### 2. Spearman Correlation

Spearman's rank correlation was used to examine the relationship between:

**Time Spent on Programming Assignments**
and
**Perceived Programming Assignment Difficulty**

This non-parametric correlation was selected because both variables are ordinal.

The corresponding visualization is titled:

> **Percentage Distribution of Programming Assignment Difficulty by Time Spent**

---

### 3. Kruskal–Wallis Test

The Kruskal–Wallis test was used to examine whether AI learning frequency differs across groups based on students' beliefs about AI's future role in computer science education.

The analysis compares:

* Daily
* Weekly
* Occasionally
* Never

across belief groups:

* Yes
* No
* Not Sure

This test is appropriate for comparing an ordinal outcome across more than two independent groups.

---

### 4. Chi-Square Tests of Independence

Chi-square tests were used to examine associations between categorical variables.

Examples include:

#### AI Usage and Exploration

**AI usage frequency** × **Exploration of programming concepts beyond the curriculum**

#### AI Usage and Problem-Solving

**AI usage frequency** × **Perceived improvement in problem-solving skills**

#### AI Usage and Long-Term Impact

**AI usage frequency** × **Perceived long-term negative impact on programming skills**

#### Primary AI Use and Ethics

**Primary use of AI tools** × **Perceived ethical acceptability**

These analyses determine whether the distribution of one categorical variable differs according to another categorical variable.

---

### 5. One-Way ANOVA

One-way ANOVA was used to examine differences in perceived long-term negative impact across AI usage frequency groups.

The analysis considers AI usage frequency as the grouping variable and the coded perception of long-term impact as the outcome.

The corresponding analysis can be described as:

> **Differences in Perceived Long-Term Negative Impact Across AI Usage Frequency Groups**

---

## Logistic Regression

A multivariable logistic regression model was developed to identify factors associated with students' perceptions of the potential long-term negative effects of heavy AI reliance on programming skills.

### Dependent Variable

**Perceived Long-Term Negative Impact**

The outcome was coded as:

* Yes = 1
* No = 0
* Unsure = 0

### Predictor Variables

The model includes several potential explanatory variables, including:

* Age
* Gender
* Academic level
* Assignment difficulty
* Assignment-solving time
* Percentage of assignments using AI
* AI usage frequency
* Perceived problem-solving improvement
* Programming confidence
* Perception that AI makes programming too easy
* AI over-reliance
* Unsolvable assignment experience
* Exploration beyond the curriculum
* Understanding of AI-generated code
* Primary AI usage mode
* Discussion of AI use with instructors or peers
* Ethical acceptability
* Submission of entirely AI-generated work
* University AI policy preferences

---

## Logistic Regression Outputs

The regression analysis evaluates:

* Regression coefficients
* Odds ratios
* p-values
* 95% confidence intervals
* Model significance
* Pseudo R²
* Multicollinearity using VIF

Odds ratios are used to describe the relationship between predictor variables and the odds of reporting perceived long-term negative impact.

---

## LASSO Logistic Regression

LASSO logistic regression is also included to examine variable selection and identify predictors that contribute to the classification of perceived long-term negative impact.

Cross-validation is used to select the regularization parameter.

This provides a complementary approach to the conventional logistic regression model.

---

## Model Validation

A holdout validation procedure is used to evaluate model performance.

The dataset is divided into:

* **80% training data**
* **20% testing data**

The validation analysis includes:

* ROC-AUC
* Classification report
* Precision
* Recall
* F1-score
* Classification accuracy

The validation results provide an indication of how well the model generalizes to previously unseen observations.

---

## Visualizations

The project includes several visualizations designed to communicate the statistical findings clearly.

Examples include:

### AI Learning Frequency

**AI Learning Frequency Distribution by Belief in AI's Future Role in Computer Science Education**

This visualization compares the percentage distribution of AI learning frequency across students' beliefs about AI's future role.

### Assignment Time and Difficulty

**Percentage Distribution of Programming Assignment Difficulty by Time Spent**

This visualization shows the percentage of students across assignment-solving time categories and perceived difficulty levels.

### AI Usage and Long-Term Impact

A categorical visualization can be used to show the distribution of perceived long-term negative impact across different AI usage-frequency groups.

---

## Hypothesis Testing

The analyses generally use a significance level of:

**α = 0.05**

The interpretation follows:

* **p < 0.05:** statistically significant evidence against the null hypothesis.
* **p ≥ 0.05:** insufficient evidence to reject the null hypothesis.

Statistical significance should be interpreted alongside effect sizes, confidence intervals, sample size, and the research context.

---

## Project Structure

A recommended repository structure is:

```text
AI-CS-Education-Analysis/
│
├── data/
│   └── survey_data.csv
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_descriptive_analysis.ipynb
│   ├── 03_visualizations.ipynb
│   ├── 04_statistical_tests.ipynb
│   └── 05_logistic_regression.ipynb
│
├── figures/
│   ├── ai_learning_frequency.png
│   ├── assignment_time_difficulty.png
│   └── ai_usage_long_term_impact.png
│
├── results/
│   ├── descriptive_statistics.csv
│   ├── statistical_tests.csv
│   └── regression_results.csv
│
├── README.md
└── requirements.txt
```

---

## Reproducibility

To reproduce the analysis:

### 1. Clone the repository

```bash
git clone <repository-url>
cd AI-CS-Education-Analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Place the dataset

Place the survey dataset inside the `data/` directory.

### 4. Run the notebooks

Run the notebooks in the recommended order:

```text
01_data_cleaning.ipynb
02_descriptive_analysis.ipynb
03_visualizations.ipynb
04_statistical_tests.ipynb
05_logistic_regression.ipynb
```

---

## Requirements

A `requirements.txt` file can contain:

```text
pandas
numpy
matplotlib
seaborn
scipy
statsmodels
scikit-learn
```

---

## Interpretation and Limitations

The analysis describes relationships and associations observed in the survey data. Statistical associations should not automatically be interpreted as causal relationships.

Important limitations may include:

* Survey responses are self-reported.
* The analysis is based on observational survey data.
* Some variables are ordinal and therefore their numerical coding represents ordered categories rather than equal numerical distances.
* Missing responses can reduce the sample size available for individual analyses.
* Logistic regression results depend on the variables included in the model and the coding of categorical responses.
* Synthetic or simulated data, if used, should not be interpreted as evidence about the real student population.

---

## Ethical Considerations

The analysis should preserve respondent privacy and avoid reporting personally identifiable information.

If synthetic data are used for development, testing, visualization, or demonstration, they should be clearly identified as synthetic and should not be presented as genuine survey observations.

---

## Research Focus

The overall research investigates how students interact with AI tools in computer science education and how AI-assisted programming relates to students' learning behaviors, perceptions, confidence, problem-solving, and concerns regarding long-term programming skills.

The project integrates statistical analysis and visualization to provide a quantitative examination of students' experiences with AI-assisted programming education.

---

## Author

**Research Project: AI Use in Computer Science Education**

Developed using Python, Pandas, SciPy, Statsmodels, Scikit-learn, Matplotlib, and Seaborn.

---

## License

Add an appropriate license if this repository will be publicly distributed.

For example:

```text
MIT License
```

or use an institutional/research-specific license where applicable.

