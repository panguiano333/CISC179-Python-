# Child Vaccination Chart
## Code
```python
patient_dict={} 
def insert(patient_info):
    for patient in patient_info:
        patient_id=patient['id']
        patient_dict[patient_id]=patient #adds to dict. with new patient id
        first_name=patient['first name']
        last_name=patient['last name']
        print('ID:', patient_id, first_name, last_name)
        for name, months in patient['vacc months'].items(): #need patient[] to access the information of each vaccine, using .item, i am assignng name to key and months to value
            print('Vacc. Name:', name, ', Administration(mos):', months)
        for name, annual in patient['vacc annual'].items():
            print('Vacc. Name:', name, ', Administration(mos):', annual)

            
new_patient=[{'id': 'R003',
             'first name': 'Paola',
             'last name': 'Quiroz',
             'vacc months':{'HepB':{0,2,6},
                           'RV':{2,4,6},
                           'DTap':{2,4,6,15},
                           'Hib':{2,4,9,12},
                           'PCV13':{2,4,6,12},
                           'IPV':{2,3,6}},
            'vacc annual':{'MMR':12,
                           'VAR':12,
                           'HepA':12}}]
patient=[
            {'id': 'R001',
             'first name': 'John',
             'last name': 'Smith',
             'vacc months':{'HepB':{0,1,6},
                           'RV':{2,4,6},
                           'DTap':{2,4,6,15},
                           'Hib':{2,4,6,12},
                           'PCV13':{2,4,6,12},
                           'IPV':{2,4,6}},
            'vacc annual':{'MMR':12,
                           'VAR':12,
                           'HepA':12}
             }, {'id': 'R002',
             'first name': 'Olivia',
             'last name': 'James',
             'vacc months':{'HepB':{0,1,6},
                           'RV':{2,4,7},
                           'DTap':{2,5,7,12},
                           'Hib':{2,4,6,12},
                           'PCV13':{2,5,7,12},
                           'IPV':{2,5,8}},
            'vacc annual':{'MMR':12,
                           'VAR':12,
                           'HepA':12}}]
insert(patient)
ID: R001 John Smith
Vacc. Name: HepB , Administration(mos): {0, 1, 6}
Vacc. Name: RV , Administration(mos): {2, 4, 6}
Vacc. Name: DTap , Administration(mos): {2, 4, 6, 15}
Vacc. Name: Hib , Administration(mos): {2, 4, 12, 6}
Vacc. Name: PCV13 , Administration(mos): {2, 4, 12, 6}
Vacc. Name: IPV , Administration(mos): {2, 4, 6}
Vacc. Name: MMR , Administration(mos): 12
Vacc. Name: VAR , Administration(mos): 12
Vacc. Name: HepA , Administration(mos): 12
ID: R002 Olivia James
Vacc. Name: HepB , Administration(mos): {0, 1, 6}
Vacc. Name: RV , Administration(mos): {2, 4, 7}
Vacc. Name: DTap , Administration(mos): {2, 12, 5, 7}
Vacc. Name: Hib , Administration(mos): {2, 4, 12, 6}
Vacc. Name: PCV13 , Administration(mos): {2, 12, 5, 7}
Vacc. Name: IPV , Administration(mos): {8, 2, 5}
Vacc. Name: MMR , Administration(mos): 12
Vacc. Name: VAR , Administration(mos): 12
Vacc. Name: HepA , Administration(mos): 12

insert(new_patient)
ID: R003 Paola Quiroz
Vacc. Name: HepB , Administration(mos): {0, 2, 6}
Vacc. Name: RV , Administration(mos): {2, 4, 6}
Vacc. Name: DTap , Administration(mos): {2, 4, 6, 15}
Vacc. Name: Hib , Administration(mos): {9, 2, 4, 12}
Vacc. Name: PCV13 , Administration(mos): {2, 4, 12, 6}
Vacc. Name: IPV , Administration(mos): {2, 3, 6}
Vacc. Name: MMR , Administration(mos): 12
Vacc. Name: VAR , Administration(mos): 12
Vacc. Name: HepA , Administration(mos): 12

patient_dict.keys()
dict_keys(['R001', 'R002', 'R003'])

patient_dict.items()
dict_items([('R001', {'id': 'R001', 'first name': 'John', 'last name': 'Smith', 'vacc months': {'HepB': {0, 1, 6}, 'RV': {2, 4, 6}, 'DTap': {2, 4, 6, 15}, 'Hib': {2, 4, 12, 6}, 'PCV13': {2, 4, 12, 6}, 'IPV': {2, 4, 6}}, 'vacc annual': {'MMR': 12, 'VAR': 12, 'HepA': 12}}), ('R002', {'id': 'R002', 'first name': 'Olivia', 'last name': 'James', 'vacc months': {'HepB': {0, 1, 6}, 'RV': {2, 4, 7}, 'DTap': {2, 12, 5, 7}, 'Hib': {2, 4, 12, 6}, 'PCV13': {2, 12, 5, 7}, 'IPV': {8, 2, 5}}, 'vacc annual': {'MMR': 12, 'VAR': 12, 'HepA': 12}}), ('R003', {'id': 'R003', 'first name': 'Paola', 'last name': 'Quiroz', 'vacc months': {'HepB': {0, 2, 6}, 'RV': {2, 4, 6}, 'DTap': {2, 4, 6, 15}, 'Hib': {9, 2, 4, 12}, 'PCV13': {2, 4, 12, 6}, 'IPV': {2, 3, 6}}, 'vacc annual': {'MMR': 12, 'VAR': 12, 'HepA': 12}})])

```
## Explanation
```python
patient_dict={}
#generated an empty dictionary as a global variable outside of the function in which then I am using a fuction to modify my dictionary by adding and storing new patients. This will be my main dictionary, where my key will be my patient id and the value is the information. Inside the main dictionary, i will have a nested dictionary, meaning after identifying the pateint with patient id (key), we then go into the nested dictionary where we have the variables such as last and first name (key) and then the patient information such as john smith which is the value. Inside, the nested dictionary, we then have a third and fourth (nested) dictionaries for the monthly and annual vaccine information of each patient.    
def insert(patient_info):
#created a function called insert() with the parameter of patient_info in which will be the patients info.  
    for patient in patient_info:
    #generated a for loop so it can loop through each pateint dictionary. 
        patient_id=patient['id']
        #i am assigning the value of patient[id] to the variable patient id, this step is storing the patient id as the key in the main dictionary, and also helps prevent overridding when you add a new patient because the key is unique to each patient.  
        patient_dict[patient_id]=patient
        #in this step, i am assigning the patient dictionary to be the value in my main dictionary. 
        first_name=patient['first name']  
        last_name=patient['last name']
        # next, I start to assign variables to the patient information so i can access them. Here i am creating first and last name variables, so i can obtain the values such as John and Smith from the patient_dict. 
        print('ID:', patient_id, first_name, last_name)
        # printing patient info as ID: [patient info] 
        for name, months in patient['vacc months'].items():
            print('Vacc. Name:', name, ', Administration(mos):', months)
        for name, annual in patient['vacc annual'].items():
            print('Vacc. Name:', name, ', Administration(mos):', annual)
        #next, i generated two loops, for monthly and annual vacc as they have seperated dictionaries that have been already generated in my patient information dictionary, meaning the key is vacc montly and vacc annual name , and the value is the information of vacc which is another dictionary. I am using .items(), so it can return both the key and the value of the vacc dictionary 

new_patient=[{'id': 'R003',
             'first name': 'Paola',
             'last name': 'Quiroz',
             'vacc months':{'HepB':{0,2,6},
                           'RV':{2,4,6},
                           'DTap':{2,4,6,15},
                           'Hib':{2,4,9,12},
                           'PCV13':{2,4,6,12},
                           'IPV':{2,3,6}},
            'vacc annual':{'MMR':12,
                           'VAR':12,
                           'HepA':12}}]
#adding the new patient, in which will be added to my main dictionary as a new key-value pair as my id is new. if my id was not new, it will override the information of the patient who has that id. 
patient=[ #first nested dictionary 
            {'id': 'R001', #first nested dictionary
             'first name': 'John',
             'last name': 'Smith',
             'vacc months':{'HepB':{0,1,6}, #second nested dictionary 
                           'RV':{2,4,6},
                           'DTap':{2,4,6,15},
                           'Hib':{2,4,6,12},
                           'PCV13':{2,4,6,12},
                           'IPV':{2,4,6}},
            'vacc annual':{'MMR':12, #another second nested dictionary 
                           'VAR':12,
                           'HepA':12}
             }, {'id': 'R002',
             'first name': 'Olivia',
             'last name': 'James',
             'vacc months':{'HepB':{0,1,6},
                           'RV':{2,4,7},
                           'DTap':{2,5,7,12},
                           'Hib':{2,4,6,12},
                           'PCV13':{2,5,7,12},
                           'IPV':{2,5,8}},
            'vacc annual':{'MMR':12,
                           'VAR':12,
                           'HepA':12}}]
insert(patient) #output
ID: R001 John Smith
Vacc. Name: HepB , Administration(mos): {0, 1, 6}
Vacc. Name: RV , Administration(mos): {2, 4, 6}
Vacc. Name: DTap , Administration(mos): {2, 4, 6, 15}
Vacc. Name: Hib , Administration(mos): {2, 4, 12, 6}
Vacc. Name: PCV13 , Administration(mos): {2, 4, 12, 6}
Vacc. Name: IPV , Administration(mos): {2, 4, 6}
Vacc. Name: MMR , Administration(mos): 12
Vacc. Name: VAR , Administration(mos): 12
Vacc. Name: HepA , Administration(mos): 12
ID: R002 Olivia James
Vacc. Name: HepB , Administration(mos): {0, 1, 6}
Vacc. Name: RV , Administration(mos): {2, 4, 7}
Vacc. Name: DTap , Administration(mos): {2, 12, 5, 7}
Vacc. Name: Hib , Administration(mos): {2, 4, 12, 6}
Vacc. Name: PCV13 , Administration(mos): {2, 12, 5, 7}
Vacc. Name: IPV , Administration(mos): {8, 2, 5}
Vacc. Name: MMR , Administration(mos): 12
Vacc. Name: VAR , Administration(mos): 12
Vacc. Name: HepA , Administration(mos): 12

insert(new_patient)
ID: R003 Paola Quiroz
Vacc. Name: HepB , Administration(mos): {0, 2, 6}
Vacc. Name: RV , Administration(mos): {2, 4, 6}
Vacc. Name: DTap , Administration(mos): {2, 4, 6, 15}
Vacc. Name: Hib , Administration(mos): {9, 2, 4, 12}
Vacc. Name: PCV13 , Administration(mos): {2, 4, 12, 6}
Vacc. Name: IPV , Administration(mos): {2, 3, 6}
Vacc. Name: MMR , Administration(mos): 12
Vacc. Name: VAR , Administration(mos): 12
Vacc. Name: HepA , Administration(mos): 12

patient_dict.keys() #here i am demostrating the first main dictionary, that each patient is store with its id as the key. 
dict_keys(['R001', 'R002', 'R003'])

patient_dict.items() #here i am demostrating the values to each patient including the new added patient. 
dict_items([('R001', {'id': 'R001', 'first name': 'John', 'last name': 'Smith', 'vacc months': {'HepB': {0, 1, 6}, 'RV': {2, 4, 6}, 'DTap': {2, 4, 6, 15}, 'Hib': {2, 4, 12, 6}, 'PCV13': {2, 4, 12, 6}, 'IPV': {2, 4, 6}}, 'vacc annual': {'MMR': 12, 'VAR': 12, 'HepA': 12}}), ('R002', {'id': 'R002', 'first name': 'Olivia', 'last name': 'James', 'vacc months': {'HepB': {0, 1, 6}, 'RV': {2, 4, 7}, 'DTap': {2, 12, 5, 7}, 'Hib': {2, 4, 12, 6}, 'PCV13': {2, 12, 5, 7}, 'IPV': {8, 2, 5}}, 'vacc annual': {'MMR': 12, 'VAR': 12, 'HepA': 12}}), ('R003', {'id': 'R003', 'first name': 'Paola', 'last name': 'Quiroz', 'vacc months': {'HepB': {0, 2, 6}, 'RV': {2, 4, 6}, 'DTap': {2, 4, 6, 15}, 'Hib': {9, 2, 4, 12}, 'PCV13': {2, 4, 12, 6}, 'IPV': {2, 3, 6}}, 'vacc annual': {'MMR': 12, 'VAR': 12, 'HepA': 12}})])        
```
