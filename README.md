# Introduction

In this project we anayse WeRateDogs twitter account. The dataset that is wrangled is the tweet archive of Twitter user [dog_rates](https://twitter.com/dog_rates), also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10.

## Dataset details

- Twitter archive file, _twitter_archive_enhanced.csv_: This was provided by Udacity and downloaded manually.

- The tweet image predictions, _image_predictions.tsv_: what breed is present in each tweet according to a neural network. This file is hosted on Udacity's servers and was downloaded programmatically using the Requests library and URL information (This neural net is actually created in one of its extracuriicular courses in Data Scientist Nanodegee)

- Twitter API & JSON, _tweet_json.txt_: by using the tweet IDs in the WeRateDogs Twitter archive, we use the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called file. This file is read line by line into a pandas data frame with tweet ID, favorite count, retweet count, followers count, friends count, source, retweeted status and URL.

These files can be found in in `data/raw/`. Usually the data files are not uploaded using regular methods due to their sheer size, [data version control](https://dvc.org) is a good way to version control your datasets.

## Setup

For working or testing this project on your system, you need to have python 3.6+ and anaconda/miniconda (preferrable). After you are done with the installations, follow the steps below.

1. Clone the repo with `git clone`

2. Navigate into the project directory `cd WeRateDogs-Analysis`

3. If you have conda installed, then issue the command `conda env create -f environment.yml`

4. Run the notebook using `jupyter notebook` or `jupyter lab`.
