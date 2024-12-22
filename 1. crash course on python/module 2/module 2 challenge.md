1. Complete the code to output the statement, “192.168.1.10 is the IP address of Printer Server 1”. Remember that precise syntax must be used to receive credit.
```
IP_address = "192.168.1.10"
host_name = "Printer Server 1"
print(IP_address + " is the IP address of " + host_name)
# Should print "192.168.1.10 is the IP address of Printer Server 1"
```

2. What’s the value of this Python expression: 7 < "number"?
- [ ] True
- [ ] False
- [x] TypeError
- [ ] 0

3. In the following code, what would be the output?
```
number = 4
if number * 4 < 15:
 print(number / 4)
elif number < 5:
 print(number + 3)
else:
 print(number * 2 % 5)
```
- [ ] 3
- [x] 7
- [ ] 4
- [ ] 1

4. Consider the following scenario about using if-elif-else statements:
The fall weather is unpredictable.  If the temperature is 32 degrees Fahrenheit or below, a heavy coat should be worn.  
If it is above 32 degrees but not above 50 degrees, then a jacket should be sufficient.  
If it is above 50 but not above 65 degrees, a sweatshirt is appropriate, and above 65 degrees a t-shirt can be worn.  
Fill in the blanks in the function below so it returns the proper clothing type for the temperature.
```
def clothing_type(temp):
    if temp > 65:
        clothing = "T-Shirt"
    elif 50 < temp <= 65:
        clothing = "Sweatshirt"
    elif 32 < temp <= 50:
        clothing = "Jacket"
    else:
        clothing = "Heavy Coat"
    return clothing


print(clothing_type(72)) # Should print T-Shirt
print(clothing_type(55)) # Should print Sweatshirt
print(clothing_type(65)) # Should print Sweatshirt
print(clothing_type(50)) # Should print Jacket
print(clothing_type(45)) # Should print Jacket
print(clothing_type(32)) # Should print Heavy Coat
print(clothing_type(0)) # Should print Heavy Coat
```

5. In the following code, what would be the output?
```
test_num = 12
if test_num > 15:
    print(test_num / 4)
else:
    print(test_num + 3)
```
- [x] 15
- [ ] 12
- [ ] 4
- [ ] 3

6. Fill in the blanks to complete the function. The “complementary_color” function receives a primary color name in all lower case, then prints its 
complementary color. Currently, the function only supports the primary colors of red, yellow, and blue. It returns "unknown" for all other colors or if 
the word has any uppercase characters.
```
def complementary_color(color):
    if color == "blue":
        complement = "orange"
    elif color == "yellow":
        complement = "purple"
    elif color == "red":
        complement = "green"
    else:
        complement = "unknown"
    return complement

print(complementary_color("blue")) # Should print orange
print(complementary_color("yellow")) # Should print purple
print(complementary_color("red")) # Should print green
print(complementary_color("black")) # Should print unknown
print(complementary_color("Blue")) # Should print unknown
print(complementary_color("")) # Should print unknown
```

7. Can you calculate the output of this code?
```
def greater_value(x, y):
    if x > y:
        return x
    else:
       return y
print(greater_value(10,3*5))
```
> 15

8. What's the value of this Python expression?
```
((10 >= 5*2) and (10 <= 5*2))
```
- [x] True
- [ ] False
- [ ] 10
- [ ] 5*2

9. Fill in the blanks to complete the function. The “make_positive” function takes in a number and converts that number to its positive equivalent.  
Complete the function to accomplish the following tasks:
-use an if statement to test if the number is negative;
-use a calculation inside the if statement to change the negative number to be positive;
-use a calculation in the else statement to return any positive “number” unchanged.
```
def make_positive(number):
    if number < 0:
        result = number * -1 
    else:
        result = number
    return result

print(make_positive(-4))   # Should print 4
print(make_positive(0))    # Should print 0
print(make_positive(-.25)) # Should print 0.25
print(make_positive(5))    # Should print 5
```

10. Which of the following are good coding-style habits? Select all that apply.
- [x] Adding comments
- [x] Refactoring the code
- [ ] Writing code using the least amount of characters as possible
- [x] Cleaning up duplicate code by creating a function that can be reused
