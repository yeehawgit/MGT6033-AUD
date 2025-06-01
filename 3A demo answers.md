# Answer Key

## Section 1: Loading and Tokenizing Text

1. **Correct Answer:** A  
**Explanation:** The `split()` method breaks up strings by whitespace by default.  
**Verbatim Quote:** "The simplest way to tokenize is simply to split the document on spaces: toks = contents.split(' ')" (3_DemoA1_Loading_Text_From_A_Local_File.txt)

2. **Correct Answers:** A, B  
**Explanation:** `word_tokenize` handles punctuation and returns tokens as a list.  
**Verbatim Quote:** "Let's see how to use both of these packages to tokenize text. We will start with nltk... 'word_tokenize(contents)'." (3_DemoA1_Loading_Text_From_A_Local_File.txt)

3. **Correct Answer:** B  
**Explanation:** Removing stop words eliminates frequent, low-value words.  
**Verbatim Quote:** "Now for most analyses, we want to exclude stopwords. ... filter these out." (3_DemoA1_Loading_Text_From_A_Local_File.txt)

4. **Correct Answers:** A, B, C  
**Explanation:** Tokenization, normalization via stemming/lemmatization, and removing stop words are standard cleaning steps.  
**Verbatim Quote:** Objectives: "...tokenizing documents, removing stopwords from documents. And then finally converting tokens to stems or lemmas." (3_DemoA1_Loading_Text_From_A_Local_File.txt)

## Section 2: Stemming vs. Lemmatization

5. **Correct Answer:** B  
**Explanation:** `.lemma_` is the spaCy token attribute for lemmatization.  
**Verbatim Quote:** "here is how we might access the token text, lemma, and part of speech: ... print(f'Word: {tok.text}\tLemma: {tok.lemma_}')" (3_DemoA2_Stemming_vs_Lemmatizing.txt)

6. **Correct Answer:** A  
**Explanation:** The lemma is identical if the file is already lemmatized.  
**Verbatim Quote:** "You may notice that the word and lemmas always match. This is because I had already lemmatized this text." (3_DemoA2_Stemming_vs_Lemmatizing.txt)

7. **Correct Answers:** A, B  
**Explanation:** Porter and Snowball may give different stems; Snowball requires a language argument.  
**Verbatim Quote:** "Porter stemmer ... snowball stemmer requires us to specify what language... you can see how the two stemmers adjust this text." (3_DemoA2_Stemming_vs_Lemmatizing.txt)

## Section 3: Sentence and Token Filtering

8. **Correct Answers:** A, C  
**Explanation:** Short sentences are likely headings/blanks and can be skipped to eliminate noise.  
**Verbatim Quote:** "Sometimes I assume those short sentences are like headings that I want to leave out." (3_DemoA4_Cleaning_Text_and_Counting_Words.txt)

9. **Correct Answer:** A  
**Explanation:** `word.is_alpha` filters to only alphabetic tokens, removing punctuation.  
**Verbatim Quote:** "what I'm going to do now is require individual words to be at least two characters and alphabetic... word.is_alpha" (3_DemoA4_Cleaning_Text_and_Counting_Words.txt)

## Section 4: Advanced Cleaning and Inspection

10. **Correct Answers:** A, B, C  
**Explanation:** The demo makes all non-acronym tokens lowercase, keeps acronyms uppercase, and uses Pandas to count word frequencies.  
**Verbatim Quote:** "make everything case insensitive except for acronyms. ... Pandas ... value_counts()." (3_DemoA5_Inspecting_Results.txt)

11. **Correct Answer:** B  
**Explanation:** `value_counts()` is the Pandas method for frequency analysis.  
**Verbatim Quote:** "I'm going to use pandas... words_series.value_counts().head(10)" (3_DemoA5_Inspecting_Results.txt)

12. **Correct Answers:** A, B, C  
**Explanation:** Recommended for quality cleaning: skip short sentences, filter non-alphabetic, and remove stop words.  
**Verbatim Quote:** "I've added those filters. ... word to be at least two characters, and I want the word to be alpha. ... filter out stop words." (3_DemoA4_Cleaning_Text_and_Counting_Words.txt)

## Section 5: Case Sensitivity and Acronym Preservation

13. **Correct Answer:** A  
**Explanation:** `word.is_upper` checks for acronyms (all uppercase).  
**Verbatim Quote:** "if word.is_upper: words.append(word.text) # don't lemmatize acronyms" (3_DemoA5_Inspecting_Results.txt)

14. **Correct Answers:** B, C  
**Explanation:** Adjusting for casing avoids merging acronyms with regular words and enables meaningful frequency counts.  
**Verbatim Quote:** "make everything case insensitive except for acronyms (like NLP). That is, build a list of words that are all lower case with the exception of acronyms." (3_DemoA5_Inspecting_Results.txt)

15. **Correct Answers:** A, B, C  
**Explanation:** Case/pattern handling prevents undercounting acronyms, splitting frequencies, and spurious duplicates.  
**Verbatim Quote:** "NLP now appears in the top 10... if you do not handle case and acronyms, you may split frequencies." (3_DemoA5_Inspecting_Results.txt)
