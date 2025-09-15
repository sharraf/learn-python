# Lesson 3: The Secret Password 🔐

## Goal
Create a program that has a secret password. The program should keep asking the user to guess the password until they get it correct.

## Python Concepts Introduced

### 🔄 **`while` Loop** - The Persistent Repeater
A `while` loop is like having a very persistent friend who keeps asking "Are we there yet?" until the answer changes. It repeats a block of code over and over as long as a condition stays true.

**Think of it like this:** Imagine you're trying to open a combination lock. You keep trying different combinations WHILE the lock is still locked. Once it opens, you stop trying.

**Real life example:** "WHILE I'm still hungry, keep eating. When I'm full, stop eating."

### ❌ **`!=` (Not Equal To)** - The "That's Not Right!" Checker
The `!=` operator checks if two things are NOT the same. It's like having a bouncer at a club who says "That's not the right password!"

**Examples:**
- `"cat" != "dog"` is True (they're different)
- `"hello" != "hello"` is False (they're the same)
- `5 != 3` is True (different numbers)

### 🛑 **`break`** - The Emergency Exit
The `break` statement is like having an emergency exit door in your loop! It lets you escape from a `while` loop immediately, even if the loop condition is still true.

**Think of it like this:** Imagine you're in a game where you keep rolling dice WHILE you haven't rolled a 6. But suddenly you decide "I'm tired of this game!" - `break` lets you quit the game right away, even if you haven't rolled a 6 yet.

**Real life example:** "WHILE I'm still shopping, keep looking at items. But IF I see something I really want, BREAK out of browsing and buy it immediately!"

**How it works:**
- `break` only works inside loops
- When Python sees `break`, it immediately jumps out of the loop
- The program continues with whatever comes after the loop

**Example:**
```python
while True:  # This would normally run forever!
    answer = input("Do you want to continue? (yes/no): ")
    if answer == "no":
        break  # Exit the loop immediately!
    print("Continuing...")
print("You chose to stop!")
```

## Step-by-Step Instructions

### Step 1: Set Up the Secret 🤫
Create a variable to hold your secret password. Pick something fun but not too hard to guess for testing!

### Step 2: Get the First Guess 🎯
Ask the user for their first password attempt and store it in a variable.

### Step 3: Create the Loop 🔄
Use a `while` loop that keeps going as long as their guess is wrong (not equal to the secret).

### Step 4: Handle Wrong Guesses 😅
Inside the loop, tell them they're wrong and ask for another guess.

### Step 5: Celebrate Success! 🎉
After the loop ends (meaning they got it right), congratulate them!

## Example Code to Get Started

### Method 1: Using the condition in the `while` statement
```python
# Step 1: Set up our secret password
secret_password = "shark"

print("🔐 Welcome to the Secret Club! 🔐")
print("You need the secret password to enter...")

# Step 2: Get their first guess
guess = input("What is the secret password? ")

# Step 3 & 4: Keep asking while they're wrong
while guess != secret_password:
    print("❌ Nope, that's not it. Try again!")
    guess = input("What is the secret password? ")

# Step 5: They got it right!
print("\n🎉 You got it! The secret door opens. 🎉")
print("Welcome to the club, member!")
```

### Method 2: Using `break` for a cleaner approach
```python
# Step 1: Set up our secret password
secret_password = "shark"

print("🔐 Welcome to the Secret Club! 🔐")
print("You need the secret password to enter...")

# Step 2 & 3: Use an infinite loop with break
while True:  # This means "loop forever"
    guess = input("What is the secret password? ")

    if guess == secret_password:
        break  # Exit the loop immediately!

    print("❌ Nope, that's not it. Try again!")

# Step 4: They got it right!
print("\n🎉 You got it! The secret door opens. 🎉")
print("Welcome to the club, member!")
```

### 🤔 What's Happening Here?

**Method 1 - Traditional Loop Logic:**

1. We ask for a guess
2. We check: "Is the guess NOT EQUAL to the secret password?"
3. If YES (it's wrong), we go into the loop:
   - Print "wrong" message
   - Ask for a new guess
   - Go back to step 2
4. If NO (it's correct), we skip the loop and print success!

**Why do we ask for the guess TWICE in Method 1?**
- Once BEFORE the loop (to get started)
- Once INSIDE the loop (to get a new guess after they're wrong)

Think of it like knocking on a door. You knock once to see if it opens. If it doesn't, you keep knocking until it does!

**Method 2 - Using `break` (Often Cleaner!):**

1. We start an infinite loop (`while True`)
2. We ask for a guess inside the loop
3. We check: "Is the guess EQUAL to the secret password?"
4. If YES (it's correct), we `break` out of the loop immediately
5. If NO (it's wrong), we print "wrong" message and the loop continues

**Why is Method 2 sometimes better?**
- We only ask for the guess in ONE place (inside the loop)
- No need to repeat the `input()` line
- The logic flows more naturally: ask → check → break if correct → otherwise continue

## 🏠 Homework Task

**Basic Tasks:**
- Make your password program case-insensitive! This means it should accept `"shark"`, `"Shark"`, `"SHARK"`, or even `"sHaRk"` - any combination of upper and lower case letters. **Hint:** You can use the `.lower()` method to convert text to all lowercase before comparing: `guess.lower()`
- Add a counter that tracks and prints how many attempts they made.

**Break Challenge:**
- Rewrite your password program using the `break` method (Method 2 from above)
- Add a "quit" option: if the user types "quit" instead of a password guess, use `break` to exit the loop and print "Thanks for playing!"

**Super Challenge:**
- Create a program that asks the user to keep entering numbers until they enter a number greater than 100. Use `break` to exit when they succeed, and show them how many numbers they entered.
