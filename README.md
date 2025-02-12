# Financial Data Visualization and Chatbot Query System

This project consists of two key components:
1. **Financial Data Visualization** – Analyzing and visualizing financial data from a CSV file.
2. **Chatbot for Financial Queries** – A chatbot that processes user queries to retrieve financial metrics from the uploaded CSV file.

---

## 📊 Task 1: Financial Data Visualization

This component processes financial data, cleans it, calculates year-over-year growth, and generates insightful visualizations.

### **Features:**
1. **Data Cleaning**:  
   - Removes special characters (e.g., `$`, `,`) from financial values.  
   - Converts financial figures into numerical data types.

2. **Year-over-Year Growth Calculation**:  
   - Uses `pct_change()` to calculate **Revenue Growth (%)**, **Net Income Growth (%)**, etc.

3. **Data Aggregation**:  
   - Summarizes financial metrics by **Company** and **Year**.  
   - Generates two CSV reports:
     - `company_summary.csv` → Aggregated data per company.
     - `year_summary.csv` → Aggregated data per year.

4. **Reshaping Data for Analysis**:  
   - Uses `pd.melt()` to transform data into a tidy format.

5. **Visualizations**:  
   - **Line Graph**: Trends in **Total Revenue** for each company over the years.  
   - **Bar Chart**: Average **Revenue Growth (%)** across companies and years.

---

## 💬 Task 2: Chatbot for Financial Queries

This chatbot enables users to query financial metrics from the uploaded CSV file.

### **How It Works:**
1. **Uploading CSV Data**:  
   - The chatbot loads financial data into a Pandas DataFrame.  
   - Column names are formatted for consistency.

2. **Interpreting User Queries**:  
   - Uses **regular expressions (regex)** to extract key components:
     - **Company Name** (e.g., Microsoft, Tesla, Apple)
     - **Year** (e.g., 2022, 2023, 2024)
     - **Financial Metric** (e.g., total revenue, net income, operating cash flow)

3. **Finding Relevant Data**:  
   - Searches the DataFrame for matching company, year, and financial metric.  
   - Returns the requested financial value if found.

4. **Generating Responses**:  
   - Displays financial data if available.  
   - Notifies the user if no matching data is found.

5. **Exit Command**:  
   - Users can type **"exit"** to terminate the conversation.

---

## 🔍 Example Queries:

- `"What is the total revenue for Apple in 2022?"`  
- `"What is the net income for Microsoft in 2023?"`  
- `"What is the operating cash flow for Tesla in 2024?"`  

The chatbot recognizes the following financial metrics:  
✔ Total Revenue  
✔ Net Income  
✔ Operating Cash Flow  
✔ Total Assets  
✔ Total Liabilities  

---

## 🚀 Installation & Setup

To run this project, install the required Python libraries:

```bash
pip install numpy pandas matplotlib
