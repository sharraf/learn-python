# Lesson 1: Hello World — Your Computer's Voice 🖨️

## Goal

Make your computer talk! By the end of this lesson, you'll know how to display text and numbers on the screen using Python's `print()` function.

## What You'll Learn

- What `print()` does (displays output on the screen)
- How to print text (strings) using quotes
- How to print numbers (without quotes)
- The difference between strings and numbers

---

## Part 1: Meet `print()`

Think of `print()` as your computer's way of talking to you! Just like you might shout something to get someone's attention, `print()` displays text on the screen so you can see it.

```python
print("Hello, world!")
```

When you run this, you'll see:
```
Hello, world!
```

**Try it yourself!** Create a new Python file and type:

```python
print("Hello, world!")
print("I am learning Python!")
print("This is so cool!")
```

---

## Part 2: Strings — Text in Quotes

When you want to print text (words, sentences, symbols), you put it inside quotes. This is called a **string**.

```python
print("My name is Luna")
print('I love pizza')
```

You can use double quotes `"..."` or single quotes `'...'` — both work the same way!

**Important:** The quotes tell Python "this is text, not code." Without quotes, Python gets confused.

```python
print("Hello")   # ✅ Works! Python knows it's text
# print(Hello)   # ❌ Error! Python thinks Hello is a command
```

---

## Part 3: Numbers — No Quotes Needed

When you want to print numbers, you don't need quotes:

```python
print(42)
print(3.14)
print(100)
```

Python knows these are numbers because there are no quotes around them.

**You can even do math inside `print()`:**

```python
print(2 + 2)       # Shows: 4
print(10 - 3)      # Shows: 7
print(5 * 4)       # Shows: 20
print(15 / 3)      # Shows: 5.0
```

---

## Part 4: Strings vs Numbers — What's the Difference?

This is **super important** to understand:

- `"5"` with quotes is **text** (a string) — it's the character "5"
- `5` without quotes is a **number** — Python can do math with it

Watch what happens:

```python
print("5" + "5")   # Shows: 55 (glued the text together!)
print(5 + 5)       # Shows: 10 (did the math!)
```

See the difference? With strings, `+` glues them together. With numbers, `+` adds them.

---

## Part 5: Fun with Print

You can make cool patterns and art with `print()`:

```python
print("=" * 20)           # Prints 20 equal signs: ====================
print("*" * 10)           # Prints 10 stars: **********
print("Hello! " * 3)      # Prints: Hello! Hello! Hello!
```

**Make a simple banner:**

```python
print("=" * 30)
print("   Welcome to My Program!")
print("=" * 30)
```

---

## Common Pitfalls (and Fixes!)

| Problem | Fix |
|---------|-----|
| Forgot quotes around text | Add `"..."` around your text |
| Used the wrong type of quotes | Make sure opening and closing quotes match |
| Nothing shows up | Make sure you saved and ran the file |

---

## 🏠 Homework Task

Create a program that prints:
1. Your name
2. Your age (as a number, no quotes)
3. Your favorite food
4. A math problem and its answer (like `print(7 * 8)`)
5. A cool banner using `"=" * 20` or similar

**Example output:**
```
Luna
11
Pizza
56
====================
 Welcome to Python!
====================
```

---

## ✅ Ready for Lesson 2?

If you can make your computer print text and numbers, you're ready!

**Next up: Lesson 2 — Variables (Memory Boxes)**
