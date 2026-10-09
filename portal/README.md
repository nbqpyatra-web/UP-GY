# UP Gunvatta Yatra portal

A single-file monitoring portal (`index.html`) for the UP GY programme. Open it in a
browser; it needs internet only for fonts and the d3 map library.

## Sections

The main pages cover only the 63 UP GY yatras in the master planner (09 Oct 2026 –
24 Mar 2027). Anything earlier lives on the Past yatras page.

| Section | What it shows |
|---|---|
| Overview | KPIs, yatra calendar, district map (status or NABH gap), next-up queue, the selected yatra's readiness / registration / attendance / leads, and phase progress |
| Yatras | All 63 yatras with CRM status and readiness, sortable and searchable |
| Districts | Map plus all 75 districts: PM-JAY universe, NABH, gap, UP GY yatra date and results |
| Lead funnel | Registered → attended → potential leads → won for UP GY yatras, every CRM status, leads by district |
| Readiness | Shared tracker per yatra: CMO letter, hospital list, CMO SPOC, venue (Not started / In progress / Done / Not needed), SPOC name, venue, notes |
| Data checks | UP GY problems (yatra held without a CRM event, CRM event not in the planner, date mismatch, missing attendance) and clean-up items for past records |
| Past yatras | CRM events before 09 Oct 2026, attendance by month, delivery-approach comparison (QCI team view only) and the (VF) district baseline |

"View as: District CMO" hides the delivery-approach comparison and partner details,
in line with the dashboard spec.

## Readiness tracker

The tracker saves to the published artifact's shared database (`readiness/<yatra id>`,
e.g. `readiness/P1-01`), so it works only in the published portal on claude.ai. Anyone
with Contributor access or above can edit; Viewers see it read-only. Each record keeps
who changed it last and when.

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
- UP GY = the 63 planned yatras from the launch on 09 Oct 2026; earlier yatras are history.
- Potential leads = Hot + Warm + Application in progress. Won = CRM "Won" +
  "Application submitted". Close rate = Won ÷ (Hot + AIP + Won).
- Gap = PM-JAY universe − NABH total, floored at 0. The map colours by absolute gap.
- A planned yatra is linked to a CRM event in one of its districts dated within 3 days of
  the plan date. CRM events from 09 Oct 2026 that match no planned yatra are listed in
  Data checks; events before 09 Oct 2026 go to Past yatras only.

## Vercel

`main` deploys to Vercel automatically (`vercel.json` serves `portal/`; `.vercelignore`
uploads only `portal/index.html`). The Vercel copy is read-only: the readiness tracker
needs the claude.ai artifact database, so it shows as unavailable there. The page is public
to anyone with the link.
