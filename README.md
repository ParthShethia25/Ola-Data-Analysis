


# OLA Data Analyst Project – Bengaluru Rides Analysis

## Project Overview

This project presents an end-to-end **data analysis of Ola ride bookings in Bengaluru** for a one-month period. The objective is to analyze booking trends, cancellations, revenue patterns, vehicle performance, and customer behavior, and to derive actionable business insights using **Python, SQL, and Power BI**.

The dataset is **synthetic but realistic**, generated under defined business constraints to closely mirror real-world ride-hailing operations.

---

## Tools & Technologies

* **Python (Pandas)** – Data cleaning and preprocessing
* **MySQL** – Data storage, querying, and views
* **Power BI** – Interactive dashboard and visualization
* **Excel / CSV** – Intermediate data handling

---

## Dataset Details

* **City:** Bengaluru
* **Time Period:** 1 Month (July 2024)
* **Total Records:** 103,024 bookings
* **Data Type:** Synthetic (business-rule-driven)

### Key Columns

* Booking ID, Booking Status
* Customer ID
* Vehicle Type
* Pickup & Drop Locations
* VTAT & CTAT
* Cancellation Reason (Customer / Driver)
* Booking Value
* Payment Method
* Ride Distance
* Driver Rating, Customer Rating
* Booking Datetime

---

## Business Constraints Applied

* **62% successful bookings**
* **Customer cancellations < 7%**
* **Driver cancellations < 18%**
* **Incomplete rides < 6%**
* Higher booking volume and value on **weekends and match days**
* **70% bookings under ₹500**, **28% between ₹500–₹1000**, remaining above ₹1000
* Booking IDs follow **CNR + numeric pattern**

---

## Data Cleaning & Preparation

Data cleaning was performed using Python (Pandas) and SQL:

* Removed irrelevant columns (e.g., Vehicle Images)
* Converted text values like `"null"` and `#NAME?` to real NULLs
* Merged Date and Time into a single `booking_datetime`
* Standardized booking outcomes and cancellation flags
* Unified cancellation reasons into one column
* Applied business rules (ratings only for successful rides)
* Standardized categorical data (case and spacing)
* Renamed columns for MySQL compatibility
* Exported cleaned data to CSV and imported into MySQL
* Removed hidden carriage-return characters (`CHAR(13)`) and whitespace after SQL import
* Normalized empty values to proper SQL `NULL`

Result: **A clean, consistent, analysis-ready dataset**

---

## SQL Analysis

A dedicated MySQL database was created and multiple views were built for analysis, including:

* Successful bookings
* Ride distance by vehicle type
* Cancelled rides by customers and drivers
* Top 5 customers
* Revenue from successful rides
* Average customer and driver ratings
* Incomplete rides with reasons

These views enabled efficient querying and seamless Power BI integration.

---

## Power BI Dashboard

The Power BI report is divided into **five analytical sections**:

1. Overall Performance
2. Vehicle Type Analysis
3. Revenue Analysis
4. Cancellation Analysis
5. Ratings Analysis

The dashboard highlights KPIs such as total bookings, revenue, cancellation rate, ride trends, payment preferences, and vehicle-wise performance.

---

## Key Business Insights

* **103,024 total bookings**, with **63,967 successful rides**
* **Cancellation rate of 28.08%**, indicating operational inefficiencies
* Total booking value of approximately **₹35 million**
* Cash is the most used payment method, followed by UPI
* Autos dominate short-distance trips (~10 km), while other vehicle types average **24–26 km**
* Driver and customer ratings average around **4.0**, indicating acceptable but improvable service quality
* A small group of customers contributes disproportionately to total revenue

---

## Business Recommendations

* Reduce cancellations through better driver tracking and automated reassignment
* Discourage drivers from requesting customer cancellations
* Promote digital payments (UPI) to reduce cash dependency
* Optimize vehicle pricing based on trip distance patterns
* Improve service quality to raise ratings beyond 4.5
* Retain high-value customers through loyalty and subscription models

---

## Project Outcome

This project demonstrates the **complete data analyst workflow**, from raw data generation and cleaning to SQL-based analysis and interactive business dashboards. The insights generated can help improve operational efficiency, customer experience, and revenue optimization for a ride-hailing platform.

---

## Author

**Parth Shethia**
Role: Data Analyst / Business Analyst

---

