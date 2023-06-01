# WeRateDogs Twitter Data Cleaning Project
The focus of this project was to use Python Pandas and other libraries to perform data wrangling. Data was gathered from a variety of sources and in a variety of formats, its quality and tidiness were assessed, then the data was cleaned. Interesting and trustworthy analyses and visualizations were then created to provide insights about the data.


## Project Overview
*Provided by Udacity*  

The dataset that was wrangled (and analyzed and visualized) was the tweet archive of Twitter user [@dog_rates](https://twitter.com/dog_rates), also known as [WeRateDogs](https://en.wikipedia.org/wiki/WeRateDogs). WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. WeRateDogs has over 4 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive and sent it to Udacity for use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017.

### Packages (Libraries) Used
- pandas
- NumPy
- requests
- tweepy
- json


## Project Data
*Provided by Udacity*  

### Enhanced Twitter Archive

The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which was used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, only tweets with ratings were filtered (there are 2356).  Data needs to be assessed and cleaned these to use them for analysis and visualization.

To help interpret the dog stage, The Dogtionary was provided via the WeRateDogs book on Amazon:
![image](https://github.com/noeliaguz/WeRateDogs-Twitter-Data-Cleaning-Project/assets/53549117/fc64f499-3703-4b7a-be3c-9f862faab192)

### Additional Data via the Twitter API

Regarding the Twitter archives: retweet count and favorite count are two of the notable column omissions. Quering Twitter's API will be necessary to gather this valuable data.

### Image Predictions File

Every image in the WeRateDogs Twitter archive was run through a neural network that can classify breeds of dogs. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).

So for the last row in that table:

- **tweet_id** is the last part of the tweet URL after "status/" → https://twitter.com/dog_rates/status/889531135344209921
- **p1** is the algorithm's #1 prediction for the image in the tweet → golden retriever
- **p1_conf** is how confident the algorithm is in its #1 prediction → 95%
- **p1_dog** is whether or not the #1 prediction is a breed of dog → TRUE
- **p2** is the algorithm's second most likely prediction → Labrador retriever
- **p2_conf** is how confident the algorithm is in its #2 prediction → 1%
- **p2_dog** is whether or not the #2 prediction is a breed of dog → TRUE
- etc.



