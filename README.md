# Spotify_EDA_Analysis_Project
In this portfolio, we'll delve into the nuances of data preparation and analysis. Starting with the preprocessing key datasets, we'll focus on fine-tuning the Spotify dataset by finding the most popular artists to multiple feature plots. Our exploration involves identifying meaningful metrics, and ultimately visualizing our findings. This process aims to provide a clear understanding of our objectives, datasets, and the pertinent questions our analysis addresses.

## Dataset
We'll explore the Spotify 2017 dataset from [Kaggle](https://www.kaggle.com/datasets/geomack/spotifyclassification) , with the guidance of [Spotify Audio Feature](https://developer.spotify.com/documentation/web-api/reference/get-audio-features). We'll do an Exploratory Data Analysis to gain as many insights we can from the dataset.

## Tasks
- Top 5 most popular artists
- Top 5 loudest tracks
- Artist with the most danceability song
- Top 5 instrumentalness tracks
- Multiple feature plots:
  - tempo
  - loudness
  - accousticness
  - danceability
  - duration_ms
  - energy
  - instrumentalness
  - liveness
  - speechiness
  - valence
- Top 10 energetic tracks
- Most common durations
- Top 10 tracks with the most valence

## Data Cleaning
We find out that our dataset is clean. Therefore, we just need to check the types of the data and make sure we have the columns we need to do our analysis.

## Analysis
First, we want to know the Top 5 most popular artists of Spotify in 2017. We make a bar plot by grouping by the "artist" and sorting the values by it's "song_title".

![1](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/7af5d06b-3627-4652-8d0c-ffe851524ac8)

We can say that the most popular artist in 2017 based on the songs they had was Drake with a total of 16 top songs, followed by Rick Ross with 13 songs, and Disclosure.

Then we want to answer the second question, what are the Top 5 Most Loudest Tracks in Spotify? We simply select columns "loudness" and "song_title" and sorting the values by the "loudness".

![2](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/72198ad2-6c87-430f-ba0c-7d79676942ee)

The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db. So we can say that The loudest track in 2017 is GodLovesUgly, followed by The Lion- Original Mix, and The Wall.

To find Artists with the most danceability song, we select columns "danceability", "song_title", and "artist" then we sort the values by "danceability".

![image](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/2350c397-c6c0-426e-b197-1bce96113051)

Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable. From the plot above, Flashwind-Radio Edit is the most danceable song through 2017.


