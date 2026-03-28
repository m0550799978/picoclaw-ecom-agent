# 🦞 PicoClaw Ecom-Researcher Agent (Termux/Mobile Edition)

A professional-grade AI Agent workspace for [PicoClaw](https://github.com/sipeed/picoclaw). This agent is specialized in high-intent e-commerce product research, specifically optimized to run on Android devices via **Termux** using minimal resources while maintaining a permanent MariaDB database of findings.

## 🚀 Features
- **6-Criteria Protocol**: Strict filtering based on Deep Pain, 3x Margin Greenzone, Weight, Evergreen Demand, Upsell Potential, and Market Validation.
- **Native SQL Integration**: Uses the direct MariaDB binary via the `exec` tool to bypass heavy Node.js MCP overhead.
- **Autonomous Research**: Uses `web_search` and `web_fetch` to analyze TikTok, Amazon reviews, and Google Trends.
- **Persistent Memory**: Saves every winning product into a structured SQL table for future scaling.

---

## 🛠 Prerequisites

Before deployment, ensure your Termux/Proot environment has the following installed:
- **MariaDB**: `apt update && apt install mariadb -y`
- **PicoClaw CLI**: Installed and configured with a valid LLM API key (GPT-4o recommended).

---

## 💾 MariaDB Database Setup

The agent requires a local database to store research results. Run these commands in your terminal to initialize the environment:

### 1. Initialize and Start the Server
```bash
# Initialize data folders (Run once)
mysql_install_db

# Start the database server in the background
mysqld_safe --user=root &
```

### 2. Create the Schema
Log in using mariadb -u root and execute the following SQL command:
```bash
SQL
CREATE DATABASE IF NOT EXISTS ecom_research;
USE ecom_research;

CREATE TABLE IF NOT EXISTS winning_products (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(255) NOT NULL,
    niche VARCHAR(100),
    winning_reason TEXT,
    net_profit DECIMAL(10, 2),
    markup_multiplier DECIMAL(5, 2),
    competitor_keywords TEXT,
    ad_hook TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

📂 Workspace Configuration
The core logic is stored in the ecom_search_workplace/ directory.
IDENTITY.md
Defines the agent as an elite expert with 20+ years of experience in identifying 7-figure products through viral social media trends.
SOUL.md
Contains the 6-Criteria Research Protocol:
Deep Problem: Solves a significant physical or emotional pain point.
Profit Margin: Minimum 3x Markup + $20 Net Profit per sale.
Lightweight: Fits in a shoebox, shipping costs < $5.
Evergreen: Verified 5-year steady demand via Google Trends.
Upsell Potential: 2-3 natural cross-sell opportunities.
Validated: High viral momentum but low market saturation.
🚀 Execution
To run the agent with this specialized workspace, navigate to the repository root and execute:

```Bash
PICOCLAW_AGENTS_DEFAULTS_WORKSPACE=$(pwd)/ecom_search_workplace picoclaw agent
```

## Recommended Test Command
Once the agent starts, verify the setup by asking:

"Research 1 winning product in the Electronics niche. Apply the 6-criteria protocol and save the results to our MariaDB database using the native binary path /data/data/com.termux/files/usr/bin/mariadb."
📊 Profit Formula Logic
The agent is hardcoded to perform the following calculation before approving a product:
Gross Profit: Sell Price - Supplier Cost
Ad Spend: 20% of Revenue
Fees: 5% (Processing/Shopify)
Returns/CS: 5%
Success Condition: Net Profit must be >$20.00 per unit.
⚠️ Mobile Optimization Note
This workspace uses the exec tool to call the mariadb binary directly. This is a Best Practice for mobile devices as it prevents "Out of Memory" crashes commonly caused by running secondary Node.js/MCP server processes.
Created by m0550799978 for the PicoClaw community.
