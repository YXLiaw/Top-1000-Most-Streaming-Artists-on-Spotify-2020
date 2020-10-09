# Top 1000 Most Streamed Artists on Spotify (EDA focus)

**Background**
---
As a new recent user to Spotify and a music lover in general, I am keen to search for new songs that I may find it interesting to listen to based on my own personal preference (i.e songs with high energy and very suitable to dance to). For this project, I will be mainly focusing on the dataset for top 1000 most streamed artists on Spotify from the ChartMasters website and using Spotify's web API for data scraping.

By doing so, this will be useful for my data analysis on some of the following key topics:
- Factors that makes an artist popular on Spotify
- Audio feature analysis for favourite artists/albums
- Overall year trend of audio features on Spotify
- Artist that has the most number of followers/streams on Spotify

**Instructions for Spotify Data Scraping**
---
For extracting data from Spotify, the following fundamental instructions are required to get started:
1. Go to Spotify Developer's website and create a new free account if not yet available: https://developer.spotify.com/dashboard/login
2. Once account is created, select "Create an app" option with a random app name.
3. After creating an app, record down the client ID and client secret, which will be required for authenticating Spotipy object on Jupyter Notebook. (Note that installation of Spotipy onto Python is required prior to data extraction)

**Code and Resources Used**
---
- **Python Version** : 3.7
- **Packages** : pandas, matplotlib, numpy, seaborn, ast, math, wordcloud
- **Dataset source** : ChartMasters - https://chartmasters.org/most-streamed-artists-ever-on-spotify/
- **Spotify Web API** : https://developer.spotify.com/documentation/web-api/reference/
- **Spotipy documentation** : https://spotipy.readthedocs.io/en/2.16.0/
- **Reference for Spotify Data Extraction Process** : https://medium.com/@RareLoot/extracting-spotify-data-on-your-favourite-artist-via-python-d58bc92a4330

**Data Cleaning**
---
After importing the data extracted from csv to data frames, I needed to clean up the data for further analysis by making the following main changes:
- Convert stream and track count values to integers by removing unwanted characters (comma sign on numbers)
- Create seperate data frame containing individual observations of genre for each artist
- Concatenating multiple data frames of information on album tracks into single data frame
- Compute follower to stream ratio for each top 1000 most streamed aritst
- Encoding data for several columns into categorical data

**EDA**
---

**Usage**
---
This project is best viewed in a notebook render viewer, which can be accessed [here](https://nbviewer.jupyter.org/github/YXLiaw/Top-1000-Most-Streamed-Artists-on-Spotify-2020/blob/main/Top%201000%20Most%20Streamed%20Artists%20on%20Spotify.ipynb?flush_cache=true). In this notebook, you will find a walkthrough of the work and the respective code with comments on observations from figures/charts.

**Legality**
---
This is a personal project made for non-commercial uses ONLY. This project will not be used to generate any promotional or monetary value for me, the creator, or the user.

If you are a Spotify representative and there are any legal issues with this project, please contact me! *
This project uses the Spotify Web API, and terms and conditions are found here: https://developer.spotify.com/terms/

"Allowable non-commercial use of the Spotify Content. Notwithstanding the foregoing, you may use the Spotify Content to perform certain analysis for non-commercial uses only, such as creating rich visualizations or exploring trends and correlations over time. For example, this is an acceptable non-commercial analytical use of the Spotify Content. “Non-commercial use” means any use of the Spotify Content which does not generate promotional or monetary value for the creator or the user, or such use does not gain economic value from the use of our content for the creator or user, i.e. you. If you are interested in commercial use of Spotify Content, a written permission is required from Spotify."
