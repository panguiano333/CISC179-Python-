# Lab 2c

# Variable Memory Usage
```python
var1=10
print(hex(id(var1)))
0x10a9804e8
var1=100
print(hex(id(var1)))
0x10a981028
```
Python generated a different address because it stores different values in different memory blocks even if the variable is the same. 
The first value is still kepted as a different memory address and its store in case you need to use 
the value 10 but var1 will be shown as 100. 

```python
var2=100
print(hex(id(var2)))
0x10a981028
```
It generated the same memory address as var1=100 because it python had already generated a memoru block for the value of 100

# Memory Map

| Address in hexadecimal | Char |
| ---------------------- | ---- |
| # 0x10a990398          |  H   |
| # 0x10a990908          |  E   |
| # 0x10a990a58          |  L   |
| # 0x10a990a58          |  L   |
| # 0x10a990ae8          |  O   |
| # 0x10a990668          |  W   |
| # 0x10a990ae8          |  O   |
| # 0x10a990b78          |  R   |
| # 0x10a990a58          |  L   |
| # 0x10a9908d8          |  D   |

# Problem Solving
- x+y = dogcat
- cannot be solved because you can't concatenate to a string without another string.
- dogdogdogdog
```python
x=50
y=1
print(x+y)
51
```
# Troubleshooting
- Choosing the same variable and value might not be the best idea because it can get confusing but it is a valid variable name
- valid variable name because it can start with a letter or underscore
- not valid because special characters are not allowed
- not valid, you cannot use keywords as varaible names
- not valid, you cannot use keywords as varaible names

# Challenges
- I am not super confident with the problem solving portion becuase im not sure if words can be accepted as a value without being a string. 
