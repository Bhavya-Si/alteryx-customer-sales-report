# Customer Sales Report Automation using Alteryx

## Objective
To build an automated Alteryx workflow that integrates customer and transaction data, applies business rules, and generates a ranked customer sales report for decision-making.

## Tools & Technologies
- Alteryx Designer
- Excel (Reporting Output)

## Input Data
1. **Customers.csv**
   - Customer master information
   - Includes responder status and customer identifiers

2. **Transactions.xml**
   - Transaction-level sales data
   - Includes customer ID and sales values

## Workflow Overview

#### Step 1: Data Ingestion & Cleaning
- Imported customer and transaction datasets
- Applied data quality checks and field standardization

#### Step 2: Business Rule Filtering
- Filtered customer data to exclude non-responders  
  *(Responder = 'No')*

#### Step 3: Transaction Aggregation
- Aggregated transaction-level data to calculate **Total Sales per Customer**

#### Step 4: Data Integration
- Joined customer master data with aggregated transaction data
- Identified and logged transactions not matched to any customer

#### Step 5: Ranking & Selection
- Sorted customers by **Total Sales (Descending)**
- Selected **Top 10 customers** by sales value

### Step 6: Reporting Output
- Exported final results to Excel:
  `CustomerSalesReport.xlsx`

## Output Report
The final Excel report contains:
- Customer details
- Total aggregated sales
- Ranked list of top-performing customers

This report is suitable for:
- Sales performance reviews
- Customer prioritization
- Management dashboards

## Key Alteryx Concepts Demonstrated
- Input & Output tools
- Data Cleansing & Filtering
- Summarize (Aggregation)
- Join tool with unmatched record handling
- Sorting & Sampling
- End-to-end workflow automation

## How to Run the Workflow
1. Open `CustomerSalesReport.yxmd` in Alteryx Designer
2. Place input files in the designated data folder
3. Run the workflow
4. View output in `CustomerSalesReport.xlsx`

## Business Value
- Eliminates manual Excel-based sales reporting
- Ensures consistent, repeatable analysis
- Improves accuracy and turnaround time for reporting

## Future Enhancements
- Parameterize date ranges using analytic apps
- Add macros for reusable customer logic
- Integrate BI tools (Power BI / Tableau) for visualization
