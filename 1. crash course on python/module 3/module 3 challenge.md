**Question 1**<br>
Fill in the blanks to print the numbers from 15 to 5, counting down by fives.
```
number = 15 # Initialize the variable
while number > 0: # Complete the while loop condition
    print(number, end=" ")
    number -= 5 # Increment the variable
# Should print 15 10 5 
```

**Question 2**<br>
Find and correct the error in the for loop below.  The loop should check each number from 1 to 5 and identify if the number is odd or even.  
```
for number in range(1,5+1):
    if number % 2 == 0:
        print("even")
    else:
        print("odd")
# Should print:
# odd
# even
# odd
# even
# odd
```

**Question 3**<br>
Fill in the blanks to complete the function “digits(n)” to count how many digits the given number has. For example: 25 has 2 digits and 144 has 3 digits. 
Tip: you can count the digits of a number by dividing it by 10 once per digit until there are no digits left.
```
def digits(n):
    count = 0
    if n == 0:
      count += 1
    while n >= 1: # Complete the while loop condition
        # Complete the body of the while loop. This should include 
        # performing a calculation and incrementing a variable in the
        # appropriate order.  
        n = n/10 
        count += 1
    return count
print(digits(25))   # Should print 2
print(digits(144))  # Should print 3
print(digits(1000)) # Should print 4
print(digits(0))    # Should print 1
```

**Question 4**<br>
Fill in the blanks to complete the “rows_asterisks” function. This function should print rows of asterisks (*), where the number of rows is equal to the “rows” 
variable. The number of asterisks per row should correspond to the row number (row 1 should have 1 asterisk, row 2 should have 2 asterisks, etc.). 
Complete the code so that “row_asterisks(5)” will print:
```
*
* *
* * *
* * * *
* * * * *
```
```
def rows_asterisks(rows):
    # Complete the outer loop range to control the number of rows
    for x in range(rows): 
        # Complete the inner loop range to control the number of 
        # asterisks per row
        for y in range(x+1): 
            # Prints one asterisk and one space
            print("*", end=" ")
        # An empty print() function inserts a line break at the 
        # end of the row 
        print()
rows_asterisks(5)
# Should print the asterisk rows shown above
```

**Question 5**<br>
Fill in the blanks to complete the “divisible” function. This function should count the number of values from 0 to the “max” parameter minus 1 that are 
evenly divisible by the “divisor” parameter. This means they do not have a remainder when divided by the divisor. 
Complete the code so that a function call like “divisible(100,10)” will return the number “10”.
```
def divisible(max, divisor):
    count = 0 # Initialize an incremental variable
    for x in range(0, max): # Complete the for loop
        if x % divisor == 0:
            count += 1 # Increment the appropriate variable
    return count
print(divisible(100, 10)) # Should be 10
print(divisible(10, 3)) # Should be 4
print(divisible(144, 17)) # Should be 9
```

**Question 6**<br>
Fill in the blanks to complete the “even_numbers” function. This function should return a space-separated string of all positive even numbers, 
excluding 0, up to and including the “maximum” variable that's passed into the function. Complete the for loop so that a function call like “even_numbers(6)” 
will return the numbers “2 4 6”.  
```
def even_numbers(maximum):

    return_string = "" # Initializes variable as a string

    # Complete the for loop with a range that includes all even numbers
    # up to and including the "maximum" value, but excluding 0.
    for even_number in range(2, maximum+1, 2): 

        # Complete the body of the loop by appending the even number
        # followed by a space to the "return_string" variable.
        return_string += str(even_number) + " "  

    # This .strip command will remove the final " " space at the end of
    # the "return_string".
    return return_string.strip() 
print(even_numbers(6))  # Should be 2 4 6
print(even_numbers(10)) # Should be 2 4 6 8 10
print(even_numbers(1))  # No numbers displayed
print(even_numbers(3))  # Should be 2
print(even_numbers(0))  # No numbers displayed
```

**Question 7**<br>
What happens when the Python interpreter executes a loop where a variable used inside the loop is not initialized?
- [ ] Nothing will happen 
- [x] Will produce a NameError stating the variable is not defined
- [ ] The variable will be auto-assigned a default value of 0
- [ ] Will produce a TypeError 

**Question 8**<br>
What is the final value of “x” at the end of this for loop? Your answer should be only one number.
```
for x in range(1, 10, 3):
    print(x)
```
> 7

**Question 9**<br>
What is the final value of "y" at the end of the following nested loop code? Your answer should be only one number.
```
for x in range(10):
    for y in range(x):
        print(y)
```
> 8

**Question 10**<br>
The following code causes an infinite loop. Can you figure out what’s incorrect and how to fix it?
```
def count_to_ten():
  # Loop through the numbers from first to last 
  x = 1
  while x <= 10:
    print(x)
    x = 1
count_to_ten()
# Should print:
# 1
# 2
# 3 
# 4
# 5
# 6
# 7
# 8 
# 9
# 10
```
- [ ] Needs to have parameters passed to the function
- [ ] The "x" variable is initialized using the wrong value
- [x] Variable "x" is assigned the value 1 in every loop
- [ ] Should use a for loop instead of a while loop
