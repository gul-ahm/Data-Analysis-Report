# Data-Analysis-Report
# 📊 WT Partnership — Construction Data Analysis (20 Problems)

> **Prepared by:** Gulzar | Data Analyst | Construction-Tech Domain  
> Every figure below is a live formula referencing the source sheets. Update source data and answers refresh automatically.

---

## 📑 Table of Contents

| # | Problem | Domain | Sheet | Rows |
|---|---------|--------|-------|------|
| 01 | [Project Cost Overrun Analysis](#problem-01--project-cost-overrun-analysis) | Cost Management | P01-CostOverrun | 50 |
| 02 | [Material Price Fluctuation Tracker](#problem-02--material-price-fluctuation-tracker) | Procurement | P02-MaterialPrice | 90 |
| 03 | [BOQ Variance Analysis](#problem-03--boq-variance-analysis) | Quantity Surveying | P03-BOQVariance | 60 |
| 04 | [Labour Productivity by Trade](#problem-04--labour-productivity-by-trade) | Resource Management | P04-LabourProd | 80 |
| 05 | [Tender Bid Comparison](#problem-05--tender-bid-comparison) | Commercial | P05-TenderBid | 40 |
| 06 | [Project Delay Root Cause](#problem-06--project-delay-root-cause-analysis) | Project Management | P06-DelayRCA | 60 |
| 07 | [Monthly Cash Flow Tracking](#problem-07--monthly-cash-flow-tracking) | Financial Management | P07-CashFlow | 48 |
| 08 | [Change Order Impact Analysis](#problem-08--change-order-vo-impact-analysis) | Contract Management | P08-ChangeOrder | 45 |
| 09 | [Subcontractor Performance Scorecard](#problem-09--subcontractor-performance-scorecard) | Vendor Management | P09-SubconScore | 30 |
| 10 | [Construction Cost Benchmarking](#problem-10--construction-cost-benchmarking) | Cost Intelligence | P10-Benchmark | 40 |
| 12 | [Earned Value Management (EVM)](#problem-12--earned-value-management-evm) | Project Controls | P12-EVM | 36 |
| 13 | [Procurement Lead Time Analysis](#problem-13--procurement-lead-time-analysis) | Supply Chain | P13-LeadTime | 50 |
| 14 | [Client Payment Aging Tracker](#problem-14--client-payment-aging-tracker) | Accounts Receivable | P14-PaymentAging | 40 |
| 15 | [Multi-Project Portfolio Dashboard](#problem-15--multi-project-portfolio-dashboard) | Portfolio Management | P15-Portfolio | 25 |

> **Note:** Problems 11 and 16–20 have no data sheet in this workbook.

---

## Problem 01 — Project Cost Overrun Analysis

**Source sheet:** `P01-CostOverrun` (50 projects)

### Q1. Which country has the highest average cost overrun percentage?

| Country | Avg Overrun % | Projects | Total Budget (USD) | Total Actual (USD) | Portfolio Overrun % |
|---------|--------------|----------|-------------------|-------------------|-------------------|
| Australia | 16.7% | 15 | 690,300,200 | 826,447,969 | 19.7% |
| India | 15.8% | 28 | 1,171,274,510 | 1,361,321,621 | 16.2% |
| New Zealand | 19.7% | 7 | 290,824,343 | 344,177,656 | 18.3% |

**Answer:** New Zealand has the highest average cost overrun at **19.7%**, vs India the lowest at 15.8%.

### Q2. Total budget vs actual cost by project type — which type has the worst variance?

| Project Type | Total Budget (USD) | Total Actual (USD) | Variance (USD) | Variance % | Projects |
|-------------|-------------------|-------------------|----------------|-----------|----------|
| Residential Tower | 238,232,594 | 300,895,518 | 62,662,924 | **26.3%** | 4 |
| Hospital | 202,218,749 | 252,196,787 | 49,978,038 | 24.7% | 5 |
| IT Park | 207,257,585 | 251,957,838 | 44,700,253 | 21.6% | 7 |
| University Campus | 304,580,669 | 370,758,337 | 66,177,668 | 21.7% | 6 |
| Industrial Warehouse | 162,936,980 | 186,876,390 | 23,939,410 | 14.7% | 3 |
| Commercial Office | 139,292,114 | 159,577,657 | 20,285,543 | 14.6% | 3 |
| Hotel | 276,402,274 | 314,328,476 | 37,926,202 | 13.7% | 7 |
| Metro Station | 194,389,591 | 220,692,772 | 26,303,181 | 13.5% | 5 |
| Data Centre | 377,404,871 | 423,300,399 | 45,895,528 | 12.2% | 9 |
| Shopping Mall | 49,683,626 | 51,363,072 | 1,679,446 | 3.4% | 1 |
| **TOTAL** | **2,152,399,053** | **2,531,947,246** | **379,548,193** | **17.6%** | **50** |

**Answer:** Worst variance = **Residential Tower at 26.3%** ($62,662,924 over budget). Best = Shopping Mall at 3.4%.

### Q3. Top 5 projects with the highest absolute cost overrun (USD)

| Rank | Project ID | Project Name | Type | Overrun (USD) | Overrun % |
|------|-----------|-------------|------|--------------|----------|
| 1 | WT-1028 | Residential Tower Per-29 | Residential Tower | 24,654,239 | 33.1% |
| 2 | WT-1032 | Residential Tower Hyd-33 | Residential Tower | 21,628,203 | 32.9% |
| 3 | WT-1033 | IT Park Syd-34 | IT Park | 19,739,335 | 33.6% |
| 4 | WT-1034 | University Campus Kol-35 | University Campus | 19,335,358 | 34.8% |
| 5 | WT-1043 | Industrial Warehouse Can-44 | Industrial Warehouse | 19,116,067 | 29.6% |

**Answer:** Largest single overrun is **WT-1028 at $24,654,239** (33.1%). Top 5 together: $104,473,202.

### Q4. Correlation — project duration vs cost overrun?

**r = -0.156** — effectively no linear relationship; duration does not explain cost overrun in this portfolio.

### Q5. Average overrun % by Country × Project Type

**Answer:** Highest average overrun combination is **Hospital in New Zealand at 29.9%**. Portfolio average overrun is 16.6%.

### Q6. Under budget vs over budget split

| Category | Projects | % of Portfolio |
|---------|----------|---------------|
| Over budget (variance > 0) | 45 | **90.0%** |
| Under budget (variance < 0) | 5 | 10.0% |

### Q7. Most cost-efficient city

**Answer:** **Gold Coast** is the most cost-efficient city (avg overrun -3.0%), while **Sydney** is the least efficient (33.6%). Note: small samples per city.

---

## Problem 02 — Material Price Fluctuation Tracker

**Source sheet:** `P02-MaterialPrice` (90 records, 15 materials, 18 months)

### Q1. Which material has the highest average price increase?

| Material | Unit | Avg Price Change % | Data Points |
|----------|------|--------------------|-------------|
| RMC M30 | cum | **14.8%** | 4 |
| Aggregate (20mm) | cum | 14.6% | 5 |
| Cement (OPC 53) | MT | 11.9% | 6 |
| Aluminium Facade | sqm | 11.7% | 8 |
| MS Pipes | m | 9.9% | 4 |
| Sand (River) | cum | 9.5% | 4 |
| Plywood (Marine) | sheet | 9.3% | 6 |
| Tiles (Vitrified) | sqm | 8.4% | 6 |
| Bricks (AAC) | 1000 nos | 7.7% | 6 |
| Structural Steel | MT | 7.0% | 6 |
| Glass (DGU) | sqm | 4.4% | 8 |
| TMT Steel (Fe500) | MT | 3.9% | 4 |
| PVC Conduits | m | 3.0% | 8 |
| Waterproofing Membrane | sqm | 2.5% | 10 |
| Copper Wiring | m | 1.9% | 5 |

**Answer:** RMC M30 shows the highest average price increase at **14.8%**; the lowest is Copper Wiring at 1.9%.

### Q3. Most volatile country for material pricing

| Country | Std Dev of Price Change % | Avg Price Change % | Data Points |
|---------|--------------------------|-------------------|-------------|
| **India** | **9.8%** | 7.1% | 39 |
| Australia | 9.2% | 7.9% | 33 |
| New Zealand | 9.0% | 7.9% | 18 |

### Q4. Top 3 materials flagged as procurement risk (avg change approaching 15%)

| Rank | Material | Avg Price Change % | Flag |
|------|----------|-------------------|------|
| 1 | RMC M30 | 14.8% | ⚠️ Monitor |
| 2 | Aggregate (20mm) | 14.6% | ⚠️ Monitor |
| 3 | Cement (OPC 53) | 11.9% | ⚠️ Monitor |

### Q6. Projected cost of 500 MT TMT Steel next quarter

- **Trend slope:** -$1.90/MT per month
- **Projected price:** $658/MT
- **Projected procurement cost:** $329,166 (vs $347,955 at latest observed price)

---

## Problem 03 — BOQ Variance Analysis

**Source sheet:** `P03-BOQVariance` (72 BOQ line items, 3 projects)

### Q1. Highest total BOQ variance by project

| Project ID | Total BOQ (USD) | Total Actual (USD) | Variance (USD) | Variance % |
|-----------|----------------|-------------------|----------------|-----------|
| **WT-OFF-SYD-02** | 5,691,800 | 6,408,710 | **716,910** | **12.6%** |
| WT-HOS-AKL-03 | 4,619,528 | 5,117,552 | 498,024 | 10.8% |
| WT-DC-MUM-01 | 5,686,240 | 6,061,895 | 375,655 | 6.6% |
| **TOTAL** | **15,997,568** | **17,588,157** | **1,590,589** | **9.9%** |

### Q2. Trade consistently exceeding BOQ across all 3 projects

**Answer:** **MEP - Electrical** is the worst offender — average quantity variance of 11.1% and over BOQ in 3 of 3 projects. 4 of 5 trades exceed BOQ in all three projects.

### Q3. Top 5 BOQ items with highest quantity variance

| Rank | Project | Trade | BOQ Item | Qty Variance % | Impact (USD) |
|------|---------|-------|----------|---------------|-------------|
| 1 | WT-HOS-AKL-03 | Civil & Structure | Plastering | 28.9% | 151,508 |
| 2 | WT-OFF-SYD-02 | MEP - Electrical | LT Panels | 28.4% | 70,934 |
| 3 | WT-DC-MUM-01 | Civil & Structure | Excavation | 27.7% | 131,440 |
| 4 | WT-HOS-AKL-03 | MEP - Electrical | Conduit Laying | 27.7% | 27,899 |
| 5 | WT-HOS-AKL-03 | Interior Fit-out | False Ceiling | 27.6% | 10,834 |

### Q4. Financial impact of quantity overruns

| Project | Overrun (USD) | Savings (USD) | Net Impact (USD) |
|---------|-------------|--------------|-----------------|
| WT-OFF-SYD-02 | 768,548 | -51,638 | **716,910** |
| WT-HOS-AKL-03 | 557,911 | -59,887 | 498,024 |
| WT-DC-MUM-01 | 502,033 | -126,378 | 375,655 |
| **TOTAL** | **1,828,491** | **-237,902** | **1,590,589** |

---

## Problem 04 — Labour Productivity by Trade

**Source sheet:** `P04-LabourProd` (80 daily records, 4 projects)

### Q1. Average productivity per man-hour by trade

| Trade | Avg Productivity/man-hour | Records |
|-------|--------------------------|---------|
| **Civil & Structure** | **3.54** | 13 |
| Interior Fit-out | 3.43 | 15 |
| Facade & Cladding | 3.10 | 13 |
| MEP - Electrical | 3.01 | 13 |
| MEP - HVAC | 2.83 | 12 |
| MEP - Plumbing | 2.23 | 14 |

### Q2. India vs Australia productivity

| Country | Projects | Avg Productivity/man-hour |
|---------|----------|--------------------------|
| India | 2 | **3.25** |
| Australia | 1 | 3.05 |
| New Zealand | 1 | 2.56 |

**Answer:** India is 6.5% more productive than Australia on this sample.

### Q5. Optimal crew size for Civil & Structure

**Answer:** **Medium crew (11–15 workers)** delivers the best productivity at 4.16 units/man-hour.

### Q6. Total man-hours by project

| Project | Total Man-hours | Avg Productivity |
|---------|----------------|-----------------|
| WT-DC-MUM-01 | 4,631 | 3.19 |
| WT-HOS-AKL-03 | 4,101 | 2.56 |
| WT-ITP-BLR-04 | 3,509 | 3.32 |
| WT-OFF-SYD-02 | 3,201 | 3.05 |

---

## Problem 05 — Tender Bid Comparison

**Source sheet:** `P05-TenderBid` (40 bids, 5 packages, 13 contractors)

### Q1. Award recommendations (lowest bid vs best scored)

| Package | Lowest Bidder | Lowest Bid (USD) | Best-Scored Bidder | Score | Quality Premium (USD) |
|---------|-------------|-----------------|-------------------|-------|---------------------|
| Structural Works | Contractor-D | 3,366,658 | Contractor-D | 80.4 | 859,550 |
| MEP Package | Contractor-O | 1,360,585 | Contractor-N | 65.3 | 303,692 |
| Facade & Glazing | Contractor-M | 2,916,771 | Contractor-I | 76.8 | 423,169 |
| Interior Fit-out | Contractor-M | 1,631,225 | Contractor-M | 91.3 | 0 |
| Landscaping | Contractor-H | 855,300 | Contractor-H | 81.6 | 0 |

### Q4. HIGH RISK contractors (Safety < 3.5 AND Defect Rate > 8%)

| Contractor | Package | Bid (USD) | Safety | Defect % | Flag |
|-----------|---------|----------|--------|---------|------|
| Contractor-M | Structural Works | 7,079,774 | 3.4 | 11.4% | 🔴 HIGH RISK |
| Contractor-O | MEP Package | 1,360,585 | 3.2 | 9.3% | 🔴 HIGH RISK |
| Contractor-O | MEP Package | 4,806,314 | 2.7 | 11.0% | 🔴 HIGH RISK |
| Contractor-F | MEP Package | 7,138,581 | 2.6 | 11.1% | 🔴 HIGH RISK |

### Q5. Total project cost comparison

| Strategy | Total Cost (USD) | Avg Score |
|---------|-----------------|-----------|
| Award to lowest bidder | 10,130,539 | 76.0 |
| Award to highest-scored | 11,716,950 | 79.1 |

**Premium for quality:** $1,586,411 (15.7%)

---

## Problem 06 — Project Delay Root Cause Analysis

**Source sheet:** `P06-DelayRCA` (60 delay events, 5 projects)

### Q1. Pareto — most frequent delay causes

| Rank | Cause | Occurrences | Total Delay Days | Cumulative % |
|------|-------|------------|-----------------|-------------|
| 1 | **RFI Response Delay** | 11 | 266 | 18.3% |
| 2 | Permit Delay | 8 | 175 | 31.7% |
| 3 | Material Delay | 8 | 162 | 45.0% |
| 4 | Client Decision Pending | 6 | 168 | 55.0% |
| 5 | Labour Shortage | 5 | 111 | 63.3% |

### Q2. Responsible party with most delay days

| Party | Total Delay Days | Incidents | % of Total |
|-------|-----------------|-----------|-----------|
| **Consultant** | **339** | 15 | **23.1%** |
| Subcontractor | 321 | 13 | 21.9% |
| Force Majeure | 301 | 11 | 20.5% |
| Authority | 240 | 10 | 16.4% |
| Contractor | 145 | 6 | 9.9% |
| Client | 121 | 5 | 8.2% |

### Q6. Cost of delay at $15,000/day burn rate

| Project | Delay Days | Cost of Delay (USD) | Dominant Cause |
|---------|-----------|--------------------|-|
| WT-DC-MUM-01 | 382 | **5,730,000** | Material Delay |
| WT-MAL-DEL-06 | 357 | 5,355,000 | Weather |
| WT-OFF-SYD-02 | 277 | 4,155,000 | Rework |
| WT-RES-MEL-05 | 246 | 3,690,000 | Weather |
| WT-HOS-AKL-03 | 205 | 3,075,000 | Rework |
| **TOTAL** | **1,467** | **22,005,000** | |

---

## Problem 07 — Monthly Cash Flow Tracking

**Source sheet:** `P07-CashFlow` (48 project-months, 4 projects, Jan–Dec 2024)

### Q1. Negative cash flow months

| Project | Months Negative | Worst Month | Worst Net CF (USD) | Total Net CF (USD) |
|---------|----------------|-------------|-------------------|-------------------|
| WT-HOS-AKL-03 | **9** | 2024-12 | -992,486 | -3,867,202 |
| WT-ITP-BLR-04 | 8 | 2024-04 | -1,331,420 | -2,898,856 |
| WT-DC-MUM-01 | 6 | 2024-02 | -868,853 | 839,758 |
| WT-OFF-SYD-02 | 6 | 2024-01 | -1,317,584 | -1,390,187 |

### Q5. Portfolio cash surplus / deficit

| Measure | Amount (USD) |
|---------|-------------|
| Total actual inflow | 43,006,437 |
| Total actual outflow | 50,322,924 |
| **Net deficit** | **-7,316,487** |
| Projects in deficit | 3 of 4 |

### Q6. Cash flow forecast accuracy

**Portfolio forecast accuracy: 76.9%** — collections are running **23.1% below** the cash-flow forecast.

---

## Problem 08 — Change Order (VO) Impact Analysis

**Source sheet:** `P08-ChangeOrder` (45 variation orders, 4 projects)

### Q1. Approved cost impact per project

| Project | Approved VOs | Approved Cost (USD) | All VOs | Total VO Book (USD) |
|---------|-------------|--------------------|---------|--------------------|
| WT-HOS-AKL-03 | 4 | **1,919,398** | 12 | 3,608,761 |
| WT-RES-MEL-05 | 2 | 892,260 | 11 | 3,770,085 |
| WT-DC-MUM-01 | 1 | 791,101 | 8 | 2,083,172 |
| WT-OFF-SYD-02 | 6 | 583,674 | 14 | 4,884,716 |
| **TOTAL** | **13** | **4,186,433** | **45** | **14,346,734** |

### Q3. Unresolved VO exposure

**15 of 45 change orders (33.3%)** are still Pending or Under Review, carrying **$3,297,152** of unquantified cost exposure.

---

## Problem 09 — Subcontractor Performance Scorecard

**Source sheet:** `P09-SubconScore` (30 scorecards, 13 subcontractors, 3 projects)

### Q1. Top 3 and Bottom 3 subcontractors

| Rank | Subcontractor | Avg Weighted Score | Scorecards |
|------|-------------|-------------------|-----------|
| 🏆 1 | Contractor-C | 3.86 | 1 |
| 🏆 2 | Contractor-M | 3.80 | 2 |
| 🏆 3 | Contractor-B | 3.65 | 2 |
| ⚠️ 11 | Contractor-E | 3.25 | 2 |
| ⚠️ 12 | Contractor-A | 3.24 | 1 |
| ⚠️ 13 | Contractor-N | 3.15 | 2 |

### Q5. Blacklist candidates (score < 3.0 AND defects > 15)

| Subcontractor | Trade | Project | Score | Defects |
|-------------|-------|---------|-------|---------|
| Contractor-G | Facade & Cladding | WT-OFF-SYD-02 | 2.81 | 22 |
| Contractor-N | Elevator Installation | WT-DC-MUM-01 | 2.99 | 20 |

---

## Problem 10 — Construction Cost Benchmarking

**Source sheet:** `P10-Benchmark` (40 completed projects, 3 countries, 2022–2025)

### Q1. Average cost per sqm by country

| Country | Avg Cost/sqm (USD) | Projects |
|---------|-------------------|----------|
| **Australia** | **$3,677** | 18 |
| New Zealand | $2,993 | 7 |
| India | $670 | 15 |

**Answer:** Australia is the most expensive market — a **448.5% premium** over India.

### Q2. Cost per sqm by project type

| Highest | Hotel | **$3,859/sqm** |
|---------|-------|----------------|
| Lowest | Data Centre | **$1,732/sqm** |

### Q6. Budget estimate — 50,000 sqm Data Centre in Mumbai

| Scenario | Budget (USD) |
|---------|-------------|
| Base case ($614/sqm) | **30,720,000** |
| Low case ($407/sqm) | 20,350,000 |
| High case ($798/sqm) | 39,900,000 |

---

## Problem 12 — Earned Value Management (EVM)

**Source sheet:** `P12-EVM` (36 monthly periods, BAC $25M)

### Key EVM Metrics at Month 36

| Metric | Value |
|--------|-------|
| BAC | $25,000,000 |
| EAC | $27,785,221 |
| **Projected Overrun** | **$2,785,221 (11.1%)** |
| CPI at Month 36 | 0.900 |
| SPI at Month 36 | 0.794 |
| Months with CPI < 1.00 | 25 of 36 |
| Months with SPI < 0.90 | 15 of 36 |

**Answer:** The project is both **behind schedule** and **over cost**. CPI trend is declining at -0.0004 per month — cost performance is getting worse.

### Q6. Cost recovery needed for CPI = 1.0 by Month 24

**$3,079,805** (15.6% of spend) must be recovered through value engineering, claim recovery or productivity gains.

---

## Problem 13 — Procurement Lead Time Analysis

**Source sheet:** `P13-LeadTime` (50 purchase orders, 10 suppliers)

### Key Findings

- **Average lead time:** 36.9 days across all 50 POs
- **Longest lead time:** Copper Wiring at 69 days
- **Shortest lead time:** Plywood (Marine) at 21.7 days
- **Late deliveries:** 35 of 50 POs (70%) delivered late
- **Average delay of late POs:** 9.6 days
- **Portfolio on-time rate:** 30.0%

### Supplier Reliability Scorecard

**All 10 suppliers rated "D — Replace"** (none above 43% on-time).

| Best | Supplier-J | 42.9% on-time |
|------|-----------|---------------|
| Worst | Supplier-B & Supplier-H | 0% on-time |

---

## Problem 14 — Client Payment Aging Tracker

**Source sheet:** `P14-PaymentAging` (40 invoices, 10 clients, 5 projects)

### Q1. Outstanding amounts

| Metric | Amount (USD) |
|--------|-------------|
| Total invoiced | 41,713,158 |
| Total paid | 29,856,300 |
| **Total outstanding** | **11,856,858** |
| Collection rate | 71.6% |

### Q3. Aging bucket analysis

| Bucket | Invoices | Outstanding (USD) | % of Outstanding |
|--------|---------|------------------|-----------------|
| 0–30 days | 3 | 998,469 | 9.2% |
| 31–60 days | 7 | 3,071,180 | 28.2% |
| 61–90 days | 0 | 0 | 0% |
| **90+ days** | **6** | **6,831,506** | **62.7%** |

### Q5. Collection rate by project

| Project | Collection Rate | Outstanding (USD) |
|---------|----------------|------------------|
| WT-DC-MUM-01 | **58.4%** (worst) | 4,625,307 |
| WT-ITP-BLR-04 | **92.5%** (best) | 446,540 |

### Q6. Interest receivable at 1.5%/month

**Total interest receivable: $797,715** on $10,901,155 overdue. Largest claim: Brookfield at $378,457.

---

## Problem 15 — Multi-Project Portfolio Dashboard

**Source sheet:** `P15-Portfolio` (25 projects, 3 countries)

### Q1. Portfolio status breakdown

| Status | Projects | % | Budget (USD) |
|--------|---------|---|-------------|
| In Progress | 4 | 16% | 142,240,052 |
| **On Hold** | **8** | **32%** | **505,848,491** |
| Completed | 8 | 32% | 397,754,853 |
| Planning | 5 | 20% | 379,882,427 |

### Q2. Portfolio financials

| Metric | Value |
|--------|-------|
| Total budget | $1,425,725,823 |
| Total spent | $690,772,336 |
| Budget remaining | $734,953,487 |
| Avg completion | 49.8% |

### Q3. Red-zone projects (CPI < 0.90 AND SPI < 0.90)

| Project | Name | Country | SPI | CPI |
|---------|------|---------|-----|-----|
| WT-2005 | IT Park Sydney | Australia | 0.78 | 0.86 |
| WT-2015 | Shopping Mall Canberra | Australia | 0.88 | 0.83 |
| WT-2024 | Hospital Bangalore | India | 0.78 | 0.89 |

### Q6. Traffic-light summary

| 🟢 GREEN | 4 projects (16%) | CPI ≥ 1.0 and SPI ≥ 1.0 |
|----------|-----------------|-------------------------|
| 🟡 AMBER | 18 projects (72%) | Either index below 1.0 |
| 🔴 RED | 3 projects (12%) | Both CPI and SPI < 0.9 |

### Executive Summary for the Board

1. **Scale** — WT is running 25 projects worth $1,425,725,823 across India, Australia and New Zealand, 49.8% complete on average, with $734,953,487 still to spend.
2. **Performance** — Average CPI is 0.93 and average SPI 0.95; 4 projects are green, 18 amber and 3 red, with 48.5% of budget drawn against 49.8% completion.
3. **Action** — The 3 red-zone projects ($87,529,465 of budget) plus 8 on-hold projects ($505,848,491) are where recovery plans and cash are needed; everything else is tracking within tolerance.

---

## 🛠️ How to Use This Workbook

1. **Open the Excel file** — every figure in the Analysis Report sheet is a live formula referencing source data.
2. **Update source sheets** (P01–P15) and all analysis answers refresh automatically.
3. **Charts** are embedded alongside the tables in the Excel for visual reference.
4. **Grey blocks** in columns H–V of the report are helper calculations — not intended for presentation.

---

> *Dataset and analysis by Gulzar — Data Scientist / AI Engineer — MEP QS Services*
