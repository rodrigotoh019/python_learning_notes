### Python Learning Notes (Organized by Topic)

---

## 1. Arithmetic Operators

* `+` Addition: Adds two numbers
* `-` Subtraction: Subtracts the second number from the first
* `*` Multiplication: Multiplies two numbers
* `/` Division: Returns a float result
* `//` Floor Division: Returns the integer result of division
* `%` Modulo: Returns the remainder of a division
* `**` Exponentiation: Raises a number to the power of another

---

## 2. Variables

* Used to temporarily store data in memory
* Use lowercase letters and underscores `_` for naming conventions

---

## 3. Data Types

* `str` – Text or string values
* `int` – Whole numbers
* `float` – Decimal numbers
* `bool` – Boolean values (`True` or `False`)

> Tip: Use type conversion functions like `int()`, `float()`, and `str()` to convert data between types.

---

## 4. Strings and Quotations

* Single quotes `'` and double quotes `"` can be used to define strings
* Triple quotes `'''` allow multiline strings
* f-strings: `f"Total: {value:.2f}"` format strings dynamically

---

## 5. Input and Type Conversion

* `input()` collects input as a string
* Convert as needed: `int(input(...))`, `float(input(...))`

---

## 6. String Methods

* `.split()` breaks strings into lists
* `len()` counts characters or items in a collection

---

## 7. Loops

### For Loop

* Repeats a block using `range(start, stop, step)`
* Example: `for i in range(5)` runs 5 times from 0 to 4

### While Loop

* Runs while a condition is `True`
* Useful for input validation, re-prompts, or menu systems

---

## 8. Dynamic Loops

* Let users decide how many times the loop should run
* Store responses in a list dynamically:

```python
for i in range(1, n + 1):
    data.append(input(...))
```

---

## 9. Lists

* Mutable, ordered sequences
* Use `append()` to add items
* Use `sum()` to total numeric values

---

## 10. String Alignment with f-strings

* `<` Left-align: `f"{text:<20}"`
* `>` Right-align: `f"{text:>20}"`
* `^` Center-align: `f"{text:^20}"`
* Useful for printing tabular data

---

## 11. Using `.map()`

* Apply a function to all items in a list

```python
doubled = list(map(lambda x: x * 2, [1, 2, 3]))
```

---

## 12. Conditional Statements

### If-Else Structure

```python
if condition:
    ...
elif another_condition:
    ...
else:
    ...
```

### Ternary Expression

```python
value = x if condition else y
```

---

## 13. List Comprehensions

* Concise way to create lists:

```python
squares = [i**2 for i in range(1, 6)]
```

* Can include conditions: `[x for x in range(10) if x % 2 == 0]`

---

## 14. Functions

```python
def function_name(parameters):
    return value
```

* Use `return` to get values back
* Can have default parameters: `def greet(name="Guest")`
* Return multiple values using tuples or lists

---

## 15. Lambda Functions

* Anonymous one-liner functions: `lambda x: x + 10`
* Great with `sorted()`, `map()`, `filter()`

---

## 16. Tuples

* Immutable sequences
* Indexed like lists: `tuple[0]`
* Methods: `.count()`, `.index()`
* Unpacking: `x, y = (1, 2)`

---

## 17. Tuple of Tuples

```python
students = (("Alice", 95), ("Bob", 80))
```

* Good for storing fixed records like name-score pairs

---

## 18. The `zip()` Function

* Pairs elements from multiple lists:

```python
zip(names, grades)
```

* Returns iterable of tuples: `[('Alice', 95), ...]`

---

## 19. Error Handling

```python
try:
    ...
except ExceptionType:
    ...
else:
    ...
finally:
    ...
```

* Use `finally` to always run cleanup code
* Handle specific errors like `ValueError`, `ZeroDivisionError`

---

## 20. Tkinter GUI Concepts

* Use `Label()` to display text/images
* `.pack()`, `.grid()`, `.place()` = geometry managers
* Use `PhotoImage()` to load and display logos/images
* `text=""` is a placeholder until the value is updated programmatically

---

## 21. Working with Dictionaries

### Unpacking with `.items()`

```python
for key, value in dict.items():
    print(key, value)
```

* Use `*value` to unpack lists of unknown length
* Often used in loading data like fonts or student grades

---

## 22. Importing Modules

* `import module` to load a full module
* `import module as alias` for cleaner code (e.g., `import numpy as np`)
* `from module import item` to bring in just what you need
* Use aliases for standard packages (`tk`, `np`, `pd`, etc.)

---
