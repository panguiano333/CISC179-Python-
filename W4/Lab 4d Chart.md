# Child Vaccination Chart
```python
def insert(patient_info):
    for patient in patient_info:
        patient_id=patient['id']
        first_name=patient['first name']
        last_name=patient['last name']
        print('ID:', patient_id, first_name, last_name)
        for name, months in patient['vacc months'].items(): #need patient[] to access the information of each vaccine, using .item, i am assignng name to key and months to value
            print('Vaccine Name:', name, ',Month of Administration:', months)
        for name, annual in patient['vacc annual'].items():
            print('Vaccine Name:', name, ',Administration', annual)

            
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
Vaccine Name: HepB ,Month of Administration: {0, 1, 6}
Vaccine Name: RV ,Month of Administration: {2, 4, 6}
Vaccine Name: DTap ,Month of Administration: {2, 4, 6, 15}
Vaccine Name: Hib ,Month of Administration: {2, 4, 12, 6}
Vaccine Name: PCV13 ,Month of Administration: {2, 4, 12, 6}
Vaccine Name: IPV ,Month of Administration: {2, 4, 6}
Vaccine Name: MMR ,Administration 12
Vaccine Name: VAR ,Administration 12
Vaccine Name: HepA ,Administration 12
ID: R002 Olivia James
Vaccine Name: HepB ,Month of Administration: {0, 1, 6}
Vaccine Name: RV ,Month of Administration: {2, 4, 7}
Vaccine Name: DTap ,Month of Administration: {2, 12, 5, 7}
Vaccine Name: Hib ,Month of Administration: {2, 4, 12, 6}
Vaccine Name: PCV13 ,Month of Administration: {2, 12, 5, 7}
Vaccine Name: IPV ,Month of Administration: {8, 2, 5}
Vaccine Name: MMR ,Administration 12
Vaccine Name: VAR ,Administration 12
Vaccine Name: HepA ,Administration 12
```
