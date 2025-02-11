# 🖨️ Optimization of 3D Printing Queue & Rod Cutting  

This project provides solutions for two optimization problems:  
1. **Optimizing a 3D printer queue** using a greedy algorithm.  
2. **Maximizing profit from rod cutting** using dynamic programming (memoization & tabulation).  

## 📌 Task 1: 3D Printer Queue Optimization  
The `optimize_printing` function schedules an efficient order for printing models while considering priority and printer constraints.  

### 🔹 Input Data  
- `print_jobs` – a list of printing jobs in the format:  
  ```python
  print_jobs = [
      {"id": "M1", "volume": 100, "priority": 1, "print_time": 120},
      {"id": "M2", "volume": 150, "priority": 2, "print_time": 90},
      {"id": "M3", "volume": 120, "priority": 3, "print_time": 150}
  ]
   ```

- `printer_constraints` – printer limitations:
  
  ```python
  printer_constraints = {
    "max_volume": 300,  
    "max_items": 2  }
  ```

### 🔹 Output Data
The function returns a dictionary with the optimal print order and total printing time:

  ```python
  {
    "print_order": ["M1", "M2", "M3"],  
    "total_time": 360  
  }
  ```
### 🔹 Algorithm Logic  
✔️ Groups jobs to print simultaneously without exceeding constraints.  
✔️ Prioritizes high-priority tasks first.  
✔️ The printing time of a batch is determined by the longest job in the group.  

---

## 📌 Task 2: Optimal Rod Cutting  

Two approaches are implemented:  

- **`rod_cutting_memo`** – recursive approach with memoization.  
- **`rod_cutting_table`** – iterative approach with tabulation.  

### 🔹 Input Data  
- **`length`** – the length of the rod.  
- **`prices`** – a list of prices for each length:  
  ```python
  length = 5  
  prices = [2, 5, 7, 8, 10]  
  ```

### 🔹 Output Data  
The function returns the maximum profit and the optimal cutting strategy:  

```python
{
    "max_profit": 12,  
    "cuts": [2, 2, 1],  
    "number_of_cuts": 2  
}
```

### 🔹 Algorithm Logic  
✔️ Uses dynamic programming for optimal cutting.  
✔️ Solutions are implemented using both recursive memoization and tabulation.  
✔️ Selects the combination of cuts that yields the highest profit.  

