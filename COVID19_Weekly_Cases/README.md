# Weekly Confirmed COVID-19 Cases: Global, Regional and Country Analysis

An analysis of 249 locations (countries, regions, income groups, and world totals) from January 2020 to October 2026, using the Our World in Data (OWID) weekly confirmed case series.

**Notebook:** `notebooks/01_weekly_covid_cases_analysis.ipynb`
**Summary:** `summary.md`
**Charts:** `figures/`

## Data

- **File:** `data/raw/weekly-covid-cases.csv` (about 18 MB, 609,658 rows)
- **Columns:** `Entity`, `Code`, `Day`, `Weekly cases`
- **Source:** Our World in Data COVID-19 dataset, compiled from official national reports. Check the OWID page for the current licence and citation (OWID data is generally released under CC BY 4.0).

### How to read the `Weekly cases` column

Each row is a date. The value is the number of confirmed cases in the seven days ending on that date. It is a rolling seven-day total, not a count for one day. Adding the rows together counts each case about seven times. The notebook divides every total by 7. As a check, the World series divided by 7 gives about 779 million cases, which matches the scale of cumulative figures WHO has published.

## Questions answered

1. How has the global weekly case count changed over time?
2. How many cases were recorded each year?
3. Which countries recorded the most cases?
4. Did continents experience waves at different times?
5. How has Africa's share of recorded cases changed?
6. When did each country reach its highest daily count?
7. How do Nigeria's waves compare with South Africa, Kenya, Ghana and Egypt?
8. Which months of the year carry the most cases?
9. How many distinct waves did each large country experience?
10. When did global cases grow fastest in a single week?
11. Which countries report in weekly batches and which report daily?
12. Which countries have stopped reporting?
13. What are the longest stretches of zero cases?
14. Are there sudden spikes that look like catch-up reporting?
15. Do countries' waves move together?
16. How do income groups differ?
17. What does the most recent year look like for the world and for Nigeria?
18. How spread out were country-level averages each year?

## Limitations

- Recorded cases depend on testing, reporting rules, and laboratory capacity. They are not a measure of infection.
- No population column is included, so comparisons between countries are in absolute counts.
- The file does not name variants. Any link between a peak and a variant is an inference from timing.
- Many countries stopped reporting. The notebook counts 147 countries with no non-zero count in 2026.
- Continent and income membership are only available for aggregates, so some questions compare countries across years rather than within a region.

## Running the notebook

```bash
pip install pandas matplotlib seaborn scipy jupyter
jupyter notebook notebooks/01_weekly_covid_cases_analysis.ipynb
```

Run the notebook from the project root so the relative paths to `data/raw/` and `figures/` resolve.

## Project structure

```
covid-weekly-cases/
  data/raw/weekly-covid-cases.csv
  figures/            (charts saved by the notebook)
  notebooks/01_weekly_covid_cases_analysis.ipynb
  README.md
  summary.md
```
