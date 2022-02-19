Importing the TinyDB library's essential classes.
```python
from tinydb import TinyDB, Query
db = TinyDB("students_db.json")
```

Inserting data in the database
```python
>>> items = {`name`: `Kennedy`, `Course`: `Nursing`, `year`: 3}
>>> {`name`: `Catherine`, `Course`: `Law`, `year`: 4},
>>> {`name`: `Anthony`, `Course`: `Computer science`,`year`: 1},
>>> {`name`: `Caroline`, `Course`: `Education`,`year`: 3}
>>> {`name`: `Moris`, `Course`: `Education`,`year`: 3}
>>> ]
>>> db.insert_multiple(items) [1, 2, 3, 4, 5]
{
"_default": {
"1": { "name": "Kennedy", "Course": "Nursing", "year": 3},
"2": { "name": "Catherine", "Course": "Law", "year": 4 },
"3": { "name": "Anthony", "Course": "Computer science","year": 1},
"4": { "name": "Caroline", "Course": "Education","year": 3}
"5": { "name": "Moris", "Course": "Education","year": 3}
}
}
```
Searching data in the database using get() function
```python
>>> db.get(Students.name == 'Catherine')
{"name": "Catherine", "Course": "Law", "year": 4}
```
Searching data in the database using search() function
```python
>>> db.search(Students.course == 'Nursing')
[{"name": "Kennedy", "Course": "Nursing", "year": 3}]
```
Updating all data in TinyDB
```python
# updating data in the database
>>> db.update({'year': 1}) 
[1, 2, 3, 4, 5]
>>> db.all()

# results
{`name`: `Kennedy`, `Course`: `Nursing`, `year`: 1}
{`name`: `Catherine`, `Course`: `Law`, `year`: 1},
{`name`: `Anthony`, `Course`: `Computer science`,`year`: 1},
{`name`: `Caroline`, `Course`: `Education`,`year`: 1}
{`name`: `Moris`, `Course`: `Education`,`year`: 1}
```

Deleting data from TinyDB
```python
# activity
>>> db.remove(Students.name == 'Kennedy')                              
[1]
# results
>>> db.all()                      
[{`name`: `Catherine`, `Course`: `Law`, `year`: 1},
{`name`: `Anthony`, `Course`: `Computer science`,`year`: 1},
{`name`: `Caroline`, `Course`: `Education`,`year`: 1}
{`name`: `Moris`, `Course`: `Education`,`year`: 1}]
```
