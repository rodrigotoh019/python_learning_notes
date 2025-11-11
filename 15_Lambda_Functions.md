## Lambda Functions in Python

Lambda functions are small anonymous functions defined using the `lambda` keyword. They're often used for short, simple operations.

---

### 🧠 Basic Syntax

```python
lambda arguments: expression
```

Example:

```python
double = lambda x: x * 2
print(double(5))  # 10
```

---

### ✅ When to Use Lambda

* When you need a small function temporarily
* Often used with `map()`, `filter()`, or `sorted()`

---

### 🔍 Example with `sorted()`

```python
students = [("Alice", 90), ("Bob", 85), ("Eve", 95)]

# Sort by score (second item in tuple)
sorted_students = sorted(students, key=lambda student: student[1])
print(sorted_students)
```

---

### 🔄 More Examples

```python
add = lambda a, b: a + b
print(add(3, 7))  # 10

is_even = lambda x: x % 2 == 0
print(is_even(4))  # True
```

---

### ⚠️ Limitations

* Limited to one expression (no statements or multiple lines)
* Not a replacement for full `def` functions when logic gets complex

> Use lambda functions for quick, inline operations — they're compact and useful, but best kept simple!
