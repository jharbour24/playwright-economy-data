# Where the essay's numbers come from

Each figure in the essay, the file in `data/dataset/` that holds it, and the value there. Seasons run August–July;
"before" is the mean of 2015-16 to 2019-20 and "after" the mean of 2022-23 to 2025-26 unless stated.
Licensing figures apply today's catalogues backwards: they describe who holds the titles now, not historical market share.

## Broadway and the regional theatre

| Essay | Value in the data | File (where) |
|---|---|---|
| Broadway plays drew 52% more admissions than their pre-pandemic average | 3,412,575 in 2025-26 against a 2014-15 to 2018-19 mean of 2,244,587: +52.0% | `broadway_by_season.csv` (type = play) |
| Musicals barely budged (+2%) | 11,455,828 against 11,246,557: +1.9% | `broadway_by_season.csv` (type = musical) |
| Contemporary productions fell from about 1,800 to 1,300 a season (−27%) | 1,773.2 → 1,289.2, −27.3% | `decline_periods.csv` (contemporary, productions) |
| LORT work weeks still below pre-pandemic | 61,627 (2018-19) → 54,441 (2024-25) | `lort_work_weeks.csv` |
| Subscribers fell in nearly every five-year window since 2003 | Every TCG Trend window from 2003–07 to 2019–23 fell except 2018–22 (+12.0%) | `tcg_trend_windows.csv` (metric = subscribers) |
| Subscriptions back within about 1% of 2019 | 2019–23 window: −1.2% | `tcg_trend_windows.csv` (edition 2023) |
| 2015-19: theatres spent more, lost 4% of subscribers, ~73% capacity | Real expenses per theatre +12.0%; subscribers −4.1%; capacity 73.5% → 73.4% (84 Trend Theatres) | `tcg_panels.csv` (84-theatre panel) |
| 63 of 90 theatres' filings in the red by 2023, a 61.5% increase | 63 of 90 with revenue below expenses in 2023, from 39 in 2019 (+61.5%). Revenue minus expenses is not an operating deficit. | `irs_panel.csv` (`negative_revenue_minus_expenses`) |

## Writers and slots

| Essay | Value in the data | File (where) |
|---|---|---|
| Writers fell from 962 to 736 (226 fewer) | Distinct lead writers 961.8 → 736.0 (−225.8) | `decline_periods.csv` (contemporary, distinct_lead_writers) |
| Random cuts leave 764 writers; chance explains 198 of 226, nearly nine in ten | Expected after random thinning 763.3 (interval 755.2–771.2); 198.5 writers reproduced, 87.9% of the decline | `decomposition.csv` (contemporary, all theatres, lead writer) |
| Writers with 4+ productions: 8% → 7% | Lead writers: 8.2% → 7.0% | `income_writers_by_season_load.csv` |
| 35 fewer theatres staged contemporary work (360 vs 325) | Active theatres 359.8 → 324.5 | `concentration_periods.csv` |
| Twenty biggest theatres: 14% → 16% of productions | Top-20 share 14.2% → 15.8% | `concentration_periods.csv` |
| Newcomers' share rose from 26% to 30% | Newly observed lead writers' share of productions 26.2% → 30.0% | `newcomer_share.csv` (all theatres, period means) |
| Returning (house) writers' share fell | House-writer share 17.2% → 14.7% (all theatres); 16.5% → 13.5% (146-theatre panel) | `house_writer_share.csv` |
| Newcomers fell from about 430 to 360 a season | Productions by newcomers: about 429 → 359 a season (share × productions with a credit). Distinct newcomer writers: 391.8 → 315.5 | `newcomer_share.csv`, `income_writers_per_season.csv` |

## Second productions

| Essay | Value in the data | File (where) |
|---|---|---|
| New plays reach a second production at about 14% in both eras | Within two seasons: 14.4% → 13.7% | `km_summary.csv` (work identity, newly observed) |
| Established writers' odds up about 3 points, newcomers' down 3.2 | Titles by previously observed writers 20.0% → 23.1% (+3.1 pts); by newly observed writers 11.7% → 8.5% (−3.2 pts) | `title_travel_by_writer_history.csv` |
| A first-time playwright's odds of being produced again within two seasons: 24% → 19% | Newly observed lead writers listed again within two seasons: 23.8% → 19.4% | `writer_return.csv` (t = 2) |

## Licensing and the mergers

| Essay | Value in the data | File (where) |
|---|---|---|
| One in five first productions are of plays now held by a licensing house; three in five by the second or later | Any checked house: launches 22.2%; second-and-later 62.6% (both periods) | `afterlife_licensing_by_type.csv` (raw slug match) |
| Concord: 16% of first productions, nearly half of second-and-later, almost 60% of third or later | Combined Concord: launches 16.2% (2022-25), 17.5% (pooled); second-and-later 49.6%; third or later 57.5% (2022-25), 68.3% (2015-19) | `afterlife_licensing_by_type.csv` |
| Before the mergers, Samuel French and DPS each held about a third of the licensed afterlife | 34.0% and 32.7% of house-held second-and-later productions (before Dec 2018) | `merger_owner_shares.csv` |
| Largest owner's share of all second-and-later productions: 20% → 24% → 49% | 20.1% (Samuel French, before Dec 2018) → 24.0% (Concord, 2019) → 48.7% (Concord, after May 2025) | `merger_concentration_path.csv` (exclude rule, both periods) |
| Largest owner goes to more than three-quarters | Share of house-held productions: 34.0% → 77.9% | `merger_concentration_path.csv` |
| HHI rose from about 900 to 2,500 | 910 → 2,471 (all productions, no-house titles counted separately); among house-held productions 2,582 → 6,298 | `merger_concentration_path.csv` |
| 66% of plays with a Broadway run are in the Concord catalogue vs 14% of regional-only plays | 65.5% vs 15.0% (raw); 58.6% vs 11.0% (verified only) | `merger_broadway_catalogue_check.csv` (all cohorts) |
| EdTA lists: Concord titles fill half or more of the top full-length play slots and most one-act slots | Full-length plays: 50.0–70.0% each year, 2017-18 to 2022-23; one-acts: 62.5–88.9% | `school_market_edta_lists.csv` |
| About 60% of Concord's 'Now Playing' productions are for amateur markets | School 30.2% + college 9.6% + community 19.2% = 59.0% (the rest is 'other', which includes professional) | `school_market_concord_venue_types.csv` |

## Money

| Essay | Value in the data | File (where) |
|---|---|---|
| Concord lists a minimum of $130 per performance | Median title-page minimum $130 (Samuel French and DPS imprints; range $65–135) | `fees_minimum_by_imprint.csv` |
| Four performances: $520; after a 50% split and 10% commission, $234 | $130 × 4 × 0.5 × 0.9 = $234 | arithmetic |
| MIT living wage for one adult in Manhattan: $75,164 | $79,469 before tax (MIT Living Wage Calculator, New York County, 1 adult, 0 children, 2026 data), deflated to 2024 dollars | `config/r3_assumptions.yaml` |
| About 320 schools / 1,280 performances | $75,164 / $234 = 321.2, so 322 four-night productions (1,288 performances) | arithmetic |
| Footnote 1: Harry Potter and Stranger Things are 34% of 2025-26 play admissions; without them the rise is about 8% | 34.2%; +7.6% with both shows removed from both periods | Broadway weekly grosses (show-level source, not in this release) |

## The income model

The `income_*` tables estimate what produced playwrights might earn from premieres, later professional productions and
amateur licensing. They are models, not observed payments. Every assumption, its range and its source is in
[`config/r3_assumptions.yaml`](config/r3_assumptions.yaml), and `income_sensitivity.csv` ranks the assumptions by how much
they move the result. The author's share of a licence fee is a placeholder pending an interview; the
standard 50/50 split scenario is in `income_standard_split.csv`.
