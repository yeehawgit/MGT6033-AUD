# Answer Key

## Section 1: Loading and Inspecting News Data

1. **Correct Answer:** B  
**Explanation:** The demo uses pandas to load the CSV file.  
**Verbatim Quote:** "import pandas as pd  
news = pd.read_csv('./articles2.csv')" (NER-3C.pdf)

2. **Correct Answer:** B  
**Explanation:** `head()` shows the first five rows for quick inspection.  
**Verbatim Quote:** "news.head() ... displays the first five rows of the DataFrame." (NER-3C.pdf)

3. **Correct Answers:** A, B, C  
**Explanation:** The DataFrame includes 'title', 'author', and 'date' columns.  
**Verbatim Quote:** "id | title | publication | author | date | year | month" (NER-3C.pdf)

4. **Correct Answer:** C  
**Explanation:** `news['title']` returns a pandas Series of all article titles.  
**Verbatim Quote:** "news['title'] ... gives you a pandas Series of the titles." (NER-3C.pdf)

5. **Correct Answer:** A  
**Explanation:** Ensuring correct types is necessary for downstream NLP tasks.  
**Verbatim Quote:** "It's good practice to check data types before processing." (NER-3C.pdf)

## Section 2: Named Entity Recognition with spaCy

6. **Correct Answer:** B  
**Explanation:** NER is Named Entity Recognition.  
**Verbatim Quote:** "Named Entity Recognition" (NER-3C.pdf)

7. **Correct Answers:** A, B  
**Explanation:** You must load the model and process the text with it.  
**Verbatim Quote:** "Load the spaCy model, then pass the text through it." (NER-3C.pdf)

8. **Correct Answer:** B  
**Explanation:** Processing text with spaCy returns a Doc object.  
**Verbatim Quote:** "nlp(title) returns a spaCy Doc object." (NER-3C.pdf)

9. **Correct Answers:** A, D  
**Explanation:** Entities are in `.ents`, and each entity has `.text` and `.label_`.  
**Verbatim Quote:** "for ent in doc.ents: print(ent.text, ent.label_)" (NER-3C.pdf)

10. **Correct Answer:** B  
**Explanation:** Iterating over `doc.ents` yields named entities and their labels.  
**Verbatim Quote:** "doc.ents gives you named entities and their labels." (NER-3C.pdf)

## Section 3: Interpreting and Using NER Output

11. **Correct Answer:** B  
**Explanation:** "ORG" stands for organization.  
**Verbatim Quote:** "ORG: Companies, agencies, institutions, etc." (NER-3C.pdf)

12. **Correct Answers:** A, B, C  
**Explanation:** PERSON, GPE (location), and PRODUCT are standard; COLOR is not.  
**Verbatim Quote:** "Standard entity types: PERSON, GPE, PRODUCT..." (NER-3C.pdf)

13. **Correct Answer:** A  
**Explanation:** "Apple" is likely labeled ORG, "iPhone" as PRODUCT.  
**Verbatim Quote:** "Apple – ORG, iPhone – PRODUCT" (NER-3C.pdf)

14. **Correct Answer:** A  
**Explanation:** Different models are trained on different data and vocabularies.  
**Verbatim Quote:** "Different models may yield different results due to training data and vocabulary." (NER-3C.pdf)

15. **Correct Answers:** A, B, D  
**Explanation:** NER output can be used for trend analysis, filtering, and frequency counts.  
**Verbatim Quote:** "NER can help you identify trends, filter by entity, and count entity types in articles." (NER-3C.pdf)
