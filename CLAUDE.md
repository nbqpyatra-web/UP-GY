# Project Context: UP Gunvatta Yatra (UP GY)

## Who / where
Quality Council of India (QCI) — National Board for Quality Promotion (NBQP).
Owner: Rachit Srivastava. Coordination: Amit Singh (Joint Director / Coordinator UP),
Mihir Sharma, Bhavishya & team (data/support).

## 1. What Gunvatta Yatra is
QCI-NBQP's national outreach programme driving healthcare organisations toward NABH
certification and accreditation. Model: a QCI team runs a district-level awareness +
technical session for hospitals; interested hospitals enter a CRM funnel worked by a
calling team.

National track record: 350+ yatras, 31 States/UTs, 190+ cities, 2,800+ pincodes,
~6,500 healthcare organisations.

Four-pillar framework:
- YATRA — awareness (the on-ground event)
- PATHSHALA — digital capacity building (e-Mitra, AI chatbot)
- MITRA — on-ground handholding
- MANTHAN — review and course correction

Hospital maturity ladder:
Empanelment → NABH Entry-Level Certification (10 chapters / 46 standards /
189 objective elements, 2-yr validity) → Full Accreditation (10 chapters /
102 standards / 639 objective elements, 4-yr validity, surveillance at yr 2).

## 2. What UP GY is
The Uttar Pradesh instance, triggered by SACHIS (UP State Health Agency, AB PM-JAY)
Circular ref **ABPMJAY/UP-GY/2026-27/161 dated 15 May 2026**, signed by CEO
Archana Verma. The circular makes NABH certification mandatory for all PM-JAY
empanelled private hospitals in UP, grounded in NHA's "AB PM-JAY Quality Indicators
for Quality of Care" (Aug 2020). Stated compliance window: 2 months from circular date.

### Scale of the problem (75 districts)
| Metric | Value |
| --- | --- |
| PM-JAY empanelled private hospitals (universe) | 3,650 |
| NABH covered total | 1,404 |
| — certified | 955 |
| — accredited | 449 |
| Gap / potential | 2,246 (61.5%) |

### Geography conventions
- Zones: Eastern UP, Western UP, Central UP, Bundelkhand (South UP); grouped by Mandal.
- Tiering (per Invest India, confirmed): UP has NO Tier 1 cities.
  Tier 2 = Agra, Ghaziabad, Kanpur, Lucknow only. Tier 3 = all other 71 districts.

## 3. Delivery model
UP GY runs entirely on the **direct, district-administration-led model** built around the
District CMO (Chief Medical Officer). Internally this is the "Runner Model"; the
alternative is the "OP Model" (Organising Partner).

Evidence for the choice — Runner 8 yatras / 236 attendees / 8.1% won-rate /
31.1% close rate / 2.4 Won per yatra vs OP 20 yatras / 412 attendees / 1.2% won-rate /
5.9% close rate / 0.2 Won per yatra. HVL generation is similar (~18–19%); the gap is in
converting leads to paid.

**Hard constraint:** the term "Runner Model" is INTERNAL ONLY. Never use it in
CEO/client/SACHIS/CMO-facing documents, decks or dashboards. Externally describe it as
a "direct, district-administration-led engagement approach".

Five-step engagement loop:
1. Engage the District CMO
2. Obtain the district hospital list
3. Match against NABH data to isolate non-certified hospitals
4. CMO-supported outreach
5. Hospitals register via a CRM auto-generated link

Five support asks placed with SACHIS:
1. Letter issued to CMOs of all 75 districts
2. List of hospitals from each district CMO
3. Participant / hospital mobilisation
4. District-wise SPOC from the CMO office
5. Venue support from CMOs

## 4. Data definitions (locked — do not redefine)
Source of truth: **`Updated District List data.xlsx`, sheet `(VF) Final Sheet`**
(75 districts). Supersedes the earlier `Districtwise data.xlsx`.

Columns: S. No., Mandal, District, Zone, Tier, PMJAY Universe, NABH Total, Cert., Accr.,
Potential (Gap), % Potential, No. of Yatras Conducted, Attended, Won,
Application in Progress, Hot, Warm.

CRM lead statuses:
- **Hot** — will take NABH within 6 months
- **Warm** — will take NABH in 6–12 months
- **Application in Progress (AIP)** — filling NABH application, fee not yet paid
- **Won** — fee paid / application submitted → a CONVERSION, not a lead
- **Cold** — interest unconfirmed (excluded)
- **Engaged** — called 3x, no response (excluded)
- **Lost** — not interested or went via consultant (excluded)
- **Existing** — already certified/accredited (excluded)
- **Registered** — registered for an upcoming yatra, not yet attended (pre-funnel, excluded)
- **Qualified** — registered but did not attend (pre-funnel, excluded; calling team does
  not reach out)
- **Unqualified** — duplicate contact from an already-counted hospital (always excluded;
  one lead per hospital)

**TRUE POTENTIAL LEADS = Hot + Warm + AIP only.** Won is tracked separately.
Close rate = Won ÷ (Hot + AIP + Won).

NABH counting methodology: count every NABH facility/type as one unit each (Hospitals,
Entry-Level Hospitals, SHCO, Entry-Level SHCO, Blood Bank, Eye Care, Dental, Panchakarma,
Allopathic Clinics, Ayush Hospital, MLP, Nursing Excellence, MIS, etc.) EXCEPT exclude
'Digital Health' rows (they re-certify a hospital already counted elsewhere).

District name normalisation (NABH city names → PM-JAY's 75 official districts):
Kanpur → Kanpur Nagar; Prayagraj → Allahabad; Noida / Greater Noida / Dadri →
Gautam Buddha Nagar; Firozabadad → Firozabad; Sahibabad / Modinagar → Ghaziabad;
Mughalsarai → Chandauli. (Full mapping already exists in scripts.)

Note: Gautam Buddha Nagar and Ghaziabad are the only districts where NABH count exceeds
PM-JAY count — potential is floored at 0.

## 5. Prioritisation rules
- Weighting: **70% potential (gap + % potential) + 30% leads (Hot + AIP)**.
- Rank on **absolute counts** (PM-JAY universe vs NABH total), NOT % potential —
  tiny-universe districts show 100% potential without being priorities. (Phase 2 rule,
  15 Sep 2026; also governs dashboard map colouring.)
- Front-load: the first 5–7 yatras must be the strongest districts on every dimension.
- Phase 1 exclusions: districts with PM-JAY universe < 20; Gautam Buddha Nagar and
  Ghaziabad always excluded; Lucknow, Prayagraj, Varanasi, Kanpur Nagar excluded
  (15 Sep 2026). Gorakhpur fixed as the first district.
- Phase 2: Lucknow and Varanasi ARE included but scheduled mid-window.
  Gautam Buddha Nagar and Ghaziabad go last (lowest priority), not excluded.
- Phase 3: districts with PM-JAY universe under 15 are clustered with nearby districts
  into a single combined yatra.

## 6. Schedule
**Phase 1 — 23 districts, 09 Oct – 27 Nov 2026**, 4 PM – 8 PM, Wednesdays and Fridays,
two raths in parallel after the Gorakhpur launch. Takes coverage to 38 of 75 districts
(20 already covered).

Gorakhpur (09 Oct launch); Bareilly & Kushi Nagar (14 Oct); Moradabad & Maharajganj
(16 Oct); Bijnor & Sant Kabir Nagar (23 Oct); Muzaffarnagar & Basti (28 Oct);
Saharanpur & Barabanki (30 Oct); Shamli & Lakhimpur Kheri (04 Nov);
Bulandshahar & Prayagraj (13 Nov); Hapur & Mirzapur (18 Nov); Aligarh & Bhadohi (20 Nov);
Kanpur Nagar & Chandauli (25 Nov); Jhansi & Mau (27 Nov).

**Phase 2 — 23 days, Jan–Mar 2027**, Wednesdays and Fridays, two yatras per day in
different districts: 6/8/13/15/20/22/27/29 Jan; 3/5/10/12/17/19/24/26 Feb;
3/5/12/17/19/24/31 Mar (10 Mar dropped).

Earlier phased framing (plan-of-action doc): Phase I Central UP (Lucknow, Kanpur,
Ayodhya); Phase II East UP (Gorakhpur, Basti, Azamgarh, Varanasi, Prayagraj, Mirzapur);
Phase III North UP / Devipatan (Bahraich, Gonda, Balrampur, Shrawasti);
Phase IV South UP (Jhansi, Chitrakoot); Phase V West UP (Meerut, Saharanpur, Moradabad,
Bareilly, Agra, Aligarh).

## 7. Current status (as of 06 Oct 2026)
- Yatras held: 25, across 20 of 75 districts
- Attended: 509
- Hot / Warm / AIP: 71 / 25 / 22
- Won: 22
- Close rate: 19.1%
- Hospitals reached (universe of covered districts): 1,725

## 8. Deliverables produced so far
- `UP_GY_Plan_of_Action.docx` — 11 pages, QCI navy/blue branding, Calibri. Sections:
  1 Background/State Mandate, 2 About Gunvatta Yatra, 3 Objectives, 4 UP Quality
  Landscape, 5 Proof of Concept, 6 Proposed Delivery Approach, 7 Support from SACHIS,
  8 Implementation Plan, 9 QCI-NABH Framework, 10 Governance/Action Plan,
  Annexure I programme agenda (Agenda A ELC 5–8 PM; Agenda B C-to-A 3–8 PM),
  Annexure II draft CMO communication letter.
- `UPGY_Tentative_Schedule_VF.pptx` (15 Sep 2026) — current final deck, 12 slides:
  1 Title; 2 The Circular; 3 About Gunvatta Yatra + Challenge vs Response;
  4 Objectives; 5 UP landscape; 6 Workshop calendar (23 rows); 7 District route map +
  coverage; 8 Tentative agenda (4–8 PM, technical session by Dr. Narendra Saini);
  9 Support requested from SACHIS; 10 Delivery approach; 11 Four pillars; 12 The Ask.
- `UP_Potential_Leads_District_Analysis.xlsx` — tabs: Summary, District Data (75),
  Ranked by Potential, CRM by District, CRM Ranked by Potential, OP vs Runner
  Effectiveness.

## 9. Dashboard workstream (design spec approved 06 Oct 2026; sample built)
- Primary audience: QCI internal delivery team → then the 75 District CMOs.
  SACHIS is a later read-only cut.
- Refresh target: daily automated pull (Freshworks CRM + NABH DB nightly;
  PM-JAY empanelment weekly).
- Six screens: Command Centre, State Map, District Detail / CMO View, Lead Queue,
  Yatra Ops & Governance, Certification & Sustainment.
- Runner/OP comparison is role-gated, internal-only; never visible to CMO or SACHIS roles.
- CMO landing page carries NO state ranking — support-tool framing, not a compliance
  scoreboard.
- Map colour uses absolute gap, not % potential.

Placeholder panels (no system holds the field yet): lead ageing and stage-entry dates,
drop-out reason codes, venue/SPOC/letter status, NABH certificate and surveillance dates,
Pathshala/Mitra/Manthan activity.

Open gating decisions before a real build:
1. Freeze the empanelment denominator (15 May 2026 circular date vs 12 June data pull)
2. Confirm NABH API access vs periodic extracts only (decides whether "daily" is real)
3. Add a stage-entry timestamp and a reason-code field to Freshworks
4. Name an owner for the ops tracker (venue, SPOC, letter, hospital-list status)
5. Choose the CMO access mechanism: magic link, per-district URL, or SACHIS portal SSO

## 10. Stakeholders and meeting record
RoD of the 08 July 2026 UP meeting — attendees: Dr. Ravikant Singh (GM Ops, Ayushman
Bharat UP), Dr. Mustafa Khan (Office of ACS-Health UP), Dr. Punam Bajaj (Director NABH),
plus the QCI team (Rachit Srivastava, Pankaj Kumar, et al.).

- Dr. Ravikant Singh: hospitals get certified but don't sustain quality — wants training
  and handholding, monitoring, and shorter validity.
- Dr. Mustafa Khan: wants all 75 districts covered via CEO(SACHIS) → ACS(Health) → CMOs;
  surprise surveillance; a joint training module.
- QCI: flagged hard-to-reach districts — Shravasti, Lalitpur, Sonbhadra — that must
  still be covered.

Follow-up meeting with CEO SACHIS: 21 July 2026.

## 11. Parallel track — MP GY (for reference only)
Madhya Pradesh runs in parallel. Order S.H.A./A.B./2026/1631 dated 30.03.2026 mandates
Entry-Level NABH certification / full accreditation for empanelled hospitals in 4 metro
cities (Bhopal, Indore, Jabalpur, Gwalior); Order 2026/2026 dated 13.04.2026 granted a
6-month extension from 01.04.2026. Structure: Stage I 4 metros → Stage II districts.
Bhopal baseline: 438 hospitals, 34 accredited, 156 certified, 248 not-yet-NABH.

**UP materials deliberately EXCLUDE MP's medical-value-travel (MVT) and NABL/ISO 15189
angles** — the UP circular is NABH-for-PM-JAY only.

## 12. Working conventions
- Totals rows go at the TOP of tables, not the bottom, across all project workbooks.
- Data definitions (especially CRM statuses) are agreed and locked before any analysis
  is built on them.
- Internal alignment details never appear in external stakeholder communications.
- Government emails: concise, formal, purposeful. No filler closing lines. A confirmed
  meeting is never framed as an open-ended request.
- Formality adapts by channel: formal note → single paragraph → WhatsApp.
- Drafts are expected to go through multiple refinement rounds.
- QCI MoM template: purple section headers (800080), grey sub-headers (DFDFDF),
  thin black borders, fixed section structure.
- PPTs are produced via Claude Design, on a user-supplied template.

## 13. Source files in the project
`UP Circular.pdf` · `RoD Meeting with ABPMJAY_UPGY_160726_VF.pdf` ·
`NABH DATA_120626.xlsx` (tab `815_Active NABH (UP)`) ·
`PMJAY_Uttar Pradesh_Data_120626.xlsx` (tab `(2543) PMJAY U_Hosp (Private)`) ·
`UP GY_CRM_Data_200726.xlsx` (tabs `(8) Runner Model Data`, `(20) OP Model`) ·
`Districtwise data.xlsx` · `Updated District List data.xlsx` (CURRENT) ·
`UPGY_Tentative_Schedule_VF.pdf` / `.pptx` · `Accreditation Pathway_Template_15072026.pdf` ·
`MP_NABH_Meeting_03072026_v3.pdf` · `MP_QCI_NABH_Note_09062026_v2.docx` ·
`NABH_NABL Order Draft_MP_10072026.docx`

Note on two number sets: the earlier 12 June 2026 pull showed a 2,543-hospital PM-JAY
universe with 811 NABH covered and 1,801 potential leads. The current and authoritative
figures are 3,650 / 1,404 / 2,246 from `Updated District List data.xlsx`. Freezing which
denominator is canonical is open gating decision #1 above.

## 14. Freshworks CRM access (via this repo)
- MCP server in `freshworks_mcp/` (see its README); credentials in the gitignored
  `freshworks_mcp/.env` or `FRESHWORKS_DOMAIN` / `FRESHWORKS_API_KEY` env vars.
  Instance: `qci-crm.myfreshworks.com`. Rate limit 5,000 calls/hour, 400/minute.
- `POST filtered_search/contact` filters dropdowns by **text value**, not choice id
  (e.g. `{"attribute":"cf_boarddevision","operator":"is_in","value":["NABH"]}`).
  `owner_id` takes the numeric user id. Results are partial (no `custom_field`); fetch
  `contacts/{id}` for event details.
- Useful ids/values: Rachit Srivastava owner_id `402000352508`. Event Type
  (`cf_event_type_A`) values include `Yatra`, `Gunvatta Mohotsav` (CRM spelling),
  `Gunvatta Yatra`. Zone = `cf_event_zone_new_dropdown`.
- Field quirks: Event Name is `cf_event_type`; Event Date `cf_yatra_date`; Event City
  `cf_yatra_city`. Two state fields disagree — `cf_yatra_state` (text) and
  `cf_event_state_new_dropdown`; check both. Attendance is `cf_attendance`
  (Registered / Attended / Not Attended / Postponed / Cancelled).
- Counting events: contacts are attendees, so count distinct `cf_event_type` values
  (format `NABH_<CITY>_<DDMMYY>_Y`). Exclude the undated catch-all `NABH_ADDITIONAL_Y`.
