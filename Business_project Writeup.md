# Business Project - Proposing building a regression model for Warner Music Group
Calvin Yu
## Abstract
This goal of this project is to propose how the upcoming regression model can help Warner Music Group to not miss the songs that have the potential to be popular. The first step of this project is to identify the business problem. The business problem that Warner Music Group facing is there are too many demos sent from all over the world, and it is hard for them to listen to all the demos. Therefore, after acquiring the Spotify most popular songs in the year of 2019 and 2020 ,and performed an exploratory data analysis, I am proposing to create a regression model that will take all the measurable features from the song and give an estimate of how much profit does this particular song will be able to make. By convincing them to use this regression model, I will show them what trend does the popular songs share in common. 

## Design
### Back Story
Since Covid-19 has started, people have spent time at home. Warner Music group has been receiving triple amount of the demos that are sent from all over the world. However, Warner Music group does not have enough human force and time to evaluate all of them. Therefore, they are trying to find a data scientst that can help them to filter the demos that have the potential to be popular. 

- #### Problem: 
    - Warner Music group has received too many demos. How can they know which demo can become popular? 

- #### Impact Hypothesis :
    - By better understanding how each feature of the song contributes to its profit, Warner Music Group can identify what songs would have the most potential to make the most profits

- #### Preliminary Analysis:  
    - Exploratory analysis and visualization of the song attributes which include keys, mode, release date, valence, tempo, acousticness, duration, energy, instrumentalness,liveness,loudness, and speechiness

- #### Future Analysis: 
    - Build a predictive model that takes all the song attributes to generate an estimated profits. Warner Music Group can use this model to predict the profits of the upcoming demos to decide if they should invest on that



## Data
### Spotify global 2019 most-streamed tracks (US)
- top 1,717 tracks with audio features and artist info for the whole year
### Spotify-Data 1921-2020
- Audio features of songs from 1921-2020
### Top 200 most streamed songs on spotify 2020 (US)
- top 200 most streamed songs per week 

## Algorithms
1. Using Python to concatenate both Spotify 2019 and Spotify 2020 datasets , and merge it with the features dataset 
2. Perform basic data cleaning on the combined dataset and export it as a csv file. 
3. Opening the exported csv file in Google Spreadsheet 
4. Convert the duration_ms column into duration_in_time and also create a profits column based on the Stream column+
5. Create a summary table which takes all the features of the dataset and get their average, minimum, and maximum
6. Using Spreadsheet to visualize how the relationship between each categorical features and the profits
7. Create a pivot table top visualize the distribution of profits per different key and different mode to see which key and mode have the highest profits 
    - (The estimated overall key of the track. Integers map to pitches using standard Pitch Class notation . E.g. 0 = C, 1 = C♯/D♭, 2 = D,)
    - C = 0, C-sharp = 1, D = 2, D-sharp = 3, E = 4, F = 5, F-sharp = 6, G = 7, G-sharp = 8, A = 9, B-flat = 10, and B = 11.

    - (Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is, 0:minor,1:major)


![Profits from different keys and modes](https://user-images.githubusercontent.com/63031028/116299878-1288a000-a753-11eb-858b-3a368b01414f.png)

8. The graph tells me that songs with C# major are the most profitable, however it may due to many songwriters wrote their songs in C# major

9. Therefore, I use the countunique method from excel to get the number of songs that are written in each key and mode, and use that to divide the overall profits from each key and mode

![chart](https://user-images.githubusercontent.com/63031028/116302689-57fa9c80-a756-11eb-96cb-0e89e5a83723.png)

10. The new average chart indicates that many of the songwriters like to write their songs in C# major, so it is not necessarily that C# major song can be popular

11. The chart also tells me that songs with C# minor, E minor, and G# minor have the highest average song profit which we need to pay close attention to 

12. I repeated the same process from above to see what is a good time to release the song, and if this can affect to the profits to the song

![SUM of Profits vs  Month](https://user-images.githubusercontent.com/63031028/116659366-58598a00-a946-11eb-8211-6f42046194b9.png)

![Average song profits vs  Month](https://user-images.githubusercontent.com/63031028/116659427-70310e00-a946-11eb-9466-c462ce2f5faa.png)

13. Warner Music Group can avoid releasing the song on January because these two graphs show us that many music companies release their songs on January which can cause an intense competition 

![SUM of Profits vs  WeekDay ](https://user-images.githubusercontent.com/63031028/116660533-06b1ff00-a948-11eb-9b0f-ad81820f13fc.png)

![Average Profits per Day vs  WeekDay ](https://user-images.githubusercontent.com/63031028/116660576-16314800-a948-11eb-8086-1fe7f2c6d61b.png)

14. Warner Music group can also avoid releasing their song on a Friday because of intense competition and release their songs on a Thursday instead

15. After evaluating all the categorial features on the dataset, I start to use Tableau to explore on the numerical features 

16. For every numerical feature, I created a visualization. Here are the Dashboards 

![179083855_573962000251605_5287096279941981977_n](https://user-images.githubusercontent.com/63031028/116662997-5c3bdb00-a94b-11eb-9fd6-048457e5c597.png)

![180713076_173110934683065_2143705862816625409_n](https://user-images.githubusercontent.com/63031028/116663047-6cec5100-a94b-11eb-93f5-7ebceb073d24.png)

17. For all the charts, I created a filter that takes in purple and gold. Each purple circle is considered to be popular 

18. In the Valence vs Profit chart, the popular songs has the valence above 0.4 and most of them are over 0.5 valence which means most of the popular songs are considered to be happy

19. In the Energy vs Profit chart, only three popular songs fall under 0.5 energy, and the rest are over 0.5 energy. This can mean the energetic songs have the higher chance of being popular 

20. In the Tempo vs Profit chart, the popular songs lie on the tempo between 80 to 140. So the songs that are either too fast, or too slow, have a high chance of not being popular 

21. In the Accousticness vs Profit chart, most of the popular songs are less than 0.4 accousticness which indicates songs with lower accusticness may have a slightly chance to be more popular 

22. In the instrumentalness vs Profit chart, all the popular charts fall under 0.2, which means songs with low instrumentalness are surely having a chance to be popular 

23. The speechiness vs Profit chart shares the similar trend with the instrumentalness vs Profit chart. The popular songs fall under 0.5 speechiness which means song with 0.5 speechiness have a chance to be popular

24. The liveness vs profit chart indicates the popular songs have low liveness 

25. The loudness vs profit chart indicates the popular song to have a loudness close to zero 


## Tools
- Google Sheets - data visualization, data manipulation
- Python Numpy, Pandas - data cleaning, data aggregation
- Tableau - data visualization 

## Communication:
- Some features contain really obvious insight 
- Will need to create a regression model to see how well can the model explain after entering all the features 
- Cannot explain melody 
- Cannot explain Artist effect 
