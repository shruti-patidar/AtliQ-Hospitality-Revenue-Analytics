# 🏨 AtliQ Hospitality Revenue Analytics Dashboard

> **An end-to-end Power BI Business Intelligence solution** developed to
> help AtliQ Grands monitor hotel performance, optimize pricing
> strategies, improve occupancy, and support data-driven revenue
> decisions.

------------------------------------------------------------------------

# 📌 Table of Contents

-   Project Overview
-   Business Problem
-   Business Objectives
-   Business Questions Answered
-   Hospitality Domain Overview
-   Dataset Description
-   ETL Process
-   Data Cleaning & Transformation
-   Data Model
-   DAX Measures
-   Dashboard Overview
-   Key Performance Indicators
-   Key Business Insights
-   Business Recommendations
-   Project Highlights
-   Business Impact
-   Dashboard Preview
-   Tech Stack
-   Project Structure
-   Skills Demonstrated
-   Future Enhancements
-   Author

------------------------------------------------------------------------

# 📖 Project Overview

AtliQ Grands is a luxury hotel chain operating across multiple cities in
India. With increasing competition and declining revenue, management
required a centralized analytics solution to monitor hotel performance
and make better business decisions.

This project transforms raw hospitality booking data into an interactive
Power BI dashboard using Power Query, Star Schema data modeling, and DAX
measures. The solution provides executives with real-time visibility
into revenue, occupancy, customer satisfaction, booking trends, and
Operational performance.

------------------------------------------------------------------------

# 🎯 Business Problem

The management faced several challenges:

-   Declining revenue and market share
-   No centralized reporting system
-   Limited visibility into property performance
-   Difficulty tracking occupancy and revenue KPIs
-   Inefficient pricing decisions
-   Heavy dependency on manual reporting

The objective was to build a dashboard capable of supporting revenue
Management and strategic decision-making.

------------------------------------------------------------------------

# 🎯 Business Objectives

-   Monitor hotel performance across cities and properties
-   Track revenue and occupancy trends
-   Evaluate booking platform performance
-   Analyze room category demand
-   Monitor customer ratings
-   Measure hospitality KPIs
-   Support pricing and revenue optimization
-   Enable data-driven executive decisions

------------------------------------------------------------------------

# ❓ Business Questions Answered

-   Which city generates the highest revenue?
-   Which hotel properties contribute the most revenue?
-   Which room class has the highest booking percentage?
-   Which booking platform contributes the highest bookings?
-   How does occupancy vary across cities and properties?
-   How do customer ratings compare across hotels?
-   How does weekday performance compare with weekends?
-   Which properties have higher cancellation rates?
-   How do ADR, RevPAR, DSRN, DBRN and Realisation % perform?

------------------------------------------------------------------------

# 🏨 Hospitality Domain Overview

This project focuses on hospitality revenue management concepts:

-   Revenue Management
-   Dynamic Pricing
-   Occupancy
-   ADR (Average Daily Rate)
-   RevPAR (Revenue Per Available Room)
-   Customer Ratings
-   Cancellation Analysis
-   Booking Platform Analysis
-   Demand vs Supply
-   Weekday vs Weekend Performance

------------------------------------------------------------------------

# 📂 Dataset Description

## Fact Tables

-   fact_bookings
-   fact_aggregated_bookings

## Dimension Tables

-   dim_hotels
-   dim_rooms
-   dim_date

The datasets contain booking transactions, hotel details, and room
categories, dates, customer ratings, capacity, and revenue information.

------------------------------------------------------------------------

# 🔄 ETL Process

``` text
CSV Files
    ↓
Power Query
    ↓
Data Cleaning
    ↓
Data Transformation
    ↓
Star Schema Data Model
    ↓
DAX Measures
    ↓
Interactive Power BI Dashboard
```

------------------------------------------------------------------------

# 🧹 Data Cleaning & Transformation

-   Validated data types
-   Created relationships
-   Built calendar table
-   Classified Weekday/Weekend
-   Optimized tables
-   Verified data quality
-   Prepared analytical model

------------------------------------------------------------------------

# ⭐ Data Model

A Star Schema was implemented using:

-   2 Fact Tables
-   3 Dimension Tables

Benefits: - Faster filtering - Better DAX performance - Reduced
redundancy - Scalable reporting

------------------------------------------------------------------------

# 🧮 DAX Measures

Developed **26+ DAX measures**, including:

### Revenue Metrics

-   Revenue
-   Total Bookings
-   Total Capacity
-   Successful Bookings

### Performance Metrics

-   Occupancy %
-   ADR
-   RevPAR
-   DBRN
-   DSRN
-   DURN

### Customer Metrics

-   Average Rating
-   Cancellation %
-   No Show %
-   Realisation %

### Analytical Metrics

-   Booking % by Platform
-   Booking % by Room Class
-   Revenue WoW %
-   Occupancy WoW %
-   ADR WoW %
-   RevPAR WoW %
-   DSRN WoW %

------------------------------------------------------------------------

# 📊 Dashboard Overview

## Page 1 -- Revenue Insights

-   Revenue Overview
-   Revenue by City
-   Occupancy by City
-   Ratings by City
-   Booking Platform Analysis
-   Weekly Trend
-   Weekday vs Weekend Analysis

## Page 2 -- Property Performance

-   Revenue by Property
-   Booking % by Room Class
-   Property Performance Matrix
-   Occupancy Analysis
-   Rating Analysis

## Page 3 -- Executive KPI Dashboard

-   Revenue
-   ADR
-   RevPAR
-   Occupancy %
-   DSRN
-   Realisation %
-   KPI Trends
-   Category Analysis

------------------------------------------------------------------------

# 📈 Key Performance Indicators

  KPI              Purpose
  ---------------- --------------------------------
  Revenue          Total realized revenue
  Occupancy %      Room utilization
  ADR              Average Daily Rate
  RevPAR           Revenue Per Available Room
  Average Rating   Customer satisfaction
  Cancellation %   Cancelled booking ratio
  Realisation %    Successfully utilized bookings
  DBRN             Daily Booked Room Nights
  DSRN             Daily Sellable Room Nights
  DURN             Daily Utilized Room Nights

------------------------------------------------------------------------

# 🔍 Key Business Insights

-   Mumbai generated the highest revenue.
-   Elite rooms recorded the highest booking share.
-   Online Travel Agencies contributed most bookings.
-   Weekend occupancy exceeded weekday occupancy.
-   Revenue and occupancy varied significantly across cities.
-   Customer ratings highlighted opportunities for service improvement.
-   Cancellation trends revealed revenue leakage opportunities.

------------------------------------------------------------------------

# 💡 Business Recommendations

-   Implement dynamic pricing during peak demand.
-   Promote direct bookings to reduce OTA commission.
-   Improve service quality at low-rated properties.
-   Optimize pricing using occupancy trends.
-   Reduce cancellation through flexible booking policies.
-   Expand premium room availability in high-demand markets.

------------------------------------------------------------------------

# 📌 Project Highlights

-   Built an end-to-end hospitality analytics solution.
-   Designed a Star Schema with 2 fact and 3 dimension tables.
-   Developed 26+ DAX measures.
-   Created a three-page interactive dashboard.
-   Implemented custom report tooltips, slicers, and conditional
    formatting.
-   Delivered actionable business insights for executives.

------------------------------------------------------------------------

# 📈 Business Impact

The dashboard enables stakeholders to:

-   Monitor KPIs in real time.
-   Compare property performance.
-   Optimize pricing strategies.
-   Improve occupancy.
-   Reduce manual reporting.
-   Support data-driven decision-making.

------------------------------------------------------------------------

# 💻 Tech Stack

-   Power BI
-   Power Query
-   DAX
-   Microsoft Excel
-   Star Schema Data Modeling

------------------------------------------------------------------------

# 📂 Project Structure

``` text
Hospitality Revenue Analytics
│
├── Dataset
├── Power BI Report (.pbix)
├── Dashboard Screenshots
├── README.md
└── Documentation
```

------------------------------------------------------------------------

# 🎯 Skills Demonstrated

### Business Intelligence

-   Dashboard Design
-   KPI Development
-   Business Storytelling

### Power BI

-   DAX
-   Power Query
-   Interactive Visualizations
-   Conditional Formatting
-   Custom Report Tooltips
-   Data Modeling

### Analytics

-   Hospitality Analytics
-   Revenue Analytics
-   Customer Analytics
-   Performance Analysis

------------------------------------------------------------------------

# 🚀 Future Enhancements

-   Dynamic Titles
-   Drill-through Navigation
-   Row-Level Security (RLS)
-   Mobile Layout Optimization
-   Time-Series Forecasting
-   AI-based Anomaly Detection

------------------------------------------------------------------------

# 👩‍💻 Author

**Shruti Patidar**

-   LinkedIn: *www.linkedin.com/in/shruti-patidar26*

------------------------------------------------------------------------

⭐ If you found this project useful, consider giving it a **Star**.
