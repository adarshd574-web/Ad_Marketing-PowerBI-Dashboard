# Ad_Marketing-PowerBI-Dashboard
An interactive Power BI dashboard that analyses digital ad campaign performance across platforms, audiences, budgets and the conversion funnel. It helps marketing teams see what is working, where budget is going, and who is engaging.


# Key Questions Answered
- How are impressions, clicks, purchases, CTR, CPC, CPM and CPA trending month over month?
- Which campaigns, ads and platforms deliver the best return?
- How is budget distributed across campaigns, and where are the funding gaps?
- Which audiences, countries and time slots engage the most?
- Where do users drop off in the funnel (impression → click → purchase)?


# What Each Dashboard Pages Shows?

# Page-1:	Executive Overview
Headline KPIs with month-over-month change, plus Instagram / Facebook platform toggles and Bar / Line view switching via bookmarks
# Page-2:	Campaign & Budget Performance
Budget share, cumulative budget %, funding gap %, and ROI proxy by campaign
# Page-3:	Ad, Platform & Funnel Performance	
Ad-level and platform comparison, funnel view, CTR and conversion rate
# Page-4:	Audience & Timing Insights
Engagement by time slot, top countries, interest match and targeting accuracy
# Page-5: Campaign Details (Drill-Through)
Detailed view for a selected campaign
# Page-6:	Demographic Tooltip	
Tooltip page showing demographic breakdowns on hover


# Key Metrics (KPIs & DAX Measures)

Total Impressions · Total Clicks · Total Purchases · Reach · CTR · CPC · CPM · CPA · Conversion Rate · Engagement Rate · Repeat Engagement Rate · Overall ROI Proxy · Adjusted ROI Proxy · Adjusted CPA · Budget Share % · Cumulative Budget % · Funding Gap % · Purchase Share % · Top Country Share % · Interest Match Rate · Targeting Accuracy Rate · Peak Engagement Slot · month-over-month displays for CTR, Conversion Rate, Clicks, Impressions and Purchases


# Data Model
- Campaigns : Campaign details and budgets 
- Ads : Ad-level attributes (platform, type) 
- AdEvents : Event-level interactions (impressions, clicks, likes, comments, shares, purchases) 
- Users : User and demographic attributes (age group, country) 
- AdsInterestsSplit, UsersInterestsSplit : Helper tables that split interests into separate rows for analysis 
- DateTable, MonthIndex : Calendar table and month ordering for time intelligence 
- Measures Table : All DAX measures 
- KPI Selector, Metric Selector, Breakdown Selector : Field parameters for dynamic KPI, metric and breakdown switching 
- Budget Adjustment % : What-if parameter for budget simulation 
- Scenario : Scenario selector table 


## Features

**Dynamic controls and parameters**

- Field parameters: `KPI Selector`, `Metric Selector` and `Breakdown Selector` let users switch the KPI, metric and breakdown (ad platform, ad type, age group, country) from a single visual
- What-if parameter: `Budget Adjustment %` (-50% to +50%, in 5% steps) for budget simulation and scenario analysis
- Scenario selector for comparing different scenarios
- Slicers for filtering across pages

**Interactivity and navigation**
- Page navigation buttons and action buttons
- Bookmark-based view toggles (Bar / Line view, Instagram / Facebook)
- Drill-through to campaign details
- Custom tooltip page for demographic breakdowns

**Analysis and visuals**
- Month-over-month comparisons using previous-month DAX measures (e.g. `Total Clicks PM`, `CTR PM`)
- Funnel, treemap, decomposition tree, map, bubble, scatter, line, donut and combo charts
- KPI cards with custom icons (Flaticon)


# How to Use
- Download ad_marketing_dashboard.pbix from this repository.
- Open it in Power BI Desktop (free, Windows only).
- Use the page navigation buttons, slicers and bookmarks to explore.
- Right-click a campaign and choose Drill through → Campaign Details for a deeper view.


# Tools Used
- Power BI Desktop
- DAX
- Power Query


#  Key Insights
- Best-performing campaign: Campaign_27_Q3 at 8.40% conversion (also lowest CPA at ₹393.52.
- Needs attention: Campaign_43_Winter — ₹81,350 budget, 0.00% conversion (Campaign_16_Winter is a close second: ₹71,522 budget, also 0.00%).
- Biggest funnel leak: Click → Purchase. Impression → Click drops 88% (340K→ 40K), but Click → Purchase drops steeper at 95% (40K→2K) 
- Platform volume split: Facebook leads on reach (216K vs. 124K impressions) and performs better — CTR 11.86% vs. 11.76%, Conversion Rate 5.21% vs. 4.82%.  Instagram is both smaller and less efficient here, so consider shifting more budget toward Facebook.
- Best ad type:  Stories — highest CTR and highest conversion rate on the Ad Type Performance chart; both decline steadily down to Image, the weakest.
- Best-converting audience (age/gender/country) : 45-54 Male is the strongest reliable segment — high conversion rate on a large base (188K impressions). 55-65 "Other" shows an even higher rate, but on a much smaller audience (34.5K impressions, about a fifth of Male's volume) 
- Best day/time: Monday Evening, with a peak engagement rate of 5.90 %


  ## Data Source
https://www.kaggle.com/datasets/alperenmyung/social-media-advertisement-performance

Social Media Advertisement Performance dataset from Kaggle. The data is synthetic, so the insights above illustrate the analysis rather than real-world results. Helper tables (interest splits, date and month index, parameters and selectors) were created in Power BI.
