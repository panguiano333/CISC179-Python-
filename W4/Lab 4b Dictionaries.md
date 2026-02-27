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
    key=items[0] 
    value=items[1] 
    my_dict[key]=value

print(my_dict)
{'Name': 'Jim Hawkins', 'Date of birth': '1 Jan 1980', 'Address': '1000 Black Mountain Drive'}
#turned list into a dictionary, but no validation for unique key, so the value of the repeated key "name", will replace the value of the first key. 
```
1e.
```python
text='The tiger (Panthera tigris) is a large cat and a member of the genus Panthera native to Asia. It has a powerful, muscular body with a large head and paws, a long tail and orange fur with black, mostly vertical stripes. It is traditionally classified into nine recent subspecies, though some recognise only two subspecies, mainland Asian tigers and the island tigers of the Sunda Islands.'
modified_text=text.replace('(','').replace(')','').replace('.','').replace(',','')
print(modified_text)
The tiger Panthera tigris is a large cat and a member of the genus Panthera native to Asia It has a powerful muscular body with a large head and paws a long tail and orange fur with black mostly vertical stripes It is traditionally classified into nine recent subspecies though some recognise only two subspecies mainland Asian tigers and the island tigers of the Sunda Islands
words=modified_text.split()
word_count={}
for word in words:
    if word in word_count:
        word_count[word]+=1
    else:
        word_count[word]=1

print(word_count)
{'The': 1, 'tiger': 1, 'Panthera': 2, 'tigris': 1, 'is': 2, 'a': 5, 'large': 2, 'cat': 1, 'and': 4, 'member': 1, 'of': 2, 'the': 3, 'genus': 1, 'native': 1, 'to': 1, 'Asia': 1, 'It': 2, 'has': 1, 'powerful': 1, 'muscular': 1, 'body': 1, 'with': 2, 'head': 1, 'paws': 1, 'long': 1, 'tail': 1, 'orange': 1, 'fur': 1, 'black': 1, 'mostly': 1, 'vertical': 1, 'stripes': 1, 'traditionally': 1, 'classified': 1, 'into': 1, 'nine': 1, 'recent': 1, 'subspecies': 2, 'though': 1, 'some': 1, 'recognise': 1, 'only': 1, 'two': 1, 'mainland': 1, 'Asian': 1, 'tigers': 2, 'island': 1, 'Sunda': 1, 'Islands': 1}
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
```python
#in the example, d_copy = d_orig, any change you make to one list the other one will mirror as both variables are the same dictionary in memory. To solve this, you must use shallow copy or deep copy, such as: 
import copy
d_orig = {123:"Coconut"}
d_copy=copy.deepcopy(d_orig)
d_copy['321']='kiwi'
print(d_orig)
{123: 'Coconut'}
print(d_copy)
{123: 'Coconut', '321': 'kiwi'}
```
2c.
```python
#it would give you an error message when using a list because they are mutable, and the application of hashing is suitable for exact-match inquiries.
my_list=["hello","hi","computer"]
hash(my_list)
Traceback (most recent call last):
  File "<pyshell#3>", line 1, in <module>
    hash(my_list)
TypeError: unhashable type: 'list'
```


