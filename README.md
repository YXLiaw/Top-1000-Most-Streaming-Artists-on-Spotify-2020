# Top 1000 Most Streamed Artists on Spotify (EDA focus)

**Background**
---
Given the upcoming U.S general election has become a recent hot topic amongst my friends and relatives living in U.S, I am keen to understand the public's opinion on their preference of candidate for the next general election. 

FiveThirthyEight's model simulations seem to be credible and useful for helping on my data analysis for the following key topics:
- Likelihood of all possible outcomes for 2020 U.S general election
- Which states have voters that provide high influence on determining the upcoming election outcome?
- Which states of voters are more favourable towards Donald Trump vs Joe Biden for the past few months?
- Does the current U.S economy performance reduce the chances of Donald Trump winning the next general election?

**Code and Resources Used**
---
- **Python Version** : 3.7
- **Packages** : pandas, matplotlib, numpy, seaborn, ast, math, wordcloud
- **Dataset source** : ChartMasters - https://chartmasters.org/most-streamed-artists-ever-on-spotify/
- **Spotify Web API** : https://developer.spotify.com/documentation/web-api/reference/
- **Spotipy documentation** : https://spotipy.readthedocs.io/en/2.16.0/

**Data Cleaning**
---
After importing the data from csv to data frames, I needed to clean up the data a bit for further analysis by making the following changes:
- Remove redundant and irrelavant columns (i.e variables related to third party candidates are removed, since the data is empty for those columns)
- Remove unwanted non-ASCII characters from string data for "scenario_description" column
- Encoding data for several columns into categorical data.

**EDA**
---
### Probability distribution of Electoral College Vote Outcomes
![Prob  distribution](https://user-images.githubusercontent.com/34255556/93668271-ea023e80-fabd-11ea-8c4d-2a3ac4879f6e.png)<br/>
Joe Biden seems to have higher chance to win majority of electoral college votes, compared to Donald Trump (413 vs 125)

### Likelihood of Possible Election Outcomes
![Likelihood of outcomes](https://user-images.githubusercontent.com/34255556/93668240-cdfe9d00-fabd-11ea-9974-524796456846.png)<br/>
Joe Biden is very highly likely to win both popularity and electoral college majority by more than 80% of probability, while Donald Trump is predicted to have less than 20% chance of winning both popularity and electoral college majority.

### States that may deliver decisive vote in Electoral College votes
![Tipping](https://user-images.githubusercontent.com/34255556/93668083-ef12be00-fabc-11ea-9a7d-2d0fb67676e7.PNG)<br/>
Pennsylvania has the highest probability of being the state that determines the outcome of electoral college votes (~32%), which is significantly greater than Florida having the 2nd highest probability at around 14%.

### Voting Power Index for different states in U.S
![Voting Power Index](https://user-images.githubusercontent.com/34255556/93668084-f0dc8180-fabc-11ea-91ce-be468cd88071.PNG)<br/>
Voters in Pennsylvania also has the highest voting power index (7.2), followed by Wisconsin (4.8), Nevada (4.5) and New Hampshire (4.5).

### Improvement in popularity margins
![Margin difference](https://user-images.githubusercontent.com/34255556/93668168-80823000-fabd-11ea-96fb-66a4ebad5268.PNG)<br/>
Joe Biden gains popularity amongst people in Arizona and Minnesota by more than 10% of improvement, compared to Donald Trump who only manages to gain popularity amongst people living in Indiana, Georgia and Missouri between 3 to 6% of improvement. 

**Usage**
---
This project is best viewed in a notebook render viewer, which can be accessed [here](https://nbviewer.jupyter.org/github/YXLiaw/Top-1000-Most-Streamed-Artists-on-Spotify-2020/blob/main/Top%201000%20Most%20Streamed%20Artists%20on%20Spotify.ipynb?flush_cache=true). In this notebook, you will find a walkthrough of the work and the respective code with comments on observations from figures.

**Legality**
---
This is a personal project made for non-commercial uses ONLY. This project will not be used to generate any promotional or monetary value for me, the creator, or the user.

If you are a Spotify representative and there are any legal issues with this project, please contact me! *
This project uses the Spotify Web API, and terms and conditions are found here: https://developer.spotify.com/terms/

"Allowable non-commercial use of the Spotify Content. Notwithstanding the foregoing, you may use the Spotify Content to perform certain analysis for non-commercial uses only, such as creating rich visualizations or exploring trends and correlations over time. For example, this is an acceptable non-commercial analytical use of the Spotify Content. “Non-commercial use” means any use of the Spotify Content which does not generate promotional or monetary value for the creator or the user, or such use does not gain economic value from the use of our content for the creator or user, i.e. you. If you are interested in commercial use of Spotify Content, a written permission is required from Spotify."
