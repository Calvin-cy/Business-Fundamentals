# Business Fundamentals Proposal
## Question/need:
- Working in a Music Production company, the company wants to to filter out all the recordings that are sent to the company and select the songs that have the potential to be popular 
- Songwriters, and the Music Production company will find this model useful
- The rest of the world can get great music

## Data Description 
  - Using two data packages from Kaggle: 
  -  First one contains (1999-2019): 
      - Billboard Hot 100
      - Spotify (and their API)
      - Genius
      - Recording Academy Grammy Awards
      - Recording Industry Association of America (RIAA)
  - Second one :
    - Trending YouTube Video statistic (USA only)

- Each song from the Billboard Hot 100 has its own unique features number and I can evaluate if the popular songs follow a similar pattern
- Will use the second dataset to find the Click rate of the billboard 100 songs 

## Tools:
- Python (Jupyter Nobebook)
- Pandas and Numpy : Examine the data and Clean the data
- Sklearn to create a regression model 
- Matplotlib and seaborn to visualize the data

## MVP 
- Create a model that can explain how does each feature contributes to the song in order to become popular 