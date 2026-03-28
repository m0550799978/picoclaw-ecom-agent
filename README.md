# 🦞 PicoClaw Ecom-Researcher Agent

A specialized workspace for identifying viral dropshipping products using PicoClaw. Optimized for Termux/Android environments.

## 📂 Structure
- `ecom_search_workplace/`: Contains the Identity and Soul of the expert agent.
- `winning_products`: MariaDB table for permanent storage.

## 🛠 MariaDB Setup (Termux/Mobile)
Before running the agent, you must initialize and configure your database:

1. **Install MariaDB**:
   ```bash
   apt update && apt install mariadb -y
Initialize Database Folders:
code
Bash
mysql_install_db
Start the Database Server:
code
Bash
mysqld_safe --user=root &
Create Database and Tables:
Log in using mariadb -u root and run:
code
SQL
CREATE DATABASE IF NOT EXISTS ecom_research;
USE ecom_research;

CREATE TABLE IF NOT EXISTS winning_products (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(255),
    niche VARCHAR(100),
    winning_reason TEXT,
    net_profit DECIMAL(10, 2),
    markup_multiplier DECIMAL(5, 2),
    competitor_keywords TEXT,
    ad_hook TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
🚀 Execution
Run the agent from the root of this repository:
code
Bash
PICOCLAW_AGENTS_DEFAULTS_WORKSPACE=$(pwd)/ecom_search_workplace picoclaw agent
🧠 Research Protocol
The agent follows a strict 6-Criteria Protocol:
Deep Problem (Physical/Emotional)
Profit Margin Greenzone (3x Markup + $20 Net Profit)
Lightweight (Low Shipping)
Evergreen (Year-Round Demand)
Upsell Potential
Validated but Not Saturated
