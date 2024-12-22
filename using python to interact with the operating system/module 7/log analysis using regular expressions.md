**Question 1**<br>
Which task can you accomplish by using regular expressions in log analysis? 
- [ ] Sorting log entries based on timestamps
- [ ] Converting log data into graphical charts
- [x] Parsing log entries to extract specific fields
- [ ] Counting the total number of log entries in a file

**Question 2**<br>
What will the following command return?
	grep ticky syslog.log
- [ ] A duplicate file of syslog 
- [ ] All the INFO logs in syslog
- [ ] All the ERROR logs in syslog
- [x] all the logs from ticky

**Question 3**<br>
Complete the sentence for the following Python regular expression: To match a string stored in a line variable, we use the search() method by defining a_____.
- [ ] span
- [x] pattern
- [ ] line
- [ ] log

**Question 4**<br>
When sorting this dictionary:
```
	fruit = {"oranges": 3, "apples": 5, "bananas": 7, "pears": 2}
```
What will the following line of code return?
```
	sorted(fruit.items(), key=operator.itemgetter(1))
```
- [ ] [('apples', 5), ('bananas', 7), ('oranges', 3), ('pears', 2)]
- [ ] sorted fruit = {"oranges": 3, "apples": 5, "bananas": 7, "pears": 2}
- [x] [('pears', 2), ('oranges', 3), ('apples', 5), ('bananas', 7)]
- [ ] [('bananas', 7), ('apples', 5), ('oranges', 3), ('pears', 2)]

**Question 5**<br>
Which of the following is a potential pitfall of automation in Python? 
- [ ] It increases the amount of manual work required
- [x] It limits the system's ability to adapt to changes
- [ ] It improves the overall efficiency of the system
- [ ] It makes the system more prone to errors

**Question 6**<br>
While you were working with the log file named syslog.log, what command did you use to view the file? 
- [ ] search syslog.log
- [ ] grep syslog.log
- [x] cat syslog.log
- [ ] cat file syslog.log

**Question 7**<br>
What syntax would you use to enlist all the ERROR messages of a specific kind?
- [ ] grep ERROR [file-name] [message]
- [x] grep ERROR [message] [file-name]
- [ ] grep [file-name] ERROR [message]
- [ ] grep [file-name] [message] ERROR

**Question 8**<br>
In Python, regular expressions are typically handled using which module? 
- [ ] os
- [ ] math
- [x] re
- [ ] sys

**Question 9**<br>
Which argument can be used with the sorted() function to sort a dictionary's items based on their values in descending order? 
- [x] sorted(dictionary.items(), key=lambda x: x[1], reverse=True)
- [ ] sorted(dictionary.values(), reverse=True)
- [ ] sorted(dictionary, key=lambda x: x[1], reverse=True)
- [ ] sorted(dictionary, reverse=True)

**Question 10**<br>
Which of the following commands would convert a csv file named error_message.csv into HTML file named errors.html? 
- [x] ./csv_to_html.py error_message.csv /var/www/html/<errors>.html
- [ ] /csv_to_html.py error_message.csv /var/www/html/<errors.html>.html
- [ ] /html_to_csv.py error_message.csv /var/www/html/<errors>.html
- [ ] /csv_convert_html.py error_message.csv /var/www/html/<errors>.html
