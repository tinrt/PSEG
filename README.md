# PSEG Research Project

## Phase 1
This research aims to understand the challenges faced by underprivileged communities in New
Jersey by analyzing social media and news article content from general online sources using
Bing search results. Our Dataset contains news articles for more than 350 areas in New Jersey in
the past year. This research has used text mining techniques and large language models to
process the data and perform topic modeling to identify the challenges communities face in New
Jersey. Sentiment analysis has also been used to detect negative-toned articles and investigate
them more. The result of the Analysis has been summarized in 3 main indicators, including
Weighted Social Negative Index (WSNI), Crime Index, and Social Negative Articles Ratio for
each area. The final results were presented using two interactive maps and a dashboard
summarizing the findings.

## Process: 
The project starts by initiating an automated data-gathering process using Python that
searches for more than 350 areas in New Jersey on Bing.com and then crawls a number
of articles related to each of these areas. The text content of each article will be saved in a
Jason file, and all the articles related to an area are gathered in a folder. Each article has been broken down into sentences and each sentence has been passed through 2 different labeling processes. First, the sentence has been passed to the Fine-
BERT model to be labeled as Environmental, Social, Governance, or None. Next, sentiment analysis will be applied to decide whether the sentence has a positive, negative, or neutral tone. The labels will be saved next to each sentence in the Jason files.

1. [**11_Get_latlong_link**](11_Get_latlong_link.ipynb): Jupiter Notebook will create a dataset containing the Latitude and Longitude of New Jersey Areas and the Bing search link.
   1. [NJ.csv](NJ.csv) is the input for this Notebook

2.  [**22_Bingsearch.ipynb**](22_Bingsearch.ipynb): ـupiter Notebook to search for URLs and create dataframes for each
   1. [NJ_with_lat_long.csv](NJ_with_lat_long.csv) is the input for this Notebook

3. [**PipeLine.ipynb**](PipeLine.ipynb) : This is the main Data Gathering Notebook that creates a json file for each article and save them in separate folders for each area in New Jersey.
   1. [NJ_with_lat_long.csv](NJ_with_lat_long.csv) is the input for this Notebook
   2. Steps in this code:
      1. Getting Bing search results from the search page link
      2. Getting HTML for each search result from the link
      3. Getting article text from each HTML
      4. Passing each sentence to Fine Bert and getting label
4.[**Sentiment.ipynb**](Sentiment.ipynb): This script determines each sentence's sentiment and adds it to its dictionary. This Notebook also calculates the percentage of each label and export label_percentages.csv
5. [**NJ Map.ipynb**](NJ_Map.ipynb) : This Notebook reads [label_percentages.csv](label_percentages.csv) and creates map.html

6. [Area.zip](Areas.zip) contains JSON files for each area.
  


