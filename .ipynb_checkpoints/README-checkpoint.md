# Table of Contents
1. [Introduction- Project In the News](#Introduction)
2. [Data, Technology and Coding Standards](#Paragraph1)
   1. [Data Sources](#SubParagraph1)
   2. [Technology Stack](#Subparagraph2) 
   3. [Coding and Release Standards](#Subparagraph3)
3. [Data Cleanse and Visualisation](#Paragraph2)
   1. [Data Cleanse](#SubParagraph4)
   2. [Model- Summary](#SubParagraph5)
   3. [Model- Prediction](#Subparagraph6) 
   4. [Model- Evaluation with Visualisations](#Subparagraph7)
   5. [Key Findings](#Subparagraph8)   
4. [Recommendations](#Paragraph3)
5. [References](#Paragraph4)

<div style="page-break-after: always;"></div>

## Introduction- Project In the News <a name="Introduction"></a>

ACT-Right is an investment advisory firm that has requested an evaluation of media impact on the price of stocks. Project In the News seeks to answer the following questions using established Natural Language Processing Models:
- Is there any correlation between the stock price and it being in the news? 
- Does any particular media outperform in this respect?
- Are only certain stocks influenced by media?
- Should ACT-Right base their recommendations on this model?

## Data, Technology and Coding Standards <a name="paragraph1"></a>
### Data Sources <a name="subparagraph1"></a>
Multiple media channels covering Social media as well as tranditional News channels were reviewed- the folowing have been used in this project:

- Reddit
- Twitter
- News API 

Data Source:
[Reddit](https://www.kaggle.com/c/winwinewine/data)
[Twitter](https://www.kaggle.com/c/winwinewine/data)
[NewsAPI](https://www.kaggle.com/c/winwinewine/data)
[Alpaca](https://www.kaggle.com/c/winwinewine/data)

Additionally, the American 10-k reports (company financial statements) has been sourced using API [American Census Data](https://api.census.gov/data/2019)

### Technology Stack <a name="subparagraph2"></a>

The following additional technologies have been deployed:
- Vader Sentiment Analysis
- SpaCy
- Twitter API Key
- Reddit API Key
- NewsAPI Key


The Jupyter Notebook has been deployed to AWS and the relevant Sagemaker Jupyter Notebook has been made available in the repository.

### Coding and Release Standards <a name="subparagraph3"></a>

Following rules have been applied during code development and testing:
1. Each input data will have its own Jupyter Notebook with the source identified in the notebook name.
2. Two separate sub folders- one for Data and another for Images- will be created in the main folder.
3. The pre-processed cleansed data will be stored in a csv file format in the Data sub folder with the source identified in the filename.
4. All variables must be in lower case and reflect their purpose. Underscore to be used as and when required. 
5. Each step of the code must contain comments to explain the purpose of the code.
6. A git hub repository called Project2 must be set up with branches for each developer.
7. Each release must provide a brief message on changes made prior to committing the code.

## Data Cleanse and Visualisation <a name="paragraph2"></a>
### Data Cleanse <a name="subparagraph4"></a>

The following data cleanse rules have been applied to the source data set:

1. Identified data set must be formatted correctly prior to use- Date format yyyy/mm/dd, amount must be integer.
2. Redundant data, if any, must be dropped- drop columns Z_CostContact', 'Z_Revenue', 'Response', 'MntGoldProds'.
3. Duplicates, if any must be dropped.
4. Sentence segmentation and tokenisation of all data sets
5. Remove Stopwords
6. Lemmatization of words
7. Ensure all dataframe columns have appropriate and correct headers.
8. Group records into appropriate sub categories- 
9. Ensure records are sorted on the required fields.
10. Validate that entire data set has been correctly loaded.




### Model- Summary <a name="subparagraph5"></a>

Post data pre processing, the data has been split into train and test data in the ratio of 80:20? The Vader Sentiment Model then has been applied to to predict the sentiment polarity.



### Model- Prediction <a name="subparagraph6"></a>
Below is the visual representation of the analysis:
![Total Wine Sales per Income Bracket](https://github.com/chirathlv/Project1/blob/Renu/Images/Total%20Wine%20Sales%20per%20Income%20Bracket.png)


### Model- Evaluation with Visualisations <a name="subparagraph7"></a>



### Key Findings <a name="subparagraph8"></a>

1. Is there any correlation between the stock price and it being in the news? 


2. Does any particular media outperform in this respect?


3. Are only certain stocks inflenced by media? 



## Recommendations <a name="paragraph3"></a>

- Should ACT-Right base their recommendations on this model?


## References <a name="paragraph4"></a>

1. [(https://www.kaggle.com/)]
