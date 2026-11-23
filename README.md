# CUSTOMER SHOPPING BEHAVIOUR AND RETAIL ANALYTICS PROJECT

OVERVIEW
An end-to-end data analytics project examining 3,900 retail customer transactions to uncover purchasing patterns, product performance, discount dependency, and customer retention behavior. The workflow covers raw data ingestion and cleaning in Python, structured business querying in MySQL, interactive visualization in Power BI, and executive storytelling through a detailed analytical report and Gamma presentation.

DATASET
- Source: Retail Customer Shopping Behavior Dataset (3,900 rows, 18 columns)
- Key Features:
  - Demographics: Customer ID, Age, Gender, Location, Subscription Status
  - Transaction Details: Item Purchased, Category, Purchase Amount (USD), Season, Size, Color
  - Shopping Behavior: Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

TOOLS & TECHNOLOGIES
- Python (pandas): Data loading, Exploratory Data Analysis (EDA), missing value imputation, and feature engineering
- MySQL: Relational database storage, conditional aggregations, and customer segmentation queries
- Power BI: Interactive dashboard design, KPI cards, dynamic slicers, and executive summary callouts
- Documentation & Storytelling: PDF Analytical Report and Gamma (executive slide presentation)

STEPS PERFORMED
1. Exploratory Data Analysis & Data Cleaning (Python)
- Inspected schema, data types, and summary statistics using df.info() and df.describe().
- Handled 37 missing values in Review Rating by imputing each product category's median rating.
- Standardized column headers to snake_case and removed redundant fields (promo_code_used) after verifying alignment with discount_applied.
- Engineered age_group bins to support demographic revenue analysis and exported the cleaned dataset to MySQL.

2. Business Analysis & Segmentation (MySQL)
- Wrote SQL queries to evaluate revenue across gender, product categories, age groups, and shipping methods.
- Calculated item-level discount dependency rates using conditional CASE WHEN aggregations.
- Segmented customers into New, Returning, and Loyal tiers based on previous_purchases along with average spend per segment.

3. Interactive Visualization (Power BI)
- Built an interactive dashboard featuring KPI cards (3.9K Customers, 3.75 Avg Review Rating, $59.76 Avg Purchase Amount).
- Added dynamic slicers (Subscription Status, Gender, Category, Shipping Type), comparative bar/donut charts, and a Key Insights card for quick executive review.

4. Reporting & Presentation (Report & Gamma)
- Compiled methodology, SQL outputs, and data-backed business recommendations into a structured PDF report.
- Created an executive presentation deck using Gamma to communicate key findings and actionable sales growth strategies clearly to non-technical stakeholders.

DASHBOARD
[Download Power BI Dashboard (.pbix)](Customer_behaviour_dashboard.pbix)

KEY RESULTS & RECOMMENDATIONS
- Non-Subscribers Drive Volume Revenue: Non-subscribers generate $170,436 (73% of total revenue) compared to $62,645 from subscribers, while average order value     is nearly identical (~$59.87 vs. $59.49).
    Recommendation: Trigger automated post-purchase incentives (e.g., free shipping after a 3rd purchase) to convert repeat non-subscribers into subscribers.

- High Discount Reliance on Select Products: Items such as Hats (50.00%) and Sneakers (49.66%) rely heavily on discounts to sell.
    Recommendation: Replace permanent blanket markdowns with bundle pricing (e.g., pairing full-price outerwear with discounted accessories) to protect profit         margins.
  
- Shipping Spend Threshold Opportunity: Express shipping orders average $60.48 versus $58.46 for standard shipping.
    Recommendation: Introduce a minimum spend threshold (e.g., free Express Shipping on orders over $75) to encourage larger basket sizes.

- Top Performers: Clothing leads category sales and revenue, while Young Adults contribute the highest revenue across age segments ($62,143).

HOW TO RUN
1. Clone the Repository:
    git clone https://github.com/your-username/customer-shopping-behavior-analysis.git
    cd customer-shopping-behavior-analysis

2. Run Python Cleaning & EDA:
    - Ensure pandas and mysql-connector-python (or sqlalchemy) are installed:
        pip install pandas sqlalchemy pymysql
    - Open and run the script/notebook inside Python_Cleaning/ to generate the cleaned dataset and load it into MySQL.

3. Execute MySQL Queries:
    - Open MySQL Workbench, connect to your local instance, and run the SQL script inside MySQL_Queries/ against the customer_behaviour schema.

4. Explore the Power BI Dashboard & Presentation:
    - Open the .pbix file in Power BI Desktop (inside Dashboard/) to interact with the filters and visuals.

Review the PDF analytical report and the Gamma presentation deck included in the repository for the full executive summary.
