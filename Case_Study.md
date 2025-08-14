#  NBA Expansion Market Analysis — Case Study

## Executive Summary
Seeing the economic potential for growth, the NBA is evaluating potential expansion and relocation markets in order to extend into untapped markets in the USA.  

This analysis identifies and ranks candidate cities using **population, demographic, economic, and sports engagement data**, with results presented 
via an **interactive Power BI dashboard** and an **Excel-based weighted criteria scoring model**.

---

## Business Problem
- **Stakeholder:** National Basketball Association Expansion Committee
- **Key Question:** Which cities offer the best potential for a new NBA franchise?
- **Why Now:** Recent revenue growth, a new $75 billion TV deal and CBA adjustments allow for expansion considerations.
- **Decision Impact:** Market selection affects long-term league revenue, fan engagement, and media rights value.

---

## Key Findings
**Seattle, Las Vegas, Austin and Nashville** were identified as the best candidates for potential NBA expansion or relocation based on their market potential, population metrics and exsisiting infrustrutuce.

---

## Data Sources
| Dataset | Notes |
|---------|-------|
| U.S. Census Demographics | Metro population, population growth and median income |
| Sports Market Size Index | Neilsen TV Market Rankings and Arena data |
| Team Finances and Investment Potential | NBA financial reports and Fortune 500 HQ's |
| Fan Engagement Data | Google Analytic Trends |

**Data Processing Steps:**
- Created standardised column names and lookup tables in Excel in prepartation for importing into Power BI
- Loaded raw CSV datasets into Excel and cleaned to ensure data normalisation (Standardised column names and removed nulls)
- Loaded Excel files in Power BI and created **Star Schema**
- Created Measures such Digital Demographic Index, Per Capita Income and Population Growth Target

---

## Methodology

### Excel
Weighted Criteria Scoring system allowed for all cites to have a standarised score acorss 8 different metrics

The highest ranked city for a particular metric receives a score of 100, the lowest ranked city gets a score of 0 and all other cities are scaled proportionally in between

Weighted Criteria Formula = (x - Min/Max - Min) x 100

Example:

Population Score = (1,500,000 - 1,000,000)/(3,000,000 - 1,000,000) x 100
                 = 25

- Weighted Critera Score = Metro Population (20%) + Population Growth (15%) + Per Capita Income (15%) + TV Market Rank (10%) + Google Trend Score (10%) + Demographics (10%) + Arena Criteria (10%) + Fortune 500 HQ''s (10%)

