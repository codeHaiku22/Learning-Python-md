## String Literals
String literals in Python are surrounded by either single quotation marks or double quotation marks.

 > ***Note:*** Therefore, 'hello' is the same as "hello"

## Assign a String to a Variable
A variable can be assigned a string value with one line of code.

```python
a = "Hello"

print(a)    #Hello
```

### Multiline Strings
You can assign a multiline string to a variable by using 3 double quotation marks or 3 single quotation marks.

```python
a = """The quick brown fox jumped
over the lazy dogs."""

print(a)    #The quick brown fox jumped
            #over the lazy dogs. 

a = '''The quick brown fox jumped
over the lazy dogs.'''

print(a)    #The quick brown fox jumped
            #over the lazy dogs.               
```

## Strings are Arrays
Strings are arrays of bytes representing Unicode characters.
- A single character is simply a string with a length of 1.
- Square brackets can be used to access elements of the string.

```python
a = "Hello, World!"

print(a[1])         #e
```

### Strings are Arrays: Diagram
The metering or measurement marks begin before each character.

| H | e | l | l | o | , | &nbsp; | W | o | r | l | d | ! |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |

### Slicing
The process of slicing allows you to take parts of a string also known as a sub-string.
- The format is as follows: `[starting poing from left : distance from left]`

```python
a = "Hello, World!"

print(a[0:5])       #Hello
```

### Negative Indexing
Slicing can also be done in reverse.  So instead of going from right-to-left, we can go from left-to-right.
- The format is as follows: `[starting poing from right : distance]`

```python
a = "Hello, World!"

print(a[-5:-2])     #orl
```

### String Length
You can also determine the number of characters in a string using the `len` function.

```python
a = "Hello, World!"

print(len(a))       #13
```

### Reversing
Making a string backwards or in reverse order is quite simple using some slicing techniques.

```python
somestring = "This string will be reversed."
somestring = somestring[::-1]

print(somestring)                                                   #.desrever eb lliw gnirts sihT
```

## String Methods
All string methods return new values; they do not change the original string.

| Method | Description |
| ---- | ---- |
| `capitalize()` | Converts the first character to upper case |
| `casefold()` | Converts string into lower case |
| `center()` | Returns a centered string |
| `count()` | Returns the number of times a specified value occurs in a string |
| `encode()` | Returns an encoded version of the string |
| `endswith()` | Returns true if the string ends with the specified value |
| `expandtabs()` | Sets the tab size of the string |
| `find()` | Searches the string for a specified value and returns the position of where it was found |
| `format()` | Formats specified values in a string |
| `format_map()` | Formats specified values in a string |
| `index()` | Searches the string for a specified value and returns the position of where it was found |
| `isalnum()` | Returns True if all characters in the string are alphanumeric |
| `isalpha()` | Returns True if all characters in the string are in the alphabet |
| `isdecimal()` | Returns True if all characters in the string are decimals |
| `isdigit()` | Returns True if all characters in the string are digits |
| `isidentifier()` | Returns True if the string is an identifier |
| `islower()` | Returns True if all characters in the string are lower case |
| `isnumeric()` | Returns True if all characters in the string are numeric |
| `isprintable()` | Returns True if all characters in the string are printable |
| `isspace()` | Returns True if all characters in the string are whitespaces |
| `istitle() ` | Returns True if the string follows the rules of a title |
| `isupper()` | Returns True if all characters in the string are upper case |
| `join()` | Joins the elements of an iterable to the end of the string |
| `ljust()` | Returns a left justified version of the string |
| `lower()` | Converts a string into lower case |
| `lstrip()` | Returns a left trim version of the string |
| `maketrans()` | Returns a translation table to be used in translations |
| `partition()` | Returns a tuple where the string is parted into three parts |
| `replace()` | Returns a string where a specified value is replaced with a specified value |
| `rfind()` | Searches the string for a specified value and returns the last position of where it was found |
| `rindex()` | Searches the string for a specified value and returns the last position of where it was found |
| `rjust()` | Returns a right justified version of the string |
| `rpartition()` | Returns a tuple where the string is parted into three parts |
| `rsplit()` | Splits the string at the specified separator, and returns a list |
| `rstrip()` | Returns a right trim version of the string |
| `split()` | Splits the string at the specified separator, and returns a list |
| `splitlines()` | Splits the string at line breaks and returns a list |
| `startswith()` | Returns true if the string starts with the specified value |
| `strip()` | Returns a trimmed version of the string |
| `swapcase()` | Swaps cases, lower case becomes upper case and vice versa |
| `title()` | Converts the first character of each word to upper case |
| `translate()` | Returns a translated string |
| `upper()` | Converts a string into upper case |
| `zfill()` | Fills the string with a specified number of 0 values at the beginning |

### `strip()` 
Removes any leading or trailing white space

```python
a = "   Hello, World!       "

print(a.strip())                #Hello, World!
```

### `lstrip()`    
Removes any leading white space

```python
a = "   Hello, World!       "

print(a.lstrip())                #'Hello, World!       '
```

### `rstrip()`
Removes any trailing white space

```python
a = "   Hello, World!       "

print(a.rstrip())                #'   Hello, World!'
```

### `lower()` 
Converts string to lowercase

```python
a = "Hello, World!"

print(a.lower())                #hello, world!
```

### `upper()`
Converts string to uppercase

```python
a = "Hello, World!"

print(a.upper())                #HELLO, WORLD!
```

### `replace()`
Replaces a string with another string

```python
a = "Hello, World!"

print(a.replace("H", "J"))      #Jello, World!
```

### `split()` 
Splits the string into substrings if it finds instances of the separator

```python
a = "Hello, World!"

print(a.split(","))             #['Hello', ' World!']
```

### `join()`
Joins the elements of an iterable to the end of the string

```python
mylist = ['android', 'apple', 'blackberry', 'librem', 'pine64']

newstring = ''.join(mylist)     

print(newstring)                #androidappleblackberrylibrempine64

newstring = ' '.join(mylist)    

print(newstring)                #android apple blackberry librem pine64
```

### `count()`
Counts the number of times a specified value occurs in a string

```python
a = "Hello, World!"

print(a.count("l"))             #3
```

### `index()`
Searches the string for a specified value and returns the position where it was found

```python
a = "Hello, World!"

print(a.index("Hello"))         #0
```

## Check String
To check if a certain phrase or character is present in or not a string. 

### `in`
Is it present within a string?

```python
txt = "The rain in Spain stays mainly in the plain."
x = "ain" in txt

print(x)                        #True
```

### `not in`
Is it not present (missing) within a string?

```python
txt = "The rain in Spain stays mainly in the plain."
x = "ain" not in txt

print(x)                        #False
```

## String Concatenation
Concatenation comes from the root word "concatenate".  This means the joining (or concatenating) of objects, in this case: strings.

```python
a = "Hello, "
b = "World!"
c = a + b

print(c)                        #Hello, World!
```

## String Format
String variables and number variables cannot be concatenated using `+`.
- The `format()` method is used to perform this type of action

```python
age = 36
txt = "My name is John, and I am {}."

print(txt.format(age))          #My name is John, and I am 36.
```

Multiple values can be implemented

```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item {} for a total of {} dollars."

print(myorder.format(quantity, itemno, price))                      #I want 3 pieces of item 567 for a total of 49.95 dollars.
```

Ordinals can control placements

```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."

print(myorder.format(quantity, itemno, price))                      #I want to pay 49.95 dollars for 3 pieces of item 567.
```

### Escape Characters
Sometimes you need the a special character to be a part of the actual string itself.  When this is the case, the special character can be included in the string using an escape character.

Code | Result 
--- | -
`\'` | Single quote 	
`\"` | Double quote
`\\` | Backslash 	
`\n` | New line 	
`\r` | Carriage return 	
`\t` | Tab 	
`\b` | Backspace 	
`\f` | Form feed 	
`\ooo` | Octal value 	
`\xhh` | Hex value
In the example below, we want the double-quotation marks to be included within the string, itself.

```python
txt = "We are the so-called \"Vikings\" from the North."

print(txt)                                                          #We are the so-called "Vikings" from the North.
```

### The `%` Symbol
The `%` symbol is also called "the percent symbol" and can be used as a placeholder that also handles formatting of a string.

```python
var = "Bill"
mystring = "The variable is: %s" % var       

print(mystring)                                                     #The variable is: Bill

var = 3
mystring = "The variable is: %d" % var

print(mystring)                                                     #The varaible is: 3

var = 3.141592653589793
mystring = "The variable is: %f" % var                              #The variable is: 3.141593

print(mystring)

var = 3.141592653589793
mystring = "The variable is: %.3f" % var                            #The variable is: 3.142

print(mystring)
```

### `.format()` Method
Another way to format a string is by using one of the methods listed above.

```python
var = 3.141592653589793
mystring = "The variable is: {}".format(var)

print(mystring)                                                     #The variable is: 3.141592653589793

var = 3.141592653589793
mystring = "The variable is: {:.3f}".format(var)

print(mystring)                                                     #The variable is: 3.142

var1 = 3.141592653589793
var2 = 5
mystring = "The variables are: {:.3f} and {}".format(var1, var2)

print(mystring)                                                     #The variables are: 3.142 and 5
```

### `f`-strings`
Using the letter `f` in a string is yet another way to format a string.  This technique is called "f-strings".

```python
var1 = 3.141592653589793
var2 = 5
mystring = f"The variables are: {var1} and {var2}"

print(mystring)                                                     #The variables are: 3.141592653589793 and 5

var1 = 3.141592653589793
var2 = 5
mystring = f"The variables are: {var1} and {var2*3}"

print(mystring) 
```
