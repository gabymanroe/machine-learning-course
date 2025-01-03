**Question 1**<br>
How are while loops and for loops different in Python?
- [ ] while loops can be used with all data types; for loops can be used only with numbers.
- [ ] for loops can be nested, but while loops can't.
- [x] while loops iterate while a condition is true; for loops iterate through a sequence of elements. (You got it! You use while loops when you want your code to execute 
repeatedly while a condition is true, and for loops when you want to execute a block of code for each element of a sequence)
- [ ] while loops can be interrupted using break; you interrupt for loops using continue.

**Question 2**<br>
Which option would fix this for loop to print the numbers 12, 18, 24, 30, 36?
```
for n in range(6,18,3):
  print(n*2)
```
- [ ] `for n in range(6,18,3):
  print(n+2)`
- [x] `for n in range(6,18+1,3):
  print(n*2)`
Great job! To include 18 in the range, add 1 to it. The second parameter could be written as 18+1 or 19.
- [ ] `for n in range(12,36,6):
  print(n*2)`
- [ ] `for n in range(0,36+1,6):
  print(n)`

**Question 3**<br>
Which for loops will print all even numbers from 0 to 18? Select all that apply.
- [x] `for n in range(19):
    if n % 2 == 0:
        print(n)`
Correct! This loop will print all even numbers from 0 to 18. The range of “n” will start at 0 and end at 18 (the end range value of 19 is excluded). 
The variable  “n” will increment by the default of 1 in each iteration of the loop. The if statement uses the modulo operator (%) to test if the "n" variable is 
divisible by 2. If true, the if statement will print the value of "n" and exit back into the for loop for the next iteration of "n." 
- [ ] `for n in range(18+1):
  print(n**2)`
- [ ] `for n in range(0,18+1,2):
  print(n*2)`
- [x] `for n in range(10):
  print(n+n)`
Correct! This loop will print all even numbers from 0 to 18. The range of “n” will start at 0 and end at 9 (the end range value of 10 is excluded), 
with “n” incrementing by the default of 1 in each iteration of the loop. The format of (n+n), where n is an integer, is equivalent to the expression (n*2). 
This expression ensures the resulting integer will be an even number. The last iteration would print the result of the calculation 9+9.

**Question 4**<br>
Fill in the blanks so that the for loop will print the first 10 cube numbers `(x**3)` in a range that starts with `x=1` and ends with `x=10`.
```
for x in range(1,10+1):
  print(x**3)
```

**Question 5**<br>
Write a for loop with a three parameter range() function that prints the multiples of 7 between 0 and 100. 
Print one multiple per line and avoid printing any numbers that aren't multiples of 7. Remember that 0 is also a multiple of 7. 
```
for x in range(0,15): 
    print (x*7)
```

**Question 6**<br>
Which of these options would output just the vowels from the following string? Select all that apply.
input = "Four score and seven years ago"
- [x] `for c in input:
  if c.lower() in ['a', 'e', 'i', 'o', 'u']:
    print(c)`
Correct! You can use a for loop to examine each character in the string. Notice that using the function lower() enables you to find both uppercase and lowercase vowels.
- [x] `print([c for c in input if c.lower() in ['a', 'e', 'i', 'o', 'u']])`
Correct! You can use a list comprehension here to gather only the characters that match the conditional expression.
- [ ] `print(input.count("aeiou"))`
- [ ] `for c in range(len(input)):
  if c in ['a', 'e', 'i', 'o', 'u']:
    print(c)`

**Question 7**<br>
Which of these statements is true about slicing strings?
- [ ] The slice() method can be used to slice a string.
- [ ] If the starting index is negative, Python generates a runtime error.
- [x] If the starting index is negative, Python counts backward from the end of the string.
- [ ] When slicing a string, you must always provide both the starting and ending indexes.
