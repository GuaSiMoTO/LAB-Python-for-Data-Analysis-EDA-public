# LAB: Python for Data Analysis - Exploratory Data Analysis (EDA)

![Excel Image](https://user-images.githubusercontent.com/970858/63474771-d6734700-c469-11e9-83bb-9429da563909.png)

## Introduction

Welcome to the Exploratory Data Analysis (EDA) lab! As a junior data analyst at a retail company, your task is to explore and analyze a sales dataset to uncover valuable insights that can influence business decisions.

You will work with a dataset that includes various numerical and categorical variables related to sales transactions. Your goal is to perform a thorough exploratory analysis to identify trends, anomalies, and opportunities.

## Initial Setup

### Requirements
Start by forking the provided GitHub repository to your account and then clone it locally. This will be your workspace for completing the lab exercises.

- [Learn how to fork this repo](https://guides.github.com/activities/forking/)
- Clone this repo into your `code/labs` folder

### Scenario

Imagine you are a junior data analyst at a retail company. Your manager has asked you to perform an exploratory analysis of sales data to uncover actionable insights. Your task is to visualize and analyze this data, identifying trends, anomalies, and potential opportunities for the company.

### Starter Code

You have to solve the different problems in the `LAB-Exploratory-Data-Analysis.ipynb` notebook.

To get started, follow these steps:

1. Open your terminal and navigate to the `cloned-repo` directory:

    ```bash
    cd path/to/your/cloned-repo/
    ```

2. Launch Jupyter Notebook:

    ```bash
    jupyter lab
    ```

3. In the Jupyter Notebook interface, open the `LAB-Exploratory-Data-Analysis.ipynb` file.

To test that everything is set up correctly, run the first cell in the notebook. This cell usually contains import statements and initial setup code. If it runs without errors, you are ready to start solving the exercises.

You can write and execute your code in the provided cells within the notebook. Any outputs, including print statements and visualizations, will be displayed directly in the notebook, making it easy to debug and verify your solutions.

### Iteration 0: Install Dependencies

Make sure you have all the necessary libraries installed by using the `requirements.txt` file provided. You can install the dependencies with the following command:

```bash
pip install -r requirements.txt
```

## Iteration 1: Load and Inspect the Dataset
Now that you've set up your environment, let's dive into the heart of our data analysis task. Our first step is to load and inspect the dataset, which is crucial for understanding its structure and contents. This foundational step will help you get acquainted with the data, allowing you to identify what needs to be cleaned or further explored.

### Load the dataset
Using pandas, we will load the provided CSV file. This will give us an initial glimpse into the dataset, including the columns and the first few rows of data.

### Inspect the dataset
- Display the basic information about the dataset, such as the number of rows, columns, and data types of each column.
- Use descriptive statistics to understand the distribution of numerical and categorical variables.

[describe - Pandas Documentation](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)

This initial inspection is crucial as it sets the stage for the next steps of data cleaning and visualization.

## Iteration 2: Data Cleaning
With a solid understanding of the dataset's structure, it's time to focus on cleaning the data. Data cleaning ensures that the dataset is accurate, consistent, and ready for analysis. This step is essential to avoid misleading results and ensure that your insights are based on high-quality data.

### Handle missing values
- Identify columns with missing values and decide on an appropriate strategy to handle them (e.g., fill with mean/median, drop rows/columns).

### Remove duplicates
- Check for and remove any duplicate rows in the dataset.

### Correct data types
- Ensure all columns have the correct data types (e.g., dates should be in datetime format).

## Iteration 3: Data Visualization with Matplotlib and Seaborn
Having cleaned the data, you're now ready to explore it visually. Visualization is a powerful tool for uncovering patterns, trends, and anomalies in the data. In this iteration, you'll create various plots to get a better understanding of the dataset.

### Distribution of Numerical Variables
- Create histograms and box plots to understand the distribution and spread of all numerical variables.

### Categorical Variable Analysis
- Create bar plots to visualize the frequency of all different categories.

### Correlation Analysis
- Create a heatmap to visualize the correlations between numerical variables.

### Sales Trends Over Time
- Create line plots to analyze sales trends over different time periods.

**Tip**: search `resample` [method](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.resample.html).

### Sales by Category and Region
- Employ facet grids to visualize the distribution of sales data across different product categories and regions, enhancing comparative analysis.

### Pair Plot Analysis
- Utilize pair plots to simultaneously explore relationships between the numerical variables 'Sales' and 'Discount', facilitating quick identification of trends, correlations, and outliers.

## Iteration 4 — Hypothesis Testing  

In this iteration you will run the **Shapiro‑Wilk normality test** on the **`Sales`** variable to check whether it follows a normal distribution.

### Purpose  
Determine whether statistical methods that assume normality are appropriate and decide—if necessary—on an alternative scaling technique.

### Hypotheses  

| Hypothesis | Description |
|-----------|-------------|
| **H₀ (null)** | The **`Sales`** data come from a normal distribution. |
| **H₁ (alternative)** | The **`Sales`** data do **not** come from a normal distribution. |

### Decision rule  

* **α = 0.05**  
* If **p‑value > α** → fail to reject **H₀** ⇒ treat the data as normal.  
* If **p‑value ≤ α** → reject **H₀** ⇒ conclude the data are **not** normal.

> **Note:** If the data are not normal, consider a different scaling method such as **`MinMaxScaler`** or a power transformation (Box‑Cox / Yeo‑Johnson).

---

## Iteration 5 — Data Scaling  

Standardising numerical variables is essential before training machine‑learning models because it ensures that every feature contributes equally to the analysis.

### Steps to follow

1. **Select numerical variables**  
   - Identify the numeric columns you will scale: **`Sales`** and **`Discount`**.

2. **Choose and apply the scaler**  
   - If *Iteration 5* indicated normal data, use `StandardScaler` from `sklearn.preprocessing`.  
   - Otherwise, use `MinMaxScaler` (or another suitable transformer).  

3. **Verify the transformation**  
   - Confirm that the transformed variables have the expected range (mean ≈ 0 & SD ≈ 1 for `StandardScaler`, or 0 → 1 for `MinMaxScaler`) to make sure scaling was applied correctly.


## Iteration 6: Dimensionality Reduction with PCA

In this iteration, you'll apply Principal Component Analysis (PCA) to reduce the dimensionality of the dataset. This technique helps simplify the dataset by transforming it into a lower-dimensional space while retaining the most important features.

### Steps to Follow

1. **Prepare the Data:**
   - Standardize numerical features if they are not already standardized.

2. **Apply PCA:**
   - Use PCA to transform the dataset into principal components.

3. **Explore Component Loadings:**
   - Analyze the component loadings by visualizing them with a heatmap to understand the contribution of each original feature to the principal components. This helps in interpreting which features are most influential in the reduced dimensions.

## Bonus Challenge: Interactive Visualizations

## Interactive Elements with Plotly

For an added challenge, explore creating interactive visualizations and dashboards. This will make your data exploration more dynamic and engaging.
Convert one of the existing plots into an interactive visualization using Plotly.

## Apply Your Skills to a Real Dataset

Now that you have completed the lab exercises and gained confidence in loading, inspecting, and cleaning datasets, it's time to apply these skills to a real-world dataset. This will help you practice and reinforce your understanding of Exploratory Data Analysis (EDA).

You will be using the Music & Mental Health Survey Results dataset available on Kaggle. This dataset contains information from a survey about the relationship between music preferences and mental health, including details on favorite music genres, reported mental health conditions, and how they correlate.

- [Music & Mental Health Survey Results](https://www.kaggle.com/datasets/catherinerasgaitis/mxmh-survey-results/data)

## Submission
Once you have completed your analysis and visualizations, push your Jupyter notebook to your forked GitHub repository. Ensure that your final submission includes narratives explaining your visualizations and insights.


```bash
$ git add .
$ git commit -m "done"
$ git push origin main
```

Then create a Pull Request!!

## Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Ploty Documentation](https://plotly.com/python/).
- [Mann-Whitney U test - Scipy Documentation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mannwhitneyu.html).

![happy_coding](https://user-images.githubusercontent.com/970858/63899010-c23fc480-c9ea-11e9-84a2-542907e42362.png)
