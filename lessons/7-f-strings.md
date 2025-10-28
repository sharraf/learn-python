# Lesson 7: Say It Nicely with f-Strings ✨

## Goal

Learn the best way to build messages in Python: f-strings. You’ll put variables inside `{}` and let Python do the work. This is the preferred way. We will avoid using `+` to glue strings together.

## What you’ll learn

- What an f-string is and why it’s preferred
- How to put variables and math inside `{}`
- How to show numbers nicely (rounding)
- Common mistakes and how to fix them (like forgetting the `f`)

---

## Part 1: Why f-strings?

Imagine writing a message with blanks you can fill in.

Bad (don’t do this):

```python
name = "Ava"
age = 11
# ❌ Avoid using + to build strings
print("Hi, my name is " + name + " and I am " + str(age) + " years old.")
```

Good (do this instead):

```python
name = "Ava"
age = 11
print(f"Hi, my name is {name} and I am {age} years old.")
```

Why this is better:

- Shorter and easier to read
- No need to write `str()` for numbers
- Fewer bugs (you won’t forget spaces or pluses)

Tip: Say it out loud — “f-string” means “format string.” The `f` tells Python to fill in the `{}` parts.

---

## Part 2: Variables and math inside `{}`

You can put any variable or math expression inside the braces.

```python
x = 3
y = 5
print(f"x = {x}, y = {y}, x + y = {x + y}")
```

You can even call simple functions inside `{}`:

```python
name = "luna"
print(f"Hello {name.title()}!")  # .title() makes "Luna"
```

Common mistake: forgetting the `f`.

```python
name = "Zoe"
print("Hello {name}")   # ❌ prints: Hello {name}
print(f"Hello {name}")  # ✅ prints: Hello Zoe
```

---

## Part 3: Numbers that look nice

Sometimes you want fewer decimals. Use `round()` inside `{}`.

```python
price = 3.14159
print(f"Price: {round(price, 2)}")  # Price: 3.14
```

Or format a percent:

```python
score = 0.875
print(f"Score: {round(score * 100, 1)}%")  # Score: 87.5%
```

Extra (optional): fixed 2 decimal places with format specifiers

```python
price = 5
print(f"Price: {price:.2f}")  # Price: 5.00
```

---

## Part 4: Examples

Turn these “bad” prints into f-strings.

1)

```python
name = "Kai"
age = 9
# print("Hello, " + name + "! You are " + str(age) + " today!")
print(f"Hello, {name}! You are {age} today!")
```

2)

```python
apples = 4
bananas = 3
# print("Apples: " + str(apples) + ", Bananas: " + str(bananas))
print(f"Apples: {apples}, Bananas: {bananas}")
```

3)

```python
width = 7
height = 2
# print("Area = " + str(width * height))
print(f"Area = {width * height}")
```

---

## Common pitfalls (and fixes)

- Forgot the `f`? → Add `f` in front: `f"Hello {name}"`
- Curly braces in your text? → Double them: `print(f"Use {{ and }} like this.")`
- Using `+` to build strings? → Don’t. Use one f-string instead.
- Mixing quotes? → Stick to one style inside the string, or escape quotes.

---

## 🏠 Homework Task: Friendly Receipt

Make a tiny “receipt” using only f-strings (no `+`).

What to do:

1) Ask for item name, quantity (int), and price per item (float)
2) Compute `total = quantity * price`
3) Print a 3-line receipt using f-strings only:
   - `You bought: NAME (QTY)`
   - `Each costs: $PRICE` (show 2 decimals)
   - `Total: $TOTAL` (show 2 decimals)

Starter snippet (fill in the TODOs):

```python
item = input("Item name: ")
qty = int(input("Quantity: "))
price = float(input("Price each: $"))
# TODO: compute total
print(f"You bought: {item} ({qty})")
print(f"Each costs: ${price:.2f}")
print(f"Total: ${total:.2f}")
```

Checklist:

- Uses only f-strings (no `+` anywhere)
- Shows prices with 2 decimals using `:.2f`
- Works with whole numbers and decimals
