# Baltic States GDP Analysis (2014–2025)

## Project Overview

An interactive Power BI project analyzing real GDP growth across the three Baltic countries: Estonia, Latvia, and Lithuania.

The goal of this project is to compare economic performance, identify long-term growth trends, examine economic downturns, and evaluate the stability of annual GDP growth.

**Period:** 2014–2025  
**Countries:** Estonia, Latvia, Lithuania  
**Data Source:** Eurostat  
**Tools:** Power BI Desktop, Power Query, DAX

## Business Questions

1. Which Baltic country demonstrated the strongest cumulative real GDP growth?
2. Which country had the lowest average annual GDP growth?
3. How did the three economies perform during 2020–2023?
4. Which country's annual GDP growth was the most stable?
5. How did economic performance change over the entire observation period?

## Data Source

Eurostat — Real GDP Growth Rate (Volume), dataset `tec00115`.

[Eurostat Data Browser](https://ec.europa.eu/eurostat/databrowser/view/tec00115/default/line?lang=en)

The dataset contains annual real GDP growth rates expressed as percentage changes relative to the previous year.

## Data Preparation

Data preparation was performed using Power Query.

Main steps:
- Imported the Eurostat Excel dataset.
- Removed unnecessary metadata and empty columns.
- Promoted the first data row to column headers.
- Removed unnecessary rows.
- Renamed columns and assigned appropriate data types.
- Used Unpivot Columns to transform the dataset from wide format into a normalized long format.

Final data structure:

| Country | Year | GDP Growth (%) |
|---|---:|---:|
| Estonia | 2014 | ... |
| Latvia | 2014 | ... |
| Lithuania | 2014 | ... |

The resulting dataset contains 36 observations.

## Data Analysis & DAX

The project uses DAX measures to calculate:

- Latest GDP Growth — annual growth in the latest available year.
- Average GDP Growth — average annual growth over the selected period.
- GDP Index (2014 = 100) — cumulative real GDP development relative to the base year.
- GDP Change (2020–2023) — cumulative real GDP change between the 2020 and 2023 levels.
- GDP Growth Volatility — standard deviation of annual GDP growth rates.

The GDP Index is calculated by compounding annual real GDP growth rates from 2015 onwards, with 2014 set as the base year (100).

## Key Findings

**1. Lithuania demonstrated the strongest cumulative growth.**

Lithuania reached a real GDP index of approximately 142.1 in 2025, representing an increase of approximately 42.1% relative to 2014.

**2. Latvia recorded the lowest average annual growth.**

Latvia had an average annual real GDP growth rate of approximately 1.98%.

**3. Estonia recorded the lowest cumulative growth between 2020 and 2023.**

Its cumulative real GDP increase over this period was approximately 5.90%, compared with 7.63% for Latvia and 9.76% for Lithuania.

**4. Lithuania demonstrated the lowest GDP growth volatility.**

Its standard deviation of annual growth rates was approximately 1.42 percentage points, indicating smaller fluctuations than in Estonia and Latvia during the observation period.

## Dashboard Pages

### 1. Overview
High-level economic performance indicators and long-term GDP trends.

### 2. Annual Dynamics
Annual GDP growth comparison, including positive and negative growth periods.

### 3. Economic Comparison
Country rankings, comparative indicators, and statistical analysis.

## Skills Demonstrated

- Data Acquisition
- Data Cleaning and Transformation
- Power Query
- Data Modeling
- DAX
- Statistical Analysis
- Data Visualization
- Economic Data Analysis
- Analytical Thinking

## Limitations

This project focuses on real GDP growth and its derived indicators. It does not assess all dimensions of economic performance, such as GDP per capita, productivity, unemployment, inflation, or household income.

GDP growth volatility should not be interpreted as a complete measure of economic stability.

## Author

Created as a personal data analytics portfolio project.
