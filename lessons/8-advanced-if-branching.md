# Lesson 8: If Power-Ups ⚡️ (and, or, not, nested decisions)

## Goal

Expand your Lesson 2 "Movie Ticket Bot" by learning the power-ups for `if` statements: combining conditions with `and`/`or`/`not`, nesting decisions, ordering your checks, and writing clear multi-branch logic.

## Python Concepts Introduced

### 🔗 `and`, `or`, `not` — Combining Ideas

- `and` means BOTH are true
- `or` means EITHER is true
- `not` flips True ↔ False (the opposite)

Real-life:

- `and`: "If it's Saturday AND I finished homework, I can play."
- `or`: "If it's raining OR snowing, bring a coat."
- `not`: "If it's NOT bedtime, I can read a book."

Tip: Use parentheses to make your meaning clear: `(age >= 13) and (has_ticket == "yes")`

### 🧩 Nested `if` — Follow-up Questions

You can put an `if` inside another `if` to ask a second question only when needed.

### 🧭 Order Matters in `if`/`elif` Chains

Python checks from top to bottom. The the first matching branch runs, and the rest are skipped. Put the most specific checks first when needed.

### 🔢 Chained Comparisons (Python superpower!)

You can write ranges cleanly: `13 <= age <= 17` instead of `(age >= 13) and (age <= 17)`

---

## Step-by-Step: Movie Ticket Bot 2.0 🎬

We’ll upgrade the Lesson 2 program to handle more realistic rules.

Rules we’ll support:

- Adults (18+) can see any movie
- Teens (13–17) can see PG-13
- Kids (<13) need a parent for PG-13
- Seniors (65+) get a discount
- Students get a discount
- Tuesday is Discount Day for everyone

We’ll also practice input clean-up with `.lower()` to make comparisons easier.

### Step 1: Gather Inputs

- Ask for age (convert with `int()`)
- Ask if they are a student (`yes`/`no`)
- Ask if they are with a parent (`yes`/`no`)
- Ask what day of the week it is

### Step 2: Decide Movie Access (nested + and/or)

- First decide if they’re allowed to see a PG-13 movie
- Then figure out price and discounts

### Example Code (starter)

```python
print("🎬 Welcome to Movie Ticket Bot 2.0!")
age = int(input("How old are you? "))
is_student = input("Are you a student? (yes/no) ").lower()
with_parent = input("Are you with a parent? (yes/no) ").lower()
day = input("What day is it? ").lower()

# Access rules
can_see_pg13 = (age >= 13) or (with_parent == "yes")

# Base price by age
if age >= 18:
    base_price = 12
elif 13 <= age <= 17:
    base_price = 10
else:
    base_price = 7

# Apply discounts
price = base_price
if age >= 65:
    price -= 2  # senior discount
if is_student == "yes":
    price -= 1  # student discount
if day == "tuesday":
    price -= 2  # discount day

# Keep price at least 0
if price < 0:
    price = 0

# Final messages
if can_see_pg13:
    print(f"You can see PG-13 movies. Your price is ${price}.")
else:
    print("You need a parent for PG-13 today. Try G-rated movies!")
```

### 🤔 What’s Happening Here?

- We normalize text with `.lower()` so `"Yes"`, `"YES"`, and `"yes"` all match
- We combine conditions with `or` for permission: 13+ OR with a parent
- We use an `if/elif/else` chain to pick exactly one base price bucket
- We use multiple independent `if` statements to stack discounts (they can add up!)
- We use a small guard `if price < 0` to keep the price sensible

---

## Mini Power-Ups with Tiny Examples

### 1) `and` vs `or`

```python
is_weekend = True
finished_homework = False
print(is_weekend and finished_homework)  # False
print(is_weekend or finished_homework)   # True
```

### 2) `not` (flip it!)

```python
is_raining = False
if not is_raining:
    print("Go play outside!")
```

### 3) Nested follow-up

```python
age = 12
if age < 13:
    with_parent = input("With a parent? (yes/no) ").lower()
    if with_parent == "yes":
        print("Allowed with parent.")
```

### 4) Chained comparisons

```python
age = 15
if 13 <= age <= 17:
    print("Teen ticket applies.")
```

### 5) Order matters

```python
score = 95
if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"  # This won’t run if score was already >= 90
```

---

## Common Pitfalls (and fixes!)

- Mixing up `and`/`or`: Read out loud! “Must be 13 AND have ticket” vs “13 OR have ticket?”
- Forgetting parentheses on complex logic: Add them to show your intent clearly.
- Using two separate `if` blocks when you meant “exactly one choice”: use `if/elif/else`.
- Comparing text without normalizing: use `.lower()` on both sides.

---

## 🏠 Homework Task

Build “Movie Night: Permissions Only.” Your goal is to ask a few questions, then clearly tell the user which movie ratings they’re allowed to watch.

### What to implement

- Ask for age (number).
- Ask if they are with a parent (yes/no). Normalize text (use `.lower()`).
- Decide permissions using these rules:
  - Everyone may watch G and PG.
  - PG-13: age ≥ 13 OR with a parent.
  - R: age ≥ 17 OR (age ≥ 15 AND with a parent).
- Print a friendly summary listing the allowed ratings (e.g., “You can watch: G, PG, PG-13”).

### Why this matters

- You’ll practice mixing `and` vs `or` and using parentheses to show your intent.
- You’ll practice writing `if`/`elif`/`else` so your messages are clear.

### Hints

- Compute helpful booleans first:
  - `can_pg13 = (age >= 13) or (with_parent == "yes")`
  - `can_r = (age >= 17) or ((age >= 15) and (with_parent == "yes"))`

### Example scenarios

- age=12, with_parent=no → You can watch: G, PG
- age=13, with_parent=no → You can watch: G, PG, PG-13
- age=15, with_parent=yes → You can watch: G, PG, PG-13, R
- age=16, with_parent=no → You can watch: G, PG, PG-13
- age=17, with_parent=no → You can watch: G, PG, PG-13, R

When you’re done, you’ll be ready for the big project in Lesson 9: The Great Cosmic Cafe! 🍔🪐

