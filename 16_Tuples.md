## Tuples in Python

Tuples are ordered, immutable collections. Once created, their values cannot be changed.

---

### 🛠️ Creating Tuples

```python
tuple1 = (1, 2, 3)
tuple2 = ("apple", "banana", "cherry")
tuple3 = ()         # Empty tuple
tuple4 = (5,)       # Single-element tuple (note the comma!)
```

---

### 🔍 Accessing Elements

Just like lists, tuples are indexed starting at 0:

```python
tuple1 = (10, 20, 30)
print(tuple1[1])  # 20
```

---

### 🧰 Tuple Methods

* `.count(x)` — Counts how many times `x` appears
* `.index(x)` — Returns the index of the first occurrence of `x`

```python
sample = (1, 2, 2, 3)
print(sample.count(2))  # 2
print(sample.index(3))  # 3
```

---

### 📦 Tuple Unpacking

You can assign tuple elements to variables:

```python
x, y = (5, 10)
print(x)  # 5
print(y)  # 10
```

Use `*` for variable-length unpacking:

```python
a, *b = (1, 2, 3, 4)
print(a)  # 1
print(b)  # [2, 3, 4]
```

---

### ✅ Tips

* Use tuples when data should not change
* Great for representing fixed sets of values, like coordinates or records

> Tuples are a safe and memory-efficient way to store grouped data that you don't want to modify.
