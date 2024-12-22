**Question 1**<br>
What is a characteristic of a CSV file? 
- [ ] Each line represents a different column of data.
- [x] Data in each row is separated by a special character.
- [ ] CSV files can contain only numeric data.
- [ ] It cannot be read by a text editor.

**Question 2**<br>
Why is it important to define headers for the output file when replacing old domain names with new ones in a CSV file using Python, as described in the lab?
- [ ] To ensure that the email addresses are correctly replaced
- [x] To identify the column that contains email addresses in the output file
- [ ] To save memory and improve script performance
- [ ] To prevent errors when opening the output file

**Question 3**<br>
What is the advantage of using absolute paths compared to relative paths?
- [ ] Absolute paths are shorter and easier to type.
- [ ] Absolute paths are required for all file system operations.
- [x] Absolute paths work consistently regardless of the current working directory.
- [ ] Absolute paths are always secure and prevent unauthorized access.

**Question 4**<br>
Imagine you're working on a different machine and are unsure of the current directory path. 
How can you display the contents of the subdirectory examples within your current directory, assuming it exists?
- [ ] cd examples
- [ ] dir examples
- [ ] ls examples
- [x] ls /user/share/doc/python3/examples 

**Question 5**<br>
You're writing a Python script that needs to read data from a file called user_data.txt. By default, the open function assumes the file is in which location?
- [ ] The user's home directory on the system
- [x] The same directory as the Python script you're running
- [ ] You need to specify the location explicitly every time
- [ ] A temporary directory created by the script

**Question 6**<br>
Imagine you're reading a text file line by line in Python. The file contains data like names, but each name has an extra blank line appended after it. 
Which of the following modifications to the code would most effectively remove these extra blank lines while keeping the names intact?
- [ ] Use a loop to iterate through each character in the line and remove any newline characters.
- [x] Apply the strip method on each line before storing it in a list.
- [ ] Open the file in write mode and rewrite the content without the blank lines.
- [ ] Add an if statement within the loop to only print lines that are not empty.

**Question 7**<br>
Imagine you're working in a terminal on a Linux system. You want to create a new directory named "project_data" within your current working directory. 
Which command achieves this?
- [ ] Right-clicking in the terminal window and selecting "New Folder".
- [ ] You need to navigate to the desired location first using cd.
- [x] mkdir project_data
- [ ] create_dir project_data

**Question 8**<br>
What is the primary function of the line reader = csv.DictReader(software) in this Python code?
- [ ] It converts the "software.csv" file into a list of lists.
- [ ] It reads the entire content of "software.csv" into a single dictionary.
- [ ] It opens the "software.csv" file in write mode for appending data.
- [x] It creates a dictionary reader object to iterate over rows in the "software.csv" file, treating each row as a dictionary.

**Question 9**<br>
Imagine you're working in a terminal on a Linux or Unix-based system. You've been instructed to navigate to the "data" directory and then list the files 
within that directory. Which of the following commands would achieve the desired outcome?
- [x] cd data and ls
- [ ] view data
- [ ] show data
- [ ] open data

**Question 10**<br>
The Python code snippet below processes data from a file (presumably CSV) and stores it in a list named employee_list. 
What does the line employee_list.append(dict(data)) achieve within the loop?
```
 employee_list = []
 for data in employee_file:
 employee_list.append(dict(data))
```
- [ ] It merges the contents of the file directly into the employee_list without any changes.
- [ ] It appends each line of the file (as a string) to the employee_list without modification.
- [ ] It creates a new dictionary for each data item and discards the original data.
- [x] It converts each data item from the file into a dictionary and appends it to the employee_list.
