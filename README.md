# PSEG Research Project


1. **11_Get_latlong_link**: Jupiter Notebook will create a dataset containing the Latitude and Longitude of New Jersey Areas and the Bing search link.
   1. NJ.csv is the input for this Notebook

2.  **22_Bingsearch.ipynb**: ـupiter Notebook to search for URLs and create dataframes for each
   1. NJ_with_lat_long.csv is the input for this Notebook

3. **PipeLine.ipynb** : This is the main Data Gathering Notebook that creates a json file for each article and save them in separate folders for each area in New Jersey.
   1. NJ_with_lat_long.csv is the input for this Notebook
   2. Steps in this code:
      1. Getting Bing search results from the search page link
      2. Getting HTML for each search result from the link
      3. Getting article text from each HTML
      4. Passing each sentence to Fine Bert and getting label
4.**Sentiment.ipynb**: This script determines each sentence's sentiment and adds it to its dictionary. This Notebook also calculates the percentage of each label and export label_percentages.csv
5. **NJ Map.ipynb** : This Notebook reads label_percentages.csv and creates map.html

6. Area.zip contains JSON files for each area.
  


