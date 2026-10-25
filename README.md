# RIA Advisor Directory

Open `dashboard.html` in a browser. It works offline and needs no server.

## Data source

`Submission File (Akshara).xlsx`, `Schwab database` sheet, rows 3–4399. This sheet has 4,397 advisor locations and 2,570 distinct firms by `firmId`. The other three sheets have headers but no advisor rows, so they are excluded. `advisor_locations.csv` is a normalized extract of the populated sheet.

The source has no country column. Country is derived as `United States` from its U.S. state and ZIP fields. ZIP codes are exported as five-character text to preserve leading zeros. No external geocoding or live refresh is performed.

## Filters and metrics

Country, state, city, and ZIP dropdowns show choices available under the other active filters. Firm search matches names and firm IDs. Each change updates all counts, state bars, and the advisor table. `Total advisor firms` is the unfiltered count of distinct firm IDs. `Filtered advisor firms` is the distinct firm count in the current selection. States, cities (state plus city), and ZIPs are counted in the filtered locations. Multiple locations can belong to one firm.

Click a table header to sort. `Export filtered CSV` exports every location matching the active filters with full contact and source profile fields. `Reset filters` restores the full dataset.

## Deliverables and limitations

`dashboard.html` is the interactive dashboard. `dashboard_summary.pdf` is a static overview. `advisor_locations.csv` is the prepared source extract. This is an offline browser dashboard, not a Power BI `.pbix`; Power BI web required a work or school sign-in in this session.
