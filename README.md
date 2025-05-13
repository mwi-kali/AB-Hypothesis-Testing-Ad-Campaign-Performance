# AB Hypothesis Testing Ad Campaign Performance

An end-to-end **statistical & ML evaluation** pipeline for an online advertising A/B campaign, combining classical & sequential hypothesis testing with a machine learning–based analysis.

---

## Repository Structure

```plain
.
├── data/
│   └── AdSmartABdata.csv
├── notebooks/
│   ├── AB_Hypothesis_Testing_Ad_Campaign_Performance_(Classic_and_Sequential_AB_Testing_Analysis).ipynb
│   └── AB_Hypothesis_Testing_Ad_Campaign_Performance_(Machine_Learning_Analysis).ipynb
├── requirements.txt
└── README.md
```

---

## Quick Start

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/AB-Hypothesis-Testing-Ad-Campaign.git
   cd AB-Hypothesis-Testing-Ad-Campaign
   ```

2. **(Optional) Create and activate a virtual environment**

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate    # Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Lab or Notebook**

   ```bash
   jupyter lab  # or jupyter notebook
   ```

5. **Execute the notebooks**

---

## Notebooks

**Classic & Sequential A/B Testing**

It examines whether the interactive ad generated a higher “Yes” response compared to the control. The analysis begins with a one-sided two-sample z-test for proportions, followed by sequential monitoring with alpha spending. Results include final p-values, confidence intervals, and a visual of statistical boundaries over time.

**Machine Learning–Based Analysis**

It treats the A/B test as a supervised learning task. Data preparation and model training (logistic regression, decision tree, random forest, XGBoost, bagging, and stacking) are performed, with cross-validation AUC, precision, recall metrics reported. Feature importance rankings reveal the factors most strongly associated with brand awareness.

---

## Conclusions

The classical and sequential testing workflow indicates no statistically significant lift in “Yes” responses; the z-statistic remains within non-significant bounds throughout the monitoring period. Predictive performance in the machine learning approach is modest (AUC approximately 0.53–0.54), with contextual variables such as time of day and browser type exerting greater influence than ad exposure. These findings suggest that the interactive advertisement did not produce a meaningful increase in brand awareness in this experiment.
