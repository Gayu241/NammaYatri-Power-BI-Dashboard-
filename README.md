# Namma Yatri Ride-Hailing Data Analysis

## Project Overview

This project presents a comprehensive data analysis of the Namma Yatri dataset, conducted using Power BI. The goal was to uncover key insights into operational efficiency, ride demand patterns, revenue generation, and customer behavior to inform strategic decision-making and improve overall service quality.

## Problem Statement

In the dynamic ride-hailing industry, understanding operational metrics and customer behavior is crucial for optimizing service delivery and ensuring profitability. This analysis addresses the need to:
* Identify periods of peak demand and revenue.
* Understand the effectiveness of different payment methods.
* Pinpoint high-performing and underperforming geographical zones.
* Analyze trip completion rates and cancellation reasons to reduce operational bottlenecks.
* Provide actionable recommendations for improving efficiency, customer satisfaction, and marketing strategies.

## Data Sources

The analysis is based on a single Excel workbook (`nammayatri.xlsx`) containing five interconnected tables:

* **`Trips`**: Core trip information including unique trip IDs, fare amounts, payment methods, and pickup/drop-off locations.
* **`Trip_Details`**: Detailed trip events, including trip requests (`searches`), quote search flags, and cancellation indicators (`customer_not_cancelled`, `driver_not_cancelled`), OTP entry, and ride completion (`end_ride`).
* **`Assembly`**: Contains geographical zone IDs and their corresponding names.
* **`Duration`**: Maps duration IDs to hourly time bins (e.g., "0-1" for 12 AM to 1 AM).
* **`Payment`**: Links payment method IDs to descriptive names (e.g., Cash, UPI, Credit Card).

## Methodology

The project followed a structured analytical methodology:

1.  **Data Acquisition:** Data was imported directly from the `nammayatri.xlsx` Excel file into Power BI Desktop.
2.  **Data Preparation & Cleaning:** Power Query Editor was extensively used to:
    * Standardize data types (e.g., `tripid` to Whole Number, `fare` to Decimal Number).
    * Ensure data consistency across tables for accurate relationships.
    * Handle any missing or anomalous values.
3.  **Data Modeling:** A robust star-schema-like data model was built in Power BI's Model View, establishing clear relationships between fact tables (`Trips`, `Trip_Details`) and dimension tables (`Assembly`, `Duration`, `Payment`). Cross-filter directions were configured for optimal data flow.
4.  **Exploratory Data Analysis (EDA):**
    * Variables were classified into categorical and numerical types.
    * Various visualization techniques (line charts, bar charts, pie charts, matrices) were employed to analyze trends, distributions, and relationships.
    * DAX (Data Analysis Expressions) measures were created for key performance indicators (KPIs) such as Total Trips, Total Revenue, Cancellation Percentages, and Completion Rates.
5.  **Insight Generation & Recommendations:** Based on the visual analysis and KPI computations, actionable business insights were derived, leading to strategic recommendations for Namma Yatri.

## Key Findings (Executive Summary)

* **High Cancellation Rates:** A significant operational bottleneck, with **41% of trips mutually cancelled** by both driver and customer, contributing to an overall successful ride rate of only **45%**.
* **Distinct Demand & Revenue Peaks:** The **"0-1 AM" (midnight)** and **"1-2 PM"** hours consistently show the highest ride demand and revenue generation, indicating critical periods for resource optimization.
* **High-Performing Zones:** **Ramanagaram** leads in trip volume, while **Bangalore South** generates the highest revenue, highlighting distinct opportunities for targeted strategies.
* **Customer Intent:** Trips initiated with a **"quote search" demonstrate a 100% completion rate** in the dataset, indicating high customer commitment at this stage of the booking process.
* **Digital Payment Preference:** Digital methods (Credit Card, UPI, Debit Card) collectively dominate over cash payments, signaling user preference and potential for streamlined financial operations.

## Business Recommendations

Based on the analysis, the following recommendations are put forth for Namma Yatri:

1.  **Prioritize Reducing Mutual Cancellations:** Investigate root causes (e.g., driver behavior, fare transparency, communication issues) and implement solutions such as driver incentives for completion, improved matching algorithms, or stricter cancellation policies.
2.  **Optimize Driver Allocation:** Strategically deploy drivers to high-demand/high-revenue zones (e.g., Ramanagaram, Bangalore South) during peak hours (0-1 AM, 1-2 PM) using dynamic heat maps and surge pricing.
3.  **Leverage Quote Search Feature:** Promote the "quote search" functionality in marketing campaigns, emphasizing its 100% completion reliability to build user trust and drive conversions.
4.  **Enhance Digital Payment Adoption:** Continue to streamline and promote digital payment options, potentially through small incentives, given the strong user preference.
5.  **Refine Overall Trip Funnel:** Address the broader 83.4% search-to-completion rate by optimizing user experience from initial search to ride completion, beyond just the quote-search stage.

## Technical Details

* **Tool:** Microsoft Power BI Desktop
* **Language:** DAX (Data Analysis Expressions) for creating custom measures and calculations.
* **Data Model:** Star schema-like with relationships between 5 tables.

## How to Use/Open the Project

1.  **Download Power BI Desktop:** Ensure you have [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed on your machine.
2.  **Clone this Repository:** `git clone [repository_url]`
3.  **Open the `.pbix` file:** Navigate to the project directory and open the `NammaYatri_Powerbi_Dashboard.pbix` file with Power BI Desktop. The data is embedded within the file.
4.  **Interact with Dashboards:** Explore the interactive dashboards and reports to delve deeper into the insights.

---
