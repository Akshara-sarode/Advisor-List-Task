# Advisor List Task - Power BI dashboard

## Open the dashboard

Live report: https://app.powerbi.com/groups/c9955dea-8185-4c1e-acd7-ca412083b92d/reports/ec62f1e0-5f92-4276-ab23-c66fadfac5e3/1b44de2a555fc95ac2c3?experience=power-bi

Open the `.pbix` file in Power BI Desktop to edit the report and its imported data. The PDF is a static view of the unfiltered report.

## Data source and preparation

Source: `Submission File (Akshara).xlsx`, populated sheet `Schwab database`. The report's `Advisor Locations` table uses the full 4,397 location rows. Its query promotes the actual header row, adds `Country = United States`, and stores ZIP as five-character text so leading zeros remain visible. The imported model also retains the raw `Schwab database` query; report visuals use `Advisor Locations`.

`firmId` identifies a firm. One firm can have multiple location rows, so advisor metrics use a distinct count of `firmId`.

## Dashboard structure

The top row shows total advisor firms, filtered advisor count, unique states, unique city names, and unique ZIP codes. With no filters applied, these are 2,570 firms, 2,570 filtered firms, 51 states (including DC), 1,314 city names, and 2,133 ZIP codes. The total-firms figure is a fixed snapshot label for this imported dataset; update it if the source is replaced. The other four cards recalculate when filters change.

The report has two pages. **Advisor Directory** contains the title **Schwab Independent Advisor Directory**, the subtitle **Akshara Sarode**, five KPIs, the slicers, a sortable advisor table, and a soft pink state bar chart. The KPI cards use light orange, light blue, baby pink, and lavender backgrounds with darker values for readability.

**Geographic Analysis** repeats the title and subtitle above two horizontal bar charts based on distinct firm IDs: **Advisor Firms by State** in soft pink and **Top 10 Cities by Advisor Firms** in burgundy. The state chart is scrollable. The city chart has a visual-level Top 10 filter. Chart bars can be selected to cross-filter other visuals on that page. The displayed figures come from the supplied workbook and can differ from the design reference.

Country, State, City, and ZIP are slicers on the same `Advisor Locations` table. Select a value in one slicer to narrow the available choices and the results in the others. The company-name input slicer uses a contains search; type a term and click its apply arrow. Clear selections to return to the full list.

The advisor table shows firm name, state, city, ZIP, phone, email, website, and SEC adviser profile URL. Some right-hand columns require horizontal scrolling. Click a column heading to sort. Hover over the table and use its **More options (...) > Export data** command to download the currently filtered rows, subject to the Power BI account's export settings.

## Files

- `Advisor List Task - Power BI Dashboard.pbix` - editable Power BI report with imported data.
- `Advisor List Task - Power BI Dashboard.pdf` - static unfiltered report export.
- `powerbi_unfiltered.png` - full list and baseline metrics.
- `powerbi_state_AL.png` - Alabama selection: 25 firms, 10 cities, 23 ZIP codes.
- `powerbi_AL_Birmingham.png` - Alabama and Birmingham selections: 12 firms, 8 ZIP codes.
- `powerbi_geographic_analysis.png` - state and top-ten-city charts in the requested colors.
- `Submission File (Akshara).xlsx` - supplied source workbook.
- `advisor_locations.csv` - cleaned, export-friendly copy of the source rows.

The screenshots show how live filtering affects the counts and advisor table. The PDF itself is static; use the live report or PBIX for interaction.
