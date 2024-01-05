# DS-Project-2
Flatiron School Data Science Project - Phase II

## Overview
* Purpose: Management recommendations for critera to create a successful Box Office Movie
* Source of data: Sourced data from Box Office Mojo, IMDB, and The Numbers 
* Focus areas and consideration:
  * Primary Success Metric: the ratio of gross box office sales to the movie budget
  * Others :Foreign Success = (foreign gross / production budget) vs Domestic Success = (domestic gross / production budget)
* Data excluded - we believe they are less relevant to our analysis and so they were dropped in order to maximize efficiency and usability of the dataset.
  * Movies made before 1990
  * Any Movies for which Production budget or box office sales were unavailable

We excluded these movies because 
For this project our group was tasked with giving three recomendations to a company hoping to start a new film studio. The company that hired us has no information about film industry and wanted us to figure out what factors lead to box office success. Sourcing data from The Box Office Mojo, IMDB, and The Numbers we created a ROI statistic to compare 4000ish different movies on and came up with three actionable insights for the company to take with them: a high risk high reward investment recomendation, a mid level of risk and reward recomendation, and a safe investment recomendation. 
 
# Presentation and Sources
Presentation: [Link](https://docs.google.com/presentation/d/1Hi3_MnZvzkC9ihIU2DZK_-aFPpEosdvJ1Twb4eDvE3g/edit#slide=id.g1ee509a9fff_0_119)

Box Office Mojo dataset: [Link](https://www.boxofficemojo.com)

IMDB dataset: [Link](https://www.imdb.com)

The Numbers dataset: [Link](https://www.the-numbers.com)

Budgeting classification source: [Link](https://www.studiobinder.com/blog/production-budget/)


# Repository Navigation
Our Github Repository contains 2 main folders names Data and Notebooks. The Notebooks folder has 3 jupyter notebooks in it. The first of those notebooks is titled Data_Cleaning and is the notebook/kernel that the other two notebooks run off of, containing all of our data cleaning and exploration steps. It is important to run this notebook first and then change the kernel of the other two notebooks to the Data_Cleaning Kernel. The next notebook is titled Visualizations_Analysis and contains the all of our visualizations and statisical anaylsis. Finally the last notebook is titled Final_Notebook and contains a combination of markdown and coding cells that provides a summary of the project as well as our three recomendations we came to at the end. The Data folder contains all of the raw data we looked at as well as the cleaned data we ended using reconverted back into csv files. 

## Data Analysis & Recommendations

The first data science steps we took was making the data more accessable and manipulatible by importing csv files and a SQL database using pandas and sqllite3 and converting files into pandas dataframes. We then explored our data, looking at different summary statistics and sorting through different variables available to us for analysis in order to narrow down the dataset in to useful information only. 
Our first cleaning step was removing all movies that we had no monetary data for as the company was focused on box office success exlusively. After reducing the data down we created a new standardized metric to allow for comparison across movies. This metric was the worldwide gross of the movie divided by the production, creating an ROI metric that told us in one number the amount of money the movie made or loss in comparison with the money spent to make the movie.
We next wanted to differentiate between big blockbuster movies and smaller indie films and what not so conducted a little bit of outside research on industry standards and created three categories of movies: low budget (budget < 5 million) movies, medium budget (5 mil < budget < 50 mil), and high budget movies (budget > 50 mil). We created three new dataframes based off of this classifications and conducted the rest of our analysis through this tiered budget lens.
Based off of our exploration we chose runtime, genre, and personel as the three most important variables that contribute to box office success and are controllable before the release of a movie. We then visualized these three variables, grouped by the three budget categories and ran signifigance testing in order to come up with actionable insights from the data we had collected. 

* 
Our recommendations are the following: (snip of slide)

<img width="1081" alt="Screenshot 2023-12-08 at 11 44 51 AM" src="https://github.com/WesleyDickens/DS-Project-1/assets/8894178/e3997252-dc83-4aca-9417-cd9874d983bf">

* Based on our breakdown of the production costs, low budget films have a much higher standard deviation of success than medium and high budget films, making them a high risk, high reward investment. (snip of std dev slide)

<img width="1051" alt="Screenshot 2023-12-08 at 11 44 26 AM" src="https://github.com/WesleyDickens/DS-Project-1/assets/8894178/69f3910a-895c-44a1-af72-3824a00c31d2">

* When it comes to genre, different genres are more successful at different production costs intervals, with Horror topping low budget, horror and musical taking the mid tier budget, and music and animation being the best for high budget films  ()

<img width="1050" alt="Screenshot 2023-12-08 at 11 45 01 AM" src="https://github.com/WesleyDickens/DS-Project-1/assets/8894178/0c92b0fa-2ce1-4eb7-939b-d47890eb5769">

* finally we looked at which actors, writers, and directors are responsible for the highest grossing movies (snip of actors/writers/directors)




