# Lesson 4: Types and Casting — Why "5" and 5 Are Different 🔢📝

## Goal

Understand the **critical** difference between text and numbers in Python. Learn how to convert between them so your programs don't crash!

## What You'll Learn

- The difference between strings (text) and integers (whole numbers)
- Why `input()` always gives you text, even when you type numbers
- How to convert text to numbers with `int()` and `float()`
- How to convert numbers to text with `str()`
- How to avoid the most common beginner error in Python!

---

## Part 1: The Big Difference — Strings vs Numbers

This is **super important** and causes the most confusion for beginners:

- `"5"` (with quotes) is **text** — Python calls this a **string**
- `5` (without quotes) is a **number** — Python calls this an **integer**

They look the same to us, but Python treats them completely differently!

```python
print("5" + "5")    # Shows: 55 (glued the text together)
print(5 + 5)        # Shows: 10 (did the math)
```

Think of it like this: The string `"5"` is like the character "5" written on paper. The integer `5` is the actual number you can count with.

---

## Part 2: The Problem with `input()`

Here's the catch: **`input()` ALWAYS returns text (a string)**, even when the user types a number!

```python
age = input("How old are you? ")   # User types: 11
print(age)                          # Shows: 11 (looks like a number!)
print(age + 1)                      # ❌ ERROR! Can't add text and numbers!
```

**The error message:**
```
TypeError: can only concatenate str (not "int") to str
```

Python is saying: "You gave me text ('11') and asked me to add the number 1 to it. I don't know how to do that!"

---

## Part 3: The Solution — `int()` Converts Text to Numbers

`int()` is like a magical translator that converts text-numbers into real numbers Python can do math with.

```python
age_text = input("How old are you? ")    # User types: 11
age = int(age_text)                       # Convert text to number
print(age + 1)                            # ✅ Shows: 12 (math works!)
```

**Shortcut:** You can combine these into one line:
```python
age = int(input("How old are you? "))
print(age + 1)                            # Shows: 12
```

---

## Part 4: `float()` for Decimal Numbers

`int()` only works for whole numbers. For decimals, use `float()`:

```python
height = float(input("How tall are you in meters? "))   # User types: 1.5
print(f"In 10 years you might be {height + 0.2} meters!") # Shows: 1.7
```

**When to use which:**
- `int()` — whole numbers like age (11), score (100), lives (3)
- `float()` — decimal numbers like height (1.75), price (9.99), temperature (98.6)

---

## Part 5: `str()` Converts Numbers to Text

Sometimes you need to go the other way — turn a number into text:

```python
score = 100
# print("Your score is " + score)      # ❌ ERROR!
print("Your score is " + str(score))   # ✅ Shows: Your score is 100
```

**But remember:** F-strings handle this automatically!
```python
score = 100
print(f"Your score is {score}")        # ✅ Easier! F-strings are preferred.
```

---

## Part 6: Complete Example — Age Calculator

Let's put it all together:

```python
print("🎂 Age Calculator 🎂")

# Get birth year as TEXT, then convert to NUMBER
birth_year_text = input("What year were you born? ")
birth_year = int(birth_year_text)

# Or do it in one line (shortcut):
# birth_year = int(input("What year were you born? "))

current_year = 2025
age = current_year - birth_year

print(f"You are (or will be) {age} years old in {current_year}!")
print(f"Next year you'll be {age + 1}!")
```

---

## Part 7: What Happens If They Don't Type a Number?

If someone types "hello" and you try to use `int()`:

```python
age = int(input("How old are you? "))   # User types: hello
# ❌ ValueError: invalid literal for int() with base 10: 'hello'
```

Python crashes because "hello" can't be converted to a number. For now, just make sure to type actual numbers. (You'll learn how to handle this gracefully later!)

---

## Quick Reference

| Type | Example | Description | When to Use |
| ---- | ------- | ----------- | ----------- |
| `str` | `"hello"`, `"5"` | Text/string | Names, messages |
| `int` | `5`, `100`, `-3` | Whole number | Age, score, count |
| `float` | `3.14`, `9.99` | Decimal number | Price, height |

| Conversion | What it does |
| ---------- | ------------ |
| `int("5")` | Text → whole number |
| `float("3.14")` | Text → decimal number |
| `str(42)` | Number → text |

---

## Common Pitfalls (and Fixes!)

- **Forgot `int()` on input:** Remember, `input()` ALWAYS gives text!
- **Used `int()` on decimals:** `int("3.14")` ❌ crashes — use `float()` instead
- **Mixing types with `+`:** `"Score: " + 100` ❌ — use f-strings or `str()`

---

## 🏠 Homework Task: Simple Calculator

Create a calculator that asks for two numbers and shows the results of adding, subtracting, multiplying, and dividing them.

```python
print("🧮 Simple Calculator 🧮")

num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

print(f"{num1} + {num2} = {num1 + num2}")
print(f"{num1} - {num2} = {num1 - num2}")
print(f"{num1} × {num2} = {num1 * num2}")
print(f"{num1} ÷ {num2} = {num1 / num2}")
```

**Bonus Challenges:**
- Modify it to use `float()` so it works with decimal numbers too
- Add a calculation for the remainder (use `%`): `num1 % num2`

---

## ✅ Ready for Lesson 5?

If you understand that `input()` gives text and you need `int()` or `float()` for math, you're ready!

**Next up: Lesson 5 — Random Numbers (The Digital Dice!)**

