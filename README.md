# Sentiment-Analysis-NLP 

## Objective:
Classifying IMDb Movie Reviews by exploring Natural Language Processing and Sentiment Analysis to predict the number of positive and negative reviews using various algorithm models.

## Data-Set
This is a Large Movie Review Dataset for binary sentiment classification. Find it [HERE!](http://ai.stanford.edu/~amaas/data/sentiment/)

The data is split evenly with 25k reviews intended for training and 25k for testing your classifier. Moreover, each set has 12.5k positive and 12.5k negative reviews.

## Unpacking and merging the datafile:

1. Move the tar file to the directory where you want this data to be stored.
2. Open a terminal window and cd to the directory that you put aclImdb_v1.tar.gz in.
3. gunzip -c aclImdb_v1.tar.gz | tar xopf -
4. cd aclImdb && mkdir movie_data
5. for split in train test; do for sentiment in pos neg; do for file in $split/$sentiment/*; do cat $file >> movie_data/full_${split}.txt; echo >> movie_data/full_${split}.txt; done; done; done;

## Analysis
- Text Processing: Stemming/Lemmatizing to convert different forms of each word into one.
- n-grams: Instead of just single-word tokens (1-gram/unigram),word pairs were included.
- Representations: Instead of simple, binary vectors, word counts or TF-IDF was chosen to transform those counts.
- Algorithms: In addition to Logistic Regression, Support Vector Machines was used.