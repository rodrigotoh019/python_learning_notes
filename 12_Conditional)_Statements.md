## Conditional Statements in Python

Conditional statements let your code make decisions based on conditions.

---

### 🧾 if-elif-else Structure

```python
age = 18

if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teen")
else:
    print("Child")
```

* `if` checks the first condition
* `elif` checks the next one if the previous is False
* `else` runs if none of the above are True

---

### ✅ Ternary Expression (One-liner if-else)

A compact way to assign a value based on a condition:

```python
status = "Adult" if age >= 18 else "Minor"
```

---

### 🔍 Comparison Operators

* `==` — equal to
* `!=` — not equal to
* `<`, `>`, `<=`, `>=` — less/greater than (or equal to)

---

### 🧠 Logical Operators

* `and`: All conditions must be true
* `or`: At least one must be true
* `not`: Reverses a condition

```python
if age > 18 and has_id:
    print("Access granted")
```

> Conditions are the backbone of decision-making in Python. Mastering them builds the logic behind every real-world program!
