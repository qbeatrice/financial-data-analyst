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

```
/sales-data-analyst
│
├── /app               # Next.js application routes and pages
│   ├── /api           # API routes (e.g., /finance, /upload)
│
├── /components        # UI components
├── /lib               # SQL Server connector and helpers
├── /public            # Static assets
├── /scripts           # Sample SQL table creation and data
├── /utils             # Vega-Lite formatters and JSON utilities
├── .env.local         # Environment variables (not committed)
└── README.md
```

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/sales-data-analyst.git
cd sales-data-analyst
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Set Environment Variables
Create a `.env.local` file:
```bash
cp .env.example .env.local
```

Update `.env.local` with your configuration:
```env
CLAUDE_API_KEY=your_anthropic_api_key
CLAUDE_MODEL=claude-3-sonnet
SQL_SERVER_HOST=your_sql_server_host
SQL_SERVER_USER=your_user
SQL_SERVER_PASSWORD=your_password
SQL_SERVER_DATABASE=your_database
```

### 4. Run the App
```bash
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000) in your browser.

## 💡 Example Prompts

- “Show total revenue by product design this quarter.”
- “Upload this sales Excel file and summarize the top 5 performing regions.”
- “Generate a line chart of monthly sales trends.”

## 🧠 How It Works

1. User sends a message or uploads a file.
2. Backend parses the input and gathers data from:
   - SQL Server (via query builder)
   - Uploaded file (parsed to JSON)
3. The Claude API processes the data and prompt to:
   - Generate insights
   - Build visualization specs (Vega-Lite JSON)
4. Results are returned to the user as:
   - Summaries
   - Charts
   - Tables

## 🚀 Future Enhancements

- Add user login and history tracking
- Claude streaming + multi-turn conversations
- Dashboard builder with drag-and-drop charts
