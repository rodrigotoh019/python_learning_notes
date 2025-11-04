## Loops in Python

Loops let you run a block of code multiple times. Python has two main types: `for` loops and `while` loops.

---

### 🔁 For Loop

Used when you want to repeat a block a specific number of times.

#### Basic Syntax:

```python
for i in range(5):
    print(i)
```

This prints numbers from 0 to 4 (5 is excluded).

#### `range(start, stop, step)`:

* `start`: Where to begin (default is 0)
* `stop`: Where to stop (not inclusive)
* `step`: How much to increase each time (default is 1)

```python
for i in range(1, 6):
    print(i)  # Prints 1 to 5
```

---

### 🔄 While Loop

Used when you want the loop to continue **until a condition is no longer true**.

#### Basic Syntax:

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

> 🧠 Use `while` when you don’t know how many times the loop will run — like waiting for user input or validating data.

---

### ✅ Tips

* Use `break` to exit a loop early
* Use `continue` to skip the rest of the loop and go to the next iteration

```python
for i in range(10):
    if i == 5:
        break  # Stops the loop
    print(i)
```

```python
for i in range(5):
    if i == 2:
        continue  # Skips when i is 2
    print(i)
```

Both loop types are powerful — choose based on whether you know how many iterations you need!
