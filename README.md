# TASK 2 : Getting the Top Keywords.

## Approach:
First the text is going to be normalized through the next steps:
1. Bringing to lower case.
2. Bringing unicode characters to ascii.
3. Removing the stopwords from the text.

The next step is going to be the search of hapaxes, and their removing from text.
The hapaxes are extracted to reduce the time of computing the ranking topics by eliminating the need of calculating them for extremely rare words.

NOTE: Aditionaly It may be used some stemming or lemantization of words, but for this task I decided to skipp this step.

Then different algorithms or metrics are aplied to the corpus to rank words.

## Definition of the Top.
The Definition of the Top highly depends on the task, but some initial asumptions can be made.
1. The Statistical metrics - the simplest frequency of words in the corpus can say a lot about the words. However, the top words are not the most frequent ones not the rarest ones, but the ones that are somewhere in the middle.
An example of this is TF-IDF method, which gives high weights to the rarest words, because they can become crucial for classification.
   
2. RAKE (Rapid Automatic Keyword Extraction) - is also a statistical method of analysing word frequency. However, this  it takes into acount the context of words, so the words that are getting more often in context with other words, should be more important.
3. Based on the Coocurence matrix between words and some classes. In such a way it may informative to find out words that may help differentiate between different classes.

## Top 10 words by TF-IDS.
1. milion
2. ai
3. new
4. game
5. google
6. raises
7. vr
8. launches
9. microsoft
10. games.

### The plot is in the Jupyter notebook file.

## What is also possible to try:

Personally I would try more ranking and scoring algorithms like:
1. TextRank.
2. Conditional Random Fields (CRF).
3. MAUI (Multipurpose automatic topic indexing).
4. Also it is possible to find the clusters the words vector represantation from models like GloVe or Bert, and find top x words that have the smallest distance to the centroids.
5. KEA (Keyphrase extraction algorithm) developed by Frank et al.
6. KPSotter.
