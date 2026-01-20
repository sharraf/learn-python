# Lesson 7: Complex Logic — Power-Ups for If Statements ⚡️

## Goal

Level up your decision-making! Learn to combine conditions with `and`/`or`/`not`, nest decisions inside each other, and build more sophisticated programs.

## What You'll Learn

- Combining conditions with `and`, `or`, and `not`
- Nesting `if` statements (decisions inside decisions)
- Chained comparisons (Python's superpower!)
- Why order matters in `if`/`elif` chains
- Building a complete project with complex logic

---

## Part 1: `and`, `or`, `not` — Combining Ideas

### `and` — BOTH Must Be True

```python
age = 15
has_ticket = True

if age >= 13 and has_ticket:
    print("You can enter the movie!")
```

**Real life:** "If it's Saturday AND I finished homework, I can play."

### `or` — EITHER Can Be True

```python
day = "saturday"

if day == "saturday" or day == "sunday":
    print("It's the weekend!")
```

**Real life:** "If it's raining OR snowing, bring a coat."

### `not` — Flips True ↔ False

```python
is_raining = False

if not is_raining:
    print("Go play outside!")
```

**Real life:** "If it's NOT bedtime, I can read."

---

## Part 2: Using Parentheses for Clarity

When mixing `and` and `or`, use parentheses to show your intent clearly:

```python
# Without parentheses - confusing!
# if age >= 13 or age >= 10 and has_parent:

# With parentheses - clear!
if (age >= 13) or (age >= 10 and has_parent):
    print("Allowed!")
```

**Rule of thumb:** When in doubt, add parentheses!

---

## Part 3: Nested `if` — Follow-Up Questions

You can put an `if` inside another `if` to ask follow-up questions:

```python
age = 12

if age < 13:
    with_parent = input("Are you with a parent? (yes/no) ").lower()
    
    if with_parent == "yes":
        print("Okay, you can watch with your parent!")
    else:
        print("Sorry, you need a parent for this movie.")
else:
    print("Welcome! Enjoy the movie!")
```

Notice the double indentation — the inner `if` is inside the outer `if`.

---

## Part 4: Chained Comparisons (Python Superpower!)

Instead of writing:
```python
if age >= 13 and age <= 17:
    print("Teen ticket!")
```

You can write:
```python
if 13 <= age <= 17:
    print("Teen ticket!")
```

This reads just like math: "13 is less than or equal to age, which is less than or equal to 17"

---

## Part 5: Order Matters in `if`/`elif`

Python checks conditions from top to bottom. The FIRST True condition wins:

```python
score = 95

if score >= 60:
    grade = "D"       # This runs! (95 >= 60 is True)
elif score >= 70:
    grade = "C"       # Skipped
elif score >= 80:
    grade = "B"       # Skipped
elif score >= 90:
    grade = "A"       # Skipped
```

**Oops!** We should check the highest first:

```python
score = 95

if score >= 90:
    grade = "A"       # This runs! ✅
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"
```

---

## Part 6: Movie Ticket Bot 2.0 🎬

Let's build a complete example with all these concepts:

```python
print("🎬 Welcome to Movie Ticket Bot 2.0!")

age = int(input("How old are you? "))
is_student = input("Are you a student? (yes/no) ").lower()
with_parent = input("Are you with a parent? (yes/no) ").lower()
day = input("What day is it? ").lower()

# Access rules - combining conditions with or
can_see_pg13 = (age >= 13) or (with_parent == "yes")

# Base price by age - order matters!
if age >= 65:
    base_price = 9     # Senior
elif age >= 18:
    base_price = 12    # Adult
elif 13 <= age <= 17:
    base_price = 10    # Teen
else:
    base_price = 7     # Kid

# Apply discounts (these stack!)
price = base_price
if is_student == "yes":
    price -= 1         # Student discount
if day == "tuesday":
    price -= 2         # Tuesday discount

# Keep price from going negative
if price < 0:
    price = 0

# Final message
if can_see_pg13:
    print(f"✅ You can see PG-13 movies!")
else:
    print("❌ You need a parent for PG-13 movies.")
print(f"Your ticket price: ${price}")
```

---

## Part 7: Quick Examples

### `and` vs `or`
```python
is_weekend = True
finished_homework = False

print(is_weekend and finished_homework)  # False (both must be True)
print(is_weekend or finished_homework)   # True (at least one is True)
```

### Multiple conditions
```python
# Must be a teen AND have a ticket AND not be banned
if (13 <= age <= 17) and has_ticket and (not is_banned):
    print("Welcome, teen!")
```

---

## Common Pitfalls (and Fixes!)

- **Mixing up `and`/`or`:** Read it out loud! "Must be 13 AND have ticket" vs "13 OR have ticket"
- **Forgetting parentheses:** Add them to make your intent clear
- **Using separate `if`s when you meant one choice:** Use `if`/`elif`/`else`
- **Text comparisons:** Always use `.lower()` to handle "Yes", "YES", "yes"

---

## 🏠 Homework Task: Movie Permissions Checker

Build a program that determines which movie ratings a person can watch.

**Rules:**
- Everyone can watch G and PG
- PG-13: age ≥ 13 OR with a parent
- R: age ≥ 17 OR (age ≥ 15 AND with a parent)

**Your program should:**
1. Ask for age (number)
2. Ask if they're with a parent (yes/no)
3. Print which ratings they can watch

**Example outputs:**
```
Age: 12, Parent: no  → You can watch: G, PG
Age: 13, Parent: no  → You can watch: G, PG, PG-13
Age: 15, Parent: yes → You can watch: G, PG, PG-13, R
Age: 17, Parent: no  → You can watch: G, PG, PG-13, R
```

**Hint:** Compute booleans first:
```python
can_pg13 = (age >= 13) or (with_parent == "yes")
can_r = (age >= 17) or ((age >= 15) and (with_parent == "yes"))
```

---

## ✅ Ready for Lesson 8?

If you can combine conditions with `and`/`or` and nest `if` statements, you're ready!

**Next up: Lesson 8 — While Loops (Repeating Code)**

