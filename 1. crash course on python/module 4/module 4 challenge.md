**Question 1**<br>
The format of the input variable “address_string” is: numeric house number, followed by the street name which may contain numbers and could be several words long 
(e.g., "123 Main Street", "1001 1st Ave", or "55 North Center Drive"). 
Complete the string methods needed in this function so that input like "123 Main Street" will produce the output "House number 123 on a street named Main Street". 
This function should:
1. accept a string through the parameters of the function;
2. separate the address string into new strings: house_number and street_name; 
3. return the variables in the string format: "House number X on a street named Y". 
```
def format_address(address_string):
    house_number = ""
    street_name = ""
    # Separate the house number from the street name.
    address_parts = address_string.split()
    
    for address_part in address_parts:
       # Complete the if-statement with a string method.  
       if address_part.isdigit():
         house_number = address_part
       else:
         street_name += address_part + " "
    # Remove the extra space at the end of the last "street_name".
    street_name = street_name.strip()
 
    # Use a string method to return the required formatted string.
    return "House number {} on a street named {}".format(house_number, street_name)

print(format_address("123 Main Street"))
# Should print: "House number 123 on a street named Main Street"

print(format_address("1001 1st Ave"))
# Should print: "House number 1001 on a street named 1st Ave"

print(format_address("55 North Center Drive"))
# Should print "House number 55 on a street named North Center Drive"
```

**Question 2**<br>
Fill in the blank to complete the “highlight_word” function. This function should change the given “word” to its upper-case version in a given “sentence”. 
Complete the string method needed in this function so that a function call like "highlight_word("Have a nice day", "nice")" will return the output 
"Have a NICE day".
```
def highlight_word(sentence, word):
    # Complete the return statement using a string method.
    return sentence.replace(word, word.upper())

print(highlight_word("Have a nice day", "nice"))
# Should print: "Have a NICE day"
print(highlight_word("Shhh, don't be so loud!", "loud"))
# Should print: "Shhh, don't be so LOUD!"
print(highlight_word("Automating with Python is fun", "fun"))
# Should print: "Automating with Python is FUN"
```

**Question 3**<br>
Consider the following scenario about using Python lists: 
A professor gave his two assistants, Jaime and Drew, the task of keeping an attendance list of students in the order they arrive in the classroom. 
Drew was the first one to note which students arrived, and then Jaime took over. After the class, they each entered their lists into the computer and 
emailed them to the professor. The professor wants to combine the two lists into one, in the order of each student's arrival. Jaime emailed a follow-up, 
saying that her list is in reverse order. 
Complete the code to combine the two lists into one in the order of: the contents of Drew's list, followed by Jaime’s list in reverse order, 
to produce an accurate list of the students as they arrived. This function should: 
1. accept two lists through the function’s parameters;
2. reverse the order of “list1”; 
3. combine the two lists so that “list2” comes first, followed by “list1”;
4. return the new list. 
```
def combine_lists(list1, list2):
  combined_list = [] # Initialize an empty list variable
  list1.reverse() # Reverse the order of "list1"
  combined_list = list2 + list1 # Combine the two lists 
  return combined_list  
  
Jaimes_list = ["Alma", "Chika", "Benjamin", "Jocelyn", "Oakley"]
Drews_list = ["Minna", "Carol", "Gunnar", "Malena"]

print(combine_lists(Jaimes_list, Drews_list))
# Should print ['Minna', 'Carol', 'Gunnar', 'Malena', 'Oakley', 'Jocelyn', 'Benjamin', 'Chika', 'Alma']
```

**Question 4**<br>
Fill in the blank to complete the “even_numbers” function. This function should use a list comprehension to create a list of even numbers using a conditional 
if statement with the modulo operator to test for numbers evenly divisible by 2. The function receives two variables and should return the list of even numbers 
that occur between the “first” and “last” variables exclusively (meaning don’t modify the default behavior of the range to exclude the “end” value in the range).
For example, even_numbers(2, 7) should return [2, 4, 6].  
```
def even_numbers(first, last):
  return [x for x in range (first, last+1) if x % 2 == 0]


print(even_numbers(4, 14)) # Should print [4, 6, 8, 10, 12]
print(even_numbers(0, 9))  # Should print [0, 2, 4, 6, 8]
print(even_numbers(2, 7))  # Should print [2, 4, 6]
```

**Question 5**<br>
Fill in the blanks to complete the “endangered_animals” function. This function accepts a dictionary containing a list of endangered animals (keys) and 
their remaining population (values).  For each key in the given “animal_dict” dictionary, format a string to print the name of the animal, 
with one animal name per line.
```
def endangered_animals(animal_dict):
    result = ""
    # Complete the for loop to iterate through the key and value items 
    # in the dictionary.    
    for animal in animal_dict.keys(): 
        # Use a string method to format the required string.
        result += animal + "\n"
    return result
print(endangered_animals({"Javan Rhinoceros":60, "Vaquita":10, "Mountain Gorilla":200, "Tiger":500}))

# Should print:
# Javan Rhinoceros
# Vaquita
# Mountain Gorilla
# Tiger
```

**Question 6**<br>
Consider the following scenario about using Python dictionaries: 
Tessa and Rick are hosting a party. Both sent out invitations to their friends, and each one collected responses into dictionaries, with names of their 
friends and how many guests each friend was bringing. Each dictionary is a partial guest list, but Rick's guest list has more current information about 
the number of guests. 
Complete the function to combine both dictionaries into one, with each friend listed only once, and the number of guests from Rick's dictionary taking precedence, 
if a name is included in both dictionaries. Then print the resulting dictionary. This function should:
1. accept two dictionaries through the function’s parameters;
2. combine both dictionaries into one, with each key listed only once;
3. the values from the “guests1” dictionary taking precedence, if a key is included in both dictionaries;
4. then print the new dictionary of combined items.
```
def combine_guests(guests1, guests2):
  guests2.update(guests1) # Use a dictionary method to combine the dictionaries.
  return guests2

Ricks_guests = { "Adam":2, "Camila":3, "David":1, "Jamal":3, "Charley":2, "Titus":1, "Raj":4}
Tessas_guests = { "David":4, "Noemi":1, "Raj":2, "Adam":1, "Sakira":3, "Chidi":5}

print(combine_guests(Ricks_guests, Tessas_guests))
# Should print:
# {'David': 1, 'Noemi': 1, 'Raj': 4, 'Adam': 2, 'Sakira': 3, 'Chidi': 5, 'Camila': 3, 'Jamal': 3, 'Charley': 2, 'Titus': 1}
```

**Question 7**<br>
Use a dictionary to count the frequency of numbers in the given “text” string. Only numbers should be counted. Do not count blank spaces, letters, or punctuation. 
Complete the function so that input like "1001000111101" will return a dictionary that holds the count of each number that occurs in the string  {'1': 7, '0': 6}.
This function should: 
1. accept a string “text” variable through the function’s parameters;
2. initialize an new dictionary;
3. iterate over each text character to check if the character is a number’
4. count the frequency of numbers in the input string, ignoring all other characters;
5. populate the new dictionary with the numbers as keys, ensuring each key is unique, and assign the value for each key with the count of that number;
6. return the new dictionary.
```
def count_numbers(text):
  # Initialize a new dictionary.
  dictionary = {} 
  # Complete the for loop to iterate through each "text" character.
  for character in text:
    # Complete the if-statement using a string method to check if the
    # character is a number.
    if character.isdigit():
      # Complete the if-statement using a logical operator to check if 
      # the number is not already in the dictionary.
      if character not in dictionary:
           # Use a dictionary operation to add the number as a key
           # and set the initial count value to zero.
           dictionary[character] = 0
      # Use a dictionary operation to increment the number count value 
      # for the existing key.
      dictionary[character] += 1
  return dictionary

print(count_numbers("1001000111101"))
# Should be {'1': 7, '0': 6}

print(count_numbers("Math is fun! 2+2=4"))
# Should be {'2': 2, '4': 1}

print(count_numbers("This is a sentence."))
# Should be {}

print(count_numbers("55 North Center Drive"))
# Should be {'5': 2}
```

**Question 8**<br>
What do the following commands return when animal = "Hippopotamus"?
```
print(animal[3:6])
print(animal[-5])
print(animal[10:])
```
- [x] pop, t, us
- [ ] popo, t, mus
- [ ] ppo, t, mus
- [ ] ppop, o, s

**Question 9**<br>
What does the list "car_makes" contain after these commands are executed?
```
car_makes = ["Ford", "Volkswagen", "Toyota"]
car_makes.remove("Ford")
```
- [ ] ['', 'Porsche', 'Vokswagen', 'Toyota']
- [x] ['Volkswagen', 'Toyota']
- [ ] [null, 'Porsche', 'Toyota']
- [ ] ['Toyota', 'Ford']

**Question 10**<br>
What do the following commands return?
```
teacher_names = {"Math": "Aniyah Cook", "Science": "Ines Bisset", "Engineering": "Wayne Branon"}
teacher_names.values()
```
- [ ] ['Aniyah Cook', 'Ines Bisset', 'Wayne Branon'']
- [ ] {"Math": "Aniyah Cook","Science": "Ines Bisset", "Engineering": "Wayne Branon"}
- [ ] ["Math", "Aniyah Cook", "Science", "Ines Bisset", "Engineering", "Wayne Branon"]
- [x] dict_values(['Aniyah Cook', 'Ines Bisset', 'Wayne Branon'])
