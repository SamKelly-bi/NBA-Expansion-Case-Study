# NBA Expansion Market Analysis — Case Study

## Executive Summary
Seeing the economic potential for growth, the NBA is evaluating potential expansion and relocation markets in order to extend into untapped markets in the USA.  

This analysis identifies and ranks candidate cities using **population, demographic, economic, and sports engagement data**, with results presented via an **interactive Power BI dashboard** and an **Excel-based weighted criteria scoring model**.

---

## Business Problem
- **Stakeholder:** National Basketball Association Expansion Committee
- **Key Question:** Which cities offer the best potential for a new NBA franchise?
- **Why Now:** Recent revenue growth, a new $75 billion TV deal, and CBA adjustments allow for expansion considerations.
- **Decision Impact:** Market selection affects long-term league revenue, fan engagement, and media rights value.

---

## Key Findings
**Seattle, Las Vegas, Austin, and Nashville** were identified as the best candidates for potential NBA expansion or relocation based on their market potential, population metrics, and existing infrastructure.

---

## Data Sources
| Dataset | Notes |
|---------|-------|
| U.S. Census Demographics | Metro population, population growth, and median income |
| Sports Market Size Index | Nielsen TV Market Rankings and arena data |
| Team Finances and Investment Potential | NBA financial reports and Fortune 500 HQs |
| Fan Engagement Data | Google Analytics Trends |

**Data Processing Steps:**
- Created standardised column names and lookup tables in Excel in preparation for importing into Power BI
- Loaded raw CSV datasets into Excel and cleaned to ensure data normalisation (removed nulls, irrelevant data, and standardised metro names)
- Loaded Excel files into Power BI and created a **star schema**
- Created measures such as Digital Demographic Index, Per Capita Income, and Population Growth Target

---

## Methodology

### Excel
The weighted criteria scoring system allowed all cities to have a standardised score across 8 different metrics.

The highest-ranked city for a particular metric receives a score of 100, the lowest-ranked city receives a score of 0, and all other cities are scaled proportionally in between.

- Weighted Criteria Formula = (x - Min / Max - Min) * 100

Example:

- Population Score = (1,500,000 - 1,000,000) / (3,000,000 - 1,000,000) * 100  
                 = 25

- Weighted Criteria Score = Metro Population (20%) + Population Growth (15%) + Per Capita Income (15%) + TV Market Rank (10%) + Google Trend Score (10%) + Demographics (10%) + Arena Criteria (10%) + Fortune 500 HQs (10%)

### Power BI
**Model:** 
- 3 fact tables — All Cities WCS (primary), Expansion Cities WCS, and NBA City WCS (secondary fact tables)
- 5 lookup tables — Expansion Cities Data, NBA Teams Data, City Attributes Lookup, Region Lookup, and Media Market Lookup

**Visuals:**
- Cards highlighting key findings
- Matrix breaking down expansion city scores
- KPI gauge indicating whether a city met the target metric
- Stacked bar chart showing the makeup of NBA city scores
- Scatter chart showing all cities’ metro population and population growth %
- Clustered column chart highlighting which teams’ fanbases were the most engaged
- Scatter chart showing NBA franchise evaluations and the average income of the city

---

## Key Results

- **Seattle** was, by far, the top expansion candidate, as it scored highest in metro population and per capita income, two of the three most heavily weighted metrics
- **Las Vegas** was identified as the second expansion city due to its existing infrastructure and investment opportunities
- **Tampa**, despite scoring very highly, was not selected due to its low average income and close proximity to an existing NBA franchise, the Orlando Magic
- **New Orleans Pelicans** and **Memphis Grizzlies** were the two NBA franchises earmarked for relocation. Both cities ranked very low in population growth and average income
- **Austin** was the best candidate for the Pelicans’ relocation due to it ranking highest among all cities in population growth %. The city will need to invest in an NBA-ready arena if it is to host an NBA team
- **Nashville** was identified as the city to take the Grizzlies’ relocation, as both are located in Tennessee, with **The Music City** being significantly wealthier, larger, and faster growing

---

## Skills Demonstrated
- Data collection and cleaning (Power Query M, lookup functions)
- Data modelling (star schema)
- DAX calculations (criteria scores, rankings, KPIs)
- Interactive dashboard design (dynamic visuals, slicers, tooltips)
- Scenario modelling in Excel and Power BI
- Data storytelling with visuals and business context

---

## Supporting Files

- ![Excel Model and Visuals](https://github.com/SamKelly-bi/NBA-Expansion-Case-Study/tree/main/Excel)
- ![Power BI Model and Visuals](https://github.com/SamKelly-bi/NBA-Expansion-Case-Study/tree/main/Power%20BI)
- ![README.md](https://github.com/SamKelly-bi/NBA-Expansion-Case-Study/blob/main/README.md)

