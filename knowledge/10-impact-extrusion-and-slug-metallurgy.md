# 10 — Impact extrusion (backward can extrusion) of aerosol cans and slug metallurgy

> Compiled 2026-10-12. **Scope:** the chain *slug composition → cold rolling → blanking → slug anneal → slug
> microstructure/properties → backward can extrusion (mechanics, loads, friction, heat) → can-wall properties and
> defects*, for lean 3xxx slugs (EN AW-3102, "modified 3102" Mn 1.10–1.30 / Mg 0.25–0.35, AA3207) and 1xxx reference
> grades. Recrystallisation kinetics, MgO models and the CRM reduction tables are **not repeated here** — they are in
> chapter 09 (§2–§5); Fe/Mn intermetallics are in chapter 02; generic cold rolling/texture in chapter 07; solute
> coefficients in chapters 05 §6 and 06 §4. This chapter cross-references those and adds the extrusion side.
>
> **Conventions.** Every claim is cited `[S-0xx, p./§]` (keys from `sources/catalog.md`; printed page numbers unless
> "PDF p."). Own working files use `W-xx` keys and chapter-09 section numbers. *(derived)* = my arithmetic on cited
> numbers (assumptions stated). *(digitised)* = read off a rendered figure, accuracy ≈ ±3 MPa / ±2 HB / ±1 % A10.
> *(inference)* = design conclusion drawn from cited facts. *(general knowledge)* = not in any source read; kept
> minimal. ⚠ = equation reconstructed from garbled OCR or image; verify before use.

---

## 1. Sources and coverage

| Ref | Work | Drive link | Readability / how far the text goes |
|---|---|---|---|
| **S-053** | W.H. Sillekens, *Backward Can Extrusion and Materials Behaviour*, PhD TU Eindhoven 1992 (DOI 10.6100/IR374925) | https://drive.google.com/file/d/19TZFzxjO1cFP7k7mwdfrpcEXIbSRYG2z/view (dups 1FgOlZBrGWWfSCsEn9pe44eb10MEYShxy, 1u7fg8Mrxj0ha6NwDE3Z79OHEJ-VLEw2u, 1n2OYmFBOJJitAFgIRO00wbGtSTIEMvWa) | `read_file_content` returns **109,131 chars for all four copies (identical)**, ending at Fig. 4.11, printed p.67 — Ch.4.3, **Ch.5 and App. C are not in that export**. The PDF itself (3.64 MB, 143 PDF pages) was therefore downloaded and text-extracted: **Ch.1–6 and App. C read completely** (pp.1–126). App. A (extra steel/brass flow curves) and App. B (error analysis) not read (not Al-relevant). Many equations are images and are garbled (⚠); Figs 2.5, 2.6, 3.4, 3.8, 5.2, 5.3, 5.6 were read from rendered page images. **Material studied is rapidly-solidified recycled car-shredder scrap (Al-6Si-3Cu), not 3xxx.** |
| **S-052** | Ø. Ryen, *Work Hardening and Mechanical Anisotropy of Aluminium Sheets and Profiles*, Dr.Ing. NTNU 2003 | https://drive.google.com/file/d/1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_/view (dup 1UzIUO6x8LEca1klH_1--rFxKuoXwsVhI) | `read_file_content` returns **132,953 chars (both copies identical)**, ending at **printed p.70 (§4.2.1, Fig. 4.6)**; the Drive search snippet (MAX) is the same text. Download refused (11.2 MB > 10 MB limit). **Read:** abstract, Ch.2 theory (pp.7–50, incl. the Nes work-hardening model), Ch.3 materials/processing (pp.53–63), §4.1–4.2.1 (pp.65–70). **Not reached:** §4.2.2–4.5 (incl. §4.5.2 AA3103 work-hardening curves, p.90), **Ch.5 (solute effects stage II–IV, particle & grain-size effects, model application, pp.97–130)**, Part B. Hence **no per-solute MPa coefficients from Ryen's own results** — only the abstract's conclusions. |
| **S-051** | T. Vasevska, "Utrjevanje aluminija in zlitin pri vzdolžnem hladnem valjanju", *Mater. Tehnol.* 38(3–4) 191 (2004) (SL) | https://drive.google.com/file/d/1wpVR73nujVXO1OfmvV57CzuvwR__bdRc/view | Full PDF downloaded (5 pp., pp.191–195), read and translated completely. **No hardening equation in the text**; the property-vs-reduction curves (Figs 3–6, Al99.5) were **digitised** from rendered images (§3.1). |
| **S-046** | Schuler, *Metal Forming Handbook* (Springer 1998) | https://drive.google.com/file/d/1n5Yidy74bZxj6ZifvCNtq0iRtk2nyh43/view | `read_file_content` returns 124,942 chars, ending in **§3.2 (press design, ≈p.60 of ~560)**. The cold/impact-extrusion chapter (**Ch.6: §6.3.2 "Billet or slug preparation" p.454, §6.3.3 surface treatment p.459, §6.5.3 backward cup extrusion p.474, §6.5.5 ironing p.476**) appears only in the table of contents — **not reached**. Download impossible (28.6 MB). Only §2.2 basics used. |
| **S-031** | J.R. Davis, "Aluminum and Aluminum Alloys", *Alloying: Understanding the Basics*, ASM 2001, pp.351–416 | https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view | Full PDF downloaded; complete. Used for solute coefficients and particle/ductile-fracture statements (also used in ch.05). |
| **S-055** | MPMA, "How aluminium aerosol cans are made" (info sheet) | https://drive.google.com/file/d/1Ul9kcbJAllC4ufhIsV3Xr2tkhjW6TBSW/view | Full (5 pp.). Process steps only. |
| **S-056** | Ardagh Group, *Metal Packaging Solutions: Steel and Aluminium Aerosols* (2015) | https://drive.google.com/file/d/1C_DUB748Ikw3LP4pcp97tQmoCn5js5uF/view | Full (8 pp.). Product range only. |
| **S-057** | Mall + Herlan, CMC 200/250 monobloc aerosol-can lines | https://drive.google.com/file/d/1MFEG_JSZSKkmzXpRJ5lF58iiv7MBxnvX/view | Full (2 large pages; columns interleaved but readable). Line data incl. press force. |
| **S-058** | Hinterkopf, N40.2 necking machine | https://drive.google.com/file/d/1rox7kzRaTGK_jAjUQrKQIBs06yvEmHQ_/view | Full (8 pp.). |
| **S-059/S-060** | "Basic punching (theory)", Mate Precision Tooling slides 62–63 (.jpg) | https://drive.google.com/file/d/13cVKT8DZmNansFOdGiUpKPv8JrAiXkNY/view · https://drive.google.com/file/d/15cVOvSbU5hiY7Gkdp7PZg2cOd1ib6CHM/view | Image labels only (slug edge zones). |
| cross-refs | S-028 Polmear, S-029 Totten *Handbook of Aluminum*, S-030 Kaufman, S-043 EAA *Aluminium in Commercial Vehicles* | links in `sources/catalog.md` | **Not re-read**; quoted via chapters 05/06/07 with the original page numbers. |
| W-02, W-08, W-09, W-13, W-15/16, W-17/18, W-22/23, W-03 | User's working files | see ch.09 file inventory | Values quoted from ch.09, not re-read. |

**Searched but nothing usable for this chapter:** Sheppard *Extrusion of Aluminium Alloys* (S-045; both copies >10 MB, download
failed; covered in ch.07 §8 for hot extrusion); Higgins (S-075; 169,189-char export contains no impact-extrusion text);
Maggs fir-tree-zone thesis (S-015; the full-text hit lies beyond its 158,688-char export); Polmear (download failed;
canstock §3.6 missing per ch.05); Dwight and Davis contain no impact-extrusion content; W-01 `Untitled0.ipynb` is a
non-technical aerosol-industry news-tracker script. **Excluded as instructed:** every hit inside
`microstructure-sim-v2.14.0` (e.g. `src/models/deformation.js`, `flow.js`, `strength.js`, `mgo.js`, run CSVs,
`MGO.md`) — parent folders verified to be `src/` and `src/models/` of that tree.

---

## 2. Process chain and line data

### 2.1 Line sequence (monobloc aerosol can)
1. **Slug**: discs of the same diameter as the finished can are punched from thick Al sheet [S-055 step 1]. In-house:
   slug thickness 6.1–7.4 mm for Ø45–53 mm cans (ch.09 §8, W-22/W-23).
2. **Lubrication**: slugs are tumbled in a lubrication drum, then separated and aligned [S-057, item 1–2].
3. **Impact extrusion**: the slug in the die is struck at high speed by a reciprocating punch and flows "without
   addition of heat" back along the punch to form a closed-end can [S-055 step 2]. Press force **up to 400 tons**
   [S-057, item 3].
4. **Ironing machine** immediately after the press: "the wall thickness is optimised and the bottom of the cylinder is
   formed … permits more uniform and more lightweight cans" [S-057, item 4]. → The impact-extruded wall is **not**
   necessarily the final wall; an ironing pass follows on M+H lines.
5. Trimming (removes "the surplus irregular edge") and brushing [S-055 step 3; S-057 item 6]; washing (water + detergent
   at 80 °C) and drying [S-057 items 7–8]; internal lacquer spray, **inside-bake oven (IBO)** for lacquer curing
   [S-057 items 10–11; S-055 steps 5–6]; base coat, print (up to 8–9 colours), overvarnish, pin-chain ovens [S-055
   steps 6–9; S-057 items 13–16].
6. **Necking**: ≈15 swaging steps [S-055 step 10]; N40.2 necker has 40 stations, up to 220 cans/min; deep necking
   ("waist") in 3–6 steps followed by re-expansion in 3–6 steps; all necking is done on the **lacquered, decorated**
   can, so "the lacquer has the right elasticity" is vital; can Ø 35–53 or 45–66 mm, trimmed length 70–300 mm [S-058
   pp.2–4, 8].
7. **Leak/pressure test**: rejects pinholes/fractures [S-055 step 11]; leak detector resolves micro-leaks down to
   **50 µm** [S-057 item 19].
- Line rate **200/250 cans/min**, 19 machines, >60/75 million cans/yr [S-057 tech. data] → **0.24–0.30 s per press
  cycle** *(derived)*. Ardagh's Al aerosol range: Ø35–66 mm, heights 70–277 mm (Ø53: 115–260 mm, 210–520 ml)
  [S-056 p.6]; the in-house sizes (Ø45–53, H 171–210 mm) are inside it.

### 2.2 Deformation measures and the in-house geometries
- Extrusion ratio R = A₀/A₁ and reduction r = (A₀−A₁)/A₀; for cylindrical cans R = R_C²/(R_C²−R_R²) (R_C chamber,
  R_R ram radius) [S-053 pp.2–3, Eqs 1.1–1.2]. Low-strength materials (CP-Al, Pb, Zn) reach **R ≫ 10 (r > 0.90)**,
  steel much less [S-053 p.3].
- Homogeneous (minimum) wall strain = ln R *(general knowledge)*.

| Can (ch.09 §8) | Ø / wall t (mm) | R = R_C²/(t(2R_C−t)) | r | ln R | Slug T₀ (mm) | T₀/R_R |
|---|---|---|---|---|---|---|
| 45 × 200 | 45 / 0.35 | 32.4 | 0.969 | 3.48 | 6.6 | 0.30 |
| 50 × 185 | 50 / 0.40 | 31.5 | 0.968 | 3.45 | 6.3 | 0.26 |
| 53 × 171–210 | 53 / 0.44 | 30.4 | 0.967 | 3.41 | 6.1–7.4 | 0.23–0.28 |

*(derived; assumes slug Ø = die Ø and that t is the as-extruded wall — if the M+H ironing step thins the wall, the
extrusion R is lower.)* → **Wall true strain ≥ 3.4**, plus redundant shear; R ≈ 30 is ~3× beyond the R = 10 example
analysed by Sillekens. T₀/R_R ≈ 0.25–0.3 means "low billets" (H/R_R < 1), the regime where his three-zone/two-zone
models govern [S-053 pp.22–23, Figs 2.7–2.8; p.81] *(inference)*.

### 2.3 Stages, flow pattern and force–stroke course
- Backward can extrusion is **instationary**: process variables depend on ram penetration [S-053 p.9]. Tooling: ram
  (often with a slightly **conical nose** for stability; shaft relieved so only the **ram land** touches the wall),
  chamber, ejector, stripper; lubricant on the billet prevents metallic contact and reduces loads [S-053 p.2].
- Upper-bound analyses assume rigid–perfectly-plastic material (constant σ₀) and constant-shear friction
  **τ_fr = m·σ₀/√3**, m = 0 (frictionless) … 1 (sticking) [S-053 p.11, Eq. 2.2].
- Four models, each with its own validity range [S-053 pp.12–25]:
  - *Spherical model* (Avitzur; flat ram, spherical-shell active zone, optimised semi-cone angle α_opt; dead zones
    under the ram) — early stage; α_opt = 42° at R = 2, 17° at R = 10 [S-053 pp.12–14, Figs 2.5–2.6].
  - *Extended three-zone model* (dead zone in the bottom, optimised zone height S_opt/R_R = 0.613 at R = 2, 0.196 at
    R = 10) — early stage of high-R extrusion [S-053 pp.17–18, Figs 2.5–2.6].
  - *Three-zone model* (Kudo: compression zone under ram, corner zone turning the flow, rigid wall) — final stage
    [S-053 pp.15–17].
  - *Two-zone model* (Avitzur) — very end of stroke [S-053 pp.14–15].
  - The governing model is the one giving the **lowest pressure** at each stroke position ("enveloping lowest curve")
    [S-053 p.21]. For R = 2 the spherical model governs early, three-zone late; for R = 10 the sequence is extended
    three-zone → three-zone → two-zone at the very end [S-053 p.21].
- In the quasi-stationary early stage the pressure **rises linearly with stroke** because the friction area grows;
  slopes depend on m only [S-053 pp.19–20]. Late in the stroke the pressure first falls, then **rises again** as the
  bottom thins [S-053 p.20; p.83].
- Visioplasticity (Kast): a dead zone forms under the ram at R ≈ 1.46 (spheroidal active zone); **no dead zone and a
  flat active zone at R ≈ 3.56** [S-053 p.23] → at R ≈ 30 a thin, flat compression zone under the ram is expected
  *(inference)*.
- Measured force–stroke (recycled Al, 230 °C; R_C = 6, R_R = 5 mm, T₀ = 4, T_e = 1 mm): steep initial rise to
  ≈30–35 kN within ≈1 mm, then a slowly rising plateau to ≈45 kN at 3 mm stroke; the model fits m ≈ 0.4 "apart from
  the initial stage" [S-053 p.85, Fig. 5.3 (read from image)]. The initial transient (filling/upsetting) is not
  captured by the models.

### 2.4 Pressure and force equations

| # | Relation | Use / validity | Source |
|---|---|---|---|
| P1 | **p_max = [a·ln R + b]·σ_UTS**, p = max ram force / billet cross-section; **non-ferrous a = 3.14, b = 0.80** (steel 2.80/0.75); conical-nose ram; **flat ram ×1.2** | Empirical (Boes & Pouw); quick press-capacity check; validity range in R not stated | [S-053 p.10, Eq. 2.1] |
| P2 | Slab (Dipper double-compression), thin-walled, no dead zone: **p_R/σ₀ = 1 + 2/√3 + (1+m)/(2√3)·T/(R_C−R_R) + (2m/(3√3))·R_R/T** | Mean ram pressure vs residual bottom thickness T; R > 2–2.5; low billets | [S-053 p.83 Eq. 5.7; App. C Eq. C.20, p.122] |
| P3 | Power (upper-bound) analysis of the same three-zone field differs from P2 only in the Γ₂-shear + bottom-friction term; differences "marginal" | Same | [S-053 p.83, Fig. 5.2] |
| P4 | Global strain for converting p/σ₀ to force (Dipper): ε_I = ln(T₀/T); ε_II = ln(T₀/T)·[1 + R_R/(4(R_C−R_R))]; volume-weighted mean ε_glob = (ε_I V_I + ε_II V_II)/(V_I+V_II) (Schmitt); then σ₀ = σ_f(ε_glob) | Strain-hardening correction | [S-053 p.84, Eqs 5.9–5.10] |
| P5 | Upper-bound envelope values, m = 0.1, h/R_R = 0.1: **p_R/σ₀ ≈ 3.5–3.8** for R = 2 (R_C/R_R = 1.41, H/R_R = 2); **≈ 4.7 rising to ≈ 5.4** then dipping to ≈ 4.5 and rising sharply at the end for R = 10 (R_C/R_R = 1.05, H/R_R = 1) | Shape of p(stroke) | [S-053 pp.20–21, Figs 2.5–2.6, read from images] |
| P6 | Slab/power example (R_C/R_R = 1.2, T₀/R_R = 0.8, T_e/R_R = 0.2, m = 0.2): p_R/σ₀ ≈ 3.7 at start → ≈ 2.9 (slab) / 3.2 (power) near the end; normal (compressive) stresses on ram and chamber up to ≈ 3.9 σ₀ (values 1.84–3.93 σ₀ shown for initial and final ram position; assignment to faces not legible in the OCR ⚠) | Tool-stress estimate | [S-053 pp.84–86, Figs 5.2, 5.4] |
| P7 | Direct forming force F = A·k_w with forming efficiency η_F = k_f/k_w; specific work w = ∫k_f dφ ≈ k_fm·φ (arithmetic mean of entry/exit flow stress allowed) | Generic | [S-046 §2.2, pp.26–28] |

Check of P2 against Fig. 5.2: start (T/R_R = 0.8) → 3.64, end (0.2) → 2.89 — matches the plotted curve *(derived)*.
Empirical formulas and nomograms (Schmitt; Burgdorf & Müschenborn ±10 %) are adequate for press capacity [S-053
pp.10, 27].

### 2.5 Worked estimates for the in-house cans *(derived — order-of-magnitude, not validated)*
**(a) Empirical press force (P1).** Factor a·ln R + b = 11.7 (Ø45), 11.6 (Ø50), 11.5 (Ø53). With slug σ_UTS
≈ 83–119 MPa (the 23–33 HB window converted with Rm ≈ 3.6·HB, §4.1):

| Can | A₀ (mm²) | p_max (MPa) at 23 → 33 HB | F_max conical ram | F_max flat ram (×1.2) |
|---|---|---|---|---|
| Ø45 | 1590 | 970 → 1395 | 1.55 → 2.22 MN (158 → 226 tf) | 190 → 271 tf |
| Ø50 | 1963 | 965 → 1384 | 1.89 → 2.72 MN (193 → 277 tf) | 232 → 332 tf |
| Ø53 | 2206 | 956 → 1371 | 2.11 → 3.02 MN (215 → 308 tf) | 258 → 370 tf |

→ Consistent with the 400 t press rating [S-057]; **force scales linearly with slug UTS (≈ HB): the 33-HB end of the
window needs ≈ 43 % more force than the 23-HB end**, and a flat-nosed Ø53 punch at 33 HB approaches the press rating.

**Update (2026-10-12): the user's slug limit is ≤ 35 HB**, not a 23–33 HB window. At 35 HB, Rm ≈ 126 MPa, and the
same factors give *(derived, same caveats)*:

| Can | p_max at 35 HB (MPa) | F_max conical ram | F_max flat ram (×1.2) |
|---|---|---|---|
| Ø45 | ≈ 1474 | ≈ 2.34 MN (≈ 239 tf) | ≈ 287 tf |
| Ø50 | ≈ 1462 | ≈ 2.87 MN (≈ 293 tf) | ≈ 351 tf |
| Ø53 | ≈ 1449 | ≈ 3.20 MN (≈ 326 tf) | ≈ 391 tf, about 98 % of the 400 t rating |

That is ≈ +52 % force vs 23 HB. At the hardness limit, a flat-nosed Ø53 punch has essentially no press margin, so
for that geometry press capacity rather than the HB specification may be the binding constraint.
Sensitivity: dp/dσ_UTS ≈ 11.5 → **+10 MPa slug UTS ≈ +115 MPa ram pressure ≈ +0.25 MN (+26 tf) on Ø53**.

**(b) Slab model (P2) for Ø53 (s = R_C−R_R = 0.44 mm, R_R = 26.06 mm).** p_R/σ₀ = 2.155 + a·T + b/T with a = 0.2887
(1+m)/s, b = 0.3849·m·R_R. Minimum at T* = √(b/a): m = 0.05 → T* = 0.85 mm, p/σ₀ = 3.33; m = 0.1 → 1.18 mm, 3.86;
m = 0.2 → 1.60 mm, 4.67. At T = 1 mm the bottom-friction term b/T is 0.50 (m 0.05), 1.00 (m 0.1), 2.01 (m 0.2), i.e.
**for large-diameter, thin-based cans the friction term m·R_R/T dominates the end of stroke** → lubricant (and anything
that degrades it, e.g. surface oxide condition) controls peak force *(inference)*. With σ₀ ≈ 190–250 MPa (flow stress
at ε ≈ 3.4 from §3.1) p ≈ 0.73–0.97 GPa at m = 0.1 — 20–30 % below the empirical P1 value (P2 omits redundant shear at
the zone boundaries) *(derived)*.
**(c) Dipper's strain (P4) cannot be used at R ≈ 30**: R_R/(4s) ≈ 15 gives ε_II ≈ 16·ln(T₀/T), i.e. strains ≫ 10
*(derived)*. Use ln R (≈ 3.4) as the wall strain and FE for local values.

### 2.6 Friction and lubrication
- Lubricant on the billet prevents tool–workpiece metallic contact and lowers loads [S-053 p.2]. Cold extrusion of
  steel only became possible with a **zinc-phosphate lubricant-carrier layer** that prevents cold welding [S-053 p.4] —
  i.e. galling is a surface-layer/lubricant problem, supporting the ch.09 §1 assessment that 0.05–0.10 % Cu is not an
  anti-galling measure *(inference)*.
- Friction factors used: m = 0.1 (model examples) [S-053 p.19]; best fit **m ≈ 0.4** for recycled Al at 230 °C with
  Molykote HTF, but "ambiguous to conclude a definite value" [S-053 pp.85, 93]; FE used Coulomb μ = 0.1 [S-053 p.93].
  Fig. 5.3: predicted force at 3 mm stroke ≈ 38 kN (m = 0), ≈ 42 (m = 0.2), ≈ 46 (m = 0.4), ≈ 65 kN (m = 0.8), i.e.
  friction from m = 0 to 0.8 adds ≈ 70 % at this low R [S-053 p.85, read from image].
- Industrial Al slug lubricant (zinc stearate, tumbled) is **not described in any source read** [S-057 only says
  "lubrication drum"] *(zinc stearate: general knowledge)*.
- Tool–workpiece interface (friction, lubrication, wear) and surface reactions with the atmosphere are separate problem
  areas (4 and 6) in the Lange systematics adopted by Sillekens [S-053 pp.5–6] → the annealing **MgO surface oxide
  belongs to these areas**; no source quantifies its effect on m (gap, §10).

### 2.7 Temperature rise and strain rate
- Backward can extrusion is "usually practised at room temperature"; difficult products may need warm extrusion
  [S-053 p.1]. Below the recrystallisation temperature the flow stress rises with strain and **strain rate has minimal
  influence**; above it, temperature and rate dominate [S-046 §2.2.1 p.26].
- Plastic work → heat; in rolling, cooling prevents the temperature reaching recovery/RX levels [S-051 p.195]; strip
  temperatures of 100–150 °C occur in commercial cold rolling at ε̇ ≈ 50–100 s⁻¹ [S-052 p.10].
- **No measured temperature or strain-rate data for impact extrusion in the sources.** Adiabatic estimate
  ΔT = β·∫σdε/(ρc) *(formula general knowledge; β ≈ 0.9, c ≈ 0.9 J g⁻¹K⁻¹, ρ = 2.70 g cm⁻³)*: with the Al99.5 curve of
  §3.1 integrated to ε = 3.45 (≈ 546 MJ m⁻³) → **ΔT ≲ 200 K** in the wall *(derived upper bound: ignores heat flow
  into tools and thermal softening)*. The stroke time is < 0.24–0.30 s (cycle time, §2.1) *(derived)*.
- Consequence: the wall deforms partly "warm"; Sillekens' data show that higher temperature lowers both C and n of the
  flow curve, and **low n promotes strain concentration and failure** [S-053 p.47] *(transfer to 3xxx: inference)*.

---

## 3. Flow stress and work hardening

### 3.1 Flow-curve data available

**Table 3-1 — Al99.5 hot-rolled strip, cold rolled in one direction, longitudinal (Vasevska Fig. 3)** [S-051 p.193,
Fig. 3, *digitised*]; Fig. 5 (reversing passes) agrees within ≈3 MPa / ≈2 HB [S-051 Fig. 5].

| Reduction e (%) | 0 | 10 | 20 | 30 | 40 | 50 | 60 | 70 | 80 | 90 |
|---|---|---|---|---|---|---|---|---|---|---|
| True strain ε = −ln(1−e) | 0 | 0.105 | 0.223 | 0.357 | 0.511 | 0.693 | 0.916 | 1.204 | 1.609 | 2.303 |
| Rm (MPa) | 84 | 92 | 107 | 118 | 126 | 138 | 148 | 156 | 165 | 182 |
| Rp0.2 (MPa) | 57 | 88 | 105 | 117 | 125 | 136 | 144 | 153 | 160 | 176 |
| HB | 23 | 26 | 33 | 37 | 38 | 40 | 42 | 43 | 45 | — |
| A10 (%) | 42 | 28 | 12 | 8.5 | 7.5 | 7 | 6 | 5.5 | 4.5 | 3.5 |

- **Fit (derived): Rp0.2 ≈ 147·ε^0.22 MPa** for 0.1 ≤ ε ≤ 2.3 (residuals ≤ 3 MPa); HB ≈ 42·ε^0.16 for 0.2 ≤ ε ≤ 1.6.
  Extrapolated to the wall strain ε ≈ 3.4: ≈ 190 MPa (cold, no recovery) *(derived)*.
- Transverse Rm/Rp0.2 exceed longitudinal by 7–20 MPa (one-direction rolling) and 3–9 MPa (reversing); transverse A10
  is lower at small reductions; reversing the rolling direction does not change properties or microstructure
  [S-051 p.194]. ≤ 30 % reduction only flattens grains; > 50 % longitudinal and transverse microstructures look alike;
  pronounced banding only > 90 % [S-051 p.195].
- **O-temper Hollomon constants** (tension) [S-029 Ch.3 Table 3, via ch.07 Table 5-1 / ch.06 Table 4.1]: 1100-O
  n = 0.242, K = 146 MPa; **3003-O n = 0.242, K = 188 MPa** (same n, +29 % K). Extrapolated to ε = 3.4: 3003 ≈ 253 MPa
  *(derived; tensile Hollomon fits are not reliable to ε ≈ 3)*. Rolling form YS = σ₁·εⁿ [S-029 via ch.07 §5.2].
- **Recycled RS Al (Al-6Si-3Cu-1.5Zn-0.7Fe)**, tension, annealed 350 °C/20 min: C ≈ 340 MPa / n ≈ 0.18 at 20 °C,
  falling to C ≈ 75–100 MPa / n ≈ 0.07–0.10 at 300–350 °C [S-053 p.40, Fig. 3.4, read from image]; C = 176 MPa,
  n = 0.13 used at 230 °C [S-053 p.85]. Reproducibility indicator I ≈ 6 % (C), 24 % (n) in tension [S-053 p.39].
- Flow curves used for extrusion should be **compression** curves (Rastegaev specimens with lubricant pockets keep
  uniaxial stress to large strain; measuring diameter rather than height improves accuracy) [S-053 pp.54–55, 69, 74].

### 3.2 Strain-path dependence (Sillekens Ch.4) — why the slug test matters
- Compression, torsion and tension flow curves of the same annealed material **do not coincide** (Hollomon fits,
  correlation R ≥ 0.9895): C22 steel C/n = 832/0.197 (compression), 756/0.232 (tension), 670/0.172 (torsion); Armco
  595/0.250, 560/0.292, 471/0.214; CuZn37 750/0.504, 759/0.503, 477/0.403 [S-053 p.62, Table 4.2]. "These parameters
  are not to be treated as material constants" [S-053 p.75]. No aluminium was tested in Ch.4.
- Causes: texture/microstructure evolve differently by mode (Taylor factor rises in tension/compression, falls in
  torsion) [S-053 pp.70–71]; **hydrostatic-pressure sensitivity** σ_f(p) = σ_f(0)·(1 + w·p) ⚠(form inferred from the
  GPa⁻¹ units), w ≈ 0.1–0.4 GPa⁻¹ for various metals (Herbertz & Wiegels), C22 ≈ 0.7, Armco ≈ 0.5 ⚠(OCR), CuZn37 ≈ 0
  [S-053 pp.71–72]. **No w for aluminium in the sources**; at the ≈ 1 GPa pressures of §2.5 even w = 0.1 GPa⁻¹ would
  matter (+10 %) *(derived)*.
- Abrupt path changes: tension→compression (Bauschinger) lowers C by ≈ 10 % (C22); tension→torsion gives a transient
  flow-stress overshoot then **markedly reduced strain hardening** (Armco — "particularly unfavourable for the stability
  of deformation"); torsion→tension lowers C linearly with prestrain (up to 15 %) at ≈ constant n (CuZn37); described by
  an "accommodated" Hollomon law σ_f = C(ε₀)·ε̄^n(ε₀), ε̄ accumulated [S-053 pp.63–67, 73–74].
- **Practical rule:** obtain the flow curve from the test resembling the process — **compression for backward can
  extrusion, torsion for punching** (slug blanking!), tension for stretcher levelling; always record the test type
  [S-053 p.74]. Backward can extrusion itself involves path changes (bottom compression → shear at zone boundaries →
  rigid wall) [S-053 pp.53–54, 102].
- For slugs *(inference)*: a fully recrystallised slug has no path memory; a **partially recrystallised** slug carries
  rolling prestrain into a different path (compression + shear) — Bauschinger-type softening and lower hardening are
  then possible, so a "hard" partially-RX slug does not simply behave like a pre-strained one.

### 3.3 Physical work-hardening model (Nes / Kocks–Mecking family; Ryen Ch.2)
- Stages: II (linear, θ ≈ G/200), III (dynamic recovery, decreasing θ), **IV (low linear θ)**, then saturation (e.g.
  CP-Al above ≈ 100 °C); **θ_IV = a·τ_IV, a ≈ 0.1** for fcc [S-052 pp.30–32, Eq. 2.10]. Polycrystals show parabolic
  σ ∝ √ε in "stage II" [S-052 p.32, Eq. 2.11]. **The can wall (ε ≥ 3.4) is deep in stage IV** *(inference)*.
- Flow stress (resolved): **τ = τ_t + τ_p + α₁Gb√ρ_i + α₂Gb(1/δ + 1/D)**, α₁ ≈ 0.3, α₂ ≈ 2; δ subgrain size, D grain
  size; τ_t thermal component from the Orowan equation γ̇ = ρ_m b v with ρ_m ≈ 0.1ρ, at RT essentially
  exp(τ_t) ∝ γ̇/ρ_m [S-052 pp.36–37, Eqs 2.18–2.22].
- Particles (Orowan, Ashby): ⚠ **τ_p = 1.24·A·G·b/(2πλ)·ln(λ/b)**, A ≈ 1; λ from volume fraction f_r and radius r
  (Brown & Ham), ⚠ λ ≈ 0.8·r·(√(π/f_r) − 2) [S-052 pp.37–38, Eqs 2.23–2.24; reconstructed from OCR].
- Storage: dρ⁺/dγ = 2/(bL); effective slip length **(1/L_eff)² = (√ρ/C)² + (1/L_G)²**, alloy barriers
  **(1/L_G)² = (1/D)² + (2f_r/r)²**, C ∝ 1/θ_II [S-052 p.39, Eqs 2.28–2.31]. Total density ρ = ρ_i + κ₀φ/(bδ), κ₀ ≈ 3
  [S-052 p.35, Eq. 2.16]; sub-boundary misorientation φ saturates at ≈ 3–4° at the III–IV transition (empirical
  element) [S-052 p.38]; storage parameter S becomes a fit parameter in stage III–IV [S-052 p.41, Eq. 2.36].
- Dynamic recovery: dipole collapse and subgrain growth, thermally activated; in solid solutions the activation energy
  is that for solute diffusion plus solute–dislocation binding, and the activation volume scales with solute spacing
  (V ∝ b³c^(−e)) [S-052 pp.37, 41–42, Eqs 2.37–2.39] → solutes slow recovery and raise storage — the "indirect" solute
  effect that dominates work hardening [S-052 p.26].
- Model behaviour: 0.5/1/2 at.% Mg raise both yield and hardening; θ_IV scales with σ_IV; **reducing grain size and
  adding non-shearable particles have essentially the same effect** (slip-length restriction + boundary term); model
  Hall–Petch k = 0.1 MPa·m^½ [S-052 pp.42–44, Fig. 2.30]. For polycrystals multiply τ by a Taylor factor (M = 3.06
  random) [S-052 pp.44–45, 50].
- At large strains flow stress ∝ 1/δ (shown for hot-worked AA3104) [S-052 pp.33–34, Fig. 2.25]; dislocation density
  inside subgrains saturates ≈ 10¹⁴ m⁻² for ε = 0.03–2, **higher in AA3207 (0.4 % Mn) than AA1050** [S-052 p.16];
  hard particles create deformation zones, raise overall dislocation density and **reduce subgrain size** [S-052
  pp.15–16].
- **Ryen's conclusions (abstract only — results chapters unreachable):** the model "successfully predicts the effects of
  Mg in solid solution" and explains particle and grain-size effects in stage II–III; **"Mn, Fe and Si in solid solution
  are suggested to create solute clusters that increase the strength significantly"**; at stage IV high-Mg alloys show
  an unexpectedly low θ_IV due to a different storage pattern and shear bands [S-052 p.iii]. Test alloy AA3103 (Mn 1.0,
  Fe 0.57, Si 0.12; Mn_ss 0.40/0.24/0.20/0.15 at.% after homogenisations AC/A/B/C; 65 µm grains; rolled to ε = 0.5–4)
  [S-052 pp.53–56, 66] — **exactly the dataset needed for can-wall strength vs Mn in solution (§10)**.
- Shear banding becomes frequent only above ≈ 2–3 % Mg (Inagaki & Kohara) and is linked to negative strain-rate
  sensitivity (dynamic strain ageing in Al-Mg at RT) and geometric softening [S-052 pp.17–19, 27] → not expected at
  0.3 % Mg *(inference)*.

### 3.4 Solute, particle and grain-size coefficients (for slug and can-wall strength)

| Contribution | Value | Basis | Source |
|---|---|---|---|
| ΔYS per wt.% in solution (super-purity, annealed) | Mn 30.3 · Mg 18.6 · Cu 13.8 · Si 9.2 · Zn 2.9 MPa | binary alloys; unit effect larger at small additions; multiple solutes **less than additive** | [S-031 Table 8, pp.368–369] (= ch.05 §6) |
| ΔUTS per wt.% | Mn 53.8 · Mg 50.3 · Cu 43.1 · Si 39.6 · Zn 15.2 MPa | same | [S-031 Table 8] |
| Mn in solution, O temper | +21 MPa YS, +42 MPa UTS per wt.% | commercial | [S-029 p.160, via ch.06 Table 4.1] |
| Mn in solution, **H19** | +35 MPa YS per wt.% | heavy cold work ≈ can wall | [S-029 p.160] |
| Mg, **H19** | +70–85 MPa YS per wt.% | heavy cold work | [S-029 pp.160, 164] |
| Mg in Al-Mg-Mn plate, O | ≈ +35 MPa UTS per 1 % Mg; Mn "about twice as effective" | 13 mm plate | [S-031 pp.380–381] |
| Mn left in solution in commercial 3xxx | only 0.2–0.3 wt.%; rest in constituents/dispersoids | after preheat + hot work | [S-029 p.94; S-028 p.30 via ch.05/06] |
| Constituent (Fe-rich) particles | ≈ +7 MPa YS per vol.% | Al-Fe-Si | [S-029 pp.122, 138 via ch.06] |
| Dispersion (8xxx) | 30–40 MPa | — | [S-028 p.131 via ch.05] |
| Work-hardening potency per atom | Cu 1.00 > Mg 0.37 (Cu-equivalent K); Doherty H: Cu 3.38, Si 1.56, Mg 1.52, Mn 1.03, Zn 0.27 GPa ⚠ | tensile | [S-029 p.99 via ch.06/07] |
| Hall–Petch k | pure Al 0.065–0.07 MPa·m^½; AlNi6 0.14; alloys 0.1–0.2 | — | [S-052 p.33; S-029 p.101] |
| Strain ageing (Mg, Cu) | ↑ hardening at low strain, **↓ hardening at large strain**, less diffuse necking; Zn no strain ageing; Fe/Si/Mn particles little effect on hardening | sheet forming | [S-031 p.408] |
| Strength vs total alloying | UTS ≈ linear in total wt.% alloying, O and H18/H38 (equation in image, not extracted) | NHT alloys | [S-052 p.7, Fig. 2.1] |
| AA3004 decomposition | solute component grows with strain; second-phase component ≈ constant after early strain | Suni et al. | [S-052 p.29] |

**Derived sensitivities per +0.1 wt.% in solution** (slug O-temper from S-031/S-029; wall from S-029 H19; ram pressure
= 11.5 × ΔUTS from P1) *(derived; additive, upper-end because super-purity unit effects exceed commercial ones)*:

| Element (+0.1 wt.% in ss) | Slug ΔYS / ΔUTS (MPa) | Δp_max ram (MPa) | Can-wall ΔYS (MPa) | Wall gain per unit ram-pressure penalty |
|---|---|---|---|---|
| Mg | 1.9 / 5.0 | +58 | +7–8.5 | **high** |
| Mn | 2.1–3.0 / 4.2–5.4 | +48–62 | +3.5 | low |
| Cu | 1.4 / 4.3 | +50 | no H19 value (strongest WH per atom) | probably high |
| Si | 0.9 / 4.0 | +46 | — | — |
| Zn | 0.3 / 1.5 | +17 | negligible | — |
| Grain 100 → 20 µm | +9 (k 0.07) … +25 (k 0.2) YS | ≈ +0.1–0.3 GPa if UTS moves equally | wall grains are re-formed; small | — |

→ **Mg buys more can-wall strength per unit of extrusion-force penalty than Mn in solution** (inference from mixing
O-temper UTS and H19 YS coefficients of two sources; verify with own data).

---

## 4. Slug microstructure requirements and mechanisms

### 4.1 Hardness — what HB means for the press
- HB ↔ Rm: Al99.5 strip Rm/HB ≈ 3.2–3.7 (Table 3-1); 1060/1100 O–H18: Rm/HB ≈ 3.6–3.9 [S-029 Table 20 via ch.06
  Table 4.2] → **Rm ≈ 3.6·HB** as working conversion; **23–33 HB ↔ Rm ≈ 83–119 MPa** *(derived; alloy-specific,
  calibrate)*.
- Benchmarks: Al99.5 hot band 23–25 HB → **+20 % cold reduction ≈ 33 HB** (Table 3-1); 1060-O 19, 1100-O 23 / H14 32 /
  H18 44 HB [S-029 Table 20 via ch.06]; 3003-O 28 / H14 40 HB (ASM values in W-15/16, ch.09 §6.3).
- Ram pressure ∝ slug UTS (P1) → the HB window maps directly to press force (§2.5a).
- **Sillekens: composition, hardness and UTS are "absolutely inadequate" to assess workability**; use the flow curve,
  the ductile-failure curve and the r-value, all obtainable from tension + torsion tests [S-053 pp.101–102]
  → HB is a necessary but not sufficient slug spec.
- Higher working temperature/softer state → lower flow stress and better ductility; for the RS material a high
  consolidation temperature lowers hardness, YS and UTS but improves ductility [S-053 p.36].

### 4.2 Grain size
- Grains above ≈ **100 µm cause orange peel and reduce formability**; fine RX grain needs ≥ 15 % prior reduction, fast
  heating, no exposure above 350–380 °C, ≤ 2 h hold [S-043 pp.52–53, via ch.06 §5]. Orange peel comes from coarse
  surface grains [S-028 p.43, via ch.07 §7.4].
- Hall–Petch effect is small: 100 → 20 µm adds ≈ 9 MPa YS (k = 0.07) to ≈ 25 MPa (k = 0.2) *(derived)* ≈ 2–7 HB.
  The in-house model HB ≈ 19.8 + 37.4/√d (ch.09 §2.2) implies k ≈ 0.13 MPa·m^½ via Rm ≈ 3.6·HB — inside the
  "alloys 0.1–0.2" range [S-029 p.101] *(derived)*.
- Through-thickness: a 0.35–0.44 mm wall made from a slug with 100 µm grains is reduced ≈ 30× in thickness (R ≈ 30);
  slug-scale grain/texture variations end up as fine bands in the wall *(derived/inference)*.
- Fine grains develop rolling texture faster [S-052 p.21]; ultrafine (< 1 µm) grains lose work-hardening capacity
  [S-029 p.102 via ch.06] — irrelevant at 20 µm.

### 4.3 Texture and anisotropy
- Anisotropy is quantified by r = ε_w/ε_t, r̄ = (r₀ + r₉₀ + 2r₄₅)/4, Δr = (r₀ + r₉₀ − 2r₄₅)/2; deep-drawing needs r̄ > 1,
  Δr ≈ 0 ("earing") [S-053 pp.45–48]. Example (RS extruded sheet): r₀ 0.56, r₄₅ 1.09, r₉₀ 0.63 → r̄ 0.84, Δr −0.50
  [S-053 p.46] (not a slug).
- Rolling texture: Cu/S/Brass β-fibre; medium (0.1–5 µm) non-shearable particles sharpen it, > 5 µm particles weaken it
  [S-052 pp.19–21]; RX texture cube vs PSN-random balance → earing direction (0/90° vs 45°) [S-028/S-029 via ch.07 §7].
- For impact extrusion the anisotropy shows up as an **irregular can rim**, removed by trimming [S-055 step 3]; the
  in-house slug masses leave no trim allowance (ch.09 §8 Assessment) *(inference: low planar anisotropy and a trim
  allowance must be designed together)*.

### 4.4 Particles
- Constituents (≥ 1 µm, from solidification/homogenisation, hard, non-shearable), dispersoids (Mn, Zr; 5–200 nm; Zener
  drag), precipitates [S-052 p.28]. Mn forms Al6(Mn,Fe) and α-Al12(Fe,Mn)Si constituents in casting and dispersoids in
  preheat; dispersoids strengthen and control RX grain size [S-031 pp.388–389]. Mn corrects the shape of acicular/
  platelike Fe constituents and reduces their embrittling effect [S-031 p.382].
- **Ductile fracture** nucleates and links voids at particles; an increase in Fe, Ni or Mn raises the number of
  void-nucleating particles; Mg further lowers fracture strain because higher flow stress aids void growth, and promotes
  shear localisation [S-031 pp.408–409]. Fe/Si/Mn particles barely affect strain hardening or necking [S-031 p.408].
- Fe + Mn ceiling for primary (Fe,Mn)Al6: < ≈ 2.0 % (3003), < ≈ 1.7 % (3004) [S-031 p.383, via ch.05 §4.2]; modified
  3102 at Mn 1.30 + Fe 0.45 = 1.75 % sits between the two limits (ch.02 §2.6 for phase selection) *(derived)*.
- Fe refines the wrought grain size (finely dispersed Fe-rich phase stabilises fine grains, e.g. 8006) [S-031 p.380].
- Lesson from scrap recycling: conventionally cast car-shredder scrap with coarse intermetallics **fractures at zero
  plastic strain**; rapid solidification (10⁵–10⁶ °C/s) refines and homogenises the particles → ≈ 40 % fracture strain
  [S-053 pp.32–33]; fracture strain is lowest across the bonding direction of the consolidated flakes [S-053 pp.40–41].
  → **For 100 %-scrap slugs (ch.09 §7) particle size/distribution, set by casting route and homogenisation, is the
  ductility lever, not only composition** *(inference)*.

### 4.5 Solute elements (summary for slug design)
- **Mg**: solid solution + strongest practical work-hardening effect; raises slug UTS ≈ 5 MPa per 0.1 % and can-wall YS
  ≈ 7–8.5 MPa per 0.1 % (§3.4); strain ageing reduces large-strain hardening [S-031 p.408]; MgO growth in annealing
  (ch.09 §2–3).
- **Mn**: in solution highly effective in binaries but largely precipitated in commercial alloys [S-031 p.368]; with
  Fe/Si possibly forming strengthening "solute clusters" [S-052 abstract]; dispersoids raise RX temperature and
  pin grains (ch.09 §5, ch.05 §4.2).
- **Cu**: most potent per atom for work hardening [S-029 p.99]; strain ages like Mg [S-031 p.408]; ≤ 0.3 % in NHT
  alloys [S-029 p.94].
- **Si, Zn**: small direct effects (Table 3.4); Zn no strain ageing [S-031 p.408]; Si in solution impedes dynamic
  recovery (1xxx) [S-029 p.140 via ch.06].

### 4.6 Slug surface and edges
- Punched slug edges show roll-over, a straight burnished wall, a fracture zone and a burr; dull punch or die edges
  enlarge burr and roll-over [S-059/S-060]. Punching corresponds to a **torsion-type (shear) strain path** [S-053 p.74].
  In-house slugs are annealed after punching (ch.09 §0) → edge work hardening is removed by the anneal *(inference)*.
- Surface oxide/MgO and lubricant: see §2.6 — no quantitative source (gap).

---

## 5. Defects and failure

### 5.1 Ductile failure — the failure-curve approach (Sillekens Ch.3, Ch.5)
- **Ductile-failure curve**: equivalent strain at fracture ε̄_F vs stress triaxiality η = σ_m/σ̄ (Hancock & Mackenzie);
  determined efficiently from a **tension test (η ≈ 1/3, Bridgman-corrected) and a torsion test (η = 0)**, linear
  interpolation/extrapolation [S-053 pp.42–44, 87–88]. It is phenomenological, for practical use [S-053 p.87].
  Compression range may need extra tests: fracture strain rises more than proportionally with superimposed pressure
  (Pugh & Green) [S-053 pp.94–96].
- Recycled RS Al: ductility ≈ doubles from 20 to 200 °C, largest gain 200–300 °C, none above 300 °C [S-053 p.44];
  ε̄_F(η = 0) of order 1 at ≤ 200 °C and ≈ 3–3.5 at 300–350 °C [S-053 p.44, Fig. 3.8, read from image]. Its 200 °C
  curve ≈ that of AlCuBiPb, its 300–350 °C curves ≈ AlMgSi1 — two conventional cold-forming grades [S-053 p.88, Fig. 5.5].
- Application: track each material point's (η, ε̄) path (flow lines from the power analysis, stresses from the slab
  analysis); failure if a path crosses the failure curve [S-053 pp.89–90]. Triaxiality in zones I/II is negative
  (compression) during piercing; **the wall (zone III) is stress-free** and the state is momentary [S-053 p.90, Eq. 5.11].
- **Critical location: exterior side of the can near the bottom corner** (highest strain); analytical ε̄_max = 5.4,
  FE (ABAQUS, μ = 0.1, 75 % bottom reduction) ε̄_max = 2.8 — local values differ by ×2, but both show **different strain
  gradients in the inner and outer wall** → hardness distribution across the wall [S-053 pp.91–94, Figs 5.7–5.8].
  Point C (originally at the outer bottom edge) crosses the extended 200 °C and 300 °C failure curves [S-053 p.90,
  Fig. 5.6].
- **Experiment:** cans extruded at 200–300 °C were visually and microscopically sound, **but subsequent ironing to
  0.75 mm wall fractured them at the corner**, while machined cans of the same material ironed without fracture →
  **hidden damage from extrusion** [S-053 p.93; discussion p.94]. Conclusion: approach promising, "not yet a
  ready-made solution"; accuracy depends on local strain/stress prediction [S-053 p.97].
- Transfer to aerosol cans *(inference)*: the M+H line irons after extrusion and the can is then necked in up to 40
  stations and leak-tested to 50 µm [S-057; S-058] → extrusion damage at the base corner/wall from coarse Fe-rich
  constituents is most likely to appear **downstream** (ironing/necking cracks, pinholes, leak rejects), not at the press.

### 5.2 Process (flow) defects
- Upper-bound defect prediction (Avitzur & Luo) adds a parameter representing a change from sound flow to a defect
  mode: **cavitation** (end of stroke, material fails to fill the die corners; modelled on the two-zone field;
  prevented by friction and external pressure), **fishskin**, **indentation** [S-053 pp.24–25]. These are
  process-geometry defects; the method lacks a material description [S-053 p.25].
- Low-hardening flow (high temperature, unfavourable path change) → strain concentration → failure [S-053 pp.47, 74].

### 5.3 Surface defects
- Orange peel: coarse grains (> ≈ 100 µm) [S-043 via ch.06]; CRM table flags "orange peel risk" for coarse-grained
  3003 slugs (ch.09 §5).
- Pinholes/fractures are screened by pressure/leak testing [S-055 step 11; S-057 item 19].
- No source covers die lines, galling pick-up, slug-edge laps or streaks in impact-extruded cans (gap).

---

## 6. Can properties
- Wall strength comes from the very large cold strain (ε ≥ 3.4, stage IV): ≈ 190 MPa YS for Al99.5 and ≈ 250 MPa for
  3003-O by cold extrapolation (§3.1) *(derived upper bounds)*; reduced in practice by adiabatic heating (§2.7),
  recovery in the IBO and pin-chain ovens [S-057; S-055] — **no bake-softening data in any source** (gap).
- Solute choices raise the wall more efficiently than the slug for Mg (§3.4); particles reduce subgrain size and raise
  stored dislocation density [S-052 pp.15–16], so dispersoid/constituent-rich alloys should reach a higher stage-IV
  stress (inference).
- The wall carries inner/outer strain gradients → non-uniform hardness [S-053 p.94]; downstream necking needs residual
  ductility and lacquer elasticity [S-058 p.2].
- Thinner walls at equal burst pressure need higher wall strength (hoop stress ∝ P·D/2t) *(general knowledge; ch.09 §1)*.

---

## 7. Link to the in-house targets (chapter 09)

| Target (ch.09) | What the literature says | Assessment |
|---|---|---|
| **Slug hardness**: user limit **≤ 35 HB** (stated 2026-10-12). The "23–33 HB" used below was inferred from the in-house model files (§2.5, §3.5) | Fully annealed Al99.5 ≈ 23–25 HB; +10 % CR ≈ 26–28; +20 % CR ≈ 33 HB [S-051 Fig. 3/5, digitised]; 1100-O 23, 3003-O 28 HB (§4.1). Ram force ∝ UTS (P1): 33 HB ≈ +43 % force vs 23 HB (§2.5a). | A fully RX lean 3xxx (between 1100 and 3003) should sit ≈ 23–28 HB; **values near 33 HB in 3102 indicate residual cold work (partial RX ≈ 15–20 % equivalent strain) or very fine grain** — HB must be paired with RX fraction/grain size (§4.1). A fully annealed **modified 3102** (≈ 3003 + 0.3 Mg) is estimated at ≈ 31–32 HB (3003-O 28 HB + ≈ 15 MPa UTS from Mg ÷ 3.6) *(derived)* → little headroom for incomplete RX and the highest press loads in the family. |
| **Grain 20–100 µm** (§3.1, §5) | > 100 µm → orange peel/formability loss [S-043]; ≥ 15 % prior strain for fine RX grain [S-043]; HP effect only 2–7 HB over 20–100 µm (§4.2). | Upper limit is literature-supported (surface); the lower limit has **no literature basis** in these sources — it is a cost/process limit (needs high CR, low T anneal; ch.09 §5), not a forming limit. |
| **Cold-rolling ε ≥ 0.80–0.95** (§5) | > 50 % reduction gives L≈T deformed microstructure, no banding until > 90 % [S-051 p.195]; ε ≥ 0.15 critical strain [S-043]; fine grains texture faster [S-052 p.21]. | 55–61 % CR sits in the homogeneous-deformation regime; supports the CRM rule (ch.09 §5) qualitatively. No source gives grain size vs ε for 3xxx. |
| **Low MgO after anneal** (§2.6, §3) | Interface/lubrication and surface reactions are recognised problem areas [S-053 pp.5–6]; end-of-stroke force is friction-dominated for thin-based Ø45–53 cans (§2.5b). | Plausible route by which MgO matters (lubricant adhesion → m → peak force, galling, surface) — **not quantified in any source** (gap). |
| **Composition windows** (§1, §10) | Mg raises wall strength efficiently (§3.4); Mn/Fe/Si clusters raise strength [S-052]; Fe/Mn particles cut fracture strain [S-031 p.408]; primary-phase Fe+Mn ceiling (§4.4). | See §8. |

---

## 8. Design levers and trade-offs

| Lever | Effect on slug (HB, flow stress) | Extrusion | Can | Risks / trade-offs | Basis |
|---|---|---|---|---|---|
| ↑ Mg (0.12 → 0.30) | +≈ 9 MPa UTS (+≈ 2.5 HB) | +≈ 0.1 GPa ram pressure (≈ +0.23 MN Ø53) | +13–15 MPa wall YS | MgO ↑ (ch.09); strain ageing ↓ large-strain hardening; ↓ fracture strain at particles | §3.4; [S-031 p.408]; *(derived)* |
| ↑ Mn total (0.3 → 1.2) | dispersoids + ≈ 0.1–0.2 % more Mn_ss: ≈ +20–30 MPa UTS (3003-O vs 1100-O ≈ +20) | +0.2–0.35 GPa | +≈ 5 MPa (ss) + unknown dispersoid share | slower RX, heating-rate sensitivity, coarser/elongated RX grain (ch.09 §5); primary (Fe,Mn)Al6 if Fe+Mn too high | §3.4, §4.4; [S-029 p.160]; *(derived)* |
| Fe (≤ 0.45) | small strengthening (≈ 7 MPa/vol.% constituent); grain refinement | — | — | more void-nucleating particles → corner cracks, pinholes; scrap Fe pick-up | [S-031 pp.380, 408; S-029] |
| Si (≤ 0.15) | small; promotes α-AlFeMnSi | — | — | lowers Mn_ss and changes dispersoid density (ch.02/05) | [S-031 p.388] |
| Cu (0.05–0.10) | ≈ +2–4 MPa UTS | small | strongest WH per atom | not an anti-galling measure (§2.6); corrosion potential | [S-031; S-029 p.99; S-053 p.4] |
| Zn (0.10–0.15) | negligible | — | — | electrochemistry only | [S-031 Table 8, p.408] |
| Slug anneal: full RX, 20–60 µm | lowest HB for the chemistry | lowest force | wall strength set by chemistry, not slug temper | under-anneal → HB ↑, path-change softening; over-anneal → coarse grain/orange peel, MgO | §4, §7; ch.09 |
| Lubricant / surface | — | m: 0.05 → 0.2 raises end-of-stroke p/σ₀ from 3.3 to 4.7 (Ø53) | surface quality | oxide/lubricant interaction unquantified | §2.5b *(derived)* |
| Punch nose | — | conical vs flat: flat ×1.2 force | — | stability (conical nose) | [S-053 pp.2, 10] |
| Warm extrusion (tools heated) | — | lower flow stress, higher ductility (≈ 200–300 °C window for RS Al) | lower wall strength | lubricant change, tool heating | [S-053 pp.48, 93] |

**Ranking for lean-3xxx slug design** *(inference)*: (1) get full recrystallisation at the lowest HB the chemistry
allows (force ∝ UTS); (2) buy can strength with Mg (and possibly Cu) rather than Mn in solution, within MgO limits;
(3) keep Fe and coarse constituents low/fine for ductility at the base corner; (4) keep grains < 100 µm; (5) control
lubrication — it dominates the end-of-stroke force on thin-based cans.

---

## 9. Model-ready equations and parameters

| ID | Equation | Parameters (units) | Source / status |
|---|---|---|---|
| M1 | R = R_C²/(R_C² − R_R²); ε_wall ≥ ln R | in-house R ≈ 30–32, ln R ≈ 3.4–3.5 | [S-053 Eq. 1.2]; §2.2 *(derived)* |
| M2 | p_max = (3.14·ln R + 0.80)·σ_UTS; ×1.2 flat ram | σ_UTS slug (MPa) | [S-053 Eq. 2.1] |
| M3 | p_R/σ₀ = 1 + 2/√3 + (1+m)/(2√3)·T/(R_C−R_R) + 2m/(3√3)·R_R/T | m 0.05–0.4; T residual bottom (mm) | [S-053 Eq. 5.7/C.20] ✓ checked vs Fig. 5.2 |
| M4 | τ_fr = m·σ₀/√3 | m | [S-053 Eq. 2.2] |
| M5 | ε_I = ln(T₀/T); ε_II = ln(T₀/T)[1 + R_R/(4(R_C−R_R))]; ε_glob volume-weighted | **not for R ≫ 10** | [S-053 Eqs 5.9–5.10] |
| M6 | σ_f = C·ε̄ⁿ; path-changed: σ_f = C(ε₀)·ε̄^n(ε₀) | test mode must match process | [S-053 pp.38–39, 63–64] |
| M7 | Al99.5 strip: Rp0.2 ≈ 147·ε^0.22 MPa (0.1–2.3); HB ≈ 42·ε^0.16 (0.2–1.6); Rm ≈ 3.6·HB | — | [S-051 Fig. 3] *(digitised + derived fit)* |
| M8 | 1100-O: K 146, n 0.242; 3003-O: K 188, n 0.242 (MPa) | tension | [S-029 Table 3 via ch.07] |
| M9 | σ_f(p) = σ_f(0)(1 + w·p) | w 0.1–0.4 GPa⁻¹ (non-Al); Al unknown | [S-053 pp.71–72] ⚠ form |
| M10 | τ = τ_t + τ_p + α₁Gb√ρ_i + α₂Gb(1/δ + 1/D) | α₁ ≈ 0.3, α₂ ≈ 2, ρ_m ≈ 0.1ρ, κ₀ ≈ 3, φ_IV ≈ 3–4°, M = 3.06 | [S-052 pp.35–38, 50] |
| M11 | dρ⁺/dγ = 2/(bL); (1/L_eff)² = (√ρ/C)² + (1/D)² + (2f_r/r)² | C ∝ 1/θ_II | [S-052 Eqs 2.28–2.31] |
| M12 | τ_p = 1.24·A·G·b/(2πλ)·ln(λ/b); λ ≈ 0.8r(√(π/f_r) − 2) | A ≈ 1 | [S-052 Eqs 2.23–2.24] ⚠ |
| M13 | θ_IV = a·τ_IV | a ≈ 0.1 | [S-052 Eq. 2.10] |
| M14 | σ_y = σ_i + k·D^(−½) | k 0.065–0.07 (pure Al) … 0.1–0.2 MPa·m^½ | [S-052 p.33; S-029 p.101] |
| M15 | Δσ_ss = Σ k_i·c_i (less than additive) | §3.4 table | [S-031 Table 8; S-029 p.160] |
| M16 | Ductile failure: ε̄_F = f(η), linear between tension (η ≈ 1/3) and torsion (η = 0) | measure per alloy/temperature | [S-053 pp.42–44, 87–88] |
| M17 | ΔT_adiabatic = β∫σdε/(ρc) | β ≈ 0.9, c ≈ 0.9 J g⁻¹K⁻¹ | *(general knowledge)*; ≲ 200 K bound §2.7 |
| M18 | F = A·k_w, η_F = k_f/k_w; w = ∫k_f dφ | — | [S-046 pp.26–28] |

Calibration points available: Sillekens Fig. 5.3 (force–stroke, R_C 6/R_R 5/T₀ 4/T_e 1 mm, C 176 MPa, n 0.13, 230 °C,
m ≈ 0.4) [S-053 p.85]; Vasevska Table 3-1. **No in-house press-force or flow-curve data exist** (ch.09 §8).

---

## 10. Open questions, gaps and recommended measurements

1. **Unreached text.** Ryen §4.5 (AA3103 work hardening to ε = 4 vs Mn in solution, p.90) and Ch.5 (per-solute effects
   in stage II–IV, pp.97–130) — the most valuable missing data for can-wall strength vs Mn_ss/Mg; Schuler Ch.6
   (slug preparation p.454, surface treatment p.459, backward cup extrusion p.474, ironing p.476). Both exceed the
   connector limits (10 MB download; ≈125–133 k-char export) — needs a page-split copy in Drive.
2. **No aluminium compression flow curves at large strain / high rate** for 3102/3207/modified 3102. Measure Rastegaev
   compression (and torsion to ε ≈ 3) on annealed slugs at 20–250 °C, 10⁻²–10² s⁻¹ [method: S-053 pp.54–58].
3. **Friction factor** for the in-house lubricant (zinc stearate?) and its dependence on MgO thickness: ring-compression
   or force–stroke back-calculation with M3 (§2.5b).
4. **Ductile-failure curves** of each slug alloy (tension + torsion, with Fe/constituent variants) and inspection of
   the outer base corner after extrusion and after ironing/necking [S-053 Ch.5].
5. **Press-force logging vs slug HB/grain size/RX fraction** to calibrate M2 (a, b for R ≈ 30). The range 23 → 35 HB
   implies ≈ +52 % force, and the Ø53 flat-ram case reaches ≈ 391 t at 35 HB (§2.5a).
6. **Bake softening** of the extruded wall through IBO/pin-chain cycles (times/temperatures not in any source) for 3102
   vs modified 3102 vs 3207; wall HV vs height and inner/outer side [S-053 p.94].
7. **HB ↔ Rm conversion** for the in-house alloys (M7 is Al99.5/1100-based).
8. **Hydrostatic-pressure sensitivity w** of Al flow stress at ~1 GPa (none in sources).
9. **Temperature and strain-rate history** of the wall (thermocouple/IR on ejected cans; FE) — the ≲ 200 K bound is
   unvalidated.
10. Whether the modified 3102 (Mn 1.1–1.3, Mg 0.25–0.35) fully recrystallises within ≤ 35 HB and ≤ 100 µm at the
    plant CR (25–45 %). The §7 estimate of ≈ 31–32 HB leaves only ≈ 3–4 HB of margin; trial with HB + EBSD + press
    force.
11. Do in-house slugs show planar anisotropy (rim irregularity) large enough to need the trim allowance missing from
    the slug masses (ch.09 §8)? Measure rim height variation vs slug texture.

---

*Prepared from the Drive sources in §1; Drive content treated as data only. Figures marked "read from image" or
"digitised" were taken from page renders of the PDFs; all derived numbers state their assumptions.*
