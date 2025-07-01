<div align="center">

# ✈️ Optimal Repatriation Scheduling for Vietnam ✈️

### _A MILP Case Study of the COVID-19 Campaign_

</div>

<div align="center">

![Project Status](https://img.shields.io/badge/status-completed-green)
![Language](https://img.shields.io/badge/language-Python-blue)
![Library](https://img.shields.io/badge/library-PuLP-orange)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

</div>

---

> This project addresses the **Repatriation Scheduling Problem (RSP)** by applying a mathematical model to find an optimal flight plan, helping to bring Vietnamese citizens home in the most efficient and humane way possible during the COVID-19 pandemic crisis.

<p align="center">
  <img src="https://i.pinimg.com/originals/3c/3d/8c/3c3d8c50e9a7e0c5242404f2d7a2b972.gif" alt="Animated Airplane" width="500"/>
</p>

## 🎯 Introduction

The COVID-19 pandemic created an unprecedented humanitarian crisis, leaving millions of people stranded abroad. In response, the Vietnamese government initiated a large-scale repatriation campaign. However, with demand far exceeding the capacity of flights and quarantine facilities, decision-making became incredibly complex.

This project utilizes **Mixed Integer Linear Programming (MILP)** to build a mathematical model that helps policymakers answer the question: *How can we allocate limited resources (aircraft, quarantine beds) to maximize humanitarian value, prioritizing the most vulnerable individuals?*

---

## 🛠️ Technical Architecture & Tools

The model was built and solved using open-source tools, following this workflow:

| Step | Tool / Library | Purpose |
| :--- | :--- | :--- |
| **1. Data Loading & Processing** | `Python`, `Pandas` | Read and structure data from an Excel file. |
| **2. Model Formulation** | `PuLP` | Translate mathematical formulas (objective function, constraints) into Python code. |
| **3. Problem Solving** | `CBC Solver (COIN-OR)` | Find the optimal solution for the formulated MILP model. |
| **4. Environment** | `Google Colab` | A cloud-based environment to run the code without complex local setup. |

## 📁 Directory Structure
## 🚀 Setup & Run Guide

To reproduce the project's results, follow these steps:

1.  **Clone the Repository** (Remember to replace with your actual repo URL)
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Install Required Libraries**
    ```bash
    pip install pandas pulp
    ```

3.  **Run the Model**
    Open the `notebooks/Repatriation_MILP_Model.ipynb` file in Google Colab or Jupyter Notebook and run all cells. Ensure the path to the data file in `data/` is correct.

---

## 📈 Key Results & Analysis

The model found an optimal solution with the following main characteristics:

| Metric | Value | Analysis |
| :--- | :--- | :--- |
| **Total Priority Score** | **22,110** | The maximum achievable "humanitarian value" score. |
| **Total Citizens Repatriated**| **2,211** | The number of people brought home in one planning period. |
| **Aircraft Fleet Utilization** | **8 / 8 (100%)** | All available aircraft were deployed and operated at full capacity. |
| **Quarantine Facility Utilization** | **2,211 / 5,000 (44.22%)** | Significant surplus in quarantine capacity. |

### 💡 Key Insight: Where is the Bottleneck?

<div align="center">

> The analysis reveals that **transportation capacity (the number of aircraft) is the primary system bottleneck**, not quarantine capacity. This implies that to repatriate more people, investing in increasing the aircraft fleet would be more effective than expanding quarantine facilities.

</div>

---

## ⚠️ Model Limitations

1.  **Static Model**: Only considers a single planning period and does not capture the dynamic, long-term nature of the actual campaign.
2.  **Estimated Data**: The input data was synthesized from public sources, not official operational data.
3.  **Simplification**: The model excludes complex real-world factors such as costs, flight routing, and diplomatic procedures.

## 🧑‍💻 Author

| Name | Student ID | Class |
| :--- | :--- | :--- |
| **Quan Manh NGUYEN** | `21070555` | BDA2021B |

---
<div align="center">
A report for the course **INS3048 - Optimization in Quantitative Management** <br>
**Vietnam National University, Hanoi - International School** <br>
_June, 2025_
</div>
