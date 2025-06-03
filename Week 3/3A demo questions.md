# Quiz Questions

## Section 1: Loading and Tokenizing Text

1. **(Easy)** Which Python method is commonly used to split a string into tokens based on whitespace?  
A. split()  
B. partition()  
C. find()  
D. groupby()  

2. **(Medium) Select all that apply:** Which of the following statements about using `word_tokenize` from NLTK are true?  
A. Handles punctuation more accurately than basic split  
B. Returns a list of tokens  
C. Must always be used on lowercase strings  
D. Converts numeric values to words by default

3. **(Medium)** What is the main reason to filter out stop words when analyzing tokenized text?  
A. To increase the number of tokens  
B. To remove semantically low-value words that are very common  
C. To preserve proper nouns  
D. To make all tokens lowercase

4. **(Hard) Select all that apply:** When processing text for NLP, what are important steps before analysis?  
A. Tokenization  
B. Lemmatization or stemming  
C. Removing stop words  
D. Sorting tokens alphabetically

## Section 2: Stemming vs. Lemmatization

5. **(Medium)** What attribute of a spaCy token object returns the lemma (root form) of a word?  
A. .stem_
B. .lemma_
C. .root_
D. .text_

6. **(Hard)** Why might the lemma of a word appear identical to its original text in a preprocessed file?  
A. The file has already been lemmatized  
B. The word is a stop word  
C. Stemming was used instead of lemmatization  
D. All spaCy Doc objects return the same value for text and lemma

7. **(Hard) Select all that apply:** What differences exist between Porter and Snowball stemmers in NLTK?  
A. They may produce different stems for the same word  
B. Snowball requires you to specify the language  
C. Porter is the only one that works on adjectives  
D. Both always return valid English words

## Section 3: Sentence and Token Filtering

8. **(Medium) Select all that apply:** Why might you skip sentences with fewer than 5 tokens in preprocessing?  
A. Such sentences are often headings or non-informative  
B. They improve overall sentence readability  
C. To minimize inclusion of noise like titles or blank lines  
D. To guarantee that only questions are analyzed

9. **(Hard)** In spaCy, which attributes can be used to filter out punctuation and ensure only clean words are collected?  
A. word.is_alpha  
B. word.is_stop  
C. word.text.isdigit()  
D. word.is_title  

## Section 4: Advanced Cleaning and Inspection

10. **(Medium) Select all that apply:** According to the demo, which steps are useful for inspecting and refining a cleaned word list?  
A. Convert non-acronym words to lowercase  
B. Keep acronyms (e.g., NLP) in uppercase  
C. Use Pandas Series to count word frequency  
D. Discard proper nouns entirely

11. **(Hard)** What is a practical pandas method to examine the most frequent non-stop words in a processed corpus?  
A. groupby()  
B. value_counts()  
C. describe()  
D. get_text()  

12. **(Hard) Select all that apply:** When iterating over spaCy `sent` and `word` objects, which of the following practices are recommended for high-quality cleaning?  
A. Skip sentences that are too short  
B. Filter out non-alphabetic tokens  
C. Remove stop words  
D. Store all tokens as title-case

## Section 5: Case Sensitivity and Acronym Preservation

13. **(Hard)** In the acronym-preserving version of the cleaning loop, what check ensures a token is an acronym?  
A. word.is_upper  
B. word.is_stop  
C. word.is_title  
D. word.text.isnumeric()  

14. **(Medium) Select all that apply:** Why is it necessary to adjust for casing when tallying frequencies of non-stop words?  
A. To distinguish between singular and plural  
B. To prevent NLP acronyms from being merged with regular words  
C. To make word frequency counts case-insensitive for non-acronyms  
D. To make all data uppercase

15. **(Hard) Select all that apply:** What potential consequences might arise if you do not handle acronyms and casing correctly in frequency analysis?  
A. Acronyms may be undercounted  
B. Frequencies for "NLP" and "nlp" could be split  
C. Case-sensitive duplicates may appear in results  
D. Lemmatization will always fail

