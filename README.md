# fast-food-nutrition-analysis-powerbi
Power BI dashboard for nutrition analysis across fast food chains
## 🚀 Fast Food Nutrition Analysis - Power BI

This project analyzes the nutritional quality of items from major fast-food chains using Power BI.

### 📂 Files Included
- `Fast Food Nutrition Analysis.pbix`: Power BI dashboard file
- `food_table_cda2.csv`: Dataset of food items and nutritional facts
- `CDACL-004-Fastfood Analysis.docx`: Written report with methodology and insights
- `Fast_Food_Analysis_Presentation.ppt`: Visual summary for presentation

### 📊 Key Insights
- Restaurants ranked by **health score** based on calorie, fat, sodium, etc.
- Distribution of **high-risk items** (based on defined nutrition thresholds)
- Chick Fil-A ranked as **one of the healthiest**, based on average nutrient score

### 🧮 Risk Category Formula
```DAX
Risk Category = 
IF(
  [calories] > 700 || [sodium] > 1500, "High",
  IF([calories] > 400 || [sodium] > 500, "Medium", "Low")
)
