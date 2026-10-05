📊 Marketing Campaign Analysis – Power BI Dashboard
<img width="1920" height="1080" alt="Screenshot (639)" src="https://github.com/user-attachments/assets/efe07292-3ee3-43a8-ad0a-5af4fe6dc8de" />


📌 Project Overview
The Marketing Campaign Analysis project is a Power BI dashboard created to analyze the performance of different marketing campaigns across regions and campaign types.
The dashboard shows important metrics like Revenue, Spend, ROI, and Campaign Performance. It helps to understand which campaigns are performing well and where marketing money is being spent.
________________________________________
🎯 Objectives
•	Analyze the performance of different marketing campaigns.
•	Compare Revenue and Spend across regions.
•	Calculate and compare ROI for different campaigns.
•	Identify high-performing campaigns.
•	Compare Digital and Traditional campaigns.
•	Analyze campaign performance across different regions.
•	Create an interactive Power BI dashboard for better analysis.
________________________________________
📁 Dataset Overview
The project utilizes three structured CSV datasets:
Dataset Name	Description
Marketing_Campaign_Details	Contains campaign type (Digital/Traditional), average spend, and ROI.
Marketing_Campaign_Performance	Campaign-level data with impressions, clicks, conversions, spend, revenue, and ROI across regions and industries.
Region_Performance	Aggregated performance metrics for each region including total spend, revenue, and average ROI.
✅ Cleaned and transformed using Power Query.
✅ Data types standardized, duplicates removed, and column names renamed for clarity.
________________________________________
🧩 Data Modeling
The data was organized in Power BI to analyze campaign performance.
•	Used Campaign Name and Region for analysis.
•	Created relationships between the required data.
•	Used the data model to create visuals and DAX measures.
•	Added filters to make the dashboard interactive.
________________________________________
🧠 DAX Measures
Key DAX measures created:
Total Impressions = SUM(Marketing_Campaign_Performance[Impressions])

Total Clicks = SUM(Marketing_Campaign_Performance[Clicks])

Total Conversions = SUM(Marketing_Campaign_Performance[Conversions])

Total Spend = SUM(Marketing_Campaign_Performance[Spend])

Total Revenue = SUM(Marketing_Campaign_Performance[Revenue])

Total ROI =
DIVIDE(
    [Total Revenue] - [Total Spend],
    [Total Spend]
)

Average ROI =
AVERAGE(Marketing_Campaign_Performance[ROI])
🏆 Best Campaign Identification:
Best Campaign =
VAR MaxROI = MAX(Marketing_Campaign_Performance[ROI])
RETURN
    CALCULATE(
        FIRSTNONBLANK(
            Marketing_Campaign_Performance[Campaign_Name],
            1
        ),
        Marketing_Campaign_Performance[ROI] = MaxROI
    )
________________________________________
📊 Visualizations
Visual Type	Insight Provided
KPI Cards	Shows Total Revenue, Total Spend and ROI.
Column Chart	Compares Spend and Revenue by Region.
Combo Chart	Shows Spend and ROI by Campaign.
Bar Chart	Compares ROI of different campaigns.
Pie Chart	Shows Digital and Traditional campaign distribution.
Gauge Chart	Shows overall ROI performance.
📌 Slicers are used to filter the dashboard by Region and Campaign Type.
________________________________________
🔍 Key Insights
1.	The dashboard shows Total Revenue of approximately 42.54M.
2.	The Total Spend is approximately 25.69M.
3.	The Average ROI is approximately 0.68.
4.	Influencer Marketing is one of the better-performing campaigns.
5.	Campaign performance can be compared across different regions.
6.	Digital and Traditional campaigns can be compared to understand their performance.
7.	The dashboard helps identify campaigns that generate better returns.
________________________________________
🧰 Tools & Technologies
•	Power BI Desktop
•	Power Query for data cleaning and transformation
•	DAX for creating KPIs and calculations
•	Data Visualization
•	Data Analysis
•	CSV Datasets
________________________________________
🚀 How to Use
1.	Clone or download this repository.
2.	Open the .pbix file using Power BI Desktop.
3.	Refresh the data if required.
4.	Use the slicers to filter the dashboard.
5.	Analyze campaign performance using Revenue, Spend, and ROI.
________________________________________
📂 Repository Structure
Marketing-Campaign-Analysis/
│
├── Marketing Campaign Analysis Dashboard.pbix
└── README.md
________________________________________
🧠 Theory Corner
•	ROI = (Revenue - Spend) / Spend — used to measure the return from a marketing investment.
•	Revenue shows the amount generated from marketing campaigns.
•	Spend shows the amount spent on marketing campaigns.
•	Digital vs Traditional comparison helps understand the performance of different campaign types.
•	Power BI is used to create interactive dashboards and visualize marketing data.

