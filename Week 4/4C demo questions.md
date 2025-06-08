# Quiz Questions

## Section 1: Using Pre-trained Word2Vec Models

1. **(Easy)** What Python package is used in the demo to work with pre-trained Word2Vec models?  
A. nltk  
B. gensim  
C. sklearn  
D. pandas  

2. **(Medium, Select all that apply):** Which of the following are true about the Google News Word2Vec model used in the demo?  
A. It is case-sensitive  
B. It contains 300-dimensional vectors  
C. It includes bigrams and some misspellings  
D. It only includes lowercase words  

3. **(Medium)** What does the `most_similar()` method of a gensim KeyedVectors object return?  
A. The most frequent words in the corpus  
B. A list of words most similar to the input word, with similarity scores  
C. The word vector for the input word  
D. The number of times a word appears in the corpus  

4. **(Hard, Select all that apply):** Why might it be beneficial for a Word2Vec model to retain case sensitivity?  
A. It can distinguish between proper nouns and common nouns  
B. It allows the model to learn different meanings for the same word with different casing  
C. It reduces the vocabulary size  
D. It helps capture context-specific usage  

5. **(Hard)** What is the dimensionality of the word vectors in the Google News Word2Vec model?  
A. 50  
B. 100  
C. 200  
D. 300  

## Section 2: Incorporating Embeddings into a Document-Term Matrix

6. **(Medium)** What is the main purpose of multiplying a document-term matrix (DTM) by a word embedding matrix?  
A. To reduce the number of documents  
B. To project documents into the word embedding space  
C. To count the number of unique words  
D. To convert word vectors to one-hot encodings  

7. **(Medium, Select all that apply):** What preprocessing steps are applied when building the DTM for this demo?  
A. Exclude English stopwords  
B. Require tokens to be all letters  
C. Require tokens to be at least 3 characters  
D. Force all tokens to lowercase  

8. **(Hard)** What is the shape of the resulting matrix after multiplying a DTM of shape (2000, 500) by a word embedding matrix of shape (500, 300)?  
A. (500, 2000)  
B. (2000, 300)  
C. (2000, 500)  
D. (300, 2000)  

9. **(Hard, Select all that apply):** Why is normalization applied to the resulting document embedding matrix?  
A. To ensure each document vector has unit length  
B. To correct for differences in document length  
C. To make cosine similarity meaningful  
D. To remove stopwords from the matrix  

10. **(Hard)** What does a high cosine similarity between a document embedding and a word vector (e.g., "oil") indicate?  
A. The document is short  
B. The document is similar in content to the word  
C. The word is not present in the document  
D. The document is mostly stopwords  

## Section 3: Custom Word2Vec Model Training

11. **(Medium)** What data structure is required by gensim’s Word2Vec model for training?  
A. A list of strings, each representing a document  
B. A list of lists, where each inner list is a sentence of tokens  
C. A dictionary mapping words to counts  
D. A NumPy array of word frequencies  

12. **(Medium, Select all that apply):** What cleaning steps are included in the `set_up_w2v` preprocessing function?  
A. Remove stopwords  
B. Skip sentences with fewer than 4 or more than 50 words  
C. Require tokens to be alphabetic and at least 3 characters  
D. Keep acronyms case-sensitive  

13. **(Hard)** What is the effect of flattening the list of lists of lists (documents → sentences → tokens) into a list of sentences for Word2Vec training?  
A. It loses the ability to tie sentences back to documents  
B. It speeds up training  
C. It allows word order within documents to be preserved  
D. It reduces the vocabulary size  

14. **(Hard, Select all that apply):** What are the default settings when instantiating a gensim Word2Vec model as shown in the demo?  
A. Continuous Bag of Words (CBOW) architecture  
B. Skip-gram architecture  
C. Default parameter values for window size and vector size  
D. No forced lowercasing of tokens  

15. **(Hard)** What is a key advantage of training a custom Word2Vec model on a domain-specific corpus (e.g., earnings announcements)?  
A. It always outperforms pre-trained models on all tasks  
B. It captures domain-specific word usage and relationships  
C. It requires no preprocessing  
D. It produces smaller word vectors  

