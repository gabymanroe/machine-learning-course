**Question 1**<br>
You have created a Python script to read a log of users running CRON jobs. The script needs to accept a command line argument for the path to the log file. 
Which line of code accomplishes this?
- [ ] import sys
- [x] syslog=sys.argv[1]
- [ ] print(line.strip())
- [ ] usernames = {}

**Question 2**<br>
Which of the following is a data structure that can be used to count how many times a specific error appears in a log?
- [x] Dictionary
- [ ] Continue
- [ ] Search
- [ ] Get

**Question 3**<br>
Which keyword will return control back to the top of a loop when iterating through logs?
- [x] Continue
- [ ] Get
- [ ] With
- [ ] Search

**Question 4**<br>
When searching log files using regex, which regex statement will search for the alphanumeric word "IP" followed by one or more digits wrapped in parentheses 
using a capturing group?
- [ ] r"IP \(\d+\)$"
- [ ] b"IP \((\w+)\)$"
- [x] r"IP \((\d+)\)$"
- [ ] r"IP \((\D+)\)$" 

**Question 5**<br>
Which of the following are true about parsing log files? (Select all that apply.)
- [ ] Load the entire log files into memory.
- [x] You should parse log files line by line.
- [x] It is efficient to ignore lines that don't contain the information we need.
- [x] We have to open() the log files first.
