## CFPB Consumer Complaint Analysis

## About the Project

This project is about analyzing consumer complaints from the Consumer Financial Protection Bureau (CFPB).

I wanted to understand how company response time and the type of financial product are related to the outcome of a complaint. In particular, I looked at whether consumers received relief and whether response time was different across different types of financial products.

The dataset used in this project contains around 5.6 million resolved complaints, so it was a good opportunity to work with a large real-world dataset.

## Main Questions

Some of the questions I looked at were:

- Does company response time have a relationship with consumer relief?
- Does the financial product affect the complaint outcome?
- Are some types of complaints taking longer to respond to?
- Does the relationship between response time and consumer relief change depending on the financial product?

## Dataset

The data comes from the CFPB Consumer Complaint Database.

Some of the information in the dataset includes:

- Financial product
- Complaint issue
- Company
- Complaint dates
- Company response
- Complaint resolution information

The full dataset is not included in this repository because of the size of the data.

## What I Did

First, I cleaned the data and worked with the date columns to calculate the response time.

Response time was calculated as the number of days between when the complaint was received and when it was sent to the company.

I also created a `consumer_relief` variable:

- 1 = consumer received relief
- 0 = no relief

After that I did some exploratory data analysis to look at the response time distribution and differences between financial products.

Some of the charts I created include:

- Distribution of company response time
- Average response time by financial product
- Response time by consumer relief
- Consumer relief rate by response time
- Response time by product and consumer relief

## Statistical Analysis

I used logistic regression because consumer relief is a binary outcome.

The model looked at response time and financial product categories to understand their relationship with consumer relief.

I also added interaction terms between response time and financial product. This was done to see if response time has a different relationship with consumer relief for different types of products.

Since response time is very skewed, I also looked at using a negative binomial regression approach for the response-time analysis.

## Some Results

The dataset had about 5.63 million resolved complaints.

The average response time was around 0.55 days and the median was 0 days. This means a large number of complaints were sent to the company on the same day.

There were also some very large response times, with the maximum being 1,962 days. Because of this, the response time distribution was heavily right skewed.

Around 39% of the complaints resulted in consumer relief.

The logistic regression showed a statistically significant negative relationship between response time and consumer relief. The response time coefficient in the refined model was -0.0140 with a p-value less than 0.001.

I also found differences between financial product categories. The interaction analysis showed that the relationship between response time and consumer relief was not exactly the same for every product category.

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Jupyter Notebook

## Skills

- Data Cleaning
- Exploratory Data Analysis
- Data Visualization
- Feature Engineering
- Statistical Analysis
- Logistic Regression
- Interaction Analysis
- Regression Modeling
- Working with Large Datasets

Note

The original CFPB dataset is not uploaded here because it is very large. The notebook contains the analysis and preprocessing steps used for the project.

Author

Mahitha Kalinathabotla
