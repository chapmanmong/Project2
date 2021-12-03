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

ACT-Right is a investment advisory firm that has requested an evaluation of media impact on the price of stocks. Project In the News seeks to answer the following questions using established Natural Language and Linear Regression Model:

- Can the sentiment for a stock be determined based on it being in the news?
- Is there any relationship between stock price and its sentiment? 
- Can sentiment be used to predict price of a stock?
- Should ACT- Right use the developed model?

## Data, Technology and Coding Standards <a name="paragraph1"></a>
### Data Sources <a name="subparagraph1"></a>

Multiple media channels covering Social media as well as tranditional news channels were reviewed- the following have been used in this project:

- Reddit
- Twitter
- News API 

Data Sources:

[Reddit](https://www.reddit.com/dev/api/)
[Twitter](?)
[NewsAPI](https://newsapi.org/docs)

The Alpaca trading platform has been used to retreive the ticker price data for 7 days.
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
4. Each step of the code must contain comments to explain the purpose of the code.
5. A git hub repository called Project2 must be set up with branches for each developer.
6. Each release must provide a brief message on changes made prior to committing the code.

## Data Cleanse and Model Evaluation <a name="paragraph2"></a>
### Data Cleanse <a name="subparagraph4"></a>

The following data cleanse rules have been applied to the source data set:

1. Identified data set must be formatted correctly prior to use- Date format yyyy/mm/dd.
2. The date range for source data is set to last 30 days except for Twitter as this data is available only for last 7 days.
3. Redundant data, if any, must be dropped.
4. Duplicates, if any must be dropped.
5. All dataframe columns have appropriate and correct headers.
6. Records are sorted on the required fields.
7. Validate that entire data set has been correctly loaded.

### Model- Summary <a name="subparagraph5"></a>

- Post data pre processing, Vader Sentiment analysis has been used to determine the sentiment for each of the stocks. 
- Linear Regression Model has been used to predict prices.
- The high, low, close, volume, percentage change and the compound sentiment have been used as features.
- The closing prices is set as target (y).
- This dataframe has then been split into train and test data.
- The train data has been used to fit the model.
- The test data has been used to prdict.
- The predictions have been visualised for comparison purposes.

Note that Twitter and Reddit have been set up only for Sentiment Analysis/ Data visualisation due to the data/time constraint. Twitter and Reddit sentiments not used in Model.

### Model- Prediction <a name="subparagraph6"></a>
The Linear Regression has been applied to predict the sentiment and the visualisation of its impact on the closing price of a stock.


### Model- Evaluation with Visualisations <a name="subparagraph7"></a>

Below is the visual representation of the analysis:
![Percent  change in closing prices](https://github.com/chirathlv/Project1/blob/Renu/Images/Total%20Wine%20Sales%20per%20Income%20Bracket.png)

![Predicted chnage versus actual]


### Key Findings <a name="subparagraph8"></a>

1. Is there any correlation between the stock price and it being in the news? 


2. Does any particular media outperform in this respect?


3. Are only certain stocks inflenced by media? 



## Recommendations <a name="paragraph3"></a>

- Should ACT-Right base their recommendations on this model?


## References <a name="paragraph4"></a>
(https://www.reddit.com/dev/api/)

(https://newsapi.org/docs)

(https://alpaca.markets/docs/api-documentation/)

(https://developer.twitter.com/en/docs/twitter-api/premium/search-api/quick-start/premium-30-day)

