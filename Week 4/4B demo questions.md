# Quiz Questions

## Section 1: Filtering and Regular Expressions in Pandas

1. **(Easy)** What is the purpose of using `str.contains(r'sent', case=False)` on the 'folder' column in the Enron email dataset?  
A. To sort the DataFrame by folder name  
B. To filter rows where the folder name contains 'sent', case-insensitive  
C. To remove all emails from the dataset  
D. To extract the sender’s email address  

2. **(Medium, Select all that apply):** Why might using word boundaries (`\b`) in a regex pattern fail to match folders like '_sent_mail' or 'sent_items'?  
A. The underscore is not considered a word boundary in regex  
B. Word boundaries only match spaces  
C. The folder names contain punctuation or underscores  
D. Word boundaries only work at the start or end of strings  

3. **(Hard)** What is the main advantage of using look-around operators (look-ahead and look-behind) when filtering folder names with regex?  
A. They allow matching patterns only if certain characters appear before or after, without including those characters in the match  
B. They increase the speed of the regex search  
C. They always match partial words  
D. They remove all punctuation from the folder name  

4. **(Medium, Select all that apply):** Which of the following are included in the custom character class for defining word boundaries in the advanced regex pattern for folder filtering?  
A. Underscore  
B. Period  
C. Whitespace  
D. Semicolon  

5. **(Hard)** What is the effect of using the pattern `(^|(?<=[_.,;?!\s]))(sent)($|(?=[_.,;?!\s]))` in the folder filter?  
A. It matches 'sent' as a standalone word or surrounded by specified punctuation/whitespace  
B. It matches any folder containing 'sent' as a substring  
C. It excludes all folders with underscores  
D. It only matches folders at the start of the DataFrame  

## Section 2: Parsing Email Metadata and Messages

6. **(Easy)** What does the regular expression `r'^(Date)(\:\s+)(.+?)$'` with the `re.M` flag match in an email message?  
A. The sender’s email address  
B. The date and time line in the email header  
C. The subject line  
D. The entire message body  

7. **(Medium, Select all that apply):** Which metadata fields are extracted using similar regex patterns in the parsing function?  
A. Date  
B. From  
C. To  
D. X-From  

8. **(Hard)** Why is the `re.M` (multiline) flag necessary when searching for metadata fields in the email message string?  
A. It allows the regex to treat each line as a separate string, matching at the start of each line  
B. It makes the regex case-insensitive  
C. It increases the speed of matching  
D. It allows matching multiple groups at once  

9. **(Hard, Select all that apply):** What is the purpose of initializing all extracted metadata variables to `None` at the start of the parsing function?  
A. To avoid errors if a field is missing  
B. To ensure a consistent return structure  
C. To skip lines containing missing data  
D. To allow for optional fields in the email  

10. **(Hard)** In the message parsing logic, what is the role of the `found_x` and `capture` variables?  
A. They control when to start capturing the actual message content after the last metadata line  
B. They store the sender and recipient names  
C. They track the number of lines in the message  
D. They indicate if the message is spam  

## Section 3: DataFrame Construction and Analysis

11. **(Easy)** After parsing, what does each row in the resulting DataFrame represent?  
A. A unique email message with its parsed metadata and body  
B. A folder in the email server  
C. A user account  
D. A timestamp only  

12. **(Medium, Select all that apply):** Which columns are present in the parsed DataFrame after running the `parse_email` function?  
A. timestamp  
B. from_email  
C. to_email  
D. msg  

13. **(Medium)** What pandas method is used to count the number of emails sent by each sender?  
A. groupby()  
B. value_counts()  
C. sort_values()  
D. count()  

14. **(Hard, Select all that apply):** What steps did Robbie use to analyze the hour of day when most emails were sent?  
A. Convert the 'timestamp' column to UTC datetime  
B. Use `.dt.hour` to extract the hour  
C. Use `value_counts()` to count occurrences  
D. Plot a histogram of the hours  

15. **(Hard)** Why might the 'timestamp' column be an object type instead of datetime, even after parsing?  
A. Because time zone offsets are included and must be normalized to UTC  
B. Because pandas cannot parse dates  
C. Because the column contains missing values  
D. Because the DataFrame is too large  

## Section 4: Searching for Keywords and Executive Emails

16. **(Easy)** What pandas string method is used to search for emails mentioning the word "fraud"?  
A. str.find()  
B. str.contains()  
C. str.replace()  
D. str.upper()  

17. **(Medium, Select all that apply):** What is the purpose of searching for executive last names (e.g., 'lay', 'skilling', 'fastow') in the 'from_email' column using `str.contains()` and `value_counts()`?  
A. To identify emails sent by key Enron executives  
B. To filter emails for legal review  
C. To count the number of emails mentioning executives  
D. To analyze communication patterns of leadership  

18. **(Hard)** Why might there be very few sent emails from executives like Ken Lay or Andy Fastow in the dataset?  
A. Their sent emails may be stored in other folders  
B. They may have used assistants or alternate accounts  
C. The dataset may be incomplete  
D. All of the above  

19. **(Hard, Select all that apply):** What can you infer from analyzing emails that mention "fraud"?  
A. Many are legal notifications or news articles  
B. Not all are direct discussions of Enron’s fraud  
C. Some are copied/pasted from external sources  
D. All are internal whistleblower reports  

20. **(Hard)** What is the main benefit of using regular expressions and pandas string methods together for email analysis?  
A. They allow efficient, flexible filtering, extraction, and organization of unstructured text data  
B. They guarantee perfect parsing of all messages  
C. They convert all emails to CSV format  
D. They encrypt email content  
