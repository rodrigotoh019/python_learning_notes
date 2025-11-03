## Data Types in Python

In Python, data types define what kind of value a variable holds. Understanding data types helps you handle data correctly and avoid unexpected errors.

### 🔢 Basic Data Types

* `int`: Whole numbers (e.g. `5`, `-12`, `1000`)
* `float`: Decimal numbers (e.g. `3.14`, `-0.5`, `2.0`)
* `str`: Strings, or text data (e.g. `'hello'`, `'123'`, `"Python"`)
* `bool`: Boolean values representing `True` or `False`

### 🧠 Type Checking

Use `type()` to check the data type of a value or variable:

```python
print(type(42))         # <class 'int'>
print(type("hello"))   # <class 'str'>
```

### 🔁 Type Conversion

Sometimes you need to convert between types:

```python
int("42")       # Converts string to integer
float("3.14")   # Converts string to float
str(123)         # Converts integer to string
```

> ⚠️ Be careful when converting strings, they must be valid numbers or you'll get a `ValueError`.

### ✅ Quick Tip:

Use descriptive variable names that hint at the expected data type, especially in large programs or collaborative projects.
