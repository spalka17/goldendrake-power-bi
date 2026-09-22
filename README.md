# GoldenDrake Bookstore - Power BI Dashboard

[View Interactive Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZGJmMmM5NjktNTUxZC00MmYwLTk5MGItNTg2Y2Q4ZTgzOGQ4IiwidCI6Ijc1YzJlNGQ0LWQwNGMtNGNlOS1hMGVhLWM5NzViZGM0MTdlYiIsImMiOjF9&embedImagePlaceholder=true)

## Project Overview

GoldenDrake Bookstore is a fictional bookstore operating across multiple sales markets.

This Power BI project focuses on sales performance, market comparison, inventory monitoring, demand planning, genre popularity, seasonality, product profitability and customer growth.

The main goal was to create an interactive analytical report that supports sales monitoring and helps identify products and markets that may require inventory, ordering or business decisions.

## Business Context

GoldenDrake Bookstore operates across multiple markets and needs a structured way to monitor sales, inventory and product performance.

The main business challenges include:

* comparing sales performance across markets,
* monitoring inventory levels and identifying low-stock products,
* reducing the risk of stockouts and order cancellations,
* supporting reorder and demand planning decisions,
* understanding differences in genre popularity between markets,
* identifying seasonal demand patterns,
* evaluating product profitability,
* monitoring new customer acquisition.

## Analysis Goals

The report was designed to answer questions such as:

* Which books generate the highest sales?
* Which products are currently selling the fastest?
* Which products have low stock levels?
* Which products may require reordering?
* What is the projected demand for the next 7 or 30 days?
* How does sales performance differ between markets?
* How efficient are individual markets compared with the global average?
* Which book genres are most popular in different markets?
* Which publishers generate the highest average sales per book?
* How does seasonality affect sales and genre demand?
* Which products generate the highest margins?
* How does the number and share of new customers change over time?

## Report Pages

### 1. Overview

The Overview page provides a high-level summary of business performance.

It includes:

* Total Sales,
* Total Cost,
* Margin,
* Margin %,
* publisher ranking,
* sales compared with the previous period,
* detailed sales and margin analysis by product.

![Overview](screenshots/01-overview.png)

### 2. Market Performance

This page compares sales performance across individual sales markets and broader market groups.

It includes:

* selected market,
* store count and store share,
* global store count,
* global average sales per store,
* total sales by sales market,
* total sales by market group,
* comparison of average sales per store with the global average.

The selected market is highlighted across the visualizations to make comparisons easier.

![Market Performance](screenshots/02-market-performance.png)

### 3. Top Products

This page focuses on product performance and recent sales activity.

It includes:

* Total Sales,
* Total QTY,
* Sales 7D,
* Top Category,
* Fastest-Selling Book,
* ranking of books by average daily quantity sold,
* detailed Top N product ranking,
* recent 7-day performance,
* sales contribution within category.

![Top Products](screenshots/03-top-products.png)

### 4. Inventory & Demand Planning

This page supports inventory monitoring and short-term demand planning.

It includes:

* Low Stock Books (<5 Units),
* low-stock books by category,
* projected demand for a selected 7- or 30-day horizon,
* Inventory Stock Monitor,
* estimated Days to Stockout,
* Reorder Point,
* Lead Time Days,
* Recommended Order Qty,
* Sales Velocity Monitor,
* comparison of recent and 30-day average sales pace.

The inventory table is prioritized by estimated days to stockout to highlight the most urgent products.

![Inventory & Demand Planning](screenshots/04-inventory-demand-planning.png)

### 5. Genre & Publisher Insights

This page compares genre popularity and publisher performance.

It includes:

* genre share in the selected market,
* average sales per book by publisher,
* comparison of genre popularity across all sales markets,
* drill-down from book genre to individual book title.

The matrix uses conditional formatting to make differences in genre and book popularity between markets easier to identify.

![Genre & Publisher Insights](screenshots/05-genre-heatmap.png)

### 6. Seasonality & Genre Trends

This page analyzes seasonal sales patterns and differences in genre demand.

It includes:

* Peak Season,
* Peak vs Low Season,
* quantity sold by season,
* seasonal genre performance,
* filtering by market and hemisphere.

The hemisphere filter allows seasonal patterns to be interpreted correctly for markets located in the Northern and Southern Hemispheres.

![Seasonality & Genre Trends](screenshots/06-seasonality-genre-trends.png)

### 7. Product Profitability

This page analyzes products based on margin value and margin percentage.

It includes:

* Top Performer Products,
* Total Margin,
* dynamic Margin Threshold,
* dynamic Margin % Threshold,
* product segmentation into four profitability groups,
* detailed sales, quantity, margin and margin percentage analysis.

Products are classified as:

* Top performers,
* High profitability, low scale,
* High scale, lower profitability,
* Low performance.

![Product Profitability](screenshots/07-product-profitability.png)

### 8. Customer Growth

This page analyzes customer acquisition over time.

It includes:

* New Customers,
* Total Customers,
* New Customer Share,
* comparison of new and total customers across the selected period.

The time granularity of the chart changes dynamically depending on the selected period, allowing the analysis to move between daily, weekly, monthly and longer-term views.

![Customer Growth](screenshots/08-customer-growth.png)

## Data and Model

The data model is based on fact and dimension tables.

### Fact Tables

**fSales** - contains sales transactions, including products, quantities, sales values, costs, margins, customers and transaction dates.

**fInventory** - contains inventory information, including stock quantity, reorder point, lead time and average weekly sales.

### Dimension Tables

**dProduct** - contains information about books, categories, genres, publishers and product attributes.

**dStore** - contains information about stores, countries, sales markets and market groups.

**dDate** - contains calendar data used for time-based analysis and period filtering.

The data was loaded from a Lakehouse in Microsoft Fabric and transformed in Power Query.

## Key Measures and Logic

The report includes DAX measures and calculations related to:

* Total Sales, Total Cost, Margin and Margin %,
* Sales 7D and QTY 7D,
* average daily quantity sold for recent and 30-day periods,
* current stock quantity,
* low-stock identification,
* Days to Stockout,
* Recommended Order Qty,
* projected demand for 7- and 30-day horizons,
* sales velocity and velocity change,
* genre and book share by market,
* average sales per book by publisher,
* Peak Season and Peak vs Low Season,
* profitability segmentation,
* new customers and New Customer Share.

## Tools Used

* Power BI
* Power Query
* DAX
* Microsoft Fabric
* Lakehouse

## Project Status

Completed portfolio project.

The final report includes eight interactive analytical pages covering sales, market performance, products, inventory, demand, genre popularity, seasonality, profitability and customer growth.

The interactive version is available through Power BI Service.
