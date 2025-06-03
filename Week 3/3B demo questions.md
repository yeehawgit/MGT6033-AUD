# Quiz Questions

## Section 1: Loading, Preparing, and Representing a Corpus

1. **(Easy)** What is the primary purpose of using scikit-learn's `CountVectorizer` in this module?  
A. To summarize the text with one number  
B. To build a document-term matrix from a corpus  
C. To generate random words  
D. To translate reviews between languages  

2. **(Medium) Select all that apply:** What preprocessing steps are handled or can be customized in `CountVectorizer`?  
A. Lemmatization  
B. Removing stop words  
C. Minimum document frequency filtering  
D. Custom tokenization  

3. **(Medium)** What is the default output format of `CountVectorizer`?  
A. A pandas DataFrame  
B. A dense NumPy matrix  
C. A Compressed Sparse Row (CSR) sparse matrix  
D. A list of dictionaries  

4. **(Medium) Select all that apply:** Why are sparse matrices preferred for storing document-term matrices in NLP?  
A. They save memory  
B. They allow faster access to rows and columns  
C. Most matrix values are zero  
D. They can store more diverse data types than dense matrices  

5. **(Hard)** What does the method `get_feature_names_out()` return after fitting a `CountVectorizer`?  
A. Row indices of the matrix  
B. The list of token (word) column names in order  
C. A dictionary mapping words to review ratings  
D. The sentences of the original text  

## Section 2: Building the DTM: Hard Way vs Easy Way

6. **(Medium) Select all that apply:** According to the demo, what filtering steps does the "hard way" tokenization function apply?  
A. Remove non-alphabetic tokens  
B. Remove stop words  
C. Convert tokens to lowercase  
D. Lemmatize tokens  

7. **(Hard)** In the "easy way" with `CountVectorizer`, what do the `min_df` and `max_df` parameters control?  
A. The minimum/maximum allowed frequency for words to be included as columns  
B. The number of rows in the DTM  
C. The minimum/maximum number of tokens per sentence  
D. The maximum allowed length of reviews  

8. **(Medium)** What is the “bag of words” representation?  
A. A model that uses sentence structure and grammar  
B. Counting each unique word in a document while ignoring order  
C. Counting only verbs in each document  
D. A matrix of word embeddings  

9. **(Hard)** Why does the number of columns in the DTM decrease when you increase `min_df`?  
A. It only keeps words that occur in at least `min_df` documents, removing rarer words  
B. It merges similar words  
C. It excludes all punctuation  
D. It ignores stop words by default  

10. **(Hard) Select all that apply:** After using a custom tokenizer with `CountVectorizer`, which of the following might still require manual adjustment?  
A. Lemmatization  
B. Removal of short tokens  
C. Elimination of numbers  
D. Handling of rare words (below min_df)  

## Section 3: Dictionary-Based Sentiment Analysis

11. **(Easy)** What is the main idea behind using a sentiment dictionary for analysis?  
A. Assigning a score or label based on the occurrence of positive/negative words  
B. Generating new reviews  
C. Removing all adjectives  
D. Counting the number of sentences only  

12. **(Medium) Select all that apply:** According to the demo, what categories does the Harvard General Inquirer Dictionary provide?  
A. Positive words  
B. Negative words  
C. Product IDs  
D. Multiple information categories per word  

13. **(Hard) Select all that apply:** What steps are needed to use the General Inquirer sentiment dictionary in a pandas workflow?  
A. Read the Excel file with `read_excel`  
B. Filter rows for positive/negative categories  
C. Split on hashes and convert tokens to lowercase  
D. Convert imported columns to string type  

14. **(Hard)** Why do some words in the sentiment dictionary appear as `"ACCORD#2"` or similar variants?  
A. They are synonyms from different languages  
B. They represent the same root word in multiple categories or meanings  
C. They are always stop words  
D. They are specific to Amazon reviews  

15. **(Hard)** What is the recommended measure for calculating review "tone" in the document-term matrix?  
A. Sum of all word counts  
B. (Positive - Negative) / (Total words)  
C. Number of sentences  
D. Product rating  

## Section 4: Pattern-Based & TextBlob Sentiment Analysis

16. **(Medium) Select all that apply:** What are features of pattern-based approaches (e.g., TextBlob) to sentiment analysis?  
A. They account for contextual modifiers like "not"  
B. They require passage-level input  
C. They measure polarity and subjectivity  
D. They only support dictionary matches  

17. **(Medium)** How does the "subjectivity" score from TextBlob differ from the "polarity" score?  
A. Subjectivity measures opinion/fact, polarity measures positive/negative  
B. Subjectivity is always 1  
C. Polarity is always negative  
D. They are computed the same way  

18. **(Hard)** How does the subjectivity-weighted polarity adjust the sentiment score from TextBlob?  
A. Polarity is multiplied by (1 - subjectivity) to down-weight highly subjective passages  
B. Subjectivity is ignored for all calculations  
C. The result is always 0 or 1  
D. Only negative polarity is weighted  

19. **(Medium)** Why did Robbie convert the tuple output from a custom TextBlob function to columns in the DataFrame?  
A. To facilitate correlation and further analysis  
B. To enable merging results with review texts  
C. To avoid redundancy  
D. To count the most common words  

20. **(Medium) Select all that apply:** Which of the following are recommended as additional steps after calculating sentiment or similarity scores?  
A. Always check your data with `.head()` for a visual check 
B. Investigate the actual review text for extreme values  
C. Merge indices to make results interpretable  
D. Ignore any NaN or missing results

