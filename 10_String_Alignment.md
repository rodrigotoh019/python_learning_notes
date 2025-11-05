## String Alignment with f-strings

f-strings not only format values — they can also align text for clean, readable output.

---

### 📐 Alignment Options

Use a colon `:` followed by a symbol to control alignment and width.

* `<` — Left-align
* `>` — Right-align
* `^` — Center-align

```python
name = "Alice"
print(f"{name:<10} | Left")
print(f"{name:>10} | Right")
print(f"{name:^10} | Center")
```

Output:

```
Alice      | Left
     Alice | Right
  Alice    | Center
```

---

### 📊 Formatting Tabular Data

You can use f-string alignment when printing table-like rows:

```python
print(f"{'Name':<10}{'Score':>6}")
print(f"{'Alice':<10}{95:>6}")
print(f"{'Bob':<10}{88:>6}")
```

Output:

```
Name         Score
Alice           95
Bob             88
```

---

### ✅ Tips

* Adjust the number after the symbol to control column width
* Useful in CLI tools, reports, or logs

> Aligning strings helps present information clearly — especially in terminal apps or when showing lists, tables, or summaries.
