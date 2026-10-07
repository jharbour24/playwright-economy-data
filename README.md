# The Playwright Economy: corrected summary dataset (v1.0)

Summary tables behind the essay *Come Back Next Month* (Earthbound, 2026), on how many new plays and playwrights
America's nonprofit theatres produce, before and after the pandemic.

**Everything here is an aggregate: counts, rates and estimates.** No row-level production listings are included. The
underlying season listings come from licensed and third-party sources that do not permit redistribution.

## What's in it

37 small CSV files in `data/dataset/`. Each one is described in [DATA_DICTIONARY.md](DATA_DICTIONARY.md). The main ones:

| Question | File |
|---|---|
| How many productions, plays and playwrights each season, and how much did they fall? | `decline_by_season.csv`, `decline_periods.csv` |
| Is the fall from theatres leaving the listings, or from smaller seasons? | `coverage_groups.csv`, `coverage_bridge.csv`, `panel_absences.csv` |
| Is the fall in writers just a fall in productions? | `decomposition.csv` |
| Do new plays get a second production? | `km_summary.csv`, `km.csv`, `pathways.csv`, `travel_predictors.csv` |
| Do new writers come back? | `writer_return.csv` |
| Are production slots concentrated in a few theatres? | `concentration_periods.csv` |
| Broadway attendance and real ticket prices | `broadway_by_season.csv`, `demand_index.csv` |
| Theatre finances (TCG Trend Theatres, IRS Form 990 panel) | `tcg_panels.csv`, `irs_panel.csv` |
| Playwright production royalties (a model) | `royalty.csv` |
| Licensing shares and timeline | `licensing_shares.csv`, `licensing_timeline.csv` |
| Television writing credits and WGA series | `tv_shares.csv`, `tv_kilroys_2014_17.csv`, `tv_event.csv`, `wga_series.csv` |
| How reliable is the data? | `audit_rates.csv`, `recall_rates.csv`, `completion_rates.csv`, `classification_coverage.csv` |

## Definitions in one paragraph

- **Unit:** an announced production of a title by a theatre in a season, from *American Theatre* magazine's season listings for TCG member theatres.
- **Seasons:**
  - print listings: 2010-11 to 2019-20
  - online listings: 2022-23 to 2025-26
  - 2020-22 was not published, and is a gap, not zero
- **Main comparison:** 2015-19 against 2022-25, with a check that leaves out the disrupted 2019-20 season.
- **"Contemporary" excludes:**
  - Shakespeare, *A Christmas Carol*, and works first staged before 1960
  - readings, festivals, tours, concerts and dance
- **Co-productions** count once.
- **Writers** exclude source authors (the novelist behind an adaptation is not its playwright).
- **Fixed panel:** theatres listed in at least 8 of 10 print seasons and 3 of 4 online seasons.

## Things to know before using the numbers

- **Announced, not completed.** Most announced productions ran, but 2019-20 runs that reached March 2020 mostly did not (`completion_rates.csv`).
- **"Straight plays" are not comparable across eras.** The online listings classify far more shows, so use the "plays, era-neutral" rows.
- **The royalty figures are a model** built on stated assumptions, not observed payments.
- **Licensing shares** use each title's licensor today, applied backwards. They are not historical market shares.
- **Data quality is measured, not assumed.** Error rates and extraction recall are in `audit_rates.csv` and `recall_rates.csv`.

## Citation and licence

Data: CC BY 4.0 (see [LICENSE-DATA](LICENSE-DATA)). Please cite as in [CITATION.cff](CITATION.cff):

> Harbour, Jared (2026). *The Playwright Economy: corrected summary dataset*, v1.0. https://github.com/jharbour24/playwright-economy-data
