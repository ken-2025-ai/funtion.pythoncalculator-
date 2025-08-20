# 🛒 Discount Calculator Program

## 🎯 Objective
This program demonstrates the use of **functions** in Python to calculate a discounted price.  
It ensures that discounts are only applied if they meet a specified threshold (20% or higher).  

---

## 📘 Function: `calculate_discount(price, discount_percent)`

- **Parameters:**
  - `price` → The original price of the item (float).
  - `discount_percent` → The discount percentage (float).  

- **Logic:**
  - If the discount is **20% or higher**, the function applies the discount and returns the reduced price.  
  - If the discount is **less than 20%**, the function returns the original price (no discount applied).  

---

## 📂 Program Flow
1. User is prompted to enter the **original price**.  
2. User is prompted to enter the **discount percentage**.  
3. The program calls the `calculate_discount()` function to determine the final price.  
4. The result is displayed:
   - If discount ≥ 20 → Show final discounted price.  
   - If discount < 20 → Show original price (no discount).  

---

## 📝 Example Code
```python
def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

price = float(input("Enter the original price: "))
discount_percent = float(input("Enter the discount percentage: "))

final_price = calculate_discount(price, discount_percent)

if discount_percent >= 20:
    print(f"✅ Final price after {discount_percent}% discount: {final_price:.2f}")
else:
    print(f"⚠️ No discount applied. Price remains: {final_price:.2f}")
