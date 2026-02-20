## Here is a set of demo scripts to solve the problem of multiclassification.

As it is from our internal dataflow you cannot use it as is, but you may view in the idea.

The input:

Set of reels from youtube with reel and channel titles.

The target:

Set one of exist brands for reels that belongs to.

*Step 1*

Get premarked reels and either learn a model or get words-bigrams for binary classification. The aim is to get reels that could be classified by targets.

*Step 2*

Learm model (tfidf+catboost) for future classification of separated on reels. There is no class "other" here. It could be added, but it is out of this task score

*Step 3*

Get reel from the input and do binary classification with them (using data from step 1)

*Step 4*

Get reels from step 3 and make multiclassifiation (using data from step 2)

*Step 5*

Upload reels with appropiriate classification

bonus:

*Step 6*
Some tests to get words significance from tfidf+catboost model
