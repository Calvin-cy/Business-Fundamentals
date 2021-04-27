# Business Project MVP

This graph shows us how much profits the songs make and is distributed by the keys and mode

- (The estimated overall key of the track. Integers map to pitches using standard Pitch Class notation . E.g. 0 = C, 1 = C♯/D♭, 2 = D,)
- C = 0, C-sharp = 1, D = 2, D-sharp = 3, E = 4, F = 5, F-sharp = 6, G = 7, G-sharp = 8, A = 9, B-flat = 10 (T), and B = 1 1 (E).

- (Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is, 0:minor,1:major)


![Profits from different keys and modes](https://user-images.githubusercontent.com/63031028/116299878-1288a000-a753-11eb-858b-3a368b01414f.png)

As we can see that songs with C# major make the most profits. However, it may due to most songwriters prefer to write songs in C# major.

Therefore, here is the Average song profit for each key.

![chart](https://user-images.githubusercontent.com/63031028/116302689-57fa9c80-a756-11eb-96cb-0e89e5a83723.png)

This time C# minor has the highest average of profit.

In conclusion, when we are selecting songs from all the recordings, we need to pay close attention to the songs with C# minor, E minor, and G# minor because they are the three most profitable averages based on our graph. So our MVP is to visualize how each feature of a song relates to the profits.

Furthermore, a song has different features like energy, valence, tempo, and so on. So our MVP is to visualize how each feature of a song relates to the profits, and I will build a Regression model that takes all of these features to predict the potential profit that a song can make. 