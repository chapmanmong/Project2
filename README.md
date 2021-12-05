# Table of Contents
1. [Introduction- Project In the News](#Introduction)
2. [Data, Technology and Coding Standards](#Paragraph1)
   1. [Data Sources](#SubParagraph1)
   2. [Technology Stack](#Subparagraph2) 
   3. [Coding and Release Standards](#Subparagraph3)
3. [Data Cleanse and Model Evaluation](#Paragraph2)
   1. [Data Cleanse](#SubParagraph4)
   2. [Model- Summary](#SubParagraph5)
   3. [Model- Prediction](#Subparagraph6) 
   4. [Model- Evaluation with Visualisations](#Subparagraph7)
   5. [Key Findings](#Subparagraph8)   
4. [Recommendations](#Paragraph3)
5. [References](#Paragraph4)

<div style="page-break-after: always;"></div>

## Introduction- Project In the News <a name="Introduction"></a>

ACT-Right is a investment advisory firm that has requested an evaluation of the media impact on the price of stocks. Project In the News seeks to answer the following questions using established Natural Language and Linear Regression Model:

- Can the sentiment for a stock be determined based on it being in the news?
- Is there any relationship between stock price and its sentiment? 
- Can sentiment be used to predict price of a stock?
- Should ACT- Right use the developed model?

## Data, Technology and Coding Standards <a name="paragraph1"></a>
### Data Sources <a name="subparagraph1"></a>

Multiple media channels covering Social media as well as traditional news channels were reviewed- the following have been used in this project:

- Reddit (Import library- Praw using pip install)
- Twitter
- News API 

Data Sources:

[Reddit](https://www.reddit.com/dev/api/)
[Twitter](https://developer.twitter.com/en/docs/twitter-api)
[NewsAPI](https://newsapi.org/docs)

The Alpaca trading platform has been used to retrieve the ticker price data for 7 days.
[Alpaca](https://alpaca.markets/docs/api-documentation/)

Keys will be required for all of the above.

### Technology Stack <a name="subparagraph2"></a>

The following additional technologies have been deployed:
- Vader Sentiment Analysis
- Amazon Sagemaker
- Scikit Learn


### Coding and Release Standards <a name="subparagraph3"></a>

Following rules have been applied during code development and testing:
1. A folder called Images will be created to store visualisations.
2. All variables must be in lower case and reflect their purpose. Underscore to be used as and when required. 
3. Each step of the code must contain comments to explain the purpose of the code.
4. A git hub repository called Project2 must be set up.
5. Each release must provide a brief message on changes made prior to committing the code.
6. On successful testing of the code in Jupyter Labs, the notebook must be deployed to AWS- Sagemaker environment.


## Data Cleanse and Model Evaluation <a name="paragraph2"></a>
### Data Cleanse <a name="subparagraph4"></a>

The following data cleanse rules have been applied to the source data set:

1. Identified data set must be formatted correctly prior to use- Date format yyyy/mm/dd.
2. The date range for source data is set to the maximum permitted for each source e.g. Twitter is 7 days, NewsAPI is 30 days, Alpaca is 6 months while Reddit is based on number of tweets.
3. Redundant data, if any, must be dropped.
4. Sentiment scores have been assigned zero where blank.
5. Duplicates, if any must be dropped.
6. All dataframe columns must have appropriate and correct headers.
7. Records are sorted on the required fields.
8. Validate that entire data set has been correctly loaded.

### Model- Summary <a name="subparagraph5"></a>

- Post data pre processing, Vader Sentiment analysis has been used to determine the sentiment for each of the stocks. 
- Linear Regression Model has been used to predict percent change in closing prices.
- The Vader compound sentiment score of each media and stock trading volumes have been used as features (x). 
- The percent change of closing prices is set as the target (y).
- This dataframe has then been split into train and test data based on the limited data available.
- The train data has been used to fit the model.
- The test data has been used to predict.
- The predictions have been visualised for comparison purposes.

An additional model for NewsAPI sentiment has also been set up. 

### Model- Prediction <a name="subparagraph6"></a>
The Linear Regression Model has been applied to predict the percent change in closing price of stock. A simple line chart has been used to visualise the results.


### Model- Evaluation with Visualisations <a name="subparagraph7"></a>

Below is the visual representation of the analysis:
![TSLA Model Predictions)https://github.com/chapmanmong/Project2/blob/main/images/TSLA%20Combined%20Results.PNG

![TSLA Model Visualisation]


### Key Findings <a name="subparagraph8"></a>

1. Can  the "sentiment" of a stock be determined based on it being in the news?

The Vader sentiment tool can be used to determine the "sentiment" associated with the stock. The normalised Compound score has been used in the model.

2. Is there any relationship between the stock price and its sentiment? 

Based on the model and the limited data available, it is difficult to provide conclusive evidence of correlation between sentiment and stock price.

3. Can the sentiment be used to predict price of a stock?

Considering the data limitations that have been encountered, it is suggested that a more extensive data set be used to confirm the model predictions.


## Recommendations <a name="paragraph3"></a>

4. Should ACT- Right use the developed model? 

ACT-Right should allocate more funds to sourcing a comprehensive data set so that more robustness is built into the model.


## References <a name="paragraph4"></a>
(https://www.reddit.com/dev/api/)

(https://newsapi.org/docs)

(https://alpaca.markets/docs/api-documentation/)

(https://developer.twitter.com/en/docs/twitter-api/premium/search-api/quick-start/premium-30-day)

