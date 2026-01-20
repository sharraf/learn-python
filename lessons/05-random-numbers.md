# Lesson 5: Random Numbers — The Digital Dice 🎲

## Goal

Add unpredictability to your programs! Learn how to generate random numbers using Python's built-in `random` library — perfect for games, simulations, and surprises.

## What You'll Learn

- How to import extra tools (libraries) into Python
- How to generate random numbers with `random.randint()`
- How to use random numbers to make games more exciting
- Combining randomness with everything you've learned so far

---

## Part 1: Importing Superpowers with `import`

Think of `import` as borrowing superpowers from other programmers! Python comes with lots of pre-built tools (called "libraries" or "modules") that other smart people have already created.

**Think of it like this:** Imagine you want to bake a cake. Instead of making flour from wheat yourself, you go to the store and buy flour that someone else already made. `import` is like going to Python's "store" and getting tools that are already built!

```python
import random
```

This gives you access to all the random number tools.

---

## Part 2: `random.randint()` — The Number Picker

`random.randint(start, end)` picks a random whole number between `start` and `end` (including both endpoints). It's like having a magic hat that picks any number in a specific range.

```python
import random

lucky_number = random.randint(1, 100)
print(f"Your lucky number is: {lucky_number}")
```

Every time you run this, you'll get a different number!

**More examples:**
```python
import random

# Random number from 1 to 10
small_number = random.randint(1, 10)
print(f"Small number: {small_number}")

# Random number from 1 to 6 (like a dice!)
dice_roll = random.randint(1, 6)
print(f"You rolled: {dice_roll}")

# Random age
random_age = random.randint(1, 120)
print(f"Random age: {random_age} years old")
```

---

## Part 3: Simulating Dice Rolls

Let's roll two dice and add them up:

```python
import random

print("🎲 Rolling two dice...")

die1 = random.randint(1, 6)
die2 = random.randint(1, 6)
total = die1 + die2

print(f"Die 1: {die1}")
print(f"Die 2: {die2}")
print(f"Total: {total}")

# Special messages for lucky rolls!
if total == 12:
    print("🎉 BOXCARS! Double sixes!")
if total == 7:
    print("Lucky seven!")
if total == 2:
    print("Snake eyes!")
```

---

## Part 4: Random Game Scores

Here's a simple "who wins" game with random scores:

```python
import random

print("🎮 Random Score Battle!")
print()

player_score = random.randint(0, 1000)
computer_score = random.randint(0, 1000)

print(f"Your score: {player_score}")
print(f"Computer score: {computer_score}")
print()

if player_score > computer_score:
    print("🎉 You win!")
elif player_score < computer_score:
    print("🤖 Computer wins!")
else:
    print("🤝 It's a tie!")
```

---

## Part 5: The Secret Number Guessing Game

Now let's make a simple guessing game. (We'll make it loop in a later lesson!)

```python
import random

print("🔮 Guess My Number!")
print("I'm thinking of a number between 1 and 10...")
print()

secret = random.randint(1, 10)
guess = int(input("What's your guess? "))

if guess == secret:
    print("🎉 WOW! You got it!")
elif guess < secret:
    print(f"Too low! The number was {secret}.")
else:
    print(f"Too high! The number was {secret}.")
```

---

## Part 6: Why Randomness is Fun

Every time you run a program with `random.randint()`, you get different results! This makes your programs:

- **Unpredictable** — even you don't know what will happen
- **Replayable** — games are different each time
- **Exciting** — adds an element of chance

This is how real games create variety!

---

## Quick Reference

```python
import random                          # Required at the top of your file

random.randint(1, 6)                   # Random number from 1 to 6 (inclusive)
random.randint(0, 100)                 # Random number from 0 to 100
random.randint(start, end)             # Random number from start to end
```

---

## Common Pitfalls (and Fixes!)

- **Forgot to import:** You must write `import random` at the top of your file
- **Misspelled:** It's `random.randint` (not `randInt` or `randomint`)
- **Same number every time?** Make sure you're running the whole program fresh each time

---

## 🏠 Homework Task: Fortune Teller

Create a "Magic 8-Ball" style fortune teller that gives random advice!

**What to do:**
1. Ask the user to type a yes/no question
2. Generate a random number from 1 to 8
3. Use `if`/`elif`/`else` to give different answers based on the number

**Example answers:**
- 1-2: "Yes, definitely!"
- 3-4: "Ask again later..."
- 5-6: "My sources say no."
- 7-8: "Cannot predict now."

**Starter code:**
```python
import random

print("🔮 Magic 8-Ball 🔮")
question = input("Ask me a yes/no question: ")

answer = random.randint(1, 8)

# TODO: Use if/elif/else to print different messages based on 'answer'
# Hint: if answer <= 2: print("Yes!")
```

**Bonus:** Add more possible answers (use a larger range like 1-12)!

---

## ✅ Ready for Lesson 6?

If you can import the random library and generate random numbers, you're ready!

**Next up: Lesson 6 — If/Else Logic (Making Decisions)**

