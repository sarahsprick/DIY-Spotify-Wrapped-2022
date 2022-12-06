# DIY-Spotify-Wrapped-2022

As a long-time Spotify Premium subscriber and an avid listener of the "Made For You" playlists (created by Spotify to "help you discover more of what you love"), I have always been curious about the metrics used to determine what I may like. I have also been curious about whether my Spotify Wrapped provided at the end of each year is accurate.

To dig into this idea, I used data both provided by Spotify and downloaded by Spotify’s API about my account to see what songs/artists dominate my streaming history, when I listen the most, whether there are any common audio features, and more!
 
![spotify-icon-256x256-jypoz69p](https://user-images.githubusercontent.com/95668919/205817996-cea1f116-7751-4fe6-952d-5b366a9392ca.png)

## The Data

### Streaming History

This first section is using my account data found [here](https://www.spotify.com/us/account/privacy/). The turnaround time for this request took around ~5 days. I received a `.zip` folder with different files about my playlists, search queries, payment, followers/following accounts, stream history, etc. from the last 12 months. For this project, I am going to be focusing on the latter (stream history).

### Spotify's Web API

In this next section, I will use data from Spotify's API.

Prior to the code below, I created a developer account [here](https://developer.spotify.com/dashboard/). You do not need a Spotify Premium subscription, but will need a Spotify account to access this tool. The process to retrieve the data is a little complicated. [Steven Morse's post titled "Exploring the Spotify API in Python"](https://stmorse.github.io/journal/spotify-api.html) and [John Mannelly's blog post titled "How to Build Your Own Spotify Wrapped with Python, Spotipy and Glide Apps"](https://jman4190.medium.com/build-your-own-spotify-wrapped-with-python-spotify-and-glide-apps-493dc7da20b) were excellent resources I used to help me get the information needed. 

Part of the reason I chose this route was because the streaming data provided by Spotify (used in the section prior to this) only contained simple information like the artist's name, track name, and date. I was interested in getting more detail about the music I listen to. 

Packages used:
- pandas
- numpy
- plotly
- spotipy
- requests
- matplotlib
- seaborn

## Visualization

Check out my [DIY Spotify Wrapped 2022](https://public.tableau.com/views/WIPSpotifyWrapped/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link) dashboard on Tableau Public!

![image](https://user-images.githubusercontent.com/95668919/205965945-46716b55-d216-4249-b7f5-dfe4a1661dd3.png)

Note: Used plotly for some visuals. These do not render in GitHub so I inserted screenshots to the notebook. For interactive visuals, download the notebook.
