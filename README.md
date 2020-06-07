# Introduction

In this project we anayse WeRateDogs twitter account. The dataset that is wrangled is the tweet archive of Twitter user [dog_rates](https://twitter.com/dog_rates), also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10.

## Project Motivation

The motivation for this project came from the account uniques rating system for the dogs. For each picture, the dogs are rated like 11/10, 13/10 15/10 and like so. This really intrigued me and I wanted to go a little deeper to find out what makes this account so special. I also looked into the pattern of tweets, most popular dog breeds that they come across and more.

## Dataset details

- Twitter archive file, _twitter_archive_enhanced.csv_: This was provided by Udacity and downloaded manually.

- The tweet image predictions, _image_predictions.tsv_: what breed is present in each tweet according to a neural network. This file is hosted on Udacity's servers and was downloaded programmatically using the Requests library and URL information (This neural net is actually created in one of its extracuriicular courses in Data Scientist Nanodegee)

- Twitter API & JSON, _tweet_json.txt_: by using the tweet IDs in the WeRateDogs Twitter archive, we use the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file. This file is read line by line into a pandas data frame with tweet ID, favorite count, retweet count, followers count, friends count, source, retweeted status and URL.

These files can be found in in `data/raw/`. Usually the data files are not uploaded using regular methods due to their size, [data version control](https://dvc.org) is a good way to version control your datasets.

## File and folder descriptions

There is a single notebook present in the `src` folder, namely `data_analysis.ipynb`. This notebook goes over data gathering, wrangling, cleaning and analysis process one by one. Each section is well documented and the process is explained as required.

The data is present in the data folder segregated as `raw` and `processed` to hold, well raw and processed data respectively.

`environment.yml` file is used to create a virtual environment for the project without distrubing any exsisting environment and packages.

## Questions answered

There are three main questions that are answered, each with their own specific set of traits. We take a look at the following questions:

- Based on the predictions, most liked dog breed: Which breed gets retweeted and favorited the most overall?

- How did the account develop (speaking about the number of tweets, retweets, favorites, image number and length of the tweets)?

- Is there a pattern visible in the timing of the tweets?

## Setup

For working or testing this project on your system, you need to have python 3.6+ and anaconda/miniconda (preferrable). After you are done with the installations, follow the steps below.

1. Clone the repo with `git clone git@github.com:agpt8/WeRateDogs-Analysis.git`

2. Navigate into the project directory `cd WeRateDogs-Analysis`

3. To create the conda environment with one command, use `conda env create -f environment.yml`

4. After the environment is created, activate the enrionment `conda activate WeRateDogs-Anaylsis`

5. Run the notebook using `jupyter notebook` or `jupyter lab`.

6. Now you can run all the cells at once or one by one.

## Results

The main findings of the code can be found at the post available [here](https://medium.com/@ayush.gpt8/weratedogs-analysis-5a92a873dfbc)

## Sources and Licences

The sources referred are available at the end of the notebook. There is no licence associated with the code. Feel free to use it as you like.
