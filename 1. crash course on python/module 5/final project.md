**Question 1**<br>
A programmer is working on a new project and encounters a complex problem. They are tempted to spend a lot of time trying to solve the problem on their own. 
However, a colleague advises them to research existing solutions first. What is the colleague's advice based on?
- [ ] The colleague believes that the programmer should not try to be innovative.
- [ ] The colleague believes that the programmer should not trust their own abilities to solve the problem.
- [x] The colleague believes that the programmer should not waste time reinventing something that already exists.
- [ ] The colleague believes that the programmer should ask someone with more experience to solve this problem. 

**Question 2**<br>
Based on the following code, what is the correct output?
```
numbers = [ 3, 5, 4, 8, 1 ]
numbers.sort()
print(numbers)
```
- [ ] 3, 5, 4, 8, 1
- [x] 1, 3, 4, 5, 8
- [ ] 3, 1, 5, 4, 8
- [ ] 8, 5, 4, 3, 1

**Question 3**<br>
Which method is used to sort a list and keep the original list intact?
- [ ] The sort() method 
- [x] The sorted() method 
- [ ] The sorted() method with a reverse argument. 
- [ ] The print() method.

**Question 4**<br>
You need to sort a list in descending order, which argument should you use in your sort() method to do this?
- [ ] backup = True
- [ ] backup = False
- [ ] reverse = False
- [x] reverse = True

**Question 5**<br>
What is the purpose of the argument key=len in a Python script?
- [x] To sort a list of strings based on their length. 
- [ ] To sort a list of strings based on importance. 
- [ ] To sort a list of strings alphabetically.
- [ ] To sort a list of strings based on their capitalization. 

**Question 6**<br>
A grocery store is tracking the inventory of its products. For each product, the store needs to keep track of the product name, the product ID, 
the quantity in stock, and the price. Which data structure is the most efficient for storing the information associated with each product?
- [ ] A set
- [ ] A tuple
- [x] A dictionary 
- [ ] A list

**Question 7**<br>
Why is it beneficial to use separate functions in your Python code? Select all that apply. 
- [x] Improves code debugging
- [ ] Ensures the code cannot be reused.
- [x] Allows code to be modified more easily
- [x] Processes data more easily 

**Question 8**<br>
Which of the following best describes the purpose of an if statement in Python?
- [ ] To repeat a block of code a certain number of times
- [x] execute a block of code only if a certain condition is true
- [ ] To store data in a temporary variable
- [ ] To define a function that performs a specific task 

**Question 9**<br>
A programmer is designing a grading script for a teacher. The teacher needs to assign grades to students based on different student assessment scores. 
The programmer needs to create a script that will execute code block A if condition 1 is true but will execute code block B if condition 1 is false and condition 2 is true. 
What type of statement should the programmer use to evaluate condition 2?
- [ ] and statement
- [x] elif statement
- [ ] if statement
- [ ] else statement

**Question 10**<br>
What is the purpose of the following code snippet?
```
def generate_report(machines):
  for machine, users in machines.items():
    if len(users) > 0:
      user_list = ", ".join(users)
      print("{}: {}".format(machine, user_list))
```
- [ ] To print a list of all the machines that are currently in use.
- [ ] To print a list of all the events that have occurred.
- [x] To create a list of all users currently logged into any machine and the machine they're logged into.
- [ ] To create a list of all the users who have ever logged into any machine.
