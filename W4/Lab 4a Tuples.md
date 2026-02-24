# Lab 4a Tuples
## 1. Exercising Tuples
1a.
```python
value1=int(input("enter value1:"))
enter value1:10
value2=int(input("enter value2:"))
enter value2:20
value3=int(input("enter value3:"))
enter value3:30
value4=int(input("enter value4:"))
enter value4:40
value5=int(input("enter value5:"))
enter value5:50
my_tuple=(value1, value2, value3, value4, value5)
print(my_tuple)
(10, 20, 30, 40, 50)
```
1b. 
```python
tuple_single_element=(1, )
print(tuple_single_element)
(1,)
print(type(tuple_single_element))
<class 'tuple'>
```
1c.
```python
my_tuple = (1,2,3,4,3,2,1,2,3,5,4,3,2,1)
counts={ }
for number in my_tuple: #going through each item and calling it number
    if number in counts: 
        counts[number]+=1
    else:
        counts[number]=1        
print(counts)
{1: 3, 2: 4, 3: 4, 4: 2, 5: 1}
#generating dictionary
```
1d.
```python
my_tuple=my_tuple+my_tuple
print(hex(id(my_tuple)))
0x10992b230
my_tuple=(1,2,3,4,3,2,1,2,3,5,4,3,2,1)
print(hex(id(my_tuple)))
0x109f96fc0
```
Part c and part d of my_tuple are different because tuples are immutable, meaning the concatenation of my_tuple in part d will generate a new tuple because the orignal cannot be modified thus creating a new memeory address. 

1e. 
```python
x = (1,2,3,4)
x.append(1)
x[1] = "hello"
del x[2]
```
