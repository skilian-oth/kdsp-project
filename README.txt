# KDSP Project


# Dependancies

- python 3 or more
- pandas : pip install pandas
- NLTK : pip install nltk

# Usage
The create_dataset.ipynb notebook can be used to create new datasets. 
It is not nessesary to run it as some datasets are already provided.

Each task is located in it's own notebook, named TaskN.ipynb.
It is nessesary to run every cell in the notebook to be able to run the application.
Each notebook have a cell called "Exemple usage" that shows how to use the application to obtain the results.


# Create a new dataset
- Set the settings in the settings cell, expecially the hashtag string and a API token
- Run the cell contraining the utility function
- Run the "import first batch" to create the files
- Run the "Import one more batch" cell to add 100 tweets to the dataset, as many times as needed
- Run the tests

# Task 1: Derive the sentiment of each tweet using Python module (no need to create your Algorithm)
- Use the add_sentiment_to_dataframe function to obtain a tweets dataframe containing the sentiment of each tweet. 
The parameter of the function is the name of the wanted dataset as a string.
- Print them using pandas


# Task 2: Top 10 hash tags and users based on their number of tweets in your data set.
- Use the print_top_10_hashtags and the print_top_10_authors functions to print the top 10s.
The parameter of the functions is a list containing the name of the wanted datasets as strings.

# Task 3: Get the followers of a given twitter user from your acquired data set.
- Set the bearer token if you want to use "online mode" which loads followers not stored in the files
- Use the user_id_by_username function to obtain the id of the wanted username : id = user_id_by_username("@ParisAntan", ["Paris"])
- Use the get_followers_offline function or get_followers_online to obtain the dataframe of followers : followers_df = get_followers_offline(id, max_results=348)
- Print them using pandas

# Task 4: Given a twitter user, obtain the tweets and profiles of all followers of the user and show it.
Same as Task3, but use get_followers_and_their_tweets instead of get_followers_offline to get the followers_df and tweets_df : followers_df, tweets_df = get_followers_and_their_tweets(id, datasets)

