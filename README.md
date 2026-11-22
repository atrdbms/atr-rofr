# RoFR Dashboard – Amrabad Tiger Reserve

Dashboard for Recognition of Forest Rights (Forest Rights Act, 2006) titles in Amrabad Tiger Reserve, Nagarkurnool District, Telangana.

**Live site:** https://atrdbms.github.io/atr-rofr/

## Pages
- **Dashboard** – key figures and charts (community, year, range, area class, section, mandal, age, habitations)
- **Map** – Google satellite / Esri imagery / street map with every title plotted from its coordinates, 816 claim boundaries from `final_polygon_2009.kml` (toggle in the layer button), an option to overlay any other .kml file, a current-location button (live GPS position, nearest title and whether you are inside a claim boundary), and full-screen mode
- **Records** – beneficiary register, sortable, Download PDF (landscape A4) and CSV export of all sheet columns
- **Reports** – Download PDF (logos, active filters, key figures), summary tables (by Range, Year, Division, Section, Beat, Grampanchayat, Mandal, Habitation, Compartment, Community, Area class), Range × Community × Year table, data-quality checks, print

## Data
The page reads the Google Sheet `ROFR` (tab `ROFR`) every time it opens and every 10 minutes while open.
The sheet must be shared as **Anyone with the link can view** for live sync to work.
If the sheet can't be reached, the page falls back to the snapshot embedded in `index.html` (21 Nov 2026).

## Files
- `index.html` – the complete, self-contained site (Leaflet 1.9.4, Chart.js 4.4.1, jsPDF 2.5.2 and jsPDF-AutoTable 3.8.4 inlined)
- `src/template.html` – readable source before logos, libraries and data snapshot are inlined
