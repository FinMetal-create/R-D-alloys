# 07 — Thermomechanical processing: rolling, extrusion, forming

**Scope.** Physical-metallurgy view of the wrought-Al process chain *after casting*: preheat/homogenisation as a working step → hot breakdown and tandem hot rolling → coiling → cold rolling (sheet, fin, foil) → intermediate/final anneal; continuous-casting routes; direct/indirect extrusion (incl. multi-port heat-exchanger tube); constitutive (hot and cold) flow-stress laws; texture/earing; sheet formability metrics. Priority alloys: 3xxx heat-exchanger/foil/fin (AA3102, AA3207, 3003, 3004/3105), plus 1xxx, 5xxx, 6xxx, 8xxx (8011/8006).

**Status:** literature distillation, 2026-10-12. Every number carries a source tag `[Ref p./§]`. Text marked **(general knowledge)** is not in the accessible sources and is kept minimal. Text marked **(derived)** is arithmetic done here from cited inputs. Text marked **(inference)** is a design conclusion drawn here from cited facts. `[INT-…]` refs are the user's own working spreadsheets — they are *heuristics/models, not literature*, and are flagged as such.

**Biggest caveat.** The Drive text extraction truncates large books. The chapters that hold the per-alloy hot-working constants (Sheppard Ch. 4–6; Totten Ch. 7 *Rolling*, Ch. 8 *Extrusion*, Ch. 18 *Sheet forming*) were **not** returned. So the per-alloy sinh-law table (§3.3) is mostly empty and is the top retrieval gap (§11).

**Full-text pass, 2026-10-12.** The PDFs were downloaded whole (base64) and converted locally with `pdftotext`. This worked for [RR] (3.81 MB), which is now read in full. It **failed** for [RA] (7.19 MB) and for both copies of [SH] (10.46 and 10.51 MB); the exact errors are in the note under §0. So §3.3, G1, G2 and G14 are still open.

---

## 0. Sources and coverage

| Ref | Title (author, year) | Drive link | Readability / coverage actually read |
|---|---|---|---|
| RA | *Rolling Aluminum: From the Mine Through the Mill*, 3rd ed. (The Aluminum Association, 2007) | https://drive.google.com/file/d/1w70bnhbLUlg5Tg4tlFIa0pVEI58GRfht/view | Clean text. Sections 1–8 read in full, glossary to "Casting" (~75 % of the book). Appendices (alloy/temper tables, typical properties, tolerances) **not returned**. Introductory and mostly qualitative, but it gives the practical plant numbers. **2026-10-12:** whole-file download failed twice (7,188,660 B; duplicate 1i-3uwU8kh3uFXgSm5umZg3Hu0YSH4iAg has the same size), so coverage is unchanged. |
| RR | *A Basic Understanding of the Mechanics of Rolling Mill Rolls* (K.H. Schröder, 2003). File "155680328-Rolling.pdf" | https://drive.google.com/file/d/1I9Qa_iFiOPw5DMU6sHFW6YAYblFC9Qyu/view | **Read in full, 2026-10-12** (downloaded whole: 3,809,860 B, 116 PDF pages = printed pp. 1–111 plus front matter; printed page = PDF page − 5; pages below are printed pages). Earlier passes had pp. 1–75. New: §4.6–4.12 (fatigue, wear, §4.8.3 bite angle and friction, roll repair, §4.10 design limits, acceptance) and Ch. 5. **§4.8.3 is qualitative.** Its bite-angle vs speed chart (Ill. 47) and campaign-friction chart (Ill. 48) are images, so no numbers can be extracted. The book has **no** rolling-force, torque or roll-flattening model. It is about roll steels and roll damage in (mostly steel) mills; little Al content. |
| SH | *Extrusion of Aluminium Alloys* (T. Sheppard, Springer/Kluwer, 1999) | https://drive.google.com/file/d/195YE0KUFE-yMliXyp304IqoaSdvnxKVU/view (duplicate "Extrusion Of Aluminium Alloys.pdf" 1pJoblJP3s9o7Z_WgFM9dhMmepLi7POET gives byte-identical extracted text) | OCR quality is poor: equations are partly garbled. Only pp. 1–~71 of ~400 returned: Ch. 1, Ch. 2 (continuum, pressure, friction, temperature, diffusion), and the start of Ch. 3. **Missing:** §3.3 homogenisation, §3.5–3.7 recovery/RX/quench sensitivity, Ch. 4 (Z–σ constants, subgrain size, limit diagrams), Ch. 5 (alloy-specific practice), Ch. 6 (6xxx, PCG, surface defects). **2026-10-12:** whole-file download failed for both copies (note below), so coverage is unchanged. |
| MFH | *Metal Forming Handbook* (Schuler, Springer 1998). File "3c-handbook-metal-forming.pdf" | https://drive.google.com/file/d/1n5Yidy74bZxj6ZifvCNtq0iRtk2nyh43/view ("vasevska.pdf" 1vbIfSVGbqJfheI2yJKigh5nZAdIK7KI4, 28.6 MB, gives **identical** extracted text, so it was read once) | Clean text, pp. 1–~60 of ~560: Ch. 2 basics and early Ch. 3 press design. Sheet-forming chapters (Ch. 4 deep drawing, bending, etc.) **not returned**. No Al-specific content. |
| POL | *Light Alloys*, 4th ed. (I.J. Polmear, 2006). File "115132137-Light-Alloys.pdf" | https://drive.google.com/file/d/1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w/view | Clean text, pp. 1–~189 (to §3.6.1). Used §2.1 (work hardening, FLC, texture, earing, annealing), §3.1 (casting, homogenisation, fabrication, heat treatment), §3.3, §3.4.3. §3.6.5 canstock **not returned**. |
| TOT | *Handbook of Aluminum Vol. 1: Physical Metallurgy and Processes* (Totten & MacKenzie eds., Dekker 2003). File "Alminium.pdf" | https://drive.google.com/file/d/1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz/view | OCR with substituted glyphs (ř = f, 3 = fi). PDF pp. 1–186 returned (Ch. 1–3; Ch. 3 = Tiryakioğlu & Staley). **Ch. 7 Rolling (p. 351), Ch. 8 Extrusion (p. 385) and Ch. 18 Sheet forming (p. 837) not returned.** Pages below are cited as PDF pages. |
| TRC | Krstić Vukelja, Duplančić, Lela, "Continuous roll casting of aluminium alloys – casting parameters analysis", *Metalurgija* 49 (2010) 115–118 | https://drive.google.com/file/d/16xRFXhETDI8_5cYr9x9tuBxUueKkY9q0/view | Read in full (4 pp.). Some printed units look wrong (flagged where used). |
| WIL | C.R. Williams, MSc thesis, Ohio Univ. 2012: *Effects of Sc and Zr additions on Al … post-braze grain structure, and extrusion* (AA3102 multi-port tube) | https://drive.google.com/file/d/1MYsjf2OwlDfrOtnb1zQas-DV9wfunqne/view | Read in full. Industrial MPE-tube extrusion data for AA3102. |
| MM | Alcoa Micromill™ presentation (J.F. Butler, 2015). File "document.pdf" | https://drive.google.com/file/d/1OYezPC_Eif_mKOTmq2xeExuqfcsTai1N/view | Read in full. Investor/marketing slides; treat the numbers as vendor claims. |
| INT-CRM | User spreadsheets "EN_AW_3207_CRM_Reduction_Table.xlsx" and "EN_AW_Master_CRM_Reduction_Tables.xlsx" | https://drive.google.com/file/d/1r-GFxL4bVuGG_ZGm_Lix-SQ3Upc7gROk/view · https://drive.google.com/file/d/1KN_kyx3RDw0QfLNvi1UHx7UYP5xwLjpq/view | Read in full. **Internal heuristics** (HRM/CRM gauge rules for cold-extrusion slugs). No literature backing is given. |
| INT-RX | User spreadsheet "AA3207_Recrystallization_Simulation.xlsx" (newest of 4 versions, 164 kB) | https://drive.google.com/file/d/1L9MDNPrCcWymlvgcowcv6Gf34eLJvwm2/view | Read in full. **Internal calibrated JMAK model.** Used here only for cross-checks. |

**Drive download limit test (2026-10-12).** Whole files were requested with the Drive connector's `download_file_content` tool (base64 output).

| File (bytes) | Result |
|---|---|
| [RR] 3,809,860 | OK (5,079,932-character base64 result, saved to disk and decoded; size matches Drive metadata) |
| S-043 EAA brochure 3,278,124 (ch06) | OK |
| [RA] 7,188,660 | Failed twice: *"The connection to MCP server "Google_Drive" was closed because a message from the server was too large or could not be parsed, so the result of tool "download_file_content" was not read."* |
| [SH] 10,463,104 (1pJoblJP3s9o7Z_WgFM9dhMmepLi7POET) | Failed with the same connection-closed message (the server accepted it, the client transport dropped it) |
| [SH] 10,512,541 (195YE0KUFE-yMliXyp304IqoaSdvnxKVU) | Refused by the server: *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API."* |

So there are two limits. The server enforces a hard 10 MB (10,485,760 B) cap. Below that, the client transport fails somewhere between 3.81 MB and 7.19 MB of file size (≈ 5.1–9.6 M base64 characters). **Practical rule: files ≤ ~3.8 MB can be fetched whole. Larger books must be split (e.g. per chapter) into ≤ ~3.8 MB PDFs on Drive first.**

Drive full-text searches run: `Zener-Hollomon`, `Zener`, `flow stress`, `hot rolling`, `extrusion`, `earing`, `forming limit`, `cold rolling`, `hyperbolic sine / subgrain size / peripheral coarse grain / extrudability`. Hits inside the `microstructure-sim-v2.14.0` tree (`models/*.js`, `*.jsx`, tests) were **not opened**, as instructed. Out of scope: the Nimonic 80A hot-deformation paper ("Microstructure_URN-NBN-SI-DOC-OFLHAUYU.pdf"; Ni superalloy, Z-methodology only). DC-casting, recrystallisation and Sc/Zr books (Eskin, Humphreys & Hatherly, Røyset) are assumed to be covered by companion KB files.

---

## 1. Conventions used in this file

- Thickness true strain in rolling: ε_t = ln(h₀/h₁). The tensile-test true strain ln(A₀/A_f) is the same quantity [POL §2.1.1 p.35–36]. Logarithmic principal strains sum to zero (volume constancy): φ₁+φ₂+φ₃ = 0 [MFH §2.2.2 p.27–28].
- The *principal* deformation φ_g is the one whose sign differs from the other two (= |largest|). It is the input for all force/work estimates [MFH §2.2.2 p.28].
- Von Mises equivalent strain for plane-strain rolling: ε̄ = (2/√3)·ε_t **(general knowledge)**. ⚠ [INT-CRM] and [INT-RX] both use ε_t (57.3 % → 0.85; 45 % → 0.598). This is consistent with each other but is 13 % below ε̄. Check which strain any constitutive or recrystallisation law was fitted with before mixing them.
- Flow stress (Tresca form): k_f = σ_max − σ_min [MFH §2.2.1 p.25]. Von Mises: k = σ̄/√3 [SH §2.1 p.26].
- Homologous temperature T_h = T / T(lowest-melting phase). Above 0.5 T_h aluminium recovers dynamically to a stable polygonised substructure [SH §1.2 p.6].
- Zener–Hollomon parameter: Z = ε̇·exp(ΔH/(G·T)), where ΔH is the activation energy for deformation and G the gas constant (Sheppard's notation) [SH §2.2 eq. 2.4 p.28].

---

## 2. Process routes and plant-level numbers

### 2.1 Mechanisms (what each step does to the microstructure)

- **Melt treatment.** Hydrogen solubility is 0.68 cm³/100 g in the liquid vs 0.036 in the solid at T_m (×19) [POL §3.1.1 p.97]. Solid solubility is ~5 % of the liquid value [RA §3 p.3-1]. Melt H must be < 0.15 cm³/100 g to avoid porosity [POL §3.1.1 p.98]. Inline degassers (SNIF, ALPUR, LARS) use Ar with up to ~3 % Cl₂ [RA §3 p.3-2]; furnace fluxing uses < 10 % Cl₂ [RA §3 p.3-1]. Ceramic foam filters have 20–70 ppi (8–30 per cm); deep-bed filters are 125–380 mm of 6–19 mm alumina media [RA §3 p.3-2].
- **Grain refining.** 5Ti-0.3B or 5Ti-0.15C rod (Ø 10 mm), addition < 0.01 wt %, fed at the last minute because the refiner fades/agglomerates if held [RA §3 p.3-3]. Al-5Ti-1B is now the favoured composition [POL §3.1.3 p.103]. Zr poisons TiB₂ [POL p.104].
- **DC casting.**
  - Holding hearth 700–730 °C; the metal loses 22–28 °C on the way to the pit [RA §3 p.3-5].
  - Mould depth ~150 mm; casting speed 40–100 mm/min; the shell leaves the mould at 300–500 °C [RA §3 p.3-6].
  - Ingots up to ~760 mm thick, 2300 mm wide, 9 m long (~27 t) [RA p.3-6]. Polmear gives ≤ 650 mm sections, ≤ 15 t, cooling 1–5 °C/s [POL §3.1.1 p.99].
  - The shrinkage gap causes a solute-enriched surface zone, which is removed by **scalping** [RA p.3-6]. Surface inverse segregation can cause edge cracking in rolling [POL p.100].
  - EMC (electromagnetic casting) avoids the enrichment zone; 3xxx/5xxx beverage stock has been rolled without scalping [RA p.3-7; POL p.100].
- **Preheat/homogenisation.** Five purposes [RA §3 p.3-8]: (1) put the metal above the recrystallisation temperature so it does not strain-harden; (2) homogenise coring; (3) spheroidise insoluble constituents (better formability); (4) soften; (5) relieve stresses.
  - Example practice: either straight to ~455 °C and held, or overshoot, hold, then fan-cool to rolling temperature [RA p.3-8].
  - Homogenisation window 450–600 °C, typically 6–24 h [POL §3.1.4 p.104–105].
- **Hot rolling.** Welds casting pores. Breaks up and redistributes Fe/Si constituents, turning the brittle cast structure into ductile wrought metal [RA §4 p.4-6/4-7; POL §3.1.5 p.107]. Grains elongate; recovery and partial recrystallisation occur pass-to-pass depending on alloy, temperature and pass reduction [POL p.107]. Most products recover dynamically. Static recrystallisation can happen between or after passes. High-Mg alloys (lower SFE) can recrystallise **dynamically** [TOT Ch.3 PDF p.142].
- **Cold rolling** adds dislocations (H-tempers). It has a natural strength limit; a fully cold-worked sheet breaks on small further strain [RA §4 p.4-7].
- **Annealing.** "Recrystallisation temperature" is a range that depends on alloy, prior strain and soak time [RA §5 p.5-6]. Recrystallisation of hard-rolled pure Al takes several hours at 280 °C, a few minutes at 380 °C, and seconds at 500 °C [POL §2.1.6 p.42].

### 2.2 DC-ingot → coil → sheet/foil route: quantitative parameters

| Step | Parameter | Value | Ref |
|---|---|---|---|
| Preheat | Rolling-entry example | ~455 °C (850 °F) | [RA p.3-8] |
| Preheat | Upper limit for hot rolling | 10–50 °C below solidus, to avoid grain-boundary weakening/cracking | [RA p.4-6/4-7] |
| Breakdown (reversing 4-high) | Ingot thickness in → slab out | 200–600 mm → 15–35 mm | [POL §3.1.5 p.107] |
| | | ~760 mm max → 100–125 mm "slab" | [RA §5 p.5-1, 5-3] |
| | Pass example | 380 → 330 → 280 mm, i.e. r = 13 %, ε_t = 0.14 per pass **(derived)** | [RA p.5-3] |
| | First-pass gap | 50–75 mm less than ingot thickness | [RA p.5-1] |
| | Drive power / force | 3730 kW per work roll (7460 kW total); ~3635 t separating force | [RA p.5-1] |
| | Mill size naming | by roll-barrel length, e.g. 3 m and 4.25 m mills | [RA p.5-1] |
| | Coolant | water + ~5 % oil emulsion, filtered and recirculated; off at bite, on during the pass | [RA p.5-2] |
| | Edge control | vertical edger rolls (edge cracking, width spread); cross-rolling to gain width | [RA p.5-3] |
| Intermediate hot / reversing coiler mill | Gauge | to ~25 mm (intermediate) or coiled at < 12 mm on a single-stand reversing hot mill with 1–2 coilers, 1–3 wraps | [RA p.5-3, 5-4] |
| Tandem hot mill | Exit gauge | 2.5–8 mm, then coiled | [POL p.107] |
| | Sheet for < 1 mm final gauge | hot rolled to 3–6 mm first | [RA §5 p.5-7] |
| | Speed | up to ~600 m/min | [RA §4 p.4-6] |
| | Inter-stand control | speed trimmed for tension (fast); gap (slow) | [RA p.5-4/5-5] |
| Hot coil | Dimensions | ID 500–600 mm; OD > 2285 mm (up to 2.4 m) | [RA p.5-4] |
| Cold rolling | First pass | ~50 % reduction; later passes similar or smaller | [RA p.5-7] |
| | Can-body stock | 2.5 → 0.25 mm in 4–5 single-stand passes, or 1 pass on a tandem. ε_t = 2.30, ε̄ = 2.66; ≈37–44 %/pass **(derived)** | [RA §5 p.5-8] |
| | Speed | 1525–1830 m/min single stand; up to 2135 m/min (fastest mills) | [RA p.5-7; p.4-6] |
| | Strip heating | to ~80 °C or more, removed by coolant | [RA p.5-7] |
| | Lubricant | light petroleum distillate + load-bearing additive. Low viscosity removes heat better; the lower limit is set by evaporation/flash point. Emulsions used at high speed | [RA p.5-8] |
| | Bright surface | small final-pass reductions, polished rolls | [RA p.5-7] |
| | Minimum gauge | alloys ~0.05 mm; pure Al foil 0.0025 mm | [RA p.5-7] |
| Annealing (NHT alloys) | Full anneal (O) | 335–405 °C, 0.5–2 h (usually ~1 h), controlled cooling | [RA §5 p.5-6] |
| | Literature windows | 345–415 °C, minutes to 3 h [POL p.107]; 350–420 °C [POL p.109]; 300–420 °C [POL p.42] | |
| Annealing (HT alloys) | Remove cold work / remove heat-treat effects | ~2 h at 335–370 °C / 400–425 °C, slow controlled cool | [RA p.5-6] |
| Stabilisation (5xxx, 3004) | H3x | ~180 °C (350 °F) [RA p.5-6]; **vs** 120–150 °C [POL §3.3.3 p.130]. ⚠ The two sources differ. | |
| Furnace type | Batch coil vs continuous strip | Batch is most common. Continuous strip heats fast and gives a finer grain | [RA p.5-7] |
| Plate | Cold reduction for strength | up to ~30 % (armour, boat) | [RA §7 p.7-1] |
| | Stretch | 1–3 % typical; ≤ 15 % for 2024/2219 T86/T87 | [RA §7 p.7-2] |
| | Reheat (slab) | 2–24 h depending on alloy | [RA p.7-1] |
| Gauge/profile | Mill accuracy | roll Ø tolerance 0.006 mm; stack eccentricity ≤ 0.01 mm | [RA §4 p.4-6] |
| | Typical tolerance | 5052, 0.75 mm, ≤ 1000 mm wide: ±0.045 mm; 1000–1500 mm wide: ±0.06 mm (ANSI H35.2) | [RA §8 p.8-1/8-2] |

**Product definitions** [RA §1 p.1-4]:
- plate > 6 mm (US ≥ 6.3 mm);
- sheet > 0.20 to ≤ 6 mm;
- foil ≤ 0.20 mm.
- By these definitions, 0.115 mm air-conditioner fin stock falls in the foil range [RA §1 p.1-4; self-test 1.11].
- Household foil is ~0.0165 mm [RA p.1-2].

### 2.3 Continuous-casting routes

| Route | Thickness | Cooling rate | Speed / productivity | Ref |
|---|---|---|---|---|
| Twin-roll caster (TRC) | < 25 mm as-cast; typically 4–12 mm; ~3–10 mm in [POL] | 55–555 °C/s [RA]; 10²–10³ °C/s [POL] | 2–3 m/min; 10–18 kg h⁻¹ cm⁻¹ width; width 760–2030 mm | [RA §3 p.3-3/3-4; POL p.102; TRC p.115] |
| Belt (Hazelett) | 12–25 mm [RA]; 12–75 mm, ≤ 2.3 m wide [POL] | 19 mm slab: 11–40 °C/s at surface, 4 °C/s at centre | 21–24.5 t m⁻¹ h⁻¹ | [RA p.3-4; POL §3.1.2 p.101–102] |
| Block caster | slab (plate gauges) | 0.5–5 °C/s; exits ~540 °C (little reheat needed) | ~6 m/min; 180–225 kg h⁻¹ cm⁻¹ | [RA p.3-4] |
| DC (reference) | 400–760 mm | 1–5 °C/s | 40–100 mm/min | [RA p.3-6; POL p.99] |

- Share: ~20 % of North-American sheet and plate is continuously cast [RA p.3-3].
- **Metallurgical differences vs DC** [RA p.3-3]:
  1. much less hot work;
  2. no homogenisation;
  3. no scalping;
  4. faster solidification → higher supersaturation and less segregation ("partly pre-homogenised").
- Dendrite cell size is 30–70 µm in DC vs 5–10 µm in TRC [POL p.102]. Transition-metal (Fe, Mn) supersaturation is retained, so properties differ from DC even at equal composition; sometimes a different or leaner alloy is used [POL p.102].
- Making CC sheet as formable as DC "may significantly reduce the advantages" of CC [RA p.3-3]. Markets include **foil and fin stock** [RA p.3-3].
- **TRC industrial window (AA1235 / AA8011 foil feedstock; Pechiney caster, TLM Šibenik)** [TRC p.115–117]:
  - Ø690 mm rolls, 1740 mm face; tip set-back 35–55 mm.
  - Melt 685 ± 5 °C; roll gap 5.2 mm; contact length ("angle") ~47–50 mm.
  - Strip 6.3–6.5 mm × 1020–1520 mm.
  - Graphite lubricant 2 L per 75 L water; Al-Ti-B wire at 28–35 cm/min.
  - Quality targets: longitudinal gauge < ±2 % per coil, < ±1 % per roll revolution, crown 0–1 %, wedge ≤ 1 %.
  - Trends: narrower strip raises roll force and contact length; thinner strip raises force and contact length.
  - Recommendations: cast close to the liquidus, keep a high melt level, use a lower casting speed, control the nozzle geometry.
  - ⚠ Printed units "0.95–1.50 cm/min" and "5·10³ kN/mm" are implausible. They are probably m/min and kN/m.
- **Micromill (Alcoa) claims** [MM slides 8, 11, 12]:
  - "20-day rolling process to 20 minutes", 50 % less energy, ¼ of the footprint.
  - 6xxx: FLD₀ 26–28 vs 23.6 for DC; LDR 2.08–2.13 vs 1.88–1.98 for DC 6022.
  - "MMHF-T4" 1.5 mm: TYS 152 MPa, UTS 282 MPa, uniform elongation 25.8 %, FLD₀ 33.7, LDR 2.13–2.18 vs 5182-O (124 / 275 / 21.2 %, FLD₀ 23.4).
  - This is a vendor presentation. The route shows that fast solidification plus in-line rolling can *beat* DC formability. It contradicts the [RA] caution, so it is unproven for 3xxx.

### 2.4 Design levers (process route)

1. **CC vs DC for 3xxx fin/foil** (inference from [RA p.3-3; POL p.102]). CC retains Mn/Fe in supersaturation and skips homogenisation. So the Mn-dispersoid population, and with it the recrystallisation temperature, sag resistance and post-braze grain size, is decided **at the first anneal**, not at preheat. Re-tune the Mn/Fe/Si balance and the anneal heating rate for CC; do not copy DC practice.
2. **Hot-band gauge sets the cold strain budget.** [RA p.5-7] gives 3–6 mm hot band for < 1 mm sheet. [INT-CRM] picks the HRM exit gauge so that the CRM ε_t is ≥ 0.85 (3207), ≥ 0.80 (3102), ≥ 0.95 (3003/1070), before the final anneal (internal heuristic).
3. **Preheat practice is an alloy-design variable.** Slow heating (≈ 75 °C/h) is needed to nucleate a fine, uniform dispersoid population (Al₆Mn, Al₁₂Mg₂Cr, Al₃Zr) [POL §3.1.4 p.106]. In the cited Al-Zn-Mg-0.3Mn case, 50 °C/h gave Al₆Mn nucleated on MgZn₂, and 500 °C/h did not [POL Fig. 3.8 p.106]. Al₆(Fe,Mn) → α-Al₁₂(Fe,Mn)₃Si conversion during homogenisation is key for canstock [POL p.107].
4. **Rule of thumb for homogenisation time:** +50 °C → ~⅓ of the time [POL p.105]. This implies an apparent Q ≈ 116 kJ/mol at 500→550 °C **(derived)**, which matches the Mg/Si/Cu entries of [SH Table 2.3] (117–126 kJ/mol) but not slow-diffusing Mn (§3.5).

### 2.5 Pitfalls / defects (route)

- Enrichment zone and surface ripples not scalped → slivers rolled in, edge cracks [RA p.3-6/3-7; POL p.100].
- Hot-roll pick-up ("roll coating"): a little helps bite; too much prints or flakes onto the product [RA §4 p.4-3].
- Lubricant too low → sticking; too high → poor bite and dull surface. Reduction marks and "herringbone" appear on the tandem hot mill [RA p.5-2, 5-5].
- **Negative crown** (thick edges) occurs in dilute, soft alloys (1xxx, 3102-type), which spoils flatness in cold rolling. Profile must be built while the strip is hot and thick; final flatness is set by the last (cold) stand [RA §5 p.5-8].
- **Age-softening** of strain-hardened 5xxx and 3004 (Mg leaving solution) → H3x stabilisation [RA p.5-6; POL p.130].
- Fire-cracking of work rolls is *more* likely when hot rolling Al than steel. Al conducts heat well and its oxide layer is thin, so the roll surface runs hotter despite the lower strip temperature [RR §4.5.3 p.75]. Fire-cracks are thermal-shock cracks: the hot roll surface is quenched by the coolant in a fraction of a second and cracks once the surface tensile stress reaches the shell strength. The pattern forms in the first roll revolutions. The worst cracking follows mill stops with a slab or strip in the gap [RR p.75].
  - Remedy after a stop, roughing stand: stop the coolant, open the gap, push the slab out and let the roll cool slowly.
  - Remedy after a stop, finishing stand: keep the gap closed and the coolant on until the strip is black, then shut down [RR p.76].
- Friction is governed by the roll *surface* (fire-crack pattern, roughness), not by the roll-grade friction coefficient [RR §3.6 p.51–52] (page cite corrected after full-text pass; was p.50–51).

---

## 3. Hot-deformation constitutive behaviour

### 3.1 Mechanisms

- High SFE (~170 mJ m⁻² [POL §2.1.2 p.36]) → dynamic recovery dominates. Above 0.5 T_h a stable polygonised substructure forms; **subgrains stay equiaxed while grains elongate and do not recrystallise during working** [SH §1.2 p.6].
- Dispersoid-formers (Cr, Mn, Zr) precipitate during homogenisation. They are strung out in the working direction and delay or stop static recrystallisation, which keeps "fibrous" grains [SH §1.2 p.6; TOT Ch.3 PDF p.142].
- At steady state the state variables are constant (dSᵢ/dt = 0), so σ = f(ε̇, T). This is valid for bulk extrusion. It is *not* valid for incremental FE at deformation-zone entry, where elements are not yet at steady state [SH §2.2 eq. 2.3 p.28].
- PSN nucleus size falls as deformation temperature falls and strain rate rises [TOT Ch.3 PDF p.142].
- Hot-worked substructure strengthens via σ = σ₀ + k₁d⁻ᵐ:
  - m = 1 for cells (~1° misorientation, low-temperature working);
  - m → 0.5 for subgrains (recovered).
  - Subgrains from hot working strengthen more effectively [POL §2.1.2 p.36–37; TOT Ch.3 PDF p.114].

### 3.2 Equations available from the sources

| # | Equation | Notes | Ref |
|---|---|---|---|
| H1 | Z = ε̇·exp(ΔH/(G·T)) | ΔH = activation energy for deformation, G = gas constant | [SH §2.2 eq. 2.4 p.28] |
| H2 | σ̄ = f(Z) "as modified by Sheppard [Sheppard & Wright 1979]", with material constants α, n (and A) | The body of eq. 2.4 is illegible in the OCR. Standard Sheppard–Wright form: σ̄ = (1/α)·sinh⁻¹[(Z/A)^{1/n}] = (1/α)·ln{(Z/A)^{1/n} + [(Z/A)^{2/n}+1]^{1/2}}, equivalent to ε̇ = A[sinh(ασ)]ⁿ exp(−Q/RT) **(general knowledge)** | [SH p.28] |
| H3 | Mean extrusion strain rate (Feltham): ε̇ = 6·V_R·D_B²·tanθ·ln R / (D_B³ − D_E³) | Classic form **(general knowledge)**. [SH] confirms the variables (D_B, D_E, V_R, R = D_B²/D_E²) | [SH p.28] |
| H4 | Modified Feltham from minimised upper bound: ε̇ = 6·V_R·D_B²·(0.171 + 1.86 ln R)·tan(38.7 + 6.9 ln R) / (D_B³ − D_E³) | OCR-reconstructed (angle in degrees). Used by Sheppard to compute Z | [SH §2.3.2 p.36–37] |
| H5 | FEM mean ε̇ vs ln R is **parabolic**, not linear as in Feltham; agreement worsens at high R (no spin correction) | | [SH §2.3.4 p.44, Fig. 2.8] |
| H6 | Breakthrough (peak) pressure increment Δp = 6.62 + 0.921·ln(Z/A) | OCR shows extra symbols ("an"); may contain α, n. Verify against Castle & Sheppard 1976 [SH ref 37] | [SH §2.5.4 eq. 2.27 p.57] |
| H7 | Diffusion: D = D₀·exp(−Q/RT); x ≈ √(Dt) | | [SH §2.6.2 eq. 2.39 p.65; POL §3.1.4 p.105] |
| H8 | Homogenisation relaxation: c(x,t) = c₀ + c_m·cos(πx/l)·exp(−t/τ), τ = l²/(π²D). Halving l cuts time by 4; l/4 cuts it by 16 | | [SH §2.6.2 eq. 2.40–2.42 p.65–66] |

### 3.3 Per-alloy constitutive constants — **status: NOT AVAILABLE in the accessible text**

| Alloy | α (MPa⁻¹) | n | Q (kJ/mol) | A (s⁻¹) or ln A | Source status |
|---|---|---|---|---|---|
| 1xxx (1100/1050) | — | — | — | — | In [SH Ch.4 Table, pp.127 ff.] and probably [TOT Ch.7/8]. Not returned |
| 3003 / 3102 / 3207 | — | — | — | — | Same. Back-calculated σ̄ point for 3102 in §3.4 |
| 5xxx (5052/5083) | — | — | — | — | Same |
| 6xxx (6060/6063/6082) | — | — | — | — | Same (SH Ch.6) |
| 7xxx (7075) | — | — | — | — | [SH §2.5.4] uses 7075 at R = 30, 3 mm/s, 300–425 °C but gives no constants in the pages read |

- **Only anchor (general knowledge):** for dilute Al alloys the apparent Q for hot working is usually close to the activation energy for Al self-diffusion, ≈ 142 kJ/mol.
- Do **not** populate the table from memory. Retrieve [SH Ch.4] / [TOT Ch.7–8] (§11, G1).
- 2026-10-12: a whole-file download of [SH] was tried and failed for both copies (§0 note), so the table is still empty. A chapter-split PDF of ≤ ~3.8 MB is needed.

### 3.4 Calibration point extracted here: AA3102 multi-port tube (derived from [WIL] + [SH])

Inputs [WIL Table 3 p.19, Table 5 p.38]:
- container 106 mm; billet Ø102 × 203 mm; R = 817;
- billet 495–503 °C; tooling 450 °C;
- ram 0.7 mm/s; exit ~34 m/min; water quench;
- peak specific pressure 445.0 MPa and 460.2 MPa (two 3102 billets); 650.7 and 653.3 MPa (Al-0.19Sc-0.05Zr).

**(derived)** Using [SH eq. 2.26 / p.36] p = σ̄(0.171 + 1.86 ln R + 4mL_B/(D_B√3)) with m = 0.88 [SH §2.4]:
- ln R = 6.706; the bracket is 12.64 + 3.89 = 16.54.
- σ̄(3102, ~500 °C) ≈ **27–28 MPa**; σ̄(AlScZr) ≈ **39.4 MPa** (+44 %, as measured).
- Without the friction term, σ̄ would be 35–36 MPa.
- Caveats:
  - porthole/bridge-die pressure includes die-land and port losses, so this σ̄ is an upper estimate;
  - eq. 2.26 is OCR-reconstructed.
- Strain-rate estimates **(derived)** differ by 20× between models, so report Z only with the model named:
  - H4: ε̇ ≈ 5.7 s⁻¹, but its die angle extrapolates to 85° at R = 817, outside its range;
  - H3 with θ = 45°: ε̇ ≈ 0.27 s⁻¹.

### 3.5 Diffusivities for homogenisation / preheat kinetics

| Element in Al | D₀ (m²/s) | Q (kJ/mol) | D at 475 °C (m²/s) [SH] | D at 500 °C [POL] (converted to m²/s) |
|---|---|---|---|---|
| Cu | 0.29×10⁻⁴ | 125.6 | 4.9×10⁻¹⁴ | 5×10⁻¹⁴ |
| Zn | 0.11×10⁻⁴ | 83.7 | 1.6×10⁻¹¹ | — |
| Mg | 0.11×10⁻³ | 117.2 | 7.2×10⁻¹³ | 1×10⁻¹³ |
| Si | 0.90×10⁻⁴ | 125.6 | 1.5×10⁻¹³ | 1×10⁻¹³ |
| **Mn** | 0.22×10⁻⁴ | 121.4 | 7.3×10⁻¹⁴ | **5×10⁻¹⁷** |
| Cr | 3.00×10⁻¹¹ (as printed) | 62.8 | 1.2×10⁻¹⁵ | — |
| Zr | 7.28×10⁻² | 240.8 | 1.1×10⁻¹⁸ | — |
| Fe | 0.41×10⁻¹⁴ (as printed) | 58.6 | 3.3×10⁻¹⁹ | — |

Sources: [SH Table 2.3 p.65] (the D values recompute correctly from D₀ and Q — **derived** check) and [POL §3.1.4 p.105] (5×10⁻¹³ cm²/s etc.).

⚠ **Mn discrepancy of ~10³×.** Sheppard's Mn entry (Q = 121.4 kJ/mol) gives fast, Mg-like diffusion. Polmear's 500 °C value is ~10³ slower, which matches Mn being a *slow* diffuser (general knowledge). Sheppard's Cr and Fe rows (low D₀ and low Q) also look non-physical. **For 3xxx dispersoid and homogenisation models, use the Polmear-scale Mn diffusivity. Do not use [SH Table 2.3] for Mn, Cr or Fe.**

### 3.6 Design levers (hot deformation)

- To raise recrystallisation resistance in hot-worked product, use small, closely spaced dispersoids, ideally **coherent**:
  - Al₃Zr is more effective than incoherent Al₁₂Mg₂Cr / Al₂₀Mn₃Cu₂ [TOT Ch.3 PDF p.137];
  - useful dispersoid size is < 0.4 µm [TOT p.137] (0.05–0.5 µm [POL p.43]);
  - Zr < 0.18 wt % gives near-spherical Al₃Zr [TOT p.137].
- Sc+Zr (Al-0.19Sc-0.05Zr) keeps the extruded tube **unrecrystallised** at 500 °C extrusion (3102 recrystallises fully during extrusion). It resists recrystallisation up to 575 °C and partially recrystallises at 600 °C / 2 min braze. Cost: **+44 % extrusion pressure** [WIL §5.1–5.2 p.38–41].
- Higher flow stress (more solute) raises press load and deformation heating (ΔT ∝ σ̄·ln R/(ρc_p), §8.2). The extrudability window therefore narrows from both the load side and the temperature side (inference from [SH §2.5.2; WIL]).

### 3.7 Pitfalls

- Mixing ε_t and ε̄, or Feltham and FEM strain rates, when transferring Z-based laws between rolling and extrusion (§1, H5).
- Constant-stress FEM with m-friction cannot tell m = 0.2 from m = 1.0 at R = 20, because hydrostatic stress dominates. Use σ_interface = m·σ₀ in a boundary layer instead [SH §2.3.4 eq. 2.18–2.19 p.41].

---

## 4. Hot rolling: mechanics and microstructure

### 4.1 Mechanisms

- Roll bite is by friction. Rougher rolls allow larger reductions per pass; smooth (bright) rolls may need less coolant, which shifts the thermal schedule [RA §4 p.4-2].
- Rolling generates heat from friction and from internal deformation. Coolant both lubricates and removes heat, controlling roll camber and temper [RA §5 p.5-1/5-2].
- Spread is small in normal lengthwise rolling (friction restrains it) [RA p.5-3]. Tandem stands must accelerate in proportion to the thickness ratio (volume constancy: 30 → 5 mm runs 6× faster) [RA p.5-3/5-4].
- Texture, grain shape and surface are temperature-dependent:
  - lower hot-rolling temperature → brighter surface, elongated grains;
  - higher temperature → recrystallisation [RA §4 p.4-6/4-7].
  - Through-thickness strain in plate is uneven (surface > centre). Larger pass reductions or pre-forging improve uniformity [POL §3.1.5 p.107].
- Reheat cycles for alloys with recrystallisation-inhibiting elements must avoid **coarse grains in critically strained regions** [POL p.107].

### 4.2 Equations (for pass-schedule models)

- Direct-force forming (upsetting, rolling): F = A·k_w, with forming efficiency η_F = k_f / k_w [MFH §2.2.3 p.29].
- Specific work: w_id = ∫k_f dφ ≈ k_fm·φ_g; W = V·w_id/η_F [MFH §2.2.3 p.29–30].

**Roll-gap friction and bite [RR, read in full 2026-10-12].**
- Inside the gap there is backward and forward slip, with static friction at the neutral point between them. If the speed is too high, flow goes in one direction only, static friction is lost, and the roll slips and then chatters (alternating bite and no-bite) [RR §3.6 p.51].
- Hot rolling with little strip tension needs "high" friction. The permissible bite angle falls as rolling speed rises. Slip is typical with freshly ground rolls after a roll change. Mills therefore roll special schedules for the first slabs to build up a fire-crack pattern. If the schedule asks for too large a bite at the desired speed, reduce the speed or roughen the roll surface (open fire-crack pattern, "ragging") [RR §4.5.3 p.74; §4.8.3 p.92].
- The bite-angle vs speed curve was measured on hot strip mills (steel) with freshly ground rolls. It is an image (Ill. 47), so no values can be extracted [RR p.92].
- Mill friction coefficients are back-calculated from measured vs calculated separating force [RR §3.6 p.51]. They are **much higher than laboratory values**, differ between roll grades, change from slab to slab and **rise during a campaign** (Ill. 48) [RR §4.8.3 p.93]. Laboratory tests (ring compression, CRM Liège) found no significant friction difference between roll grades [RR p.51–52]. So the surface (fire-cracks, oxide) matters more than the roll material [RR p.93].
- **Consequence for pass-schedule models (inference):** a single μ fitted at roll change will drift. Calibrate μ online from measured roll force, as mills do [RR p.51], rather than taking a handbook value.

**Roll elastic data and mill design limits [RR].** These are inputs or checks for any roll-force or roll-flattening model:

| Quantity | Value | Ref |
|---|---|---|
| E, ferritic/bainitic/martensitic steel rolls | 210 000 N/mm² ± 3 % (insensitive to alloying and heat treatment) | [RR §3.2.1 p.18] |
| E, austenitic steel | 180 000 N/mm² ± 3 % | [RR p.18] |
| E, nodular (ductile) iron | 175 000 N/mm² ± 5 % | [RR p.18] |
| E, grey (lamellar) iron | no single value: it "behaves totally differently" (non-linear elasticity, see RR §3.2.3) | [RR p.18] |
| Poisson ratio | 0.3 elastic; 0.5 fully plastic | [RR p.18; §3.7 p.53] |
| Compound (double-poured) rolls | Effective E combines shell and core and changes as the shell is ground away | [RR §3.7 p.53] |
| Safe nominal bending stress (fillet notch factor 1.8 ≤ α_K ≤ 2.2) | grey iron < 60; nodular iron < 90; cast steel < 120; forged steel < 150 N/mm² | [RR §4.10.1 p.100] |
| Static torque strength | 90 % of tensile strength (torque fatigue failures are rare) | [RR §4.5.2 p.74; §4.10.1.1 p.100] |
| Linear load, hot strip vs work roll | traditionally < 1500 t/m of strip width (≈ 14.7 kN/mm, **derived**). Above this, use only work rolls with nodular-iron cores | [RR §4.10.1.2 p.100] |
| Hertzian pressure, work roll vs back-up roll | safe limit 2100 N/mm². Peaks occur near the barrel edges (back-up roll bending), so a back-up roll chamfer is required | [RR §4.10.2.1 p.101] |
| Roll accuracy | roll TIR must be one grade better than the product tolerance; ≤ 0.003 mm is acceptable for tin-plate rolls | [RR §4.11 p.102–103] |

These limits come from steel hot strip and plate mills. For Al they are upper-bound sanity checks, not design values (inference).

The textbook rolling-force set below is **not in the accessible sources (general knowledge)**. The full-text pass confirmed that [RR] contains no Orowan, Sims, Ekelund or Hitchcock model. Use the set only for first estimates until [TOT Ch.7] is retrieved. For E_roll, take the [RR] values above:
- Projected contact length: L = √(R·Δh). Bite condition: μ ≥ tan α_bite (α_bite = roll angle of contact).
- Ekelund hot-rolling mean pressure: p̄ = (2/√3)·σ̄·[1 + (1.6·μ·√(RΔh) − 1.2Δh)/(h₀ + h₁)]. Roll force F = p̄·w·L.
- Ekelund mean strain rate: ε̄̇ ≈ 2·v_R·√(Δh/R)/(h₀ + h₁).
- Hitchcock roll flattening: R′ = R·[1 + 16(1 − ν²)·F′/(π·E_roll·Δh)], F′ = force per unit width. Iterate with L′ = √(R′Δh).

### 4.3 Recrystallisation after hot rolling

- Static recrystallisation between or after passes is typical. Alloys with dispersoids retain dynamically recovered subgrains inside elongated grains [TOT Ch.3 PDF p.142].
- Nucleation sites for subsequent recrystallisation [POL §2.1.6 p.42, Fig. 2.4]:
  1. transition bands (cube nuclei);
  2. coarse particles (PSN, > ~1 µm);
  3. old grain boundaries;
  4. shear bands.
  - The final texture is the result of the (1) vs (2) competition.
- Cube nucleation at transition bands is known after cold rolling and "seems likely" after warm/hot rolling as well [POL p.42]. This is the root of hot-band cube texture, which balances earing in can stock (§7).
- **Self-annealing in the hot coil, hot-band exit temperatures, and coil cooling rates are not given in any accessible source** (gap G3).

### 4.4 Design levers (hot rolling)

- (inference from [POL p.42; TOT p.142–143]) For **can stock and deep-drawn fin collars**, aim for a hot band with substantial cube (from recrystallisation at transition bands) and limited PSN-random texture. That means controlled coarse-particle fraction (Fe, Si, Mn) and enough finishing temperature to recrystallise in the coil.
- For **long-life fin/tube stock (sag resistance, large post-braze grains)** the opposite applies. Keep Mn in solution or as fine dispersoids through hot rolling, so recrystallisation is pushed to the final anneal or brazing cycle (see §6, §8.5).
- Build profile and crown in the hot mill (thick, hot strip). Dilute soft alloys tend towards negative crown [RA p.5-8].

### 4.5 Pitfalls

- Too high a temperature → grain-boundary weakening and cracking [RA p.4-6/4-7].
- Edge cracking in plate. Edges are trimmed after intermediate rolling so cracks do not run in [RA §7 p.7-1].
- Wedge (side-to-side thickness difference) comes from non-parallel rolls or uneven temperature across the gap [RA p.5-8].
- Herringbone and reduction marks come from lubricant problems [RA p.5-5].
- **Al hot-mill roll problems** [RR, full text]:
  - The coolant in Al hot mills contains aggressive chemical (cleaning) additives. These affect roll wear [RR §4.8.1 p.88] and cause **corrosion fatigue at back-up-roll neck fillets**. Corrosion fatigue has no fatigue limit [RR §4.6.1.2 p.80; §4.9.4.1 p.98].
  - Back-up rolls in Al hot mills see almost no wear, so they run much longer campaigns than in steel mills. The fillet must be sealed against coolant. Fillet repair by welding or re-machining is forbidden; cracked rolls can run under fracture-mechanics crack-growth monitoring [RR p.79–80, 98].
  - Broken brush wires in Al hot mills can enter between work and back-up rolls and cause local overload [RR §4.5.4 p.76].

---

## 5. Cold rolling and work hardening

### 5.1 Mechanisms

- Work hardening comes from dislocation multiplication, tangles, cells and subgrain walls. The grain-boundary area grows [POL §2.1 p.32].
- Shear bands (~35° to the rolling plane) form at true strain ≳ 1. At very high strains they can cross the whole thickness and become failure paths [POL p.32–33].
- Coarse particles cause local deformation zones, which are PSN sites [POL p.33–34, Fig. 2.5].
- Solute effects [POL p.34; TOT Ch.3 PDF p.111–112]:
  - Cu is most effective per atom at suppressing dynamic recovery and raising dislocation storage, then Mg ≈ Si; Zn has a negligible effect.
  - Mg has the greatest *practical* value because of its high solubility.
  - In ternary systems (Al-Mg-Si, Al-Zn-Mg, Al-Cu-Mg) hardening is more than additive.
- Work hardening has an alloy-specific limit; strength and ductility trade off [RA §4 p.4-7]. Cold-worked 3003 draws *better* than annealed 3003, which matters for cans [POL p.35].

### 5.2 Quantitative laws and parameters

Hollomon law σ = K·εⁿ [POL §2.1.1 p.35–36; TOT Ch.3 PDF p.110–112]:
- For pre-strained tempers: σ = K(ε₀ + ε)ⁿ, where ε₀ is the prior cold work or the "equivalent cold work" of a hot-worked temper [POL p.36].
- Rolling form (Alcoa): **YS = σ₁·εⁿ**, ε = ln(t_i/t_f). σ₁ = YS at true rolling strain 1 (63 % reduction) [TOT PDF p.111].

**Table 5-1 — Hollomon parameters, O-temper** [TOT Ch.3 Table 3, PDF p.112]

| Alloy | n | K (MPa) |
|---|---|---|
| 1100-O | 0.242 | 146 |
| 3003-O | 0.242 | 188 |
| 6061-O | 0.209 | 224 |
| 5052-O | 0.198 | 281 |
| 5454-O | 0.189 | 340 |
| 5086-O | 0.193 | 368 |
| 5456-O | 0.178 | 479 |

Trend: n falls from 0.25 to 0.17 as K rises from 175 to 450 MPa [POL p.36]. Note 3003 has the same n as 1100 but a 29 % higher K.

**Table 5-2 — Solute work-hardening parameters** [TOT Ch.3 Table 2, PDF p.111]

| Solute | K (Cu-equivalent per at %) | Doherty H (GPa) |
|---|---|---|
| Cu | 1.00 | 3.38 ± 0.20 |
| Ge | 0.64 | — |
| Si | — | 1.56 ± 0.05 |
| Mg | 0.37 | 1.52 ± 0.14 |
| Mn | — | 1.03 ± 0.17 |
| Cd | 0.33 | — |
| Ag | 0.15 | — |
| Zn | 0.071 | 0.27 (column assignment uncertain in OCR) |

- K example: 1 at % Mg behaves like 0.37 at % Cu.
- H normalises the gain in σ₁ by the solute atomic fraction. The exact exponent is garbled in the OCR; check before use.

Other work-hardening facts:
- Cryogenic working: 1100 rolled at −196 °C gains up to ~40 % strength but loses ductility [POL p.36].
- Strength gain examples [RA §2 p.2-6]:
  - 3003: UTS 110 → 200 MPa (O → H18);
  - 3004: UTS 180 → 280 MPa (O → H38);
  - NHT alloys span YS 20–500 MPa from O to H19 [POL §3.3 p.128].
- Annealed baselines [POL §3.3 p.129–130]:
  - SP Al proof stress 7–11 MPa;
  - 1100 UTS 90 MPa; 3003 UTS 110 MPa; 3004 UTS 180 MPa;
  - 5005: YS 40 / UTS 125 MPa; 5456: YS 160 / UTS 310 MPa;
  - 8xxx dispersion hardening 30–40 MPa, plus solid solution 2–10 MPa (YS) and 5–20 MPa (UTS) [POL p.131].

### 5.3 Friction, lubrication, rolls

- Friction is set by the roll surface (roughness, fire-crack network), which changes over a campaign. Lab friction coefficients of different roll grades are similar [RR §3.6 p.51–52] (page cite corrected after full-text pass).
- Chrome-plated work rolls are used for hardness, finish and life [RA §4 p.4-3]. Work rolls for Al hot rolling and for cold rolling wear little, but **their surfaces lose roughness**, and this shows on the product. Chrome plating prolongs campaigns [RR §4.9.1 p.95].
- **Cold-mill roll pairing.** Cold strip work-hardens immediately and cannot absorb accidental local overload, and the work roll must not deform. So the back-up roll must be **significantly softer** (lower yield strength) than the work roll and take the overload plastically [RR §4.5.4 p.77; §4.10.2.2 p.101]. Hot mills do not need this [RR p.77, 101].
- Cold-mill back-up rolls develop work-hardened areas, which are checked by hardness readings and ground off. Every regrind should end with eddy-current crack testing [RR §4.9.1 p.95; §4.6.2.3 p.84].
- Sub-surface "crumbly" spalls in cold-mill back-up rolls start at inclusions or micro-porosity at the depth of maximum Hertzian shear. Particle cleanliness of the roll material (e.g. ESR) is the cure [RR §4.6.2.3 p.84].
- Hardness within one roll grade has no effect on work-roll tonnage performance (ICDP data). Carbide *type* matters more than carbide content [RR §4.8.1 p.89–90].
- Roll crown, roll bending, tilting, crossing, axial shifting (CVC-type profiled rolls), stepped and sleeved back-ups, and zoned spray cooling are the flatness/profile actuators [RA §5 p.5-9/5-10].
- Small rolls give larger reductions per pass but deflect more; large rolls are thermally more stable but have more inertia [RA §4 p.4-3/4-4].
- Cold-mill coolant mainly controls roll temperature and dimensions [RA self-test 5.20].

### 5.4 Foil rolling

What is in the sources:
- Al alloys can be rolled to ~0.05 mm, pure Al to 0.0025 mm [RA p.5-7].
- Two-high mills are used mostly for foil and in labs [RA §4 p.4-4].
- 8011 is a deep-drawing bottle-cap alloy; 8006 (Al-1.6Fe-0.65Mn) and other dilute TM-bearing alloys are used for foil and fin stock [POL §3.3.4 p.131].
- TRC is an established foil-feedstock route (1235/8011) [TRC].

Gap G4: no pass schedules, pack ("double") rolling, or pinhole limits in the accessible text.

### 5.5 Internal heuristics (user spreadsheets — not literature) [INT-CRM]

| Alloy | CRM ε_t target | Reduction | Final anneal | Expected grain size (µm) | Heating-rate note |
|---|---|---|---|---|---|
| EN AW 1070 | ≥ 0.95 | ≥ 61 % | 280–320 °C, 1–2 h (avoid > 340 °C) | 28–48 | not critical |
| EN AW 1050 | ≥ 0.90 | ≥ 59 % | 300–340 °C, 1–2 h (keep < 360 °C) | 30–50 | moderate |
| EN AW 3102 | ≥ 0.80 | ≥ 55 % | 340–370 °C, 1–2 h | 40–65 (slightly elongated) | moderate |
| EN AW 3207 | ≥ 0.85 | ≥ 57 % | 350–380 °C, 1–2 h | 30–50 | reasonably fast |
| EN AW 3003 | ≥ 0.95 | ≥ 61 % | 370–400 °C, 1–3 h | 35–55 | **fast** — slow heating raises T_rx by ~100 °C |

Context: start strip 22 mm → HRM → CRM → full anneal → cold-extrusion slugs. Below ε_t ≈ 0.85, grains are coarser and more variable (orange-peel risk for 3003). Ideal 3207 CRM ε_t is 0.85–1.10, with diminishing returns above ~1.2.
- Status: plausible, and consistent with [POL p.42] (300–420 °C window) and [RA p.5-6]. **The grain sizes are internal estimates, not measured.**
- Cross-check against [INT-RX]: the JMAK model gives T(50 % RX in 1 h) of 327 °C at 45 % CR and 299 °C at 70 % CR for 3207 (0.45Mn-0.15Mg-0.09Cu). So the 350–380 °C anneal has ~25–50 °C margin (internal model).

### 5.6 Design levers (cold rolling)

- **Final cold reduction before anneal** is the main lever on recrystallised grain size and cube fraction; **cold reduction after anneal** sets the H-temper. Table 5-1 together with YS = σ₁εⁿ [TOT] gives the reduction needed for a target YS (inference).
- Per-atom solute choice for work hardening (Table 5-2): Cu ≫ Mg ≈ Si > Mn ≫ Zn. Cu ≤ 0.3 % in NHT alloys [POL p.34]. For 3xxx fin/tube, small Cu/Mg additions add H14/H24 strength cheaply. Watch the corrosion potential (outside scope).
- Avoid excessive total ε before a soft anneal: the risk is shear bands and edge cracks at ε ≳ 1 [POL p.32–33].
- **Roll campaign as a hidden process variable (inference from [RR p.93, 95]).** Work-roll roughness falls and roll-gap friction drifts during a campaign. For slug strip, record the work-roll campaign position (tonnage or km since regrind) with each coil. Friction changes the through-thickness shear, the strip heating and the surface topography, so it can move the surface recrystallised grain size and the lubricant residue left for the anneal (MgO growth). The size of the effect is not quantified in any source.

### 5.7 Pitfalls

- Heat build-up to ≥ 80 °C at high speed allows recovery and lowers the as-rolled temper. Flatness is lost through thermal crown [RA p.5-7].
- Over-rolling beyond the alloy's work-hardening limit → cracking on the next pass; an intermediate anneal is needed [RA p.5-7].
- Lüders bands (Al-Mg O-temper) and PLC serrations: avoid by forming strain-hardened stock or forming above 150 °C [POL §2.1.5 p.40–41].

---

## 6. Annealing after cold rolling (process view)

Physics belongs to the recrystallisation KB; only the process numbers are given here.
- Dislocation density: ~10¹² cm⁻² (heavily cold worked) → ~10¹⁰ cm⁻² after recovery → 10⁷–10⁸ cm⁻² after recrystallisation [POL §2.1.6 p.41].
- Strength falls gradually during recovery, then sharply during recrystallisation. Data for hard-rolled CP-Al: 5 min anneals [POL Fig. 2.10 p.41].
- Batch coil annealing must allow conduction to the innermost wraps. Continuous strip annealing heats fast and gives a finer grain [RA §5 p.5-7].
- Atmosphere: dry N₂ to avoid oxidising lubricant residues and forming MgO on Mg alloys [RA p.5-7].
- **Heating-rate sensitivity in Mn-bearing 3xxx.** The mechanism (Mn precipitating before recrystallisation and pinning the substructure) is stated only in [INT-CRM] and [INT-RX] notes; it is not in the accessible literature pages. It is consistent with the dispersoid-pinning role in [TOT p.137; POL p.43]. Status: **plausible, needs a literature source** (gap G5).
- Internal model constants [INT-RX] (internal, calibrated, not literature):
  - Q_rx = Q₀ + Σ dQᵢ·cᵢ = 100 + 100·Mg + 200·Cu + 80·Mn(ss) = 145 kJ/mol for 3207;
  - JMAK n = 3; B₀ = 2.5×10²⁸ s⁻ⁿ; strain exponent m = 2;
  - t₅₀ ≈ 300 s at 350 °C, 70 % CR.
  - ⚠ Internal inconsistency: Zener limit d = 4r/(3F_v) = 17.8 µm and P_Z = 0.0365 MPa both use **r = 80 nm**, while the sheet labels 80 nm as the dispersoid *size*. If 80 nm is a diameter, d_Z = 8.9 µm and P_Z doubles **(derived)**.

---

## 7. Texture and earing (can, foil, fin-collar stock)

### 7.1 Mechanisms

- **Rolling (deformation) texture** of FCC sheet [TOT Ch.3 PDF p.143; POL §2.1.4 p.39]:
  - components {110}⟨112⟩ (Brass), {123}⟨634⟩ (S), {112}⟨111⟩ (Copper);
  - Polmear describes them as a "tube" of orientations linking (110)[1̄12], (112)[1̄1̄1] and (123)[4̄1̄2] (indices garbled in the text).
- **Recrystallisation texture** [TOT p.143; POL p.39]:
  - cube {001}⟨100⟩ and Goss {011}⟨100⟩, strong especially in high-purity alloys;
  - PSN from coarse constituents randomises the texture;
  - final texture and grain size depend on cold work, heating rate, temperature/time, composition, and particle size and distribution.
- **Extrusions/rod/wire** develop a ⟨111⟩+⟨001⟩ dual fibre (⟨110⟩ fibre for wire per [POL p.39]). In heat-treatable extrusions this raises longitudinal YS by ~70 MPa over transverse [TOT p.143]. An ideal fibre texture can be ~20 % stronger along the fibre than a random aggregate [POL p.39].
- **Earing** [POL §2.1.4 p.39–40; TOT p.143]:
  - four ears usually form;
  - rolling texture dominant → ears at **45°** to RD;
  - cube (annealing) texture dominant → ears at **0°/90°**;
  - a balanced mix → eight small ears or none.
  - Earing is controlled by careful rolling and annealing schedules, sometimes with cross-rolling [POL p.40].
  - For 3004-H19 can stock, earing is controlled by **balancing the cube texture developed during annealing against the rolling texture added on the way to final temper** [TOT p.143].
  - Can stock also depends on controlling the size, volume fraction and distribution of Al₁₂(Fe,Mn)₃Si constituents [TOT PDF p.135].
- r-value: a large r means few slip modes give through-thickness strain, which resists thinning and is good for deep drawing [POL p.37, 39].

### 7.2 Quantities

- Earing % definitions, planar anisotropy Δr, and texture-volume fractions vs process are **not** in the accessible text (gaps G6/G7).
- Only quantitative texture values found: [INT-RX] sheet "RX texture vs annealing temperature". It is an **internal assumption table**: cube 5 % at 250 °C → 30 % at 350 °C → 52 % at 500 °C; PSN-random 15–30 %. Do not treat it as data.

### 7.3 Design levers (inference from [POL; TOT])

- To get **low earing in cups and collars**, set the hot-band/annealed cube fraction so that the 45° ears added by the final cold reduction cancel the 0/90° cube ears. Final cold reduction and hot-band cube are coupled design variables.
- **Alloy lever.** More coarse constituents (Fe/Si/Mn, e.g. α-AlFeMnSi) give more PSN, a more random texture and lower earing amplitude, at the cost of formability and surface. Dispersoids suppress PSN and favour cube (also the [INT-RX] assumption). So Fe/Mn/Si in 3xxx foil and fin tunes the cube vs random balance.
- Cross-rolling at breakdown weakens textures [POL p.40; RA p.5-3].

### 7.4 Pitfalls

- Mechanical fibring (grain shape, particle alignment) causes anisotropy that is often larger than crystallographic texture. Do not attribute all anisotropy to texture [POL p.40].
- Orange peel comes from coarse surface grains. Shallow coarse grains are less harmful, and hot-worked products are less prone than cold-worked [POL §2.1.6 p.43].

---

## 8. Extrusion

### 8.1 Modes and equipment

**Direct vs indirect** [SH §1.3 p.7–12; §1.6 p.20–21]:
- Direct extrusion: the billet slides or shears against the container. Up to **50 % of the work** goes into shearing the near-wall layer [SH p.20].
- Aluminium sticks to the container. A close-fitting dummy block leaves little shell; surface impurities and peripheral segregation collect in the **discard** [SH p.10].
- In heavy metals a dummy block ~2 mm under container diameter leaves a shell ("Dick's method") [SH p.10].
- Indirect extrusion [SH p.11–12, 20–21]:
  - **25–50 % lower peak load**; pressure does not depend on billet length;
  - no frictional surface heating, so higher speeds and less edge or surface cracking;
  - no PCG or coarse peripheral zone; possible zero recrystallisation after solution treatment.
  - Penalties: billets must be machined or die-scalped; cross-section is limited by the hollow stem; quench is delayed (product travels through the stem).
  - Best suited to 2xxx/7xxx bars, tubes and heavy sections.
- Load–stroke curve [SH §1.3 p.10–11]:
  - direct: rises steeply on upset, peaks at breakthrough, falls with billet length, then rises at end of stroke;
  - indirect: flat, no length dependence.
- **Bridge/porthole (welding-chamber) dies** are used for hollow and multi-port shapes. They suit 1xxx, 6xxx, dilute 3xxx/5xxx and Al-Zn-Mg 7xxx; they exclude high-strength aerospace alloys [SH §1.5 p.14–15]. Billet-to-billet extrusion works for the same alloy groups [SH p.13].
- Air removal: rapid front heating gives an axial gradient of ~90–100 °C, so upset fills the container front-to-back [SH p.13]. Dummy-block cleaning return load can reach ~10 % of press capacity [SH p.14].
- **Press example (16 MN direct)** [SH Fig. 1.9 p.18]:
  - containers Ø156 mm (840 MPa) and Ø206 mm (480 MPa), 850 mm long;
  - max ram speed under load 20 mm/s.
- Columns are prestressed ~20 % above maximum load [SH p.18]. Containers and liners are 5 % Cr hot-work steel [SH p.20].
- Billet heating [SH §1.6 p.19; §2.5.1 p.49]:
  - 50 Hz induction: centre-to-surface spread ≤ 3–4 %; allows taper heating;
  - modern gas furnaces: 15–20 min cycle with comparable uniformity;
  - the printed induction penetration depth "~18 µm" is likely an OCR or print error (mm order).
- Extrusion ratios up to ~100:1 are common, but most industrial empirical formulas were fitted at R < 10 [SH §2.3.2 p.35; §2.3.3 p.37]. MPE tube runs at R ≈ 817 [WIL].

### 8.2 Pressure, friction and temperature equations

| # | Equation | Use / numbers | Ref |
|---|---|---|---|
| E1 | p = σ̄·ln R (homogeneous work, Siebel) | **Underestimates by ~60 %**: ignores the peak, friction and redundant work | [SH §2.3 eq. 2.5 p.29] |
| E2 | p = σ̄(a + b·ln R + c·L) | Generic form: a = redundant work, b = inhomogeneity, c = friction | [SH eq. 2.6 p.29] |
| E3 | p_T = σ̄·(a + b ln R + 4mL/(√3·D_B)) | Bulk (slab) analysis with sticking factor m | [SH §2.3.1 eq. 2.7 p.31] |
| E4 | **P = σ̄·[0.171 + 1.86 ln R + 4m·L_B/(√3·D_B)]** | Minimised axisymmetric upper bound (double-triangle field) | [SH §2.3.2 p.36] |
| E4′ | P = σ̄·[0.171 + 1.86 ln R + 4m·(L_B − (D_B − D_E)/(2 tan α))/(√3·D_B)] | Dead-zone-corrected friction length. Reconstructed from OCR | [SH eq. 2.26 p.57] |
| E5 | Dead-zone/deformation depth X_D = 0.35·D_B·(1 + 0.15√R − 0.0145R); semi-angle α = 38.7 + 6.9 ln R (°) | OCR-reconstructed. α is "normally assumed 45°" | [SH eq. 2.28–2.29 p.57] |
| E6 | Friction: τ = m·k (m = 0 perfect lubrication, m = 1 sticking) or τ = μp | **Design m ≈ 0.85**; measured m = 0.88 (1100, 2014 at 300–475 °C). The shear layer at the container is ~40–100 µm thick | [SH §2.4 p.48–49] |
| E7 | Table 2.2 μ values (R = 30, P = aL + C) | 1100, 8 mm/s: μ = 0.075 (300 °C), 0.092 (400 °C). 2014, 5 mm/s: μ = 0.048 (300 °C), 0.055 (400 °C), 0.098 (475 °C). μ *rises* with T, contrary to earlier reports | [SH Table 2.2 p.49] |
| E8 | Stüwe ΔT₁ (adiabatic deformation heat): ∝ σ̄·ln R/(ρc_p) | Exact prefactor illegible. Temperature rise ∝ flow stress × ln R | [SH §2.5.2 p.51] |
| E9 | Stüwe ΔT₂ (container friction) ∝ (σ̄/√3)/(ρc_p)·√(V_R L_B/a). Die-land ΔT₃ ∝ (σ̄/√3)/(ρc_p)·√(V_E L_D/a); heated depth y_D ∝ √(a L_D/V_E) | Die-land contact time < 0.005 s for 6xxx, so heat concentrates in a thin surface layer that forms the product surface | [SH p.51] |
| E10 | Lange: edge ΔT ≈ 2 × mid-face ΔT; ΔT grows with exit speed and die-land length | | [SH p.52, Fig. 2.11] |
| E11 | Integral-profile heat balance: 95 % of work → heat. Material constants: Al k = 201 W/m·K, ρ = 2800 kg/m³, c_p = 1063.9 J/kg·K; Cr-V tool steel k = 32.65 W/m·K, ρ = 7860 kg/m³, c_p = 489.76 J/kg·K | Real-time capable; matches FEM for 7075 (R = 30, 3 mm/s, billet 300–425 °C) | [SH §2.5.4 p.55–58] |
| E12 | Interface temperature T_I = f(T_B, T_C, effusivities √(kρc_p)) | Billet–container contact | [SH eq. 2.25 p.56] |

**Exit temperature** is the controlling variable. It rises when deformation and friction heat exceed losses, so above a certain ram speed heat generation dominates [SH §2.5.2 p.50–51]. Exit temperature rises steeply with both R and ram speed (7075, R = 30) [SH Figs 2.18–2.19 p.60]. Die-land friction adds a significant surface ΔT for 6063 at R = 60, 25–55 mm/s, 400 °C [SH Fig. 2.20 p.61].

### 8.3 Microstructure during extrusion

- Strain-rate and hydrostatic-stress gradients are steep. The main strain-rate line M1 (die entry) controls the product microstructure via the Z it imposes. M2 (container shear) shortens as the ram advances [SH §2.3.4 p.46–47].
- In unlubricated direct extrusion, strain accumulates at the border streamline. Slow loading along M2 favours **static recrystallisation at the periphery** after passing M1. This is the mechanistic origin of peripheral coarse grain (PCG) heterogeneity [SH p.47].
- PCG concentrates at the **back end** of the extrudate and lowers longitudinal tensile strength by **10–15 %** [POL §3.1.5 p.108]. In strong alloys (2024, 7075) the heavily sheared outer layer becomes a coarse-grained low-strength zone after heat treatment [SH p.20].
- Avoid unnecessarily high temperatures and long solution treatments for extrusions and forgings made from extruded stock: non-uniform strain makes them prone to local grain growth [POL §3.1.6 p.109].
- Large surface recrystallised grains are slightly cathodic to the unrecrystallised core, so machining that exposes the core can trigger preferential attack [POL §2.4 p.76–77].
- Hydrostatic-stress gradient at the billet rear drives flow towards the axis, causing the **piping** defect. It is more likely in direct extrusion [SH p.47].

### 8.4 6xxx and quench sensitivity

- Balanced Mg+Si 0.8–1.2 % alloys (6063) extrude easily and are **press-quenched** with water spray or trough; thin sections < 3 mm can be air-cooled. Ageing at 160–190 °C. 6063-T6: 215 / 245 MPa [POL §3.4.3 p.138–140].
- Mg+Si > 1.4 %: quench-sensitive, so separate solution treatment and water quench [POL p.140].
- Low-Mg 6060 (Al-0.35Mg-0.5Si) gives properties comparable to 6063 at **up to 20 % higher extrusion speed** [POL p.141].
- Delay between quench and ageing:
  - > 1 % Mg₂Si: 24 h delay → up to −10 % tensile properties;
  - < 0.9 % Mg₂Si: properties enhanced;
  - ~0.25 % Cu reduces the penalty [POL p.141–142].
- Quench sensitivity [POL §3.1.6 p.112–113]:
  - critical range **290–400 °C**;
  - worse for concentrated alloys;
  - worse with dispersoids that nucleate coarse precipitates (Mg₂Si needles on Mn-bearing particles, Fig. 3.14);
  - ranking: Al₁₂Mg₂Cr (worst) > Al₆Mn > Al₃Zr (least) [POL p.112].
  - Cr (6151) and Mn (6351) refine grain and inhibit recrystallisation during solution treatment [POL p.141].
- Not in the pages read: β-AlFeSi → α-AlFeSi transformation during 6xxx homogenisation, Mg₂Si dissolution vs extrudability, and speed–temperature **limit diagrams**. They are in [SH Ch. 5–6] (gap G2).

### 8.5 Heat-exchanger multi-port tube (AA3102) — process and post-braze data [WIL]

| Item | Value | Ref |
|---|---|---|
| AA3102 composition used | Si 0.07, Fe 0.41, Mn 0.24 wt % | [WIL Table 2 p.18] |
| Tube | 12.0 × 1.30 mm, Ø0.76 mm ports, 0.30–0.40 mm walls | [WIL Fig. 1/7 p.11, 19] |
| Billet / container | Ø102 × 203 mm / Ø106 mm | [WIL Table 3 p.19] |
| Billet / tooling temperature | 495–503 °C / 450 °C | [WIL Tables 3, 5] |
| Ram / exit speed | 0.7 mm/s / ~34 m/min; R = 817 | [WIL Table 3] |
| Peak specific pressure | 445–460 MPa (3102); 651–653 MPa (Al-0.19Sc-0.05Zr, +44 %) | [WIL Table 5 p.38] |
| Exit temperature, 0.3 m after platen | 499–529 °C (3102); 504–517 °C (AlScZr) | [WIL Table 5] |
| Billet homogenisation (AlScZr) | 400 °C/8 h or 450 °C/4 h; heat 50 °C/h, cool 350 °C/h. No measurable effect on extrusion or post-braze properties | [WIL p.18–19, 43] |
| As-extruded structure | 3102: fine, equiaxed, **recrystallised**. AlScZr: unrecrystallised, heavily deformed, some fine recrystallised grains at edges | [WIL §5.2 p.39–40] |
| Sizing/straightening strain | 3–7 % thickness reduction typical. At ~3 % reduction, post-braze strength falls by ~22 % (coarse grains in inner walls) | [WIL §1.1 p.13] |
| Braze simulation | 600 °C, 2 min, air cool. Inner webs fail first | [WIL §3.2 p.21; p.12] |
| Burst pressure, 3102 | 0 % red., no braze 38 MPa; brazed 39 MPa; 5 % red., no braze 48 MPa; 5 % red. + braze 39 MPa | [WIL Table 6 p.50] |
| Burst pressure, AlScZr | 0 % 50 MPa; brazed 39 MPa; 5 % red. 60–63 MPa; 5 % red. + braze 42 MPa. Braze then 288 °C/8 h age: YS 154 vs 60 MPa (brazed AlScZr) vs 39 MPa (brazed 3102) | [WIL Table 6; §5.3 p.48] |
| Design pressure context | R744 (CO₂) ~13 MPa vs R134a ~2 MPa | [WIL p.10] |

### 8.6 Design levers (extrusion)

- **Extrudability ↔ alloy.** Every MPa of σ̄ at ~500 °C costs ln-R-scaled pressure (E4) and adds heat (E8). Dilute 3102 runs at ~27 MPa effective σ̄; AlScZr needs ~39 MPa (derived, §3.4). For R ≈ 800 MPE tubes, a strengthening addition must be weighed against press capacity and exit-temperature limits (inference).
- **Post-braze grain size in tubes** is set by (i) as-extruded state (recrystallised vs fibrous) and (ii) post-extrusion strain (sizing 3–7 %). Small strains → few nuclei → giant grains after braze. Options (inference from [WIL]):
  1. minimise or homogenise sizing strain;
  2. keep the structure unrecrystallised with stable dispersoids (Sc/Zr), recognising Al₃Sc dissolution near 595 °C [WIL p.41];
  3. use precipitation (post-braze ageing) for strength.
- **6xxx speed lever:** reduce Mg towards the 1:1 Mg:Si cluster stoichiometry (6060 concept), +20 % speed [POL p.141]. Prefer Zr or Mn over Cr where quench sensitivity matters [POL p.112].
- **Indirect extrusion** is the process lever against PCG and surface-temperature-limited speed in hard alloys [SH p.11–12, 20–21].
- **Taper heating / isothermal extrusion:** induction taper or rear spray cooling offsets the late-stroke temperature rise [SH p.19, 49]. Real-time integral-profile control of ram speed for constant exit temperature [SH p.55].

### 8.7 Pitfalls (extrusion)

- **Surface tearing.** Starts at edges and corners, where the temperature rise is about double, then spreads over the surface as exit temperature or speed rises [SH §2.5.2 p.52, Fig. 2.10].
- Lubrication: too much or too little graphite grease on die and dummy block causes surface defects not seen in normal unlubricated practice [SH p.10].
- Back-end defects: oxide and dross pipe; discard must be long enough [SH p.10].
- PCG at the back end [POL p.108]. Coarse peripheral zone in 2024/7075 [SH p.20].
- Blisters in solution treatment come from humid atmosphere, hydrogen, unhealed porosity or overheating [POL §3.1.6 p.110–111].

---

## 9. Formability metrics and forming basics

- **n-value:** Tables 5-1/5-2.
- **r-value** = width strain / thickness strain. r > 1 resists thinning; high r helps deep drawing [POL §2.1.3 p.37; §2.1.4 p.39].
- **FLC/FLD:** grid-strain measurement of the boundary between safe and necked/failed strain states [POL §2.1.3 p.38, Fig. 2.8]:
  - positive minor strain = stretching, from uniaxial to equi-biaxial;
  - negative minor strain = drawing (tension–compression, e.g. cup walls).
  - Steel normally out-forms Al sheet.
  - 5052 forms better in O than H24, but **3004 forms better strain-hardened** (canstock).
- **Hydrostatic pressure controls formability:**
  - formability depends on the mean pressure p_m = (σ₁+σ₂+σ₃)/3 [MFH §2.2.4 p.31];
  - EC-Al elongation is ~30 % in tension, ~400 % in cold rolling, and "several 1000 %" in extrusion [SH §2.1 p.24];
  - extrusion is triaxially compressive; ram stress ≥ 2σ̄ before friction if the radial stress is 50 % of the axial [SH §2.1 p.26].
- **Process classification (DIN 8582–8587):** compressive (rolling, forging, extrusion), tensile + compressive (drawing, deep drawing, ironing, spinning, flanging), tensile (stretching, stretch forming, expanding), bending (die, roll, swivel), shear [MFH §2.1 p.6–19]. Forming forces [MFH §2.2.3 p.28–30]:
  - direct (upsetting, rolling): F = A·k_w;
  - indirect (drawing, deep drawing): F = A·k_fm·φ_g/η_F.
- Industrial formability benchmarks [MM slides 11–12]: FLD₀ 23.4 (5182-O) to 33.7 (MMHF-T4); LDR 1.88–2.18 (vendor data).
- Lüders and PLC stretcher-strain markings: avoid with strain-hardened stock or forming above 150 °C [POL p.40–41]. Orange peel comes from coarse grains [POL p.43].

**Design levers (inference).** For deep-drawn fin collars and foil containers, aim for high n and r and low Δr (balanced cube/rolling texture, §7), and a fine, uniform recrystallised grain (enough final cold reduction before anneal, §5.5). For tube stock that sees small sizing strains before braze, prioritise grain-size stability over n and r.

---

## 10. Model-ready constitutive and process parameters

| Group | Parameter | Value | Validity / note | Ref |
|---|---|---|---|---|
| Cold flow | Hollomon K, n (O-temper) | 1100: 146 MPa, 0.242 · 3003: 188, 0.242 · 6061: 224, 0.209 · 5052: 281, 0.198 · 5454: 340, 0.189 · 5086: 368, 0.193 · 5456: 479, 0.178 | RT tensile; σ = K(ε₀+ε)ⁿ for pre-strained material | [TOT PDF p.112; POL p.36] |
| Cold flow | Rolling YS law | YS = σ₁·εⁿ, ε = ln(t_i/t_f); σ₁ = YS at ε = 1 (63 % CR) | per alloy (Alcoa) | [TOT PDF p.111] |
| Cold flow | Solute K and Doherty H | Cu 1.00 / 3.38 GPa; Mg 0.37 / 1.52; Si — / 1.56; Mn — / 1.03; Zn 0.071 / 0.27(?) | per at. fraction (OCR caveat) | [TOT PDF p.111] |
| Cold flow | Cryogenic gain | +~40 % strength at −196 °C (1100) | | [POL p.36] |
| Substructure | σ = σ₀ + k₁d⁻ᵐ | m = 1 (cells) → 0.5 (subgrains) | | [POL p.36–37] |
| Physical | SFE (Al) | ~170 mJ/m² | | [POL p.36] |
| Hot flow | Z | ε̇·exp(Q/RT) | | [SH eq. 2.4 p.28] |
| Hot flow | α, n, Q, A per alloy | **missing** | retrieve SH Ch.4 / TOT Ch.7–8. The SH whole-file download failed on 2026-10-12 (size limit); needs a split PDF | — |
| Hot flow | σ̄ AA3102, ~500 °C, MPE extrusion | ≈ 27–28 MPa (36 MPa if no friction term) | back-calculated **(derived)** from E4 + WIL data | [WIL; SH] |
| Hot flow | σ̄ Al-0.19Sc-0.05Zr, same | ≈ 39 MPa (+44 %) | **(derived)** | [WIL; SH] |
| Extrusion | Pressure | P = σ̄[0.171 + 1.86 ln R + 4mL_B/(√3 D_B)] | upper bound; OCR-reconstructed | [SH p.36] |
| Extrusion | Homogeneous lower bound | p = σ̄ ln R (−~60 %) | | [SH p.29] |
| Extrusion | Friction factor | m = 0.85 (design); 0.88 measured | sticking regime | [SH p.48–49] |
| Extrusion | Coulomb μ | 1100: 0.075–0.092 · 2014: 0.048–0.098 (300–475 °C) | R = 30 | [SH Table 2.2] |
| Extrusion | Shear-layer thickness | 40–100 µm | | [SH p.49] |
| Extrusion | Deformation-zone geometry | α = 38.7 + 6.9 ln R (°); X_D = 0.35 D_B(1 + 0.15√R − 0.0145R) | OCR-reconstructed; fitted at modest R | [SH p.57] |
| Extrusion | Breakthrough increment | Δp = 6.62 + 0.921 ln(Z/A) | OCR uncertain | [SH p.57] |
| Extrusion | Strain rate | Feltham (H3) or modified (H4) | FEM: parabolic in ln R | [SH p.28, 36–37, 44] |
| Extrusion | Indirect vs direct load | −25 to −50 % | | [SH p.11–12] |
| Thermal | Al: k, ρ, c_p | 201 W/m·K, 2800 kg/m³, 1063.9 J/kg·K | for extrusion heat balance | [SH p.56] |
| Thermal | Tool steel: k, ρ, c_p | 32.65 W/m·K, 7860 kg/m³, 489.76 J/kg·K | | [SH p.56] |
| Thermal | Work → heat | 95 % | | [SH p.55] |
| Diffusion | D₀, Q (Cu, Zn, Mg, Si, Zr) | Table §3.5 | Mn/Cr/Fe rows of SH suspect | [SH Table 2.3 p.65] |
| Diffusion | D(500 °C), cm²/s | Mn 5×10⁻¹³; Cu 5×10⁻¹⁰; Mg, Si 1×10⁻⁹ | use for 3xxx | [POL p.105] |
| Homogenisation | Window / time | 450–600 °C; 6–24 h; +50 °C → ~⅓ time (Q_app ≈ 116 kJ/mol, **derived**) | | [POL p.104–105] |
| Homogenisation | Heating rate for dispersoid nucleation | slow, e.g. ~75 °C/h (50 °C/h vs 500 °C/h example) | | [POL p.106] |
| Homogenisation | Relaxation time | τ = l²/(π²D) | | [SH p.66] |
| Preheat | Max hot-working temperature | 10–50 °C below solidus | | [RA p.4-6/4-7] |
| Hot rolling | Breakdown in/out | 200–600 mm → 15–35 mm | | [POL p.107] |
| Hot rolling | Tandem exit | 2.5–8 mm (3–6 mm for < 1 mm final) | | [POL p.107; RA p.5-7] |
| Hot rolling | Pass example | ~13 % (ε_t 0.14) per breakdown pass | **(derived)** | [RA p.5-3] |
| Hot rolling | Mill speed | ≤ ~600 m/min | | [RA p.4-6] |
| Rolls | Young's modulus (for roll flattening, stack deflection) | steel 210 GPa ± 3 %; nodular iron 175 GPa ± 5 %; austenitic steel 180 GPa ± 3 %; ν = 0.3 | grey-iron cores are non-linear; compound-roll E drifts as the shell is ground away | [RR §3.2.1 p.18; §3.7 p.53] |
| Rolls | Safe nominal bending stress | grey iron 60; nodular 90; cast steel 120; forged steel 150 MPa | fillet notch factor 1.8–2.2 | [RR §4.10.1 p.100] |
| Rolls | Linear load, strip vs work roll (hot strip) | < 1500 t/m width (≈ 14.7 kN/mm, **derived**) | steel-mill experience limit; above it only nodular-core rolls | [RR §4.10.1.2 p.100] |
| Rolls | Hertzian pressure, work roll vs back-up roll | ≤ 2100 MPa | peaks near barrel edges; chamfer the back-up roll | [RR §4.10.2.1 p.101] |
| Rolls | Static torque strength | 0.9 × tensile strength | torque treated as static load | [RR p.74, 100] |
| Rolls | Roll accuracy | TIR one grade finer than product tolerance; ≤ 0.003 mm (tin plate) | | [RR p.102–103] |
| Roll gap | Friction coefficient μ | **no numbers in sources**. Mill μ ≫ lab μ and rises during a campaign. Allowed bite angle falls with speed | back-calculate μ from measured roll force | [RR p.51–52, 92–93] |
| Cold rolling | First pass | ~50 % | | [RA p.5-7] |
| Cold rolling | Speed | 1525–1830 m/min (≤ 2135) | | [RA p.5-7, 4-6] |
| Cold rolling | Strip temperature rise | to ≥ ~80 °C | | [RA p.5-7] |
| Annealing | O-temper NHT | 335–405 °C, 0.5–2 h | | [RA p.5-6] |
| Annealing | Pure Al RX time | hours at 280 °C; minutes at 380 °C; seconds at 500 °C | hard-rolled | [POL p.42] |
| Annealing | Dislocation density | 10¹² → 10¹⁰ → 10⁷–10⁸ cm⁻² | CW → recovered → recrystallised | [POL p.41] |
| Stabilisation | H3x | 120–150 °C [POL] vs ~180 °C [RA] | conflict | |
| Microstructure | Effective dispersoid size | < 0.4 µm [TOT]; 0.05–0.5 µm [POL]; coarse PSN particles > ~1 µm [POL] | | [TOT p.137; POL p.42–43] |
| Microstructure | PCG penalty | −10–15 % longitudinal TS | | [POL p.108] |
| Texture | Extrusion fibre strengthening | +~70 MPa longitudinal vs transverse | HT extrusions | [TOT p.143] |
| Quench | Critical range | 290–400 °C. Sensitivity: Cr > Mn > Zr dispersoids | | [POL p.112–113] |
| Casting | DC cooling / DAS | 1–5 °C/s; 30–70 µm | | [POL p.99, 102] |
| Casting | TRC cooling / DAS | 10²–10³ °C/s (55–555); 5–10 µm | | [POL p.102; RA p.3-4] |
| Casting | TRC window (1235/8011) | 685 ± 5 °C melt; 5.2 mm gap; ~50 mm contact; Ø690 mm rolls | | [TRC p.116] |
| HX tube | Sizing strain → post-braze strength | 3–7 % typical; ~3 % → −22 % | AA3102 MPE | [WIL p.13] |
| HX tube | Extrusion window | 495–503 °C billet, R = 817, 0.7 mm/s, ~34 m/min, 445–460 MPa | AA3102 | [WIL Tables 3, 5] |
| Internal | CRM ε_t targets / anneal | 1070 ≥ 0.95 / 280–320 °C · 1050 ≥ 0.90 / 300–340 · 3102 ≥ 0.80 / 340–370 · 3207 ≥ 0.85 / 350–380 · 3003 ≥ 0.95 / 370–400 | **heuristic** | [INT-CRM] |
| Internal | 3207 Q_rx, JMAK | 145 kJ/mol; n = 3; B₀ = 2.5e28; m = 2 | **internal calibration** | [INT-RX] |

---

## 11. Open questions / gaps

| ID | Gap | Why it matters | Where to get it |
|---|---|---|---|
| **G1** | **Per-alloy sinh-law constants (α, n, Q, A) for 1xxx, 3003/3102/3207, 5xxx, 6xxx, 7xxx**; subgrain size vs Z (d⁻¹ = a + b ln Z); flow-stress tables | Core of any hot-rolling or extrusion model. Currently only a single σ̄ point for 3102 (derived) | [SH Ch.4 §4.2, 4.11.4 (pp.127 ff.)]; [TOT Ch.7 p.351, Ch.8 p.385]. **2026-10-12 whole-file download failed:** 10.46 MB copy → "connection … closed because a message from the server was too large"; 10.51 MB copy → "File too large for download, over limit of 10 MB" (§0 note). Next step: put a chapter-split PDF (Ch.4, ≤ ~3.8 MB) on Drive, or use the Drive API outside this connector |
| G2 | 6xxx homogenisation (β → α-AlFeSi, Mg₂Si dissolution) vs extrudability; **limit diagrams** (speed–temperature); 3xxx homogenisation practice for extrusion billets | Extrudability and surface-defect windows | [SH §3.3, Ch.5–6]. Same retrieval block as G1 (2026-10-12) |
| G3 | Hot-mill finishing temperatures, coiling temperatures, coil cooling and self-annealing of 3xxx/1xxx hot band | Sets hot-band texture/RX state, and therefore earing and recrystallisation response | [TOT Ch.7]; recrystallisation KB. [RR] (read in full) has none. [RA] appendices are still unread: its 7.19 MB download failed on 2026-10-12 |
| G4 | Foil rolling practice: pass schedule, pack/double rolling, pinholes, final-anneal practice for 8011/8006/1235 | Foil and fin stock | [TOT Ch.7]. Not in [RR] (read in full) |
| G5 | Literature confirmation of the heating-rate effect (Mn precipitation before RX) on anneal grain size in 3xxx | [INT-CRM]/[INT-RX] assume it; 3003 "~100 °C T_rx increase" is unsourced | Recrystallisation KB (Humphreys & Hatherly) |
| G6 | Quantitative earing: % ears vs cube volume fraction vs final cold reduction (3004/3104, 8011 closures) | Can and fin-collar design | [POL §3.6.5] (not returned); [TOT Ch.18] |
| G7 | r-values, Δr and FLDs for 3xxx fin/foil tempers | Formability metrics for HX alloys | [TOT Ch.18] |
| G8 | Rolling-force/torque models (Orowan, Sims, Ekelund) with Al friction data | Pass-schedule models; the force equations in §4.2 are still general knowledge | [TOT Ch.7]. **Partly filled 2026-10-12:** [RR] is now read in full. It gives roll E/ν, mill design limits (linear load, Hertzian pressure, bending, torque) and qualitative bite/friction behaviour (§4.2, §10). It contains **no** force, torque or flattening model and no Al friction numbers (its bite and friction charts are images). Still needed: the force models and μ for Al hot and cold rolling |
| G9 | Correct Mn, Cr, Fe diffusivities | Sheppard Table 2.3 Mn is ~10³× faster than Polmear; Cr/Fe rows look non-physical | Recrystallisation/diffusion KB; primary diffusion data |
| G10 | Stabilisation temperature for H3x: 120–150 °C [POL] vs ~180 °C [RA] | Temper practice for 5xxx/3004 | Primary temper spec (EN 515). The EAA brochure (S-043, ch06 §5) defines H3x as stabilised "by a low temperature heat treatment or as a result of heat introduced during fabrication" and gives no temperature, so the gap is still open |
| G11 | Units in [TRC] (strip speed "cm/min", load "kN/mm", productivity "t/(m·h)") | Caster modelling | Original thesis [TRC ref 7] |
| G12 | [INT-RX] Zener limit uses r = 80 nm while the sheet labels 80 nm as "size". [INT-CRM] grain sizes are unvalidated | Internal model consistency | Measure dispersoid radius by TEM/SEM; EBSD grain-size validation |
| G13 | Strain-measure consistency: [INT-*] use ε_t; constitutive and RX literature may use ε̄ = 1.155·ε_t | Systematic error if mixed | Fix the convention in the model code |
| G14 | Sheppard eqs. 2.4, 2.26–2.29 and 2.27 (Δp) are OCR-reconstructed | Verify before coding | Clean copy of [SH] pp.28, 36–37, 57. Not verified: the 2026-10-12 download failed (G1). A split PDF of Ch.2 (pp.23–71) would also settle this |

**Top 5 implications for alloy design (summary).**
1. Per-atom work hardening Cu ≫ Mg ≈ Si > Mn ≫ Zn [TOT] gives cheap H-temper strength in 3xxx fin/tube. Cu ≤ 0.3 % in NHT alloys [POL].
2. Earing control is a texture-balance problem: hot-band/annealed cube against final-reduction rolling texture. Coarse constituents (PSN) randomise the texture; dispersoids favour cube [POL; TOT].
3. Dispersoid state (size < 0.4 µm, coherent better; Cr worst for quench sensitivity) decides fibrous vs recrystallised extrusions, PCG, and the quench penalty. Tune the homogenisation heating rate (~75 °C/h for nucleation) [POL; TOT].
4. Heat-exchanger tube: small sizing strains (3–7 %) plus brazing produce coarse grains and ~22 % strength loss in 3102. Sc+Zr keeps the tube unrecrystallised to ~575 °C but costs +44 % extrusion pressure [WIL].
5. Continuous-cast 3xxx/8xxx keeps Mn/Fe supersaturated (no homogenisation). Its anneal response and formability need alloy and process re-tuning, not DC practice [RA; POL; MM].
