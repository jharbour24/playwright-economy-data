# Data dictionary

All files are in `data/dataset/`. All values are aggregates. Seasons run August-July (`start` = first year).
Percentages are 0-100. `ci95_low` / `ci95_high` are 95% intervals. Money is US dollars; 'real' means 2024 dollars (CPI-U).

## acquisitions_concord_newly_available_by_month.csv

Concord's monthly 'newly available' lists, January 2025 to September 2026: titles and plays per month.

21 rows. Columns: `month`, `after_blg_acquisition`, `titles`, `plays`, `musicals`, `unparsed_type`, `post_present`, `note`, `label`

## acquisitions_concord_newly_available_lag.csv

Years from premiere to 'newly available' for plays, before and after Concord acquired Broadway Licensing (May 2025).

2 rows. Columns: `period`, `posts`, `titles`, `titles_per_post`, `plays`, `plays_per_post`, `musicals`, `plays_with_lag`, `lag_median_years`, `lag_median_ci95`, `lag_p25`, `lag_p75`, `lag_mean`, `lag_share_within_5y_pct`, `note`, `label`

## acquisitions_concord_newly_available_newcomers.csv

Share of newly available plays whose lead author had no listed production before the post's season.

2 rows. Columns: `period`, `plays`, `lead_author_never_listed_before_post_season`, `pct`, `ci95`, `note`, `label`

## acquisitions_dps_new_plays.csv

Dramatists Play Service new plays per catalogue year and the share by authors new to DPS.

18 rows. Columns: `catalogue`, `period`, `new_plays`, `index_entries`, `lead_authors`, `lead_authors_new_to_dps`, `new_author_share_pct`, `flag`, `label`

## afterlife_broadway_coverage.csv

Broadway productions in the comparison windows by type and whether they match a listed contemporary work.

14 rows. Columns: `period`, `master_show_type`, `match`, `broadway_productions`, `label`

## afterlife_licensing_by_type.csv

Share of productions of each type whose title is held today by any checked licensing house, by Concord's pre-merger imprints, by today's combined Concord catalogue, or by none; raw, verified-only and precision-adjusted, with intervals. Current catalogues applied backwards, not historical market share.

360 rows. Columns: `group`, `measure`, `basis`, `share_pct`, `ci95_low`, `ci95_high`, `n_productions`, `n_works`, `label`, `licensing`

## afterlife_licensing_differences.csv

Differences in licensing shares between second-and-later productions and launches, and over time, with intervals.

14 rows. Columns: `period`, `measure`, `comparison`, `difference_pts`, `ci95_low`, `ci95_high`, `label`, `basis`, `licensing`

## afterlife_type_counts.csv

Productions by type (launch, second production, third or later, later with launch unobserved, launch-theatre return, Broadway run) and period.

12 rows. Columns: `period`, `type`, `productions`, `works`, `combined_entity_productions`, `imprint_unknown_productions`, `imprint_known_pct_of_combined`, `label`, `licensing`

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

## deep_cutting_difference.csv

Difference in newcomer-share change between deep-cutting and other theatres, with interval.

1 rows. Columns: `comparison`, `difference_pts`, `ci95_low`, `ci95_high`, `n_deep`, `n_rest`, `original_extraction`, `label`, `cluster`

## deep_cutting_intervals.csv

Bootstrap intervals for the deep-cutting theatre groups.

24 rows. Columns: `group`, `measure`, `period`, `share_pct`, `ci95_low`, `ci95_high`, `label`, `cluster`

## deep_cutting_theatres.csv

Theatres grouped by how much they cut contemporary productions (cut 30% or more; 10-30%; under 10% or grew): season sizes, newcomer and house-writer shares before and after.

4 rows. Columns: `group`, `theatres`, `mean_season_size_pre`, `mean_season_size_post`, `median_theatre_change_pct`, `productions_with_credit_pre`, `productions_with_credit_post`, `newcomer_share_pre_pct`, `newcomer_share_post_pct`, `newcomer_change_pts`, `house_writer_share_pre_pct`, `house_writer_share_post_pct`, `house_writer_n_pre`, `house_writer_n_post`, `sample`, `label`

## demand_index.csv

Index (2014-19 = 100): Broadway play and musical attendance, regional contemporary productions, era-neutral plays, Equity LORT work weeks.

15 rows. Columns: `start`, `broadway_play_attendance`, `broadway_musical_attendance`, `regional_contemporary_productions`, `regional_plays_productions`, `lort_work_weeks`, `base`

## exclusion_counts.csv

Per season: listing rows removed by each exclusion (readings, festivals/series/talks, tours, TBA, concerts/revues, dance).

84 rows. Columns: `season`, `exclusion`, `rows_removed`

## fees_comparability_check.csv

Why historical DPS catalogue fees and Concord 2026 per-performance minimums cannot be compared as a price change.

5 rows. Columns: `item`, `evidence`, `label`

## fees_minimum_by_imprint.csv

Concord title-page per-performance minimum fees (amateur/stock, retrieved 2026-09-27) by imprint and work type: median and quartiles. Titles from the AT top lists, not a random sample.

6 rows. Columns: `imprint`, `work_type`, `n`, `median_usd`, `p25_usd`, `p75_usd`, `min_usd`, `max_usd`, `quoted_on_application`, `basis`, `sample`, `label`

## gap_followup.csv

Descriptive only: 2014-18 cohorts reaching another theatre before 2020 and listed elsewhere in 2022-25 (the 2020-22 gap is unobserved).

5 rows. Columns: `cohort`, `titles`, `reached_before_2020_pct`, `listed_elsewhere_2022_25_pct`, `note`

## house_writer_share.csv

Per season and period means: share of a theatre's productions whose lead writer was produced by the same theatre in its previous four listed seasons, with sensitivities and intervals.

78 rows. Columns: `measure`, `universe`, `season`, `n_productions`, `share_pct`, `ci95_low`, `ci95_high`, `theatres_clusters`, `label`, `rows`, `cluster`

## income_amateur_coverage_gap.csv

Credited writers whose titles sit at houses with no production feed (MTI, TRW, Broadway Play Publishing): amateur income not estimated, not zero.

2 rows. Columns: `era`, `credited_writers_in_era`, `with_concord_now_playing_income`, `title_at_other_checked_house_mti_trw_bpp`, `only_other_checked_houses_no_concord_title`, `no_title_in_any_checked_house`, `amateur_income_not_estimated_other_house_titles`, `note`, `label`

## income_amateur_edta_check.csv

Cross-check: where EdTA top-list titles held by Concord rank in the modeled amateur income, with rank correlations.

4 rows. Columns: `category`, `edta_concord_titles`, `found_in_now_playing`, `median_percentile_of_est_income_among_now_playing_titles`, `pct_in_top_10pct`, `spearman_edta_mean_rank_vs_est_income_rank`, `p_value`, `spearman_edta_appearances_vs_est_income_rank`, `p_value_appearances`, `titles_not_found`, `note`, `label`

## income_amateur_effect.csv

How many writers cross $25k and $40k only because of the amateur layer, and the imprint group of their amateur titles.

16 rows. Columns: `scenario`, `era`, `threshold`, `over_per_season_professional_only`, `over_per_season_with_amateur`, `added_per_season`, `added_listed_this_season`, `added_not_listed_this_season`, `added_mainly_blg_imprint_titles`, `added_mainly_premerger_concord_titles`, `added_mainly_imprint_not_recorded`, `distinct_writers_added`, `note`, `label`

## income_amateur_market.csv

Modeled annual amateur, school, college and community productions and licence revenue for Concord titles, by venue type, fee basis and work type.

11 rows. Columns: `venue_type`, `rows_sample`, `rows_census_titles`, `est_annual_productions_central`, `performances_per_production`, `est_licence_revenue_central`, `note`, `label`

## income_amateur_sampling.csv

Correction of the Concord 'Now Playing' sample: draws, unique rows, estimated list size, inclusion probability (theory and census check), turnover guide, professional rows removed.

26 rows. Columns: `item`, `value`, `label`

## income_amateur_turnover_sensitivity.csv

How the amateur layer changes with the assumed annual turnover of the 'Now Playing' list.

7 rows. Columns: `turnover_per_year`, `est_annual_productions`, `est_licence_revenue`, `est_author_income_all_authors`, `authors_over_25000`, `authors_over_40000`, `label`

## income_box_office.csv

Estimated gross per production by two methods (performances x seats x occupancy x ticket income; and the m12 method), 990 match rate, run-date coverage and estimated performances.

6 rows. Columns: `era`, `theatres`, `productions`, `pct_of_productions`, `theatres_n`, `pct_with_listed_run_dates`, `median_run_days`, `mean_performances_est`, `tcg_performances_per_production`, `median_gross_method_b`, `mean_gross_method_b`, `median_gross_method_a_m12`, `mean_gross_method_a_m12`, `match_note`, `label`

## income_concord_flow.csv

Share of modeled author income passing through today's combined Concord catalogue.

8 rows. Columns: `scenario`, `era`, `share_through_combined_concord_pct`, `of_which_licensed_professional_pct`, `of_which_amateur_pct`, `professional_only_share_through_combined_concord_pct`, `note`, `licensing`, `label`

## income_fee_sources.csv

Where each production's per-performance fee comes from (title minimum, imprint median, all-imprint median, assumed musical fee).

16 rows. Columns: `era`, `layer`, `fee_src`, `productions`, `label`

## income_m12_replication.csv

The earlier royalty estimate (m12) re-run on the corrected build: writers per season, median and 90th-percentile royalty, writers over $10k/$25k/$40k at 5/6/8% royalty, old and corrected side by side.

6 rows. Columns: `royalty_rate`, `era`, `writers_per_season_m12`, `writers_per_season_corrected`, `median_royalty_m12`, `median_royalty_corrected`, `p90_royalty_m12`, `p90_royalty_corrected`, `over_10000_m12`, `over_10000_corrected`, `over_25000_m12`, `over_25000_corrected`, `over_40000_m12`, `over_40000_corrected`, `label`

## income_m12_replication_diagnostics.csv

Inputs behind the replication: box-office basis, Trend Theatre default, production counts.

4 rows. Columns: `item`, `m12`, `corrected`, `label`

## income_monte_carlo.csv

1,000 draws over every assumption range: 10th, 50th and 90th percentile of writers per season over $25k and $40k, by era and change, with and without agent commission and the standard split.

48 rows. Columns: `agent_commission`, `author_share`, `layers`, `threshold`, `era`, `p10`, `p50`, `p90`, `mean`, `draws`, `pct_draws_post_below_pre`, `note`, `label`

## income_newcomers.csv

Modeled income for newcomers, previously observed writers and writers with amateur income only.

24 rows. Columns: `scenario`, `era`, `group`, `writers_per_season`, `median_income`, `p90_income`, `over_25000_per_season`, `over_40000_per_season`, `amateur_share_of_income_pct`, `note`, `label`

## income_premieres_vs_licensed.csv

Productions classed as premieres (launches) or licensed later productions, with the r2 types, reclassifications and licensing shares.

17 rows. Columns: `era`, `layer`, `productions`, `per_season`, `pct_in_combined_concord`, `pct_any_checked_house`, `label`

## income_professional_by_layer.csv

Modeled writer income from premieres and licensed professional productions, per season, by scenario, box-office method and fee basis.

64 rows. Columns: `scenario`, `box_office_method`, `licensed_fee_basis`, `era`, `layer`, `productions`, `writer_income_total_per_season`, `mean_per_production`, `median_per_production`, `through_combined_concord_pct`, `dollars`, `agent_commission`, `author_share_note`, `label`

## income_sensitivity.csv

Each assumption moved to its low and high end, one at a time: writers over $40k per season, ranked by swing.

22 rows. Columns: `rank`, `parameter`, `label`, `low`, `central`, `high`, `pre_at_low`, `post_at_low`, `pre_at_high`, `post_at_high`, `post_swing`, `pre_swing`, `central_over_40000_pre`, `central_over_40000_post`, `note`

## income_shares_by_layer.csv

Share of modeled income from premieres, licensed professional productions and amateur licensing.

8 rows. Columns: `scenario`, `era`, `aggregate_share_premiere_pct`, `aggregate_share_licensed_pct`, `aggregate_share_amateur_pct`, `mean_writer_share_premiere_pct`, `mean_writer_share_licensed_pct`, `mean_writer_share_amateur_pct`, `over_40k_mean_writer_share_premiere_pct`, `over_40k_mean_writer_share_licensed_pct`, `over_40k_mean_writer_share_amateur_pct`, `writers_with_any_amateur_income_pct`, `note`, `label`

## income_standard_split.csv

What a standard 50/50 licence split leaves the playwright: fees collected by houses, the house's half, the writer's half before and after a 10% agent commission, and threshold counts.

2 rows. Columns: `era`, `author_share`, `writer_seasons`, `licence_fees_collected_by_houses_per_season`, `house_keeps_per_season`, `playwrights_receive_per_season`, `playwrights_receive_after_agent_per_season`, `income_not_through_a_house_per_season_premieres_direct_licences`, `median_writer_house_fees_full`, `median_writer_share_of_fees`, `p90_writer_house_fees_full`, `p90_writer_share_of_fees`, `median_total_income_before_agent`, `median_total_income_after_agent`, `p90_total_income_before_agent`, `p90_total_income_after_agent`, `over_25000_if_author_kept_100pct`, `over_25000_after_split`, `over_25000_after_split_and_agent`, `over_40000_if_author_kept_100pct`, `over_40000_after_split`, `over_40000_after_split_and_agent`, `note`, `label`

## income_summary.csv

Modeled income per writer-season by era: median, 90th percentile, writers over $25k, $40k and a NYC living wage, for low / central / high assumptions and a standard 50/50 licence split, agent commission on and off, credited-split and lead-only.

64 rows. Columns: `scenario`, `writers`, `agent_commission`, `era`, `layers`, `writer_seasons`, `median_income`, `p90_income`, `over_25000_per_season`, `over_40000_per_season`, `over_nyc_living_wage_per_season`, `amateur_tier`, `note`, `label`

## income_writers_by_season_load.csv

Observed: writers with 1, 2, 3 or 4+ listed productions in a season, all and by newcomer status.

12 rows. Columns: `era`, `basis`, `group`, `writers_1_production_per_season`, `writers_2_productions_per_season`, `writers_3_productions_per_season`, `writers_4_plus_productions_per_season`, `pct_1`, `pct_2`, `pct_3`, `pct_4_plus`, `label`

## income_writers_per_season.csv

Observed: distinct lead and credited writers per season, newcomers vs previously observed, and writers with a title in today's combined Concord catalogue or any checked house.

4 rows. Columns: `era`, `basis`, `distinct_writers_per_season`, `newcomers_per_season`, `previously_observed_per_season`, `with_title_in_combined_concord_per_season`, `pct_combined_concord`, `with_title_in_any_checked_house_per_season`, `pct_any_checked_house`, `note`, `label`

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

## lort_work_weeks.csv

Actors' Equity LORT work weeks by season, from Equity's annual reports (URL per row).

21 rows. Columns: `season`, `season_start_year`, `lort_work_weeks`, `source_url`

## merger_broadway_catalogue_check.csv

Share of newly observed plays with a verified Broadway run whose title is in today's combined Concord catalogue, against regional-only plays of the same cohorts (descriptive; selection is obvious).

9 rows. Columns: `cohorts`, `measure`, `broadway_plays_n`, `broadway_share_pct`, `regional_only_n`, `regional_only_share_pct_reweighted`, `difference_pts`, `ci95_low`, `ci95_high`, `label`, `licensing`, `precision_note`

## merger_concentration_path.csv

Concentration of licensed afterlife productions at four dates (before and after each merger), today's catalogue held fixed: largest owner's share of all productions and of house-held productions, and HHI. Structural: the mergers alone, not observed market behaviour.

72 rows. Columns: `productions`, `base`, `unknown_imprint_rule`, `date`, `n_productions`, `n_works`, `excluded_unknown_imprint_productions`, `largest_owner`, `largest_owner_share_of_all_pct`, `ci_all`, `largest_owner_share_of_checked_house_pct`, `ci_checked`, `hhi_checked_houses`, `ci_hhi_checked`, `hhi_all_productions_no_house_titles_atomistic`, `ci_hhi_all`, `checked_house_share_pct`, `owner_groups`, `label`, `licensing`, `note`

## merger_owner_shares.csv

Productions held by each owner group at each of the four dates (today's catalogue held fixed).

132 rows. Columns: `productions`, `base`, `date`, `owner`, `productions_held`, `share_of_checked_house_pct`, `label`, `licensing`

## newcomer_name_variant_check.csv

Newly observed lead writers whose name closely matches an earlier listed writer (fuzzy ratio 88 or more): a check on name variants.

12 rows. Columns: `season`, `newly_observed_lead_writers`, `close_match_to_earlier_name_ratio_ge_88`, `pct`, `note`

## newcomer_repeat_check.csv

Share of productions whose title was listed at the same theatre in the preceding listed season (a check on the newcomer measure).

14 rows. Columns: `start`, `productions`, `same_title_same_theatre_prev_season`, `pct`, `note`

## newcomer_share.csv

Per season and 2015-19 / 2022-25 means: share of contemporary productions whose lead writer is newly observed (not listed in the previous four listed seasons), all theatres, 146-theatre panel and strict 71-theatre panel, with sensitivities; theatre-clustered bootstrap intervals.

156 rows. Columns: `measure`, `universe`, `season`, `n_productions`, `share_pct`, `ci95_low`, `ci95_high`, `theatres_clusters`, `label`, `look_back`, `cluster`

## panel_absences.csv

How missing seasons enter the fixed theatre panel: absent theatre-seasons and productions per listed theatre-season.

2 rows. Columns: `period`, `panel_theatres`, `theatre_seasons`, `absent_theatre_seasons`, `absent_pct`, `productions_per_season`, `productions_per_listed_theatre_season`, `strict_panel_theatres`, `strict14_theatres`

## pathways.csv

Per 100 new titles: second and third listed theatre, verified licensing catalogue, and Broadway within a fixed 3-season window.

3 rows. Columns: `cohort`, `subset`, `titles`, `second_theatre_later_seasons_pct`, `third_theatre_later_seasons_pct`, `second_theatre_incl_same_season_pct`, `third_theatre_incl_same_season_pct`, `licensed_concord_verified_by_2026_pct`, `broadway_window`, `broadway_by_2026_titles_unequal_followup`, `broadway_after_first_listing_titles`, `broadway_after_first_listing_pct`, `broadway_original_after`, `broadway_revival_after`, `broadway_same_season_as_first_listing_titles`, `broadway_before_first_listing_titles`, `broadway_ambiguous_candidates`, `broadway_rejected_candidates`

## recall_rates.csv

Share of source listing entries captured by the original and corrected extraction (hand-read sample, tuning and holdout).

6 rows. Columns: `extraction`, `columns`, `eligible_entries`, `recovered`, `recall_pct`, `ci95_low`, `ci95_high`, `false_rows`, `extracted_rows`, `false_row_pct`

## rolling_world_premiere_coverage.csv

How many Rolling World Premiere titles match the listings.

1 rows. Columns: `rwp_titles_in_nnpn_rwp`, `rwp_titles_matched_to_listings_cohort_works`, `title_only_hits_excluded`, `rwp_fiscal_years`

## rolling_world_premiere_travel.csv

NNPN Rolling World Premiere titles vs other multi-theatre launches of the same cohorts: share reaching a production outside the launch set (descriptive).

5 rows. Columns: `era`, `horizon_seasons`, `rwp_matched_titles`, `rwp_reach_pct`, `rwp_at_risk`, `comparison_titles`, `comparison_reach_pct`, `difference_pts`, `ci95_low`, `ci95_high`, `rwp_launch_types`, `comparison`, `match`, `label`

## royalty.csv

Production-royalty model at 5%, 6% and 8%: writers per season above $10k, $25k and $40k, under alternative co-writer and completion assumptions.

24 rows. Columns: `royalty_rate`, `co_writers`, `completion`, `period`, `writers_per_season`, `pct_one_production`, `median_royalty`, `p90_royalty`, `writers_over_10000_per_season`, `writers_over_25000_per_season`, `writers_over_40000_per_season`, `dollars`, `box_office_basis_share_theatre_990`

## sample_survival.csv

Per season: listing rows surviving each filter (exclusions, co-productions, classics) down to contemporary productions, by repertoire category and fixed panel.

14 rows. Columns: `season`, `era`, `listed_rows`, `eligible_rows`, `eligible_productions`, `coproduction_rows_merged`, `classic_christmas_carol`, `classic_shakespeare`, `classic_pre1960`, `contemporary_productions`, `contemporary_straight_play`, `contemporary_musical`, `contemporary_uncertain`, `contemporary_new_adaptation_of_classic`, `fixed_panel_contemporary`, `contemporary_writer_ok`, `contemporary_writer_missing`, `contemporary_writer_unparsed`, `classification_coverage_pct`, `writer_missing_or_unresolved_pct`

## school_market_concord_play_vs_musical.csv

The same snapshot split into plays, musicals and unclassified titles.

3 rows. Columns: `kind`, `productions`, `school`, `college`, `community`, `other`, `share_of_productions_pct`, `titles`, `note`, `label`

## school_market_concord_title_concentration.csv

The same snapshot: concentration of productions across titles (top-10, top-50, top-100 shares, HHI).

3 rows. Columns: `titles`, `productions`, `top10_share_pct`, `top50_share_pct`, `top100_share_pct`, `hhi_across_titles`, `titles_with_1_production_pct`, `subset`, `note`, `label`

## school_market_concord_venue_types.csv

Concord 'Now Playing' snapshot (2026-09-30, a ~63% random sample of current and announced productions): productions by venue type inferred from organisation names.

4 rows. Columns: `venue_type`, `productions`, `share_pct`, `note`, `label`

## school_market_edta_lists.csv

Educational Theatre Association top-10 lists by survey year and category: largest licensor at the survey date and the share held by today's combined Concord (ranked titles, not production counts).

16 rows. Columns: `survey_year`, `category`, `listed_entries`, `section_complete`, `entries_with_licensor`, `largest_owner_at_survey_date`, `largest_owner_share_pct`, `concord_at_survey_date_pct`, `combined_entity_today_share_of_entries_pct`, `combined_entity_today_top10_slots`, `top10_slots`, `combined_entity_today_distinct_titles_pct`, `owners_at_survey_date`, `note`, `label`, `licensing`

## tcg_panels.csv

TCG Trend Theatre panels (84 theatres 2015-19; 137 theatres 2019-23, kept separate): attendance per performance, real ticket income per attendee, expenses per production, federal support.

10 rows. Columns: `panel`, `year`, `attendance_aggregate`, `performances_aggregate`, `productions_aggregate`, `attendance_per_performance`, `real_ticket_income_per_attendee`, `real_expenses_per_theatre`, `real_expenses_per_production`, `earned_income_pct_of_expenses`, `ticket_income_pct_of_expenses`, `federal_support_per_theatre_nominal`, `federal_support_per_theatre_real`, `dollars`, `productions_note`

## tcg_trend_windows.csv

TCG Theatre Facts headline series by edition: each edition's Trend Theatre panel, first and last year of its window, values and % change (subscribers, attendance, performances, productions where printed).

95 rows. Columns: `edition`, `metric`, `first_year`, `last_year`, `first_value`, `last_value`, `change_pct`, `n_trend_theatres`

## theatre_finance_differences.csv

Differences between budget and net-asset thirds, with intervals.

6 rows. Columns: `split`, `difference`, `estimate`, `ci95_low`, `ci95_high`, `n_richest`, `n_poorest`, `label`, `cluster`

## theatre_finance_match_rate.csv

How many listed theatres are matched to an IRS Form 990 (searches covered only the original panel, leavers and closures).

5 rows. Columns: `universe`, `theatres`, `matched_to_990`, `match_rate_pct`, `note`, `label`

## theatre_finance_terciles.csv

Matched theatres split into thirds by 2015-19 real expenses and by real net assets: season-size change and newcomer shares.

6 rows. Columns: `split`, `tercile`, `theatres`, `range_2024usd`, `season_size_pre`, `season_size_post`, `season_change_pct`, `newcomer_slots_per_season_pre`, `newcomer_slots_per_season_post`, `newcomer_share_pre_pct`, `newcomer_share_post_pct`, `dollars`, `label`

## title_travel_by_writer_history.csv

Share of newly observed works reaching a theatre outside the launch set within two seasons, for newly observed vs previously observed lead writers.

2 rows. Columns: `titles_by`, `n_pre`, `reach_2_seasons_pre_pct`, `n_post`, `reach_2_seasons_post_pct`, `change_pts`, `ci95_low`, `ci95_high`, `method`, `label`

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

## writer_return_by_first_theatre.csv

Share of newly observed lead writers listed again within two seasons (Kaplan-Meier), by whether their first theatre cut deeply.

8 rows. Columns: `era`, `group`, `writers`, `at_risk_t2`, `listed_again_within_2_seasons_pct`, `ci95_low`, `ci95_high`, `method`, `r1_reference`, `label`

## writer_status.csv

Per season: contemporary productions with a usable writer credit, a missing credit, or an unresolvable credit.

14 rows. Columns: `season`, `era`, `contemporary_productions`, `contemporary_writer_ok`, `contemporary_writer_missing`, `contemporary_writer_unparsed`, `writer_missing_or_unresolved_pct`
