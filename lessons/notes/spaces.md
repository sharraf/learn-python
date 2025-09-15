### Making Your Code Easy to Read with Spaces

Think of spacing in your code like spacing in a normal sentence.

This is hard to read: `thecatjumpedoverthelazydog`
This is easy to read: `the cat jumped over the lazy dog`

While Python's interpreter doesn't always *need* spaces to understand everything, humans do! The main goal of spacing is **readability**. It helps our eyes separate different parts of a statement, just like spaces separate words.

The official Python style guide, called PEP 8, provides these recommendations so that all Python code can look and feel consistent. [peps.python.org](https://peps.python.org/pep-0008/)

### The Golden Rule: Let It Breathe

The most important rule is to **give your code room to breathe**. Don't cram everything together. A few well-placed spaces make a huge difference.

### When to Use Spaces

Always add a single space on either side of these operators.

#### 1. Around Assignment and Math Operators (`=`, `+`, `-`, `*`, `/`)

Use spaces around operators to make equations clear.

**Do this:**
```python
x = 5
total_pizzas = 10
pizzas_eaten = 3
pizzas_left = total_pizzas - pizzas_eaten  # Easy to see the math
```
**Not this:**
```python
x=5
pizzas_left=total_pizzas-pizzas_eaten # Harder to read
```

#### 2. Around Comparison Operators (`==`, `!=`, `<`, `>`, `<=`, `>=`)

This makes your `if` statements much cleaner.

**Do this:**
```python
if age >= 13:
    print("You can see the movie!")

while guess != secret_number:
    print("Wrong, try again!")
```
**Not this:**
```python
if age>=13:
    print("You can see the movie!")

while guess!=secret_number:
    print("Wrong, try again!")
```

#### 3. After Commas
Just like in English, always put a space after a comma. You will see this in lists and when you give multiple items to a function.

**Do this:**
```python
colors = ["red", "green", "blue"]
print("Hello", name, "welcome!")
```
**Not this:**
```python
colors = ["red","green","blue"]
print("Hello",name,"welcome!")
```

### When **NOT** to Use Spaces

There are a few important places where you should *avoid* adding spaces.

#### 1. Directly Inside Parentheses, Brackets, or Braces
Don't put spaces right after an opening `(` or right before a closing `)`.

**Do this:**
```python
# Good: The parentheses 'hug' the content
print(my_variable)
my_list[0]
```
**Not this:**
```python
# Bad: Unnecessary space inside the parentheses
print( my_variable )
my_list[ 0 ]
```

#### 2. Between a Function Name and its Opening Parenthesis
The name of a function and the parenthesis `()` used to call it should always be stuck together. This visually groups them as a single action: "running a function."

**Do this:**
```python
print("Hello, world!")
age = int(user_input)
```
**Not this:**
```python
# This can look confusing and is against Python style
print ("Hello, world!")
age = int (user_input)
```

The same rule applies to getting an item from a list. The list name and the brackets `[]` should be stuck together.

**Do this:** `colors[1]`
**Not this:** `colors [1]`

