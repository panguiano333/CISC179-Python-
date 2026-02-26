# Lab 4b Dictionaries
## Creating and Accesing Dictionary
1a.
```python
my_dictionary={
    'name':'lab supplies',
    'item1':'flask',
    'item2':'pipete',
    'pipete_count':5,
    'item3':'lab notebook',
    'item4':'computer',
    'computer_count':10,
    'item5':'centrifuge',
    'item6':'waterproof pens',
    'pen_colors':['red','blue','black'],
    }
```
1b.
```python
my_user_dict={}
user_id=1 #storing users as numbers
while True:
    name=input('enter name:')
    age=input('enter age:')
    occupation=input('enter occupation:')
    my_user_dict[user_id]={
        'name':name,
        'age':age,
        'occupation':occupation
    }
    user_id+=1
    answer=''
    answer=input('do you want to continue (y/n):')
    if answer.lower()!='y':
        break

    
enter name:Paola
enter age:25
enter occupation:Researcher
do you want to continue (y/n):y
enter name:Amaya
enter age:24
enter occupation:PhD Student
do you want to continue (y/n):n
print(my_user_dict)
{1: {'name': 'Paola', 'age': '25', 'occupation': 'Researcher'}, 2: {'name': 'Amaya', 'age': '24', 'occupation': 'PhD Student'}}
```
You don't need any keys to create a dictionary as shown in my code, I started with an empty dictionary and filled out with user input. 
1c.
```python
```
1d.
```python
list_into_dict=[
    ('Name', 'Sarah Connor'),
    ('Date of birth', '1 Jan 1980'),
    ('Address', '1000 Black Mountain Drive', 92126),
    ('Name', 'Jim Hawkins')
]
my_dict={}
for items in list_into_dict:
    key=items[0] #identifying first element as key
    value=items[1] #identifying second element as the value
    if key in my_dict:
        print('repeated key:', key)
        new_key=input('enter new key:')
        key=new_key
    my_dict[key]=value

    
repeated key: Name
enter new key: name2
print(my_dict)
{'Name': 'Sarah Connor', 'Date of birth': '1 Jan 1980', 'Address': '1000 Black Mountain Drive', ' name2': 'Jim Hawkins'}
```
1e.
```python
```
## TroubleShooting
2a. 
```python
d_orig = {123:"Coconut"}
d_copy = d_orig.copy()
d_copy['123']='kiwi'
print(d_orig)
{123: 'Coconut'}
print(d_copy)
{123: 'Coconut', '123': 'kiwi'}
```
2b.



