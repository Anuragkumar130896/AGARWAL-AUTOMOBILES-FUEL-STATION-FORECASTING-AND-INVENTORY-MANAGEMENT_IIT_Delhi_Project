#  Fuel Station Forecasting and Inventory Management

###  Academic Case Study | ADSDS Batch 3 - Group 15  
**Authors**: Anurag Kumar, Anupam Deep Verma  
**Presented at**: Indian Institute of Technology (IIT) Delhi

---

##  Project Overview

This repository contains a detailed case study on **forecasting fuel demand and optimizing inventory management** for **Agarwal Automobiles**, an authorized Bharat Petroleum fuel station located in **Sagar District, Madhya Pradesh, India**.

The project combines:
- Descriptive statistics
- Time series forecasting techniques
- Optimization modeling  
to **minimize operational costs** while ensuring sufficient fuel inventory.

---

## Tools & Technologies Used

- **Excel** – Descriptive statistics, error metrics, Solver-based inventory planning
- **Python** – Forecasting model implementation
- **Google Colab** – Model evaluation and visualizations
- **Git & GitHub** – Version control and collaboration
- **Solver** – Optimization model for order planning

---


---

##  Business Background

- **Fuel Station**: Agarwal Automobiles (Authorized BPCL dealer)
- **Products**: Diesel, Petrol, High-Speed Petrol (HSP)
- **Storage Tanks**:  
  - Diesel: 20,000 Litres  
  - Petrol: 15,000 Litres  
  - HSP: 10,000 Litres

- **Ordering Rules**:  
  - Orders must total **exactly 12,000 Litres**
  - Orders can only be placed in **multiples of 3,000 Litres**
  - Deadline: Orders placed before 3:00 p.m. are delivered next day
  - **Losses**: 0.4% per 1,000 litres due to transit evaporation
  - **Ordering cost**: ₹150 per order

---

## Data Available

- **Monthly Sales**: Apr 2009 – May 2016
- **Daily Sales**: May 2015 – May 2016
- **Orders Placed on BPCL**: Dec 2015 – May 2016
- **Prices & Margins**:
  - Diesel: ₹60/litre, ₹1.5 margin
  - Petrol: ₹70/litre, ₹2.33 margin
  - HSP: ₹73/litre, ₹2.5 margin

---

##  Descriptive Analysis

### Central Tendency & Variability (Daily Sales)

| Fuel | Mean | Std Dev | Min | Max |
|------|------|---------|-----|-----|
| Petrol | 3606 | 706 | 1430 | 5940 |
| Diesel | 5366 | 1884 | 353 | 14579 |
| HSP | 361 | 172 | 21 | 1116 |

- **Diesel** shows highest variability and largest number of outliers.
- **HSP** is the most stable with least variation.

### Boxplot Insights

- Diesel: Wide IQR, extreme outliers.
- Petrol: Moderate variability with some high-value spikes.
- HSP: Tight distribution, minimal fluctuation.

### Outlier & Trend Analysis

- Outliers concentrated in late 2015 to early 2016.
- Diesel had unusual spikes suggesting external events.
- Petrol showed consistent demand.
- HSP showed flat demand trend.

---

##  Forecasting Techniques Used

Forecasting was done using multiple models for all three fuel types:

- **Simple Moving Average**
- **Weighted Moving Average**
- **Exponential Smoothing**
- **Double Exponential Smoothing**
- **Triple Exponential Smoothing**

#### Forecasting Error Metrics
- ME (Mean Error)
- MAD (Mean Absolute Deviation)
- MAPE (Mean Absolute Percentage Error)
- RMSE (Root Mean Square Error)

| Fuel | Best Model | MAPE |
|------|------------|------|
| Petrol | Weighted Moving Average (9-day) | 10.93% |
| Diesel | Double Exponential Smoothing | 22.44% |
| HSP | Double Exponential Smoothing | 40.43% |

---

##  Inventory Planning Model

###  Objective: **Minimize Total Cost**
**Cost Components**:
1. Holding Cost = 10% of Cost Price  
2. Ordering Cost = ₹150  
3. Fuel Cost = Selling Price – Margin

###  Constraints:
- Total order = 12,000 litres or 0
- Multiples of 3,000 litres only
- Tank capacity limits
- Forecasts and re-order point logic


Used **Excel Solver** to minimize TC subject to the constraints.

---

##  Key Findings

- Diesel is the most unpredictable fuel to manage due to erratic demand.
- Using **Weighted Moving Average** and **Exponential Smoothing**, prediction accuracy improved significantly.
- The optimal inventory model reduced waste and ensured adequate supply.
- Manual intuition used previously can be replaced with **data-driven analytics**.

---

##  Google Colab Link for Python Forecasting

[Open Colab ]https://drive.google.com/file/d/1WPzeJKKOtAz5mSAG6SqY2_lH-573h4hL/view?usp=sharing

---


---

## Author

**Anurag Kumar**  

 Data Science Certifications – IIT Roorkee, IIT Delhi 
M.Tech (Construction Technology and Management)   
anu130896@gmail.com  
+91 9680285982  

---

##  Acknowledgments

- Indian Institute of Technology (Delhi)
- BPCL fuel station team
- ADSDS Batch 3 – Group 15

---

##  License

This project is for academic and educational use only. Not for commercial reuse.





