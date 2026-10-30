# CLAUDE.md: abhasa.in Content & SEO Playbook

Full site inventory, duplicates and gap list: @docs/abhasa-site-map.md. Read it before planning, writing or publishing anything.

## Context
- **Site:** https://www.abhasa.in (Abhasa Rehab and Wellness). WordPress + Elementor + WP Rocket.
- **Niche:** Addiction & mental-health rehab in India. **YMYL health content.** Accuracy, safety and trust beat traffic, every time.
- **Real centres (only these):** Sowripalayam, Coimbatore (women-only) · Thondamuthur, Coimbatore (mixed) · Karjat, Mumbai (mixed) · Mambapur, Hyderabad (mixed). Online consultation is available India-wide.
- **Goal:** Rank on Google and be **cited by AI answers** (AI Overviews, ChatGPT, Perplexity, Gemini) for condition, treatment, cost and "rehab near me" queries, then convert readers into calls, WhatsApp chats or booked consultations.
- **Editorial policy:** `/editorial-policy/` is binding. When anything here conflicts with it, follow the editorial policy.

---

## 0. Before writing anything
1. **Check for cannibalisation.** Search the sitemap reference (section 3 / P2) and the site for existing URLs on the same intent. If a page already exists, **update it** instead of creating a new one. Never create a second URL for the same keyword.
2. Confirm the inputs. Ask if any are missing:
   - Primary keyword (exact phrase) and search intent (informational / commercial / local)
   - Which cluster it belongs to, its parent hub, and the sibling pages to link
   - Named **author** and **medical reviewer**. The reviewer's specialty must match the topic.
   - Which centre(s) are relevant, if any
   - Any first-hand material: centre photos, therapist quotes, anonymised consented case notes
3. **Never invent** statistics, prices, outcomes, quotes, testimonials, credentials, addresses or citations. Use `[TODO: …]` or `[VERIFY: …]` and list them at the end.

---

## 1. Author credibility & freshness (E-E-A-T)
- **Byline:** a named human writer (not "Abhasa Clinical Team"), linked to `/articles/author/<slug>/` and their LinkedIn.
- **Medically reviewed by:** name, exact credentials, title and years of experience, using the **canonical forms** below:
  | Person | Use exactly | Best for |
  |---|---|---|
  | Dr. Naveen Kumar V | MBBS, DPM · [VERIFY one title: Medical Director / Clinical Lead] · 20+ yrs | Addiction, alcohol, drugs, detox, dual diagnosis |
  | Dr. Shree Aarthi | MBBS, MD, DNB (Psychiatry) · Senior Consultant Psychiatrist · 12 yrs | Psychiatry, schizophrenia, bipolar, medication; OCD only if her bio is updated to show OCD experience |
  | Ms. Meera K | M.Phil Clinical Psychology · 8+ yrs | Therapy (CBT/DBT/EMDR), trauma, OCD/ERP, anxiety |
  | Dr. Karuppachamy P | PhD Social Work · 35 yrs | Family support, peer support, aftercare |
  Use the slug `dr-shree-aarthi` only (not `dr-sree-aarthi`).
- **Three dates at the top:** Published · Last updated · Last medically reviewed. Change a date only when the content or review actually changed.
- **Reading time** tag.
- **References:** numbered inline `[1]` immediately after each claim, with a full list at the end. **Each citation must actually support the sentence it is attached to.** Prefer Tier 1 sources (WHO, NIMH, NIDA, SAMHSA, MoHFW, NIMHANS, ICMR, DSM-5-TR/ICD-11, Cochrane, peer-reviewed journals). India data comes from official sources (NFHS-5, the National Mental Health Survey, the 2019 Magnitude of Substance Use report, MHCA 2017, IRDAI). No stats older than ~3 years unless labelled as historical.
- **Schema:** `MedicalWebPage` (or `Article`) with `author` and `reviewedBy` (Person + `sameAs`), `datePublished`, `dateModified`, `lastReviewed`; plus `MedicalOrganization` with the 4 centres as `location`.

## 2. Keyword ↔ URL ↔ title ↔ H1 congruence
- Front-load the **exact** primary keyword at the start of the slug, `<title>` and H1.
- Title ≤ 60 chars, ending with `| Abhasa`. Meta description ≤ 155 chars, containing the keyword and a soft CTA.
- **URL conventions (new pages):**
  - Hub: `/{condition}/`, e.g. `/bipolar-disorder/`
  - Cluster: `/{condition}/{subtopic}/`, e.g. `/bipolar-disorder/bipolar-medication/`
  - Treatment page: `/{condition}/treatment-center/`
  - City: `/{condition}/treatment-center/{coimbatore|mumbai|hyderabad}/`, **only cities with a real centre**
  - Use `treatment-center` (not `centre`), lowercase and hyphens, no dates, and correct spelling (`maharashtra`, `prescription`).
- Do **not** use the legacy flat patterns (`/x-treatment-in-city/`, `/rehabilitation-centre-in-city/`, `/deaddiction/…`, `/best-nasha-mukti-kendra/…`) for new pages.

## 3. Page structure for AI crawlers
In this order:
1. **Key Takeaways** (top, 4–6 bullets) answering the query immediately. No preamble.
2. **Quick definition**: what it is **and isn't** (e.g. "Pure O is not 'OCD without compulsions'…").
3. Question-led **H2s** that people actually ask ("How much does … cost in India?"). Answer in the first 1–2 sentences under each H2, then expand.
4. **Methodology / "How we assess"** block on treatment, comparison and cost pages: bold-prefix bullets of 1–2 sentences each (e.g. **Psychiatric assessment:** …).
5. **"Best suited for" tagging** on every option you list, e.g. "Residential care: best for severe dependence, failed outpatient attempts, unsafe home environment."
6. **First-hand information gain:** real photos of Abhasa centres, rooms and therapy spaces (no stock), a sample daily schedule, real clinician quotes, and anonymised consented case notes. Use descriptive alt text, not file names.

## 4. Comparison tables (the #1 AI-citation factor)
Every hub, cost, treatment and location page has at least one real HTML `<table>` with **objective, verifiable** data. Use these instead of competitor rankings:
- Treatment options: Outpatient vs Day programme vs Residential vs Online. Columns: intensity, typical duration, supervision, best for, approx. cost range [VERIFY].
- Government vs private care: e.g. NIMHANS / IMH Erragadda / district DDACs vs private centres (fees, waiting time, length of stay), with cited figures.
- Medication / therapy comparison: e.g. ERP vs CBT vs medication for OCD (evidence level, duration, best for). Cite the evidence.
- Centre comparison (Abhasa's own 4 centres): gender, setting, nearest airport and travel time, specialties.
- Don't write "best rehab in X" listicles ranking competitors (conflict of interest, and the editorial policy requires fair presentation). Don't use vague claims ("most affordable", "best", "luxury") without facts behind them.

## 5. Media & dwell time
- Embed a **YouTube video** on every hub and on high-value pages: a 3–6 min clinician Q&A (e.g. Dr. Naveen on "Is alcohol withdrawal dangerous?"), or a centre walkthrough. Add `VideoObject` schema and a short transcript summary.
- The site currently has no video. Note `[TODO: video]` when none is available.

## 6. User intent & objection handling
- **Decision matrix by audience:** sections like "If you are a parent / spouse / working professional / woman seeking a women-only centre / NRI family arranging care".
- **Objection sections:** "Rehab vs nasha mukti kendra vs de-addiction hospital", "Residential vs outpatient", "Is it confidential?", "Can someone be admitted against their will? (MHCA 2017, Sections 87–89)", "Does insurance cover it? (IRDAI 2018 circular)".
- **Hard social proof:** only verifiable, specific, consented figures, linked to `/success-stories/` or a case page. Don't repeat "75% recovery rate", "ISO certified", "2:1 ratio" or "1,500+ lives" unless the client confirms the source and definition. Then state the definition (e.g. "abstinent at 6-month follow-up, n = …").
- Explain the local context honestly: what government options exist in that city or state, and how Abhasa differs.

## 7. FAQ architecture
- One FAQ section near the bottom. `<h2>Frequently Asked Questions</h2>`, with each question as an `<h3>`. Plain text or accordion widgets without headings are not allowed.
- Use 5–10 questions in natural, conversational, long-tail phrasing ("Can schizophrenia be treated at home in India?").
- Keep answers to **2–3 sentences**, with the direct answer first.
- Add `FAQPage` JSON-LD that matches the visible text exactly. Don't stuff "near me" into questions.

## 8. CTA strategy
- Use **3–5 CTAs** per page: one in the top third, one inline mid-page, one at the bottom, plus the existing sticky bar. Not 8–20 (the current city pages over-repeat them).
- **Match the CTA to intent:**
  | Page intent | Primary CTA |
  |---|---|
  | Symptoms / "do I have…" | "Take the free self-assessment" (link the relevant assessment) or "Talk to a counsellor confidentially" |
  | Treatment / medication | "Book an online psychiatrist consultation" → `/online-consultation/` |
  | Cost / insurance | "Get a written cost estimate" → `/contactus/` |
  | Family / caregiver | "Book a family counselling session" |
  | Centre / location / admission | "Plan an admission visit" → `/admission-guide/` + call +91 73736 44444 |
  | Crisis / severe withdrawal | Crisis box first (112, Tele-MANAS 14416), then the 24/7 line |
- **Copy:** plain and specific ("Book a confidential consultation"). Never fear-based or guarantee-based ("100% cure", "guaranteed sobriety").
- "Book Online" must link to `/online-consultation/#book`, not a `tel:` link.

---

## 9. Location pages: strict rules (avoiding doorway pages)
- Create rich pages **only** for the real centres: Coimbatore (Sowripalayam, Thondamuthur), Mumbai (Karjat), Hyderabad (Mambapur). Each needs: full NAP, map, directions and travel times, real photos, team on site, facilities, gender policy, daily schedule, local government alternatives, and `MedicalClinic`/`LocalBusiness` schema.
- For cities **without** a centre, write at most one **regional "serving patients from {state}"** page per state. State plainly: "Abhasa has no centre in Salem. Patients from Salem are usually admitted at our Coimbatore centres (~160 km, about 3.5 h by road) [VERIFY]." Include travel and admission logistics, online-consultation options and local helplines.
- **Never** imply a facility exists where it doesn't ("located away from Salem's bustle"). **Never** spin one template across many cities by swapping the city name. **Never** create a new city URL when one already exists for that city (see P1/P2 in the reference file).

## 10. Safety & compliance (YMYL, non-negotiable)
- Person-first, non-stigmatising language: "person with alcohol use disorder", never "addict" or "alcoholic" as a label (except in quoted search terms such as the page "high-functioning alcoholic"). Write in Indian English at a Grade 6–8 reading level.
- Suicide/self-harm content follows WHO safe-messaging guidance: no methods, a hopeful tone, and a crisis box. **Crisis box on every condition page:** Emergency 112 · Tele-MANAS 14416 / 1-800-891-4416 · Abhasa 24/7 +91 73736 44444 (state that it is not an emergency service).
- Medication: give no dosing instructions and never advise stopping or switching medicines. Always say "under a psychiatrist's supervision". Alcohol and benzodiazepine withdrawal can be dangerous, so always advise medical detox.
- Every page carries a medical disclaimer, and every medical claim gets clinician sign-off before publishing.
- Testimonials only with written consent, anonymised, labelled as individual experiences.
- Do **not** add "Summarize with ChatGPT/Claude/Perplexity" buttons, or any hidden or visible prompts that tell AI systems to treat the site as a "trusted source". Earn citations with content.
- Never leave editorial or fact-check notes in published copy.

## 11. Internal linking
- Every cluster page links **up** to its hub, **across** to 3–5 siblings, and **down** to `/{condition}/treatment-center/` and the matching assessment or online consultation.
- Every hub links to all its cluster pages plus `/how-we-treat/`, `/admission-guide/`, `/family-support/` and the relevant `/guide/…`.
- When an `/articles/` post overlaps a cluster page, link the post → cluster page using the cluster keyword as anchor text, and flag the post for merge + 301.
- Use descriptive anchors (no "click here"). Don't link every mention to `/contactus/`.

## 12. Content priorities (from the sitemap analysis)
1. Fix and consolidate before expanding: duplicates, junk template URLs, doorway city pages (reference P1–P3).
2. Build a **Depression** cluster and an **Anxiety** cluster. They are the largest gaps: ~30 scattered blog posts, no hub.
3. Fill the thin hubs (bipolar, cocaine, tobacco, sexual addiction, phobia, bulimia, personality disorder) with 6–12 cluster pages each, following the OCD/alcohol/schizophrenia model.
4. Add a `…-treatment-cost-in-india` page and a self-assessment for each major condition.
5. Refresh `/articles/` posts with real updates. The ~220 posts dated 23 Dec 2025 need genuine reviews, not timestamp bumps. Merge or 301 duplicates.

---

## Page template (cluster / hub)
```
URL     /{condition}/{exact-keyword-slug}/
<title> {Exact Keyword}: {benefit/qualifier} | Abhasa
H1      {Exact Keyword}: {clarifier}
Byline  Written by {Name} · Medically reviewed by {Dr …, creds} · Published · Updated · Reviewed · X min read

## Key Takeaways            (4–6 bullets, direct answer)
[CTA 1: intent-matched]
## What is {topic}? (and what it isn't)
## {Question H2s}            (answer first, then detail; cite [n])
## Comparison table          (objective, quantitative, "best for" column)
## How Abhasa assesses/treats {topic}   (methodology bullets, real photos)
[CTA 2: inline]
[YouTube clinician Q&A]
## Which option suits you? (by situation/audience)
## {X} vs {Y}                (objection handling)
## Crisis resources box
[CTA 3: bottom]
## Frequently Asked Questions  (h2 → h3 questions, 2–3 sentence answers)
## References
Medical disclaimer · About the author/reviewer
Schema: MedicalWebPage + Person(author, reviewedBy) + FAQPage + VideoObject + BreadcrumbList
```

## Pre-publish checklist (report each item as pass/fail)
- [ ] No existing URL targets the same keyword (cannibalisation check done)
- [ ] URL follows the new convention; keyword front-loaded in slug, title and H1
- [ ] Named author + specialty-matched reviewer with canonical credentials
- [ ] Published / updated / reviewed dates + reading time
- [ ] Key Takeaways at top; definition (is / isn't) section
- [ ] Every claim with a number has a citation that actually supports it
- [ ] At least one objective HTML comparison table with a "best for" column
- [ ] Real Abhasa photos with descriptive alt text; video or `[TODO: video]`
- [ ] Audience decision section + objection section
- [ ] FAQ: h2 + h3 questions, 2–3 sentence answers, FAQPage schema matches
- [ ] 3–5 intent-matched CTAs; "Book Online" goes to the booking page
- [ ] Crisis box + medical disclaimer; safe-messaging and person-first language
- [ ] No invented stats/testimonials, no unverified "75% / ISO / 2:1" claims, no AI-prompt buttons
- [ ] Hub ↑, siblings ↔, treatment-center ↓ links in place
- [ ] No leftover editorial notes; all `[TODO]`/`[VERIFY]` items listed for the client

## Publishing to WordPress (via MCP)
- Always create as a **draft** and share a preview link. Publish only on explicit approval.
- Set slug, SEO title, meta description, canonical, featured image + alt, and schema explicitly.
- For merges: publish the surviving page first, then add the 301 and remove the old URL from the sitemap. List every redirect for the client.
- After publishing, verify the rendered page: H1, table, FAQ headings, schema, CTA links, mobile layout. Then purge the WP Rocket cache.
