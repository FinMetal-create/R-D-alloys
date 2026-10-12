# 04 — Precipitation, Dispersoids and Alloying Elements in Wrought Al

**Scope.** Physical-metallurgy knowledge base for the chain *composition → solidification (partitioning) → homogenisation (dispersoid precipitation) → deformation/annealing (Zener pinning, RX) → ageing (clusters/precipitates) → strength, conductivity, corrosion*. Focus: 3xxx heat-exchanger/foil alloys (AA3102, AA3207), with 1xxx/5xxx/6xxx/7xxx/8xxx where the sources allow. Topics: solid solubility, diffusion, partitioning; Mn/Fe/Cr/Zr/Sc dispersoids; L1₂ Al₃Sc / Al₃Zr / Al₃(Sc,Zr); KWN-type precipitation modelling; clusters and precipitation sequences; strengthening; per-element effects; Sc cost and substitutes; Mo.

**Conventions.** wt% unless stated. Citations are `[Ref, p.x]`: the printed journal or book page, or `§` for a section. **(derived)** means I calculated it from the cited numbers. **(inference)** means it is my synthesis of the cited facts, not a claim the source makes. **(general knowledge)** means it is not in any source here. These are kept to a minimum and must be checked before use in a model. Equations that lost symbols in PDF text extraction are flagged ⚠.

## Sources

| Ref | Title (Drive file name) | Drive link | Readability / coverage |
|---|---|---|---|
| R1 | Robson J.D., *A new model for prediction of dispersoid precipitation in aluminium alloys containing zirconium and scandium*, Acta Mater. 52 (2004) 1409–1421 ("A new model for prediction of dispersoid percipitation in Al, zr, sC alloys.pdf") | https://drive.google.com/file/d/1hVcF0Jxx5hg5BVVJJjPNyGk8o0oslgRk/view | Full text (13 pp) read. Equation layout is garbled in extraction but reconstructable; figures (curves) are not readable. |
| R2 | Williams C.R., *The Effects of Scandium and Zirconium Additions on Aluminum Mechanical Properties, Post-Braze Grain Structure, and Extrusion*, MS thesis, Ohio Univ. 2012 ("Effects of Zr and Sc on Aluminium.pdf") | https://drive.google.com/file/d/1MYsjf2OwlDfrOtnb1zQas-DV9wfunqne/view | Full text (~56 pp) read. Figures and graphs (e.g. Fig. 6, RX temperature vs. additions) are not readable. Directly relevant to brazed 3102 tube. |
| R3 | Røyset J., *Scandium in aluminium alloys overview: physical metallurgy, properties and applications*, Metall. Sci. Tech. 25(2) (2007) 11–21 ("Scandium and Aluminum alloys.pdf") | https://drive.google.com/file/d/1FizSqhIa3XAhPQpZYt0maHVsHdEsKrhW/view | Full text read. Two-column text is interleaved, but Tables 1 and 2 were recoverable. |
| R4 | Røyset J., Ryum N., *Scandium in aluminium alloys*, Int. Mater. Rev. 50 (2005) 19–44 ("Royset-2005-Scandium Aluminium.pdf") | https://drive.google.com/file/d/1A_yvqnRq-o1I53m3tieuVp4Sq5zUu1iL/view | Full text (26 pp) read. All tables were readable except Table 3, which is partly garbled. Figures are not readable. Main Sc reference. |
| R5 | Ivanov R., *Solute clustering in multi-component aluminium alloys*, PhD thesis, Univ. Grenoble Alpes 2017 ("Clusters in Al alloys.pdf") | https://drive.google.com/file/d/1x56HZKJZm77CxOCd9uFSz4Zlj6UclDIr/view | **Extraction truncated at thesis p.73**: Ch. 1–5.3.2 were read; Ch. 6–9 are missing, apart from their summaries on pp.5–6. Equations lost their symbols. Focus is Al-Cu-(Li,Mg). |
| R6 | Zaid A.I.O., Atieh A.M., *Effect of molybdenum addition on aluminium grain refined by titanium…*, IOP Conf. Ser. MSE 60 (2014) 012052 ("Al_Mo.pdf") | https://drive.google.com/file/d/1ON8iVgDGl7jAcEPzomcKjFVIabk8ld_Q/view | Full (8 pp) read. Low information: casting and ECAP grain size only. No solubility, dispersoid or thermal-stability data. |
| R7 | Rana R.S., Purohit R., Das S., *Reviews on the influences of alloying elements on the microstructure and mechanical properties of aluminum alloys and aluminum alloy composites*, IJSRP 2(6) 2012 ("Influence of alloying elements.pdf") | https://drive.google.com/file/d/1eenW1k-qr4_bAY3wtnZBPPDu-uDBzGJC/view | Full (7 pp) read. Qualitative and casting-oriented; text interleaved. |
| R8 | Belov N.A., Eskin D.G., Aksenov A.A., *Multicomponent Phase Diagrams: Applications for Commercial Aluminum Alloys*, Elsevier 2005, Ch. 1 "Alloys of the Al-Fe-Mn-Si system" ("Chapter 1 - Alloys of the Al_Fe_Mn_Si System.pdf") — *found by Drive search* | https://drive.google.com/file/d/1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD/view | Full chapter (pp.1–46) read. Tables 1.9 and 1.13 were reconstructed from garbled columns. Figures are lost. Key source for 3xxx. |
| R9 | Eskin D.G., *Physical Metallurgy of Direct Chill Casting of Aluminum Alloys*, CRC 2008, Ch. 2 "Solidification of aluminum alloys" ("62816_ch02.pdf") — *found by Drive search* | https://drive.google.com/file/d/1MBeZaNbetcIq6Xjcoj2Y56AW9wZPwcb2/view | Full chapter read (text interleaved). Used for Scheil, growth restriction and Al–Sc–Zr. |
| R10 | Davis J.R. (ed.), *Alloying: Understanding the Basics*, ASM 2001, "Aluminum and Aluminum Alloys" pp.351–416 ("Aluminum and Aluminum Alloys Davis.pdf") — *found by Drive search* | https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view | Full read. Good per-element text; Table 8 gives solid-solution strengthening data. Figures are not readable. |
| R11 | Polmear I.J., *Light Alloys*, 4th ed., Butterworth-Heinemann 2006 ("115132137-Light-Alloys.pdf") — *found by Drive search* | https://drive.google.com/file/d/1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w/view | **Extraction truncated at ~book p.174** (Ch. 1–3). Ch. 2 was read fully; Ch. 3 in parts. Some symbols (π, −, Greek) were lost. |
| R12 | Humphreys F.J., Hatherly M., *Recrystallization and Related Annealing Phenomena*, 2nd ed., Elsevier 2004 ("85721252-…Re-Crystallization…pdf") — *found by Drive search* | https://drive.google.com/file/d/1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w/view | Extraction truncated at ~book p.190. Only §4.6 (Zener drag) was used. γ symbols were lost and have been restored. |

Not used:
- Anything in the `microstructure-sim-v2.14.0` tree (`src/models/*.js`, `App.jsx`, tests), as instructed.
- `AA3207_Recrystallization_Simulation.xlsx`, which is a user model, not literature.
- Large handbooks (ASM vol. 1, *Alminium.pdf*, extrusion books, Kaufman), which I did not read. They are candidates for later passes.

---

## 0. Executive summary for alloy design (3xxx-centred)

1. **Mn dispersoid budget is set by casting plus Fe/Si, not by the nominal Mn.**
   - Binary Mn solubility falls from 1.82 % at 658 °C to about 0.2 % at 427 °C [R11 p.30; R8 p.12 Table 1.9].
   - When Al₃Fe and Al₆(FeMn) are co-present, Mn solubility drops to 0.23 % at 654 °C and 0.026 % at 427 °C [R8 Table 1.9].
   - In the Si-saturated field, Mn solubility is ≤0.08 % from 573 °C downwards [R8 Table 1.13].
   - Only 0.2–0.3 % Mn tends to stay in solid solution after preheat and hot work [R11 p.30].
2. **Si converts Mn chemistry from Al₆(Mn,Fe) to α-Al₁₅(FeMn)₃Si₂.**
   - Si enables α-dispersoid formation during annealing [R8 p.32].
   - Si drastically lowers Mn solubility, so more Mn precipitates [R8 Table 1.13].
   - When Fe and Si are fully bound in α, the Mn and Si left in (Al) set the dispersoid amount [R8 p.37].
   - Homogenisation transforms Al₆(Fe,Mn) into α-Al₁₂(Fe,Mn)₃Si [R11 p.106].
3. **Dispersoid number density, not size, is the lever. Supersaturation drives nucleation.**
   - Extra Sc/Zr mainly raises number density; radius stays about 10 nm at 480 °C [R1 pp.1415, 1419].
   - Recrystallisation resistance is best when dispersoids form at T_disp < T_anneal before deformation, or during an intermediate anneal [R4 p.35].
   - Slow heating (50–75 °C h⁻¹) promotes fine, uniform dispersoids [R11 p.105].
4. **Sc + Zr core–shell L1₂ is the strongest anti-RX dispersoid, and very little Sc is needed.**
   - In 7050, 0.02 % Sc is predicted to almost eliminate recrystallisation [R1 p.1420].
   - Zr slows coarsening and the late stage of precipitation; it does not change the start [R4 p.32; R3 p.14].
   - **Braze-cycle caution (3102 tube):** 0.19Sc–0.05Zr extruded tube stayed unrecrystallised to 575 °C but recrystallised by 600 °C in a 2 min braze. This was attributed to dissolution (solvus about 595 °C for 0.19 % Sc) [R2 pp.41, 52].
   - Sc left in solution after brazing can be recovered by a post-braze 288 °C/8 h age: YS 154 MPa vs 60 MPa (+156 %), and vs 39 MPa for brazed AA3102 [R2 p.48].
5. **Cost.**
   - At about US$2000/kg Sc in master alloy, 0.2 % Sc adds about US$4/kg (3–4× the alloy price) [R4 p.39].
   - 0.02 % Sc would add about US$0.40/kg (derived).
   - Red-mud Sc₂O₃ was projected at about US$400/kg Sc, i.e. US$0.80/kg at 0.2 % Sc [R4 p.40].
   - Zr (up to Al₃Sc₀.₆Zr₀.₄), Ti, Hf and rare earths (Y, Gd, Ho, Er) substitute on the Sc sublattice [R9 p.68; R4 pp.24, 33; R3 p.15].
6. **Si and Fe are Sc poisons.**
   - Si makes the ternary V-phase AlSc₂Si₂, promotes discontinuous precipitation and delays the late stage of Al₃Sc precipitation. Fe also delays the late stage [R4 pp.22, 32–33].
   - **(inference)** 3xxx + Sc needs low Si. Al₃Sc formed at 0.4Sc/≤0.8Si but not at 0.10Sc/1.10Si [R4 p.32].

---

## 1. Thermodynamic and kinetic base data: solubility, diffusion, partitioning

### 1.1 Mechanisms

- **Few elements have large solubility.**
  - Only Zn and Mg (>10 at%), Cu and Si have significant solid solubility in Al.
  - Cr, Mn and Zr have <1 at% but are used to form compounds that control grain structure.
  - Maximum solubility occurs at the eutectic or peritectic temperature (Sn excepted) [R11 p.29].
- **Peritectic versus eutectic formers.**
  - Polmear: the maximum solubility is peritectic for **Cr, Ti, V, Zn, Zr** and eutectic for all others in his table [R11 p.30 note (i)].
  - Peritectic aluminium ends: Mo [R10 p.383; R6 p.3], V (VAl₁₁) [R10 p.385], Nb [R10 p.383], Zr [R10 p.390].
  - Ti and Cr particles form by peritectic reactions in as-cast 6xxx; Mn forms eutectic particles [R9, 6xxx section].
  - Al–Ti is peritectic (Al₃Ti); Al–Sc is eutectic (Al₃Sc) [R9 p.68].
- **Partitioning sign follows from this.**
  - k > 1 (peritectic, e.g. Zr): the element enriches dendrite **centres**.
  - k < 1 (eutectic, e.g. Sc): the element enriches dendrite **edges** [R1 p.1411].
  - In peritectic and hypereutectic systems, constitutional undercooling is caused by the solvent (Al) [R9 p.60 footnote].
- **Solid solution after casting is supersaturated.**
  - Mn and Cr in chill-cast ingot "greatly exceed the equilibrium solubility" [R10 p.369].
  - Mn "remains in solution when chill cast, so that most of the manganese added is substantially retained in solution, even in large ingots" [R10 p.382].
  - Fe lowers the as-cast Mn supersaturation because Mn is bound in Al₆(FeMn) [R8 p.12].

### 1.2 Maximum solid solubility (binary)

| Element | T (°C) | wt % | at % | Eutectic / peritectic | Source |
|---|---|---|---|---|---|
| Ag | 566 | 55.6 | 23.8 | E | [R11 p.30] |
| Cd | 649 | 0.4 | 0.09 | E | [R11 p.30] |
| Co | 657 | 0.02 | 0.01 | E | [R11 p.30] |
| Cr | 661 | 0.77 | 0.40 | **P** | [R11 p.30] |
| Cu | 548 | 5.65 | 2.40 | E | [R11 p.30] |
| Fe | 655 | 0.05 | 0.025 | E | [R11 p.30]; ≈0.05 [R10 pp.379, 388]; ≤0.05 [R8 p.3] |
| Ge | 424 | 7.2 | 2.7 | E | [R11 p.30] |
| Li | 600 | 4.2 | 16.3 | E | [R11 p.30] |
| Mg | 450 | 17.4 | 18.5 | E | [R11 p.30; R10 p.380] |
| Mg₂Si (quasi-binary) | — | 1.85 | — | — | decreases with T [R10 p.380] |
| Mn | 658 | 1.82 | 0.90 | E | [R11 p.30]; 1.8 at 654 °C [R8 Table 1.9] |
| Ni | 640 | 0.04 | 0.02 | E | [R11 p.30; R10 p.383] |
| Sc | 655–659 (eutectic) | ≈0.35 (≈0.38 max quoted) | — | E (eutectic ≈0.6 wt% Sc) | [R4 p.20; R3 p.13] |
| Si | 577 | 1.65 | 1.59 | E | [R11 p.30] |
| Sn | 228 | ~0.06 | ~0.01 | — | [R11 p.30] |
| Ti | 665 | ~1.3 | ~0.74 | **P** | [R11 p.30] |
| V | 661 | ~0.4 | ~0.21 | **P** | [R11 p.30] |
| Zn | 443 | 82.8 | 66.4 | **P** (per source) | [R11 p.30] |
| Zr | 660.5 | 0.28 | 0.08 | **P** | [R11 p.30] |
| Mo | — | — | — | **P** ("peritectic limit" ≈0.1 wt%) | [R6 p.3; R10 p.383] |
| Sb | — | <0.01 | — | — | [R10 p.371] |
| P | 660 (melt) | ~0.01 in liquid | — | — | [R10 p.383] |

Solubility at 20 °C is about 2 wt% for Mg and Zn, 0.1–0.2 wt% for Ge, Li and Ag, and <0.1 wt% for all other elements [R11 p.30 note (ii)].

### 1.3 Solubility versus temperature (model-ready points)

**Mn in (Al) with Fe and/or Si present — the key 3xxx dataset.**

| T (°C) | Binary Al–Mn | (Al)+Al₃Fe+Al₆(FeMn) | (Al)+Al₆Mn+α-Al₁₅Mn₃Si₂ | (Al)+(Si)+α-Al₁₅Mn₃Si₂ |
|---|---|---|---|---|
| 654 | 1.8 Mn | 0.23 Mn / 0.044 Fe | — | — |
| 649 | — | — | 1.3 Mn / 0.10 Si | — |
| 627 | 1.0 | 0.13 | — | — |
| 600 | — | — | 0.73 Mn / 0.09 Si | — |
| 573 | — | — | — | 0.08 Mn / 1.66 Si |
| 550 | — | — | 0.44 / 0.08 | 0.07 / 1.36 |
| 527 | 0.42 | 0.05 | — | — |
| 500 | — | — | 0.25 / 0.08 | 0.06 / 0.85 |
| 450 | — | — | 0.15 / 0.08 | 0.05 / 0.45 |
| 427 | 0.2 | 0.026 | — | — |
| 400 | — | — | 0.06 / 0.08 | 0.04 / 0.25 |

Sources: binary and Fe columns from [R8 p.12 Table 1.9; values below 654 °C are approximations]; Si columns from [R8 p.14 Table 1.13] (Drits 1977 and Phillips 1959; I reconstructed the columns from the garbled extraction ⚠). In the α+Al₆Mn field Mn solubility is about the same as binary Al–Mn; in the Si-saturated field Mn is ≤0.1 % [R8 p.13 text]. Note that R8 Fig 1.4b (Mondolfo) disagrees: it shows ~1 % Mn at 527 °C instead of ~0.4 %. The calculated 550 °C section (Du et al. 2004) agrees with the table [R8 p.13].

**Fe and Si.**
- Fe in (Al) is ≤0.05 % [R8 p.3].
- Secondary (solid-state) Fe-phase volume cannot exceed 0.1–0.2 vol% [R8 p.10; R9].

**Sc.**
- About 0.025 wt% at 430 °C (binary) [R4 p.22].
- With Zr present, mutual equilibrium solubilities are 0.03 % Sc + 0.06 % Zr at 550 °C, and 0.06 % Sc + 0.09 % Zr at 600 °C [R9 p.68].
- Williams reads a solvus of about 595 °C for his 0.19 % Sc alloy [R2 p.41].
- At 100 K s⁻¹ cooling the eutectic drops 3–4 °C, the eutectic composition rises from 0.6 to 0.7 % and the maximum solubility rises to ~0.6 % [R4 p.21]. R3 gives the same ~0.6 % [R3 p.13].
- Melt-spinning gives >5 % [R3 p.13].
- Sc + Zr total solubility is somewhat higher than Sc alone, and as-cast supersaturation of Sc + Zr exceeds that of Sc or Zr alone (conductivity data, Al–1.5(Sc+Zr)) [R4 p.34].

**Ternary effects on Sc solubility.**
- Mg and Sc mutually reduce each other's solubility. The α-Al corner is at 10.5 Mg / 0.007 Sc at 430 °C [R4 p.21].
- Mn does not lower Sc solubility; Sc distinctly lowers Mn solubility. The Al–Mn–Sc corner is at 0.08 Sc / 0.2 Mn (500 °C) and 0.2 Sc / 0.55 Mn (600 °C) [R4 p.23].
- Si does not change Sc solubility; Sc lowers Si solubility [R4 p.22].
- Cu solubility decreases slightly with Sc; Sc solubility is unaffected by Cu [R4 p.22].
- In 7050 and 2024, Cu, Mg and Zn shift the Al₃(Sc,Zr) solvus to lower Sc and Zr. The shift is largest in 7050, so less Sc/Zr is needed for the same volume fraction [R1 pp.1410–1411].

### 1.4 Diffusion data

| Quantity | Value | Conditions | Source |
|---|---|---|---|
| D_Mn in Al | 5×10⁻¹³ cm² s⁻¹ (= 5×10⁻¹⁷ m² s⁻¹) | 500 °C | [R11 p.105] |
| D_Cu in Al | 5×10⁻¹⁰ cm² s⁻¹ (= 5×10⁻¹⁴ m² s⁻¹) | 500 °C | [R11 p.105] |
| D_Mg, D_Si in Al | 1×10⁻⁹ cm² s⁻¹ (= 1×10⁻¹³ m² s⁻¹) | 500 °C | [R11 p.105] |
| D_Sc / D_Zr | ≈ 4 | at 480 °C, as used in the KWN model | [R1 p.1414] |
| Q* (atom transfer across nucleus interface) | ≈ 2.07 eV atom⁻¹ | within the range reported for Sc and Zr | [R1 p.1412] |
| Cr | "slow diffusion rate" → fine dispersed phases | qualitative | [R10 p.373] |
| Dispersoid formers | "modest solubility and … diffuse slowly" | qualitative | [R11 p.78] |

- Diffusion distance is x = √(Dt) [R11 p.105].
- Doubling x needs 4× time. Raising the homogenisation temperature by 50 °C cuts time to about ⅓. Practical homogenisation times are 6–24 h [R11 p.105].
- **(derived)** For 24 h at 500 °C, x ≈ 2 µm for Mn, ≈ 66 µm for Cu and ≈ 93 µm for Mg/Si. Mn therefore never levels across a 20–50 µm dendrite cell; Cu, Mg and Si do.
- In KWN slice models, long-range Sc and Zr diffusion between dendrite slices had only a minor effect [R1 p.1413].
- **D₀ and Q for individual solutes are not given in any source read.** See §12.

### 1.5 Partition coefficients, Scheil and growth restriction

- **Gulliver–Scheil (liquid):** C_L = C₀(1 − f_s)^(k−1), with k = C_S/C_L [R9 p.29, Eq 2.4].
  - This assumes complete liquid diffusion and none in the solid.
  - Al–4Cu leaves about 8 vol% liquid at the eutectic temperature [R9 p.31].
- **Solid-profile form used to initialise KWN:** c = k c̄ (1 − f_s)^(k−1), where f_s ≈ fractional distance from dendrite centre to edge [R1 p.1411, Eq 2].
  - **Fitted k_Zr = 1.4 and k_Sc = 0.9** for DC-cast 7050 (0.13 Zr; 0, 0.1 or 0.3 Sc), from microprobe [R1 p.1411].
- **Undercooling parameter:** P = mC₀(k−1)/k = ΔT₀ [R9 p.59, Eq 2.7].
- **Growth restriction factor:** Q = mC₀(k−1) = kΔT₀ [R9 p.60, Eq 2.8].
- **Constitutional undercooling:** ΔT_c = ΞQ [Eq 2.9].
- **Tip velocity:** V = D_s ΔT_c²/(QΓ), with Γ = σ_ls/Δs_f [R9 p.60, Eq 2.10].
- Q(Ti) ≈ 35 at 0.15 % Ti; Q(Sc) = 2.5 at 0.6 % Sc; P(Sc) = 5 versus P(Ti) = 4.4 [R9 pp.64–65].
- Commercial Ti additions are only 0.001–0.005 % [R9 p.65].
- Grain refinement in binaries needs primary phase, i.e. >0.15 % Ti or >0.6 % Sc [R9 p.68; R4 p.33].
- **Non-equilibrium solidus examples.**
  - 3003 (1.19Mn/0.55Fe/0.18Si): the as-cast structure is Al₆(FeMn) + Al₁₅(FeMn)₃Si₂. With 0.6 Si and low Fe, free Si appears and the solidus falls to 573 °C [R8 p.37].
  - 1050 (0.37Fe/0.05Si): solidus 642/638/630 °C at 0.4/1.2/18 K s⁻¹ [R8 Table 1.17].
  - 5182: the eutectic liquid persists to 470 °C versus an equilibrium solidus of 576–578 °C [R9, 5182 section].

### 1.6 Design levers

- To keep Mn in solution for later dispersoid precipitation, minimise Fe (it binds Mn in Al₆(FeMn)) and cast fast [R8 p.12].
- To get *less* Mn in solid solution (higher conductivity, softer O-temper), add Si and/or homogenise high so that Mn precipitates and coarsens [R8 Table 1.13] (inference).
- Use k values to predict where dispersoid-free zones will form:
  - Zr (k > 1) is depleted at dendrite edges.
  - Sc (k < 1) is enriched at edges and is complementary to Zr [R1 p.1418].
- **(general knowledge)** Mn has k < 1, so the centres of Mn dendrite cells are lean in Mn.

### 1.7 Pitfalls

- Equilibrium binary solubility overstates usable supersaturation in commercial alloys; ternary fields cut Mn by 5–10× [R8].
- Phase-diagram compilations disagree (Mondolfo vs Drits/Du for Al–Mn–Si; Russian vs non-Russian Sc solvus data) [R8 p.13; R4 p.21].
- 3xxx with Si can partially melt about 60 °C below the binary Al–Mn solidus at 600 °C [R8 p.35].

---

## 2. Transition-metal dispersoids in commercial alloys (Mn, Fe, Cr, Cu–Mn, Zr)

### 2.1 Mechanisms

- **Three particle classes** [R11 pp.78–79]:
  1. Coarse constituents from solidification.
  2. **Dispersoids, 0.05–0.5 µm**, formed during ingot homogenisation by solid-state precipitation of slowly diffusing, modestly soluble transition-metal compounds (Al₂₀Mn₃Cu₂, Al₁₂Mg₂Cr, Al₃Zr). Once formed they resist dissolution and coarsening, and retard recrystallisation and grain growth.
  3. Age-hardening precipitates up to 0.1 µm.
- **Purpose of preheat precipitation is grain control, not hardening.**
  - Preheat precipitates the Mn or Cr phase; this "does not cause appreciable hardening … its purpose is to produce finely divided and dispersed particles that retard or inhibit recrystallization and grain growth".
  - These dispersoids are **incoherent**.
  - **Electrical conductivity measures how complete the precipitation is** [R10 pp.369–370].
- **3xxx phase path** [R10 pp.388–389]:
  - During solidification, Al₆(Mn,Fe) and cubic Al₁₂(Fe,Mn)Si form eutectically.
  - Remaining Mn precipitates during preheat as **Al₁₂(Mn,Fe)Si and Al₆(Mn,Fe) dispersoids**, which "strengthen the material and control recrystallized grain size".
  - In Cu-bearing alloys, **Al₂₀Cu₂Mn₃** forms instead (minor strength effect; grain control after solution treatment).
- **8006-type (Fe ≫ Si):** dispersoids formed by annealing above 300–350 °C are mostly **Al₆Mn**, not Al₆(FeMn), because Fe solubility is negligible. Their amount is set by the non-equilibrium Mn in (Al) [R8 p.31].
- **Cr dispersoids:** Al₁₈Mg₃Cr₂ in 5xxx; closer to Al₁₂Mg₂Cr in 7xxx. They contribute strength in non-heat-treatable (NHT) alloys and control recrystallisation in heat-treatable alloys [R10 p.390].
- **Zr dispersoids:** equilibrium Al₃Zr is tetragonal, but fine **metastable cubic (L1₂) Al₃Zr** forms in preheat; usually <0.15 % Zr [R10 p.390].
  - In Ref. [R1]'s 7050 (0–0.3Sc, ≤0.13Zr), all dispersoids remained L1₂ even after 40 h at 475 °C; no D0₂₃ formed [R1 p.1410].
- **Heterogeneous nucleation on transient precipitates.**
  - Dispersoids nucleate on precipitate particles that form and grow during *slow* heating. The dispersoids survive at the homogenisation temperature; the precursor precipitates redissolve.
  - Example: η-MgZn₂ nucleated Al₆Mn in Al–Zn–Mg–0.3Mn homogenised 500 °C/24 h, heated at 50 vs 500 °C h⁻¹ [R11 pp.105–106, Fig 3.8].
- **Si effect on Mn dispersoids.**
  - With Si, α-Al₁₅(Fe,Mn)₃Si₂ forms in casting **and** in annealing, because Si has relatively high solubility [R8 p.32].
  - In the Si-saturated field, Mn solubility drops to 0.04–0.08 % (400–573 °C) [R8 Table 1.13]. Si therefore raises the driving force for Mn precipitation (inference).
  - Si also converts Al₆(Fe,Mn) constituents to α during homogenisation [R11 p.106].
  - Single-phase 3003 (no excess phases) requires Mn < 1 % and Si < 0.1 %. Then Mn microsegregation can be removed by annealing above 540–550 °C [R8 pp.32–33].

### 2.2 Quantitative data

**Phase data (3xxx/8xxx)** [R8 pp.1–19]:

| Phase | Composition (wt%) | Structure | Lattice (nm) | Other |
|---|---|---|---|---|
| α-Al₁₅Mn₃Si₂ (Al₁₀Mn₃Si, α(MnSi)) | 26.3Mn, 8.9Si; range 25–29Mn, 8–13Si | cubic Pm3, 138 atoms/cell | a = 1.265–1.268 (1.260) | ρ = 3.55 g cm⁻³; HV 8.8 GPa; dissolves 0.7–0.8 Mn |
| α-Al₁₅(FeMn)₃Si₂ | Fe substitutes Mn up to 31Fe–1.5Mn–8Si | cubic | 1.265 (0 % Fe) → 1.25 (31.1 % Fe) | Zakharov reports a quaternary Al₁₆(FeMn)₄Si₃ (a = 1.252); Davignon (550 °C, 12 weeks) supports a single α field |
| Al₆(FeMn) | Al₆Mn dissolves Fe up to ≈Al₁₂FeMn (12.85Fe, 12.64Mn) | orthorhombic | a 0.75518, b 0.64978, c 0.88703 | isomorphous with Al₆Fe and Al₆Mn |
| Al₃Fe | dissolves Mn to Al₃Fe₀.₈₈Mn₀.₁₂ (4–5 Mn) | monoclinic [R10 p.388] | — | needle-like, does not spheroidise [R8 p.23] |
| α-Al₈Fe₂Si | 31.6Fe, 7.8Si | hexagonal | a 1.23–1.24, c 2.62–2.63 | ρ 3.58; spheroidises at 550 °C/10 h [R8 p.23] |
| β-Al₅FeSi | 25.6Fe, 12.8Si | monoclinic | — | HV 5.8 GPa; needles |
| Al₂₀Cu₂Mn₃ | — | — | — | Cu-bearing alloys [R10 pp.369, 389] |
| Al₁₂Mg₂Cr / Al₁₈Mg₃Cr₂ | — | fcc (Al₁₈Mg₃Cr₂) | — | [R10 p.390] |

Davis calls α "cubic αAl₁₂Fe₃Si", β "monoclinic β-Al₉Fe₂Si₂" and the quaternary "Al₁₂(Fe,Mn)₃Si" [R10 pp.369, 388]. The phases are the same; the formula conventions differ.

**Invariant reactions** relevant to 3xxx casting:
- Al–Mn–Si [R8 p.15 Table 1.11]:
  - L + Al₆Mn → (Al) + α-Al₁₅Mn₃Si₂ at **648–649 °C** (liquid 2.5–2.8 Mn, 1.5–1.7 Si).
  - L → (Al) + (Si) + α at 573–574 °C.
- Al–Fe–Mn [R8 p.11]: L → (Al) + Al₃Fe + Al₆(FeMn) at **654 °C**.
- Al–Fe–Mn–Si [R8 Table 1.15]: L + Al₆(FeMn) + Al₃Fe → (Al) + α at 648 °C.
- Non-equilibrium Al₄Mn and Al₁₀Mn₃Si appear above about 2.5 % Mn [R8 p.13].
- **Primary-intermetallic limit:** keep Fe + Mn below about 2.0 % (3003) and 1.7 % (3004) to avoid primary (Fe,Mn)Al₆ [R10 p.383].
- 3xxx is limited to ≤1.25 % Mn (versus 1.82 % binary solubility) because Fe lowers solubility and risks primary Al₆Mn [R11 p.129].

**Homogenisation practice:**
- 450–600 °C for 6–24 h [R11 p.105].
- Slow heating, about 75 °C h⁻¹, "necessary to promote nucleation and growth of a fine and uniform dispersion" [R11 p.105].
- Cooling-rate control and a second isothermal step are sometimes used [R11 p.106].
- R2's Sc–Zr billets: heat 50 °C h⁻¹, cool 350 °C h⁻¹, 400 °C/8 h versus 450 °C/4 h. Both gave negligible differences in extrusion and post-braze properties [R2 pp.18, 38, 43].

**Strength contribution:**
- 8xxx (8006 Al–1.6Fe–0.65Mn, 8011): dispersion hardening is about **30–40 MPa** of proof and tensile strength; solid solution adds 2–10 MPa (proof) and 5–20 MPa (UTS) [R11 p.131].
- Annealed 3003 UTS ≈110 MPa versus 90 MPa for 1100 [R11 p.129].
- 3004 annealed UTS ≈180 MPa [R11 p.130].
- Al–Mg–Mn plate: Mn is about twice as effective as Mg per % (≈35 MPa UTS per 1 % Mg) [R10 p.380].

**Quench sensitivity** (critical range 290–400 °C):
- Al₁₂Mg₂Cr is worst, Al₆Mn intermediate, Al₃Zr least [R11 pp.112–113].
- Mn-bearing particles nucleate coarse Mg₂Si needles [R11 p.113 Fig 3.14].

### 2.3 Dispersoid-free zones (DFZ) from microsegregation

- In Sc-free 7050 (0.13 Zr), a DFZ forms at the **dendrite edges**, where initial Zr is too low for Al₃Zr. These Zr-lean regions recrystallise [R1 pp.1409–1410, 1418].
- Adding 0.1 % Sc fills the edges, because Sc segregates there (k = 0.9), and raises number density everywhere [R1 p.1418].
- **(general knowledge)** In 3xxx the analogue is Mn-lean dendrite centres (k_Mn < 1) and Mn-depleted zones around constituent particles. This needs a 3xxx-specific source.

### 2.4 Design levers

- Fe + Mn total sets the constituent fraction and the primary-phase risk (≤1.7–2.0 %) [R10 p.383]. Fe also controls how much Mn goes into constituent versus solid solution [R8 p.12].
- Si/Mn ratio decides Al₆(Mn,Fe) versus α. More Si gives more, finer α dispersoids and lower Mn in solid solution [R8 pp.32, 37; R10 p.389] (inference on "finer").
- Heating rate of 50–75 °C h⁻¹ through the nucleation window, an optional isothermal hold, then soak at 450–600 °C [R11 pp.105–106].
- Use electrical conductivity as an in-line metric of Mn precipitation [R10 p.370].

### 2.5 Pitfalls

- Coarse dispersoids or constituents above about 1 µm act as particle-stimulated nucleation (PSN) sites, which promotes recrystallisation [R11 p.42].
- Dispersoids also nucleate microvoids [R11 p.82].
- Dispersoids raise quench sensitivity in heat-treatable alloys (Cr > Mn > Zr) [R11 p.112].
- **Conflict:** Davis states Mn "decreases resistivity" [R10 p.382]. This contradicts the general understanding that Mn in solid solution raises resistivity strongly (general knowledge). Treat that sentence as an error.

---

## 3. L1₂ Al₃Sc, Al₃Zr and core–shell Al₃(Sc,Zr)

### 3.1 Phase data, crystallography and misfit

| Item | Value | Source |
|---|---|---|
| Al lattice parameter | a = 4.0496 Å, ρ = 2.699 g cm⁻³ | [R4 p.20 Table 1] |
| Al₃Sc | L1₂ (cP4, Pm3̄m, AuCu₃), a = 4.103 Å (0.4104 nm), ρ = 3.026–3.03 g cm⁻³, forms peritectically at about 1320 °C | [R4 pp.20, 25; R9 p.68] |
| Burgers vector b (Al) | a/√2 = 0.2863 nm | (derived from R4 Table 1) |
| Misfit δ at room temperature | ≈1.3 % | (derived); consistent with d_crit = b/δ ≈ 21.5 nm [R4 p.29] |
| Misfit at eutectic temperature (~660 °C) | ≈0.47–0.5 % (a: Al₃Sc 0.414 nm vs Al 0.412 nm) | [R4 p.34; R3 p.13] |
| Al₃Zr (equilibrium) | D0₂₃ tetragonal, a = 0.4006–0.4014, c = 1.727–1.732 nm; congruent melting 1577 °C | [R9 p.68] |
| Al₃Zr (metastable) | cubic L1₂, isomorphous with Al₃Sc | [R10 p.390; R11 p.52] |
| Zr in Al₃Sc | up to ~35 wt% (Al₃Sc₀.₆Zr₀.₄) at 600 °C; 6 at% (~16 wt%) at 500 °C; 12.2 at% (~50 % of Sc sites) at 430 °C in Al–Mg–Sc–Zr and at 1200 °C | [R4 pp.23–24; R9 p.68] |
| Sc in Al₃Zr | ~5 wt% (Al₃Zr₀.₈Sc₀.₂); 6.5 at% at 500 °C; 3–5 at% at 1200 °C | [R4 p.23; R9 p.68] |
| Zr/Sc partition into Al₃Sc | (Zr/Sc in particle) ≈ 2.2 × (Zr/Sc in alloy), 600 °C | [R4 p.23] |
| Other X in Al₃Sc | Ti ≈12.5 at% (≈half the Sc), sharp lattice-parameter decrease; Cr ≈11 at%; V 1.4–2.7 at%; Co 1.2 at%; Mn slight; Mg a few % | [R4 pp.23–24] |
| Al₃Sc properties ⚠ (table partly garbled) | E ≈ 163–166 GPa (calc./exp.), ν ≈ 0.20–0.22, CTE ≈ 16×10⁻⁶ K⁻¹, calculated APB energy up to ~670 mJ m⁻² (111) / 450 (100); one dataset gives E ≈ 111 GPa falling to ~97 GPa at 550 °C | [R4 p.25 Table 3] |
| Equilibrium shape | great rhombicuboctahedron (multifaceted; looks spherical in TEM) | [R4 p.28] |

**Ternary phases that consume Sc** [R4 pp.21–25]:
- Si → V-phase **AlSc₂Si₂**. Invariants: L + Al₃Sc → (Al) + V at 617 °C; L → (Al) + Si + V at 574 °C.
- Cu → W-phase Al₅.₄₋₈Cu₆.₆₋₄Sc. Invariants: L + Al₃Sc → (Al) + W at 572 °C; L → (Al) + Al₂Cu + W at 546 °C. W was not observed in practical Al–2.5Cu–0.23Sc or Al–4.4Cu–0.48Sc heat treatments.
- No ternary phases with Mg, Zn, Li, Mn, Fe, Cr, Mo, Zr. In Al–Mo–Sc at 550 °C, Al₃Sc and **Al₁₂Mo** are in equilibrium with Al.

### 3.2 Formation modes and temperature windows

1. **Primary Al₃Sc** (hypereutectic, >0.6 % Sc) acts as a grain refiner.
   - Faceted cubic or dendritic ⟨110⟩, nucleated on oxides [R4 p.26].
   - Al₃(Sc,Ti) nuclei are far more potent: at 100 K s⁻¹, about 100 % of Al₃(Sc,Ti) particles nucleated grains versus about 2 % of Al₃Sc [R4 p.34].
   - 25 % Ti on the Sc sites gives zero mismatch at about 550 °C [R4 p.34].
   - Zr:Sc < 1 gives primary Al₃Sc; Zr:Sc > 1 gives primary Al₃Zr. Al₃Sc rims "activate" Al₃Zr, so 0.15Sc + 0.15Zr refines well [R9 pp.68–69].
2. **Eutectic Al₃Sc**: about 0.63 vol% at equilibrium [R4 p.26].
3. **Discontinuous (cellular) precipitation (DP)** [R4 p.27]. This mode is *undesired*: coarse, little strength, and it wastes Sc.
   - Mostly seen at ≥0.4 % Sc, but also seen at 0.27 % and at 0.2 % Sc (quenched from 600 °C to 370–490 °C).
   - The DP nose is at a higher temperature than the continuous-precipitation nose.
   - Cold work before ageing suppresses DP.
   - Mg, Cu, Cr and Ti suppress DP; Si, Zn and Mn promote it [R4 pp.30–33].
4. **Continuous precipitation**: homogeneous nucleation and diffusion-controlled growth, with **no metastable precursor** [R4 p.27].
   - Heterogeneous nucleation on dislocations and grain boundaries dominates at low Sc and high temperature; homogeneous dominates at high Sc and low temperature (nucleation map) [R4 p.27].

**Temperature windows** [R4 p.33; R3 pp.13–14]:
- **250–350 °C → hardening precipitates 2–6 nm**. Al₃Sc hardening is "typically in the order of 100 MPa" [R3 p.13].
- **400–600 °C (homogenisation, hot rolling, extrusion) → dispersoids 20–100 nm**. Number density is usually too low for strength, but they are very effective against recrystallisation [R3 p.14].
- Polmear: Al₃Sc precipitates at relatively high temperature (~350 °C), resists coarsening, and inhibits recrystallisation up to about 600 °C [R11 p.52].

### 3.3 Precipitation kinetics (binary and ternary)

- **Hyland, Al–0.18Sc, quenched from 650 °C, constant nucleation rate** [R4 p.28]:
  - 288 °C: incubation about 24.5 min; diffusion fields overlap at about 150 min.
  - 343 °C: 7 min and 20 min.
- **JMAK:** X(t) = 1 − exp[−k(Dt)ⁿ]. Theory gives n = 5/2 for constant nucleation and 3/2 for site saturation [R4 p.28, Eq 1]. Measured n [R4 p.28 Table 4]:

| C₀ (wt% Sc) | T (°C) | n | Note |
|---|---|---|---|
| 0.30 | 300 | 1.3 / 1.6 / 2.0 | solution treated 500 / 600 / 640 °C; n falls to 0.26 at late stage |
| 0.15 | 260–370 | 1.30–1.49 | — |
| 0.25 | 260–370 | 1.45–1.96 | — |
| 0.20 | 240–350 | 1.88–2.16 | — |
| 0.23 | 270–350 | 1.65–1.85 | solution treated 600 °C, direct quench |

- **Quench path matters:** a water quench (excess vacancies) dramatically shortens incubation [R4 p.29].
- **Ternary effects on Al₃Sc kinetics** (Al–0.4Sc base, 300–500 °C C-curves) [R4 pp.30–33]:

| Addition | Effect on Al₃Sc precipitation |
|---|---|
| Mg ≤5 % | minor (slightly faster); hardness increment reduced (some Sc goes into Al₃Mg₂); about 3× Mg enrichment at the interface; d_crit rises to 80 nm (Al–3Mg–0.2Sc) and >116 nm (Al–6.3Mg–0.2Sc) |
| Cu ≤1.4 % | minor; late stage slowed above 400 °C at high Cu; θ′ can nucleate on Al₃Sc |
| Si ≤0.4 % | onset barely changed; **late stage considerably delayed**; V-phase risk |
| Fe ≤0.7 % | late stage significantly slowed |
| Zn ≤5 % | minor |
| Mn, Cr <0.3 % | minor |
| Li | onset unchanged |
| Zr 0.15 % | initial stage marginal; **late stage much slower; coarsening much slower** |
| Y, Gd, Ho, Er (0.3 at%) | form L1₂ Al₃(Sc₁₋ₓXₓ); peak about 10 h at 285 °C, unchanged |

### 3.4 Core–shell structure, coarsening and coherency loss

- **Core–shell.** Nucleation and early growth produce nearly pure Al₃Sc (controlled by Sc diffusion). Zr enters later, forming a Zr-rich shell. Late growth and coarsening are therefore controlled by the slow Zr diffusion [R3 p.14; R4 p.32].
  - 3D atom probe at 475 °C: core ≈ Al₃Sc, shell ≈ equal Sc and Zr [R4 p.32].
  - At 300 °C the Zr content stays low even after long times [R4 p.33].
  - KWN (7050, 480 °C): Zr depletion accelerates only after about half the Sc has precipitated. Early interfaces are Sc-enriched relative to the equilibrium tie-line, because D_Sc ≈ 4 D_Zr [R1 p.1414].
- **LSW coarsening:** r̄³ − r̄₀³ = a_LSW(t − t₀) [R1 p.1416, Eq 5].
  - The model predicts t^1/3 kinetics only after about 500 h, i.e. >100× the time when coarsening begins.
  - The steady-state size distribution is broader than LSW [R1 pp.1416–1417].
- **Kuehmann–Voorhees ternary rate constant** [R1 p.1417, Eq 6]:

  a_KV = 8σV_m / { 9R_gT [ c^α_Sc(1 − k_Sc)²/D_Sc + c^α_Zr(1 − k_Zr)²/D_Zr ] }

  Here k_i = c^β_i/c^α_i is the particle/matrix distribution coefficient and c^α_i the matrix interface concentration.

- **Coarsening constants for 7050 variants, model at 480 °C** [R1 p.1417 Table 2], in 10⁻³⁰ m³ s⁻¹:

| Alloy (wt%) | KWN model | KV theory | Measured |
|---|---|---|---|
| 0.13Zr–0Sc | 1.69 | 7.02 | — |
| 0.13Zr–0.10Sc | 1.88 | 7.98 | — |
| 0.13Zr–0.18Sc | 2.34 | 8.27 | — |
| 0.07Zr–0.10Sc | 2.43 | 11.38 | 6.9 |

  - Coarsening rises with the Sc:Zr ratio and is insensitive to volume fraction [R1 p.1418].
  - Al₃(Sc,Zr) coarsens "much slower" than Al₃Sc [R4 p.32].
- **Coherency loss:** d_crit ≈ b/δ, about 21.5 nm at room temperature [R4 p.29, Eq 2].
  - Vacancy and Sc-in-solution corrections cancel [R4 p.30].
  - Refined analysis gives 24.6 nm [R4 p.30].
  - Predicted d_crit: 30.8 nm at 400 °C, 33.5 nm at 450 °C, 36.2 nm at 490 °C.
  - Measured d_crit: 28–50 nm for 0.12–0.5 Sc at 400–500 °C, and 30–80 nm in one dataset [R4 p.30 Table 5].
  - Loss of coherency is sometimes, not always, followed by faster coarsening [R4 p.30].
- **Al/Al₃Sc interfacial energy γ (mJ m⁻²)** [R4 p.31 Table 6]:

| Value | Method |
|---|---|
| 10 | fit of coarsening data (Lifshitz–Slyozov) |
| 78 ± 20 (288 °C), 93 ± 20 (343 °C) | back-calculated from incubation time |
| 123 ± 41 (288 °C), 125 ± 35 (343 °C) | back-calculated from nucleation rate |
| 54.2 (400 °C), 63.2 (430 °C), 41.3 (460 °C) | Ostwald-ripening fit |
| (100) 192, (111) 226 (0 K) | pseudopotential calculation |
| (100) 32.5, (110) 51.3, (111) 78.2 (0 K); (100) 31.5 (288 °C) | atomistic simulation |
| 105 | LSW fit |
| 20–300 | Ostwald fit at 16 temperatures |
| 57 | precipitation-model fit (may be lower in the nucleation stage) |
| 120 coherent / 170 semicoherent | coarsening fit |

  - Robson used **σ = 0.1 J m⁻²** (tuned), inside the 0.06–0.18 J m⁻² experimental range for Al₃Sc, Al₃Zr and Al₃(Sc,Zr) [R1 p.1411].

### 3.5 KWN predictions for Sc + Zr in 7050 (2.2Cu–2.1Mg–6.1Zn) [R1]

- 0.1Sc–0.13Zr at 480 °C reaches the near-equilibrium volume fraction in about 1 h [R1 p.1413].
- ≥0.1 % Sc cuts the time to a given volume fraction by more than an order of magnitude [R1 p.1420].
- Mean radius is about 10 nm at the plateau for all 0.13 Zr variants; about 12 nm for 0.07Zr–0.1Sc. Sc mainly increases **number density** [R1 p.1415].
- Nucleation and coarsening do not overlap; there is a plateau in number density [R1 p.1415].
- **Critical radius at the start:** 1.0 nm (Sc-free) versus 0.15 nm (0.07Zr–0.18Sc). Sc-free precipitation is mostly heterogeneous on dislocations, so the model under-predicts size there [R1 p.1416].
- **Measured versus predicted mean radius at 475 °C** [R1 p.1416 Table 1]:

| Alloy | 10 h meas. | 10 h pred. | 40 h meas. | 40 h pred. |
|---|---|---|---|---|
| 0.07Zr–0Sc | 11 nm | 9.2 | 28 | 19.8 |
| 0.07Zr–0.1Sc | 8 | 12.2 | 11 | 12.9 |
| 0.07Zr–0.18Sc | 12 | 12.0 | 14 | 13.1 |

- At 0.3 % Sc, almost half the Sc formed primary Al₃(Sc,Zr), leaving 0.18 % in solution [R1 p.1411].
- **RX prediction:** recrystallisation occurs where V_f/r < a critical value. With homogenisation at 480 °C/24 h, Sc boosts V_f/r especially at the dendrite edges. The recrystallised fraction falls linearly with Sc; **0.02 % Sc** almost eliminates it (from 30 % in the Sc-free alloy), assuming constant driving force. This is probably an underestimate [R1 pp.1419–1420].

### 3.6 Property data for Sc-containing NHT alloys

**1xxx (binary Al–Sc)** [R4 p.37 Table 7; R3 p.16]. YS/UTS in MPa:

| Sc | Cast, aged 288 °C/8 h | Cold rolled 89 %, aged 288 °C/8 h | Cold rolled, quenched 649 °C, aged 288 °C/8 h |
|---|---|---|---|
| 0 | 15/48 | 14/49 | 8/34 |
| 0.23 | 159/185 | 198/208 | 147/157 |
| 0.38 | 199/220 | 240/264 | 193/199 |

Other 1xxx rows:
- 0.5Sc: hot rolled 288 °C + cold rolled 69–81 %, aged 288 °C/4 h → 298/319.
- 0.1Sc: quenched 630 °C, aged 320 °C/13.3 h → 132/166.

**3xxx** [R3 p.16 Table 1 (as-extruded flat bar); R4 p.37 Table 7]:
- Al–0.5Mn–0.2Mg–0.15Zr: 87/140 MPa.
  - +0.11Sc → 119/173.
  - +0.21Sc → 152/198.
  - +0.26Sc → 168/207.
  - **(derived)** That is about 300 MPa YS per wt% Sc in this range.
- Al–1Mn + 0.15Sc (cold rolled 89 %, aged 288 °C/8 h) → 216/221; Al–1Mn + 0.5Sc → 309/323.
- Al–0.5Mn–0.2Mg–0.26Sc–0.15Zr, extruded, solution treated 600 °C, aged 250 °C → 162/201.
- R3 notes that no commercial 3xxx specification with Sc exists [R3 p.16].

**5xxx** [R3 p.16; R4 p.37]:
- Al–5.3Mg 147/259 versus +0.3Sc 368/401 (cold rolled 50 % with intermediate anneals at 343 °C; aged 288 °C/8 h).
- Russian 1515/1523/1535/1545/1570 (Sc 0.15–0.50, Zr 0.05–0.20) give +80 to +140 MPa YS over the Mn-bearing equivalents.

**Brazed tube (R2), 1xxx + 0.192Sc + 0.049Zr versus AA3102 (0.07Si–0.41Fe–0.24Mn):**
- Extrusion pressure +44 % (650–653 versus 445–460 MPa specific pressure) [R2 p.38].
- As extruded at 500 °C, the Sc–Zr tube was largely unrecrystallised (fine recrystallised edges); 3102 was fully recrystallised [R2 p.39].
- Recrystallisation and coarse grains formed between 575 and 600 °C (2 min hold) [R2 pp.41, 52].
- 0–10 % cold roll-sizing had a negligible effect on Sc–Zr post-braze properties [R2 p.45].
  - For 3102, 3–7 % sizing is typical, and about 3 % sizing gives about 22 % lower failure pressure after brazing (coarse grains) [R2 p.13].
- Post-braze YS/UTS of Sc–Zr was within 8 % of 3102 [R2 p.52].
- Braze (600 °C) **then** 288 °C/8 h: YS 154 MPa; burst pressure ≥69 MPa (≥10,000 psi, no failure) versus 42 (Sc–Zr brazed) and 39 MPa (3102 brazed) [R2 pp.48, 50].
- Ageing **before** braze had no benefit (41 MPa), because the dispersoids dissolve at 600 °C [R2 p.50].

**Corrosion:**
- Sc makes Al slightly more noble (much more so when hypereutectic). Self-corrosion generally improves.
- Hypereutectic primary Al₃Sc can cause micro-galvanic attack.
- Al–Mg–Sc annealed at 350 °C is immune to intergranular corrosion; after sensitisation it is less susceptible than Sc-free alloys [R4 pp.38–39].

### 3.7 Design levers (Sc/Zr)

- **Sc:Zr ratio.** Higher Sc speeds nucleation and raises number density, but also raises the coarsening rate (Table 2 above). Zr slows coarsening and adds shell stability. Use Sc + Zr together; they are "complementary … most potent when used in combination" [R1 p.1419; R4 p.34].
- **Precipitation route** [R4 p.35]:
  - Best: dispersoids formed **before deformation at T_disp < T_anneal**, or during an intermediate anneal of solution-treated and deformed material.
  - Worst: Sc in solid solution with a fast up-quench to the annealing temperature, or T_disp ≥ T_anneal.
  - Reason: Zener drag usually decays (coarsening) more slowly than the recrystallisation driving force (recovery), which favours many small dispersoids formed at T_disp ≪ T_anneal.
  - **(inference)** A two-step homogenisation (a nucleation hold in the 250–350 °C precipitation window [R4 p.33], then a 400–480 °C soak to grow the Zr shell [R4 p.32; R1]) should maximise Al₃(Sc,Zr) number density. This is a hypothesis to test, not a sourced schedule.
- **Braze survivability (3xxx tube/fin).** 0.19 % Sc dissolves at about 595 °C [R2 p.41].
  - **(inference)** Raise Zr (shell, lower solubility) and/or Sc up to the extent the cost model allows, and test a 600–610 °C braze.
  - Alternatively, exploit post-braze age hardening at about 288 °C [R2 p.48].
- **Si and Fe control** for Sc alloys: Si → V-phase and DP; Fe slows the late stage [R4 pp.32–33]. Mn does not reduce Sc solubility but Sc reduces Mn solubility [R4 p.23]. Expect fewer Mn dispersoids in Sc-bearing 3xxx (inference).
- **Supersaturation helpers:** in concentrated alloys Cu, Mg and Zn lower the Sc needed for a given volume fraction [R1 p.1410].

### 3.8 Pitfalls

- Primary Al₃Sc above about 0.6 % (lower with Mg or Zr) wastes Sc [R4 p.33; R1 p.1411].
- Al₃Sc hardening (250–350 °C) falls between the solution-treatment and ageing windows of 2xxx, 6xxx and 7xxx, so it cannot be combined with full T6 hardening [R3 p.14; R4 p.36].
- High-temperature homogenisation (≥450–500 °C) of binary Al–Sc coarsens dispersoids. Al–Mg–Sc stays unrecrystallised only to about 400–450 °C [R4 p.34].
- **Conflicting claims:** Polmear says recrystallisation is inhibited "as high as 600 °C" [R11 p.52]; R2 measured recrystallisation at 575–600 °C for 0.19Sc–0.05Zr.

---

## 4. Classical nucleation, growth and coarsening (KWN) — model-ready equations

**Framework (Kampmann–Wagner numerical)** [R1 pp.1411–1413]:
- Discrete time steps, with adaptive Runge–Kutta and error control.
- Size distribution discretised into many classes.
- Nucleation from classical theory.
- Diffusion-controlled spherical growth with Gibbs–Thomson interfacial compositions.
- Mean-field matrix mass balance.
- New nuclei are placed **10 % above r\*** so they can grow.
- Segregation is handled by running about **50 parallel slices** from dendrite centre to edge, initialised with the Scheil profile (§1.5), with inter-slice diffusion allowed.

| # | Equation | Variables / units | Source |
|---|---|---|---|
| E1 | c^α_r = c^α_∞ exp[2σV_m/(R_g T r)] (Gibbs–Thomson) | c: matrix concentration at the interface for radius r; σ (J m⁻²); V_m (m³ mol⁻¹) of the precipitate; R_g = 8.314 J mol⁻¹ K⁻¹ | [R1 p.1411 Eq 1] |
| E2 | I = N_v (kT/h) exp[−(4πσr\*² + Q\*)/(3kT)] ⚠ | I: nucleation rate (m⁻³ s⁻¹); N_v: site density; h: Planck; k: Boltzmann; Q\* ≈ 2.07 eV atom⁻¹; r\*: critical radius. ⚠ as extracted — check grouping of the 1/3 factor against the original | [R1 p.1412 Eq 3] |
| E3 | r\* = radius at which the capillarity-shifted solvus passes through the current mean matrix composition (consistent for nucleation and growth) | — | [R1 p.1412] |
| E4 | dr/dt = (D_Sc/r)(c̄_Sc − c^α_Sc(r))/(c^β_Sc − c^α_Sc(r)) = (D_Zr/r)(c̄_Zr − c^α_Zr(r))/(c^β_Zr − c^α_Zr(r)) | ternary flux-balance tie-line, solved by Newton–Raphson for each size class; negative values give dissolution | [R1 p.1412 Eq 4] |
| E5 | c = k c̄ (1 − f_s)^(k−1) | initial segregation profile; k_Zr = 1.4, k_Sc = 0.9 | [R1 p.1411 Eq 2] |
| E6 | r̄³ − r̄₀³ = a(t − t₀) | LSW coarsening | [R1 p.1416 Eq 5] |
| E7 | a_KV (see §3.4) | ternary coarsening constant | [R1 p.1417 Eq 6] |
| E8 | X = 1 − exp[−k(Dt)ⁿ] | JMAK; n = 3/2 (site saturation) to 5/2 (constant nucleation) | [R4 p.28 Eq 1] |
| E9 | d_crit = b/δ | coherency-loss diameter | [R4 p.29 Eq 2] |
| E10 | x = √(Dt) | diffusion distance | [R11 p.105] |

**Key parameter values used by Robson [R1]:**
- σ = 0.1 J m⁻² (fit).
- Q\* = 2.07 eV atom⁻¹.
- D_Sc/D_Zr ≈ 4.
- k_Zr = 1.4, k_Sc = 0.9.
- Thermodynamics from the Alcoa database, with ideal Sc–Zr mixing on the ordered sublattice. Ideal mixing is supported by Zr fraction in particles scaling with alloy Zr [R1 p.1410].
- **D₀ and Q values are not listed in R1.**

**Interpretation rules** [R1 p.1416]:
- Lower supersaturation gives a larger r\*, and nucleation falls much faster than growth. The result is fewer, larger particles and incomplete precipitation even after 40 h (0.07Zr–0Sc).
- Low-driving-force systems precipitate heterogeneously on dislocations. A homogeneous-only KWN model under-predicts size; add a dislocation nucleation channel [R1 p.1416; R4 p.27].

---

## 5. Zener pinning and recrystallisation resistance

- **Single-particle force:**
  - Incoherent sphere: F = 2πrγ cosθ sinθ, with maximum F_S = πrγ [R12 p.109, Eqs 4.11–4.12].
  - **Coherent sphere: F_C = 2πrγ, i.e. 2× incoherent** [R12 p.112, Eq 4.19].
  - Particle shape matters only for plates face-on or needles edge-on [R12 p.110].
- **Random distribution:** N_V = 3F_V/(4πr³); N_S = 3F_V/(2πr²) [R12 p.113].
- **Zener pinning pressure:** **P_Z = 3F_Vγ/(2r)** [R12 p.114, Eq 4.24]. Røyset's generic form is p_Z = k f/r [R4 p.34, Eq 3].
  - Pinning rises when the grain size D is close to the particle spacing D_C = (4πr³/3F_V)^(1/3): P′_Z = 3DF_Vγ/(4r²), with maximum ≈ 1.2F_V^(2/3)γ/r [R12 pp.115–116, Eqs 4.27–4.29] (γ restored ⚠).
- **Interaction with coherent L1₂ particles:**
  - A passing boundary makes the particle lose coherency (100–150 nm Al₃Sc, Al–4Mg–0.2Sc, 575 °C).
  - Rotation by cutting: 30→48 nm, Al–0.25Sc. R12 also notes cutting of semi-coherent Al₃Sc [R12 p.112].
  - Dissolution and re-precipitation (50 % cold-rolled Al–0.2Sc) [R4 p.35].
- **V_f/r criterion:** the recrystallised fraction is estimated from where V_f/r falls below a critical value [R1 p.1419].
- **Quantitative recrystallisation-temperature data:**
  - The 0.3 % Sc patent raised the onset of recrystallisation by about **220 °C** in pure Al, less in alloys [R4 p.34].
  - Al–Mg–Sc stays unrecrystallised up to about 400–450 °C [R4 p.34].
  - 0.25Sc + 0.08Zr cold worked: no recrystallisation after 8 h at 520 °C; recrystallises at about 600 °C [R2 p.16].
  - 0.19Sc–0.05Zr extrusions: recrystallise at 575–600 °C [R2 p.41].
  - Hard-rolled pure Al: recrystallisation takes hours at 280 °C, minutes at 380 °C, seconds at 500 °C. Commercial anneals are 300–420 °C [R11 p.42].
- **Other elements:**
  - Mn raises the recrystallisation temperature, gives fibrous hot-worked structures and slows recovery [R10 p.382].
  - Cr prevents recrystallisation in Al–Mg–Si and Al–Zn alloys [R10 p.373].
  - Zr at 0.1–0.3 % inhibits recovery and recrystallisation [R10 p.386].
  - V raises the recrystallisation temperature [R10 p.385].
  - 0.2 % Ca alters recrystallisation in 3003 [R10 p.372].
  - Yb + Cr + Zr strongly raise recrystallisation resistance in Al–Zn–Mg–Cu [R7 p.6].
- **Lever:** maximise F_V/r, i.e. many fine particles, homogeneously distributed. Avoid >1 µm particles, which act as PSN sites [R11 p.42].

---

## 6. Clusters, natural ageing and precipitation sequences

### 6.1 Sequences

| System | Sequence | Source |
|---|---|---|
| Al–Cu | SSSS → GP (single Cu layers on {100}) → θ″ (GP2) → θ′ (Al₂Cu, tetragonal a 0.404 / c 0.580 nm, semi-coherent, on dislocations) → θ (bct a 0.607 / c 0.487 nm) | [R5 p.11; R11 p.57 Table 2.3; R4 p.37] |
| Al–Cu–Mg | SSSS → Cu–Mg co-clusters → GPB (rods ⟨100⟩) → S′ → S (Al₂CuMg; S′ a 0.404, b 0.925, c 0.718 nm) | [R11 p.58; R3 p.16; R5 p.12] |
| Al–Mg–Si | SSSS → Mg and Si clusters → Mg–Si co-clusters → GP → β″ (monoclinic a 1.534, b 0.405, c 0.683 nm, β 106°, ~MgSi) → β′ (hex, ~Mg₁.₇Si) / B′ (high Si:Mg) → β (Mg₂Si fcc a 0.639 nm) | [R11 pp.58–59, 63–66; R3 p.17] |
| Al–Mg–Si–Cu | SSSS → GP → Q′ → Q (Al₅Cu₂Mg₈Si₆) | [R3 p.17; R11 p.141] |
| Al–Zn–Mg(–Cu) | SSSS → GP(I) spherical 1–1.5 nm / GP(II) Zn {111} discs → η′ (Mg:Zn ≈ 1:1–1:1.15) → η (MgZn₂); or T′ → T (Mg₃₂(Al,Zn)₄₉) at high Mg:Zn | [R11 pp.59, 66; R3 p.18] |
| Al–Li | SSSS → δ′ (Al₃Li, L1₂) → δ (AlLi); T₁ (Al₂CuLi) on {111} in Al–Cu–Li | [R11 p.59; R4 p.38] |
| Al–Mg | GP solvus below room temperature for <5 % Mg → no hardening; β′ → β (Mg₅Al₈ / Al₃Mg₂) | [R11 pp.46, 57; R10 p.389] |
| Al–Sc | SSSS → Al₃Sc (L1₂) directly, no precursor | [R4 p.27] |

### 6.2 Clusters

- **Definition.** "Solute clusters are chemical fluctuations of a non-random solid solution". They are coherent, with diffuse interfaces [R5 p.4].
  - Atom-probe field-ion microscopy finds 20–50-atom disordered clusters before GP zones [R11 p.44].
  - GP-zone densities reach 10¹⁷–10¹⁸ cm⁻³ [R11 p.45].
- **Al–Cu–Mg cluster hardening.**
  - Two-stage hardening at about 100–240 °C. The first stage gives **60–70 % of total hardening within 60 s**, followed by a plateau of up to about 100 h.
  - It is attributed to about 10¹⁹ cm⁻³ Cu–Mg clusters [R11 p.64].
  - Strengthening scales with the number density of Cu–Mg co-clusters. Cu–Cu and Mg–Mg clusters do not correlate with hardness. Vacancy–Mg–Cu complexes are proposed [R5 p.12].
- **Natural-ageing data** (Al–1.1Cu–1.7Mg; Al–1.5Cu–3.5Li ± 0.44Mg at.%; solution treated 500–505 °C 30 min, water quenched) [R5 pp.29–31, 71–73]:
  - Most change happens in the first 24 h; hardening saturates after about 10 h; 72 h is stable up to 6 months.
  - HV goes from 74 → 117 (Al–Cu–Mg, +55 %), 64 → 77 (Al–Cu–Li, +20 %) and 64 → 115 (Al–Cu–Li–Mg, +82 %).
  - **0.4 at% Mg turns on Cu clustering.**
  - Cluster Mg/Cu: 0.70 → 1.82 (Al–Cu–Mg, as-quenched → naturally aged); 0.13 → 0.42 (Al–Cu–Li–Mg).
  - Correlations vanish beyond about 2 nm (atom probe). Li stays random.
  - Small-angle scattering correlation length ξ ≈ 2–5 Å; inter-cluster periodicity λ ≈ 36–72 Å (Table 6).
  - DSC at 10 °C min⁻¹: cluster formation exotherm 50–125 °C; dissolution endotherm 150–260 °C (double minimum). The exotherm area halves within 1 h of natural ageing.
  - Reversion: Cu-rich clusters dissolve at lower temperature than Cu–Mg clusters. Reverting Cu–Mg clusters at 250 °C recreates a supersaturated solid solution that decomposes like one quenched from 500 °C. Mg is linked to the retained excess vacancies [R5 pp.5–6, summary of the missing chapters].
- **Al–Mg–Si negative natural-ageing effect (quantified).**
  - A 24 h room-temperature delay before ageing at about 170 °C reduces tensile properties by **up to 10 %** in alloys with >1 % Mg₂Si.
  - The same delay **improves** properties in alloys with <0.9 % Mg₂Si.
  - Mechanism: clusters and vacancies, and a GP solvus above 170 °C in the richer alloys, give coarser β″.
  - 0.25 % Cu lessens the effect [R11 pp.141–142].
  - Si-rich room-temperature clusters lock up solute. Industrial pre-ageing makes Mg–Si clusters dominant. Sn traps vacancies and retards Si clustering by orders of magnitude [R5 pp.9, 15, 45].
- **Microalloying mechanisms** [R11 p.49]:
  1. Vacancy trapping (Cd, In, Sn retard natural ageing and enhance artificial ageing in Al–Cu).
  2. Raising the GP solvus (Ag in Al–Zn–Mg).
  3. Lowering the interfacial energy.
  4. A new precipitate (Ag → Ω in Al–Cu–Mg).
  5. Heterogeneous sites (Sn particles about 5 nm nucleate θ′).
  6. Increased supersaturation.
  - Sn example: the θ′ heat stays at about 17 J g⁻¹, but the DSC peak moves to 200 °C versus 285 °C at 2 °C min⁻¹ [R11 pp.50–51].
- **Precipitate-free zones at grain boundaries.**
  - About 50 nm is solute-depleted; the remainder is vacancy-depleted.
  - They are narrower with higher solution-treatment temperature, faster quench and lower ageing temperature [R11 pp.48–49].
  - In Cu-rich 6xxx, Cu/Si-depleted PFZs are anodic and drive intergranular corrosion; a T78 overage is the cure [R11 p.141].
- **Secondary precipitation and interrupted ageing.**
  - Retained mobile vacancies allow further low-temperature ageing.
  - 7075 underaged 0.5 h at 130 °C, then held at 65 °C, reaches 225 DPN after 10⁴ h, versus 195 for T6.
  - T6I6 for Al–4Cu: 3 h at 150 °C → quench → 500 h at 65 °C → 50 h at 150 °C [R11 pp.67–69].
- **Cold work before ageing** adds heterogeneous nucleation sites (T8; T₁ in Al–Cu–Li) [R11 p.46; R5 p.9].
- **Activation energies** for cluster formation or dissolution are **not given** in the sources read (see §12). Sc raises the apparent activation energy of δ′ precipitation (DSC; no value given) [R4 p.38].

### 6.3 Interactions with Sc

Sc has little or no effect on the kinetics of θ′, β″ or η′. θ′ nucleates on Al₃Sc [R4 p.37]. δ′ becomes finer and forms shells on Al₃Sc [R4 p.38]. In 6060 + Zr, adding Sc raises T1 YS from 81 to 182 MPa (dispersoid and grain effect) [R3 p.16].

---

## 7. Strengthening contributions

### 7.1 Solid solution

- **Requirements** [R11 p.29]: the solute must be soluble at the annealing temperature, retained on slow cooling, and not tied up in insoluble phases.
- **Baseline:** high-purity Al annealed YS is 7–11 MPa [R11 p.29]; ≈10 MPa [R10 p.367].
- **Unit strengthening in annealed super-purity binaries** [R10 p.368 Table 8] (MPa per 1 % addition; listed by increasing atomic-radius misfit):

| Element | (r_x − r_Al)/r_Al | ΔYS /at% | ΔYS /wt% | ΔUTS /at% | ΔUTS /wt% |
|---|---|---|---|---|---|
| Si | −3.8 % | 9.3 | 9.2 | 40.0 | 39.6 |
| Zn | −6.0 % | 6.6 | 2.9 | 20.7 | 15.2 |
| Cu | −10.7 % | 16.2 | 13.8 | 88.3 | 43.1 |
| Mn | −11.3 % | — (1 at% insoluble) | 30.3 | — | 53.8 |
| Mg | +11.8 % | 17.2 | 18.6 | 51.0 | 50.3 |

- **Behaviour** [R10 pp.367–368]:
  - The relationship is non-linear: small additions have larger unit effects.
  - Strengthening rises with radius misfit, plus an electronic factor.
  - Multiple solutes are slightly less than additive.
  - Mn in solid solution is very effective, but in commercial alloys Mn is mostly precipitated.
- **Model form:** σ_ss = Σ k_i c_i^n.
  - Sources give only linear unit slopes (n = 1 fit) with a non-linearity caveat.
  - **(general knowledge)** n ≈ 2/3–1 is commonly used.
  - Fit k_i and n to the user's own 3xxx data.
- **Other solid-solution statements** [R11 pp.30, 34]:
  - On an atomic basis, Mn and Cu are the most effective at ≤0.5 %.
  - Only 0.2–0.3 % Mn stays in solution after preheat.
  - Cu is ≤0.3 % in NHT alloys.
  - Up to 6 % Mg gives annealed YS up to 175 MPa.
  - Zn strengthens little, and has a negligible effect on work hardening.
  - Cu is the most effective at raising dislocation multiplication and slowing recovery.
- **Additivity:** solid-solution, constituent and dispersoid contributions add roughly linearly (Al–Mg–Mn, Fig. 9) [R10 p.370].

### 7.2 Precipitation and dispersion (shear versus bypass)

- **Mechanism** [R11 pp.52–56]:
  - Peak hardening occurs when the obstacle spacing ≈ the limiting dislocation radius, about 50 atomic spacings (≈10 nm).
  - GP zones are sheared; this gives chemical (interface) hardening and planar slip.
  - Large or widely spaced particles are bypassed by Orowan looping, with high work hardening.
  - Peak strength is at the shear/bypass crossover. A higher volume fraction raises both branches.
- **Shearable L1₂ (Al₃Sc):** dominant terms are coherency strain and antiphase-boundary energy (Parker), plus modulus mismatch (Marquis); these give good agreement at room temperature and 300 °C [R4 p.36].
  - Per atomic fraction, Sc is a more effective hardener than the common hardening elements. One paper claims only Au is stronger. The absolute increment is limited by low supersaturation, typically about 100 MPa [R4 p.36; R3 p.13].
- **Orowan (Polmear/Nie form)** ⚠ [R11 pp.56, 60]: Δτ = [Gb / (2π√(1−ν))] (1/λ) ln(D_p/r₀).
  - Δτ: critical resolved shear stress increment; G: shear modulus; b: Burgers vector; ν: Poisson's ratio; λ: effective planar spacing; D_p: planar particle diameter; r₀: dislocation core radius.
  - Planar spacing (π and minus signs lost ⚠):
    - {100} plates: λ = 0.931(0.306πDt/f)^½ − πD/8 − 1.061t.
    - {111} plates: λ = 0.931(0.265πDt/f)^½ − πD/8 − 0.919t.
  - Ranking: plates > rods > spheres; {111} plates > {100}; strengthening rises with aspect ratio [R11 p.60].
- **User-specified Orowan–Ashby form (general knowledge, not in sources):** Δσ = 0.4 M G b ln(2r̄/b) / (π λ √(1−ν)).
  - **(general knowledge)** For Al: M ≈ 3.06, G ≈ 26 GPa, ν ≈ 0.33.
  - b = 0.2863 nm (derived from a = 0.40496 nm [R4 Table 1]).
  - Convert CRSS to yield stress with Δσ = MΔτ.
- **Magnitudes:**
  - Age hardening can raise YS of high-purity Al by up to 50×; the theoretical upper limit for Al is about 900 MPa [R11 p.61].
  - Dispersion hardening in 8xxx is 30–40 MPa [R11 p.131].
  - Al₃Sc hardening is about 100 MPa [R3 p.13].
  - Excess Si: 0.2 % excess adds about 70 MPa to a 0.8 % Mg₂Si alloy [R10 p.381].
- **Work hardening and substructure** [R11 pp.36, 41]:
  - σ = kεⁿ, with n falling from 0.25 to 0.17 as k rises from 175 to 450 MPa.
  - Substructure: σ = σ₀ + k₁d^(−m), with m from 1 (cells) to 0.5 (subgrains).
  - Stacking-fault energy is about 170 mJ m⁻².
  - Dislocation density falls from 10¹² (cold worked) to 10¹⁰ (recovered) to 10⁷–10⁸ cm⁻² (recrystallised).

---

## 8. Sc cost, availability and substitution

- **Abundance and supply:**
  - Sc is the 31st most abundant element: half as abundant as Cu, twice Pb, 10× Sn.
  - It has no stand-alone ore; it is a by-product of W, Sn, U and Al ores [R3 p.12].
- **Master alloy production:**
  - Made by reducing Sc₂O₃ directly in molten Al, about 10× cheaper than going via Sc metal. The master-alloy price therefore tracks Sc₂O₃.
  - Al–2 % Sc is the common master alloy (1–20 % available) [R3 pp.12–13; R4 p.40].
  - Pure Sc pellets take more than 1 h to dissolve at 800 °C [R3 p.12].
- **Prices:**

| Year/source | Price | Added cost |
|---|---|---|
| 2005 [R4 p.39] | ≈US$2000/kg Sc in master alloy | 0.2 % Sc → +US$4/kg alloy (3–4× alloy price). Price had fallen 3–10× over the previous 10–15 years. |
| ~2007 [R3 p.18] | Al–2Sc ≈US$50/kg → US$2500/kg Sc | 0.2 % Sc → +US$5/kg (2–4× alloy cost) |
| Projection, red mud [R4 p.40] | ≈US$400/kg Sc | 0.2 % Sc → +US$0.80/kg |

  - Supply was mostly ex-USSR Sc₂O₃ stockpiles "to be exhausted within a few years" [R4 p.40].
  - Red mud from the Bayer process (leach → ion exchange → solvent extraction) is a bolt-on to alumina plants. R3 estimates a Sc₂O₃ price reduction of about half an order of magnitude [R3 p.18].
  - **(derived)** At US$2000/kg Sc: 0.02 % Sc ≈ US$0.40/kg; 0.05 % ≈ US$1.0/kg; 0.1 % ≈ US$2/kg alloy.
- **Substitution levers:**
  - **Zr** replaces up to about 40 % of Sc sites (Al₃Sc₀.₆Zr₀.₄) [R9 p.68]. It slows coarsening [R4 p.32], adds recrystallisation resistance beyond binary Al–Sc [R4 p.34], and allows grain refinement at lower Sc [R4 p.40].
  - **Ti** substitutes for about half the Sc at 1200 °C, lowers the Al₃Sc lattice parameter and improves grain refinement [R4 pp.24, 34].
  - **Hf, rare earths (Y, Gd, Ho, Er)** form L1₂ Al₃(Sc,X) with unchanged peak-ageing time [R4 p.33; R3 p.15].
  - **Cu, Mg, Zn** in the matrix lower the Sc needed for the same volume fraction [R1 p.1410].
  - **Small Sc in Zr alloys:** 0.02 % Sc is predicted to suppress recrystallisation in 7050 [R1 p.1420].
  - No Er-, Yb- or Hf-specific quantitative data were found (see §12). Qualitatively, Yb improves Al–Cu–Mg–Ag and Al–Zn–Mg–Cu–Zr, and Ce improves the thermal stability of Ω [R7 p.5].
- **Market (2005–07):** sports goods (bats from 1997, bicycle tubes, tent poles), Russian Al–Li and Al–Mg–Sc aerospace alloys (1421, 1570 …), and AA 2023 (Sc 0.01–0.06) and 5025 (Sc 0.05–0.55, inactive) [R4 p.39; R3 pp.16–18].

---

## 9. Mo in Al

- **Binary behaviour:** the Al end is peritectic [R10 p.383]. "0.1 wt% Mo … corresponds to the peritectic limit on the Al–Mo phase diagram" [R6 p.3].
- **Equilibrium phase:** Al₁₂Mo is in equilibrium with Al (and with Al₃Sc at 550 °C, Al–Mo–Sc) [R4 p.24].
- **Use:** 0.1–1 ppm impurity. Historically used at 0.3 % as a grain refiner and as a modifier of Fe constituents; "not in current use for these purposes" [R10 p.383].
- **Conductivity:** B precipitates V, Ti, Cr and Mo to restore conductivity, so Mo in solid solution is harmful to conductivity [R10 p.372].
- **Melt practice:** the Al–6 % Mo master alloy needs 1100 °C (versus 800 °C for Al–Ti) [R6 p.3].
- **Grain size (CP Al, as cast → after ECAP)** [R6 pp.1, 5]: pure 139 → 32 µm; +0.15Ti 91 → 18; +0.1Mo 76 → 32; +0.15Ti+0.1Mo 48 → 40/41.
  - Ti + Mo is non-additive and coarsens after ECAP ("poisoning").
- **Hollomon fits** [R6 pp.6–7]:
  - As cast: σ = 143ε^0.309 (pure Al) versus 130ε^0.299 (+0.1Mo). Flow stress at ε = 0.2: 89.5 versus 81.5 MPa (−9 %).
  - After ECAP: 141ε^0.114 versus 147ε^0.128 (+4.7 %).
  - Earlier work: 0.3 % Mo gave +16 % hardness and >30 % flow stress [R6 p.2].
- **Thermal stability and dispersoid benefits of Mo: no data in any source read** (see §12).

---

## 10. Per-element alloying effects (wrought Al)

Notation: SS = solid solution; RX = recrystallisation; cond. = electrical conductivity; NHT = non-heat-treatable. Max solubility is from [R11 p.30] unless noted. Diffusion is D at 500 °C [R11 p.105] where available.

| Element | Max solubility (wt% @ °C) | Diffusion | Partitioning / reaction | Phases formed | Strength | RX / grain | Corrosion | Conductivity | Castability / process | Typical levels |
|---|---|---|---|---|---|---|---|---|---|---|
| **Mn** | 1.82 @ 658; ≤0.23 @ 654 with Fe; ≤0.08 with Si saturation [R8] | 5×10⁻¹³ cm²/s (slowest listed) | eutectic (k < 1, gen. knowl.) | Al₆(Mn,Fe), α-Al₁₅(FeMn)₃Si₂, Al₂₀Cu₂Mn₃, Al₆Mn dispersoids [R8; R10 p.389] | SS 30.3 MPa/wt% YS [R10 Table 8]; dispersion; Mn ≈ 2× Mg in Al–Mg–Mn [R10 p.380] | raises RX temperature, fibrous structure, slows recovery [R10 p.382] | no adverse effect; Al₆(Mn,Fe) and α at ≈ matrix potential [R10 pp.382, 401]; MnAl₆ −0.85 V [R11 Table 2.5] | strong reduction in SS (gen. knowl.; R10 text says otherwise ⚠) | Fe + Mn < 1.7–2.0 % to avoid primary Al₆ [R10 p.383]; corrects acicular Fe phases | 3102: 0.05–0.4; 3207: 0.4–0.8; 3003: 1.0–1.6 [R8 Table 1.10]; ≤1.25 [R11] |
| **Fe** | 0.05 @ 655 | — | eutectic | Al₃Fe, Al₆Fe (>1–10 K/s), α-Al₈Fe₂Si, β-Al₅FeSi, Al₆(FeMn), Al₇Cu₂Fe [R8; R10] | slight; creep in conductors [R10 p.379]; 8006 fine-grain strength | reduces grain size; stabilises fine grains (8006) [R10 p.379] | Al₃Fe/Al₆Fe/AlFeSi cathodic → pitting ∝ area fraction [R10 p.399]; FeAl₃ −0.56 V | — | Fe:Si > 1 to avoid hot tearing [R8 p.29]; needles in foil | 0.4–0.7 (3xxx); 1.2–2 (8006) |
| **Si** | 1.65 @ 577 | 1×10⁻⁹ | eutectic | Si, α/β-AlFeSi, α-Al(FeMn)Si, Mg₂Si, AlSc₂Si₂ [R4] | 9.2 MPa/wt% YS; excess Si in 6xxx +70 MPa [R10] | promotes α dispersoids [R8]; GB segregation in 6xxx [R10 p.381] | Si −0.26 V (cathodic but polarised) [R11; R10 p.402]; excess Si → intergranular corrosion in 6xxx | — | hot short 0.17–0.8 % in high-purity Al [R10 p.384]; fluidity | 0.1–0.6 (3xxx) |
| **Cu** | 5.65 @ 548 | 5×10⁻¹⁰ | eutectic | θ series, S, Q, Al₂₀Cu₂Mn₃, Al₇Cu₂Fe [R10; R11] | 13.8 MPa/wt% YS (SS); age hardening max 4–6 % [R10 p.373] | most effective at slowing recovery [R11 p.34] | most detrimental (micro-constituents); 0.05–0.2 % gives more uniform corrosion and less pitting [R11 p.72]; raises potential (Al–4Cu −0.69 V) | — | ≤0.3 % in NHT [R11 p.30]; SCC in some tempers [R7 p.2] | 0.05–0.3 (3xxx) |
| **Mg** | 17.4 @ 450 | 1×10⁻⁹ | eutectic | Mg₅Al₈ (β), Mg₂Si, S, η, Al₁₂Mg₂Cr, Al₂LiMg | 18.6 MPa/wt% YS; ≤175 MPa annealed at 6 % [R11 p.30] | — | >3–4 % → β at grain boundaries → intergranular corrosion / SCC [R11 p.130; R10 p.403]; Al–5Mg −0.88 V | — | Lüders lines; hot cracking with Na [R10 p.380] | 0.1–0.3 (3xxx), 0.8–5.5 (5xxx) |
| **Zn** | 82.8 @ 443 (peritectic per R11) | — | — | MgZn₂, T-phase; τ in Al–Mg | 2.9 MPa/wt% YS; little work hardening [R11 p.34] | — | raises potential (anodic) → 7072 clad, sacrificial anodes [R10 p.385]; 0.68–0.70 % Zn in 5083 → τ instead of β [R7 p.5] | — | — | 1–1.5 for HX fin anodic protection (gen. knowl.) |
| **Cr** | 0.77 @ 661 (peritectic) | slow (qualitative) [R10 p.373] | peritectic; Al₇Cr primary at lower Cr in commercial alloys [R10 p.389] | Al₁₂Mg₂Cr, Al₁₈Mg₃Cr₂ dispersoids | slight | prevents RX in 6xxx/7xxx | reduces SCC (fibrous structure); yellow anodic film [R10 p.373] | large resistivity increase [R10 p.373] | highest quench sensitivity [R11 p.112]; sludge (factor Fe + 2Mn + 3Cr) [R7 p.5] | ≤0.35 |
| **Zr** | 0.28 @ 660.5 (peritectic) | D_Sc ≈ 4 D_Zr [R1] | peritectic, **k = 1.4** [R1] | L1₂ Al₃Zr (metastable), D0₂₃ (eq.), Al₃(Sc,Zr) shell | small | 0.1–0.3 % inhibits recovery and RX [R10 p.386]; dendrite-edge dispersoid-free zones [R1] | non-recrystallised structure helps SCC resistance [R10 p.386] | — | least quench-sensitive dispersoid [R11]; reduces TiB grain refining [R10 p.386] | <0.15 (0.05–0.25 with Sc) |
| **Sc** | ≈0.35–0.38 @ 655–659 (eutectic, 0.6 % at eutectic point) [R4; R3]; 0.025 @ 430 [R4] | D_Sc ≈ 4 D_Zr [R1] | eutectic, **k = 0.9** [R1] | L1₂ Al₃Sc (core), AlSc₂Si₂, W-phase [R4] | ~100 MPa hardening; about 300 MPa/wt% YS in 3xxx (derived) [R3] | strongest anti-RX element; +220 °C onset (0.3 %) [R4 p.34] | slightly more noble; improved self-corrosion [R4 p.38] | — (not in sources) | best grain refiner (>0.6 %, or lower with Zr) [R4 p.33]; +44 % extrusion pressure [R2] | 0.02–0.3 |
| **Ti** | ~1.3 @ 665 (peritectic) | — | peritectic; Q ≈ 35 at 0.15 % [R9] | Al₃Ti, TiB₂; substitutes in Al₃Sc [R4] | slight | grain refiner (with B); Al₃(Sc,Ti) nucleants [R4 p.34] | higher Ti improves corrosion in 3003 [R7 p.3] | depresses conductivity; removed by B [R10 p.385] | ~0.015 % optimal in DC 3003; ≥0.15 % coarser grains and casting problems [R7 p.3] | 0.01–0.05 |
| **V** | ~0.4 @ 661 (peritectic) | — | peritectic (VAl₁₁) | Al₂₁V₂; V in Al₃Sc 1.4–2.7 at% [R4] | — | raises RX temperature [R10 p.385] | — | lowers conductivity; removed by B [R10] | weaker refiner than Ti and Zr | 10–200 ppm impurity |
| **Mo** | ≈0.1 "peritectic limit" [R6] | — | peritectic | Al₁₂Mo [R4] | as cast −9 % flow stress; after ECAP +4.7 % [R6] | grain refiner at 0.3 % (historic) [R10] | — | harmful in solid solution (removed by B) [R10 p.372] | master alloy at 1100 °C [R6] | 0.1–1 ppm impurity |
| **Ni** | 0.04 @ 640 | — | eutectic | Al₃Ni (with Fe) | up to 2 % strengthens and lowers ductility; hot hardness [R10 p.383; R7 p.2] | — | promotes pitting in 1100 [R10 p.383]; NiAl₃ −0.52 V | — | — | 8001: 1.1 |
| **Li** | 4.2 @ 600 | — | — | δ′, T₁, AlLi | low density, +modulus | — | <5 ppm causes blue corrosion of foil [R10 p.380] | — | oxidises melt | — |
| **Ag** | 55.6 @ 566 | — | — | Ω (with Cu, Mg), Ag–Mg clusters | 0.1–0.6 % in Al–Zn–Mg improves strength and SCC [R10 p.384] | — | — | — | — | — |
| **Sn / In / Cd** | Sn ~0.06 @ 228 | — | — | Sn particles nucleate θ′ | 0.05 % Sn boosts artificial ageing of Al–Cu [R10 p.384; R11 p.50] | — | 0.01 % Sn darkens surfaces and raises corrosion susceptibility [R10 p.384] | — | traps vacancies; delays Si clustering [R5] | ppm–0.1 |
| **RE (Y, Gd, Ho, Er, Yb, Ce)** | — | — | — | Al₃(Sc,X) L1₂ [R4 p.33] | Y 0.1–0.2 % improves 2519 [R7 p.5] | Yb + Cr + Zr raises RX resistance [R7 p.6] | — | — | Ce changes acicular FeAl₃ [R10 p.373] | ≤0.3 at% |
| **B / Ca / Co** | Ca very low (CaAl₄) | — | — | TiB₂, VB₂ …; CaSi₂; Co₂Al₉ | Co in powder-metallurgy 7xxx | 0.2 % Ca alters RX of 3003 [R10 p.372] | — | B and Ca raise conductivity (precipitate impurities) [R10 p.372] | Ti:B 5:1–50:1 [R10 p.390]; 10 ppm Ca increases H pickup | B 0.005–0.1 |

**Electrode potentials** [R11 p.73 Table 2.5]. Volts versus 0.1 M calomel in 53 g/L NaCl + 3 g/L H₂O₂ at 25 °C; ⚠ the minus signs were lost in extraction and the values are restored as negative:

| Phase or solid solution | Potential (V) |
|---|---|
| Mg₅Al₈ | −1.24 |
| Al–Zn–Mg SS | −1.07 |
| MgZn₂ | −1.05 |
| Al₂CuMg | −1.00 |
| Al–5Mg | −0.88 |
| MnAl₆ | −0.85 |
| Al 99.95 | −0.85 |
| Al–1 % Mg₂Si | −0.83 |
| Al–1Si | −0.81 |
| Al–2Cu | −0.75 |
| Al–4Cu | −0.69 |
| FeAl₃ | −0.56 |
| CuAl₂ | −0.53 |
| NiAl₃ | −0.52 |
| Si | −0.26 |

**(inference)** For 3xxx the matrix potential is the lever. Mn and Cu in solid solution move it noble; Zn moves it anodic. Dispersoid precipitation lowers matrix Mn, so it shifts the potential, relevant to sacrificial fin/tube pairs. This is not quantified in the sources.

---

## 11. Model-ready parameter table

| Parameter | Value | Units | Conditions | Source |
|---|---|---|---|---|
| a_Al | 0.40496 | nm | room temperature | [R4 Table 1] |
| b (Al) | 0.2863 | nm | a/√2 | derived |
| a_Al₃Sc | 0.4103–0.4104 | nm | room temperature | [R4 Table 1; R9 p.68] |
| Misfit Al₃Sc/Al | ≈1.3 (RT); ≈0.47–0.5 (≈660 °C) | % | — | derived; [R4 p.34] |
| d_crit, coherency loss | 21.5 (RT), 30.8 (400 °C), 33.5 (450 °C), 36.2 (490 °C) | nm | binary Al–Sc | [R4 pp.29–30] |
| σ, Al/Al₃(Sc,Zr) | 0.1 (model); 0.06–0.18 (exp.) | J m⁻² | KWN fit | [R1 p.1411] |
| σ, Al/Al₃Sc | 0.01–0.30; cluster around 0.05–0.13 | J m⁻² | see Table §3.4 | [R4 Table 6] |
| Q\*, interface transfer | 2.07 | eV atom⁻¹ | Sc, Zr | [R1 p.1412] |
| D_Sc/D_Zr | ≈4 | — | 480 °C | [R1 p.1414] |
| D_Mn, D_Cu, D_Mg/Si | 5×10⁻¹⁷, 5×10⁻¹⁴, 1×10⁻¹³ | m² s⁻¹ | 500 °C | [R11 p.105] |
| k_Zr, k_Sc (Scheil fit) | 1.4, 0.9 | — | DC 7050 | [R1 p.1411] |
| Zr/Sc enrichment in Al₃Sc | 2.2 × alloy ratio | — | 600 °C | [R4 p.23] |
| KWN nucleus size offset | 1.10 r\* | — | — | [R1 p.1412] |
| Slices across dendrite | ~50 | — | — | [R1 p.1413] |
| a_LSW, Al₃(Sc,Zr) 7050 | 1.7–2.4 (model), 7.0–11.4 (KV), 6.9 (meas.) | 10⁻³⁰ m³ s⁻¹ | 480 °C | [R1 Table 2] |
| JMAK n, Al₃Sc | 1.3–2.16 | — | 240–370 °C | [R4 Table 4] |
| Incubation / overlap, Al–0.18Sc | 24.5 / 150 min (288 °C); 7 / 20 min (343 °C) | min | quenched from 650 °C | [R4 p.28] |
| Al₃Sc hardening window | 250–350 | °C | 2–6 nm | [R4 p.33] |
| Al₃Sc dispersoid window | 400–600 | °C | 20–100 nm | [R4 p.33] |
| Al₃(Sc,Zr) mean radius, 7050 | ≈10 (0.13Zr), ≈12 (0.07Zr–0.1Sc) | nm | 480 °C plateau | [R1 p.1415] |
| Time to plateau volume fraction | ≈1 | h | 0.1Sc–0.13Zr, 480 °C | [R1 p.1413] |
| Sc solubility | 0.35 (eut.), 0.025 (430 °C), 0.03 (550 °C, with Zr), 0.06 (600 °C, with Zr) | wt% | — | [R4 pp.20, 22; R9 p.68] |
| Mn solubility (binary) | 1.8 (654), 1.0 (627), 0.42 (527), 0.2 (427) | wt% | °C in brackets | [R8 Table 1.9] |
| Mn solubility (+Fe) | 0.23, 0.13, 0.05, 0.026 | wt% | same temperatures | [R8 Table 1.9] |
| Mn solubility (+Si, Si-saturated) | 0.08 (573), 0.07 (550), 0.06 (500), 0.05 (450), 0.04 (400) | wt% | — | [R8 Table 1.13] |
| Mn solubility (α + Al₆Mn field) | 1.3 (649), 0.73 (600), 0.44 (550), 0.25 (500), 0.15 (450), 0.06 (400) | wt% | — | [R8 Table 1.13] |
| Si solubility (α + Si field) | 1.66 (573), 1.36 (550), 0.85 (500), 0.45 (450), 0.25 (400) | wt% | — | [R8 Table 1.13] |
| Dispersoid size range | 0.05–0.5 | µm | homogenisation | [R11 pp.43, 78] |
| PSN threshold | >~1 | µm | — | [R11 p.42] |
| Homogenisation heating rate | ~50–75 | °C h⁻¹ | fine dispersoids | [R11 p.105; R2 p.18] |
| Homogenisation T, t | 450–600; 6–24 | °C; h | — | [R11 p.105] |
| Δt factor per +50 °C | ≈1/3 | — | homogenisation | [R11 p.105] |
| Zener pressure | P_Z = 3F_Vγ/(2r) | Pa | random, incoherent | [R12 p.114] |
| Coherent pinning factor | 2× | — | F_C = 2πrγ | [R12 p.112] |
| SS slopes (YS) | Si 9.2, Zn 2.9, Cu 13.8, Mn 30.3, Mg 18.6 | MPa/wt% | annealed super-purity | [R10 Table 8] |
| Dispersion hardening (8xxx) | 30–40 | MPa | — | [R11 p.131] |
| Al₃Sc hardening | ~100 | MPa | — | [R3 p.13] |
| Sc YS increment (3xxx extruded) | ~300 | MPa/wt% Sc | 0–0.26 Sc, Al–0.5Mn–0.2Mg–0.15Zr | derived [R3 Table 1] |
| Quench-sensitivity range | 290–400 | °C | — | [R11 p.112] |
| Grain-refinement Q | Ti ≈35 (0.15 %), Sc 2.5 (0.6 %) | K | — | [R9 p.65] |
| Fe_crit (Al–Si casting) | 0.075[%Si] − 0.05 | wt% | casting alloys | [R7 p.5] |
| Sludge factor | [Fe] + 2[Mn] + 3[Cr] | wt% | casting | [R7 p.5] |

---

## 12. Open questions and gaps

1. **D₀ and Q per solute** (Mn, Fe, Si, Cu, Mg, Zn, Cr, Zr, Sc, Ti, Mo, V, Er) are **missing from every source read**. Only D(500 °C) for Mn, Cu, Mg and Si [R11] and the ratio D_Sc/D_Zr ≈ 4 [R1] are available.
   - **(general knowledge)** Commonly used Arrhenius data for Sc and Zr imply a much larger D_Sc/D_Zr at 480 °C than 4. This must be reconciled before KWN calibration.
   - Action: source the Du et al. 2003 or Fujikawa compilations into the Drive.
2. **Mn dispersoid kinetics for 3xxx** (α-Al(Mn,Fe)Si number density, size and coarsening; nucleation on Mg₂Si/"u-phase" precursors; DFZ widths) are not quantified in any source. R8 gives only phase fields; R10 and R11 are qualitative.
   - A 3xxx homogenisation/dispersoid paper is needed, e.g. Li & Arnberg (general knowledge).
3. **Partition coefficients** are available only for Zr and Sc [R1]. k for Mn, Fe, Si, Cu, Cr and Ti is needed for Scheil initialisation.
4. **Activation energies** for cluster formation, GP/β″ precipitation and Al₃Sc nucleation are absent, apart from Q\* = 2.07 eV for interface transfer [R1].
5. **R5 is truncated (p.73).** Chapters 6–8 (reversion kinetics, the Mg–vacancy link, Mg-gradient diffusion couple) were not read. Re-read in page ranges.
6. **R11 and R12 are truncated.** Polmear Ch. 4+ and Humphreys Ch. 9 (particle pinning in recrystallisation, critical F_V/r, Smith–Zener limit) and Ch. 11 were not read.
7. **Braze survival of Al₃(Sc,Zr) at 600–610 °C.**
   - Polmear claims recrystallisation inhibition up to 600 °C [R11 p.52]; R2 measured recrystallisation at 575–600 °C with 0.19Sc–0.05Zr.
   - The Zr level and core–shell state needed for a 2–3 min 600 °C braze are unknown. Proposed experiment: Sc 0.05–0.15 × Zr 0.10–0.20 on 3102/3207 bases.
8. **Sc in Fe/Si-bearing 3xxx.** The thresholds for V-phase (AlSc₂Si₂) formation and the loss of Sc efficiency at 3xxx Si/Fe levels are not quantified. There are only two data points [R4 p.32].
9. **Er, Yb, Hf substitution.** No quantitative kinetics or coarsening data. R4 gives only "unchanged peak time" for Y, Gd, Ho and Er at 285 °C.
10. **Mo.** No data on solubility versus temperature, diffusivity, Al₁₂Mo dispersoids or thermal-stability benefits. R6 is a grain-size and ECAP study only.
    - **(general knowledge)** Recent literature reports Mo-modified α-Al(Mn,Fe,Mo)Si dispersoids with improved thermal stability in 3xxx. That literature should be added to the Drive.
11. **Conductivity coefficients** (resistivity per wt% in solid solution and per vol% of precipitate) are missing. They are needed to use conductivity as a dispersoid-precipitation sensor [R10 p.370].
12. **Equation fidelity** ⚠: check against the PDFs:
    - R1 Eq. 3 (grouping of the 1/3 factor);
    - R11 Orowan / planar-spacing expressions (π and minus signs);
    - R4 Table 3 (Al₃Sc properties);
    - R8 Tables 1.9 and 1.13 (column alignment).
13. **Strengthening constants.** G, Taylor factor M and ν for Al are not stated in any source. Solid-solution exponent n is not stated; only linear unit effects with a non-linearity caveat [R10].
