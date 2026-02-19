# Lab 3B 
(fyi: the comments are notes for myself)
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
