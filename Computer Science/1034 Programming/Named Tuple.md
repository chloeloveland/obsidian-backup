Named tuple provides a way to create simple, lightweight data structures similar to a class, but without the overhead of defining a full class. Like [[Dictionary|dictionaries]], they contain keys that are hashed to a particular value. However, it supports both access from key-value and iteration, the functionality that dictionaries lack.

Python Syntax:
```
namedtuple(typename, field_names)

- typename – The name of the namedtuple.
- field_names – The list of attributes stored in the namedtuple.
```