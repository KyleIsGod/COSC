# Python
# Type Casting
```
str(float(myvar))
Mynewvariable = str(float(myvar))
int(myvar)
float(myvar)
```
# Math signs
```
/ - divide float 30 / 10 = 3.0
// - divide integer 30 // 10 = 3
+ - addition
- is subtraction
* - multiplication
** - exponent (for example 2 ** 2 is 4 and 2 ** 3 is 8)
% - gives left over (for example 30 % 8 is 6 because 8 goes into 30 3 times with 6 being remaining)
```
# Legacy activities

# Part 1
def invert(l):
    Inverts the given list
    Args:
        l (list): list of strings representing integers in the range [0-255]
    Returns:
        None
    
    

def inverted(l):
    Returns a new list that is the given list inverted
    Args:
        l (list): list of strings representing integers in the range [0-255]
    Returns:
        list: new list that is the given list inverted
    

```
def invert(l):
     x = 0
     for i in l:
         l[x] = str(255 - int(i))
         x += 1
         print(l)
     
     pass
 
 def inverted(l):
     random = []
     for i in l:
         random.append(str(255 - int(i)))
     return(random)
 
 
 
     pass
 
 if __name__ == '__main__':
     pass
```
Seperate method
```
for item in range(0,len(l)):
  l[item] = str(255 - int(l[item]))
  
  
return [str(255 - int(i)) for i in l]
```
# Boolean Expressions
```
Equal to is ==
Not equal to is !=
Less than is <
Less than or equal to <=
Greater than >
Greater than or equal to >=
Value in collection is “in”
Object id match “is”
And is both have to be true
8 < 10 and 5 == 5
true
OR only one has to be true
8 > 10 or 5 == 5
true
```
# .format
```
	#!/usr/bin/python3
	
	Name = “LCpl Aycock”
	Age = “19”
	print(f”Hello {name} you are {age} years old!”)


	Name = input(“Please enter your name: “)
	Age = input(“Please enter your age:” )
	print(f”Hello {name} you are {age} years old!”)

	int(input(“Enter a number: “))
```

# If and ELIF statement
```
#!/usr/bin/python3

Age = int(input(“What is your age?: “))

If age >= 21:
	print(“You can drink!”)
Elif age < 21:
	print (“Sorry too young!”)
Elif age == 19:
	print(“Close but no cigar”) - This would not be calculated due to being more specific and the needs of age 19 will have been met with the up above elif function. For this to be useful place more specific functions above the more broad ones. 
```

# EXERCISE EXAMPLE:
```
number = int(input("Please enter a number: "))

if number < 0 and number % 2 == 0:
    print("Negative Even")
elif number < 0 and number % 2 != 0:
    print("Negative Odd")
if number == 0:
    print("Zero")
if number > 0 and number % 2 == 0:
    print("Positive Even")
elif number > 0 and number % 2 != 0:
    print("Positive Odd")
```







```
def guess_number(n):
    
    while True:
        number = int(input("Please enter a number between 0-100: "))
        if n > number and number > 0:
            print("too low")
        elif n < number and number < 100:
            print("too high")
        elif n == number:
            print("win")
            break
        else:
            pass

guess_number(23)
```

# Replacing and splitting
```
Test = email.replace(“@”,”.”)
Lst = test.split(“.”)
```







# Defining a function
```
Def multiply(a,b): - this is defining the function to be used later
	print(a * b)
Myvar1 =  int(input(“provide first number: “))
Myvar2 = int(input(“provide second number: “))

multiply(myvar1,myvar2) - This is calling the function to be used
```

# FOR LOOPS:
```
List = [1,3,5,7]	
For item in List:
	print(item)
```
```
myStr = “The dog jumped the fence
For item in myStr:
	print(item)
```
# WHILE LOOPS:
```
While 5 == 5:
	print(“I’m here forever”)
```
```
i = 0 
While i < 10:
	print (i)
	i += 1
```
```
While 5 == 5:
	If 5 == 5:
		Break
```
If using a while “true” you must have a break statement somewhere. Whether its an if, break, or the condition to make it false is possible.


# RANGE:

list(range(0,10)) START, STOP, STEP will never give the last number. Only up to.
	[0,1,2,3,4,5,6,7,8,9]

For example
list(range(0,10,5))
	[0,5]

myRange = range(0,10,2)
For item in myRange:
	print(item)


# LIST SLICING:

myList = list(range(0,100))
myList
[0,-99]

myList[0:5:1]
Pulls out first 5 items

myList[0:10]
Pulls out first 10 items

myList[0:10:2]
Pulls out first 10 but in intervals of 2

myList[::-1]
Goes backwards and lists it

newList = [item for item in range(0,100) if item % 2 == 0

# Codewars good to know problems

## Problem one

Build a function that returns an array of integers from n to 1 where n>0.

Example : n=5 --> [5,4,3,2,1]
```
def reverse_seq(n):
    l = []
    y =[]
    for i in range(1,n+1):
        l.append(i)
        
    y = l[::-1]
    return y
```







# Practice exam one QnAs

## Question one
Option one:

Given the floatstr, which is a comma separated string of floats, return a list with each of the floats in the argument as elements in the list.

The premace of this is to split the string on the commas and using split turns the string into a list, you are then taking every item of that list and making it a float and adding it to the new list you created. Creating a new list of floats instead of a string of floats
``` 
def q1(floatstr):
    newlist = []
    for item in floatstr.split(','):
        newlist.append(float(item))
    return newlist
```
Option two: List comprehension
```
return [float(x) fopr x in floatstr.split(',')]
```
Option three: Map function
```
return list(list(map(float,floatstr.split(',')))
```
## Question two
Option one:

Given the variable length argument list, return the average of all the arguments as a float

Adding every single number in "args" to the variable "result" and then diving by the length of args one / for float two // for int
```
def q1(*args):
    result = 0
    for i in args:
      result += i
      ave_num = result / len(args)
    return ave_num
```
## Question three
Option one:

Given a list (lst) and a number of items (n), return a new list containing the last n entries in lst.

Takes the number of items (n) and takes that value and gets the last "n" slots from lst
```
def q1(lst,n):
    newlst = lst[-n:]
    return newlst
```
## Question four
Option one:

Given an input string, return a list containing the ordinal numbers of each character in the string in the order found in the input string.

taking every single element of the list and ording it, adding it to a new list, then prinitng the new list
```
def q1(strng):
    newlst = []
    for i in strng:
        newlst.append(ord(i))
    return newlst
```
Option two: List comprehension

```
return [ord(x) for x in list(strng)]
```
## Question five 
Option one:

Given an input string, return a tuple with each element in the tuple containing a single word from the input string in order.

```
def q1(strng):
    return tuple(strng.split())
```

## Question six
Given a dictionary (catalog) whose keys are product names and values are product prices per unit and a list of tuples (order) of product names and quantities, compute and return the total value of the order.

Example catalog:

{
'AMD Ryzen 5 5600X': 289.99,
'Intel Core i9-9900K': 363.50,
'AMD Ryzen 9 5900X': 569.99
}
Example order:

[
('AMD Ryzen 5 5600X', 5), 
('Intel Core i9-9900K', 3)
]
Example result:

2540.45

How the above result was computed:

(289.99 * 5) + (363.50 * 3)
```
def q6(catalog, order):
    total = []
    for key in catalog:
        for item in order:
            if item[0] == key:
                total.append(catalog[key] * item[1])
    return sum(total)
```
Option two:
```
def q6(catalog, order):
	total = 0
	for product, quantity in order:
		total += catalog[product] * quantity
	return total
```
Option three:
```
def q6(catalog, order):
	return sum(catalog[product]*quantity for product,quantity in order)
```
## Question seven
Option one: 

Given a filename, open the file and return the length of the first line in the file excluding the line terminator.

x reads the first line, y takes the length of it and subtracts one for the line terminator. 
```
with open(filename) as fp:
	x = fp.readline()
	y = len(x) -1
	return y
```

## Question eight

Given a filename and a list, write each entry from the list to the file on separate lines until a case-insensitive entry of "stop" is found in the list. If "stop" is not found in the list, write the entire list to the file on separate lines.

```
def q1(filename,lst):
	with open(filename, 'w') as fp:
		for item in lst:
			if item.lower() == 'stop':
				break
			fp.write(f'{item}\n')
```

## Question nine

Given the military time in the argument miltime, return a string containing the greeting of the day.

```
def q1(miltime):
    if miltime >= 301 and miltime < 1200:
        return "Good Morning"
    elif miltime >= 1200 and miltime < 1600:
        return "Good Afternoon"
    elif miltime >= 1600 and miltime < 2100:
        return "Good Evening"
    elif miltime >= 2100 or miltime < 300:
        return "Good Night"
```

## Question ten

Given the argument numlist as a list of numbers, return True if all numbers in the list are NOT negative. If any numbers in the list are negative, return False.

```
def q1(numlist):
    for i in numlist:
        if i > 0:
            return True
        else:
            return False
```

# Exam two QnAs

## Question one
Given a string of multiple words separated by single spaces, return a new string with the sentence reversed. The words themselves should remain as they are
For example, given 'it is accepted as a masterpiece on strategy', the returned string should be 'strategy on masterpiece a as accepted is it'.
```
def q1(sentence):
    s = sentence.split()[::-1]
    l = []
    for i in s:
        l.append(i)
    return(" ".join(l))
```
## Question two
Given a positive integer, return its string representation with commas seperating groups of 3 digits.

For example, given 65535 the returned string should be '65,535'.
```
def q1(n):
    return(f"{n:,d}")
```
## Question three
Given two lists of integers, return a sorted list that contains all integers from both lists in descending order.

For example, given [3,4,9] and [8,1,5] the returned list should be [9,8,5,4,3,1]. The returned list may contain duplicates.
```
def q1(lst0, lst1):
    L = lst0 + lst1
    test = sorted(L)
    return test[::-1]
```
## Question four
Given 3 scores in the range [0-100] inclusive, return 'GO' if the average score is greater than 50. Otherwise return 'NOGO'.
```
def q1(s1,s2,s3):
    sum = s1 + s2 + s3
    if sum / 3 > 50:
        return "GO"
    else:
        return "NOGO"
```

## Question five
Given an integer and limit, return a list of even multiples of the integer up to and including the limit.

For example, if integer = 3 and limit = 30, the returned list should be [0,6,12,18,24,30]. Note, 0 is a multiple of any integer except 0 itself.
```
def q1(integer, limit):
    test = []
    x = 0
    while x <= limit:
        if x % 2 == 0:
            test.append(x)
        x += integer
    return test
```

## Question six
Given two filenames, return a list whose elements consist of line numbers for which the two files differ. The first line is considered line 0.

```
def q1(f0, f1):
    diffs = []
    linenumber = 0
    with open (f0) as file1, open(f1) as file2:
        for l0,l1 in zip (file1,file2):
            if l0 != l1:
                diffs.append(linenumber)
            linenumber += 1
        return diffs
```
## Question seven
As you iterate through the given list, return the first duplicate value you come across.

For example, if given [5,7,9,1,3,7,9,5], the returned value should be 7.
```
def q1(lst):
    seen = set()
    for i in lst:
        if i in seen:
            return i
        seen.add(i)

    return -1
```
Option two:
```
def q1(lst):
	seen = set()
	for i in lst:
		if i in seen:
			return i
		else:
			seen.add(i)
```
## Question eight
Given a sentence as a string with words being separated by a single space, return the length of the shortest word.

```
def q1(strng):
    test = []
    list = strng.split(' ')
    for i in list:
        test.append(len(i))
    return min(test)
```
```
def q1(strng):
return len(min(strng.split(), key=len))
```

## Question nine
Given an alphanumeric string, return the character whose ascii value is that of the integer represenation of all of the digits in the string concatenated in the order in which they appear.

For example, given 'hell9oworld7', the returned character should be 'a' which has the ascii value of 97.
```
def q1(strng):
    true = []
    for i in strng:
        if i.isdigit() == True:
            true.append(i)
        if i.isdigit() == False:
            pass
    test = chr(int(''.join(true)))
    return test
```
```
def q1(strng):
	chars = []
	for c in strng:
		if c.isdigit():
			chars.append(c)
	return chr(int(''.join(chars)))
```
## Question ten
Given a list of positive integers sorted in ascending order, return the first non-consecutive value. If all values are consecutive, return None.

For example, given [1,2,3,4,6,7], the returned value should be 6.
```
def q1(arr):
    i = 1
    for x in arr:
        if i < len(arr) and arr[i] - arr[i-1] != 1:
            return arr[i]
        i += 1
    return None
```

# Runestone questions

## Question one
The textfile, travel_plans.txt, contains the summer travel plans for someone with some commentary. Find the total number of characters in the file and save to the variable num.

```
with open('travel_plans.txt') as fp:
    test = str(len(fp.read()))
    num = int(test)
    print(num)
```

## Question two
We have provided a file called emotion_words.txt that contains lines of words that describe emotions. Find the total number of words in the file and assign this value to the variable num_words.
```
num_words = 0
with open('emotion_words.txt') as fp:
    for line in fp:
        words = line.split()
        num_words += len(words)
print("Number of words:")
print(num_words)
```

## Question three
Assign to the variable num_lines the number of lines in the file school_prompt.txt.
```
with open('school_prompt.txt') as fp:
    num_lines = len(fp.readlines())
    print(num_lines)
```

## Question four
Assign the first 30 characters of school_prompt.txt as a string to the variable beginning_chars.
```
with open('school_prompt.txt') as fp:
    beginning_chars = fp.read(30)
```

## Question five
Using the file school_prompt.txt, assign the third word of every line to a list called three.
```
three = []
with open('school_prompt.txt') as fp:
    for i in fp.readlines():
        three.append(i.split()[2])
```

## Question six
Create a list called emotions that contains the first word of every line in emotion_words.txt
```
with open('emotion_words.txt') as fp:
    
    list = fp.readlines()
tmp = ""
word = ""
emotions = []
for i in list:
    word = ''.join(i)
    tmp = word.split()
    emotions.append(tmp[0])
    print(emotions)
```

## Question seven
Assign the first 33 characters from the textfile, travel_plans.txt to the variable first_chars
```
with open('travel_plans.txt') as fp:
    first_chars = fp.read(33)
```
## Question eight
Using the file school_prompt.txt, if the character ‘p’ is in a word, then add the word to a list called p_words
```
p_words = []
with open('school_prompt.txt') as fp:
    lines = fp.read()
    for i in lines.split():
        if 'p' in i:
            p_words.append(i)
```


