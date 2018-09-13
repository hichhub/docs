- Feature Name: Hich API ROUTE PATERN
- Create Date: 2018-09-11
- Modification Date: 2018-09-11
- Version: 1.0.0

# Summary
HARP is name of our routes patern that is customised by us base of entities we used ... 

# Detailed design
We only return data of one entities in our resource result .

# Resource example
For example we have two entities as X and Y

#### For return X by :id
## GET Method
### .../Xs/:id

#### For return list of X
## GET Method
### .../Xs

#### For return list of X that belongs to Y by Y's id
## GET Method
### .../Xs/by/y/:id

#### For return list of X (filtering) that belongs to Y by Y's id
## POST Method (_search)
### .../Xs/by/y/:id/_search

