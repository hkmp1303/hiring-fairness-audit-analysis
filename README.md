# Hiring with AI Fairness Audit Analysis

## Project Overview

This project analyzes fairness and bias patterns in AI-assisted hiring systems using a simulated recruitment dataset. The analysis compares AI-generated candidate evaluations against human reviewer scores to identify systematic differences in scoring behavior, examine how these differences vary across candidate profiles and assess whether scoring divergence affects final hiring decisions.

The project uses exploratory data analysis (EDA) and statistical visualization to investigate whether AI screening tools evaluate candidates differently than human reviewers and whether factors like education level or years of experience moderate this relationship.

**Key focus areas:**
- Quantifying the AI-human scoring gap across the candidate pool
- Testing whether candidate attributes (experience, education) explain scoring divergence
- Assessing decision agreement rates between AI and human raters

This is an educational project demonstrating data cleaning, pandas operations, statistical reasoning, and principled visualization using matplotlib. All findings describe the synthetic data generator, not real-world hiring systems.

## Research Questions

This analysis explores the following questions about AI-assisted hiring systems:

1. **Do AI and human raters assign systematically different scores to candidates?**
   - Is there a consistent scoring gap between AI-generated and human-generated evaluations?
   - What is the magnitude and direction of this divergence?

2. **Does candidate experience explain the AI-human scoring gap?**
   - Do more experienced candidates receive more similar scores from both raters?
   - Is the scoring divergence constant across experience levels?

3. **Does education level moderate the AI-human scoring gap?**
   - Do candidates with advanced degrees experience smaller or larger divergence?
   - Which education levels show the most agreement between AI and human raters?

4. **Do scoring differences translate into hiring decision differences?**
   - Despite score divergence, do AI and human raters agree on final hiring decisions?
   - What is the decision agreement rate between the two evaluation methods?

**Note:** This dataset does not contain protected attributes (gender, ethnicity, age), so bias audits along those dimensions are out of scope. The data is simulated and findings describe the synthetic generator, not real-world hiring systems.

## Dataset Overview
This project uses the “AI-Assisted Hiring Fairness and Bias Audit Dataset” from Kaggle. The referenced data set contains simulated recruitment records including applicant attributes,
AI screening scores, human evaluations, and hiring outcomes.

The dataset is designed for fairness and bias analysis in AI-assisted hiring systems.

### Data Source
**Dataset:**
AI-Assisted Hiring Fairness and Bias Audit Dataset

**Author:** Aulqarnain Haider @Zulqarnain11 (Kaggle)

**Source link:**
[https://www.kaggle.com/datasets/zulqarnain11/zzzzzzzzzzzzzzzz](https://www.kaggle.com/datasets/zulqarnain11/zzzzzzzzzzzzzzzz)

The dataset is owned by the original author and is used in accordance with Kaggle’s terms and any applicable licensing conditions.

### Dataset Structure

The dataset contains approximately:
- 1,500 records
- demographic attributes
- AI evaluation scores
- human review scores
- hiring decisions

Primary variables include:
- education
- years of experience
- AI suitability score
- hiring outcome

## Project Usage

This dataset is used for educational purposes to explore whether AI-assisted hiring systems produce different outcomes based on demographics and to compare AI-generated evaluations with human decision-making.

## Reproducibility

To reproduce the analysis:
1. Download the dataset from the original Kaggle source
2. Place the CSV file in the `/data` directory as `ai_hiring_audit_dataset.csv`
3. Install dependencies: `pip install -r requirements.txt`
4. Run the analysis notebook: `jupyter notebook notebook.ipynb`

## Key Findings

- AI systematically scores candidates 7-8 points lower than human reviewers
- Education level moderates the AI-Human gap: candidates with advanced degrees experience smaller divergence
- Years of experience shows no relationship with the scoring gap
- AI and human raters agree on final hiring decisions in ~91% of cases

## Project Structure

```
hiring-fairness-audit-analysis/
├── data/
│   └── ai_hiring_audit_dataset.csv
├── notebook.ipynb          # Main analysis
├── README.md
└── .gitignore
```

## Limitations and Ethical Notes

**Data Limitations:**
- This dataset contains **simulated recruitment scenarios**, not real hiring data. All findings describe the synthetic data generator's behavior, not actual AI hiring systems or employer practices.
- The dataset **lacks protected attributes** (gender, ethnicity, age). Making bias audits along those dimensions is not possible. Age can only be indirectly inferred from years of experience.
- The data generation process, sampling assumptions, and labeling methodology are **not documented** by the original author and cannot be verified from the CSV alone.

**Analytical Limitations:**
- The analysis cannot explain **why** the AI rater systematically scores lower—whether this reflects deliberate calibration, threshold choices, or artifacts of the synthetic generator.
- While the 91% decision agreement rate is measured, the **9% disagreement subset** is not examined in detail.
- Score divergence patterns do not necessarily translate to hiring outcome disparities.

**Ethical Boundaries:**
- Results should be understood as **exploratory** rather than definitive proof of algorithmic discrimination.
- Findings **do not transfer** to real-world recruitment systems.
- This analysis is for **educational purposes** only—demonstrating data cleaning, statistical reasoning, and principled visualization techniques.

## License
Code in this repository is licensed under the GPL License.

The dataset used in this project belongs to its original author on Kaggle and is subject to separate licensing and usage terms.

## Author
Heather Payne
