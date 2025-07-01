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
