# 09 — In-house R&D data (user's own working files, Google Drive)

> Compiled 2026-10-12 from the user's own Google Drive working files (owner: the user).
> Numbers in the "data" parts are transcribed **exactly** as they appear in the Drive text export.
> Everything under an **Assessment** heading is the documenting metallurgist's interpretation, not user data.
> Where a number in an Assessment is my own back-calculation it is marked *(recalc.)*; where it is general
> literature/standard knowledge (not from the user's files) it is marked *(ext., verify)*.

## 0. What these files are

The files are working spreadsheets, documents and one presentation produced mainly between Jan and Apr 2026.
**Note:** the application context is **aluminium slugs for cold impact extrusion of aerosol cans**
(1xxx and lean 3xxx alloys: EN AW-1070, -1050, -3102, -3207, -3003), *not* heat-exchanger fin/foil.
The 3xxx physical metallurgy (Mn dispersoids, recrystallisation (RX), Zener pinning, concurrent precipitation)
carries over to HEX/foil work, but the process windows (low cold reduction of 25–60 %, batch annealing of
thick strip/slugs, MgO surface oxide) are specific to slugs.

Chronology (all on 2026-03-23/24 unless stated): `mg_dashboard` (14:29–15:02 UTC) → `3102_RX_simulation`
(15:14–15:17) → `AA3207_Recrystallization_Simulation` (4 versions, 16:14–16:26) → temper tables (20:39–20:52)
→ CRM (cold-rolling-mill) reduction tables (next morning 08:38–08:39).

**Important terminology finding:** in these files **"CRM" = Cold Rolling Mill** (paired with "HRM" = Hot
Rolling Mill). The `EN_AW_Master_CRM_Reduction_Tables.xlsx` workbook contains **no EU critical-raw-materials
content** (no Mg/Si/Sc criticality, no substitution strategies). Likewise the CBAM presentation contains **no
embedded-emissions (tCO2e/t) figures** — only a CBAM cost trajectory in $/t.

### File inventory

| # | File | Type | Last modified (UTC) | Drive link | Readability |
|---|------|------|--------------------|-----------|-------------|
| 1 | Modified 3102 Alloy Composition Explained | Google Sheet | 2026-01-19 08:56 | https://docs.google.com/spreadsheets/d/1tLOr9HtNx_UJbJOkkBQfU9Ej-tIjQS-xKueHwr_wBwU | Full (one 11×3 table, no comments) |
| 2 | 3102_RX_simulation.xlsx | xlsx (25.7 kB, 3 sheets) | 2026-03-23 15:17 | https://drive.google.com/file/d/1nnyhJQ5mlPHC2uJupDlVSyyiQ2H1GC6O/view | Values readable; cell formulas and the 2 embedded charts are not in the export. Model formulas reverse-engineered (§2) |
| 3a | mg_dashboard.xlsx (latest) | xlsx (45.3 kB, 6 sheets) | 2026-03-23 15:02 | https://drive.google.com/file/d/1-7mxtk6cte3lJ6qknxcP8qKO9SVkOcQQ/view | Values readable; formulas/charts not exported |
| 3b | mg_dashboard.xlsx | xlsx (31.4 kB) | 2026-03-23 14:46 | https://drive.google.com/file/d/1qiRjIGLjR6IlcUF0qCaf1utUnA5tvdG2/view | Same text as 3a |
| 3c | mg_dashboard.xlsx | xlsx (45.3 kB) | 2026-03-23 14:43 | https://drive.google.com/file/d/1FtbQAUJ2JgBpWM_tI8wK_UdP6zzFT3nu/view | Same text as 3a except evaluator input CR = 45 % |
| 4a | AA3207_Recrystallization_Simulation.xlsx (latest) | xlsx (164.6 kB, 8 sheets) | 2026-03-23 16:26 | https://drive.google.com/file/d/1L9MDNPrCcWymlvgcowcv6Gf34eLJvwm2/view | Values readable; formulas not exported but equations are written in the sheets and were verified by recalculation |
| 4b | AA3207_Recrystallization_Simulation.xlsx | xlsx (48.8 kB) | 2026-03-23 16:23 | https://drive.google.com/file/d/1t2chD4lXva-h6DdnMQDXoOrfz-xenRSR/view | Values readable |
| 4c | AA3207_Recrystallization_Simulation.xlsx | xlsx (45.3 kB) | 2026-03-23 16:17 | https://drive.google.com/file/d/1QH-vB1QFvltSsp1cHaffXQSQ6bzwXrhW/view | Values readable |
| 4d | AA3207_Recrystallization_Simulation.xlsx | xlsx (61.4 kB) | 2026-03-23 16:15 | https://drive.google.com/file/d/1jw-jp7hdKhxk4eKLBnWLu-7gTSehRXpm/view | Values readable |
| 5a | EN_AW_Master_CRM_Reduction_Tables.xlsx | xlsx (38.2 kB, 6 sheets) | 2026-03-24 08:39 | https://drive.google.com/file/d/1KN_kyx3RDw0QfLNvi1UHx7UYP5xwLjpq/view | Values readable; cell colours not exported |
| 5b | EN_AW_3207_CRM_Reduction_Table.xlsx | xlsx (11.6 kB, 1 sheet) | 2026-03-24 08:38 | https://drive.google.com/file/d/1r-GFxL4bVuGG_ZGm_Lix-SQ3Upc7gROk/view | Full (includes colour legend as text) |
| 6a | aluminium_tempers_v3.xlsx | xlsx (24.5 kB, 7 sheets) | 2026-03-23 20:45 | https://drive.google.com/file/d/1XYBOGMAvW4uHGHxxecQr3HeGGlQ4EO-k/view | Full text |
| 6b | aluminium_tempers_v2.xlsx | xlsx (19.9 kB, 6 sheets) | 2026-03-23 20:39 | https://drive.google.com/file/d/1jujW_zC4r4jPc2HXq6FuyaNhPouPKhqP/view | Full text |
| 6c | aluminium_tempers_SLO.xlsx | xlsx (24.9 kB, 7 sheets, Slovenian) | 2026-03-23 20:52 | https://drive.google.com/file/d/1qg7Mvfi33_I1jax72vUiRI8YPRWyN09j/view | Full text (newest of the three) |
| 7 | Aluminium_Alloys_CBAM_Presentation.pptx | pptx (53.1 kB, ~5 slides) | 2026-01-22 15:08 | https://drive.google.com/file/d/1UQmAOQXlfJI3pv-4Mz3W2K0ESDv2gTxZ/view | Slide text only (images/graphics not exported) |
| 8a | Aluminum Slug Specifications - Technical Analysis | Google Doc | 2026-04-23 21:05 | https://docs.google.com/document/d/1GDXMCKCnH1YrBwSuEtkir9aDZA1nRD6pGbPFJX_lKzY | Full; encoding artefact "»B" (= "³") |
| 8b | Aluminum Slug Data Table | Google Doc | 2026-04-23 21:06 | https://docs.google.com/document/d/1vqiAL2AcCpv584C0DPJspPvnRL-8DiPU4iXmY_qM4U8 | Full |
| 8c | Aluminum Slug Specifications Reference | Google Doc | 2026-04-23 21:04 | https://docs.google.com/document/d/1a2PUBN1OpYaCwpsmSeUqfkI8ViHDcYezazENjEMCfHQ | Essentially empty (only the text "Aluminum Slug") |

Files 3a–c, 5b and 8b–c were found by Drive search (not in the original request list).
**Excluded:** everything in the folder `microstructure-sim-v2.14.0` (incl. its `src/`, `models/`, `data/`
sub-folders with `mgo.js`, `anneal.js`, `grain.js`, `a1-2026-08-09.csv`, `calibration-trial.csv`, etc.) as
instructed; reference literature PDFs/books (not the user's own work); and commercial/financial documents
(company valuation, sales report, pricing instruction), which are non-technical.

---

## 1. Modified 3102 Alloy Composition Explained (Google Sheet)

**Purpose:** proposed chemistry window for a "modified 3102" slug alloy, with the intended role of each element.
Header "Kemija" = Slovenian for "chemistry". No numeric property targets in the file.

| Kemija | % | Role in your Alloy |
|---|---|---|
| Aluminum (Al) | | Base metal. |
| Manganese (Mn) | 1.10 – 1.30 | Primary strengthener; enables thin-walling and "burst" resistance. |
| Magnesium (Mg) | 0.25 – 0.35 | Enhances yield strength and work-hardening response. |
| Zinc (Zn) | 0.10 – 0.15 | Improves formability, refines grain, and provides natural aging. |
| Iron (Fe) | ≤ 0.45 | Limited to prevent brittle intermetallics and "slither" defects. |
| Silicon (Si) | ≤ 0.15 | Kept low to avoid localized hardness and tool wear. |
| Copper (Cu) | 0.05 – 0.10 | Added for surface finish and to prevent "galling" on the punch. |
| Titanium (Ti) | ≤ 0.05 | Acts as a grain refiner during casting. |
| Others (Each) | ≤ 0.05 | Impurity control. |
| Others (Total) | ≤ 0.15 | Impurity control. |

**Implied design targets (qualitative, from the "Role" column):** thinner can walls ("thin-walling"),
higher burst resistance, higher yield strength / work hardening, no galling on the punch, low tool wear.

### Assessment
- **Designation:** Mn 1.10–1.30 is far outside EN AW-3102 (Mn 0.05–0.40 per the user's own other files); this is
  3003/3103-level Mn. With Mg 0.25–0.35 the alloy is closer to a lean 3005/3103 variant than to 3102.
  It would need its own designation/customer approval *(ext., verify against EN 573-3)*.
- **Rationale that is physically sound:** Mn (solid solution + α-Al(Mn,Fe)Si / Al6(Mn,Fe) dispersoids) and Mg
  (solid solution, higher work-hardening rate) both raise the flow stress of the impact-extruded wall, which is
  what allows thinner walls at equal burst pressure (hoop stress ∝ P·D/2t). Mn in solution/dispersoids also
  improves resistance to softening during the lacquer-curing bake of cans.
- **Statements that are not supported by physical metallurgy:**
  - Zn 0.10–0.15 % does **not** improve formability, refine grain or give natural ageing; at this level Zn sits in
    solid solution with negligible mechanical effect (Al-Zn-Mg ageing needs several % Zn). Its main effect is to
    make the alloy more electrochemically active. It is better regarded as a tolerated scrap impurity.
  - Cu 0.05–0.10 % is not a recognised anti-galling addition (galling is governed by lubricant, surface oxide,
    slug surface condition and tooling). Cu raises strength slightly, shifts the corrosion potential nobler and
    slows recovery; it lowers thermal conductivity.
  - Ti ≤ 0.05 % refines the as-cast grain only together with TiB2/Al3Ti nuclei (grain-refiner rod); Ti alone is
    weak.
  - "Slither defects" probably means "sliver" defects (coarse primary Fe/Mn intermetallics tearing out in thin
    walls). Mn + Fe up to 1.75 % should be checked against the primary Al6(Mn,Fe) limit for the actual casting
    route *(ext., verify)*.
  - Si ≤ 0.15 %: low Si keeps more Mn in supersaturated solid solution (fewer α-dispersoids) → higher strength
    but **slower recrystallisation and a stronger heating-rate sensitivity** (see §5 notes on EN AW-3003).
- **Process consequences** (from the user's own other files): 2–3× more Mg than the current 3102 (0.12 %) will
  increase MgO growth during annealing (§2 note: "0.12 % Mg gives ~60 % less MgO than 0.4 % Mg alloys"), and
  1.1–1.3 % Mn puts the alloy in the "3003" row of the CRM table (§5): higher cold reduction (ε ≥ 0.95) and **fast
  heating** are required to avoid coarse, elongated RX grains. Slug hardness and press loads will rise.
- **Gap:** no quantitative targets (slug HB, can UTS/YS, burst pressure, wall thickness) are recorded.

---

## 2. 3102_RX_simulation.xlsx — JMAK annealing simulator for EN AW-3102 slugs

**Purpose:** JMAK recrystallisation model of the batch slug anneal versus cold reduction (CR) and soak
temperature, with a cycle calculator including MgO oxide growth. Sheets: `3102-3207 Alloy`,
`JMAK CR Simulation`, `Cycle Simulator`.

### 2.1 Composition & dispersoid system (sheet 1)
Title line: **"EN AW 3102/3207 — 0.09%Cu, 0.12%Mg, 0.2%Mn"**

| Element | wt% | Spec | Metallurgical role |
|---|---|---|---|
| Si | 0.17 | ≤0.40 | α-Al(Mn,Fe)Si dispersoids |
| Fe | 0.35 | ≤0.70 | Constitutive particles → PSN sites |
| Cu | 0.09 | ≤0.10 | ↑ Stored energy; Al₂Cu at GB possible |
| Mn | 0.3 | 0.05–0.40 | Al₆Mn dispersoids → Zener pinning |
| Mg | 0.12 | ≤0.15 | MgO formation driver |
| Al | Bal. | ≥99.0 | Matrix |

Key metallurgical notes (verbatim):
- "Zener limit D_lim ≈ 27 µm from Al₆Mn (r~0.2µm, Fv~0.01). Grain growth onset ~450°C."
- "Cu 0.09%: increases stored energy ~5-10% vs Cu-free → slightly faster RX nucleation."
- "Mn precipitation zone 270-350°C: AVOID prolonged holds here (pins dislocations before RX nucleation)."
- "MgO transition at ~400°C: logarithmic→parabolic. Your 0.12%Mg gives ~60% less MgO than 0.4%Mg alloys."

### 2.2 Model equations
The export shows values only. The following formulas were **reverse-engineered** from the tables and reproduce
every tabulated t99 value and every RX % value exactly *(recalc.)*:

- JMAK: X(t,T) = 1 − exp[−ln2 · (t / t₀.₅(T))ⁿ]  →  t₉₉ = t₀.₅ · (ln100 / ln2)^(1/n)
- Arrhenius: t₀.₅(T) = t₀.₅(430 °C) · exp[(Q_rx/R)·(1/T − 1/703.15 K)], R = 8.314 J/(mol·K)
- CR dependence (CR in %):
  - n(CR) = 1.8 + 0.012·(CR − 25)
  - Q_rx(CR) = 200 − 0.8·(CR − 25) kJ/mol
  - t₀.₅(430 °C, CR) = 22.0 − 0.38·(CR − 25) min
- Grain size in the "optimal cycle" table follows ≈ d ∝ CR^-0.7, and hardness follows
  HB ≈ 19.8 + 37.4/√d(µm) (Hall–Petch-type fit reproducing 114/80/43 µm → 23.3/23.9/25.5 HB) *(recalc.)*.

Cycle-simulator outputs (Avrami n = 1.8, Q_rx = 200.0 kJ/mol, t₀.₅(430 °C) = 22.0 min at 25 % CR) are consistent
with the formulas above.

### 2.3 Results — t₉₉ map: time for 99 % RX (min) by CR and soak temperature

| CR(%) | 350°C | 360°C | 370°C | 380°C | 390°C | 400°C | 410°C | 415°C | 420°C | 430°C |
|---|---|---|---|---|---|---|---|---|---|---|
| 15 | 7672.0 | 4069.3 | 2201.4 | 1213.5 | 681.1 | 388.9 | 225.7 | 173.0 | 133.1 | 79.6 |
| 20 | 6261.2 | 3361.8 | 1840.3 | 1026.1 | 582.3 | 336.1 | 197.1 | 151.8 | 117.4 | 71.0 |
| 25 | 5090.7 | 2766.8 | 1532.6 | 864.4 | 496.0 | 289.4 | 171.5 | 132.8 | 103.2 | 63.0 |
| 30 | 4117.8 | 2265.5 | 1269.8 | 724.5 | 420.4 | 247.9 | 148.5 | 115.5 | 90.2 | 55.6 |
| 35 | 3308.0 | 1842.3 | 1044.9 | 603.0 | 353.8 | 210.9 | 127.6 | 99.8 | 78.4 | 48.8 |
| 40 | 2633.6 | 1484.7 | 852.1 | 497.4 | 295.1 | 177.8 | 108.8 | 85.5 | 67.5 | 42.4 |
| 45 | 2071.9 | 1182.4 | 686.6 | 405.4 | 243.2 | 148.1 | 91.6 | 72.4 | 57.4 | 36.4 |
| 50 | 1604.2 | 926.7 | 544.5 | 325.2 | 197.3 | 121.5 | 75.9 | 60.3 | 48.0 | 30.8 |
| 55 | 1215.1 | 710.6 | 422.5 | 255.3 | 156.6 | 97.4 | 61.5 | 49.1 | 39.3 | 25.5 |
| 60 | 892.0 | 528.0 | 317.7 | 194.2 | 120.4 | 75.8 | 48.3 | 38.8 | 31.2 | 20.4 |

### 2.4 Results — RX % vs time at 415 °C ("optimal soak T for 25 % CR")

| Time (min) | 15%CR | 25%CR | 35%CR | 45%CR | 50%CR |
|---|---|---|---|---|---|
| 0 | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 |
| 5 | 1.2 | 1.3 | 1.5 | 2.0 | 2.4 |
| 10 | 3.8 | 4.3 | 5.4 | 7.8 | 10.1 |
| 15 | 7.3 | 8.7 | 11.4 | 17.0 | 22.0 |
| 20 | 11.6 | 14.1 | 19.0 | 28.4 | 36.5 |
| 30 | 21.5 | 27.1 | 36.7 | 53.4 | 65.5 |
| 45 | 38.1 | 48.1 | 63.1 | 82.6 | 91.7 |
| 60 | 54.0 | 66.8 | 82.3 | 95.7 | 99.0 |
| 75 | 67.7 | 80.7 | 93.0 | 99.3 | 99.9 |
| 90 | 78.5 | 89.8 | 97.7 | 99.9 | 100.0 |
| 120 | 91.7 | 97.8 | 99.9 | 100.0 | 100.0 |
| 150 | 97.3 | 99.7 | 100.0 | 100.0 | 100.0 |

### 2.5 Results — optimal cycle & microstructure by CR

| CR(%) | Grain(µm) | HB | Opt.T(°C) | Soak(min) | MgO(nm) | vs25%CR |
|---|---|---|---|---|---|---|
| 15 | 114 | 23.3 | 430 | 91 | 9.3 | +1% |
| 20 | 94 | 23.6 | 430 | 81 | 9.1 | -1% |
| 25 | 80 | 23.9 | 425 | 92 | 9.2 | +0% |
| 30 | 70 | 24.1 | 425 | 81 | 9 | -2% |
| 35 | 63 | 24.4 | 420 | 90 | 9 | -1% |
| 40 | 58 | 24.6 | 415 | 98 | 9.1 | -1% |
| 45 | 53 | 24.8 | 415 | 83 | 8.8 | -4% |
| 50 | 49 | 25 | 410 | 87 | 8.8 | -4% |
| 55 | 46 | 25.3 | 405 | 88 | 8.7 | -5% |
| 60 | 43 | 25.5 | 400 | 87 | 6 | -35% |

("vs25%CR" is the MgO change relative to 25 % CR.)

### 2.6 Cycle simulator (inputs blue = editable)

| Input | Value | Unit | Note |
|---|---|---|---|
| Cold reduction CR% | 25 | % | 15-60% |
| Soak temperature | 415 | °C | Main RX hold |
| Soak time | 75 | min | Hold time |
| Equalization T | 370 | °C | <400°C! |
| Equalization hold | 30 | min | |
| Impact T (0=none) | 450 | °C | Overshoot |
| Impact hold | 10 | min | |
| Ramp rate 1 | 3.5 | °C/min | Amb→eq |
| Ramp rate 2 | 2.5 | °C/min | eq→soak |
| Cool rate | 2 | °C/min | Natural |

| Output | Value | Unit |
|---|---|---|
| Avrami n | 1.8 | — |
| Q_rx | 200.0 | kJ/mol |
| t₀.₅ at 430°C | 22.0 | min |
| t₀.₅ at soak T | 46.4 | min |
| t₉₉ at soak T | 132.8 | min |
| RX% at soak end | 80.7 | % |
| Full RX? | NO — increase T or time | — |
| Time >400°C | 105.0 | min |
| Total cycle | 353.1 | min |
| MgO oxide | 9.1 | nm |
| Grain size | 80.0 | µm |
| Hardness HB | 23.9 | HB |

Cycle structure (from the identical calculator in `mg_dashboard`, §3.6): 25 °C → 370 °C at 3.5 °C/min (98.6 min)
→ equalise 30 min → ramp 2.5 °C/min to the 450 °C "impact"/overshoot (32 min) → hold 10 min → soak 415 °C
75 min → cool 2 °C/min to 200 °C (107.5 min) = 353.1 min; time > 400 °C = 20 + 10 + 75 = 105 min *(recalc.)*.

### Assessment
- **Internally consistent:** all tables follow the reconstructed formulas exactly; the n and Q values are
  physically reasonable for commercial Al-Mn (experimental Avrami exponents 1–2; apparent Q for RX of
  commercial Al alloys of order 150–250 kJ/mol *(ext.)*). Increasing n and decreasing Q with CR is a reasonable
  empirical description.
- **Linear t₀.₅(CR) law** reaches zero at CR ≈ 83 % *(recalc.)* — fine for the stated 15–60 % range, but must not
  be extrapolated.
- **"RX % at soak end = 80.7 %, Full RX? NO" is conservative:** it is the isothermal 415 °C value only. The
  10 min overshoot at 450 °C before the soak and the ramps are not credited. With the same model, 10 min at
  450 °C alone gives ≈ 60 % RX (t₀.₅(450 °C) ≈ 8.5 min) *(recalc.)*. A non-isothermal additivity (Scheil)
  integration over the whole T(t) path should be used.
- **Composition inconsistency:** title says 0.2 % Mn (and `mg_dashboard` calls the alloy AlMn0.2) but the table
  says Mn 0.3. Mg 0.12 % — EN AW-3102 does not list Mg explicitly, so Mg would normally fall under
  "others ≤ 0.05" *(ext., verify)*; the "≤0.15" spec in this sheet needs a source.
- **Zener limit (27 µm) vs predicted grain size (43–114 µm):** not a contradiction per se — a Zener limit caps
  *grain growth*, not the RX grain size set by nucleation density; RX grains larger than D_lim simply will not
  grow. But "Al₆Mn r ≈ 0.2 µm, Fv ≈ 0.01" implies almost all Mn precipitated as dispersoids, which is
  unrealistic with Fe 0.35 % (much Mn is bound in constituents) — a measured dispersoid Fv/r would help.
- **Cu treatment conflicts with the AA3207 model (§4):** here Cu *accelerates* RX (stored energy), there Cu is a
  potent *retarder* (solute drag). At 0.09 % in a commercial alloy the net effect is small either way.
- **Implied Hall–Petch slope** (37.4 HB·µm^½) is on the high side of literature values for Al
  (k_y ≈ 0.04–0.07 MPa·m^½) *(ext.)*; hardness differences attributed to grain size should be checked by
  measurement.
- **Grain-growth onset ~450 °C** coincides with the 450 °C overshoot step — worth checking grain size on parts
  that see the overshoot longest.

---

## 3. mg_dashboard.xlsx — Annealing cycle dashboard, EN AW 3102 (AlMn0.2): MgO & RX optimisation (found by search)

**Purpose:** compare real plant annealing cycles (batch furnace, furnaces A and B, trial A1) with proposed
cycles (A2 variants) for MgO surface-oxide growth and recrystallisation. Sheets: `Dashboard`,
`MgO Growth Curves`, `JMAK Recrystallization`, `New Cycle Evaluator`, `A2 AO-45 Cycle`, `Risk Scoring`.
The three versions have identical text, except that the 14:43 version has evaluator input "Cold reduction (%) = 45"
(outputs unchanged); the 14:46 version is smaller (31 kB vs 45 kB; possibly without charts — not verifiable).

### 3.1 KPI table — all cycles

| Metric | Unit | Cycle 1 (Batch) | Cycle 2 (Furn. A) | Cycle 3 (Furn. B) | C3 Improved | A1 Test (Actual) | A2 Optimized (370°C Eq.) | A2 AO (25%CR/415°C) | A2 AO-45 (45%CR/400°C) |
|---|---|---|---|---|---|---|---|---|---|
| Peak / Soak T | °C | ~455 | ~435 | ~435 | 432 | 430 | 432 | 415 | 400 |
| Time at ≥400°C | min | ~45 | ~190 | ~190 | ~130 | ~110 | ~70 | ~83 | ~50 |
| Soak time at peak | min | ~25 | ~150 | ~150 | ~70 | 60 | 40 | 75 | 50 |
| Total cycle time | min | ~270 | ~300 | ~330 | ~250 | 220 | ~225 | ~413 | ~345 |
| MgO oxide (Zayan) | nm | 10.6 | — | 12.1 | — | 9.1 | 10.0 | 8.6 | 7.1 |
| MgO Risk Score | 1–5 | 2.25 | 4.00 | 3.95 | 2.75 | 2.90 | ~2.1 | — | — |
| Sensor spread | °C | 5–10 | 10–20 | 5–10 | ≤5 | 15–20 | ≤5 | ≤5 | ≤5 |
| Cold reduction | % | — | — | — | — | — | 25 | 25 | 45 |
| Recryst. achieved? | — | Yes | Yes | Yes | Yes | Partial | Yes | Yes | Yes |
| Est. grain size | µm | — | — | — | — | — | — | 50–100 | 20–40 |
| Equalization step? | — | No | No | No | No | No | Yes | Yes | Yes |
| MgO Rank | # | 4 | — | 5 (worst) | — | 3 | 3 | 2 | 1 (BEST) |

MgO oxide thickness comparison (Zayan diffusion model, nm): Cycle 1 Batch 10.59; Cycle 3 Original 12.06;
A1 Test 9.14; A2 Optim. (432°C) 10.01; A2 AO (415°C) 8.58; A2 AO-45 (400°C) 7.12.

Verdict & recommendations (verbatim):
- BEST for lowest MgO: "A2 AO-45 (45% CR at 400°C) — 7.1 nm total oxide, stays at MgO transition boundary"
- BEST for 25% CR: "A2 AO (415°C soak, 75 min) — 8.6 nm, full RX with 370°C equalization"
- A1 test lesson: "Shorter soak (60 min) works, but impact temperature REQUIRED for uniformity (T8 problem)"
- Key principle: "TIME AT TEMPERATURE is the #1 MgO driver — reduce soak time, not just lower temperature"
- Next step: "A2 test with 370°C equalization + 450°C impact — expected MgO score ~2.05–2.25"

### 3.2 Cumulative MgO oxide thickness (Zayan diffusion model), nm

| Time (min) | A2 Optim. | A1 Test | Cycle 3 Original | Cycle 1 Batch | A2 AO 25%CR | A2 AO-45 45%CR |
|---|---|---|---|---|---|---|
| 0 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 |
| 80 | 0.10 | 0.10 | 0.10 | 0.10 | 0.10 | 0.10 |
| 120 | 3.41 | 3.41 | 3.41 | 0.10 | 3.41 | 3.41 |
| 150 | 6.26 | 3.41 | 3.41 | 0.10 | 6.26 | 5.96 |
| 170 | 7.33 | 5.14 | 5.32 | 0.10 | 6.56 | 6.26 |
| 180 | 8.20 | 5.14 | 5.32 | 3.40 | 6.69 | 6.26 |
| 200 | 8.20 | 8.34 | 5.32 | 7.29 | 8.18 | 6.82 |
| 225 | 9.61 | 8.34 | 11.66 | 7.29 | 8.18 | 6.82 |
| 250 | 9.91 | 9.04 | 11.66 | 7.75 | 8.48 | 7.02 |
| 300 | 10.01 | 9.14 | 11.96 | 10.59 | 8.58 | 7.12 |
| 350 | 10.01 | 9.14 | 11.96 | 10.59 | 8.58 | 7.12 |
| 400 | 10.01 | 9.14 | 12.06 | 10.59 | 8.58 | 7.12 |
| 450 | 10.01 | 9.14 | 12.06 | 10.59 | 8.58 | 7.12 |
| 500 | 10.01 | 9.14 | 12.06 | 10.59 | 8.58 | 7.12 |

### 3.3 JMAK model parameters by cold reduction

| Parameter | Unit | 25% CR | 33% CR | 41% CR | 45% CR | 50% CR | Basis |
|---|---|---|---|---|---|---|---|
| Avrami exponent n | — | 2 | 2.1 | 2.2 | 2.3 | 2.5 | Higher CR → more uniform nucleation |
| Activation energy Q_rx | kJ/mol | 200 | 192 | 185 | 180 | 170 | Higher CR → more stored energy → lower barrier |
| t₀.₅ at 430°C | min | 20 | 12 | 7 | 5 | 3 | Half-time drops exponentially with CR |
| Stored energy (est.) | J/mol | ~50 | ~85 | ~130 | ~160 | ~200 | Non-linear with CR (Taylor hardening) |
| Expected RX onset | °C | 300–350 | 280–330 | 260–310 | 250–300 | 240–290 | Higher stored energy → lower onset T |
| Expected grain size | µm | 50–100 | 35–70 | 25–50 | 20–40 | 15–30 | More nuclei → finer grains |

Same JMAK form as §2.2 (X = 1 − exp[−ln2·(t/t₀.₅)ⁿ], Arrhenius from 430 °C); verified for 25 % CR, 415 °C:
t₀.₅ = 42.2 min, t₉₉ = 108.7 min, X(75 min) = 88.8 % *(recalc.)*.

Time for 99 % RX (min):

| Soak T (°C) | 25% CR | 33% CR | 41% CR | 45% CR | 50% CR | MgO Risk | Assessment (sheet) |
|---|---|---|---|---|---|---|---|
| 350 | 4165.7 | 2004.3 | 962.3 | 593.3 | 267.6 | Negligible | Only viable ≥45%CR |
| 370 | 1254.1 | 633.1 | 317.0 | 201.4 | 96.4 | Low (LOG) | Equalization T, partial RX at 25%CR |
| 390 | 405.9 | 214.4 | 111.7 | 73.0 | 37.0 | Transition | Below 400°C, slow for 25%CR |
| 400 | 236.8 | 127.8 | 67.8 | 44.9 | 23.4 | Moderate | At MgO transition, still slow 25%CR |
| 415 | 108.7 | 60.5 | 33.0 | 22.3 | 12.1 | Moderate | OPTIMAL for 25%CR 3102 |
| 430 | 51.6 | 29.6 | 16.6 | 11.4 | 6.4 | High | Fast RX, more MgO |
| 450 | 20.0 | 11.9 | 6.9 | 4.9 | 2.9 | Very high | Unnecessary. Excessive MgO. |

RX % vs time at 415 °C:

| Time (min) | 25% CR | 33% CR | 41% CR | 45% CR | 50% CR |
|---|---|---|---|---|---|
| 0 | 0.0 | 0.0 | 0.0 | 0.0 | 0.0 |
| 5 | 1.0 | 2.4 | 7.0 | 13.8 | 39.9 |
| 10 | 3.8 | 10.0 | 28.3 | 51.8 | 94.4 |
| 15 | 8.4 | 21.8 | 55.6 | 84.3 | 100.0 |
| 20 | 14.4 | 36.3 | 78.4 | 97.2 | 100.0 |
| 30 | 29.6 | 65.2 | 97.6 | 100.0 | 100.0 |
| 45 | 54.6 | 91.6 | 100.0 | 100.0 | 100.0 |
| 60 | 75.4 | 98.9 | 100.0 | 100.0 | 100.0 |
| 75 | 88.8 | 99.9 | 100.0 | 100.0 | 100.0 |
| 90 | 95.8 | 100.0 | 100.0 | 100.0 | 100.0 |
| 105 | 98.6 | 100.0 | 100.0 | 100.0 | 100.0 |
| 120 | 99.6 | 100.0 | 100.0 | 100.0 | 100.0 |

### 3.4 New-cycle evaluator (same inputs as §2.6)
Inputs: Cycle name NEW CYCLE; Cold reduction 25 % (45 % in the 14:43 version), "Range: 15–60%";
Equalization temperature 370 °C ("Must stay <400°C (LOG MgO regime)"); Equalization hold 30 min ("Until all
sensors ≤5°C spread"); Ramp to soak 2.5 °C/min; Impact/overshoot 450 °C; Impact hold 10 min; Soak 415 °C;
Soak time 75 min; Cooling rate 2 °C/min.

| Output metric | Value | Unit | Formula / logic (sheet text) |
|---|---|---|---|
| Ramp time (ambient → eq. T) | 98.6 | min | Assumes 25°C start, 3.5°C/min average ramp |
| Ramp time (eq. T → soak T) | 32.0 | min | If impact: to impact T. Else: to soak T |
| Time above 400°C (est.) | 105.0 | min | Ramp through >400°C + impact hold + soak |
| Total cycle time (est.) | 353.1 | min | All phases: ramp + equalize + impact + soak + cool to 200°C |
| MgO risk zone | HIGH — >100 min above 400°C | — | Based on estimated time above 400°C |
| Soak T vs 400°C margin | 15 | °C | Higher = more parabolic MgO growth |

Benchmark cycles:

| Cycle | Soak T (°C) | Soak (min) | Time >400°C | MgO (nm) | MgO Rank |
|---|---|---|---|---|---|
| A2 AO-45 (45%CR/400°C) | 400 | 50 | ~50 | 7.1 | 1 |
| A2 AO (25%CR/415°C) | 415 | 75 | ~83 | 8.6 | 2 |
| A1 Test (430°C) | 430 | 60 | ~110 | 9.1 | 3 |
| A2 Optimized (432°C) | 432 | 40 | ~70 | 10 | 4 |
| Cycle 1 Batch (455°C) | 455 | 25 | ~60 | 10.6 | 5 |
| Cycle 3 Original (435°C) | 435 | 150 | ~195 | 12.1 | 6 |

### 3.5 Proposed cycle A2 AO-45 (45 % CR at 400 °C, "lowest MgO achievable")

| Parameter | A2 AO-45 (45%CR) | A2 AO (25%CR) | Improvement |
|---|---|---|---|
| Soak temperature | 400°C | 415°C | 15°C lower → at MgO transition boundary |
| Soak time for 99% RX | ~38 min | ~90 min | 2.4× faster recrystallization |
| Recommended soak | 50–60 min | 75–90 min | 25–30 min shorter |
| Time above 400°C | ~50–60 min | ~83 min | ~30–40% less parabolic MgO |
| Expected MgO oxide | ~7.1 nm | ~8.6 nm | ~17% less MgO |
| Expected grain size | 20–40 µm | 50–100 µm | Finer grains → higher hardness |
| Expected hardness | 29–33 HB | 26–28 HB | +3–5 HB (Hall-Petch) |

| Phase | Duration | T start (°C) | T end (°C) | Rate (°C/min) | MgO Risk | Process notes |
|---|---|---|---|---|---|---|
| 1. LOAD & START | — | Ambient | ~30 | — | No risk | Spaced stacking. Close doors. |
| 2. RAMP to 300°C | ~80 min | ~30 | 300 | ~3–4 | Al₂O₃ only | Recovery >200°C. Through Mn precip zone. |
| 3. RAMP 300→370°C | ~40 min | 300 | 370 | ~2 | MgO LOG | RX nucleation active at 45%CR. |
| 4. EQUALIZE 370°C | 20–30 min | 370 | 370 | 0 | LOG safe | HOLD until ≤5°C spread. |
| 5. RAMP 370→400°C | ~15 min | 370 | 400 | ~2 | Transition | All zones uniform → rise together. |
| 6. SOAK at 400°C | 50 min | 400 | 400 | 0 | Para. START | 99%RX in ~38 min + margin. |
| 7. COOL-DOWN | ~2–3 hr | 400 | <200 | ~1–3 | Negligible | Natural cooling. MgO nil <350°C. |
| 8. UNLOAD | — | <200 | Ambient | — | Complete | Confirm <200°C. |

### 3.6 MgO risk scoring (weighted, 1 = low, 5 = high)

| Risk factor | Weight | Cycle 1 (Batch) | Cycle 3 (Original) | C3 Improved | A1 Test | A2 Optim. (370°C Eq) | A2 AO-45 (45%CR) |
|---|---|---|---|---|---|---|---|
| Peak temperature | 0.30 | 4 | 3 | 3 | 3 | 3 | 2 |
| Time at ≥400°C (critical!) | 0.35 | 1 | 5 | 3 | 3 | 2 | 1 |
| Soak duration at peak | 0.15 | 1 | 5 | 2 | 2 | 2 | 2 |
| Cooling rate | 0.15 | 3 | 3 | 3 | 3 | 3 | 3 |
| Temperature uniformity | 0.05 | 2 | 2 | 1 | 4 | 1 | 1 |
| WEIGHTED RISK SCORE | 1 | 2.25 | 3.95 | 2.75 | 2.90 | 2.40 | 1.75 |
| RANK (1=Best) | | #3 | #6 (worst) | #4 | #5 | #2 | #1 (BEST) |

Scoring notes: weights adjustable; time ≥400 °C weighted highest as "#1 MgO growth driver"; cooling identical
(~1–3 °C/min, thermal-mass limited); "All scores assume no protective atmosphere (N₂/Ar). Inert gas reduces risk
for all cycles."

### Assessment
- **This is the only file with real plant observations** (Cycles 1–3, A1 test): RX achieved at ~455 °C/~25 min
  soak, ~435 °C/~150 min, 432 °C/~70 min; **partial RX at 430 °C/60 min** (A1, sensor spread 15–20 °C). CR of
  the plant cycles is not recorded ("—"). These are the natural calibration points for every model in §2–§4.
- **Model-version drift:** the dashboard uses n = 2.0 at 25 % CR, t₀.₅(430 °C) = 20 min; the later
  `3102_RX_simulation` uses n = 1.8, 22 min. Hence "A2 AO full RX" here (88.8 % at 75 min isothermal, t₉₉ 108.7
  min) versus "Full RX? NO" (80.7 %) there. Neither credits the 450 °C overshoot (see §2 Assessment).
- **Small internal inconsistencies:** A2 Optimized risk score "~2.1" (KPI) vs 2.40 (scoring sheet); Cycle 1 time
  ≥400 °C ~45 (KPI) vs ~60 (benchmark table); Cycle 3 ~190 vs ~195; A1 and A2 Optim. both "rank 3" in the KPI
  table, 3 and 4 in the benchmark table.
- **Stored energy ~50–200 J/mol** looks high: typical estimates for cold-rolled Al alloys are of order 1 MPa
  (≈10 J/mol) *(ext., verify)*; it is labelled "est." and does not enter the kinetics.
- **Hardness gain +3–5 HB from 50–100 → 20–40 µm** is larger than a typical Al Hall–Petch slope would give
  (order 1–2 HB) *(ext.)*; the 26–28 HB / 29–33 HB targets also differ from `3102_RX_simulation`
  (23.9 HB at 80 µm, 24.8 HB at 53 µm). Needs measured HB vs grain size.
- **Heating-rate trade-off:** the A2 schedule ramps slowly through 300–370 °C and holds 20–30 min at 370 °C
  (for furnace uniformity and MgO), while the user's own notes say "avoid prolonged holds 270–350 °C" and the
  CRM tables (§5) say Mn alloys need *fast* heating to avoid concurrent Mn precipitation before RX. For 0.2–0.3 % Mn
  the effect is "mild" (§5), but for the modified 3102 (1.1–1.3 % Mn) the same schedule would be risky.
- **MgO model:** the "Zayan diffusion model" is cited without reference or parameters; outputs are step-wise
  cumulative values. A log-to-parabolic transition near 400 °C is plausible for Al-Mg surface oxidation, but the
  model should be validated against measured oxide (e.g. XPS/GDOES depth profiles) and the reason MgO matters
  (lacquer adhesion? discolouration? lubricant behaviour?) should be recorded.

---

## 4. AA3207_Recrystallization_Simulation.xlsx — physically-based JMAK model for AA3207 (4 versions)

**Purpose:** "Physically-based JMAK model with solute drag, Zener pinning, PSN" for AA3207 after cold rolling;
outputs RX kinetics, T_rx vs reduction, RX grain size, hardness softening curves, phases/texture, sensitivity.
Sheets: `Alloy & Parameters`, `JMAK Kinetics`, `RX Temperature`, `Grain Size`, `Hardness & Softening`,
`Microstructure`, `Sensitivity`, `Notes & References` ("VERSION 1.0 | March 2026"). Latest version (16:26) documented in full.

### 4.1 Alloy composition (all versions)

| Element | Content (wt%) | Role in Recrystallization |
|---|---|---|
| Mn | 0.45 | Dispersoid former, Zener pinning |
| Mg | 0.15 | Solid solution, solute drag on GB |
| Cu | 0.09 | Solute drag, raises Q_rx |
| Fe | 0.35 | Constituent particles, PSN sites |
| Si | 0.15 | Dispersoid/constituent formation |
| Zn | 0.01 | Minor SS effect |
| Ti | 0.015 | Grain refiner (TiB2/Al3Ti) |
| Al | 98.785 | Balance (matrix) |

### 4.2 Process parameters (latest, 16:26)

| Parameter | Value | Unit | Notes |
|---|---|---|---|
| Cold rolling reduction (%) | 45 | % | Typical 30-95% |
| Hot band grain size (um) | 60 | um | After hot rolling + RX |
| Hot band thickness (mm) | 9.5 | mm | Entry gauge |
| Final gauge (mm) | 5.225 | mm | Calculated |
| True strain | 0.597837001 | - | Calculated |
| Dispersoid size (nm) | 80 | nm | After coarsening during hot rolling/anneal |
| Dispersoid volume fraction Fv | 0.006 | - | Lower Mn → fewer dispersoids than AA3004 |
| Constituent particle size (um) | 3 | um | Al6(FeMn) |
| Constituent particle Fv | 0.015 | - | Large particles |
| Heating rate (C/min) | 50 | C/min | To anneal temperature |

### 4.3 Physical & kinetic constants (latest, 16:26)

| Parameter | Value | Unit | Source / Notes |
|---|---|---|---|
| Base activation energy Q0 (pure Al) | 100 | kJ/mol | Commercial Al base (not zone-refined) |
| dQ per wt% Mg (solute drag) | 100 | kJ/mol/wt% | Frois & Dimitrov 1966 (moderate drag) |
| dQ per wt% Cu (solute drag) | 200 | kJ/mol/wt% | Calibrated for commercial alloy (not ultra-pure) |
| dQ per wt% Mn (in solution) | 80 | kJ/mol/wt% | Mn in solid solution retards GB migration |
| Effective Q_rx | 145 | kJ/mol | Calculated |
| Gas constant R | 8.314 | J/(mol*K) | Universal constant |
| JMAK exponent n (site saturated) | 3 | - | Table 7.3 Humphreys & Hatherly |
| Boundary energy gamma_gb | 0.324 | J/m2 | Typical Al high-angle GB |
| Pre-exponential B0 | 2.5E+28 | s^-n | Calibrated: t50~300s at 350°C, 70% CR |
| Mn in solid solution (wt%) | 0.15 | wt% | Remainder as dispersoids |
| Zener pinning pressure Pz (MPa) | 0.03645 | MPa | Calculated |
| Strain exponent m (JMAK sheet) | 2 | — | |

### 4.4 Model equations (stated in the workbook; all verified by recalculation)
1. JMAK: X_v = 1 − exp(−B·tⁿ), n = 3 ("site-saturated 3D nucleation")
2. Arrhenius/strain: B = B0·exp(−n·Q/(R·T))·ε^(n·m)  ⇒ t₅₀ = (ln2/B)^(1/n) ∝ ε^(−m)·exp(Q/RT)
3. Solute drag: Q_eff = Q0 + Σ dQ_i·C_i (Mg, Cu, Mn in solution) → 100 + 100·0.15 + 200·0.09 + 80·0.15 = 145 kJ/mol ✓
4. Zener: P_z = 3·F_v·γ_gb/(2r) → 3·0.006·0.324/(2·80 nm) = 0.03645 MPa ✓; d_max = 4r/(3F_v) → 17.8 µm ✓
5. True strain ε = ln(h0/h); final gauge = h0·(1 − CR): 9.5·0.55 = 5.225 mm, ε = 0.5978 ✓
6. T_rx (50 % in 1 h): T = n·Q / {R·ln[B0·ε^(n·m)·tⁿ/ln2]}, t = 3600 s ✓
7. RX grain size: d_rx = A·ε^(−p)·exp(−Q_d/(R·T)), capped by the Zener limit; A = 800 µm, p = 1, Q_d = 20 kJ/mol ✓
8. Hardness: H(t) = H_rec·(1 − X_v) + H_rx·X_v; H_def = H0 + k·ε^0.5; H_rec = H_def − f_rec·(H_def − H_ann)
   → 35 + 55·√0.5978 = 77.5 HV; 77.5 − 0.15·(77.5 − 38) = 71.6 HV ✓
9. Texture: "Cube vs PSN competition depends on dispersoid/particle balance" (tabulated, not computed — see below)

Adjustable inputs noted in the sheet: composition (Sheet 1 rows 6-12), CR (B17), dispersoids (B22-B23),
kinetic constants (rows 30-39), hardness (Sheet 5 rows 4-9). References listed: Humphreys & Hatherly 2nd ed.
(Ch. 5, 7, 9, 12, 15, 16); ASM Handbook of Aluminium Pt.1; Vandermeer & Gordon (1962); Frois & Dimitrov (1966);
Gordon & Vandermeer (1966).

### 4.5 Results — fraction recrystallised X_v(t,T), 45 % CR (ε = 0.5978), latest version

| Time (s) | Time (min) | 250 C | 275 C | 300 C | 325 C | 350 C | 375 C | 400 C | 425 C | 450 C |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 0.0 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 |
| 2 | 0.0 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0003 |
| 5 | 0.1 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0004 | 0.0054 |
| 10 | 0.2 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0002 | 0.0032 | 0.0423 |
| 20 | 0.3 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0001 | 0.0016 | 0.0256 | 0.2921 |
| 50 | 0.8 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0012 | 0.0247 | 0.3328 | 0.9955 |
| 100 | 1.7 | 0.0000 | 0.0000 | 0.0000 | 0.0000 | 0.0004 | 0.0099 | 0.1814 | 0.9607 | 1.0000 |
| 200 | 3.3 | 0.0000 | 0.0000 | 0.0000 | 0.0001 | 0.0031 | 0.0768 | 0.7984 | 1.0000 | 1.0000 |
| 500 | 8.3 | 0.0000 | 0.0000 | 0.0000 | 0.0015 | 0.0478 | 0.7130 | 1.0000 | 1.0000 | 1.0000 |
| 1000 | 16.7 | 0.0000 | 0.0000 | 0.0003 | 0.0116 | 0.3240 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 2000 | 33.3 | 0.0000 | 0.0000 | 0.0021 | 0.0895 | 0.9564 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 5000 | 83.3 | 0.0000 | 0.0005 | 0.0317 | 0.7688 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 10000 | 166.7 | 0.0000 | 0.0040 | 0.2275 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 20000 | 333.3 | 0.0003 | 0.0316 | 0.8732 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 50000 | 833.3 | 0.0052 | 0.3946 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 100000 | 1666.7 | 0.0411 | 0.9820 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 200000 | 3333.3 | 0.2851 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 500000 | 8333.3 | 0.9947 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 1000000 | 16666.7 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| 2000000 | 33333.3 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| **t50 (s)** | | 254,710 | 55,683 | 13,900 | 3,896 | 1,210 | 411 | 151 | 60 | 25 |
| **t50 (min)** | | 4,245.2 | 928.1 | 231.7 | 64.9 | 20.2 | 6.8 | 2.5 | 1.0 | 0.4 |

### 4.6 Results — T_rx (50 % RX in 1 h) vs reduction, and effect of Mg (at 70 % reduction)

| Reduction (%) | True strain | T_rx (C) | T_rx (K) |
|---|---|---|---|
| 20% | 0.223 | 370.2 | 643.4 |
| 25% | 0.288 | 358.4 | 631.6 |
| 30% | 0.357 | 348.7 | 621.9 |
| 35% | 0.431 | 340.5 | 613.6 |
| 40% | 0.511 | 333.2 | 606.3 |
| 45% | 0.598 | 326.6 | 599.8 |
| 50% | 0.693 | 320.6 | 593.7 |
| 55% | 0.799 | 314.9 | 588.1 |
| 60% | 0.916 | 309.5 | 582.7 |
| 65% | 1.050 | 304.3 | 577.4 |
| 70% | 1.204 | 299.1 | 572.2 |
| 75% | 1.386 | 293.8 | 567.0 |
| 80% | 1.609 | 288.4 | 561.5 |
| 85% | 1.897 | 282.5 | 555.6 |
| 90% | 2.303 | 275.7 | 548.9 |
| 95% | 2.996 | 266.8 | 539.9 |

| Mg (wt%) | Q_eff (kJ/mol) | T_rx (C) |
|---|---|---|
| 0 | 130.0 | 239.9 |
| 0.05 | 135.0 | 259.6 |
| 0.1 | 140.0 | 279.3 |
| 0.15 | 145.0 | 299.1 |
| 0.2 | 150.0 | 318.8 |
| 0.3 | 160.0 | 358.3 |
| 0.5 | 180.0 | 437.2 |

### 4.7 Results — predicted RX grain size (µm), Zener limit 17.8 µm

| Reduction (%) | True strain | 300 C | 325 C | 350 C | 375 C | 400 C | 425 C | 450 C |
|---|---|---|---|---|---|---|---|---|
| 30% | 0.357 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 |
| 40% | 0.511 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 |
| 50% | 0.693 | 17.4 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 |
| 60% | 0.916 | 13.1 | 15.6 | 17.8 | 17.8 | 17.8 | 17.8 | 17.8 |
| 70% | 1.204 | 10.0 | 11.9 | 14.0 | 16.2 | 17.8 | 17.8 | 17.8 |
| 80% | 1.609 | 7.5 | 8.9 | 10.5 | 12.1 | 13.9 | 15.8 | 17.8 |
| 90% | 2.303 | 5.2 | 6.2 | 7.3 | 8.5 | 9.7 | 11.1 | 12.5 |
| 95% | 2.996 | 4.0 | 4.8 | 5.6 | 6.5 | 7.5 | 8.5 | 9.6 |

### 4.8 Results — hardness (HV) vs time, 45 % CR
Parameters: H_annealed 38 HV; H_deformed base (0 %) 35 HV; work-hardening coeff k 55; WH exponent 0.5;
H_deformed at current reduction 77.5 HV; recovery fraction 0.15; H after recovery 71.6 HV.

| Time (s) | Time (min) | HV@300C | HV@325C | HV@350C | HV@375C | HV@400C |
|---|---|---|---|---|---|---|
| 1 | 0.0 | 71.6 | 71.6 | 71.6 | 71.6 | 71.6 |
| 10 | 0.2 | 71.6 | 71.6 | 71.6 | 71.6 | 71.6 |
| 30 | 0.5 | 71.6 | 71.6 | 71.6 | 71.6 | 71.4 |
| 60 | 1.0 | 71.6 | 71.6 | 71.6 | 71.5 | 70.2 |
| 120 | 2.0 | 71.6 | 71.6 | 71.6 | 71.0 | 61.8 |
| 300 | 5.0 | 71.6 | 71.6 | 71.2 | 63.7 | 38.2 |
| 600 | 10.0 | 71.6 | 71.5 | 68.9 | 41.9 | 38.0 |
| 1200 | 20.0 | 71.6 | 70.9 | 55.1 | 38.0 | 38.0 |
| 1800 | 30.0 | 71.5 | 69.4 | 41.4 | 38.0 | 38.0 |
| 3600 | 60.0 | 71.2 | 57.4 | 38.0 | 38.0 | 38.0 |
| 7200 | 120.0 | 68.5 | 38.4 | 38.0 | 38.0 | 38.0 |
| 14400 | 240.0 | 53.5 | 38.0 | 38.0 | 38.0 | 38.0 |
| 28800 | 480.0 | 38.1 | 38.0 | 38.0 | 38.0 | 38.0 |
| 57600 | 960.0 | 38.0 | 38.0 | 38.0 | 38.0 | 38.0 |
| 86400 | 1440.0 | 38.0 | 38.0 | 38.0 | 38.0 | 38.0 |

### 4.9 Microstructure sheet

Predicted phases & precipitates:

| Phase | Formula | Size | Fv | Effect on RX | Nucleation |
|---|---|---|---|---|---|
| alpha-dispersoids | Al15(FeMn)3Si2 | 20-100 nm | 0.0060 | Zener pinning | Inhibit PSN, promote Cube |
| Constituent | Al6(FeMn) | 1-10 um | 0.0150 | PSN random nuclei | Particle Stimulated Nucleation |
| Mg2Si | Mg2Si | 0.1-2 um | 0.0012 | Dissolves >350C | Pin or stimulate |
| Al2Cu trace | Al2Cu/GPB | nm | 0.0005 | Solute drag | Slows RX front |
| Matrix | FCC Al+ss | - | 0.9774 | Recovery | - |

RX texture vs annealing temperature ("Cube vs PSN competition: dispersoids suppress PSN -> Cube strengthens at high T"):

| T (C) | Cube {001}<100> | S {123}<634> | Brass {011}<211> | R/Goss | PSN Random | Other |
|---|---|---|---|---|---|---|
| 250 | 5% | 25% | 20% | 10% | 15% | 25% |
| 275 | 8% | 22% | 18% | 10% | 17% | 25% |
| 300 | 15% | 18% | 12% | 8% | 22% | 25% |
| 325 | 22% | 12% | 8% | 6% | 27% | 25% |
| 350 | 30% | 8% | 5% | 5% | 30% | 22% |
| 375 | 38% | 5% | 3% | 4% | 28% | 22% |
| 400 | 42% | 4% | 2% | 3% | 25% | 24% |
| 425 | 45% | 3% | 2% | 2% | 22% | 26% |
| 450 | 48% | 2% | 1% | 2% | 20% | 27% |
| 475 | 50% | 2% | 1% | 1% | 18% | 28% |
| 500 | 52% | 1% | 1% | 1% | 15% | 30% |

Solute effects summary:

| Solute | wt% | In solution | Effect T_rx | Effect grain | Mechanism |
|---|---|---|---|---|---|
| Mn | 0.45 | 0.15 | Up moderate | Down via Zener | Dispersoids + weak drag |
| Mg | 0.15 | 0.15 | Up strong | Up slightly | Strong solute drag on GB |
| Cu | 0.09 | 0.09 | Up very strong/at% | Minimal | Potent drag, +60kJ/0.007at% |
| Fe | 0.35 | 0.01 | Up if in ss | Down via PSN | Constituent particles -> PSN |
| Si | 0.15 | 0.05 | Moderate | Down via dispersoids | Co-precipitates as dispersoids |

### 4.10 Sensitivity (latest version; computed at 70 % CR)

Effect of Mg on t50 (s):

| Mg (wt%) | t50@300C | t50@325C | t50@350C | t50@375C | t50@400C |
|---|---|---|---|---|---|
| 0 | 147 | 47 | 16 | 6 | 3 |
| 0.05 | 420 | 129 | 43 | 16 | 6 |
| 0.1 | 1,200 | 352 | 114 | 40 | 15 |
| 0.15 | 3,427 | 961 | 298 | 101 | 37 |
| 0.2 | 9,786 | 2,626 | 783 | 256 | 91 |
| 0.25 | 27,945 | 7,176 | 2,055 | 648 | 223 |
| 0.3 | 79,801 | 19,612 | 5,395 | 1,639 | 544 |
| 0.4 | 650,730 | 146,499 | 37,173 | 10,485 | 3,249 |
| 0.5 | 5,306,332 | 1,094,297 | 256,148 | 67,065 | 19,397 |

Effect of reduction on t50 at 350 °C:

| Reduction | eps | t50 (s) | t50 (min) |
|---|---|---|---|
| 20% | 0.223 | 8,683 | 144.7 |
| 30% | 0.357 | 3,398 | 56.6 |
| 40% | 0.511 | 1,657 | 27.6 |
| 50% | 0.693 | 900 | 15.0 |
| 60% | 0.916 | 515 | 8.6 |
| 70% | 1.204 | 298 | 5.0 |
| 75% | 1.386 | 225 | 3.7 |
| 80% | 1.609 | 167 | 2.8 |
| 85% | 1.897 | 120 | 2.0 |
| 90% | 2.303 | 82 | 1.4 |
| 95% | 2.996 | 48 | 0.8 |

### 4.11 Version differences

| Version (UTC) | CR / gauge | ε | Dispersoid r, Fv | Q0; dQ Mg/Cu/Mn | Q_eff | B0 | Pz; Zener d | Grain A | Hardness H0/k → H_def/H_rec | Outcome |
|---|---|---|---|---|---|---|---|---|---|---|
| 16:15 (1jw-…) | 45 %; 9 → 4.95 mm | 0.5978 | 50 nm, 0.012 ("alpha-Al15Mn3Si2", "From homogenization") | 140 (Vandermeer & Gordon 1962); 80 / 667 (Vandermeer & Gordon 1963) / 40 | 218.03 | 1.5E+20 ("Fitted to Al-Mn alloy data") | 0.11664 MPa; 5.6 µm | 2500 µm | 30/85 → 95.7/87.1 | **Unphysical:** X_v = 0 everywhere up to 2·10⁶ s; t50 = 2.6·10⁹ s (450 °C) to 2.7·10¹⁵ s (250 °C); T_rx = 735.8–987.8 °C; grain 5.6 µm everywhere |
| 16:17 (1QH-…) | 70 %; 3 → 0.9 mm | 1.2040 | as 16:15 | as 16:15 | 218.03 | 1.5E+20 | as 16:15 | 2500 | 30/85 → 123.3/110.5 | Same unphysical result (t50 6.45·10⁸–6.77·10¹⁴ s) |
| 16:23 (1t2c…) | 70 %; 3 → 0.9 mm | 1.2040 | 80 nm, 0.006 | 100; 100 / 200 / 80 | 145 | 2.5E+28 (calibrated t50 ~300 s @350 °C, 70 % CR) | 0.03645 MPa; 17.8 µm | 800 | 35/55 → 95.3/86.7 | Recalibrated. t50 (s): 62,803 @250; 13,730 @275; 3,427 @300; 961 @325; 298 @350; 101 @375; 37 @400; 15 @425; 6 @450 |
| 16:26 (1L9M…) | 45 %; 9.5 → 5.225 mm | 0.5978 | 80 nm, 0.006 | 100; 100 / 200 / 80 | 145 | 2.5E+28 | 0.03645 MPa; 17.8 µm | 800 | 35/55 → 77.5/71.6 | As documented above (t50 1,210 s @350 °C) |

T_rx, Mg-sensitivity and reduction tables are always evaluated at 70 % CR and therefore identical between
16:23 and 16:26 (and between 16:15 and 16:17).

### Assessment
- **Arithmetic is correct and self-consistent** (Q_eff, P_z, d_max, ε, t50, T_rx, d_rx and hardness all reproduce
  *(recalc.)*). The 16:15/16:17 versions were broken by importing ultra-pure-Al solute-drag data
  (dQ_Cu = 667 kJ/mol/wt%, Q0 = 140) — T_rx above the solidus. The 16:23/16:26 recalibration is the usable one.
- **Single calibration point.** B0 = 2.5E+28 s⁻³ is fixed by "t50 ~300 s at 350 °C, 70 % CR", source not stated.
  Everything else is extrapolation from that point.
- **n = 3 is too high for real cold-rolled Al alloys.** Measured Avrami exponents are typically 1–2 because
  nucleation is non-random and stored energy heterogeneous (Humphreys & Hatherly ch. 7) *(ext.)*. With n = 3 the
  5→95 % transition spans only ×3.9 in time versus ×9.6 for n = 1.8 *(recalc.)*. The user's 3102 models use
  n = 1.8–2.5, which is more realistic.
- **Linear "Q_eff = Q0 + ΣdQ·C" overstates solute effects.** At 100 kJ/mol per wt% Mg, every +0.1 % Mg
  multiplies t50 by ≈ 6.9 at 350 °C (table: 114 → 783 s) *(recalc.)*. Extrapolated, 1 % Mg alloys (3004/3104)
  or 5xxx alloys would effectively never recrystallise, which contradicts practice (they recrystallise readily at
  ~300–350 °C after cold rolling) *(ext.)*. Solute drag saturates, and Mg also *raises* stored energy. The CRM
  tables (§5) treat Mg as increasing stored energy (beneficial), which contradicts this model.
- **The dominant 3xxx mechanism is under-represented:** Mn in supersaturated solution and **concurrent
  precipitation during heating** (strongly heating-rate dependent) appear only as a fixed "0.15 wt% Mn in
  solution" Q increment. The heating-rate input (50 °C/min) does not appear to enter any isothermal table
  (formulas not visible). Recommended: non-isothermal additivity plus a precipitation state variable (Fv, r
  evolving during heating; P_z compared with the driving pressure for nucleation), as in ALSOFT-type models
  *(ext.)*.
- **Zener limit used as a cap on RX grain size is physically the wrong way round.** The Zener limit bounds
  *subsequent grain growth*; it does not reduce RX grains below their impingement size. Strong pinning normally
  makes RX grains **coarser** (fewer viable nuclei) and elongated — as the user's own CRM notes state for 3003.
  The cap also makes grain size insensitive to reduction ≤ 50 %, contradicting the CRM table logic.
- **d_rx increases with T** (Q_d = +20 kJ/mol). For Al-Mn with concurrent precipitation, faster/higher-T
  anneals often give *finer* grains because RX outruns precipitation — the sign should be validated.
- **Low-strain behaviour:** t50 ∝ ε⁻² with no critical strain. At 25 % CR this model gives t50(415 °C) ≈ 6 min,
  ~7× faster than `3102_RX_simulation` (46 min) for a *leaner* alloy and inconsistent with the plant A1 result
  (partial RX at 430 °C/60 min) *(recalc.)*. At the low CRs used for slugs (25–45 %) the AA3207 model is
  probably too fast.
- **Hardness inputs:** H_deformed at 0 % (35 HV) < H_annealed (38 HV) is inconsistent (they should coincide).
  38 HV for O-temper lean 3xxx is high compared with the user's own tables (3003-O HB 28; 3102 slugs 23–28 HB).
- **Texture table** is a fixed hand-entered table (identical in all four versions despite different Fv) — treat
  as illustrative. The microstructure table entries Al2Cu/GPB at 0.09 % Cu are unlikely (Cu stays in solution).
- **Composition:** Mg 0.15 % vs EN AW-3207 Mg ≤ 0.10 % and Mn 0.45 % within 0.40–0.8 % *(ext., verify against
  EN 573-3)*; confirm whether 0.15 Mg is a real cast analysis.

---

## 5. CRM (cold-rolling-mill) reduction tables for cold-extrusion slug strip

Files: `EN_AW_Master_CRM_Reduction_Tables.xlsx` (Summary + one sheet each for EN AW 1070, 1050, 3102, 3207, 3003)
and `EN_AW_3207_CRM_Reduction_Table.xlsx` (the 3207 sheet alone, with legend and notes).
Route: **"Starting strip: 22.0 mm → HRM → CRM → Full anneal → Cold extrusion"**.
**Not** a critical-raw-materials analysis.

### 5.1 Summary — alloy comparison, CRM targets for cold extrusion

| Alloy | Target CRM ε | CRM % | Anneal Temp | Grain Growth Risk | Heating Rate | Key Difference |
|---|---|---|---|---|---|---|
| EN AW 1070 | ≥ 0.95 | ≥ 61% | 280–320°C | HIGH — no pinning particles. Anneal temp is your only control. | Not critical (no Mn precipitation risk) | Very pure Al. High SFE → easy dynamic recovery → less stored energy at same strain. No dispersoids → grain growth is the main risk. Need high ε for maximum nucleation density to start with finest possible grain, because grains WILL coarsen during anneal. |
| EN AW 1050 | ≥ 0.90 | ≥ 59% | 300–340°C | HIGH — very few pinning particles. Fe/Si constituents help nucleation but not pinning. | Moderate (slight Fe-precipitation effect at 360°C) | Nearly pure Al but more Fe/Si than 1070 → some constituent particles for PSN, slightly lower grain growth risk. Still no Mn dispersoids → grain growth is main concern. Need high ε. |
| EN AW 3102 | ≥ 0.80 | ≥ 55% | 340–370°C | MODERATE — low Mn dispersoid population provides some Zener pinning. | Moderate — some Mn precipitation risk but mild | Low Mn content → mild dispersoid pinning. Behaves between 1xxx and 3207. Recrystallizes relatively easily. Some Zener pinning gives moderate grain growth control. Target ε can be slightly lower than 3207. |
| EN AW 3207 | ≥ 0.85 | ≥ 57% | 350–380°C | LOW — Mn dispersoids provide effective Zener pinning after recrystallization. | Reasonably fast — avoid slow heating which causes Mn precipitation before rx | Reference alloy. Moderate Mn → moderate dispersoid pinning during anneal. Mg increases stored energy. Good grain growth stability. ε ≥ 0.85 overcomes pinning and gives fine equiaxed grain. |
| EN AW 3003 | ≥ 0.95 | ≥ 61% | 370–400°C | VERY LOW — dense Mn dispersoid population provides strong Zener pinning. | FAST — critical! Slow heating causes heavy Mn precipitation before rx → coarse elongated grains | High Mn (1.0–1.5%) → strong dispersoid precipitation during anneal pins boundaries. Stored energy must overcome Zener pinning pressure (Pz). Need higher ε to ensure enough driving force. Slow heating is very dangerous — raises rx temperature by ~100°C. Fast heating + high ε is essential. |

Alloy headers in the per-alloy sheets: "EN AW 1070 — Al 99.7% (≤0.25% Fe, ≤0.20% Si)", anneal 280–320°C / 1–2h;
"EN AW 1050 — Al 99.5% (≤0.40% Fe, ≤0.25% Si)", 300–340°C / 1–2h; "EN AW 3102 — Al-Mn (≤0.40% Mn, ≤0.10% Cu)",
340–370°C / 1–2h; "EN AW 3207 — Al-Mn (≤0.60% Mn, 0.15% Mg, 0.09% Cu)", 350–380°C / 1–2h;
"EN AW 3003 — Al-Mn (1.0–1.5% Mn, 0.05–0.20% Cu)", 370–400°C / 1–3h. Extra alloy notes:
1070 "LOW temp critical — no dispersoids to limit grain growth. Avoid >340°C."; 1050 "Keep below 360°C — Fe in
solid solution can cause Fe-precipitation pinning at ~360°C, then grain growth above. Coarse FeAl₃/AlFeSi
particles provide some PSN."; 3102 "Less sensitive to heating rate than 3207/3003."; 3207 "Mg in solid solution
increases stored energy slightly (beneficial). Good balance of nucleation and pinning."; 3003 "Risk of partial rx
at low ε. May need higher temp or longer soak. Heating rate is CRITICAL."

### 5.2 Table logic (each alloy sheet: final thickness 2.0–10.0 mm in 0.1 mm steps, 81 rows)
- CRM reduction r = 1 − exp(−ε_target); HRM exit gauge = t_final/(1 − r), capped at 22.0 mm; HRM reduction and
  ε_HRM = ln(22.0/HRM exit). When the cap is reached, CRM reduction = 1 − t_final/22.0 and ε falls below target.
- Grain size, shape, surface, max. extrusion area reduction and rating are **step bands** keyed to CRM ε:

| Alloy | Full-target range (Good) | Grain (µm) / shape / surface / max extr. area red. in target range | Below-target rows |
|---|---|---|---|
| 1070 | t_final ≤ 8.5 mm (ε 0.950) | 28–48 / Near equiaxed / Smooth / 70–80 % | 8.6–9.4 mm (ε 0.939–0.850): same bands, Acceptable; 9.5–9.8 mm (ε 0.840–0.809): 45–80 / Slightly elong. / Good / 60–72, Acceptable; 9.9–10.0 mm (ε 0.799–0.788): Marginal |
| 1050 | ≤ 8.9 mm (ε 0.900) | 30–50 / Near equiaxed / Smooth / 70–80 % | 9.0–9.4 mm (ε 0.894–0.850): Acceptable; 9.5–10.0 mm (ε 0.840–0.788): 48–80 / Slightly elong. / Good / 60–72, Acceptable |
| 3102 | ≤ 9.8 mm (ε 0.800) | 40–65 / Slightly elong. / Good / 60–72 % | 9.9–10.0 mm (ε 0.799, 0.788): Acceptable |
| 3207 | ≤ 9.4 mm (ε 0.850) | 30–50 / Near equiaxed / Smooth / 70–80 % | 9.5–10.0 mm (ε 0.840–0.788): 45–75 / Slightly elong(ated) / Good / 60–72, Acceptable |
| 3003 | ≤ 8.5 mm (ε 0.950) | 35–55 / Near equiaxed / Good / 70–80 % | 8.6–9.4 mm (ε 0.939–0.850): Acceptable; 9.5–9.8 mm (ε 0.840–0.809): 55–90 / Slightly elong. / Orange peel risk / 60–72, Acceptable; 9.9–10.0 mm: Marginal |

Selected rows for 3102 and 3207 (incl. the slug thicknesses 6.1/6.3/6.6/7.2/7.4 mm from §8):

| Alloy | Final (mm) | HRM exit (mm) | HRM red. (%) | HRM ε | CRM red. (%) | CRM ε | Grain (µm) | Rating |
|---|---|---|---|---|---|---|---|---|
| 3102 | 2.0 | 4.45 | 79.8 | 1.598 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 4.0 | 8.90 | 59.5 | 0.905 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 6.1 | 13.58 | 38.3 | 0.483 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 6.3 | 14.02 | 36.3 | 0.450 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 6.6 | 14.69 | 33.2 | 0.404 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 7.2 | 16.02 | 27.2 | 0.317 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 7.4 | 16.47 | 25.1 | 0.290 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 9.8 | 21.81 | 0.9 | 0.009 | 55.1 | 0.800 | 40–65 | Good |
| 3102 | 10.0 | 22.00 | 0.0 | 0.000 | 54.5 | 0.788 | 40–65 | Acceptable |
| 3207 | 2.0 | 4.68 | 78.7 | 1.548 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 4.0 | 9.36 | 57.5 | 0.855 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 6.1 | 14.27 | 35.1 | 0.433 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 6.3 | 14.74 | 33.0 | 0.400 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 6.6 | 15.44 | 29.8 | 0.354 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 7.2 | 16.85 | 23.4 | 0.267 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 7.4 | 17.31 | 21.3 | 0.240 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 9.4 | 21.99 | 0.0 | 0.000 | 57.3 | 0.850 | 30–50 | Good |
| 3207 | 9.5 | 22.00 | 0.0 | 0.000 | 56.8 | 0.840 | 45–75 | Acceptable |
| 3207 | 10.0 | 22.00 | 0.0 | 0.000 | 54.5 | 0.788 | 45–75 | Acceptable |

`EN_AW_3207_CRM_Reduction_Table.xlsx` adds (verbatim summaries): header "Full anneal after CRM (~360°C / 2h)";
"Rule: CRM provides the grain refinement. HRM exit gauge is set to guarantee CRM ε ≥ 0.85. For thick slugs, HRM
reduction is lowered to give CRM enough work." Legend: Green = CRM ε ≥ 0.85 (recommended); Yellow = ε 0.55–0.84
(acceptable to marginal, coarser grain, more variability); Red = ε < 0.55 (poor: very coarse grain, high scatter,
orange peel, limited extrudability). Notes: (2) for slugs > 9.4 mm 22 mm stock cannot deliver ε = 0.85;
(3) grain sizes are estimates for full anneal ~350–380 °C / 1–2 h with moderate heating rate and depend on
homogenisation state, Mn dispersoid distribution and prior hot-rolling temperature; (4) for ≥ 9.4 mm consider an
intermediate anneal + second cold pass; (5) use reasonably fast heating to avoid Mn precipitation before RX;
(6) "Ideal CRM zone for cold extrusion: ε = 0.85–1.10 (57–67% reduction). Diminishing returns above ε ≈ 1.2."

### Assessment
- **Physically sound core idea:** RX grain size after the final anneal is controlled by the cold strain after the
  last recrystallising step; higher ε → more nuclei (PSN at constituents > ~1 µm needs sufficient strain) → finer,
  more equiaxed grain → better surface (no orange peel) and higher permissible extrusion reduction. The ordering
  of anneal temperatures (1070 < 1050 < 3102 < 3207 < 3003) and the heating-rate warnings for Mn alloys agree with
  the literature (e.g. Al-1.3Mn: +75 °C RX temperature at slow heating in the user's own H&H table, §6) *(ext.)*.
- **Assumes the hot band is fully recrystallised** at HRM exit (HRM strain "reset"). If the hot band is only
  recovered (low exit temperature), retained strain adds to the CRM strain — worth checking by hot-band EBSD.
- **Grain sizes are heuristic bands, not model outputs**, and disagree with the user's models: 3207 at ε ≥ 0.85
  → 30–50 µm here vs 17.8 µm (AA3207 model at 45 % CR); 3102 at ε 0.8 → 40–65 µm here vs 46 µm (55 % CR,
  `3102_RX_simulation`) — the latter is consistent.
- **Anneal-window conflict for 3102:** this table recommends 340–370 °C for 1–2 h at ε ≥ 0.80 (55 % CR), but the
  user's own 3102 JMAK model gives t₉₉ = 1215.1 min at 350 °C and 422.5 min at 370 °C for 55 % CR (§2.3), and the
  dashboard gives 96.4 min at 370 °C for 50 % CR. Only the dashboard model, at ≥ 50 % CR and ≈ 370 °C, reaches
  99 % RX within ~1.6 h; the 3102 simulator does not reach it anywhere in this window. The plant uses
  415–455 °C at 25 % CR.
- **Plant CR vs table:** the annealing dashboard works at 25 % (current) and 45 % (proposed) CR — well below the
  55–61 % targets here. Raising CR is the most effective lever for both grain size and lower anneal T (lower MgO).

---

## 6. Temper tables: aluminium_tempers_v2 / v3 / SLO

**Purpose:** reference workbook on O/H temper designations, required cold reductions, annealing/partial
anneal/stabilisation temperatures, typical and minimum properties, and the Dwight/EN 515 strength formula.
Sources cited in the workbook: ASM Handbook of Aluminium, Humphreys & Hatherly, Aluminum Association, Dwight
"Aluminium Design and Construction" (1999). No 3102/3207-specific property data.

**Versions:** v2 (6 sheets) has a one-line O-temper anneal note and generic H2x/H3x thermal text and lacks the
"Annealing Temperatures" sheet. v3 (7 sheets) adds series/alloy anneal temperatures, partial-anneal/stabilisation
temperatures and the H&H RX-temperature table, **but its "Annealing / Thermal Treatment" column is shifted down
one row from H22 to H111** (e.g. H22 "Calibrated by trial to hit 1/8-hard", H24 "Target: 3/8 hard",
H31 "PARTIAL ANNEAL … Target: full-hard", H111 "STABILIZATION … Max strength + stabilized for 5xxx").
**SLO (Slovenian, 20:52, newest)** is a translation of v3 with this shift corrected — use SLO (or a fixed v3) as
master. Numeric tables are identical in all three.

### 6.1 Cold reduction by temper (2nd digit) — sheet "CW Reduction Summary"

| 2nd Digit | Hardness Name | H1x (CW only) Cold Reduction % | H3x (CW+stab.) Cold Reduction % | H2x Initial CW % (before partial anneal) | Approx. True Strain ε (for H1x/H3x) |
|---|---|---|---|---|---|
| 1 (1/8 hard) | ~1/8 hard | 5–10% | 5–10% | ≥10–20% | 0.05–0.11 |
| 2 (1/4 hard) | Quarter-hard | 10–20% | 10–20% | ≥25–35% | 0.11–0.22 |
| 3 (3/8 hard) | ~3/8 hard | 20–25% | 20–25% | ≥35–45% | 0.22–0.29 |
| 4 (1/2 hard) | Half-hard | 25–35% | 25–35% | ≥45–65% | 0.29–0.43 |
| 5 (5/8 hard) | ~5/8 hard | 35–45% | 35–45% | ≥55–75% | 0.43–0.60 |
| 6 (3/4 hard) | Three-quarter-hard | 45–55% | 45–55% | ≥65–80% | 0.60–0.80 |
| 7 (7/8 hard) | ~7/8 hard | 55–65% | 55–65% | ≥75–85% | 0.80–1.05 |
| 8 (full-hard) | Full-hard | ~75% (REFERENCE) | ~75% | ≥85–90% | ~1.39 |
| 9 (extra-hard) | Extra-hard | 85–90% (87% for can stock) | — | — | 1.90–2.30 |

Key formulas: ε = −ln(1 − r); r = 1 − exp(−ε); 75 % → ε = 1.386; 87 % → ε = 2.04. H19: "UTS ≥ H18 + 14 MPa (2 ksi)";
AA3104 can body stock cold rolled 87 % for H19. Special tempers: H111 (~1–3 % CW from levelling/stretching,
ε ~0.01–0.03, after full anneal); H112 (as-fabricated, residual hot-work strain, no guaranteed CW); H116 (5xxx
Mg ≥ 4 %, min. properties + exfoliation resistance per ASTM B928); H321 (CW < H32, ~5–15 %, stabilised, ASTM B928).
Thermal treatments (SLO/v3): H2x partial anneal ~200–280 °C (390–535 °F), 1–4 h, below full RX, calibrated per
alloy/gauge; H3x stabilisation 120–175 °C (250–350 °F), 1–6 h (5xxx).

### 6.2 Annealing temperatures (v3/SLO)

Minimum full-annealing temperature by series (Dwight §3.3):

| Alloy Series | Min. Anneal Temp (°C) | (°F) | Type | Cooling Rate | Notes |
|---|---|---|---|---|---|
| 1xxx (pure Al) | 360 | 680 | Non-heat-treatable | Any (not critical) | Recrystallization anneal. Heat quickly to avoid grain growth. |
| 3xxx (Al-Mn) | 400 | 750 | Non-heat-treatable | Any (not critical) | Higher min. temp than 1xxx/5xxx due to Mn dispersoids retarding recrystallization. |
| 5xxx (Al-Mg) | 350 | 660 | Non-heat-treatable | Any (not critical) | Mg in solid solution lowers recrystallization temp slightly vs pure Al. |
| 2xxx (Al-Cu) | 413 (775°F typical) | 775 | Heat-treatable | Slow cool ~28°C/hr (50°F/hr) to 230°C (450°F) | Must remove effect of prior solution heat treatment. |
| 6xxx (Al-Mg-Si) | 413 (775°F typical) | 775 | Heat-treatable | Slow cool ~28°C/hr to 230°C | Same as 2xxx. |
| 7xxx (Al-Zn-Mg) | 413 (775°F typical) | 775 | Heat-treatable | Two-stage: slow cool to 230°C, hold 230°C 4 hr, air cool | Two-stage anneal needed. |

Specific annealing conditions (ASM Table 7): 1060, 1100, 1350 — 343 °C (650 °F), until centre at temperature,
rate not critical; **3003 — 413 °C (775 °F)**; **3004, 3105 — 343 °C (650 °F)**; 5005, 5050, 5052, 5056, 5083,
5086, 5154, 5254, 5454, 5456, 5457, 5652 — 343 °C; 2014, 2017, 2024, 2117, 2219 — 404 °C (760 °F), 2–3 h, slow
cool 50 °F/h to 500 °F; 2036 — 385 °C (725 °F); 6005, 6053, 6061, 6063, 6066 — 404 °C, 2–3 h, slow cool;
7001, 7075, 7178 — 404 °C, 2–3 h, two-stage (air cool to 400 °F, hold 450 °F 4 h).

Recrystallisation temperatures — effect of alloying (from Humphreys & Hatherly):

| Alloy / Element | RX Temp (°C) Fast Heating (500°C/s) | RX Temp (°C) Slow Heating (10°C/hr) | Notes |
|---|---|---|---|
| Al–0.25% Sc | 575 ± 5 | 550 ± 20 | Sc precipitates before recrystallization at slow heating rates |
| Al–0.25% Zr | 380 ± 10 | 480 ± 20 | Zr precipitation raises recrystallization temp by ~100°C at slow heating |
| Al–1.3% Mn | 425 ± 5 | 500 ± 20 | Mn dispersoids raise recrystallization temp significantly at slow heating |
| High purity Al (99.999%) | ~−20 (deformed at −196°C) | — | Recrystallizes at extremely low temp |
| 99.998% Al (deformed RT) | ~300 | — | Recovery peak 100–250°C; recrystallization peak ~300°C |
| Commercial Al (AA1050) | 280–520 (varies!) | — | Strongly depends on Fe/Si content, prior heat treatment, and annealing temp |

### 6.3 Typical mechanical properties (ASM Handbook)

| Alloy | Temper | UTS (MPa) | Yield (MPa) | Elong. (%) | HB | Approx. CW% | Product Form |
|---|---|---|---|---|---|---|---|
| 1070 | O | 70 | 30 | 43 | 19 | 0% | Sheet |
| 1070 | H18 | 130 | 125 | 6 | 35 | ~75% | Sheet |
| 1070 | H24 | 100 | 90 | 12 | 26 | Initially >35%, annealed back | Sheet |
| 1100 | O | 90 | 35 | 35 | 23 | 0% | Sheet, plate |
| 1100 | H12 | 110 | 105 | 12 | 28 | ~10–20% | Sheet, plate |
| 1100 | H14 | 125 | 118 | 9 | 32 | ~25–35% | Sheet, plate |
| 1100 | H16 | 145 | 140 | 6 | 38 | ~45–55% | Sheet, plate |
| 1100 | H18 | 165 | 150 | 5 | 44 | ~75% | Sheet, plate |
| 3003 | O | 110 | 40 | 30 | 28 | 0% | Sheet, plate |
| 3003 | H12 | 130 | 125 | 10 | 35 | ~10–20% | Sheet, plate |
| 3003 | H14 | 150 | 145 | 8 | 40 | ~25–35% | Sheet, plate |
| 3003 | H16 | 178 | 170 | 5 | 47 | ~45–55% | Sheet, plate |
| 3003 | H18 | 200 | 185 | 4 | 55 | ~75% | Sheet, plate |
| 3104 | H19 | — | — | ~2% | — | ~87% | Can body sheet |
| 5052 | O | 194 | 90 | 25 | 47 | 0% | Sheet, plate |
| 5052 | H32 | 230 | 195 | 12 | 60 | ~10–20% + stab. | Sheet, plate |
| 5052 | H34 | 261 | 215 | 10 | 68 | ~25–35% + stab. | Sheet, plate |
| 5052 | H36 | 275 | 240 | 8 | 73 | ~45–55% + stab. | Sheet, plate |
| 5052 | H38 | 290 | 255 | 7 | 77 | ~75% + stab. | Sheet, plate |
| 5056 | O | 290 | 151 | 32 | 65 | 0% | Rod, wire |
| 5056 | H18 | 435 | 405 | 9 | 105 | ~75% | Wire |
| 5056 | H38 | 415 | 345 | 14 | 100 | ~75% + stab. | Wire |
| 5083 | O | — | — | — | 67 | 0% | Sheet, plate |
| 5083 | H321 | — | — | — | 82 | ~5–15% + stab. | Sheet, forgings |
| 5454 | O | — | — | — | 62 | 0% | Sheet, plate |
| 5454 | H34 | — | — | — | 81 | ~25–35% + stab. | Sheet, plate |
| 5454 | H111 | — | — | — | 70 | ~1–3% | Extruded |
| 5454 | H112 | — | — | — | 62 | Residual from hot work | Forgings |

### 6.4 Minimum strength (Dwight Table 4.5, BS EN 485/755)

| Alloy | Composition | Temper | t (mm) Plate/Sheet | fo (MPa) Plate/Sheet | fu (MPa) Plate/Sheet | fo (MPa) Extrusion | fu (MPa) Extrusion | Elong. % |
|---|---|---|---|---|---|---|---|---|
| 3103 | Mn 1.2 | O | <50 | 35 | 90 | — | — | 17–28 |
| 3103 | | H14 | <25 | 120 | 140 | — | — | 2–5 |
| 3103 | | H18 | <3 | 165 | 185 | — | — | 1–2 |
| 5251 | Mg 2.0, Mn 0.3 | O | <50 | 60 | 160 | 60 | 160 | 13–18 |
| 5251 | | H22 | <25 | 120 | 190 | — | — | 4–12 |
| 5251 | | H24 | <12 | 140 | 210 | — | — | 3–10 |
| 5251 | | H26 | <4 | 170 | 230 | — | — | 3–7 |
| 5154A | Mg 3.5 | O | <50 | 85 | 215 | 85 | 200 | 12–16 |
| 5154A | | H22 | <40 | 180 | 250 | — | — | 5–9 |
| 5154A | | H24 | <25 | 200 | 270 | — | — | 4–7 |
| 5154A | | H26 | <6 | 230 | 290 | — | — | 3–5 |
| 5083 | Mg 4.5, Mn 0.7, Cr 0.15 | O | <50 | 125 | 275 | 110 | 270 | 10–16 |
| 5083 | | H22 | <40 | 215 | 305 | — | — | 5–10 |
| 5083 | | H24 | <25 | 250 | 340 | — | — | 4–7 |
| 6063 | Mg 0.7, Si 0.4 | T4 | — | — | — | 65 | 130 | 12–14 |
| 6063 | | T5 | — | — | — | 130 | 175 | 5–8 |
| 6063 | | T6 | — | — | — | 170 | 215 | 6–8 |
| 6061 | Mg 1.0, Si 0.6, Cu 0.25 | T4 | <12 | 110 | 205 | 110 | 180 | 12–18 |
| 6061 | | T6 | <12 | 240 | 290 | 240 | 260 | 6–10 |
| 6082 | Mg 0.9, Si 1.0, Mn 0.7 | T4 | <12 | 110 | 205 | 110 | 205 | 12–14 |
| 6082 | | T6 | <6 | 260 | 310 | 250 | 290 | 6–10 |
| 6082 | | T6 | 6–12 | 255 | 300 | 260 | 310 | 6–10 |
| 7020 | Zn 4.5, Mg 1.2, Cr 0.2 | T4 | <12 | 210 | 320 | — | — | 11–14 |
| 7020 | | T6 | <12 | 280 | 350 | 290 | 350 | 7–10 |
| 7019 | Zn 4.0, Mg 2.0 | T6 | — | 330 | 380 | 330 | 380 | 8 |

### 6.5 Temper vs tensile strength — "BSEN.515 formula" (from Dwight): fu = P × fuo + Q

| Temper | P | Q (N/mm²) | Description | Example fuo = 160 MPa (5251-O) |
|---|---|---|---|---|
| O | 1 | 0 | Annealed baseline | 160 |
| Hx2 (H12, H22, H32) | 1.03 | 20 | Quarter-hard | 185 |
| Hx4 (H14, H24, H34) | 1.06 | 40 | Half-hard | 210 |
| Hx6 (H16, H26, H36) | 1.09 | 60 | Three-quarter-hard | 234 |
| Hx8 (H18, H28, H38) | 1.12 | 80 | Full-hard | 259 |

Dwight notes: valid for annealed UTS > ~90 N/mm² (excludes pure Al); H2x/H3x have the same UTS as H1x of the same
2nd digit but slightly lower proof stress and higher elongation; odd 2nd digits interpolated linearly.
Processing routes: H1x = anneal → cold roll to target → ship (e.g. 1100-H14 ~30 %, 3003-H18 ~75 %, 3104-H19
~87 %); H2x = anneal → over-roll → partial anneal back (e.g. 1070-H24: roll ~50–65 %, partial anneal ~200–280 °C);
H3x = anneal → cold roll → stabilise ~150 °C (5052-H34 ~30 %, 5052-H38 ~75 %).

### Assessment
- Content is standard and broadly consistent with AA/ASM/EN 515 practice. The CW% per temper is a reasonable
  sheet-practice guide; actual reductions depend on the alloy's work-hardening curve.
- The v3 row shift (above) is a real error that could mislead (e.g. H31 described as a partial anneal).
- The "BSEN.515 formula" applies to *minimum* UTS of sheet; the Dwight note excludes alloys with fuo < ~90 MPa,
  i.e. it does **not** apply to 1070/1050 and is marginal for 3102/3207 slugs (O-temper UTS around/below 90 MPa).
- **Gap for the R&D goal:** no 3102/3207 O/H-temper limits (EN 485-2/EN 573) and no in-house tensile/HB data;
  slugs are supplied essentially in the O condition, so the relevant data are O-temper HB/UTS vs grain size.
- Inconsistency with §5: the ASM anneal temperature for 3003 (413 °C) and the Dwight 3xxx minimum (400 °C) are
  above the 3003 window in the CRM table (370–400 °C) and far above the 3102 window (340–370 °C).

---

## 7. Aluminium_Alloys_CBAM_Presentation.pptx

**Purpose:** company/commercial presentation (≈5 slides, exported from an `index.html`) positioning a
**100 %-scrap-based slug producer** under CBAM. Text content:

Slide "Aluminum Alloy Series Classification":

| Series | Main Element | Second Most Common Addition | |
|---|---|---|---|
| 1xxx | 99%+ Aluminum (Pure) | Iron, Silicon | ★ |
| 2xxx | Copper (2.0-6.8%) | Magnesium | |
| 3xxx | Manganese (0.3-1.5%) | Magnesium | ★ |
| 4xxx | Silicon (3.6-13.5%) | Copper, Magnesium | |
| 5xxx | Magnesium (0.5-5.5%) | Manganese, Chromium | |
| 6xxx | Magnesium + Silicon | Iron, Copper | |
| 7xxx | Zinc (1.0-8.0%) | Magnesium, Copper | |
| 8xxx | Other Elements | Lithium, Iron, etc. | |

"★ Primary alloys used for aerosol cans (1xxx and 3xxx series)"

Slide "New Elements Challenge in Recycling — Emerging Elements During Aluminum Recycling":
- Magnesium: lightweighting potential; improved strength-to-weight; challenges: dross formation, oxidation; tool
  wear; dimension controls after extrusion (spring back).
- Zinc: corrosion resistance; enhanced mechanical properties; challenges: tool wear, volatility; (also listed:
  hot cracking, inner lacquer compatibility).
- Copper: strength improvement; thermal conductivity; challenges: hot cracking, inner lacquer compatibility.
- Manganese: grain refinement; improved formability; challenges: intermetallic formation, tool wear.
- "These elements bring OPPORTUNITIES for lightweighting and performance, alongside technical CHALLENGES."

Slide "Transforming Challenges into Opportunities — WE ARE READY": new investment in specialised equipment;
advanced alloy production capabilities, annealing; melting & casting technology; enhanced QC; R&D partnership with
industry players; "Positioned to produce complex alloys meeting tomorrow's lightweighting demands".

Slide "Sustainable Recycling & EU Regulatory Excellence": "Only slug producer sourcing 100% scrap - NO primary
ingots or SOWs used"; closed-loop can recycling; "95% energy savings vs. primary"; zero waste to landfill; full
traceability; ISO 14001; below emission limits; advanced filtration; real-time monitoring.

Slide "CBAM Impact on Aluminum Pricing & Competitiveness": "CBAM will increase European aluminum costs from
**$45/t (2026) to $308/t (2034)**" (2026: +$45/t; 2030: "progressive increase"; 2034: +$308/t). EU recyclers face
higher EU ingot prices and scrap prices linked to primary. 100 % scrap strategy: minimises CBAM exposure,
circular-economy advantage, "closing the material loop with conversion business".

**No embedded-emissions figures (tCO2e/t), scrap ratios by alloy or composition limits are given.**

### Assessment
- **Alloy-design implication (the important one):** 100 % scrap feed (largely used beverage cans: 3104 body
  ~1 % Mn/~1 % Mg and 5182 ends ~4.5 % Mg *(ext.)*) inevitably raises Mg, Mn, Cu, Zn, Fe, Si in slug melts. This is
  the likely driver for the wider Mg/Zn/Cu windows and the higher Mn of the "modified 3102" (§1) and for the
  0.12–0.15 % Mg / 0.09 % Cu in the 3102/3207 models. It also explains the MgO focus in annealing (§3). Alloy
  windows should be set from a scrap-mix mass balance (dilution capacity) rather than from primary-alloy habits.
- **Technical statements to correct:** Cu in solid solution *lowers* thermal conductivity; Mn does not refine the
  as-cast grain (it controls recrystallised grain size via dispersoids); low-level Zn makes Al more anodic rather
  than "more corrosion resistant" (relevant to HEX sacrificial design, not to cans); the duplicated
  "hot cracking, inner lacquer compatibility" bullet under Zn looks like a copy error.
- **CBAM numbers:** the source and assumptions (carbon price, emission intensity, default values) for $45 → $308/t
  are not stated. Under Regulation (EU) 2023/956 the CBAM obligation phases in from 2.5 % (2026) to 100 % (2034)
  of the full charge, a ×40 ratio at constant carbon price, versus ×6.8 here; for aluminium only *direct* emissions
  are covered *(ext., verify)*. CBAM is an import charge — for an EU recycler the effect is indirect (EU price
  of primary metal and scrap-price linkage), as the slide itself says.

---

## 8. Aluminium slug specification documents

`Aluminum Slug Data Table` (data) and `Aluminum Slug Specifications - Technical Analysis` (same data + analysis);
`Aluminum Slug Specifications Reference` is empty apart from the title text.

| DIA (mm) | Can H (mm) | t (mm) | Weight (g) | Slug Thickness (mm) |
|---|---|---|---|---|
| 45 | 200 | 0.35 | 27.97 | 6.60 |
| 50 | 185 | 0.40 | 33.19 | 6.30 |
| 53 | 171 | 0.44 | 36.08 | 6.10 |
| 53 | 205 | 0.44 | 42.75 | 7.20 |
| 53 | 210 | 0.44 | 43.73 | 7.40 |

Technical analysis (verbatim summary): slug thickness = required blank thickness, Al density 2.70 g/cm³;
example 53/205/0.44: finished can surface area ~36,341 mm², wall + base volume ~15.99 cm³, theoretical weight
43.17 g vs 42.75 g actual, "Material efficiency: 98.8% (1.2% trim/scalping allowance)"; "All specifications appear
consistent with 3102 alloy aerosol can requirements"; "Material efficiency of 98-99% is typical for AEROBAL-grade
production"; slug thickness range 6.1–7.4 mm "within standard extrusion parameters"; "Production ready for customer
quoting".

**Not present in any slug document:** composition limits, grain size, hardness (HB), annealing/temper, surface
(MgO/oxide) or lubrication requirements. The closest in-house targets are in §2/§3 (HB values in the model files
span ≈ 23–33, grain 20–100 µm, MgO ≤ ~7–9 nm) and §5 (grain bands, max extrusion area reduction).

**User clarifications (2026-10-12):**
- "23–33 HB" is not a specification; it was inferred from the model files. A slug around **35 HB** is acceptable
  and simply means a stronger alloy.
- The goal is alloys that are stronger, good to impact-extrude, and castable on the user's **rotary strip
  caster**. This also answers §11 Q9: the starting strip is continuously cast on a rotary caster.
- Actual line: 22 mm cast strip → in-line hot rolling **≥ 50 %** → **cooling bath** → cold rolling **30–50 %**.
  - *Assessment:* for the 6.1–7.4 mm slugs (§8), this gives cold ε ≈ 0.40–0.59.
  - The §5 tables assume 21–38 % hot and 55–57 % cold reduction (ε 0.80–0.85).
  - Current practice therefore sits in the tables' own "red/yellow" bands (ε < 0.55 / 0.55–0.84).
  - The table data themselves are unchanged.

### Assessment
- Slug geometry is self-consistent: slug mass = (π/4)·D²·h·2.70 within 0.3–1.3 %, and slug thickness =
  mass/(2.70·πD²/4) rounded **up** to 0.1 mm (i.e. slug Ø = can Ø assumed) *(recalc.)*.
- **The listed slug weights are ≈ 99.0–99.1 % of the mass of a can with uniform wall and base thickness t** for
  all five sizes *(recalc.)* — the slug is *lighter* than the "theoretical can". The analysis's reading as "98.8 %
  efficiency / 1.2 % trim allowance" inverts the relation (and 42.75/43.17 = 99.0 %, not 98.8 %). Impact extrusion
  needs slug mass > finished can mass + trim. Either t is a nominal/maximum wall (actual wall thinner) or base and
  wall thicknesses differ; this must be clarified before quoting.
- Slug thicknesses 6.1–7.4 mm fall in the "Good" rows of the CRM tables (§5) for both 3102 and 3207, but they
  require HRM exit gauges of 13.6–17.3 mm, i.e. only 21–38 % hot reduction from 22 mm strip *(from §5 data)*.

---

## 9. Cross-file synthesis (Assessment)

1. **Three mutually inconsistent RX kinetics models** exist for practically the same lean Al-Mn chemistry:
   AA3207 model (n = 3, Q = 145 kJ/mol, t50 ∝ ε⁻²), 3102 simulator (n = 1.8–2.2, Q = 200–172 kJ/mol), 3102 dashboard
   (n = 2.0–2.5, Q = 200–170 kJ/mol). At 25 % CR / 415 °C the predicted t50 differs ~7× (6 min vs 46 min)
   *(recalc.)*. Only the dashboard links to plant observations; none has a documented measured calibration set.
2. **Grain-size predictions disagree** (AA3207 model 17.8 µm cap; 3102 simulator 43–114 µm; dashboard 15–100 µm;
   CRM tables 28–90 µm bands). Measured slug grain sizes (linear intercept / EBSD) vs CR and cycle are the key
   missing data.
3. **Role of Mg and Cu is contradictory** across files (stored-energy accelerator vs strong solute-drag retarder).
   Physically: at 0.1–0.3 % Mg and ≤ 0.1 % Cu in commercial alloys both effects are modest; Mn in supersaturated
   solution and concurrent Mn precipitation dominate 3xxx RX behaviour and depend on homogenisation and heating
   rate — which none of the models represent dynamically.
4. **Process levers ranked by the user's own data:** raise cold reduction (25 → ≥ 45–55 %) → lower anneal T and
   time → less MgO and finer grain; keep heating fast through ~300–400 °C for higher-Mn variants; credit the full
   T(t) path (ramps + overshoot) in RX predictions.
5. **Composition direction:** the "modified 3102" (high Mn/Mg) increases strength for thin walls but moves the
   alloy into the slow-RX, heating-rate-sensitive, higher-MgO regime that the dashboard is trying to avoid; a
   trial should be planned together with a CR/anneal redesign.

---

## 10. Consolidated alloy compositions (wt %, as written in the user's files)

| Source file | Alloy / label | Basis | Si | Fe | Cu | Mn | Mg | Zn | Ti | Others each / total | Al |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Modified 3102 Alloy Composition Explained | "Modified 3102" | Proposed window | ≤ 0.15 | ≤ 0.45 | 0.05 – 0.10 | 1.10 – 1.30 | 0.25 – 0.35 | 0.10 – 0.15 | ≤ 0.05 | ≤ 0.05 / ≤ 0.15 | base |
| 3102_RX_simulation | EN AW 3102/3207 (title: "0.09%Cu, 0.12%Mg, 0.2%Mn") | Model input ("wt%") | 0.17 | 0.35 | 0.09 | 0.3 | 0.12 | — | — | — | Bal. |
| 3102_RX_simulation | same | "Spec" column | ≤0.40 | ≤0.70 | ≤0.10 | 0.05–0.40 | ≤0.15 | — | — | — | ≥99.0 |
| mg_dashboard | EN AW 3102 (AlMn0.2) | Designation only | — | — | — | — | — | — | — | — | — |
| AA3207_Recrystallization_Simulation (all 4) | AA3207 ("Al-0.45Mn-0.15Mg-0.09Cu") | Model input | 0.15 | 0.35 | 0.09 | 0.45 (0.15 in solid solution) | 0.15 | 0.01 | 0.015 | — | 98.785 |
| EN_AW_Master_CRM_Reduction_Tables | EN AW 1070 | Header note | ≤0.20 | ≤0.25 | — | — | — | — | — | — | 99.7 |
| EN_AW_Master_CRM_Reduction_Tables | EN AW 1050 | Header note | ≤0.25 | ≤0.40 | — | — | — | — | — | — | 99.5 |
| EN_AW_Master_CRM_Reduction_Tables | EN AW 3102 | Header note | — | — | ≤0.10 | ≤0.40 | — | — | — | — | — |
| EN_AW_Master_CRM_Reduction_Tables / 3207 table | EN AW 3207 | Header note | — | — | 0.09 | ≤0.60 | 0.15 | — | — | — | — |
| EN_AW_Master_CRM_Reduction_Tables | EN AW 3003 | Header note | — | — | 0.05–0.20 | 1.0–1.5 | — | — | — | — | — |
| aluminium_tempers (Dwight Table 4.5) | 3103 | Nominal | — | — | — | 1.2 | — | — | — | — | — |

Other nominal compositions in the temper workbook (reference alloys, not in-house): 5251 Mg 2.0, Mn 0.3;
5154A Mg 3.5; 5083 Mg 4.5, Mn 0.7, Cr 0.15; 6063 Mg 0.7, Si 0.4; 6061 Mg 1.0, Si 0.6, Cu 0.25; 6082 Mg 0.9, Si 1.0,
Mn 0.7; 7020 Zn 4.5, Mg 1.2, Cr 0.2; 7019 Zn 4.0, Mg 2.0.

Flags *(Assessment)*: 3102 Mn stated as both 0.2 and 0.3; Mg 0.12–0.15 in "3102" and 0.15 in "3207" should be
checked against EN 573-3 limits; the modified 3102 is outside EN AW-3102 for Mn (and probably Mg).

---

## 11. Open questions for the user

1. **Modified 3102:** is it a planned trial alloy? What are the quantitative targets (slug HB, can wall UTS/YS,
   burst pressure, target wall thickness, lacquer-bake softening)? Which designation would it carry, given Mn
   1.10–1.30 % is outside EN AW-3102?
2. **Actual 3102 chemistry:** is Mn ≈ 0.2 % (AlMn0.2, dashboard/title) or 0.3 % (composition table)? How is
   Mg 0.12 % reconciled with the EN AW-3102 limits? Typical/maximum Mg, Cu, Zn pick-up from the 100 % scrap feed?
3. **AA3207 inputs:** are Mn 0.45 / Mg 0.15 / Cu 0.09 / Fe 0.35 / Si 0.15 measured cast analyses? Is Mg 0.15 %
   within your customer spec for 3207?
4. **Calibration data:** where does "t50 ~300 s at 350 °C, 70 % CR" come from? Do you have measured softening
   curves (HB vs time/temperature), RX fractions (metallography/EBSD), dispersoid size/Fv (TEM/SEM, conductivity)?
5. **Plant cycles:** what cold reductions did Cycles 1–3 and A1 have? Measured HB and grain size after each? Was
   the A1 "partial RX" confirmed metallographically, and at which load position (T8)?
6. **Which RX model is current** for 3102 — `3102_RX_simulation` (n = 1.8) or `mg_dashboard` (n = 2.0)? Can the
   cell formulas be shared (the Drive export shows values only; the formulas in §2.2 are reconstructions)?
7. **Anneal window conflict:** the CRM table recommends 340–370 °C / 1–2 h for 3102 at ≥ 55 % CR, while your own
   JMAK model needs ≥ 7 h at 370 °C — which has been validated in production?
8. **MgO:** why is MgO minimised (lacquer adhesion, discolouration, lubricant/phosphating, extrusion friction)?
   Any measured oxide thickness to validate the "Zayan" model? Is N₂/Ar atmosphere an option?
9. **"CRM" meaning:** confirm CRM = cold rolling mill. Is there a separate **critical-raw-materials** analysis
   (none was found in Drive)? Is the 22 mm starting strip continuously cast (which caster)?
10. **CBAM:** source and assumptions for $45/t (2026) → $308/t (2034)? Any embedded-emission (tCO2e/t) figures for
    your products or scrap mix?
11. **Slug specs:** which alloy/temper are the five slug sizes for? Required HB, grain size, surface condition?
    Does "t" mean wall thickness only (base thicker/thinner)? The slug weights are ~1 % *below* the uniform-wall
    can mass, which leaves no trim allowance.
12. **Temper workbook:** treat `aluminium_tempers_SLO.xlsx` (row-shift corrected) as the master, and fix v3?
    Are 3102/3207 O-temper property limits (EN 485-2) or in-house tensile data available to add?
