# Enhancing Product Categorization on Amazon through NLP and Machine Learning Techniques

Team Members: [Tiffany Gunawan](https://github.com/kuwtiiff), [Neha Sharma](https://github.com/amarasharma), and [Baraa Zekeria](https://github.com/bzekeria)

<a id='overview'></a>
## Overview
This project aims to develop a classification model to categorize product names accurately on Amazon products. The workflow begins with data cleaning, including removing punctuation, converting text to lowercase, and eliminating stopwords. Next, exploratory data analysis is performed to gain insights into the dataset and visualize keyword prominence within each category. The text is then transformed using TF-IDF, capturing important features and representing the data numerically. Two classification algorithms, Multinomial Naive Bayes and Logistic Regression, are trained and evaluated using metrics like accuracy, precision, recall, and F1-score. The goal is to automate the categorization process and improve efficiency.

<a id='start'></a>
## Getting Started

To get started with the project, follow these steps:
<!--2. Install the required dependencies: `pip install -r requirements.txt`-->
1. Clone the repository: `git clone https://github.com/bzekeria/cogs109-final-project.git`
1. Explore the `notebooks/` directory for step-by-step analysis and modeling.
1. Access the `reports/` directory for project reports and documentation.

**Note:** This project utilizes Google Colab instead of JupyterHub, so the directory structure in the notebooks may not align with the directory structure on your local machine. Please make the necessary adjustments when running the notebook locally on your computer. See the example below:
  - To read in the data file for ```00_data_preprocessing.ipynb```
    - Change this
    ```py
       from google.colab import drive 
       drive.mount('/content/drive')
       df = pd.read_csv("drive/MyDrive/COGS 109 Amazon Project/Data/amazon_products_raw.csv")
    ``` 
    -  To this
    ```py
    df = pd.read_csv("data/amazon_products_raw.csv")
    ```

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
│   └── ...
├── .gitignore
├── README.md
```
