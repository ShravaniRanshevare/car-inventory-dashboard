# car-inventory-dashboard
Excel data modelling project with Fact/Dim schema and interactive dashboard.
**📊 Car Inventory Dashboard (Excel + Tableau)**
*📌 Overview*
This project analyzes a fictional car inventory dataset using a Fact/Dimension star schema, Excel-based data modelling, and an interactive Tableau dashboard.
The goal is to demonstrate skills in data cleaning, modelling, KPI creation, and visual analytics.
The final dashboard allows users to explore:
Mileage patterns
Warranty risk
Driver behaviour
Car age distribution
Make/Model performance
*🧱 Data Model (Star Schema)*
The dataset was modelled using a Fact table and multiple Dimension tables:
Code
                 DimDriver
                     |
                 DriverKey
                     |
DimCar — CarKey — FactCarInventory — MakeModelKey — DimMakeModel
                     |
                 WarrantyKey
                     |
                 DimWarranty
*Fact Table*
FactCarInventory
CarKey
DriverKey
MakeModelKey
WarrantyKey
Age
Miles
MilesPerYear
WarrantyRisk (calculated)
Dimension Tables
DimDriver – Driver details
DimMakeModel – Make & model attributes
DimWarranty – Warranty limits
DimCar – Car metadata
*🧮 Key Calculations*
Miles Per Year
Code
Miles / Age
Warranty Risk
Code
IF Miles > WarrantyMiles THEN "Exceeded" ELSE "WithinLimit"
Total Cars
Average Miles
% Exceeding Warranty
Oldest Car Age
***📈 Dashboard Features (Tableau)***
The interactive Tableau dashboard includes:
1. Miles by Driver
Horizontal bar chart ranking drivers by total mileage.
2. Warranty Risk
Pie chart showing the proportion of cars exceeding warranty limits.
3. Car Age Distribution
Column chart showing how many cars fall into each age group.
4. Average Miles by Make
Bar chart comparing average mileage across manufacturers.
5. Interactive Filters
Users can filter the entire dashboard by:
Driver
Make
Model
Warranty Status
Age
*🛠 Tools Used*
Excel
Power Query
XLOOKUP
Fact/Dim modelling
PivotTables
Tableau
Relationships
Filters
Dashboard design
GitHub
Project documentation
Screenshots:
/screenshots/Dashboard.png
/screenshots/AvgMilesbyMake.png
/screenshots/FiltersinAction.png
*💡 Insights*
Chrysler vehicles show the highest average mileage.
Most cars remain within warranty limits, but a notable minority exceed them.
Driver “Smith” has the highest total mileage.
Car ages cluster between 10–20 years, with a few older outliers.
**🎯 What I Learned**
How to design a clean star schema for analysis
How to enrich fact tables using XLOOKUP
How to build interactive dashboards in Tableau
How to communicate insights visually
How to structure a project for portfolio and GitHub
***📁 Repository Structure***
Code
├── Car_Inventory_Dashboard.xlsx
├── screenshots/
│   ├── Dashboard.png
│   ├── AvgMilesbyMake.png
│   └── FiltersinAction.png
└── README.md
