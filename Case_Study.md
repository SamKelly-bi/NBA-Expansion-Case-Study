# 🏀 NBA Expansion Market Analysis — Case Study

## Executive Summary
Seeing the economic potential for growth, the NBA is evaluating potential expansion and relocation markets in order to extend into untapped markets in the USA.  
This analysis identifies and ranks candidate cities using **population, demographic, economic, and sports engagement data**, with results presented 
via an **interactive Power BI dashboard** and an **Excel-based weighted criteria scoring model**.

**Key Findings:**  
Seattle, Las Vegas, Austin and Nashville were identified as the best candidates for potential NBA expansion or relocation based on their market potential, exsisting population and infrustrutuce.

---

## Business Problem
- **Stakeholder:** National Basketball Association Expansion Committee
- **Key Question:** Which cities offer the best potential for a new NBA franchise?
- **Why Now:** Recent revenue growth, a new $75 billion TV deal and CBA adjustments allow for expansion considerations.
- **Decision Impact:** Market selection affects long-term league revenue, fan engagement, and media rights value.

---

## 3️⃣ Data Sources
| Dataset | Source | Time Period | Notes |
|---------|--------|-------------|-------|
| U.S. Census Demographics | [data.census.gov](https://data.census.gov) | 2023 | City population, median income |
| Sports Market Size Index | Public sports market rankings | 2023 | Includes TV market size |
| NBA Attendance & Revenue | Basketball Reference | 2019–2023 | Used for benchmarking |
| Fan Engagement Data | Google Trends, Twitter API | 2023 | Indexed search & social interest |

**Data Processing Steps:**
- Loaded raw CSV/Excel files into **Power Query** (Power BI + Excel)
- Standardized column names, removed nulls, merged on `City` field
- Created calculated columns (Market Growth %, Engagement Index)
- Stored clean tables in **Star Schema** for Power BI modeling

---

## 4️⃣ Methodology

### Power BI
- **Model:** 1 Fact table (`City_Metrics`) + 4 Dimension tables (`City`, `Market`, `Demographics`, `Engagement`)
- **Key Measures:**
```DAX
Total Market Score :=
AVERAGEX(
    VALUES('City'[City]),
    [Market Size Score] + [Income Score] + [Engagement Score]
)

Projected Revenue :=
[Avg Attendance] * [Ticket Price] * 41

