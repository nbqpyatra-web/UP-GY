# UP-GY — project memory

This repository holds Gunvatta Yatra Uttar Pradesh video work for the Quality Council of India (QCI).
Read this file before starting any new video, edit or follow-up.

## Gunvatta Yatra UP — what it is

- A QCI-led drive to raise healthcare quality across Uttar Pradesh. It runs **NABH Entry Level Certification workshops** for **Ayushman Bharat PM-JAY empanelled private hospitals**.
- Basis: the **SACHIS circular dated 14 May 2026**, issued by the State Health Agency (Ayushman Bharat PM-JAY, Lucknow) and signed by CEO Archana Verma.
  - All PM-JAY empanelled private hospitals, plus hospitals applying for empanelment, must get **NABH certification within 2 months**.
  - The reason given: PM-JAY's core aim is quality, standard healthcare, but inspections found some hospitals not meeting minimum standards.
  - The circular cites the NHA "Quality Indicators for Quality of Care" guidelines (August 2020), under which quality is linked to incentives.
  - Benefits it lists: (1) better quality of health services; (2) treatment as per standards; (3) better and transparent services for beneficiaries.
- The plan is in `Planned_Yatras_All_Phases.xlsx` (the user's upload):
  - **63 yatras · 75 districts · 2 raths (Rath A, Rath B) · 09 Oct 2026 – 24 Mar 2027 · 4 PM – 8 PM sessions**
  - Phase 1 (Oct–Nov 2026): 23 districts. Phase 2 (Jan–Mar 2027): 33 districts. Phase 3 cluster yatras (Mar 2027): 19 districts.
  - Top 5, in order: Gorakhpur (09 Oct, launch, Rath A + B), Bareilly (14 Oct, A), Kushinagar (14 Oct, B), Moradabad (16 Oct, A), Maharajganj (16 Oct, B).
  - All 75 districts in planner order, with Hindi names, dates and SVG shapes: `videos/gunvatta-yatra-up/assets/up-districts.json`.

## The user's standing preferences

- **QCI presents** every video. Logos used: QCI, NABH and Ayushman Bharat PM-JAY, in `videos/gunvatta-yatra-up/assets/logos/`. No usable SACHIS logo was found, so SACHIS appears as text only.
- **Do not show hospital counts** or other planner statistics (PM-JAY universe, NABH totals, gaps, leads). Allowed numbers: 63 yatras, 75 districts, 2 raths, dates, 2 months, 4–8 PM.
- Key message: reaching **every district, every city, every pincode** (हर ज़िला · हर शहर · हर पिनकोड). Show the top 5 districts first, then all 75 in planner order.
- **Voiceover:** Hinglish (Hindi with English terms like hospital, quality, NABH, certification), female, warm and energetic.
- **On-screen text:** Hindi headlines with English support. Captions on.
- **Length:** 2:30. 16:9 (1920×1080) for YouTube and screens. The user wants it engaging, not plain: fast cuts on the voice, map zooms, counters, stamps, sound effects.
- **Tools:** HyperFrames, using the faceless-explainer workflow. Voice is the free Microsoft Edge TTS voice `hi-IN-SwaraNeural` at rate +6%; it isn't formally licensed for commercial use, so mention this. HeyGen is not used because its API is paid.
- Ask the user before inventing facts. Never invent statistics, dates or schedules.

## Where things are

- Project: `videos/gunvatta-yatra-up/` (`BRIEF.md`, `STORYBOARD.md`, `SCRIPT-v2-draft.md`, `frame.md`, `compositions/frames/`, `audio_meta.json`)
- Renders: `renders/video.mp4` (v2, 2:29, final), `renders/video-share.mp4` (compressed), `renders/video-v1-60s.mp4` (the first 60-second version)
- NotebookLM handoff: `videos/gunvatta-yatra-up/notebooklm/`
- Working branch: `claude/fervent-fermat-h4kkh7`

## Things to know when rebuilding

- The district map data is injected after the build at the `/*UP_DISTRICTS_DATA*/null` marker in the map frames (06–12).
- After `captions.mjs build`, patch `compositions/captions.html` so the last caption group ends at `group.end + 0.6`. Otherwise it lingers over the end card.
- Don't run `audio.mjs sync-durations`. Frame duration is set to voice length + 0.9s.
- Python tools that do HTTPS need the proxy CA bundle (`/root/.ccr/ca-bundle.crt`). For edge-tts, patch `certifi.where()` to return it.
