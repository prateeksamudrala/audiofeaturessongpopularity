# audiofeaturessongpopularity
This project is to understand the relation between audio features and song popularity using a Spotify Dataset

Dataset: https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks

As a musician, I find it interesting to explore this Spotify dataset to better understand the factors that make a song more appealing. Many home-studio-producers - like myself - don’t have the budgets, influence, or marketing strategies to “create” a popular song. However, the essence of the song - the audio features and associated emotions - are certainly controllable by all. With that said, I want to:

1. Understand how audio features influence a song’s popularity.
2. Create a model that can perhaps be provided through streaming platforms to help independent musicians and producers create influential music. Example: When I release a song on Spotify, using this model, maybe Spotify can guide me to make a more appealing song; for instance, Spotify could indicate that my song needs less “valence”.

This is a personal project, and will evolve. The rmd file has been dated accordingly; the file also has details on the analysis. The end goal is to understand the influence of audio features on song appeal, to help independent musicians and producers fine tune their creations for a broader appeal.

Please feel free to reach out to collaborate, to build on this project. 

Dataset Dictionary per Spotify: 

1.	acousticness : The relative metric of the track being acoustic
2.	danceability: The relative measurement of the track being danceable
3.	duration_ms: The length of the track in milliseconds (ms)
4.	energy: The energy of the track
5.	instrumentalness: The relative ratio of the track being instrumental
6.	liveness: The relative duration of the track sounding as a live performance
7.	loudness: Relative loudness of the track in the typical range [-60, 0] in decibel (dB)
8.	speechiness: The relative length of the track containing any kind of human voice
9.	tempo: The tempo of the track in Beat Per Minute (BPM)
10.	valence: The positiveness of the track
11.	key: The primary key of the track encoded as integers in between 0 and 11
12.	mode: The progression of track whether it is major (1) or minor (0)
13.	popularity: The popularity of the song lately, default country = US

Insights:

1. Audio features account for 37% variablilty in a song's popularity

2. All audio features except for tempo have a strong relationship to a song's popularity

3. The relationship is as follows: 

If acousticness increases by one standard deviation (0.30), then popularity increases by 0.07 standard deviations. The standard deviation for popularity is 32.08, so popularity increases by 2.38 units (32.08 × 0.07) for every 0.30 units increase in acousticness.

If danceablity increases by one standard deviation (0.16), then popularity increases by 0.20 standard deviations. The standard deviation for popularity is 32.08, so popularity increases by 6.6 units (32.08 × 0.20) for every 0.16 units increase in danceability

If duration increases by one standard deviation (144886.1), then popularity decreases by 0.083 standard deviations. The standard deviation for popularity is 32.08, so popularity decreases by 2.66 units (32.08 × 0.083) for every 144886.1 milli second increase in duration

If energy increases by one standard deviation (0.227), then popularity decreases by 0.366 standard deviations. The standard deviation for popularity is 32.08, so popularity decreases by 11.74 units (32.08 × 0.366) for every 0.227 units increase in energy

If instrumentalness increases by one standard deviation (0.361), then popularity decreases by 0.264 standard deviations. The standard deviation for popularity is 32.08, so popularity decreases by 8.46 units (32.08 × 0.264) for every 0.361 units increase in instrumentalness

If liveness increases by one standard deviation (0.201), then popularity decreases by 0.105 standard deviations. The standard deviation for popularity is 32.08, so popularity decreases by 3.36 units (32.08 × 0.105) for every 0.201 units increase in liveness

If loudness increases by one standard deviation (4.109), then popularity increases by 0.36 standard deviations. The standard deviation for popularity is 32.08, so popularity increases by 11.54 units (32.08 × 0.36) for every 4.109 units increase in loudness

If speechiness increases by one standard deviation (0.1551), then popularity decreases by 0.057 standard deviations. The standard deviation for popularity is 32.08, so popularity decreases by 1.82 units (32.08 × 0.057) for every 0.1551 units increase in speechiness

If valence increases by one standard deviation (0.244), then popularity decreases by 0.07 standard deviations. The standard deviation for popularity is 32.08, so popularity decreases by 2.24 units (32.08 × 0.07) for every 0.244 units increase in valence

4.	Except for tempo, we can confidently rely on our multilinear regression model to predict a song’s popularity based on audio features.

5.	The linear model is not unduly influenced by outliers, does not break the assumption of independence or no multicollinearity.

6.	Considering model accuracy, I would only use logistic regression (83% accuracy) for predictions. KNN model is 36% accurate. K means clustering is not indicative of much. 
