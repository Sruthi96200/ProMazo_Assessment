
# ACME Strategic Optimization Dashboard

**Author:** Sruthi Keerthana Nuttakki  
**Date:** February 23, 2025  

---

## Overview

This project implements the ProMazo/Acme case study by developing an optimization engine and interactive dashboard. The solution focuses on maximizing sales and margins under a set of business constraints, providing actionable insights through interactive visualizations.

**Key Components:**
- **Synthetic Data Generation:**  
  Creates a dataset that replicates Acme's corporate hierarchy:
  - *Portfolio → Geography → Category → Brand → Segment*  
  Each segment contains realistic financial parameters: **Initial Sales**, **Margin**, **Min Trend**, **Max Trend**, **Min Contribution**, and **Max Contribution**.

- **Optimization Algorithms:**  
  The model enforces:
  - **Trend Constraints:** New Sales must fall between *Initial Sales × (1 + Min Trend)* and *Initial Sales × (1 + Max Trend)*.
  - **Contribution Constraints:** Each segment’s new sales (as a fraction of its brand’s total) must lie within defined bounds. For feasibility, the sum of minimum contributions per brand is ≤ 1 and the sum of maximum contributions is ≥ 1.
  
  Four strategic scenarios are implemented:
  1. **Maximize Sales:** Compute the maximum achievable sales.
  2. **Maximize Profit (Margin):** Optimize to achieve the highest profit.
  3. **Sales Target + Profit Maximization:** Identify a solution that meets a specific sales target while maximizing profit.
  4. **Profit Target + Sales Maximization:** Determine a solution that meets a specific profit target while maximizing sales.

- **Interactive Visualizations:**  
  Interactive Plotly charts display:
  - A grouped bar chart comparing **Old vs. New Sales**.
  - A pie chart showing the **Distribution of New Sales by Segment**.
  - A brand-level bar chart summarizing overall performance.

- **5-Year Projections:**  
  An iterative simulation updates the model over a 5-year period, culminating in a line chart that visualizes brand-level sales trends.

> **Note:** If a scenario returns an **Infeasible** result, it indicates that the specified target is too aggressive given the current constraints. This feedback is valuable for strategic adjustments.

---

## Deliverables

- **Synthetic Data Set:**  
  A dataset reflecting Acme’s corporate hierarchy with realistic financial values and enforced contribution constraints.

- **Optimization Scenarios:**  
  Implementation of four strategic scenarios:
  1. Maximize Sales
  2. Maximize Profit (Margin)
  3. Sales Target with Profit Maximization
  4. Profit Target with Sales Maximization

- **Interactive Visualizations:**  
  - Sales Comparison (grouped bar chart)
  - Sales Distribution (pie chart)
  - Brand-Level Performance (bar chart)

- **5-Year Financial Projections:**  
  An iterative simulation forecasting brand-level performance over 5 years.

- **Streamlit Dashboard:**  
  An interactive dashboard that integrates all components for real-time scenario analysis.

---

## Setup and Installation

### Prerequisites

Ensure that the following Python packages are installed in your environment:
- `streamlit`
- `pandas`
- `numpy`
- `plotly`
- `pulp`
- `matplotlib`


## Code Structure

- **acme_dashboard.py:**  
  The main Streamlit application integrating synthetic data generation, optimization, and visualization components.
  
- **synthetic_data.py:**  
  Contains functions for generating synthetic data that reflects Acme's corporate hierarchy.

- **optimization.py:**  
  Implements the optimization algorithms for the four strategic scenarios.

- **visualization.py:**  
  Provides functions for creating interactive Plotly charts.

- **requirements.txt:**  
  Lists all Python dependencies required to run the project.

---

## Results

The dashboard provides actionable insights into optimal sales and margin under various constraints, helping Acme make informed strategic decisions.

### Optimization Results
- Detailed tables and metrics show the impact of each scenario on sales, profit, and segment contributions.

### Visualizations
- Interactive charts allow users to explore:
  - **Sales Comparison:** Grouped bar chart for Old vs. New Sales.
  - **Sales Distribution:** Pie chart illustrating the distribution of New Sales by segment.
  - **Brand Performance:** Bar chart summarizing overall brand performance.

### 5-Year Projections
- A forward-looking analysis forecasts brand-level performance over a 5-year period, providing strategic insights for long-term growth and profitability.


### Running the Dashboard

Open a terminal or command prompt, navigate to the project directory, and


```bash
streamlit run "FULL_PATH_TO_YOUR_FILE.py"




