# Advisor List Task 

## Dashboard

<img width="1920" height="1088" alt="image" src="https://github.com/user-attachments/assets/b9960a08-dfb4-40fb-bec6-b25eb67178b3" />

<img width="1902" height="1056" alt="image" src="https://github.com/user-attachments/assets/3ac3a090-04cc-4cab-ab1b-2da059dd39c0" />


Open the `.pbix` file in Power BI Desktop to edit the report and its imported data. The PDF is a static view of the unfiltered report.

## Data source and preparation

Source: `Submission File (Akshara).xlsx`, populated sheet `Schwab database`. The report's `Advisor Locations` table uses the full 4,397 location rows. Its query promotes the actual header row, adds `Country = United States`, and stores ZIP as five-character text so leading zeros remain visible. The imported model also retains the raw `Schwab database` query; report visuals use `Advisor Locations`.

`firmId` identifies a firm. One firm can have multiple location rows, so advisor metrics use a distinct count of `firmId`.

## Dashboard structure

The top row shows total advisor firms, filtered advisor count, unique states, unique city names, and unique ZIP codes. With no filters applied, these are 2,570 firms, 2,570 filtered firms, 51 states (including DC), 1,314 city names, and 2,133 ZIP codes. The total-firms figure is a fixed snapshot label for this imported dataset; update it if the source is replaced. The other four cards recalculate when filters change.

The report has two pages. **Advisor Directory** is the main, single-page dashboard matching the supplied layout reference. It contains the title **Schwab Independent Advisor Directory**, the subtitle **Akshara Sarode**, five KPIs across the top, four geographic dropdown filters, a firm-name search at the upper right, the advisor table on the left, and both horizontal charts on the right. The KPI cards use light orange, light blue, baby pink, and lavender backgrounds with darker values for readability.

**Geographic Analysis** repeats the title and subtitle above two horizontal bar charts based on distinct firm IDs: **Advisor Firms by State** in soft pink and **Top 10 Cities by Advisor Firms** in burgundy. The state chart is scrollable. The city chart has a visual-level Top 10 filter. Chart bars can be selected to cross-filter other visuals on that page. The displayed figures come from the supplied workbook and can differ from the design reference.

Country, State, City, ZIP, and company name are dropdown slicers on the same `Advisor Locations` table. Open **Search Advisor / Firm** to choose from the company names in the dataset; the dropdown includes a search box to find a name quickly. Selecting a firm or location narrows the advisor table, charts, and dynamic KPI cards. Select the checked firm again or use **Reset to default** to return to the full list.

The advisor table shows Firm Name, CRD, Address, City, State, ZIP Code, Phone, Email, Website, and SEC Profile. Some right-hand columns require horizontal scrolling. Click a column heading to sort. Hover over the table and use its **More options (...) > Export data** command to download the currently filtered rows, subject to the Power BI account's export settings.

## Files

- `Advisor List Task - Power BI Dashboard.pbix` - editable Power BI report with imported data.
- `Advisor List Task - Power BI Dashboard.pdf` - static unfiltered report export.
- `powerbi_unfiltered.png` - full list and baseline metrics.
- `powerbi_company_dropdown.png` - updated company-name dropdown.
- `powerbi_state_AL.png` - Alabama selection: 25 firms, 10 cities, 23 ZIP codes.
- `powerbi_AL_Birmingham.png` - Alabama and Birmingham selections: 12 firms, 8 ZIP codes.
- `powerbi_geographic_analysis.png` - separate geographic analysis page with the same two charts.
- `Submission File (Akshara).xlsx` - supplied source workbook.
- `advisor_locations.csv` - cleaned, export-friendly copy of the source rows.

The screenshots show how live filtering affects the counts and advisor table. The PDF itself is static; use the live report or PBIX for interaction.
