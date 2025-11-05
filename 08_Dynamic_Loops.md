## Dynamic Loops in Python

Dynamic loops adjust based on user input or data length, making your program flexible and interactive.

### 📥 User-Controlled Repetition

Let the user decide how many times a loop should run:

```python
n = int(input("How many items? "))

for i in range(1, n + 1):
    item = input(f"Enter item {i}: ")
    print(f"Item {i}: {item}")
```

This allows the loop to run `n` times, where `n` is provided at runtime.

---

### 🗃️ Building Lists Dynamically

You can collect data into a list during a loop:

```python
n = int(input("How many numbers? "))
numbers = []

for i in range(n):
    number = int(input(f"Enter number {i + 1}: "))
    numbers.append(number)

print(numbers)
```

This technique is great for storing scores, names, answers, and more.

---

### ✅ Tips

* Always validate user input when possible
* Consider using a `while` loop if the number of repetitions isn’t known in advance

> 🔄 Dynamic loops let your program adapt to real input — they’re essential for interactive scripts!
