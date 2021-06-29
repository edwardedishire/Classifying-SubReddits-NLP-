# Project 3: Binary Classification of Subreddits (NLP)


## Problem Statement

Mental health issues have been on a high in recent times, with increasing cases of as a result of factors like post traumatic stress disorder (PTSD), bullying (real-life or cyber) and suicides. All these lead to depression which is a cause of concern for the government. 

Being part of a research team in the Institute of Mental Health (IMH), my team is tasked to come up a solution that can accurately predict and classify a post on reddit according to the subreddits (depression and forever alone). Both topics are commonly thought to be similar but they are not. Forever alone is a phrase or term used by a single person to express his loneliness at not having a significant other; or in broader perspective, lack of friends. It is also used more humorously at times as a slang or internet meme. This term is linked to people claiming to be "depressed" but in fact they are not.

On the other hand, depression is a serious matter and more often than not, one do not even realize that they actually have depression. It is also extremely challenging to determine if a person has depression by relying on behaviorial cues, even for a highly qualified psychiatrist. Furthermore, if the depressed person is introverted, he/she might not want to share his problems openly to his/her family or friends or even seek professional help in fear being stigmatized by society. As such, the person might turn to reddit, an online forum, to express his/her personal feelings and thoughts with other users in the same subreddit annoymously. He/she might feel more comfortable in that way. That being said, a user with depression might get confused over the terms depression and forever alone in thinking they are the same , thus posting in the forever alone subreddit rather than the depression subreddit. 

Hence, we aim to come up with a model that is able to accurately classify a post to the respective subreddits (depression/forever alone). Our model also aims to check for misclassification of post by diving deeper into the post, unraveling the false positive and identifying top 10 words of each subreddit. Hence, we are able to provide early detection of potential depression cases along with identify existing cases. We can then look to get them the help they need. The target audience of this project is everyone, especially those working in the psychological and healthcare departments.


## Approach

The objective of this project is to execute different binary classification algorithms/models and find the best model over several attempts. Firstly, i will clean the data do prepreocessing in preparation for the modeling process. I will also analyze the data and relationships to see what are the deciding factors related to the respective subreddits and display their distributions.

As for modeling, my initial models will be without any adjustments to hyperparameters. My second attempt will be to run the models with tuned hyperparamaters and find the most accurate model. Lastly, i will use my final model and evaluate it further to conclude.


## Data Dictionary

Data Dictionary:

subreddit(string): Subreddit Category (Depression/Forever Alone)

text(string): Post Text

title(string): Post Title

word count(integer): Word Count for Post 

text length(integer): Text Length for Post 

## Summary, Conclusions & Recommendations

This project about binary classification problem has been an interesting one yet tricky one. The goal of the project is to use Natural Language Processing (NLP) to train a classifier on which subreddit a given post came from. In this case it would be to come up with a model that can best effecfively classify if a post in a subreddit is from the Depression or Forever Alone subreddit based on the post text.

Through several testing and iterations, i have chosen to go with the Multinomial Naive Bayes model equipped with the TFIDF Vectorizor based on test results in comparison with the other models like Logistic Regression, K Nearest Neighbours and Random Forest. With consistently higher scores and low variance, the model manage to produce a 83% accuracy which is 33% higher of the baseline accuracy of 51%.

This results may not be the best but the model could be pretty useful and applicable in real situations. It could be a key factor in early detection of depression based on (1) correct classification of a post in the Depression subreddit and (2) words used by a user in his/her post. I hope this model can be meaningful to the public and those in psychological in detecing and helping those in need.

With regards to future work, given more time, i would like to optimise the model. I ought to explore the effects on other features like word count/length and title words to see how i can come up with a better and more accurate model to classify a post. This features could be useful in affecting the mix in the model as the initial model was purely using the post texts as a variable along with some feature engineering.


## References

Understanding and Recognizing the Warning Signs of Depression. Extracted from:
https://www.betterhelp.com/advice/depression/understanding-and-recognizing-the-warning-signs-of-depression/?utm_source=AdWords&utm_medium=Search_PPC_c&utm_term=_b&utm_content=118051369567&network=g&placement=&target=&matchtype=b&utm_campaign=11771068538&ad_type=text&adposition=&gclid=CjwKCAjwmv-DBhAMEiwA7xYrdwe5XC2X0TTz_J-Ek9Bngmh3gUgLg6e7kkPokzPMHVk8N5jak5jCthoCEa8QAvD_BwE

Depression subreddit. Extracted from: https://www.reddit.com/r/depression/

Forever Alone subreddits. Extracted from: https://www.reddit.com/r/ForeverAlone/comments/muj5p8/i_know_i_will_be_forever_alone/

Confusion Matrix Machine Learning. Extracted from: https://www.analyticsvidhya.com/blog/2020/04/confusion-matrix-machine-learning/
