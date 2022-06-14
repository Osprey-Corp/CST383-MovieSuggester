# Movie Suggester [(Video Link)](https://drive.google.com/file/d/13qSuhsRrUWzm1kt996fj2e677HC1H7zb/view?usp=sharing)
### By: Haylee Bell, Marilyn Kathka, David Baker and Eduardo Belman
### Introduction
After you finish watching a movie do you feel empty with nothing to do? This project aims to solve this common problem by suggesting a similar movie to you, so you have something else to watch.
At the end of this project we will be able to predict which movies a user will be most likely to enjoy, depending on the last movie they watched. To do this we will be using imdb score, release year, and runtime as predictors to find which movie the user should watch next.

### Selection of Data: justwatch by victor-soeiro ([dataset](https://github.com/victor-soeiro/WebScraping-Projects/tree/main/justwatch))
This data was compiled by Victor Soeiro over many years of web scraping. The set he compiled is distributed through github and kaggle for research purposes. 
The data from this dataset was scraped from various streaming platforms such as amazon, apple tv, crunchyroll, darkmatter, disney, funimation, hbo, hulu, netflix, paramount, rakuten viki, and starz. 
The information included in the dataset from the movies/tv shows are the title, type, description, release year, age_certification, runtime, genres, production countries, seasons, imdb id, imdb score, imdb votes, imdb popularity and imdb score.\
\
The data munging that had to be done was remove all of the entries in the data that weren't of type movie. This is due to the goal of our project being movie based and does not include predictions for tv shows. 

### Methods
The programming language used to get the job of creating a movie recommendation model was Python. To manipulate the data we used the **numpy** and **pandas** libraries.
SKLearn was used for the machine learning portion of the project. We imported their **train_test_split** module from SKLearn to create training and test data from our dataset. 
We also imported **StandardScaler** to scale our data before training our model. The **NearestNeighbors** module was used to train our model. This algorithm was chosen because it's simple and
perfect for the job we want to get done. We can provide our trained model a movie and it'll give us back various movies similar to the one we gave it. This is exactly what we need to get the job done.

### Results
After implementing the machine learning algorithm to our data, we were able to succesfully create a model that will recommend movies to a user similar to the one they input. The imdb score, release year, and runtime were used as predictors and are the factors that help the model choose similar movies. Here's an example:

#### Movie Chosen by User
| Title | IMDB Score | Release Year | Runtime |
| :---:                             | :-: | :--: | :-: |
| Transformers: Age of Extinction   | 5.6 | 2014 | 165 | 

#### Movies Recommended by Trained Model
| Title | IMDB Score | Release Year | Runtime |
| :---:                             | :-: | :--: | :-:|
| Sheborg Massacre                  | 3.9 | 2016 | 90 | 
| The Taking of Deborah Logan       | 6.0 | 2014 | 90 | 
| Events Transpiring Before...      | 5.9 | 2020 | 76 | 
| Cannibal Island                   | 6.1 | 2011 | 55 | 
| Guns Akimbo                       | 6.3 | 2020 | 95 | 

Visualizations
| Average IMDB Score by Genre | Average IMDB Score by Release Year | Average Runtime by Release Year |
| :---:                             | :-: | :--: |
| ![1](https://raw.githubusercontent.com/Osprey-Corp/CST383-MovieSuggester/main/1.png) | ![2](https://raw.githubusercontent.com/Osprey-Corp/CST383-MovieSuggester/main/2.png) | ![3](https://raw.githubusercontent.com/Osprey-Corp/CST383-MovieSuggester/main/3.png) |
| Lowest Rated Genre: horror <br /> Score: 4.22  | Lowest Rated Year: 1935 <br /> Score: 5.40 | Year with Lowest Runtime: 1901 <br /> Avg Runtime: 2.0  |
| Highest Rated Genre: documentation <br /> Score: 6.91 |  Highest Rated Year: 1926 <br /> Score: 7.20 |Year with Highest Runtime: 1916 <br /> Avg Runtime: 138.8 |
### Discussion
The results of this project were more effective than expected. It was a matter of choosing the right machine learning algorithm and manipulating the data in the correct way to produce the best results. A way in which this project could have been improved would be by using more predictors so the model can make better choices. If we had more time, every category could potentially be used. For example the genre category could have been turned into numerical data depending on what categories the movie was labeled. This would allow us to also use it as a predictor and yield better results. Python is one of the best languages for data science due to all of the great libraries that can be used. Numpy, pandas, sklearn and pyplot were crucial in getting the task completed. Their ease of use and simple implementations allowed the team to get further into the project than at first thought possible.

### Summary
The most important findings in this project is how simple and easy it is to make a movie recommendator. Big companies such as Netflix or Hulu probably implement the same types of machine learning used in this project to make their recommendations. This could potentially lead someone who specializes in such topics to have a great career in a company that focuses on streaming. These companies rely heavily on algorithms to provide the best experience to their users and this project was great to get a good understanding what goes on behind the scenes.
