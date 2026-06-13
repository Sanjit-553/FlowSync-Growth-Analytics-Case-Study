# Dataset Specification

## Project

FlowSync Growth Analytics Case Study

---

# 1. Dataset Overview

The FlowSync dataset is a synthetic SaaS business dataset designed to simulate customer acquisition, activation, retention, product adoption, support operations, and revenue growth.

The dataset represents a fictional B2B SaaS company operating between January 2024 and December 2025.

The purpose of the dataset is to support business analysis, KPI development, executive reporting, and strategic decision-making.

---

# 2. Business Scenario

FlowSync is a workflow automation and project management platform serving organizations of different sizes.

Although customer acquisition has grown steadily, revenue growth has not increased at the same pace.

Leadership requires a comprehensive analysis of:

* Customer acquisition
* Product activation
* Customer retention
* Revenue growth
* Expansion opportunities
* Marketing efficiency

---

# 3. Analysis Objectives

The dataset is designed to answer the following questions:

### Acquisition

* Which channels acquire the most customers?
* Which channels acquire the highest-value customers?

### Activation

* What behaviors drive successful activation?

### Retention

* What factors contribute to churn?
* Which segments retain most effectively?

### Product

* Which features drive engagement?
* Does feature adoption improve retention?

### Revenue

* What drives recurring revenue growth?
* Which customers generate the highest lifetime value?

---

# 4. Dataset Tables

## Users

Purpose:

Stores customer profile information.

Expected Records:

10,000

Columns:

| Column             | Description                          |
| ------------------ | ------------------------------------ |
| UserID             | Unique customer identifier           |
| SignupDate         | Initial signup date                  |
| Country            | Customer country                     |
| Industry           | Customer industry                    |
| CompanySize        | Startup, SMB, Mid-Market, Enterprise |
| AcquisitionChannel | Source of acquisition                |

---

## Subscription History

Purpose:

Monthly customer subscription snapshots.

Expected Records:

240,000

Columns:

| Column | Description                    |
| ------ | ------------------------------ |
| UserID | Customer identifier            |
| Month  | Reporting month                |
| Plan   | Free, Starter, Pro, Enterprise |
| Status | Active, Churned                |
| MRR    | Monthly recurring revenue      |

---

## Feature Usage

Purpose:

Measures product engagement.

Expected Records:

120,000

Columns:

| Column          | Description                 |
| --------------- | --------------------------- |
| UserID          | Customer identifier         |
| Month           | Reporting month             |
| ProjectsCreated | Projects created            |
| AutomationsUsed | Automation workflows used   |
| TeamInvites     | Number of teammates invited |
| Logins          | Monthly logins              |

---

## Marketing Performance

Purpose:

Measures acquisition efficiency.

Expected Records:

144

Columns:

| Column           | Description         |
| ---------------- | ------------------- |
| Month            | Reporting month     |
| Channel          | Acquisition channel |
| Spend            | Marketing spend     |
| Leads            | Leads generated     |
| Customers        | Customers acquired  |
| RevenueGenerated | Revenue attributed  |

---

## Support Tickets

Purpose:

Measures customer support quality.

Expected Records:

50,000

Columns:

| Column          | Description                 |
| --------------- | --------------------------- |
| TicketID        | Unique ticket identifier    |
| UserID          | Customer identifier         |
| Priority        | Low, Medium, High, Critical |
| ResolutionHours | Time to resolution          |
| CSAT            | Customer satisfaction score |

---

## Product Events

Purpose:

Supports behavioral and funnel analysis.

Expected Records:

150,000

Columns:

| Column    | Description         |
| --------- | ------------------- |
| EventID   | Event identifier    |
| UserID    | Customer identifier |
| EventDate | Event date          |
| EventType | Product activity    |

Supported Events:

* Login
* CreateProject
* InviteUser
* AutomationUsed
* UpgradePlan

---

## Account Expansion

Purpose:

Tracks revenue expansion and contraction.

Expected Records:

20,000

Columns:

| Column        | Description           |
| ------------- | --------------------- |
| UserID        | Customer identifier   |
| EventDate     | Revenue change date   |
| EventType     | Upgrade or Downgrade  |
| RevenueChange | MRR increase/decrease |

---

# 5. Business Rules

## Pricing

| Plan       | Monthly Price |
| ---------- | ------------- |
| Free       | $0            |
| Starter    | $29           |
| Pro        | $99           |
| Enterprise | $499          |

---

## Customer Segments

| Segment    | Distribution |
| ---------- | ------------ |
| Startup    | 40%          |
| SMB        | 35%          |
| Mid-Market | 18%          |
| Enterprise | 7%           |

---

## Acquisition Channels

| Channel           | Distribution |
| ----------------- | ------------ |
| Google Ads        | 40%          |
| Organic Search    | 25%          |
| Referral          | 12%          |
| LinkedIn Ads      | 8%           |
| Direct            | 8%           |
| Content Marketing | 7%           |

---

## Activation Definition

A customer is considered activated when:

* ProjectsCreated >= 3
* Logins >= 5

---

## Churn Rates

| Plan       | Monthly Churn |
| ---------- | ------------- |
| Free       | 12%           |
| Starter    | 5%            |
| Pro        | 2.5%          |
| Enterprise | 1%            |

---

# 6. Embedded Business Insights

The dataset intentionally contains the following patterns:

### Insight 1

Google Ads generates the highest volume of signups but lower customer quality.

### Insight 2

LinkedIn Ads generates fewer customers but higher customer lifetime value.

### Insight 3

Automation feature adoption significantly improves retention.

### Insight 4

Customers who collaborate with teammates upgrade more frequently.

### Insight 5

Enterprise customers contribute a disproportionately high share of revenue.

### Insight 6

Slow support response times increase downgrade risk.

---

# 7. Expected Deliverables

The dataset will support:

* KPI Development
* Revenue Analysis
* Churn Analysis
* Retention Analysis
* Product Analytics
* Marketing Analytics
* Executive Dashboarding
* Strategic Recommendations

