# Quiz Questions

## Section 1: Data Preparation and Feature Extraction

1. **(Easy)** What is the primary text field used for topic modeling in the CFPB complaints dataset?  
A. company  
B. complaint_what_happened  
C. product  
D. issue  

2. **(Medium) Select all that apply:** Which preprocessing steps are applied before generating the document-term matrix for LDA?  
A. Remove stopwords  
B. Remove dates and anonymized tokens (e.g., XXXX)  
C. Only include tokens with at least 3 letters  
D. Allow both unigrams and bigrams  
E. Use TF-IDF weighting  

3. **(Medium)** Why is it important to use a count-based (integer) document-term matrix for LDA in sklearn?  
A. LDA requires integer word counts for probabilistic modeling  
B. LDA can only use binary input  
C. LDA works best with TF-IDF  
D. LDA requires normalized data  

4. **(Hard) Select all that apply:** What does the `CountVectorizer` parameter `ngram_range=(1,2)` accomplish?  
A. Includes both single words and two-word phrases as features  
B. Removes all bigrams  
C. Limits features to only bigrams  
D. Allows the model to capture more context  

5. **(Hard)** Why is the vocabulary converted to a NumPy array before extracting top words for each topic?  
A. NumPy has better methods for NLP  
B. To remove duplicates  
C. To allow fast indexing and subset selection  
D. To convert words to numbers  

## Section 2: LDA Model Fitting and Output Interpretation

6. **(Easy)** What does the `n_components` parameter control in sklearn’s LDA model?  
A. Number of documents  
B. Number of topics  
C. Number of words  
D. Number of features per topic  

7. **(Medium) Select all that apply:** What are the roles of `doc_topic_prior` (alpha) and `topic_word_prior` (beta) in LDA?  
A. Control topic distribution per document  
B. Control word distribution per topic  
C. Are Dirichlet priors  
D. Always set to zero  

8. **(Medium)** After fitting LDA, what does each row in the `doc_topics` matrix represent?  
A. The word counts for a document  
B. The counts of topics for a document  
C. The most common topic in the corpus  
D. The probability distribution of topics for a document  

9. **(Hard) Select all that apply:** Why might you threshold topic probabilities (e.g., at 0.10) when analyzing LDA output?  
A. To convert probabilities to binary topic presence  
B. To identify which topics are “relevant” in each document  
C. To reduce noise in downstream analyses  
D. To guarantee each document has only one topic  

10. **(Hard)** What is a typical average number of topics per document in the CFPB complaints sample when using a 0.10 threshold?  
A. 1  
B. 2  
C. 1.5  
D. 10  

## Section 3: Topic-Word Matrix and Topic Interpretation

11. **(Easy)** What is the shape of the topic-word matrix (`lda.components_`) if you fit 100 topics with 1,000 features?  
A. (1000, 100)  
B. (100, 1000)  
C. (10, 100)  
D. (100, 10)  

12. **(Medium) Select all that apply:** According to the demo, steps are involved when selecting the top words for a given topic from the topic-word matrix?  
A. Select the first 10 columns  
B. Use `argsort` to find indices of highest values in the topic’s row  
C. Use only words with zero counts  
D. Map indices to words using the vocabulary array  

13. **(Medium)** Why is the topic-word matrix not probabilistic (i.e., rows do not sum to 1)?  
A. It contains unnormalized word relevance scores  
B. It is normalized by document length  
C. It is a binary matrix  
D. It is not used for interpretation  

14. **(Hard) Select all that apply:** What are signs of a coherent topic when inspecting its top words?  
A. Words are semantically related  
B. Words reflect a clear theme  
C. Words are generic or unrelated  
D. Words appear frequently together in the corpus  

15. **(Easy)** What does `[::-1]` do in the following function from the demo? 
```
def get_topic_words(topic,top_word,vocab,topn=10):
    top_words = top_word[topic,:].argsort()[-topn:][::-1].tolist()
    return vocab[top_words]
```
A. It gives you the top word of the list  
B. It selects the last word of the list  
C. It removes the last word of the list  
D. It reverses the list order  

## Section 4: Model Evaluation and Tuning

16. **(Hard)** What does the perplexity score measure in LDA models?  
A. Accuracy of the topics  
B. Average similarity between each cluster and its most similar cluster  
C. Model complexity and fit  
D. Ratio of between cluster dispersion vs within cluster dispersion  

17. **(Medium) Select all that apply:** What are limitations of using perplexity for LDA model selection in sklearn?  
A. Perplexity may not be reliable due to implementation bugs  
B. Perplexity is not always interpretable  
C. Perplexity alone is insufficient for topic quality  
D. Perplexity always decreases with more topics  

18. **(Medium)** In the code below from the demo, what does the `u_mass` coherence score evaluate?  
```
umass = metric_coherence_gensim(measure = "u_mass",
                        top_n = 5,
                        topic_word_distrib = top_word,
                        dtm = dtm.todense(),
                        vocab = vocab,
                        texts = None)
```
A. The likelihood that top words in a topic co-occur in the corpus  
B. The distance between words  
C. The Calinski-Harabasz (CH) index  
D. The number of unique words  

19. **(Hard) Select all that apply:** Which strategies are recommended for tuning LDA models?  
A. Vary number of topics and evaluate metrics  
B. Use GridSearchCV or RandomizedSearchCV for parameter tuning  
C. Run a model multiple times on the same parameters and average the results  
D. Consider both model-level and topic-level metrics  

20. **(Hard) Select all that apply:** What is a key difference between LDA and NMF models in sklearn?  
A. LDA is probabilistic; NMF is not  
B. NMF requires scaling document-topic matrix before thresholding  
C. NMF requires integer counts    
D. Both always produce identical topics  

---

