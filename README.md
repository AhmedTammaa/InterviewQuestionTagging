# InterviewQuestionTagging
This project is a helper project for <a href= "https://github.com/AhmedTammaa/InterviewInsightMine">InterviewInsightMine</a> which taggs question of scrapped data

# Problem
In the  <a href= "https://github.com/AhmedTammaa/InterviewInsightMine">InterviewInsightMine</a> there has been collected 9000+ data, however analyzing them is difficult task since they are not tagged
# Solution
Train a model from data StackOverFlow and StackExchange website. They publish <a href="https://archive.org/details/stackexchange"> Stack Exchage Data Dumps</a> <br>
  In this project we are interested in Posts file which contains the question and the tags.
  The first iteration of this project is done on stats.meta.stackexchange.com.7z.
  Because of the limited GPU power and also we don't need all tags I extracted only the top 50 tags. 
# Preprocessing
  The preprocessing is basic
  1. Removing StopWords
  2. Making all strings to lower
  3. stemming the words 
  4. Removing the slashes and other symbols

# Model
The data is then fitted with tfidf vectorizer and fed into covolution model
# Prediction
The prediction is a vector of 50 elements withe each from 0 to 1 as probability for a tag to be associated with question
# Loss Function
MSE loss between the actual vs predicted vector. 
Current Testing loss: 0.0268

  
