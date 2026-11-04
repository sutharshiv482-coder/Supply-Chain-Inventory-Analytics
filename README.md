# 📦 Supply Chain & Inventory Analytics

An end-to-end **Supply Chain & Inventory Analytics** project designed to analyze inventory levels, product demand, supplier performance, order fulfillment, and supply chain operations using **Python, SQL, Excel, and an Interactive Dashboard**.

This project follows a structured Data Analyst workflow, covering business problem definition, data inspection, data cleaning, data preparation, exploratory data analysis (EDA), SQL business analysis, KPI development, dashboard development, business insights, and actionable recommendations.

The objective is to transform supply chain and inventory data into meaningful business insights that support better inventory planning, operational efficiency, and data-driven decision-making.

---

## 🎯 Project Objective

The objective of this project is to analyze supply chain and inventory operations to understand stock availability, product demand, supplier performance, and operational efficiency.

Key objectives include:

- Analyze inventory levels and stock availability.
- Identify products with low stock or potential overstocking.
- Understand product demand and sales patterns.
- Evaluate supplier performance.
- Analyze order fulfillment and delivery performance.
- Identify inventory management inefficiencies.
- Monitor product and category performance.
- Develop relevant supply chain and inventory KPIs.
- Build an interactive dashboard for performance monitoring.
- Generate actionable recommendations for inventory optimization.

---

## 💼 Business Problem

Businesses must maintain sufficient inventory to meet customer demand while avoiding excessive stock that increases storage costs and ties up working capital.

Poor inventory management can lead to stockouts, overstocking, delayed deliveries, inefficient purchasing decisions, and increased operational costs.

Supply chain teams need to understand:

- Which products have insufficient inventory?
- Which products have excess stock?
- Which products demonstrate higher demand?
- Which suppliers perform better?
- Are customer orders being fulfilled on time?
- Which product categories contribute most to demand or sales?
- Where do supply chain delays occur?
- How efficiently is inventory being managed?
- Which operational areas require improvement?

This project uses data analytics to investigate these questions and support informed supply chain and inventory management decisions.

---

## 💡 Business Value

The analysis provides a structured approach to:

- Monitor inventory availability.
- Identify potential stockout and overstock risks.
- Understand product demand patterns.
- Evaluate supplier and order performance.
- Analyze order fulfillment and delivery metrics.
- Compare product and category performance.
- Improve inventory planning and replenishment decisions.
- Identify operational inefficiencies.
- Support data-driven supply chain decisions.

The goal is to connect inventory, product demand, supplier performance, and order fulfillment with measurable operational outcomes.

---

## ❓ Business Questions

The project focuses on answering the following business questions:

1. What is the total inventory available?
2. Which products have the lowest stock levels?
3. Which products may be at risk of stockouts?
4. Which products have comparatively high inventory levels?
5. Which products or categories demonstrate higher demand?
6. Which suppliers provide better operational performance?
7. What is the average order fulfillment time?
8. Are orders being delivered within the expected timeframe?
9. Which product categories contribute most to sales or order volume?
10. Which products require inventory replenishment?
11. Where are potential supply chain bottlenecks?
12. How can inventory management and operational efficiency be improved?

*The questions addressed in the final analysis depend on the fields available in the dataset.*

---

# 🔄 Project Workflow

The project follows an end-to-end Data Analyst workflow.

```text
1. Understand Business Problem
          ↓
2. Inspect Supply Chain Dataset
          ↓
3. Perform Data Cleaning
          ↓
4. Prepare Data using Pandas
          ↓
5. Validate Prepared Data
          ↓
6. Perform Exploratory Data Analysis
          ↓
7. Perform SQL Business Analysis
          ↓
8. Define Supply Chain & Inventory KPIs
          ↓
9. Analyze Inventory & Operational Performance
          ↓
10. Build Interactive Dashboard
          ↓
11. Generate Business Insights
          ↓
12. Recommend Actions
```

---

## 1️⃣ Understand Business Problem

The first step was to translate supply chain and inventory management requirements into analytical questions.

Key activities:

- Define the project objectives.
- Understand inventory management requirements.
- Identify important supply chain metrics.
- Determine the product, supplier, and order dimensions required for analysis.
- Identify potential stock availability and replenishment issues.
- Establish the business questions to be answered.

---

## 2️⃣ Inspect the Supply Chain Dataset

The dataset was inspected to understand its structure, assess data quality, and identify fields relevant to supply chain and inventory analysis.

Key activities:
- Load the dataset and inspect its structure.
- Review the number of rows and columns.
- Examine column names and data types.
- Inspect product, SKU, and category information.
- Review supplier and warehouse details.
- Examine purchase orders and delivery dates.
- Inspect order quantities and received quantities.
- Review inventory levels, reorder points, and safety stock.
- Examine unit costs, freight costs, and GST rates.
- Identify fields required for supply chain KPIs.

---

## 3️⃣ Perform Data Cleaning

Python and Pandas were used to identify, investigate, and address data-quality issues before analysis.

Key activities:
- Identify missing values and inconsistent placeholders.
- Detect and remove exact duplicate records.
- Investigate repeated purchase order IDs and near-duplicate records.
- Standardize text formatting and categorical values.
- Normalize supplier, product, warehouse, and location information.
- Parse numeric fields containing currency symbols, units, and inconsistent separators.
- Validate GST rates and supplier GSTIN formats.
- Investigate negative, zero, and unusually large quantities or costs.
- Review inconsistencies between ordered and received quantities.
- Parse order, promised, and received dates while preserving the original values.
- Flag invalid dates and investigate ambiguous date formats.
- Identify conflicting order statuses and delivery information.

Data corrections were applied where justified. Records with unresolved issues were retained for review rather than automatically modified.

---

## 4️⃣ Prepare Data Using Pandas

Pandas was used to standardize data, create analytical fields, and prepare the dataset for further analysis.

Key activities:
- Standardize column values and data formats.
- Convert validated numeric fields to appropriate data types.
- Prepare parsed date columns for time-based analysis.
- Organize product, supplier, warehouse, and purchase order information.
- Prepare inventory fields, including on-hand stock, reorder points, and safety stock.
- Create data-quality flags for suspicious or inconsistent records.
- Prepare fields for order fulfillment and supplier lead-time analysis.
- Structure the dataset for exploratory analysis, SQL analysis, and dashboard development.
- Preserve original values where corrections or interpretations require further review.

Derived metrics were prepared only when the required source fields and calculation rules were sufficiently clear.

---

## 5️⃣ Validate the Prepared Dataset

Validation checks were performed after cleaning and transformation to assess data consistency and identify unresolved issues.

Key activities:
- Recheck missing and invalid values.
- Verify exact duplicate removal and repeated order ID handling.
- Confirm data types and numeric conversions.
- Review standardized categorical values.
- Validate product, supplier, and warehouse information.
- Investigate negative and zero inventory-related values.
- Review discrepancies between ordered and received quantities.
- Check order, promised, and received date sequences.
- Reassess cancelled orders with recorded receipt dates.
- Verify calculated fields and data-quality flags.
- Perform final consistency checks before analysis.

Unresolved anomalies were flagged for further investigation instead of being treated as confirmed errors. This helps reduce the risk of misleading supply chain metrics.

---

## 6️⃣ Perform Exploratory Data Analysis (EDA)

Exploratory Data Analysis was used to investigate inventory levels, procurement activity, supplier performance, and order fulfillment patterns.

### 📦 Inventory Analysis

- Analyze on-hand stock across products and categories.
- Identify products below their reorder points.
- Compare inventory levels against safety stock.
- Investigate potential stock shortages and excess inventory.
- Identify products requiring closer inventory monitoring.
- Examine inventory distribution across warehouses.

### 📈 Product Demand Analysis

- Analyze average daily demand across products.
- Compare order quantities across products and categories.
- Identify products with comparatively high demand.
- Examine demand patterns across available time periods.
- Compare demand with current inventory levels.
- Identify products that may require replenishment planning.

### 🏭 Supplier Performance Analysis

- Compare procurement activity across suppliers.
- Analyze supplier-related order volumes.
- Calculate supplier lead times using validated order and receipt dates.
- Examine delivery delays against promised dates.
- Identify suppliers associated with recurring delays.
- Compare supplier performance using consistent and clearly defined measures.

### 🚚 Order Fulfillment Analysis

- Analyze the relationship between order, promised, and received dates.
- Calculate fulfillment time using validated date fields.
- Identify orders received later than their promised dates.
- Investigate orders with missing or inconsistent receipt information.
- Compare fulfillment patterns across suppliers and warehouses.
- Examine cancelled orders with conflicting delivery records.

### 🗂️ Product Category Analysis

- Compare inventory levels across product categories.
- Analyze order quantities by category.
- Identify categories with higher inventory requirements.
- Compare demand and stock availability across categories.
- Investigate category-level patterns that may affect replenishment decisions.

### 💰 Cost and Procurement Analysis

- Analyze unit purchasing costs across products and suppliers.
- Examine freight costs across available procurement records.
- Calculate order-level costs where the required fields are reliable.
- Review GST rates and their impact on cost calculations where applicable.
- Compare purchasing and freight costs across suppliers or categories.
- Investigate unusual cost values and potential procurement inefficiencies.

EDA provides the foundation for SQL-based business analysis, KPI development, dashboard reporting, and data-driven supply chain recommendations.

---

## 7️⃣ Perform SQL Business Analysis

SQL was used to perform structured, business-focused analysis on the prepared supply chain and inventory data.

### Business Questions

- What is the total recorded inventory quantity?
- How many distinct products are included in the analysis?
- Which products have the lowest stock levels?
- Which products have the highest inventory quantities?
- Which categories have higher inventory levels?
- Which products demonstrate higher demand?
- Which suppliers have better delivery performance?
- What is the average fulfillment time?
- How many orders were delivered late?
- Which products may require replenishment?

*Questions involving suppliers, orders, delivery performance, demand, or costs require the corresponding fields in the dataset.*

### SQL Analysis Areas

- Inventory quantity analysis.
- Product-level analysis.
- Product category analysis.
- Stock availability analysis.
- Demand and order analysis.
- Supplier performance analysis.
- Order fulfillment analysis.
- Delivery delay analysis.
- Cost analysis, where applicable.
- KPI calculations.
- Performance comparisons across products and categories.

SQL transforms prepared data into structured metrics that support operational analysis and dashboard reporting.

---

## 8️⃣ Define Key Performance Indicators (KPIs)

KPIs provide a consistent way to monitor inventory status, product demand, supplier performance, and operational efficiency.

| KPI | Purpose |
|---|---|
| Total Products | Measures the number of distinct products analyzed |
| Total Inventory Quantity | Measures the recorded quantity of inventory |
| Low-Stock Products | Counts products meeting the defined low-stock criteria |
| Overstocked Products | Counts products meeting the defined overstock criteria |
| Total Orders | Measures the number of orders analyzed |
| Average Order Fulfillment Time | Measures average time required to fulfill orders |
| On-Time Delivery Rate (%) | Measures the percentage of eligible orders delivered on time |
| Supplier Lead Time | Measures the time between ordering from a supplier and receiving the goods |
| Product Demand | Measures demand using an appropriate order quantity or sales metric |
| Inventory Value | Measures inventory value when reliable quantity and unit cost data are available |

### KPI Calculation Considerations

- Define low-stock and overstock thresholds before classifying products.
- Avoid summing inventory quantities across incompatible units of measurement.
- Distinguish order processing time from supplier lead time.
- Define on-time delivery using an agreed delivery date and actual delivery date.
- Calculate inventory value only when quantity and unit cost fields are available.
- Use the correct level of analysis to avoid double-counting orders or products.

The final KPI list should match the available dataset and the metrics actually implemented.

---

## 9️⃣ Analyze Inventory & Operational Performance

This stage combines product, inventory, supplier, demand, and order metrics to understand operational performance.
