## Python Collection Arrays
There are 4 collection data types in the Python programming language.

| Type       | Ordered | Indexed | Changeable | Duplicates |
| ---------- | :-----: | :-----: | :--------: | :--------: |
| List       |    X    |    X    |     X      |     X      |
| Tuple      |    X    |    X    |            |     X      |
| Set        |         |         |     X      |            |
| Dictionary |         |    X    |     X      |            |

## Set Methods

| Method                          | Description                                                                    |
| ------------------------------- | ------------------------------------------------------------------------------ |
| `add()`                         | Adds an element to the set                                                     |
| `clear()`                       | Removes all the elements from the set                                          |
| `copy()`                        | Returns a copy of the set                                                      |
| `difference()`                  | Returns a set containing the difference between two or more sets               |
| `difference_update()`           | Removes the items in this set that are also included in another, specified set |
| `discard()`                     | Remove the specified item                                                      |
| `intersection()`                | Returns a set, that is the intersection of two other sets                      |
| `intersection_update()`         | Removes the items in this set that are not present in other, specified set(s)  |
| `isdisjoint()`                  | Returns whether two sets have an intersection or not                           |
| `issubset()`                    | Returns whether another set contains this set or not                           |
| `issuperset()`                  | Returns whether this set contains another set or not                           |
| `pop()`                         | Removes an element from the set                                                |
| `remove()`                      | Removes the specified element                                                  |
| `symmetric_difference()`        | Returns a set with the symmetric differences of two sets                       |
| `symmetric_difference_update()` | Inserts the symmetric differences from this set and another                    |
| `union()`                       | Return a set containing the union of sets                                      |
| `update()`                      | Update the set with the union of this set and others                           |

## Set
A set is a collection which is unordered and unindexed.

```python
thisset = {"apple", "banana", "cherry"}

print(thisset)                              #{'cherry', 'banana', 'apple'}
```

### Access Items
You cannot access items in a set by referring to an index or a key.

```python
thisset = {"apple", "banana", "cherry"}

for x in thisset:
    print(x)                                #cherry
                                            #apple
                                            #banana
```

### Change Item Value
Once a set is created, you cannot change its items, but you can add new items.

#### Add items
The `add()` method is used to add items to a a set.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

thisset.add("papaya")

print(thisset)                              #{'papaya', 'cherry', 'kiwi', 'mango', 'orange', 'nectarine', 'banana', 'apple'}
```

#### Add Many Items at Once
You can also add multiple items to a set using the `update()` method.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}
thisset.update(["papaya", "strawberry", "zuchini"])

print(thisset)                              #{'nectarine', 'mango', 'orange', 'zuchini', 'papaya', 'banana', 'kiwi', 'cherry', 'strawberry', 'apple'}
```

### Get the Length of a Set
The `len()` method can be used to determine how many items are in a set.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

print(len(thisset))                         #7
```

### Remove Items

#### `remove()`
The `remove()` method is used to remove a specified item. 

> ***Note:*** If the item does not exist, it will raise an error.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

thisset.remove("banana")

print(thisset)                              #{'cherry', 'kiwi', 'mango', 'apple', 'orange', 'nectarine'}
```

#### `discard()`
The `discard()` method is used to remove a specified item. 

> ***Note:*** If the item does not exist, it will NOT raise an error.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

thisset.discard("banana")

print(thisset)                              #{'cherry', 'kiwi', 'mango', 'apple', 'orange', 'nectarine'}}
```

#### `pop()`
The `pop()` method removes the last item of the set.

> ***Note:*** Remember that sets are unordered, so when using the pop() method, you will not know which item that gets removed!

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

thisset.pop()

print(thisset)                              #{'apple', 'nectarine', 'kiwi', 'mango', 'cherry', 'orange'}
```

#### `clear()`
The `clear()` method empties the entire set of all values.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

thisset.clear()

print(thisset)                              #set()
```

#### `del()`
The `del()` method deletes the set completely.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

del thisset

print(thisset)                             #NameError: name 'thisset' is not defined
```

### Copy a Set

#### `copy()`
You cannot copy a set simply by typing `set2 = set1` because: `set2` will only be a reference to `set1`, and changes made in `set1` will automatically also be made in `set2`.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

newset = thisset.copy()

print(newset)                               #{'apple', 'banana', 'cherry', 'kiwi', 'mango', 'nectarine', 'orange'}
```

### Join Two Sets

#### `union()`
The `union()` method returns a new set containing all items from both sets.

> ***Note:*** The result will EXCLUDE duplicate items.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

thatset = {"papaya", "strawberry", "zuchini"}

myset = thisset.union(thatset)              

print(myset)                                #{'kiwi', 'orange', 'strawberry', 'papaya', 'mango', 'zuchini', 'cherry', 'nectarine', 'banana', 'apple'}
```

#### `update()`
The `update()` method inserts the items from one set into another

> ***Note:*** The result will EXCLUDE duplicate items.

```python
thisset = {"apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"}

thatset = {"papaya", "strawberry", "zuchini"}

thisset.update(thatset)              

print(thisset)                              #{'kiwi', 'orange', 'strawberry', 'papaya', 'mango', 'zuchini', 'cherry', 'nectarine', 'banana', 'apple'}
```

### Compare Two Sets

#### `difference()`
The `difference()` method returns a new set containing the difference between 2 or more sets

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

newSet = ubuntuSet.difference(debianSet)    

print(newSet)                               #{'Xubuntu', 'Ubuntu Kylin', 'Pop!_os', 'KDE Neon', 'Ubuntu Mate', 'elementaryOS', 'Kubuntu', 'Lubuntu', 'Zorin', 'Ubuntu Studio', 'Ubuntu Budgie'}
```

#### `difference_update()`
The `difference_update` method removes the items in this set that are also included in another specified set.

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

debianSet.difference_update(ubuntuSet)

print(debianSet)                            #{'Debian', 'Deepin', 'Raspian', 'PureOS', 'MX Linux', 'Kali Linux', 'Linux Mint'}
```

#### `intersection()`
The `intersection()` method returns a new set that is the intersection of 2 other sets.

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

newSet = ubuntuSet.intersection(debianSet)

print(newSet)                               #{Ubuntu}
```

#### `intersection_update()`
The `intersection_update()` method removes the items in this set that are not present in other specified sets

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

debianSet.intersection_update(ubuntuSet)

print(debianSet)                            #{Ubuntu}
```

#### `isdisjoint()`
The `isdisjoint()` method returns whether two sets have an intersection or not.
- Returns `True` if no items in first set is present in second set.
- Returns `False` if at least one item from first set is present in second set.

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

isDisjoint = ubuntuSet.isdisjoint(debianSet)

print(isDisjoint)                           #False
```

### `issubset()`
The `isusbset()` method returns whether one set contains the entirety of this set.

- Returns `True` if all items in one set are present in the other set.
- Returns `False` if at least one item from one set is not present in the other set.

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

isSubset = ubuntuSet.issubset(debianSet)

print(isSubset)                             #False
```

#### `issuperset()`
The `issuperset()` method returns whether this set contains the entirety of another set

- Returns `True` if all items in the main set are present in the sub set.
- Returns `False` if at least one item from the sub set is not present in the main set.

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

isSuperset = ubuntuSet.issuperset(debianSet)

print(isSuperset)                           #False
```

#### `symmetric_difference()`
The `symettric_difference()` method returns a set that contains all items from both sets, except items that are present in both sets (everything except the matching items).

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

newSet = ubuntuSet.symmetric_difference(debianSet)

print(newSet)                               #{'Ubuntu Kylin', 'Pop!_os', 'Linux Mint', 'Lubuntu', 'PureOS', 'Deepin', 'Xubuntu', 'Debian', 'Kubuntu', 'Zorin', 'Raspian', 'Ubuntu Mate', 'KDE Neon', 'Kali Linux', 'Ubuntu Budgie', 'elementaryOS', 'Ubuntu Studio', 'MX Linux'}
```

#### `symmetric_difference_update()`
The `symmetric_difference_update()` method removes the items that are present in both sets, AND inserts the items that are not present in both sets.

```python
ubuntuSet = {"Pop!_os", "KDE Neon", "Xubuntu", "Kubuntu", "Lubuntu", "Ubuntu Mate", "Ubuntu Budgie", "Ubuntu Studio", "Ubuntu Kylin", "Zorin", "elementaryOS", "Ubuntu"}

debianSet = {"Deepin", "Ubuntu", "Debian", "MX Linux", "Kali Linux", "PureOS", "Raspian", "Linux Mint"}

ubuntuSet.symmetric_difference_update(debianSet)

print(ubuntuSet)                            #{'Kali Linux', 'Debian', 'KDE Neon', 'PureOS', 'Raspian', 'Ubuntu Studio', 'Ubuntu Kylin', 'MX Linux', 'Pop!_os', 'Ubuntu Mate', 'Xubuntu', 'elementaryOS', 'Linux Mint', 'Zorin', 'Deepin', 'Lubuntu', 'Ubuntu Budgie', 'Kubuntu'}  
```

### The `set()` Constructor
It is also possible to use the set() constructor to make a new set.

```python
thisset = set(("apple", "banana", "cherry", "kiwi", "mango", "nectarine", "orange"))

print(thisset)                              #{'apple', 'banana', 'cherry', 'kiwi', 'mango', 'nectarine', 'orange'}
```

### Frozen Sets
A frozen set is one that, after being created, cannot be changed.

```python
frznSet = frozenset([1, 2, 3 ,4])

print(frznSet)                            #frozenset({1, 2, 3, 4})
```
