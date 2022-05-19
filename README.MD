# Disaster-Tweet-Analysis
This repo contains an approach I implemented for the Disaster Tweets competition on Kaggle. 
## Data
Each sample in the train and test set has the following information:

- The text of a tweet
- A keyword from that tweet (although this may be blank!)
- The location the tweet was sent from (may also be blank)
-
## Files
- train.csv - the training set
- test.csv - the test set
- sample_submission.csv - a sample submission file in the correct format
## Columns
- id - a unique identifier for each tweet
- text - the text of the tweet
- location - the location the tweet was sent from (may be blank)
- keyword - a particular keyword from the tweet (may be blank)
- target - in train.csv only, this denotes whether a tweet is about a real disaster (1) or not (0)

## Necessary Libraires or packages are:-
- Pandas
- Numpy
- Regular expression (re)
- NLTK
- matplotlib
- tensorflow
- GloVe
-
## My approach
- Clean text data present in both test and train dataset
- tokenizing the text
- removing the stopwords (on the basis of  nltk.corpus.stopwords)
- lemmatizing the text entries
- converting list of strings into joint strings
- <b>Importing the GloVe embeddings</b>

Next, I have used TextVectorization layer. And I also create an embedding matrix. In this case, the embedding matrix is N-by-300 matrix, where N is the total count of distinct words in the input dataframe. If the word is not found in the embeddings_index, then the corresponding column is all-zeroes.

### At last, I have initialized the keras model for training purpose, the architecture of the model is Embedding layer, Dropout, LSTM, Conv1D, GlobalMaxPooling1D, Dense and Output.
