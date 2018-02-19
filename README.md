# python-snippets
Commonly used Python3 code snippets

## Quick Reference Links

* [Python 3 — Quick Reference Card](http://www.cs.put.poznan.pl/csobaniec/software/python/py-qrc.html)
* [Python 3 Basic Reference Card](https://perso.limsi.fr/pointal/_media/python:cours:mementopython3-v1.0.5a-english.pdf)
* [Python 3.2 Reference Card](https://perso.limsi.fr/pointal/_media/python:cours:abregepython-english.pdf)


## Documentation Links
selected links from:  https://docs.python.org/3.4/contents.html 

| Category | Selected Links |
| :------- | :---- | 
| [The Python Tutorial](https://docs.python.org/3.4/tutorial/index.html)           | [5. Data Structures [list], (tuple), {dict}][python3-data-structures] <br> [7.2: Reading and Writing Files][python3-file-io] <br> [8. Errors and Exceptions][python3-exceptions] | 
| [The Python Language Reference](https://docs.python.org/3.4/reference/index.html) | [6. Modules (Packages) ](https://docs.python.org/3.4/tutorial/modules.html) <br> [8. Compound Statements (if,while,for,try,with)](https://docs.python.org/3.4/reference/compound_stmts.html)
| [The Python Standard Library](https://docs.python.org/3.4/library/index.html)   | [2. Built-in Functions][python3-file-io] <br> [8. Data Types](https://docs.python.org/3.4/library/datatypes.html) <br> [12. Data Persistence](https://docs.python.org/3.4/library/persistence.html) <br> [16. Generic Operating System Services (os,io,time,argparse,getopt,logging...)](https://docs.python.org/3.4/library/allos.html) <br> [17. Concurrent Execution (threading,multiprocessing,...)](https://docs.python.org/3.4/library/concurrency.html) <br> [18. Interprocess Communication and Networking](https://docs.python.org/3.4/library/ipc.html) <br> [19. Internet Data Handling](https://docs.python.org/3.4/library/netdata.html) <br> [20. Structured Markup Processing Tools (html,xml,...](https://docs.python.org/3.4/library/markup.html) <br> [21. Internet Protocols and Support (urllib,http.client,...)](https://docs.python.org/3.4/library/internet.html)|

## File I/O
Open a file:  open(filename, mode)
```python
f = open('workfile', 'w')
```

[python3-file-io]: https://docs.python.org/3.4/tutorial/inputoutput.html#reading-and-writing-files
[python3-data-structures]: https://docs.python.org/3.4/tutorial/datastructures.html
[python3-exceptions]: https://docs.python.org/3.4/tutorial/errors.html
[python3-builtin-fuctions]: https://docs.python.org/3.4/library/functions.html

## Tuples(), Lists[] and Dictionaries{key1:value1, key2:value2, ...}
**Lists** are what they seem - a list of values. Each one of them is numbered, starting from zero - the first one is numbered zero, the second 1, the third 2, etc. You can remove values from the list, and add new values to the end.  You can also sort lists.  
```python
# create a new list
cats = ['Tom', 'Snappy', 'Kitty', 'Jessie', 'Chester']
```
**Tuples** are just like lists, but you can't change their values. The values that you give it first up, are the values that you are stuck with for the rest of the program. Again, each value is numbered starting from zero, for easy reference. Example: the names of the months of the year.
```python
# create a tuple
months = ('January','February','March','April','May','June','July','August','September','October','November','December')
```
**Dictionaries** contain key/value pairs. The values in a dictionary aren't numbered - you have an 'index' of words (keys), and for each of them a definition.  The values in a dictionary aren't numbered - they aren't in any specific order, either - the key does the same thing. You can add, remove, and modify the values in dictionaries. 
```python
# create a new dictionary
phonebook = {'Andrew Parson':8806336, \
'Emily Everett':6784346, 'Peter Power':7658344, \
'Lewis Lame':1122345}

# Add the person 'Gingerbread Man' to the phonebook:
phonebook['Gingerbread Man'] = 1234567

# Define an empty dictionary
ages = {}

# Add a couple of names to the dictionary
ages['Sue'] = 23
ages['Peter'] = 19
ages['Andrew'] = 78
ages['Karren'] = 45

# Function has_key() - returns True or False
if ages.has_key('Sue'):
    print("Sue is in the dictionary. She is", ages['Sue'], "years old")
else:
    print("Sue is not in the dictionary")

# keys() - returns a list of all the names of the keys
print("The following people are in the dictionary:", ages.keys())

# values() - returns a list of all values:
print("People are aged the following:", ages.values())

# sort() - wil sort all values in a listalphabetically, numerically, etc.
print keys
keys.sort()
print(keys)

# len() - find the number of entries in a dict
print("The dictionary has", len(ages), "entries in it")
```
