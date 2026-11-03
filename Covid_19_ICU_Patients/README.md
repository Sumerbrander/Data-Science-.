# COVID-19 Patients in Intensive Care: Country Analysis

An analysis of daily ICU occupancy for 42 countries and territories, from February 2020 to August 2024. The notebook also links ICU counts with weekly case counts to test how the two move together.

**Notebook:** `notebooks/02_icu_patients_analysis.ipynb`
**Summary:** `summary.md`
**Charts:** `figures/`

## Data

- **ICU file:** `data/raw/current-covid-patients-icu.csv` (39,116 rows)
- **Metadata:** `data/raw/current-covid-patients-icu_metadata.json`
- **Cases file (used in sections 13 to 15):** `data/raw/weekly-covid-cases.csv`
- **Source:** Official hospital and ICU reports collated by Our World in Data. OWID licence is CC BY 4.0, and each country's original source is listed in the metadata.

### Important: the series ends in August 2024

The metadata records that no new ICU data has been added since 13 August 2024. The file was downloaded in November 2026, but it does not contain data after that date. Every result here is historical. Do not use this file to describe current hospital pressure.

### Other things to know about the data

- Reporting is uneven. In January 2022, 42 countries reported. By August 2024, only Czechia, Italy and Malaysia still did.
- Some countries report ventilated or critically ill patients instead of ICU patients, as the metadata notes. Cross-country comparisons mix definitions.
- The file contains zero values. In Malta, 39 percent of records are zero, which likely reflects missing reports.
- No population column is included.

## Questions answered

1. Which countries reached the highest ICU occupancy?
2. How complete is each country's record?
3. How did ICU occupancy move in ten selected countries?
4. How many countries were reporting in each month?
5. How many separate waves did each country show?
6. When did each country reach its main ICU peak?
7. What does a month-by-month view of each country's waves look like?
8. Did later waves put fewer people in ICU than earlier ones?
9. Do ICU records differ on weekends?
10. How often is the count recorded as zero?
11. How spread out are ICU counts within each country?
12. What are the longest gaps between records?
13. Do case counts lead ICU counts, and by how many days?
14. Does the ICU peak come after the case peak?
15. How many ICU patients are there per 1,000 daily cases?
16. Which countries' ICU waves moved together?
17. When did each country's series end?
18. Summary of findings

## Known weak points in the analysis

- The lag analysis (section 13) picks the single best lag. Correlations are moderate, and most countries show short lags, so the result is a pattern in this data and not a measured clinical delay.
- The 120-day search window in section 14 is a judgement call. Algeria's result sits at the edge of the window and should be treated as unreliable.
- The severity ratio in section 15 mostly reflects how cases were counted. Sweden's ratio of about 1,000 ICU patients per 1,000 daily cases shows this clearly. Do not present section 15 as a severity measure.

## Running the notebook

```bash
pip install pandas matplotlib seaborn scipy jupyter
jupyter notebook notebooks/02_icu_patients_analysis.ipynb
```

Run from the project root. Section 13 onward reads the weekly cases file from `data/raw/`.

## Project structure

```
covid-icu-patients/
  data/raw/current-covid-patients-icu.csv
  data/raw/current-covid-patients-icu_metadata.json
  data/raw/weekly-covid-cases.csv
  figures/
  notebooks/02_icu_patients_analysis.ipynb
  README.md
  summary.md
```
