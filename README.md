# CUSTOMER COMPLAINTS ANALYSIS


[![LinkedIn](https://img.shields.io/badge/LinkedIn-Post-blue)](https://www.linkedin.com/posts/eromosele-itoya_tableau-datavisualization-customerexperience-activity-7378500174664597504-TF4Y?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEbDOGsBGINDr5uoWo3fkmNHZc_HI1Qst6k)

### Table of Contents
- [Project Overview](#Project-Overview)
- [Tools](#Tools)
- [Workflow](#Workflow)
- [Insights](#Insights)
- [Recommendations](#Recommendations)
- [Strategic Goals](#Strategic-Goals)
- [Dashboard](#Dashboard)

### Project Overview
This project explores CFPB consumer complaint data from 2011-2020, analyzing 72,431 banking-related entries to identify trends in products, submission channels, timelines, and geographies. Using Tableau, I crafted an interactive dashboard that empowers users to filter by year, state, or product for deep dives—e.g., spotting why Cards complaints spiked 15% YoY. Key metrics include total complaints (72K+), resolution rates (up to 37% resolved by 2020), and state distributions (CA leading). Beyond visuals, it's about actionable intel: How can banks cut disputes by targeting high-volume issues like billing errors? This scalable setup could extend to real-time feeds or multi-sector comparisons.

### Tools
- Tableau: For data ingestion, calculated fields (e.g., % of Total), LOD expressions (e.g., fixed yearly trends), parameters for dynamic filtering, and interactive viz (maps, trends, pies).

### Workflow
A structured, iterative build ensured clean data flows into insightful, user-friendly outputs.
#### 1. Data Loading and Cleaning:
- Imported the CSV dataset (~72K rows) into Tableau, covering fields like Complaint ID, Date Received, Issue, Product (e.g., Cards, Mortgages), State, Sub-issue, Submitted via (e.g., Web, Referral).
- Handled nulls/duplicates (e.g., anonymized ZIPs), parsed dates for year/month granularity, and created bins for trends (e.g., quarterly complaints).
- Filtered to focus on key products (Accounts, Cards, etc.) and added flags like "Disputed" (Yes/No) for segmentation.
    
#### 2.	Data Modelling and Processing:
- Used Tableau's data interpreter for quick joins; created relationships via Complaint ID for sub-issue drills.
- Parameters for slicers (e.g., Product dropdown: Cards, Mortgages; Year range: 2011-2020) and dynamic titles (e.g., "Complaints by [Selected Product]").
- Aggregations for KPIs: Total Complaints = COUNTD([Complaint ID]), Avg per Year = AVG([Annual Count]).

#### 3.	Data Analysis & Visualization:
- Designed core visuals: Stacked bars for yearly trends (% resolved/unresolved), pie for request channels, filled map for states (color-coded by volume), line chart for year-over-year growth.
- Added interactivity: Action filters for state drills (e.g., click CA → filter sub-issues), tooltips with details (e.g., "Top Issue: Billing Disputes – 12K cases"), and legends for product breakdowns.
- Enhancements: Conditional formatting (red for high unresolved), heatmaps for state density, and export options for raw slices.

#### 4. Dashboard Assembly:
- Single-page layout for simplicity: Top KPIs, product matrix, trends chart, state map, channel pie, and detail table.
- Tested cross-filters (e.g., select "Web" → updates all metrics) and performance (blended data for speed).
- Polished with custom colors (blues for resolved, grays for totals), icons, and navigation tooltips.

### Insights
Data-driven highlights, each tied to visuals for easy validation.
#### 1. Overall Performance:
Total Complaints: 72,431 | Peak Year: 2019 (3,567) | Avg Annual: 7,243 | Resolution Improvement: From 0% (2011) to 37% (2020).
Growth: +95% from 2012 baseline, with a 23% 2020 drop—economic recovery signal?

<img width="243" height="115" alt="Screenshot 2025-09-29 193518" src="https://github.com/user-attachments/assets/cb20b750-9d38-4aa3-a425-8bd779d52eff" />

#### 2. Product Breakdown
Cards: 28,557 (39.43%, $583K equiv. impact if monetized) | Accounts: 21,882 (30.21%) | Mortgages: 11,918 (16.45%).
Lending underperforms at 4.16% but shows volatility—early warning for policy tweaks?

<img width="1451" height="204" alt="Screenshot 2025-09-29 193500" src="https://github.com/user-attachments/assets/7d4de6c9-53ae-4178-9a4d-f6fd2e8f00cd" />

#### 3. Request Channels
Referrals: 42.9% (31,049) | Web: 37.8% (27,379) | Phone: 14.7% (10,647).
Digital dominance (80%+ combined) vs. legacy (Fax/Email <2%)—streamline online portals?

<img width="1503" height="784" alt="Screenshot 2025-09-29 195600" src="https://github.com/user-attachments/assets/12566b11-108a-434e-8258-575bf0fd2344" />
<img width="1503" height="786" alt="Screenshot 2025-09-29 195545" src="https://github.com/user-attachments/assets/420170e5-5b9a-4515-8122-e0fe04c2e72b" />
<img width="1502" height="790" alt="Screenshot 2025-09-29 195635" src="https://github.com/user-attachments/assets/dd66803d-6549-4cd6-a3de-b8ff9d0849ec" />
<img width="1505" height="790" alt="Screenshot 2025-09-29 195622" src="https://github.com/user-attachments/assets/617ac76d-eeac-4f90-9a29-85300e83be0a" />
<img width="1497" height="792" alt="Screenshot 2025-09-29 195610" src="https://github.com/user-attachments/assets/0b11d227-a7aa-4a00-a751-54163fa3fb21" />


#### 4. Time Trends

Steady climb to 2019 peak, then decline; unresolved % halved over decade.
Quarterly patterns: Q4 surges in Mortgages (holiday stress?).

<img width="1498" height="791" alt="Screenshot 2025-09-29 200004" src="https://github.com/user-attachments/assets/8df76dfe-91c6-4e0f-86e0-50d625e0a904" />
<img width="1503" height="793" alt="Screenshot 2025-09-29 200051" src="https://github.com/user-attachments/assets/fd334ece-ff97-4570-b7ba-a52fb30a8034" />
<img width="1508" height="797" alt="Screenshot 2025-09-29 200039" src="https://github.com/user-attachments/assets/b1f06924-ca7e-48cc-94a3-7abc07a06a70" />
<img width="1505" height="795" alt="Screenshot 2025-09-29 200027" src="https://github.com/user-attachments/assets/3860dba5-8de3-40b3-9545-607fe2796012" />
<img width="1502" height="792" alt="Screenshot 2025-09-29 200015" src="https://github.com/user-attachments/assets/25ff9883-2891-4b49-b541-7fffca7ba05d" />

#### 5. State Insights
Top: CA (434), TX (325), FL (257), NY (241) | Lowest: WY (<10).
Density heatmap flags urban clusters—CA's 0.6% of total but 5x national avg per capita.

<img width="1301" height="715" alt="Screenshot 2025-09-29 200304" src="https://github.com/user-attachments/assets/5a85abdc-29bf-4801-b034-d4d325eca311" />

#### 6. Granular Details
Top Issues: "Billing Disputes" (Cards, 18K), "Account Management" (Accounts, 12K).
Disputed Cases: 15% overall (10,865), highest in Mortgages (22%).

### Recommendations
From the patterns:
- Prioritize Cards: Automate billing resolutions to cut 20% of volume.
- Go Digital: Invest in Web/Referral tools—could reduce Phone backlog by 50%.
- Regional Focus: Tailor state campaigns (e.g., CA mortgage workshops).
- Trend Monitoring: Add alerts for >10% YoY spikes; integrate sentiment analysis.
- Data Expansion: Blend with response times for full lifecycle views.

### Strategic Goals
- Reduce complaint volume 15-25% via proactive fixes, lifting CSAT scores.
- Enable faster decisions: Dashboard cuts analysis time from days to minutes.
- Scale for sectors: Adapt for retail/healthcare complaints.
- Foster CX culture: Train teams on geo-trends for localized service.

### Dashboard
- ####  Overview Analysis:
<img width="1486" height="841" alt="Screenshot 2025-09-29 200457" src="https://github.com/user-attachments/assets/20a51196-93ae-47ca-98c1-6c0c62cabf19" />
<img width="1489" height="841" alt="Screenshot 2025-09-29 200509" src="https://github.com/user-attachments/assets/5e7a59c3-9be3-44f9-9326-988173f67289" />

## Connect with Me 👋
[LinkedIn](https://www.linkedin.com/in/eromosele-itoya/) | 
[GitHub](https://github.com/youngdrizzy1)
