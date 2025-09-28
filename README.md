# TMDB Film Rating Analysis Project

This is a project completed for the "Introduction to Data Science" course investigating the factors that lead to higher or lower movie ratings based on the TMDB movie database. It was a group project made by me and my fellow classnames (names listed in the report) and I played a key role in each step from the brainstorming, to the coding, to the analysis.

*The RMD file code and pdf knit can be found in the "analysis & report" folder.*
Link to the dataset: https://www.kaggle.com/datasets/joebeachcapital/top-10000-most-popular-movies-from-imdb/data

An introduction to this project, per our report:

## Motivating Questions and Scope of Analysis
Movies are one of the most popular pastimes in the world. Whether you drive down to the cinema to watch the latest release, or use Netflix from the comfort of your own home, chances are you have a feeling or opinion about the film that you’ve watched. TMDB is a website that stores movie information, and allows people to rate any movie that they’ve watched. As a team of movie-loving people, we wanted to ask the question: **what affects the rating of a movie?**

## Background on TMDB

**Overall Info:** TMDB (otherwise known as The Movie Database) is a movie database that contains detailed information about films in 50+ languages, as well as provides users an opportunity to rate the quality of films that they choose. Despite their similar name to IMDB, TMDB doesn’t use data from the former site, although ratings can be (and often are) similar. The reason we used TMDB is because the site is specifically designed to be great for data collection. A key feature of TMDB is its API which allows people to easily take their stored movie data and use it for data analysis, as we are doing currently!

**Ratings Details:** TMDB allows registered users to rate movies on a scale from 0.5 to 10.0 in 0.5-point increments. These ratings reflect the user’s personal opinion and are combined across all users to calculate the vote_average. Unlike some platforms, TMDB does not apply weighted averages or critic adjustments, every user’s vote carries equal weight.

**Information Details:** TMDB collects its data through a combination of user contributions and official studio sources. Registeredusersaroundtheworldaddandupdatemoviedetailslikecast, crew, genres, andruntime, while studios provide verified data such as trailers, budgets, and box office revenue. All entries are reviewed by moderators or voted on by the community to ensure accuracy.

**API Details:** TMDB offers a free and simple way for users to access its movie data through an API. After signing up and requesting an API key, users can search for films, get cast and rating info, and download data for analysis. This tool is especially helpful for developers, researchers, or anyone working on movie-related projects.

**Dataset Details:** The movies in our database were selected based on TMDB’s internal popularity score, which ranks films according to real-time user engagement. This metric is not the same as average rating or total votes, but instead incorporates multiple signals of user interest.

**How This Is Accomplished:** First, a request is made to the TMDB API to retrieve movies, which are then sorted in descending order of a popularity score. This popularity metric is a proprietary measure that includes factors such as page views, searches, frequency of user interactions (rating submissions, watchlist additions), and recency of engagement (recent movies or trending titles tend to be weighted more heavily).

From this ranked list, the top 10,000 movies at the time of collection were selected, without filtering by genre, time period, or language. For each movie, metadata is then pulled from the API to be compiled into the dataset, including title, vote average, vote count, release date, original language, genre, runtime, and more. Factors such as critical acclaim, box office success, historical or cultural importance, and completeness of data were not accounted for in selection.

Due to this approach, the dataset is biased towards more recent and popularly engaged films. Older or niche movies with fewer interactions are underrepresented, and those that are included are likely classics or cult favorites that maintain high ratings despite fewer votes.
