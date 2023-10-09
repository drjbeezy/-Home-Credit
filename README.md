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
- Columns such as AMT_annuity, AMT_GOODS_PRICE, CNT_Payment, PRODUCT_COMBINATION, and AMT_CREDIT had NULLS. Due to the importance of these columns for data analysis, I decided to replace the missing values by using the MEAN for all columns, except for AMT_CREDIT - decided to use the Mode = 0. 

### Amount Of Borrowers Who Are at Risk for Defaulting on Consumer Loans
Of the customers who took out Consumer loans, almost 600,000 were able to pay [0] versus the <50,000 (<10%) [1] who couldn't and were at risk of defaulting on their loan (Figure 1).

![Figure 1](https://github.com/drjbeezy/-Home-Credit/blob/main/%23%20Of%20Borrowers%20with%20Types%20of%20Loans.png?raw=true)

### Amount Of High Default Risk Borrowers With High-Interest Rates
Of the 50,000 who were at risk of defaulting on their loans, ~17,500 accrued high-interest rates due to their inability to pay either the amount and/or on time (Figure 2).

![Figure 2](https://github.com/drjbeezy/-Home-Credit/blob/main/%23%20of%20High%20Default%20Risk%20Borrowers%20by%20Interest%20Rate.png?raw=true)

### Risky Borrowers and Collateral
Finally, of all consumers with high interest rates due to their inability to pay either the amount and/or on time, they could use their car and home as collateral, respectively. 20,000+ did not own a car but did own their home and could use it as collateral. 10,000+ could use their car and home as collateral vs. the 10,000 who had neither. ~5000 could use their car as collateral but did not own a home.  (Figure 2).

![Figure 3](https://github.com/drjbeezy/-Home-Credit/blob/main/Risky%20Borrowers%20Car%20and%3AOr%20Home%20Ownership%20as%20Collateral.png?raw=true)

### Conclusions and Recommendations

As suspected, borrowers with risky debt-to-income ratios are borrowing more than they can earn. Those with high default risk will typically pay higher interest rates and are more likely to be at high risk for loan defaults. They can use their car and house as collateral, but the majority of high risk borrowers can typically use their own as collateral since most don't own a car. 

## Authors

- **Lavanya Acharya** - *Referenced Modeling Flu Survey Data* -
    [LAcharya](https://github.com/LAcharya/Modeling-Flu-Survey-Data)

## Acknowledgments

- **Paula Bannerman** - *Provided guidance and oversight* - [dcartist](https://github.com/dcartist)
- **Andrew Riddle** - *Provided guidance and oversight* - [ajriddle](https://github.com/ajriddle)
