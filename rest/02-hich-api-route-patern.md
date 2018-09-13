- Feature Name: Hich API ROUTE PATERN
- Create Date: 2018-09-11
- Modification Date: 2018-09-11
- Version: 1.0.0

# Summary
HARP is name of our routes patern that is customised by us base of entities we used ... 

# Detailed design
We only return data of one entities in our resource result .

# Resource example
#### For example we have two entities as X and Y

## GET Method
For return X by id
```
.../Xs/:id
```

## GET Method
For return list of X
```
.../Xs
```

## GET Method
For return list of X that belongs to Y by Y's id
```
.../Xs/by/y/:id
```

## POST Method (_search)
For return list of X (filtering) that belongs to Y, query should be run on X and Y (default is X)
```
.../Xs/by/y/_search/:skip/:size
```

## POST Method (_search)
For return list of X (filtering) that belongs to Y by Y's id
```
.../Xs/by/y/:id/_search/:skip/:size
```

