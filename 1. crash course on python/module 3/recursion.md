**Question 1**<br>
What is recursion used for?
- [ ] Recursion is used to create loops in languages where other loops are not available.
- [ ] We use recursion only to implement mathematical formulas in code.
- [ ] Recursion is used to iterate through files in a single directory
- [x] Recursion is used to call a function from inside the same function.
You nailed it! You can call a function inside of itself to iterate over a hierarchy of objects, like directories and subdirectories. 

**Question 2**<br>
Which of these activities are good use cases for recursive programs? Check all that apply.
- [x] Going through a file system collecting information related to directories and files.
Right on! Because directories can contain subdirectories that can contain more subdirectories, going through these contents is a good use case for a recursive program.
- [ ] Creating a user account for a new employee.
- [ ] Installing or upgrading software on a computer.
- [x] Managing permissions assigned to groups inside a company, when each group can contain both subgroups and users.
You got it! As the groups can contain both groups and users, this is the kind of problem that is a great use case for a recursive solution.
Checking if a computer is connected to the local network.

**Question 3**<br>
Fill in the blanks to make the is_power_of function return whether the number is a power of the given base. Note: base is assumed to be a positive number. 
Tip: for functions that return a boolean value, you can return the result of a comparison.
```
def is_power_of(number, base):
 # Base case: when number is smaller than base.
    if number == 1:
        return True
    if number < base:
        # If number is equal to 1, it's a power (base**0).
        return False

    # Recursive case: keep dividing number by base.
    return is_power_of(number/base, base)

print(is_power_of(8,2))     # Should be True
print(is_power_of(64,4))    # Should be True
print(is_power_of(70,10))   # Should be False
```

**Question 4**<br>
Recursion is a process where a function calls itself one or more times with modified values to accomplish a task. 
This technique can be particularly effective when solving complex problems that can be broken down into smaller, simpler problems of the same type. 
In the provided code, the count_users function uses recursion to count the number of users that belong to a group within a company's system. 
It does this by iterating through each member of a group, and if a member is another group, it recursively calls count_users to count the users within that subgroup.
However, there is a bug in the code! Can you spot the problem and fix it?
```
def count_users(group):
  count = 0
  for member in get_members(group):
    if is_group(member):
      count += count_users(member)
    else:
      count += 1
  return count

print(count_users("sales")) # Should be 3
print(count_users("engineering")) # Should be 8
print(count_users("everyone")) # Should be 18
```

**Question 5**<br>
In the while loops practice quiz, you were asked to write a function to calculate the sum of all positive numbers between 1 and n. 
Rewrite the function using recursion instead of a while loop. Remember that when n is less than 1, the function should return 0 as the answer.
```
def sum_positive_numbers(n):
    if n < 1:
        return 0
    return n + sum_positive_numbers(n-1)

print(sum_positive_numbers(3)) # Should be 6
print(sum_positive_numbers(5)) # Should be 15
```
