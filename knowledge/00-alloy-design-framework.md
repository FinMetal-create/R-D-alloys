# 00 — Alloy design framework: lean Al–Mn slug alloys for impact-extruded aerosol cans

**What this is.** This chapter is the synthesis of the knowledge base. It turns chapters 01–18 into one
physical-metallurgy playbook for designing slug alloys and processes. It does not restate the chapters. It
links them, ranks the levers, and says where the evidence is strong and where it is weak.

**How to read citations.**
- `[chNN §x]` points to a chapter in this knowledge base. Follow that chapter's own citation to reach the
  Drive or web source.
- **Evidence grades** used in the tables:
  - **D**: Drive literature, read in full text.
  - **W**: web research, abstract or snippet level only, because full texts could not be fetched in this
    session (chapters 11–18, §0 of each).
  - **I**: in-house data or model (chapter 09).
  - **G**: derived or general knowledge.
- **(Inference)** marks a step of reasoning made in this chapter that no source states directly.

**Status.** Compiled 2026-10-12. Chapters 10 and 18 are referenced where they apply. Every recommendation
here is a hypothesis to test against plant data, not a validated result.

---

## 1. The design problem

**Process chain** [ch09 §0, §5; ch10 §2; ch11]:

```
melt (scrap-rich) → rotary strip caster (22 mm) → in-line hot rolling (≥ 50 %) → cooling bath (quench)
  → [homogenisation?] → cold rolling (CRM, 30–50 %, ε ≈ 0.36–0.69) → slug blanking
  → slug anneal (batch or continuous) → impact (backward) extrusion → necking/shaping
  → internal lacquer cure → aerosol can
```

### 1.1 Requirements

| Requirement | Target or constraint | Controlling microstructure | Where |
|---|---|---|---|
| **Design goal (user, 2026-10-12)** | **Stronger alloy, good to impact-extrude, castable on a rotary strip caster** | Strength from solute, dispersoids and work hardening, balanced against press force and slug ductility; castability set by freezing range, hot tearing and segregation at rotary-caster cooling rates | user; [ch10]; [ch11]; [ch15] |
| Slug hardness | Around 35 HB is acceptable: it means a stronger alloy and is **not** a cap. The earlier "23–33 HB" was inferred from in-house model files [ch09 §2–3] | Fully recrystallised matrix. The level is set by solute (Mn_ss, Mg, Cu), dispersoids and grain size. The practical ceiling is press force and extrudability (R21) | user; [ch10 §2.5] |
| Casting route | **Rotary (wheel-type) strip caster**, **22 mm cast strip → in-line hot rolling ≥ 50 % → cooling-bath quench → cold rolling 30–50 %** (user); narrow strip up to ≈ 20 mm in the literature, typically hot rolled in line; the standard route for aerosol slugs | High cooling rate (finer constituents, more Mn/Fe supersaturation), no ingot homogenisation, centreline segregation, possibly variable cooling from wheel/band contact | [ch15 §1]; [ch11 §3]; [ch02 §4] |
| Slug grain size | 20–100 µm, equiaxed. No pancake grains and no coarse surface grains (orange peel) | Recrystallisation (RX) nucleation density vs Zener drag. Precipitation-before-RX sequence | [ch09 §2–3] (I); [ch03 §5, §7.1] (D) |
| Slug surface | Low MgO (in-house ≲ 7–9 nm). No abrasive oxide | Mg surface segregation and selective oxidation during the anneal | [ch09 §3] (I); [ch14] (W); [ch11 §2] (W) |
| Extrudability | Low punch force, no splits, good wall surface | Low flow stress, high ductility, uniform fine grains, compact constituents | [ch10]; [ch03 §7.1] (D) |
| Can performance | Test pressure ≥ 10 bar or 1.5 × P(50 °C); burst ≥ 1.2 × test pressure; P(50 °C) max 12 / 13.2 / 15 bar depending on propellant | Strength of the heavily cold-worked wall **after** the lacquer cure | [ch11 §4] (W) |
| Lacquer-cure stability | Bake **220 °C / 10 min** (user). Minimise strength loss in the cure (reported up to ≈ 15 % loss during can making) | Recovery / RX resistance of the extruded wall: solute drag, dispersoid pinning | [ch11 §1.2, §4.2] (W) |
| Recycled content | High scrap share; Fe, Si, Cu, Zn pick-up | Fe-phase engineering with Mn, Si control, cooling rate | [ch16 §1, §5] (W); [ch02] (D) |
| Specification | EN 573-3 / AA registration windows for 3102 / 3207 | — | [ch17] (W) |
| Carbon / CBAM | Post-consumer scrap counts as zero embedded emissions. Primary metal carries the charge | Scrap share and provenance | [ch16 §2–3] (W) |
| IP | Patent claim windows overlap lean 3xxx slug chemistries | — | [ch11 §1]; [ch16 §1.5] (W) |

### 1.2 The central tension

**The slug must recrystallise easily. The can wall must resist softening.** The same metallurgical tools act
on both:
- Mn in solid solution;
- fine Mn or Zr dispersoids;
- Mg and Cu solute.

What separates the two steps is **temperature, strain and timing**:
- The slug anneal runs at about 340–420 °C after ε ≈ 0.8–1.2 [ch09 §5; ch03 §4.3].
- The lacquer cure runs at about 200–250 °C for minutes (W, snippet level [ch11 §4.2]), on a wall with true
  strain of order 2–4 [ch10 §2.2].

The design task is to place the alloy so that:
- RX is fast and fine at the slug-anneal temperature;
- recovery is slow at the cure temperature.

The published industrial routes to cure resistance are (i) solute from 3104 scrap (Ball), (ii) Zr dispersoids
(Talum, Moravia patents), and (iii) the lean Al–Mn route of 3102/3207 [ch11 §1.2]. All three trade slug
softness or anneal temperature for wall stability. **(Inference)**

---

## 2. Mechanism map: process stage → physics → levers

| Stage | Controlling physics | State variables to track | Main levers | Chapters |
|---|---|---|---|---|
| Casting | Phase selection in Al–Fe–Mn–Si: Al₆(Fe,Mn) vs α-Al(Fe,Mn)Si vs β-AlFeSi. Mn supersaturation (k ≈ 0.82, mild). Fe macrosegregation (k = 0.03). Cooling rate: DC 1–20 K/s; continuous casting 10–10³ K/s | Mn_ss as cast; constituent type, size and fraction; centreline segregation | Fe:Si, Fe+Mn, Mn/Fe; cooling rate; grain refiner dose | [ch01 §2–4, §8, §11]; [ch02 §2–5, §9]; [ch15] |
| Homogenisation (DC), or none (continuous casting) | Mn precipitation as α-Al(Mn,Fe)Si / Al₆(Mn,Fe) dispersoids. Al₆ → α transformation (needs Si). Coarsening. D_Mn is ≈ 1000× slower than D_Cu | Mn_ss (via conductivity); dispersoid number density, size, volume fraction | T, t, heating rate (slow, ≈ 50–75 °C/h → fine dense dispersoids); stepped cooling (→ low Mn_ss, coarse dispersoids) | [ch03 §5.1]; [ch04 §0, §2]; [ch05 §4.2]; [ch06 §6]; [ch12]; [ch15 §3] |
| Cold rolling (CRM) | Stored energy, ≈ 7 MPa when heavily deformed. Deformation zones round > 1 µm particles (sites for particle-stimulated nucleation, PSN) | ε (true strain); particle size distribution | Total reduction (ε ≥ 0.8–0.95 in-house targets); last-anneal-to-final-gauge strain | [ch03 §1, §3]; [ch07 §5]; [ch09 §5] |
| Slug anneal | **Race between RX and Mn precipitation** (two C-curves). Zener drag P_Z = 3F_Vγ/2r. Solute drag. Mg surface segregation → MgO | X_RX, grain size and shape, Mn_ss, oxide thickness | Heating rate; peak T and time; cold reduction; atmosphere (O₂, dew point); Mn_ss and dispersoid state set upstream | [ch03 §4–6]; [ch12]; [ch14]; [ch15 §3]; [ch09 §2–4] |
| Impact extrusion | Large-strain flow stress and work hardening. Friction. Ductile failure | HB / flow stress of the slug; grain size; constituents | Slug softness; grain size; lubricant | [ch10]; [ch06 §4]; [ch07 §5] |
| Lacquer cure | Static recovery (and possibly RX) of the very heavily strained wall | Wall YS / UTS after the cure | Mg and Mn solute; fine dispersoids (Mn, Zr) | [ch11 §1.2, §4]; [ch03 §2] |

---

## 3. Element playbook for slug alloys

Strengthening coefficients are for **annealed super-purity binaries** unless stated. Multiple solutes add
**less than linearly** [ch05 §6].

| Element | Registered windows (3102 / 3207) | Strength effect | Effect on slug anneal (RX, grain) | Effect on can / cure | MgO | Scrap / CRM | Refs |
|---|---|---|---|---|---|---|---|
| **Mn** | 0.05–0.40 / 0.40–0.8 [ch17] | ΔYS 30.3 MPa/wt % (binary, annealed) [ch05 §6]. Mn in solution: +21 MPa YS (O), +35 MPa (H19) per wt % [ch06 §4] | Supersaturated Mn precipitates during the anneal. Precipitation before RX gives slow RX and coarse pancake grains [ch03 §5.2–5.4]. Only 0.2–0.3 % stays in solution after preheat [ch05 §4.2] | Mn_ss and dispersoids slow recovery → better cure stability (G/Inference) | none | Binds Fe into compact phases; not a CRM issue | [ch03 §5]; [ch04 §0, §2]; [ch16 §5 #3] |
| **Fe** | ≤ 0.7 (3003-class); slug patents use 0.25–0.44 [ch16 §1.5] | Constituents add ≈ 7 MPa per vol % [ch06 §4] | > 1 µm constituents are PSN sites → finer RX grains [ch03 §3]. Fe lowers Mn solubility, so less Mn is available for dispersoids [ch04 §0] | — | — | Main scrap impurity; not removable [ch16 §1.6] | [ch02 §9]; [ch16 §1.2–1.5] |
| **Si** | low (see [ch17]) | ΔYS 9.2 MPa/wt % [ch05 §6] | **Accelerates Mn precipitation** and turns Al₆(Fe,Mn) into α [ch03 §5.1; ch04 §0]. Si-saturated Mn solubility ≤ 0.08 % [ch04 §0]. Free Si drops the solidus to 573 °C [ch01 §11] | — | — | Not removable; control by sorting | [ch01 §4.3]; [ch02 §9] |
| **Mg** | none listed for 3102 (counts as "others" ≤ 0.05 under the usual convention, unverified); ≤ 0.10 for 3207 [ch17] | ΔYS 18.6 MPa/wt % (annealed); +70–85 MPa/wt % in H19 [ch05 §6; ch06 §4] | Solute drag, minor at 0.1–0.3 % [ch09 §9 item 3] | Solute drag on recovery → cure stability (the solute route in the patents) [ch11 §1.2] | **Main driver.** Surface segregation from 100–200 °C; Mg-rich oxide above ≈ 337–400 °C; still active at 0.05–0.1 % Mg [ch14] | EU CRM (Mg) [ch16 §4] | [ch14]; [ch11 §2] |
| **Cu** | ≤ 0.10 both [ch17] | ΔYS 13.8 MPa/wt %. Strongest work-hardening promoter per atom (Cu ≫ Mg ≈ Si > Mn ≫ Zn) [ch05 §6; ch07 §10] | Minor at ≤ 0.1 % (G) | Raises work hardening of the wall | — | Scrap pick-up | [ch05 §4.2] (Cu 0.05–0.2 changes pitting into general corrosion) |
| **Zn** | low | ΔYS 2.9 MPa/wt %; negligible work hardening [ch05 §6] | negligible | — | — | Scrap pick-up | [ch05 §4.2] |
| **Ti (TiB)** | low | — | Finer cast grain. Ti grain refiner raises centreline segregation in sheet ingots; use the minimum effective dose [ch01 §11] | — | — | Accumulates in closed loops [ch16 §5 #9] | [ch01 §5] |
| **Zr** | not in 3102/3207 | Small | Al₃Zr pins boundaries → raises the RX threshold. The slug anneal still has to recrystallise [ch11 §1.2] | **Patent route to cure resistance** (Al–Fe–Mn–Zr, 3207+Zr) [ch11 §1.1] | none | Not a CRM | [ch04 §3, §5]; [ch03 §5.3] (dispersoid-free zones) |
| **Sc** | — | Strongest RX inhibitor. 0.02 % predicted to almost stop RX in 7050 [ch04 §0] | Too strong for a slug that must recrystallise (Inference) | — | — | CRM; poisoned by Si and Fe [ch04 §0] | [ch04 §3, §8] |
| **Cr** | scrap-borne; patent window 0.02–0.10 [ch16 §1.5] | Dispersoids | Retards RX [ch16 §5 #8] | Possible cure stability (G) | — | — | [ch05 §5.2] |

---

## 4. Quantitative rules of thumb

| # | Rule | Value | Grade | Source |
|---|---|---|---|---|
| R1 | Avoid primary Al₆(Fe,Mn) | Fe + Mn < ≈ 2.0 % (3003), < ≈ 1.7 % (3004); continuous casting tolerates more | D | [ch02 §9]; [ch05 §4.2] |
| R2 | Avoid free Si and the low-melting β + Si eutectic | Fe:Si > 1. Fe:Si ≈ 2 gives the worst fir-tree zone in 1xxx; aim for ≈ 3–5 there | D | [ch01 §11]; [ch02 summary] |
| R3 | Mn in solid solution after preheat and hot work | ≈ 0.2–0.3 wt %. As-cast 3003/3103: 0.7–0.9 wt % | D | [ch03 §5.1]; [ch05 §4.2] |
| R4 | Mn solubility with Fe phases present / Si-saturated | 0.23 % at 654 °C, 0.026 % at 427 °C / ≤ 0.08 % below 573 °C | D | [ch04 §0] |
| R5 | Mn diffusivity | D(500 °C) ≈ 5×10⁻¹³ cm²/s (Polmear). Reject Sheppard's Mn row | D | [ch05 §4.2]; [ch07 §11 G9]; [ch13] |
| R6 | Dispersoid nucleation during homogenisation | Slow heating ≈ 50–75 °C/h → fine, uniform dispersoids | D | [ch04 §0]; [ch05 §4.2] |
| R7 | Homogenisation sets Mn_ss (AA3103) | 0.40 → 0.24 → 0.20 → 0.15 at % for as-cast, single step, and stepped slow cooling | D | [ch03 §5.1]; [ch06 §6] |
| R8 | Industrial O-anneal (3207, 3103, 3003, 3105, 3005, 3004) | 380–420 °C, 0.5–1 h metal temperature; fast heat-up | D | [ch03 §4.3] |
| R9 | Fast RX anchor | AA3103 (Mn_ss 0.20 at %), ε = 2, 400 °C salt bath: fully RX in 45 s, 6 µm, no Mn precipitation | D | [ch03 §4.3] |
| R10 | Heating rate and grain shape (supersaturated 3xxx) | Fast (≈ 50 °C/s) → fine equiaxed; ≤ 3 °C/s → coarse. Fine dense dispersoids or concurrent precipitation → pancake grains | W | [ch12]; [ch15 §3] |
| R11 | JMAK parameters are **not constant** across the precipitation window | n falls 3.0 → 0.8 (371 → 427 °C), apparent Q ≈ 456 kJ/mol (one Al–Mn alloy); continuously cast 3xxx n ≈ 2.9 → 0.8, Q 222–539 kJ/mol vs n ≈ 1.5 for DC 3003 | W | [ch12]; [ch15 §3] |
| R12 | Zener pressure | P_Z = 3F_Vγ/2r (random); much stronger when particles sit on boundaries | D | [ch04 §5]; [ch03 §5.3, §6] |
| R13 | Grain-size control in lean 3xxx | Estimated Zener limit from published dispersoid statistics ≈ 3–5 µm, so 20–100 µm slug grains are set by **nucleation density** (G, web-derived). HH's calibrated Zener cap (≈ 0.35–0.47·r/F_V) is smaller still, which supports this | W/G/D | [ch12]; [ch03 §6] |
| R14 | PSN | The critical particle diameter depends on strain: **≈ 3–7 µm at 30–60 % cold reduction**; ≈ 1 µm only at high strain. Efficiency ≈ 14 % of eligible particles, so the **coarse tail of the constituent size distribution** sets nucleus density and slug grain size. Fine precipitates in the deformation zones suppress PSN *(corrected after the HH full-text pass)* | D | [ch03 §3, §3.2b] |
| R15 | Critical-strain coarsening | 3–7 % strain + high-T cycle → very coarse grains (AA3102 tube: ≈ −22 % strength at ≈ 3 % sizing) | D | [ch03 §7.1]; [ch07 §10] |
| R16 | Hall–Petch | k = 0.065–0.07 MPa·m^½ (pure Al); ≤ 0.15 for Mg-free alloys | D | [ch06 §4]; [ch03 §7.2] |
| R17 | O-temper work hardening | 3003-O: K = 188 MPa, n = 0.242; 1100-O: K = 146 MPa, n = 0.242 | D | [ch06 §4]; [ch07 §10] |
| R18 | MgO onset | Mg segregation from 100–200 °C; Mg-rich oxide above ≈ 337–400 °C; inert gas needs O₂ < a few hundred ppm | W | [ch14] |
| R19 | Aerosol pressure rules | Test ≥ 10 bar or 1.5 × P(50 °C); burst ≥ 1.2 × test | W | [ch11 §4] |
| R20 | Thin-wall lightweighting | t ∝ 1/σ_allowable; +10 % post-cure strength ≈ −9 % wall | G | [ch11 §1.2] |
| R21 | Press force vs slug hardness | Ram force follows the slug's **large-strain flow stress**; HB is only a proxy (Rm/HB ≈ 3.6–3.9, or 4.1–4.2 for Mg-bearing O tempers). With Rm ≈ 3.6·HB at ≈ 30:1 reduction, 33 HB needs ≈ 43 % more force than 23 HB, and **35 HB ≈ 52 % more**. At 35 HB a flat-nosed Ø53 punch is estimated at ≈ 391 t, about 98 % of a 400 t press; conical Ø53 is ≈ 326 t. Punch stress is then ≈ 1.4–1.5 GPa, at Kuhn's 1400 MPa die-steel guide value, so tooling becomes a limit too (order-of-magnitude estimates, not validated) | D/G | [ch10 §2.5, §4.1] |
| R22 | What HB means for lean 3xxx slugs | Fully RX lean 3xxx ≈ 23–28 HB (between 1100-O 23 and 3003-O 28 HB). Readings above ≈ 30 HB in **lean** 3102/3207 point to residual cold work (partial RX) or very fine grain. In a deliberately stronger alloy, ≈ 35 HB can be fully recrystallised. Always pair HB with RX fraction and grain size | D/G | [ch10 §4.1, §7] |
| R23 | Base-corner damage | Coarse Fe/Mn constituents nucleate hidden ductile damage at the base corner; it shows up later in ironing or necking | D | [ch10 §5.1] |

---

## 5. Processing-route playbook for slugs

### 5.1 Casting route
- **DC + hot rolling.** Mn supersaturation is partly removed by preheat, leaving 0.2–0.3 % [ch05 §4.2]. Fe
  macrosegregation and the centreline are the main risks; cast speed × diameter ≤ 25,000–33,300 mm²/min
  [ch02 §9].
- **Continuous casting (≈ 20 mm belt-cast strip is the documented slug feedstock; twin-roll gives 3–8 mm)**
  [ch15].
  - Higher Mn and Fe supersaturation and finer constituents [ch05 §4.2; ch15].
  - Without homogenisation, dispersoids precipitate during the slug anneal. That favours coarse, elongated,
    strongly textured grains unless heating is fast [ch15 §3].
  - A high-temperature homogenisation at cast gauge (≈ 580–620 °C class) **accelerated** RX in twin-roll-cast
    3105; a 440 °C treatment did worse [ch15 §3].

### 5.2 The homogenisation decision
Pick the target microstructure from [ch03 §5.4] (table "fine equiaxed vs coarse elongated"):
- **Fine equiaxed slug grains** need low Mn_ss and coarse, sparse dispersoids before cold rolling. That means a
  high-T soak with slow or stepped cooling (R7). Then high reduction and fast heating in the slug anneal (R9,
  R10).
- High Mn_ss at the slug anneal (no homogenisation, or a low-T one) is the recipe for precipitation before RX,
  i.e. coarse pancake grains, unless the anneal heats fast and hot enough for RX to win the race.

### 5.3 Cold reduction
- More reduction raises stored energy and the nucleation density, and lowers the RX temperature and time.
- **Plant vs in-house targets (Assessment).**
  - The actual route is ≥ 50 % hot reduction (22 → ≤ 11 mm), a quench, then 30–50 % cold reduction. For the
    6.1–7.4 mm slugs that gives ε_cold ≈ 0.40–0.59.
  - The in-house CRM tables call for ε ≥ 0.80 (3102) / 0.85 (3207), which needs only 21–38 % hot reduction
    [ch09 §5, §8]. By the tables' own legend, current practice is "red" (ε < 0.55: coarse grain, high scatter,
    orange-peel risk) to "yellow" (0.55–0.84).
  - Hot rolling runs at ≈ 500 → 380 °C (user). Hot strain is partly recovered dynamically; the quench keeps a
    fine subgrain structure that adds some driving force, but it does not substitute for cold strain (general
    knowledge; [ch03 §9]).
  - **Shifting reduction from the hot mill to the cold mill is the most direct process lever** [ch19 P10]. The
    user confirmed the split is flexible per final thickness. Rule: hot-band gauge = t_final·e^(ε_target)
    (≈ 20–38 % hot / 55–60 % cold for 6–7.5 mm slugs). Check that enough hot reduction remains to break up the
    cast structure.
- In-house data already rank this as the strongest process lever: 25 → ≥ 45–55 % CR allows a lower annealing
  T and t, finer grains and less MgO [ch09 §9 item 4].

### 5.4 Slug anneal
- Design the anneal as a **position on the RX / precipitation C-curve diagram**, not as a single T–t point
  [ch03 §5.2, §4.5].
- Include the full T(t) path: ramp, overshoot, and load-position lag [ch09 §9 item 4].
- **Batch vs continuous.**
  - Continuous mesh-belt annealing (fast heating) is used industrially, partly to control abrasive MgO on
    slugs [ch11 §2] (W).
  - Fast heating also favours fine equiaxed grains (R10).
- **Atmosphere.** Inert gas with low O₂ and low dew point limits MgO [ch14] (W).

### 5.5 Extrusion and cure
- Softer, finer-grained, uniform slugs lower punch force and improve the wall surface [ch10].
- Wall strength after the cure is the performance property to design for [ch11 §1.2].

---

### 5.6 Process innovation for the rotary-cast route
See [ch19]. Key point: Mn cannot homogenise at slug-anneal temperatures (it moves only ≈ 0.01–0.05 µm per hour at
350–420 °C). Homogenisation needs ≈ 580–620 °C for ≈ 0.5–4 h. So move Mn precipitation and homogenisation
upstream to the 22 mm cast coil (P1/P2/P5), and/or recrystallise first and precipitate second in a fast slug
anneal (P3/P4).

---

## 6. Assessment of in-house alloys and models

*This section is assessment, not a restatement of in-house data. The data themselves are in ch09.*

### 6.1 Compositions vs registered windows [ch17; ch09 §10]
- In-house "3207 Mn ≤ 0.60" does not match the registered 3207 window (Mn 0.40–0.8).
- 3102 has no registered Mg limit. Under the usual AA/EN convention, Mg is an "other" at ≤ 0.05 % (footnote
  not verified in the source). The in-house 3102 model's Mg = 0.12 % should therefore be checked against the
  customer spec.
- The 3102 model shows Mn as both 0.2 % (title) and 0.3 % (table) [ch09 §2.1].
- The **modified 3102** (Mn 1.10–1.30, Mg 0.25–0.35) is outside both 3102 and 3207. Its window overlaps 3005
  (and 3103 for the lower-Mg part) [ch17]. It would need a different designation.

### 6.2 Modified 3102: expected consequences (Inference, mechanism-based)
- **Strength.** Higher. Mg 0.12 → 0.30 % adds ≈ +3 MPa annealed YS by the binary coefficient, and more in the
  work-hardened wall (+70–85 MPa/wt % in H19 → ≈ +13–15 MPa) [ch05 §6; ch06 §4] (G). Higher Mn adds dispersoid
  and solute strength; the size depends on homogenisation.
- **Slug anneal.** Much higher Mn supersaturation as cast moves the alloy into the slow-RX, heating-rate-
  sensitive regime [ch03 §5; ch09 §9 item 5].
- **Slug hardness and press force.** Fully annealed, it is estimated at ≈ 31–32 HB, versus 23–28 HB for lean
  3102/3207 [ch10 §7] (derived). That is in the stronger range the user is aiming for (≈ 35 HB acceptable). The
  real questions are press force (the highest in the family, R21), full RX at the plant cold reduction, and
  castability on the rotary strip caster.
- **Mg vs Mn.** Per wt %, Mg raises can-wall strength ≈ 2× more than Mn in solution. *Corrected after the
  full-text pass:* per unit of extra press force the two are close under the work method. So choose between them
  on other grounds: MgO, RX behaviour, castability, scrap chemistry [ch10 §3.4, §8].
  The Mg route, however, raises MgO.
- **MgO.** About 2–3× more Mg means more MgO at a given cycle [ch14].
- **IP.** Check against the Ball and Talum claim windows [ch11 §1.1; ch16 §1.5].
- **Verdict.** Viable only if it is co-designed with the process (homogenisation to cut Mn_ss, high CR, fast
  heating, controlled atmosphere) and justified by a quantified wall-strength or lightweighting target. No
  such target exists yet [ch09 §11 Q1].

### 6.3 Recrystallisation models: why they disagree, and how to fix them
The three in-house models differ ≈ 7× in t₅₀ and disagree on grain size [ch09 §9]. Physical reasons, in
order of importance:
1. **One Q and one n across the precipitation C-curve is invalid** for supersaturated 3xxx [ch03 §4.5].
   Measured n and Q move strongly with temperature (R11).
2. **Heating path ignored.** Batch ramps of hours let Mn precipitate before RX; salt-bath data do not
   transfer [ch03 §4.5].
3. **Grain size from a Zener cap.** The AA3207 model's 17.8 µm cap conflicts with the ≈ 3–5 µm Zener limit
   estimated from published dispersoid data (R13). The 20–100 µm grains are better modelled as nucleation-
   controlled: grain size ∝ N_V^(−1/3), with N_V set by PSN sites and stored energy [ch03 §3; ch12] (G).
4. **Calibration.** Each model rests on one unsourced point (e.g. "t₅₀ ≈ 300 s at 350 °C, 70 % CR")
   [ch09 §4].

**Fix (proposal).** Replace the single-JMAK models with a two-process model:
- Mn precipitation, using a KWN or JMAK C-curve, tracked with conductivity;
- RX nucleation and growth whose driving force is reduced by recovery and whose boundaries are dragged by
  Mn_ss and by dispersoids formed **before** RX.

Integrate over the real T(t). Calibrate with the minimal experiments in §8. See [ch04 §4] (KWN equations),
[ch03 §11] (model-ready RX equations), [ch13] (resistivity per solute) and [ch18] (tools).

### 6.4 MgO model [ch14 assessment]
- The in-house model is based on data at 550 °C for 90 h with 0.4–2 % Mg. It has no input for Mg content, dew
  point or atmosphere, and it is unvalidated.
- Its proposed A2 AO-45 cycle forms ≈ 84 % of the oxide at or below 370 °C by the model's own numbers. That
  contradicts its rule that "time above 400 °C drives MgO". Check this against the cell formulas, which the
  Drive export does not show.
- Literature supports the ≈ 400 °C transition (R18). It does **not** support "nil below 350 °C", because Mg
  segregates to the surface at 100–200 °C.

### 6.5 Annealing-window conflict [ch09 §11 Q7]
- The in-house cold-rolling-mill table recommends 340–370 °C for 1–2 h for 3102 at ≥ 55 % CR.
- An in-house JMAK model needs ≥ 7 h at 370 °C.
- The external guideline for 3207/3103/3003 is 380–420 °C for 0.5–1 h with fast heat-up (R8).

The guideline and the table are close, so the slow model is the outlier. Plant hardness and grain-size data
from the existing cycles would settle it.

---

## 7. Candidate development directions

Each direction is a hypothesis to test. They are ranked by expected benefit per unit of risk (Inference).

| # | Direction | Mechanism | Expected effect | Main risks | Decisive experiment |
|---|---|---|---|---|---|
| H1 | **Process first, current alloys.** Higher final CR (≥ 45–55 %), faster heating (continuous or rapid-ramp anneal), lower peak T, inert or low-O₂ atmosphere | More stored energy and nucleation; RX wins the race against Mn precipitation; less time at T for Mg oxidation | Finer, equiaxed grains in the same HB window; shorter cycles; less MgO | Capex for continuous annealing; heat-up uniformity in batch loads | HB, grain size and oxide vs CR × heating rate × T (§8, set A) |
| H2 | **Set Mn_ss deliberately** (homogenisation for DC; high-T at-gauge treatment for continuous casting) | Low Mn_ss at the slug anneal → no precipitation before RX | Robust RX at lower T; less sensitivity to furnace ramp | Energy and CO₂ of the extra step; coarser dispersoids mean less cure stability | Conductivity + HB + grain size after variants (§8, set B) |
| H3 | **Scrap-tolerant window**: Fe ≈ 0.3–0.45 balanced by Mn, Si ≤ ≈ 0.15 (Fe:Si ≥ 2), Mg and Cu capped by MgO and HB | Fe bound in compact Al₆(Fe,Mn) / α; no β; enough PSN particles | Higher recycled share, lower CBAM exposure, stable RX | Coarser constituents (die wear, surface); patent windows | Trial casts across Fe/Si; RX + extrusion trials |
| H4 | **Cure-stable wall** via a dispersoid route (Zr microaddition) rather than more Mg | Al₃Zr pins the wall substructure in the cure without much solute strengthening of the slug | Higher post-cure strength at the same slug HB; lightweighting | Slug anneal must still recrystallise; Zr–TiB interaction; IP (Talum EP 3075875 claims Al–Fe–Mn–Zr) | Cure simulation on heavily rolled strip (§8, set C) |
| H5 | **Modified 3102 (high Mn/Mg)** only as a co-designed package (H1 + H2) with a quantified wall target | Solute and dispersoid strength | Stronger wall | Slow RX, high HB, MgO, designation, IP (§6.2) | Same as H2 + C, against a stated wall/burst target |

---

## 8. Minimal calibration and validation plan

Use inexpensive, high-information measurements first [ch03 §5.2; ch13; ch18].

- **Set A: slug-anneal map.**
  - Strip at 2–3 cold reductions (e.g. 25 / 45 / 70 %).
  - Anneals at 3–4 temperatures (≈ 320–420 °C) and 2 heating rates (furnace ramp vs fast).
  - Measure HB vs time (softening curves), electrical conductivity (Mn_ss; coefficients in [ch13]), grain size
    and shape (optical/EBSD), and oxide (colour/abrasion test, ideally XPS or GDOES on a subset).
- **Set B: Mn_ss control.** As-cast vs 1–2 homogenisation variants. Measure conductivity and dispersoid
  size/density (SEM/TEM on a few samples) before cold rolling. Then repeat a reduced version of set A.
- **Set C: cure stability.** Heavily cold-rolled strip (ε ≥ 2) or extruded can walls. Cure simulation at the
  real lacquer schedule. Measure HB / tensile before and after.
- **Model use.** Fit the two-process model (§6.3) to sets A–B with Bayesian calibration. Use the posterior to
  choose the next experiments (active learning) [ch18].
- **Suggested low-cost toolchain** [ch18] (W):
  - pycalphad + scheil for phase selection during solidification;
  - kawin (Python KWN) for Mn dispersoid precipitation and Zener-pinned grain growth;
  - a custom ALSOFT-type recovery/RX module;
  - PyMC hierarchical Bayesian calibration on HB, conductivity, EBSD and DSC data (≈ 9 isothermal softening
    curves plus 2–3 hold-out industrial cycles per alloy);
  - BoTorch/Ax to optimise composition and process.

  **Caveat:** the free COST 507 database splits α-Al(Mn,Fe)Si into separate Fe-free and Mn-free phases, so it
  cannot represent the 3xxx dispersoid. Either refit the Al–Mn–Fe–Si description (ESPEI), or buy a short
  commercial Al-database licence (TCAL or PanAl) [ch18].

---

## 9. Evidence gaps and how to close them

1. **Blocked web full texts.** The environment's network policy blocked all publisher hosts. Chapters 11–18
   are therefore abstract or snippet level. Allowing the domains listed in [ch12 §8], [ch11 §6] and [ch13]
   and re-running those agents would upgrade W-grade rules to D-grade.
2. **Truncated Drive books.** The books are in Drive, but the Drive connector caps what it returns:
   - **Text reading** stops around 110–390 k characters per file.
   - **Whole-file download** works up to about **6 MB** per PDF. Measured 2026-10-12: Kaufman 6.09 MB
     succeeded; *Rolling Aluminum* 7.19 MB and Polmear 9.68 MB failed with "message too large"; files over
     10 MB are refused outright.

   The truncated sources under the limit have been read in full (Dwight, Kaufman, Schröder, EAA, Belov, Davis,
   the blister paper, Junit, Farrar, Everhart and Thienel; see each chapter's coverage table). Books above the limit
   can be read in full once they are saved in Drive as parts of **≤ ~5 MB** each:
   - Totten, *Handbook of Aluminum* Vol. 1 (17.7 MB);
   - Humphreys & Hatherly (12.7 MB);
   - Ryen (11.2 MB);
   - Sheppard (10.5 MB);
   - Polmear (9.7 MB);
   - *Rolling Aluminum* (7.2 MB).

   The parts most worth having:
   - Humphreys & Hatherly beyond §6.5 (RX kinetics, PSN, ch. 9 two-phase alloys, textures);
   - Polmear §3.6.5 (canstock and foil);
   - Sheppard ch. 4 (constitutive constants);
   - Totten Handbook of Aluminum Vol. 1 ch. 7–8 (rolling, extrusion);
   - Ryen ch. 4.5–5 (per-solute work-hardening results);
   - the Schuler handbook's cold-extrusion chapter (pp. 443–480).

   Sillekens was recovered in full by downloading the PDF [ch10 §1]. Files over ≈ 10 MB cannot be downloaded
   this way.
3. **In-house calibration data** are the binding constraint for every model [ch09 §11 Q4–Q5]: measured
   softening curves, grain sizes, conductivity and oxide thickness for the existing cycles.
4. **Targets.** No wall-strength, burst-pressure or cure-softening target is stated anywhere [ch09 §11 Q1].
   Set them before choosing between H3, H4 and H5.
5. **IP.** Verify the patent claims cited in [ch11 §1.1] and [ch16 §1.5] (snippet level), and run a
   freedom-to-operate review before fixing a new composition window.
6. **Open data conflicts** (do not pick a value silently):

   | Quantity | Conflict | Sources |
   |---|---|---|
   | D_Mn in Al | Sheppard's row is ≈ 10³× faster than Polmear's. Use Polmear | [ch07 §11 G9]; [ch13] |
   | D_Sc / D_Zr at ≈ 480 °C | ≈ 4 in the KWN parameters of ch04, vs ≈ 510 [ch13] and ≈ 640 [ch18] from diffusion data. Recheck before any Sc/Zr modelling | [ch04 §11]; [ch13]; [ch18] |
   | Mn "solubility" 1.82 vs 1.25 wt % | Not a real conflict. 1.82 % is the maximum equilibrium solubility at 658 °C; ≤ 1.25 % is the practical commercial ceiling set by the primary-Al₆(Fe,Mn) risk | [ch05 §4.2]; [ch13] |
   | H3x stabilisation temperature | 120–150 °C [Polmear] vs ≈ 180 °C [Rolling Aluminum] | [ch07 §11 G10] |
   | Fe:Si for 1xxx fir-tree control | "≈ 3" [ch01] vs "3–5, worst at ≈ 2" [ch02]. These are consistent ranges, not a contradiction | [ch01 §11]; [ch02] |
