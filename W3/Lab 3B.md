# Lab 3B 

1A. While Loop
```python
n0=16
if n0<=0:
    print("number must be non-negative and non-zero int")
else:
    print(n0)#prints starting number first 
    while n0!=1: #boolean condition, n0 is not 1. once reaches 1 condition becomes false and the loops stops.
        if n0&1==0:
            n0=n0//2
        else:
            n0=3*n0+1
        print(n0)#inside, prints each number
       
8
4
2
1
```
1B.
```python
n0=16
if n0<=0:
    print("number must be non-negative and non-zero int")
else:
    print(n0)#prints starting number first 
    while n0!=1: #boolean condition, n0 is not 1. once reaches 1 condition becomes false and the loops stops.
        if n0&1==0:
            n0=n0//2
        else:
            n0=3*n0+1
        print(n0)#inside, prints each number
        if n0==1:
          break 
       
8
4
2
1
```
1C.
```python
value1=int(input("enter value1:"))
enter value1:3
value2=int(input("enter value2:"))
enter value2:8
print("arithmetic operation options:")
arithmetic operation options:
print("+")
+
print("-")
-
print("*")
*
print("/")
/
answer=""
while answer.lower()!="no": #must add for case sensitivity
    print("run arithmetic operation yes or no?:") 
    answer=input("type yes or no:").lower()
    if answer=="yes":
        choose_option=input("select arithmetic operation:")
        if choose_option=="+":
            result=value1+value2
            print(result)
        elif choose_option=="-":
            result=value1-value2
            print(result)
        elif choose_option=="*":
            result=value1*value2
            print(result)
        elif choose_option=="/":
            if value2 !=0:
                result=value1/value2
                print(result)
            else:
                print("re-input value2 for a non-zero value")
    elif answer=="no":
        print("have a good day")
        break
    else:
        print("redo arithmetic operation? yes or no")

        
run arithmetic operation yes or no?:
type yes or no:yes
select arithmetic operation:-
-5
run arithmetic operation yes or no?:
type yes or no:no
have a good day
```
2. For Loops
```python
phrase="to be or not to be"
total_letters=0
for char in phrase:
    if char >="a" and char <="z":
        total_letters=total_letters+1

        
print(total_letters)
13
```
