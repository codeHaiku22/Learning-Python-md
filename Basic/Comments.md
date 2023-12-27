## Benefits / Purposes of Comments
Comments have many use cases:
- Comments are often used to explain code
- They help programmers understand things about the code
- They also help to make the code more readable
- Comments can be used to prevent the execution of certain code when testing

## Creating a Comment

### Single-Line Comments
Comments start with a `#` symbol.

```python
#This is a comment
print("Hello, World!")
```

Comments can also be placed at the end of a line.

```python
print("Hello, World!") #This is a comment
```

A comment can also be applied to code.

```python
#print("Hello, World!")
print("Hello, Student!")
```

### Multi-Line Comments
In python, there isn't really a dedicated way of commenting multiple lines of text.  The most obvious way is to use a `#` symbol for each line.

```python
#This is a comment
#This is another comment
#This is yet another comment
print("Hello, World!")
```

There is one more way of doing this that is a bit easier.  A multi-line string is a string that spans across more than one line.  It is best defined by using 3 `"` signs before and after the string.  We can also use 3 `"` signs before and after multiple lines that are to be commented out.  Since the multi-line string isn't assigned a variable, Python will read the code, but will ignores it.

```python
"""
This is a comment
This is another comment
This is yet another comment
"""
print("Hello, World!")
```