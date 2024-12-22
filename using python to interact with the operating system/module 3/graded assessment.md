**Question 1**<br>
What is a regular expression? 
- [ ] A function in Python for handling exceptions
- [ ] A method of encrypting data
- [ ] A type of data structure in Python
- [x] A sequence of characters that forms a search pattern

**Question 2**<br>
Which of the following statements are correct regarding the re.sub() function? Select all that apply.
- [x] The re.sub() function allows the use of capturing groups to reuse matched patterns in the replacement text.
- [x] The re.sub() function takes four parameters: the pattern, the replacement string, the input text, and an optional flags parameter.
- [ ] The re.sub() function directly modifies the original input text.
- [x] The replacement string in re.sub() can contain back references to captured groups.

**Question 3**<br>
You are reading an article that contains website urls in the format https://www.website-domain.com. 
You’d like to extract the complete urls from the text automatically, instead of copying and pasting them by hand. 
Complete the function find_url to extract all encrypted websites that begin with https:// and end with any top level domain, 
such as .org, .com, or .co from the text.
```
def find_url(website):
 pattern = r'https://[^\s]+\.[a-z]{2,3}' #enter the regex pattern here
 result = re.findall(pattern, website) #enter the re method here
 return result

print(find_url("Go to the website https://www.coursera.com find more information about Google Certificate Programs. Then, visit https://www.python.org/ to learn more about Python. ")) # Should return ['https://www.coursera.com', 'https://www.python.org']
print(find_url("You can find anything on https://www.google.com!")) # Should return ['https://www.google.com']
print(find_url("You can find anything on http://www.google.com!")) # Should return []
print(find_url("Check out python.org!")) # Should return []
```

**Question 4**<br>
You are exploring the punctuation at the end of sentences and want to split sentences so that each word is separate and any punctuation is 
included in the word next to it. Complete the parse_sentences function to accomplish this task. 
```
def parse_sentences(sentence):
 pattern = r'\w+[!?.]|\w+|\S' #enter the regex pattern here
 result = re.findall(pattern, sentence) #enter the re method  here
 return result

print(parse_sentences("Hello! How are you doing?")) # should return ['Hello!', 'How', 'are', 'you', 'doing?']
print(parse_sentences("what a beautiful day it is")) # should return ['what', 'a', 'beautiful', 'day', 'it', 'is']
print(parse_sentences("2 + 2 is definitely 4!")) # should return ['2', '+', '2', 'is', 'definitely', '4!']
```

**Question 5**<br>
A company uses unique, 9-character codes that begin with a capital letter, followed by a hyphen (-), followed by 7 or 8 digits as employee ID numbers, 
in the format A-1234567 or A-12345678. Project reports submitted to the company include the employee’s ID number and a summary of the work they completed 
on the project. 

A data analyst wants to pull all of the employee ID numbers out of these projects. Complete the find_eid function to extract these employee ID numbers 
from the reports. 
```
def find_eid(report):
  pattern = r'\b[A-Z]-\d{7,8}\b' #enter the regex pattern here
  result = re.findall(pattern, report) #enter the re method  here
  return result

print(find_eid("Employees B-1234567 and C-12345678 worked with products X-123456 and Z-123456789")) # Should return ['B-1234567', 'C-1234567']
print(find_eid("Employees B-1234567 and C-12345678, not employees b-1234567 and c-12345678")) #Should return ['B-1234567', 'C-1234567']
```

**Question 6**<br>
In the provided code snippet, what is the purpose of the replace_domain function?
```
def replace_domain(address, old_domain, new_domain):
  old_domain_pattern = r'' + old_domain + '$'
  address = re.sub(old_domain_pattern, new_domain, address)
  return address
```
- [ ] To remove any domain from the email address
- [ ] To validate the format of an email address
- [x] To create a new email address by replacing an old domain with a new domain
- [ ] To extract the username part of an email address

**Question 7**<br>
What is the purpose of initializing the old_domain_email_list in the code from the lab?
- [x] To store email addresses with the old domain that match the regex pattern
- [ ] To store email addresses with the new domain
- [ ] To perform a substitution operation on email addresses
- [ ] To store all email addresses from user_email_list

**Question 8**<br>
Why is it considered good practice to use the close() method to close a file after processing it in Python?
- [ ] To encrypt the file and enhance its security
- [ ] To permanently delete the file from the system
- [x] To free up system resources and prevent further reading or writing to the file
- [ ] To ensure the file remains open for other processes to access.

**Question 9**<br>
What is a key benefit of using Python for creating reports and employing regular expressions?
- [ ] To develop virtual reality applications.
- [ ] To enhance cybersecurity measures.
- [x] To automate repetitive tasks and data analysis.
- [ ] To optimize website performance.

**Question 10**<br>
In the Python script for processing user_emails.csv, what is the purpose of the contains_domain function?
- [ ] To count the number of email addresses in the CSV file
- [ ] To encrypt email addresses in the CSV file for security
- [x] To check if an email address belongs to a specific domain, using Regular Expressions (RegEx)
- [ ] To add a new domain to each email address in the CSV file
