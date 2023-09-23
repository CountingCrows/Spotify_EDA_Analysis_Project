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

For the top 5 instrumentalness tracks, we then select columns "intrumentalness", "song_title", and "artist" then sorting the values by "instrumentalness". We visualize this using a pie chart. 

![image](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/10f9b01c-23b3-4684-855c-cc3e916ef55e)

Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0. The most instrumentalness song is Senseless Order.

Next, we want to take various audio features of songs from a dataframe and visualizes their distribution using histograms. For each feature, it splits the data into "positive" and "negative" based on a "target" column and then plots the distribution of values for positive and negative data. This provides insights into how each audio characteristic differs between the positive and negative labeled songs. 

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/4c3a9a0f-42bc-483d-9e9d-fd4283a6a46d)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/aaa674be-d832-45dd-8786-ce5a54fd38a9)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/3d11f201-f38d-426c-88a2-f7c939e6b6a7)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/bb77ea1c-df9c-4bdd-b624-986f7c9624b3)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/d736bd28-e750-452e-b0a8-2aa2ffd2f20f)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/ea79f37e-1740-4c9a-89cc-6706525db421)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/8c9b4397-47ee-4a04-89cd-597f774303df)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/c9957d66-97ee-4939-a3af-9b8ccda93c4e)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/e35bfe08-ca12-41d9-9b93-bce3a8d8a7e5)

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/a5c60389-e211-45ec-aee4-c0e8d8898bb8)

We then try to analyze the top 10 energetic tracks. We simply select columns "energy", "song_title", "artist" and sorting the values by the "energy".

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/00072548-2435-4479-a9ad-780a5875b776)

Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.

For the most common durations, we subset dataframe for songs with the most common duration and loop over each mode and subset dataframe. 

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/8e01898b-6ff8-4c2d-a3d1-0a272bce5bf5)

This code aims to identify the most common song durations (in milliseconds) in a dataset and then subset the dataset to retrieve song titles and artists for songs with these durations. If multiple duration values are equally common, the code will retrieve songs for all of these durations.

For our last analysis, we try to find the top 10 tracks with the most valence. Simply by selecting columns "valence", "song_title", "artist" and sorting the values by the "valence".

![download](https://github.com/CountingCrows/Spotify_EDA_Analysis_Project/assets/85608120/f9cb104b-addd-4f54-b11f-06e4695b9d44)

A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).

