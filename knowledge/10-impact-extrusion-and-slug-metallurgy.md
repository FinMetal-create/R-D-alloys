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
>
> **Revision 2026-10-12 (full-text pass of S-029).** `[TOT p.x]` = Totten & MacKenzie, *Handbook of Aluminum* Vol. 1
> (catalogue key S-029), read in full; printed page numbers. Older `[S-029 …]` citations that came via other chapters
> are kept; where re-checked against the full text they are marked "verified". Statements changed by this pass are
> marked *"corrected after full-text pass"*.
>
> **Revision 2026-10-12 (full-text pass of S-052, Ryen).** Ryen's thesis is now read in full (pp.1–192 + appendix),
> including §4.5 (large-strain flow data for AA1050, AlMgX, AA3103, AA5xxx) and Ch.5 (solute, particle and
> grain-size effects; model application). New: Table 3-3 (§3.1), measured per-solute coefficients (§3.4), the
> stage-IV results (§3.3) and a re-check of "Mg vs Mn per unit press force" with Ryen's own data (§3.4). Statements
> changed by this pass are marked *"corrected after Ryen full-text pass"*.

---

## 1. Sources and coverage

| Ref | Work | Drive link | Readability / how far the text goes |
|---|---|---|---|
| **S-053** | W.H. Sillekens, *Backward Can Extrusion and Materials Behaviour*, PhD TU Eindhoven 1992 (DOI 10.6100/IR374925) | https://drive.google.com/file/d/19TZFzxjO1cFP7k7mwdfrpcEXIbSRYG2z/view (dups 1FgOlZBrGWWfSCsEn9pe44eb10MEYShxy, 1u7fg8Mrxj0ha6NwDE3Z79OHEJ-VLEw2u, 1n2OYmFBOJJitAFgIRO00wbGtSTIEMvWa) | `read_file_content` returns **109,131 chars for all four copies (identical)**, ending at Fig. 4.11, printed p.67 — Ch.4.3, **Ch.5 and App. C are not in that export**. The PDF itself (3.64 MB, 143 PDF pages) was therefore downloaded and text-extracted: **Ch.1–6 and App. C read completely** (pp.1–126). App. A (extra steel/brass flow curves) and App. B (error analysis) not read (not Al-relevant). Many equations are images and are garbled (⚠); Figs 2.5, 2.6, 3.4, 3.8, 5.2, 5.3, 5.6 were read from rendered page images. **Material studied is rapidly-solidified recycled car-shredder scrap (Al-6Si-3Cu), not 3xxx.** |
| **TOT (= S-029)** | G.E. Totten & D.S. MacKenzie (eds.), *Handbook of Aluminum, Vol. 1: Physical Metallurgy and Processes*, Marcel Dekker 2003 (ISBN 0-8247-0494-0). Used here: **Ch.17 K. Shinozaki & K. Miyamoto, "Forging" (pp.809–836)**; **Ch.18 W.J. Thomas, T. Altan & S. Kaya, "Sheet Forming of Aluminum Alloys" (pp.837–880)**; Ch.16 H.A. Kuhn, "Designing for Aluminum Forging" (pp.775–808); Ch.3 M. Tiryakioğlu & J.T. Staley (spot checks pp.98–100, 160, 164) | Four PDF parts in Drive folder "Cloud part book": https://drive.google.com/file/d/1Yxag4tVsKp2w7GaNvUqpz09wJRuCpLVT/view (pp.1–388) · https://drive.google.com/file/d/1EwIKZG891qUZJJfloJCpHAP2hJmgXhZE/view (pp.388–788) · https://drive.google.com/file/d/10ilZD0Rt4LM1rUzaCa9hLB0Up-NaH7a3/view (pp.788–988) · https://drive.google.com/file/d/1KmVD2fbnjMnPd2M5YfDEQaI0OflR_NMD/view (pp.989–1296) | **Full text, coverage complete (2026-10-12).** All four parts downloaded; the broken font maps were rebuilt and the text re-extracted. **Ch.17 and Ch.18 read completely.** Ch.16 read for cold-forging, flow-stress, friction, defect and tooling content (the rest is hot die forging of 2xxx/6xxx/7xxx). Ch.21 (Machining) skimmed: no flow-stress or strain-rate data for 1xxx/3xxx. Ch.17 Fig. 2 (flow curve) and Fig. 17 (specific extrusion pressure) were **digitised** from 300-dpi page renders; Figs 19 and 22 and garbled equations were read from page images. Tables have extraction quirks; all numbers used were checked against the page images. |
| **S-052** | Ø. Ryen, *Work Hardening and Mechanical Anisotropy of Aluminium Sheets and Profiles*, Dr.Ing. NTNU 2003 | https://drive.google.com/file/d/1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_/view (dup 1UzIUO6x8LEca1klH_1--rFxKuoXwsVhI). Split copy in Drive folder "Cloud part book": er.pdf https://drive.google.com/file/d/1DXwBCcZG8Shr2h-ip3xtVuBbvsGGUMlo/view (pp.i–viii, 1–40) · qwqwqw.pdf https://drive.google.com/file/d/1i29-pTkkrRlcz6mxmDS-3L2g8n7wBDXV/view (pp.41–90; errr.pdf 1P5XI7XyJz7ASf2kTTLCF-oqWlRjiKg1B is a text-identical copy) · Thesis.book.pdf https://drive.google.com/file/d/1tCTAF9aRtRvPtObL6vkblyscDBf1BOX_/view (pp.91–192, A-1–A-4) | **Full text, 2026-10-12.** The three split parts were downloaded (2.51 / 5.86 / 2.85 MB, sizes verified) and converted with `pdftotext -layout`; they cover the whole thesis without gaps. A fourth part, qwq.pdf (8.23 MB), broke the connector and was not needed. Equations 2.20–2.39 were checked on page renders. The large-strain figures 4.31(a), 4.33(b) and 4.35 were **digitised** from 300-dpi renders: axes were calibrated on the tick marks and marker centroids located by image analysis (± ≈ 2–3 MPa). Earlier passes had only the Drive text to p.70. Printed page numbers are cited. |
| **S-051** | T. Vasevska, "Utrjevanje aluminija in zlitin pri vzdolžnem hladnem valjanju", *Mater. Tehnol.* 38(3–4) 191 (2004) (SL) | https://drive.google.com/file/d/1wpVR73nujVXO1OfmvV57CzuvwR__bdRc/view | Full PDF downloaded (5 pp., pp.191–195), read and translated completely. **No hardening equation in the text**; the property-vs-reduction curves (Figs 3–6, Al99.5) were **digitised** from rendered images (§3.1). |
| **S-046** | Schuler, *Metal Forming Handbook* (Springer 1998) | https://drive.google.com/file/d/1n5Yidy74bZxj6ZifvCNtq0iRtk2nyh43/view | `read_file_content` returns 124,942 chars, ending in **§3.2 (press design, ≈p.60 of ~560)**. The cold/impact-extrusion chapter (**Ch.6: §6.3.2 "Billet or slug preparation" p.454, §6.3.3 surface treatment p.459, §6.5.3 backward cup extrusion p.474, §6.5.5 ironing p.476**) appears only in the table of contents — **not reached**. Download impossible (28.6 MB). Only §2.2 basics used. |
| **S-031** | J.R. Davis, "Aluminum and Aluminum Alloys", *Alloying: Understanding the Basics*, ASM 2001, pp.351–416 | https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view | Full PDF downloaded; complete. Used for solute coefficients and particle/ductile-fracture statements (also used in ch.05). |
| **S-055** | MPMA, "How aluminium aerosol cans are made" (info sheet) | https://drive.google.com/file/d/1Ul9kcbJAllC4ufhIsV3Xr2tkhjW6TBSW/view | Full (5 pp.). Process steps only. |
| **S-056** | Ardagh Group, *Metal Packaging Solutions: Steel and Aluminium Aerosols* (2015) | https://drive.google.com/file/d/1C_DUB748Ikw3LP4pcp97tQmoCn5js5uF/view | Full (8 pp.). Product range only. |
| **S-057** | Mall + Herlan, CMC 200/250 monobloc aerosol-can lines | https://drive.google.com/file/d/1MFEG_JSZSKkmzXpRJ5lF58iiv7MBxnvX/view | Full (2 large pages; columns interleaved but readable). Line data incl. press force. |
| **S-058** | Hinterkopf, N40.2 necking machine | https://drive.google.com/file/d/1rox7kzRaTGK_jAjUQrKQIBs06yvEmHQ_/view | Full (8 pp.). |
| **S-059/S-060** | "Basic punching (theory)", Mate Precision Tooling slides 62–63 (.jpg) | https://drive.google.com/file/d/13cVKT8DZmNansFOdGiUpKPv8JrAiXkNY/view · https://drive.google.com/file/d/15cVOvSbU5hiY7Gkdp7PZg2cOd1ib6CHM/view | Image labels only (slug edge zones). |
| cross-refs | S-028 Polmear, S-030 Kaufman, S-043 EAA *Aluminium in Commercial Vehicles*; S-029 Ch.3 values quoted via chapters 05/06/07 | links in `sources/catalog.md` | S-028/S-030/S-043 **not re-read**; quoted via chapters 05/06/07 with the original page numbers. **S-029 is now read in full (row TOT)**; the Ch.3 values used below (pp.98–100, 160, 164) were re-checked against it. |
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
- **Closest documented analogue: a backward-extruded marker-pen housing (Miyamoto Industry).** The route is: blank
  pierced from thick pure-Al sheet → lubricating with **zinc stearate** → backward extrusion of the tube at room
  temperature → trimming and rolling of the tube end → degreasing → drying → pre-painting, painting and
  over-coating, each followed by drying → inspection [TOT p.827]. The alloy is given as A1050 in the process text but
  A1070 in the figure captions and §2.6 of that chapter [TOT pp.814, 818, 827] (inconsistency in the source).
  - Blank Ø15.85 × 10.5 mm, with a 0.5 mm recess on one face and a curved (in the drawing, chamfered) other face.
    Tube Ø15.3 mm × ≈ 110 mm, wall dimensioned 0.3 ± 0.05 mm, bottom 3.1 mm [TOT pp.827–828, Fig. 22, read from
    image; the drawing is partly illegible and does not explain why the blank is wider than the tube].
  - Wall/diameter ≈ 0.020, against ≈ 0.008 for the in-house cans *(derived)*. Output was 5 tubes/min on a
    special-purpose press [TOT p.828], against 200–250 cans/min on aerosol lines [S-057].

### 2.2 Deformation measures and the in-house geometries
- Extrusion ratio R = A₀/A₁ and reduction r = (A₀−A₁)/A₀; for cylindrical cans R = R_C²/(R_C²−R_R²) (R_C chamber,
  R_R ram radius) [S-053 pp.2–3, Eqs 1.1–1.2]. Low-strength materials (CP-Al, Pb, Zn) reach **R ≫ 10 (r > 0.90)**,
  steel much less [S-053 p.3].
- Homogeneous (minimum) wall strain = ln R *(general knowledge)*. Logarithmic strain ε = ln(h₀/h) is the measure
  used for forging, and "many forged products have strain between 2 and 4" [TOT p.810, Eq. 2].
- Shinozaki defines the backward-can reduction in area as **r = d₂²/d₀²** (punch² / container², i.e. inner² / outer²
  can diameter) [TOT p.813, Eq. 4]. This is the r column below.
- Punch pressure is **lowest at r ≈ 40–60 %**. Very thin walls (large r) and very thick walls (small r) both need
  higher pressure [TOT p.813]. The aerosol cans (r ≈ 0.97) sit at the high-pressure extreme *(inference)*.

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
- Shinozaki gives the same picture. In backward can extrusion the punch force stays "rather flat" because friction on
  the can wall does not grow seriously. **At the end of the stroke, when the billet has become short, the punch force
  rises suddenly**, and very short billets or flat plates need more force to overcome friction [TOT p.813, Fig. 6a].
  In forward rod extrusion the peak comes early and then falls as container-wall friction decreases [TOT p.812].
- **Deep cans are limited by lubricant on the punch.** Lubricant cannot be added to the punch face during the
  stroke, so "it is difficult to manufacture deep cans because of a shortage of lubricant on the punch surface". The
  punch must also be kept from sitting eccentrically or buckling [TOT p.813].

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
| P8 | **Constraint-factor (work) method: p = c·Y_m**, where c = p/Y is read from upper-bound charts (Table 2-2) and Y_m = (1/c)∫₀ᶜ Y dε, so **p = ∫₀ᶜ Y dε**. Basis: Hill showed that without friction the mean plastic work per unit volume equals the drawing stress, so c is the mean equivalent strain. For non-steady processes ∫dε̄ = ∫(p/Y)(dh/h) | Uses the whole flow curve rather than UTS; "can be applied if we know individual flow stress–strain curves" | [TOT pp.821–822, Eqs 7–9] |
| P9 | Upsetting with Coulomb friction: **p = Y(1 + μd/(3h))** | μ = 0.03–0.05 for well-lubricated cold-forged surfaces | [TOT pp.820–821, Eq. 5] |
| P10 | Plane-strain slab with friction factor: **f = m·k, k = 0.577 S**; yield p − q = 1.15 S; web pressure p = 1.15 S[1 + (m/2)(L/t)(1 − 2x/L)]; **corner filling q = 1.15 S(1 + m/2)·ln(r/R)** (R = unfilled corner radius, so R → 0 gives q → ∞) | Example m = 0.3, S = 100 MPa, r = w′/2 = 6 mm: R = 1.6 mm → 175 MPa, R = 3.2 mm → 83 MPa (recomputed ✓) | [TOT pp.790–791, 796–797, Eqs 1–3, 8] |
| P11 | Friction laws: Coulomb τ = μσₙ (low pressure, sheet forming); friction factor **τ = m·σ̄/√3** (bulk forming); **sticking once μp ≥ k**, after which μ is meaningless and m must be used | In bulk forming p ≫ k | [TOT pp.848–849, Eqs 2–4] |

Check of P2 against Fig. 5.2: start (T/R_R = 0.8) → 3.64, end (0.2) → 2.89 — matches the plotted curve *(derived)*.
Empirical formulas and nomograms (Schmitt; Burgdorf & Müschenborn ±10 %) are adequate for press capacity [S-053
pp.10, 27].

**Table 2-2: specific pressure c = p/Y for backward can extrusion vs reduction in area r** (Kudo upper-bound
analysis) [TOT p.821, Fig. 17, *digitised*, ±0.2]

| r (%) | 30 | 50 | 70 | 80 | 90 | ≈ 95–96 |
|---|---|---|---|---|---|---|
| Friction-free | — (curve starts at r ≈ 43 %, c ≈ 1.55) | 1.7 | 2.3 | 3.0 | 3.8 | 4.6–5.1 (end of curve) |
| No lubricant (sticking) | 1.3 | 2.1 | 3.2 | 4.1 | 5.7 | off scale (≈ 6.5 at r ≈ 92 %) |

- Forward rod extrusion gives curves close to these. Actual lubrication lies between the two lines [TOT pp.821–822].
- The in-house cans (r = 0.967) are beyond the plotted range: **c ≈ 5–5.5 frictionless and well above 6.5
  unlubricated** *(extrapolated)*.
- Lubrication is worth more at high r. "No lubricant" exceeds "friction-free" by ≈ 24 % at r = 50 %, ≈ 40 % at 70 %
  and ≈ 50 % at 90 % *(derived)*.

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

**Update (2026-10-12): the user aims for stronger alloys; ≈ 35 HB is acceptable and not a cap**, so there is no 23–33 HB window. At 35 HB, Rm ≈ 126 MPa, and the
same factors give *(derived, same caveats)*:

| Can | p_max at 35 HB (MPa) | F_max conical ram | F_max flat ram (×1.2) |
|---|---|---|---|
| Ø45 | ≈ 1474 | ≈ 2.34 MN (≈ 239 tf) | ≈ 287 tf |
| Ø50 | ≈ 1462 | ≈ 2.87 MN (≈ 293 tf) | ≈ 351 tf |
| Ø53 | ≈ 1449 | ≈ 3.20 MN (≈ 326 tf) | ≈ 391 tf, about 98 % of the 400 t rating |

That is ≈ +52 % force vs 23 HB. At the hardness limit, a flat-nosed Ø53 punch has essentially no press margin, so
for that geometry press capacity rather than the HB specification may be the binding constraint.
Sensitivity: dp/dσ_UTS ≈ 11.5 → **+10 MPa slug UTS ≈ +115 MPa ram pressure ≈ +0.25 MN (+26 tf) on Ø53**.

*Corrected after full-text pass (HB → Rm conversion).*
- Rm/HB depends on alloy and temper. It is 3.6–3.9 for 1070/1100/3003 in O–H18, but 4.1–4.2 for 5052-O and 6061-O
  [TOT p.815, Table 1; ratios derived; §4.1].
- 35 HB corresponds to Rm = 130 MPa in both 1070-H18 and 3003-H12 [TOT p.815].
- With Rm = 130–147 MPa at 35 HB, the forces above rise by ≈ 3–17 %: Ø53 flat ram ≈ 403–456 t (at or above the 400 t
  rating), Ø53 conical ≈ 336–380 t *(derived)*.
- So for Mg-bearing slugs (T11, modified 3102), measure Rm directly instead of converting HB.
- P1 may overstate the penalty of hardness that comes from residual cold work (see (e)).

**(b) Slab model (P2) for Ø53 (s = R_C−R_R = 0.44 mm, R_R = 26.06 mm).** p_R/σ₀ = 2.155 + a·T + b/T with a = 0.2887
(1+m)/s, b = 0.3849·m·R_R. Minimum at T* = √(b/a): m = 0.05 → T* = 0.85 mm, p/σ₀ = 3.33; m = 0.1 → 1.18 mm, 3.86;
m = 0.2 → 1.60 mm, 4.67. At T = 1 mm the bottom-friction term b/T is 0.50 (m 0.05), 1.00 (m 0.1), 2.01 (m 0.2), i.e.
**for large-diameter, thin-based cans the friction term m·R_R/T dominates the end of stroke** → lubricant (and anything
that degrades it, e.g. surface oxide condition) controls peak force *(inference)*. With σ₀ ≈ 160–250 MPa (flow stress
at ε ≈ 3.4: 161 MPa measured in compression for 99.7 % Al [TOT p.811, Fig. 2, digitised], up to ≈ 250 MPa extrapolated
for 3003-O, §3.1) p ≈ 0.62–0.97 GPa at m = 0.1, below the empirical P1 value (P2 omits redundant shear at the zone
boundaries) *(derived; corrected after full-text pass: the lower bound was 190 MPa)*.
**(c) Dipper's strain (P4) cannot be used at R ≈ 30**: R_R/(4s) ≈ 15 gives ε_II ≈ 16·ln(T₀/T), i.e. strains ≫ 10
*(derived)*. Use ln R (≈ 3.4) as the wall strain and FE for local values.

**(d) Cross-check with the work method (P8)** *(derived)*.
- Integrating the digitised 99.7 % Al compression curve (Table 3-2) to c = 5 gives **p ≈ 0.71 GPa** frictionless
  (≈ 0.80 GPa at c = 5.5).
- P1 with the 1070-O tensile strength (70 MPa [TOT p.815]) gives 11.5 × 70 ≈ 0.80 GPa.
- The two agree within ≈ 0–12 %. P1 is therefore a fair press-capacity rule for annealed slugs whose whole flow curve
  scales with UTS.

**(e) What actually raises the force: whole-curve strength vs residual cold work** *(derived; model, not
validated)*. In P8 the pressure is the area under the flow curve up to ε ≈ 5, so the large-strain part dominates.
In pure Al the first unit of strain contributes only ≈ 93 of ≈ 710 MPa (≈ 13 %). Three consequences follow.
- **Residual cold work** (prestrain ε₀) only shifts the curve: Δp = ∫_c^(c+ε₀) Y dε − ∫₀^ε₀ Y dε.
  - Take ε₀ ≈ 0.2. This is roughly the step from 3003-O to 3003-H12 (28 → 35 HB; ε₀ ≈ 0.19 from the 3003-O Hollomon
    fit, YS 40 → 125 MPa [TOT p.815; S-029 p.100]).
  - On the pure-Al curve this adds only ≈ 23 MPa (≈ +3 %). UTS scaling (P1) would predict +18 % (Rm 110 → 130 MPa).
  - Bauschinger-type softening on the path change (§3.2) would lower the increase further.
  - The real cost of residual cold work is **ductility** (3003-H12 has 10 % elongation, 3003-O 30 % [TOT p.815]) and
    uneven grains/texture, not press force.
- **Solute or particle strengthening** raises the whole curve. Mg raises Hollomon k at constant n [S-029 p.164,
  verified]. So press force and can-wall strength rise together: ΔY_wall/Δp ≈ 1/c ≈ 0.2.
- **HB is a weak predictor of force** (as Sillekens says, §4.1). Two slugs at 35 HB can need quite different forces.
  Calibrate with press-force logging (§10 #5) and compression flow curves to ε ≈ 4 (§10 #2).

### 2.6 Friction and lubrication
- Lubricant on the billet prevents tool–workpiece metallic contact and lowers loads [S-053 p.2]. Cold extrusion of
  steel only became possible with a **zinc-phosphate lubricant-carrier layer** that prevents cold welding [S-053 p.4] —
  i.e. galling is a surface-layer/lubricant problem, supporting the ch.09 §1 assessment that 0.05–0.10 % Cu is not an
  anti-galling measure *(inference)*.
- Friction factors used: m = 0.1 (model examples) [S-053 p.19]; best fit **m ≈ 0.4** for recycled Al at 230 °C with
  Molykote HTF, but "ambiguous to conclude a definite value" [S-053 pp.85, 93]; FE used Coulomb μ = 0.1 [S-053 p.93].
  Fig. 5.3: predicted force at 3 mm stroke ≈ 38 kN (m = 0), ≈ 42 (m = 0.2), ≈ 46 (m = 0.4), ≈ 65 kN (m = 0.8), i.e.
  friction from m = 0 to 0.8 adds ≈ 70 % at this low R [S-053 p.85, read from image].
- **Zinc stearate is the documented lubricant for cold backward extrusion of aluminium.** It was used for the pure-Al
  marker-pen housing (RT backward extrusion of a blank pierced from thick sheet) and, after annealing, for cold-forged
  A2218 blanks [TOT pp.827–828]. *(Corrected after full-text pass: this chapter said earlier that no source described
  it.)* Tumbling as the application method is still only implied by the "lubrication drum" [S-057]. Graphite was used
  for hot forging of Al–Si powder preforms at 793 K [TOT p.833].
- **Phosphating** (zinc-phosphate carrier layer) is documented only for steel [S-053 p.4]. TOT gives no phosphate or
  conversion-coating pre-treatment for Al slugs (gap, §10).
- Friction values: well-lubricated cold-forged surfaces **μ = 0.03–0.05** (upsetting) [TOT p.821]; **m = 0.3** is "a
  typical value for aluminum forging" (hot impression dies) [TOT p.791].
- **Use the friction factor m, not μ, at extrusion pressures.** Coulomb friction applies at low pressure (sheet
  forming). In bulk forming p ≫ k, the shear stress saturates, and sticking sets in once μp ≥ k; μ is then meaningless
  [TOT pp.848–849].
  - At the punch face p ≈ 1.0–1.5 GPa (§2.5) and k = Y/√3 ≈ 90–130 MPa (Y ≈ 160–220 MPa), so Coulomb friction reaches
    sticking at μ ≈ 0.06–0.13 *(derived)*.
  - The FE run with μ = 0.1 [S-053 p.93] therefore imposes near-sticking on the punch face *(derived)*. Calibrate m
    instead (§10 #3).
- **Lubricant starvation on the punch nose** limits deep cans [TOT p.813]. For a Ø53 × 200 mm can the inner wall area
  is ≈ 15× the punch-face area (π·52·200 vs π/4·52²) *(derived)*, so the stearate carried in on the slug face must
  survive a large surface extension *(inference)*. This is the most plausible route by which the slug surface (MgO,
  roughness) matters: it controls how much stearate adheres and stays *(inference)*.
- **Too much lubricant also harms.** Excess lubricant on the billet surface causes underfill [TOT p.822] and an
  orange-peel appearance with loss of the smooth bright surface [TOT p.825].
- **Friction belongs to the whole tribosystem** (workpiece, tool, intermediate medium, surrounding medium, load). It
  varies with location and during the process, and depends on sliding distance and velocity, pressure, tool and
  workpiece hardness, finish and composition, and lubricant viscosity and composition [TOT p.854]. Sliding contact
  can **pressure-weld** the workpiece onto the die (galling) [TOT p.854]. → Measure m on the real slug surface with
  the real stearate and tool finish *(inference)*.
- Warm forging at 150–200 °C is used to lower lubricant viscosity and friction [TOT p.826]. → Lubricant behaviour
  probably changes as the tooling warms up during a run *(inference)*.
- Tool–workpiece interface (friction, lubrication, wear) and surface reactions with the atmosphere are separate problem
  areas (4 and 6) in the Lange systematics adopted by Sillekens [S-053 pp.5–6] → the annealing **MgO surface oxide
  belongs to these areas**; no source quantifies its effect on m (gap, §10).

### 2.7 Temperature rise and strain rate
- Backward can extrusion is "usually practised at room temperature"; difficult products may need warm extrusion
  [S-053 p.1]. Below the recrystallisation temperature the flow stress rises with strain and **strain rate has minimal
  influence**; above it, temperature and rate dominate [S-046 §2.2.1 p.26].
- Plastic work → heat; in rolling, cooling prevents the temperature reaching recovery/RX levels [S-051 p.195]; strip
  temperatures of 100–150 °C occur in commercial cold rolling at ε̇ ≈ 50–100 s⁻¹ [S-052 p.10].
- "Ninety percent of the energy used for forging will dissipate as heat", and the forged part can end up hotter than
  the billet [TOT p.825] → **β ≈ 0.9 is now sourced**. In high-speed forging (mechanical press, hammer) the heat has
  little time to diffuse into the dies, so heating is essentially adiabatic [TOT pp.777, 785].
- **No measured temperature or strain-rate data for impact extrusion in the sources.** Adiabatic estimate
  ΔT = β·∫σdε/(ρc) *(formula general knowledge; β ≈ 0.9 [TOT p.825], c ≈ 0.9 J g⁻¹K⁻¹, ρ = 2.70 g cm⁻³)*.
  *Corrected after full-text pass* using the measured 99.7 % Al compression curve (Table 3-2):
  - work to ε = 3.45 ≈ 445 MJ m⁻³ → **ΔT ≈ 165 K**;
  - work to the mean equivalent strain c ≈ 5 (P8, includes redundant work) ≈ 710 MJ m⁻³ → **ΔT ≈ 260 K**;
  - both are upper bounds that ignore heat flow into the tools and thermal softening; they scale with flow stress, so
    they are higher for stronger alloys *(derived)*;
  - the earlier figure (≈ 546 MJ m⁻³, ≲ 200 K) came from extrapolating the Al99.5 rolling fit.
  The stroke time is < 0.24–0.30 s (cycle time, §2.1) *(derived)*.
- **Strain-rate sensitivity is very low in the cold.** 3003-O at RT has m = 0.005 (6009-T4 0.002) [TOT p.853,
  Table 4], so a 10⁶-fold rise in strain rate (tensile test → impact) raises the flow stress by only
  10^(6 × 0.005) ≈ +7 % *(derived)*, consistent with [S-046 §2.2.1]. In the hot range the opposite holds: at 350 °C
  raising the rate from 0.1 to 20 s⁻¹ raises the flow stress of 6061/2014/7075 by about half, and 100 °C lower more than
  doubles it [TOT pp.784–786].
- Ductility of Al alloys is "sensitive to strain rate sometimes", so presses with easily changed speeds are recommended
  [TOT p.833]. To get equal tube lengths after trimming, "the extruded tube must have the same temperature" [TOT
  p.827] → the thermal steady state of the tooling affects can length *(inference)*.
- Consequence: the wall deforms partly "warm"; Sillekens' data show that higher temperature lowers both C and n of the
  flow curve, and **low n promotes strain concentration and failure** [S-053 p.47] *(transfer to 3xxx: inference)*.

### 2.8 Tooling, die and punch design, presses and slug preparation
- **Tool set for RT backward extrusion of a thin pure-Al tube** (marker-pen housing) [TOT pp.827–829, Fig. 23]:
  - punch M2 (SKH51), 62 HRC; back-up punch H13 (SKD61), 53 HRC; die insert M2, 58 HRC; **container of cemented
    carbide**; shrink ring H13; stripper;
  - punch life ≈ **2 million** strokes;
  - **a bottom thinner than 3.1 mm shortened die life**.
  - Harder alloys (A2218, A2011-O) gave tool lives of ≈ 50,000 shots [TOT pp.829–830].
- **Punch alignment.** For deep cans the punch must be protected from eccentric seating and buckling [TOT p.813].
  Sillekens' conical-nose ram serves the same stability purpose [S-053 p.2].
- **Corner radii.**
  - The pressure needed to fill a corner grows as ln(r/R) (P10). In Kuhn's example, halving R from 3.2 to 1.6 mm
    roughly doubled it [TOT p.797].
  - Small radii cause laps, cracks, die checking (cracks in die corners) and fast wear from high local pressure, high
    flow rate and frictional heating [TOT pp.798–801, 803].
  - Rounded die corners and gradual profile changes reduce velocity discontinuities, and with them dead metal and skin
    inclusion [TOT p.823].
  - A larger punch or die corner radius widens the deformation zone and prevents contraction at the can's bottom
    corner [TOT p.824] (§5.2).
- **Pressure limits.** Kuhn takes **1400 MPa** as "a typical limit for hot working die steels" in die-forging design
  [TOT p.805]. No limit for cold punches is given. The P1 estimate for Ø45–53 cans at 35 HB (≈ 1.45 GPa, §2.5a)
  already exceeds that hot-die guide value → **punch stress and punch-nose geometry, not only press tonnage, may limit
  how strong a slug can be** *(inference; check with the tool supplier)*.
- **Slug shape and mass.**
  - The pen-housing blank had a 0.5 mm recess on one face and a curved other face [TOT pp.827–828, Fig. 22]. Billet
    height/diameter ratio, corner trimming and small end recesses or tapers are the levers for sound die filling
    [TOT p.814].
  - Blanks for precision cold forging were **sorted by mass**: 70 ± 0.25 g, and 12–15 g with < ±0.05 g scatter, i.e.
    ≈ ±0.3–0.4 % [TOT pp.829–830; % derived]. For slugs the equivalent is slug-mass control against the trim
    allowance (§4.3, ch.09 §8) *(inference)*.
- **Anneal before each forming step.** In multi-stage cold forging, anneal → lubricate is repeated before each step
  (e.g. A2218: 410 °C × 1.5 h, cooled to 260 °C at 25 °C/h) [TOT pp.828–830]. Heat treatment "before and during"
  cold forging is done "to increase or recover ductility" [TOT p.814].
- **Presses** [TOT pp.831–833]:
  - crank press: simple, productive, easy to automate;
  - **link (knuckle) press**: large force near bottom dead centre and a slightly longer dwell, which helps the part
    copy the die profile;
  - hydraulic press: large capacity, long stroke, easy speed control;
  - special-purpose presses for mass-produced tubes.
  - Faster forging equipment limits the shape complexity that can be reached [TOT p.777].
- **Counter punch.** Counter pressure on the extruded end (a 300 kPa hydraulic cylinder in one case, 40–50 kN in
  another) equalises extruded lengths: fin-height scatter < 0.5 mm with it, 20 mm without [TOT p.826]. It also
  suppresses contraction defects [TOT p.824].
- For the downstream drawing/ironing tools (not the extrusion die), sheet-drawing guidance for Al is a die radius of
  (4–10)·t and a punch radius of (4–10)·t [TOT p.844, Table 1].

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
  Extrapolated to the wall strain ε ≈ 3.4: ≈ 190 MPa (cold, no recovery) *(derived)*. *Corrected after full-text
  pass:* the measured compression curve below gives 161 MPa at ε = 3.4 (see the note after Table 3-2).

**Table 3-2: annealed 99.7 % Al (18 HV), compression to large strain** (re-shape upsetting, RT, hydraulic testing
machine) [TOT pp.810–811, Fig. 2, *digitised*, ±2 MPa]

| ε | 0.02 | 0.1 | 0.2 | 0.3 | 0.5 | 0.7 | 1.0 | 1.5 | 2.0 | 2.5 | 3.0 | 3.4 | 4.0 | 4.4 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Y (MPa) | 46 | 62 | 74 | 83 | 98 | 108 | 120 | 135 | 145 | 152 | 157 | 161 | 166 | 169 |

- The curve starts at ≈ 40 MPa at ε = 0 *(digitised)*.
- Fit *(derived)*: **Y ≈ 122·ε^0.226 MPa for 1 ≤ ε ≤ 4.4** (residuals ≤ 2.2 MPa). The best single Hollomon fit over
  0.1–4.4 is 117·ε^0.27, with residuals up to 6 MPa, so n falls with strain. Between ε = 2 and 4.4 the slope is
  ≈ 10 MPa per unit strain (stage IV-like, §3.3).
- Method: re-shape upsetting keeps h/d between 1.5 (buckling above) and 0.5 (friction no longer negligible below)
  [TOT p.810]. Each re-machining step allows ε ≈ 0.73 (h₀/h = 3^(2/3) at constant volume), so ε ≈ 4 needs ≈ 5–6
  steps *(derived)*. Low-friction compression is the standard flow-curve test; compression with friction and bend
  tests are the fracture tests [TOT p.784]. This is the practical route to the large-strain curves that the slug
  alloys lack (§10 #2).
- Flow stress and hardness "have very good mutual co-relations"; if the flow curve is unknown, hardness helps
  [TOT p.810]. Check with Tabor's HV ≈ 3·Y at ≈ 8 % strain *(general knowledge)*: 18 HV ≈ 176 MPa and
  Y(0.08) ≈ 58 MPa give a ratio of ≈ 3.0 *(derived)*.
- **Correction after full-text pass.** The Al99.5 rolling fit extrapolated to ε ≈ 3.4 gives ≈ 190 MPa; the measured
  99.7 % Al compression curve gives **161 MPa**. Even with the rolling strain converted to von Mises equivalent strain
  (×2/√3 for plane strain, *general knowledge*), the rolling fit gives ≈ 186 MPa. The gap reflects purity (99.5 vs
  99.7 %), test mode (rolled then tensile vs compression, §3.2) and extrapolation. Use **≈ 160–190 MPa** for
  commercially pure Al at ε ≈ 3.4 *(derived)*.
- Transverse Rm/Rp0.2 exceed longitudinal by 7–20 MPa (one-direction rolling) and 3–9 MPa (reversing); transverse A10
  is lower at small reductions; reversing the rolling direction does not change properties or microstructure
  [S-051 p.194]. ≤ 30 % reduction only flattens grains; > 50 % longitudinal and transverse microstructures look alike;
  pronounced banding only > 90 % [S-051 p.195].
- **O-temper Hollomon constants** (tension) [S-029 p.100, Table 3, verified]: 1100-O n = 0.242, K = 146 MPa;
  **3003-O n = 0.242, K = 188 MPa** (same n, +29 % K); 6061-O 0.209 / 224; 5052-O 0.198 / 281; 5454-O 0.189 / 340;
  5086-O 0.193 / 368; 5456-O 0.178 / 479 MPa. More Mg gives higher K and lower n.
  - Extrapolated to ε = 3.4: 3003 ≈ 253 MPa *(derived; tensile Hollomon fits are not reliable to ε ≈ 3)*.
  - Check against Table 3-2: the 1100-O fit extrapolated to ε = 3.4 gives 196 MPa, against 161 MPa measured for
    99.7 % Al, so tensile fits overshoot by ≈ 20 % at this strain (purity differs slightly). Scaling 253 MPa by the
    same factor gives **≈ 210 MPa for 3003 at ε ≈ 3.4** *(derived, rough)*.
  - Rolling form YS = k·εⁿ with ε = ln(T_i/T_f) (Alcoa) [S-029 pp.98–99, Eq. 8, verified].
- Mg lowers n compared with pure Al but raises k; with more Mg, n stays constant while k keeps rising, i.e. Mg raises
  the rate of strain hardening [S-029 p.164, verified].
- **Sheet data, 3003-O** [TOT p.853, Table 4]: YS 48, UTS 110 MPa, uniform elongation 23 %, total 33 %, n 0.24,
  r̄ 0.6, Δr 0.2, strain-rate sensitivity m 0.005 (6009-T4: 131 / 234 MPa, n 0.23, r̄ 0.6, Δr 0.1, m 0.002). In
  tension n equals the true uniform strain, and low-n material localises strain and fractures earlier [TOT p.851].
- **Recycled RS Al (Al-6Si-3Cu-1.5Zn-0.7Fe)**, tension, annealed 350 °C/20 min: C ≈ 340 MPa / n ≈ 0.18 at 20 °C,
  falling to C ≈ 75–100 MPa / n ≈ 0.07–0.10 at 300–350 °C [S-053 p.40, Fig. 3.4, read from image]; C = 176 MPa,
  n = 0.13 used at 230 °C [S-053 p.85]. Reproducibility indicator I ≈ 6 % (C), 24 % (n) in tension [S-053 p.39].
- Flow curves used for extrusion should be **compression** curves (Rastegaev specimens with lubricant pockets keep
  uniaxial stress to large strain; measuring diameter rather than height improves accuracy) [S-053 pp.54–55, 69, 74].

**Table 3-3: commercial alloys cold rolled to large strain, then tensile tested along RD (Ryen)** (*added after Ryen
full-text pass*). The strain is the von Mises equivalent of the rolling strain, ε_vM = (2/√3)·ln(t₀/t)
[S-052 p.55, Eq. 3.3], the same measure as the can-wall strain (§2.2). Values are UTS / Rp0.2 in MPa, *digitised*
from [S-052 p.90, Fig. 4.31(a); p.91, Fig. 4.33(b); p.93, Fig. 4.35] (± ≈ 2–3 MPa; "≈" = marker partly hidden).
O-temper values are tensile results from [S-052 p.88, Table 4.3; p.91, Table 4.4; p.92, Table 4.5]; starting grain
sizes from [S-052 p.66].

| Alloy (wt.%) [S-052 p.53, Table 3.1] | Grain (µm) | O temper | ε_vM 0.58 | 1.15 | 2.31 | 3.46 | 4.6 |
|---|---|---|---|---|---|---|---|
| AA1050 (Fe 0.27, Si 0.09) | 117 | 76.8 / 24.0 | 112 / ≈104 | 132 / 121 | 160 / 142 | **186 / 160** | — |
| AlMg0.5 (Mg 0.48, Fe 0.18, Si 0.04) | 86 | 95.9 / 28.0 | 139 / ≈134 | 156 / ≈148 | 189 / 170 | **223 / 205** | — |
| AlMg1 (Mg 1.01, Fe 0.19, Si 0.04) | 79 | 119.9 / 38.3 | 170 / ≈164 | 190 / 182 | 222 / 204 | **252 / 235** | — |
| AlMg3 (Mg 2.93, Fe 0.20, Si 0.06) | 68 | 193.4 / 62.1 | 277 / 243 | 305 / 274 | 346 / 304 | **377 / 341** | — |
| AA3103-B (Mn 1.0, Mn_ss 0.41*, Fe 0.57, Si 0.12) | 65 | 101.7 / 46.0 | ≈145 / ≈142 | 171 / 163 | 201 / 187 | **232 / 207** | — |
| AA3103-B fine-grained | 6 | — | 167 / — | 190 / — | 209 / — (ε_vM 2.0) | 219 / — (ε_vM 2.5) | — |
| AA5005 (Mg 0.8, Fe 0.3, Si 0.1) | 175 | 138.8 / 54 | — / 185 | — / 206 | — / 245 | — / **273** | — / 299 |
| AA5182 (Mg 4.55, Mn 0.27) | 50 | 265.3 / 107 | — / 302 | — / 345 | — / 416 | — / **449** | — / 494 |

\* 0.20 at.% Mn in solution [S-052 p.54, Table 3.2], converted to wt.% (derived). The AA3103-B points sit at
ε_vM ≈ 0.61, 1.11, 2.21 and 3.46. The AA5xxx were rolled from hot-rolled transfer gauge by Hydro Aluminium
Deutschland [S-052 p.55, 92]; the other alloys were rolled from as-cast + homogenised plate in a laboratory mill.

- **These are the first measured large-strain data for a 3xxx alloy in the library.** At the can-wall strain
  (ε_vM ≈ 3.4–3.5) AA1050 reaches 160 / 186 MPa (Rp0.2 / UTS) and AA3103-B 207 / 232 MPa. The earlier *derived*
  estimates of ≈ 160–190 MPa for commercially pure Al and ≈ 210–250 MPa for 3003 (§3.1 above, §6) are confirmed
  (derived comparison).
- **Stage IV is linear** above ε_vM ≈ 1 [S-052 p.89]. Slopes between ε_vM 1.15 and 3.46 (UTS, derived): AA1050
  23, AA3103-B 26, AlMg1 27, AlMg3 31 MPa per unit ε_vM. Ryen's own stage-IV rates, M²θ_IV = 27 (AA1050) and 30 MPa
  (AA3103-B) [S-052 p.112, Table 5.6], equal these slopes × 2/√3, so they are per unit *rolling* strain (derived
  check). Extrapolating linearly to ε_vM ≈ 4.5 gives ≈ 210 MPa UTS for AA1050 and ≈ 260 MPa for AA3103-B (derived).
- **Rm − Rp0.2 after rolling is static recovery, not a material constant.** Immediately after a rolling pass the
  Frank-network dislocations start to recover at RT; on reloading the structure must be rebuilt, which shows up as a
  yield-to-UTS gap. It grows with strain in the low-Mg alloys and AA3103, and is large from the start in AlMg3 and
  AA5182 [S-052 pp.89–90, 93, 112–113, Fig. 5.14]. High-Mg alloys recover more,
  "which demonstrates the need of a stabilising treatment" (H38) [S-052 p.112]. For the can wall the UTS column is
  the better estimate of the flow stress at the end of extrusion; the Rp0.2 column is closer to what a can that has
  stood at RT will show (inference).
- Tension of the O-temper and compression (REAP project) agree for AA1050/AlMgX, and compression extends the curves
  to ε = 0.5–0.8; the stress measured in cold-rolled material is "somewhat higher" than compression at the same
  strain [S-052 p.89, Fig. 4.30].
- Commercially pure Al hardens in stage IV only because of its impurities: Al99.99 has θ_IV ≈ 1.5 MPa (near
  saturation, subgrain growth) against 19 MPa for AA1050 (Rp0.2 basis, Guyot & Raynaud data) [S-052 p.108,
  Fig. 5.10]. Binary AlMn1 (Mn fully in solution) hardens no more than AA1050 to ε_vM ≈ 5 (Nes et al. 1982 data)
  [S-052 p.109, Fig. 5.11].

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
  - *Corrected after Ryen full-text pass:* a ≈ 0.1 holds for pure Al tested in torsion at various temperatures
    (Alberdi). Ryen's commercial alloys at RT **do not obey Eq. 2.10**: a = 0.037–0.073, falling with Mg, while
    θ_IV/G = 0.12–0.16·10⁻³ (M = 3) [S-052 pp.110–111, Fig. 5.13]. Rollett et al. found a constant a = 0.05 for Mg,
    Mn and Cu additions in torsion [S-052 p.111].
  - **θ_IV is almost independent of alloying.** M²θ_IV rises only from ≈ 27 MPa (AA1050) to ≈ 36 MPa at 3–5 at.% Mg,
    mostly between 0 and 0.5 at.% (digitised from [S-052 p.111, Fig. 5.13(a)]); AA3103-B gives 30 MPa [S-052 p.112,
    Table 5.6]. Grain size does not change θ_IV either; it only lifts the curve [S-052 p.118]. The flow stress at
    the start of stage IV (ε = 1), by contrast, rises strongly with Mg: K = 54 MPa/at.% [S-052 p.111].
  - **Consequence for the can wall** *(inference)*: the wall's strength advantage of an alloy is the advantage it
    has built up by ε ≈ 1 (stages II–III, set by solute, particles and grain size), carried forward almost unchanged
    through stage IV. Alloying does not buy a steeper stage IV.
- Flow stress (resolved): **τ = τ_t + τ_p + α₁Gb√ρ_i + α₂Gb(1/δ + 1/D)**, α₁ ≈ 0.3, α₂ ≈ 2; δ subgrain size, D grain
  size; τ_t thermal component from the Orowan equation γ̇ = ρ_m b v with ρ_m ≈ 0.1ρ, at RT essentially
  exp(τ_t) ∝ γ̇/ρ_m [S-052 pp.36–37, Eqs 2.18–2.22].
- Particles (Orowan, Ashby): **τ_p = A·G·b/(1.24·2π) · (1/λ)·ln(λ/b)**, A ≈ 1; λ from volume fraction f_r and radius r
  (Brown & Ham), **λ = 0.8·r·(√(π/f_r) − 2)** [S-052 pp.37–38, Eqs 2.23–2.24; verified on the page render].
  *Corrected after Ryen full-text pass:* the factor 1.24 is in the **denominator**; the earlier OCR reconstruction
  put it in the numerator (a factor ≈ 1.5 error). In application Ryen uses A ≈ 0.3 for dispersoid-bearing alloys
  (Nes et al. 2001) and gets σ_p = M·τ_p ≈ 4 MPa for AA3103-C (f ≈ 0.03, r 0.5 µm; ≈ 10 MPa with A = 1, f = 0.048)
  [S-052 p.128].
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
- **Ryen's results (full text; replaces the abstract-only summary):**
  - Test alloy AA3103 (Mn 1.0, Fe 0.57, Si 0.12; Mn_ss 0.40/0.24/0.20/0.15 at.% after homogenisations AC/A/B/C;
    65 µm grains; rolled to ε = 0.5–3) [S-052 pp.53–56, 66]. *Corrected after Ryen full-text pass:* ε = 4 was
    reached only by the AA5xxx alloys [S-052 p.56, Table 3.3]. Large-strain data are in Table 3-3.
  - **Mn in commercial AA3103 strengthens strongly; Mn in binary Al–Mn does not.** Fitted on the homogenised
    conditions with AA1050 as the near-zero-solute reference, Mn_ss gives K = 95 (ε = 0.002) to 149 MPa/at.%
    (ε = 0.2), roughly strain-invariant [S-052 pp.102–103, Table 5.4], against 11–46 MPa/at.% for Mg
    [S-052 p.99, Table 5.2]. In hot torsion (ln Z = 25) the Mn effect drops to K = 17.6 MPa/at.%, close to Mg's
    10.4 [S-052 pp.101, 105, Eqs 5.6, Fig. 5.7]. Binary AlMn1 (≈ 0.5 at.% Mn_ss) is slightly *weaker* than AA1050 to
    ε_vM ≈ 5 [S-052 p.109, Fig. 5.11].
  - Ryen's explanation: **Mn, together with Fe and/or Si, forms solute clusters at RT** that act as hard spots and
    dissolve at high temperature. Mn is smaller than Al (−4.4 % radius vs +11.9 % for Mg), so size misfit cannot
    explain the strengthening [S-052 pp.104–105, Table 5.5]. "In order to create the strong solute clusters, Mn
    requires the presence of Fe or Si" [S-052 p.109]. The pure solid-solution effect of Mn is "of the same order as
    that of magnesium" [S-052 p.133, conclusion 3]. The clusters are a hypothesis; Ryen calls for high-resolution
    TEM to confirm them [S-052 p.131].
  - **Impurity Fe and Si strengthen strongly.** AA1050 (Al99.6) is ≈ 30–35 MPa stronger than Al99.99, and its flow
    curve coincides with binary Al–0.55 at.% Mg [S-052 pp.106–107, Fig. 5.9]. Mahon & Marshall report +20 MPa UTS
    from only 0.02 wt.% Fe in solution in high-purity Al, with Si and Mn somewhat less [S-052 p.106].
  - **Particles give a high yield stress but negligible work hardening** (AA3103 and AA5005); stage II becomes more
    curved [S-052 pp.114–116, 133]. Small dispersoids (strip-cast AA3207, r = 0.1 µm, Forbord) act like the large
    primary particles: rapid initial hardening, then a lower rate than the precipitate-free variant above 3 % strain
    [S-052 pp.115–116, Fig. 5.16]. For AA3103-C, of the 20 MPa gap to AA1050 only ≈ 4 MPa is Orowan and ≈ 5 MPa
    slip-length restriction (L_p = 8.3 µm vs L_ρ = 12 µm, L_D = 65 µm); the rest is attributed to clusters
    [S-052 pp.114, 128–129, Fig. 5.26].
  - **Stage IV** is nearly alloy-invariant (see the θ_IV bullet above). The model reproduces stage II–III for AlMgX
    with C falling linearly with Mg [S-052 pp.119–121, Figs 5.19–5.20]. It overpredicts θ_IV for high-Mg alloys
    unless the storage parameters q_c (raised with Mg) and S_IV/S_sc (lowered from 1 with Mg) are tuned; shear
    banding is the proposed physical cause [S-052 pp.122–127, Figs 5.21, 5.24–5.25].
  - Model inputs used for AlMgX: D = 60 µm, f = 0.015, r = 0.5 µm (L_eff = 20 µm), ε̇ = 0.001 s⁻¹, M = 3; the
    activation volumes scale with c^(−e), e ≈ 0.55 [S-052 pp.120–121]. A rise of 1° in sub-boundary misorientation
    at ε = 3 lowers the modelled stress by only ≈ 10 MPa [S-052 p.124].
- Shear banding becomes frequent only above ≈ 2–3 % Mg (Inagaki & Kohara) and is linked to negative strain-rate
  sensitivity (dynamic strain ageing in Al-Mg at RT) and geometric softening [S-052 pp.17–19, 27] → not expected at
  0.3 % Mg *(inference)*.

### 3.4 Solute, particle and grain-size coefficients (for slug and can-wall strength)

| Contribution | Value | Basis | Source |
|---|---|---|---|
| ΔYS per wt.% in solution (super-purity, annealed) | Mn 30.3 · Mg 18.6 · Cu 13.8 · Si 9.2 · Zn 2.9 MPa | binary alloys; unit effect larger at small additions; multiple solutes **less than additive** | [S-031 Table 8, pp.368–369] (= ch.05 §6) |
| ΔUTS per wt.% | Mn 53.8 · Mg 50.3 · Cu 43.1 · Si 39.6 · Zn 15.2 MPa | same | [S-031 Table 8] |
| Mn in solution, O temper | +21 MPa YS, +42 MPa UTS per wt.% | binary Al-Mn, Mn kept in solution by a high-temperature anneal and rapid quench | [S-029 p.160, verified] |
| Mn in solution, **H19** | +35 MPa YS per wt.% | heavy cold work ≈ can wall | [S-029 p.160, verified] |
| Mg, **H19** | +70–85 MPa YS per wt.% | heavy cold work | [S-029 pp.160, 164, verified] |
| Si in 3xxx | accelerates Mn precipitation, gives denser Al₁₂(Mn,Fe)₃Si and less Mn left in solution after homogenisation; as-cast 3003 ingot holds 0.7–0.9 wt.% Mn in solution | DC ingot | [S-029 p.160, verified] |
| Mg in Al-Mg-Mn plate, O | ≈ +35 MPa UTS per 1 % Mg; Mn "about twice as effective" | 13 mm plate | [S-031 pp.380–381] |
| Mn left in solution in commercial 3xxx | only 0.2–0.3 wt.%; rest in constituents/dispersoids | after preheat + hot work | [S-029 p.94; S-028 p.30 via ch.05/06] |
| Constituent (Fe-rich) particles | ≈ +7 MPa YS per vol.% | Al-Fe-Si | [S-029 pp.122, 138 via ch.06] |
| Dispersion (8xxx) | 30–40 MPa | — | [S-028 p.131 via ch.05] |
| Work-hardening potency per atom | Cu-equivalent K: Cu 1.00, Ge 0.64, Mg 0.37, Cd 0.33, Ag 0.15, Zn 0.071; Doherty H: Cu 3.38 ± 0.20, Si 1.56 ± 0.05, Mg 1.52 ± 0.14, Mn 1.03 ± 0.17, Zn 0.27 GPa | K from **tensile** curves; H from the **cold-rolling** YS at ε = 1 (*corrected after full-text pass*: H was labelled tensile and flagged ⚠; values now verified) | [S-029 pp.98–100, Table 2, Eq. 9, verified] |
| Hall–Petch k | pure Al 0.065–0.07 MPa·m^½; AlNi6 0.14; alloys 0.1–0.2 | — | [S-052 p.33; S-029 p.101] |
| Hall–Petch k, measured (Rp0.5) | AA1100 0.06; rising to **0.15 for AlMg3** (yield-point effect at small grain + high solute); **AA3103-B 0.01** (particles dominate the slip length). **No grain-size effect above ≈ 25 µm** for AA1050/AlMgX | coarse vs recrystallised fine-grained variants | [S-052 pp.116–117, Fig. 5.17] (*added after Ryen full-text pass*) |
| **Mg in solution, commercial base (Fe/Si present)** | σ = σ_99.6 + K·c^n (c at.%): ε 0.002: K 11.3, n 1.22; ε 0.025: 21.8 / 0.98; 0.05: 30.6 / 0.92; 0.1: 40.9 / 0.92; 0.2: 46.0 / 0.99. Linear yield fit **σ0.2 = 20 + 14.5·c** MPa. Stage-IV start stress (ε = 1): K = 54 MPa/at.% | AA1050, AlMg0.5/1/3, AA5182 | [S-052 pp.99–100, Table 5.2, Eq. 5.5; p.111] |
| Mg in solution, binary high-purity (Sherby) | σ = σ_99.99 + K·c^¾; K 27.4 (ε 0.025) → 54.5 MPa/at.% (ε 0.2). At 277 °C: 28·c^0.7; at 377 °C: 12·c^0.65 | binary Al–Mg | [S-052 pp.97–99, Table 5.1, Eqs 5.2–5.4] |
| **Mn in solution, commercial AA3103** | K (n = 1) = 94.7 (ε 0.002), 126.3 (0.025), 134.5 (0.05), 145.6 (0.1), 148.5 MPa/at.% (0.2) | homogenised A/B/C, AA1050 as zero point; includes the proposed Mn–Fe–Si cluster effect | [S-052 pp.102–103, Table 5.4, Fig. 5.5] |
| Mn in solution, binary high-purity (Mahon & Marshall, 0–0.05 at.%) | Yield: K 48.9, n 0.59; uniform strain: K 308, n 0.93 (few data) | binary Al–Mn | [S-052 p.102, Table 5.3] |
| Hot flow stress (torsion, ln Z = 25) | AlMg: σ = 20 + 10.4·c; AA3103 Mn_ss: K = 17.6 MPa/at.% (cluster effect lost) | 350–550 °C | [S-052 pp.101, 105–106, Eq. 5.6, Fig. 5.7] |
| Fe in solution | +20 MPa UTS from 0.02 wt.% Fe_ss in high-purity Al (Mahon & Marshall); Si and Mn somewhat less, "much higher than … Mg" | per Ryen, probably clusters | [S-052 p.106] |
| Particles (AA3103-C vs AA1050) | 20–22 MPa gap over ε = 0–0.3: ≈ 4 MPa Orowan + ≈ 5 MPa slip-length, rest attributed to clusters; particles add little work hardening | f 0.045–0.048, r 0.5 µm (homogenised) | [S-052 pp.113–115, 128–129, Table 5.7] |
| Strain ageing (Mg, Cu) | ↑ hardening at low strain, **↓ hardening at large strain**, less diffuse necking; Zn no strain ageing; Fe/Si/Mn particles little effect on hardening | sheet forming | [S-031 p.408] |
| Strength vs total alloying | UTS ≈ linear in total wt.% alloying, O and H18/H38: **R_m = R_m⁰ + const·(Fe + Mn + Si + Mg + Cr, wt.%)**; the constants are not printed (*read from the figure after Ryen full-text pass*). Ryen's own alloys follow it in the O temper and after 87 % CR, except AA3103 (Rm varies with Mn_ss at constant total) and AA5005 | NHT alloys | [S-052 pp.7–8, Fig. 2.1; pp.95–96, Fig. 5.1] |
| AA3004 decomposition | solute component grows with strain; second-phase component ≈ constant after early strain | Suni et al. | [S-052 p.29] |

**Derived sensitivities per +0.1 wt.% in solution** (slug O-temper from S-031/S-029; wall from S-029 H19; ram pressure
= 11.5 × ΔUTS from P1) *(derived; additive, upper-end because super-purity unit effects exceed commercial ones)*:

| Element (+0.1 wt.% in ss) | Slug ΔYS / ΔUTS (MPa) | Δp_max ram (MPa, P1) | Can-wall ΔYS (MPa) | Wall gain per unit ram-pressure penalty (P1 basis; see refinement below) |
|---|---|---|---|---|
| Mg | 1.9 / 5.0 | +58 | +7–8.5 (HB H19); **+6–9 measured at ε_vM 3.46** (Ryen, see below) | **high** |
| Mn | 2.1–3.0 / 4.2–5.4 | +48–62 | +3.5 (HB, **binary** Al–Mn); **≈ +4.6–4.8 per 0.1 % total Mn in commercial AA3103** (≤ +11–12 per 0.1 % Mn_ss, incl. particles; Ryen) | low (P1) → about equal to Mg (Ryen, below) |
| Cu | 1.4 / 4.3 | +50 | no H19 value (strongest WH per atom) | probably high |
| Si | 0.9 / 4.0 | +46 | — | — |
| Zn | 0.3 / 1.5 | +17 | negligible | — |
| Grain 100 → 20 µm | +9 (k 0.07) … +25 (k 0.2) YS; *Ryen measured:* ≈ 0 above 25 µm (AA1050, AlMgX), ≈ +1 for AA3103-B (k 0.01) (derived) | ≈ +0.1–0.3 GPa if UTS moves equally (upper bound; ≈ 0 on Ryen's data) | wall grains are re-formed; small | — |

→ **On the P1 basis, Mg buys more can-wall strength per unit of extrusion-force penalty than Mn in solution**
(inference from mixing O-temper UTS and H19 YS coefficients of two sources; verify with own data). The work method
below narrows this to about parity, and Ryen's measured curves confirm parity (re-check below).

**Refinement after full-text pass (work method P8, §2.5e)** *(derived; assumes each element's effect rises from its
O-temper to its H19 value by ε ≈ 1–2)*.
- If ram pressure follows p ≈ c·Y_m (c ≈ 5, frictionless) rather than 11.5·UTS, the force penalty per +0.1 wt.% in
  solution is ≈ c × (mean ΔY over ε = 0–5).
  - Mg: ΔY ≈ 2 MPa (annealed) rising to 7–8.5 MPa (H19), mean ≈ 6–7.5 → Δp ≈ +30–37 MPa.
  - Mn: ΔY ≈ 2.1–3.0 MPa (annealed) rising to 3.5 MPa (H19), mean ≈ 3.2–3.4 → Δp ≈ +16–17 MPa.
- Wall gain per unit ram pressure is then ≈ 0.19–0.28 for Mg and ≈ 0.21–0.22 for Mn, i.e. **about equal, ≈ 1/c**.
  *Corrected after full-text pass:* the ≈ 2× Mg advantage in the table above comes from P1, which charges Mn for its
  large O-temper UTS effect (+42 MPa/wt.%) although at large strain Mn adds only +35 MPa/wt.% YS against +70–85 for
  Mg [S-029 p.160]. Mg still gives more wall strength **per wt.%** (≈ 2× on HB's binary coefficients; ≈ 1.3–2× on
  Ryen's commercial alloys, *corrected after Ryen full-text pass*, see below), so less alloy is needed for a given
  target. Per unit of press force, however, the two are close, so choose between them on other grounds: MgO, RX
  behaviour, castability, bake response.
- Any strengthening that acts at large strain costs ram pressure at roughly 1/c. Friction, which adds pressure without
  adding wall strength, is the other lever (§2.6).
- **Strength that appears after extrusion** (strain ageing or Mg–Si clustering in the 220 °C / 10 min bake) is the only
  route found that raises the wall without raising press force *(inference; bake response unmeasured, §6, §10 #6)*.

**Re-check with Ryen's measured large-strain data** (*corrected after Ryen full-text pass*; all numbers derived from
Table 3-3 and [S-052 Tables 4.3–4.4, 5.2, 5.4]; same laboratory, route and test for all four alloys)

| Alloy − AA1050 | Addition (wt.%) | Δ yield, O temper | Δ at ε_vM 1.15 (UTS) | Δ at ε_vM 3.46, UTS / Rp0.2 ("wall") | Wall Δ per wt.% added | Mean Δ over ε_vM 0–3.46 | Wall Δ ÷ mean Δ |
|---|---|---|---|---|---|---|---|
| AlMg0.5 | Mg 0.48 | +4 | +24 | +37 / +45 | 77 / 94 MPa | — | — |
| AlMg1 | Mg 1.01 | +14 | +58 | +66 / +75 | 65 / 74 MPa | ≈ 59 / 62 MPa | **1.11 / 1.22** |
| AlMg3 | Mg 2.93 | +38 | +173 | +191 / +181 | 65 / 62 MPa | — | — |
| AA3103-B | Mn 1.0 (0.41 in solution), Fe +0.30, Si +0.03 | +22 | +39 | +46 / +48 | 46 / 48 MPa per wt.% Mn; ≈ 112 / 117 per wt.% Mn_ss | ≈ 40 / 43 MPa | **1.16 / 1.12** |

The mean Δ uses Ryen's stage II fits at ε ≤ 0.2 (Tables 5.2, 5.4) joined to the rolled points by trapezoids.
- **Per unit of press force Mg and Mn are at parity, now from measured curves.** Both differences to AA1050 are
  nearly constant lifts from ε_vM ≈ 0.6 onward, because θ_IV is alloy-invariant (§3.3). Wall gain ÷ mean flow-stress
  gain is 1.1–1.2 for both, so wall gain per unit ram pressure is ≈ 1.1–1.2/c for both (work method, M19). This
  confirms the earlier *derived* parity, which had rested on two different handbooks' coefficients.
- **Per wt.% added, Mg gives ≈ 1.3–2× the wall strength of Mn** (62–94 against 46–48 MPa/wt.%), not "≈ 2×".
  Mg's wall gain per wt.% falls as Mg rises (94 → 62 MPa/wt.%, Rp basis), so lean additions are the most efficient.
- **Per wt.% actually in solution, Mn in a commercial (Fe/Si-bearing) alloy is at least as potent as Mg** (≤ 112–117
  MPa/wt.% Mn_ss, an upper bound because AA3103-B also carries more particles and Fe than AA1050). The HB value of
  +35 MPa/wt.% for H19 [S-029 p.160] was measured on **binary** Al–Mn sheet. Ryen's binary AlMn1 is likewise no
  stronger than AA1050 at large strain [S-052 p.109]. **The two Drive sources therefore disagree for commercial
  alloys**, and the disagreement is explained by Ryen's Mn–Fe–Si cluster hypothesis (§3.3). Use HB's Mn values only
  for high-purity Al–Mn.
- **Relevance to T11 (Mg 0.26, Mn 0.14, Fe 0.52, Si 0.38)** *(inference)*: Ryen's lowest Mg alloy (0.48 %) gives
  ≈ 77–94 MPa/wt.%, so 0.26 Mg should add ≈ 20–25 MPa to the wall (derived, extrapolated below Ryen's range). The
  quenched, unhomogenised strip keeps Mn, Fe and Si in solution (CLAUDE.md), which is exactly the condition in which
  Ryen sees strong Mn–Fe–Si cluster strengthening (as-cast AA3103 had the highest yield, 58 MPa [S-052 p.91], though its particle structure also differs [S-052 p.103]). How
  much of it survives the slug anneal decides both slug hardness and wall strength; measure conductivity and HB before
  and after the anneal (§10 #16).
- The other route to a stronger wall at the same press force remains strength gained after extrusion (bake, §6) and
  force margin won back from friction (§2.6).

---

## 4. Slug microstructure requirements and mechanisms

### 4.1 Hardness — what HB means for the press
- HB ↔ Rm: Al99.5 strip Rm/HB ≈ 3.2–3.7 (Table 3-1); 1060/1100 O–H18: Rm/HB ≈ 3.6–3.9 [S-029 Table 20 via ch.06
  Table 4.2] → **Rm ≈ 3.6·HB** as working conversion; **23–33 HB ↔ Rm ≈ 83–119 MPa** *(derived; alloy-specific,
  calibrate)*.
- **Reference tempers at RT (HB 10/500)** [TOT p.815, Table 1; Rm/HB derived]:

  | Alloy-temper | UTS (MPa) | YS (MPa) | El. (%) | HB | Rm/HB |
  |---|---|---|---|---|---|
  | 1070-O / H24 / H18 | 70 / 100 / 130 | 30 / 90 / 125 | 43 / 12 / 6 | 19 / 26 / **35** | 3.7 / 3.8 / 3.7 |
  | 1100-O / H12 / H14 / H16 / H18 | 90 / 110 / 125 / 145 / 165 | 35 / 105 / 118 / 140 / 150 | 35 / 12 / 9 / 6 / 5 | 23 / 28 / 32 / 38 / 44 | 3.9 / 3.9 / 3.9 / 3.8 / 3.75 |
  | 3003-O / H12 / H14 / H16 / H18 | 110 / 130 / 150 / 178 / 200 | 40 / 125 / 145 / 170 / 185 | 30 / 10 / 8 / 5 / 4 | 28 / **35** / 40 / 47 / 55 | 3.9 / 3.7 / 3.75 / 3.8 / 3.6 |
  | 5052-O | 194 | 90 | 25 | 47 | 4.1 |
  | 6061-O | 125 | 55 | 25 | 30 | 4.2 |
  | 6063-O | 90 | 50 | – | 25 | 3.6 |

  - **35 HB is the hardness of 1070-H18 and 3003-H12** (both Rm 130 MPa). A slug at 35 HB is therefore either a fully
    recrystallised alloy ≈ 20 MPa stronger than 3003-O (more solute or dispersoid than 3003), or a leaner alloy
    carrying residual cold work, with H12–H18 ductility (6–10 % elongation vs 30–43 % in O) *(derived)*. HB alone
    cannot tell the two apart; RX fraction and grain size can (§7).
  - *Corrected after full-text pass:* Rm/HB is 3.6–3.9 for 1xxx/3xxx but 4.1–4.2 for Mg-bearing 5052-O and 6061-O
    *(derived)*. "Rm ≈ 3.6·HB" is the low end: use ≈ 3.75 for 1xxx/3xxx and measure Mg-bearing slugs (T11).
- Forging alloys need "ductility and low flow stress"; "soft material causes low stress on the die" [TOT p.814].
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
  - *Corrected after Ryen full-text pass:* measured on the same alloys, **grain size has no effect on the yield
    stress above ≈ 25 µm** in AA1050 and AlMgX; below it k is 0.06 (AA1100) to 0.15 MPa·m^½ (AlMg3). In
    particle-rich **AA3103-B, k ≈ 0.01**: a ten-fold grain refinement (65 → 6 µm) barely moves the yield, because the
    particles already set the slip length [S-052 pp.116–117, 133]. For lean 3xxx slugs at 20–100 µm the grain-size
    contribution is therefore ≈ 0–3 MPa (derived), less than the range above, and the in-house model's grain-size term
    should be treated as a fit, not as Hall–Petch physics (inference).
  - Fine grains do raise the curve at larger strain: fine-grained (6 µm) AA3103-B is ≈ 20 MPa above the 65 µm
    material at ε_vM ≈ 0.6–1.2 and ≈ 10 MPa at ε_vM ≈ 2.5 (Table 3-3, derived); θ_IV is unchanged [S-052 p.118].
- Through-thickness: a 0.35–0.44 mm wall made from a slug with 100 µm grains is reduced ≈ 30× in thickness (R ≈ 30);
  slug-scale grain/texture variations end up as fine bands in the wall *(derived/inference)*.
- Fine grains develop rolling texture faster [S-052 p.21]; ultrafine (< 1 µm) grains lose work-hardening capacity
  [S-029 p.102 via ch.06] — irrelevant at 20 µm.
- Forged parts carry a spread of strains, so grain growth on heat treatment is likely wherever "a certain amount of
  strain" was applied; large grains have poor properties, and uniform ≈ 30 µm grains are desirable for a fine anodised
  finish [TOT p.825]. Orange peel comes from grain-to-grain differences in flow stress, and reducing the grain size is
  the most convenient remedy [TOT p.856].

### 4.3 Texture and anisotropy
- Anisotropy is quantified by r = ε_w/ε_t, r̄ = (r₀ + r₉₀ + 2r₄₅)/4, Δr = (r₀ + r₉₀ − 2r₄₅)/2; deep-drawing needs r̄ > 1,
  Δr ≈ 0 ("earing") [S-053 pp.45–48]. Example (RS extruded sheet): r₀ 0.56, r₄₅ 1.09, r₉₀ 0.63 → r̄ 0.84, Δr −0.50
  [S-053 p.46] (not a slug). The same definitions are in [TOT p.851, Eqs 5–7]. **3003-O sheet: r̄ 0.6, Δr 0.2**
  (6009-T4 0.6 / 0.1; the steels listed 1.0–1.9) [TOT p.853, Table 4]. Earing grows with Δr and has to be
  trimmed [TOT p.852].
- Rolling texture: Cu/S/Brass β-fibre; medium (0.1–5 µm) non-shearable particles sharpen it, > 5 µm particles weaken it
  [S-052 pp.19–21]; RX texture cube vs PSN-random balance → earing direction (0/90° vs 45°) [S-028/S-029 via ch.07 §7].
- *Ryen full-text pass:* starting from random as-cast textures, the rolling texture of AA1050 and AlMgX is **very weak at
  ε = 0.5** and mostly developed by ε = 2 [S-052 p.68]; AA3103 (A, B, C) develops it like AA1050 [S-052 p.96]. A fine
  starting grain (15 µm) gives a relatively strong copper–S texture already at ε = 0.6 [S-052 p.69]. At the line's
  30–50 % cold reduction (ε ≈ 0.36–0.69) a coarse-grained hot band should therefore carry only a weak deformation
  texture into the slug anneal, which favours low planar anisotropy (inference; the hot-band texture itself is not
  random and is unmeasured).
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
- **Particles lift the flow curve but add almost no work hardening** (AA3103, AA5005); dispersoids (r ≈ 0.1 µm) and
  primary particles (r ≈ 0.5 µm) behave alike [S-052 pp.114–116, 133]. As-cast AA3103 (platelike primaries,
  0.40 at.% Mn_ss) has a yield close to AlMg3 but then hardens like AlMg1 [S-052 p.115, Fig. 5.15(b)]. Its
  rolling texture develops like AA1050's, so the deformation zones around the particles are small [S-052 pp.96, 115].
  → For the slug, particle strength is paid for at the start of the stroke and carried into the wall unchanged
  (inference, §3.4).
- Lesson from scrap recycling: conventionally cast car-shredder scrap with coarse intermetallics **fractures at zero
  plastic strain**; rapid solidification (10⁵–10⁶ °C/s) refines and homogenises the particles → ≈ 40 % fracture strain
  [S-053 pp.32–33]; fracture strain is lowest across the bonding direction of the consolidated flakes [S-053 pp.40–41].
  → **For 100 %-scrap slugs (ch.09 §7) particle size/distribution, set by casting route and homogenisation, is the
  ductility lever, not only composition** *(inference)*.

### 4.5 Solute elements (summary for slug design)
- **Mg**: solid solution + strongest practical work-hardening effect; raises slug UTS ≈ 5 MPa per 0.1 % and can-wall YS
  ≈ 7–8.5 MPa per 0.1 % (§3.4; Ryen measured 6–9 MPa per 0.1 % at ε_vM 3.46); raises Hollomon k at constant n, i.e.
  lifts the whole flow curve and hence press force too [S-029 p.164; §2.5e]; strain ageing reduces large-strain
  hardening [S-031 p.408]; MgO growth in annealing (ch.09 §2–3). Above ≈ 2–3 % Mg it also promotes shear banding and
  a lower θ_IV [S-052 pp.126, 134], irrelevant at slug Mg levels (inference). Small grains + Mg give Lüders yielding
  in the O temper [S-052 pp.87, 134].
- **Mn**: in solution highly effective in binaries but largely precipitated in commercial alloys [S-031 p.368].
  *Corrected after Ryen full-text pass:* Ryen finds the opposite ranking for binary vs commercial alloys at large
  strain. Binary AlMn1 is no stronger than AA1050, whereas Mn_ss in commercial AA3103 gives K ≈ 95–149 MPa/at.%,
  which he attributes to Mn–Fe–Si clusters that need Fe or Si and dissolve at hot-working temperatures [S-052
  pp.102–109, 133]. Dispersoids raise RX temperature and pin grains (ch.09 §5, ch.05 §4.2).
- **Fe, Si (impurity level)**: AA1050's ≈ 0.4 % Fe + Si makes it ≈ 30–35 MPa stronger than Al99.99 and gives it its
  stage-IV hardening (θ_IV 19 vs 1.5 MPa); 0.02 % Fe in solution adds ≈ 20 MPa UTS to high-purity Al [S-052
  pp.106–108]. In unhomogenised, quenched strip (the rotary route) Fe and Si in solution are therefore a strength and
  press-force term in their own right (inference).
- **Cu**: most potent per atom for work hardening [S-029 p.99]; strain ages like Mg [S-031 p.408]; ≤ 0.3 % in NHT
  alloys [S-029 p.94].
- **Si, Zn**: small direct effects (Table 3.4); Zn no strain ageing [S-031 p.408]; Si in solution impedes dynamic
  recovery (1xxx) [S-029 p.140 via ch.06].

### 4.6 Slug surface and edges
- Punched slug edges show roll-over, a straight burnished wall, a fracture zone and a burr; dull punch or die edges
  enlarge burr and roll-over [S-059/S-060]. Punching corresponds to a **torsion-type (shear) strain path** [S-053 p.74].
  In-house slugs are annealed after punching (ch.09 §0) → edge work hardening is removed by the anneal *(inference)*.
- Surface oxide/MgO and lubricant: see §2.6. The mechanism (stearate adhesion and retention on the punch nose,
  friction as a tribosystem property) is now described [TOT pp.813, 854], but there is still no quantitative source
  (gap).

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
- Shinozaki states the same physics in practical terms. Cracking occurs where large shear or tensile stresses act,
  from velocity discontinuities or external loads; **cracking criteria are functions of strain and mean stress**.
  Counter pressure prevents cracking by raising the mean stress; heating raises ductility; annealing before and during
  cold forging restores it [TOT p.823].
- **Kuhn's workability (upset) test.** Compressing cylinders with friction bulges the free surface into circumferential
  tension plus axial compression. Surface strains measured at fracture give a workability diagram (example: AA2024
  at RT and at hot-working temperature) [TOT pp.787–788]. → A cheap ductility screen for slug alloys: upset
  slug-thickness cylinders and record the surface strains at the first crack *(inference)*.
- Higher pressure suppresses ductile fracture. In low-workability alloys thin ribs crack less than thick ribs
  because the higher forming pressure prevents the ductile mechanism; friction along free surfaces pulls them into
  tension [TOT p.799].
- Transfer to aerosol cans *(inference)*: the M+H line irons after extrusion and the can is then necked in up to 40
  stations and leak-tested to 50 µm [S-057; S-058] → extrusion damage at the base corner/wall from coarse Fe-rich
  constituents is most likely to appear **downstream** (ironing/necking cracks, pinholes, leak rejects), not at the press.

### 5.2 Process (flow) defects
- Upper-bound defect prediction (Avitzur & Luo) adds a parameter representing a change from sound flow to a defect
  mode: **cavitation** (end of stroke, material fails to fill the die corners; modelled on the two-zone field;
  prevented by friction and external pressure), **fishskin**, **indentation** [S-053 pp.24–25]. These are
  process-geometry defects; the method lacks a material description [S-053 p.25].
- Low-hardening flow (high temperature, unfavourable path change) → strain concentration → failure [S-053 pp.47, 74].
- **Defect catalogue for cold extrusion and forging** [TOT pp.822–825, Fig. 19]:
  - *Underfill*: unsuitable billet shape, air trapped at die corners, excess lubricant. Fix by billet shape (trial and
    error or simulation) or by adding an operation [p.822].
  - *Dead metal and skin inclusion*: material split off from the main flow in die corners or concavities; skin
    inclusion is the early form. Causes: too large velocity discontinuities **and low ductility**. Fix: round the die
    corners and change die profiles gradually [pp.822–823]. Fig. 19(b) shows both in backward can extrusion with a
    counter punch.
  - *Chevron cracking*: central tensile stress in a forward-extruded rod. **"If impact extrusion is made, body force of
    the extruded part is pulling the deforming zone"**, which raises the central tension. Some cases were cured by
    reducing the extrusion speed [p.823, Fig. 19c].
    - Backward can extrusion has no central rod, so the classic chevron does not apply. The analogue would be axial
      tension at the base-corner/wall exit when the punch decelerates near bottom dead centre and the momentum of the
      already-formed wall pulls on the deforming zone. Extrusion speed and wall friction would be the levers
      *(inference; no source gives backward-can data)*.
  - *Contraction (suck-in)*: at the end of stroke, when the billet is short, metal leaves the die surface along the
    minimum-energy flow path. **In backward can extrusion it appears at the corner of the billet bottom**
    [p.824, Fig. 19e]. Fix: a longer billet (thicker residual bottom), a larger punch or die corner radius, or a
    counter punch [p.824].
  - *Laps*: flow separates from a die corner whose radius is too small and folds over [TOT p.798].
- **The outer base corner collects four mechanisms**: highest strain and hidden ductile damage [S-053 pp.91–94]; dead
  metal and skin inclusion [TOT pp.822–823]; contraction at the end of stroke [TOT p.824]; and the friction-dominated
  end-of-stroke pressure (§2.5b). Design levers: corner radii, residual bottom thickness (the pen-housing tool needed
  ≥ 3.1 mm for die life [TOT p.828]), lubrication, extrusion speed, and compact, fine constituents *(inference)*.

### 5.3 Surface defects
- Orange peel: coarse grains (> ≈ 100 µm) [S-043 via ch.06]; CRM table flags "orange peel risk" for coarse-grained
  3003 slugs (ch.09 §5). Grain-to-grain flow-stress variation is the mechanism, and finer grain the remedy [TOT p.856].
  **A second cause: too much lubricant** gives an orange-peel appearance and loses the smooth, bright surface
  [TOT p.825].
- Pinholes/fractures are screened by pressure/leak testing [S-055 step 11; S-057 item 19].
- Stretcher-strain markings occur "especially" in Al–Mg alloys: Type A (irregular, yield-point elongation) and Type B
  (regular, serrated flow); they cannot be hidden by paint [TOT pp.855–856]. No Mg threshold is given. At 0.26–0.35 %
  Mg (T11, modified 3102) the risk is probably low (DSA and shear banding become frequent only above ≈ 2–3 % Mg, §3.3),
  but check the necked and re-expanded zones of the first cans *(inference)*.
- *Partly closed after full-text pass:* galling is pressure welding in sliding contact [TOT p.854]; laps form at
  small corner radii [TOT p.798]; die checking and wear concentrate at die corners [TOT pp.799–801]. Still **no
  source** on die lines, streaks or slug-edge defects specific to impact-extruded cans (gap).

---

## 6. Can properties
- Wall strength comes from the very large cold strain (ε ≥ 3.4, stage IV): ≈ 160–190 MPa for commercially pure Al
  (161 MPa measured in compression for 99.7 % Al [TOT p.811]) and ≈ 210–250 MPa for 3003-O (§3.1) *(derived upper
  bounds; corrected after full-text pass, previously 190 / 250 MPa)*. In practice it is reduced by adiabatic heating
  (§2.7) and by recovery in the IBO and pin-chain ovens [S-057; S-055]. **No bake-softening data in any source** (gap).
  - *Confirmed after Ryen full-text pass:* measured at ε_vM 3.46 after cold rolling, AA1050 gives 160 / 186 MPa
    (Rp0.2 / UTS) and AA3103-B 207 / 232 MPa; AlMg0.5 205 / 223, AlMg1 235 / 252 MPa (Table 3-3). Linear stage-IV
    extrapolation to ε_vM ≈ 4.5 adds ≈ 25 MPa (derived).
  - Even at RT the rolled structure recovers statically between deformation and testing, which is why Rp0.2 sits
    ≈ 17–36 MPa below UTS at ε_vM 3.46 in these alloys [S-052 p.112, Fig. 5.14; Table 3-3]. A wall that has stood
    before burst testing, and then sees the 220 °C bake, starts from the lower value (inference).
- **Wall strength and press force are coupled** *(derived, §2.5e, §3.4)*. Both are set by the large-strain flow
  stress, so any strength the slug carries costs ram pressure at roughly 1/c. Strength added **after** extrusion,
  by strain ageing or Mg–Si clustering in the 220 °C / 10 min bake, does not. For T11 (Mg 0.26, Si 0.38), Mg and Si
  are held in solution by the hot-band quench, and stay there only if the slug is cooled fast enough after its anneal
  (trials/T11 §2.3 risk 2a, §2.4). The bake response is then the most force-efficient strength lever, provided
  recovery of the heavily worked wall does not cancel it *(inference; unmeasured, §10 #6)*.
- The downstream re-expansion steps of necking (S-058) stretch the wall. In sheet forming the forming limit is
  lowest in plane strain [TOT p.840], and low-n material localises strain early [TOT p.851]; a stage-IV wall has very
  low n *(inference)*.
- Per wt.%, Mg raises the wall more than the slug (§3.4; per unit of press force see the §3.4 refinement). Particles
  reduce subgrain size and raise stored dislocation density [S-052 pp.15–16], so dispersoid/constituent-rich alloys
  should reach a higher stage-IV stress (inference). *Ryen full-text pass:* they do, but only by the lift they
  give in stages II–III; the stage-IV slope is the same (AA3103-B M²θ_IV 30 vs AA1050 27 MPa) [S-052 pp.112, 114].
- The wall carries inner/outer strain gradients → non-uniform hardness [S-053 p.94]; downstream necking needs residual
  ductility and lacquer elasticity [S-058 p.2].
- Thinner walls at equal burst pressure need higher wall strength (hoop stress ∝ P·D/2t) *(general knowledge; ch.09 §1)*.

---

## 7. Link to the in-house targets (chapter 09)

| Target (ch.09) | What the literature says | Assessment |
|---|---|---|
| **Design goal (user, 2026-10-12)**: stronger alloy, good to impact-extrude, castable on the rotary strip caster | Ram pressure ≈ area under the flow curve to ε ≈ 5 plus friction (P8, Table 2-2); can-wall strength ≈ flow stress at ε ≈ 3.4–5 (§6); lubrication is worth ≈ 50 % of the pressure at r ≈ 0.9 [TOT p.821, digitised]; fine, compact constituents from fast solidification raise ductility [S-053 pp.32–33]. Casting itself: ch.11, ch.15. | Strength carried by the slug costs press force at ≈ 1/c whichever element provides it (§2.5e, §3.4). The levers that do not cost force are (i) strength gained **after** extrusion (bake response) and (ii) force margin won back through lower friction and better tooling (§2.6, §2.8), which can then be spent on a stronger slug. Residual cold work raises HB but mainly costs ductility *(derived/inference)*. |
| **Slug hardness**: ≈ 35 HB is acceptable and means a stronger alloy; it is not a cap (user, 2026-10-12). The "23–33 HB" used below was inferred from the in-house model files (§2.5, §3.5) | Fully annealed Al99.5 ≈ 23–25 HB; +10 % CR ≈ 26–28; +20 % CR ≈ 33 HB [S-051 Fig. 3/5, digitised]; 1100-O 23, 3003-O 28 HB (§4.1). **35 HB = 1070-H18 = 3003-H12 (Rm 130 MPa)** [TOT p.815]. Ram force ∝ UTS (P1): 33 HB ≈ +43 % force vs 23 HB (§2.5a). | A fully RX lean 3xxx (between 1100 and 3003) should sit ≈ 23–28 HB; **values near 33 HB in 3102 indicate residual cold work (partial RX ≈ 15–20 % equivalent strain) or very fine grain** — HB must be paired with RX fraction/grain size (§4.1). A fully annealed **modified 3102** (≈ 3003 + 0.3 Mg) is estimated at ≈ 31–32 HB (3003-O 28 HB + ≈ 15 MPa UTS from Mg ÷ 3.6) *(derived)* → little headroom for incomplete RX and the highest press loads in the family. *Full-text pass:* under the work method (§2.5e), HB from residual cold work costs little press force (≈ +3 % for ε₀ ≈ 0.2) but much ductility; HB from solute or particles costs force in proportion and also raises the wall. At ≈ 35 HB the questions are therefore ductility, full RX, and punch stress (§2.8), not the HB value as such *(derived)*. |
| **Grain 20–100 µm** (§3.1, §5) | > 100 µm → orange peel/formability loss [S-043]; ≥ 15 % prior strain for fine RX grain [S-043]; HP effect only 2–7 HB over 20–100 µm (§4.2). | Upper limit is literature-supported (surface); the lower limit has **no literature basis** in these sources — it is a cost/process limit (needs high CR, low T anneal; ch.09 §5), not a forming limit. |
| **Cold-rolling ε ≥ 0.80–0.95** (§5) | > 50 % reduction gives L≈T deformed microstructure, no banding until > 90 % [S-051 p.195]; ε ≥ 0.15 critical strain [S-043]; fine grains texture faster [S-052 p.21]. | The CRM-table target (55–61 % CR) sits in the homogeneous-deformation regime and supports the CRM rule (ch.09 §5) qualitatively. **The actual line rolls only 30–50 % cold (ε ≈ 0.36–0.69; CLAUDE.md, ch.19)**, i.e. between grain flattening (≤ 30 %) and L≈T homogeneity (> 50 %) [S-051 p.195] → coarser, less uniform RX grain is expected unless the hot/cold split is moved *(inference; ch.19)*. No source gives grain size vs ε for 3xxx. |
| **Low MgO after anneal** (§2.6, §3) | Interface/lubrication and surface reactions are recognised problem areas [S-053 pp.5–6]; end-of-stroke force is friction-dominated for thin-based Ø45–53 cans (§2.5b). | Plausible route by which MgO matters (lubricant adhesion → m → peak force, galling, surface) — **not quantified in any source** (gap). The full text adds the mechanism: lubricant on the punch nose cannot be replenished during the stroke, so deep cans are limited by lubricant starvation [TOT p.813], and friction is a property of the whole tribosystem [TOT p.854] → the stearate's adhesion to the annealed (MgO-bearing) surface is the quantity to measure *(inference)*. |
| **Composition windows** (§1, §10) | Mg raises wall strength ≈ 1.3–2× more per wt.% added than Mn (Ryen's measured curves; HB's binary coefficients gave ≈ 2×); per unit of press force the two are at parity (wall gain ÷ mean flow-stress gain 1.1–1.2 for both, §3.4, corrected after Ryen full-text pass); Mn–Fe–Si clusters raise strength in commercial alloys and are lost at hot-working temperatures [S-052 pp.102–109]; Fe/Mn particles cut fracture strain [S-031 p.408]; primary-phase Fe+Mn ceiling (§4.4). | See §8. |

---

## 8. Design levers and trade-offs

| Lever | Effect on slug (HB, flow stress) | Extrusion | Can | Risks / trade-offs | Basis |
|---|---|---|---|---|---|
| ↑ Mg (0.12 → 0.30) | +≈ 9 MPa UTS (+≈ 2.5 HB) | +≈ 0.1 GPa ram pressure by P1 (≈ +0.23 MN Ø53); ≈ +0.05–0.07 GPa by the work method P8 (§3.4) | +13–15 MPa wall YS | MgO ↑ (ch.09); strain ageing ↓ large-strain hardening; ↓ fracture strain at particles | §3.4; [S-031 p.408]; *(derived)* |
| ↑ Mn total (0.3 → 1.2) | dispersoids + ≈ 0.1–0.2 % more Mn_ss: ≈ +20–30 MPa UTS (3003-O vs 1100-O ≈ +20) | +0.2–0.35 GPa | +≈ 5 MPa (ss, HB binary) + unknown dispersoid share; *Ryen:* 1.0 % Mn (AA3103-B) is +46–48 MPa over AA1050 at ε_vM 3.46, i.e. ≈ +40 MPa for +0.9 % if linear in Mn (derived, rough; AA3103-B also has +0.3 Fe) | slower RX, heating-rate sensitivity, coarser/elongated RX grain (ch.09 §5); primary (Fe,Mn)Al6 if Fe+Mn too high | §3.4, §4.4; [S-029 p.160; S-052 Table 3-3]; *(derived)* |
| Fe (≤ 0.45) | small strengthening (≈ 7 MPa/vol.% constituent); grain refinement | — | — | more void-nucleating particles → corner cracks, pinholes; scrap Fe pick-up | [S-031 pp.380, 408; S-029] |
| Si (≤ 0.15) | small; promotes α-AlFeMnSi | — | — | lowers Mn_ss and changes dispersoid density (ch.02/05) | [S-031 p.388] |
| Cu (0.05–0.10) | ≈ +2–4 MPa UTS | small | strongest WH per atom | not an anti-galling measure (§2.6); corrosion potential | [S-031; S-029 p.99; S-053 p.4] |
| Zn (0.10–0.15) | negligible | — | — | electrochemistry only | [S-031 Table 8, p.408] |
| Slug anneal: full RX, 20–60 µm | lowest HB for the chemistry; restores ductility (3003-O 30 % vs H12 10 % elongation) | lowest force, but less force saving than the HB drop suggests (≈ 3 % for ε₀ ≈ 0.2, §2.5e) | wall strength set by chemistry, not slug temper | under-anneal → HB ↑, ductility ↓, path-change softening; over-anneal → coarse grain/orange peel, MgO | §2.5e, §4, §7; [TOT p.815]; ch.09 |
| Lubricant / surface (zinc stearate) | — | m: 0.05 → 0.2 raises end-of-stroke p/σ₀ from 3.3 to 4.7 (Ø53); no lubricant vs friction-free ≈ +50 % at r = 0.9 | surface quality; too much lubricant → underfill, orange peel | lubricant starvation on the punch nose limits deep cans; oxide/lubricant interaction unquantified | §2.5b *(derived)*; [TOT pp.813, 821–822, 825, 827] |
| Punch nose and corner radii | — | conical vs flat: flat ×1.2 force; corner-filling pressure ∝ ln(r/R) | larger radii avoid contraction, dead metal, laps at the base corner | stability (conical nose, centring); punch stress at ≈ 1.4–1.5 GPa (Kuhn's hot-die guide value 1400 MPa) | [S-053 pp.2, 10]; [TOT pp.797–805, 813, 823–824] |
| Residual bottom thickness | — | thinner bottom → friction-dominated force spike at end of stroke (§2.5b) | — | pen-housing tool needed ≥ 3.1 mm bottom for die life; contraction at the bottom corner when the billet gets short | [TOT pp.813, 824, 828] |
| Extrusion speed | — | strain-rate effect on flow stress small (m = 0.005, ≈ +7 % per 10⁶) but adiabatic heating larger | — | body force (inertia) of the extruded part adds tension (chevron cracks in rod extrusion; slowing down helped) | [TOT pp.823, 833, 853] |
| Bake response (Mg + Si kept in solution) | none in the slug if Mg/Si stay in solution | **no extra force** | wall strengthening in the 220 °C / 10 min bake, if it outweighs recovery | slug hardness drifts with storage (natural ageing, trials/T11) | *(inference; unmeasured)* §6 |
| Warm extrusion (tools heated) | — | lower flow stress, higher ductility (≈ 200–300 °C window for RS Al) | lower wall strength | lubricant change, tool heating | [S-053 pp.48, 93] |

**Ranking for lean-3xxx slug design** *(inference; revised after full-text pass)*:
1. **Get full recrystallisation**, chiefly for ductility and uniform grain. HB itself predicts force poorly
   (§2.5e).
2. **Get can strength where it costs no press force first** (the bake response of Mg + Si in solution), and win
   back force margin through lower friction (stearate retention, tool finish), which then allows a stronger slug.
   Then use solute: Mg gives ≈ 1.3–2× more wall strength per wt.% added than Mn (less alloy needed), but per unit
   of press force the two are at parity (§3.4, Ryen re-check). Stay within MgO limits.
3. Keep Fe and coarse constituents low and fine for ductility at the base corner.
4. Keep grains < 100 µm (for surface and formability; above ≈ 25 µm grain size adds no strength [S-052 p.117]).
5. Control lubrication and tooling: stearate quantity and retention, generous punch/die corner radii, adequate
   residual bottom, punch centring, moderate speed. Friction dominates the end-of-stroke force on thin-based cans,
   and the base corner collects the defect mechanisms (§5.2).

---

## 9. Model-ready equations and parameters

| ID | Equation | Parameters (units) | Source / status |
|---|---|---|---|
| M1 | R = R_C²/(R_C² − R_R²); ε_wall ≥ ln R | in-house R ≈ 30–32, ln R ≈ 3.4–3.5 | [S-053 Eq. 1.2]; §2.2 *(derived)* |
| M2 | p_max = (3.14·ln R + 0.80)·σ_UTS; ×1.2 flat ram | σ_UTS slug (MPa) | [S-053 Eq. 2.1] |
| M3 | p_R/σ₀ = 1 + 2/√3 + (1+m)/(2√3)·T/(R_C−R_R) + 2m/(3√3)·R_R/T | m 0.05–0.4; T residual bottom (mm) | [S-053 Eq. 5.7/C.20] ✓ checked vs Fig. 5.2 |
| M4 | τ_fr = m·σ₀/√3 | m; preferred over Coulomb μ at bulk-forming pressures (M22) | [S-053 Eq. 2.2; TOT p.849] |
| M5 | ε_I = ln(T₀/T); ε_II = ln(T₀/T)[1 + R_R/(4(R_C−R_R))]; ε_glob volume-weighted | **not for R ≫ 10** | [S-053 Eqs 5.9–5.10] |
| M6 | σ_f = C·ε̄ⁿ; path-changed: σ_f = C(ε₀)·ε̄^n(ε₀) | test mode must match process | [S-053 pp.38–39, 63–64] |
| M7 | Al99.5 strip: Rp0.2 ≈ 147·ε^0.22 MPa (0.1–2.3); HB ≈ 42·ε^0.16 (0.2–1.6); Rm ≈ 3.6·HB | do not extrapolate past ε ≈ 2.3 (gives ≈ 190 MPa at 3.4 vs 161 MPa measured, §3.1); for Rm/HB see M25 | [S-051 Fig. 3] *(digitised + derived fit)* |
| M8 | 1100-O: K 146, n 0.242; 3003-O: K 188, n 0.242 (MPa) | tension; overshoot ≈ 20 % at ε ≈ 3.4 (§3.1) | [S-029 p.100, Table 3, verified] |
| M9 | σ_f(p) = σ_f(0)(1 + w·p) | w 0.1–0.4 GPa⁻¹ (non-Al); Al unknown | [S-053 pp.71–72] ⚠ form |
| M10 | τ = τ_t + τ_p + α₁Gb√ρ_i + α₂Gb(1/δ + 1/D) | α₁ ≈ 0.3, α₂ ≈ 2, ρ_m ≈ 0.1ρ, κ₀ ≈ 3, φ_IV ≈ 3–4°, M = 3.06 | [S-052 pp.35–38, 50] |
| M11 | dρ⁺/dγ = 2/(bL); (1/L_eff)² = (√ρ/C)² + (1/D)² + (2f_r/r)² | C ∝ 1/θ_II | [S-052 Eqs 2.28–2.31] |
| M12 | τ_p = A·G·b/(1.24·2π)·(1/λ)·ln(λ/b); λ = 0.8r(√(π/f_r) − 2) | A ≈ 1 (≈ 0.3 with dispersoids); σ_p = M·τ_p ≈ 4–10 MPa for AA3103 | [S-052 Eqs 2.23–2.24, p.128] ✓ verified on page render (*corrected: 1.24 is in the denominator*) |
| M13 | θ_IV = a·τ_IV | a ≈ 0.1 (pure Al, torsion); **a = 0.037–0.073 for commercial AA1050/AlMg/AA5182 at RT** (not constant); M²θ_IV ≈ 27–36 MPa per unit rolling strain | [S-052 Eq. 2.10; pp.110–112, Fig. 5.13, Table 5.6] |
| M14 | σ_y = σ_i + k·D^(−½) | k 0.065–0.07 (pure Al) … 0.1–0.2 MPa·m^½; measured: AA1100 0.06, AlMg3 0.15, AA3103-B 0.01; no effect > 25 µm | [S-052 pp.33, 116–117; S-029 p.101] |
| M26 | Solute law at fixed strain: σ = σ_ref + K·c^n (c at.%) | Mg commercial: n ≈ 1, K 11 → 46 MPa/at.% (ε 0.002 → 0.2), 54 at ε = 1; σ0.2 = 20 + 14.5c. Mg binary: n ≈ ¾. Mn_ss in AA3103: n = 1, K 95 → 149 MPa/at.% | [S-052 Tables 5.1–5.4, Eq. 5.5, p.111] |
| M27 | θ_IV = α₂Gb · 2ρ_i·C·S_IV / (κφ_IV·√(ρ_i + κφ_IV/(bδ))) | S_IV/S_sc = 1 for pure metal, falls with Mg; q_c rises with Mg; θ_IV falls if φ keeps rising beyond φ_IV | [S-052 p.123, Eq. 5.9; Figs 5.21, 5.24] ✓ page render |
| M28 | Slip lengths: L_ρ = C/√ρ, L_p = r/(2f_r), L_D = D | AA3103-C: L_p 8.3, L_ρ 12, L_D 65 µm → L_eff 11 → 7 µm with particles | [S-052 pp.128–129, Eq. 5.11] |
| M29 | Measured large-strain flow data (rolled, then tensile) | Table 3-3 | [S-052 Figs 4.31, 4.33, 4.35] *(digitised)* |
| M15 | Δσ_ss = Σ k_i·c_i (less than additive) | §3.4 table | [S-031 Table 8; S-029 p.160] |
| M16 | Ductile failure: ε̄_F = f(η), linear between tension (η ≈ 1/3) and torsion (η = 0) | measure per alloy/temperature | [S-053 pp.42–44, 87–88] |
| M17 | ΔT_adiabatic = β∫σdε/(ρc) | β ≈ 0.9 [TOT p.825], c ≈ 0.9 J g⁻¹K⁻¹ *(general knowledge)* | formula *(general knowledge)*; bound ≈ 165–260 K for pure Al (§2.7, corrected after full-text pass) |
| M18 | F = A·k_w, η_F = k_f/k_w; w = ∫k_f dφ | — | [S-046 pp.26–28] |
| M19 | **p = c·Y_m = ∫₀ᶜ Y dε̄** (frictionless; c = mean equivalent strain from upper-bound charts) | c (backward can) from Table 2-2; ≈ 5–5.5 at r ≈ 0.97 *(extrapolated)* | [TOT pp.821–822, Fig. 17] ✓ cross-checked against P1 (§2.5d) |
| M20 | 99.7 % Al, compression, RT: Y ≈ 122·ε^0.226 MPa (1 ≤ ε ≤ 4.4); full curve in Table 3-2 | 18 HV annealed; Y(0) ≈ 40 MPa | [TOT pp.810–811, Fig. 2] *(digitised + derived fit)* |
| M21 | Plane-strain slab: k = 0.577 S; p = 1.15 S[1 + (m/2)(L/t)]; corner filling q = 1.15 S(1 + m/2)·ln(r/R) | m ≈ 0.3 for hot Al forging | [TOT pp.790–791, 797] ✓ example recomputed |
| M22 | Sticking when μp ≥ k (k = σ̄/√3); then use τ = m·σ̄/√3 | at p ≈ 1–1.5 GPa sticking for μ ≳ 0.06–0.13 *(derived)* | [TOT pp.848–849] |
| M23 | Strain-rate sensitivity σ ∝ ε̇^m | 3003-O m = 0.005, 6009-T4 0.002 (RT) | [TOT p.853, Table 4] |
| M24 | Upsetting with Coulomb friction p = Y(1 + μd/(3h)) | μ = 0.03–0.05, well-lubricated cold forging | [TOT pp.820–821] |
| M25 | Rm/HB (HB 10/500) | 3.6–3.9 (1xxx/3xxx O–H18); 4.1–4.2 (5052-O, 6061-O) | [TOT p.815, Table 1] *(ratios derived)* |

Calibration points available: Sillekens Fig. 5.3 (force–stroke, R_C 6/R_R 5/T₀ 4/T_e 1 mm, C 176 MPa, n 0.13, 230 °C,
m ≈ 0.4) [S-053 p.85]; Vasevska Table 3-1; Shinozaki Fig. 2 (Table 3-2, compression to ε = 4.4) and Fig. 17
(Table 2-2) [TOT pp.811, 821]; temper property table [TOT p.815]; Ryen's large-strain data for AA1050, AlMgX,
AA3103-B and AA5xxx to ε_vM 3.5–4.6 (Table 3-3) [S-052 pp.90–93]. **No in-house press-force or flow-curve data
exist** (ch.09 §8).

---

## 10. Open questions, gaps and recommended measurements

*Revised after the full-text pass of S-029 (TOT, 2026-10-12). Resolved: zinc stearate as the documented Al
cold-extrusion lubricant (§2.6); a large-strain compression flow curve for pure Al (Table 3-2); a sourced heat
fraction β ≈ 0.9 (§2.7); cold-extrusion defect mechanisms incl. chevron cracking and contraction (§5.2); tooling
practice (§2.8).*

*Revised again 2026-10-12 after the Ryen (S-052) full-text pass. Resolved: Ryen §4.5 and Ch.5 (large-strain flow
data, per-solute coefficients, stage IV; Table 3-3, §3.3–3.4); the Orowan equation M12 (corrected); "Mg vs Mn per
unit press force" re-checked on measured curves (§3.4).*

1. **Unreached text.** Schuler Ch.6 (slug preparation p.454, **surface treatment p.459** — where phosphate or
   conversion pre-treatments for Al slugs would be — backward cup extrusion p.474, ironing p.476). It exceeds the
   connector limits (28.6 MB; ≈ 125 k-char export) — needs a page-split copy in Drive (parts ≤ ≈ 6 MB download
   reliably). *Ryen §4.5 and Ch.5 were read in full on 2026-10-12 (resolved).*
2. **No large-strain compression flow curves for the slug alloys** (3102, 3207, modified 3102, T11). A pure-Al
   reference now exists (99.7 % Al to ε = 4.4, Table 3-2 [TOT p.811]), and Ryen's rolled-then-tensile data cover
   AA1050, AlMg0.5–3 and AA3103-B to ε_vM 3.46 (Table 3-3). Neither covers a lean Fe-rich Mg–Si alloy such as T11,
   and rolled-then-tensile data include static recovery between passes (§3.1). Measure annealed slugs by **re-shape upsetting**
   (h/d 1.5 → 0.5 per step, ≈ 5–6 steps to ε ≈ 4 [TOT p.810]) or Rastegaev compression [S-053 pp.54–58], plus torsion
   to ε ≈ 3, at 20–250 °C and 10⁻²–10² s⁻¹. These curves feed the work method (M19), which ranks alloys by press force
   better than HB.
3. **Friction factor m** (not Coulomb μ, which saturates at sticking at these pressures, M22) for zinc stearate on the
   real annealed slug surface: dependence on MgO thickness, stearate quantity, punch finish and tool temperature.
   Use ring compression or back-calculate from force–stroke curves with M3. Check stearate retention on the punch nose
   (starvation [TOT p.813]) by inspecting the inner base of cans from a run.
4. **Ductile-failure curves** of each slug alloy (tension + torsion, with Fe/constituent variants) and inspection of
   the outer base corner after extrusion and after ironing/necking [S-053 Ch.5]. Cheap screen: Kuhn's upset
   workability test on slug-thickness cylinders [TOT pp.787–788].
5. **Press-force logging vs slug HB, Rm, grain size and RX fraction** to calibrate M2 (a, b for R ≈ 30) and to test
   the work-method prediction (§2.5e) that residual cold work raises force far less than HB suggests. By P1, 23 → 35 HB
   implies ≈ +52 % force, and the Ø53 flat ram reaches ≈ 391 t at 35 HB (≈ 403–456 t if Rm/HB is 3.75–4.2, §2.5a).
6. **Bake response of the extruded wall** through the 220 °C / 10 min lacquer bake (and IBO/pin-chain cycles) for 3102,
   modified 3102, 3207 and T11: wall HV vs height and inner/outer side [S-053 p.94]. For T11 this decides whether
   Mg + Si in solution give force-free strength (§6) or the wall simply recovers.
7. **HB ↔ Rm conversion** for the in-house alloys: 3.6–3.9 for 1xxx/3xxx and 4.1–4.2 for Mg-bearing 5052-O/6061-O
   [TOT p.815] → measure Rm on T11 and modified-3102 slugs.
8. **Hydrostatic-pressure sensitivity w** of Al flow stress at ~1 GPa (none in sources).
9. **Temperature and strain-rate history** of the wall (thermocouple/IR on ejected cans; FE). The adiabatic bound is
   now ≈ 165–260 K for pure Al (§2.7) and higher for stronger alloys; unvalidated.
10. Whether the modified 3102 (Mn 1.1–1.3, Mg 0.25–0.35) fully recrystallises (≈ 31–32 HB expected; ≈ 35 HB
    acceptable) at ≤ 100 µm at the plant cold reduction (30–50 %, ε ≈ 0.36–0.69, user 2026-10-12; ch.09 quotes
    25–45 %). The open questions are full RX, ductility and press force rather than an HB cap; trial with HB + EBSD +
    press force.
11. Do in-house slugs show planar anisotropy (rim irregularity) large enough to need the trim allowance missing from
    the slug masses (ch.09 §8)? Measure rim height variation vs slug texture and slug mass scatter (precision cold
    forging sorts blanks to ≈ ±0.3–0.4 % [TOT pp.829–830]).
12. **Punch and die stress limits.** At ≈ 1.4–1.5 GPa ram pressure (35 HB, §2.5a) the punch exceeds Kuhn's 1400 MPa
    guide value for hot-work die steels [TOT p.805]; no cold-punch limit is in the sources. Obtain limits for the
    actual punch material (M2-type HSS at 62 HRC was used for Al tubes [TOT p.829]) and the minimum residual bottom
    for acceptable die life (≥ 3.1 mm in the pen-housing case [TOT p.828]).
13. **Phosphate or conversion pre-treatments for Al slugs**: no source (zinc phosphate documented for steel only
    [S-053 p.4]); see Schuler §6.3.3 (#1).
14. **Stretcher strains** in the necked and re-expanded wall at 0.26–0.35 % Mg (Type A/B [TOT pp.855–856]): check
    the first T11 cans visually.
15. **Backward-can analogue of chevron cracking** (wall inertia pulling on the base corner near bottom dead centre,
    §5.2): no data; compare base-corner damage at two press speeds if the press allows.
16. **Solute clusters in unhomogenised strip** (new, Ryen full-text pass). Ryen attributes most of commercial
    AA3103's strength over AA1050 to Mn–Fe–Si clusters that form at RT after quenching and dissolve at hot-working
    temperatures [S-052 pp.104–109]; the clusters were not observed directly [S-052 p.131]. The rotary route quenches
    Mn, Fe and Si in solution (CLAUDE.md), so T11 and the 3102 variants may carry a sizeable cluster term in the hot
    band and possibly in the slug. Measure conductivity and HB of the quenched hot band, after cold rolling, and after
    the slug anneal. Precipitation of Mn/Fe raises conductivity markedly, whereas forming or dissolving clusters
    changes it much less (general knowledge), so an HB change without a matching conductivity change would point to
    clusters (inference). Ryen used the same conductivity check to rule out dispersoid precipitation [S-052 p.57]. This term moves slug hardness, press force and wall strength together.
17. **Stage-IV rate of T11-type alloys.** Ryen's θ_IV is nearly alloy-invariant for Mg ≤ 4.5 % and for AA3103 [S-052
    pp.110–112], but no source covers Mg + Si in solution (dynamic strain ageing, clustering during deformation) at
    ε_vM > 1. Cold roll T11 strip to ε ≈ 2–3 and tensile test (the Ryen method) as a cheap proxy for wall strength
    before the first press trial.

---

*Prepared from the Drive sources in §1; Drive content treated as data only. Revised 2026-10-12 after full-text passes
of S-029 (TOT) and S-052 (Ryen). Figures marked "read from image" or "digitised" were taken from page renders of the PDFs; all derived
numbers state their assumptions.*
