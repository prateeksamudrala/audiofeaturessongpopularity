# audiofeaturessongpopularity
This project is to understand the relation between audio features and song popularity using a Spotify Dataset

Dataset: https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks

As a musician, I find it interesting to explore this Spotify dataset to better understand the factors that make a song more appealing. Many home-studio-producers - like myself - don’t have the budgets, influence, or marketing strategies to “create” a popular song. However, the essence of the song - the audio features and associated emotions - are certainly controllable by all. With that said, I want to:

1. Understand how audio features influence a song’s popularity.
2. Create a model that can perhaps be provided through streaming platforms to help independent musicians and producers create influential music. Example: When I release a song on Spotify, using this model, maybe Spotify can guide me to make a more appealing song; for instance, Spotify could indicate that my song needs less “valence”.

This is a personal project. The end goal is to understand the influence of audio features on song appeal, to help independent musicians and producers fine tune their creations for a broader appeal.

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

