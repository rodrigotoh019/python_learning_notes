## List Comprehensions in Python

List comprehensions offer a concise way to create lists in a single line of code.

---

### 🔧 Basic Syntax

```python
new_list = [expression for item in iterable]
```

Example:

```python
squares = [x**2 for x in range(1, 6)]
# [1, 4, 9, 16, 25]
```

---

### ✅ With Conditions

Add an `if` clause to filter items:

```python
even_numbers = [x for x in range(10) if x % 2 == 0]
# [0, 2, 4, 6, 8]
```

You can also include an `else` for inline conditional logic:

```python
labels = ["even" if x % 2 == 0 else "odd" for x in range(5)]
# ['even', 'odd', 'even', 'odd', 'even']
```

---

### 🧠 Advantages

* Shorter and more readable than traditional `for` loops
* Often faster in execution

> Use list comprehensions when you want to transform or filter data from an iterable into a new list — clean and Pythonic!
