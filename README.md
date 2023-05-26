# Exploratory Data Analysis of Video Game Dataset
I am very fond of Video Games. In this project I have solely used Python only for data cleaning, **EDA**- Exploratory Data Analysis as well as Data Visualizaion
to derive insights from the given dataset. I started with cleaning the data and soon got indulged in fascinating trends which came during my analysis
## 1. Data Collection
The data set which I used is available on Kaggle. It had 20,580 entries, with each entry representing a video game. The dataset includes 8 columns:
1. id: Unique identifier for each video game (data type: int64).
2. name: The title or name of the video game (data type: object).
3. released: The release date of the video game (data type: object).
4. added: The number of times the game has been added or favorited (data type: int64).
5. playtime: The average playtime in minutes (data type: int64).
6. reviews_count: The number of reviews for the video game (data type: int64).
7. ratings_count: The total number of ratings received by the game (data type: int64).
8. rating: The average rating score for the video game (data type: float64). 

Link to database repository is: https://www.kaggle.com/datasets/shivamvadalia27/video-games

## 2. Data Cleaning
I started with basic **Handling of NULL values**. Firstly, I checked if any null values were present. Then I determined how much percentage of my
dataset they were. Since they came out to be around 3.5% I felt of filling those values by 'bfill' in many of them values above and below them were same.
Then I **dropped duplicate** values. Now further I converted my released column data type to datetime from object by **parsing date**.
Then I extracted Year and month from released date using dt.year and dt.month. **Trailing space** was also removed by strip() function and **fuzzywuzzy** was used for game
Portal 2 as there were some similar named games present in my dataset. Then after getting satisfied that there was no writing error in their names and they were 
distinct, I summarized my dataset to start analysis.

## 3. Data Analysis
This data was sorted according to playtime to determine the most played game out of all. After getting the results games released in 1999 was sorted out separately,
as it's average playtime was abnormally high. Then year-wise most played games were sorted in ascending order. As soon  as this process was applied according to
rating column the results didn't match, which gave us a conclusion that the most rated games were not always the most played ones. So the criteria for popularity
of game can't be the rating of that game. Now the probability of rating a game if it is reviewed was determined. Then this data was grouped, counted and sorted
according to year to determine when did the production boomed. Most favorite games were determined overall and yearwise by sorting them accordingly then after.

## 4. Data Visualization and Conclusion
The  above found trends were then visualized by using pyplot interface of matplotlib library of python and the following conclusions were made:

Conclusions:
1. Most rated games are not always the top played ones. Some of them however, are most popular ones. Hence, rating of any game
   can't be considered as criteria of determining popularity of any game.
2. There is a high chance that people reviewing a game will give good ratings.
3. There was significant increase in production of games after 2013. Also, total playtime and average playtime was significantly
   increased after increase in production of games.
4. The most played game of all time is Pokémon Gold, Silver which was released in 1999, due to which there was an abnormal
   increase in average playtime in 1999.
5. The most favorite and most rated games of all time are Grand Theft Auto V and AI: THE SOMNIUM FILES - nirvanA Initiative
   respectively.
