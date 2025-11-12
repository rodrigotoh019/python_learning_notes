## The `zip()` Function in Python

The `zip()` function combines multiple iterables (like lists or tuples) into one iterable of tuples.

---

### 🔗 Basic Usage

```python
names = ["Alice", "Bob", "Eve"]
scores = [95, 80, 88]

paired = zip(names, scores)
print(list(paired))
# [('Alice', 95), ('Bob', 80), ('Eve', 88)]
```

Each tuple contains one element from each input iterable.

---

### 🔁 Looping with `zip()`

```python
for name, score in zip(names, scores):
    print(f"{name} scored {score}")
```

---

### ⚠️ Length Mismatch

`zip()` stops at the shortest iterable:

```python
list(zip([1, 2], ["a", "b", "c"]))
# [(1, 'a'), (2, 'b')]
```

Use `itertools.zip_longest()` if you need to handle uneven lengths.

---

### ✅ Tips

* `zip()` is great for pairing data from multiple sources
* Often used for combining names and values, or questions and answers
* Produces an iterable, convert to list or tuple to view or reuse

> `zip()` makes it easy to merge data and is especially useful in loops and data processing!
