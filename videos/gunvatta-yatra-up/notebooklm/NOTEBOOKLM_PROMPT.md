# NotebookLM — Video Overview prompt for Gunvatta Yatra UP

## Steps

1. Create a new notebook in NotebookLM and add these sources:
   - `SOURCE_PACK.md`, from this folder. It's the most important source: it has the circular summary, the plan and all 75 districts.
   - The SACHIS circular image or PDF (14 May 2026).
   - The planner `Planned_Yatras_All_Phases.xlsx`. If upload fails, export it to PDF or Google Sheets.
   - Optional: `SCRIPT-v2-draft.md`, the script used for the HyperFrames video.
2. Open **Studio → Video Overview → Customize**.
3. Set the language to **Hindi (हिन्दी)**. Choose the **Explainer** format if it's offered.
4. Paste the prompt below into the "What should the AI hosts focus on?" box, then click **Generate**.

NotebookLM decides the final length, voices and visuals itself. The prompt steers them; it can't fix them exactly.

---

## Prompt (copy everything between the lines)

---

Create an engaging video overview in Hinglish (conversational Hindi, keeping English terms like hospital, quality, NABH, certification, workshop and pincode in English) about "Gunvatta Yatra Uttar Pradesh" (गुणवत्ता यात्रा, उत्तर प्रदेश), presented by the Quality Council of India (QCI). Target length: about 2 minutes 30 seconds. Audience: managers and doctors of Ayushman Bharat PM-JAY empanelled private hospitals, district health officials, and citizens of UP. Tone: warm, energetic, hopeful and fast-paced, not a dry government announcement. Prefer a female narrator voice if possible.

Follow this story order:

1. HOOK (emotional): open with a relatable question — when a family takes a loved one to hospital, what do they need first? "भरोसा" (trust): treatment whose quality they can trust.
2. WHY: Ayushman Bharat PM-JAY exists to give every beneficiary quality, standard healthcare. But inspections found that some empanelled hospitals still do not meet minimum standards.
3. THE DIRECTIVE: explain the SACHIS circular of 14 May 2026. NABH certification is now mandatory for all PM-JAY empanelled private hospitals, and for new hospitals applying for empanelment, within 2 months. Mention that, under the National Health Authority's Quality Indicators for Quality of Care guidelines (August 2020), quality is linked to incentives.
4. WHAT PATIENTS GET: name the circular's three benefits as a clear "एक, दो, तीन": (1) better quality of health services, (2) treatment as per standards, (3) better and transparent services.
5. ENTER GUNVATTA YATRA: QCI's initiative to take this change to every hospital. Two raths (Rath A and Rath B), 63 yatras and 75 districts, running NABH Entry Level Certification workshops from 4 PM to 8 PM, directly in each district, from 9 October 2026 to 24 March 2027.
6. THE FIRST FIVE STOPS, in this exact order with dates: Gorakhpur (9 October 2026, grand launch, both raths), then on 14 October Bareilly (Rath A) and Kushinagar (Rath B), then on 16 October Moradabad (Rath A) and Maharajganj (Rath B). Show them on a map of Uttar Pradesh.
7. ALL 75 DISTRICTS: show the journey spreading across the whole state in planner order. Phase 1 (October–November 2026, 23 districts), Phase 2 (January–March 2027, 33 districts, including Meerut, Agra, Varanasi and Lucknow), and Phase 3 cluster yatras in March 2027 (19 districts, from Bundelkhand to the Terai). Use the district list in the sources. Name a selection of districts aloud, and show as many as possible on screen.
8. THE BIG LINE: "हर ज़िला। हर शहर। हर पिनकोड।" (every district, every city, every pincode): all 75 districts of Uttar Pradesh.
9. CALL TO ACTION: when the Gunvatta Yatra comes to your district, join the 4–8 PM NABH workshop. Close with: quality is not just a certificate, it is trust (भरोसा). End line: "गुणवत्ता — हर द्वार तक" (Quality, at every doorstep), presented by the Quality Council of India.

Rules:

- Do NOT quote hospital counts or any statistics from the planner (no PM-JAY hospital totals, NABH totals, gaps, attendance or lead figures). The only numbers to use are 63 yatras, 75 districts, 2 raths, the dates, 2 months, and 4–8 PM.
- Do not invent facts, dates, statistics or quotes beyond the sources.
- Make it visually engaging: a map of Uttar Pradesh lighting up district by district, the circular with an "अनिवार्य" (mandatory) stamp, the NABH badge, a 2-month countdown, three benefit cards, two raths travelling the map, and a rolling pincode counter.
- Use Hindi headlines on screen with short English support text.
- Keep the energy high and the pacing quick. Every scene should move the story forward.

---

## Things NotebookLM may not follow exactly

- **Hinglish:** if the Hindi output is too formal, regenerate with "Use simple spoken Hinglish, not formal Hindi".
- **Female voice:** NotebookLM may not offer a voice choice. If you get a male voice, try regenerating.
- **2:30 length:** Video Overviews pick their own length. If it runs long, add "Keep it under 3 minutes" and regenerate.
- **Logos:** NotebookLM cannot place the official QCI, NABH or PM-JAY logos. Add them afterwards in an editor, or ask me to add an end card to the NotebookLM video in HyperFrames.
