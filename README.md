# netflix-movie-recommendation-engine

Netflix is all about connecting people to the movies they love. To help customers find those movies, they developed world-class movie recommendation system: CinematchSM. Its job is to predict whether someone will enjoy a movie based on how much they liked or disliked other movies. Netflix use those predictions to make personal movie recommendations based on each customer’s unique tastes. And while Cinematch is doing pretty well, it can always be made better.

Now there are a lot of interesting alternative approaches to how Cinematch works that netflix haven’t tried. Some are described in the literature, some aren’t. We’re curious whether any of these can beat Cinematch by making better predictions. Because, frankly, if there is a much better approach it could make a big difference to our customers and our business.

Read more about Netflix Prize: https://en.wikipedia.org/wiki/Netflix_Prize

Here, Netflix has provided a lot of anonymous rating data, and a prediction accuracy bar that is 10% better than what Cinematch can do on the same training data set. (Accuracy is a measurement of how closely predicted ratings of movies match subsequent actual ratings.) 


### Given data:
The file "training_set.tar" is a tar of a directory containing 17770 files, one per movie. The first line of each file contains the movie id followed by a colon. Each subsequent line in the file corresponds to a rating from a customer and its date in the following format:

CustomerID,Rating,Date
~ MovieIDs range from 1 to 17770 sequentially.
~ CustomerIDs range from 1 to 2649429, with gaps. There are 480189 users.
~ Ratings are on a five star (integral) scale from 1 to 5.
~ Dates have the format YYYY-MM-DD.

Movie information in "movie_titles.txt" is in the following format:

MovieID,YearOfRelease,Title

~ MovieID do not correspond to actual Netflix movie ids or IMDB movie ids.
~ YearOfRelease can range from 1890 to 2005 and may correspond to the release of corresponding DVD, not necessarily its theaterical release.
~ Title is the Netflix movie title and may not correspond to titles used on other sites. Titles are in English.

4 input files: combined_data_(1,2,3,4).txt

### Objectives:
1. Predict the rating that a user would give to a movie that he ahs not yet rated.
2. Minimize the difference between predicted and actual rating (RMSE and MAPE)