# Child Vaccination Chart
```python
def insert(patient_info):
    for patient in patient_info:
        patient_id=patient['id']
        first_name=patient['first name']
        last_name=patient['last name']
        print('ID:', patient_id, first_name, last_name)
        for name, months in patient['vacc months'].items(): #need patient[] to access the information of each vaccine, using .item, i am assignng name to key and months to value
            print('Vacc. Name:', name, ',Administration(mos):', months)
        for name, annual in patient['vacc annual'].items():
            print('Vacc. Name:', name, ',Administration(mos):', annual)

            
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
Vacc. Name: HepB ,Administration(mos): {0, 1, 6}
Vacc. Name: RV ,Administration(mos): {2, 4, 6}
Vacc. Name: DTap ,Administration(mos): {2, 4, 6, 15}
Vacc. Name: Hib ,Administration(mos): {2, 4, 12, 6}
Vacc. Name: PCV13 ,Administration(mos): {2, 4, 12, 6}
Vacc. Name: IPV ,Administration(mos): {2, 4, 6}
Vacc. Name: MMR ,Administration(mos): 12
Vacc. Name: VAR ,Administration(mos): 12
Vacc. Name: HepA ,Administration(mos): 12
ID: R002 Olivia James
Vacc. Name: HepB ,Administration(mos): {0, 1, 6}
Vacc. Name: RV ,Administration(mos): {2, 4, 7}
Vacc. Name: DTap ,Administration(mos): {2, 12, 5, 7}
Vacc. Name: Hib ,Administration(mos): {2, 4, 12, 6}
Vacc. Name: PCV13 ,Administration(mos): {2, 12, 5, 7}
Vacc. Name: IPV ,Administration(mos): {8, 2, 5}
Vacc. Name: MMR ,Administration(mos): 12
Vacc. Name: VAR ,Administration(mos): 12
Vacc. Name: HepA ,Administration(mos): 12


```
