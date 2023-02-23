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


