# OptiStock – Inventory & Logistics Management System

## 📌 Overview
OptiStock is a **C++ inventory and logistics management system** that integrates:
- **Inventory control** (Add, Delete, Update, View stock)
- **Order processing** (Automatic inventory update after sales)
- **Search functionality** (Rabin–Karp pattern matching)
- **Route optimization** (Floyd–Warshall shortest path)
- **Restocking decisions** (Greedy algorithm)
- **Inventory optimization** (Backtracking for best subset selection)
- **Stock analysis** (Divide-and-Conquer to find highest-stock item)

Data is stored in simple text files for persistence.

---

## 📂 File Structure
optistock/
│── proj.cpp # Main program with all logic
│── inventory.txt # Inventory data: particulars,quantity
│── graph.txt # Adjacency matrix for city routes
│── order_number.txt # Tracks last order number
│── order_files/ # Generated order files (e.g., delhiorder_6.txt)


---

## ⚙️ Features & Functions

### **1. Graph Algorithms**
| Function | Description |
|----------|-------------|
| `readGraph(filename)` | Reads a weighted adjacency matrix from file and returns cost matrix. |
| `floydWarshall(graph)` | Implements Floyd–Warshall all-pairs shortest path algorithm. |

---

### **2. String Matching**
| Function | Description |
|----------|-------------|
| `searchRabinKarp(text, pattern)` | Rabin–Karp substring search using rolling hash. |

---

### **3. Inventory Search**
| Function | Description |
|----------|-------------|
| `searchInventory(item)` | Case-insensitive search in `inventory.txt` using Rabin–Karp. |

---

### **4. Inventory File Operations**
| Function | Description |
|----------|-------------|
| `readInventory()` | Reads all items from inventory file into memory. |
| `writeInventory(inventory)` | Saves updated inventory to file. |

---

### **5. Inventory CRUD**
| Function | Description |
|----------|-------------|
| `addItemToInventory(particulars, quantity)` | Adds a new item to inventory. |
| `deleteItemFromInventory(particulars)` | Removes an item from inventory. |
| `upgradeItemInInventory(particulars, newQuantity)` | Updates quantity for an item. |
| `showFullInventory()` | Displays entire inventory in a table. |

---

### **6. Order Processing**
| Function | Description |
|----------|-------------|
| `processOrder()` | Creates order file, updates inventory, and increments order number. |

---

### **7. Inventory Algorithms**
| Function | Description |
|----------|-------------|
| `greedyRestocking()` | Lists items with stock below a user-defined threshold. |
| `backtrackingOptimization()` | Finds subset of items with maximum total quantity (backtracking). |
| `divideAndConquerAnalysis()` | Finds the highest-stock item using divide-and-conquer. |

---

### **8. Menus**
| Function | Description |
|----------|-------------|
| `manageInventory()` | Inventory management menu. |
| `main()` | Main menu with navigation to all features. |

---

## 🧮 Algorithms Used
| Feature                  | Algorithm           |
|--------------------------|--------------------|
| Route Optimization       | Floyd–Warshall     |
| String Search            | Rabin–Karp         |
| Restocking Decision      | Greedy             |
| Inventory Optimization   | Backtracking       |
| Quantity Analysis        | Divide & Conquer   |


Follow Menu Options

M → Manage Inventory

P → Process Orders

O → Optimize Routes

S → Search Inventory

Q → Quit

💡 Example Workflow

Add an item → Manage Inventory → Add Item.

Process an order → Inventory is updated automatically.

Find shortest route → Optimize Routes menu.

Search an item → Search Inventory.

Check restocking needs → Greedy Algorithm.

Optimize stock subset → Backtracking.
