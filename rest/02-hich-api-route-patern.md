- Feature Name: Hich API Route Pattern
- Create Date: 2018-09-11
- Modification Date: 2018-09-11
- Version: 1.0.0

# Summary
HARP is name of our routes pattern that is customised by us base of entities we used ... 

# Detailed design
We only return data of one entities in our resource result, The entitie will be returned that we want info about that,
With this pattern we collect are related routes in one place and we know what kind of data we need and will return ...

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

