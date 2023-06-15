# Enhancing Product Categorization on Amazon through NLP and Machine Learning Techniques

<a id='overview'></a>
## Overview
This project aims to develop a classification model to categorize product names accurately on Amazon products. The workflow begins with data cleaning, including removing punctuation, converting text to lowercase, and eliminating stopwords. Next, exploratory data analysis is performed to gain insights into the dataset and visualize keyword prominence within each category. The text is then transformed using TF-IDF, capturing important features and representing the data numerically. Two classification algorithms, Multinomial Naive Bayes and Logistic Regression, are trained and evaluated using metrics like accuracy, precision, recall, and F1-score. The goal is to automate the categorization process and improve efficiency.

<a id='start'></a>
## Getting Started

To get started with the project, follow these steps:
<!--2. Install the required dependencies: `pip install -r requirements.txt`-->
1. Clone the repository: `git clone https://github.com/bzekeria/cogs109-final-project.git`
  - #### To make changes, follow this:
    1. **Before any changes made**: 
        - ```cd cogs109-final-project```
        - ```git pull```
    1. **After you make a change**:
        - ```git add [file-name]```
        - ```git commit -m "[add short message on what you did]"```
        - ```git push```
3. Explore the `notebooks/` directory for step-by-step analysis and modeling.
4. Access the `reports/` directory for project reports and documentation.

<a id='directory'></a>
## Directory Structure

The repository is organized as follows:

```bash
cogs109-final-project/
├── meetings/
│   ├── timeline.md
│   └── ...
├── notebooks/
│   ├── data/
│   ├── 00_reduce_data.ipynb
│   ├── 01_data_preprocessing.ipynb
│   └── ...
├── reports/
│   └── project_report.pdf
├── .gitignore
├── README.md
└── requirements.txt
```
