# Lesson 2: Movie Ticket Bot 🎬

## Goal
Create a program that asks for the user's age and tells them if they are old enough to see a PG-13 movie by themselves (assuming an age of 13).

## Python Concepts Introduced

### 🔢 **`int()`** - The Number Converter
When you use `input()`, everything you type comes back as text (even numbers!). But sometimes we need to do math with numbers. `int()` is like a magical translator that converts text-numbers into real numbers that Python can count with.

**Think of it like this:** If someone writes "5" on a piece of paper, you see the symbol "5". But `int()` helps the computer understand that this symbol means the actual number 5 that you can add, subtract, or compare.

**Example:** `int("12")` turns the text "12" into the number 12.

### ⚖️ **Comparison Operators** - The Decision Makers
These are special symbols that help your program compare things and make decisions:
- **`>`** (greater than): Is the left side bigger? Like asking "Is 15 > 10?" (Yes!)
- **`<`** (less than): Is the left side smaller? Like asking "Is 5 < 10?" (Yes!)
- **`>=`** (greater than or equal): Is the left side bigger OR the same? Like asking "Is 13 >= 13?" (Yes!)
- **`<=`** (less than or equal): Is the left side smaller OR the same?

### 🤔 **`if`/`elif`/`else` Statements** - The Choice Maker
`if`/`elif`/`else` statements are like having a robot that can make decisions! It's like saying "IF this is true, do this thing. ELSE IF that other thing is true, do something different. OTHERWISE (else), do a third thing."

**Real life example:** "IF it's raining, bring an umbrella. ELIF it's sunny, wear sunglasses. ELSE, just wear a jacket."

- **`if`**: The first condition to check
- **`elif`**: Short for "else if" - additional conditions to check if the first one was false
- **`else`**: What to do if none of the conditions above were true

## Step-by-Step Instructions

### Step 1: Get the Age as Text 📝
Use `input()` to ask for their age. Remember, this comes back as text!

### Step 2: Convert Text to Number 🔄
Use `int()` to turn that text into a real number that Python can compare.

### Step 3: Make the Decision 🤖
Write an `if` statement to check if they're old enough, and an `else` for when they're not.

## Example Code to Get Started

```python
# Step 1: Ask for the user's age as text
print("🎬 Welcome to Awesome Cinema! 🎬")
age_string = input("How old are you? ")

# Step 2: Convert the text to a real number
age_number = int(age_string)

# Step 3: Check their age and give appropriate response
if age_number >= 18:
    print("🎉 You're an adult! You can see any movie. Enjoy!")
elif age_number >= 13:
    print("🎉 You can see PG-13 movies. Have fun!")
else:
    print("😊 You'll need a parent for PG-13 movies.")
    print("But we have some great G-rated movies playing too!")
```

### 🤔 What's Happening Here?

**Line by line breakdown:**

1. **Line 2**: We welcome the user with a fun movie theater greeting
2. **Line 3**: We ask for their age and store the TEXT version in `age_string`
3. **Line 6**: We convert that text to a NUMBER and store it in `age_number`
4. **Line 9**: We check: "Is age_number greater than or equal to 18?" (First condition)
5. **Line 10**: If YES (True), we print the adult message
6. **Line 11**: If NO (False), we check the SECOND condition: "Is age_number greater than or equal to 13?"
7. **Line 12**: If this second condition is YES (True), we print the teen message
8. **Line 13-15**: If BOTH conditions were NO (False), we print the child message

**The Decision Tree:** Python checks conditions in order:
- First: Are they 18+? → Adult message
- If not, then: Are they 13+? → Teen message
- If neither: → Child message

**Why do we need two variables?** Think of it like this: `input()` always gives you a "word version" of what someone types. Even if they type "15", you get the word "fifteen" written down. But to compare ages, you need the actual number 15. That's what `int()` does - it reads the word and gives you the number!

## 🏠 Homework Task

Upgrade your program! Use an `if`/`elif`/`else` chain to create a ticket pricing system:

- **Kids** (under 13): $7
- **Teens** (13-17): $10
- **Adults** (18+): $12

Your program should tell them their ticket price based on their age.
