About the project:
Social Media Platforms are filled with mean comments which disturb the decorum of the platform. To tackle this problem we have built an ML model which can detect
and classify Toxic sentences into 6 different categories i.e Toxic, Severe_toxic, obscene, threat, insult, Identity hate.

Dataset:
The data set used is taken from kaggle as part of the toxicity classification challenge, the training dataset contains nearly 160k sentences out of which 16225 sentences
are negative ones.
The testing dataset used was also from kaggle which has around 153k sentences.

Preprocessing:
As the data is text based, we have to go through a number of preprocessing steps to clean the data.
1. Removing html tags, hyper links, punctuations.
2. correcting commonly misspelled words.
3. Mapping contractions into original words, eg: Don't -> do not
4. Removing stop words such as "is", "the:, "an", "then" etc
5. Vectorizing the sentence using TFID Vectorizer

Model:
We have used logistic regression using OneVsRest classifier.
The reason to use this is to be able to independently classify each target value.

Score:
The model was tested using AUC ROC metric, which yielded a score of 0.97285 on kaggle.