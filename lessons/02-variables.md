# Lesson 2: Variables — Memory Boxes 📦

## Goal

Learn how to store information so your program can remember it! Variables are like labeled boxes where you put data to use later.

## What You'll Learn

- What a variable is (a labeled box that remembers a value)
- How to create variables with `=` (assignment)
- How to change what's in a variable (reassignment)
- How to use variables in your code
- Good naming habits for variables

---

## Part 1: Meet Variables

Think of a variable as a **labeled box** that remembers something for you.

- **Left side** (before `=`) is the **label** (the name)
- **Right side** (after `=`) is the **value** you put into the box
- Only one thing fits at a time — a new value replaces the old value

```python
name = "Luna"
age = 11
favorite_color = "purple"
```

Say it out loud: `name = "Luna"` means **"put 'Luna' into the box called name"**

**Important:** The single `=` means "put into" (assignment). It does NOT mean "equals" like in math class. (We'll learn `==` for comparing things later!)

---

## Part 2: Using Variables

Once you store something in a variable, you can use it by its name:

```python
name = "Luna"
print(name)              # Shows: Luna
print("Hello!")
print(name)              # Shows: Luna (still remembers!)
```

You can use variables anywhere you'd use the actual value:

```python
pet = "cat"
print("I have a")
print(pet)
print("My pet is awesome!")
```

---

## Part 3: Changing What's in the Box (Reassignment)

You can change what's stored in a variable at any time. The new value replaces the old one:

```python
pet = "cat"
print(pet)      # Shows: cat

pet = "dog"     # Now pet remembers "dog" instead
print(pet)      # Shows: dog

pet = "hamster" # Changed again!
print(pet)      # Shows: hamster
```

Think of it like erasing what's written on a whiteboard and writing something new.

---

## Part 4: Numbers in Variables

Variables can hold numbers too:

```python
score = 100
lives = 3
level = 1

print(score)    # Shows: 100
print(lives)    # Shows: 3
```

You can do math with number variables:

```python
apples = 5
bananas = 3
total_fruit = apples + bananas
print(total_fruit)   # Shows: 8
```

---

## Part 5: Updating Variables with Math

A common pattern is updating a variable based on its current value:

```python
score = 0
print(score)    # Shows: 0

score = score + 10   # Take the old score (0), add 10, store the result back
print(score)    # Shows: 10

score = score + 5    # Take the old score (10), add 5, store it back
print(score)    # Shows: 15
```

**Shortcut:** Python has `+=` and `-=` to make this easier:

```python
coins = 10
coins += 5      # Same as: coins = coins + 5
print(coins)    # Shows: 15

coins -= 3      # Same as: coins = coins - 3
print(coins)    # Shows: 12
```

---

## Part 6: Naming Rules and Good Habits

**Rules (Python will complain if you break these):**
- Names can use letters, numbers, and underscores `_`
- Names **cannot** start with a number
- Names **cannot** have spaces

**Good habits (makes your code easier to read):**
- Use lowercase with underscores: `favorite_color`, `player_score`
- Use meaningful names that describe what's inside
- **The "say it" rule:** If you read the name out loud, could a friend guess what it means?

| Good Names ✅ | Not Great ❌ |
|--------------|-------------|
| `player_name` | `pn` |
| `total_score` | `x` |
| `lives_left` | `stuff` |
| `favorite_food` | `f1` |

---

## Common Pitfalls (and Fixes!)

- **Forgetting quotes for text:** `name = Luna` ❌ → `name = "Luna"` ✅
- **Using spaces in names:** `my name = "Luna"` ❌ → `my_name = "Luna"` ✅
- **Starting with a number:** `1st_place = "Gold"` ❌ → `first_place = "Gold"` ✅
- **Checking current value:** Add `print(variable_name)` to peek inside your "box"

---

## 🏠 Homework Task: All About Me

Create a program that stores information about yourself in variables, then prints it all out.

**What to do:**
1. Create variables for: your name, age, favorite color, favorite animal, favorite number
2. Print each one with a nice label

**Starter code:**

```python
# Store your info in variables
name = "Luna"
age = 11
favorite_color = "purple"
favorite_animal = "dolphin"
lucky_number = 7

# Print it all out
print("=== All About Me ===")
print("Name:")
print(name)
print("Age:")
print(age)
print("Favorite color:")
print(favorite_color)
print("Favorite animal:")
print(favorite_animal)
print("Lucky number:")
print(lucky_number)
```

**Bonus Challenge:**
- Create a `score` variable starting at 0
- Add 10 points, print the score
- Add 25 more points, print the score
- Lose 5 points, print the final score

---

## ✅ Ready for Lesson 3?

If you can create variables, change them, and use them in print statements, you're ready!

**Next up: Lesson 3 — Input and F-strings (Getting User Input)**

