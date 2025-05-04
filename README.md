# Sales Data Analyst Agent

This project is an intelligent data analyst agent powered by **Claude API (Anthropic)**. It allows users to ask natural language questions and receive insights or visualizations derived from a connected SQL Server database or uploaded files.

## 🔍 Features

- Connects to a SQL Server database with the following tables:
  - `sales_data`
  - `product_design`
  - `vehicle_master`
- Accepts file uploads (CSV, Excel) for ad hoc analysis.
- Supports:
  - Natural language queries
  - Tabular insights
  - Vega-Lite JSON visualizations
- Uses **Claude API** to generate analysis, summarize findings, and interpret business data.

## 🛠 Tech Stack

- **Frontend**: Next.js (React)
- **Backend**: Node.js with API routes
- **Database**: Microsoft SQL Server
- **AI Engine**: Claude 3 (via Anthropic API)
- **Visualization**: Vega-Lite (JSON-based chart rendering)

## 📂 Folder Structure

