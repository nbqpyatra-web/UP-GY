---
format: 1920x1080
duration: 60s
message: "Gunvatta Yatra is taking quality to every corner of Uttar Pradesh — join the journey."
arc: story-explainer with how-to
audience: UP MSMEs, healthcare & education institutions, government and the general public
mode: autonomous
language: hi-en
music: none
captions: skipped (no narration — on-screen text carries the story)
---

## Video direction

- palette: `frame.md` blue-professional — cream `bg` ground, cobalt `primary` the ONLY accent (route line, pins, CTA pill, eyebrows), `text` near-black headlines, `text-muted` English sub-lines, `card-tinted` for stop cards. No other hues.
- type: Hindi lines in Noto Sans Devanagari (frame.md `hindi` token, `assets/fonts/`), English in Space Grotesk (display) / Inter (body). Hindi is the hero line; English sits beneath it, smaller, `text-muted`.
- shared map stage (frames 02–07 — MUST be identical so the push-slides read as one continuous journey): UP outline from `assets/up-map.json` (`path`, viewBox `0 0 1000 973`), drawn as an SVG at left 150px, top 80px, width 781px, height 760px (scale 0.781). Outline: `primary` stroke 2.5px, fill `card-bg`. City pins (map-space coords in `up-map.json.cities`): Agra, Kanpur, Lucknow, Varanasi, Gorakhpur. Route = dashed cobalt polyline (stroke 4px, dash 14 10) Agra→Kanpur→Lucknow→Varanasi→Gorakhpur. Visited pins: solid cobalt dot r=12 + white center r=4 + city label (Hindi, 26px, `text`) beside it. Current pin gets a soft cobalt pulse ring. Stop card: right column x 1010–1790, vertically centered ~y 450.
- motion grammar: long-tail eases (power3.out default), reveals paced to the beat (silent film — paced to reading time, one idea per ~1.2–1.8s), never front-load. Route segments draw with stroke-dashoffset (mask technique so the dash pattern is kept). Holds are still — no breathing, no drift.
- rhythm: 01 kinetic open → 02 the big map build (energy peak) → 03–07 a steady repeating stop rhythm → 08 held breather/turn → 09 clean held end card.
- negative list: no official logos or emblems, no invented numbers/dates, no photos, no gradients/bokeh, no shadows (except CTA), no slideshow front-loading, no screensaver floating.

## Frame 1 — Hook: quality, everywhere

- type: hook
- scene: A single cobalt dot pulses on cream; Hindi line types beside it, English sub-line settles under it
- duration: 6s
- poster: 4.5s
- transition_in: cut
- status: animated
- persuasion: Rhetorical question + direct address
- beat: Curiosity + recognition
- voiceover: "क्या गुणवत्ता हर ज़िले तक पहुँच सकती है? — What if quality reached every district of UP?"
- src: compositions/frames/01-hook.html
- blueprint: kinetic-type-beats (Adapt)
- focal: the Hindi question line
- roles: cobalt dot = supporting · Hindi question = foreground subject · English sub-line = supporting · faint hairline grid = background (dim ~30%)

narrativeRole: Opens the gap — quality is usually something "elsewhere"; asks whether it can reach every district.
keyMessage: Quality is not just for big cities — this is about all of Uttar Pradesh.

Adapt: keep the beat-by-beat word landing; the payoff is a word-swap emphasis on "हर ज़िले" (every district).
Scene 1 (0.0–1.2s): cream ground + faint cobalt hairline grid; a single cobalt dot springs in at center-left and pulses once. Centered, sparse.
Scene 2 (1.2–3.4s): the Hindi line "क्या गुणवत्ता हर ज़िले तक पहुँच सकती है?" reveals word by word (per-word reveal, rise + fade) at h1 scale, centered ~y 420; "हर ज़िले" lands last-but-one in cobalt with an underline that draws on.
Scene 3 (3.4–4.6s): English sub-line "What if quality reached every district of UP?" fades up beneath (body, text-muted).
Scene 4 (4.6–6.0s): held read; the dot slides to the line's left edge and holds still (it will become the route start in 02).

## Frame 2 — Introducing Gunvatta Yatra

- type: product_intro
- scene: The dot becomes the start of a route; the UP outline draws on, a dashed route traces west→east through five pins; title lockup "गुणवत्ता यात्रा / Gunvatta Yatra · Uttar Pradesh" with "An initiative of the Quality Council of India"
- duration: 8s
- poster: 6s
- transition_in: crossfade
- status: animated
- persuasion: Concept announcement + frame-then-fill (show the whole route before visiting each stop)
- beat: Clarity + anticipation
- voiceover: "गुणवत्ता यात्रा — a quality journey across Uttar Pradesh, by the Quality Council of India."
- src: compositions/frames/02-intro.html
- blueprint: logo-assemble-lockup (Adapt)
- focal: the UP outline with the 5-pin route
- roles: UP outline = foreground subject · dashed route + 5 pins = supporting · title lockup = foreground (right column) · hairline grid = background

narrativeRole: Names the protagonist (the Yatra) and states the thesis by beat 2: one journey, the whole state.
keyMessage: Gunvatta Yatra is QCI's journey taking quality to every corner of UP.

Adapt: keep the signature "outline draws on, then the lockup resolves"; the mark being assembled is the UP map + route.
Scene 1 (0.0–2.4s): UP outline draws on (stroke-dashoffset) on the shared map stage, fill fades to card-bg as the stroke closes.
Scene 2 (2.4–4.6s): the dashed route traces Agra→Kanpur→Lucknow→Varanasi→Gorakhpur; the 5 pins pop in sequence as the route reaches each (pins WITHOUT labels here — small, r=8).
Scene 3 (4.6–6.6s): right column: eyebrow "उत्तर प्रदेश · UTTAR PRADESH" (h4-eyebrow, primary), then the title "गुणवत्ता यात्रा" (Hindi, ~120px, 700, text) rises in, then "Gunvatta Yatra" (h2, primary) beneath.
Scene 4 (6.6–8.0s): "An initiative of the Quality Council of India" pill (tag-pill style, larger 22px) fades up under the title; hold still.
NOTE: frame 03 starts with the route reset to only the Agra pin lit — that is the journey beginning.

## Frame 3 — Stop 1: Agra · Skilling

- type: feature_showcase
- scene: Map stage, camera eased onto Agra pin (west); stop card slides in: "पड़ाव 1 · आगरा" / "Skilling — quality skills, quality services"
- duration: 6.5s
- poster: 4.5s
- transition_in: push-slide LEFT
- status: animated
- persuasion: Signposting (numbered stops) + concretization
- beat: Momentum
- voiceover: "पड़ाव 1 · आगरा — कौशल. Skilled people deliver quality services."
- src: compositions/frames/03-agra.html
- blueprint: compose
- focal: the Agra stop card + pin
- roles: shared map stage = background-midground · Agra pin + pulse = foreground · stop card = foreground subject (right column)

narrativeRole: First step of the journey — quality starts with people's skills.
keyMessage: Skilling is the foundation of quality.

Map stage state at t=0: outline fully drawn (no route segments yet), all 5 pins shown faint (opacity 0.25, r=8).
Scene 1 (0.0–1.4s): Agra pin activates (scales up to the visited style, pulse ring), label "आगरा" appears beside it.
Scene 2 (1.4–3.4s): stop card slides in from right (card-tinted): eyebrow "पड़ाव 1 · STOP 1", then Hindi headline "कौशल" (~96px 700), then English "Skilling" (h2, primary).
Scene 3 (3.4–5.0s): card line "Quality skills → quality services" (body, text-muted) fades up, with a small 3-segment progress bar (cobalt) filling to 1/5.
Scene 4 (5.0–6.5s): held read, still.

## Frame 4 — Stop 2: Kanpur · MSMEs (ZED & LEAN)

- type: feature_showcase
- scene: Same map stage, route extends to Kanpur; stop card: "पड़ाव 2 · कानपुर" / "MSMEs — ZED: Zero Effect, Zero Defect · LEAN"; two chips pop
- duration: 6.5s
- poster: 4.5s
- transition_in: push-slide LEFT
- status: animated
- persuasion: Signposting + coined term (Zero Effect, Zero Defect)
- beat: Comprehension
- voiceover: "पड़ाव 2 · कानपुर — उद्योग. MSMEs adopt ZED and LEAN: zero defect, zero effect."
- src: compositions/frames/04-kanpur.html
- blueprint: compose
- focal: the Kanpur stop card with ZED + LEAN chips
- roles: shared map stage = background-midground · Agra→Kanpur route segment + pin = foreground · stop card = foreground subject

narrativeRole: Industry stop — QCI's ZED and LEAN help MSMEs build better and cleaner.
keyMessage: MSMEs can certify quality through ZED and LEAN.

Map stage state at t=0: outline drawn; Agra visited (solid pin + label); other pins faint.
Scene 1 (0.0–1.5s): route segment Agra→Kanpur draws on (dashed); Kanpur pin activates with pulse, label "कानपुर".
Scene 2 (1.5–3.3s): stop card slides in: eyebrow "पड़ाव 2 · STOP 2", Hindi headline "उद्योग", English "MSMEs" (h2, primary).
Scene 3 (3.3–5.0s): two pill chips pop in one after another: "ZED · Zero Effect, Zero Defect" and "LEAN"; progress bar fills to 2/5.
Scene 4 (5.0–6.5s): held read, still.

## Frame 5 — Stop 3: Lucknow · Healthcare

- type: feature_showcase
- scene: Same map stage, route extends to Lucknow; stop card: "पड़ाव 3 · लखनऊ" / "Healthcare — safer, accredited care"
- duration: 6.5s
- poster: 4.5s
- transition_in: push-slide LEFT
- status: animated
- persuasion: Signposting + concretization
- beat: Confidence
- voiceover: "पड़ाव 3 · लखनऊ — स्वास्थ्य. Quality care, patient safety first."
- src: compositions/frames/05-lucknow.html
- blueprint: compose
- focal: the Lucknow stop card
- roles: shared map stage · Kanpur→Lucknow route segment + pin = foreground · stop card = foreground subject

narrativeRole: Health stop — quality reaches hospitals and clinics.
keyMessage: Quality in healthcare means safer care for every patient.

Map stage state at t=0: outline; route Agra→Kanpur drawn; Agra, Kanpur visited; others faint.
Scene 1 (0.0–1.5s): route Kanpur→Lucknow draws on; Lucknow pin activates with pulse, label "लखनऊ".
Scene 2 (1.5–3.3s): stop card slides in: eyebrow "पड़ाव 3 · STOP 3", Hindi headline "स्वास्थ्य", English "Healthcare" (h2, primary).
Scene 3 (3.3–5.0s): card line "Safer, accredited care for every patient" (body, text-muted); progress bar fills to 3/5.
Scene 4 (5.0–6.5s): held read, still.

## Frame 6 — Stop 4: Varanasi · Education

- type: feature_showcase
- scene: Same map stage, route extends to Varanasi; stop card: "पड़ाव 4 · वाराणसी" / "Education — quality learning, quality institutions"
- duration: 6.5s
- poster: 4.5s
- transition_in: push-slide LEFT
- status: animated
- persuasion: Signposting + concretization
- beat: Foresight
- voiceover: "पड़ाव 4 · वाराणसी — शिक्षा. Quality institutions shape quality futures."
- src: compositions/frames/06-varanasi.html
- blueprint: compose
- focal: the Varanasi stop card
- roles: shared map stage · Lucknow→Varanasi route segment + pin = foreground · stop card = foreground subject

narrativeRole: Education stop — quality in schools and colleges.
keyMessage: Quality education builds the next generation.

Map stage state at t=0: outline; route Agra→Kanpur→Lucknow drawn; three pins visited; others faint.
Scene 1 (0.0–1.5s): route Lucknow→Varanasi draws on; Varanasi pin activates with pulse, label "वाराणसी".
Scene 2 (1.5–3.3s): stop card slides in: eyebrow "पड़ाव 4 · STOP 4", Hindi headline "शिक्षा", English "Education" (h2, primary).
Scene 3 (3.3–5.0s): card line "Quality institutions, quality futures" (body, text-muted); progress bar fills to 4/5.
Scene 4 (5.0–6.5s): held read, still.

## Frame 7 — Stop 5: Gorakhpur · Citizens

- type: feature_showcase
- scene: Same map stage, route reaches Gorakhpur; all five pins now glow; stop card: "पड़ाव 5 · गोरखपुर" / "Citizens — quality as everyone's right"
- duration: 6.5s
- poster: 4.5s
- transition_in: push-slide LEFT
- status: animated
- persuasion: Signposting + build-up (all stops lit = the whole state)
- beat: Momentum + delight
- voiceover: "पड़ाव 5 · गोरखपुर — नागरिक. Quality is every citizen's right."
- src: compositions/frames/07-gorakhpur.html
- blueprint: compose
- focal: the fully lit route + Gorakhpur card
- roles: shared map stage · Varanasi→Gorakhpur segment + all 5 pins = foreground · stop card = foreground subject

narrativeRole: Final stop closes the loop from institutions to people; the fully lit route shows reach.
keyMessage: Quality is for every citizen, in every district.

Map stage state at t=0: outline; route up to Varanasi drawn; four pins visited; Gorakhpur faint.
Scene 1 (0.0–1.5s): route Varanasi→Gorakhpur draws on; Gorakhpur pin activates, label "गोरखपुर".
Scene 2 (1.5–3.3s): stop card slides in: eyebrow "पड़ाव 5 · STOP 5", Hindi headline "नागरिक", English "Citizens" (h2, primary).
Scene 3 (3.3–5.0s): card line "Quality is every citizen's right" (body, text-muted); progress bar completes 5/5; all five pins pulse once together in a stagger along the route (the whole state lit).
Scene 4 (5.0–6.5s): held read, still.

## Frame 8 — The vision: Aatmanirbhar → Daata Pradesh

- type: branding
- scene: Map pulls back and fades; two words on a line — "आत्मनिर्भर प्रदेश" morphs/arrow → "दाता प्रदेश"; English sub-line "From self-reliant to a state that gives back to the nation"
- duration: 6.5s
- poster: 5s
- transition_in: blur-crossfade
- status: animated
- persuasion: Before/after + distillation
- beat: Inspiration
- voiceover: "आत्मनिर्भर प्रदेश से दाता प्रदेश तक — from self-reliant to a state that gives back to the nation."
- src: compositions/frames/08-vision.html
- blueprint: kinetic-type-beats (Adapt)
- focal: the before→after word pair
- roles: 'आत्मनिर्भर प्रदेश' = supporting (before) · arrow = supporting · 'दाता प्रदेश' = foreground subject · faint UP outline watermark = background (opacity ~0.06)

narrativeRole: The "so what" — quality is how UP moves from self-reliance to giving back (UP Gunvatta Sankalp vision).
keyMessage: Quality turns UP into a state that gives back to India.

Adapt: keep the in-place escalation that resolves on a payoff word; the swap is self-reliant → giving.
Scene 1 (0.0–1.6s): faint UP outline watermark large behind; "आत्मनिर्भर प्रदेश" rises in (Hindi ~84px, 600, text), centered ~y 360.
Scene 2 (1.6–3.4s): a cobalt arrow draws downward/rightward; "दाता प्रदेश" lands beneath at larger scale (~130px, 700, primary) — the payoff.
Scene 3 (3.4–5.0s): English "From self-reliant to a state that gives back to the nation" (h3, text-muted) fades up under it.
Scene 4 (5.0–6.5s): held breather, still.

## Frame 9 — Join the Yatra

- type: cta
- scene: Clean end card: "यात्रा से जुड़ें · Join the Yatra" with a cobalt pill CTA, lockup "गुणवत्ता यात्रा · Quality Council of India", the small route mark returning as a callback
- duration: 7s
- poster: 5s
- transition_in: crossfade
- status: animated
- persuasion: Callback (route mark from frame 2) + direct ask
- beat: Resolve
- voiceover: "यात्रा से जुड़ें — Join the Gunvatta Yatra. गुणवत्ता, हर द्वार तक."
- src: compositions/frames/09-cta.html
- blueprint: titlecard-reveal (Adapt)
- focal: the 'यात्रा से जुड़ें · Join the Yatra' CTA pill
- roles: small route mark (callback: mini dashed line with 5 dots) = supporting · Hindi title = foreground · CTA pill = foreground subject · QCI text mark = supporting

narrativeRole: The ask — invite every viewer to take part.
keyMessage: Join the journey — quality, at every doorstep.

Adapt: keep the calm single-move reveal + still hold; a 3-step stack instead of a chain.
Scene 1 (0.0–1.6s): a mini route mark (dashed cobalt line through 5 dots, ~420px wide) draws left→right at ~y 300 (callback to 02).
Scene 2 (1.6–3.4s): "गुणवत्ता, हर द्वार तक" (Hindi ~96px 700 text) slides up beneath; then "Quality, at every doorstep" (h3, text-muted).
Scene 3 (3.4–5.0s): the cta-button pill "यात्रा से जुड़ें · Join the Yatra" (cobalt fill, cream text, ~40px) scales in at ~y 680.
Scene 4 (5.0–7.0s): text mark "Gunvatta Yatra · Quality Council of India" (counter style, 20px, text-muted) fades in at ~y 820; final frame: everything holds still, then a gentle fade of the whole frame to cream over the last 0.6s.
