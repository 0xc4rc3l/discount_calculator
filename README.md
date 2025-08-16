# 🛒 Discount Calculator (Python)

This simple Python program calculates the final price of an item after applying a discount.  
It demonstrates how to use functions, conditional statements, and user input.

---

## 📖 How It Works

1. The program defines a function `calculate_discount(price, discount_percent)`:
   - If the discount is **20% or higher**, the discount is applied to the price.
   - Otherwise, the function returns the original price.

2. The program then:
   - Prompts the user to enter the **original price** of an item.
   - Prompts the user to enter the **discount percentage**.
   - Uses the `calculate_discount` function to compute the final price.
   - Prints the result.

---

## 📝 Example Code

```python
def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        return price - discount_amount
    else:
        return price


# --- Main program ---
try:
    price = float(input("Enter the original price of the item: "))
    discount_percent = float(input("Enter the discount percentage: "))

    final_price = calculate_discount(price, discount_percent)

    print(f"\nFinal price: ${final_price:.2f}")
except ValueError:
    print("❌ Please enter valid numeric values for price and discount.")
