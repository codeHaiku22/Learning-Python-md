## Fundamentals
### Creating Variables
Python does not have a formal declaration for variables.  Instead, variables are declared as follows.

```python
x = 5
y = "John"

print(x)
print(y)
```

Variable declaration is quite simple; it doesn't need to be declared with any particular type.  Variables can even change type after they have been set.

```python
z = 4          #type is int
z = "Staci"    #type is str

print(z)
```

### Casting
Sometimes, you may want to specify the data type of a variable.  This can be done during declaration of the variable with casting.

```python
x = str(42)      #z is equal to '3'
y = int(42)      #z is equal to 3
z = float(42)    #z is equal to 42.0
```

### Getting the Data Type
You can get the data type of any object by using the `type()` function.

```python
x = 5
y = "John"

print(type(x))
print(type(y))
```

### Single Quotes and Double Quotes
In Python, both single quotes and double quotes are the same.  Strings can be declared using either single or double quotes.

```python
x = "John"
x = 'John'
```

### Case Sensitivity
Python is a case-sensitive language.

```Python
a = 34
A = 'Staci'

print(a)
print(A)
```

## Variable Names
Rules for Python Variables
- A variable name must start with a letter or the underscore character.
- A variable name cannot start with a number.
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ _)
- Variable names are case-sensitive

### Illegal Variable Names
Here are some examples of variable names that don't follow the rules.

```python
2ne1 = "I am the Best"

some-variable = "Just some illegal variable name"

spaced out = 5
```

### Variable Naming Strategies

#### Hungarian Notation
This notation reveals the data type of the variable since it uses the data type within the variable name itself.

Data Type | Type Code | Example
--- | --- | ---
String | `str` | `strName`
Integer | `int` | `intAge`
Float | `float` | `fltPi`
List | `list` | `lstFruits`
Tuple | `tuple` | `tplVegetables`
Dictionary | `dict` | `dctCars`
Boolean | `bool` | `blnSkate`
Binary | `bytes` | `binStream`

#### Camel Case
With this format, every word (except the first word) begins with a capital letter.

```python
myAwesomeVariable = "So cool"

strMyAwesomeVariable = "Even cooler with Hungarian Notation and Camel Case.  Hungarian Camel, anyone?"
```

#### Pascal Case
With this format, each work begins with a capital letter.

```python
MyAwesomeVariable = "So cool"

StrMyAwesomeVariable = "Even cooler with Hungarian Notation and Pascal Case: Pascalian Camel: is that even a thing?"
```

#### Snake Case
With this format, every word is separated by an underscore character.

```python
my_awesome_variable = "Oh still so cool"

str_My_Awesome_Variable = "I don't think Hungarian snake camels should exist."
```

## Assigning Multiple Values

### Many Values to Many Variables
Python let's you assigns multiple values to multiple variables, all on the same line!

```Python
x, y, z = "Apple", "Banana", "Cherry"

print(x)  
print(y)  
print(z)
```

### One Value to Many Variables
Python also lets you assign the same value to multiple variables, all on the same line!

```Python
x = y = z = "Coconut"

print(x)  
print(y)  
print(z)
```

### Unpacking a Collection
Collection data types include lists and tuples.  Python allows for the extraction of the values into separate variables.  This process is called ***unpacking***.

```python
fruits = ["apple", "banana", "cherry", "coconut", ]
w, x, y, z = fruits

print(w) 
print(x)  
print(y)  
print(z)
```

## Output Variables

### Using the `print()` Function for Single Variable
The `print()` function is a simple way to output the value of a variable.

```python
x = "This variable has a boring name."

print(x)
```

### Using the `print()` Function for Multiple Variables
The `print()` function is a simple way to output values for multiple variables, also.

#### Using a Comma

```python
v = "This"
w = "is" 
x = "a sentence of"
y = "6"
z = "words."

print(v, w, x, y, z)
```

#### Using a Plus Operator: The Right Way

```python
v = "This"
w = "is" 
x = "a sentence of"
y = "6"
z = "words."

print(v + w + x + y + z)
print(v+ " " + w + " " + x + " " + y + " " + z)
```

> ***Note:*** The plus operator (`+`) concatenates strings.  When used with numbers, the plus operator performs addition.

#### Using a Plus Operator: The Wrong Way

```python
v = "This"
w = "is" 
x = "a sentence of"
y = 6
z = "words."

print(v + w + x + y + z)
```

> ***Note:*** The plus operator (`+`) cannot be used with both strings and numbers.

#### The Benefit of the Comma 
The comma supports the usage of multiple data types.

```python
v = "This"
w = "is" 
x = "a sentence of"
y = 6
z = "words."

print(v, w, x, y, z)
```