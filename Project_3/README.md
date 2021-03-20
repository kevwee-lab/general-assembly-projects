# Project 3 - Subreddit classification: Horror vs SciFi

## **Problem Statement**

In the words of Arthur C Clarke (a famous science fiction author), science fiction seldom attempts to predict the future. More often than not, it tries to prevent the future. This implies that science fiction is a sobering warning to us about dystopian or undesirable futures that might happen if we do not take steps now to change it.

Therefore, sometimes science fiction could be accompanied by some elements of horror and might be indistinguishable from the horror genre. 

Being a long time fan of a subreddit called r/nosleep, where redditors write and post horror stories, I attempt to investigate and discover if there are ways to differentiate science fiction from horror.

Specifically, my problem statement is as follows:

**Are there a set of words that define a genre, in this instance. horror vs scifi?**
<hr/>

## **Executive Summary**

To address the abovementioned problem statement, we did the following:
1) Scraped the r/nosleep (horror) and r/shortscifistories (science fiction) to obtain data for analysis <br>
2) Cleaned data by removing null values and non text posts.<br>
3) Split the data into single word tokens, removed punctuations and digits, and lemmatized the tokens to reduce the tokens to a single form, i.e. 'builds' to 'build'. <br>
4) Fitted and evaluated machine learning classification models to determine which model best distinguishes scifi from horror. <br>
5) Analysed the best model to look at misclassified posts. <br>
<hr/>

## **Conclusion**

Horror and scifi do have some similiarities but are different genres in their own right. Certain sets of words define the respective genres and set them apart from each other. Some of the words that define the scifi genre are words related to technology, the galaxy and planets, e.g. ai, system, robot, earth etc.The words that define horror genres seem to be related to either the senses, e.g. seeing or hearing something, or to home related words like room, house, and door.

We also note that our best model, after considering all 6 metrics of best score, delta, ROC AUC, confusion matrix, precision and recall, was the Logistic Regression model with the TfidfVectorizer. Our model's best score was about 93.99%, which performed better than baseline. Out of the test data of 484 posts, our model misclassified 32 posts (19 false positives and 13 false negatives). We also took a step further to analyse the tokens for a false positive post, and found that the misclassification occurred because tokens from the positive class (class 1: r/nosleep) occurred more frequently than tokens from the negative class (class 0: r/shortscifistories).


If we had subreddit dedicated to full length scifi stories like nosleep, we could have come up with a better classifier as there could be more tokens that could further distinguish the 2 genres.