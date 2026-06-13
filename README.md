
# 📊 Analysing E-Learning Platform Purchases using MySQL

## 📌 Project Overview
This project designs and queries a relational database to study learner purchases across countries.  
It integrates **Learners, Courses, and Purchases** data to uncover:
- Sales trends
- Learner behaviour
- Category performance  

SQL techniques applied: **Joins, Aggregations, Subqueries, CTEs, Views, CASE, NULL handling**.

---

## 🎯 Objectives
1. Build a normalized database schema with proper keys & relationships.  
2. Explore data using joins & aggregations to analyse spending, popular courses, and category revenues.  
3. Apply advanced SQL (subqueries, CTEs, CASE, NULL handling) to classify learners & detect patterns.  
4. Summarize findings with actionable insights for management.  

---

## 🗄️ Database Schema
Database: **`elearning_db`**

### Learners Table
- `learner_id` (PK)  
- `full_name`  
- `country`

### Courses Table
- `course_id` (PK)  
- `course_name`  
- `category`  
- `unit_price`

### Purchases Table
- `purchase_id` (PK)  
- `learner_id` (FK → learners)  
- `course_id` (FK → courses)  
- `quantity`  
- `purchase_date`

📸 **Schema Screenshot:**  

- <img width="407" height="87" alt="Screenshot 2026-06-11 135055" src="https://github.com/user-attachments/assets/7c406b0b-6d75-4de2-963d-f6bfd04e5117" />
  

---

## 🛠️ Database Setup & Sample Data
- Created database `elearning_db`
- Inserted sample learners, courses, and purchases

📸 **Table Creation Screenshot:**  

- <img width="655" height="833" alt="Screenshot 2026-06-11 135132" src="https://github.com/user-attachments/assets/f7fe0319-5e6e-4212-848c-e81a3d4a7977" />


📸 **Sample Data Screenshot:**  

- <img width="866" height="718" alt="Screenshot 2026-06-11 143756" src="https://github.com/user-attachments/assets/c0f57d09-e114-4205-9476-293509cb6dc8" />

---

## 🔍 Data Exploration (Joins)
Queries to display learner name, course name, category, quantity, total amount, and purchase date using:
- **INNER JOIN**
- **LEFT JOIN**
- **RIGHT JOIN**

📸 **Inner Join Result:**  


📸 **Left Join Result:**  


📸 **Right Join Result:**  

---

## 📈 Core Analytical Queries
1. Learner’s total spending by country  
   📸 ![Screenshot](screenshots/q1_total_spending.png)

2. Top 3 most purchased courses  
   📸 ![Screenshot](screenshots/q2_top_courses.png)

3. Category revenue & unique learners  
   📸 ![Screenshot](screenshots/q3_category_revenue.png)

4. Learners purchasing from multiple categories  
   📸 ![Screenshot](screenshots/q4_multi_category.png)

5. Courses never purchased  
   📸 ![Screenshot](screenshots/q5_unpurchased_courses.png)

---

## 🧩 Subqueries & Correlated Subqueries
6. Learners spending above average  
   📸 ![Screenshot](screenshots/q6_above_avg.png)

7. Courses priced higher than Marketing category  
   📸 ![Screenshot](screenshots/q7_price_comparison.png)

8. Learners spending above country average  
   📸 ![Screenshot](screenshots/q8_country_avg.png)

---

## 🔗 CTE, CASE, Views & NULL Handling
9. CTE – Learners with spending above 10,000  
   📸 ![Screenshot](screenshots/q9_cte.png)

10. CASE – Classify learners (High/Medium/Low value)  
    📸 ![Screenshot](screenshots/q10_case.png)

11. NULL Handling – Replace NULL purchase counts with 0  
    📸 ![Screenshot](screenshots/q11_null_handling.png)

12. View – Category performance view  
    📸 ![Screenshot](screenshots/q12_view.png)

---

## 📊 Enhanced ER Diagram
📸 ![Screenshot](screenshots/er_diagram.png)

---

## 📌 Key Insights
- Programming courses drive **highest demand & purchase volume**.  
- AI & Data Science generate **most revenue** due to premium pricing.  
- Marketing courses are **weak performers**, requiring promotional focus.  

📸 **Insights Screenshot:**  
![Screenshot](screenshots/key_insights.png)

---

## ✅ Conclusion
- **Programming** → Volume-driven growth  
- **AI & Data Science** → Value-driven profitability  
- **Marketing** → Needs strategic repositioning  

---

## 📂 Repository Structure
