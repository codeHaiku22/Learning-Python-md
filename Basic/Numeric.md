## Python Numbers

There are 3 numeric types in Python:
- Integer
- Float
- Complex

### `int`
Integer, or `int`, is a whole number that can be positive or negative of unlimited length.

```python
x = 1
y = 35656222554887711
z = 3255522

print(type(x))
print(type(y))
print(type(y))
```

### `float`
Floating point number, or `float` is a number that can be positive or negative containing one or more decimal places.

```python
x = 1.10
y = 1.0
x = -35.59

print(type(x))
print(type(y))
print(type(y))

#Float can also include scientific notation with an "e" to indicate the power of 10.
x = 35e3
y = 12E4
z = -87.7e100

print(type(x))
print(type(y))
print(type(y))
```

### `complex`
Complex numbers, or `complex`, are written with `j` as the imaginary part.

```python
x = 3+5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(y))
```

### Type Conversion
You can convert from one type to another with the `int()`, `float()`, and `complex()` methods.

```python
x = 3+5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(y))

x = 1
y = 2.8
z = 1j

#int to float
a = float(x)

#float to int
b = int(y)

#int to complex
c = complex(x)

print(a)            #1.0
print(b)            #2
print(c)            #(1+0j)

print(type(a))      #<class 'float'>
print(type(b))      #<class 'int'>
print(type(c))      #<class 'complex'>
```

### Random Number
Python does not have a `random()` function to generate a random number.  However, Python does have a built in module called `random` that can be used to make random numbers.

```python
import random

print(random.randrange(1, 10))      #2
```
