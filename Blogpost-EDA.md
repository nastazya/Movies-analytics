# Movies Analytics

### Dataset Structure
The movies dataset contains metadata for all 45,000 movies listed in the Full MovieLens Dataset. 
The dataset consists of movies released on or before July 2017. Data points include cast, crew, plot keywords, budget, revenue, posters, 
release dates, languages, production companies, countries, TMDB vote counts and vote averages. This dataset also has files containing 26 million ratings from 270,000 users for all 45,000 movies. 
([Source](https://www.kaggle.com/rounakbanik/the-movies-dataset))

The files used in our analysis and their relations are showed below:

![Dataset_structure](https://user-images.githubusercontent.com/46948881/57199665-9be3ae00-6f4f-11e9-8e9d-5d9bddfc41ac.jpg)

After performing data wrangling we finished by having one dataset of the following structure: 

![Dataset_screenshot](https://user-images.githubusercontent.com/46948881/57199906-ac495800-6f52-11e9-80a7-721af8e792bd.jpg)

### Exploratory Data Analysis 

Movies Dataset contains **4627 movies** in 20 genres produced between 1915 and 2017. 

The yearly number of movies produced has a tendency to grow with time. 
![num_of_movies](https://user-images.githubusercontent.com/46948881/57202801-900be200-6f77-11e9-8581-e7ee8686aa7d.jpg)


There are **4981 production companies** in the dataset. Here is the 20 biggest companies (which produced the highest number of movies)
![prod_comp](https://user-images.githubusercontent.com/46948881/57202633-8f724c00-6f75-11e9-9e55-eb4f8eed3164.jpg)

Let's check yearly average budget spent by these companies:
![yearly budget-1](https://user-images.githubusercontent.com/46948881/57202638-a44edf80-6f75-11e9-85d1-e44d0e8a4e64.jpg)

There is a suspicious race of a budget somewhere between 1925 and 1935. Let's take a closer look. Here are the movies produced within this period:
![movies_25-35](https://user-images.githubusercontent.com/46948881/57202691-54bce380-6f76-11e9-94e9-8b2f74b1a60f.jpg)

Now we see that the movie "Metropolis" has a budget of $92,620,000. After double checking on we IMDB website, we see that the real budget is $6,000,000. Here is the trend after correcting this value:
![yearly budget-2](https://user-images.githubusercontent.com/46948881/57202740-e4fb2880-6f76-11e9-9df6-66b3cfdbe858.jpg)

And we can conclude that unlike the number of movies, the budget spent on production started dropping after the year 2000.

Let's look into budget and revenue curves for Universal Pictures:
