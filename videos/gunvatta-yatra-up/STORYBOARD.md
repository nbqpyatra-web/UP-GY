---
format: 1920x1080
duration: 150s
message: "Gunvatta Yatra takes NABH quality to every PM-JAY hospital — every district, every city, every pincode of Uttar Pradesh."
arc: story-explainer with how-to
audience: PM-JAY empanelled private hospitals, health administrators and citizens of UP
mode: autonomous
language: hi-en
music: none
captions: enabled
---

## Video direction

- palette: `frame.md` blue-professional — cream `bg` ground, cobalt `primary` the ONLY accent; `negative` (#dc2626) ONLY for the 'not meeting standards' flags (frame 03) and the 'अनिवार्य' stamp (frame 04). Energy frames 04 and 11 are INVERTED: full cobalt field with cream (#fdfae7) text/elements.
- type: Hindi in Noto Sans Devanagari (font-family: "Noto Sans Devanagari", "Inter", sans-serif; line-height ≥ 1.3), English display Space Grotesk, body Inter. Fonts in assets/fonts/.
- real logos (only these files, never redraw them): assets/logos/qci.png (Quality Council of India — presenter), assets/logos/nabh.png (NABH), assets/logos/pmjay.png (Ayushman Bharat PM-JAY emblem). Use <img> with object-fit: contain; never recolor or crop them.
- shared district map stage (frames 06–12): put exactly this inline script inside the template BEFORE your timeline script: `<script>window.UP_DISTRICTS = window.UP_DISTRICTS || /*UP_DISTRICTS_DATA*/null;</script>` (the orchestrator injects the data at the marker after you finish; to inspect the data read assets/up-districts.json). It defines `window.UP_DISTRICTS = { viewBox: "0 0 1000 972", districts: [ {order, district, hi, phase, date, rath, zone, d, cx, cy}, … 75 in PLANNER ORDER ] }`. Build the SVG paths from it at timeline-construction time (synchronously, before registering the timeline). Placement: SVG at left 110px, top 70px, width 823px, height 800px (viewBox 0 0 1000 972). District style: stroke primary 1.2 (vector-effect: non-scaling-stroke), fill card-bg rgba(30,43,250,0.04); FILLED/visited = fill primary (opacity 0.9) with cream stroke. Labels: Hindi (Noto Sans Devanagari 600). Planner order #1–#5: Gorakhpur, Bareilly, Kushi Nagar, Moradabad, Maharajganj.
- captions: ENABLED — the bottom ~17% (y > 900) is reserved for the caption pill in EVERY frame; keep all content above y ≤ 900.
- motion grammar: long-tail eases (power3.out default), every reveal lands on its voiceover cue (word timings are listed per frame), never front-load; holds are still (no breathing/drift). Engaging = decisive hits on cues: scale-pops, slams, fast counters, camera pushes — but each element moves once and then rests.
- sfx are mounted by the orchestrator at the root; workers mount no audio.
- negative list: no invented statistics or hospital numbers; no logos other than the three files; no photos; no gradients/bokeh; no slideshow front-loading; no screensaver floating.

## Frame 1 — Hook: भरोसा

- type: hook
- scene: A cobalt ECG heartbeat line traces across a cream field; the word भरोसा lands huge on the spoken cue
- duration: 13.84s
- poster: 11.1s
- transition_in: cut
- status: animated
- beat: Recognition + warmth
- voiceover: "जब कोई अपने परिवार को hospital लेकर जाता है... तो उसे सबसे पहले क्या चाहिए? भरोसा। ऐसा इलाज, जिसकी quality पर भरोसा हो।"
- src: compositions/frames/01-hook.html
- blueprint: kinetic-type-beats (Adapt)
- focal: the word 'भरोसा'
- roles: heartbeat line = supporting · question text = supporting · 'भरोसा' = foreground subject · hairline grid = background

voice word cues (seconds from frame start): जब@0.10 · कोई@0.47 · अपने@0.78 · परिवार@1.11 · को@1.59 · hospital@1.75 · लेकर@2.32 · जाता@2.67 · है@3.00 · तो@4.07 · उसे@4.33 · सबसे@4.64 · पहले@5.11 · क्या@5.49 · चाहिए@5.76 · भरोसा@7.10 · ऐसा@8.68 · इलाज@9.18 · जिसकी@10.03 · quality@10.52 · पर@11.04 · भरोसा@11.24 · हो@11.68

Scene 1 (0.0–4.0s): cream field + faint hairline grid; a cobalt ECG line draws left→right across mid-frame (y≈430), one sharp heartbeat spike at center; small Hindi line "अस्पताल · परिवार" fades in above it at 1.1s ("परिवार" cue).
Scene 2 (4.0–7.0s): the line keeps a slow pulse; question text "सबसे पहले क्या चाहिए?" (Hindi h2) rises in at 4.6s, centered y≈300.
Scene 3 (7.0–8.6s): on the cue "भरोसा" (7.1s) the question clears upward and "भरोसा" slams in huge (≈220px, 700, primary) at center; the ECG spike flashes once behind it.
Scene 4 (8.6–end): under it, "ऐसा इलाज, जिसकी quality पर भरोसा हो" (Hindi 44px, text-muted) reveals word-by-word synced to the voice (8.68–11.7s); "quality" in cobalt. Hold.

## Frame 2 — PM-JAY's aim

- type: pain_point
- scene: The Ayushman Bharat PM-JAY emblem rises in; its aim — quality, standard healthcare for every beneficiary — builds as chips
- duration: 10.19s
- poster: 8.2s
- transition_in: crossfade
- status: animated
- beat: Orientation
- voiceover: "आयुष्मान भारत, प्रधानमंत्री जन आरोग्य योजना का मूल उद्देश्य है — हर लाभार्थी को quality और standard healthcare."
- src: compositions/frames/02-pmjay.html
- blueprint: compose
- focal: PM-JAY emblem + 'हर लाभार्थी' line
- roles: assets/logos/pmjay.png = foreground (left) · aim text + chips = foreground (right) · soft cobalt radial = background

voice word cues (seconds from frame start): आयुष्मान@0.10 · भारत@0.81 · प्रधानमंत्री@1.55 · जन@2.47 · आरोग्य@2.77 · योजना@3.26 · का@3.79 · मूल@3.94 · उद्देश्य@4.25 · है@4.78 · हर@5.35 · लाभार्थी@5.64 · को@6.31 · quality@6.49 · और@7.08 · standard@7.34 · healthcare@7.85

Scene 1 (0.0–2.4s): left third: the real PM-JAY emblem image (assets/logos/pmjay.png, ~360px) scales in from 0.85 with a soft cobalt ring drawing around it; right: eyebrow "आयुष्मान भारत · PM-JAY" (eyebrow style).
Scene 2 (2.4–5.6s): on "मूल उद्देश्य" (~3.3s) the headline "योजना का मूल उद्देश्य" (Hindi h2) rises in on the right.
Scene 3 (5.6–end): on "हर लाभार्थी" (~5.8s) a big line "हर लाभार्थी को" (Hindi 72px) and then two pill chips pop on their cues: "Quality healthcare" (~6.3s) and "Standard care" (~7.3s). Hold.

## Frame 3 — The gap

- type: pain_point
- scene: An inspection lens sweeps across a grid of hospital tiles; a few tiles flag red — 'minimum standards' not met
- duration: 7.69s
- poster: 6.2s
- transition_in: push-slide LEFT
- status: animated
- beat: Concern
- voiceover: "लेकिन inspection में पाया गया, कि कुछ hospitals अभी भी minimum standards पूरे नहीं कर रहे।"
- src: compositions/frames/03-gap.html
- blueprint: compose
- focal: the hospital-tile grid under the inspection lens
- roles: 4x3 grid of simple hospital tiles (line icon: building + plus) = foreground · magnifier = supporting · red flags = supporting

voice word cues (seconds from frame start): लेकिन@0.10 · inspection@0.57 · में@1.18 · पाया@1.29 · गया@1.67 · कि@2.20 · कुछ@2.43 · hospitals@2.66 · अभी@3.35 · भी@3.65 · minimum@3.81 · standards@4.22 · पूरे@4.81 · नहीं@5.16 · कर@5.47 · रहे@5.58

Scene 1 (0.0–1.6s): a 6x2 grid of hospital tiles (card-tinted, cobalt line icons: a building with a plus) cascades in on the left 60% (stagger).
Scene 2 (1.6–3.4s): on "inspection" (~0.9s cue) a cobalt magnifier ring glides across the grid tile by tile (camera-free, element move).
Scene 3 (3.4–5.0s): on "कुछ hospitals" (~3.3s) three tiles turn negative (#dc2626 border + small ✕ badge) one by one.
Scene 4 (5.0–end): right column: "minimum standards" (Space Grotesk 600, 64px) with a red strike/underline drawing, and Hindi "पूरे नहीं" (Hindi 56px, negative). Hold.

## Frame 4 — SACHIS directive: NABH mandatory

- type: product_intro
- scene: A circular slides in and is stamped 'अनिवार्य'; the NABH logo locks in; quality↔incentive link; a 2-month countdown
- duration: 16.12s
- poster: 12.9s
- transition_in: zoom-through
- status: animated
- beat: Resolve + urgency
- voiceover: "इसीलिए SACHIS ने तय किया — योजना से जुड़े सभी private hospitals के लिए, NABH certification अनिवार्य। Quality अब सीधे incentive से जुड़ी है... और लक्ष्य — दो महीने के अंदर!"
- src: compositions/frames/04-directive.html
- blueprint: compose
- focal: the circular card + 'अनिवार्य' stamp
- roles: circular paper card (cream, hairline, with header lines) = foreground · assets/logos/nabh.png = foreground · stamp = foreground · countdown chip = supporting

voice word cues (seconds from frame start): इसीलिए@0.10 · SACHIS@0.74 · ने@1.30 · तय@1.48 · किया@1.76 · योजना@2.38 · से@2.94 · जुड़े@3.17 · सभी@3.50 · private@3.89 · hospitals@4.38 · के@5.06 · लिए@5.19 · NABH@5.81 · certification@6.22 · अनिवार्य@7.09 · Quality@8.58 · अब@9.21 · सीधे@9.39 · incentive@9.87 · से@10.46 · जुड़ी@10.68 · है@11.03 · और@12.07 · लक्ष्य@12.35 · दो@13.06 · महीने@13.36 · के@13.71 · अंदर@13.87

Scene 1 (0.0–2.3s): a paper "circular" card (cream #fdfae7 on a full cobalt field — inverted frame for energy) slides up from below, tilted −3°: header "SACHIS · परिपत्र · 14 मई 2026" (Hindi/Latin mix), grey text lines as placeholders.
Scene 2 (2.3–5.8s): on "private hospitals" (~3.9s) the card's subject line highlights "सभी सूचीबद्ध निजी चिकित्सालय"; on "NABH certification" (~5.8s) the real NABH logo image (assets/logos/nabh.png, ~520px wide) slides onto the card's right side.
Scene 3 (5.8–8.5s): on "अनिवार्य" (7.1s) a red-ink stamp "अनिवार्य" (rotated −12°, bordered) slams onto the card (scale 1.6→1 + slight shake).
Scene 4 (8.5–12.0s): on "Quality ... incentive" (8.6/9.9s) two pills "Quality" ⇄ "Incentive" with a link line drawing between them, top-right on the cobalt field (cream pills).
Scene 5 (12.0–end): on "दो महीने" (13.1s) a big countdown chip "2 महीने" (cream on cobalt, 90px) pops with a circular progress ring sweeping. Hold.

## Frame 5 — Three benefits

- type: benefit_highlight
- scene: Three numbered benefit cards land on 'एक, दो, तीन'
- duration: 16.14s
- poster: 12.9s
- transition_in: push-slide LEFT
- status: animated
- beat: Clarity
- voiceover: "इसका मतलब? एक — स्वास्थ्य सेवाओं की quality में सुधार। दो — मरीज़ों का इलाज, तय standards के अनुसार। तीन — लाभार्थियों को बेहतर और पारदर्शी सेवाएं।"
- src: compositions/frames/05-benefits.html
- blueprint: grid-card-assemble (Adapt)
- focal: three benefit cards
- roles: cards 1–3 = foreground · numerals = supporting · hairline grid = background

voice word cues (seconds from frame start): इसका@0.10 · मतलब@0.50 · एक@1.81 · स्वास्थ्य@2.46 · सेवाओं@3.09 · की@3.59 · quality@3.73 · में@4.21 · सुधार@4.37 · दो@5.75 · मरीज़ों@6.44 · का@6.97 · इलाज@7.15 · तय@8.01 · standards@8.27 · के@8.86 · अनुसार@9.04 · तीन@10.50 · लाभार्थियों@11.23 · को@12.13 · बेहतर@12.27 · और@12.69 · पारदर्शी@12.94 · सेवाएं@13.56

Adapt: keep the staggered self-assembly, but each card lands on its spoken numeral, not a cascade.
Scene 1 (0.0–1.4s): eyebrow "मरीज़ों को क्या मिलेगा?" (Hindi h3, primary) top-left y≈150.
Scene 2 (1.4–5.5s): on "एक" (~1.5s) card 1 rises in (triptych, left): big cobalt numeral "1", Hindi "स्वास्थ्य सेवाओं की गुणवत्ता में सुधार", English sub "Better quality of care".
Scene 3 (5.5–10.2s): on "दो" (~5.6s) card 2 (center): "2", "मानकों के अनुरूप उपचार", "Treatment as per standards".
Scene 4 (10.2–end): on "तीन" (~10.3s) card 3 (right): "3", "बेहतर एवं पारदर्शी सेवाएं", "Better, transparent services"; then all three cards' top borders turn solid cobalt in a sweep. Hold.

## Frame 6 — Enter: Gunvatta Yatra

- type: product_intro
- scene: The 75-district UP map assembles; two raths (A, B) drive on; title गुणवत्ता यात्रा; counters 2 रथ · 63 यात्राएं · 75 ज़िले; QCI pahal
- duration: 18.97s
- poster: 15.2s
- transition_in: blur-crossfade
- status: animated
- beat: Excitement
- voiceover: "और इस बदलाव को हर hospital तक पहुँचाने निकली है — गुणवत्ता यात्रा! Quality Council of India की पहल। दो रथ, तिरसठ यात्राएं, पचहत्तर ज़िले — NABH Entry Level Certification workshops, सीधे आपके ज़िले में।"
- src: compositions/frames/06-yatra.html
- blueprint: logo-assemble-lockup (Adapt)
- focal: the district map + title lockup
- roles: UP district mesh (shared map stage) = foreground (left) · rath icons = supporting · title + counters = foreground (right) · assets/logos/qci.png = supporting

voice word cues (seconds from frame start): और@0.10 · इस@0.44 · बदलाव@0.65 · को@1.18 · हर@1.36 · hospital@1.60 · तक@2.25 · पहुँचाने@2.45 · निकली@2.94 · है@3.33 · गुणवत्ता@3.76 · यात्रा@4.38 · Quality@5.82 · Council@6.36 · of@6.85 · India@7.05 · की@7.42 · पहल@7.62 · दो@8.94 · रथ@9.30 · तिरसठ@9.87 · यात्राएं@10.38 · पचहत्तर@11.34 · ज़िले@12.03 · NABH@12.64 · Entry@13.13 · Level@13.51 · Certification@13.85 · workshops@14.68 · सीधे@15.66 · आपके@16.28 · ज़िले@16.68 · में@16.95

Adapt: keep the signature "parts assemble into the mark" — the mark is the UP district mesh.
Scene 1 (0.0–3.0s): all 75 district outlines (shared map stage) draw/fade in with a fast random-order stagger (deterministic order: by index) — hairline cobalt strokes, card-bg fill.
Scene 2 (3.0–6.0s): on "गुणवत्ता यात्रा" (~3.6s) the title lockup lands on the right: "गुणवत्ता यात्रा" (Hindi 120px, 700) + "Gunvatta Yatra · Uttar Pradesh" (Space Grotesk 44px, primary).
Scene 3 (6.0–9.0s): on "Quality Council of India की पहल" (~6.3s) the real QCI logo (assets/logos/qci.png, ~300px wide) fades in under the title with a small "की पहल" label.
Scene 4 (9.0–12.5s): counters pop on cues: "2 रथ" (~9.5s "दो रथ"), "63 यात्राएं" (~10.4s), "75 ज़िले" (~11.3s) — Space Grotesk 700 numbers counting up quickly, Hindi labels. Two small rath badges (rounded bus/van glyph built in SVG, labelled A and B) drive along the bottom of the map from left/right edges.
Scene 5 (12.5–end): on "NABH Entry Level Certification workshops" (~13.0s) a wide pill "NABH Entry Level Certification Workshops" appears under the counters; on "आपके ज़िले में" the map gives one cobalt pulse. Hold.

## Frame 7 — Stop 1: Gorakhpur launch

- type: feature_showcase
- scene: Camera zooms into Gorakhpur on the district map; it fills cobalt; launch chip 09 Oct 2026 · Rath A + B
- duration: 7.09s
- poster: 5.7s
- transition_in: zoom-through
- status: animated
- beat: Momentum
- voiceover: "शुरुआत — गोरखपुर से! नौ अक्टूबर को, launch के साथ।"
- src: compositions/frames/07-gorakhpur.html
- blueprint: compose
- focal: Gorakhpur district filling
- roles: shared district map (zoomed) = background-midground · Gorakhpur fill + label = foreground · date/launch card = foreground (right)

voice word cues (seconds from frame start): शुरुआत@0.10 · गोरखपुर@1.09 · से@1.70 · नौ@2.84 · अक्टूबर@3.26 · को@3.76 · launch@4.21 · के@4.68 · साथ@4.85

Scene 1 (0.0–1.4s): district map at full view, then a camera push (scale ~2.6) centered on Gorakhpur (district #1 cx/cy), easing power3.inOut over 1.2s; other districts stay hairline.
Scene 2 (1.4–3.0s): on "गोरखपुर" (~1.0s) Gorakhpur fills cobalt from 0 opacity and its Hindi label "गोरखपुर" (Hindi 600) appears beside it; a pulse ring expands from its centroid.
Scene 3 (3.0–end): right card: "#1" big cobalt numeral, "09 Oct 2026" (Space Grotesk 600), "Launch · Rath A + B" pill, and "1 / 75" counter. Hold.

## Frame 8 — Stops 2–3: Bareilly + Kushinagar

- type: feature_showcase
- scene: Split action on the full district map: Rath A heads west to Bareilly, Rath B east to Kushinagar; both fill; date chip 14 Oct
- duration: 6.88s
- poster: 5.5s
- transition_in: push-slide LEFT
- status: animated
- beat: Momentum
- voiceover: "चौदह अक्टूबर — Rath A पहुँचेगा बरेली, और Rath B — कुशीनगर।"
- src: compositions/frames/08-bareilly-kushinagar.html
- blueprint: compose
- focal: the two simultaneous rath routes
- roles: shared district map (full view, Gorakhpur already filled) = foreground · two dashed routes + rath badges = foreground · date chip = supporting

voice word cues (seconds from frame start): चौदह@0.10 · अक्टूबर@0.77 · Rath@1.62 · A@1.98 · पहुँचेगा@2.10 · बरेली@2.64 · और@3.34 · Rath@3.59 · B@3.86 · कुशीनगर@4.39

Map state at t=0: full view, Gorakhpur filled cobalt.
Scene 1 (0.0–1.4s): date chip "14 Oct 2026" pops top-right; counter "1 / 75".
Scene 2 (1.4–3.0s): on "Rath A" (~1.4s) a dashed route draws from Gorakhpur westward to Bareilly (#2) with an "A" rath badge riding its head; Bareilly fills on arrival (~2.6s "बरेली"), label "बरेली".
Scene 3 (3.0–end): on "Rath B" (~3.6s) a second dashed route draws from Gorakhpur east to Kushinagar (#3) with a "B" badge; Kushinagar fills (~4.5s), label "कुशीनगर"; counter ticks to "3 / 75". Hold.

## Frame 9 — Stops 4–5: Moradabad + Maharajganj

- type: feature_showcase
- scene: Same map: Rath A continues to Moradabad, Rath B to Maharajganj; date chip 16 Oct; counter 5/75
- duration: 6.37s
- poster: 5.1s
- transition_in: push-slide LEFT
- status: animated
- beat: Momentum
- voiceover: "सोलह अक्टूबर — मुरादाबाद... और महराजगंज।"
- src: compositions/frames/09-moradabad-maharajganj.html
- blueprint: compose
- focal: the two routes extending
- roles: shared district map (full view; Gorakhpur, Bareilly, Kushinagar filled; their routes drawn) = foreground · rath badges = supporting · date chip = supporting

voice word cues (seconds from frame start): सोलह@0.10 · अक्टूबर@0.88 · मुरादाबाद@1.62 · और@3.34 · महराजगंज@3.68

Map state at t=0: full view; Gorakhpur, Bareilly, Kushinagar filled; routes G→Bareilly and G→Kushinagar drawn.
Scene 1 (0.0–1.0s): date chip "16 Oct 2026" swaps in top-right; counter "3 / 75".
Scene 2 (1.0–2.6s): on "मुरादाबाद" (~1.7s) route extends Bareilly→Moradabad (#4) with badge A; Moradabad fills, label "मुरादाबाद".
Scene 3 (2.6–end): on "महराजगंज" (~3.6s) route extends Kushinagar→Maharajganj (#5) with badge B; it fills, label "महराजगंज"; counter "5 / 75". Hold.

## Frame 10 — All 75 districts

- type: social_proof
- scene: Fast montage: districts 6–75 fill one by one in planner order; a name ticker streams; phase bands; counter 5→75
- duration: 16.96s
- poster: 13.6s
- transition_in: cut
- status: animated
- beat: Momentum → awe
- voiceover: "फिर बिजनौर, बस्ती, सहारनपुर, प्रयागराज, कानपुर, झाँसी... जनवरी में मेरठ, आगरा, वाराणसी, लखनऊ... और मार्च में cluster यात्राएं — बुंदेलखंड से तराई तक।"
- src: compositions/frames/10-all-districts.html
- blueprint: compose
- focal: the map filling district by district
- roles: shared district map = foreground (left 60%) · name ticker + phase band + counter = foreground (right column)

voice word cues (seconds from frame start): फिर@0.10 · बिजनौर@0.48 · बस्ती@1.26 · सहारनपुर@2.09 · प्रयागराज@3.20 · कानपुर@4.35 · झाँसी@5.12 · जनवरी@6.63 · में@7.24 · मेरठ@7.37 · आगरा@8.00 · वाराणसी@8.76 · लखनऊ@9.71 · और@11.21 · मार्च@11.51 · में@11.94 · cluster@12.10 · यात्राएं@12.56 · बुंदेलखंड@13.51 · से@14.24 · तराई@14.46 · तक@14.86

Map state at t=0: full view; districts 1–5 filled.
Scene 1 (0.0–5.5s) PHASE 1: districts #6–#23 fill in planner order (≈0.28s apart, starting 0.3s); each fill flashes its Hindi name in the right-column ticker (large current name, previous names scrolling up and fading). Phase band top-right: "Phase 1 · Oct–Nov 2026". Counter counts with fills ("N / 75").
Scene 2 (5.5–10.8s) PHASE 2: band swaps to "Phase 2 · Jan–Mar 2027"; districts #24–#56 fill (≈0.16s apart).
Scene 3 (10.8–15.0s) PHASE 3: band "Phase 3 · Cluster Yatras · Mar 2027"; districts #57–#75 fill (≈0.2s apart), cluster members filling together per cluster.
Scene 4 (15.0–end): counter lands on "75 / 75" with a scale pop; the whole map gets one glow pulse. Hold.

## Frame 11 — हर ज़िला · हर शहर · हर पिनकोड

- type: branding
- scene: Inverted cobalt frame: three stacked kinetic lines hit on the voice — हर ज़िला / हर शहर / हर पिनकोड — with a rolling pincode counter; 'पूरे 75 ज़िले'
- duration: 8.39s
- poster: 6.7s
- transition_in: zoom-through
- status: animated
- beat: Pride
- voiceover: "हर ज़िला। हर शहर। हर pincode। पूरे पचहत्तर ज़िले!"
- src: compositions/frames/11-every-pincode.html
- blueprint: kinetic-type-beats (Reproduce)
- focal: the three kinetic lines
- roles: full cobalt field = background · three lines (cream) = foreground · rolling 6-digit pincode digits = supporting · faint lit-map watermark = background

voice word cues (seconds from frame start): हर@0.10 · ज़िला@0.44 · हर@1.70 · शहर@2.03 · हर@3.35 · pincode@3.69 · पूरे@5.19 · पचहत्तर@5.66 · ज़िले@6.26

Full cobalt (#1e2bfa) field, faint cream lit-map watermark (opacity 0.08) of all 75 districts.
Scene 1 (0.0–1.6s): "हर ज़िला" (cream Hindi 130px 700) slams in at y≈230 on 0.1s.
Scene 2 (1.6–3.3s): "हर शहर" slams in at y≈420 on 1.7s.
Scene 3 (3.3–5.0s): "हर पिनकोड" slams in at y≈610 on 3.35s; beside it a 6-digit odometer of pincode-style digits rolls (deterministic sequence through 2xxxxx values like 273001 → 243001 → 274401 → 244001 → 273303) and settles.
Scene 4 (5.0–end): "पूरे 75 ज़िले" (Space Grotesk/Hindi 60px, cream, inside a cream-outlined pill) rises at y≈800 on 5.2s. Hold.

## Frame 12 — Join the Yatra

- type: cta
- scene: Clean CTA: यात्रा से जुड़ें pill, workshop chip 4–8 PM, then the closing line गुणवत्ता — हर द्वार तक with भरोसा callback
- duration: 16.33s
- poster: 13.1s
- transition_in: crossfade
- status: animated
- beat: Resolve
- voiceover: "अपने ज़िले में गुणवत्ता यात्रा आए, तो ज़रूर जुड़िए — शाम चार से आठ बजे, NABH workshop। क्योंकि quality सिर्फ़ एक certificate नहीं — भरोसा है। गुणवत्ता — हर द्वार तक।"
- src: compositions/frames/12-cta.html
- blueprint: titlecard-reveal (Adapt)
- focal: the 'यात्रा से जुड़ें' CTA pill
- roles: CTA pill = foreground · workshop chip = supporting · closing line = foreground · small lit UP map = background (right, dim)

voice word cues (seconds from frame start): अपने@0.10 · ज़िले@0.54 · में@0.83 · गुणवत्ता@0.98 · यात्रा@1.57 · आए@2.12 · तो@2.85 · ज़रूर@3.00 · जुड़िए@3.37 · शाम@4.05 · चार@4.50 · से@4.81 · आठ@5.10 · बजे@5.39 · NABH@5.94 · workshop@6.40 · क्योंकि@7.86 · quality@8.33 · सिर्फ़@8.85 · एक@9.21 · certificate@9.45 · नहीं@10.16 · भरोसा@10.86 · है@11.41 · गुणवत्ता@12.47 · हर@13.56 · द्वार@13.87 · तक@14.21

Scene 1 (0.0–3.5s): left side: "अपने ज़िले में" (Hindi h3, text-muted) then the cobalt cta-button pill "यात्रा से जुड़ें · Join the Yatra" scales in (on "जुड़िए" ~2.6s). Right side: the lit district map, dim (opacity 0.35).
Scene 2 (3.5–7.5s): on "चार से आठ" (~3.9s) a chip "NABH Entry Level Certification Workshop · 4 PM – 8 PM" slides in under the pill.
Scene 3 (7.5–11.5s): on "certificate नहीं" (~8.6s) the word "certificate" appears struck through, then on "भरोसा" (~10.3s) "भरोसा" (Hindi 120px primary) lands — callback to frame 1 — with a tiny heartbeat line under it.
Scene 4 (11.5–end): on "गुणवत्ता — हर द्वार तक" (~12.3s) the closing line "गुणवत्ता — हर द्वार तक" (Hindi 84px, text) settles at the bottom of the content area (y≈760). Hold.

## Frame 13 — End card: QCI presents

- type: branding
- scene: End lockup: QCI logo large, 'गुणवत्ता यात्रा · उत्तर प्रदेश', partner logos row (NABH, PM-JAY)
- duration: 4.5s
- poster: 3.6s
- transition_in: crossfade
- status: animated
- beat: Closure
- voiceover: ""
- src: compositions/frames/13-endcard.html
- blueprint: logo-assemble-lockup (Adapt)
- focal: QCI logo
- roles: assets/logos/qci.png = foreground subject · title = foreground · partner row (assets/logos/nabh.png, assets/logos/pmjay.png) = supporting

voice word cues (seconds from frame start): (silent frame)

Scene 1 (0.0–1.4s): QCI logo (assets/logos/qci.png, ~620px wide) scales 0.92→1 + fades in at center y≈330 with the label "प्रस्तुति · Presented by" above it (eyebrow).
Scene 2 (1.4–2.6s): "गुणवत्ता यात्रा · उत्तर प्रदेश" (Hindi 64px) rises under it.
Scene 3 (2.6–4.5s): a hairline divider draws and a partner row fades in at y≈760: NABH logo (assets/logos/nabh.png, height 90px) and PM-JAY emblem (assets/logos/pmjay.png, height 110px). Final frame: in the last 0.6s the whole frame fades to cream.

