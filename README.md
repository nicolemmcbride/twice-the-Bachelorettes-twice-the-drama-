<b>Bachelorette Season 19 : Twice the Bachelorettes, twice the drama?</b>
---
Abstract
---
A variety of natural language processing techniques were run to examine all the subtitled text from Season 19 of The Bachelorette, which resulted in a total corpus text of 150,290 words. The overall sentiment of each episode was superbly positive and each episode typically spends 60% of the time centered around dating and 40% of the time centered around decision making and final rose selections. In sum, the season did not show negative sentiment.

Design  </b>
The Bachelorette has been running in the USA for a total of 19 seasons, and this was the first ever season to have two contestants as the Bachelorette vice only one. ABC prides itself on making every season more dramatic that the previous. Therefore, natural language processing will be used to see how dramatic this season really was. This is important for the fandom as most of us are definitely expecting this.
---
Data  </b>
All subtitled text were downloaded as .srt files from opensubtitles.org. The files are plain text files that contain start and end time stamps of text and sequential number of subtitles. Each episode was downloaded then went through a variety of data cleaning and pre-processing techniques. Capital letters, punctuation, numeric values, and stop words were removed.
---
Algorithms  
Feature Engineering: Episode, segment, and five minute interval were feature engineered. Each row in the corpus represented all the subtitled text for each 5 minute duration in each episode. This resulted in a final corpus of 194 documents. Additional corpus text were made where each document represented an episode (11 total documents) and another made where each document represented a segment in an episode (intro, first ⅓, second ⅓, third ⅓, outro).  
Exploratory Analysis: A world cloud was created to display the most common words for each episode. This world cloud revealed that “love” was a top word, but mostly after episode 6. A horizontal bar chart of how many times “love” was said for each episode revealed that “love” was said the most in Episodes 7, 9, and 11. This makes sense because episode 7 is where the contestants get to take the Bachelorette to their hometown, episode 9 is where the contestant and the Bachelorette get to spend the whole day and night together, and episode 11 is the finale.  </b>
Textual Analysis: A Vader sentiment analysis was performed on all the subtitled text for each episode and revealed an average compound score for each episode of .99. A series of topic models were performed using a variety of techniques and manipulation of variety of hyperparameters, such as min_df, max_df, iterations, vectorization, stop word removal, and part of speech tagging. After 24 topic models run, the model that pulled nouns, adjectives, plural nouns, and eliminated words that appeared in less than 25% of the documents and words that appeared in more than 80% of the documents were removed. This model resulted in two topics - “Dating” and “Rose Selection”. These topics were applied to the episode segment corpus and found that “Dating” was most found in the intro, first ⅓, and second ⅓ of each episode and “Rose Selection” for the third ⅓ and outro of each episode.
---
Tools  </b>
Numpy, Pandas, Scikit-learn, Matplotlib, NLTK, wordcloud, VADER sentiment, gensim
---
Communication: Final Presentation

