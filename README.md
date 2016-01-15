# Applied Natural Language Processing

Find the categories of *questions* posted to Yahoo! Answers.

A Kaggle-based text classification task for INFO 256, UC Berkeley School of
Information.

## Goal

Classify questions into **one** of the following categories:

1. Business&Finance
2. Computers&Internet
3. Entertainment&Music
4. Family&Relationships
5. Education&Reference
6. Health
7. Science&Mathematics

## Data

Each document&mdash;a row in the data file representing a single
question&mdash;is short.

> The training data contains 2,698 questions, already labeled with one of the 
above categories. The test data contains 1,874 questions that are unlabeled.

## Methods

The data were loaded into pandas DataFrames. We removed HTML-escaped
characters, such as `&#xd;&lt;br&gt;`, using regular expressions.

We started with logistic regression and multinomial naive Bayes models.

We then used a document similarity approach, using Scikit-Learn's
`TfidfVectorizer` and `cosine_similarity` function.

Finally, we experimented with support vector classifiers.

All models were validated using cross-validation.
