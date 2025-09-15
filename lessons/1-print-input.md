# Lesson 1: The Mad Libs Story Generator

## Goal
Create a program that asks the user for different types of words (nouns, verbs, adjectives) and then uses those words to create a funny story.

## Python Concepts Introduced

### 🖨️ **`print()`** - Your Computer's Voice
Think of `print()` as your computer's way of talking to you! Just like you might shout something to get someone's attention, `print()` displays text on the screen so you can see it.

**Example:** `print("Hello!")` makes the computer say "Hello!" on the screen.

### 🎤 **`input()`** - Your Computer's Ears
`input()` is like giving your computer ears so it can listen to what you type. When your program uses `input()`, it stops and waits for you to type something and press Enter.

**Example:** `name = input("What's your name? ")` asks for your name and remembers it.

### 📦 **Variables** - Memory Boxes
Variables are like labeled boxes where you can store information. Just like you might have a box labeled "toys" to store your toys, variables have names and store data.

**Example:** `favorite_color = "blue"` creates a box called "favorite_color" and puts "blue" inside it.

### 🔗 **f-strings** - The Magic Glue
f-strings are a special way to combine text with the stuff stored in your variables. It's like having magic glue that can stick words together perfectly!

**Example:** `f"My name is {name}"` takes whatever is in the `name` variable and glues it into the sentence.

## Step-by-Step Instructions

### Step 1: Collect the Words 📝
Ask the user for different types of words and store each one in its own variable (memory box). Think of this like collecting ingredients before you cook!

### Step 2: Write Your Story Template 📖
Create a story with blanks where the user's words will go. It's like writing a story but leaving some words missing on purpose.

### Step 3: Fill in the Blanks ✨
Use f-strings to combine your story template with the words the user gave you. This is the magic moment where everything comes together!

## Example Code to Get Started

```python
# --- Get words from the user ---
print("Let's play Mad Libs!")
print("I need some words to create a funny story!")

adjective = input("Enter an adjective (describing word like 'silly' or 'huge'): ")
animal = input("Enter an animal: ")
verb = input("Enter a verb in past tense (action word ending in -ed): ")
place = input("Enter a place: ")
food = input("Enter a type of food: ")

# --- Tell the story ---
print("\n" + "="*50)
print("🎉 HERE IS YOUR HILARIOUS STORY! 🎉")
print("="*50)
print(f"The {adjective} {animal} {verb} all the way to {place}")
print(f"to eat a giant plate of {food}!")
print("="*50)
```

### 🤔 What's Happening Here?
- **Line 1-2**: We greet the user and explain what we're doing
- **Lines 4-8**: We ask for 5 different words and store each in a variable
- **Lines 11-16**: We create a fun story using those words with f-strings
- **The `\n`**: This creates a blank line to make the output look nicer
- **The `"="*50`**: This creates a line of 50 equal signs for decoration

## 🏠 Homework Task

Expand on this! Create your own, longer story. Your story should ask for at least 10 different words, including:
- A person's name
- A silly noise (like "BOING!" or "SPLAT!")
- A number
- At least 2 adjectives
- At least 2 animals
- At least 2 verbs

**Bonus Points:** Add some decorative elements like emojis or lines of symbols to make your story look extra cool when it prints out!
