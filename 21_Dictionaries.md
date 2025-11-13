## Working with Dictionaries in Python

Dictionaries store data as key-value pairs. They're unordered (before Python 3.7), mutable, and very useful for fast lookups.

---

### 🔑 Creating a Dictionary

```python
student = {
    "name": "Alice",
    "age": 20,
    "grades": [88, 92, 79]
}
```

Access values using keys:

```python
print(student["name"])  # Alice
```

---

### 🧰 Common Dictionary Methods

* `.get(key)` — Safely get a value (returns `None` if not found)
* `.keys()` — Returns all keys
* `.values()` — Returns all values
* `.items()` — Returns key-value pairs as tuples
* `.update({...})` — Update or add new key-value pairs

---

### 🔁 Looping with `.items()`

```python
for key, value in student.items():
    print(f"{key}: {value}")
```

---

### 📦 Unpacking Lists in Dictionaries

You can unpack lists stored in values:

```python
fonts = {
    "Roboto": ["Roboto-Bold.ttf", "Roboto-Regular.ttf"],
    "Lato": ["Lato-Light.ttf"]
}

for name, files in fonts.items():
    for file in files:
        print(f"Font file: {file}")
```

Use `*files` to unpack unknown-length lists:

```python
for name, *files in fonts.items():
    print(name, files)
```

---

### ✅ Tips

* Keys must be immutable (strings, numbers, tuples)
* Values can be any data type
* Dictionaries are very useful for structuring real-world data

> Dictionaries help model structured, relational data and are an essential tool in any Python programmer’s toolkit!
