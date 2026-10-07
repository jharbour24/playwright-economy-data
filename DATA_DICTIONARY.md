# Data dictionary

All files are in `data/dataset/`. All values are aggregates. Seasons run August-July (`start` = first year).
Percentages are 0-100. `ci95_low` / `ci95_high` are 95% intervals. Money is US dollars; 'real' means 2024 dollars (CPI-U).

## audit_rates.csv

Random audit of the corrected listings against source pages: error rates with 95% intervals by field and stratum.

29 rows. Columns: `stratum`, `field`, `errors`, `n`, `error_pct`, `ci95_low`, `ci95_high`, `source_errors`

## broadway_by_season.csv

Broadway attendance, grosses and average ticket prices by season and show type, nominal and real (2024 dollars, three deflation conventions).

30 rows. Columns: `season`, `start`, `type`, `weeks`, `attendance`, `gross_nominal`, `avg_ticket_nominal`, `avg_ticket_real_weekly`, `avg_ticket_real_season`, `avg_ticket_real_calendar`, `base`

## classification_coverage.csv

Per season: contemporary productions classified as straight play, musical, or uncertain, and the share classified.

14 rows. Columns: `season`, `era`, `contemporary_productions`, `contemporary_straight_play`, `contemporary_musical`, `contemporary_uncertain`, `classification_coverage_pct`

## completion_rates.csv

Stratified check of whether announced productions occurred, were curtailed, cancelled or postponed, or could not be verified.

42 rows. Columns: `stratum`, `drawn`, `checked`, `status`, `count`, `pct`, `ci95_low`, `ci95_high`

## concentration_by_season.csv

Per season: theatres' shares of production slots (HHI, effective number of theatres, top-10/20 shares, mean and median season size).

42 rows. Columns: `start`, `slots`, `active_theatres`, `hhi`, `effective_theatres`, `top10_share_pct`, `top20_share_pct`, `mean_per_theatre`, `median_per_theatre`, `universe`, `allocation`

## concentration_periods.csv

Period means and changes of the concentration measures.

24 rows. Columns: `universe`, `measure`, `pre_2015_19`, `pre_2015_18`, `post_2022_25`, `change`, `pct_change`, `change_excl_2019`, `pct_change_excl_2019`

## coverage_bridge.csv

The 2015-19 to 2022-25 change in productions per season split by theatre group (unrounded).

6 rows. Columns: `group`, `pre`, `post`, `change`, `share_of_total_change_pct`

## coverage_groups.csv

Theatres listed in both periods, only before, or only after: theatre counts, productions per season, season size.

10 rows. Columns: `group`, `period`, `theatres_total`, `theatres_listed_per_season`, `productions_per_season`, `productions_per_listed_theatre`

## coverage_writers.csv

Distinct lead writers per period, and how many were produced only at theatres that left or joined the listings.

2 rows. Columns: `period`, `distinct_lead_writers_pooled`, `at_both_group_theatres`, `at_departed_theatres`, `at_both_kinds`, `only_at_departed_theatres`, `at_new_theatres`, `only_at_new_theatres`

## decline_by_season.csv

Per season and universe: productions, productions with a usable credit, distinct works, distinct lead writers, distinct credited writers, missing-credit share.

224 rows. Columns: `start`, `productions`, `with_usable_credit`, `missing_or_unresolved`, `missing_pct`, `distinct_works`, `distinct_lead_writers`, `distinct_relevant_writers`, `universe`

## decline_periods.csv

2015-19 vs 2022-25 means (and the 2015-18 check) for each universe and measure, with previous (pre-correction) results for comparison.

98 rows. Columns: `universe`, `measure`, `source`, `pre_2015_19`, `pre_2015_18`, `post_2022_25`, `change`, `pct_change`, `change_excl_2019`, `pct_change_excl_2019`

## decomposition.csv

Random thinning of 2015-19 seasons to 2022-25 volume (1,000 simulations, seed 20261006): writers expected from volume alone vs observed, under three benchmarks.

14 rows. Columns: `repertoire`, `theatres`, `writer_measure`, `pre_productions_usable`, `post_productions_usable`, `missing_credit_excluded_pre`, `missing_credit_excluded_post`, `writers_before`, `writers_after`, `observed_decline`, `observed_pct`, `random_expected`, `random_interval`, `random_reproduced`, `random_difference_from_benchmark`, `random_pct_of_decline_reproduced`, `theatre_preserving_expected`, `theatre_preserving_interval`, `theatre_preserving_reproduced`, `theatre_preserving_difference_from_benchmark`, `theatre_preserving_pct_of_decline_reproduced`, `continuing_theatres_writers_before`, `continuing_theatres_writers_after`, `observed_contraction_productions_sampled`, `continuing_theatres_productions_after`, `observed_contraction_sampled_total_equals_target`, `observed_contraction_expected`, `observed_contraction_interval`, `observed_contraction_difference_from_benchmark`, `observed_contraction_pct_of_decline_reproduced`, `seed`, `simulations`

## demand_index.csv

Index (2014-19 = 100): Broadway play and musical attendance, regional contemporary productions, era-neutral plays, Equity LORT work weeks.

15 rows. Columns: `start`, `broadway_play_attendance`, `broadway_musical_attendance`, `regional_contemporary_productions`, `regional_plays_productions`, `lort_work_weeks`, `base`

## exclusion_counts.csv

Per season: listing rows removed by each exclusion (readings, festivals/series/talks, tours, TBA, concerts/revues, dance).

84 rows. Columns: `season`, `exclusion`, `rows_removed`

## gap_followup.csv

Descriptive only: 2014-18 cohorts reaching another theatre before 2020 and listed elsewhere in 2022-25 (the 2020-22 gap is unobserved).

5 rows. Columns: `cohort`, `titles`, `reached_before_2020_pct`, `listed_elsewhere_2022_25_pct`, `note`

## irs_panel.csv

IRS Form 990 balanced panel (90 organisations, tax years 2012-23): revenue, expenses, contributions, program-service revenue, ratios, and counts with revenue below expenses.

12 rows. Columns: `tax_year`, `organisations`, `total_revenue_real`, `total_expenses_real`, `contributions_real`, `program_revenue_real`, `aggregate_program_revenue_pct_of_expenses`, `mean_theatre_program_revenue_pct_of_expenses`, `median_theatre_program_revenue_pct_of_expenses`, `aggregate_contributions_pct_of_expenses`, `negative_revenue_minus_expenses`, `sensitivity_excl_short_period_orgs_negative_balances`, `sensitivity_excl_short_period_orgs_psr_pct`, `sensitivity_orgs`, `panel`, `dollars`, `caution`

## km.csv

Kaplan-Meier estimates by season: share of newly observed titles produced at another listed theatre, with titles at risk, events, censoring and 95% intervals.

55 rows. Columns: `t`, `at_risk`, `events`, `censored`, `reach_pct`, `ci95_low`, `ci95_high`, `variant`, `era`, `cohort`, `cohort_size`

## km_summary.csv

Kaplan-Meier summary: probability of a second listed theatre within 2, 3 and 5 seasons, by cohort and sensitivity variant.

15 rows. Columns: `variant`, `era`, `cohort`, `titles`, `events_total`, `censored_total`, `same_theatre_return_pct`, `multi_theatre_launch_pct`, `reach_by_2`, `reach_by_3`, `reach_by_5`

## launch_types.csv

Newly observed titles by launch type: single theatre, joint production, independent same-season launches.

30 rows. Columns: `era`, `launch_type`, `titles`, `variant`

## licensing_match_quality.csv

Precision of the title match to Concord pages, by era, from author-checked pages.

2 rows. Columns: `era`, `slug_matches_checked`, `author_verified`, `precision`, `note`

## licensing_shares.csv

Per season: Concord's current representation of listed contemporary titles and productions (title match, precision-adjusted, verified lower bound).

14 rows. Columns: `start`, `works`, `productions`, `concord_slug_share_of_works_pct`, `concord_slug_share_of_productions_pct`, `concord_share_among_licensor_matched_works_pct`, `licensor_matched_share_of_works_pct`, `concord_precision_adjusted_share_of_works_pct`, `concord_verified_share_of_works_pct_lower_bound`, `label`

## licensing_timeline.csv

Dated licensing transactions with sources: historical consolidation, Concord-Broadway Licensing Global (2025), BMG-Concord (2026).

15 rows. Columns: `event_date`, `date_precision`, `phase`, `parties`, `entity`, `event_type`, `description`, `source_url`

## panel_absences.csv

How missing seasons enter the fixed theatre panel: absent theatre-seasons and productions per listed theatre-season.

2 rows. Columns: `period`, `panel_theatres`, `theatre_seasons`, `absent_theatre_seasons`, `absent_pct`, `productions_per_season`, `productions_per_listed_theatre_season`, `strict_panel_theatres`, `strict14_theatres`

## pathways.csv

Per 100 new titles: second and third listed theatre, verified licensing catalogue, and Broadway within a fixed 3-season window.

3 rows. Columns: `cohort`, `subset`, `titles`, `second_theatre_later_seasons_pct`, `third_theatre_later_seasons_pct`, `second_theatre_incl_same_season_pct`, `third_theatre_incl_same_season_pct`, `licensed_concord_verified_by_2026_pct`, `broadway_window`, `broadway_by_2026_titles_unequal_followup`, `broadway_after_first_listing_titles`, `broadway_after_first_listing_pct`, `broadway_original_after`, `broadway_revival_after`, `broadway_same_season_as_first_listing_titles`, `broadway_before_first_listing_titles`, `broadway_ambiguous_candidates`, `broadway_rejected_candidates`

## recall_rates.csv

Share of source listing entries captured by the original and corrected extraction (hand-read sample, tuning and holdout).

6 rows. Columns: `extraction`, `columns`, `eligible_entries`, `recovered`, `recall_pct`, `ci95_low`, `ci95_high`, `false_rows`, `extracted_rows`, `false_row_pct`

## royalty.csv

Production-royalty model at 5%, 6% and 8%: writers per season above $10k, $25k and $40k, under alternative co-writer and completion assumptions.

24 rows. Columns: `royalty_rate`, `co_writers`, `completion`, `period`, `writers_per_season`, `pct_one_production`, `median_royalty`, `p90_royalty`, `writers_over_10000_per_season`, `writers_over_25000_per_season`, `writers_over_40000_per_season`, `dollars`, `box_office_basis_share_theatre_990`

## sample_survival.csv

Per season: listing rows surviving each filter (exclusions, co-productions, classics) down to contemporary productions, by repertoire category and fixed panel.

14 rows. Columns: `season`, `era`, `listed_rows`, `eligible_rows`, `eligible_productions`, `coproduction_rows_merged`, `classic_christmas_carol`, `classic_shakespeare`, `classic_pre1960`, `contemporary_productions`, `contemporary_straight_play`, `contemporary_musical`, `contemporary_uncertain`, `contemporary_new_adaptation_of_classic`, `fixed_panel_contemporary`, `contemporary_writer_ok`, `contemporary_writer_missing`, `contemporary_writer_unparsed`, `classification_coverage_pct`, `writer_missing_or_unresolved_pct`

## tcg_panels.csv

TCG Trend Theatre panels (84 theatres 2015-19; 137 theatres 2019-23, kept separate): attendance per performance, real ticket income per attendee, expenses per production, federal support.

10 rows. Columns: `panel`, `year`, `attendance_aggregate`, `performances_aggregate`, `productions_aggregate`, `attendance_per_performance`, `real_ticket_income_per_attendee`, `real_expenses_per_theatre`, `real_expenses_per_production`, `earned_income_pct_of_expenses`, `ticket_income_pct_of_expenses`, `federal_support_per_theatre_nominal`, `federal_support_per_theatre_real`, `dollars`, `productions_note`

## travel_model.csv

Descriptive logistic regression of reaching another theatre within 2 seasons: odds ratios and average marginal effects.

10 rows. Columns: `era`, `n`, `term`, `odds_ratio`, `or_ci95`, `p`, `avg_marginal_effect_pts`, `model`

## travel_predictors.csv

Probability a new title reaches another theatre within 2 or 3 seasons, by writer history, launch theatre budget third, and launch type, with differences, ratios and bootstrap intervals.

22 rows. Columns: `era`, `horizon_seasons`, `predictor`, `group`, `n_group`, `pct_group`, `reference`, `n_reference`, `pct_reference`, `difference_pts`, `diff_ci95`, `ratio`, `ratio_ci95`, `budget_years`

## tv_event.csv

Listed productions per season around a playwright's first TV writing credit (relative years -5 to +5), with a balanced-window check.

11 rows. Columns: `k`, `writers`, `observed`, `in_gap_season`, `mean_productions`, `balanced_window_mean_productions`, `balanced_window_writers_observed`, `balanced_window_writers`, `first_credit`

## tv_first_credit_uncertainty.csv

Difference between first TV credit year by episode and by series start (summary statistics).

8 rows. Columns: `statistic`, `difference_years`

## tv_kilroys_2014_17.csv

Kilroys 2014-17 lists: exact denominators and TV writing credit shares, per list and pooled.

10 rows. Columns: `lists`, `credit_measure`, `writers`, `matched_people`, `with_tv_writing_credit`, `pct_of_all_lower_bound`, `pct_of_matched`, `note`

## tv_shares.csv

Selected playwrights with a TV writing credit (IMDb-matched): share of everyone (lower bound) and of matched people, by group and credit definition.

16 rows. Columns: `group`, `credit_measure`, `people`, `matched`, `with_credit`, `pct_of_all_selected_lower_bound`, `pct_of_matched`

## wga_series.csv

WGA television writing employment series, kept separate by definition, with first-reported vs revised values and preliminary flags.

52 rows. Columns: `series_id`, `measure`, `period`, `value`, `vintage`, `preliminary`, `note`, `source_url`

## writer_return.csv

Kaplan-Meier: share of newly observed lead writers credited again within 2, 3 and 5 seasons.

16 rows. Columns: `definition`, `era`, `writers`, `t`, `at_risk`, `events`, `censored`, `reach_pct`, `ci95_low`, `ci95_high`

## writer_status.csv

Per season: contemporary productions with a usable writer credit, a missing credit, or an unresolvable credit.

14 rows. Columns: `season`, `era`, `contemporary_productions`, `contemporary_writer_ok`, `contemporary_writer_missing`, `contemporary_writer_unparsed`, `writer_missing_or_unresolved_pct`
