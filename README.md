# Advisor List Task 

Schwab Independent Advisor Directory

An interactive Power BI directory for exploring Registered Investment Advisory (RIA) firms by location. Built by **Akshara Sarode** using the submitted Part 1 advisor workbook.

**[Open the live Power BI report](https://app.powerbi.com/groups/c9955dea-8185-4c1e-acd7-ca412083b92d/reports/ec62f1e0-5f92-4276-ab23-c66fadfac5e3/1b44de2a555fc95ac2c3?experience=power-bi)** · [Download the PBIX](./Advisor%20List%20Task%20-%20Power%20BI%20Dashboard.pbix) · [View the PDF](./Advisor%20List%20Task%20-%20Power%20BI%20Dashboard.pdf)

> The live report may require Power BI access. The PDF is a static export; use the live report or PBIX for interactive filtering.

## What the dashboard includes

- **Five summary metrics:** Total Advisor Firms, Filtered Advisor Count, Unique States, Unique Cities, and Unique ZIP Codes.
- **Linked location filters:** Country, State, City, and ZIP Code dropdowns progressively narrow the advisor list.
- **Firm selector:** The **Search Advisor / Firm** dropdown lists company names from the dataset. Selecting one filters the details and dynamic metrics.
- **Advisor details:** A sortable table with firm name, CRD, address, city, state, ZIP, phone, email, website, and SEC profile. Right-hand columns can be reached by horizontal scrolling.
- **Geographic analysis:** Horizontal charts for Advisor Firms by State and Top 10 Cities by Advisor Firms.
- **Two report pages:** `Advisor Directory` and `Geographic Analysis`.

## Dashboard

<img width="1920" height="1088" alt="image" src="https://github.com/user-attachments/assets/b9960a08-dfb4-40fb-bec6-b25eb67178b3" />

<img width="1902" height="1056" alt="image" src="https://github.com/user-attachments/assets/3ac3a090-04cc-4cab-ab1b-2da059dd39c0" />


Open the `.pbix` file in Power BI Desktop to edit the report and its imported data. The PDF is a static view of the unfiltered report.

Data and metric definitions

The source is [`Submission File (Akshara).xlsx`](./Submission%20File%20%28Akshara%29.xlsx), using its populated `Schwab database` sheet. Power BI prepares an `Advisor Locations` table with **4,397 location rows**. The report also retains the raw sheet query. `Country` is set to `United States`, and ZIP codes are stored as text to preserve leading zeros.

At the unfiltered view, the report shows:

| Metric | Value |
| --- | ---: |
| Total Advisor Firms | 2,570 |
| Filtered Advisor Count | 2,570 |
| Unique States, including DC | 51 |
| Unique Cities shown in the report | 1,314 |
| Unique ZIP Codes | 2,133 |

One firm can have multiple office rows. Firm metrics use **distinct firm IDs** so offices do not inflate the advisor count. `Total Advisor Firms` is a fixed baseline label for this imported snapshot; the other four KPI cards recalculate with filters. Check the fixed label if the source data is later replaced.

## How to use it

1. Open the [live report](https://app.powerbi.com/groups/c9955dea-8185-4c1e-acd7-ca412083b92d/reports/ec62f1e0-5f92-4276-ab23-c66fadfac5e3/1b44de2a555fc95ac2c3?experience=power-bi) or the PBIX in Power BI Desktop.
2. Choose a company or select Country, State, City, and ZIP values. The available results and dynamic counts update with the selection.
3. Sort the advisor table by clicking a column heading. To export visible rows, use the table visual's **More options (...) > Export data** command, if enabled for your Power BI account.
4. Use **Reset to default** to clear selections and return to the full directory.

## Files in this repository

| File | Purpose |
| --- | --- |
| [`Advisor List Task - Power BI Dashboard.pbix`](./Advisor%20List%20Task%20-%20Power%20BI%20Dashboard.pbix) | Editable Power BI report with imported data |
| [`Advisor List Task - Power BI Dashboard.pdf`](./Advisor%20List%20Task%20-%20Power%20BI%20Dashboard.pdf) | Static two-page report export |
| [`Submission File (Akshara).xlsx`](./Submission%20File%20%28Akshara%29.xlsx) | Supplied Part 1 workbook |
| [`advisor_locations.csv`](advisor_locations.csv) | Portable location-row data export |
| [`Advisor_List_Task_Process_Documentation_Akshara.docx`](Advisor_List_Task_Process_Documentation_Akshara.docx) | Five-page process documentation |
| `powerbi_*.png` | Dashboard and filter-interaction screenshots |

## Filter evidence

The screenshots demonstrate the unfiltered report, the populated [company dropdown](powerbi_company_dropdown.png), an [Alabama selection](powerbi_state_AL.png), and the [Geographic Analysis page](powerbi_geographic_analysis.png). For example, selecting Alabama showed 25 firms, 10 cities, and 23 ZIP codes; narrowing to Birmingham showed 12 firms and 8 ZIP codes.

## Process documentation

The [five-page document](Advisor_List_Task_Process_Documentation_Akshara.docx) explains the source workbook, preparation steps, dashboard structure, count logic, interaction testing, export, and handoff. It distinguishes the supplied Part 1 collection process from the Power BI work completed for Part 2.

