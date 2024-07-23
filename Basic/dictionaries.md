## Python Collection Arrays
There are 4 collection data types in the Python programming language.

| Type       | Ordered | Indexed | Changeable | Duplicates |
| ---------- | :-----: | :-----: | :--------: | :--------: |
| List       |    X    |    X    |     X      |     X      |
| Tuple      |    X    |    X    |            |     X      |
| Set        |         |         |     X      |            |
| Dictionary |         |    X    |     X      |            |

## Set Methods

Method | Description
--- | ---
`clear()` | Removes all the elements from the dictionary
`copy()` | Returns a copy of the dictionary
`fromkeys()` | Returns a dictionary with the specified keys and value
`get()` | Returns the value of the specified key
`items()` | Returns a list containing a tuple for each key value pair
`keys()` | Returns a list containing the dictionary's keys
`pop()` | Removes the element with the specified key
`popitem()` | Removes the last inserted key-value pair
`setdefault()` | Returns the value of the specified key. If the key does not exist: insert the key, with the specified value
`update()` | Updates the dictionary with the specified key-value pairs
`values()` | Returns a list of all the values in the dictionary

## Dictionary
A dictionary is a collection which is unordered, changeable, and indexed.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

print(thisdict)                              #{'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor'}
```


### Accessing Items
You can access the items of a dictionary by referring to its key name, inside square brackets.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

x = thisdict["model"]

print(x)                                    #F-150
```

####  `fromkeys()`
Returns a dictionary with the specified keys and the specified value.

```python
k = ('key1', 'key2', 'key3')
v = 0

anotherdict = dict.fromkeys(k, v)

print(anotherdict)                          #{'key1': 0, 'key2': 0, 'key3': 0}
```

#### `get()`
Returns the value of the items with the specified key.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

x = thisdict.get("model")

print(x)                                    #F-150
```

### Change Values
You can change the value of a specific item by referring to its key name.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

thisdict["trim"] = "STX"

print(thisdict)                             #{'brand': 'Ford', 'model': 'F-150', 'trim': 'STX'}
```

### Loop Through a Dictionary
You can loop through a dictionary by using a for loop.

> ***Note:*** When looping through a dictionary, the return values are the keys of the dictionary, but there are methods to return the values as well.

Print all keys' names in the dictionary

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

for x in thisdict:
    print(x)                                #brand
                                            #model
                                            #trim
```

### Printing Keys and Printing Values

#### Use the `keys()`  Method to Print Keys
You can also use the `keys()` method to return keys of a dictionary.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

for x in thisdict.keys():
    print(x)                                #brand
                                            #model
                                            #trim                                             
```

#### Print Values
Print all values in the dictionary.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

for x in thisdict:
    print(thisdict[x])                      #Ford
                                            #F-150
                                            #Raptor
```

#### Use the `values()`  Method to Print Values
You can also use the `values()` method to return values of a dictionary

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

for x in thisdict.values():
    print(x)                                #Ford
                                            #F-150
                                            #Raptor
```

#### Use the `items()` Method to Print both Keys and Values
You can loop through both keys and values by using the `items()` method.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

for x, y in thisdict.items():
    print(x, y)                             #brand Ford
                                            #model F-150
                                            #trim Raptor        
```

### Check if Key Exists
To determine if a specified key is present in a dictionary, use the `in` keyword.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

if "model" in thisdict:
    print("Yes, 'model' is one of the keys in thisdict dictionary.")
```

### Return Value of Specified Key or Create New Key 

#### `setdefault()`
The `setdefault()` method sets the default key-value pair of the dictionary.  This can be tested using the `print` function to returns the value of the default item.
 
 ```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

x = thisdict.setdefault("trim", "STX")

print(x)                                    #Raptor
```

 If the key does not exist, insert the key, with the specified value.
 
```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
}

x = thisdict.setdefault("trim", "STX")

print(x)                                    #STX
```

### Dictionary Length
To determine how many items (key-value pairs) a dictionary has, use the `len()` function.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

print(len(thisdict))                        #3
```

### Add New Items (Keys and Values)

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

thisdict["color"] = "charcoal"

print(thisdict)                             #{'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor', 'color': 'charcoal'}
```

### Update Existing Items with `update()` Method
The `update()` method inserts the specified items to the dictionary.  The specified items can be a dictionary or an iterable object.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

thisdict.update({"color": "charcoal"})

print(thisdict)                             #{'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor', 'color': 'charcoal'}
```

### Remove Items

#### `pop()`
Using the `#pop()` method, we can removes the item with the specified key name.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

thisdict.pop("model")

print(thisdict)                             #{'brand': 'Ford', 'trim': 'Raptor'}
```

#### `popitem()`
The `popitem()` method removes the last inserted item.

> ***Note:*** In versions before Python 3.7, a random item is removed instead.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

thisdict.popitem()

print(thisdict)                             #{'brand': 'Ford', 'model': 'F-150'}
```

#### `del()`
The `del()` method removes the item with the specified key name.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

del thisdict["model"]

print(thisdict)                             #{'brand': 'Ford', 'trim': 'Raptor'}
```

This method can also be used to delete the dictionary completely!

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

del thisdict

print(thisdict)                            #NameError: name 'thisdict' is not defined
```

#### `clear()`
The `clear()` method empties the entire dictionary.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

thisdict.clear()

print(thisdict)                            #{}
```

### Copy a Dictionary
Similar to sets, you cannot copy a dictionary simply by typing dict2 = dict1, because: dict2 will only be a reference to dict1, and changes made in dict1 will automatically also be made in dict2.

#### `copy()`
The `copy()` method provides for a simple way to make an actual copy of a dictionary.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

newdict = thisdict.copy()

print(newdict)                              #{'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor'}
```

#### `dict()`
The `dict()` constructor can also be sued to make a copy of a dictionary.

```python
thisdict = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

newdict = dict(thisdict)

print(newdict)                              #{'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor'}
```

### Nested Dictionaries
A dictionary can also contain many dictionaries.

```python
trucks = {
    "truck1" : {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
    },
    "truck2" : {
    "brand": "Toyota",
    "model": "Tundra",
    "trim": "TRD Pro"
    },
    "truck3" : {
    "brand": "Chevrolet",
    "model": "Silverado",
    "trim": "High Country"
    }
}

print(trucks)                               #{
                                            # 'truck1': {'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor'}, 
                                            # 'truck2': {'brand': 'Toyota', 'model': 'Tundra', 'trim': 'TRD Pro'}, 
                                            # 'truck3': {'brand': 'Chevrolet', 'model': 'Silverado', 'trim': 'High Country'}
                                            # }
```

Separate dictionaries can be nested as children into a parent dictionary.

```python
truck1 = {
    "brand": "Ford",
    "model": "F-150",
    "trim": "Raptor"
}

truck2 = {
    "brand": "Toyota",
    "model": "Tundra",
    "trim": "TRD Pro"
}

truck3 = {
    "brand": "Chevrolet",
    "model": "Silverado",
    "trim": "High Country"
}

alltrucks = {
    "truck1": truck1,
    "truck2": truck2,
    "truck3": truck3,
}

print(alltrucks)                            #{
                                            # 'truck1': {'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor'}, 
                                            # 'truck2': {'brand': 'Toyota', 'model': 'Tundra', 'trim': 'TRD Pro'}, 
                                            # 'truck3': {'brand': 'Chevrolet', 'model': 'Silverado', 'trim': 'High Country'}
                                            # }
```

### The `dict()` Constructor
It is also possible to use the `dict()` constructor to make a new dictionary.

```python
thisdict = dict(brand="Ford", model="F-150", trim="Raptor")

print(thisdict)                             #{'brand': 'Ford', 'model': 'F-150', 'trim': 'Raptor'}
```
