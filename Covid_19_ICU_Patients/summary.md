# Summary: COVID-19 patients in intensive care

**What the data shows**

- The highest single-day ICU count in this file is 28,891 patients in the United States, on 12 January 2021. The US record has 1,381 days, one of the longer series here.
- Peak timing varies. The main ICU peak ranges from late March 2020 in Estonia to early April 2022 in South Korea (section 6). Countries with many reporting days show four to six separate waves (section 5).
- Reporting thins out quickly. In January 2022, 42 countries reported. In August 2024, only Czechia, Italy and Malaysia still did (section 4). Global totals built from these data would be incomplete for the later years.
- In 36 of 38 countries that reported in both periods, average ICU counts were lower in 2022 and 2023 than in 2020 and 2021. The median ratio is 0.34. South Korea (2.18) and Australia (1.63) were the exceptions (section 8). The drop fits lower infection pressure, better treatment and vaccination, but this data cannot separate those effects from changes in reporting.
- Weekend counts sit very close to weekday counts. The median weekend-to-weekday ratio is 0.99 across 36 countries (section 9). Weekend effects are small here.
- Zero values are common in some series. In Malta, 39 percent of records are zero, which most likely reflects missing reports entered as zero (section 10).
- Case counts and ICU counts move together with little delay. In 12 of 38 countries the best lag is zero days, and 19 of 38 have a best lag of three days or less. Only one country's best lag reached 14 days. The correlation is moderate, with a median of 0.40, and 16 countries fall below 0.30 (section 13). The one to two week delay often expected between infections and ICU admissions is hard to see in this data.
- In 23 of 38 countries the ICU peak came after the nearby case peak. The median gap is 10 days, and the spread is wide, from minus 120 to plus 65 days. Algeria's value sits at the edge of the 120-day search window, so treat it as unreliable (section 14).
- The severity ratio in section 15 is not a valid severity measure in this data. Sweden shows about 1,000 ICU patients for every 1,000 daily cases, which points to case counts that understate infections at that time. The ratio mostly reflects how cases were counted.

**What the data cannot show**

- No population column is included, so counts cannot be compared per person without outside data.
- The series ends in August 2024. Any statement about current hospital pressure would need newer data.
- ICU definitions vary. The metadata notes that some countries report ventilated or critically ill patients instead. Cross-country comparisons therefore mix definitions.
- Results in sections 13 to 15 describe this dataset only. They are not clinical measurements.

**Suggested next steps**

Add the OWID population file to compare countries per 100,000 people. Check the national sources listed in the metadata for any country with long gaps or many zeros. Repeat the lag analysis with the hospital admissions series from the same collection, which may give a cleaner timing signal than ICU counts.
