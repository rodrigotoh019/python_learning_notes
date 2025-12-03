# Understanding JSON in Python 📋

> **Note:** This is based on my current understanding of JSON as I learn Python. I'll update and expand this as I gain more experience!

## What is JSON?

* **JSON** stands for **JavaScript Object Notation**.
* Despite the name, it works with Python and many other programming languages!
* JSON is a **universal format** that helps different programs share data with each other.

**What makes JSON special:**

* ✅ **Human-readable** - You can open it in any text editor and understand it
* ✅ **Lightweight** - Small file sizes
* ✅ **Easy to work with** - Simple conversion between JSON and Python

## What Does JSON Look Like?

```json
{
    "name": "Alice",
    "age": 25,
    "hobbies": ["reading", "gaming", "coding"]
}
```

> Notice how similar this looks to Python dictionaries? That's intentional!

## JSON Data Types

| JSON Type | Python Equivalent | Example |
|-----------|------------------|---------|
| Object | Dictionary | `{"key": "value"}` |
| Array | List | `[1, 2, 3]` |
| String | String | `"hello"` |
| Number | Int or Float | `42` or `3.14` |
| Boolean | Boolean | `true` or `false` |
| Null | None | `null` |

### Key Differences from Python:

* JSON uses `true`/`false` (lowercase), Python uses `True`/`False` (capitalized)
* JSON uses `null`, Python uses `None`
* JSON only allows **double quotes** `"` for strings

> Don't worry - Python handles these conversions automatically!

## Why Use JSON?

### Saving App Settings

Store user preferences so they persist even after closing the app:

```json
{
    "theme": "dark",
    "language": "en",
    "volume": 70
}
```

### Keeping Data Between Sessions

Save data so users don't lose their progress:

```json
{
    "username": "Guest",
    "level": 5,
    "high_score": 100
}
```

## Python's `json` Module

Python has a built-in module for working with JSON:

```python
import json
```

### The Four Main Functions

| Function | Purpose | Memory Trick |
|----------|---------|--------------|
| `json.dump()` | Write to file | **dump** = dump data OUT to file |
| `json.dumps()` | Convert to string | **dumps** = dump to **s**tring |
| `json.load()` | Read from file | **load** = load data IN from file |
| `json.loads()` | Parse string | **loads** = load from **s**tring |

> **Remember:** "dump" = write OUT, "load" = read IN. The extra "s" = working with strings instead of files.

---

## `json.dump()` - Write to File

**Purpose:** Save Python data to a JSON file

```python
import json

data = {
    "name": "Bob",
    "age": 30
}

# Save to file with readable formatting
with open("data.json", "w") as f:
    json.dump(data, f, indent=4)
```

**Parameters:**

* First parameter (`data`) - Python data to save
* Second parameter (`f`) - File object
* `indent=4` - Optional, adds 4-space indentation for readability

---

## `json.load()` - Read from File

**Purpose:** Read JSON file and convert to Python objects

```python
import json

# Read from file
with open("data.json", "r") as f:
    data = json.load(f)

print(data)  # Python dictionary!
print(data["name"])  # Access like normal dict
```

### Handling Missing Files

```python
import json
import os

if os.path.exists("settings.json"):
    with open("settings.json", "r") as f:
        settings = json.load(f)
else:
    # Use defaults if file doesn't exist
    settings = {"theme": "light", "volume": 50}
```

> This prevents crashes and provides sensible defaults!

---

## Complete Example: Save and Load Settings

Here's a practical example I use in my programs:

```python
import json
import os

CONFIG_FILE = "my_settings.json"

def load_settings():
    """Load settings from file, or return defaults"""
    if os.path.exists(CONFIG_FILE):
        with open(CONFIG_FILE, "r") as f:
            return json.load(f)
    else:
        return {
            "color": "white",
            "name": "User"
        }

def save_settings(settings):
    """Save settings to file"""
    with open(CONFIG_FILE, "w") as f:
        json.dump(settings, f, indent=4)
    print(f"Saved: {settings}")

# Load on startup
settings = load_settings()

# Modify settings
settings["color"] = "green"

# Save changes
save_settings(settings)
```

**What's happening:**

1. Program tries to load `my_settings.json`
2. If it doesn't exist (first run), uses default values
3. User can modify settings during the program
4. Changes are saved back to the file
5. Next time, their settings load automatically!

---

## Common JSON Operations

### Add New Key

```python
settings = {"theme": "dark"}
settings["language"] = "en"
```

### Update Existing Key

```python
settings["theme"] = "light"
```

### Remove Key

```python
del settings["theme"]
```

### Check if Key Exists

```python
if "theme" in settings:
    print(settings["theme"])
```

---

## Best Practices

### ✅ Always Use Indentation

```python
# Readable
json.dump(data, f, indent=4)
```

### ✅ Handle Missing Files

```python
if os.path.exists("file.json"):
    with open("file.json", "r") as f:
        data = json.load(f)
else:
    data = {}  # Use defaults
```

### ✅ Handle Errors

```python
try:
    with open("data.json", "r") as f:
        data = json.load(f)
except json.JSONDecodeError:
    print("Invalid JSON!")
    data = {}
except FileNotFoundError:
    print("File not found!")
    data = {}
```

---

## ⚠️ Security Note

**Don't store sensitive information in plain JSON files!**

Plain JSON files are just text - anyone can open them and read everything.

### 🔴 Never Store:

* Passwords
* API keys
* Credit card numbers
* Personal identification numbers

### 🟢 Safe to Store:

* App preferences (theme, language, font size)
* Non-sensitive user choices
* UI settings

> If you need to store sensitive data, you'll need encryption or other security methods!

---

## Quick Reference

```python
import json

# Write to file
with open("file.json", "w") as f:
    json.dump(data, f, indent=4)

# Read from file
with open("file.json", "r") as f:
    data = json.load(f)

# Check if file exists
import os
if os.path.exists("file.json"):
    # File exists
    pass
```

---

## Summary

* JSON is a format for storing and sharing data
* Python's `json` module provides `dump()` and `load()` for working with files
* `dump()` writes Python data to JSON files
* `load()` reads JSON files into Python
* Always use `with open()` when working with files
* Use `indent=4` to make JSON files readable
* Handle missing files with `os.path.exists()`
* Never store passwords or sensitive data in plain JSON

> **Note:** As I continue learning, I'll add more advanced topics like `dumps()` and `loads()` for working with JSON strings. For now, these basics cover what I need for my projects! 🚀