

# COVID-19 Data Exploration Using SQL

## Project Overview

This project explores global COVID-19 data using SQL. The analysis focuses on understanding the spread of COVID-19, mortality rates, and vaccination progress across different countries and continents.

The project uses two datasets:

* **CovidDeaths** – Contains information about COVID-19 cases, deaths, population, and geographic data.
* **CovidVaccinations** – Contains information about vaccinations administered, people vaccinated, fully vaccinated individuals, and related metrics.

The objective of this project is to practice SQL skills such as:

* Data exploration
* Aggregations
* Joins
* Filtering
* Calculated fields
* Ranking and sorting
* Basic analytical reporting

---

## Datasets

### CovidDeaths

Key columns:

| Column       | Description           |
| ------------ | --------------------- |
| location     | Country or region     |
| continent    | Continent name        |
| date         | Reporting date        |
| population   | Population size       |
| total_cases  | Total reported cases  |
| new_cases    | Daily reported cases  |
| total_deaths | Total reported deaths |
| new_deaths   | Daily reported deaths |

---

### CovidVaccinations

Key columns:

| Column                  | Description                           |
| ----------------------- | ------------------------------------- |
| location                | Country or region                     |
| date                    | Reporting date                        |
| total_vaccinations      | Total vaccine doses administered      |
| people_vaccinated       | People who received at least one dose |
| people_fully_vaccinated | Fully vaccinated individuals          |
| new_vaccinations        | Daily vaccinations                    |

---

## SQL Concepts Demonstrated

* SELECT Statements
* Filtering with WHERE
* Aggregate Functions (SUM, MAX)
* GROUP BY
* ORDER BY
* INNER JOIN
* Percentage Calculations
* Data Analysis and Reporting

---

# Analysis Performed

## 1. Total Cases vs Total Deaths

Determine the likelihood of death among reported COVID-19 cases.

### Insight

Countries with higher death percentages may indicate healthcare challenges, reporting differences, or more severe outbreaks.

---

## 2. Percentage of Population Infected

Calculate the percentage of a country's population that contracted COVID-19.

### Insight

Helps identify countries with the highest infection rates relative to population size.

---

## 3. Countries with Highest Death Counts

Identify countries with the largest total number of COVID-related deaths.

### Insight

Highlights regions most severely impacted by the pandemic.

---

## 4. Global Cases and Death Trends

Aggregate worldwide cases and deaths by date.

### Insight

Shows major COVID-19 waves and trends throughout the pandemic.

---

## 5. Vaccination Analysis

### 5.1 Percentage of Population Vaccinated

Calculate the percentage of each country's population that received at least one vaccine dose.

### Insight

Measures vaccine adoption across countries.

---

### 5.2 Total Vaccinations Per Country

Determine which countries administered the most vaccine doses.

### Insight

Shows countries with the largest vaccination campaigns.

---

### 5.3 Fully Vaccinated Population Percentage

Calculate the percentage of fully vaccinated individuals relative to the country's population.

### Insight

Provides a better measure of vaccination coverage than total doses administered.

---

### 5.4 South Africa Vaccination Progress

Track vaccination growth over time in South Africa.

### Insight

Allows visualization of vaccine rollout and uptake.

---

### 5.5 Cases vs Vaccinations

Compare total cases with vaccination progress over time.

### Insight

Can be used to investigate whether increased vaccination rates coincided with reduced case growth.

---

### 5.6 Top 10 Most Vaccinated Countries

Identify countries with the highest number of vaccinated people.

### Insight

Highlights global leaders in vaccination efforts.

---

### 5.7 Vaccinations vs Deaths

Compare vaccination numbers with total deaths by country.

### Insight

Provides a foundation for further analysis into the relationship between vaccination coverage and mortality outcomes.

---

## Example Join Used

```sql
SELECT
    dea.location,
    dea.date,
    vac.people_vaccinated
FROM CovidDeaths dea
JOIN CovidVaccinations vac
    ON dea.location = vac.location
    AND dea.date = vac.date;
```

---

## Key Findings

* Some countries experienced significantly higher infection rates than others relative to population size.
* Death counts varied greatly across regions and continents.
* Vaccination rollout differed considerably between countries.
* Countries with higher vaccination coverage generally showed stronger pandemic response outcomes.
* Combining deaths and vaccination datasets provides richer insights than analyzing either dataset independently.

---

## Tools Used

* SQL Server / MySQL / PostgreSQL (adaptable)
* COVID-19 Datasets
* GitHub
* Optional: Power BI or Tableau for visualization

---

## Future Enhancements

* Implement Window Functions
* Create CTEs (Common Table Expressions)
* Build Views for reporting
* Develop a Power BI dashboard
* Create vaccination and mortality trend visualizations
* Perform continent-level and regional comparisons

---

## Author

**Makaziwe Lubisi**

Data Analytics & Power Platform Enthusiast

This project was completed as part of a SQL data analytics portfolio to demonstrate data exploration, SQL querying, and analytical reporting skills.


https://www.figma.com/make/iAd7p0T8YSFkPn6U4cRRjB/Interactive-dashboard-creation?fullscreen=1&t=ifuFf5kdPQPXWuB5-1&code-node-id=0-9
