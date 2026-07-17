# HR People & Culture Analytics: Attrition Deep-Dive

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data_Analytics-005571?style=for-the-badge)

## 📌 Project Overview
This project is an interactive, executive-level **Human Resources (HR) Analytics Dashboard** built in **Tableau**. It is designed to move beyond basic reporting and answer critical management questions: *Are we retaining our best people? Which departments are bleeding talent? Who is at the highest risk of leaving next?*

The dashboard focuses on actionable visual storytelling, identifying the root causes of employee attrition (turnover) and estimating its financial impact on the business.

🔗 **[View the Interactive Dashboard on Tableau Public](INSERT_YOUR_TABLEAU_PUBLIC_LINK_HERE)**

---

## 📊 Key Features & Visuals
The dashboard is composed of 5 highly distinct, purpose-driven visualizations:

1. **Executive KPIs**: Instantly shows the overall Attrition Rate, Employee Count, and a calculated **Estimated Attrition Cost** (based on the industry benchmark of 50% of annual salary per lost employee).
2. **The Problem Area (Heatmap)**: A Department vs. Job Role matrix that uses a diverging color palette to instantly pinpoint the exact teams experiencing the highest turnover.
3. **The Salary Squeeze (Box Plots)**: Analyzes salary distributions across job roles, highlighting the compensation differences between employees who left vs. those who stayed.
4. **The Flight Risk Radar (Scatter Plot)**: Plots Job Satisfaction against Years Since Last Promotion. It uses calculated logic to flag active employees as "High Risk" if they are highly dissatisfied and stuck in their roles for 3+ years.
5. **The Overtime Burnout (Donut Chart)**: A dual-axis chart demonstrating the direct correlation between working overtime and increased attrition rates.

---

## ⚙️ Technical Highlights (Calculated Fields)
This project translates complex business logic into Tableau calculated fields, including:
*   **Dynamic Attrition Costing**: `SUM([Attrition Count]) * AVERAGE([MonthlyIncome]) * 12 * 0.5`
*   **Predictive Flight Risk Flagging**: `IF [JobSatisfaction] <= 2 AND [YearsSinceLastPromotion] >= 3 THEN 'High Risk' ELSE 'Low Risk' END`
*   **Advanced Dashboard Actions**: Fully interactive filtering where selecting a specific department or role filters all other visuals on the canvas simultaneously.

---

## 📁 Dataset
*   **Source**: IBM HR Analytics Employee Attrition & Performance (via Kaggle)
*   **Details**: 1,470 rows of simulated HR data containing demographics, job roles, satisfaction scores, and attrition flags.

---

## 🚀 How to Use This Repository
1. Click the link above to interact with the live dashboard on Tableau Public.
2. The raw dataset (`WA_Fn-UseC_-HR-Employee-Attrition.csv`) is included in this repository.
3. You can download the `.twbx` (Tableau Packaged Workbook) directly from my Tableau Public profile to view the backend calculations, container structure, and dashboard actions.

---
*Built by [Your Name/LinkedIn] - 2026*
