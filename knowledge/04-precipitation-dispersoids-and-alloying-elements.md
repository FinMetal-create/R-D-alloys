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
| R5 | Ivanov R., *Solute clustering in multi-component aluminium alloys*, PhD thesis, Univ. Grenoble Alpes 2017, HAL tel-01688296 (catalog **S-020**; "Clusters in Al alloys.pdf"). Full-text pass from the four split parts in Drive folder "Cloud part book", in page order a → c → d → b | Whole file: https://drive.google.com/file/d/1x56HZKJZm77CxOCd9uFSz4Zlj6UclDIr/view · parts: a (front matter, pp.1–23) https://drive.google.com/file/d/1_b2vYkSh-D3q_xK1trgin68tSXUIMDJq/view · c (pp.30–60) https://drive.google.com/file/d/1rh9i0xBcFlpWWnXgwa5ld9f3yZkbxZug/view · d (pp.60–93) https://drive.google.com/file/d/13541hzVFdzVjghUtlwz5W27mkaWM-Y59/view · b (pp.94–130) https://drive.google.com/file/d/1Onl4LXeACBjQZY-B2CMWhg6OD0r794kc/view | **Near-full text, 2026-10-12.** Front matter and pp.1–23 and 30–130 read (Ch. 1–9, all four result chapters). **pp.24–29 are missing** (end of the Ch. 2 reference list, Ch. 3 opener, start of §3.1; the alloy table on p.30 is present). pp.30–60 exist only as Drive text without page breaks; their page numbers come from the printed page markers in that text. Equations lost their symbols (U+FFFD) and are described only where the prose makes them unambiguous; figures are not readable. Citations are **printed** pages. Focus is Al–Cu–(Li,Mg) with 1.1–1.5 at% Cu; Al–Mg–Si appears only in the literature review and chapter introductions. |
| R6 | Zaid A.I.O., Atieh A.M., *Effect of molybdenum addition on aluminium grain refined by titanium…*, IOP Conf. Ser. MSE 60 (2014) 012052 ("Al_Mo.pdf") | https://drive.google.com/file/d/1ON8iVgDGl7jAcEPzomcKjFVIabk8ld_Q/view | Full (8 pp) read. Low information: casting and ECAP grain size only. No solubility, dispersoid or thermal-stability data. |
| R7 | Rana R.S., Purohit R., Das S., *Reviews on the influences of alloying elements on the microstructure and mechanical properties of aluminum alloys and aluminum alloy composites*, IJSRP 2(6) 2012 ("Influence of alloying elements.pdf") | https://drive.google.com/file/d/1eenW1k-qr4_bAY3wtnZBPPDu-uDBzGJC/view | Full (7 pp) read. Qualitative and casting-oriented; text interleaved. |
| R8 | Belov N.A., Eskin D.G., Aksenov A.A., *Multicomponent Phase Diagrams: Applications for Commercial Aluminum Alloys*, Elsevier 2005, Ch. 1 "Alloys of the Al-Fe-Mn-Si system" ("Chapter 1 - Alloys of the Al_Fe_Mn_Si System.pdf") — *found by Drive search* | https://drive.google.com/file/d/1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD/view | Full chapter (pp.1–46) read. Tables 1.9 and 1.13 were reconstructed from garbled columns. Figures are lost. Key source for 3xxx. |
| R9 | Eskin D.G., *Physical Metallurgy of Direct Chill Casting of Aluminum Alloys*, CRC 2008, Ch. 2 "Solidification of aluminum alloys" ("62816_ch02.pdf") — *found by Drive search* | https://drive.google.com/file/d/1MBeZaNbetcIq6Xjcoj2Y56AW9wZPwcb2/view | Full chapter read (text interleaved). Used for Scheil, growth restriction and Al–Sc–Zr. |
| R10 | Davis J.R. (ed.), *Alloying: Understanding the Basics*, ASM 2001, "Aluminum and Aluminum Alloys" pp.351–416 ("Aluminum and Aluminum Alloys Davis.pdf") — *found by Drive search* | https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view | Full read. Good per-element text; Table 8 gives solid-solution strengthening data. Figures are not readable. |
| R11 | Polmear I.J., *Light Alloys*, 4th ed., Butterworth-Heinemann 2006 ("115132137-Light-Alloys.pdf") — *found by Drive search* | https://drive.google.com/file/d/1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w/view | **Extraction truncated at ~book p.174** (Ch. 1–3). Ch. 2 was read fully; Ch. 3 in parts. Some symbols (π, −, Greek) were lost. |
| R12 | Humphreys F.J., Hatherly M., *Recrystallization and Related Annealing Phenomena*, 2nd ed., Elsevier 2004 ("85721252-…Re-Crystallization…pdf") — *found by Drive search* | https://drive.google.com/file/d/1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w/view | Extraction truncated at ~book p.190. Only §4.6 (Zener drag) was used. γ symbols were lost and have been restored. |
| TOT | Totten G.E., MacKenzie D.S. (eds.), *Handbook of Aluminum, Vol. 1: Physical Metallurgy and Processes*, Marcel Dekker 2003 (catalog **S-029**). Used: **Ch. 3** Tiryakioğlu M., Staley J.T., "Physical Metallurgy and the Effect of Alloying Additions in Aluminum Alloys", pp.81–210; **Ch. 5** Katgerman L., Eskin D., "Hardening, Annealing, and Aging", pp.259–301; Ch. 2 (Sverdlin) pp.39–40 and 52 only | S-029: https://drive.google.com/file/d/1UsZI7XP3jC8Pu0Mjiqksj2dQEmozI2O2/view ; part file `Al 1-400.pdf`: https://drive.google.com/file/d/1Yxag4tVsKp2w7GaNvUqpz09wJRuCpLVT/view | **Full text 2026-10-12.** Ch. 3 and Ch. 5 read in full from a repaired text layer; whole book searched for diffusion data. Citations `[TOT p.x]` are **printed** pages (PDF page = printed page + 12). Figures are not readable. Some equations are garbled and some Greek letters are guesses; these are flagged ⚠. |

Not used:
- Anything in the `microstructure-sim-v2.14.0` tree (`src/models/*.js`, `App.jsx`, tests), as instructed.
- `AA3207_Recrystallization_Simulation.xlsx`, which is a user model, not literature.
- Large handbooks (ASM vol. 1, extrusion books, Kaufman), which I did not read. They are candidates for later passes. *Alminium.pdf* is the same book as S-029, and its Ch. 3 and 5 are now used as [TOT] (full-text pass 2026-10-12).

---

## 0. Executive summary for alloy design (3xxx-centred)

1. **Mn dispersoid budget is set by casting plus Fe/Si, not by the nominal Mn.**
   - Binary Mn solubility falls from 1.82 % at 658 °C to about 0.2 % at 427 °C [R11 p.30; R8 p.12 Table 1.9].
   - When Al₃Fe and Al₆(FeMn) are co-present, Mn solubility drops to 0.23 % at 654 °C and 0.026 % at 427 °C [R8 Table 1.9].
   - In the Si-saturated field, Mn solubility is ≤0.08 % from 573 °C downwards [R8 Table 1.13].
   - Only 0.2–0.3 % Mn tends to stay in solid solution after preheat and hot work [R11 p.30; TOT p.94].
   - As-cast DC 3003 holds 0.7–0.9 % Mn in solution; the rest sits in Al–Mn–Fe(–Si) constituents [TOT p.160].
   - Casting at 10–100 K s⁻¹ can saturate (Al) with transition metals up to the equilibrium limit (eutectic systems) [TOT p.294]. Mn in (Al) reaches 2.5 % at 10 K s⁻¹ and 2.8 % at 100 K s⁻¹ [TOT p.294 Table 33].
2. **Si converts Mn chemistry from Al₆(Mn,Fe) to α-Al₁₅(FeMn)₃Si₂.**
   - Si enables α-dispersoid formation during annealing [R8 p.32].
   - Si drastically lowers Mn solubility, so more Mn precipitates [R8 Table 1.13].
   - When Fe and Si are fully bound in α, the Mn and Si left in (Al) set the dispersoid amount [R8 p.37].
   - Homogenisation transforms Al₆(Fe,Mn) into α-Al₁₂(Fe,Mn)₃Si [R11 p.107; TOT p.160].
   - Si accelerates Mn precipitation, gives a denser α-Al₁₂(Mn,Fe)₃Si dispersion and lowers retained Mn. Below 0.07 % Si the dispersoid is usually Al₆(Mn,Fe) [TOT p.160].
3. **Dispersoid number density, not size, is the lever. Supersaturation drives nucleation.**
   - Extra Sc/Zr mainly raises number density; radius stays about 10 nm at 480 °C [R1 pp.1415, 1419].
   - Recrystallisation resistance is best when dispersoids form at T_disp < T_anneal before deformation, or during an intermediate anneal [R4 p.35].
   - Slow heating (50–75 °C h⁻¹) promotes fine, uniform dispersoids [R11 p.106].
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
7. **Lean Al–Fe–Si–Mg(–Mn) slug alloys such as T11 are controlled by Si partitioning, not by Mn.** (Added after the [TOT] full-text pass; details in §2.6 and §6.4.)
   - The Fe-phase type decides how much Si stays free for Mg₂Si. The rule Si(available) = Si − ¼(Fe + Mn) [TOT p.171 Eq 26] gives ≈ 0.22 % for T11 (derived). If β-Al₅FeSi forms instead, only ≈ 0.07–0.12 % is left (derived, §6.4).
   - Dilute Mg₂Si alloys (< 0.8–0.9 %) gain, not lose, from room-temperature storage before artificial ageing [TOT pp.175–176, 279; R11 pp.141–142].
   - Fe retained in solution by fast casting raises the recrystallisation onset (+65 K at 0.04 at% Fe in Yelagin's binaries) through fine Al–Fe precipitation during the anneal [TOT pp.140, 296 Table 35].
8. **Room-temperature clustering runs on quenched-in vacancies, and 200–250 °C is the cluster-reversion window.** (Added after the [R5] full-text pass; details in §6.5–6.6.)
   - In Al–Cu–(Li,Mg) quenched from 500 °C, natural ageing is mostly done in 24 h, hardness saturates after ≈ 10 h, and the 72 h state is stable for 6 months [R5 pp.30–31, 71]. Mg accelerates clustering with no threshold; Mg is thought to raise the number or mobility of free vacancies [R5 pp.103, 109].
   - Once the quenched-in vacancies are gone, dissolved solute does not re-cluster at room temperature for 20 days [R5 p.102]. **Storage drift is therefore set by the last fast cooling, not by the solute content alone** (inference for T11 slugs).
   - Natural-ageing clusters dissolve within seconds to a minute at 200–250 °C, and dissolution overlaps with the start of precipitation [R5 pp.92, 95–96]. The 220 °C/10 min bake lies in this window, so clusters formed in storage should revert early in the bake (inference, transferred from Al–Cu–(Li,Mg)). Whether they revert or seed β″ in Al–Mg–Si is open (§6.5). Any bake gain in the wall then has to come from precipitation on dislocations.

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
  - TOT groups the transition metals as **eutectic: Mn, Fe, Sc, Ni** and **peritectic: Cr, V, Zr, Ti, Mo** [TOT p.294].
  - Al–Cr: peritectic at 661 °C, peritectic composition 0.41 % Cr, maximum solubility 0.77 % Cr. Primary Al₇Cr forms between these limits and is retained under commercial cooling [TOT p.116].
  - Al–Mn: eutectic Al–Al₆Mn at ≈ 1.9 % Mn and 657 °C [TOT p.159].
- **Transition-metal (TM) supersaturation depends on the solidification type** [TOT pp.293–295].
  - Supersaturation rises continuously with cooling rate in eutectic systems. Peritectic systems need a threshold cooling rate of about 10² K s⁻¹.
  - Al–TM supersaturated solutions are much more stable than those of Cu, Mg, Zn, Si and Li. They decompose between 250 and 650 °C, depending on the element.
  - Eutectic-system solid solutions decompose at lower temperature and faster than peritectic ones, because the eutectic-forming elements diffuse about an order of magnitude faster.
  - Dendritic TM segregation is not easily removed by homogenisation, because TM diffusion is slow.
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

**Full-text check against [TOT] (2026-10-12).** TOT Table 1 [TOT p.92] gives the maximum solubility in at% and agrees with the table above for Ag, Cr, Fe, Mn, Ni, Si and Zn. Differences are flagged, not resolved:
- **Mg ⚠ conflict.** TOT gives 14.9 wt% at 450 °C [TOT p.161] and 16.26 at% [TOT p.92]. R11 gives 17.4 wt% / 18.5 at%. TOT also gives ≈ 1.7 wt% at room temperature [TOT p.161].
- Cu: 2.48 at% [TOT p.92] versus 2.40 at% [R11]. Ge: 2.30 versus 2.7 at%.
- Li: TOT is internally inconsistent: 13.9 at% in Table 1 [TOT p.92], "≈ 4 wt% (16 at%) at 610 °C" in the text [TOT p.152]. R11 gives 4.2 wt% at 600 °C.
- Limit solubilities in TOT Table 34 [TOT p.295], at%: Mn 0.88, Cr 0.41, Zr 0.093, V 0.21, **Ti 0.17** and **Sc 0.28**.
  - Ti 0.17 at% is far below R11's ~0.74 at% (~1.3 wt%). Sc 0.28 at% (≈ 0.47 wt%, derived) is above R4's ≈ 0.35–0.38 wt% (≈ 0.21–0.23 at%, derived). ⚠ Both differences are unresolved.
- Mg₂Si quasi-binary: eutectic at 595 °C and maximum solubility 1.85 wt% Mg₂Si [TOT p.171], the same as R10. **No solvus-versus-temperature values are given** (the figure is not readable).

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

Sources: binary and Fe columns from [R8 p.12 Table 1.9; values below 654 °C are approximations]; Si columns from [R8 p.15 Table 1.13] (Drits 1977 and Phillips 1959; I reconstructed the columns from the garbled extraction ⚠). In the α+Al₆Mn field Mn solubility is about the same as binary Al–Mn; in the Si-saturated field Mn is ≤0.1 % [R8 p.13 text]. Note that R8 Fig 1.4b (Mondolfo) disagrees: it shows ~1 % Mn at 527 °C instead of ~0.4 %. The calculated 550 °C section (Du et al. 2004) agrees with the table [R8 p.13].

**Fe and Si.**
- Fe in (Al) is ≤0.05 % [R8 p.3; TOT pp.117, 138].
- Secondary (solid-state) Fe-phase volume cannot exceed 0.1–0.2 vol% [R8 p.10; R9].
- Si solubility in (Al) is lowered by other elements, especially Mg [TOT p.122].
- **Si available for Mg₂Si** = wt% Si − ¼(wt% Fe + wt% Mn) [TOT p.171 Eq 26].
- With excess Si, wt% Mg₂Si = 1.578 × wt% Mg [TOT p.171 Eq 25]. The stoichiometric Mg:Si weight ratio is 1.73 [TOT p.169].

**Effect of cooling rate on TM supersaturation of (Al)** [TOT p.294 Table 33] (wt% as printed, presumably):

| Cooling rate (K s⁻¹) | Mn | Cr | Zr | V | Ti | Sc |
|---|---|---|---|---|---|---|
| 10⁻¹ | 1.82 | 0.82 | 0.28 | 0.37 | 0.28 | 0.4 |
| 10¹ | 2.5 | 0.4 | 0.1 | 0.1 | 0.1 | 0.4 |
| 10² | 2.8 | 0.7–1.0 | 0.15–0.17 | 0.25 | 0.2 | 0.5 |
| 10³ | 3.0–5.0 | 1.5–3.5 | 0.5–0.7 | 1.3 | 0.4–1.0 | 1.1 |
| 10⁴ | 5.0–7.0 | 2.0–5.7 | 0.9–1.7 | — | 1.4 | — |
| 10⁵ | 6.1–10.0 | 5.35–5.7 | 1.2–2.0 | 1.3 | — | 3.2 |
| 10⁶ | 8.6–14.0 | 5.8–7.75 | 2.5–2.8 | 2.6 | 3.7–5.0 | — |

- The dip at 10 K s⁻¹ for the peritectic formers (Cr, Zr, V, Ti) fits the ~10² K s⁻¹ threshold [TOT p.295].
- Ingot and casting practice runs at 10–100 K s⁻¹ [TOT p.294]. Fe is not in the table.
- **Relevance (rotary-cast 22 mm strip):** at a casting cooling rate in or above this range, all of T11's 0.14 % Mn could in principle stay in (Al). In practice part of it goes into Fe-rich constituents [TOT p.160] (inference). The cast strip should be treated as a supersaturated, non-homogenised solid solution in Mn and, possibly, Fe (inference; see §5).

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
| Cr | "slow diffusion rate" → fine dispersed phases | qualitative | [R10 p.373]; Cr can stay in solution because of its low diffusivity [TOT p.168] |
| Dispersoid formers | "modest solubility and … diffuse slowly" | qualitative | [R11 p.78; TOT p.102] |
| Transition metals in Al (range) | 10⁻¹⁴ to 10⁻¹² cm² s⁻¹ (printed "cm³/sec", a misprint) | 500 °C | [TOT p.295] |
| Eutectic vs peritectic TM | D(Mn, Fe, Sc, Ni) about **10×** D(Cr, V, Zr, Ti, Mo) | group statement | [TOT p.295] |
| Vacancy formation / migration / self-diffusion energy | E_f = 0.76 eV, E_m = 0.65 eV, E_sd = 1.4 eV (single vacancy); divacancy binding 0.17 eV, migration 0.50 eV | pure Al | [TOT p.40 Table 8] |
| Vacancy formation energy | ≈ 0.7 eV | pure Al | [TOT p.86] |
| Solute transport during GP-zone formation | several orders of magnitude faster than normal diffusion at the same temperature (quenched-in vacancies); ≈ 10⁷× the expected rate in Al–Cu | after quench | [TOT pp.128, 271] |
| D₀, Q for Cu in Al | 4.44×10⁻⁵ m² s⁻¹, 133.9 kJ mol⁻¹ (Du et al. 2003); 1.00×10⁻⁵, 127.6 (Doig & Edington 1973); 4.37×10⁻⁶, 120.6 (Mantina et al. 2009, first principles) | Arrhenius | [R5 p.121 Table 10] (secondary compilation) |
| D₀, Q for Mg in Al | 1.49×10⁻⁵ m² s⁻¹, 120.5 kJ mol⁻¹ (Du); 1.00×10⁻⁶, 110.0 (Doig & Edington); 1.19×10⁻⁵, 122.5 (Mantina) | Arrhenius | [R5 p.121 Table 10] |
| D₀, Q for Li in Al | 1.55×10⁻⁵ m² s⁻¹, 119.2 kJ mol⁻¹ (Wen et al. 1980) | Arrhenius | [R5 p.121 Table 10] |
| Al self-diffusion | D₀ = 6.6×10⁻⁶ m² s⁻¹, Q = 124.5 kJ mol⁻¹ (the normalising values in the Table 10 caption; source not named) | Arrhenius | [R5 p.121] |
| Vacancy formation enthalpy | 0.75 eV (used to estimate equilibrium vacancy ratios) | pure Al | [R5 p.103]; cf. 0.76 eV [TOT p.40] |
| Solute–vacancy binding (first principles, Wolverton 2007) | Cu ≈ +0.02 eV, Mg ≈ −0.02 eV (repulsive), Sn 0.25 eV | dilute Al | [R5 p.122] |

- Diffusion distance is x = √(Dt) [R11 p.105].
- Doubling x needs 4× time. Raising the homogenisation temperature by 50 °C cuts time to about ⅓. Practical homogenisation times are 6–24 h [R11 p.105].
- **(derived)** For 24 h at 500 °C, x ≈ 2 µm for Mn, ≈ 66 µm for Cu and ≈ 93 µm for Mg/Si. Mn therefore never levels across a 20–50 µm dendrite cell; Cu, Mg and Si do.
- In KWN slice models, long-range Sc and Zr diffusion between dendrite slices had only a minor effect [R1 p.1413].
- **D₀ and Q per solute: now available for Cu, Mg and Li only** [R5 p.121 Table 10] (updated after the [R5] full-text pass). [TOT] gives none: Ch. 2, 3 and 5 were checked and the whole book was searched (2026-10-12). Si, Mn, Fe, Zn, Cr, Zr, Sc and Ti are still missing (§12).
  - **Cross-check (derived):** the Du et al. set gives D_Mg(500 °C) ≈ 1.1×10⁻¹³ m² s⁻¹ and D_Cu(500 °C) ≈ 4.0×10⁻¹⁴ m² s⁻¹. These agree with Polmear's 1×10⁻¹³ and 5×10⁻¹⁴ m² s⁻¹ [R11 p.105].
  - All three data sets have Mg diffusing faster than Cu (Mg ≈ Li > Cu) [R5 p.121]. Experimental and first-principles D₀ differ by up to 15× for Mg; R5 does not choose between them.
  - **Equilibrium-vacancy diffusion is negligible at room temperature (derived):** at 20 °C the Mg sets give D ≈ 2×10⁻²⁷–3×10⁻²⁶ m² s⁻¹, i.e. a diffusion distance below 0.3 nm (one atomic spacing) in 30 days. Natural ageing within hours therefore needs excess (quenched-in) vacancies, consistent with [TOT pp.128, 271] and [R5 pp.3, 89].
  - **Bake-scale diffusion (derived, T11):** at 220 °C for 10 min, √(Dt) ≈ 28–39 nm for Mg and 13–21 nm for Cu, with equilibrium vacancies only. Si is not in Table 10; R11 gives D_Si ≈ D_Mg at 500 °C [R11 p.105]. This agrees with the 30–45 nm used in [ch19 §1.1].
- **Mn-diffusivity conflict, resolved for this chapter (full-text pass).** Elsewhere in the knowledge base, Sheppard's Mn row gives diffusion about 10³× faster than Polmear's D_Mn(500 °C) = 5×10⁻¹³ cm² s⁻¹ [ch07 §11 G9]. TOT's TM range at 500 °C, 10⁻¹⁴–10⁻¹² cm² s⁻¹ [TOT p.295], contains Polmear's value. A value 10³× higher would lie outside it (derived). **Use the Polmear scale.**
- **D_Sc/D_Zr, still unresolved.** R1 uses ≈ 4 at 480 °C [R1 p.1414]. Arrhenius sets elsewhere in the knowledge base give ≈ 510 [ch13] and ≈ 640 [ch18 §2.3] at 480 °C. TOT gives only the group statement that eutectic formers (Sc) diffuse about 10× faster than peritectic formers (Zr) [TOT p.295]. That supports D_Sc > D_Zr but fixes neither value. Tracer data (Fujikawa) are still needed (§12).

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
- **3xxx phase path, TOT version** [TOT pp.159–160, 299; Table 6 p.123; Table 7 p.125]:
  - Constituents in 3xxx: Al₆(Fe,Mn) and Al₁₂(Fe,Mn)₃Si. Dispersoids in 3003: Al₁₂(Mn,Fe)₃Si and Al₆(Mn,Fe).
  - Ingot casting (cooling rate < 10² K s⁻¹) readily gives a Mn-supersaturated (Al). It decomposes **above ≈ 325 °C** into fine Al₆Mn or (AlFeMn) and (AlFeMnSi) dispersoids. Table 34 gives a decomposition range of **300–350 °C** for Al–Mn [TOT pp.295, 299].
  - There is "no real precipitation hardening". The dispersoids act by hindering grain growth during recrystallisation, which gives fine grains [TOT p.299].
  - Dispersoid size is typically < 1 µm and depends on the homogenisation conditions [TOT p.160].
  - **A high Fe/Mn ratio can produce Al₁₃(Fe,Mn)₄ in as-cast 3xxx** [TOT p.160, citing Cama et al. 1997].
  - High Fe and Si, and small Cu and Mg contents, also refine the grain size. Fe controls the texture and hence earing [TOT p.299].
  - 3004-H19 can body sheet relies on careful control of the size, volume fraction and distribution of Al₁₂(Fe,Mn)Si constituents [TOT p.123].
- **Mn partners in other families** [TOT pp.168, 177, 179, 192]:
  - In 5xxx, Mn dispersoids form as **Al₆(Mn,Fe)**, because Mg₂Si consumes the Si.
  - In 6xxx, Mn forms Al₁₀Mn₂Si (as printed) or α-Al₁₅(Mn,Fe)₃Si₂ ("virtually insoluble"). This takes Si out of the matrix and lowers the ageing response.
  - In 7xxx, AlMn₆ (Cu-free) and Al₂₀Cu₂Mn₃ dispersoids are larger than the Cr E-phase and less effective against recrystallisation.
- **Effectiveness ranking** [TOT p.125]:
  - Particles below about 0.4 µm retard recrystallisation by pinning subgrain boundaries and preventing subgrain coalescence.
  - Coherent dispersoids (Al₃Zr) beat incoherent ones (Al₁₂Mg₂Cr, Al₂₀Mn₃Cu₂). A passing boundary must either change the interface to semi- or incoherent, or dissolve and reprecipitate the particle.
- **8006-type (Fe ≫ Si):** dispersoids formed by annealing above 300–350 °C are mostly **Al₆Mn**, not Al₆(FeMn), because Fe solubility is negligible. Their amount is set by the non-equilibrium Mn in (Al) [R8 pp.31–32].
- **Cr dispersoids:** Al₁₈Mg₃Cr₂ in 5xxx; closer to Al₁₂Mg₂Cr in 7xxx. They contribute strength in non-heat-treatable (NHT) alloys and control recrystallisation in heat-treatable alloys [R10 p.390].
- **Zr dispersoids:** equilibrium Al₃Zr is tetragonal, but fine **metastable cubic (L1₂) Al₃Zr** forms in preheat; usually <0.15 % Zr [R10 p.390].
  - In Ref. [R1]'s 7050 (0–0.3Sc, ≤0.13Zr), all dispersoids remained L1₂ even after 40 h at 475 °C; no D0₂₃ formed [R1 p.1410].
- **Heterogeneous nucleation on transient precipitates.**
  - Dispersoids nucleate on precipitate particles that form and grow during *slow* heating. The dispersoids survive at the homogenisation temperature; the precursor precipitates redissolve.
  - Example: η-MgZn₂ nucleated Al₆Mn in Al–Zn–Mg–0.3Mn homogenised 500 °C/24 h, heated at 50 vs 500 °C h⁻¹ [R11 pp.105–106, Fig 3.8].
- **Si effect on Mn dispersoids.**
  - With Si, α-Al₁₅(Fe,Mn)₃Si₂ forms in casting **and** in annealing, because Si has relatively high solubility [R8 p.32].
  - In the Si-saturated field, Mn solubility drops to 0.04–0.08 % (400–573 °C) [R8 Table 1.13]. Si therefore raises the driving force for Mn precipitation (inference).
  - Si also converts Al₆(Fe,Mn) constituents to α during homogenisation [R11 p.107].
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

Davis calls α "cubic αAl₁₂Fe₃Si", β "monoclinic β-Al₉Fe₂Si₂" and the quaternary "Al₁₂(Fe,Mn)₃Si" [R10 pp.369, 388]. The phases are the same; the formula conventions differ. TOT uses the same names: α-Al₁₂Fe₃Si, β-Al₉Fe₂Si₂ [TOT p.138], α-Al₈Fe₂Si and β-Al₅FeSi [TOT p.179].

**Binary Al–TM phases** [TOT p.295 Table 34]:

| System | Phase | Structure, lattice (nm) | Limit solubility (at%) | Decomposition T of the supersaturated solution (°C) | Precipitation-hardening effect ΔH/C (per at%) ⚠ |
|---|---|---|---|---|---|
| Al–Mn | Al₆Mn | orthorhombic a 0.6498, b 0.7552, c 0.8870; metastable cubic Al₁₂Mn a 0.747 | 0.88 | 300–350 | 10 |
| Al–Cr | Al₇Cr | orthorhombic a 2.48, b 2.47, c 3.02 | 0.41 | 450–500 | 51 |
| Al–Zr | Al₃Zr | tetragonal a 0.4006, c 1.727; metastable cubic a 0.407 | 0.093 | 400–450 | 154 |
| Al–V | Al₁₁V | cubic a 1.4586 | 0.21 | 500–550 | 31 |
| Al–Ti | Al₃Ti | tetragonal a 0.3848, c 0.8596 | 0.17 | — | — |
| Al–Sc | Al₃Sc | cubic a 0.4104 | 0.28 | 250–350 | 208 |

⚠ The quantity H and its unit are not defined in the extracted text. Use the last column as a relative ranking only. The Al₆Mn lattice matches R8's Al₆(FeMn) (a 0.75518, b 0.64978, c 0.88703) with a and b swapped.

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
- Slow heating, about 75 °C h⁻¹, "necessary to promote nucleation and growth of a fine and uniform dispersion" [R11 p.106].
- Cooling-rate control and a second isothermal step are sometimes used [R11 p.107].
- R2's Sc–Zr billets: heat 50 °C h⁻¹, cool 350 °C h⁻¹, 400 °C/8 h versus 450 °C/4 h. Both gave negligible differences in extrusion and post-braze properties [R2 pp.18, 38, 43].

**Strength contribution:**
- 8xxx (8006 Al–1.6Fe–0.65Mn, 8011): dispersion hardening is about **30–40 MPa** of proof and tensile strength; solid solution adds 2–10 MPa (proof) and 5–20 MPa (UTS) [R11 p.131].
- Annealed 3003 UTS ≈110 MPa versus 90 MPa for 1100 [R11 p.129].
- 3004 annealed UTS ≈180 MPa [R11 p.130].
- **Commercial Al–Mn alloys** [TOT p.299 Table 37]. All contain up to 0.25 Cu and 0.70 Fe, plus "0.3–0.6 %" of an element the extracted text does not name (presumably Si ⚠):

| Alloy | Mn | Mg | Anneal (°C) | O: UTS / YS / El | Worked: UTS / YS / El |
|---|---|---|---|---|---|
| 3003 | 1.0–1.5 | — | 400–600 | 110 / 42 / 35 % | H14: 150 / 145 / 12 % |
| 3004 | 1.0–1.5 | 0.8–1.3 | 415 | 180 / 70 / 22 % | H34: 240 / 200 / 11 % |
| 3105 | 0.2–0.8 | 0.2–0.8 | 345 | 115 / 55 / 24 % | H14: 170 / 150 / 5 % |

  - **Relevance:** 3105 is the registered alloy closest to the lean Mn–Mg slug alloys. T11 (Mn 0.14, Mg 0.26) sits below its Mn range (inference).
- **Constituent strengthening.** In annealed Al–0.05Si–(0.15–1.17)Fe 1xxx alloys, YS rises by **≈ 7 MPa per vol% constituent** (Al₃Fe or Al₆Fe), whatever the temper or intermetallic type [TOT pp.122, 138; Alcoa unpublished data]. Constituents are otherwise said to give no strengthening [TOT p.122].
- Al–Mg–Mn plate: Mn is about twice as effective as Mg per % (≈35 MPa UTS per 1 % Mg) [R10 p.380].

**Quench sensitivity** (critical range 290–400 °C):
- Al₁₂Mg₂Cr is worst, Al₆Mn intermediate, Al₃Zr least [R11 pp.112–113].
- Mn-bearing particles nucleate coarse Mg₂Si needles [R11 p.113 Fig 3.14].
- TOT agrees on the Cr > Mn > Zr ranking [TOT pp.127, 192–194]. It adds that V affects the quench sensitivity of Al–Zn–Mg more than Cr or Mn [TOT pp.193–194].
- In Al–1 % Mg₂Si, the Mn and Cr variants show the largest YS loss between still air (0.65 °C s⁻¹) and cold water (> 1000 °C s⁻¹), because their dispersoids nucleate β″ heterogeneously. Homogenised ingot is less quench sensitive [TOT pp.177–179].
- Fe and Si constituents alone can raise quench sensitivity, and they magnify the effect of dispersoid formers [TOT pp.192, 194].

### 2.3 Dispersoid-free zones (DFZ) from microsegregation

- In Sc-free 7050 (0.13 Zr), a DFZ forms at the **dendrite edges**, where initial Zr is too low for Al₃Zr. These Zr-lean regions recrystallise [R1 pp.1409–1410, 1418].
- Adding 0.1 % Sc fills the edges, because Sc segregates there (k = 0.9), and raises number density everywhere [R1 p.1418].
- **(general knowledge)** In 3xxx the analogue is Mn-lean dendrite centres (k_Mn < 1) and Mn-depleted zones around constituent particles. This needs a 3xxx-specific source.

### 2.4 Design levers

- Fe + Mn total sets the constituent fraction and the primary-phase risk (≤1.7–2.0 %) [R10 p.383]. Fe also controls how much Mn goes into constituent versus solid solution [R8 p.12].
- Si/Mn ratio decides Al₆(Mn,Fe) versus α. More Si gives more α dispersoids and lower Mn in solid solution [R8 pp.32, 37; R10 p.389].
  - TOT confirms the "denser distribution" and the faster Mn precipitation with Si, and puts the Al₆(Mn,Fe)/α switch at about 0.07 % Si [TOT p.160]. *Updated after full-text pass; "finer" was an inference, "denser" is sourced.*
- Heating rate of 50–75 °C h⁻¹ through the nucleation window, an optional isothermal hold, then soak at 450–600 °C [R11 pp.105–106].
- Use electrical conductivity as an in-line metric of Mn precipitation [R10 p.370].

### 2.5 Pitfalls

- Coarse dispersoids or constituents above about 1 µm act as particle-stimulated nucleation (PSN) sites, which promotes recrystallisation [R11 p.42].
- Dispersoids also nucleate microvoids [R11 p.82].
- Dispersoids raise quench sensitivity in heat-treatable alloys (Cr > Mn > Zr) [R11 p.112].
- **Conflict resolved (corrected after full-text pass):** Davis states Mn "decreases resistivity" [R10 p.382]. TOT lists impurities by their effect on conductivity as **Cr, V, Mn, Ti, Mg, Ag, Cu, Zn, Si, Fe, Ni** (Fridlyander). The text calls this an order of "increasingly negative influence", but the next paragraph names Cr, V, Mn and Ti as the most harmful. The list therefore runs from most to least harmful (reading ⚠). TOT names Cr, V, Mn and Ti as the most harmful and limits Cr + V + Mn + Ti to ≤ 0.010–0.015 % in electrical-grade Al [TOT p.52]. Mn in solid solution therefore lowers conductivity. Treat R10's sentence as an error.
- Coarse constituents crack early: 25–50 % of them are cracked after 7 % plastic strain in uniaxial tension [TOT p.122]. Incoherent Mn-bearing dispersoids lower toughness and speed fatigue-crack growth in 7xxx [TOT p.193].

### 2.6 Fe-phase selection in lean Al–Fe–Si(–Mg–Mn) alloys (added after the [TOT] full-text pass)

**Mechanisms and data.**
- **Binary Al–Fe.**
  - Fe above ≈ 0.05 % forms constituents at grain and cell boundaries. The equilibrium phase is monoclinic Al₃Fe, but commercial 1xxx solidification gives metastable Al₆Fe or AlₘFe; Mn also favours Al₆Fe [TOT pp.116–117, 138].
  - Binary ingot preheated 16 h at 607 °C gives Al₃Fe; 16 h at 482 °C gives Al₆Fe [TOT p.138].
- **With Si.** 1xxx sheet contains α-Al₁₂Fe₃Si or β-Al₉Fe₂Si₂ [TOT p.138]. 1350 contains Al₁₂Fe₃Si + Al₆Fe [TOT p.123 Table 6].
- **Growth-velocity selection** [TOT p.139, citing Todd & Jones 1996]:
  - Below a solidification-front velocity of 0.5 mm s⁻¹, Al₃Fe dominates; above it, Al₆Fe dominates.
  - **Si stabilises Al₃Fe against rising velocity, and 0.75 % Mg stabilises it further.** Ce and La suppress Al₃Fe.
  - ⚠ The text says "alloys with 4.6–6.1 wt% Fe", but the cited study is titled "…alloys based on Al-0.5 wt% Fe". The range may be a misprint for 0.46–0.61 wt%. Check the original.
- **Formability.** Coarse Al₃Fe cracks and makes notches, which lowers formability and fatigue resistance. Finely dispersed Al₆Fe does not [TOT p.139].
- **Morphology control.**
  - Small Mn or Cr additions, or Sr, favour Chinese-script α-Al₈Fe₂Si over plate-like β-Al₅FeSi. β creates large misfit strain and, in castings, blocks feeding [TOT p.179].
  - Mn gives α-Al₁₅(Mn,Fe)₃Si₂ [TOT p.179]. Be gives script Al₈BeSiFe₂ [TOT p.180].
  - A high Fe/Mn ratio gives Al₁₃(Fe,Mn)₄ in as-cast 3xxx [TOT p.160].
  - TOT gives no quantitative Mn threshold for the β→α switch.
- **Solute Fe and Si during annealing** [TOT p.140]:
  - Fe in solid solution before the anneal raises the recrystallisation start temperature, through fine Al–Fe precipitation during the anneal.
  - Si that precipitates before or during the anneal as fine Al–Fe–Si or Si particles also delays early recrystallisation. It does so by reducing the deformation zones that can act as nuclei.
  - Conversely, more Fe and Si out of solution as constituents means more PSN-capable particles and finer annealed grains (1xxx).
- **Si in solution** impedes dynamic recovery and raises strain hardening [TOT p.140].
- **Si tied up per unit Fe (derived from the R8 compositions in §2.2):**
  - Si/Fe weight ratio 0.25 in α-Al₈Fe₂Si (7.8/31.6), 0.50 in β-Al₅FeSi (12.8/25.6), 0 in Al₃Fe/Al₆Fe.
  - Si/Mn ratio 0.34 in α-Al₁₅Mn₃Si₂ (8.9/26.3).
  - TOT's "¼(Fe + Mn)" rule [TOT p.171] therefore corresponds to α-type binding (inference).

**Relevance (T11: Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26, Cu 0.04).**
- Ratios (derived): Fe:Si ≈ 1.4, Mn:Fe ≈ 0.27, Fe/Mn ≈ 3.7.
- **Candidate constituents (inference from the data above):**
  - α-AlFeSi (Al₈Fe₂Si/Al₁₂Fe₃Si type, with some Mn).
  - β-Al₅FeSi.
  - Si-free Al₆(Fe,Mn) or Al₁₃(Fe,Mn)₄ in Si-lean interdendritic regions; the high Fe/Mn favours the latter [TOT p.160].
- With only 0.14 % Mn, little Mn is available to tip the balance to script α [TOT p.179].
- T11 contains both Si and Mg, which push toward Al₃Fe rather than Al₆Fe at a given front velocity [TOT p.139]. Whether the rotary caster's front velocity is above or below the ≈ 0.5 mm s⁻¹ switch is unknown (§12).
- **Consequence for strength:** the phase type sets how much Si is left for Mg₂Si, by up to a factor of two (§6.4).
- **Measure:** Fe-phase type, size and morphology at the strip surface and centre, both as cast and after the slug anneal. The Al₆Fe→Al₃Fe and β→α changes are temperature dependent [TOT p.138; R8 p.23].

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
| Al₃Zr (β′) misfit, shape | misfit ≈ 0.6 %; approximately spherical below 0.18 % Zr; coherent or semi-coherent depending on process history; ≈ 20 nm in 7xxx; lattice of the metastable cubic form a = 0.407 nm | [TOT pp.125, 192, 295] |
| Al₃Sc lattice match | a = 0.4104 nm versus 0.404 nm for Al (as printed): "the best match in all known equilibrium phases" | [TOT p.297] |
| Misfit in Al–Mg | Mg raises the Al lattice parameter. Misfit falls to **0.54 %** in Al–6.5Mg, and Al₃Sc stays coherent up to 450 °C for ≤ 10 h | [TOT p.300] |
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
- **Sc + Zr (TOT, Russian work)** [TOT pp.297–298]:
  - Al₃Sc and metastable cubic Al₃Zr precipitate together at **300–400 °C**. This is between the effective windows of binary Al–Sc and Al–Zr, and gives higher strength than either binary.
  - With Zr, Sc can be lowered to 0.15–0.2 %.
  - At 350–450 °C for up to 200 h: **Al₃Zr 5–11 nm** (stays coherent and keeps hardening), **Al₃Sc 25–35 nm** (coarsens, loses coherency, pins dislocations).
  - ⚠ TOT describes separate Al₃Sc and Al₃Zr particles. R1 and R4 describe core–shell Al₃(Sc,Zr) (§3.4). The descriptions differ and are not reconciled here.
- **Al–TM precipitation-hardening window** is 250–450 °C, versus 150–200 °C for conventional ageing of wrought alloys. Only Zr and Sc form coherent or semi-coherent precipitates [TOT p.295].

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
- TOT, same family [TOT pp.163, 300]:
  - 0.3 % Sc more than doubles the YS of Al–5.25Mg, to 365 MPa.
  - Al₃Sc formed at 300–350 °C raises the recrystallisation start by 50–175 °C. In Al–6.5Mg–0.2Sc, recrystallisation starts at ≈ 400 °C and "never finishes up to the liquidus".
  - 1570 (5–6 Mg + Sc, Zr, Mn), annealed 320 °C/1 h: UTS 380–440 MPa, YS 250–340 MPa, El 16–20 %. That is ≈ 100 MPa above Sc-free Al–Mg.
  - 1570 hot-rolled + annealed structure: unrecrystallised grains 150 × 50 × 20 µm, subgrains 5 µm, Al₆Mn 0.4 µm at grain boundaries, Al₃Sc/Al₃Zr < 20 nm inside subgrains.
  - Ingot anneal before deformation: 250–350 °C. The stated precipitate size there, "40–300 nm", conflicts with the < 20 nm given for the final product ⚠.
- **Hardening per unit solute** [TOT p.298 Table 36]: 0.5 % Sc (0.12 at%, 0.48 vol%) gives ΔYS_max = 120 MPa, i.e. **≈ 1000 MPa per at%**. Conventional ageing systems give 48–191 MPa per at%; 6061-type 1Mg–0.6Si–0.25Cu gives 140 MPa, 79 MPa per at%.

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
- **Conflicting claims:** Polmear says recrystallisation is inhibited "as high as 600 °C" [R11 p.52]; R2 measured recrystallisation at 575–600 °C for 0.19Sc–0.05Zr. TOT says Al₃Sc raises the recrystallisation temperature "to above 600 °C" (7xxx context) [TOT p.194]. That sides with Polmear but gives no braze-cycle data, so the conflict stands.
- In Al–Mg–Sc, maximum strength comes from annealing *before* deformation. This makes working harder, and intermediate anneals cost strength [TOT p.301].

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
| E4 | dr/dt = (D_Sc/r)(c̄_Sc − c^α_Sc(r))/(c^β_Sc − c^α_Sc(r)) = (D_Zr/r)(c̄_Zr − c^α_Zr(r))/(c^β_Zr − c^α_Zr(r)) | ternary flux-balance tie-line, solved by Newton–Raphson for each size class; negative values give dissolution | [R1 p.1413 Eq 4] |
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

**Nucleation-site and competition rules for multi-phase models** [TOT pp.128–129, 265, 270–272]:
- Coherent phases nucleate homogeneously unless they create large strains. If the zone or new phase has a larger specific volume than the matrix, it nucleates on vacancy clusters. Semi-coherent phases nucleate on dislocations; incoherent ones on grain boundaries [TOT p.272; Table 7 p.270].
- The interfacial energy of coherent θ″ is about one third that of semi-coherent θ′ [TOT p.271]. This is why metastable sequences win nucleation (§6).
- When several phases compete, the one with the simpler structure, formed by the faster-diffusing elements, wins. The precipitation sequence then sets the solid-solution depletion and hence the final phase mix [TOT p.265]. This explains β″ forming instead of the equilibrium Q phase in Al–Cu–Mg–Si [TOT p.283].
- Vacancy-aided nucleation comes closest to homogeneous nucleation [TOT p.128]. Slow quenching lowers T_v, the highest temperature at which homogeneous nucleation is possible. A low-temperature pre-age below T_v can then restore a fine distribution [TOT p.128].
- Early-stage resistivity rises in two steps: a "rapid reaction" over minutes, then a slow one. The first step is read as solute segregation, possibly spinodal (Al–Zn, Al–Zn–Mg). Zones may act as a vacancy "pump", which keeps diffusion above its equilibrium rate [TOT pp.270–271].

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
  - Zr at 0.1–0.3 % inhibits recovery and recrystallisation [R10 p.387].
  - V raises the recrystallisation temperature [R10 p.385].
  - 0.2 % Ca alters recrystallisation in 3003 [R10 p.372].
  - Yb + Cr + Zr strongly raise recrystallisation resistance in Al–Zn–Mg–Cu [R7 p.6].
- **Recrystallisation-temperature increments from TM additions (Yelagin)** [TOT p.296 Table 35]. Binary alloys were cast, annealed at 500 °C, hot rolled at 420–450 °C, annealed at 450 °C and cold rolled. C is the concentration giving the maximum increment:

| Element | Atomic radius (nm) | C (at%) | Δ onset (K) | Δ finish (K) |
|---|---|---|---|---|
| Sc | 0.16 | 0.20 | +120 | +320 |
| Zr | 0.16 | 0.09 | +105 | +240 |
| Mo | 0.14 | 0.12 | +70 | +45 |
| **Fe** | 0.137 | **0.04** | **+65** | +35 |
| Cr | 0.128 | 0.35 | +45 | +30 |
| Nb | 0.147 | 0.12 | +35 | +35 |
| Mn | 0.131 | 0.77 | +30 | +25 |
| V | 0.136 | 0.21 | +15 | +15 |
| Ti | 0.145 | 0.25 | +5 | +180 |
| Ni | 0.124 | 0.04 | −10 | +5 |

  - **Period IV** TMs (Sc … Ni) raise the recrystallisation temperature only above a threshold concentration close to their solubility at the solution-treatment temperature. **Period V** TMs (Zr, Nb, Mo) raise it even at very small additions. Some TMs show a maximum that correlates with their solubility limit [TOT p.296].
  - An effective anti-recrystallisation TM has an incomplete 3d shell with few electrons, a large atomic-radius mismatch with Al, forms a supersaturated solution on solidification, and decomposes into thermally stable fine dispersoids [TOT p.296].
  - (derived) 0.04 at% Fe ≈ 0.08 wt%, above the 0.05 wt% equilibrium limit. The Fe effect is therefore a supersaturation-plus-precipitation effect, in line with [TOT p.140].
- **Relevance (rotary-cast, unhomogenised slug strip):**
  - Fe retained in solution by fast casting and by the post-hot-mill quench should raise the slug's recrystallisation onset. So should Mn, but much less per at% (inference from Table 35 and [TOT p.140]).
  - Strip-to-strip variation in Fe supersaturation is therefore a candidate cause of anneal-response scatter. Conductivity of the cold-rolled strip is the proxy (inference; §12).
- Dispersoids below about 0.4 µm pin subgrain boundaries [TOT p.125]. Constituents are PSN sites [TOT p.122]. The particle size able to nucleate recrystallisation falls as deformation temperature falls and strain rate rises [TOT p.130].
- **Lever:** maximise F_V/r, i.e. many fine particles, homogeneously distributed. Avoid >1 µm particles, which act as PSN sites [R11 p.42].

---

## 6. Clusters, natural ageing and precipitation sequences

### 6.1 Sequences

| System | Sequence | Source |
|---|---|---|
| Al–Cu | SSSS → GP (single Cu layers on {100}) → θ″ (GP2) → θ′ (Al₂Cu, tetragonal a 0.404 / c 0.580 nm, semi-coherent, on dislocations) → θ (bct a 0.607 / c 0.487 nm) | [R5 p.10; R11 p.57 Table 2.3; R4 p.37] |
| Al–Cu–Mg | SSSS → Cu–Mg co-clusters → GPB (rods ⟨100⟩) → S′ → S (Al₂CuMg; S′ a 0.404, b 0.925, c 0.718 nm) | [R11 p.58; R3 p.16; R5 pp.12–13] |
| Al–Mg–Si | SSSS → Mg and Si clusters → Mg–Si co-clusters → GP → β″ (monoclinic a 1.534, b 0.405, c 0.683 nm, β 106°, ~MgSi) → β′ (hex, ~Mg₁.₇Si) / B′ (high Si:Mg) → β (Mg₂Si fcc a 0.639 nm) | [R11 pp.58–59, 63–66; R3 p.17] |
| Al–Mg–Si (TOT) | SSSS → independent Mg and Si clusters, Mg–Si co-clusters → GP zones → "Si-rich phase" → β″ → β′ → β (Mg₂Si; a 0.639 or 0.6351 nm). The Mg:Si ratio rises along GPZ → β″ → β′ → β, so the metastable phases are Si-enriched. ⚠ TOT's β″ lattice entries (a = b = 0.616, c = 0.710 nm, γ = 82°; or 0.77/0.67/0.203 nm, γ = 75°) are older structure models and differ from R11's | [TOT pp.173, 278–279 Table 17] |
| Al–Si | Si clusters → diamond-cubic Si directly, with no intermediate phase. Coherency is lost below ≈ 2 nm, so there is no useful hardening | [TOT pp.168, 280] |
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
  - It is attributed to about 10¹⁹ cm⁻³ Cu–Mg clusters [R11 pp.64–65].
  - Strengthening scales with the number density of Cu–Mg co-clusters. Cu–Cu and Mg–Mg clusters do not correlate with hardness. Vacancy–Mg–Cu complexes are proposed [R5 p.12].
- **Natural-ageing data** (Al–1.1Cu–1.7Mg; Al–1.5Cu–3.5Li ± 0.45Mg at.%, i.e. 2.5Cu–1.5Mg and 3.5Cu–0.9Li ± 0.4Mg wt%; homogenised 500 °C/24 h, hot rolled at ≥ 350 °C, solution treated 500–505 °C 30 min, water quenched at 20 °C) [R5 pp.30–31, 47, 68, 71–73]. *Citations corrected after the full-text pass (previously "pp.29–31").*
  - Most change happens in the first 24 h; hardening saturates after about 10 h; 72 h is stable up to 6 months [R5 pp.30–31, 71]. DSC shows clustering approaching completion after 16 h [R5 p.82].
  - HV goes from 74 → 117 (Al–Cu–Mg, +55 %), 64 → 77 (Al–Cu–Li, +20 %) and 64 → 115 (Al–Cu–Li–Mg, +82 %) [R5 pp.71–72]. The 0.4 at% Mg addition does not change the as-quenched hardness [R5 p.71].
  - **Mg turns on Cu clustering, with no threshold.** *Corrected after the full-text pass:* the earlier "0.4 at% Mg" was only the alloy level. A diffusion couple with 0–0.33 at% Mg shows naturally aged hardness, cluster scattering and Mg content following the same profile, and an as-quenched DSC clustering exotherm already at 0.09 at% Mg [R5 pp.109, 112–113] (§6.5).
  - Cluster Mg/Cu: 0.70 → 1.82 (Al–Cu–Mg, as-quenched → naturally aged); 0.13 → 0.42 (Al–Cu–Li–Mg) [R5 p.56 Table 6]. ⚠ The Ch. 5 text gives 0.48 for naturally aged Al–Cu–Li–Mg (38.9 Cu and 9.0 Mg excess per nm³) [R5 p.78] against Table 6's 0.42 (7.1 Mg). This is an internal inconsistency in R5.
  - Correlations vanish beyond about 2 nm (atom probe) [R5 p.54]. Li stays random [R5 pp.54, 129].
  - Small-angle scattering correlation length ξ ≈ 2.2–5.2 Å; inter-cluster periodicity λ ≈ 36–72 Å [R5 p.56 Table 6]. Cluster size stays below 1 nm in all three alloys [R5 p.94].
  - DSC at 10 °C min⁻¹ (Al–Cu–Mg): cluster formation exotherm 50–125 °C; dissolution endotherm 150–260 °C (double minimum). The exotherm area halves within 1 h of natural ageing and keeps falling for 6 h. The endotherm area does not change with ageing time, so the same solute ends up in clusters whether they form at room temperature or during the scan [R5 p.72].
  - Reversion: Cu-rich clusters dissolve at lower temperature (≤ 200 °C) than Cu–Mg clusters (≈ 250 °C). Reverting the Mg-bearing clusters at 250 °C recreates a solid solution that clusters as fast as one quenched from 500 °C. Mg is linked to the retained excess vacancies [R5 pp.5–6, 96–103]. *Now read in full; details in §6.5.*
- **Al–Mg–Si negative natural-ageing effect (quantified).**
  - A 24 h room-temperature delay before ageing at about 170 °C reduces tensile properties by **up to 10 %** in alloys with >1 % Mg₂Si.
  - The same delay **improves** properties in alloys with <0.9 % Mg₂Si.
  - Mechanism: clusters and vacancies, and a GP solvus above 170 °C in the richer alloys, give coarser β″.
  - 0.25 % Cu lessens the effect [R11 pp.141–142].
  - Si-rich room-temperature clusters lock up solute. Industrial pre-ageing (≈ 80 °C) makes Mg–Si clusters dominant. Sn traps vacancies and retards Si clustering by orders of magnitude [R5 pp.9–10, 15–16, 45, 89]. *Pages corrected and the pre-ageing temperature added after the full-text pass;* the other Al–Mg–Si statements in R5 are collected in §6.5.
  - TOT gives the same split but in **at% Mg₂Si**: below 0.9 at%, the delay refines the aged structure, because the clusters act as nuclei; above 1.1 at%, it coarsens the structure [TOT pp.175–176, citing Baba & Takashima 1969]. ⚠ R11 uses wt% (0.9 / 1 %) for the same thresholds. The unit is unresolved; Ch. 5 uses "Mg₂Si < 0.8 %" with no unit [TOT p.279]. Details in §6.4.
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
- **Cold work before ageing** adds heterogeneous nucleation sites (T8; T₁ in Al–Cu–Li) [R11 p.46; R5 p.9]. Dislocations act through solute segregation, which atom probe shows along dislocations after heating to the ageing temperature; the segregation speeds up precipitation [R5 pp.9, 14].
- **Activation energies** for cluster formation or dissolution are **not given** in the sources read, including [TOT] and [R5] (see §12). R5 gives only solute diffusion D₀/Q for Cu, Mg and Li (§1.4) and a vacancy formation enthalpy of 0.75 eV [R5 pp.103, 121]. Sc raises the apparent activation energy of δ′ precipitation (DSC; no value given) [R4 p.38]. TOT gives only temperature windows and stage times (§6.4).
- **Quench-retained vacancies** form prismatic loops in dilute alloys and helicoids in concentrated ones. Elements with high vacancy binding (Li, Si) hinder loop formation [TOT pp.87, 269]. Loop densities reach ≈ 10¹⁵ cm⁻³ [TOT p.87].
- **GP-zone data (Al–Cu)** [TOT pp.141, 272–273]:
  - Natural-ageing GP zones: 10¹⁷–10¹⁸ cm⁻³, up to 5 nm, spacing 2.5–4 nm. θ″: 10–100 nm. θ′: 10–60 nm at 10¹¹–10¹² cm⁻³.
  - GP zones in Al–Cu redissolve above ≈ 190 °C.
  - Mn, Zr and Ti dispersoids nucleate relatively large θ′ and so reduce the ageing effect [TOT p.273].
- **Cu–Mg clusters (Al–Cu–Mg):** the first hardening stage gives ≈ 70 % of the total strength [TOT p.275], in line with R11's 60–70 %.

### 6.3 Interactions with Sc

Sc has little or no effect on the kinetics of θ′, β″ or η′. θ′ nucleates on Al₃Sc [R4 p.37]. δ′ becomes finer and forms shells on Al₃Sc [R4 p.38]. In 6060 + Zr, adding Sc raises T1 YS from 81 to 182 MPa (dispersoid and grain effect) [R3 p.16]. TOT: Zr in solution slows δ′ coarsening 10× at 250 °C [TOT p.157], and Al₃Zr/Al₃Sc act as substrates for δ′, forming composite core–shell particles [TOT pp.292, 298].

### 6.4 Al–Mg–Si precipitation and natural ageing in lean alloys (added after the [TOT] full-text pass)

**Clustering and zones.**
- Mg clusters are present as quenched (Al–0.65Mg–0.72Si). Si clusters form extremely fast, within the first minute of ageing at 200 °C [TOT p.174]. DSC places Mg/Si segregation below 100 °C [TOT p.280]. The solid solution decomposes even at room temperature [TOT p.278].
- GP zones [TOT p.174]:
  - Plates "one atomic layer, i.e. 2.5 nm" thick (⚠ internally inconsistent as printed) and ≈ 30 nm long.
  - Mg:Si = 1, with alternating Mg and Si columns along ⟨100⟩. Only partially coherent.
  - Stable up to ≈ 260 °C.
- β″ [TOT pp.174–175]:
  - Coherent ⟨100⟩ needles. Composition printed as "Si:Al:Mg = 6:3:1" ⚠.
  - GP → β″ proceeds without GP-zone dissolution (DSC on 6061).
  - GP zones and β″ are sheared, which localises slip. β′ is bypassed by Orowan looping. Equilibrium β adds little strength.

**Stage times and temperature regimes (6xxx).**
- Stage times [TOT p.279]:
  - The zone stage lasts **5 h at 150 °C and 8 min at 200 °C**.
  - The transition to β′ takes **200 h at 150 °C and 8 h at 200 °C**.
  - Zone density is 3×10¹⁵ mm⁻³, zone size "6 × 20–100 nm". β″ has the same density and size "5 × 16–200 nm" (as printed).
- Above 300 °C, β′ forms directly. Above 400 °C, only equilibrium β forms. At 300–350 °C, β′ and β coexist for long times [TOT pp.278–279].
- DSC windows in Al–Mg₂Si–Si [TOT p.280]:
  - segregates < 100 °C;
  - needle zones 200–250 °C;
  - free Si 240–320 °C;
  - β″ and β′ "below 450 °C";
  - β above 400 °C.
- Free Si precipitation is complete in 17 h at 150 °C and in 30 min at 250 °C, without hardening [TOT p.280].

**Excess Si.**
- Excess Si lowers Mg₂Si solubility, speeds precipitation and raises GP-zone density [TOT p.174].
- Peak strength comes with excess Si at the β″ stage. Si–vacancy complexes are proposed as the nuclei [TOT p.278].
- β′ has Mg:Si = 1.21 in Si-excess alloys versus 1.75 in balanced alloys (atomic ratio, as printed) [TOT p.280]. Metastable precursors have Mg:Si nearer 1:1 than 1.73 [TOT p.184].

**Delay between quench and ageing ("natural ageing").**
- Below **0.9 at% Mg₂Si**, ageing straight after the quench precipitates heterogeneously on dislocations. A delay refines the final structure, because the clusters act as nuclei [TOT pp.175–176].
- Above **1.1 at%**, the delay forms many clusters < 10 Å that grow poorly, giving a coarser structure [TOT p.176].
- In dilute alloys (Mg₂Si < 0.8 %), β″ nucleates on zones, and prior natural ageing gives very fine, uniform β″ [TOT p.279].
- **T_v (°C) = 111 + 71·(wt% Mg₂Si)** is the critical temperature above which GP zones do not form [TOT p.177 Eq 28].
- Modifiers of the delay effect:
  - 0.25 % Cu reduces it.
  - Cu, Ag, Be, Cd and Zn raised the natural-ageing hardness during the delay [TOT p.177].
  - Cd, In and Pb help only for ageing below 160–170 °C [TOT p.280].
- Ways to remove the penalty [TOT p.177]:
  - A short pre-age above the ageing temperature dissolves the delay zones.
  - In Al–1.2Mg₂Si, 0.5 h at 160 °C straight after the quench, then storage, then 16 h at 160 °C removes the penalty.
- Below 80 °C the reaction switches from fast to slow as vacancies are trapped at zones. Zone growth needs > 120 °C [TOT p.179].

**Other elements.**
- Mn (and Cr, Zr, V, Fe) bind Si ("Al₁₀Mn₂Si", as printed). This lowers the ageing response and coarsens the precipitates, but it also reduces the delay penalty, especially at slow quench rates (15 °C min⁻¹) [TOT p.177].
- 0.1 % Be raises the hardening rate and peak of Al–0.75Mg–0.5Si; 0.2 % Ca does the opposite [TOT p.180]. Sb, Pb and Sn bind Mg as Mg₂X [TOT p.280].
- Deformation before ageing changes 6xxx properties only slightly. It speeds ageing and lowers precipitation temperatures, more so with excess Si, because Si nucleates on dislocations [TOT p.180].
- Cu (< 2 %) speeds β″ and refines it about 3× [TOT p.279]. Below ≈ 0.2–0.5 % Cu, Al–Mg–Si–Cu stays in the Q-free "tetrahedron III" field [TOT p.183].

**Relevance: T11 Mg₂Si budget, solvus and natural ageing (derived/inference).**
- Si needed to bind 0.26 Mg as Mg₂Si: 0.26/1.73 = **0.150 %** (derived).
- **Si available depends on the Fe phase** (§2.6):
  - **TOT rule** (≈ α-type binding): 0.38 − ¼(0.52 + 0.14) = **0.215 %**. That is ≈ 0.065 % excess Si and **Mg₂Si ≈ 1.578 × 0.26 = 0.41 %** (derived).
  - **β-Al₅FeSi** (Si/Fe 0.5), with Mn in α (Si/Mn 0.34) or in Al₆(Fe,Mn): 0.07–0.12 % Si left. Si then limits Mg₂Si to ≈ 2.73 × Si_avail = **0.20–0.33 %**, leaving 0.05–0.14 % Mg in solution (derived).
  - **Si-free Al₃Fe/Al₆Fe**: almost all 0.38 % Si stays free, which is strongly Si-excess (derived).
  - The Fe-phase selection therefore changes the Mg₂Si potential by about 2× and moves T11 between Si-excess and Mg-excess chemistry (inference).
- **Solvus.** TOT gives only the quasi-binary eutectic (595 °C, 1.85 %). The dissolution temperature of 0.2–0.4 % Mg₂Si is not in any source read (§12).
  - TOT's regimes (β′ directly above 300 °C, β alone above 400 °C [TOT p.278]) imply that Mg₂Si forming during the ≈ 500 → 380 °C in-line hot rolling would be coarse β′/β on dislocations, not hardening β″ (inference). The water quench retains the rest (inference).
- **Natural ageing.** At 0.2–0.4 % Mg₂Si, T11 is below the 0.8–0.9 % thresholds whatever the unit.
  - By TOT, storage before a later heat treatment is neutral or beneficial: it gives finer β″ later [TOT pp.175–176, 279] (inference).
  - Hardness still drifts during storage through clustering, so record slug HB against age (T11 measurement plan).
  - [R5] adds the vacancy control and the time scale of this drift; see the T11 notes in §6.5.
- **Bake 220 °C/10 min.** T_v = 111 + 71 × (0.20–0.41) ≈ **125–140 °C** (derived). The bake is above T_v, so no new homogeneous GP zones nucleate.
  - Any bake hardening must come from growth of clusters or zones formed beforehand, or from precipitation on the dense dislocation structure of the extruded wall (inference).
  - 10 min at 220 °C is of the order of the 8 min zone stage at 200 °C and far short of the 8 h β′ transition [TOT p.279]. The wall should therefore be in the zone/β″ stage, not overaged (inference, extrapolated from 6xxx).
  - ⚠ *Added after the [R5] pass:* in Al–Cu–(Li,Mg), natural-ageing clusters **dissolve** at 200–250 °C within seconds to a minute [R5 pp.95–96]. Whether T11's storage clusters "grow" into β″ at 220 °C (as above) or first revert is therefore open (§6.5).
- **Quench sensitivity.** T11 has little Mn, so it should be little quench sensitive from dispersoids (inference from [TOT pp.177–179]).

### 6.5 Cluster kinetics, vacancies and reversion: what transfers from Ivanov's thesis (added after the [R5] full-text pass, 2026-10-12)

**Transfer caveat.** R5's alloys contain 1.1–1.5 at% Cu plus 0.45–1.7 at% Mg (or 3.5 at% Li), and the clustering partners are Cu and Mg [R5 pp.30, 47]. T11 has ≈ 0.29 at% Mg (derived), ≈ 0.1–0.2 wt% free Si (§6.4) and no Cu. **The mechanisms (vacancy control, reversion) and the measurement methods transfer; R5's times, temperatures and hardness increments do not transfer as numbers.**

**Kinetics and the role of vacancies.**
- Natural ageing is vacancy-aided solute diffusion in a quenched supersaturated solution that also holds an above-equilibrium vacancy concentration [R5 pp.3, 7].
- Some Cu-rich clusters already exist as quenched, i.e. they form during the quench. R5 attributes this to the low Cu solubility [R5 pp.55, 77, 129]. Positron (coincidence Doppler broadening) and atom-probe work in the literature shows solutes and vacancies clustering during the quench [R5 p.14].
- **Time scales** after a water quench from 500 °C [R5 pp.78, 83]:
  - Al–Cu–Mg: excess Cu in clusters is ≈ 10 nm⁻³ from the start. Mg joins during the first hour and then exceeds Cu.
  - Al–Cu–Li–Mg: the excess Cu rises from 10.7 to 15.6 nm⁻³ in the first hour and reaches 38.9 nm⁻³ when naturally aged. Mg joins only after ≈ 2 h and passes the alloy Mg/Cu ratio after ≈ 8 h.
  - In both, clusters form Cu-rich first and become Cu–Mg-rich later [R5 pp.123, 129].
- **Mg acts as a catalyst.**
  - Without Mg (Al–Cu–Li), the few as-quenched Cu clusters do not evolve; hardness rises by only 20 % and the scattering hardly changes [R5 pp.71, 77].
  - Adding 0.45 at% Mg makes Cu cluster about as fast as in Al–Cu–Mg with 1.7 at% Mg, and the hardening rates are comparable [R5 pp.82, 84].
  - In the 0–0.33 at% Mg diffusion couple, clustering is proportionally faster with more Mg, and there is no threshold [R5 pp.109, 114–115].
  - R5 concludes that Mg raises the concentration and/or mobility of vacancies available for diffusion [R5 pp.84, 103].
- **Proposed mechanism (a hypothesis in R5).**
  - First-principles solute–vacancy binding energies are ≈ +0.02 eV for Cu and ≈ −0.02 eV for Mg, against 0.25 eV for Sn [R5 p.122]. Both are too small for Sn-type trapping.
  - R5 suggests that vacancies linger near Cu atoms, where their exchanges are correlated and "useless". The weakly repulsive Mg–vacancy pair instead makes uncorrelated, "useful" exchanges and sweeps up solute [R5 p.123].
  - Mg diffuses faster than Cu in every data set (§1.4), yet Cu clusters first. R5 leaves this paradox unresolved [R5 pp.121, 124].
- **Vacancy loss.**
  - After 72 h of natural ageing and a reversion at 200 °C, the released solute does not cluster again within 20 days (Al–Cu–Li, Al–Cu–Mg) or 3 days (Al–Cu–Li–Mg) [R5 pp.97–99, 102].
  - The quenched-in vacancies have therefore been annihilated during natural ageing or trapped at sites that are stable to 200 °C [R5 p.102].
- **Re-activation.**
  - Reversion at 250 °C for 30 s also dissolves the Mg-bearing clusters. It restores as-quenched clustering kinetics: the hardness rises again as fast as, or slightly faster than, in the first natural ageing [R5 pp.100–101, 103].
  - For a vacancy formation enthalpy of 0.75 eV, the equilibrium vacancy concentration at 250 °C is only ≈ 6× that at 200 °C. That is too small to explain the ≈ 100× difference in post-reversion kinetics.
  - R5 concludes that Mg released into solution re-activates the vacancies, with some help from the higher equilibrium vacancy content [R5 p.103].
- **Quench rate was not varied in R5.** There are only two hints:
  - The lower excess Cu after reversion than after the solution quench "might be attributed to" the different quench conditions [R5 p.99].
  - Part of the quenched-in vacancies may be lost to defects during the solution quench [R5 p.103].
  - Quench-rate effects for 6xxx are in [TOT p.177] (§6.4).
- **Vacancy traps ("trap and release").** Sn's high vacancy binding and suitable solubility cut the free vacancies after the quench and delay Si clustering in Al–Mg–Si by orders of magnitude, while still allowing precipitation at higher temperature [R5 pp.10, 45, 89, 122].

**Thermal stability and reversion.** Ramps are DSC and in-situ SAXS at 10 °C min⁻¹ on 72 h naturally aged material; isothermal reversions were done in an oil bath.

| Alloy | Clusters stable to | Dissolution events | Isothermal reversion | Source |
|---|---|---|---|---|
| Al–Cu–Li | ≈ 110 °C by SAXS (the Fig. 34 caption says 140 °C ⚠) | broad DSC minimum at 130 °C, complete by 200 °C; SAXS minimum by 180 °C | 200 °C: no effect after 5 s, complete after 60 s | [R5 pp.92, 94–95] |
| Al–Cu–Mg | ≈ 200 °C by SAXS | DSC minima at 200 °C (Cu-rich) and 240 °C (Cu–Mg); SAXS minimum at 270 °C | 200–235 °C removes only the 200 °C event. After 60 s at 200 °C the excess Cu falls by 25 % and Mg by 40 %. At 240 °C, 30 s turns the clusters into precipitates | [R5 pp.92, 94–95, 98] |
| Al–Cu–Li–Mg | ≈ 60 °C by DSC, ≈ 130 °C by SAXS | DSC events at 105 °C (ascribed to Li short-range order), 165 °C and 220 °C; all clusters gone by ≈ 250 °C | 120 °C/60 s removes the 105 °C event; 200 °C/60 s removes the 165–170 °C event; 250 °C/30 s also dissolves the Mg-rich clusters | [R5 pp.93–96] |

- **Dissolution and precipitation overlap.** In Al–Cu–Mg there is no zero-heat-flow gap between the cluster endotherms and the precipitation exotherm [R5 p.92].
- The 240 °C/30 s change in Al–Cu–Mg is too fast for long-range diffusion. R5 ascribes it to short-range rearrangement of solute from clusters into precipitates [R5 p.95].
- **Hardness after reversion (Al–Cu–Li–Mg)** [R5 pp.100–101]:
  - 60 s at 200 °C causes "a loss of more than 60 % of the hardness from that of the naturally aged condition". ⚠ Taken literally, this would fall below the 64 HV as-quenched value; it presumably means 60 % of the natural-ageing gain.
  - Hardness recovers only after more than 100 h.
  - After 250 °C/30 s, hardness falls slightly further, then re-hardens as fast as after the solution quench.
  - A slightly lower post-reversion hardness may come from a few larger precipitates formed on dislocations during reversion.
- **Effect of Mg content on stability.** More Mg gives more thermally stable clusters [R5 p.83]. In the diffusion couple, a second dissolution peak at 215 °C appears above 0.21 at% Mg. The precipitation peak moves to lower temperature, with a step near 0.18 at% Mg [R5 p.113].

**Strengthening from clusters.**
- **Hardness tracks the amount of clustering.** Across the 0–0.33 at% Mg gradient, naturally aged hardness rises from 90 ± 3 to 123 ± 2 HV (25 gf). Over the same gradient, the cluster scattering rises from 23 to 48 excess electrons per nm³ [R5 p.112].
  - ⚠ The Mg-free end (90 HV) does not match the 77 HV of Ch. 5. The indentation load (25 vs 200 gf) and the material history differ.
- Literature cited in R5:
  - In Al–Cu–Mg, strengthening scales with the number density of Cu–Mg co-clusters [R5 p.12].
  - Natural-ageing hardening has been explained by modulus hardening [R5 p.13].
- **Cu-rich clusters harden as much but give little DSC heat.** Al–Cu–Li–Mg (mostly Cu-rich clusters) and Al–Cu–Mg (Cu–Mg clusters) reach similar hardness, but the DSC signal follows the Mg content [R5 pp.83–84]. **DSC heat is therefore not a proxy for cluster strengthening.**
- **R5 gives no quantitative cluster-strengthening law.** The co-cluster models it cites are not in the Drive (§12): Starink & Wang 2009 for Al–Cu–Mg [R5 p.126 ref. 7] and Starink, Cao & Rometsch 2012 for Al–Mg–Si [R5 p.117 ref. 16].

**Al–Mg–Si statements in R5.** These come from the literature review and chapter introductions, not from R5's own data.
- 6xxx alloys combine medium strength, good formability and high toughness, and can be strengthened after shaping (bake hardening) [R5 p.7].
- Room-temperature clustering in Al–Mg–Si lowers formability and slows later precipitation [R5 pp.15, 45, 67].
- Si-rich clusters lock up solute that cannot evolve continuously into precipitates, unlike in Al–Cu [R5 pp.9, 15].
- Several cluster types coexist in naturally aged Al–Mg–Si [R5 p.89].
- **Countermeasures** [R5 pp.9–10, 15–16, 89]:
  - pre-ageing at ≈ 80 °C, so that Si–Mg clusters form instead of Si-rich ones;
  - complex ageing sequences, which have been adopted industrially;
  - Sn as a vacancy trap.
  - One pre-ageing reference is on a **twin-roll cast** Al–Mg–Si alloy (Birol, Mater. Sci. Eng. A 391 (2005) 175–180) [R5 p.105 ref. 14]. It is not in the Drive.
- ⚠ **A difference of scope, not a contradiction.** R5's "negative" natural-ageing effect is a general 6xxx statement with no composition dependence. TOT and R11 find the delay neutral or beneficial below ≈ 0.8–0.9 % Mg₂Si (§6.2, §6.4).
  - For T11's ≈ 0.2–0.4 % Mg₂Si, the composition-specific TOT/R11 statements should take precedence for the bake response (inference).
  - R5's formability point still bears on slugs stored before extrusion (inference).

**Relevance to T11** (inference; the transfer from Al–Cu–(Li,Mg) is qualitative only).
- **Natural-ageing drift of slugs.**
  - The drift needs excess vacancies, and these come from the **last fast cooling** before storage. At room temperature, equilibrium vacancies move Mg less than one atomic spacing in 30 days (§1.4, derived).
    - A slug cooled slowly from the anneal should therefore drift little; one cooled fast from a high temperature may drift (inference).
    - This is the vacancy-side reason behind T11 risk 2b, and it complements the solute-side reason (Mg₂Si precipitated by slow cooling) in risk 2a.
  - For E_f = 0.75 eV, the equilibrium vacancy fraction at 380 °C is ≈ 8× lower than at 500 °C (derived). The hot band quenched from ≈ 380 °C therefore holds fewer quenched-in vacancies than a solution-quenched sheet, but the slug anneal resets this (inference).
  - It is not known whether Mg's catalytic role carries over to Al–Mg–Si; R5 does not show it. If it does, 0.26 % Mg (≈ 0.29 at%) lies inside the 0–0.45 at% range in which R5 saw clustering switch on without a threshold (inference).
  - If vacancies are retained, expect most of the change within 24 h and a plateau within ≈ 3 days, by analogy (inference).
    - The slug HB plan (day 0, 1, 7, 30) should add points at ≈ 2–6 h and 3 days.
    - "Day 0" should mean tested within minutes or held cold. R5 tested within 2–5 min, or stored samples at −52 °C or in liquid nitrogen [R5 pp.30, 47, 68].
  - A DSC comparison of fresh and stored slugs would show a shrinking low-temperature formation exotherm if clustering occurs (method in §6.6). The Al–Mg–Si peak temperatures will differ from R5's.
- **Bake at 220 °C/10 min on the extruded wall.**
  - 220 °C lies between R5's 200 °C, where Cu-rich clusters revert in ≤ 60 s, and 250 °C, where the Mg-bearing clusters revert in 30 s [R5 pp.95–96]. It is also above T11's GP-zone critical temperature T_v ≈ 125–140 °C (§6.4). Clusters formed while slugs or cans are stored should therefore not survive the bake as clusters (inference).
  - ⚠ **Open question.** R5's clusters revert, whereas TOT reports GP → β″ in 6061 without zone dissolution, and β″ nucleating on zones in dilute alloys [TOT pp.174–175, 279]. These sources cannot settle whether T11's storage clusters dissolve (softening) or seed β″ (hardening) at 220 °C. R5 adds that reversion and precipitation overlap in this temperature range [R5 pp.92, 95].
  - **Precipitation on the wall's dislocations is kinetically possible (derived).** At 220 °C, Mg diffuses ≈ 30–40 nm in 10 min with equilibrium vacancies alone (§1.4). R11 gives D_Si ≈ D_Mg at 500 °C [R11 p.105]. Both distances exceed the ≈ 10 nm dislocation spacing at 10¹² cm⁻², the cold-worked density [R11 pp.36, 41] (derived).
    - Solute segregation to dislocations during the bake is therefore kinetically possible (inference; mechanism from [R5 pp.9, 14]).
    - Whether it outruns recovery softening must be measured: HV of the wall simulation before and after 220 °C/10 min (T11 plan).
  - **The can wall may age again after the bake (inference).** In R5, reversion at 200 °C left no mobile vacancies, but reversion at 250 °C restored as-quenched kinetics [R5 pp.102–103]. 220 °C lies between the two. Measure wall HV 1 day and 30 days after the bake.

### 6.6 Characterising clusters: what each method measures (from [R5], 2026-10-12)

| Method | What it measures | Limits | R5 practice | Use for T11 (inference) |
|---|---|---|---|---|
| Micro-hardness | Net strengthening from clusters, the most direct link to properties | No chemistry or size information | Vickers 200 gf, 10 s, ≥ 10 indents; 25 gf every 500 µm on the diffusion couple; as-quenched samples tested within 5 min [R5 pp.32, 68, 111] | Primary metric: slug HB/HV against storage time |
| Electrical resistivity / conductivity | Global, indirect evidence of clustering; resistivity, like hardness, can fall during heating before any precipitate forms [R5 pp.10, 16] | Not specific to one solute | Not used experimentally in R5 | Cheap in-line companion to HB (already in the T11 plan) |
| DSC | Heat of cluster formation (exotherm) and dissolution (endotherms). The exotherm area falls with storage time (progress of natural ageing); endotherm temperatures give thermal stability [R5 pp.72, 92] | The signal is dominated by strong bonds (Cu–Mg); Cu-rich clusters give little heat yet harden [R5 pp.83–84]. Baseline artefacts from heat capacity and sample position [R5 pp.34–35] | TA Q200 from −50 °C, so that clustering above 0 °C is captured; 10 °C min⁻¹. **Two-heat baseline:** ramp to 350 °C, cool at 50 °C min⁻¹, then a second ramp as the sample's own baseline (valid to ≈ 250 °C). Full-range scans 30–550 °C use a polynomial baseline [R5 pp.32–36, 68–69] | Feasible in-house for fresh versus stored slugs and baked walls; Al–Mg–Si peak positions differ |
| SAXS | Electron-density fluctuations. With R5's statistical model it gives the correlation length ξ (size), periodicity λ (spacing) and the invariant (mean-square fluctuation); in-situ kinetics and heating ramps are possible [R5 pp.39, 49–50] | Elemental sensitivity (f_i − f_Al)/f_Al: Cu 1.23, **Mg −0.08**, Li −0.77. **Nearly blind to Mg and Si in Al** [R5 pp.46, 48–49, 77] | Lab Cu-Kα rotating anode, q = 0.02–0.5 Å⁻¹, 80 µm foils; synchrotron ramps up to 100 °C min⁻¹ with 1 s counts [R5 pp.39, 47, 69] | Unsuitable for Mg–Si clusters (inference from the sensitivities) |
| SANS | Nuclear-scattering fluctuations: Mg contrast 0.55, Cu 1.23, Li −1.55 [R5 p.46]. Combined with SAXS ("contrast variation"), it separates the Cu and Mg contributions [R5 pp.46, 52] | ≥ 10 min per point; room temperature only in R5; Si contrast not given [R5 pp.38–39] | ILL D11, λ = 5 Å (above the Bragg cut-off) [R5 pp.38, 47] | Research tool only |
| APT | Atom-by-atom 3D positions. Equally sensitive to all elements, so it separates Mg and Si in Al [R5 p.16] | Cluster-finding (maximum separation) depends on the chosen parameters and drops small clusters (e.g. < 10 atoms). Anisotropic spatial resolution and detector efficiency. The as-quenched state cannot be measured because of the time between polishing and analysis [R5 pp.16, 40, 47–48] | LEAP 4000, 40 K, 20 % pulse fraction, 200 kHz. Uses assumption-free radial distribution / pair-correlation functions [R5 pp.48, 53–54, 57] | Method of choice for Mg–Si cluster chemistry (external laboratory) |
| TEM / HR-STEM | Clusters are rarely imaged: small, diffuse, low contrast [R5 pp.16, 67] | — | — | Not for clusters; use it for β″/β′ on dislocations after the bake |
| Positron annihilation, NMR | Local vacancy and solute environment [R5 pp.4, 67] | Specialist | Not used | Would test the vacancy story directly |

- **SAS model.** R5 treats clusters as concentration fluctuations and models them with an exponentially decaying, cosine-modulated correlation function, following Couturier et al. and Teubner & Strey [R5 pp.49–50]. ξ scales with cluster size and λ with the distance between clusters [R5 p.50].
  - The mean-square concentration fluctuation can be non-monotonic as clusters grow and dilute. R5 therefore uses the **mean-square number of excess solute atoms** as the progress variable [R5 pp.51–52].
  - Parameter uncertainty was estimated from 100 refits with random starting values [R5 p.56].
- **APT and SAS measure the same thing.** The amplitude of the APT radial distribution function and the SAS correlation function both measure the same solute fluctuation, so the two can be compared directly [R5 pp.18, 53]. The Mg/Cu ratio from SAXS + SANS matched earlier APT values for the same alloy [R5 p.58].

---

## 7. Strengthening contributions

### 7.1 Solid solution

- **Requirements** [R11 p.29]: the solute must be soluble at the annealing temperature, retained on slow cooling, and not tied up in insoluble phases.
- **Baseline:** high-purity Al annealed YS is 7–11 MPa [R11 p.29]; ≈10 MPa [R10 p.367]. TOT: friction stress σ_f = 10 MPa for pure Al [TOT pp.101, 113]; single-crystal CRSS 0.79 MPa [TOT p.89].
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
- **TOT solid-solution data (full-text pass)** [TOT pp.90–95, 160–167]:
  - **Mn in solution** (binary Al–Mn, retained by high-temperature anneal + rapid quench): annealed YS **+21 MPa per wt%**, UTS **+42 MPa per wt%**; H19 YS only +35 MPa per wt% [TOT p.160]. ⚠ **Conflict:** R10 Table 8 gives 30.3 (YS) and 53.8 (UTS) MPa per wt% Mn. Both are Alcoa-lineage data, with different alloys and tempers. Not resolved; use the range 21–30 MPa per wt% YS.
  - **Mg:** H19 YS +70–85 MPa per wt% Mg, which is why commercial 3xxx alloys add Mg and/or Cu [TOT pp.160, 164]. In Hall–Petch fits of 5xxx, **σ_f = 15.5 × (wt% Mg) MPa** [TOT p.167 Eq 24].
  - **Concentration exponent (Mg):** ΔYS ∝ (at% Mg)^(2/3) below 1 at%, and ∝ (at% Mg)^(1/3) in more concentrated alloys [TOT p.162].
  - **Size-misfit law:** ΔHV = K·|(r_s − r_Al)/r_Al|^1.33·f_s [TOT p.92 Eq 4]. It holds for Cr, Mn, Cu and Zr. Fe, Co and Ni harden more than predicted, which TOT attributes to clustering [TOT p.92].
  - **Ranking:** Mn and Cu are the most effective strengtheners per atom at ≤ 0.5 at%. Mg is the most effective per wt% and is highly soluble. Zn is the least efficient [TOT pp.94–95].
  - **Additivity ⚠:** TOT says dilute solute effects are "usually additive" [TOT p.90], and that Mg + Si, Cu + Mg and Zn + Mg together give *more* than the sum [TOT p.95]. R10 says multiple solutes give slightly *less* than additive. Flagged.
  - **Elastic modulus:** Si raises E by 8.5 % per at% in solution, Cu by 4.4 % and Li by 1.5 % [TOT p.95]. Mg lowers density by ≈ 0.5 % per wt% in solution [TOT p.160].
- **Model form:** σ_ss = Σ k_i c_i^n.
  - R10 gives only linear unit slopes (n = 1 fit) with a non-linearity caveat.
  - TOT gives **n = 2/3 for dilute Mg (< 1 at%)** and 1/3 above (see above). *Updated after full-text pass; previously "general knowledge n ≈ 2/3–1".* No exponent is given for Mn, Si or Fe.
  - Fit k_i and n to the user's own 3xxx data.
- **Relevance (T11):** 0.26 % Mg is ≈ 0.29 at% (derived), inside the dilute (n = 2/3) regime. 0.14 % Mn, if fully dissolved, adds ≤ 3–4 MPa YS on the 21–30 MPa per wt% slopes (derived).
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
- **Orowan (Polmear/Nie form)** [R11 pp.56, 60; TOT p.107 Eq 15]: Δτ = [Gb / (2π√(1−ν))] (1/λ) ln(D_p/r₀).
  - TOT prints the prefactor as 2Gb/(4π√(1−ν)), which is the same thing.
  - Δτ: critical resolved shear stress increment; G: shear modulus; b: Burgers vector; ν: Poisson's ratio; λ: effective planar spacing; D_p: planar particle diameter; r₀: dislocation core radius.
  - Maximum hardening is expected when the spacing equals the limiting dislocation radius of curvature, about 50 atomic spacings (≈ 10 nm) [TOT pp.107, 108].
  - **Planar spacing and diameter** [TOT p.109 Table 5; R11 p.60]. *Corrected after full-text pass: TOT prints the π and minus signs that were lost in R11.* D = plate diameter, T (t) = plate thickness, D_s / D_R = sphere / rod diameter, f = volume fraction:
    - {100} plates: λ = 0.931(0.306πDT/f)^½ − πD/8 − 1.061T; D_p = 1.225T.
    - {111} plates: λ = 0.931(0.265πDT/f)^½ − πD/8 − 0.919T; D_p = 1.061T.
    - ⟨100⟩ rods: λ = 1.075·D_R·(0.433π/f)^½ − 1.316·D_R; D_p = 1.316·D_R ⚠ (layout partly garbled).
    - Random spheres: λ = 0.538·D_s·(2π/3f)^½ − πD_s/4; D_p = D_s ⚠ (layout partly garbled).
  - Ranking: plates > rods > spheres; {111} plates > {100}; strengthening rises with aspect ratio [R11 p.60; TOT pp.108–109].
- **Shear/bypass scaling and critical size** [TOT pp.103–107]:
  - Shearing: Δσ_y = c·f^m·r^q, with m, q ≈ 0.5 [Eq 11]. Bypassing: Δσ_y = β·r⁻¹·f^0.5 [Eq 12].
  - The critical diameter for the shear-to-bypass transition is (D_p)s→b = 4πbC·G_Al/G_particle for a non-coherent particle (C ≈ 1 for spheres) [Eq 13], and G_Al·b²/γ_APB for an ordered coherent one [Eq 14].
  - Table 4 values (units not printed, presumably nm ⚠): Ge 0.2; Si, FeAl₃, CuAl₂ 0.5–5; Zn 15; δ′ 50 (single dislocations), > 500 (pairs); T₁ 0.8 (critical plate thickness); S′ 2; η′ 6. Elsewhere in TOT, δ′ is 34 nm in binary Al–Li and 18 nm with Cu [TOT pp.152, 156].
  - Peak strength is reached as soon as the *largest* precipitates reach (D_p)s→b, so a narrower size distribution gives a higher peak [TOT pp.109–110].
- **Other mechanisms, TOT forms** ⚠ (exponents partly garbled; check the PDF before use) [TOT pp.110–113]: chemical (∝ (γ_s³bf/G)^½/r) [Eq 16]; stacking-fault [Eq 17]; modulus [Eq 18]; coherency (∝ f^½(ε/r…)^¼) [Eqs 19–20]; order (∝ (γ_APB³ f r/(b²G))^½) [Eq 21]. The GP-zone stacking-fault energy is 350 mJ m⁻² in Al–Zn–Mg [TOT p.111].
- **Superposition** [TOT p.113 Eqs 22–23]: σ = σ_f + ΣΔσ_i for different mechanisms. For several precipitate types, Δσ^q = ΣΔσ_i^q, with **q = 1.5** fitting better than 2 (Al–Li–Cu–Mg–Zr example: (45^1.5 + 15^1.5)^(1/1.5) = 51 MPa versus 55 MPa measured).
- **Orowan–Ashby form (general knowledge, not in the sources):** Δσ = 0.4 M G b ln(2r̄/b) / (π λ √(1−ν)).
  - *Corrected after full-text pass:* **G_Al = 23 GPa** [TOT p.85] (previously "≈ 26 GPa, general knowledge"); **M ≈ 3** [TOT p.89] (3.06 is the general-knowledge random-texture value); b = 0.286 nm [TOT p.83], or 0.2863 nm derived from a = 0.40496 nm [R4 Table 1].
  - ν ≈ 0.33 is still general knowledge; no source gives a value.
  - Convert CRSS to yield stress with Δσ = MΔτ.
- **Magnitudes:**
  - Age hardening can raise YS of high-purity Al by up to 50×; the theoretical upper limit for Al is about 900 MPa [R11 p.61].
  - Dispersion hardening in 8xxx is 30–40 MPa [R11 p.131].
  - Al₃Sc hardening is about 100 MPa [R3 p.13].
  - Excess Si: 0.2 % excess adds about 70 MPa to a 0.8 % Mg₂Si alloy [R10 p.381].
  - Fe-rich constituents: ≈ 7 MPa YS per vol% in annealed 1xxx [TOT pp.122, 138]. For T11's ≈ 1.5–2 vol% constituents (estimate in the T11 record) that is ≈ 10–14 MPa (derived).
  - Al₃Zr dispersoids add little dispersion strength (low volume fraction) but a lot of grain- and subgrain-boundary strength by preventing recrystallisation: +25 MPa in Al–2.5Li–Zr [TOT p.114].
  - Texture strengthening of unrecrystallised extrusions: longitudinal YS ≈ 70 MPa above transverse. It is lost on recrystallisation [TOT p.131].
- **Work hardening and substructure** [R11 pp.36, 41]:
  - σ = kεⁿ, with n falling from 0.25 to 0.17 as k rises from 175 to 450 MPa.
  - Substructure: σ = σ₀ + k₁d^(−m), with m from 1 (cells) to 0.5 (subgrains). TOT agrees: hot-work subgrains m ≈ ½, low-temperature cells m ≈ 1; fine-grained 8xxx with particle-stabilised grains also m ≈ 1 [TOT pp.101–102].
  - Stacking-fault energy is about 170 mJ m⁻². ⚠ TOT gives **200 mJ m⁻²** [TOT p.85]. Flagged.
  - Dislocation density falls from 10¹² (cold worked) to 10¹⁰ (recovered) to 10⁷–10⁸ cm⁻² (recrystallised).
- **Work hardening, TOT data** [TOT pp.96–102, 140, 160–166]:
  - Taylor hardening: Δσ_y = MαGb√ρ, with α ≈ 0.2–0.3 depending on composition [Eq 6, p.96]. Initial strain hardening of pure Al ≈ G/20 [p.97].
  - Hall–Petch: σ_y = σ_f + k·d^(−½). k = 0.065 MPa m^½ for pure Al and 0.1–0.2 for many alloys [p.101]. Mg-free alloys have k ≤ 0.15, Al–Mg alloys > 0.2. 5754: k 0.22, σ_f 42.5 MPa; 5182: k 0.30, σ_f 57.6 MPa [p.167]. k is about 5× lower than in ferrous alloys [TOT p.263].
  - **Hollomon parameters, O temper** [TOT p.100 Table 3]:

| Alloy | n | k (MPa) |
|---|---|---|
| 1100-O | 0.242 | 146 |
| 3003-O | 0.242 | 188 |
| 6061-O | 0.209 | 224 |
| 5052-O | 0.198 | 281 |
| 5454-O | 0.189 | 340 |
| 5086-O | 0.193 | 368 |
| 5456-O | 0.178 | 479 |

  - **Solute work-hardening parameters** [TOT p.99 Table 2]:
    - Dorn "Cu-equivalent" K per at%: Cu 1.00, Ge 0.64, Mg 0.37, Cd 0.33, Ag 0.15, Zn 0.071.
    - Doherty H (GPa), from YS after a rolling strain of 1: Cu 3.38 ± 0.20, Si 1.56 ± 0.05, Mg 1.52 ± 0.14, Mn 1.03 ± 0.17, Zn 0.27. ⚠ The defining Eq 9 (H ∝ (k_alloy − k_Al)/(at. fraction)^(2/3)) is garbled in extraction.
  - Si in solution impedes dynamic recovery and raises work hardening (Al–0.27Fe–xSi) [TOT p.140]. Mg suppresses cell formation in Al–Mn, which gives finer substructure and higher strength in 3004 than in 3003 [TOT pp.160, 166].
  - In 1145, dislocation cells reach a limiting size just under 1 µm at a true strain of ≈ 0.15 [TOT p.140].
  - Rolling: YS = k·ε_roll^n, with ε_roll = ln(t_i/t_f) [TOT pp.98–99 Eq 8].
- **Relevance (impact extrusion of slugs):** the Hollomon pairs give a direct prior for flow-stress and press-force models. 1100-O (k 146) to 3003-O (k 188) brackets lean slug alloys (inference). Mg and Si in solution raise k through higher work hardening (H: Mg 1.52, Si 1.56 GPa) more than through YS [TOT pp.99, 140, 164].

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
- **Recrystallisation (full-text pass).** In Yelagin's binaries, 0.12 at% Mo (≈ 0.43 wt%, derived) raised the recrystallisation onset by **+70 K** and the finish by **+45 K** [TOT p.296 Table 35]. As a Period V TM, Mo acts even at very small additions [TOT p.296]. TOT also lists Al–Mo as peritectic [TOT p.294].
  - Molybdenum is the third most effective onset-raiser in that table, after Sc and Zr and ahead of Cr and Mn (derived ranking).
- **Thermal stability and dispersoid size or kinetics of Mo:** still no data in any source read (see §12).

---

## 10. Per-element alloying effects (wrought Al)

Notation: SS = solid solution; RX = recrystallisation; cond. = electrical conductivity; NHT = non-heat-treatable. Max solubility is from [R11 p.30] unless noted (TOT cross-check in §1.2). Diffusion is D at 500 °C [R11 p.105] where available; TOT gives only a TM range and a group ratio; R5 adds D₀/Q for Cu, Mg and Li [R5 p.121] (§1.4). RX increments "+x / +y K" are the maximum rises of recrystallisation onset / finish in Yelagin's binaries [TOT p.296 Table 35] (§5). The conductivity column uses TOT's harm ranking Cr > V > Mn > Ti > Mg > Ag > Cu > Zn > Si > Fe > Ni [TOT p.52]. Work-hardening parameters K and H are from [TOT p.99 Table 2] (§7.2). *Table updated after full-text pass 2026-10-12.*

| Element | Max solubility (wt% @ °C) | Diffusion | Partitioning / reaction | Phases formed | Strength | RX / grain | Corrosion | Conductivity | Castability / process | Typical levels |
|---|---|---|---|---|---|---|---|---|---|---|
| **Mn** | 1.82 @ 658; ≤0.23 @ 654 with Fe; ≤0.08 with Si saturation [R8]; eutectic ≈ 1.9 % @ 657 °C [TOT p.159]; 2.5–2.8 % retained at 10–100 K/s casting [TOT p.294] | 5×10⁻¹³ cm²/s (slowest listed) [R11]; inside the TM range 10⁻¹⁴–10⁻¹² cm²/s [TOT p.295] | eutectic [TOT p.294] (k < 1, gen. knowl.) | Al₆(Mn,Fe), α-Al₁₅(FeMn)₃Si₂ / Al₁₂(Mn,Fe)₃Si, Al₂₀Cu₂Mn₃, Al₆Mn dispersoids [R8; R10 p.389; TOT pp.160, 299]; Al₁₃(Fe,Mn)₄ at high Fe/Mn [TOT p.160] | SS: annealed YS +21, UTS +42 MPa/wt% [TOT p.160] vs YS 30.3 [R10 Table 8] ⚠; H19 YS +35 MPa/wt% [TOT p.160]; H = 1.03 GPa [TOT p.99]; dispersion, but "no real precipitation hardening" [TOT p.299]; Mn ≈ 2× Mg in Al–Mg–Mn [R10 p.380] | raises RX temperature, fibrous structure, slows recovery [R10 p.382]; only +30 K onset at 0.77 at% [TOT Table 35]; supersaturated (Al) decomposes > 325 °C (300–350 °C) [TOT pp.295, 299] | no adverse effect; Al₆(Mn,Fe) and α at ≈ matrix potential [R10 pp.382, 402]; MnAl₆ −0.85 V [R11 Table 2.5] | strongly lowers conductivity; among the most harmful with Cr, V, Ti [TOT p.52] (*corrected after full-text pass*; R10 p.382 is wrong) | Fe + Mn < 1.7–2.0 % to avoid primary Al₆ [R10 p.383]; ≤1.25 % because Fe lowers Mn solubility [TOT pp.159–160]; small additions favour script α over β-AlFeSi [TOT p.179]; raises quench sensitivity [TOT pp.177–179] | 3102: 0.05–0.4; 3207: 0.4–0.8; 3003: 1.0–1.6 [R8 Table 1.10]; ≤1.25 [R11]; 3105: 0.2–0.8 [TOT Table 37] |
| **Fe** | 0.05 @ 655 [R11; TOT pp.117, 138] | not given; eutectic-group TMs diffuse ≈ 10× faster than peritectic ones [TOT p.295] | eutectic [TOT p.294] | Al₃Fe (eq., monoclinic); metastable Al₆Fe / AlₘFe in commercial casting; Al₃Fe below ≈ 0.5 mm/s front velocity, Al₆Fe above, Si and Mg stabilise Al₃Fe [TOT pp.138–139]; α-Al₈Fe₂Si / Al₁₂Fe₃Si, β-Al₅FeSi / Al₉Fe₂Si₂, Al₆(FeMn), Al₇Cu₂Fe [R8; R10; TOT] | slight; creep in conductors [R10 p.379]; 8006 fine-grain strength; constituents ≈ 7 MPa YS per vol% [TOT p.122]; hardens more than the size law predicts (clustering) [TOT p.92] | reduces grain size; stabilises fine grains (8006) [R10 p.379; TOT p.297]; **+65 K RX onset at 0.04 at% in SS** [TOT Table 35]; Fe in SS delays RX through fine Al–Fe precipitation [TOT p.140]; controls texture and earing in 3xxx [TOT p.299] | Al₃Fe/Al₆Fe/AlFeSi cathodic → pitting ∝ area fraction [R10 p.399]; FeAl₃ −0.56 V | small (mostly out of solution; near the end of TOT's harm ranking) [TOT p.52] | Fe:Si > 1 to avoid hot tearing [R8 p.29]; needles in foil; coarse Al₃Fe cracks and lowers formability, fine Al₆Fe does not [TOT p.139]; raises quench sensitivity [TOT p.194] | 0.4–0.7 (3xxx); 1.2–2 (8006) |
| **Si** | 1.65 @ 577; lowered by Mg [TOT p.122] | 1×10⁻⁹ | eutectic | Si (direct, no transition phase [TOT p.168]), α/β-AlFeSi, α-Al(FeMn)Si, Mg₂Si, AlSc₂Si₂ [R4] | 9.2 MPa/wt% YS; excess Si in 6xxx +70 MPa [R10]; raises work hardening, H = 1.56 GPa [TOT pp.99, 140]; E +8.5 %/at% [TOT p.95]; Si available for Mg₂Si = Si − ¼(Fe + Mn) [TOT p.171] | promotes α dispersoids and speeds Mn precipitation [R8; TOT p.160]; GB segregation in 6xxx [R10 p.381; TOT p.172]; fine Si/AlFeSi particles delay early RX [TOT p.140] | Si −0.26 V (cathodic but polarised) [R11; R10 p.402]; excess Si → intergranular corrosion in 6xxx | moderate (9th of 11 in TOT's ranking) [TOT p.52] | hot short 0.17–0.8 % in high-purity Al [R10 p.384]; fluidity; improves feeding and hot-crack resistance in Al–Cu [TOT p.149] | 0.1–0.6 (3xxx) |
| **Cu** | 5.65 @ 548 | 5×10⁻¹⁰; D₀ 4.44×10⁻⁵ m²/s, Q 133.9 kJ/mol (Du, via [R5 p.121]) | eutectic | θ series, S, Q, Al₂₀Cu₂Mn₃, Al₇Cu₂Fe [R10; R11; TOT] | 13.8 MPa/wt% YS (SS); age hardening max 4–6 % [R10 p.373]; most effective per atom together with Mn [TOT p.94]; strongest work-hardening solute: K = 1, H = 3.38 GPa [TOT p.99]; E +4.4 %/at% [TOT p.95] | most effective at slowing recovery [R11 p.34; TOT p.100] | most detrimental (micro-constituents); 0.05–0.2 % gives more uniform corrosion and less pitting [R11 p.72]; raises potential (Al–4Cu −0.69 V) | moderate [TOT p.52] | ≤0.3 % in NHT (avoids Al–Cu–Fe constituents and ageing) [R11 p.30; TOT p.94]; SCC in some tempers [R7 p.2]; 0.25 % reduces the 6xxx natural-ageing penalty; refines β″ [TOT pp.177, 279] | 0.05–0.3 (3xxx) |
| **Mg** | 17.4 @ 450 [R11] ⚠ vs 14.9 @ 450 [TOT p.161]; ≈ 1.7 at RT [TOT p.161] | 1×10⁻⁹; D₀ 1.49×10⁻⁵ m²/s, Q 120.5 kJ/mol (Du, via [R5 p.121]); faster than Cu in all data sets [R5 p.121] | eutectic | Mg₅Al₈ (β), Mg₂Si, S, η, Al₁₂Mg₂Cr, Al₂LiMg | 18.6 MPa/wt% YS [R10]; ΔYS ∝ (at% Mg)^(2/3) below 1 at% [TOT p.162]; σ_f = 15.5·wt% Mg (5xxx) [TOT p.167]; H19 +70–85 MPa/wt% [TOT p.160]; K = 0.37, H = 1.52 GPa [TOT p.99]; ≤175 MPa annealed at 6 % [R11 p.30; TOT p.94]; catalyses room-temperature Cu clustering, with no threshold, by making vacancies available (Al–Cu–Li–Mg) [R5 pp.103, 109] | finer annealed grains up to 3.5 % Mg [TOT p.166]; suppresses dynamic recovery and cell formation [TOT pp.160, 166]; high-Mg alloys lose strength mainly by recovery [TOT p.168] | >3–4 % → β at grain boundaries → intergranular corrosion / SCC [R11 p.130; R10 p.403]; Al–5Mg −0.88 V | moderate (5th of 11 in TOT's ranking) [TOT p.52] | Lüders lines; hot cracking with Na [R10 p.380]; thicker oxide on the melt [TOT p.168]; Mg₂Si constituent in 5xxx [TOT p.167] | 0.1–0.3 (3xxx), 0.8–5.5 (5xxx) |
| **Zn** | 82.8 @ 443 (peritectic per R11) | — | — | MgZn₂, T-phase; τ in Al–Mg | 2.9 MPa/wt% YS; little work hardening [R11 p.34]; least efficient solute, K = 0.071, H = 0.27 GPa [TOT pp.95, 99] | — | raises potential (anodic) → 7072 clad, sacrificial anodes [R10 p.385]; ≈ 1 % in some NHT alloys to adjust potential [TOT p.95]; 0.68–0.70 % Zn in 5083 → τ instead of β [R7 p.5] | small [TOT p.52] | — | 1–1.5 for HX fin anodic protection (gen. knowl.) |
| **Cr** | 0.77 @ 661 (peritectic; peritectic composition 0.41 %) [R11; TOT p.116] | slow (qualitative) [R10 p.373; TOT p.168] | peritectic; primary Al₇Cr above 0.41 % [TOT p.116]; Al₇Cr primary at lower Cr in commercial alloys [R10 p.389] | Al₁₂Mg₂Cr, Al₁₈Mg₃Cr₂ dispersoids; Al₇Cr below ≈ 2 % Mg [TOT p.192]; supersaturated (Al) decomposes at 450–500 °C [TOT p.295] | slight | prevents RX in 6xxx/7xxx; +45 K onset at 0.35 at% [TOT Table 35] | reduces SCC (fibrous structure); yellow anodic film [R10 p.373] | large resistivity increase [R10 p.373]; the most harmful impurity in TOT's ranking [TOT p.52] | highest quench sensitivity [R11 p.112; TOT p.127]; sludge (factor Fe + 2Mn + 3Cr) [R7 p.5] | ≤0.35 |
| **Zr** | 0.28 @ 660.5 (peritectic) [R11]; 0.093 at% [TOT p.295] | D_Sc/D_Zr ≈ 4 [R1] ⚠ vs ≈ 510–640 [ch13; ch18]; peritectic group ≈ 10× slower than eutectic [TOT p.295] | peritectic, **k = 1.4** [R1] | L1₂ Al₃Zr (metastable; misfit ≈ 0.6 %; ≈ 20 nm; 5–11 nm after 350–450 °C/200 h), D0₂₃ (eq.), Al₃(Sc,Zr) shell [R1; TOT pp.125, 192, 298]; supersaturated (Al) decomposes at 400–450 °C [TOT p.295] | small; ΔH/C 154 per at% (relative) [TOT Table 34] | 0.1–0.3 % inhibits recovery and RX [R10 p.387]; the most effective RX inhibitor in 7xxx [TOT p.192]; +105 / +240 K (onset/finish) at 0.09 at% [TOT Table 35]; dendrite-edge dispersoid-free zones [R1] | non-recrystallised structure helps SCC resistance [R10 p.387] | — | least quench-sensitive dispersoid [R11; TOT p.127]; Al₃Zr formation strongly helped by excess Si in 6xxx [TOT p.179]; reduces TiB grain refining [R10 p.387] | <0.15 (0.05–0.25 with Sc) |
| **Sc** | ≈0.35–0.38 @ 655–659 (eutectic, 0.6 % at eutectic point) [R4; R3]; 0.025 @ 430 [R4]; 0.28 at% (≈0.47 wt%) [TOT p.295] ⚠ | see Zr | eutectic, **k = 0.9** [R1] | L1₂ Al₃Sc (core), AlSc₂Si₂, W-phase [R4]; supersaturated (Al) decomposes at 250–350 °C [TOT p.295] | ~100 MPa hardening; about 300 MPa/wt% YS in 3xxx (derived) [R3]; ΔYS_max/C ≈ 1000 MPa per at% (0.5 % Sc) [TOT Table 36] | strongest anti-RX element; +220 °C onset (0.3 %) [R4 p.34]; +120 / +320 K at 0.20 at% [TOT Table 35] | slightly more noble; improved self-corrosion [R4 p.38] | — (not in sources) | best grain refiner (>0.6 %, or lower with Zr) [R4 p.33]; +44 % extrusion pressure [R2] | 0.02–0.3 |
| **Ti** | ~1.3 @ 665 (peritectic) [R11] ⚠ vs 0.17 at% [TOT p.295] | — | peritectic; Q ≈ 35 at 0.15 % [R9] | Al₃Ti, TiB₂; substitutes in Al₃Sc [R4] | slight | grain refiner (with B); Al₃(Sc,Ti) nucleants [R4 p.34]; +5 / +180 K at 0.25 at% [TOT Table 35] | higher Ti improves corrosion in 3003 [R7 p.3] | depresses conductivity; removed by B [R10 p.385]; among the most harmful [TOT p.52] | ~0.015 % optimal in DC 3003; ≥0.15 % coarser grains and casting problems [R7 p.3] | 0.01–0.05 |
| **V** | ~0.4 @ 661 (peritectic) [R11]; 0.21 at% [TOT p.295] | — | peritectic (VAl₁₁) | Al₂₁V₂; Al₁₁V (TOT); V in Al₃Sc 1.4–2.7 at% [R4]; supersaturated (Al) decomposes at 500–550 °C [TOT p.295] | — | raises RX temperature [R10 p.385]; only +15 / +15 K at 0.21 at% [TOT Table 35] | — | lowers conductivity; removed by B [R10]; second most harmful [TOT p.52] | weaker refiner than Ti and Zr; raises quench sensitivity of Al–Zn–Mg more than Cr or Mn [TOT pp.193–194] | 10–200 ppm impurity |
| **Mo** | ≈0.1 "peritectic limit" [R6] | — (peritectic group, slow [TOT p.295]) | peritectic [R6; TOT p.294] | Al₁₂Mo [R4] | as cast −9 % flow stress; after ECAP +4.7 % [R6] | grain refiner at 0.3 % (historic) [R10]; +70 / +45 K at 0.12 at% [TOT Table 35] | — | harmful in solid solution (removed by B) [R10 p.372] | master alloy at 1100 °C [R6] | 0.1–1 ppm impurity |
| **Ni** | 0.04 @ 640 | — | eutectic [TOT p.294] | Al₃Ni (with Fe) | up to 2 % strengthens and lowers ductility; hot hardness [R10 p.383; R7 p.2]; hardens more than the size law predicts (clustering) [TOT p.92] | −10 / +5 K at 0.04 at% [TOT Table 35] | promotes pitting in 1100 [R10 p.383]; NiAl₃ −0.52 V | least harmful in TOT's ranking [TOT p.52] | — | 8001: 1.1 |
| **Nb** | — | — (Period V, peritectic [R10 p.383]) | peritectic | — | — | +35 / +35 K at 0.12 at% [TOT Table 35] | — | — | — | — |
| **Li** | 4.2 @ 600 [R11]; ≈ 4 wt% (16 at%) @ 610 [TOT p.152] | D₀ 1.55×10⁻⁵ m²/s, Q 119.2 kJ/mol [R5 p.121] | — | δ′, T₁, AlLi; stays random (no clusters) in naturally aged Al–Cu–Li(–Mg) [R5 pp.54, 129] | low density (−3 % per 1 % Li), modulus +5–6 % per 1 % Li [TOT pp.152, 289] | — | <5 ppm causes blue corrosion of foil [R10 p.380] | — | oxidises melt; high vacancy binding hinders loop formation [TOT p.87] | — |
| **Ag** | 55.6 @ 566 | — | — | Ω (with Cu, Mg), Ag–Mg clusters | 0.1–0.6 % in Al–Zn–Mg improves strength and SCC [R10 p.384] | — | — | — | — | — |
| **Sn / In / Cd** | Sn ~0.06 @ 228 | — | — | Sn particles nucleate θ′ | 0.05 % Sn boosts artificial ageing of Al–Cu [R10 p.384; R11 p.50] | — | 0.01 % Sn darkens surfaces and raises corrosion susceptibility [R10 p.384] | — | traps vacancies (binding 0.25 eV vs ≈ ±0.02 eV for Cu and Mg [R5 p.122]); delays Si clustering in Al–Mg–Si by orders of magnitude [R5 pp.10, 45, 89] | ppm–0.1 |
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
| D_Sc/D_Zr | ≈4 ⚠ (≈ 510–640 from Arrhenius sets [ch13; ch18]; TOT group ratio ≈ 10 [TOT p.295]); unresolved, §1.4 | — | 480 °C | [R1 p.1414] |
| D_Mn, D_Cu, D_Mg/Si | 5×10⁻¹⁷, 5×10⁻¹⁴, 1×10⁻¹³ | m² s⁻¹ | 500 °C | [R11 p.105]; D_Mn inside the TOT TM range [TOT p.295] |
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
| Homogenisation heating rate | ~50–75 | °C h⁻¹ | fine dispersoids | [R11 p.106; R2 p.18] |
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
| *Rows below added after the [TOT] full-text pass (2026-10-12)* | | | | |
| G_Al (shear modulus) | 23 | GPa | — | [TOT p.85] |
| Burgers vector b | 0.286 | nm | — | [TOT p.83] |
| Taylor factor M | ≈ 3 | — | polycrystal | [TOT p.89] |
| Taylor constant α (Δσ = MαGb√ρ) | 0.2–0.3 | — | composition dependent | [TOT p.96] |
| Stacking-fault energy | 200 (TOT) vs ≈ 170 (R11) ⚠ | mJ m⁻² | pure Al | [TOT p.85; R11 p.36] |
| CRSS, pure Al single crystal | 0.79 | MPa | — | [TOT p.89] |
| Friction stress σ_f, pure Al | 10 | MPa | — | [TOT pp.101, 113] |
| Hall–Petch k | 0.065 (pure Al); 0.1–0.2 (alloys); ≤ 0.15 (Mg-free); 0.22 (5754), 0.30 (5182) | MPa m^½ | — | [TOT pp.101, 167] |
| σ_f(Mg), 5xxx | 15.5 × wt% Mg | MPa | Hall–Petch fits | [TOT p.167] |
| Mn SS strengthening | YS +21, UTS +42 per wt% (annealed); H19 YS +35 per wt% | MPa | binary Al–Mn, Mn retained by quench | [TOT p.160]; cf. 30.3 [R10] ⚠ |
| Mg strengthening, H19 | +70–85 | MPa per wt% | — | [TOT pp.160, 164] |
| Mg SS exponent | ΔYS ∝ c^(2/3) (< 1 at%); c^(1/3) (concentrated) | — | annealed Al–Mg | [TOT p.162] |
| Constituent strengthening | ≈ 7 | MPa YS per vol% | annealed Al–0.05Si–(0.15–1.17)Fe | [TOT pp.122, 138] |
| Doherty H (work hardening) | Cu 3.38, Si 1.56, Mg 1.52, Mn 1.03, Zn 0.27 | GPa | cold rolling, ε = 1 | [TOT p.99] |
| Dorn K (Cu-equivalent per at%) | Cu 1.00, Ge 0.64, Mg 0.37, Cd 0.33, Ag 0.15, Zn 0.071 | — | tensile | [TOT p.99] |
| Hollomon n / k, O temper | 1100 0.242/146; 3003 0.242/188; 6061 0.209/224; 5052 0.198/281; 5454 0.189/340; 5086 0.193/368; 5456 0.178/479 | — / MPa | — | [TOT p.100] |
| Precipitate superposition exponent q | 1.5 (better than 2) | — | Δσ^q = ΣΔσ_i^q | [TOT p.113] |
| Max-hardening spacing | ≈ 10 (≈ 50 atomic spacings) | nm | — | [TOT p.107] |
| E change per at% in SS | Si +8.5, Cu +4.4, Li +1.5 | % | — | [TOT p.95] |
| Vacancy energies | E_f 0.76 (≈ 0.7), E_m 0.65, E_sd 1.4 | eV | pure Al | [TOT pp.40, 86] |
| TM diffusivity range | 10⁻¹⁴–10⁻¹² | cm² s⁻¹ | 500 °C | [TOT p.295] |
| D(eutectic TMs)/D(peritectic TMs) | ≈ 10 | — | group statement | [TOT p.295] |
| Peritectic-TM supersaturation threshold | ≈ 10² | K s⁻¹ | solidification | [TOT p.295] |
| Mn in (Al) versus cooling rate | 1.82 (0.1), 2.5 (10), 2.8 (10²), 3–5 (10³) | wt% (K s⁻¹) | — | [TOT p.294 Table 33] |
| Decomposition T of supersaturated (Al) | Mn 300–350 (> 325); Sc 250–350; Zr 400–450; Cr 450–500; V 500–550 | °C | binary | [TOT pp.295, 299] |
| RX onset / finish increments | Sc +120/+320 (0.20 at%); Zr +105/+240 (0.09); Mo +70/+45 (0.12); Fe +65/+35 (0.04); Cr +45/+30 (0.35); Mn +30/+25 (0.77) | K | Yelagin binaries | [TOT p.296 Table 35] |
| Al₃Zr misfit | ≈ 0.6 | % | — | [TOT p.125] |
| Al₃Sc misfit in Al–6.5Mg | 0.54 | % | — | [TOT p.300] |
| Al₃Zr / Al₃Sc size | 5–11 / 25–35 | nm | 350–450 °C, ≤ 200 h | [TOT p.298] |
| Dispersoid size for RX retardation | < 0.4 | µm | — | [TOT p.125] |
| Si available for Mg₂Si | Si − ¼(Fe + Mn) | wt% | 6xxx rule | [TOT p.171] |
| Mg₂Si from Mg (excess Si) | 1.578 × Mg | wt% | — | [TOT p.171] |
| Mg₂Si quasi-binary | eutectic 595 °C; max solubility 1.85 | °C; wt% | no solvus curve given | [TOT p.171] |
| GP-zone critical temperature T_v | 111 + 71·(wt% Mg₂Si) | °C | Al–Mg–Si | [TOT p.177] |
| Natural-ageing (delay) thresholds | beneficial < 0.9; harmful > 1.1 (at% as printed; R11: wt%) ⚠ | % Mg₂Si | Al–Mg–Si | [TOT pp.175–176; R11 pp.141–142] |
| Zone stage / β′ transition time | 5 h / 200 h (150 °C); 8 min / 8 h (200 °C) | — | 6xxx | [TOT p.279] |
| Direct β′ / β-only temperature | > 300 / > 400 | °C | Al–Mg–Si | [TOT p.278] |
| Si precipitation complete | 17 h (150 °C) to 30 min (250 °C) | — | Al–Si | [TOT p.280] |
| Quench rates (6xxx sensitivity test) | still air 0.65; cold water > 1000 | °C s⁻¹ | — | [TOT p.177] |
| *Rows below added after the [R5] full-text pass (2026-10-12)* | | | | |
| D₀, Q (Cu in Al) | 4.44×10⁻⁵, 133.9 (Du); 1.00×10⁻⁵, 127.6 (Doig); 4.37×10⁻⁶, 120.6 (first principles) | m² s⁻¹; kJ mol⁻¹ | Arrhenius | [R5 p.121 Table 10] |
| D₀, Q (Mg in Al) | 1.49×10⁻⁵, 120.5 (Du); 1.00×10⁻⁶, 110.0 (Doig); 1.19×10⁻⁵, 122.5 (first principles) | m² s⁻¹; kJ mol⁻¹ | Arrhenius; Du set reproduces R11's D(500 °C) | [R5 p.121 Table 10] |
| D₀, Q (Li in Al) | 1.55×10⁻⁵, 119.2 | m² s⁻¹; kJ mol⁻¹ | Arrhenius | [R5 p.121 Table 10] |
| D₀, Q (Al self-diffusion) | 6.6×10⁻⁶, 124.5 | m² s⁻¹; kJ mol⁻¹ | normalising values in the Table 10 caption | [R5 p.121] |
| Vacancy formation enthalpy | 0.75 | eV | c_v,eq(250 °C)/c_v,eq(200 °C) ≈ 6 | [R5 p.103] |
| Solute–vacancy binding | Cu ≈ +0.02, Mg ≈ −0.02, Sn 0.25 | eV | first principles (Wolverton 2007) | [R5 p.122] |
| Natural-ageing time scale (Al–Cu–(Li,Mg), water-quenched from 500 °C) | hardness saturates ≈ 10 h; mostly complete in 24 h; stable from 72 h to 6 months | — | room temperature | [R5 pp.30–31, 71] |
| Natural-ageing hardness gain | +20 % (no Mg), +55 % (1.7 at% Mg), +82 % (0.45 at% Mg + Li) | HV | Al–Cu–(Li,Mg) | [R5 pp.71–72] |
| Cluster size / spacing (SAS) | ξ 2.2–5.2; λ 36–72; size < 1 nm | Å | as-quenched and naturally aged | [R5 pp.56, 94] |
| Cluster DSC windows (10 °C min⁻¹) | formation exotherm 50–135; dissolution endotherms 50–260, main minima 130–240 | °C | Al–Cu–(Li,Mg) | [R5 pp.72–74, 92–93] |
| Cluster reversion | Cu-rich: 200 °C/≤ 60 s; Mg-bearing: 250 °C/30 s; Al–Cu–Mg precipitates within 30 s at 240 °C | — | isothermal oil bath | [R5 pp.95–96] |
| SAS sensitivity (f_i − f_Al)/f_Al | SAXS: Cu 1.23, Mg −0.08, Li −0.77; SANS: Cu 1.23, Mg 0.55, Li −1.55 | — | — | [R5 p.46 Table 4] |

---

## 12. Open questions and gaps

*Updated after the [TOT] full-text pass (2026-10-12). Resolved items were removed: the Orowan/planar-spacing signs (now [TOT p.109]), G and M for Al ([TOT pp.85, 89]), the Mg solid-solution exponent ([TOT p.162]), the Mn-resistivity contradiction ([TOT p.52]) and the Mn-diffusivity scale ([TOT p.295]). Partly filled items are marked.*

*Updated again after the [R5] full-text pass (2026-10-12). The old item 5 ("R5 is truncated at p.73") is resolved: Ch. 6–9 were read (§6.5–6.6). Items 1 and 4 are partly filled. Items 19–21 are new.*

1. **D₀ and Q per solute** (Mn, Fe, Si, Zn, Cr, Zr, Sc, Ti, Mo, V, Er) are still **missing from every source read**. TOT gives only vacancy energies [TOT p.40], a TM range at 500 °C, and the factor ≈ 10 between eutectic and peritectic TMs [TOT p.295].
   - *Partly filled (R5):* Cu, Mg and Li now have D₀/Q, as a secondary compilation of Du et al. 2003, Doig & Edington 1973, Mantina et al. 2009 and Wen et al. 1980 [R5 p.121]. The Du set reproduces Polmear's D(500 °C) for Cu and Mg (§1.4). **Si is still missing**, and it is the key solute for T11.
   - **Mn scale: resolved for this chapter.** Polmear's D_Mn(500 °C) = 5×10⁻¹³ cm² s⁻¹ lies inside TOT's range; Sheppard's 10³× faster row does not (§1.4).
   - **D_Sc/D_Zr: still open.** R1 has ≈ 4; the Arrhenius sets give ≈ 510–640 [ch13; ch18]; TOT gives a group-level ≈ 10. Possibly a definition or transcription issue in R1. Reconcile before KWN calibration.
   - Action: source the Du et al. 2003 (Mater. Sci. Eng. A 363 (2003) 140–151, cited in [R5 p.126]) or Fujikawa compilations into the Drive. Du et al. should also give Si and several TMs (general knowledge; not checked).
2. **Mn dispersoid kinetics for 3xxx** (α-Al(Mn,Fe)Si number density, size and coarsening; nucleation on Mg₂Si/"u-phase" precursors; DFZ widths) are not quantified in any source. *Partly filled:* TOT gives the decomposition onset (> 325 °C; 300–350 °C), the Si acceleration, the Al₆/α switch at ≈ 0.07 % Si and the size (< 1 µm) [TOT pp.160, 295, 299], but no number densities.
   - A 3xxx homogenisation/dispersoid paper is needed, e.g. Li & Arnberg (general knowledge).
3. **Partition coefficients** are available only for Zr and Sc [R1]. k for Mn, Fe, Si, Cu, Cr and Ti is needed for Scheil initialisation. TOT gives none.
4. **Activation energies** for cluster formation, GP/β″ precipitation and Al₃Sc nucleation are absent, apart from Q\* = 2.07 eV for interface transfer [R1]. *Partly filled:* TOT gives DSC windows and the 150/200 °C stage times for Al–Mg–Si [TOT pp.279–280], from which an apparent Q could be fitted (not done). R5 adds only solute-diffusion Q (Cu, Mg, Li), E_f = 0.75 eV and solute–vacancy binding energies [R5 pp.103, 121–122]. R5's set-up allowed DSC rates of 2–100 °C min⁻¹ and SAXS ramps from 20 °C h⁻¹ to 100 °C min⁻¹, but results are reported only at 10 °C min⁻¹ [R5 pp.34, 39]. No Kissinger-type activation energy for clustering can therefore be derived from R5.
5. **R5 coverage (mostly resolved).** The full text was read on 2026-10-12, except **pp.24–29** (the end of the Ch. 2 reference list, the Ch. 3 opener and the start of §3.1). Nothing quantitative used here depends on those pages. pp.30–60 exist only as unpaginated Drive text; a ≤ 5 MB re-split of part c would give laid-out text and figures.
6. **R11 and R12 are truncated.** Polmear Ch. 4+ and Humphreys Ch. 9 (particle pinning in recrystallisation, critical F_V/r, Smith–Zener limit) and Ch. 11 were not read.
7. **Braze survival of Al₃(Sc,Zr) at 600–610 °C.**
   - Polmear [R11 p.52] and TOT [TOT p.194] say recrystallisation is inhibited to ≈ 600 °C or above; R2 measured recrystallisation at 575–600 °C with 0.19Sc–0.05Zr.
   - The Zr level and core–shell state needed for a 2–3 min 600 °C braze are unknown. Proposed experiment: Sc 0.05–0.15 × Zr 0.10–0.20 on 3102/3207 bases.
   - TOT's separate Al₃Sc + Al₃Zr description [TOT p.298] versus the core–shell picture [R1; R4] is also unreconciled.
8. **Sc in Fe/Si-bearing 3xxx.** The thresholds for V-phase (AlSc₂Si₂) formation and the loss of Sc efficiency at 3xxx Si/Fe levels are not quantified. There are only two data points [R4 p.32].
9. **Er, Yb, Hf substitution.** No quantitative kinetics or coarsening data. R4 gives only "unchanged peak time" for Y, Gd, Ho and Er at 285 °C.
10. **Mo.** No data on solubility versus temperature, diffusivity, Al₁₂Mo dispersoids or thermal stability. *Partly filled:* +70/+45 K recrystallisation onset/finish at 0.12 at% [TOT p.296].
    - **(general knowledge)** Recent literature reports Mo-modified α-Al(Mn,Fe,Mo)Si dispersoids with improved thermal stability in 3xxx. That literature should be added to the Drive.
11. **Conductivity coefficients** (resistivity per wt% in solid solution and per vol% of precipitate) are still missing. They are needed to use conductivity as a dispersoid-precipitation sensor [R10 p.370].
    - *Partly filled:* TOT gives only a qualitative ranking (Cr > V > Mn > Ti > Mg > Ag > Cu > Zn > Si > Fe > Ni) and the vacancy/interstitial resistivity of 3.4 µΩ cm per at% [TOT pp.39, 52].
12. **Equation fidelity** ⚠: check against the PDFs:
    - R1 Eq. 3 (grouping of the 1/3 factor);
    - R4 Table 3 (Al₃Sc properties);
    - R8 Tables 1.9 and 1.13 (column alignment);
    - TOT Eqs 9, 16–21 and the sphere/rod rows of Table 5 [TOT pp.100, 109–113];
    - TOT Table 34 "ΔH/C" (quantity and unit undefined) [TOT p.295].
13. **Strengthening constants.** Poisson's ratio ν for Al is not given in any source (0.33 is general knowledge). Solid-solution exponents are given only for Mg (2/3 below 1 at%) [TOT p.162]; Mn, Si and Fe are still linear unit effects. The SFE (170 vs 200 mJ m⁻²) and the Mn SS slope (21 vs 30.3 MPa per wt%) conflict between sources (§7).
14. **Mg₂Si solvus versus temperature (new, T11).** No source read gives the temperature at which 0.2–0.4 % Mg₂Si dissolves, with or without excess Si; the TOT figure is unreadable [TOT p.171]. This is needed to set slug-anneal cooling and to predict how much Mg/Si the hot band retains. Action: compute with a CALPHAD tool or source a solvus table.
15. **Natural-ageing threshold unit (new).** 0.9/1.1 % Mg₂Si is "at%" in TOT [TOT pp.175–176] and wt% in R11 [R11 pp.141–142]. Check Baba & Takashima (1969) or Dorward (1973).
16. **Fe-phase selection at rotary-caster conditions (new, T11).**
    - Is the strip solidification-front velocity above or below the ≈ 0.5 mm s⁻¹ Al₃Fe/Al₆Fe switch?
    - How far do Si 0.38 and Mg 0.26 shift it [TOT p.139]?
    - Which of α-AlFeSi, β-Al₅FeSi and Al₁₃(Fe,Mn)₄ forms at Fe:Si ≈ 1.4 with Mn:Fe ≈ 0.27?
    - Check the "4.6–6.1 wt% Fe" range in [TOT p.139] against Todd & Jones (1996) (likely 0.46–0.61 %).
    - Settle by metallography of the T11 cast strip (T11 measurement plan).
17. **Fe supersaturation in rotary-cast strip (new).** TOT Table 33 has no Fe column [TOT p.294]. Retained Fe raises the recrystallisation onset (+65 K at 0.04 at%) [TOT p.296]. Measure conductivity of the cast and quenched strip, and the recrystallisation start, to quantify the effect.
18. **TOT internal and cross-source inconsistencies to check in the PDF:**
    - Mg maximum solubility (14.9 vs 17.4 wt%);
    - Li (13.9 vs 16 at%);
    - Ti (0.17 vs ~0.74 at%);
    - Sc (0.28 at% vs 0.35–0.38 wt%);
    - GP-zone thickness "one atomic layer, i.e. 2.5 nm" and β″ "Si:Al:Mg = 6:3:1" [TOT p.174];
    - Al₃Sc/Al₃Zr "40–300 nm" [TOT p.300].
19. **Al–Mg–Si clustering in dilute alloys (new, T11).** R5 has no Al–Mg–Si data of its own (§6.5). The key papers it cites are not in the Drive:
    - Birol 2005, pre-ageing for bake hardening of a **twin-roll cast** Al–Mg–Si alloy [R5 p.105 ref. 14];
    - Yamada, Sato & Kamio 2000, effect of **quench conditions** on two-step ageing [R5 p.104 ref. 4];
    - Aruga et al. 2014 and 2016, clusters and bake hardening, and natural ageing after pre-ageing [R5 p.60 refs. 25–26];
    - Werinos et al. 2016, controlled natural ageing with Sn [R5 p.105 ref. 11];
    - Pogatscher et al. 2011 [R5 p.105 ref. 12] and Banhart et al. 2010 [R5 p.104 ref. 5].
    - Priority: Birol (strip-cast route), Yamada (quench rate) and Aruga (bake response). These would test the open question in §6.5: do storage clusters dissolve or seed β″ at 220 °C?
20. **Cluster-strengthening law (new).** R5 gives only hardness–cluster correlations [R5 pp.12–13, 112]. The co-cluster strengthening model for Al–Mg–Si (Starink, Cao & Rometsch 2012 [R5 p.117 ref. 16]) is needed to turn a measured slug drift into ΔHB per unit of clustered solute.
21. **Vacancy retention on the T11 route (new).** R5 did not vary the quench rate (§6.5). Whether the slug cooling after the anneal leaves enough excess vacancies for drift must be measured. For both cooling rates in the T11 plan, measure:
    - slug HB at ≈ 2–6 h, 1, 3, 7 and 30 days;
    - DSC of fresh versus stored slugs;
    - wall HV 1 and 30 days after the 220 °C/10 min bake.
