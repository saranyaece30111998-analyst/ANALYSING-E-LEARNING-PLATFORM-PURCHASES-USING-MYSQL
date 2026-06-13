
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
- <img width="927" height="732" alt="Screenshot 2026-06-11 143827" src="https://github.com/user-attachments/assets/d1213e83-567d-4a39-a537-45c178356c1a" />


📸 **Left Join Result:**  
- <img width="822" height="610" alt="Screenshot 2026-06-12 095310" src="https://github.com/user-attachments/assets/66b0e698-cf78-4005-bc4a-e36d8e96e489" />


📸 **Right Join Result:**  
- <img width="1002" height="646" alt="Screenshot 2026-06-12 095356" src="https://github.com/user-attachments/assets/d3d8024d-b60e-4677-9662-6e8bb0432180" />

---

## 📈 Core Analytical Queries
1. Learner’s total spending by country  
   - <img width="731" height="531" alt="Screenshot 2026-06-12 095651" src="https://github.com/user-attachments/assets/2baeecc5-f425-4600-a6ca-f0d8fd7bff99" />


2. Top 3 most purchased courses  
   - <img width="661" height="480" alt="Screenshot 2026-06-12 095757" src="https://github.com/user-attachments/assets/09a04ae7-b276-4a21-afbc-6416642c8c30" />

3. Category revenue & unique learners  
   - <img width="807" height="492" alt="Screenshot 2026-06-12 095900" src="https://github.com/user-attachments/assets/752a3fbb-2335-4be4-8c15-399147f892e6" />


4. Learners purchasing from multiple categories  
   - <img width="732" height="527" alt="Screenshot 2026-06-12 095931" src="https://github.com/user-attachments/assets/98b345f8-b8de-4051-825c-5c6ed77045b3" />


5. Courses never purchased  
   - <img width="647" height="402" alt="Screenshot 2026-06-12 100010" src="https://github.com/user-attachments/assets/7c61678c-6164-4147-b356-5ab4aa8f226f" />


---

## 🧩 Subqueries & Correlated Subqueries
6. Learners spending above average  
   - <img width="1016" height="692" alt="Screenshot 2026-06-12 100055" src="https://github.com/user-attachments/assets/54b5cca8-ffa1-4fca-8c28-3e9167528011" />


7. Courses priced higher than Marketing category  
   - <img width="992" height="567" alt="Screenshot 2026-06-12 100157" src="https://github.com/user-attachments/assets/d8a7e66d-d26f-4841-82ec-fa26c2bd6b08" />


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

## 📊 Analytics & Insights

### **1. Descriptive Analysis (What happened?)**
- All five courses were purchased at least once, ensuring full dataset coverage.  
- **Programming courses** (Python Basics, Web Development) recorded the highest purchase counts.  
- **AI (Machine Learning)** and **Data Science** contributed the highest revenue due to premium pricing.  
- **Marketing (Digital Marketing)** showed the lowest demand compared to technical categories.  
- Revenue distribution highlights Programming as **volume-driven** and AI/Data Science as **value-driven**.  

---

### **2. Diagnostic Analysis (Why it happened?)**
- **Python Basics** recorded strong demand with ₹150,000 revenue from multiple purchases.  
- **Web Development** contributed ₹240,000 revenue, making Programming the highest-volume category.  
- **Machine Learning (AI)** generated ₹200,000 revenue from fewer transactions, showing high value due to premium pricing.  
- **Data Science Fundamentals** achieved ₹150,000 revenue, reflecting steady demand for advanced skills.  
- **Digital Marketing** produced only ₹40,000 revenue, confirming it as the weakest performer.  
- Overall, Programming drives purchase **volume**, while AI and Data Science drive **profitability**.  

---

### **3. Predictive Analysis (What is likely to happen?)**
- Programming courses are expected to continue leading in purchase volume, with projected revenues rising to **₹450,000–₹500,000**.  
- AI (Machine Learning) is likely to remain the highest revenue driver, potentially crossing **₹300,000+**.  
- Data Science courses are projected to sustain steady growth, reaching **₹200,000–₹250,000**.  
- Marketing may remain underperforming unless supported by targeted promotions, stagnating near **₹50,000–₹80,000**.  
- Technical categories (Programming, AI, Data Science) will dominate both learner interest and profitability.  

---

### **4. Prescriptive Analysis (What should be done?)**
- **Promote Programming courses** (Python Basics, Web Development) through bundled offers or certifications to leverage high demand.  
- **Upsell premium courses** (Machine Learning, Data Science) by offering advanced learning paths to sustain revenue growth.  
- **Revitalize Marketing courses** with targeted campaigns, discounts, or updated content to improve learner uptake.  
- **Introduce cross-category packages** (e.g., Programming + AI) to encourage multi-category purchases.  
- **Monitor seasonal trends** and align promotions with peak months to capture higher order volumes.  
- Focus on technical categories as **core revenue drivers**, while strategically repositioning Marketing to balance portfolio performance.  

---

## ✅ Conclusion
- **Programming** → Volume-driven growth  
- **AI & Data Science** → Value-driven profitability  
- **Marketing** → Needs strategic repositioning  

---


