## Error Handling in Python

Python allows you to handle errors gracefully using `try`, `except`, `else`, and `finally` blocks.

---

### 🔐 Basic Try-Except Structure

```python
try:
    number = int(input("Enter a number: "))
except ValueError:
    print("That’s not a valid number.")
```

Use this to catch and handle expected errors without crashing your program.

---

### 🎯 Catching Specific Exceptions

You can catch different error types with multiple except blocks:

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("You can't divide by zero!")
except ValueError:
    print("Invalid input.")
```

---

### ✅ Optional Else Block

Runs only if no exceptions occur:

```python
try:
    print("No error here!")
except:
    print("Something went wrong")
else:
    print("All good!")
```

---

### ♻️ Finally Block

Always runs, whether there was an error or not:

```python
try:
    print("Trying something risky")
finally:
    print("Cleanup done")
```

---

### 🧠 Tips

* Catch specific errors rather than a general `except:` when possible
* Use `finally` to close files, connections, or cleanup code
* Don’t ignore exceptions silently, always log or handle them clearly

> Error handling keeps your programs robust and user-friendly!
