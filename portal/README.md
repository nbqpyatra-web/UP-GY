# UP Gunvatta Yatra portal

A single-file monitoring portal (`index.html`) for the UP GY programme. Open it in a
browser; it needs internet only for fonts and the d3 map library.

## Sections

| Section | What it shows |
|---|---|
| Overview | KPIs, yatra calendar, district map (status or NABH gap), next-up queue, and the selected yatra's before / during / after view |
| Yatras | Every yatra (held in the CRM or planned), sortable and searchable |
| Districts | Map plus all 75 districts: PM-JAY universe, NABH, gap, yatras held, leads, next date |
| Lead funnel | Registered → attended → potential leads → won, every CRM status, leads by district |
| Readiness | The next 12 yatras: CRM registration status plus CMO letter, hospital list, SPOC and venue (not tracked yet) |
| Reports | Attendance by month and the delivery-approach comparison (QCI team view only) |
| Data checks | CRM and planner problems to fix: missing attendance, wrong state/district fields, planned yatras without a CRM event |

"View as: District CMO" hides the delivery-approach comparison and partner details,
in line with the dashboard spec.

## Refreshing the data

The data is embedded in `index.html`. Rebuild it with:

```bash
python3 portal/build_data.py            # live pull from Freshworks (~9 min, ~860 API calls)
python3 portal/build_data.py --cached   # reuse the last pull (after editing the page or planner)
python3 portal/build_data.py --no-crm   # planner only
```

Sources: `data/Planned_Yatras_All_Phases.xlsx`, Freshworks CRM (credentials as in
`freshworks_mcp/README.md`) and `up_districts.geojson` (simplified 2011 census
district boundaries). Only aggregate counts are taken from the CRM.

## Rules applied

- A CRM event is any distinct Event Name with Board = NABH, Event Type = Yatra /
  Gunvatta Mohotsav / Gunvatta Yatra, and either state field = Uttar Pradesh. Events
  whose text state names another state are dropped; `NABH_ADDITIONAL_Y` is excluded.
- "UP GY" period = yatras on or after the circular date, 15 May 2026.
- Potential leads = Hot + Warm + Application in progress. Won = CRM "Won" +
  "Application submitted". Close rate = Won ÷ (Hot + AIP + Won).
- Gap = PM-JAY universe − NABH total, floored at 0. The map colours by absolute gap.
- A planned yatra is linked to a CRM event when the district and date match.
