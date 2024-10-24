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
- Create bar plots and box plots to compare sales across different product categories and geographical regions.

## Iteration 4: Advanced Visualizations and Insights
Building on the initial visualizations, it's time to dive deeper with advanced techniques. These visualizations will provide more nuanced insights and allow you to explore relationships between multiple variables.

### Pair Plot Analysis
- Utilize pair plots to simultaneously explore relationships between the numerical variables 'Sales' and 'Discount', facilitating quick identification of trends, correlations, and outliers.

### Facet Grids
- Employ facet grids to visualize the distribution of sales data across different product categories and regions, enhancing comparative analysis.

## Iteration 5: Data Scaling
 
Standardizing numerical variables is an important step, especially when preparing data for machine learning models. This iteration focuses on scaling your data to ensure that all features contribute equally to the analysis.

**Steps to Follow:**

1. **Select the Numerical Variables:**
   - Identify the numerical columns in the sales dataset that you want to standardize. The columns in your dataset are Sales and Discount.
  
2. Standardize the Variables:
    - Use `StandardScaler` from `sklearn.preprocessing` to standardize the selected numerical variables. This process will transform the data so that each            variable has a mean of 0 and a standard deviation of 1.

3. **Verify the Transformation:**
   - Check that the standardized variables have a mean close to 0 and a standard deviation close to 1 to ensure the standardization was applied correctly.
---

## Iteration 6: Hypothesis Testing

Hypothesis testing allows you to make statistical inferences about the data. In this iteration,you will perform the Shapiro-Wilk Normality Test.

The Shapiro-Wilk test will be conducted on the sales data from both the East and West regions to assess whether the sales data follows a normal distribution. This test is appropriate for small to medium-sized datasets and evaluates if the data is normally distributed.

Null Hypothesis (H0): The sales data follows a normal distribution.
Alternative Hypothesis (H1): The sales data does not follow a normal distribution.

If the resulting p-value is greater than the significance level (α = 0.05), we fail to reject the null hypothesis, indicating that the data is normally distributed. If the p-value is less than 0.05, we reject the null hypothesis, indicating that the data does not follow a normal distribution.


## Iteration 7: Dimensionality Reduction with PCA

In this iteration, you'll apply Principal Component Analysis (PCA) to reduce the dimensionality of the dataset. This technique helps simplify the dataset by transforming it into a lower-dimensional space while retaining the most important features.

### Steps to Follow

1. **Prepare the Data:**
   - Standardize numerical features if they are not already standardized.

2. **Apply PCA:**
   - Use PCA to transform the dataset into principal components.

3. **Analyze Results:**
   - Examine the explained variance ratio to understand how much variance each principal component captures.

4. **Visualize PCA Components:**
   - Create a scatter plot to visualize the distribution of the data in the reduced feature space.
5. **Explore Component Loadings:**
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
