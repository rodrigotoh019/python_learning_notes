## Strings and Quotations in Python

Strings are sequences of characters enclosed in quotes. They are used to store text-based data.

### 🧵 Creating Strings

You can create strings using:

* Single quotes: `'Hello'`
* Double quotes: `"World"`
* Triple quotes (single or double): `'''Multi-line'''` or `"""Multi-line"""`

Triple quotes allow you to write multi-line strings:

```python
message = '''This is
a multi-line
string.'''
```

### 🔤 String Formatting with f-strings

f-strings let you embed expressions inside string literals using curly braces `{}`:

```python
name = "Alice"
score = 95
print(f"{name} scored {score} points.")
```

You can also format numbers:

```python
price = 12.5
print(f"Price: ${price:.2f}")  # Output: Price: $12.50
```

### ✅ Tip:

* Prefer f-strings for formatting as they are concise and readable (Python 3.6+)
* You can use escape characters like `\n` (newline), `\t` (tab), and `\"` (quote)

### 🔍 Example:

```python
quote = 'She said, "Python is awesome!"'
print(quote)
```
