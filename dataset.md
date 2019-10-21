# DataSet <h1>

### Data Description
This data is obtained from the list of followers of the target account.

### Format
Saved in .csv and .json

### Field Names
* Account :
contains a list of user accounts from the target Instagram account.
* Post : 
contains a caption in every post from the user's account.
* Hastag : 
contains hashtags that are used for each user posting account.
* Likes :
contains the number of likes obtained by user accounts for each user account post.
* Comments :
contains the contents of comments in each user account post.

| Account | Post | Hastag | Likes | Comments |
| -------- | ---- | ------ | ----- | ------- |
| ........ | ..... | ..... | ...... | ...... |
| ........ | ..... | ..... | ...... | ...... |



### How many dataset can be reached? 
Have reached about 14000 row of dataset and size about 1 mb


### How to process 
Log in to your Instagram account with your username and password using the '''L method = installal.Installoader (max_connection_attempts = 0)'''. After that we determine the target username that we want to see account information. Create a profile object using the instaloader.Profile.from_username method whose parameters are taken from previously created variables. After that, iterate the followers owned by the target username. after completing iterates all followers, each follower index is iterated again by followers. We create an output file in the form of CSV and Json to store all follower list information from the target username. This CSV file consists of the names of the following fields: account, post, hashtag, likes, comments, post date, and private. This private output is only True or False. If the followers account is private, then proceed to the next account. On each profile, followers have posts, then repeat the post. If the post has no text, then continue to the next post. But if the post has a title, post, hashtag, likes, and comments, and the post date will be filled in. We provide a limit for each account post. We only take the first 100 posts from each account.

### Bag Of Words
Search for standard words in post account instagram.

### Format
Saved in .json 

### Field Names
* Account :
Contains a list of user accounts from the target Instagram account.
* Word1, Word2, ........ Word-n :
The word on the Instagram account posting

| Account | Word1 | Word2 | Word3 | Word-n |
| -------- | ---- | ------ | ----- | ------- |
| ........ | ..... | ..... | ...... | ...... |
| ........ | ..... | ..... | ...... | ...... |

### How many dataset can be reached? 
Have reached about 644 words of dataset and size about 250kb.

### How to process 

After successfully logging into the instragram and successfully retrieving followers from the results of crawling, then we take the standard words from the dictionary.text in accordance with the given contraints. After that take new words that are not in the dictionary. Text is from the post account followers that we have successfully crawled. After that iterates all the standard words from the post account. Collected in advance all the words we can until the iteration is finished. The output will be in the form of a json file like a table. The column will be filled if the words are in the Instagram account post.

