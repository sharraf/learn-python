# Lesson 9: The Great Cosmic Cafe Project 🚀

## Goal

Today, instead of small problems, we're going to build one big, awesome program from start to finish! You are the manager of the busiest restaurant in the galaxy, "The Cosmic Cafe." Your job is to create a smart ordering system that can take customer orders, figure out special deals, and calculate the final price.

We will build this step-by-step. Complete each part before moving on to the next!

Note: To keep input simple, ALL choices are numbers (0/1/2/3...). We'll use `int()` and compare numbers—no string cleanup needed.

## 🎯 What You'll Practice

- Problem Decomposition: Breaking down a big project into smaller steps.
- Complex `if`/`elif`/`else` logic: Handling many different choices.
- Logical Operators (`and`, `or`) with parentheses: Combining conditions safely.
- Nested `if` statements: Asking follow-up questions based on previous answers.
- Updating variables: Keeping a running total of the cost.

---

### Part 1: Taking the Main Order (Easy)

First, let's get the customer's main course order using a numbered menu.

**Your Task:**

1. Welcome the customer to the Cosmic Cafe.
2. Display the main options with numbers:

   - 1: Meteor Burger
   - 2: Galaxy Pizza
   - 3: Black Hole Bagel
3. Ask: "Choose a main (1/2/3):" and read it with `int()`.
4. Use an `if`/`elif`/`else` to confirm the order or report an invalid number.

**Example Interaction:**
```
Welcome to the Cosmic Cafe! What can I get for you today?
1) Meteor Burger   2) Galaxy Pizza   3) Black Hole Bagel
> 2
One Galaxy Pizza coming right up!
```

```python
# Starter Snippet — numeric menu
print("1) Meteor Burger  2) Galaxy Pizza  3) Black Hole Bagel")
main_choice = int(input("Choose a main (1/2/3): "))
# TODO: use if/elif/else to confirm the order or say it's not on the menu
```

---

### Part 2: Adding Sides and Calculating Cost (Medium)

**Your Task:**

1. Build on your code from Part 1.
2. Create a variable `total_cost = 0`.
3. Assign prices to mains and add to `total_cost`:

   - Meteor Burger (1): 10 credits
   - Galaxy Pizza (2): 12 credits
   - Black Hole Bagel (3): 8 credits
4. Ask for a side (numeric) with a "no side" option:

   - 0: No side
   - 1: Asteroid Fries (+3)
   - 2: Saturn Rings (+4)
5. Add the side cost to `total_cost`.
6. Print the subtotal.

**Example Interaction:**
```
... (after choosing main)
Sides — 0) none  1) Asteroid Fries  2) Saturn Rings
> 1
Your subtotal is 13 credits.
```

```python
# Starter Snippet — prices and side menu
total_cost = 0
# TODO: add base price by main_choice (1→10, 2→12, 3→8)
print("Sides — 0) none  1) Asteroid Fries  2) Saturn Rings")
side_choice = int(input("> "))
# TODO: add side cost (1→+3, 2→+4)
# Hint: print your subtotal using an f-string
```

---

### Part 3: Combo Deals! (Hard)

Now let's add special deals using `and`, `or`, and parentheses.

**Your Task:**

1. Build on your code from Part 2.

2. Implement the classic "Burger + Fries" combo:
   - If `main_choice == 1` (Burger) AND `side_choice == 1` (Fries), subtract 2 credits.
3. Add a second combo that REQUIRES parentheses (mixing `and` + `or`):

   - If (main is Galaxy Pizza OR Black Hole Bagel) AND (you chose any side), subtract 1 credit.
   - In numbers: `if (main_choice == 2 or main_choice == 3) and (side_choice != 0):` minus 1.
4. Print a message when a combo is applied.

```python
# Starter Snippet — combos
# TODO: Burger + Fries → total_cost -= 2
# TODO: (Pizza OR Bagel) AND (any side) → total_cost -= 1
# Hint: when mixing and/or, use parentheses:
# (main_choice == 2 or main_choice == 3) and (side_choice != 0)
```

---

### Part 4: The Ultimate Challenge — Planetary Delivery

**Your Task:**

1. Build on your code from Part 3.
2. Ask for planet by number: `1=Mars`, `2=Venus`, `3=Jupiter`, `0=Other`.
3. Add delivery fees using `if`/`elif`/`else`:

   - Mars (+5)
   - Venus (+7)
   - Jupiter: ask another numeric question — Is today Tuesday? `1=yes`, `2=no`
       - If yes (1), delivery is free
       - If no (2), delivery is +10
   - Any other number: can't deliver
4. Print the final total.

```python
# Starter Snippet — planetary delivery
planet = int(input("Which planet? 1=Mars, 2=Venus, 3=Jupiter, 0=Other\n> "))
# TODO: if/elif/else delivery fees; if planet==3, ask is_tuesday (1/2) then nest if
# Hint: Mars → total_cost += 5; Venus → total_cost += 7; Jupiter (not Tuesday) → total_cost += 10
# Finally, print the total using an f-string
```

### Test Yourself (quick checklist)
Try these and check your totals:

1) Main 1 (Burger), Side 1 (Fries), Planet 1 (Mars) → expected total: 16
2) Main 2 (Pizza), Side 2 (Rings), Planet 2 (Venus) → expected total: 22
3) Main 3 (Bagel), Side 0 (none), Planet 0 (Other) → expected total: 8
4) Main 3 (Bagel), Side 1 (Fries), Planet 3 (Jupiter), Tuesday? 1=yes → expected total: 10
5) Main 2 (Pizza), Side 0 (none), Planet 3 (Jupiter), Tuesday? 2=no → expected total: 22

Tip: If your totals don’t match, print intermediate values (subtotal, after deals, after delivery).

### Bonus Challenges (Optional)

- Add a drink menu as numbers (0=none, 1=Comet Cola, 2=Moon Milk) with prices.
- Create a new combo using `or` and another condition that needs parentheses.
- Add a secret numeric coupon: Enter 42 at the beginning for 10% off the final total.
- Add a Medium-order bonus using a chained comparison: if `10 <= total_cost <= 15` (before delivery), subtract 1 credit.

Pro Tip: When mixing `and` and `or`, add parentheses to show your intent clearly, even when Python would figure it out.

