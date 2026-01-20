# Lesson 6: If/Else Logic — Making Decisions 🤔

## Goal

Teach your program to make decisions! Learn how to use `if`, `elif`, and `else` to run different code based on conditions.

## What You'll Learn

- How comparison operators work (`>`, `<`, `>=`, `<=`, `==`, `!=`)
- How to use `if` statements to make decisions
- How to use `elif` for multiple choices
- How to use `else` as a catch-all
- **CRITICAL:** How indentation works in Python (this is required syntax!)

---

## Part 1: Comparison Operators — The Decision Makers

These special symbols help your program compare things and make decisions:

| Operator | Meaning | Example | Result |
| -------- | ------- | ------- | ------ |
| `>` | greater than | `15 > 10` | True |
| `<` | less than | `5 < 10` | True |
| `>=` | greater than or equal | `13 >= 13` | True |
| `<=` | less than or equal | `5 <= 10` | True |
| `==` | equal to | `5 == 5` | True |
| `!=` | not equal to | `5 != 3` | True |

**Important:** Notice `==` (two equals) for comparing, NOT `=` (which puts values in variables).

---

## Part 2: The `if` Statement — Your First Decision

An `if` statement checks a condition. If it's True, the indented code runs:

```python
age = 15

if age >= 13:
    print("You're a teenager!")

print("Thanks for visiting!")
```

**Output:**
```
You're a teenager!
Thanks for visiting!
```

---

## Part 3: CRITICAL — Indentation is REQUIRED! ⚠️

**In Python, indentation isn't just for looks — it's required syntax!**

The indentation (the spaces at the beginning of a line) tells Python which code belongs to the `if` statement.

**Correct ✅:**
```python
if age >= 13:
    print("You're a teenager!")    # INDENTED with 4 spaces
    print("Welcome!")              # INDENTED - part of the if
print("Goodbye!")                  # NOT indented - runs no matter what
```

**Wrong ❌:**
```python
if age >= 13:
print("You're a teenager!")        # ERROR! Python expects indentation here
```

**The Rules:**
1. **Indent after a colon (`:`)** — Any line ending with `:` starts a new block
2. **Use 4 spaces** — This is the standard (your Tab key usually does this)
3. **Un-indent to end the block** — Go back to the original level when done

Think of it like an outline:
```
1. Check if teenager:
    - If yes: print "You're a teenager!"
    - If yes: print "Welcome!"
2. Print "Goodbye!" (always)
```

---

## Part 4: `if`/`else` — Two Choices

Use `else` to handle "what if the condition is False?":

```python
age = 10

if age >= 13:
    print("You're a teenager!")
else:
    print("You're not a teenager yet.")

print("Have a great day!")
```

**Output:**
```
You're not a teenager yet.
Have a great day!
```

---

## Part 5: `if`/`elif`/`else` — Multiple Choices

Use `elif` (short for "else if") when you have more than two possibilities:

```python
age = int(input("How old are you? "))

if age >= 18:
    print("You're an adult!")
elif age >= 13:
    print("You're a teenager!")
else:
    print("You're a kid!")
```

**How it works:**
1. Python checks the first condition (`age >= 18`)
2. If False, it checks the next (`age >= 13`)
3. If all conditions are False, `else` runs

**Important:** Only ONE branch runs! Once Python finds a True condition, it skips the rest.

---

## Part 6: The Movie Ticket Bot 🎬

Let's build a practical example:

```python
print("🎬 Welcome to Awesome Cinema! 🎬")

age = int(input("How old are you? "))

if age >= 18:
    print("🎉 You're an adult! You can see any movie.")
    price = 12
elif age >= 13:
    print("🎉 You can see PG-13 movies!")
    price = 10
else:
    print("😊 You'll need a parent for PG-13 movies.")
    print("But we have great G-rated movies!")
    price = 7

print(f"Your ticket costs ${price}.")
```

---

## Part 7: Using Comparisons with Text

You can compare text too:

```python
answer = input("Do you like pizza? (yes/no) ")

if answer == "yes":
    print("Me too! 🍕")
else:
    print("That's okay, more for me!")
```

**Tip:** Text comparisons are case-sensitive! `"Yes"` is NOT the same as `"yes"`.
Use `.lower()` to handle this:

```python
answer = input("Do you like pizza? (yes/no) ").lower()

if answer == "yes":
    print("Me too! 🍕")
```

Now "YES", "Yes", and "yes" all work!

---

## Quick Indentation Reference

```python
if condition:
    # Everything indented here runs IF condition is True
    print("This runs if True")
    print("This too")
# Back to no indent = outside the if
print("This always runs")
```

---

## Common Pitfalls (and Fixes!)

- **Forgot the colon:** `if age >= 13` ❌ → `if age >= 13:` ✅
- **Wrong indentation:** Python will give `IndentationError` — check your spaces!
- **Used `=` instead of `==`:** `if age = 13:` ❌ → `if age == 13:` ✅
- **Case mismatch:** `"Yes" == "yes"` is False! Use `.lower()` to normalize

---

## 🏠 Homework Task: Ticket Pricing System

Upgrade the Movie Ticket Bot to include discounts:

**Requirements:**
- Kids (under 13): $7
- Teens (13-17): $10
- Adults (18-64): $12
- Seniors (65+): $9

**Bonus challenges:**
- Ask if it's Tuesday — if yes, everyone gets $2 off!
- Ask if they're a student — students get $1 off

**Example output:**
```
How old are you? 70
🎉 Senior ticket!
Your ticket costs $9.
```

---

## ✅ Ready for Lesson 7?

If you can write `if`/`elif`/`else` statements with proper indentation, you're ready!

**Next up: Lesson 7 — Complex Logic (and, or, nested ifs)**

