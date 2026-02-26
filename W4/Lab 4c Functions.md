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


