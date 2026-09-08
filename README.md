[README.md](https://github.com/user-attachments/files/31954336/README.md)
# Session 7 – Conditional Statements in Python

This notebook is a set of beginner exercises demonstrating `if` / `elif` / `else` logic in Python, using relatable, India-context examples (IPL tickets, social media followers, Zomato delivery, Flipkart cashback).

## Contents

### 1. IPL Ticket Eligibility
Checks whether a user is eligible to book IPL tickets based on age.

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("Eligible for IPL ticket booking")
else:
    print("Not eligible")
```
**Logic:** Age `>= 18` → eligible, otherwise not eligible.

---

### 2. Influencer Tier Classifier
Classifies a social media account into a tier based on follower count. This logic is run three times in the notebook with different sample inputs.

```python
followers = int(input("Enter number of followers: "))

if followers < 10000:
    print("Micro Influencer")
elif followers <= 100000:
    print("Rising Star")
else:
    print("Celebrity")
```

| Followers | Tier |
|---|---|
| < 10,000 | Micro Influencer |
| 10,000 – 100,000 | Rising Star |
| > 100,000 | Celebrity |

---

### 3. Zomato Free Delivery Check
Determines delivery charge status based on order total. Run twice with different totals in the notebook.

```python
total = float(input("Enter your Zomato order total: "))

if total > 299:
    print("Apply Free Delivery")
elif total >= 200:
    print("Add more items for free delivery")
else:
    print("Delivery charges apply")
```

| Order Total | Result |
|---|---|
| > ₹299 | Apply Free Delivery |
| ₹200 – ₹299 | Add more items for free delivery |
| < ₹200 | Delivery charges apply |

---

### 4. Flipkart Cashback Eligibility (Nested Conditionals)
Uses a **nested `if`** to determine cashback percentage based on cart value and payment method.

```python
cart_value = float(input("Enter Flipkart cart value: "))
payment = input("Enter payment method (UPI/Card/Cash): ")

if cart_value > 1000:
    if payment == "UPI":
        print("Eligible for 10% cashback")
    else:
        print("Eligible for 5% cashback")
else:
    print("No cashback")
```

| Cart Value | Payment | Result |
|---|---|---|
| > ₹1000 | UPI | 10% cashback |
| > ₹1000 | Card / Cash | 5% cashback |
| ≤ ₹1000 | Any | No cashback |

---

## Concepts Covered
- Basic `if` / `else` statements
- `if` / `elif` / `else` chains for multi-way branching
- Comparison operators (`<`, `<=`, `>`, `>=`, `==`)
- Type casting user input with `int()` and `float()`
- Nested conditional statements

## Requirements
- Python 3.x
- Jupyter Notebook (or any Python interpreter, since all cells use `input()`)

## How to Run
1. Open the notebook in Jupyter.
2. Run each cell in order.
3. Enter the requested value when prompted (age, followers, order total, cart value/payment method).
