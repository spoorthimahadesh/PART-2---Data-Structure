# PART-2---Data-Structure
# 🍽️ Restaurant Order Management System

A Python-based Jupyter Notebook project that simulates a complete **restaurant ordering system** — from menu display to cart management, inventory tracking, and sales analytics — using core Python data structures with no external libraries.

---

## 📁 Project Structure

```
📦 part2-order-system
 ┗ 📓 part2_order_system.ipynb
```

---

## 📌 Features

### ✅ Task 1 — Menu Management

- Stores a **10-item menu** across 3 categories (Starters, Mains, Desserts) with price and availability status
- Displays menu **grouped by category** in a formatted table with `Available` / `Unavailable` labels
- Calculates and prints:
  - Total number of menu items
  - Count of currently available items
  - Most expensive item
  - All items priced under ₹150

### ✅ Task 2 — Cart System

A full cart management system with 3 functions:

| Function | Description |
|----------|-------------|
| `add_to_cart(item, qty)` | Adds item to cart; updates quantity if already present; rejects unavailable or invalid items |
| `remove_from_cart(item)` | Removes an item from cart; handles case where item isn't in cart |
| `update_quantity(item, qty)` | Updates the quantity of an existing cart item |

**Order Summary** includes:
- Itemised list with quantity and line total
- Subtotal
- GST at 5%
- Final total amount

### ✅ Task 3 — Inventory Management

- Uses `copy.deepcopy()` to create a **safe backup** of inventory before any changes
- Deducts stock for each item in the cart after an order is placed
- Prints **before and after stock levels** for transparency
- Flags items that have fallen at or below their **reorder level**
- Compares current inventory against the backup to verify changes

### ✅ Task 4 — Sales Analytics

- Calculates **total daily revenue** from a 4-day sales log
- Identifies the **best performing day** by revenue
- Counts how many times each item was ordered — finds the **most ordered item**
- Dynamically adds a **new day's orders** to the sales log and recalculates
- Prints a **numbered order log** showing date, order ID, total, and items

---

## 🗂️ Data Structures Used

| Structure | Purpose |
|-----------|---------|
| `menu` (dict of dicts) | Stores item name, category, price, and availability |
| `inventory` (dict of dicts) | Tracks stock quantity and reorder threshold per item |
| `sales_log` (dict of lists of dicts) | Date-wise list of orders with items and totals |
| `cart` (list of dicts) | Active cart with item name, quantity, and price |

---

## 🧾 Sample Menu

| Item | Category | Price | Status |
|------|----------|-------|--------|
| Paneer Tikka | Starters | ₹180 | Available |
| Chicken Wings | Starters | ₹220 | Unavailable |
| Butter Chicken | Mains | ₹320 | Available |
| Veg Biryani | Mains | ₹250 | Available |
| Gulab Jamun | Desserts | ₹90 | Available |
| Ice Cream | Desserts | ₹110 | Unavailable |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook or JupyterLab

### Run the Notebook

```bash
# Clone the repository
git clone https://github.com/your-username/part2-order-system.git

# Navigate into the folder
cd part2-order-system

# Launch the notebook
jupyter notebook part2_order_system.ipynb
```

> Run each cell **sequentially from top to bottom** — the menu, inventory, and sales_log are defined in the first cell and used throughout.

---

## 🛠️ Built With

- **Python 3** — Core logic and data processing
- **copy** (built-in) — Deep copy for safe inventory backup
- **Jupyter Notebook** — Interactive development environment

---

## 👩‍💻 Author

**Spoorthi M**  
**Student_id : bitsom_ba_2511762**

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
