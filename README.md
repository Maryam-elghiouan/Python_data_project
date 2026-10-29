# Data Job Market Analysis: Data Analyst Skills in the US

## Overview

This project analyzes 2023 job postings to understand what the data job market looks like for **Data Analysts in the United States**. It focuses on which skills employers ask for most, how demand changes over the year, how much these jobs pay, and which skills offer the best balance between demand and salary.

The goal is to turn raw job posting data into clear, practical answers, and to practice a full analysis workflow in Python: loading data, cleaning it, exploring it, and presenting results with charts.

## The Question

The analysis is organized around five questions, one per notebook:

1. **What are the most demanded skills** for the top data job roles?
2. **How are in-demand skills trending** over the year for Data Analysts?
3. **How well do jobs and skills pay** for Data Analysts?
4. **How do salaries compare** across data roles (Data Analyst, Data Engineer, Data Scientist, and senior versions)?
5. **What are the optimal skills to learn** for Data Analysts (high demand and high pay)?

## Project Structure

```
Python_Data_Project/
├── Advanced_python/
└── Project/
    ├── 1_Project_Intro.ipynb
    ├── 2_Skills_Count.ipynb
    ├── 3_Skills_Trend.ipynb
    ├── 4_Salary_Analysis.ipynb
    └── 5_Optimal_Skills.ipynb
```

## Tools I Used

| Tool | Purpose |
|---|---|
| **Python** | Main programming language |
| **Pandas** | Loading, cleaning, filtering, grouping, and reshaping data |
| **Matplotlib** | Building charts and customizing axes, labels, and annotations |
| **Seaborn** | Statistical charts (bar plots, line plots, box plots, scatter plots) |
| **Hugging Face `lukebarousse/data_jobs`** | Loading the job postings dataset |
| **Jupyter Notebooks** | Running the analysis step by step and documenting it |
| **VS Code** | Code editor |
| **Git and GitHub** | Version control and sharing the project |

## The Analysis

Each notebook starts with the same preparation: load the data, convert the posting date to a datetime, and convert the skills column into a list.

### 1. Skills Count
I filtered the data for the US, grouped by job title and skill, and counted how often each skill appears. I converted counts into **percentages of postings** so that roles with different numbers of jobs can be compared fairly. I then plotted the top 5 skills for each role with the percentage shown at the end of each bar.

### 2. Skills Trend
I filtered Data Analyst jobs in the US, created a month column from the posting date, exploded the skills list so each skill has its own row, and built a pivot table (months by skills). I divided each month by the total number of postings in that month to get a percentage, then plotted the top 5 skills as lines over the year.

### 3. Salary Analysis
I kept only postings with a yearly salary and compared salary distributions across roles with **box plots**. I also calculated the **median salary and number of postings per skill** for Data Analysts, to find both the highest paid skills and the most in-demand skills.

### 4. Optimal Skills
I combined demand (percentage of postings) and pay (median salary) for the most in-demand skills, and showed them in a scatter plot. Skills were colored by technology type (programming, analyst tools, databases) to make the chart easier to read.

## What I Learned: My Journey from Basics to Project

### Stage 1: Python Basics
I started with the fundamentals: variables, data types, loops, conditions, and functions. This gave me the logic needed to read and write code, and the habit of reading error messages instead of fearing them.

### Stage 2: Advanced Python and Data Analysis
Then I moved to the tools of data analysis:
- **Pandas**: accessing and filtering data, working with dates, `groupby`, merging and concatenating tables, pivot tables, and `explode` for list columns.
- **Matplotlib and Seaborn**: bar charts, line charts, box plots, and scatter plots, and how to customize labels, axes, and colors so a chart is easy to read.

### Stage 3: The Project
I applied everything to real job posting data. This is where I learned the most, because the data was messy and nothing was given step by step:
- Turning counts into correct **percentages** (using the right totals).
- Choosing the right chart for each question.
- Debugging real errors and fixing unreadable charts (overlapping labels, scientific notation, confusing colors).
- Setting up a professional workflow: virtual environments, VS Code notebooks, Git, and GitHub.

### Main Takeaway
Following a tutorial is easy; **applying it alone is where learning happens**. Each error I fixed taught me more than the code that worked the first time.VS Code, and organizing a project into folders.

## Insights

- **SQL is the most requested skill for Data Analysts** (about half of postings), followed by **Excel**, **Tableau**, and **Python**.
- Demand for the top skills stays **fairly stable across the year**, with a small decline toward the end of 2023.
- **Python is more important for Data Scientists (about 72%) and Data Engineers (about 65%)** than for Data Analysts (about 27%).
- **Senior roles and Data Scientists have higher salary ranges**, and every role has large outliers on the high end.
- The **highest paid skills** for Data Analysts (such as `dplyr`, `bitbucket`, `gitlab`) are specialized and rarely requested, so a high salary here is based on few postings.
- **Python offers the best combination for Data Analysts**: a high median salary (close to $97K) with solid demand. **SQL** has the highest demand, with a good median salary.
- Common office tools (**Word**, **PowerPoint**, **Excel**) are requested often but are associated with the lowest median salaries.

## Challenges I Faced

- **Slow internet and large packages**: installing `## 📁 Dataset
* **Dataset Name**: `lukebarousse/data_jobs`
* **Source**: [Hugging Face - lukebarousse/data_jobs](https://huggingface.co/datasets/lukebarousse/data_jobs)
* ` meant downloading heavy dependencies such as `pyarrow`, and the download was interrupted once. I learned that pip resumes and reuses its cache.
- **Python 3.14 is very recent**, so I had to be careful that libraries supported it, and I learned when a virtual environment is worth creating.
- **Common errors**: `ModuleNotFoundError`, `TypeError: 'DataFrame' object is not callable`, and `'Axes' object is not subscriptable`. These taught me to read the error message and check variable names and parentheses.
- **Forgetting to assign results**: methods like `reset_index()` return a new object, so the result must be saved.
- **Chart readability**: overlapping labels (Python and Tableau at the end of the trend chart), scientific notation (`1e6`) on the salary axis, and confusing colors when color and sorting followed different columns.
- **Percentages need the right denominator**: totals must come from the postings count, not from the exploded skills table.
- **Project setup**: renaming folders blocked by OneDrive and open kernels, and working with notebooks in VS Code.

## Conclusion

For someone aiming to become a Data Analyst in the US, the data points to a clear learning path: **start with SQL and Excel, add a visualization tool such as Tableau, and learn Python**, which combines strong demand with high pay. Very high-paying niche skills exist, but they appear in few postings, so they are better as a second step than a first priority.

Beyond the results, this project helped me practice the full workflow of a data analysis: asking a question, preparing the data, analyzing it, visualizing it, and explaining what it means.

## Dataset

Job postings dataset (2023) loaded with the Hugging Face `## 📁 Dataset
* **Dataset Name**: `lukebarousse/data_jobs`
* **Source**: [Hugging Face - lukebarousse/data_jobs](https://huggingface.co/datasets/lukebarousse/data_jobs)` library.
## How to Run
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate

Then open the notebooks in VS Code, select the `.venv` kernel, and run the cells in order.
