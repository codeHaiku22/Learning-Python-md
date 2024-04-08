## Either True or False
You can evaluate any expression in Python, and get one of two answers, True or False.

```python
print(10 > 9)       #True
print(10 == 9)      #False
print(10 < 9)       #False
```

## `if` Statement
The `if` statement is a mechanism that is very conducive to Booleans since there can be 2 outcomes if we use the `else` part.

```python
a = 200
b = 33

if b > a:
  print("b is greater than a")          
else:
  print("b is not greater than a") 
```

## Evaluate Values and Variables
The `bool()` function allows you to evaluate any value and returns True or False.

Evaluate a string and a number

```python
print(bool("Hello"))        #True
print(bool(15))             #True
```

Evaluate two variables

```python
x = "Hello"
y = 15

print(bool(x))              #True
print(bool(y))              #True
```

## Most Values are True
When we perform the evaluations above, we can see that most results were True.  

Here are some rules that make sense of this.
- Any string is True, except empty strings.
- Any number is True, except 0.
- Any list, tuple, set, and dictionary are True, except empty ones.

Almost any value is evaluated to True if it has some sort of content.

```python
bool("abc")                                 #True
bool(123)                                   #True
bool(["apple", "cherry", "banana"])         #True
```

There are not many values that evaluate to False, except empty values, False, None, and 0.

```python
bool(False)                                 #False
bool(None)                                  #False 
bool(0)                                     #False
bool("")                                    #False
bool(())                                    #False
bool([])                                    #False
bool({})                                    #False
```

## Objects
If you have an object that is made from a class with a `len` function that returns 0 or False.

```python
class myclass():
  def __len__(self):
    return 0

myobj = myclass()
print(bool(myobj))                          #False
```

## Functions
Functions Can Return a Boolean Value

```python
def myFunction():
  return True

print(myFunction())                         #True

if myFunction():
  print("YES!")                             #YES!
else:
  print("NO!") 

x = 200
print(isinstance(x, int))                   #True
```

