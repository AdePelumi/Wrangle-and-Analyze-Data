# (Wrangle and Analyze Data )
## by (Adetimilehin  Pelumi)

## Introduction
Real-world data rarely comes clean. Using Python and its libraries, I will gather data from three of sources and in a variety of formats, assess its quality and tidiness, then clean it. This is called data wrangling. I will be documenting my wrangling efforts in this Jupyter Notebook, plus showcase them through analyses and visualizations using Python (and its libraries)


## Dataset
I gathered three different data from three different data sources:

1. WeRateDogs Twitter archive downloaded Manually from Udacity.
To get the file "(twitter_archive_enhanced.csv)” into my notebook 
after downloading from Udacity, I read it using pandas "read_csv" function 
and stored it as "t_archive". Choose “t_archive” so it would be easier to 
work with using a short name.
2. tweet image predictions file downloaded programmatically using requests 
library from Udacity's provided URL.
I was provided a URL which stored the file "(image_predictions.tsv)". 
And to get that, I used the Requests library "get" function to retrieve the file 
from the URL provided. The content of the file was read into a python data 
from using pandas and stored as pred. Using a short name again.
3. Additional data retrieved by querying Twitter's API using Tweepy libary.
Here comes the tricky part. After getting the required credentials from Twitter to 
use the Twitter API. I queried each tweet Id stored in t_archive for "favorite count" 
and "retweets" using a for loop and storing the result if the tweet Id was found in"tweets_id_data" while those that were not found were stored in 
"notweets_id_data". Saved the final result after in a file called "tweets_json.txt" and stored it as “tweet_data” in my notebook.

* The process took 3047 seconds to complete
* 2296 tweet id found
* 60 tweet id not found

## Assesment Summary

#### Quality Issues (Issues with file content)

1. t_archive data - Timestamp column is in object format


2. t_archive data - Lots of dog rating numerator greater than 15


3. t_archive data - Lots of dog rating denuminator greater than  10


4. t_archive data - The source column needs cleaning


5. t_archive data - Colunms with empty values have None as a value which is not showing as Null or NaN(null object not null)


6. pred data - The names in the dog breed predictions are not uniform some in lower case while others in mixed case


7. t_archive data - Some dogs have invalid names


8. pred data - Three dog breed prediction available



9. all_merged- Retweets and reply present


10. all_merged-  Unnecessary columns


11. all_merged - Tweets without image


12. all_merged - Wrong assigned datatype

#### Tidiness Issues (issues with file structure)
1. t_archive - Dog stage is scattered in 4 colunms


2. General - The three dataset have tweet id in common 

## Questions for Analysis 
1. How is the dog stage distributed in the data
2. What are the top  10 dog breeds
3. Source of tweet distribution 
4. Visualize the high correlation between favorites and retweets counts
5. Dog rating distribution 

## Summary of Findings

### Insights:
1. "Pupper" was the most common dog stage having a whooping 66.6% of the dog stage.

2. The most popular dog breed goes to "Golden retriever"

3. Iphones dominated in the source of tweets

4. The more the favourite count the more  retweet the post gets

5. 12/10 is the most common rating given to dogs rated by WeRateDogs.
