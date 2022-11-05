# WeRateDogs Twitter Analysis

## Dataset

WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the 
dog. These ratings mostly have a denominator of 10, with the numerator mostly greater than 10 
i.e 11/10, 12/10,13/10 etc, simply because, according to them, the dogs are good. 

The data used for this analysis was gathered from three sources: 

- Enhanced Twitter Archive : a stored csv file which contains WeRateDogs basic tweet data for 
 all 5000+ of their tweets, but not all.

- Additional data from the Twitter API: contains data extracted from the twitter API. It 
 includes some other columns like retweet_count, favorite_count which gives further 
 insights to the analysis. 

- Image Prediction: contains a table full of image predictions (the top three only) alongside 
 each tweet ID, image URL, and the image number that corresponded to the most 
 confident prediction.

The sole aim of the analysis is to wrangle WeRateDogs Twitter data to create interesting and 
trustworthy analyses and visualizations.


## Summary of findings

Due to the fact that the analysis is more of data wrangling, I ensured the various quality and tidiness 
issues were solved before delving into the analysis. 

### Quality
Twitter_archive table
- Presence of null values in some columns
- Inconsistency in the dog names
- Presence of urls in text column
- Timestamp column is in object datatype instead of datetime
- Presence of outliers in the rating numerator column
- Presence of outliers on the rating denominator column
Image_prediction table
- Presence of images that are not dogs
- Some attributes(columns) need to be renamed

### Tidiness
- Dog stages in the Twitter Archive tables are spread across the columns
- The predictions in the image predictions table are also spread across the column

After the necessary wrangling, a master csv file was created. This contains all the cleaned 
data used for visualization. Then, two key features were considered; the dog rating and the breed.
There was a postive relationship between the favourite count and the dog rating. 

Asides this, I considered the dogs that got the highest likes and highest retweets using bar charts. 
I then looked at the relationship between the confidence level (confident prediction) and the dog rating.
I discovered there was no relationship as people may not rate every dog image they see. Word cloud
was also used to check for most frequent words.


