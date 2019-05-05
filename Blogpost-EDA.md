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

Movies Dataset contains 4627 movies in 20 genres produced between 1915 and 2017. 

The yearly number of movies produced has a tendency to grow with time. However the average budget started dropping after the year 2000 (see below).

  Yearly number of movies  |  Yearly budget 
:-------------------------:|:-------------------------:
![num_of_movies](https://user-images.githubusercontent.com/46948881/57201292-21be2400-6f65-11e9-9710-87993d1ecc0e.jpg) | ![yearly budget](https://user-images.githubusercontent.com/46948881/57201506-c3df0b80-6f67-11e9-8a2e-1e43fbc234af.jpg)

