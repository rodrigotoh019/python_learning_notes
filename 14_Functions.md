## Functions in Python

Functions help you group reusable blocks of code. They improve organization, avoid repetition, and make your code easier to maintain.

---

### 🛠️ Defining a Function

```python
def greet():
    print("Hello!")

greet()  # Calls the function
```

Use `def` to define a function, followed by a name and parentheses.

---

### 📥 Parameters and Arguments

You can pass values into a function:

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
```

Use default values if needed:

```python
def greet(name="Guest"):
    print(f"Welcome, {name}!")
```

---

### 🔁 Returning Values

Functions can return results:

```python
def add(x, y):
    return x + y

result = add(3, 5)  # result is 8
```

---

### 📦 Return Multiple Values

Use a tuple or list to return more than one value:

```python
def calc(x, y):
    return x + y, x * y

sum_val, product = calc(2, 4)
```

---

### ✅ Tips

* Use descriptive names for functions and parameters
* Keep functions focused on a single task
* Document them with comments or docstrings

> Functions are essential for clean, organized, and reusable code!
