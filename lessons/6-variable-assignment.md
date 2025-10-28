# Lesson 6: Variables and Assignment — Remembering Things 🧠

## Goal

Build on Lesson 1’s `input()` by learning how to store answers in variables, change (update) them, and use numbers safely with type conversion. By the end, you’ll know how to keep track of information and do simple math with it.

## What you’ll learn

- What a variable is (a labeled box that remembers a value)
- Assignment with `=` and reassignment (changing a value)
- Numeric input: converting strings to numbers with `int()`/`float()`
- Using variables in messages with f-strings
- Updating values with `+=` and `-=` (counters)
- Simple math with inputs (add, subtract, multiply)

---

## Part 1: Meet Variables

Think of a variable as a labeled box that remembers something for you.

- Left side (before `=`) is the label (the name)
- Right side (after `=`) is the value you put into the box
- Only one thing fits at a time — a new value replaces the old value
- Say it out loud: `name = "Ava"` means “put "Ava" into `name`”
- Important: `=` means “put into”. `==` (two equals) means “is this the same?” (we’ll use that later)

```python
name = input("What is your name? ")
favorite_planet = input("Favorite planet? ")
print(f"Hi {name}! I love {favorite_planet} too!")
```

Try changing the value (reassignment):

```python
pet = "cat"
print(pet)
pet = "dog"  # now pet remembers "dog"
print(pet)
```

Try it yourself — upgrade a name with a fun title:

```python
name = input("Your name? ")
name = name + " the Brave"
print(f"Welcome, {name}!")
```

---

## Part 2: Numbers from input (important!)

`input()` always gives you text (a string). To do math, convert it to a number first.

Step-by-step:

1) Ask for the text
2) Convert the text to a number with `int()` (whole numbers) or `float()` (decimals)
3) Do math

```python
age_text = input("How old are you? ")
# age_text is a string like "11"
age = int(age_text)           # now it’s a number (int)!
print(age + 1)                # next birthday
```

Tip: If you expect decimals (like 3.5), use `float()` instead of `int()`.

Common pitfall (strings vs numbers):

```python
# print("Next year: " + age)         # ❌ TypeError (string + number)
print("Next year: " + str(age))       # ✅ convert number to text
print(f"Next year: {age}")            # ✅ f-strings are easiest and **preferred**
```

Try it — add two numbers from the user:

```python
x = int(input("First number: "))
y = int(input("Second number: "))
print(f"Sum = {x + y}")
```

---

## Part 3: The Space Sticker Shop ✨

We’ll keep track of coins, buy stickers, and update our coins.

Rules:

- Each star sticker costs 3 coins
- Each planet sticker costs 5 coins

Build it step-by-step:

1) Ask how many coins you have (convert to `int`)
2) Ask how many of each sticker you want (also `int`)
3) Compute the cost using math
4) Update `coins` by subtracting the cost (this is reassignment!)
5) Print the results with f-strings

```python
print("Welcome to the Space Sticker Shop!")
coins = int(input("How many coins do you have? "))
star_count = int(input("How many star stickers (3 coins each)? "))
planet_count = int(input("How many planet stickers (5 coins each)? "))

cost = star_count * 3 + planet_count * 5
print(f"Total cost: {cost} coins")

# Update remaining coins (reassignment)
coins = coins - cost
print(f"You have {coins} coins left.")
```

What did we learn?

- Variables can change over time (`coins` before vs after)
- You can compute one variable from others (`cost`)
- The same variable name can be reused to store the new value (this is normal!)

Optional guard (extra):

```python
if coins < 0:
    print("Uh-oh, not enough coins!")
    coins = 0
```

Bonus: Try earning 2 more coins and spending 1 coin using `+=` and `-=`:

```python
coins += 2
coins -= 1
print(f"After chores and a snack, coins = {coins}")
```

---

## Part 4: Naming and style

- Use meaningful names: `coins`, `price`, `total_cost` (clear beats short)
- Lowercase_with_underscores is the usual Python style
- A name can use letters, numbers, and `_` (but cannot start with a number)
- Good vs not-so-good:
  - Good: `stars_bought`, `planet_cost`, `total`
  - Not great: `s`, `pc`, `x1`
- Say-it rule: If you read the name out loud, could a friend guess what it means?

---

## Common pitfalls (and fixes)

- Forgetting `int()` on numeric input → you can’t do math on text (convert first!)
- Mixing strings and numbers without `str()` or f-strings → TypeError (use `str()` or f-strings)
- Overwriting a variable accidentally → print values often to check what it is now
- Using spaces or starting with a number in a name → use underscores and start with a letter

---

## 🏠 Homework Task: Allowance Tracker

Make a tiny “Allowance Tracker” that asks for a few numbers and shows the result.

What to do (step-by-step):

1) Ask (and convert to `int`) the following:
   - `weekly_allowance`
   - `chores_earned` (extra coins)
   - `spent` (snacks/toys)
2) Compute totals:
   - `total = weekly_allowance + chores_earned`
   - `left = total - spent`
3) Print a friendly summary with f-strings.

Starter snippet (fill in the TODOs):

```python
print("Allowance Tracker")
weekly_allowance = int(input("Weekly allowance: "))
chores_earned = int(input("Coins earned from chores: "))
spent = int(input("Coins spent: "))

# TODO: compute total
# TODO: compute left

print(f"You started with {weekly_allowance} and earned {chores_earned}.")
print(f"You spent {spent}.")
print(f"You have {left} coins left.")
```

Checklist:

- Handles zero just fine (try 0 for any answer)
- Uses clear variable names (no `x`, `y`)
- Uses `int()` for numbers and f-strings for messages

Try these:

- Input: allowance=10, earned=3, spent=4 → left=9
- Input: allowance=5, earned=0, spent=2 → left=3

Tip: If something looks wrong, `print()` your variables after each step to peek inside your “boxes.”
