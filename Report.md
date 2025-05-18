# 📊 Chicken Pastil Production Model – Linear Programming Project Report

---

## 📝 1. Problem Statement & Assumptions

This project models the production of **Chicken Pastil**, a traditional Filipino rice dish, using **linear programming concepts**. The goal is to calculate how many units can be produced based on ingredient constraints, determine total cost, profit, and break-even point, and visualize these metrics.

### Assumptions:
- Ingredients are measured in grams (g) or milliliters (mL).
- Each unit of pastil has a fixed recipe requirement.
- Ingredient prices are per gram or per mL.
- Only one product is produced.
- Fixed overhead costs (e.g., utilities) are user-input.
- No ingredient spoilage, waste, or price fluctuation.

---

## 🧠 2. Algorithm & Design Approach

### Inputs:
- Available quantity of each ingredient
- Cost per unit of each ingredient
- Recipe quantity needed per pastil unit
- Selling price per unit
- Fixed overhead cost

### Computation Steps:
1. **Max Units**: Determine the maximum number of units producible by finding the minimum of (available quantity / recipe requirement) across all ingredients.
2. **Total Cost**: Multiply each ingredient’s recipe quantity by its cost and total units produced.
3. **Cost per Unit**: Total cost ÷ units produced.
4. **Revenue**: Units × selling price.
5. **Profit**: Revenue − total cost.
6. **Break-even**: 
   \[
   \left\lceil \frac{\text{Fixed Cost}}{\text{Selling Price} - \text{Cost per Unit}} \right\rceil
   \]

### Output:
- Printable results
- Matplotlib graph: Cost, Revenue, Profit vs. Units

---

## 📊 3. Sample Calculations

### Input Data:
| Ingredient     | Available | Cost per Unit | Recipe Qty |
|----------------|-----------|----------------|-------------|
| Rice           | 10,000 g  | ₱0.05          | 150 g       |
| Chicken Breast | 5,000 g   | ₱0.20          | 100 g       |
| Onion          | 1,000 g   | ₱0.06          | 10 g        |
| Garlic         | 500 g     | ₱0.12          | 5 g         |
| Soy Sauce      | 1,000 mL  | ₱0.03          | 10 mL       |
| Cooking Oil    | 1,000 mL  | ₱0.08          | 5 mL        |
| Banana Leaf    | 500 g     | ₱0.025         | 20 g        |

- Selling Price: ₱60
- Fixed Cost: ₱1000

### Manual Calculation:
- Rice: 10,000 / 150 = 66 units
- Chicken: 5,000 / 100 = 50 units
- Onion: 1,000 / 10 = 100 units  
- Banana Leaf: 500 / 20 = 25 units → LIMITING INGREDIENT

**Max Units = 25**

### Cost per Unit:
- Total cost from all ingredients × 25 units = ₱679.40
- Cost per unit = ₱27.18

### Revenue:
- 25 × ₱60 = ₱1500

### Profit:
- ₱1500 – ₱679.40 = ₱820.60

### Break-even Units:
\[
\left\lceil \frac{1000}{60 - 27.18} \right\rceil = \left\lceil \frac{1000}{32.82} \right\rceil = 31 \text{ units}
\]

---

## 🖥️ 4. Program Output

