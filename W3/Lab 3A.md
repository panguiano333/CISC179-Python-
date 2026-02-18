#Lab 3A
1. Comparison Operators
```python
ord("`")
96
ord("~")
126
ord("!")
33
ord("1")
49
ord("@")
64
ord("2")
50
ord("3")
51
ord("#")
35
ord("4")
52
ord("$")
36
ord("5")
53
ord("6")
54
ord("^")
94
ord("7")
55
ord("&")
38
ord("8")
56
ord("*")
42
ord("9")
57
ord("(")
40
```
+ the rest of the keys in which they all have a unique identifier.

5. Problem Solving: Larger Number
```python
number1=int(input("enter the first number:"))
enter the first number:3
number2=int(input("enter the second number:"))
enter the second number:5
number3=int(input("enter the third number:"))
enter the third number:2
if number1>number2 and number1>number3:
    larger_number=number1
elif number2>number1 and number2>number3:
    larger_number=number2
else:
    larger_number=number3

    
print("The larger number is:", larger_number)
The larger number is: 5
```
5. Problem Solving Method 1: 
```python
value=int(input("enter a value:"))
enter a value:5
#approach1
if value%2==0:
    print("value is even")
else:
    print("value is odd")
value is odd
```
5. method 2:
```python
value=int(input("enter a value:"))
enter a value:5
if value & 1==1:
    print("value is odd")
else:
    print("value is even") 
value is odd
#bit number for 5 is 101, because it ends in 1, number is odd.
```
5C. grading scheme
```python
grade=int(input("input grade:"))
input grade:95
if grade >= 90:
    print("Grade: A", "Description: Work of genuinely superior quality.")
elif (grade >= 80) and (grade<=89):
    print("Grade: B", "Description: Passing performance falls approximately in the upper distribution of passing grades.")
elif (grade >= 71) and (grade<=79):
    print("Grade: C", "Description: Passing performance falls approximately in the center of the distribution of all passing grades.")
elif (grade >=65) and (grade <=70):
    print("Grade: D", "Description: Passing performance falls approximately in the lower distribution of passing grades.")
else:
    print("grade: F", "Failing performance that does not satisfy the basic requirements of the course and needs to be improved in significant ways.")   
Grade: A Description: Work of genuinely superior quality.
```
5D. Truth Table
```python

5E.
```python
value=int(input("enter a value:"))
enter a value:10
if value & 1==1:
    print("value is odd")
else:
    print("value is even") 
value is even
#bit number for 10 is 1010, because it ends in 1, number is odd, and even if it ends in 0. 
```
6. Code Revision
```python
name = input("What's your name? ")
What's your name? paola
time = int(input("What time is it? "))
What time is it? 1500
if (time < 1200):
    print("Hi "+name + ", good morning!")
elif (time < 1800):
    print("Hi "+name + ", good afternoon!")
elif (time > 1800):
    print("Hi "+name + ", good evening!")
else:
    print("Good Bye")   
Hi paola, good afternoon!
```
7. Output Verification
```python
x = 1
y = 1.0
z = "1"

if x == y:
    print("one")
if y == int(z): 
    print("two")
elif x == y: #repeated statement
    print("three")
else:
    print("four")
#output would be one because the first statement is true, meaning python will not continue with the rest of the conditions despite the fact that the next 2 statements are also true.
```

  
