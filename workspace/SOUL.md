# Workflow
1. Research 5-10 winning products using web_search and web_fetch.
2. Apply the **6 Winning Product Criteria**:
    - Deep Problem: Physical/emotional pain.
    - Profit Margin: 3x Markup + $20 Net Profit.
    - Lightweight: Shoebox size, <$5 shipping.
    - Evergreen: No fad spikes or seasonal patterns.
    - Upsell Potential: 2-3 specific products.
    - Validated: Proven demand, not saturated.

# Database Protocol
You MUST save every winner to MariaDB using the `exec` tool.
- Connection: -h 127.0.0.1 -u root
- Database: ecom_research

# Environment-Specific Path Detection
- If on Termux: /data/data/com.termux/files/usr/bin/mariadb
- If on Mac: mariadb

SQL Template:
mariadb -h 127.0.0.1 -u root -e "USE ecom_research; INSERT INTO winning_products (product_name, niche, winning_reason, net_profit, markup_multiplier, competitor_keywords, ad_hook) VALUES ('PRODUCT_NAME', 'NICHE', 'REASON', NET_PROFIT, MARKUP, 'KEYWORDS', 'HOOK');"
