# Movies Analytics

### Dataset Structure
The movies dataset contains metadata for all 45,000 movies listed in the Full MovieLens Dataset. 
The dataset consists of movies released on or before July 2017. Data points include cast, crew, plot keywords, budget, revenue, posters, 
release dates, languages, production companies, countries, TMDB vote counts and vote averages. This dataset also has files containing 26 million ratings from 270,000 users for all 45,000 movies. 
([Source](https://www.kaggle.com/rounakbanik/the-movies-dataset))

The files used in our analysis and their relations are showed below:
![Dataset_structure](https://user-images.githubusercontent.com/46948881/57206113-5516a800-6f91-11e9-9dad-e213775ffef3.jpg)


After performing data wrangling we finished by having one dataset of the following structure: 

![Dataset_screenshot](https://user-images.githubusercontent.com/46948881/57199906-ac495800-6f52-11e9-80a7-721af8e792bd.jpg)

### Exploratory Data Analysis 

Movies Dataset contains **4627 movies** in 20 genres produced between 1915 and 2017. 

The yearly number of movies produced has a tendency to grow with time. 
![num_of_movies](https://user-images.githubusercontent.com/46948881/57203055-52f51f00-6f7a-11e9-83fc-5f990ecb7cea.jpg)

There are **4981 production companies** in the dataset. Here is the 20 biggest companies (which produced the highest number of movies)
![prod_comp](https://user-images.githubusercontent.com/46948881/57202633-8f724c00-6f75-11e9-9e55-eb4f8eed3164.jpg)

### Budget 
Let's check yearly average budget spent by these companies:
![yearly budget-1](https://user-images.githubusercontent.com/46948881/57202638-a44edf80-6f75-11e9-85d1-e44d0e8a4e64.jpg)

There is a suspicious race of a budget somewhere between 1925 and 1935. Let's take a closer look. Here are the movies produced within this period:
![movies_25-35](https://user-images.githubusercontent.com/46948881/57202691-54bce380-6f76-11e9-94e9-8b2f74b1a60f.jpg)

Now we see that the movie "Metropolis" has a budget of $92,620,000. After double checking on we IMDB website, we see that the real budget is $6,000,000. Here is the trend after correcting this value:
![yearly budget-2](https://user-images.githubusercontent.com/46948881/57203031-132e3780-6f7a-11e9-9ddc-4847b2262b0a.jpg)

And we can conclude that unlike the number of movies, the budget spent on production started dropping after the year 2000.

### Universal Pictures Revenues
Let's look into budget and revenue curves for **Universal Pictures**:
![universal_budget](https://user-images.githubusercontent.com/46948881/57203058-57b9d300-6f7a-11e9-9a49-c1fbede5e143.jpg)

This time the revenue jumps up in 1975. Once looking closer we get one movie from 1975:
![universal_1975](https://user-images.githubusercontent.com/46948881/57204303-e6cbe880-6f84-11e9-9a82-550119ef3198.jpg)

This time there is no mistake: 14-award winner "Jaws" brought in $470,653,000.

In the previous plot, we saw that amount of $470,653,000 was looking higher than the revenues from the last years. 
This looks not logical. Let's check which 10 movies brought the higest revenue:
![highest_revenues](https://user-images.githubusercontent.com/46948881/57205260-4f1dc880-6f8b-11e9-9abb-01102b1ab296.jpg)


However, the highest income during last years gets over a billion. Here we realized that we shouldn't have removed the budget and revenue "outliers", as they are probably not. We adjusted our data wrangling file and saved a new version of "clean" dataset. 
These are the 10 movies with higest revenues after adjustment:
![highest_revenues_real](https://user-images.githubusercontent.com/46948881/57206288-a1161c80-6f92-11e9-9031-36ebb584d768.jpg)

This is an updated plot for Universal Pictures but here we are comparing total revenues instead of mean as in 1975 they produce only "Jaws" and the mean for 1975 will be higher than all other years.
![universal_budget_sum](https://user-images.githubusercontent.com/46948881/57206010-965a8800-6f90-11e9-8f0e-4b465c77b601.jpg)

We are noticing positive dynamics for Universal as with time the gap between budget and revenue is getting bigger.

### Add revenue by release month
