# Functions
## Create a unit conversion program using functions
1a.
```python
def unit_conversion():
    answer=''
    while answer.lower()!='n':
        answer=input('run unit conversion?(y/n):').lower()
        if answer =='y':
            value=input('enter units of starting value(kpl/mpg):').lower()
            if value not in ['kpl','mpg']:
                print("invalid. please enter 'kpl' or 'mpg':")
                continue
            if value=='mpg':
                value_mpg=float(input("enter mpg value:"))
                result=value_mpg/2.35215
                print('mpg value in kpl is', result)
            elif value=='kpl':
                value_kpl=float(input("enter kpl value:"))
                result=value_kpl*2.35215
                print('kpl value in mpg is', result)
        elif answer=='n':
            print('Have a good day')
        else:
            print('rerun unit conversion?(y/n)')

            
unit_conversion()
run unit conversion?(y/n):y
enter units of starting value(kpl/mpg):mpg
enter mpg value:87
mpg value in kpl is 36.98743702569989
run unit conversion?(y/n):y
enter units of starting value(kpl/mpg):kpl
enter kpl value:87
kpl value in mpg is 204.63705
run unit conversion?(y/n):n
Have a good day
```
1b.
```python
def reverse(*args):
#used stackoverflow, searched "function unnamed argument" in which I found *args variable.
    for arg in args[::-1]:
        print(arg)

        
reverse(1,2,3,4)
4
3
2
1
```
1c.
```python
#operations that modify a list or dictionary would be visible outside of the functions such as .append, remove(), etc for list and .pop, update(), etc for dictionaries because the modification are being done to same obeject in memory.
def modify(patient_info):
    patient_info['age']='25'
patient={
    'name':'paola',
    'occupation':'researcher'
    }
modify(patient)
print(patient)
{'name': 'paola', 'occupation': 'researcher', 'age': '25'}
#to minimize the risk of changing the original list or dictionary, making a deepcopy preserves original list and generates a new list as you are no longer making the modification to the same object in memory but rather a different one due to the deep copy. 
```
1d.
```python
x=5
def funct_1():
    x=3
funct_1()
print(x)
5
# x=5 is a global variable. x=3 is a local variable in which it does not affect the global variable meaning x remains as 5. 
x=5
def funct_2():
    global x
    x=2
funct_2()   
print(x)
2
# global x allows for the modification of the global variable rather than generating a local variable inside of the function, thus, after calling the function, the global variable x is updated to 2. 
```
## Troubleshooting
2a. 
```python
def my_func(a,b,*c): #**c = keyword collecter *c=positional collector
    print(a,b,c)
  
my_func(1,2,3,4,5,6)
1 2 (3, 4, 5, 6)
# I fixed the error by assigning the rest of the values to c, meaning, 3,4,5,6 will now have a positonal arguments as a tuple and you will no longer obtain the error. 
```
2b.
```python
def my_func_global():
    global x
    x=100

    
x=10
my_func_global()
print(x)
100
#to modify, you must have the global x variable inside of the function and applied before the declaring x. In the original code, it was placed outside of the function so it did not apply any changes, and x=100 was coded as a local variable. 
```
