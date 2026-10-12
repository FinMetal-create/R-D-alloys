# Talum 1 — first plant trial alloy

**Name (user, 2026-10-12):** the alloy is called **Talum 1**. It was trial ID **T11** until the user renamed it;
the other alloy-design session and older notes still say Talum 1. "Talum 1" is a trade name; it does not replace a
registered designation. The alloy fits AA8010 only if Cu ≥ 0.10 (§2.1); otherwise it
is sold to an own specification.

**Status:** planned; recommended process window in §2.5 (composition from the user's alloy-design session "Aerosol can alloy composition", shared
2026-10-12). All property values below are model estimates or inferences; none is plant-tested yet.

## 1. Composition (wt %)

| Group | Si | Fe | Mn | Mg | Cu | Ti | Zn | Cr |
|---|---|---|---|---|---|---|---|---|
| Talum 1 (target) | 0.38 | 0.52 | 0.14 | 0.26 | 0.038 | 0.043 | 0.034 | 0.011 |
| min | 0.37 | 0.51 | 0.13 | 0.24 | – | – | – | – |
| max | 0.39 | 0.53 | 0.15 | 0.28 | 0.042 | 0.050 | 0.050 | 0.030 |

**Charge per 10 t of metal (from the other session):** 3,110 kg T11S scrap (weigh in ≈ 3,460 kg for melt loss);
6,802 kg 1xxx scrap; 28 kg Al-75Fe; 51 kg Al-20Mn; 10 kg AlTi5B1. Reported as ≈ €8/t cheaper than the 24 %
recipe.

**Claims from the other session, not verifiable from this knowledge base:**
- "Mg ≤ 0.30 is the limit for air annealing." No such threshold appears in ch09 or ch14. Ch14 shows Mg segregates
  and forms Mg-rich oxide even at 0.05–0.1 % Mg. Ask that session for its source.
- "Cu must stay < 0.04 because of a Ball patent." Not in ch11 or ch16; the claim-1 window captured there
  (US 12,385,112) lists no Cu. Verify the patent text.
- Predicted slug hardness: ≈ 30 HB annealed in air, ≈ 29 HB in N₂.

**Route:** rotary strip caster → 22 mm strip → in-line hot rolling ≥ 50 % → cooling bath (quench) → cold
rolling 30–50 % → slugs → anneal (air or N₂) → impact extrusion → 220 °C / 10 min bake.

## 2. Assessment against the knowledge base

*Assessment = inference from the cited chapters. Ratios are derived.*

### 2.1 What Talum 1 is, metallurgically
- **Not a 3102/3207-type Al–Mn alloy.** With Mn 0.14, Mg 0.26 and Si 0.38, it behaves like a
  **Mg-bearing, Fe-rich 1xxx/8xxx base with lean-6xxx (Mg–Si) character**.
- **Registered windows:**
  - 3102 lists no Mg limit, so Mg counts as an "other" at ≤ 0.05, and 0.26 is outside (convention unverified).
  - 3207 needs Mn 0.40–0.8 and Mg ≤ 0.10. 3207A needs Mn ≥ 0.30. [ch17]
  - So Talum 1 would sell under a customer- or own-specification, not under 3102/3207. Check what the can customers
    require.
  - **Closest registered alloy: AA8010** [ch05 §4.8/§4.10, Polmear Table 3.2]: Si 0.40, Fe 0.35–0.7, Cu 0.10–0.30,
    Mn 0.10–0.8, Mg 0.10–0.50, Zn 0.40, Cr 0.20, Ti 0.10.
    - Talum 1 meets every limit **except Cu** (0.038 vs ≥ 0.10).
    - Raising Cu to ≈ 0.10–0.12 would make Talum 1 an 8010. Cu also adds work hardening (Cu is the strongest
      work-hardening solute per atom [ch07 §10]) and shifts corrosion towards a general rather than pitting mode
      [ch05 §4.2].
    - **Before changing Cu:** check the other session's unverified "Cu < 0.04 because of a Ball patent" rule
      (§1), check the 8010 limits against the Aluminum Association Teal Sheets [ch17], and check lacquer and
      product compatibility.
- **Patents:** Talum 1 sits **outside** the captured Ball US 12,385,112 claim-1 window on Si, Fe, Mn and Mg
  (window: Si 0.10–0.18, Fe 0.25–0.44, Mn 0.18–0.61, Mg 0.05–0.17) [ch16 §1.5]. It is also outside Talum
  EP 3075875 (Zr-bearing, Mg < 0.01) [ch11 §1.1]. Both are snippet-level; confirm with full claims.
  - EP 3075875 is assigned to **TALUM d.d. (Kidričevo)**. If that is the user's company, it is the company's
    own IP and prior art for any new filing on Talum 1, not a third-party risk.

### 2.2 Strengths of the design
1. **It sidesteps the rotary-caster Mn problem.** With Mn only 0.14, there is little Mn supersaturation, so
   there is little risk of precipitation before RX, slow RX or pancake grains in strip that is not homogenised
   [ch19 §1; ch03 §5; ch15 §3].
   - Expect easy, fast recrystallisation.
   - The roughly 1.5–2 vol % Fe-rich constituents are potential PSN sites [ch03 §3].
     *Corrected after the HH full-text pass:* at 30–60 % cold reduction, only particles ≳ 3–7 µm nucleate grains
     (≈ 14 % efficiency) [ch03 §3.2b]. Fast-cooled rotary-cast constituents may be mostly finer, so grain size
     depends on the coarse tail of the particle sizes and on the cold reduction (prefer ε ≈ 0.85–0.90).
   - A lower or shorter anneal is possible, which means less MgO.
2. **Strength comes mainly from Mg.** Per wt %, Mg raises wall strength ≈ 1.3–2× more than Mn in solution (Ryen, measured). Per unit
   of press force the two are close (work method; corrected after full-text pass) [ch10 §3.4, §8].
   - Expect about +13 MPa UTS (≈ +3–4 HB) from 0.26 Mg in solid solution (ΔUTS ≈ 50 MPa per wt % [ch05 §6];
     HB ≈ UTS/3.6 [ch10 §4.1]).
   - That puts a ≈ 1100-type base (23 HB) at ≈ 27–30 HB, consistent with the other session's ≈ 30 HB.
   - **Can-wall level (Ryen, measured at can-wall strains):** AA1050 reaches ≈ 160/186 MPa (Rp0.2/UTS) and
     AA3103 ≈ 207/232 MPa. Stage-IV hardening barely depends on alloy. Mg 0.26 should add ≈ 20–25 MPa to a
     1050-type base [ch10 §3.4; ch06] (estimate).
3. **Possible bake strengthening.**
   - Mg and Si in solution can strain-age or cluster in the heavily worked wall during 220 °C / 10 min, since
     Mg and Si diffuse ≈ 30–45 nm [ch19 §1.1, P6].
   - That could reduce or even reverse cure softening [ch11 §1.2] (hypothesis).
   - **Update:** the zone solvus T_v ≈ 125–140 °C means the 220 °C bake nucleates no new Mg–Si zones
     [ch04 §6.4]. So only strain ageing or growth of existing clusters can help. At 0.2–0.4 % Mg₂Si, storage
     before the bake is neutral or beneficial [ch04].
4. **High scrap share at low cost**, with Fe tolerated rather than diluted [ch16 §5].

### 2.3 Risks to check in the trial
1. **Fe-phase type: risk of β-AlFeSi platelets ("needles").**
   - Fe:Si = 0.52/0.38 ≈ 1.4. This is above the free-Si limit (> 1, R2), but well below the "Fe/Si well above
     2" recommended to avoid β [ch16 §5 #4; ch02 §9].
   - Mn:Fe ≈ 0.27 is low, so little Mn is available to convert Fe phases to compact α-Al(Fe,Mn)Si. Mn and
     ≈ 0.3 % Mn/Cu stabilise the cubic α phase [ch02 §9].
   - β is non-spheroidising and hard [ch02 §9]. Coarse Fe constituents nucleate hidden damage at the can's
     base corner and cause die wear [ch10 §5, R23].
   - Fast rotary-caster cooling helps by giving finer, often metastable phases [ch02 §3].
   - **Measure the Fe-phase type and size in the cast strip (surface and centre).**
   - **Update after the Ryen/TRIMET pass** [ch02 §3.8]:
     - Expected: α script near the fast-cooled surface, **β through the thickness, most at the centre**.
     - The normal route has no step that converts β later. A high-T hot-band treatment (ch19 P1) might partly
       transform it (unverified for this alloy).
     - Levers if β dominates:
       - Mn ≈ 0.25–0.30 (Mn:Fe ≈ 0.5);
       - more TiB₂ grain refiner (Talum 1's 10 kg AlTi5B1 per 10 t gives ≈ 0.001 % B, vs ≈ 0.005 % B in the cited
         practice);
       - a small Cr addition.
     - Classify particles by EDX with the separator in R25 (ch00).
2. **Lean-6xxx behaviour (Mg + Si).**
   - Mg 0.26 needs ≈ 0.15 Si for Mg₂Si. After the Fe phases take ≈ 0.13–0.26 Si, roughly 0.1–0.25 Si stays
     available. So Talum 1 has **≈ 0.3–0.4 wt % Mg₂Si potential (derived)**.
   - Consequences:
     - (a) **Slug hardness depends on cooling after the anneal.** Slow furnace cooling precipitates coarse
       Mg₂Si (softer, stable). Faster cooling keeps Mg and Si in solution (harder, bake-responsive).
     - (b) **Slugs with Mg and Si in solution may harden during storage** (natural ageing / clustering
       [ch04 §6]). Press force could then drift with slug age.
3. **Castability on the rotary caster.**
   - Mg + Si widen the freezing range compared with 1xxx.
   - 6xxx-type alloys are more hot-tear sensitive. The hot-tear maximum is reported at 0.3–0.4 % Fe in 6063
     [ch01 §11].
   - Watch for cracks and centreline segregation (Fe-rich) [ch15].
4. **MgO in air annealing.**
   - Mg 0.26 is about 2× the Mg in the in-house 3102/3207 models [ch09 §10].
   - The literature shows Mg-rich oxide forms above ≈ 337–400 °C, and Mg segregates to the surface even at
     low Mg [ch14].
   - The air vs N₂ comparison in this trial is therefore important. Low anneal temperatures (enabled by the low
     Mn) help.

### 2.4 Effects of the actual line (hot rolling ≥ 50 % → quench → cold 30–50 %) [ch19 §1.3]
- **Quench after hot rolling (≈ 500 °C at the caster → ≈ 380 °C after the hot mill → bath).** Mg and Si (and the
  little Mn) stay largely in solution in the hot band.
  - The hot band can **natural-age** during storage before cold rolling [ch04 §6]. Note the storage time.
  - During slow heating in the slug anneal, Mg₂Si can precipitate on the cold-worked structure before RX. At
    0.26 Mg the fraction is small, so the effect should be minor, but watch grain shape.
- **Low cold strain (ε ≈ 0.36–0.69).** With little Mn pinning, Talum 1 should still recrystallise readily. But
  fewer nuclei mean **coarser and more variable grains** than the in-house CRM tables assume (ε ≥ 0.80)
  [ch19 §1.3; ch09 §5].
  - The split is flexible (user), so for the trial set the hot-band gauge to give **ε_cold ≈ 0.85–0.90**: e.g.
    6.1 mm slug ← 14.3–15.0 mm hot band; 7.4 mm ← 17.3–18.2 mm [ch19 P10 table]. If possible, run one coil at
    the current split for comparison.
  - Measure grain size and its scatter, including the surface vs centre of the slug.

### 2.5 Recommended process window for the first cast (2026-10-12)

*Inference from the cited chapters. Values marked (estimate) do not come from a source in this knowledge base;
the trial must confirm them.*

**Numbers the reasoning rests on**
- **Liquidus ≈ 655 °C** (estimate from linearised binary liquidus slopes, general knowledge; Si and Mg lower it
  most). It is only a few K below 1xxx and lean 3xxx. Confirm with Thermo-Calc or DSC.
- **Mg₂Si potential.** Si available = Si − ¼(Fe + Mn) = 0.38 − 0.165 ≈ 0.215 %. With excess Si,
  Mg₂Si = 1.578 × Mg ≈ **0.41 %**, plus ≈ 0.07 % excess Si [ch06, HB p.169–171] (derived). The GP-zone limit is
  T_v = 111 + 71 × 0.41 ≈ 140 °C [ch04, TOT p.177] (derived).
- **Mg₂Si solvus ≈ 360–400 °C** (estimate). It comes from the Al–Mg₂Si solubility curve (1.85 % at 595 °C
  [ch04]; lower-temperature points from general knowledge), corrected for the excess Si. No solvus data exist in
  the knowledge base (ch04 gap 14). The lab anneal series LA01 measures it.
- **Full RX.** The commercial window for lean 3xxx is 345–420 °C [ch03 §4.3]. The in-house tables give
  340–380 °C at ε_cold ≥ 0.80–0.85 [ch09 §5]. Talum 1 has little Mn but runs at lower cold strain, so expect
  **≈ 380–410 °C for full RX in 1 h** (estimate).

**1. Melt temperature: 680–690 °C at the caster inlet (superheat ≈ 25–35 K)**
- **"Melt hot, cast cold"** [ch01, Eskin ch3 p.88]. Dissolve the Al-75Fe and Al-20Mn at ≈ 730–750 °C (general
  practice), then let the melt cool so it reaches the caster at 680–690 °C. Set the furnace tapping temperature
  from the measured launder loss.
- **Why not hotter:**
  - more hydrogen pick-up [ch01, Eskin ch2 p.24]. With no homogenisation, hydrogen stays in the strip until the
    slug anneal and then forms blisters [ch01 §10];
  - feathery grains, which form when a superheated melt meets a water-cooled mould. They give anisotropy and
    uneven RX [ch01; ch02];
  - more heat to remove before the strip centre solidifies, hence slower centre solidification, coarser
    constituents and more β-AlFeSi at the centre (inference from [ch02 §3.8]);
  - more Mg oxidation and dross (general knowledge).
- **Why not colder:**
  - cold folds carrying oxides and pores [ch01, Eskin ch3 p.121], and nozzle freeze-off;
  - in DC Al–2.8Cu, higher superheat *reduced* hot cracking through eutectic healing [ch02, R12 p.259–262].
    Talum 1's freezing range is wider than 1xxx, so do not run it colder than the plant's normal practice.
- **Comparable practice:** twin-roll casting of AA8011/1235 runs at 685 ± 5 °C [ch02 §4.2]. In practice, keep
  the superheat the plant uses for its standard alloy; do not raise it.
- **Grain refiner:** feed AlTi5B1 rod into the launder **after** the filter [ch01 §5.4, §10.3]. Fine grain is
  the main defence against hot tearing [ch01, TOT p.644], and the Talum 1 charge adds only ≈ 0.001 % B (§2.3).

**2. HRM and CRM reductions: cold mill at the top of its range (45–50 %, ε ≈ 0.6–0.7); hot mill takes the rest**
- The slug gauge fixes the total strain (22 → 6.1 mm: ε = 1.28). Every extra percent of hot reduction is cold
  strain lost.
  - Dynamic recovery removes much of the hot strain. Cold strain is what sets the RX nucleus density, the grain
    size and the anneal temperature needed [ch19 §1.3, P10; ch03 §4.4].
  - Talum 1 has almost no Mn supersaturation, so the split mainly controls grain size, grain uniformity and
    anneal temperature (and through it MgO). It does not control precipitation before RX.
- **Rule:** hot-band gauge ≈ 1.8–2 × slug thickness (derived):

  | Slug | Hot band | Hot reduction | Cold reduction | ε_cold |
  |---|---|---|---|---|
  | 6.1 mm | 11.0–12.2 mm | 45–50 % | 45–50 % | 0.60–0.69 |
  | 6.6 mm | 12.0–13.2 mm | 40–45 % | 45–50 % | 0.60–0.69 |
  | 7.4 mm | 13.5–14.8 mm | 33–39 % | 45–50 % | 0.60–0.69 |

- **6.1 mm slugs:** 22 → 11 → 6.1 mm fits the plant's ≥ 50 % hot rule.
- **Thicker slugs** need < 50 % hot reduction to reach this cold strain. A published twin-belt slug route
  hot-mills 27.9–35.1 mm slab to 6.0–18.0 mm, i.e. hot reductions from ≈ 35 % up [ch15, W15-04] (snippet).
  Trial one coil and check the macro-etch, porosity and blisters (workbook CS06, HB03, SL06).
- **Do not go above 50 % hot.** At 60 % hot (8.8 mm) the cold mill gives only 31 % (ε 0.37) for 6.1 mm slugs,
  and less than 30 % for 7.4 mm (derived).
- If the cold mill can exceed 50 %, ε 0.85–0.90 (57–59 % cold) is the knowledge-base optimum (ch19 P10 table).

**3. Slug anneal: ≈ 430 °C metal temperature (coldest slug ≥ 420 °C), 1 h soak, pre-heated furnace, N₂ preferred; fast cooling for strength**
- **One step does both jobs.** 430 °C is above the estimated full-RX temperature *and* the estimated Mg₂Si
  solvus. The result is a fully recrystallised slug with Mg and Si back in solution.
- **Fast cooling** after the soak (forced air; record the curve, workbook P5) keeps Mg and Si in solution.
  - Per wt %, Mg in solution raises can-wall strength the most (≈ 1.3–2× Mn) [ch10 §3.4]. Mg locked in coarse
    Mg₂Si does little.
  - Expect a somewhat harder slug, still below ~35 HB. Expect some natural-ageing drift (T_v ≈ 140 °C), so
    extrude within a fixed slug-age window (workbook SL01).
- **Slow furnace cooling** instead precipitates coarse Mg₂Si: softer, stable slugs and lower press force, but
  weaker cans [ch04 §6]. Run both cooling routes as the trial variants.
- **Pre-heated furnace / fast heating** shortens the time at 250–380 °C. In that range Mg₂Si (and Fe) can
  precipitate on the deformed structure before RX, giving coarse or elongated grains [ch03 §5.2; R10].
- **Why not hotter** (470–600 °C, the range used for pure-Al and ReAl slugs [ch11]):
  - Talum 1 has no Mn supersaturation to remove, and too little Mn to turn β into α, so a high-temperature
    step buys nothing;
  - it grows more Mg-rich oxide, since Mg oxide dominates above ≈ 337–400 °C [ch14; R18];
  - it risks grain growth with few pinning dispersoids.
- **Why not colder (≤ 380 °C):** RX may be incomplete at ε 0.4–0.7, and Mg₂Si may stay undissolved. Check with
  LA01.
- **Atmosphere:** at 430 °C the surface is in the Mg-oxide regime. Use N₂ with O₂ below a few hundred ppm
  [R18], or keep the time in air as short as possible.

**What the first cast must confirm:**
- liquidus and Mg₂Si solvus (DSC or Thermo-Calc; LA01 conductivity on water-quenched samples);
- 100 % RX and grain size at 430 °C (SL02, SL04);
- MgO in air vs N₂ (SL06);
- hardness drift after fast vs slow cooling (SL01);
- can strength and burst (K01–K05);
- castability at 680–690 °C (CS06, cracks in the process log).

## 3. What to measure (minimum set)

**Data-collection workbook:** [`Talum-1-data-collection.xlsx`](Talum-1-data-collection.xlsx) turns this plan into a
checklist (47 items, priority A/B, each linked to the model it feeds and the chapter/rule behind it), a chemistry
sheet with the Talum 1 window, a per-coil process log (reductions, true strains, heating rate and slug age calculated)
and a one-row-per-reading results sheet. Fill it during the trial and send it back; the values go into §4.

| Stage | Measurement | Why |
|---|---|---|
| Cast strip 22 mm and quenched hot band | Metallography of Fe phases (β needles vs α script), surface/centre; **constituent size distribution (fraction > 3–7 µm, PSN-eligible)** and cell/DAS size; cracks; conductivity; hot-band HB vs storage days | Risks 1 and 3; §2.4 |
| After cold rolling | Conductivity | Solute state baseline |
| Slug anneal | Air vs N₂ (as planned) × 2 cooling rates (furnace-slow vs faster). **Record the actual heating rate / T(t) of every load**: without homogenisation, heating rate shifts the RX temperature by tens of °C [ch03 §5.2; ch07] | Risk 2a, risk 4 |
| Slugs | HB at **2–6 h**, day 1, **3**, 7, 30 after the anneal (clustering is vacancy-controlled, so the early points matter; depends on cooling rate after the anneal [ch04 §6.5]); grain size and RX fraction; oxide (colour/abrasion, XPS on a subset) | Risk 2b, grain target 20–100 µm |
| Wall simulation | Strip cold rolled to ε ≥ 2, then 220 °C / 10 min: HV before, and **1 and 30 days after** the bake | Bake response (2.2 #3). Storage clusters revert at 200–250 °C, so any gain must come from precipitation or strain ageing on dislocations [ch04 §6.5–6.6] |
| Extrusion | Press force vs slug HB and age; base-corner inspection after extrusion and necking | Risks 1, 2b |
| Cans | Burst / deformation pressure **after the 220 °C / 10 min bake** (the H4x-type lacquered condition) vs current alloy at the same wall | The real strength target |
| Control | Run the current production alloy through the same steps | Baseline |

**Optional sister cast,** if a second melt is possible: same as Talum 1 but Si ≈ 0.25 (Fe:Si ≈ 2) or Mn ≈ 0.25.
That separates the β-phase risk from the Mg effect. Any variant must be re-checked against the patent windows
in ch16.

## 4. Results

*(to be filled after the trial: actual cast analysis, measurements above, observations; this record feeds the
model calibration loop in ch00 §8 / ch18)*
