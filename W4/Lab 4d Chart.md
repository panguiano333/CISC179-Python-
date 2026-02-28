# Child Vaccination Chart
```python

def insert(patient_info):
    for patient in patient_info:
        patient_id=patient['id']
        first_name=patient['first name']
        last_name=patient['last name']
        vacc_months=patient['vacc months']
        vacc_annual=patient['vacc annual']
        print(patient_id, first_name, last_name, vacc_months, vacc_annual)

        
patient_vacc=[
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

insert(patient_vacc)
R001 John Smith {'HepB': {0, 1, 6}, 'RV': {2, 4, 6}, 'DTap': {2, 4, 6, 15}, 'Hib': {2, 4, 12, 6}, 'PCV13': {2, 4, 12, 6}, 'IPV': {2, 4, 6}} {'MMR': 12, 'VAR': 12, 'HepA': 12}
R002 Olivia James {'HepB': {0, 1, 6}, 'RV': {2, 4, 7}, 'DTap': {2, 12, 5, 7}, 'Hib': {2, 4, 12, 6}, 'PCV13': {2, 12, 5, 7}, 'IPV': {8, 2, 5}} {'MMR': 12, 'VAR': 12, 'HepA': 12}
