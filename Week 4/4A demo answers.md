# Answer Key

## Section 1: Building and Tuning Regular Expressions

1. **Correct Answer:** B  
**Explanation:** `\b` sets a word boundary for precise matching.  
**Verbatim Quote:** “Recall that the \b  signifies a word boundary, which requires the match to be 'complete'.” (4A-RegEx-basics.pdf)

2. **Correct Answers:** A, D  
**Explanation:** `[a-z0-9._]+` and `[a-z0-9\._]+` both match valid mailbox components in example regex.  
**Verbatim Quote:** “the mailbox (letters, numbers, periods, underscores)” (4A-RegEx-basics.pdf)

3. **Correct Answer:** B  
**Explanation:** Most domains block mailboxes with hyphens to avoid confusion.  
**Verbatim Quote:** “I also think a mailbox may be able to have a hyphen, though...most domains block them to avoid confusion...” (4A-RegEx-basics.pdf)

4. **Correct Answers:** A, B, C, D  
**Explanation:** The domain allows letters, numbers, hyphens, and ends with a period.  
**Verbatim Quote:** “one or more domain labels (letters, numbers, hyphens), followed by period” (4A-RegEx-basics.pdf)

5. **Correct Answer:** B  
**Explanation:** `re.compile()` precompiles the regex for efficiency and reuse.  
**Verbatim Quote:** “re.compile()...can be a little more efficient, though it's not generally necessary.” (4A-RegEx-basics.pdf)

## Section 2: Match Objects and Extraction

6. **Correct Answer:** B  
**Explanation:** Group 0 always contains the entire matched string.  
**Verbatim Quote:** “group 0 is always the full match with re.search ” (4_DemoA2-Analyzing-the-Match-Object.txt)

7. **Correct Answers:** A, B, C, D  
**Explanation:** All listed attributes/methods can be used on match objects.  
**Verbatim Quote:** “extract specific match groups... .group(), .groups(), .start(), .end()” (4_DemoA2-Analyzing-the-Match-Object.txt)

8. **Correct Answer:** B  
**Explanation:** A match object evaluates to True if a match is found; otherwise, False.  
**Verbatim Quote:** “You can use these match objects as Booleans...they can be pretty nice for logic control.” (4_DemoA2-Analyzing-the-Match-Object.txt)

9. **Correct Answers:** D  
**Explanation:** All these issues can prevent a valid match for Twitter handles, incomplete domains, etc.  
**Verbatim Quote:** “So those last two, there's something...that indicates they're not true email addresses.” (4_DemoA1-Rebuilding-Regular-Expressions.txt)

10. **Correct Answer:** B  
**Explanation:** Raw strings prevent Python from interpreting backslashes, letting regex work as intended.  
**Verbatim Quote:** “By leading the string with the r, I'm telling Python not to parse the string.” (4A-RegEx-basics.pdf)

## Section 3: Extracting and Cleaning Data from HTML

11. **Correct Answers:** A, B, C  
**Explanation:** Some a tags lack 'href'; not all a tags are email links; not all emails are in hyperlinks.  
**Verbatim Quote:** “Some a tags have no href...many linked sources of information...not all emails are in hyperlinks.” (4A-RegEx-basics.pdf)

12. **Correct Answer:** B  
**Explanation:** “mailto:” in href indicates a link to an email address.  
**Verbatim Quote:** “mailto: , which instructs the browser to launch the default email client if the link is clicked.” (4A-RegEx-basics.pdf)

13. **Correct Answers:** A, B, D  
**Explanation:** MHT format and local save methods may split or corrupt domains; HTML encoding can break addresses.  
**Verbatim Quote:** “The issue has to do with that MHT format...addresses were cut off...HTML encoding can break up email addresses.” (4_DemoA3-Extracting-All-Matches.txt)

14. **Correct Answer:** A  
**Explanation:** Storing in DataFrame enables cleaning, sorting, deduplication.  
**Verbatim Quote:** “put these in a DataFrame and inspect the results” (4_DemoA3-Extracting-All-Matches.txt)

15. **Correct Answers:** A, B, C  
**Explanation:** The demo fixes common domain errors with programmatic mapping and regex substitution.  
**Verbatim Quote:** “write a function to take care of this...replace with scheller.gatech.edu... anything starting with gatech becomes gatech.edu...incomplete domains like qcf.gatech become qcf.gatech.edu” (4_DemoA3-Extracting-All-Matches.txt)

## Section 4: Phone Number Extraction and Normalization

16. **Correct Answer:** A  
**Explanation:** This regex matches standard US 10-digit numbers with or without dashes or periods.  
**Verbatim Quote:** `([0-9]{3})[-.]?([0-9]{3})[-.]?([0-9]{4})` (4_DemoA4-Final-Assignment.txt)

17. **Correct Answers:** A, B, C  
**Explanation:** Normalization steps: reformat, deduplicate, extract area code and prefix for analysis.  
**Verbatim Quote:** “apply a standard format...remove duplicates...extract the area code and prefix for analysis.” (4_DemoA4-Final-Assignment.txt)

18. **Correct Answer:** B  
**Explanation:** The prefix is the middle three digits in a US phone number (e.g., '385' in 404-385-1234).  
**Verbatim Quote:** “the prefix, that's the next three” (4_DemoA4-Final-Assignment.txt)

19. **Correct Answer:** B  
**Explanation:** 404 is the most common area code in the Georgia Tech data.  
**Verbatim Quote:** “As you might expect, 404 the main Atlanta area code shows up as Number 1…” (4_DemoA4-Final-Assignment.txt)

20. **Correct Answers:** A, B, C  
**Explanation:** Match groups allow extraction, structuring, and substitution, but not ignoring partial matches.  
**Verbatim Quote:** “groups is a list of all of the match groups...structure a DataFrame...substitute using group references.” (4_DemoA2-Analyzing-the-Match-Object.txt)
