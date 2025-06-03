# Quiz Questions

## Section 1: Loading and Inspecting News Data

1. **(Easy)** What Python library is used to load the news articles CSV file in the demo?  
A. collections  
B. pandas  
C. spaCy  
D. sklearn  

2. **(Medium)** What is the purpose of calling `news.head()` after loading the CSV?  
A. To show the last five rows of the DataFrame  
B. To show the first five rows of the DataFrame  
C. To count the number of articles  
D. To print column data types  

3. **(Medium) Select all that apply:** Which columns are present in the loaded news DataFrame?  
A. title  
B. author  
C. date  
D. review  

4. **(Hard)** What does `news['title']` return?  
A. A list of all article authors  
B. The DataFrame’s index  
C. A pandas Series containing all article titles  
D. The full text of each article  

5. **(Hard)** Why is it important to inspect the data types of columns in the DataFrame before processing?  
A. To ensure compatibility with NLP tools  
B. To filter out stop words  
C. To automatically lemmatize text  
D. To convert all numbers to strings  

## Section 2: Named Entity Recognition with spaCy

6. **(Easy)** What does NER stand for?  
A. Named Entity Representation   
B. Named Entity Recognition  
C. Noun Expression Recognition  
D. Named Expression Representation  

7. **(Medium) Select all that apply:** Which steps are required before performing NER on article titles using spaCy?  
A. Load the spaCy language model  
B. Pass the text through the model  
C. Convert the DataFrame to a NumPy array  
D. Tokenize with `split()`  

8. **(Medium)** What type of object is returned when you process a string with a spaCy model (e.g., `nlp(title)`)?  
A. A list of tokens  
B. A spaCy Doc object  
C. A pandas Series  
D. A string  

9. **(Hard) Select all that apply:** Which attributes or methods can be used to extract named entities from a spaCy Doc object?  
A. .ents  
B. .lemma_  
C. .text  
D. .label_  

10. **(Hard)** What is the output of iterating over `doc.ents` for a processed title?  
A. Each token in the sentence  
B. Each named entity and its label (e.g., "Barack Obama" – PERSON)  
C. Each word’s lemma  
D. The number of sentences  

## Section 3: Interpreting and Using NER Output

11. **(Easy)** What does the NER label "ORG" typically represent?  
A. A location  
B. An organization  
C. A date  
D. A product  

12. **(Medium) Select all that apply:** Which of the following are standard NER entity types in spaCy?  
A. PERSON  
B. GPE  
C. PRODUCT  
D. COLOR  

13. **(Medium)** If a title contains "Apple launches new iPhone," which entities and labels would spaCy most likely assign?  
A. "Apple" – ORG, "iPhone" – PRODUCT  
B. "Apple" – PERSON, "iPhone" – GPE  
C. "Apple" - ORG, "iPhone" – GPE  
D. "Apple" – PRODUCT, "iPhone" – PRODUCT    

14. **(Hard)** Why might different spaCy models yield different NER results on the same text?  
A. They are trained on different data and have different vocabularies  
B. They always return the same output  
C. Some models ignore punctuation  
D. Only one model supports English  

15. **(Hard) Select all that apply:** What are potential uses of NER output in analyzing a news article corpus?  
A. Identifying trends in organizations or people mentioned  
B. Filtering articles by location or product  
C. Automatically generating article summaries  
D. Counting the frequency of entity types  