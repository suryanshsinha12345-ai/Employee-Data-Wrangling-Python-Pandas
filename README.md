# 🐍 Employee Data Wrangling & Transformation | Python

## 📊 Project Overview

This project demonstrates practical **data wrangling and transformation techniques using Python and Pandas**.

The project works with employee, project, and seniority data and combines multiple datasets into a final analytical dataset.

The objective is to demonstrate how raw datasets can be cleaned, transformed, merged, enriched, and aggregated to produce structured data ready for further analysis.

<img width="962" height="561" alt="image" src="https://github.com/user-attachments/assets/3ec927cd-02d3-4982-8fbd-de0d76d7d7bf" />

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Create structured DataFrames using Pandas
- Export and import datasets using CSV files
- Handle missing values
- Split and transform text fields
- Merge multiple datasets
- Create calculated columns
- Apply conditional transformations
- Modify designation levels based on business rules
- Aggregate project costs by employee
- Filter records based on text conditions
- Export the transformed datasets for further use

---

## 📂 Dataset Structure

The project works with three main datasets:

### 1. Project Dataset

Contains information about individual projects, including:

- ID
- Project
- Cost
- Status

Project statuses include:

- Finished
- Ongoing
- Failed

### 2. Employee Dataset

Contains employee-level information including:

- ID
- Name
- Gender
- City
- Age

### 3. Seniority Dataset

Contains:

- ID
- Designation Level

These datasets are connected through the common **ID** field. :contentReference[oaicite:1]{index=1}

---

## 🔄 Data Wrangling Process

### Step 1 — Create DataFrames

The project begins by creating separate Pandas DataFrames for:

- Projects
- Employees
- Seniority

The datasets are then saved as CSV files for subsequent processing. :contentReference[oaicite:2]{index=2}

---

### Step 2 — Handle Missing Values

Missing project costs are identified and the average project cost is calculated.

The project demonstrates the use of Pandas `fillna()` for replacing missing values with the calculated average. :contentReference[oaicite:3]{index=3}

---

### Step 3 — Split Employee Names

The original `Name` field is split into:

- First Name
- Last Name

The original Name column is then removed from the transformed dataset. :contentReference[oaicite:4]{index=4}

---

### Step 4 — Merge Multiple DataFrames

The Project, Employee, and Seniority datasets are merged using the common **ID** field.

This creates a consolidated dataset containing project information alongside employee and seniority details. :contentReference[oaicite:5]{index=5}

---

### Step 5 — Calculate Project Bonus

A new **Bonus** column is created.

Employees receive a bonus equal to **5% of project cost for Finished projects**.

Projects with other statuses receive no bonus. :contentReference[oaicite:6]{index=6}

---

### Step 6 — Modify Designation Levels

The project applies conditional business rules to designation levels:

- Employees associated with **Failed projects** are demoted by one designation level.
- Records with designation levels greater than 4 are removed. :contentReference[oaicite:7]{index=7}

---

### Step 7 — Transform Employee Names

Gender-based prefixes are added to employee first names:

- `Mr.` for male employees
- `Mrs.` for female employees

After applying the transformation, the original Gender column is removed. :contentReference[oaicite:8]{index=8}

---

### Step 8 — Age-Based Promotion

Another business rule is applied to designation levels.

Employees with an age greater than **29** receive an increase of one designation level. :contentReference[oaicite:9]{index=9}

---

### Step 9 — Calculate Total Project Cost

Project costs are aggregated by employee using Pandas `groupby()`.

The resulting dataset contains:

- Employee ID
- Employee First Name
- Total Project Cost

This provides a consolidated view of the total project cost associated with each employee. :contentReference[oaicite:10]{index=10}

---

### Step 10 — Filter Employees by City

The project also demonstrates text-based filtering by identifying employees whose city contains the letter **"o"**.

This uses Pandas string operations with `str.contains()`. :contentReference[oaicite:11]{index=11}

---

## 📈 Final Output

The final transformed dataset contains information such as:

- Employee ID
- Project
- Cost
- Project Status
- City
- Age
- First Name
- Last Name
- Designation Level
- Bonus

The notebook also generates:

- A final transformed DataFrame
- Total project cost by employee
- Employees whose city contains `"o"`

The final datasets are exported as CSV files for further analysis or use in other tools. :contentReference[oaicite:12]{index=12}

---

## 🔍 Example Results

The final project-cost aggregation produces:

| Employee | Total Project Cost |
|---|---:|
| Mr. John | 3,002,000 |
| Mrs. Alice | 2,680,000 |
| Mr. Tom | 5,150,000 |
| Mrs. Nina | 9,500,000 |
| Mrs. Amy | 600,000 |

The notebook also identifies employees associated with cities containing the letter `"o"`, including employees based in London and Newyork. :contentReference[oaicite:13]{index=13}

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Google Colab**
- **CSV**

### Python Concepts Demonstrated

- DataFrames
- Data cleaning
- Missing-value handling
- String manipulation
- Conditional transformations
- DataFrame merging
- GroupBy aggregation
- Boolean filtering
- CSV input/output

---

## 💡 Skills Demonstrated

This project demonstrates practical skills in:

- Data Wrangling
- Data Cleaning
- Data Transformation
- Data Integration
- Feature Creation
- Conditional Logic
- Aggregation
- Text Processing
- Data Export
- Pandas Data Manipulation

---

## 🚀 Key Takeaways

Through this project, I practiced how to:

1. Build structured datasets using Pandas.
2. Handle missing values in numerical columns.
3. Transform text-based fields.
4. Combine multiple datasets using common keys.
5. Create calculated fields using business rules.
6. Apply conditional transformations to data.
7. Aggregate data using `groupby()`.
8. Filter records using string conditions.
9. Export processed datasets for downstream analysis.

---

## 📂 Project Structure

```text
Employee-Data-Wrangling/
│
├── employee_project_data_wrangling.ipynb
├── Project.csv
├── Employee.csv
├── Seniority.csv
├── Final.csv
├── Employees_with_o.csv
└── README.md
