# Lesson 0: VS Code Setup (Write + Run Python) 🧰💻

## Goal
Get your computer ready to write and run Python code using **VS Code**.

By the end, you will:
- open this lesson folder in VS Code
- create a Python file (`.py`)
- run it and see the output

---

## What you’ll learn
- What VS Code is (a code editor)
- How to install **Python** (the language) and the **Python extension** (the helper)
- How to run a `.py` file in VS Code and in the terminal

---

## Step 1: Install VS Code
1. Download VS Code from: https://code.visualstudio.com/
2. Install it like any other app.

Tip for grown-ups: VS Code is free.

---

## Step 2: Install Python (the language)
Python is the thing that actually runs your code.

1. Download Python 3 from: https://www.python.org/downloads/
2. Install it.

### Windows super-important step ✅
During installation, check the box:
**“Add Python to PATH”**

---

## Step 3: Open VS Code and install the Python extension
1. Open **VS Code**
2. Click the **Extensions** icon (it looks like 4 blocks)
3. Search for **Python**
4. Install the one by **Microsoft**

This extension adds a Run button, helps you find errors, and makes coding easier.

---

## Step 4: Open the lesson folder in VS Code
In VS Code:
1. Click **File → Open Folder…**
2. Choose this project folder (the one that contains the `lessons/` folder)

Now you can see all the lesson files on the left.

---

## Step 5: Create your first Python file
1. In the left sidebar (Explorer), right-click and choose **New File**
2. Name it: `hello.py`

Important: it must end with **`.py`**.

---

## Step 6: Write your first program
In `hello.py`, type:

```python
print("Hello, world!")
print("I can run Python from VS Code!")
```

Save the file:
- Windows/Linux: **Ctrl + S**
- Mac: **Cmd + S**

---

## Step 7: Run your program (two ways)

### Way A (easy): Run button
1. Open `hello.py`
2. Look for a **Run** / **Play ▶** button near the top right
3. Click it

You should see your text in the **Terminal** panel at the bottom.

### Way B (power-up): Run in the terminal
1. Open the terminal in VS Code: **Terminal → New Terminal**
2. Type one of these:

- On Mac/Linux (usually): `python3 hello.py`
- On Windows (often): `python hello.py`

Press Enter.

---

## Step 8: Pick the right Python (if VS Code asks)
Sometimes VS Code asks you to choose a Python interpreter.

Pick the one that says **Python 3**.
If you see multiple, choose the newest one.

---

## Step 9: How to use VS Code during these lessons
Here's a simple workflow to use every time:
1. Open the lesson file in `lessons/` (it's a Markdown `.md` file)
2. Create a folder named `practice/` (optional, but recommended)
3. Make a new Python file like `practice/lesson01.py`
4. Type the code from the lesson (or start from the example)
5. Run it (Run button or terminal)

---

## Common problems (quick fixes)

### “python is not recognized” / “command not found: python”
- Python isn’t installed OR it wasn’t added to PATH.
- Try restarting VS Code.
- On Mac/Linux try `python3` instead of `python`.

### Nothing happens when you run
- Make sure you **saved** the file.
- Make sure you’re running `hello.py` (not a different file).

### You see red squiggles everywhere
- Make sure the Python extension (Microsoft) is installed.
- Make sure VS Code is using Python 3 (Step 8).

---

## ✅ Ready for Lesson 1?
If you can run `hello.py` and see output, you’re ready.

Next up: **Lesson 1: Printing**

---

## 🏠 Homework
Make `hello.py` say:
1. your name
2. your favorite animal
3. a “cool banner” line like `"=" * 20`