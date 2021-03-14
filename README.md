# Movies Recommendation System 
## Problem Statement
In this hustling world, we have spent too much time on entertainment media to refresh our mood or re-energize ourselves by listening to various music songs/videos or watching numerous movies.  Because searching for movies that the users are likely to enjoy does require a lot of time and energy, a movie recommendation system that can suggest a list of movies based on the user’s watch history or various preferences, such as actors/actresses, directors, or genres, can be quite useful for the user to decide which movies they want to watch right at the moment.  As we set out to design and implement a robust movie recommendation system, we identified the following challenges that needed to be addressed in our implementation:
1. How will you design your recommendation system if you want to recommend movies watched by "similar" users? How to determine if users are "similar"? How to evaluate if the recommendation is effective?
2. How will you improve your model if user behavior is considered stateful? In other words, if you are also given the watching history of a user ordered by time, how are you going to recommend the next movie for that user? How to evaluate if the recommendation is effective in this case?
3. How to recommend movies to new users in the absence of a user history?
As stated above, we described a problem that we plan to solve along with three challenges that need to be addressed in our implementation of a movie recommendation system.  

## Dataset(s)

## Approaches/Techniques/Algorithms
In this section, we’re going to cover the approaches, techniques, and algorithms that we initially proposed to use for our project, as well as the ones that we ended up using in designing and implementing our movie recommendation system.
First, let’s take a look at what we proposed to use in our project proposal.

### Proposed Approaches/Techniques/Algorithms
According to our project proposal for implementing a movie recommendation system, we proposed to use the following approaches and methods:
    *Machine learning algorithms in recommender systems typically fit into two categories: **content-based systems** and **collaborative filtering systems**. Content-based methods are based on the similarity of movie attributes.  With collaborative filtering, the system is based on past interactions between users and movies.*

    *Both “Collaborative filtering method(s) and content-based method(s)” can be used for addressing the challenges mentioned above along with other techniques as described below.
    **Collaborative Filtering Method(s)** calculate similarity from interactions.
    - Recommend items liked by similar users
    - Enable exploration of diverse content
    - Matrix factorization technique: Matrix factorization is a class of collaborative filtering algorithms used in recommender systems.(used in Netflix prize challenge)

    **User-based k-Nearest Neighbors**
    - Compute similarity of users
    - Find k most similar users to a particular user
    - Recommend movies not seen by the particular user
    
    Content-Based Method(s) are based on similarity of item attributes.
    - Given the watching history of a user ordered by time, we can recommend the next movie for that user 

    **Evaluation Measures**
    - Given some observed, explicit ratings (e.g. assigned number of stars), the recommender is to predict a rating for an unknown user-item pair by using RMSE
    - More practical offline evaluation measure is recall or precision evaluation percentage of correctly recommended items (out of recommended or relevant items).
    **Attribute Similarity** can be used in addressing the cold start problem.
    - Items clustered based on their interaction similarity and attribute similarity are often aligned.
    We can use a neural network to predict interaction similarity from attributes similarity (and vice versa).*

### Actual Approaches/Techniques/Algorithms
Here are actual approaches, techniques, and algorithms that we ended up using for designing and implementing our movie recommendation system.

#### Collaborative Filtering based Recommendation

#### Content-based Recommendation
In addition to using the collaborative filter approach, we used the content-based approach in recommending movies based on the similarity of move attributes as the input for building a content-based recommender is movie attributes (metadata).  For example, if a user watches a comedy starring Adam Sandle, the system will recommend movies in the same genre, starring the same actor or both.

#### Recommending Movies Based on the User’s Watch History
In our research, we couldn't find an existing movie recommender that is based on a user's watch history. So, we decided to come up with our own movie recommender that accounts for the user's watch history as shown below. 


## Our Implementations vs. Existing Work
The following future shows three challenges that we identified early on in our project and whether we came up with our own solutions/work in addressing each challenge.  Except for the challenge 3, we were able to come up with our own solutions/work in addressing challenges 1 and 2.


## Experimental results and analysis
In this section, we’re going to describe experimental results and analysis that we conducted on the following approaches, techniques, and algorithms: Collaborative filtering, content-based, and recommending movies based on the user’s watch history.
### Collaborative Filtering

### Content-based Recommendation
Because TfidfVectorizer() has more columns, it requires more computing resources.  Hence, for our implementation of the content-based recommendation system, CountVectorizer() is a better choice.  After sorting the similarity rankings, both CountVectorizer() and TfidfVectorizer() recommend the same list of 10 movies for an input movie ‘Mission Impossible II (2000)’ as shown below.

## Future work 
The following list shows additional work that could be done in the future:
- a mobile app for easy-access
- better ways to evaluate the model
- Implementing the Low-dimensional factor models
- Improving the ‘recommend_movies_based_on_user_watch_history’ function by accounting for the user’s movie ratings

## References
1. https://towardsdatascience.com/how-to-build-from-scratch-a-content-based-movie-recommender-with-natural-language-processing-25ad400eb243
2. https://analyticsindiamag.com/how-to-build-a-content-based-movie-recommendation-system-in-python/
