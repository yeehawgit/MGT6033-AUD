# Answer Key

## Section 1: Loading, Preparing, and Representing a Corpus

1. **Correct Answer:** B  
**Explanation:** `CountVectorizer` is used to build a document-term matrix from text data.  
**Verbatim Quote:** "using scikit-learn count vectorizer to build a document term matrix"  
(*3_DemoB1_Loading_Data_Into_a_Corpus.txt*)

2. **Correct Answers:** B, C, D  
**Explanation:** CountVectorizer can handle or customize stopword removal, min/max document frequency, and tokenization. Lemmatization is not handled by default.  
**Verbatim Quote:** "Count vectorizer includes a number of very useful keyword arguments...min-df, max-df, stopwords...tokenizer...preprocessor..."  
(*3_DemoB3_The_Easy_Way.txt*)

3. **Correct Answer:** C  
**Explanation:** "dtm2 is our DTM, but it's in a very different format ... 'sparse matrix' ... very memory efficient."  
**Verbatim Quote:** "The 'sparse matrix' format refers to the fact that the vast majority of the data is zero. This is very memory efficient."  
(*Corpus-Representation-Sentiment-Analysis-3B.pdf*)

4. **Correct Answers:** A, C  
**Explanation:** Sparse matrices are memory-efficient because most entries are zero.  
**Verbatim Quote:** "The sparse matrix format refers to the fact that the vast majority of the data is one value -- 0. This is very memory efficient."  
(*Corpus-Representation-Sentiment-Analysis-3B.pdf*)

5. **Correct Answer:** B  
**Explanation:** `get_feature_names_out()` returns the list of column names from the vocabulary, corresponding to tokens.  
**Verbatim Quote:** "we can get a list of feature names with get_feature_names_out()"  
(*Corpus-Representation-Sentiment-Analysis-3B.pdf*)

## Section 2: Building the DTM: Hard Way vs Easy Way

6. **Correct Answers:** A, B, C, D  
**Explanation:** The custom function for the “hard way” applies all these steps for cleaning to get quality tokens for the DTM.  
**Verbatim Quote:** "I'm going to write a function that accepts a string of text and returns a list of lemmatized words...filter the non-alpha...skip stop words...convert to lowercase..."  
(*3_DemoB2_Building_A_Document_Term_Matrix_The_Hard_Way.txt*)

7. **Correct Answer:** A  
**Explanation:** These parameters specify how common or rare a word must be to be included in the DTM.  
**Verbatim Quote:** "min-df and max-df...specifies the minimum (or maximum) number or proportion of documents a word must appear in to be included in the DTM."  
(*3_DemoB3_The_Easy_Way.txt*)

8. **Correct Answer:** B  
**Explanation:** Bag of words counts each unique word, ignoring order or syntax.  
**Verbatim Quote:** "Bag of words simply says, we're ignoring sentence structure, we're ignoring direct objects and grammar, and we're just looking at simple word counts."  
(*3_DemoB2_Building_A_Document_Term_Matrix_The_Hard_Way.txt*)

9. **Correct Answer:** A  
**Explanation:** Increasing `min_df` removes rare words; only those in at least `min_df` documents are kept as columns.  
**Verbatim Quote:** "we require words to be in at least two documents. That's the major difference."  
(*3_DemoB3_The_Easy_Way.txt*)

10. **Correct Answers:** A, B, C  
**Explanation:** Lemmatization, removal of very short tokens, and filtering numbers may require manual work even with a custom tokenizer.  
**Verbatim Quote:** "We haven't lemmatized...not restricted based on token length...includes numeric tokens..."  
(*Corpus-Representation-Sentiment-Analysis-3B.pdf*)

## Section 3: Dictionary-Based Sentiment Analysis

11. **Correct Answer:** A  
**Explanation:** Dictionary-based sentiment assigns a tone or score based on the presence of positive/negative words.  
**Verbatim Quote:** "One approach to measuring sentiment is by looking for specific terms that likely indicate the construct we are trying to measure (or its opposite)."  
(*Corpus-Representation-Sentiment-Analysis-3B.pdf*)

12. **Correct Answers:** A, B, D  
**Explanation:** The dictionary includes positive, negative, and "many categories of information" per word.  
**Verbatim Quote:** "...contains many categories of information...We'll focus on positive (Positiv) and Negative (Negativ) words..."  
(*Corpus-Representation-Sentiment-Analysis-3B.pdf*)

13. **Correct Answers:** A, B, C, D  
**Explanation:** All these steps are described as necessary when working with this Excel-based dictionary.  
**Verbatim Quote:** "You have a copy available...grab positive words...split on number sign...convert to lowercase...cast to a string."  
(*3_DemoB5_Sentiment_Analysis_Building_A_Dictionary.txt*)

14. **Correct Answer:** B  
**Explanation:** Multiple variants (e.g., "ACCORD#2") represent the same root in different contexts or dictionary entries.  
**Verbatim Quote:** "...what it means is you might have ... ACCORD#2, ACCORD#3 ... for various reasons those words appear multiple times."  
(*3_DemoB5_Sentiment_Analysis_Building_A_Dictionary.txt*)

15. **Correct Answer:** B  
**Explanation:** The recommended sentiment formula is (positive - negative) / total words.  
**Verbatim Quote:** "...subtract the sum of negative words from the sum of positive words and divide by total words."  
(*3_DemoB5_Sentiment_Analysis_Building_A_Dictionary.txt*)

## Section 4: Pattern-Based & TextBlob Sentiment Analysis

16. **Correct Answers:** A, B, C  
**Explanation:** Pattern-based sentiment (e.g., TextBlob) accounts for context and outputs both polarity and subjectivity at the passage level.  
**Verbatim Quote:** "...pattern based approach combines elements of a dictionary based approach with some syntactic and grammatical adjustments... measure polarity and subjectivity..."  
(*3_DemoB6_Sentiment_Analysis_Pattern-Based_Approach.txt*)

17. **Correct Answer:** A  
**Explanation:** Subjectivity measures opinion/fact; polarity measures positivity/negativity.  
**Verbatim Quote:** "Subjectivity is exactly what it sounds like, does the procedure think this is more opinion or more factual? Polarity ... is what we generally think of as tone..."  
(*3_DemoB6_Sentiment_Analysis_Pattern-Based_Approach.txt*)

18. **Correct Answer:** A  
**Explanation:** Weighted polarity = polarity * (1 - subjectivity), down-weighting subjective passages.  
**Verbatim Quote:** "I'm just going to multiply polarity by one minus subjectivity."  
(*3_DemoB6_Sentiment_Analysis_Pattern-Based_Approach.txt*)

19. **Correct Answer:** A  
**Explanation:** Converting tuple output to columns allows correlation and further analysis, like regression.  
**Verbatim Quote:** "I'd like to have those as columns in my original DataFrame...to facilitate analysis."  
(*3_DemoB6_Sentiment_Analysis_Pattern-Based_Approach.txt*)

20. **Correct Answers:** A, B, C  
**Explanation:** Visual checks, reviewing actual reviews, and merging indices to interpret results are all recommended for NLP analyses.  
**Verbatim Quote:** "Always check your data. ...use .head()...see what you get. ...use merging to interpret which review matches."  
(*3_DemoB7_Measuring_Similarity.txt*)
