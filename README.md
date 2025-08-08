# 📦 Inventory Risk Analysis using Pandas, NumPy & Seaborn

This project simulates a real-world supply chain scenario using actual eCommerce event data to identify inventory risks based on demand-driven logic.

## 🧠 Objective
Estimate daily product demand using historical purchase data, calculate reorder points using business logic, and flag understocked products — all using core Python libraries.

---

## 🗃 Dataset
**Source:** [Ecommerce Events History in Cosmetics Shop (Kaggle)](https://www.kaggle.com/datasets/mkechinov/ecommerce-events-history-in-cosmetics-shop)  
**File Used:** `2019-Dec.csv`  
**Volume:** ~3.5M records including views, carts, and purchases

---

## ⚙️ Tech Stack
- **Python**
- **Pandas**
- **NumPy**
- **Seaborn**
- **Matplotlib**
- Jupyter Notebook

---

## 📊 Project Workflow

1. **Load & Inspect Data**: Understand volume, missing values, event types.
2. **Filter Purchase Events**: Focus only on confirmed transactions.
3. **Estimate Daily Demand**: Use groupby and aggregation by `product_id` and date.
4. **Calculate Reorder Point**:
   - Simulate lead time (3–10 days)
   - Simulate current stock
   - Apply formula: `ROP = Daily Demand × Lead Time`
5. **Flag Stock Risk**:
   - If `stock < ROP`, flag as **"Reorder Needed"**
6. **Visualize Results**:
   - Bar plot: Current stock vs ROP
   - Heatmap: Risk level per product

---

## ✅ Sample Output

| product_id | avg_daily_demand | lead_time | reorder_point | current_stock |
|------------|------------------|-----------|----------------|----------------|
0        3762          2.518519          9           22.7             38   
1        3763          1.000000          6            6.0             44   
2        3774          1.714286          7           12.0             33   
3        3806          1.000000          9            9.0             21   
4        3928          1.000000          5            5.0             26   

 | stock_status |  
0     Stock OK  
1     Stock OK  
2     Stock OK  
3     Stock OK  
4     Stock OK
---

## 📁 Deliverables

| File | Description |
|------|-------------|
| `inventory_analysis.ipynb` | Full code with explanations |
| `final_output.csv` | Final DataFrame with demand, stock, and flags |
| `inventory_chart.png` | Side-by-side bar plot for sample products |

---

## 🚀 Skills Demonstrated
- Demand estimation from transaction data
- Real-world supply chain logic
- Pandas & NumPy for business calculations
- Seaborn for stakeholder-friendly visuals

---

## 🔗 Author
**Sankalpa Joshi**  
_Data Science & Supply Chain Analyst in progress_  
(https://www.linkedin.com/in/sankalpa-joshi/)
