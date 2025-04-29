# AB Hypothesis Testing Ad Campaign Performance

This repository contains a series of Jupyter notebooks that provide a comprehensive analysis of an online advertising campaign aimed at increasing brand awareness. Two distinct approaches are presented: classical hypothesis testing (including sequential analysis) and a machine learning–based evaluation of A/B testing results.

---

## **Objective**

The goal of these analyses is to determine whether exposure to a creative, interactive advertisement (the **exposed** group) leads to a statistically significant improvement in brand awareness—measured by the "Yes" response—to the question, "Do you know the brand SmartAd?" compared to a dummy advertisement (the **control** group).

**Two main approaches are explored:**

- **Classic and Sequential A/B Testing**  
  This approach uses standard hypothesis testing methods, including a one-sided two-sample z-test for proportions, and extends to sequential analysis with alpha spending adjustments. It provides insight into both the final aggregated data and the evolution of the test statistic over time.

- **Machine Learning-Based A/B Testing Analysis**  
  Here, the A/B testing problem is reframed as a supervised classification task. Multiple models—including Logistic Regression, Decision Trees, XGBoost, Random Forests, Bagging, and Stacking classifiers—are tuned and evaluated using cross-validation. The analysis not only measures overall predictive performance but also examines feature importances to assess the impact of the experimental treatment relative to other factors like time of day, browser type, and device characteristics.

---

## Prerequisites & Installation

The notebooks were developed using Python 3 and require several libraries. You can install the necessary dependencies using `pip`:

```bash
pip install numpy pandas scipy statsmodels plotly scikit-learn xgboost matplotlib seaborn
```

Alternatively, you can use the provided requirements.txt file (if available) by running:

```bash
pip install -r requirements.txt
```

---

## How to Run the Notebooks

1. **Clone the repository:**
   ```bash
   git clone https://github.com/<your-username>/AB-Hypothesis-Testing-Ad-campaign-performance.git
   cd AB-Hypothesis-Testing-Ad-campaign-performance
    ```

2. **Launch Jupyter Notebook or JupyterLab:**
    ```bash
   jupyter notebook
    ```
    or
    ```bash
   jupyter lab
    ```

3. **Open and Run the Notebooks**

    **Start with Classic_Sequential_AB_Testing.ipynb**  
    Review the hypothesis testing analysis contained within this notebook.

    **Then proceed to ML_AB_Testing.ipynb**  
    Explore the machine learning–based approach presented in this notebook.

---

## Conclusions

### Classic and Sequential Testing
The classical hypothesis testing approach indicates that, while the exposed group shows a marginally higher proportion of "Yes" responses, the difference is not statistically significant. The sequential analysis further supports this conclusion by showing that the cumulative z-statistic never crosses the predefined significance boundaries.

### Machine Learning Approach
Predictive models exhibit modest performance (AUC around 0.53–0.54), suggesting that the current feature set does not strongly predict brand awareness. Although the experimental condition is among the important features, factors such as time of day and browser type have a more pronounced effect.

Overall, both analytical approaches suggest that there is insufficient evidence to claim a significant improvement in brand awareness due to the ad exposure in this experiment.

