## Tuple of Tuples in Python

A tuple of tuples is simply a collection of fixed pairs (or groups) stored as immutable tuples inside a main tuple.

---

### 📦 Why Use Tuple of Tuples?

* Ideal for structured, read-only data
* Keeps records grouped and safe from modification

---

### 🧱 Example: Storing Student Scores

```python
students = (("Alice", 95), ("Bob", 80), ("Eve", 88))
```

You can loop through and unpack the tuples:

```python
for name, score in students:
    print(f"{name} scored {score}")
```

---

### 🔍 Accessing Elements

Access individual records and elements like this:

```python
print(students[1])      # ("Bob", 80)
print(students[1][0])   # "Bob"
print(students[1][1])   # 80
```

---

### ✅ Tips

* Useful when you need read-only, tabular-style data
* Since they're immutable, you can use them as dictionary keys or set elements

> Tuple of tuples is a simple but powerful structure when you need predictable, locked-down datasets!
