## Lists in Python

Lists are used to store multiple items in a single variable. They're ordered, mutable, and can hold mixed data types.

---

### 🔢 Creating a List

```python
fruits = ["apple", "banana", "cherry"]
mixed = [1, "text", True]
```

You can access items by index (starting at 0):

```python
print(fruits[0])  # 'apple'
```

---

### 🧰 Useful List Methods

* `.append(x)` — Adds `x` to the end
* `.remove(x)` — Removes the first occurrence of `x`
* `.pop()` — Removes the last item (or item at a given index)
* `.insert(i, x)` — Inserts `x` at position `i`
* `.sort()` — Sorts items (only if all items are the same type)
* `.reverse()` — Reverses the list

---

### 🔁 Looping Through Lists

```python
for fruit in fruits:
    print(fruit)
```

---

### ➕ Summing Numeric Lists

```python
scores = [90, 85, 78]
total = sum(scores)
print(f"Total: {total}")
```

---

### ✅ Tips

* Lists are mutable, meaning they can be changed after creation
* Indexing can use negative numbers (`-1` is the last item)
* Use `len()` to get the number of elements in a list

> Lists are one of the most common and powerful data structures in Python. Mastering them is essential!
