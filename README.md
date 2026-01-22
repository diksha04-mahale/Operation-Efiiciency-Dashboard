# 📊 Operational Efficiency Dashboard (Power BI)

## 🔹 Project Overview

The **Operational Efficiency Dashboard** is a Power BI project designed to monitor, analyze, and improve operational performance across departments and resources. The dashboard converts raw operational data into actionable insights by tracking utilization, downtime, productivity, and quality metrics.

This project demonstrates skills in **data modeling, DAX, KPI design, and business-oriented analytics**, making it suitable for roles in operations analytics, business intelligence, product, and PSU/enterprise environments.

---

## 🎯 Objectives

* Measure overall operational efficiency
* Identify high-downtime resources and bottlenecks
* Track productivity and quality trends over time
* Enable data-driven decision-making through interactive visuals

---

## 🛠️ Tools & Technologies

* **Power BI** – Data visualization & dashboarding
* **DAX** – Calculated measures & KPIs
* **Excel / CSV** – Data source
* **Data Modeling** – Relationships & aggregations

---

## 📁 Dataset Structure

**Table: `Operations_Data`**

| Column Name    | Description                                            |
| -------------- | ------------------------------------------------------ |
| Date           | Operational date                                       |
| Department     | Functional department (Manufacturing, Packaging, etc.) |
| Resource       | Machine / Production Line                              |
| Shift          | Morning / Evening / Night                              |
| Planned Hours  | Scheduled operational hours                            |
| Actual Hours   | Actual working hours                                   |
| Downtime (hrs) | Non-operational hours                                  |
| Units Produced | Total output units                                     |
| Defects        | Defective units                                        |

---

## 📐 Key DAX Measures

### Resource Utilization (%)

```DAX
Utilization % =
DIVIDE(SUM(Operations_Data[Actual Hours]), SUM(Operations_Data[Planned Hours])) * 100
```

### Downtime (%)

```DAX
Downtime % =
DIVIDE(SUM(Operations_Data[Downtime (hrs)]), SUM(Operations_Data[Planned Hours])) * 100
```

### Production Efficiency (Units / Hour)

```DAX
Production Efficiency =
DIVIDE(SUM(Operations_Data[Units Produced]), SUM(Operations_Data[Actual Hours]))
```

### Defect Rate (%)

```DAX
Defect Rate % =
DIVIDE(SUM(Operations_Data[Defects]), SUM(Operations_Data[Units Produced])) * 100
```

---

## 📊 Dashboard Components

### 🔹 KPI Cards

* Average Resource Utilization (%)
* Downtime Percentage (%)
* Production Efficiency (Units/Hour)
* Defect Rate (%)

### 🔹 Trend Analysis

* **Line Chart** showing utilization trends over time
* Drill-down by department and shift

### 🔹 Bottleneck Analysis

* **Bar Chart** displaying downtime by resource/machine
* Highlights underperforming assets

### 🔹 Output vs Quality

* **Clustered Column Chart** comparing units produced vs defects by department

### 🔹 Interactive Filters (Slicers)

* Department
* Resource
* Shift
* Date

---

## 💡 Key Insights (Example)

* Manufacturing department shows highest utilization but contributes most to downtime
* Machine B accounts for ~35% of total downtime
* Defect rate decreases significantly during optimized shift allocation

---

## 📈 Business Impact

* Enables early identification of operational inefficiencies
* Supports preventive maintenance planning
* Improves resource allocation and productivity
* Enhances quality monitoring

---

This dashboard focuses not just on visualization, but on **operational decision-making**, aligning technical analytics with real-world business efficiency problems.

---

If you find this project useful, feel free to ⭐ the repository!
