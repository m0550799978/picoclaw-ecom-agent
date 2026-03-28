# Workflow
Step 1: Ask the user to choose ONE niche:
- Fashion & Apparel
- Pets
- Electronics & Gadgets
- Home & Garden
- Fitness & Sports
- Beauty & Personal Care
- Not sure…
If they respond: "not sure" continue with the research and just do it broadly.

Step 2: Research 5-10 winning products by:
- Analyzing viral momentum (TikTok, Instagram Reels, Reddit, Meta Ad Library)
- Mining customer reviews for pain points and gaps
- Evaluating competitor products for market opportunities
- Verifying evergreen demand via Google Trends (5-10 year view)
- Confirming profit margins and shipping costs
- Searching AutoDS and AliExpress for actual product listings
- Verifying each link works before including it

# 6 Winning Product Criteria (ALL Required)
1. Deep Problem (Physical or Emotional Pain): Solves physical pain (back pain, joint pain, body discomfort) OR emotional pain (confidence issues, self-image, pet-related distress). Must affect daily life significantly enough that customers actively seek solutions and pay premium prices. Validate by checking if reviews mention "desperate," "finally," or "life-changing."
2. Profit Margin "Greenzone" (3x Markup + $20 Net Profit): Must sell for at least 3x supplier cost with $20+ remaining after ALL costs (ads, fees, returns). Example: $15 cost → $45+ sell price. Use the profit formula below to calculate exact net profit.
3. Lightweight (Low Shipping Costs): Fits in shoebox or smaller. Keeps shipping under $5. Heavy products (furniture, car parts, appliances) destroy margins. Validate with product dimensions and weight specifications.
4. Evergreen (Year-Round Demand): Sells consistently throughout the year, not seasonal. Google Trends must show steady or increasing demand over 5+ years with no fad spikes (like fidget spinners) or seasonal patterns (like beach toys).
5. Upsell Potential (Cross-Sell Opportunities): Natural opportunities to increase customer lifetime value through complementary products. Example: blue light glasses + case + cleaning kit. List 2-3 specific upsell products for each recommendation.
6. Validated But Not Oversaturated: Provide specific competitor research keywords for each product. User will manually verify: competitors doing $100k+/mo, ads running 7+ days, new angles being tested, and ability to create better content or hit different audiences.

# Profit Breakdown Formula
Use this exact calculation for every product:
- Supplier Cost: Actual AutoDS/AliExpress price
- Sell Price: 3x supplier cost minimum
- Gross Profit: Sell price - supplier cost
- Deduct Costs:
  - Ad spend: 20% of revenue (sell price)
  - Payment processing + Shopify: 5% of revenue
  - Returns/refunds/CS: 5% of revenue
- Net Profit: Must be $20+ per sale

Example Calculation:
Cost: $15 | Sell: $49 | Gross: $34
Ad spend (20%): -$9.80 | Processing (5%): -$2.45 | Returns (5%): -$2.45
Net Profit: $19.30 ❌ (Under $20 - reject this product)

# Output Format
Present each product using this structure:
Product #[Number]: [Product Name]
**Why It's A Winner:**
[3-5 sentences covering: (1) specific customer pain point or emotional need, (2) current viral trend or social media buzz with specific data, (3) evidence from competitor analysis, (4) why customers will pay premium, (5) shipping/perceived value]

**Criteria Validation:**
- Deep Problem: [One sentence explanation]
- Profit Margin: [One sentence confirming 3x markup and $20+ net profit]
- Lightweight: [One sentence confirming size/weight]
- Evergreen: [One sentence with Google Trends data]
- Upsell Potential: [One sentence listing 2-3 products]
- Validation: [Estimated only - use research keywords below]

**Profit Breakdown:**
*Note: These are estimated calculations based on typical costs. Actual numbers will vary.* 
Cost: X | Sell: $X | Gross: $X | Ad spend (20%): -X | Processing (5%): -X | Returns (5%): -X | **Net Profit: $X**

**Competitor Research:**
- Search Terms: [5-10 terms]
- Hashtags: [5-10 hashtags]

**Ad Angle/Hook:**
[Specific, actionable hook for FB/TikTok ads]

---

# Formatting Rules
- Bold all section labels.
- Use line breaks between each section.
- "Why It's A Winner" must be 60-100 words with specific data points.
- Each criteria validation point must be exactly one sentence.
- Include complete profit calculation showing all deductions.
- Use web_search and web_fetch tools to find actual working product information.

# Example for reference
Product #1: Posture Corrector Back Brace
Why It's A Winner: Remote work epidemic created chronic back pain affecting 15M+ people with over 15,000 Amazon reviews mentioning "desperate for relief." #posturecorrector has 45M+ TikTok views with influencers showing dramatic before/after transformations. Competitor reviews average 3-stars with complaints about "uncomfortable straps" and "cheap materials" - this breathable, adjustable version solves those gaps. Customers pay $35-50 for immediate pain relief and confidence boost (emotional need: looking better, feeling better). Weighs 8oz, ships for $3-4 with 400%+ markup potential.
Criteria Validation:
Deep Problem: Solves chronic back pain (physical) and poor posture confidence issues (emotional) affecting remote workers daily
Profit Margin: 4.8x markup with calculations confirming $20+ net profit after all costs - ESTIMATE ONLY
Lightweight: Under 8oz, fits in small mailer, shipping costs only $3-4
Evergreen: Google Trends shows steady 5-year growth for "posture corrector" with no seasonal dips
Upsell Potential: Natural upsells include lumbar support cushion, resistance bands, posture reminder app
Validation: Estimated only - use research keywords below to check validation following steps given in video
Profit Breakdown:
 Note: These are estimated calculations based on typical costs. Actual numbers will vary. Cost: $8 | Sell: $39 | Gross: $31 | Ad spend (20%): -$7.80 | Processing (5%): -$1.95 | Returns (5%): -$1.95 | Net Profit: $19.30 ❌ Need to increase sell price to $42+ or reduce costs
Competitor Research:
Search Terms: posture corrector, back brace, posture support, spine alignment, back pain relief, adjustable back brace, breathable posture corrector, posture fix
Hashtags: #posturecorrector, #backpainrelief, #posturetok, #wfhposture, #backpain, #posturecheck, #spinehealth, #posturesupport
Ad Angle/Hook: "POV: You've been working from home for 3 years and your back is screaming for help. This $39 brace fixed my posture in 2 weeks."

Final Deliverable: Provide 5-10 products ranked by opportunity.

# 🛑 MANDATORY DATABASE RULES (STRICT)
1. **Database Name**: You MUST ONLY use `ecom_research`. Never create a new database.
2. **Table Name**: You MUST ONLY use `winning_products`.
3. **Forbidden Actions**: Never run `CREATE DATABASE`. I have already created it for you.
4. **Schema Enforcement**: You MUST map your findings to these EXACT columns:
   - `product_name` (Name of item)
   - `niche` (Category)
   - `winning_reason` (Max 250 characters summary)
   - `net_profit` (Numerical decimal)
   - `markup_multiplier` (Numerical decimal)
   - `competitor_keywords` (Comma separated string)
   - `ad_hook` (The marketing angle)

# Storage Command Template
/data/data/com.termux/files/usr/bin/mariadb -h 127.0.0.1 -u root -e "USE ecom_research; INSERT INTO winning_products (product_name, niche, winning_reason, net_profit, markup_multiplier, competitor_keywords, ad_hook) VALUES ('...', '...', '...', ..., ..., '...', '...');"


# 🛡️ SQL ESCAPING SAFETY RULE
When using `exec` to run MariaDB commands:
1. Always wrap the entire SQL query in double quotes `"..."`.
2. Inside the SQL, replace any single quotes in text (e.g., "here's") with a space or a double-single-quote ('' ) to prevent syntax errors.
3. If the data is complex, continue using the "write to temp_insert.sql" method as it is the most stable for your phone's memory.
