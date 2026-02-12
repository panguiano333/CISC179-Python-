# Lab 2b
```python
print(5+2-2)
5
print(5/2)
2.5
print(6//2)
3
print(2.*3)
6.0
print(2<4)
True
print(2=>2)
SyntaxError: expression cannot contain assignment, perhaps you meant "=="?
print(2>=2)
True
print("Hello"+"World")
HelloWorld
print("bla"*3)
blablabla
print(2*3*33)
198
print(2*3*3)
18
print(5 * 25 // 13 + 100 / 2 % 13 // 2)
14.0
print(6%5)
1
print((2 % -4), (2 % 4), (2 ** 3 ** 2))
-2 2 512


type("hello")
<class 'str'>
type(1+"2")
Traceback (most recent call last):
  File "<pyshell#17>", line 1, in <module>
    type(1+"2")
TypeError: unsupported operand type(s) for +: 'int' and 'str'
type(True)
<class 'bool'>
type("False")
<class 'str'>


print(-10+2*2//7+6.5**2/6)
-2.958333333333333
```

# Work without Python
## 1. Literals
### 125 // 13 + 100 / 2 % 13 // 2
###    9  + 100 / 2 % 13 // 2
###    9 + 50 % 13 // 2 
###    9 + 11 // 2
###	  9 + 5 = 14
## 3. Operator Precedence
### -10 + 2 * 2 // 7 + 6.5 ** 2 / 6
### -10 + 2 * 2 // 7 + 42.25 / 6
### -10 + 4 //7 + 42.25 / 6
### -10 + 0  + 42.25 / 6
### -10 + 7.04 = -2.9583

## Challenges 
I made the same mistake for 2 % -4 and 2 % 4, I had to do some research on why I got this wrong and it's because I didn’t apply “floor” so for 2%4=-0.5 , applying floor would be -1 and 2%4=1. 
