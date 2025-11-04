## String Methods in Python

String methods are built-in functions that help you manipulate and work with text.

### ✂️ Common String Methods

* `.split()` — Splits a string into a list using spaces or a specified delimiter:

```python
text = "apple,banana,orange"
fruits = text.split(",")
# ['apple', 'banana', 'orange']
```

* `.strip()` — Removes whitespace (or characters) from the beginning and end:

```python
name = "  Alice  "
cleaned = name.strip()  # 'Alice'
```

* `.lower()` and `.upper()` — Converts to lowercase or uppercase:

```python
"HeLLo".lower()  # 'hello'
"hi".upper()     # 'HI'
```

* `.capitalize()` — Capitalizes only the first letter:

```python
"python is fun".capitalize()  # 'Python is fun'
```

* `.title()` — Capitalizes the first letter of every word:

```python
"hello world".title()  # 'Hello World'
```

* `.replace()` — Replaces part of the string:

```python
"I love Java".replace("Java", "Python")
# 'I love Python'
```

### 🔍 Other Useful Tools

* `len()` — Counts the number of characters in a string

```python
len("Python")  # 6
```

> 🔹 Many string methods return a **new** string — they don’t modify the original string.

### ✅ Tip:

Chain string methods for powerful one-liners:

```python
sentence = "  hello world  "
formatted = sentence.strip().title()
# 'Hello World'
```