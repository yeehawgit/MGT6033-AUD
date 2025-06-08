# Answer Key

## Section 1: Using Pre-trained Word2Vec Models

1. **Correct Answer:** B  
**Explanation:** The demo uses gensim for Word2Vec models.  
**Verbatim Quote:** "In python, the best implementation of Word2Vec is through an NLP packaged called gensim..." (4C-Word2Vec.pdf)

2. **Correct Answers:** A, B, C  
**Explanation:** The model is case-sensitive, uses 300 dimensions, and includes bigrams and misspellings.  
**Verbatim Quote:** "We can see that these vectors are 'cased'... this model represents words in 300-dimensional space... it allowed for bigrams and some misspellings." (4C-Word2Vec.pdf)

3. **Correct Answer:** B  
**Explanation:** `most_similar()` returns a list of the most similar words and their similarity scores.  
**Verbatim Quote:** "what words are most similar to 'president'? ... [('President', 0.8006), ...]" (4C-Word2Vec.pdf)

4. **Correct Answers:** A, B, D  
**Explanation:** Case sensitivity allows distinguishing proper nouns, learning context, and capturing usage.  
**Verbatim Quote:** "With sufficient data this is good practice since 'President ...' likely refers to something different than 'the president of company X.'" (4C-Word2Vec.pdf)

5. **Correct Answer:** D  
**Explanation:** The vectors are 300-dimensional.  
**Verbatim Quote:** "The shape (300) matches the label of the word2vec model we downloaded..." (4C-Word2Vec.pdf)

## Section 2: Incorporating Embeddings into a Document-Term Matrix

6. **Correct Answer:** B  
**Explanation:** Multiplying the DTM by the embedding matrix projects documents into the embedding space.  
**Verbatim Quote:** "The final step is actually very easy, as we can use linear algebra to combine these two matrices." (4_DemoC4-Convert-DTM-to-Word2Vec-Space.txt)

7. **Correct Answers:** A, B, C  
**Explanation:** The preprocessing excludes stopwords, requires all letters, and at least 3 characters.  
**Verbatim Quote:** "I'm going to exclude English stop words and require tokens to be all letters (to get rid of numbers) and at least 3 characters." (4C-Word2Vec.pdf)

8. **Correct Answer:** B  
**Explanation:** The resulting shape is (2000, 300).  
**Verbatim Quote:** "dtm.shape ... (2000,500)... word_vectors.shape ... (500,300)... dtm_w2v.shape ... (2000, 300)" (4C-Word2Vec.pdf)

9. **Correct Answers:** A, B, C  
**Explanation:** Normalization ensures unit length, corrects for document length, and enables meaningful cosine similarity.  
**Verbatim Quote:** "We can correct this by 'norming' the output matrix such that each element has unit length... This is effectively the same as scaling by length." (4_DemoC4-Convert-DTM-to-Word2Vec-Space.txt)

10. **Correct Answer:** B  
**Explanation:** High similarity means the document is semantically similar to the word.  
**Verbatim Quote:** "The more similar it is to a given word, the higher the likelihood that earning's announcement is talking about whatever word it is..." (4_DemoC4-Convert-DTM-to-Word2Vec-Space.txt)

## Section 3: Custom Word2Vec Model Training

11. **Correct Answer:** B  
**Explanation:** gensim Word2Vec expects a list of lists (sentences of tokens).  
**Verbatim Quote:** "Model training requires a list of lists, where each element of the outer list is a sentence, and each element of the inner list is a token." (4C-Word2Vec.pdf)

12. **Correct Answers:** A, B, C, D  
**Explanation:** The function removes stopwords, skips short/long sentences, requires alphabetic tokens, and keeps acronyms case-sensitive.  
**Verbatim Quote:** "if len(words) <= 3 or len(words) >= 50: ... if word.lower() in stopwords: ... elif not word.isalpha(): ... elif len(word)<3: ... elif word.upper()==word: ... good_tokens.append(word) ..." (4C-Word2Vec.pdf)

13. **Correct Answer:** A  
**Explanation:** Flattening loses the ability to tie sentences back to documents.  
**Verbatim Quote:** "I'm going to lose my ability to tie back to the raw data if I remove that outer layer... but that's okay because all I'm doing here is training a model." (4_DemoC6-Model-Training.txt)

14. **Correct Answers:** A, C, D  
**Explanation:** The default is CBOW, with default parameters, and no forced lowercasing.  
**Verbatim Quote:** "The default is the continuous bag of words, so that's what we're going to be running... I'm going to leave all of the default parameters for Word2Vec as-is..." (4_DemoC6-Model-Training.txt)

15. **Correct Answer:** B  
**Explanation:** Custom models capture domain-specific usage and relationships.  
**Verbatim Quote:** "Even with only 2,000 earnings announcements it appears that our custom model does a much better job of picking up nuances of financial language." (4C-Word2Vec.pdf)
