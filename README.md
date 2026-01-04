# 📊 Excel Job Market & Salary Analysis Dashboard

![Dashboard Preview](/0_Resources/Images/1_Salary_Dashboard_Final_Dashboard.gif)

---

## 📌 Introduction

This Excel-based **Job Market & Salary Dashboard** was developed to help job seekers explore salary trends, skill requirements, and job characteristics across data and AI-related roles. The dashboard enables users to interactively analyze how **job title, location, employment type, and experience level** influence compensation.

The dataset used in this project is a **2025 job market dataset sourced from Kaggle**, containing real-world job postings with detailed information on salaries, required skills, company locations, and employment structures. This project demonstrates how Excel can be used as a powerful analytics and visualization tool for real-world, data-driven decision-making.

---

## 📁 Project File

- 📊 **Final Dashboard:**  
  [Job_Market_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx)

---

## 🛠️ Excel Skills Used

- 📉 Data Visualization (Bar Charts & Map Charts)
- 🧮 Advanced Formulas & Dynamic Arrays
- ❎ Data Validation & Dropdown Controls
- 🔎 Text Analysis for Skill Extraction
- 📊 Dashboard Design & UX Optimization

---

## 📂 Dataset Overview

The dataset includes thousands of job postings with the following attributes:

- 👨‍💼 Job Titles  
- 💰 Annual Salaries (USD)  
- 📍 Company Location  
- 🧠 Experience Level  
- 🛠️ Required Skills  
- ⏱️ Employment Type  

Source: **Kaggle (2025 Job Market Dataset)**

---

## 📉 Dashboard Visualizations

### 📊 Salary by Job Title

<img src="/0_Resources/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary by Job Title">

- Horizontal bar chart sorted by median salary  
- Enables quick comparison across roles  
- Highlights higher-paying senior and engineering positions  

---

## 🧮 Key Excel Formulas

### 💰 Median Salary by Role, Country & Type

```excel
=MEDIAN(
 IF(
   (jobs[job_title_short]=A2)*
   (jobs[job_country]=country)*
   (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
   (jobs[salary_year_avg]<>0),
   jobs[salary_year_avg]
 )
)
