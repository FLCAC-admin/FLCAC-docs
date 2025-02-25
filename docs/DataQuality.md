---
title: Data Quality Guidance
description: Details on assigning and interpreting data quality scores
abbreviations:
  FLCAC: Federal LCA Commons
  LCA: Life Cycle Assessment
  LCI: Life Cycle Inventory
---

:::{important}

Data quality scoring is highly encouraged for data on the FLCAC.
Users are recommended to use EPA's data quality system, which is available in the [Commons Core Database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets).
Additional information on the development of the system can be found in [EPA's Guidance on Data Quality Assessment for Life Cycle Inventory Data](https://cfpub.epa.gov/si/si_public_record_report.cfm?Lab=NRMRL&dirEntryId=321834).
:::

Data quality is assigned using numerical scores of 1-5.
In EPA's pedigree system, data that are of higher quality receive lower scores.
The matrices below are replicated from those published by [EPA](https://cfpub.epa.gov/si/si_public_record_report.cfm?Lab=NRMRL&dirEntryId=321834).

## Process level data quality

| Indicator  | 1 (highest)  | 2   | 3   | 4   | 5 (lowest)     |
|:----------:|:------------:|:---:|:---:|:---:|:--------------:|
| Process Review       |  Documented reviews by a minimum of two types[^1] of third party reviewers | Documented reviews by a minimum of two types of reviewers, with one being a third party | Documented review by a third party reviewer  | Documented review by an internal reviewer  | No documented review  |
| Process Completeness | >80% of determined flows have been evaluated and given a value   | 60-79% of determined flows have been evaluated and given a value   | 40-59% of determined flows have been evaluated and given a value | <40-59% of determined flows have been evaluated and given a value | Process completeness not scored |

[^1]: Types are defined as either industry or LCA experts

## Flow level data quality

| Indicator  | 1 (highest)  | 2   | 3   | 4   | 5 (lowest)     |
|:----------:|:------------:|:---:|:---:|:---:|:--------------:|
| Flow Reliability          | Verified[^2] data based on measurements   | Verified data based on a calculation OR non-verified data based on measurements    | Non-verified data based on a calculation     | Documented estimate   | Undocumented estimate    |
| Temporal Correlation      | Less than 3 years of difference[^3]  | Less than 6 years of difference  | Less than 10 years of difference    | Less than 15 years of difference   | Age of data unknown or more than 15 years    |
| Geographical Correlation  | Data from same resolution and same area of study.   | Within one level of resolution and a related area of study [^4] | Within two levels of resolution and a related area of study   | Outside of two levels of resolution but a related area of study    | From a different or unknown area of study    |
| Technological Correlation | All technology categories[^5] are equivalent   | Three of the technology categories are equivalent  | Two of the technology categories are equivalent  | One of the technology categories is equivalent   | None of the technology categories are equivalent  |
| Data Collection           | Representative data from >80% of the relevant market[^6], over an adequate period[^7] | Representative data from 60-79% of the relevant market over an adequate period  or representative data from >80% of the relevant market over a shorter period of time | Representative data from 40-59% of the relevant market over an adequate period  or representative data from >60-79% of the relevant market over a shorter period of time | Representative data from <40% of the relevant market over an adequate period  or representative data from >40-59% of the relevant market over a shorter period of time | Unknown or data from a small number of sites and from shorter periods |

[^2]: Verification may take place in several ways, e.g. by on-site checking, by recalculation, through mass balances or crosschecks with other sources. For values calculated from a mass-balance or another verification method, an independent verification method must be used in order to qualify the value as verified.

[^3]: Temporal difference refers to the difference between date of data generation and the date of representativeness as defined by the scope of the project.

[^4]: A related area of study is defined by the user and should be documented in the geographical metadata. The relationship established in the metadata of the unit process should be consistently applied to all flows within the unit process. Default relationship is established as within the same hierarchy of political boundaries (e.g. Denver is within Colorado, is within the USA, is within North America).

[^5]: Technology categories are process design, operating conditions, material quality, and process scale.

[^6]: The relevant market should be documented in the DQG. The default relevant market is measured in production units. If the relevant market is determined using other units, this should be documented in the DQG. The relevant market established in the metadata should be consistently applied to all flows within the unit process.

[^7]: Adequate time period can be evaluated as a time period long enough to even out normal fluctuations. The default time period is 1 year, except for emerging technologies (2-6 months) or agricultural projects >3 years.
