## Using `.map()` in Python

The `map()` function applies a given function to all items in an iterable (like a list) and returns a new iterable (a `map` object).

---

### 🧠 Basic Syntax

```python
map(function, iterable)
```

To see the results, convert the result to a list:

```python
nums = [1, 2, 3, 4]
doubled = list(map(lambda x: x * 2, nums))
print(doubled)  # [2, 4, 6, 8]
```

---

### ✅ When to Use `map()`

* When applying the same operation to every element in a list
* Useful for transforming data quickly and cleanly

---

### 📌 With Defined Functions

You can also pass a named function:

```python
def square(x):
    return x * x

nums = [1, 2, 3]
squares = list(map(square, nums))
print(squares)  # [1, 4, 9]
```

---

### 🆚 `map()` vs List Comprehensions

Both can do the same thing:

```python
# map()
list(map(lambda x: x + 1, [1, 2, 3]))

# list comprehension
[x + 1 for x in [1, 2, 3]]
```

Use whichever makes your code clearer.

> `map()` is powerful, especially when combined with `lambda`, `filter()`, or `reduce()`.
