# Investigate TMDB Movie Data
The dataset that I'm gonna investigate is a dataset that contains information about 10,000 movies collected from The Movie Database(TMDb), including user ratings and revenue.

## Table of contents
1. [Installation](#installation)
2. [File Descriptions](#files)
3. [Data](#data)
4. [Data Analysis](#dataanalysis)
5. [Results](#observations)
6. [License](#license)

## Installation
The following libraries and tools are used in this project:
- **`Numpy`**
- **`Pandas`**
- **`Matplotlib`**
- **`Seaborn`**
- The code should run with no issues using Python version 3.*.

## File Descriptions
This project contains the following files:
- **`tmdb_movies.csv`**: holds the movie data.
- **`InvestigateTMDBMovieData.ipynb`**: Jupyter notebook containing python code and brief description about each step.
- **`InvestigateTMDBMovieData.html`**: HTML version of notebook.

## Data
The data for following is collected from [The Movie Database(TMDb)](https://www.themoviedb.org/?language=en-US). You can also find data form [kaggle](https://www.kaggle.com/tmdb/tmdb-movie-metadata) but it seems like the data on kaggle is different from what I have. Anyway if you want the same data I have used you can find the [file](https://github.com/ManideepTelukuntla/InvestigateTMDBMovieData/blob/master/tmdb_movies.csv) in the repo.
- The data contains around **`10,000`** movies and **`21`** attributes for each movie:
    - id                         
    - imdb_id                   
    - popularity                
    - budget                    
    - revenue                   
    - original_title            
    - cast                      
    - homepage                
    - director                  
    - tagline                 
    - keywords                
    - overview                  
    - runtime                   
    - genres                   
    - production_companies    
    - release_date              
    - vote_count                 
    - vote_average               
    - release_year               
    - budget_adj                 
    - revenue_adj

## Data Analysis
I have performed data analysis process on this dataset which includes five main steps:
- Questions
- Data Wrangling
- Exploratory Data Analysis(EDA)
- Draw Conclusions
- Communicate Findings

#### Questions
These are the following questions I want to analyze using this dataset:
1. Which genres are receiving higher user ratings?
2. What kinds of properties are associated with movies that have high revenues?
3. Does higher budget movies have higher user ratings?
4. How is the revenue and popularity trend for movies from year to year?

#### Data Wrangling
In this section I have done lot of data cleaning which includes handling **`NULLs`**, **`Duplicates`**, **`Datatypes`**, etc.. I just want to provide you summary of what I have done.

- Initially started inspecting general properties of dataframe like `shape`, `nulls`, and `dtypes`.
- Removed the columns containing `nulls` and the columns that are not necessary for my analysis.
- Inspected for duplicates, found only `1` duplicate and dropped from the dataframe.
- Next, inspected for number of rows with `nulls` and dropped from the dataframe.
- Finally, inspected for data types and converted `budget`, `revenue` and `runtime` columns to `floats`.
- After all these data wrangling steps I ended up with `9806` rows and `14` columns.

#### Exploratory Data Analysis(EDA)
In this step I have explored my data to compute statistics and create visualizations with the goal of addressing the research questions that I have posed in the Introduction section.
- Please have a look at the notebook for detailed information on this step.

#### Draw Conclusions
Based on the analysis performed in the EDA step I have drawn some conclusions which are listed down next to the each step in the notebook(look for EDA step).

#### Communicate Findings
Finally I have communicated my findings using visuals and markdown notes at the end of the notebook.

## Results
These are the answers I found based on my analysis:
>**ANS 1**: Based on my findings it is found that these are some of the genres receiving higher user ratings:
- Science Fiction
- Animation
- Drama
- Fantasy
- Action

>**ANS 2**: Based on my findings the following properties are associated with movies that generate higher revenues:
- Higher user ratings
- Higher number of votes
- Higher popularity

>**ANS 3**: Based on my findings higher budget movies have higher user ratings which implies that most of the higher budget movies are successful.

>**ANS 4**: Based on my findings the trend of revenue and popularity of movies from year to year is increasing which implies interest for movies has increased as years progressed.

#### Limitations
- There are certain movies with `0` value for both `budget_adj` and `revenue_adj` which I left as is which might alter my statistics.

## License
Licensed under [MIT License](https://github.com/ManideepTelukuntla/InvestigateTMDBMovieData/blob/master/LICENSE)
