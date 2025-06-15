# Answer Key

## Section 1: Data Preparation and Feature Extraction

1. **Correct Answer:** B  
Explanation: The main field for modeling is 'complaint_what_happened'.  
Verbatim Quote: “the actual text of the complaint is in 'complaint_what_happened'.” (5A-Topic-Modeling.pdf)

2. **Correct Answers:** A, B, C, D  
Explanation: All are preprocessing steps except E (TF-IDF is not used for LDA).  
Verbatim Quote: “1. Include only letters and require at least 3 characters per token... 2. Remove stop words and dates... 3. Consider bigrams or single words... 4. Retain only the 1,000 most common features.” (5A-Topic-Modeling.pdf)

3. **Correct Answer:** A  
Explanation: LDA requires integer word counts for probabilistic topic modeling.  
Verbatim Quote: “LDA Requires these integer word counts.” (5_DemoA2-Preprocessing-Feature-Extraction.txt)

4. **Correct Answers:** A, D  
Explanation: ngram_range=(1,2) includes unigrams and bigrams, capturing more context.  
Verbatim Quote: “I'm going to consider bigrams and single words here.” (5_DemoA2-Preprocessing-Feature-Extraction.txt)

5. **Correct Answer:** C  
Explanation: NumPy arrays allow fast indexing and subset selection for top words.  
Verbatim Quote: “I'm just going to convert this to a numpy array, which is why I wrap it in this numpy command.” (5_DemoA5-Exploring-Topics-with-Topic-Word-Matrix.txt)

## Section 2: LDA Model Fitting and Output Interpretation

6. **Correct Answer:** B  
Explanation: n_components sets the number of topics.  
Verbatim Quote: “The first is components. That's the most important one, that's the number of topics.” (5_DemoA3-LDA-with-sklearn.txt)

7. **Correct Answers:** A, B, C  
Explanation: Alpha and beta are Dirichlet priors controlling topic and word distributions.  
Verbatim Quote: “doc_topic_prior and topic_word_prior, those are Alpha and Beta from the slides. So those are the two DLA priors. They govern how the generative process is assumed to work.” (5_DemoA3-LDA-with-sklearn.txt)

8. **Correct Answer:** D  
Explanation: Each row is the probability distribution of topics for a document.  
Verbatim Quote: “each one of these numbers actually tells you the likelihood that the topic is in this document.” (5_DemoA4-Exploring-the-Topic-Document-Matrix.txt)

9. **Correct Answers:** A, B, C  
Explanation: Thresholding converts probabilities to binary, identifies relevant topics, and reduces noise.  
Verbatim Quote: “I'm going to set this threshold equal to 10% to 0.10... what I've done here is converted my matrix into, instead of probabilities, it's now going to be a bunch of ones and zeros.” (5_DemoA4-Exploring-the-Topic-Document-Matrix.txt)

10. **Correct Answer:** C  
Explanation: The average is about 1.5 topics per document at a 0.10 threshold.  
Verbatim Quote: “how many topics on average are there in each document? About 1.5.” (5_DemoA4-Exploring-the-Topic-Document-Matrix.txt)

## Section 3: Topic-Word Matrix and Topic Interpretation

11. **Correct Answer:** B  
Explanation: The shape is (100, 1000): 100 topics by 1000 words.  
Verbatim Quote: “we see it is 100 topics. That's the rows by 1,000 words, right?” (5_DemoA5-Exploring-Topics-with-Topic-Word-Matrix.txt)

12. **Correct Answers:** B, D  
Explanation: Use argsort to find top indices, then map to words using the vocabulary.  
Verbatim Quote: “We just have to find the largest values in each of these rows... use again, what does argsort do? ... map indices to words using the vocabulary array.” (5_DemoA5-Exploring-Topics-with-Topic-Word-Matrix.txt)

13. **Correct Answer:** A  
Explanation: The topic-word matrix contains unnormalized relevance scores, not probabilities.  
Verbatim Quote: “this is not probabilistic. Right before we had nice probabilities that sum to one, This doesn't have that same property, but higher values do indicate a greater likelihood that the word relates to a specific topic.” (5_DemoA5-Exploring-Topics-with-Topic-Word-Matrix.txt)

14. **Correct Answers:** A, B, D  
Explanation: Coherent topics have semantically related words that reflect a theme and often co-occur.  
Verbatim Quote: “the words do seem coherent or the topics seem coherent. The words seem like they belong together, which can give an indication that we're doing a reasonably good job of identifying meaningful topics.” (5_DemoA5-Exploring-Topics-with-Topic-Word-Matrix.txt)

15. **Correct Answer:** D  
Explanation: `[::-1]` reverses the order of any list. 
You should know this.

## Section 4: Model Evaluation and Tuning

16. **Correct Answer:** C  
Explanation: Perplexity measures model complexity and fit.  
Verbatim Quote: “You can access or you can estimate perplexity with the LDA model with this perplexity method.” (5_DemoA6-Evaluating-Model-Topic-Quality.txt)

17. **Correct Answers:** A, B, C  
Explanation: Perplexity in sklearn may be buggy, is not always interpretable, and is insufficient alone.  
Verbatim Quote: “there's actually a bug in psyche learns version of perplexity... it's really better to use some topic quality score intrusion task based coherence, as well as just your own intuition.” (5_DemoA6-Evaluating-Model-Topic-Quality.txt)

18. **Correct Answer:** A  
Explanation: u_mass evaluates how likely top topic words co-occur in the corpus.  
Verbatim Quote: “umass... is one of these indices that's evaluating the likelihood the words in a topic called, occur.” (5_DemoA6-Evaluating-Model-Topic-Quality.txt)

19. **Correct Answers:** A, B, D  
Explanation: Vary topics and metrics, use GridSearchCV/RandomizedSearchCV, and consider both model- and topic-level metrics.  
Verbatim Quote: “you would want to do more than just topics, which is the parameter I'm going to tune. And sklearn actually offers something called GridSearchCV, or RandomizedSearch.” (5_DemoA7-Tuning-the-Model.txt)

20. **Correct Answers:** A, B  
Explanation: LDA is probabilistic, NMF is not, and NMF requires scaling for thresholding.  
Verbatim Quote: “Now one thing that you'll notice if you get to the point that you have a document topic matrix, is this method is not probabilistic. We don't have these rows that sum to one. And so because of that, we need to do some scaling so that we can set a threshold.” (5_DemoA7-Tuning-the-Model.txt)
