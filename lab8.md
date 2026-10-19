# Lab 8

## Basic plotting

### Code from class

```
import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns

taxis.describe(include = "all")

# create a histogram for fare
sns.displot(data = taxis, x = "fare")
plt.show()

# create a bar plot for pickup_borough
sns.displot(data = taxis, x = "pickup_borough")
plt.show()

# Create a histogram of the "total_bill" variable
sns.displot(data=tips, x="total_bill")
plt.show()

# Create a histogram of the "total_bill" variable colored by "smoker" and faceted by "time"
sns.displot(data=tips, x="total_bill",hue = "smoker", col="time", kind = "hist")
plt.show()

sns.displot(data=tips, x = "tip", hue="time", kind="kde")
plt.show()
```

Documentation for function:
* `displot`: https://seaborn.pydata.org/generated/seaborn.displot.html

## Lab exercises

You will submit the .html version of your Jupyter Notebook for this assignment (File --> Save and export notebook as... --> html). Label the code that answers each question with a comment or a Markdown block. 

1. Download the college majors dataset and load it using pandas: https://drive.google.com/file/d/1WK9sQdr_S7RHDUIdEBPZ88dPeOUvTY7E/view?usp=sharing (you can find documentation about this dataset here: https://www.kaggle.com/datasets/fivethirtyeight/fivethirtyeight-college-majors-dataset
1. Use the `.head()` command to display the first 7 rows of the data frame.
1. Use `.shape` to find the number of rows and columns of the dataframe.
1. Use `.describe(include="all")` to calculate basic summary statistics for the data.
1. State a few things you learned from these summary statistics.  
1. Use `value_counts()`  to find the frequency of each value in the following columns: "Major", "Major_category", "STEM"
1. Display `Major` and `Median_salary` for the three majors with the highest median salaries (use `sort_values()` in descending order and `head()).
1. Filter the rows of the data frame based on the following conditions: `ShareWomen` greater than 0.5, `STEM` equal to "STEM", `Unemployment_rate" less than 0.05, and `Median_salary` greater than 40,000.
1. Create a histogram for one of the quantitative variables in the dataset. Set `hue` as one of the non-quantitative columns.
1. What can you learn from the plot you created? Feel free to try different combinations of variables until you find something interesting. 
1. Create a bar plot for one of the non-quantitative variables. Set `col` as one of the non-quantitative columns.
1. What can you learn from the plot you created? Feel free to try different combinations of variables until you find something interesting.
1. Think of a question about this dataset that you can answer using the tools we've learned so far (for example, "what's the difference in employment rate between STEM and non-STEM majors?").
1. Answer your question. Try to gather as much relevant evidence as you can (e.g. plot(s), values in the dataframe, etc). Describe what you are able to conclude.    
1. Download your jupyter notebook as an html file and submit it (File --> Save and export notebook as... --> html). Make sure each question is labeled in the notebook.

