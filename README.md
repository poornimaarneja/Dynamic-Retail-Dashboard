# Dynamic-Retail-Dashboard 
### Dynamic Retail Dashboard: Overview

The Dynamic Retail Dashboard is an interactive Excel-based tool designed to analyze and visualize retail data. Leveraging Power Query for data transformation and integrating datasets hosted on GitHub, the dashboard provides dynamic charts and KPIs to address key business questions and support data-driven decision-making.

---

### Datasets Used

1. **Orders Table**  
   Tracks details of customer orders, including product, shipping, and financial metrics.  

   **Sample Data:**

   | Order ID        | Returned | Order Date | Ship Date | Ship Mode      | Customer Name | Segment   | Country        | Market  | Sales   | Profit | Discount |
   |-----------------|----------|------------|-----------|----------------|---------------|-----------|----------------|---------|---------|--------|----------|
   | CA-2012-124891 | No       | 31-07-2020 | 31-07-2020| Same Day       | Rick Hansen   | Consumer  | United States  | US      | 2309.65 | 762.18 | 0        |
   | IN-2013-77878  | Yes      | 05-02-2021 | 07-02-2021| Second Class   | Justin Ritter | Corporate | Australia      | APAC    | 3709.40 | -288.77| 0.1      |
   | IN-2013-71249  | No       | 17-10-2021 | 18-10-2021| First Class    | Craig Reiter  | Consumer  | Australia      | APAC    | 5175.17 | 919.97 | 0.1      |

2. **Returns Table**  
   Records returned orders and their corresponding markets.

   **Sample Data:**

   | Returned | Order ID       | Market         |
   |----------|----------------|----------------|
   | Yes      | MX-2013-168137 | LATAM          |
   | Yes      | US-2011-165316 | LATAM          |
   | Yes      | ES-2013-1525878| EU             |
   | Yes      | CA-2013-118311 | United States  |

3. **People Table**  
   Provides information about sales representatives and their regions.

   **Sample Data:**

   | Person            | Region   |
   |-------------------|----------|
   | Anna Andreadi     | Central  |
   | Chuck Magee       | South    |
   | Kelly Williams    | East     |
   | Matt Collister    | West     |
   | Deborah Brumfield | Africa   |

---

### Problems Solved and Approach

#### 1. **Key Performance Indicators (KPIs)**
   - **Objective:** Dynamically calculate metrics like Total Sales, Total Profit, Orders, and Profit Margin.
   - **Steps:**  
     - Load the Orders table using Power Query.  
     - Create calculated fields for Profit Margin, Total Sales, Total Profit, and Orders.  
     - Display KPIs using an interactive table with visual indicators like icons.

![image](https://github.com/user-attachments/assets/8ca3fa2d-a4c1-4439-9400-c04a9143f2c9)


#### 2. **Sales and Profit Analysis**
   - **Objective:** Identify trends in sales and profits over time.  
   - **Steps:**  
     - Build a Pivot Table grouping data by Year and Month.  
     - Plot Sales and Profit values on a Line Chart.  
     - Use slicers for filtering by categories, regions, or segments.

![image](https://github.com/user-attachments/assets/dbaeb84d-f3f3-434b-8217-add4acc97d3f)


#### 3. **Category-Wise Profit**
   - **Objective:** Evaluate profitability across product categories.  
   - **Steps:**  
     - Create a Pivot Table with Category as rows and Profit as values.  
     - Visualize data with a sorted Bar Chart and interactive slicers.

![image](https://github.com/user-attachments/assets/51b99977-c762-4c66-ae64-56bd765a7192)


#### 4. **Segment-Wise Sales Share**
   - **Objective:** Show sales contribution of customer segments.  
   - **Steps:**  
     - Calculate percentage share of each segment using Sales values.  
     - Present data with a Pie or Donut Chart, displaying percentage labels dynamically.

![image](https://github.com/user-attachments/assets/344f2889-7660-48eb-9d88-9e5162d4b6d0)


#### 5. **Sales by Country**
   - **Objective:** Compare sales performance by country.  
   - **Steps:**  
     - Use a Pivot Table to group sales by country.  
     - Apply conditional formatting or Heatmaps for visualization.  
     - Optionally, use a Geographic Map Chart for a spatial overview.

![image](https://github.com/user-attachments/assets/ca621679-ef0b-447a-9f6a-98b13e71d07c)


#### 6. **Top 5 Subcategories**
   - **Objective:** Identify the best-performing subcategories.  
   - **Steps:**  
     - Sort a Pivot Table by Sales in descending order.  
     - Filter for the top 5 subcategories and create a Column Chart.

![image](https://github.com/user-attachments/assets/452beea5-bce6-4746-bda7-5b3976837820)


#### 7. **Bottom 5 Subcategories**
   - **Objective:** Highlight underperforming subcategories.  
   - **Steps:**  
     - Sort the Pivot Table by Sales in ascending order.  
     - Filter for the bottom 5 subcategories and emphasize them in a Column Chart.

![image](https://github.com/user-attachments/assets/9c01cae6-f4f9-4657-a036-fba9c9128693)


#### 8. **Yearly Sales Trends**
   - **Objective:** Analyze yearly sales trends.  
   - **Steps:**  
     - Use a Pivot Table to group data by Year.  
     - Create a Line Chart to show trends over time with slicers for interactive filtering.

![image](https://github.com/user-attachments/assets/4ec4d2e5-3787-455a-9953-84378b01daff)


#### 9. **Market-Wise Total Sales** 

- **Load Data:** Import the Orders Table using Power Query.  
- **Group by Market:** Summarize total sales by the "Market" column.  
- **Create Pivot Table:** Add "Market" to Rows and "Sales" to Values.  
- **Sort:** Arrange markets by descending sales to highlight top performers.  
- **Visualize:** Use a Bar or Column Chart to display sales by market.

---


![image](https://github.com/user-attachments/assets/4d9660a3-fff5-43d3-86d6-9b65f0d6e281)


#### 10. **Region-Wise Total Sales**  

   - **Combine Data:** Merge Orders and People Tables via "Region" using Power Query.  
- **Group by Region:** Calculate total sales for each region.  
- **Create Pivot Table:** Add "Region" to Rows and "Sales" to Values.  
- **Highlight:** Use Conditional Formatting to emphasize highest and lowest regions.  
- **Visualize (Optional):** Create a Map Chart for geographical insights.
![image](https://github.com/user-attachments/assets/74534801-9a3b-40c0-bd8d-c3ac046c37d5)

---

### Dynamic Features
- **Real-Time Updates:** Charts and KPIs refresh automatically based on slicer inputs.
- **Automated Data Handling:** Power Query ensures seamless data cleaning and transformation.
- **Interactive Visualizations:** Multiple filters enable deeper insights.

---

### Future Enhancements
- **Return Analysis:** Investigate return rates by market or category.  
- **Customer Profitability:** Identify the most and least profitable customers.  
- **Market Insights:** Compare market performance trends.  
- **Product-Level Analysis:** Assess contributions of individual products.

---

### Significance
This dashboard is a powerful tool for retail businesses to:
- Monitor key metrics and trends.
- Optimize operations and identify growth opportunities.
- Make informed, data-driven decisions.

