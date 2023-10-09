# Home-Credit
Utilize Pandas and other Python libraries to generate and communicate business insights from a data set.

### Deliverables
A Jupyter Notebook containing:
- Imported data, including at least two DataFrames and at least one combination of DataFrames via methods such as joining.
- Functions for cleaning the data set, with explanations for how null values are being handled in each field.
- At least two visualizations accompanied by textual descriptions of the business insights they communicate.

### Data Analytics Process:
Frame 
- Develops well-informed, hypothesis-driven business questions for analysis.
- Demonstrates ability to iterate and refine business questions based on new insights.

Extract
- Selects data that is relevant to the hypothesis-driven business question(s). 
- Uses data extraction techniques and formatting appropriate for the selected data.

Wrangle/Prepare
- Implements data cleaning techniques such as removing duplicates and correcting erroneous values. 
- Organizes raw data into a workable, analytics-friendly format. 

Analyze
- Manipulates data for exploration, insight gathering, and analysis.
- Uses rationale for revising the original business question, collecting more data based on the initial analysis, or continuing on to interpretation. 

Interpret
- Creates appropriate visualizations that support the findings and insights. 
- Identifies key insights pertaining to the original business question(s).
- Incorporates results of the analysis to support decisions and recommendations.

## Contents:
- Introduction
- Data
- Methodology
- Results
- Conclusions and Recommendations
- Tables

## Introduction
Problem Statement
Home Credit is looking for patterns in its data regarding the default risk of consumer loans. Conduct an analysis to surface any notable patterns related to default risk.

According to this [article on default risk](https://www.investopedia.com/terms/d/defaultrisk.asp#:~:text=Default%20risk%20refers%20to%20the,credit%20reports%20and%20credit%20scores), 
there's some important things to consider in terms of default risks:
- Default risk refers to how likely borrowers won't be able to make their required debt payments to a lender.
- Check borrowers' credit reports and credit scores.
- The default risks are rated by rating agencies.

Hypothesis: 
- Borrowers with risky debt-to-income ratios where they are borrowing more than they can earn. 
- And those with high default risk will typically pay higher interest rates and are more likely to be at high risk for loan defaults.

## Data

Data was obtained from [Kaggle](https://www.kaggle.com), a website that hosts data science competitions and crowdsources social challenges from across the world. This particular dataset was from the [Home Credit Default Risk](https://www.kaggle.com/competitions/home-credit-default-risk/data) competition.

The selected dataframes consist of ~160 features consisting of binary, ordinal, and categorical responses. The data dictionary from Kaggle is provided in the [Dataset Description](https://www.kaggle.com/competitions/home-credit-default-risk/data) and specific details in the HomeCredit_columns_descriptions.csv file.

## Methodology

1. First, conduct exploratory data analysis and NULLs imputation on the two datasets.
2. Created a debt-to-income ratio column and a risky borrowers column to identify existing consumers’ spending patterns related to consumer loan default risk.
3. Then, merge via INNER JOIN to the final dataset for data visualizations via Pandas and Matplotlib.

## Results
### EDA and Cleaning
Exploring and Imputing Nulls:
- Columns such as AMT_annuity, AMT_GOODS_PRICE, CNT_Payment, PRODUCT_COMBINATION, and AMT_CREDIT had NULLS. Due to the importance of these columns for data analysis, I decided to replace the missing values by using the MEAN for all columns, except for AMT_CREDIT. Decided to use the Mode which is 0. 


### Installing

A step-by-step series of examples that tell you how to get a development
environment running

1. Download and open your open-source code editor. 

2. Download John Bacolores_Home_Credit.ipynb file.

3. Upload John Bacolores_Home_Credit.ipynb file.

## Running the tests

Run all cells. Awaiting user commands in the final cell of the notebook. 

### Sample Tests

How to add a transaction: Press [a] to add a transaction

    [a] then "Enter"

Input the title of the transaction:

    Check from brother

What is the category:

    income or expense

Enter the amount:

    500

Input the date in mm/dd/yyyy format:

    08/29/2023

Returns to user input: 

    Press [a] to add a transaction, [b] to view the account balance, [v] to view all transactions, or [q] to quit.

## Deployment

N/A - can launch via Jupyter Notebook

### Post-MVP Goals:
- The program allows you to track multiple accounts
- The program can analyze profit and loss for a specific month or year
- The program can provide high-level stats, such as average transaction size
- The program can track and analyze transactions by specific customers or vendors

## Built With

  - [Contributor Covenant](https://www.contributor-covenant.org/) - Used
    for the Code of Conduct
  - [Creative Commons](https://creativecommons.org/) - Used to choose
    the license

## Authors

- **Billie Thompson** - *Provided README Template* -
    [PurpleBooth](https://github.com/PurpleBooth)

## Acknowledgments

- Hat tip to anyone whose code is used
- **Paula Bannerman** - *Provided guidance and oversight* - [dcartist](https://github.com/dcartist)
- **Andrew Riddle** - *Provided guidance and oversight* - [ajriddle](https://github.com/ajriddle)
