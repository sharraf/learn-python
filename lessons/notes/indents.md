### What Are Code Indents in Python?

In Python, **indentation** refers to the spaces at the beginning of a line of code.

While many other programming languages use curly braces `{}` or keywords to show where blocks of code begin and end, Python uses indentation. This isn't just for style—it's a strict rule that the Python interpreter uses to understand the structure of your program.
### Why is Indentation Useful?

Think of it like an outline for a report or a list with sub-items. The indentation visually shows which lines of code belong together as a group.

Imagine you're giving instructions:

1.  Find your coat.
    *   *If it's raining:*
        *   Also grab an umbrella.
        *   Put on your rain boots.
2.  Open the door.

The indented items ("grab an umbrella," "put on rain boots") only happen under the "If it's raining" condition. You can see they belong to that instruction because they are nested underneath it.

Python works the exact same way. It uses indentation to know which code to run for an `if` statement or which code to repeat inside a `while` loop. This makes the code extremely easy to read, for both you and the computer.

```python
# The indent shows what code "belongs to" the if statement.
if weather == "raining":
    print("It's raining! Take an umbrella.") # INDENTED
    print("Wear your rain boots.")           # INDENTED
else:
    print("It's a sunny day!")               # INDENTED
    
print("Have a good day!") # NOT INDENTED - runs no matter what
```

### When and How Do You Use Indents?

Here are the simple rules for when and how to indent your code.

**1. You indent after a colon (`:`).**

Any line that ends with a colon is setting up a new block of code. The line or lines that follow it **must** be indented. You will see this with:
*   `if`, `elif`, and `else` statements
*   `while` and `for` loops
*   Function definitions with `def`

**2. Use four spaces.**

The official style guide for Python (called PEP 8) recommends using **four spaces** for each level of indentation.

You can use tabs, but you must be consistent. Mixing tabs and spaces in the same file will cause an `IndentationError`. The easiest way to avoid this is to set your code editor to insert four spaces whenever you press the `Tab` key.

**3. Un-indent to end a block.**

How do you tell Python that the code block is finished? You simply stop indenting. Go back to the same level of indentation as the line that started the block (like the `if` or `while` statement).

In the example below, `print("This will always run at the end.")` is "outside" the `if/else` block, so it will run no matter which condition was met.

```python
age = 15

if age < 18:
    # --- Start of the 'if' block ---
    print("You are a minor.")
    print("You can't vote yet.")
    # --- End of the 'if' block ---

# This line is not indented, so it is outside the 'if' block.
print("This will always run at the end.")
```

