## Tkinter GUI Concepts

Tkinter is Python’s standard GUI (Graphical User Interface) library. It allows you to build desktop applications with windows, buttons, labels, and more.

---

### 🧱 Basic Structure

```python
import tkinter as tk

root = tk.Tk()
root.title("My App")
root.mainloop()
```

* `tk.Tk()` creates the main application window
* `.mainloop()` keeps the window open and listens for events

---

### 🏷️ Widgets

Widgets are elements like labels, buttons, and entry fields:

```python
label = tk.Label(root, text="Hello")
label.pack()
```

Common widgets:

* `Label` – display text or images
* `Button` – clickable actions
* `Entry` – single-line text input
* `Text` – multiline text area

---

### 📐 Geometry Managers

Control widget placement using:

* `.pack()` – simple vertical/horizontal stacking
* `.grid()` – row/column layout
* `.place()` – absolute positioning

```python
label.grid(row=0, column=0)
```

---

### 🖼️ Adding Images (Logo Example)

```python
photo = tk.PhotoImage(file="logo.png")
logo_label = tk.Label(root, image=photo)
logo_label.pack()
```

Use `PhotoImage` for `.png` files. For `.jpg`, use `PIL` or `Pillow`.

---

### ✅ Tips

* Always create the root window first
* Use `.mainloop()` once at the end
* Try `ttk` (themed Tkinter) for modern widget styling

> Tkinter is beginner-friendly and a great way to start building desktop apps in Python!
