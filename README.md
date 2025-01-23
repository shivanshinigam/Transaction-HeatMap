# Transaction HeatMap

Transaction Map is a data visualization tool that provides an intuitive heatmap representation of daily transaction data. By grouping transactions by date and analyzing net balances, users can easily identify trends, outliers, and patterns in their financial activity.

---

## Key Features

### 🔍 **Heatmap Visualization**
- Displays daily net transactions as colored cells.
- Shades of **green** represent positive net balances (credits dominate).
- Shades of **red** represent negative net balances (debits dominate).
- Intensity of the color varies based on the magnitude of the balance.

### 🗂️ **Data Grouping by Date**
- Automatically organizes transactions into groups based on their date.
- Enables seamless aggregation and streamlined analysis.

### 📊 **Dynamic Calculations**
- Computes **net transaction values** (credits - debits) for each day.
- Categorizes values into meaningful ranges to ensure insightful visualization.

### 🎨 **Interactive Design**
- Includes hoverable tooltips for additional insights into daily transaction details.
- Customizable cell colors to match different thematic designs.

---

## How It Works

### 1. **Input Data**
The application expects transaction data in the following format:
json
[
  
    "date": "YYYY-MM-DD",
    "transactionType": "credit" | "debit",
    "amount": Number
  
]

## Data Processing
Grouping by Date: Transactions are grouped by their date using the groupByDate utility.
Net Transaction Calculation: For each date group, the net transaction amount is calculated using getNetTransactions.
Heatmap Coloring: Each day's net amount determines the heatmap cell color via getHeatmapCellColor.


## Visualization
The data is displayed in a heatmap format.
Tooltips provide detailed information about the day's transactions

🦾Customization
Update Heatmap Color Ranges
To modify the thresholds or colors for the heatmap:

Open transactionUtils.js.
Edit the ranges in the getHeatmapCellColor function.
Adjust corresponding CSS classes in App.css.

