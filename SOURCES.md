# NYC Fiscal Sources — Full Outlook

A directory of the direct sources behind the NYC Council Fiscal Suite: the documents committed in this repo, plus the authoritative external sources for every part of the city's fiscal decision-making — City Council, OMB / the Mayor, the Comptroller, capital, open data, and the municipal market.

All embedded figures in the suite are tied out to these sources. Nothing is fabricated.

---

## 1. Committed in this repo (`/data` and root)

Direct source documents you can open straight from GitHub.

### Adopted budget — Schedule C (discretionary / member designations)
| Year | File |
|---|---|
| FY2022 | `Fiscal-2022-Schedule-C-Merge-6.30.21.pdf` |
| FY2023 | `data/Fiscal-2023-Schedule-C-Merge-6.13.22-Final-1.pdf` |
| FY2024 | `data/Fiscal-2024-Schedule-C-Merge-Final.pdf` |
| FY2025 | `data/Fiscal-2025-Schedule-C-MERGE-FINAL-2.pdf` |
| FY2026 | `Fiscal-2026-Schedule-C-4.pdf` |
| Parsed | `data/fy22_schedule_c.json` … `data/fy27_schedule_c.json` (structured, one row per designation) |

### Capital — §254 Council changes & supporting detail
- `data/FY23-Sec254-Capital-Supporting-Detail-Book.pdf`, `data/FY23-Sec254-Capital-ResoA-Book.pdf`
- `data/FY2024-Sec254-Supporting-Detail-Book_7.10.2023pwp-2.pdf`, `data/Fiscal-Year-2024-Changes-To-The-Executive-Capital-Budget-Adopted-by-the-City-Council.pdf`
- `data/FY25-Section-254-Supporting-Detail-Book-Council-Version-24.07.17.pdf`, `data/FIscal-Year-2025-Changes-to-the-Executive-Capital-Budget-Adopted-by-the-City-Council.pdf`
- `data/Fiscal-2026-Capital-Budget-Supporting-Details-1.pdf`

### Economic & tax forecast
- `data/Fiscal2026_Economic_and_Tax_Revenue_Forecast.pdf` · parsed: `data/nyc_council_tax_forecast_feb2026.json`

### Transparency Resolutions
- `data/FY27_Transparency_Reso_1_Report.pdf` · parsed: `data/fy27_transparency_reso_1.json`

### District 49 / North Shore master (curated, tied out to $39,627,090)
- `data/FY27_North_Shore_Codex.pdf`
- `data/D49_FY27_Full_Breakdown.docx` (245 items × 17 categories)
- `data/FY27_SI_EIN_Census_and_Reconciliation.xlsx` (v1) · `data/FY27_SI_EIN_Census_and_Reconciliation_v3.xlsx` (latest, 56-sheet reconciliation + EIN census)

---

## 2. NYC City Council — Finance Division
- **Budget hub (all years):** https://council.nyc.gov/budget/
- **FY2027:** https://council.nyc.gov/budget/fy2027/ · **FY2026:** https://council.nyc.gov/budget/fy2026/ (year hubs run back to FY2008)
- **Schedule C:** https://council.nyc.gov/budget/schedule-c/
- **Discretionary funding policies:** https://council.nyc.gov/budget/discretionary-funding-policies-and-procedures/
- **Interactive dashboards (Power BI):** https://council.nyc.gov/budget/dashboards/
- **Legislation (Legistar):** https://legistar.council.nyc.gov/ · API: https://webapi.legistar.com/v1/nyc/
- Marquee FY27 docs: [Financial Plan Overview](https://council.nyc.gov/budget/wp-content/uploads/sites/54/2026/03/Fiscal-2027-Financial-Plan-Overview.pdf) · [Preliminary Budget Response](https://council.nyc.gov/budget/wp-content/uploads/sites/54/2026/04/Fiscal-Year-2027-Preliminary-Budget-Response-2.pdf) · [Adopted Schedule C](https://council.nyc.gov/budget/wp-content/uploads/sites/54/2026/06/Fiscal-2027-Schedule-C-Final.pdf)

## 3. OMB / the Mayor — Office of Management & Budget
- **Publications (all financial plans, budgets):** https://www.nyc.gov/site/omb/publications/publications.page
- **OMB home:** https://www.nyc.gov/site/omb/index.page
- Financial plan stages: Preliminary (Jan) → Executive (Apr) → Adopted (Jun) → in-year Modifications (Nov/Feb/Apr plans)

## 4. Comptroller — Office of the NYC Comptroller
- **Budget analysis & comments (Prelim/Exec/Adopted, all years):** https://comptroller.nyc.gov/services/financial-matters/nyc-budget/
- **Checkbook NYC — every payment, contract, payroll (penny-level):** https://www.checkbooknyc.com/
- **Annual Comprehensive Financial Report (ACFR):** https://comptroller.nyc.gov/reports/
- **"New York by the Numbers" — monthly economic & fiscal outlook:** https://comptroller.nyc.gov/newsroom/
- **Annual State of the City's Economy and Finances:** https://comptroller.nyc.gov/reports/

## 5. Independent Budget Office (IBO)
- **Home:** https://www.ibo.nyc.ny.us/ · **Fiscal history:** https://www.ibo.nyc.ny.us/fiscalhistory.html · **Citywide summary:** https://ibo.nyc.ny.us/RevenueSpending/citywide-summary.html

## 6. Capital projects
- **Council §254 capital changes:** on each FY hub (above) · **OMB Capital Commitment Plan:** https://www.nyc.gov/site/omb/publications/publications.page
- **Capital Projects Dashboard (Comptroller):** https://comptroller.nyc.gov/services/for-the-public/nyc-capital-projects/
- **School Construction Authority capital plan:** https://www.nycsca.org/

## 7. NYC Open Data (Socrata) — live datasets the suite pulls
| Dataset | ID | What |
|---|---|---|
| Expense budget | `mwzb-yiwb` | Adopted/modified expense by agency & object class |
| Adopted budget (all-funds) | `39g5-gbp3` | Total/city/state/federal by year |
| Revenue budget | `ugzk-a6x4` | OMB revenue plan |
| Capital commitments | `2cmn-uidm` | Capital plan ($ thousands) |
| Contract awards | `qyyg-4tf5` | Registered contracts / vendors |
| Discretionary award tracker | `ujre-m2tj` | Member designations by council district |
| Citywide payroll | `k397-673e` | Headcount, salary, overtime |
| 311 service requests | `erm2-nwe9` | Live quality-of-life signal by district |
| Council district boundaries | `872g-cjhh` | GeoJSON for the maps |
| Campaign finance (CFB) | `rjkp-yttg` | Contributions |
| Census (ACS) | `ye4r-qpmp` | Income, poverty, population by district |
- Portal: https://data.cityofnewyork.us/ · App-token raises the rate limit (set in the Sources tab).

## 8. Organizations, vendors & the market
- **Organizations → IRS Form 990:** https://projects.propublica.org/nonprofits/ (by EIN)
- **Vendors → legal entity:** https://opencorporates.com/
- **Campaign finance:** https://www.nyccfb.info/follow-the-money/
- **Municipal market (NYC's own bonds):** MSRB EMMA — https://emma.msrb.org/ (NYC GO & TFA disclosures, yields, ratings)
- **Macro / economic indicators:** FRED (St. Louis Fed) — https://fred.stlouisfed.org/ (NYC employment, wages, rates); NYS Comptroller — https://www.osc.ny.gov/

---

*Maintained alongside `NYC_Council_Fiscal_Suite_LIVE.html`. The suite embeds verified reference data from these sources and queries the rest live; open the **Wiki** tab in the suite to search everything, or the **Sources** tab for live connectivity status.*
