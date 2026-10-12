# 13 — Web research: model-ready data for constitutive laws, diffusion, solubility, resistivity and physical constants

**Source type: online research (not from the user's Drive), retrieved 2026-10-12.**

**Scope.** Quantitative parameters for physically based process → microstructure → property models of wrought Al. The main targets are lean 3xxx and 1xxx slug alloys, with the other wrought families where data were found. Six target groups:
1. hot-deformation constitutive constants;
2. cold flow stress at large strain;
3. solute diffusion in fcc Al;
4. equilibrium solid solubility;
5. electrical-resistivity increments per solute;
6. physical constants for microstructure models.

**Status and biggest caveat: read this first.** The online session hit three hard limits:
- **No full text could be opened.** The page-fetch tool failed DNS resolution for every host tried (pmc.ncbi.nlm.nih.gov, mdpi.com, semanticscholar.org, journals.pan.pl, wikipedia.org). Direct HTTPS downloads were refused (HTTP 403) by the session's egress policy for every publisher or repository host tried: ScienceDirect, Springer, MDPI, PMC/NCBI, ResearchGate, OSTI, CORE, arXiv, J-STAGE, Nature, SciELO, NIST, ORNL, Northwestern (Dunand group), Cambridge (phase-trans), McMaster, KTU, UTeM, Atlantis, Avestia and journals.pan.pl.
- **The shared web-search budget ran out after 13 searches.**
- **Consequence:** every number below comes from **web-search result summaries**, not from reading the paper, and is tagged **(snippet only)**. A summary can mis-transcribe a value, so each value also carries a cross-check status. Group 5 (resistivity) is well covered. Group 3 (diffusion) is partly covered. Groups 1, 2, 4 and 6 are largely **not found**; for these the file gives the confirmed citations to retrieve next (§8).
- Per the repo rule (ch. 07 §3.3), **no table was populated from memory**. Where a cell is empty, it is empty on purpose.

**Tags used.**

| Tag | Meaning |
|---|---|
| (snippet only) | The value appeared in a search-engine summary of the page; the page itself was not read |
| (citation only) | Only the bibliographic reference and/or scope was confirmed; no values |
| (derived) | Arithmetic done here from cited inputs |
| (general knowledge) | Standard constant or definition, not from a web source read here |
| ✓n | n independent web sources agree on the value |
| ✓repo | Agrees with a value already in this repo (chapter cited) |
| ✗ | Not cross-checked: single source |

---

## 0. Sources

| Key | Authors | Year | Title | Journal / venue | DOI / URL | What was read |
|---|---|---|---|---|---|---|
| W13-01 | Y. Du, Y.A. Chang, B. Huang, et al. | 2003 | Diffusion coefficients of some solutes in fcc and liquid Al: critical evaluation and correlation | Mater. Sci. Eng. A 363, 140–151 | https://www.sciencedirect.com/science/article/abs/pii/S0921509303006245 | (citation only). Scope confirmed: Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Mg, Si, Ga, Ge in fcc and liquid Al; least-squares assessment plus semi-empirical correlation; D = D₀ exp(−Q/RT). **The assessed D₀/Q table was not retrieved.** (The Academia.edu page for its Table 5 covers **liquid** Al only.) |
| W13-02 | J.V. Pearce | 2016 | Survey of key parameters of impurities in aluminium: diffusion coefficients, solubility, and liquidus slopes | Int. J. Thermophys. | 10.1007/s10765-016-2128-z; https://eprintspublications.npl.co.uk/7337/ | (citation only). Survey of 237 diffusion coefficients and 274 solubilities in liquid and solid Al. It lists the Mn tracer studies W13-07 and W13-08 and Beke et al. (1989) |
| W13-03 | Marumo, Fujikawa, Hirano | 1973 | Diffusion of zirconium in aluminum | J. Jpn. Inst. Light Met. | — | Not read. Values are via W13-04 |
| W13-04 | (OSTI report) | — | Using interfaces as templates for planar L1₂ precipitation … | OSTI | https://www.osti.gov/servlets/purl/1883854 | (snippet only). Quotes W13-03 for Zr: Q = 242 kJ/mol, D₀ = 7.18×10⁻² m²/s |
| W13-05 | (authors not shown) | 2014 | Study of dilute Al–Sc alloys giving an Arrhenius law for Sc | Metall. Mater. Trans. A | 10.1007/s11661-014-2275-4 | (snippet only). D₀ = 2.34×10⁻⁴ m²/s, Q = 167 ± 6 kJ/mol |
| W13-06 | Dunand group (file "AM05-Al-Sc-Ti_vanDalen", probably van Dalen, Dunand & Seidman, Acta Mater. 2005); De Luca et al. review | 2005; 2018 (per file name) | Effects of Ti additions on the nanostructure and creep properties … (Al–Sc–Ti); Sc-enriched nanoprecipitates review | Acta Mater. / Dunand site | https://dunand.northwestern.edu/refs/files/AM05-Al-Sc-Ti_vanDalen.pdf ; https://dunand.mccormick.northwestern.edu/pdf/deluca2018b.pdf | (snippet only). D_Zr/D_Ti = 23 at 300 °C. Ranking D_Er > D_Sc > D_Zr. ⚠ Which Dunand paper gives "23" was not verified |
| W13-07 | Lundy & Murdock | 1962 | Diffusion of Al(26) and Mn(54) in aluminum | J. Appl. Phys. 33, 1671–1673 | — | (citation only, via W13-02) |
| W13-08 | Fujikawa, Hirano | 1987 | Impurity diffusion of manganese in aluminum | Mater. Sci. Forum 13, 539–545 | — | (citation only, via W13-02) |
| W13-09 | (Diffusion Fundamentals, Leipzig) | 2022 | Diffusion in Metals and Intermetallics — an Overview | Diffusion Fundamentals 34, 02 | https://diffusion.uni-leipzig.de/pdf/volume34/diff_fund_34(2022)02.pdf | (snippet only). Qualitative: most transition metals diffuse extremely slowly in Al compared with Al self-diffusion |
| W13-10 | (first-principles study) | 2006 | First-principles calculations of impurity diffusion activation energies in Al | Phys. Rev. B 73, 014108 | https://journals.aps.org/prb/abstract/10.1103/PhysRevB.73.014108 | (abstract/snippet only). Ti, V and Cr have high activation energies, so their diffusion in Al is "anomalously" slow |
| W13-11 | (review; authors not shown) | 2024–25 | Thermal and Electrical Conductivity of Aluminum Alloys: Fundamentals, structure–property relationships, and pathways to enhance conductivity | Mater. Sci. Eng. A (PII S0921509324016976) | https://www.sciencedirect.com/science/article/pii/S0921509324016976 | (snippet only). Table of resistivity increase per wt.% in and out of solid solution for Cr, Cu, Fe, Mg, Mn, Ni, Si, Ti, V, Zn, Zr |
| W13-12 | A. Zhang, Y. Li | 2023 | Thermal Conductivity of Aluminum Alloys—A Review | Materials 16, 2972 | 10.3390/ma16082972 | (snippet only). Table 2: resistivity increments in and out of solution, plus maximum solubilities. Confirmed: Si 1.65 wt.% at 577 °C with 1.02/0.088; Mn max 1.82 wt.%; Zr max 0.28 wt.%; the in-solution column matches W13-11 for Si, Zn, Mn, Zr, Fe |
| W13-13 | (AGH University authors) | vol. 59 (year not confirmed) | Title not shown; tabulates resistivity coefficients from several sources (Zr focus) | Arch. Metall. Mater. 59(1), paper 57 | https://journals.pan.pl/Content/88342/PDF/10172%20Volume%2059%20Issue%201-57%20paper.pdf.pdf | (snippet only). Willey's in-solution coefficients (nΩ·m per wt.%). Zr precipitated 0.44 nΩ·m per wt.%. Zr coefficients across authors span 0.4–45 nΩ·m per wt.% |
| W13-14 | (authors not shown) | 2018 | Improving Elevated-Temperature Strength of an Al–Mn–Si Alloy by Strain-Induced Precipitation | (journal not shown) | https://www.researchgate.net/publication/325702705 | (snippet only). ρ = 0.0267 + 0.032Fe + 0.033Mn + 0.0068Si (wt.% in solution), attributed to its ref. [3]. Dispersoid fraction f_p = c·Δ(Mn,Fe)% with Δ(Mn,Fe)% = Δρ/0.033 and c ≈ 2.5 |
| W13-15 | Y.J. Li, L. Arnberg | 2003 | Quantitative study on the precipitation behavior of dispersoids in DC-cast AA3003 alloy during heating and homogenization | (snippet says Acta Mater.; journal **not verified**) | — | (abstract snippet only). The dispersoid volume fraction from TEM follows the same trend as the fraction calculated from electrical conductivity |
| W13-16 | (Univ. of Windsor authors) | 2023 | ICNFA paper 108 (Al–Mn conductor alloy) | Proc. NewTech 2023 / ICNFA, Avestia | https://avestia.com/NewTech2023_Proceedings/files/paper/ICNFA/ICNFA_108.pdf | (snippet only). Max Mn solubility 1.25 wt.% at 658 °C. 0.3 wt.% Mn in cast high-purity Al: 61.1 → 45.6 %IACS |
| W13-17 | (review) | 2024 | Aluminum alloys for electrical engineering: a review | J. Mater. Sci. | 10.1007/s10853-024-09890-0 | (snippet only). Mn max solubility 0.62 at.% (1.25 wt.%) at 658 °C (eutectic). Mn lowers conductivity "almost twice" as much as Zr at equal concentration |
| W13-18 | A.R. Eivani, H. Ahmed, J. Zhou, J. Duszczyk | 2009 | Correlation between electrical resistivity, particle dissolution, precipitation of dispersoids and recrystallization behaviour of AA7020 | Metall. Mater. Trans. A 40, 2435–2446 | 10.1007/s11661-009-9917-y | (abstract snippet only). Qualitative: resistivity as an indirect measure of dispersoid fraction and particle dissolution. Solute depletion raises (sub)boundary mobility |
| W13-19 | Shi et al. | 1997 | Constitutive equations for high temperature flow stress of aluminium alloys | Mater. Sci. Technol. 13, 210–216 | https://acnpsearch.tweb-dev.unibo.it/singlejournalindex/7521125 | (citation/scope only). Sah-type and sinh fits to hot **plane-strain compression** of commercial-purity Al, Al-1Mn and Al-1Mg. **Constants not retrieved** |
| W13-20 | T. Sheppard, A. Jackson | 1997 | Constitutive equations for use in prediction of flow stress during extrusion of a[luminium alloys] | Mater. Sci. Technol. (1997) | Cited in J. Cent. South Univ. Technol. 2001, 10.1007/s11771-001-0017-4 ("Flow stress equation for multipass hot-rolling of aluminum alloys") | (citation only; title truncated in the snippet) |
| W13-21 | (KTU authors) | — | AA3003 hot deformation: grain size and microhardness vs Zener–Hollomon parameter | Materials Science (Medžiagotyra), KTU | https://matsc.ktu.lt/index.php/MatSc/article/view/19436/12738 | (snippet only). Qualitative: grain size falls as Z rises; microhardness is linear in ln Z; a prediction model for steady-state flow stress and grain size exists. **Constants not retrieved** |
| W13-22 | (MDPI *Modelling* paper) | 2022 | (constitutive-modelling paper) | Modelling 3(3), 23 | https://www.mdpi.com/2673-3951/3/3/23 | (snippet only). Sellars–Tegart framework: Z = Aσⁿ at low stress, Z = A·exp(βσ) at high stress, sinh form spans both |
| W13-23 | Knipling, Dunand, Seidman | 2006 | Criteria for developing castable, creep-resistant aluminum-based alloys — a review | Z. Metallkd. 97(3), 246–265 | — | (citation only). Contains a solute D₀/Q compilation (Sc, Zr, Ti, …) that was **not retrieved** |
| W13-24 | Robson & Prangnell; Robson | 2001; 2004 | Dispersoid precipitation and process modelling in zirconium containing commercial aluminium alloys; A new model for prediction of dispersoid precipitation in aluminium alloys containing zirconium and scandium | Acta Mater. | https://www.sciencedirect.com/science/article/abs/pii/S1359645400003517 ; …/S1359645403007225 | (citation only). KWN Al₃Zr/Al₃(Sc,Zr) models that tabulate D and γ inputs |
| W13-25 | (Al–Cu–Mg–Zr thermoforming model) | 2025 | Physically based modeling of flow stress … multi-stage thermoforming of Al-Cu-Mg-Zr | J. Alloys Compd. (PII S0925838825074626) | https://www.sciencedirect.com/science/article/pii/S0925838825074626 | (snippet only). Model input for Cu: D₀ = 1×10⁻⁵ m²/s, Q = 142.3 kJ/mol. See the §3 warning |
| W13-26 | (Al–Mg–Mn study) | 2023 | Enhancement in dispersoid precipitation and dispersion strengthening by prior deformation in an Al–Mg–Mn alloy | Mater. Sci. Eng. A (PII S0921509323002320) | https://www.sciencedirect.com/science/article/abs/pii/S0921509323002320 | (abstract snippet only). Qualitative: prior deformation greatly increases the Mn diffusion distance, mainly through dislocation pipe paths |
| W13-27 | (AA3104 study) | 2024 | Intermetallic and dispersoid structures in AA3104 aluminium alloy during two-step homogenisation | Sci. Rep. | https://www.nature.com/articles/s41598-024-51890-2 | (snippet only). Qualitative: Fe and Si reduce Mn solubility and speed up Mn-dispersoid precipitation |
| W13-28 | (Phys. Rev. B) | 1970 | Impurity Diffusion in Aluminum | Phys. Rev. B 1, 3264 | https://journals.aps.org/prb/abstract/10.1103/PhysRevB.1.3264 | (citation/scope only). Arrhenius fits for Ge, Cu, Ag, Au (cm²/s); Co and Cr mentioned briefly |

---

## 1. Hot-deformation constitutive constants (Sellars–Tegart) — **status: NOT RETRIEVED**

**Framework (confirmed, W13-22, snippet only).**
- Low-stress regime: Z = A·σⁿ.
- High-stress regime: Z = A·exp(βσ).
- The hyperbolic-sine law spans both: ε̇ = A[sinh(ασ)]ⁿ·exp(−Q/RT), with Z = ε̇·exp(Q/RT).
- α = β/n links the two limits **(general knowledge)**.

**Per-alloy table.** It is left empty on purpose: no α, n, Q or A value was seen in any search result.

| Alloy | α (MPa⁻¹) | n | Q (kJ/mol) | A (s⁻¹) | T, ε̇ range | Test | Best lead (confirmed citation) |
|---|---|---|---|---|---|---|---|
| CP-Al (≈1050/1100/1200) | — | — | — | — | — | PSC | W13-19 (Shi et al. 1997, MST 13:210–216); W13-20 |
| Al-1Mn (≈3103/3003 base) | — | — | — | — | — | PSC | **W13-19**. This is the closest published analogue to the user's 3xxx slug alloys |
| Al-1Mg (≈5005/5050) | — | — | — | — | — | PSC | W13-19 |
| 3003 | — | — | — | — | — | compression | W13-21. Gives Z → grain-size and flow-stress models; constants not seen |
| 1100, 3003, 5xxx, 6063, 7075 (extrusion set) | — | — | — | — | — | (torsion/compression compilation) | W13-20 (Sheppard & Jackson 1997, MST) |
| 7075 (as-extruded) | — | — | — | — | — | compression | Materials Research (SciELO) 2012, doi 10.1590/S1516-14392012005000156 (citation only) |
| 3004/3105/3102/3207, 5052/5083/5754, 6060/6082/6061 | — | — | — | — | — | — | Not searched (budget exhausted) |

**Subgrain size vs Z** (1/δ = a + b·ln Z): **not found.** W13-21 confirms only that grain size falls as Z rises in 3003 (qualitative).

**Data-quality notes.**
- One irrelevant hit is recorded so it is not reused by mistake: Q = 320.79 kJ/mol belongs to a SiCp/Al–Cu composite, not to a wrought alloy.
- Constants depend on the test (PSC, torsion or axial compression), the strain used (peak or steady state) and the strain measure. G13 in ch. 07 still applies. When W13-19/W13-20 are retrieved, record which equivalent-strain definition they used before mixing them with the ε_t-based in-house models.

---

## 2. Cold flow stress / work hardening at large strain (Voce, Hollomon) — **status: NOT SEARCHED**

The search budget ran out before this group was reached. No online data.

- The only values in the repo remain the O-temper Hollomon fits (1100: K = 146 MPa, n = 0.242; 3003: K = 188 MPa, n = 0.242) [ch. 07 Table 5-1; ch. 06 Table 4.1, from Totten/Hatch].
- **(inference)** Hollomon parameters fitted on tensile data (uniform strain ≲ 0.3) diverge badly at the true strains of 1–4 seen in impact extrusion. Al saturates (stage IV, θ_IV ≈ 0.1·τ_IV [ch. 06, RY p.31]), so σ = K·εⁿ over-predicts flow stress at ε > 1. **Do not extrapolate Table 5-1 beyond ε ≈ 0.5 without a saturating (Voce-type) term.**
- Needed: stacked or ring compression or ECAP-calibrated Voce fits for 1050/1070/1100/3003/3103/3004 (see §8).

---

## 3. Diffusion of solutes in fcc Al

### 3.1 Arrhenius parameters found (D = D₀·exp(−Q/RT))

| Solute | D₀ (m²/s) | Q (kJ/mol) | Validity | Source | Check | Note |
|---|---|---|---|---|---|---|
| **Zr** | 7.18×10⁻² (W13-04) / 7.28×10⁻² (Sheppard Table 2.3, ch. 07 §3.5) | 242 (W13-04) / 240.8 (Sheppard) | not stated in snippet (original tracer range per W13-03) | W13-03 via W13-04 (snippet only); ch. 07 [SH] | **✓repo** (two sources agree within transcription error) | **Prefer D₀ = 7.28×10⁻² m²/s, Q = 242 kJ/mol.** "7.18" is probably a snippet mis-transcription. Both pairs give D within ±25 % over 400–640 °C (§3.2) |
| **Sc** | 2.34×10⁻⁴ | 167 ± 6 | dilute Al–Sc, temperature range not in snippet | W13-05 (snippet only) | ✗ | The classic Fujikawa Sc tracer data (Defect Diffus. Forum 143–147, 1997, p.115; citation only) were **not** retrieved. Cross-check before KWN calibration |
| Cu | 1×10⁻⁵ | 142.3 | model input, not a measurement | W13-25 (snippet only) | ✗ — **conflicts** | ⚠ Gives D(500 °C) = 2.4×10⁻¹⁵ m²/s (derived), **20× below** Polmear's 5×10⁻¹⁴ [ch. 04 §1.4] and Sheppard's Cu row (ch. 07 §3.5). **Do not use.** Keep Sheppard's Cu row (D₀ 0.29×10⁻⁴, Q 125.6), which gives 9.5×10⁻¹⁴ m²/s at 500 °C, within ×2 of Polmear (derived) |
| **Mn** | — | — | — | Held in W13-01 (assessed), W13-07, W13-08, Beke et al. 1989 (all citation only) | — | **Not retrieved.** See §3.3 for the discrepancy resolution |
| Fe, Cr, Ti, V | — | — | — | W13-01 (assessed; citation only) | — | Not retrieved. W13-10: Ti, V and Cr have high Q and are anomalously slow |
| Mg, Si, Zn | — | — | — | W13-01 (citation only) | — | Not retrieved. Sheppard's rows (ch. 07 §3.5) give D(500 °C) **×13 (Mg) and ×3 (Si)** above Polmear's 1×10⁻¹³ m²/s (derived). Usable only as order-of-magnitude values until W13-01 is read |

**Ratios and orderings (snippet only).**
- D_Zr/D_Ti = 23 at 300 °C (W13-06).
- D_Er > D_Sc > D_Zr (W13-06, De Luca review).
- Transition metals are extremely slow diffusers in Al compared with Al self-diffusion (W13-09).
- Prior cold deformation raises the effective Mn diffusion distance through pipe diffusion (W13-26). This is qualitative and relevant to strain-induced dispersoid precipitation in 3xxx.

### 3.2 Derived D(T) from the parameters above (m²/s)

| T (°C) | Zr (7.28×10⁻², 242) | Sc (2.34×10⁻⁴, 167) | Sheppard "Mn" row (2.2×10⁻⁵, 121.4) — **rejected** |
|---|---|---|---|
| 300 | 6.4×10⁻²⁴ | 1.4×10⁻¹⁹ | 1.9×10⁻¹⁶ |
| 400 | 1.2×10⁻²⁰ | 2.6×10⁻¹⁷ | 8.4×10⁻¹⁵ |
| 450 | 2.4×10⁻¹⁹ | 2.0×10⁻¹⁶ | 3.7×10⁻¹⁴ |
| 480 | 1.2×10⁻¹⁸ | 6.1×10⁻¹⁶ | 8.4×10⁻¹⁴ |
| 500 | 3.3×10⁻¹⁸ | 1.2×10⁻¹⁵ | 1.4×10⁻¹³ |
| 550 | 3.2×10⁻¹⁷ | 5.9×10⁻¹⁵ | 4.4×10⁻¹³ |
| 600 | 2.4×10⁻¹⁶ | 2.4×10⁻¹⁴ | 1.2×10⁻¹² |
| 640 | 1.0×10⁻¹⁵ | 6.6×10⁻¹⁴ | 2.5×10⁻¹² |

(derived, R = 8.314 J/mol·K)

**Implications (derived).**
- **D_Sc/D_Zr ≈ 510 at 480 °C** (≈ 2×10⁴ at 300 °C). The KWN model in ch. 04 [R1 p.1414] uses **≈ 4** at 480 °C. That is two orders of magnitude apart, which confirms the concern in ch. 04 §12 item 1.
  - Before calibrating Al₃(Sc,Zr) kinetics, check whether R1's "4" is an effective or fitted ratio (e.g. absorbed into Q*) or uses different tracer data.
  - Do not mix R1's ratio with these Arrhenius laws.
- Over 24 h at 500 °C, x = √(Dt) is ≈ 0.5 µm for Zr and ≈ 10 µm for Sc **(derived)**. Zr therefore stays segregated on the dendrite scale (20–50 µm). This is consistent with the dispersoid-free-zone discussion in ch. 04 §2.3.

### 3.3 Resolving the Mn discrepancy (ch. 07 G9; ch. 04 §12.1)

| Evidence | Mn D(500 °C) (m²/s) | x = √(Dt), 24 h at 500 °C | Status |
|---|---|---|---|
| Polmear [ch. 04 §1.4; ch. 07 §3.5] | 5×10⁻¹⁷ | ≈ 2.1 µm (derived) | consistent with W13-09/W13-10 (transition metals slow) |
| Sheppard Table 2.3 (D₀ 2.2×10⁻⁵, Q 121.4) | 1.4×10⁻¹³ (derived) | ≈ 109 µm (derived) | as fast as Mg/Si (Polmear 1×10⁻¹³). Contradicts W13-09/W13-10 and the observed persistence of Mn microsegregation |
| Zr (W13-03/04), for scale | 3.3×10⁻¹⁸ (derived) | ≈ 0.5 µm | Zr < Mn ordering is consistent with Polmear, not Sheppard |

**Q implied by Polmear's D(500 °C) = 5×10⁻¹⁷ m²/s for a range of D₀** **(derived; a sensitivity check, not data)**:

| D₀ (m²/s) | 10⁻⁴ | 10⁻³ | 10⁻² | 10⁻¹ |
|---|---|---|---|---|
| Implied Q (kJ/mol) | 182 | 197 | 212 | 227 |

**Verdict.**
- Sheppard's Mn row (Q = 121 kJ/mol) **cannot be right** for Mn in Al. For any physically plausible D₀ (10⁻⁴–10⁻¹ m²/s), Polmear's value needs Q ≈ 180–230 kJ/mol. That is well above the ~142 kJ/mol Al self-diffusion anchor [ch. 07 §3.3, general knowledge], as expected for a slow 3d solute (W13-10).
- **Use the Polmear scale for 3xxx homogenisation and dispersoid models.** Take the definitive D₀/Q from W13-01 (Du et al. 2003, assessed) or W13-08 (Fujikawa & Hirano 1987) when they can be read.
- Sheppard's Cr and Fe rows (ch. 07 §3.5) are equally suspect (W13-10: Cr anomalously slow). Do not use them.

---

## 4. Equilibrium solid solubility — **status: mostly NOT RETRIEVED**

No temperature fits (ln c = A − B/T) were found. Points obtained:

| Element | Max solubility | T (°C) | Source | Check | Note |
|---|---|---|---|---|---|
| Mn | **1.82 wt.%** (0.90 at.%) | 658 | W13-12 (snippet only); Polmear [ch. 04 §1.2] | ✓repo | — |
| Mn | **1.25 wt.% (0.62 at.%)** | 658 (eutectic) | W13-16, W13-17 (snippet only) | ✓2 (may not be independent) | ⚠ **Conflict ×1.45 with 1.82 wt.%.** Both pairs convert self-consistently (0.62 at.% ≡ 1.254 wt.%; 0.90 at.% ≡ 1.816 wt.%, derived), so this is a real data disagreement, not a unit error |
| Zr | 0.28 wt.% | (peritectic) | W13-12 (snippet only); Polmear [ch. 04 §1.2] | ✓repo | — |
| Si | 1.65 wt.% | 577 | W13-12 (snippet only); Polmear [ch. 04 §1.2] | ✓repo | — |

**Which Mn value to prefer.**
- Keep **1.82 wt.%** for now. It is consistent with the temperature-dependent Al–Mn binary table already in the repo (ch. 04 §1.3, 1.8 wt.% at 654 °C [R8]).
- Flag the conflict for resolution against an assessed Al–Mn diagram.
- For 3xxx models this matters little: with Fe and Si present, Mn solubility at homogenisation temperatures is 5–30× lower than the binary maximum (ch. 04 §1.3). W13-27 confirms qualitatively that Fe and Si reduce Mn solubility and speed up dispersoid precipitation.

Fe, Mg, Cu, Zn, Cr, Sc and Ti versus T: not found online. The repo already holds Sc/Zr points (ch. 04 §1.3).

---

## 5. Electrical-resistivity increments (Matthiessen's rule) — **status: FILLED (snippet level, cross-checked)**

### 5.1 Increment per wt.% solute, room temperature

| Element | In solid solution (µΩ·cm per wt.%) | Out of solution (µΩ·cm per wt.%) | Ratio out/in (derived) | In solution per at.% (µΩ·cm, derived) | Willey, in solution (W13-13) (µΩ·cm/wt.%, converted) | Check |
|---|---|---|---|---|---|---|
| Cr | **4.00** | 0.18 | 0.045 | 7.7 | 4.0 | in-solution ✓2; out ✗ |
| V | **3.58** | 0.28 | 0.078 | 6.8 | 3.6 | in ✓2; out ✗ |
| Mn | **2.94** | 0.34 | 0.116 | 6.0 | 2.9 | in ✓3 (W13-11/12/13); out ✗ |
| Ti | **2.88** | 0.12 | 0.042 | 5.1 | 2.9 | in ✓2; out ✗ |
| Fe | **2.56** | 0.058 | 0.023 | 5.3 | 2.6 | in ✓3; out ✓repo (ch. 06 §2: ≈ 0.05 derived from HB p.53) |
| Zr | **1.74** | 0.044 | 0.025 | 5.9 | 1.74 | in ✓3; out ✓2 (W13-13: 0.44 nΩ·m) |
| Si | **1.02** | 0.088 | 0.086 | 1.06 | 1.0 | in ✓3; out ✓2 (W13-12) |
| Ni | 0.81 | 0.061 | 0.075 | 1.8 | 0.8 | in ✓2; out ✗ |
| Mg | 0.54 | 0.22 | 0.41 | 0.49 | 0.5 | in ✓2; out ✗ |
| Cu | 0.344 | 0.030 | 0.087 | 0.81 | 0.34 | in ✓2; out ✗ |
| Zn | 0.09 | 0.023 | 0.26 | 0.22 | 0.1 | in ✓3; out ✗ |
| Li | — | — | — | — | 3.3 | ✗ (W13-13 only) |

**Sources.**
- Main columns: W13-11 (snippet only). The in-solution values for Si, Zn, Mn, Zr and Fe are confirmed by W13-12 (snippet only).
- Willey column: W13-13 (snippet only), converted from nΩ·m (1 nΩ·m = 0.1 µΩ·cm).
- Per-at.% values (derived): Δρ_at = Δρ_wt × M_X/M_Al, valid for dilute solutions, with standard atomic masses **(general knowledge)**.

**Data-quality notes.**
- **The three compilations are probably not independent.** Willey's data (ASM, 1960s) are the likely common ancestor of the Hatch-type table reproduced in W13-11 and W13-12. Their agreement shows consistent transcription, not independent measurement.
- The spread across *all* authors is large: for Zr, 0.4–45 nΩ·m per wt.% (W13-13).
- "Out of solution" values depend on particle size and fraction. Treat them as order-of-magnitude values: roughly 2–12 % of the in-solution effect for transition metals, ~40 % for Mg (derived from the ratios above).
- **Cross-check against repo ranking (ch. 06 §2, Fridlyander):** Cr > V > Mn > Ti > … The top four in-solution values above follow exactly this order ✓.
  - Fridlyander places Fe and Ni last because, in practice, they sit in particles (out-of-solution 0.058 and 0.061).
- **Cross-check against W13-17:** Mn costs "almost twice" the conductivity of Zr. Per wt.%, 2.94/1.74 = 1.69 (derived) ✓. Per at.% they are nearly equal (6.0 vs 5.9, derived).

### 5.2 3xxx-specific relation (Mn, Fe, Si in solution)

- **ρ (µΩ·m) = 0.0267 + 0.032·Fe_ss + 0.033·Mn_ss + 0.0068·Si_ss** (wt.% in solid solution). Source: W13-14 (snippet only), attributed to its ref. [3], probably the Li & Arnberg AA3003 work (W13-15). ✗ Not verified against the original.
  - Same relation in µΩ·cm **(derived)**: ρ = 2.67 + 3.2·Fe_ss + 3.3·Mn_ss + 0.68·Si_ss.
  - ρ₀ = 2.67 µΩ·cm ≈ 64.6 %IACS (derived, using 100 %IACS = 1.7241 µΩ·cm, general knowledge). This is consistent with 99.99 % Al at 2.68 µΩ·cm [ch. 06 Table 2.1] ✓repo.
- **Dispersoid fraction from resistivity (W13-14, snippet only):**
  - f_p = c·Δ(Mn,Fe)%, with Δ(Mn,Fe)% = |Δρ|/0.033 (ρ in µΩ·m) and **c ≈ 2.5** (presumably vol.% of dispersoid per wt.% of Mn+Fe precipitated; source of c not shown).
  - The sign convention and the units of c are **not verified**.
  - W13-15 reports that TEM-measured dispersoid fractions follow the same trend as conductivity-derived ones (AA3003).
- **Independent check, Mn (derived from W13-16):** cast high-purity Al + 0.3 wt.% Mn goes from 61.1 to 45.6 %IACS. That is ρ 2.82 → 3.78 µΩ·cm, i.e. **≈ 3.2 µΩ·cm per wt.% Mn**, assuming all Mn is in solution and nothing else changes. This sits between 2.94 (Hatch/Willey) and 3.3 (3003 fit) ✓.

**Which Mn coefficient to prefer.**
- In a full Matthiessen sum using the §5.1 table: **2.94 µΩ·cm/wt.%**.
- In 3xxx dispersoid-fraction inversions that use the W13-14 framework: **3.3** (W13-14 fit), so that c ≈ 2.5 stays consistent.
- Realistic uncertainty ≈ ±10 % (spread 2.94–3.3).
- For Fe_ss and Si_ss, the 3003 fit (3.2 and 0.68) and Hatch/Willey (2.56 and 1.02) differ by ±25–50 %. Fe_ss is tiny (≤ 0.05 wt.%, ch. 04 §1.2), so this matters little; Si_ss does matter.

### 5.3 Model-ready use (derived)

**Equation.** ρ₂₀ = ρ_Al + Σᵢ (aᵢ^ss·cᵢ^ss + aᵢ^out·cᵢ^out) (+ dislocation and vacancy terms), with %IACS = 172.41/ρ[µΩ·cm].
- ρ_Al: use 2.63–2.68 µΩ·cm [ch. 06 Table 2.1].
- Vacancies add 3.4 µΩ·cm per at.% [ch. 06, HB p.39].
- **Temper effect:** cold work raises ρ by ~0.045 µΩ·cm in commercial Al (ch. 06 pitfall), the same order as 0.1 wt.% Fe out of solution.

**3xxx conductivity sensor (derived).** Precipitating 0.1 wt.% Mn from solution lowers ρ by 0.1 × (2.94 − 0.34) = 0.26 µΩ·cm:

| Starting ρ (µΩ·cm) | Starting %IACS | Gain (%IACS) |
|---|---|---|
| 4.2 | 41.0 | +2.7 |
| 3.4 | 50.7 | +4.2 |

A standard eddy-current conductivity meter can therefore resolve Mn precipitation steps of ~0.01–0.02 wt.% (inference).

---

## 6. Physical constants for microstructure models — **status: NOT SEARCHED online**

The budget ran out before this group was reached. No new online values. The repo already contains, from book sources:

| Constant | Value in repo | Where | Note |
|---|---|---|---|
| Shear modulus G (RT) | 25.4 GPa [HH]; 25–26.5 (high purity) / 27–28 GPa (commercial) [HB]; 26 GPa [WP] | ch. 03 §2; ch. 06 Table 2.1 | **G(T) not available**, still a gap |
| Burgers vector b | 0.286 nm | ch. 03; ch. 04 §11 (derived a/√2 = 0.2863); ch. 06 | — |
| Taylor factor M | **3.06 (random fcc), sourced [RY p.50]** | ch. 06 Table 4.1 | ⚠ **Repo inconsistency:** ch. 03 §2 and ch. 04 §12.13 say M is "general knowledge / not stated in any source". ch. 06 shows it *is* sourced |
| HAGB energy | 0.324 J/m² (Murr 1975) [HH] | ch. 03 §2 | — |
| HAGB / LAGB mobility | LAGB Q 125–154 kJ/mol (Al–0.05Si); HP-Al HAGB Q 63–67 kJ/mol [HH] | ch. 03 §2, §4.1 | pre-factor M₀ still missing |
| SFE | ~170 mJ/m² [POL] vs ≈ 200 mJ/m² [HB] | ch. 07 §3.1; ch. 06 Table 2.1 | conflict not resolved here |
| Interfacial energy Al₃Sc, Al₃(Sc,Zr) | 0.05–0.13 (cluster), 0.1 (KWN), 0.06–0.18 J/m² (exp.) | ch. 04 §11 | **Al₆Mn, α-AlMnSi and Al₃Zr (alone): still missing** |
| Solute drag | CLS form only, no per-solute α, β | ch. 03 §4.1 | still missing |

---

## 7. Which gaps this fills

| Repo gap | Status after this file |
|---|---|
| ch. 06 §2: missing per-wt.% conductivity coefficients | **Filled** (§5.1; snippet level; in-solution values cross-checked across 2–3 compilations) |
| ch. 04 §12 item 11: resistivity per wt.% in solution and per amount precipitated | **Filled** for per-wt.% in and out of solution (§5.1). The 3xxx dispersoid-fraction inversion is in §5.2. A per-vol.%-of-precipitate coefficient is available only via c ≈ 2.5 (unverified) |
| ch. 07 G9 / §3.5: Mn (and Cr, Fe) diffusivity discrepancy | **Resolved qualitatively and by derived consistency checks** (§3.3): reject Sheppard's Mn/Cr/Fe rows; use the Polmear scale. The Zr row is confirmed. The final Mn D₀/Q is still to be read from W13-01/W13-08 |
| ch. 04 §1.4 / §12 item 1: D₀/Q per element; D_Sc/D_Zr reconciliation | **Partly filled**: Zr (✓repo) and Sc (✗). Derived D_Sc/D_Zr ≈ 510 at 480 °C vs ≈ 4 in R1. **Mismatch confirmed** |
| ch. 04 §12 item 13 / ch. 03 open item 7: Taylor factor | Repo-internal: ch. 06 already has a sourced M = 3.06 [RY p.50] (§6) |
| ch. 07 G1: sinh-law constants, subgrain–Z relation | **Not filled.** Confirmed citations identified (W13-19, W13-20, W13-21) |
| ch. 07 G13: strain-measure consistency | Not addressed by data. The note in §1 applies when W13-19/W13-20 are retrieved |
| Cold large-strain flow curves (impact extrusion) | **Not filled** (§2) |

---

## 8. Open questions / not found — retrieval worklist (priority order)

1. **Du et al. 2003, MSE A 363:140–151 (W13-01), assessed fcc-Al table.** One read fills Mn, Fe, Cr, Ti, V, Cu, Mg, Si and Zn D₀/Q and closes G9 quantitatively. Cross-check Mn against Fujikawa & Hirano 1987 (W13-08) and Lundy & Murdock 1962 (W13-07).
2. **Sc tracer data.** Fujikawa, Defect Diffus. Forum 143–147 (1997) 115 (citation only), to cross-check W13-05 (2.34×10⁻⁴ m²/s, 167 kJ/mol). Then re-examine R1's D_Sc/D_Zr ≈ 4.
3. **Shi et al. 1997, MST 13:210–216 (W13-19).** Sinh/Sah constants for CP-Al, Al-1Mn and Al-1Mg in PSC: the most direct analogue for 1xxx/3xxx slug stock.
4. **Sheppard & Jackson 1997, MST (W13-20).** Per-alloy α, n, Q, ln A for the extrusion alloy set. Also the J. Cent. South Univ. 2001 multipass-rolling flow-stress paper (10.1007/s11771-001-0017-4).
5. **AA3003 Z-model (W13-21, KTU).** Steady-state σ(Z) and grain size d(Z).
6. **Cold large-strain flow curves** (not searched): Voce/Hockett–Sherby fits for 1050/1070/1100/3003/3103/3004 to ε = 1–4 (stacked compression, ECAP, cold-forging flow-curve atlases).
7. **Solubility vs T fits** for Mn, Fe, Si, Mg, Cu, Zn, Cr, Zr, Sc and Ti (not found). Resolve the Mn maximum 1.82 vs 1.25 wt.% (§4) against an assessed Al–Mn diagram. Pearce 2016 (W13-02) compiles 274 solubility entries.
8. **Li & Arnberg 2003 (W13-15) and W13-14 ref. [3].** Verify the 3003 resistivity equation coefficients, units and the c ≈ 2.5 constant.
9. **Physical constants** (not searched): G(T) (e.g. Frost & Ashby form); GB mobility pre-factor; Al₆Mn, α-Al(Mn,Fe)Si and Al₃Zr interfacial energies (Robson 2001/2004, W13-24, for Al₃Zr); per-solute solute-drag parameters; resolve SFE 170 vs 200 mJ/m².
10. **Knipling, Dunand & Seidman 2006, Z. Metallkd. 97:246–265 (W13-23).** Compiled D₀/Q for trialuminide formers (Sc, Zr, Ti, V, Hf, Er): a second source for Zr/Sc/Ti/V.

**Access note for the next attempt.** All of the above sit on hosts this session's egress policy blocked (sciencedirect.com, link.springer.com, mdpi.com, ncbi.nlm.nih.gov, osti.gov, researchgate.net, journals.pan.pl, matsc.ktu.lt, dunand.northwestern.edu, etc.). The fetch tool also failed DNS for every host tried. Either allow these hosts in the environment's network settings, or put the PDFs into the user's Drive.
