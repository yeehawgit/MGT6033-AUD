# Answer Key

## Section 1: Filtering and Regular Expressions in Pandas

1. **Correct Answer:** B  
**Explanation:** The method filters rows where the folder name contains 'sent', regardless of case.  
**Verbatim Quote:** “So in this folder column … I want to see if it contains the word sent. And I’m going to make it case insensitive.” (4_DemoB1-The-Data.txt)

2. **Correct Answers:** A, C  
**Explanation:** Word boundaries do not recognize underscores or punctuation, so folders like '_sent_mail' or 'sent_items' are not matched.  
**Verbatim Quote:** “The reason that that happened is because an underscore is not a word boundary. … it’s part of that word character class.” (4_DemoB1-The-Data.txt)

3. **Correct Answer:** A  
**Explanation:** Look-around operators let you require certain characters before/after the match without including them in the result.  
**Verbatim Quote:** “The look-around operators with regex allow you to specify something that is required to be (or not to be) adjacent to the search pattern.” (4_DemoB1-The-Data.txt)

4. **Correct Answers:** A, B, C, D  
**Explanation:** The custom character class includes underscore, period, whitespace, and semicolon, among others.  
**Verbatim Quote:** “My look behind includes an underscore, a period, a comma, a semicolon, a question mark and exclamation point, and a space.” (4_DemoB1-The-Data.txt)

5. **Correct Answer:** A  
**Explanation:** The pattern matches 'sent' as a standalone word or when surrounded by specified punctuation or whitespace.  
**Verbatim Quote:** “So allowing for the beginning of the string, allowing for the end of the string all operator, all operator, and then my custom character class in my look around.” (4_DemoB1-The-Data.txt)

## Section 2: Parsing Email Metadata and Messages

6. **Correct Answer:** B  
**Explanation:** The regex matches the date and time line in the email header.  
**Verbatim Quote:** “So let’s start with date. … I want to find date that appears at the beginning of the line.” (4_DemoB2-Parsing.txt)

7. **Correct Answers:** A, B, C, D  
**Explanation:** The function extracts Date, From, To, X-From, and X-To with similar patterns.  
**Verbatim Quote:** “So date from email to email, from person to person. That’s the five pieces of information that I’m going to collect.” (4_DemoB2-Parsing.txt)

8. **Correct Answer:** A  
**Explanation:** The `re.M` flag treats each line as a separate string, enabling `^` to match the start of each line.  
**Verbatim Quote:** “The reason is regular expression engine is by default to consider this string to be that just that one big string. … There’s this flag called multi-line or re.M for short that does just what I wanted to do.” (4_DemoB2-Parsing.txt)

9. **Correct Answers:** A, B, D  
**Explanation:** Initializing to None avoids errors, ensures consistent returns, and allows for missing/optional fields.  
**Verbatim Quote:** “I’m just initializing them all to none and you’ll see in a minute why I’m taking this extra step. … account for the possibility that some of these regular expressions will fail to match.” (4_DemoB2-Parsing.txt)

10. **Correct Answer:** A  
**Explanation:** These variables control when to start capturing the actual message content after the last metadata line.  
**Verbatim Quote:** “I’m going to set both of those equal to false. … If capture equals true, grab the line, stick it in message lines.” (4_DemoB3-Parsing-Messages.txt)

## Section 3: DataFrame Construction and Analysis

11. **Correct Answer:** A  
**Explanation:** Each row represents a unique parsed email with its metadata and body.  
**Verbatim Quote:** “So here’s the final function … I go ahead and add this backslash n join message lines like we saw above.” (4_DemoB3-Parsing-Messages.txt)

12. **Correct Answers:** A, B, C, D  
**Explanation:** The parsed DataFrame includes timestamp, from_email, to_email, and msg columns.  
**Verbatim Quote:** “parsed = pd.DataFrame(parsed.to_list(),columns = ['timestamp','from_email','to_email','from_person','to_person','msg'])” (4B-RegEx-Pandas.pdf)

13. **Correct Answer:** B  
**Explanation:** value_counts() is used to count the number of emails sent by each sender.  
**Verbatim Quote:** “print(parsed['from_email'].value_counts().head(5))” (4_-DemoB4-Analyzing-the-Data.txt)

14. **Correct Answers:** A, B, C, D  
**Explanation:** Convert to UTC, extract hour, count occurrences, and optionally plot a histogram.  
**Verbatim Quote:** “pd.to_datetime(parsed['timestamp'], utc=True).dt.hour.value_counts()” (4_-DemoB4-Analyzing-the-Data.txt)

15. **Correct Answer:** A  
**Explanation:** The column remains object type if time zone offsets are present and must be normalized to UTC.  
**Verbatim Quote:** “The reason that this happened is because we have those offsets built in. These are in different time zones.” (4_-DemoB4-Analyzing-the-Data.txt)

## Section 4: Searching for Keywords and Executive Emails

16. **Correct Answer:** B  
**Explanation:** str.contains() is used to search for the presence of a keyword in a string column.  
**Verbatim Quote:** “parsed.loc[parsed['msg'].str.contains('fraud',case=False)]” (4_-DemoB4-Analyzing-the-Data.txt)

17. **Correct Answers:** A, D  
**Explanation:** Searching for executive names helps identify emails sent by executives and analyze leadership communication.  
**Verbatim Quote:** “parsed.loc[parsed['from_email'].str.contains(r'(lay|skilling|fastow)'),'from_email'].value_counts()” (4_-DemoB4-Analyzing-the-Data.txt)

18. **Correct Answer:** D  
**Explanation:** Few sent emails from executives may be due to alternate folders, assistants, or incomplete data.  
**Verbatim Quote:** “Maybe their sent emails were on other folders. Maybe they had someone else running their email for them. … not much from those two and actually nothing from the CFO at least with this subset.” (4_-DemoB4-Analyzing-the-Data.txt)

19. **Correct Answers:** A, B, C  
**Explanation:** Many emails mentioning 'fraud' are legal notifications, news, or copied content, not direct discussions.  
**Verbatim Quote:** “You can see a lot of them tend to be copy and paste of other things. It seems like a lot of legalese.” (4_-DemoB4-Analyzing-the-Data.txt)

20. **Correct Answer:** A  
**Explanation:** Regular expressions and pandas string methods allow flexible, efficient processing of unstructured text.  
**Verbatim Quote:** “You now have some knowledge of how to use regular expressions to filter and search through these.” (4_-DemoB4-Analyzing-the-Data.txt)
