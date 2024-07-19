# LAB: Python for Data Analysis - Exploratory Data Analysis (EDA)

## Introduction

Hello everyone! In this session, we will explore the use of pandas, Matplotlib, and Seaborn to perform Exploratory Data Analysis (EDA). This includes learning how to load datasets, clean data, and create various visualizations to understand the underlying patterns and insights in the data. Imagine you are part of a small team at a company, and you need to analyze the team's data using Python. This lab will empower you with the techniques to perform thorough EDA, making you more effective in your data handling roles.

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
# Iteration 1: Load and Inspect the Dataset
In this iteration, you will learn to load the dataset, inspect its structure, and understand the basic statistics of the data.

## Load the dataset
Use pandas to load the provided CSV file and inspect the first few rows to understand its structure.

## Inspect the dataset
- Display the basic information about the dataset, such as the number of rows, columns, and data types of each column.
- Use descriptive statistics to understand the distribution of numerical variables.

# Iteration 2: Data Cleaning
In this iteration, you will handle missing values, duplicate rows, and incorrect data types.

## Handle missing values
- Identify columns with missing values and decide on an appropriate strategy to handle them (e.g., fill with mean/median, drop rows/columns).

## Remove duplicates
- Check for and remove any duplicate rows in the dataset.

## Correct data types
- Ensure all columns have the correct data types (e.g., dates should be in datetime format).

# Iteration 3: Data Visualization with Matplotlib and Seaborn
In this iteration, you will create various visualizations to explore the data.

## Distribution of Numerical Variables
- Create histograms and box plots to understand the distribution and spread of numerical variables.

## Categorical Variable Analysis
- Create bar plots to visualize the frequency of different categories.

## Correlation Analysis
- Create a heatmap to visualize the correlations between numerical variables.

## Sales Trends Over Time
- Create line plots to analyze sales trends over different time periods.

## Sales by Category and Region
- Create bar plots and box plots to compare sales across different product categories and geographical regions.

# Iteration 4: Advanced Visualizations and Insights
In this iteration, you will create more complex visualizations to uncover deeper insights.

## Pair Plot Analysis
- Use pair plots to explore relationships between multiple variables simultaneously.

## Facet Grids
- Create facet grids to visualize distributions across different subsets of data.

## Enhanced Visualizations
- Add annotations, customize color maps, and adjust axes properties for clarity and visual appeal.

# Iteration 5: Data Scaling
In this iteration, you will standardize the numerical variables in your dataset, specifically Sales and Discount, to have a mean of 0 and a standard deviation of 1. This ensures all features contribute equally to the analysis and improves the performance of machine learning models. Ensures that Sales and Discount are on the same scale, making comparisons more meaningfulIn this iteration, you will standardize the Sales and Discount columns to have a mean of 0 and a standard deviation of 1. This helps improve model performance, allows for fair comparisons between features, and enhances visualizations by ensuring all data points contribute equally to the analysis. Use StandardScaler from sklearn.preprocessing to transform these columns.

# Iteration 6: Hypothesis Testing
In this iteration, you will perform hypothesis testing to compare sales between different regions. Specifically, you will use a two-sample T-test to determine if there is a significant difference in the average sales between two regions (e.g., 'North' and 'South'). This test helps you understand if the observed differences in sales are statistically significant or if they could have occurred by random chance.

# Iteration 7: Summarize Findings
In this final iteration, you will summarize your findings and prepare a presentation for stakeholders.

Summarize the key insights obtained from the analysis in a clear and concise manner.

## Presentation-Ready Visuals
- Apply different Seaborn styles and color palettes to improve visual presentation.

## Create a Report
- Compile the visualizations and insights into a report or presentation format.

# Bonus Challenge: Interactive Visualizations
## Interactive Elements with Plotly
- Convert one of the existing plots into an interactive visualization using Plotly.

# Dashboard Layout
## Dashboard with Multiple Plots
- Create a dashboard layout with multiple subplots to show different aspects of the data in a single visualization.

# Submission
Once you have completed your analysis and visualizations, push your Jupyter notebook to your forked GitHub repository. Ensure that your final submission includes narratives explaining your visualizations and insights.


```bash
$ git add .
$ git commit -m "done"
$ git push origin main
```

Then create a Pull Request!!

# Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Python Graph Gallery](https://www.python-graph-gallery.com/) for inspiration and code snippets.
- [Plotly Documentation](https://plotly.com/python/)

![happy_coding](https://user-images.githubusercontent.com/970858/63899010-c23fc480-c9ea-11e9-84a2-542907e42362.png)
