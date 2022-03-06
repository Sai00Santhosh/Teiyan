# Teiyan


Teiyan is a content-based anime filtering algorithm, that recommends anime based on genres, year, no. of episodes, and popularity.

### How does it work?

All of the "features" I considered are important <span style="color:red"> *(Note: subjective from person to person)*</span> are merged into one string and is added in the dataframe (seen in the last column on cell 9). We then use countVectorizer from the Scikit learn package to create a matrix which is then loaded into the cosine_similarity functions that generates a matrix where each combination of all the animes from our dataframes are compared. If the value is close to **1** the anime is highly similar and if close to **0** they are barely related/unrelated. The similarity scores are generated based on the **features** section in the dataframe we created as shown in cell 9.

We then choose our anime of prefererance and find related animes to that. We do this using the anime_id (as shown in cell 12), where we obtain the title in which the recommendation engine will pull out the most similar animes from the similarity matrix of that anime. 

### Future Changes and Modifications

I would like to give credit to this repo https://github.com/Prianca25/Machine-Learning/blob/master/Movie%20Recommender%20System.ipynb for the inspiration on how to go about solving the problem.

The code is far from ready to be used in production as there are several missing components I would like to add. Some of them include:

    - Building a better database (as there is no online database for anime that are up-to-date or extensive)
    - Getting user-data that would help in developing a hybrid-recommender system.
    - Modifying the current code to give reccomendations that "make more sense".
    
If any of you have any suggestions or could help me with any of the above, you could either create an issue on the Teiyan github repository or connect with me on LinkedIn (the link is on my profile) to discuss further.

Thank You for taking your time reading!