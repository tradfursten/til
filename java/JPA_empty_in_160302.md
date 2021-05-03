# JPA and empty in clause

The JPA 2.1 specification says:

There must be at least one element in the comma separated list that defines the set of values for the IN
expression. 

So you as a developer needs to handle the case of an empty (or null) parameter that is sent to an in clause.

Ex.
```
SELECT *
FROM Customer c
WHERE c.country in :countryList
```

The thing set to `countryList` will return a exeption if it is empty.
