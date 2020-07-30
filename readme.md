# Oscar success prediction

Using data scraped from the official Oscars website, as well as movie websites such as IMDB,boxofficemojo, and rotten tomatoes, this project uses linear regression, LASSO regression, and Ridge regression to predict the number of Oscars a nominated film will take home

## Project Pipeline

#### Data Acquisition

5 different data sources were used:

1. [Official Oscars website](http://awardsdatabase.oscars.org) Oscar nominee and winners data from 1985 to 2019

2. [Boxofficemojo](https://www.boxofficemojo.com)

3. [TV tropes](https://tvtropes.org)

4. [Rotten tomatoes](https://www.rottentomatoes.com)

5. [Wikipedia](https://wikipedia.org)

The Oscars website was used to collect data on all nominees in the past 35 years. Boxofficemojo is where a majority of movie data was collected such as genre, distributor, domestic boxoffice, runtime, budget, rating, release year,etc. TV tropes was used to collect the number of Oscar-favored tropes each movie had. This study goes into more details if you are interested: [[https://github.com/dw-data/movie-tropes]{.underline}].

Rotten tomatoes was used for movie review data and wikipedia was used for trivia data such as weather or not the movie was based on a book or real life events.

#### Data Processing

-Combining different data sets scraped from different websites into one.

-Used helper functions such as regex and fuzzywuzzy to match data sets to their correct location as well as cleaning them.

-For any missing budget or boxoffice value, the average of those values across the entire dataset was used to replace it.

- Date of release was converted to months to get a better look at different time period's effects.

#### Machine Learning attempts

Three types of regressions were used: OLS, LASSO, and Ridge. For each one of the three, a cross validation test with a 60-20-20 split was performed. The dataset was iterated after each attempt to better the r squared, p value, and condition number, a variance inflation factor test was also done on the data. Interaction effects were also explored.

## Deliverables

#### Notebooks

[Web scraping](/Notebooks/web_scraping.ipynb)

[Machine Learning/Visualization](/Notebooks/ML_+_visualization.ipynb)

#### Presentation

[Oscars_Prediction.pdf](/Presentation/Oscars_Prediction.pdf)

- [Andrew Wu](https://github.com/andywzz/)

## Additional Information

#### Folders

```Notebooks``` - all Jupyter notebooks used for the project.

```Data```

- ```movie_data.csv``` - A csv file of all the movie information collected

- ```sorted_movie_data``` - a textedit file for notebook use

- ```sorted_movie_data2``` - a second textedit file for notebook use

### Technologies Used

* Jupyter Notebook

* Python

* Pandas

* Numpy

* Matplotlib

* Fuzzywuzzy

* sklearn

* statsmodel
