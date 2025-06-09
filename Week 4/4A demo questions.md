# Quiz Questions

## Section 1: Building and Tuning Regular Expressions

1. **(Easy)** What does the `\b` symbol designate in a regular expression used for email addresses?  
A. Beginning of file  
B. Word boundary  
C. Uppercase only  
D. Blank space  

2. **(Medium, Select all that apply):** Which regular expression elements are recommended for matching the mailbox part of an email address ("robbie.moon" in "robbie.moon@gatech.edu") in the demos?  
A. [a-z0-9._]+  
B. \d+  
C. [A-Z]  
D. [a-z0-9\\._]+  

3. **(Hard)** Why are hyphens typically excluded from the mailbox group in the email address regex presented?  
A. They are not allowed in any email address  
B. Most domains block mailboxes with hyphens to avoid confusion  
C. Regex cannot process hyphens  
D. Hyphens are only required in web addresses  

4. **(Medium, Select all that apply):** When matching the domain part of an email, what character types and symbols are included in the demo's regex?  
A. Letters  
B. Numbers  
C. Hyphens  
D. Periods  

5. **(Hard)** What is the main purpose of using `re.compile()` in the regular expression demos?  
A. To force the use of raw strings  
B. To precompile and possibly reuse the regex efficiently  
C. To suppress error messages  
D. To skip syntax checks  

## Section 2: Match Objects and Extraction

6. **(Medium)** Which group in the match object always contains the entire matched string?  
A. Group 1  
B. Group 0  
C. Group 2  
D. .groups()  

7. **(Hard, Select all that apply):** What attributes or methods can you use on a match object to extract specific information?  
A. .group(n)  
B. .groups()  
C. .start()  
D. .end(n)  

8. **(Medium)** When using regular expressions for logic control, how is a match object evaluated in a boolean context?  
A. Always False  
B. True if a match is found, False otherwise  
C. Always True  
D. Only True if all groups are non-empty  

9. **(Hard):** In the email extraction demo, why might an address like “@twitter_handle” not be matched by the regular expression?  
A. It is missing the mailbox part before the @  
B. The domain part is incomplete  
C. The suffix is missing or invalid  
D. All of the above  

10. **(Hard)** Why is a raw string (e.g., `r"pattern"`) often used when defining regex patterns in Python?  
A. It allows Python to parse mixed data types  
B. It prevents Python from interpreting backslashes  
C. It changes the regex to case-insensitive  
D. It enables multi-line matching  

## Section 3: Extracting and Cleaning Data from HTML

11. **(Medium, Select all that apply):** When using BeautifulSoup to extract email addresses from HTML, what errors must be handled or avoided?  
A. Some `<a>` tags do not have an 'href' attribute  
B. HTML may contain non-email links in `<a>` tags  
C. Not all emails are in hyperlinks  
D. All `<a>` tags are guaranteed to be emails  

12. **(Medium)** What is the significance of the string `'mailto:'` in the extracted `href` attributes?  
A. It marks a link that downloads a file  
B. It indicates a link to an email address  
C. It means the tag is a header  
D. It only appears in external links  

13. **(Hard, Select all that apply):** Why do some extracted email domains appear incomplete or malformed in the demo (e.g., “gatech.ed”)?  
A. The raw MHT format splits addresses across lines  
B. Some addresses are corrupted during local save  
C. Regex is not capable of extracting correct domains  
D. HTML encoding can break up email addresses  

14. **(Hard)** What is the main benefit of storing extracted emails and their domains in a pandas DataFrame?  
A. It enables further cleaning, sorting, and deduplication  
B. It increases processing speed  
C. It encrypts the data automatically  
D. It removes all duplicate domains by default  

15. **(Medium, Select all that apply):** In cleaning email domains, what fixes are applied in the demo's mapping or function-based approach?  
A. Replace all “schel…” with “scheller.gatech.edu”  
B. Standardize anything starting with “gatech” to “gatech.edu”  
C. Substitute incomplete domains like “qcf.gatech” with “qcf.gatech.edu”  
D. Delete all emails with a dot in the domain  

## Section 4: Phone Number Extraction and Normalization

16. **(Easy)** Which regex pattern best matches a standard US phone number (with or without dashes or periods)?  
A. `([0-9]{3})[-.]?([0-9]{3})[-.]?([0-9]{4})`  
B. `\w+@\w+\.\w+`  
C. `[a-z]+://`  
D. `\d{12}`  

17. **(Hard, Select all that apply):** After extracting phone numbers, what normalization steps are performed in the demo?  
A. Reformat all numbers to a standard (e.g., “404-385-1234”)  
B. Remove duplicates  
C. Extract area code and prefix for analysis  
D. Store as a JSON string  

18. **(Medium)** Which part of a phone number is called the “prefix” in US numbers like “404-385-1234”?  
A. 404  
B. 385  
C. 1234  
D. 12  

19. **(Hard)** What was discovered about area codes when extracting phone numbers from the Georgia Tech faculty directory?  
A. Only non-US numbers were found  
B. 404 was the most common area code  
C. No numbers had area codes  
D. All area codes were unique  

20. **(Medium, Select all that apply):** What are reasons to use match groups (parentheses) in regex for extracting information?  
A. To extract specific subcomponents of a match  
B. To reorganize extracted data for a DataFrame  
C. To perform substitutions using group references  
D. To ignore partial matches  
 