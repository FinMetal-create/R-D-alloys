# 08 — Other alloy families & general physical-metallurgy principles (transfer to wrought Al)

**Scope.** Distils steels (low-alloy creep and cryogenic steels, structural/HSLA, stainless, nanoprecipitate/AHSS), Ni and Ni-base superalloys, Mg alloys and metal-matrix composites (MMCs) into **design principles that transfer to wrought-aluminium alloy design**. It also skims the TMS 2018 proceedings for aluminium-relevant results. It is not a full handbook of these families. It keeps only the mechanisms, quantitative anchors and "levers" useful for designing better wrought Al alloys.

**Conventions.** `[REF, p./§]` = source citation (page numbers are the printed book pages unless noted "PDF p."). **(general knowledge)** = not in the sources read here. Keep these minimal and verify them before quantitative use. **(inference)** = my reasoning that carries a source result over to Al. It is a hypothesis to test, not a source fact. Compositions are in wt% unless stated otherwise.

**Status.** Extracted 2026-10-12. Every Drive source was truncated by the reader, so coverage is partial (see table). German text is translated to English.

## Sources

| Ref | Title (author/editor, year) | Drive link | Lang. | Readability / coverage actually read |
|---|---|---|---|---|
| FAR | *The Alloy Tree: A Guide to Low-alloy Steels, Stainless Steels and Nickel-base Alloys* (J.C.M. Farrar, Woodhead/CRC 2004) | https://drive.google.com/file/d/1DI6Ec7thYXVhQ_z0ApTBihCCkJy3Heve/view | EN | Clean text, ~95 k chars. **Read: front matter, Groups A–D data sheets (pp. 1–63) and the Group E tree (p. ~67).** Groups E–J data sheets, App. 5 (role of elements) and App. 6 (corrosion) were **not returned** (≈35 % of book). |
| EVE | *Engineering Properties of Nickel and Nickel Alloys* (J.L. Everhart, Plenum/Springer 1971) | https://drive.google.com/file/d/1yPxmtJr-sKsxhNlEpkEl6xINfBRUg2k_/view | EN | Good OCR, with garbled figure axes. **Read: Ch. 1–3 and Ch. 4 to p. 68.** Ch. 5 (superalloys, p. 82+), stainless steels, Ch. 8–11 **not returned** (≈30 %). |
| SEG | "Nickel supper alloys.pdf" = M. Segersäll, *Nickel-Based Single-Crystal Superalloys – the crystal orientation influence on high temperature properties*, Linköping Lic. Thesis 1568 (2013) | https://drive.google.com/file/d/1d1gAovTKmXwAhqINacTcB-qS5fyz6aYT/view | EN | Clean LaTeX text. **Read: complete Part I (pp. 1–56) and bibliography.** Part II appended papers (p. 57+) **not returned**. The tables of alloy compositions are partly mis-aligned in the extraction, so only Re levels are quoted. |
| THI | *Werkstoffe I – Chemie und Eigenschaften metallischer Werkstoffe – Stahl und NE-Metalle* (K.-Ch. Thienel, lecture notes, UniBw München, HT 2017) | https://drive.google.com/file/d/13ighAAUOs8kif9PuB8fWFy2mkyR3MYH_/view | **DE → EN** | Good text. Equations were partly scrambled and are reconstructed in the notes. **Read: pp. 1–80 (Ch. 1–9 + start of Ch. 10.1 Al production).** Al properties, Cu, Zn and Ch. 11 corrosion **not returned** (≈70 % read). |
| HIG | *Materials for Engineers and Technicians*, 4th ed. (R.A. Higgins & W. Bolton, Newnes/Elsevier 2006) | https://drive.google.com/file/d/1yZIlYSmfyQIXY3iUdzovF7u1tCHGmWc0/view | EN | Fair OCR. **Read: pp. 1–65 only (Ch. 1–5, Ch. 6 to §6.2.4).** Alloy steels, Al, Ni/Ti/Mg and composites chapters **not returned** (≈15 %). |
| MG18 | *Magnesium Technology 2018* (D. Orlov, V. Joshi, K.N. Solanki, N.R. Neelameggham eds., TMS/Springer) | https://drive.google.com/file/d/1ZE6TQOXNnemhdi165P__jiKo9GGRVJtQ/view | EN | Skimmed. **Read: full TOC + papers on book pp. 3–~100** (PDF pp. 1–110). |
| MMC18 | *Metal-Matrix Composites: Innovations, Advances and Applications* (T.S. Srivatsan, Y. Zhang, W.C. Harrigan eds., TMS 2018) | https://drive.google.com/file/d/1Ru1LakxdwSSI0o8r_BvToL2Y3cd3I3Kw/view | EN | Skimmed. **Read: TOC + papers book pp. 3–~175** (PDF pp. 1–188). The papers from Sarma (p. 183) onward were not returned. |
| RMT18 | *Rare Metal Technology 2018* (H. Kim et al. eds., TMS) | https://drive.google.com/file/d/1DYRsPSD29mVLtfSNcLMvLvXaev4s4OPb/view | EN | Skimmed. **Read: TOC + book pp. 3–~160.** Extractive metallurgy only, with no Al-alloy papers. |
| HTMP18 | *9th Int. Symp. on High-Temperature Metallurgical Processing* (J.-Y. Hwang et al. eds., TMS 2018) | https://drive.google.com/file/d/1wySzX9KBrTFoD3tBmgrSVLaYk2XWXy3f/view | EN | **The given ID returned empty text.** The text came instead from a byte-identical copy (same size of 35,826,573 B and same date) in *Claude/Metalurgija/TMS 2018*, ID `1oBif3n1WXGDbxiHMyU2og1Q4FInjNwzJ` (not in the excluded folder). **Read: TOC + book pp. 3–~154.** Extractive/ironmaking focus. |
| CFD18 | *CFD Modeling and Simulation in Materials Processing 2018* (L. Nastac et al. eds., TMS) | https://drive.google.com/file/d/1QWHQFOooJUKzdA-stsXlijoq6ccASsal/view | EN | Skimmed. **Read: TOC + book pp. 3–~185.** |
| MPF18 | *Materials Processing Fundamentals 2018* (G. Lambotte, J. Lee, A. Allanore, S. Wagstaff eds., TMS) | https://drive.google.com/file/d/1r1eM2hsO3i-Rj3dYkNQvQT1yUZ5hP6BG/view | EN | Skimmed. **Read: TOC + book pp. 3–~160.** |
| SUP18 | *TMS 2018 147th Annual Meeting & Exhibition Supplemental Proceedings* (TMS) | https://drive.google.com/file/d/1ljrL1I8fg5y2_yzoTFKP5S4z5Ij-dbT9/view | EN | Skimmed. **Read: full TOC (pp. 1–955 listed) but text only for book pp. 3–~190.** Several Al papers appear in the TOC only (see §6.3). |

Not read: anything in the `microstructure-sim-v2.14.0` folder (excluded by instruction).

---

## 1. Transferable alloy-design principles

### 1.1 Solid solutions: what dissolves and what it buys

- **Substitutional vs interstitial.** Mn, Ni and Cr substitute in Fe. H, O, C and N occupy interstitial sites [THI §3.1 p.12–13]. Interstitial solubility depends on the lattice. In the fcc γ-Fe lattice the octahedral hole is larger than in bcc α-Fe, so the maximum C solubility is 2.06 % in γ at 1147 °C, 0.1 % in δ near 1500 °C and 0.02 % in α at 723 °C [THI §3.4 p.15–16].
- **Hume-Rothery rules (general knowledge).** Extensive substitutional solubility needs four things: atomic-size difference ≲15 %, similar electronegativity, the same crystal structure and similar valency. The sources show the consequences:
  - Ni–Cu is completely miscible [EVE p.33].
  - About 30 % Cr dissolves in Ni [EVE p.58].
  - Ba has a radius 1.36 × that of Mg. It is therefore a strong solid-solution strengthener at small additions and also forms Ba–Al/Mg intermetallics for Orowan strengthening [MG18 Dieringa et al. p.7].
  - Ca is chosen to strengthen Mg–Li "due to its significant size mismatch" [MG18 p.63].
- **Solid-solution strengthening as a creep lever.**
  - In ferritic steels, 0.5 % Mo provides "matrix strengthening" and extends useful creep strength to ~450 °C [FAR A–0 p.4–5]. Cr + Mo strengthen the matrix and form carbides that pin grain boundaries and dislocations [FAR A–1 p.6].
  - In Ni, Cr gives oxidation resistance plus solid-solution strengthening [EVE p.58]. Ni–Mo alloys (Hastelloy B ≈ 61Ni–28Mo; C ≈ 54Ni–16Mo–15.5Cr–4W; X ≈ 47Ni–22Cr–18.5Fe–9Mo) are solid-solution strengthened. They keep >50 % of room-temperature (RT) strength to ≥1200 °F (649 °C) [EVE Table 3-9 p.47, p.46, p.50].
  - In superalloys, Re, W and Mo strengthen γ. For creep the ranking is **Re > W > Ta > Cr > Co** [SEG §3.2.3 p.18].
- **Solutes also change stacking-fault energy and plastic anisotropy.** In Mg, density functional theory (DFT) shows that Y's unique effect, compared with Al or Zn, is a large drop in the pyramidal-I stacking-fault energy. Y's effect on the basal I1 fault can be matched by twice as much Al, yet Mg–Al alloys are not ductile. So the "basal-I1" explanation of RE ductility is not supported [MG18 Yin, Wu, Curtin p.15].
- **Interstitial control as a design lever.**
  - Very low C and N enabled weldable, tough supermartensitic stainless steels (C ≈ 0.01) [FAR C–6 p.48–49] and superferritic steels (C ≤ 0.02 plus Ti/Nb ≈ 0.6) [FAR C–7 p.50].
  - In cryogenic Ni steels, C is cut to ~0.1 % because "it is not required for alloy strengthening and has a detrimental effect on toughness" [FAR B–1 p.28].
  - In Ni, 0.02 % C instead of 0.15 % C lowers the work-hardening rate for deep drawing and improves creep above 600 °F [EVE p.8–9, p.20–22].
  - Sulfur, even at normal impurity levels, reduces both hot and cold workability of Ni [EVE p.9].
  - *Al transfer (inference):* the Al equivalent is tight control of Fe and Si and of trace Na/Ca/P for formability and toughness. Treat impurity specification as a design variable, not as given.

### 1.2 Grain size, grain boundaries and grain-boundary engineering

- **Hall–Petch:** σ_HP = k_HP·d^(−1/2). For cryomilled AA5083, **k_HP = 0.165 MPa·m^1/2** (with the Mg solid-solution effect folded in). It gives 274–595 MPa for grain sizes of 77–362 nm and is the dominant term in ultrafine-grained (UFG) Al–Mg/3YSZ composites [MMC18 Dussing et al. p.71ff].
- **Ways to refine grains:**
  - **Solidification:** chilling → undercooling → more nuclei → finer grains. Die castings are therefore finer, tougher and stronger than sand castings [HIG §4.5 p.49–50; THI §3.3 p.14].
  - **Inoculation.** In AZ91, 0.7 % of an extruded Al–30SiC refiner gives grain size 550 → 90 µm, or 670 → 160 µm in industrial ingots, and resists fading for >8 h after remelting [MG18 Bae et al. p.71–77]. In AM60, 1 % AlN nanoparticles give 1277 → 85 µm and TYS 44.9 → 91.2 MPa [MG18 Dieringa p.8].
  - **Melt agitation.** EM or ultrasonic stirring fragments dendrite arms and brings the columnar-to-equiaxed transition earlier [CFD18 Poole & Nastac p.9].
  - **Thermomechanical:** repeated hot deformation plus recrystallisation refines the cast structure [THI §4.6.1 p.34].
  - **Particle pinning** (§1.4).
- **Grain-boundary chemistry:**
  - **B, C, Hf and Zr** are added to polycrystalline superalloys to form grain-boundary carbides and borides. They are removed in single crystals (SX), which raises the melting temperature [SEG p.18].
  - **Ti+B** "have a synergistic effect in stabilising the microstructure" in T24 steel [FAR A–6 p.17].
  - Ti in 430Ti "restricts grain growth and embrittlement in the weld HAZ" [FAR C–2 p.41].
  - In Mg, Ca + Zn segregation raises grain-boundary cohesive energy and lowers slip anisotropy. This gives a compressive fracture strain of 0.40 [MG18 Mukai p.87].
  - Impurities segregate to the last liquid to freeze (interdendritic spaces and grain boundaries), and this embrittles castings [HIG §4.4 p.48].
- **Remove the boundaries altogether.** Single-crystal blades eliminate grain-boundary sliding during creep [SEG §3.1 p.13].
- **Critical-strain coarse grains.** Cold-worked steel recrystallises at 650–750 °C in the HAZ to a grain size that depends on prior strain, coarse at **5–12 %** strain [THI §7.3.2 p.71]. *Al transfer (inference):* this is the same critical-strain coarse-grain trap seen in Al stretching and forming followed by solution treatment.

### 1.3 Precipitation and ordered-particle strengthening

- **Orowan (non-shearable particles)** [MG18 Dieringa et al., eq. 1–2, p.8]:
  - Δσ_OR = (0.13·b·G_m/λ)·ln(d_p/2b), with interparticle spacing λ = d_p·[(1/(2V_p))^(1/3) − 1].
  - b is the Burgers vector, G_m the matrix shear modulus, d_p the particle diameter and V_p the volume fraction.
  - The effect is largest for **randomly distributed particles of 50–200 nm**, and the strength gain scales inversely with mean free path.
- **Coherent L1₂ γ′ in Ni (template for any coherent-precipitate system)** [SEG §3.2.1 p.14–16]:
  - γ′ = Ni₃(Al,Ti,Ta), cubes ≈0.5 µm, γ channels ≈0.1 µm.
  - **Volume fraction 60–70 %. Creep-rupture life peaks near 65 % γ′**, and the effect is stronger in SX than in polycrystals [SEG p.14, p.35].
  - **Lattice misfit δ = 2(a_γ′ − a_γ)/(a_γ′ + a_γ)** (eq. 1, p.16). Small misfit gives cuboidal precipitates and good thermal stability. Because γ′ has the lower expansion coefficient, δ becomes more negative with temperature.
  - Dislocations must cut γ′ in pairs (superdislocations) because of the anti-phase-boundary (APB) penalty [SEG p.16]. Kear–Wilsdorf locks produce the anomalous rise of yield stress up to ~800 °C. Above ~800 °C the APB energy falls and strength drops fast [SEG §3.4.1 p.21–22].
  - Heat treatment changed precipitate shape but not γ′ fraction or composition [SEG p.14]. A CMSX-2 treatment that gave aligned 0.45 µm cuboids raised creep strength [SEG p.36].
- **Metastable strengtheners have a ceiling temperature.** γ″ in IN718 is body-centred tetragonal (BCT), disc-shaped and metastable. It strengthens only up to **650 °C**, then transforms to δ and strength is lost [SEG p.17]. Aged Monel K-500 (Ni₃(Al,Ti)) keeps its advantage only to ~1000 °F (538 °C) [EVE p.40].
- **Shearable nanoclusters give strength without losing ductility.**
  - Cu-rich bcc nanoprecipitates in ferritic steel: ageing at 450–600 °C historically adds **100–200 MPa** YS, with the hardening peak at **2.5–3.0 nm** [MPF18 Zhao et al. p.28].
  - The peak comes after 2 h at 500 °C, 1 h at 550 °C and 30 min at 600 °C (classic C-curve kinetics). After 500 °C/1 h: YS 1135.5 MPa, UTS 1159.8 MPa, El 11.9 %. Fracture stays dimpled and ductile because dislocations cut the Cu clusters [MPF18 p.32–35].
- **Matrix and precipitates can be tuned independently.** In a 1.64 GPa / 14 % El steel, the precipitation contribution (~494 MPa) was the same in hot-rolled and annealed matrices [SUP18 Xu et al. p.157].
- **Ageing usually lowers fatigue endurance ratios.** Monel K-500 rod falls from 0.43 (annealed) to 0.37 (cold drawn) to 0.28 (cold drawn + aged) [EVE Table 3-4 p.39]. Ageing also lowers the endurance ratio of IN718 [EVE p.65]. Long exposure of Hastelloy X at 1500–1600 °F drops Charpy from 54 to 9 ft-lb [EVE Table 3-12 p.49].
- **Precipitation hardening in stainless steel.** 17-4PH (16.5Cr–4Ni–3.5Cu–0.2Nb, C 0.03) reaches proof stress >1100 MPa (≈3 × 300-series) or is over-aged to ~600 MPa. At the highest strengths, toughness falls and **SCC susceptibility rises** [FAR C–4 p.44–45].

### 1.4 Thermally stable dispersoids, the high-temperature lever

- **Particles that do not dissolve keep Orowan strengthening at temperature.**
  - 1100 Al + 8–9 % nano-Al₂O₃ reaches YS 251–260 MPa at RT, against 30–34 MPa for 1100-O [MMC18 Harrigan p.14–15; Zhang et al. Table 1 p.24].
  - At **375 °C after 10,000 h** it keeps 133 MPa, against 11 MPa for 1100-O. At 350 °C, 2618-T6 has only 28 MPa [MMC18 Zhang et al. p.24].
  - Nanocomposites are **4–10 × stronger at 350 °C** than their matrices [MMC18 p.21]. No grain growth occurred after 500 °C/5 h [MMC18 p.21].
- **Carbonitride microalloying in steels.**
  - V, Nb and N additions turn 9Cr–1Mo into P91. For the same duty (600 °C, 30 MPa, 100,000 h) the pipe wall drops from **115 mm (P22) to 77 mm (X20) to 49 mm (P91)** [FAR A–3 Fig. 1 p.11].
  - Adding W (P92/E911) raises creep-rupture strength up to ~30 % above P91 [FAR A–4 p.13]. 12Cr P122 has ~30 % higher allowable stress than P91 at 600 °C [FAR A–8 p.21].
- **Microalloy precipitates also control recrystallisation.** Nb, Ti and V retard austenite recrystallisation during thermomechanical (TM) rolling, which finishes at 900–700 °C [THI §4.6.1 p.34–35]. V, Nb and Ti nitrides/carbides hinder γ grain growth and act as nuclei for transformation. The result is fine grain, higher YS at lower C, and better weldability [THI §6.2.2 p.56].
  - *Al transfer (inference):* this is the direct analogue of Al₃Zr / Al₃(Sc,Zr) / Mn- and Cr-dispersoids for recrystallisation control in 7xxx/6xxx extrusions. Dussing et al. also cite strong Al₃(Sc,Zr) strengthening in Al–Mg [MMC18 p.71ff].

### 1.5 Phase stability: avoiding deleterious phases

- **Topologically close-packed (TCP) phases (σ, µ, P) in Ni superalloys** are promoted by high Cr, Mo, W and Re. **~2 % Ru lowers the TCP precipitation rate** [SEG §3.2.2 p.16]. TCP formation takes Re and W out of the matrix and so lowers creep resistance [SEG p.34, p.36].
- **The alloying ceiling in stainless steel is set by intermetallics.** Superduplex (PREn > 40, plus Cu/W) "probably represent[s] the limit of alloy development". More alloying would cause rapid intermetallic formation in the HAZ and weld metal [FAR D intro p.55]. σ and other intermetallics form quickly at **~400–800 °C** [FAR D–2 p.61].
- **Embrittlement windows to design around:**
  - 475 °C embrittlement of 17–26 % Cr ferritics [FAR C–2 p.41; C–3 p.42].
  - Temper embrittlement of Cr–Mo steels, controlled by low P and As residuals [FAR A–1 p.7].
  - Blue brittleness at 250–350 °C [THI Fig. 29 p.41].
  - Strain ageing after 2–3 % cold work: natural at RT over hundreds of hours to years, artificial at 100–300 °C in minutes to hours [THI p.40].
  - Laves phase in additively manufactured (AM) IN718, which solution treatment plus ageing (STA) turns into δ needles [SUP18 Popovich et al. p.85].
- **Narrow optimum windows for microadditions.** In FeCrAl cladding, 0.02 % Ce gives the best UTS and elongation, and >0.05 % degrades them through excess intermetallics [SUP18 Liu et al. p.61]. In Mg–Ca–Y–Zr, 0.5 % Y gives the finest grains [MG18 You et al. p.91].
- **Austenite-stabiliser balance.**
  - Cr is a ferrite former, and ~17 % Cr with low Ni makes 430 ferritic at all temperatures [FAR C–2 p.40].
  - Co prevents retained δ-ferrite in 12Cr–2.5W–2.5Co creep steels [FAR A–8 p.21].
  - N is the austenite stabiliser that rescued duplex HAZ microstructures [FAR D–1 p.58].
  - The Group E tree builds austenite with "Cr + Ni to form austenite" and "+Mn +N minus Ni for strong austenite" [FAR Group E tree p.~67].
- **Schaeffler / DeLong (general knowledge).** Cr_eq = Cr + Mo + 1.5Si + 0.5Nb; Ni_eq = Ni + 30C + 0.5Mn, and DeLong adds +30N. The diagrams map weld-metal phase (A / A+F / F / M). The Farrar data sheets read here did not print these equations.
- **Electron-vacancy and d-electron methods (general knowledge).** PHACOMP uses the average electron-vacancy number N̄v of the γ matrix after γ′/carbide partitioning. New PHACOMP uses Md̄ = Σ xᵢ·Mdᵢ (metal d-level). Higher values mean higher TCP propensity, and critical values are alloy-family specific. In the sources, this approach appears only as SUP18 TOC items, which were not read: Mostafaei & Abbasi, "incipient melting map and γ′ features … molecular orbital method" p.453, and Sadeghpour et al., "multi-element β-Ti … d-electron method" p.377.
  - *Al transfer (inference):* an Md/Bo-style descriptor has no standard Al analogue. CALPHAD driving-force screening of unwanted phases (Al₇Cu₂Fe, Mg₂Si coarse, β-AlFeSi, S/T phases) plays that role. Note, though, that CALPHAD databases can be wrong: for Mg–Al–Ce, experiment contradicted the published liquidus and a new hexagonal Al₅Ce₂ phase was found [MG18 Wong et al. p.79].

### 1.6 Creep-resistance design rules (cross-family)

1. **Solid solution + stable carbides/carbonitrides + fine dispersoids, layered.**
   - The path runs Mo → Cr–Mo → Cr–Mo–V → 9Cr–Mo–Nb–V–N → +W.
   - Service temperature rises with each step: ~450 °C for 0.5Mo, ~560 °C for P11/P22 (>250,000 h service), ~600 °C for P91/P92, and up to 650 °C for advanced 12Cr [FAR A intro p.3; A–1 p.7; A–3 to A–8].
2. **There is a Cr threshold for rupture strength.** CrMoV steels improve markedly once Cr exceeds 2.25 % [FAR A–5 p.15].
3. **Slow diffusers win.**
   - Re is the main creep element. Up to 1 % Re raises creep and fatigue strength. Re can raise rupture life from 100 h to 1000 h because it diffuses slowly in Ni. 1 nm Re clusters are now considered unlikely to be the cause [SEG §4.2 p.35].
   - From 1st- to 3rd-generation SX alloys (0 → ~3 → ~6 % Re), rupture life rose ~10× at 850 °C/500 MPa and from 250 h to 1000 h at 1050 °C/150 MPa [SEG p.19, p.35–36].
4. **Avoid low-melting or coarsening precipitates at service temperature.**
   - In Mg, β-Mg₁₇Al₁₂ limits creep. Creep alloys are either Al-free (AM-SC1: 1.4–1.9Nd, 0.8–1.2 other RE, 0.4–0.7Zn, 0.3–1.0Zr) or tie Al up in other phases.
   - Gd and Y give an order of magnitude lower minimum creep rate than Nd in Mg–La. The key is the ability to form fine dispersed precipitates [MG18 Dieringa p.6–7].
5. **Cold work does not help above the recrystallisation temperature.**
   - Annealed Monel 400 creeps less than hot-rolled or cold-drawn-and-stress-relieved material at 800–1000 °F [EVE Table 3-6 p.41].
   - Ni–Mo alloys are used annealed above the recrystallisation temperature [EVE p.46].
   - Cold-worked steel strength is lost on heating into the recrystallisation range (welding, fire) [THI §5.6 p.53].
6. **Rafting and morphology** (SX superalloys):
   - Rafting is directional γ′ coarsening, diffusion-controlled near ~900 °C. In CMSX-4 at 100 MPa/1150 °C it completes in 10 h [SEG §3.3 p.19].
   - Negative misfit plus tension gives N-type rafts. The rafting parameter is R = L/(2T), with R = 0.5 for cubes (eq. 2, p.20).
   - Rafted structures lost ~25 % YS. Pre-rafts parallel to the stress improve creep and fatigue [SEG p.20].
7. **Data:**
   - 0.2C steel rupture in 1000 h: 295 MPa at 400 °C, 118 MPa at 500 °C [HIG §3.5 p.37].
   - Low-C Ni (0.02C) at 1000 °F creeps less than 0.15C Ni at 800 °F [EVE p.20–22].
   - Larson–Miller P = T(C + log t_r) is the usual time–temperature parameter (general knowledge).

### 1.7 Corrosion design rules

- **Passivity threshold.** Stainless steel needs **≥10.5 % Cr** and ≤1.2 % C. The passive Cr-oxide film is ~10 atomic layers thick [THI §6.2.4 p.58]. 11–12 % Cr is "just stainless" [FAR C–1 p.38–39].
- **Pitting index:** PREN = Cr + 3.3Mo + 16N (task brief / general knowledge; PREW replaces Mo by Mo + 0.5W, general knowledge). Values in the source:

| Family (FAR sheet) | Typical composition | PRE(N) |
|---|---|---|
| Soft martensitic CA6NM (C–5, p.47) | 0.04C–13Cr–4.5Ni–0.75Mo | 15–21 |
| Lean duplex 2304/UR50 (D–0, p.56) | 23Cr–4.5Ni–0.15N … 22Cr–7Ni–2.5Mo–1.5Cu–0.1N | 26–32 |
| Standard duplex 2205 (D–1, p.58) | 22Cr–5Ni–3Mo–0.17N | ≥35 |
| Superduplex 2507 (D–2, p.60) | 25Cr–7Ni–4Mo–0.25N | >40 (defining criterion) |
| Superferritic AL 29-4C (C–7, p.51) | 0.02C–29Cr–4Mo–0.6(Ti+Nb) | ~40 |

- **A ferrite matrix gives immunity, or high resistance, to chloride stress-corrosion cracking (SCC)** in superferritics and duplex steels [FAR C–7 p.51; D–1 p.59].
- **Strength vs SCC trade-off.** Peak-aged precipitation-hardened stainless steels are "rather sensitive to SCC" [FAR C–4 p.45]. *Al transfer (inference):* this matches the 7xxx T6-vs-T7x over-ageing logic.
- **Self-healing protective layers by alloying.** Weathering steels (Cu, Ni, Cr) form an adherent oxide, but chlorides and poor ventilation prevent it forming. P raises corrosion resistance but destroys weldability [THI §6.2.3 p.58].
- **Mg, a lesson in impurity tolerance:**
  - Heavy-metal impurities dominate Mg corrosion, so keep them below the tolerance limits.
  - Choose alloying elements with small potential difference to the matrix, or film formers (Al, RE), to limit micro-galvanic attack.
  - Electrically decouple Mg in multi-material assemblies [MG18 Dieringa p.9].
  - **Cathodic poisoning** by As, and its non-toxic analogue Ge, lowers corrosion and H₂ evolution. Mg with **>10.5 % Li** forms a protective Li₂CO₃ film [MG18 Birbilis et al. p.17].
  - New inhibitors complex cations of nobler impurities [MG18 p.10].
  - *Al transfer (inference):* for recycled Al, treat Cu and Fe intermetallics as cathodes. Design for low cathodic activity (constituent particle size and chemistry) rather than relying on purity alone.

### 1.8 Carbon equivalent, hardenability and weldability (steels)

- **Effect of alloying on steel properties** [THI §5.2 p.44]:
  - Strength: C ⇑, Mn ↑, V/Nb ↑.
  - Hardenability: C ⇑, Mn ↑, Si ↑.
  - Corrosion: Cr ⇑, Cu+P ↑. Ni, Mo, Cu and Al are also listed as beneficial, but the table layout is garbled.
  - Cold formability: C ↓, Si ↓, P/S ↓.
  - Weldability: C ⇓, Mn ↓.
- **Carbon-equivalent formulas** [THI §7.3.2 p.72; DE text, reconstructed from a scrambled equation layout]:
  - IIW, for C > 0.18 %: **CE = C + Mn/6 + (Cr+Mo+V)/5 + (Ni+Cu)/15**.
  - High-strength or Q&T fine-grain steels: a second formula with terms Mn/10, (Cr+Cu+Mo)/20 and Ni/40. Its exact grouping is garbled; the standard EN 1011-2 **CET = C + (Mn+Mo)/10 + (Cr+Cu)/20 + Ni/40** is general knowledge.
  - Ito–Bessyo, for C < 0.18 %: **C + Si/30 + (Mn+Cu+Cr)/20 + Ni/60 + Mo/15 + V/10 + 5B**.
- **Preheat rule** [THI Table 9 p.72–73]:
  - CE(IIW) < 0.45 needs no preheat.
  - 0.45–0.60 needs 100–200 °C.
  - >0.60 needs 200–500 °C.
  - Unalloyed steel welds without preheat to 0.22 % C [THI p.72].
  - Procedures use **t8/5**, the 800 → 500 °C cooling time. Too low a preheat risks cold cracks; too high a preheat lowers HAZ toughness [THI p.73].
- **The HAZ is a sequence of thermal zones** (cast → coarse γ → fine normalised → intercritical, partly re-hardened → tempering/ageing) [THI Fig. 70 p.71].
  - *Al transfer (inference):* the same zonation (fusion → partially melted → solutionised → over-aged → unaffected) explains 6xxx/7xxx HAZ softening. A local yield-strength map can be computed with the A356 local-heat-treatment framework [MPF18 Holzmann et al. p.77].

### 1.9 Processing levers that cross families

- **Thermomechanical (TM) rolling instead of carbon.**
  - Since ~1985 structural steels have cut C for weldability and recovered strength by TM rolling: microalloying, low finish temperature, accelerated cooling (ACC), quenching and self-tempering (QST), direct quenching (DQ) [THI §4.6.1 p.34].
  - At ~0.2 % C, YS rises from 300–400 MPa (as-rolled) to 500–700 MPa (microalloyed) or 500–1100 MPa (microalloyed, cold work, water cooling or TM) [THI §5.3 p.45].
  - TM steels cannot be hot-formed or heat-treated afterwards without losing properties, and they carry higher residual stresses [THI Table 3 p.35].
- **Strength vs uniform ductility** [THI Table 4 p.46–47]. Every strengthening route lowers Rm/Re:
  - As-rolled: 1.4–1.6.
  - Microalloyed: 1.25–1.40.
  - Water-cooled: 1.15–1.25.
  - Cold-worked: 1.02–1.10.
  - Rebar ductility classes are A (Rm/Re ≥ 1.05, Agt ≥ 2.5 %) and B (≥ 1.08, ≥ 5.0 %) [THI §6.3.1 p.60].
- **Stiffness-limited design.** Higher YS cannot be exploited where E governs (buckling, bending stiffness), and fine-grained steels have the same E as mild steel [THI §6.2.2 p.57]. *Al transfer (inference):* this is the main argument for raising E in Al, via Li or particles (§5).
- **Annealing toolbox** [THI §4.7.2 p.37–38]: stress relief, soft/spheroidise, normalise, recrystallise, coarse-grain (for machinability) and diffusion/homogenise against segregation. Recovery softens without changing grain shape. Recrystallisation (nucleation + growth) erases cold-work effects [THI p.40–41].
- **Melt cleanliness:**
  - Al is the strongest common deoxidiser (Mn < V < Si < Ti < B < Al) [THI §4.4.3.1 p.29].
  - Al-killed steel (≥0.020 % Al, Al:N ≥ 2:1) binds N and so resists ageing [THI p.30].
  - Vacuum treatment removes H, N and volatile Sn, Cu, Pb, Sb [THI §4.4.3.2 p.30].
  - Clean 20MnCr5 raised gear bending-fatigue σF lim by **+37.5 % and +61.4 %** over the reference steel [SUP18 Dugic et al. p.123].
- **Scrap-route residuals.** About 40 % of the Al used in Britain is recycled from drinks cans [HIG §1.6 p.12]. Steel residuals depend "very much on the quantity and quality of scrap" [FAR B–0 p.26]. Electric-arc-furnace (EAF) scrap melting makes Cu, S and P removal harder [THI §4.1 p.22]. *Al transfer (inference):* tramp elements that cannot be refined out (Fe, Cu, Zn in Al) must be tolerated by alloy design, through phase engineering and composition windows, not removed by processing.
- **Casting routes** [HIG §5 p.55–60]:
  - Die casting gives finer grains, but high-shrinkage alloys crack in rigid dies.
  - Semi-solid processing (~50 % solid, stirred, thixotropic) suits wide-freezing-range Al alloys and saves up to 35 % fuel versus die casting.
  - Rapid solidification (~10⁶ °C/s) gives microcrystalline or amorphous structures with no heavy segregation [HIG §4.5.1 p.51].

**Design levers — §1 summary**

| Lever | Mechanism | Anchor |
|---|---|---|
| Solute choice by size mismatch | Solid solution + SFE/anisotropy change | Ba 1.36×Mg [MG18 p.7]; Re>W>Ta>Cr>Co [SEG p.18] |
| Grain size | Hall–Petch | k_HP = 0.165 MPa·m^½ (AA5083) [MMC18 Dussing] |
| Coherent ordered precipitates | Order + misfit | 60–70 % γ′, optimum ~65 %; δ small [SEG p.14–16] |
| Shearable nanoclusters | Strength without ductility loss | Cu clusters peak at 2.5–3.0 nm [MPF18 p.28] |
| Non-dissolving dispersoids | Orowan at high T; grain pinning | 50–200 nm optimum [MG18 p.8]; 4–10× strength at 350 °C [MMC18 p.21] |
| Slow-diffusing solutes | Creep | Re: 100 h → 1000 h rupture [SEG p.35] |
| Deleterious-phase ceilings | TCP/σ, β-Mg₁₇Al₁₂, Laves | σ at 400–800 °C [FAR D–2]; ~2 % Ru [SEG p.16] |
| Interstitial/impurity minimisation | Toughness, weldability, corrosion | C ≈ 0.01 supermartensitic [FAR C–6]; Mg impurity limits [MG18 p.9] |

---

## 2. Steels

### 2.1 Family map (alloy tree)
- Two evolutionary routes start from plain C steel [FAR "How to use" p.xi]:
  - **Left:** low / very-low C for **aqueous corrosion** (martensitic → duplex → austenitic/superaustenitic → Ni alloys).
  - **Right:** controlled / high C for **heat resistance**.
  - Side branches cover creep-resisting low-alloy and cryogenic Ni steels.
- Fe–C basics: the eutectoid is 0.8 % C at 723 °C, and pearlite is 88 % ferrite + 12 % cementite [THI p.17–18]. Steel is ≤2.06 % C [THI p.15].

### 2.2 Creep-resisting low-alloy steels (FAR Group A, pp. 1–21)

| Grade | Key composition | Microstructure (N+T) | Service limit / benefit | Ref |
|---|---|---|---|---|
| P1 | 0.15C–1Mn–0.5Mo–0.05Al | Fine-grained | ≤450 °C; resists H attack | A–0 p.4–5 |
| P11 / P22 | 1.25Cr–0.5Mo / 2.25Cr–1Mo | Tempered bainite, retemper ~690 °C | ≤~560 °C; Cr/Mo carbides pin GBs and dislocations | A–1 p.6–7 |
| P5 / P9 | 5Cr–0.5Mo / 9Cr–1Mo | Bainite / martensite–bainite | ≤600 °C; more Cr adds corrosion and H resistance, not creep | A–2 p.8–9 |
| P91 | 0.1C–9Cr–1Mo–0.08Nb–0.2V–0.05N | Tempered martensite, retemper 760 °C | Wall 49 mm vs 115 mm for P22 at the same duty | A–3 p.10–11 |
| P92 / E911 | P91 + 1.7W–0.5Mo–0.003B / +1W–1Mo | Tempered martensite | Rupture strength up to ~30 % > P91 | A–4 p.12–13 |
| CrMoV | 0.5–3.5Cr–0.5–1Mo–0.25V | Bainite + V carbides | ≤580 °C; marked gain when Cr > 2.25 % | A–5 p.14–15 |
| T23 / T24 | 2.2Cr–1.6W–0.25V–0.05Nb–0.002B / 2.25Cr–1Mo–0.25V–0.07Ti–0.004B | Bainite; C ≈ 0.06–0.07, so no preheat | Rupture ≈ 2 × Gr22 ≈ Gr91 | A–6 p.16–17 |
| X20 | 0.2C–12Cr–1Mo–0.3V | Higher-C martensite | Creep between P22 and P91; H-cracking risk in welding | A–7 p.18–19 |
| P122 | 11.5Cr–0.5Mo–2W–0.06Nb–0.2V–0.06N | Tempered martensite | ~30 % > P91 allowable stress at 600 °C; better oxidation | A–8 p.20–21 |

### 2.3 Cryogenic and structural steels
- **Mn and Ni for low-temperature toughness.** C–Mn steel is usable to −50 °C, 2–3 % Ni to −100 °C and 9 % Ni to −196 °C [FAR B intro p.25].
  - 9 % Ni (0.06C, Q&T lath martensite) gives UTS > 650 MPa, CVN > 100 J and CTOD > 1 mm at −196 °C [FAR B–2 p.31].
  - Matching-composition weld metals cannot reach these values, so Ni-base consumables are used [FAR B–1 p.29; B–2 p.31].
- **Fine-grain structural steels** [THI §6.2.2 p.56–57]:
  - Normalised (N) and TM (M) grades: 275–460 MPa.
  - Q&T (Q) grades: 460–960 MPa.
  - Economical only where the higher YS reduces cross-section.
- **Newer TMS 2018 data:**
  - X100 high-Ni HSLA after TMCP + Q&T: tempering removes retained austenite and raises toughness, with 550 °C best [SUP18 Mousavi Anijdan p.145].
  - Crack-arrest YP460: Ac1 683 °C, Ac3 843 °C, best after 950 °C/1 h [SUP18 Chen et al. p.135].
  - Nano-twinned Fe–12.5Mn–1.2C resists hydrogen embrittlement better, because twins spread internal stress [SUP18 Khedr et al. p.113].

### 2.4 Stainless steels (FAR Groups C–D)
- **Martensitic:** 410/420 (0.1–0.2C–12Cr, air-hardening, proof >1000 MPa, ~45 % of RT strength kept at 600 °C) [FAR C–1 p.39].
- **Soft martensitic** CA6NM: a fine dispersion of stable reverted austenite gives toughness, with proof ≤800 MPa [FAR C–5 p.46–47].
- **Supermartensitic** (0.01C; 11Cr–2Ni lean to 12Cr–6Ni–2.5Mo high): proof ≤850 MPa, meeting X80/X100 [FAR C–6 p.48–49].
- **Ferritic** 430/446: Cr raises oxidation and sulfidation resistance. HAZ grain growth and 475 °C embrittlement limit welding and section size [FAR C–2/C–3 p.40–43].
  - 430Ti (+0.4Ti, Si) has excellent scaling resistance up to ~850 °C and is the exhaust-system grade [FAR C–2 p.41].
- **Duplex:** ~50/50 austenite/ferrite after solution treatment and quench. Strength ≈2 × 316L, with high resistance to chloride SCC [FAR D–0–D–3 p.56–63].
  - Cu and W additions (Zeron 100, DP3W, SD40, UR52N+) widen acid resistance and add ~10 % strength over 2507 [FAR D–3 p.62–63].
- **Additive manufacturing (AM):** DMLS 15Cr–5Ni aged 486 °C/1 h gains ×1.4 in YS and E, +8 % UTS and −42 % work-hardening exponent n, with K_IC ≈ 62 MPa√m [SUP18 Jafarlou et al. p.75].

### 2.5 Nanoprecipitate / ultra-high-strength steels
- Cu-cluster ferritic steel (<0.05C–2Mn–2.5Cu–2Ni–1Al–0.5Mo–0.5Cr–Nb/Ti/B) reaches ~1.1 GPa YS with ductile fracture (§1.3) [MPF18 Zhao et al. p.27–35].
- A 1.64 GPa / 14 % El steel shows that matrix and precipitates can be controlled separately [SUP18 Xu et al. p.157].

**Design levers — steels → Al (all inference unless cited)**
1. **Layered strengthening for creep:** solid solution, then stable carbide, then microalloy carbonitride, then a slow-diffusing heavy element (W). The Al parallel is Mg/Cu solid solution, then Al₃(Zr,Sc,Er) dispersoids, then slow diffusers [FAR A series].
2. **Cut the embrittling interstitial or impurity and recover strength by processing (TM rolling).** In Al this means low Fe/Si plus controlled hot-rolling and extrusion recrystallisation [THI p.34; FAR C–6].
3. **Grade ladders tied to an index** (PREn 26 → 35 → 40) make alloy families legible. A similar index for Al, for example a quench-sensitivity or intergranular-corrosion index, is an open idea [FAR D].
4. **Weldability is a composition budget** (CE < 0.45 needs no preheat). An "Al weldability equivalent" for hot-cracking (Si, Cu, Mg windows) would be the analogue (general knowledge).

---

## 3. Nickel and Ni-base superalloys

### 3.1 Commercial Ni and solid-solution / age-hardenable Ni alloys (Everhart)
- **Pure Ni:**
  - fcc (a = 3.5238 Å), Tm 1453 °C, E ≈ 30,000 ksi (207 GPa), ν = 0.26 [EVE pp. 8–13]. SC Ni elastic anisotropy: E⟨001⟩ 125, E⟨011⟩ 220, E⟨111⟩ 294 GPa, against 207 GPa polycrystalline [SEG §3.5.1 p.24].
  - Hardens only by cold work: annealed 55 ksi → up to 145 ksi [EVE p.13–14]. Work-hardening rate is similar to mild steel [EVE p.16].
  - Fatigue ratio 0.31–0.42 [EVE p.18]. Like other fcc metals it has no ductile–brittle transition [EVE p.23].
- **Ni–Cu (Monel):**
  - Monel 400: 66.5Ni–31.5Cu.
  - **K-500** adds ~3Al–0.6Ti and precipitates Ni₃(Al,Ti) at ~1100 °F (593 °C). UTS reaches 220 ksi; ageing adds ~30 ksi at 60 % cold work [EVE Table 3-1 p.33; pp. 34–37].
  - Cast Ni–Cu uses Si for fluidity: 1.5 % Si gives 75 ksi and 4 % Si gives 150 ksi by precipitation [EVE p.44].
- **Ni–Mo / Ni–Cr–Mo (Hastelloy B, C, N, X)** are solid-solution strengthened and used annealed [EVE pp. 46–57].
- **Ni–Cr (Inconel)** [EVE Table 4-1 p.59–60]:

| Alloy | Ni | Cr | Fe | Al | Ti | Mo | Nb+Ta | Strengthening |
|---|---|---|---|---|---|---|---|---|
| 600 | 76 | 15.5 | 8.0 | – | – | – | – | Solid solution / cold work |
| 601 | 60.5 | 23.0 | 14.1 | 1.15 | – | – | – | Solid solution |
| 625 | 61 | 21.5 | 2.5 | 0.2 | 0.2 | 9.0 | 3.65 | Solid solution (Mo, Nb) |
| 718 | 52.5 | 19.0 | 18.5 | 0.5 | 0.9 | 3.0 | 5.1 | γ″ (Nb) age-hardening |
| X-750 | 73 | 15.5 | 7.0 | 0.7 | 2.5 | – | 0.95 | γ′ Ni₃(Al,Ti) |

- **IN718 design logic.** Nb replaces much of the Al+Ti and Fe replaces Co. This lowers peak high-temperature strength but gives **better weldability** [EVE p.59]. Service limit is 1300 °F (704 °C) [EVE p.59], but γ″ strengthening stops at 650 °C [SEG p.17]. Aged 718 rod/bar: YS 165–180 ksi, UTS 190–210 ksi [EVE Table 4-3 p.62]. Optimum heat treatment: 1700–1850 °F, then 1350 °F/8 h, furnace cool to 1150 °F, 18 h total [EVE p.68].
- **Corrosion-resistant Ni alloys** (Farrar Groups G–J) are listed in the contents [FAR p.vii], but their data sheets were not returned.

### 3.2 Single-crystal γ/γ′ superalloys (Segersäll)
- Superalloys keep good properties above **0.6 Tm**. Ni is fcc with no phase change from RT to 1455 °C [SEG §2.3 p.10].
- Product forms: wrought polycrystalline discs; DS or SX cast blades. SX is used in the first row [SEG p.10].
- **Generations:** 1st has no Re/Ru; 2nd ~3 % Re; 3rd ~6 % Re; 4th Re+Ru [SEG p.19]. CMSX-4 carries 2.9 % Re [SEG Table 1 p.18].
- **Element roles** [SEG p.18]:
  - Al, Ti and Ta form γ′.
  - Re, W and Mo strengthen γ.
  - Al, Cr and Co improve resistance to oxidation, corrosion and sulfidation.
  - Too much Re hardens γ and causes non-uniform oxidation.
- **Anisotropy and orientation:**
  - ⟨001⟩ has the lowest E and therefore the longest strain-controlled fatigue life. Blades are cast ⟨001⟩-up; the secondary orientation is not controlled [SEG §3.1, §4 p.13, p.29].
  - ⟨011⟩ is worst in creep and shows serrated yielding: a single active slip system plus dynamic strain ageing [SEG pp. 25–27, p.42].
  - René N4 YS at RT: 889 MPa ⟨001⟩ vs 830 MPa ⟨011⟩ [SEG p.25–26].
- **Tension/compression asymmetry (non-Schmid):** ⟨001⟩ is stronger in tension. In stress relaxation at 750 °C its creep rate is ~10 × higher in compression [SEG p.23, p.45].
- **Creep behaviour:**
  - SX alloys show little steady-state creep.
  - In ⟨001⟩ CMSX-4, creep rate falls during rafting (complete by 10 h), then accelerates beyond a critical strain of **0.7 ± 0.3 %** [SEG p.36].
  - The 1st-to-3rd-generation gains are given in §1.6.
- **Thermomechanical fatigue (TMF):**
  - Out-of-phase (OP) cycles represent hot spots and are the more damaging. Twinning dominates.
  - Intersecting twins trigger recrystallisation, which shortens TMF life, and cracks follow recrystallisation rather than causing it [SEG pp. 31–34, p.41].
  - TCP phases in aged material blocked twins but took Re and W out of the matrix [SEG p.34].
- **Additive manufacturing of IN718:**
  - A functionally graded part (coarse-grained core, fine-grained shell) gave the best creep–TMF trade-off.
  - STA turns Laves into δ, improves creep and doubles TMF life. Pores dominate the scatter [SUP18 Popovich et al. p.85].

**Design levers — Ni / superalloys → Al**
1. **Optimum precipitate volume fraction plus minimum misfit** gives coarsening resistance. For Al, aim for coherent L1₂ Al₃(Sc,Zr,Er) with small misfit (general knowledge) [SEG p.14–16].
2. **Slow diffusers pay for creep but carry a phase-stability cost** (Re ↔ TCP). Add an antidote element (Ru). The analogue question for Al is which addition delays Al₃Sc coarsening without forming primary Al₃X (open) [SEG p.16, p.35].
3. **Grain-boundary engineering vs boundary removal.** Add B/C/Zr/Hf boundary formers, or remove boundaries (SX) [SEG p.18].
4. **Trade peak strength for processability.** IN718 accepts lower strength from Nb γ″ in return for weldability [EVE p.59]. Al 6xxx-vs-7xxx choices follow the same logic (inference).
5. **Every precipitation strengthener has a ceiling temperature** (γ″ at 650 °C; aged K-500 at ~540 °C). Design to the ceiling of the specific precipitate, not to the alloy family [SEG p.17; EVE p.40].
6. **Texture/orientation is a design variable for fatigue** (lowest E along the load axis) [SEG p.13].

---

## 4. Magnesium alloys

- **Positioning.** Mg is the lightest structural metal, with good damping and electromagnetic (EM) shielding, but faces challenges in primary supply, alloying capacity, formability, reactivity, creep and closed-loop recycling [MG18 Preface p.v]. Its density is 1.74 g/cm³, which is 66 % of Al [MG18 Yang & Lin p.37].
- **Deformation:**
  - Twinning needs more stress than slip and is common in hcp metals [HIG §6.2.4 p.65].
  - Pure Mg has low ductility from strong plastic anisotropy and from a ⟨c+a⟩ → sessile transition [MG18 Yin et al. p.15].
  - Twinning changes the β/matrix orientation relationship and raises the Mg₁₇Al₁₂/matrix interfacial energy by ~250 mJ/m² [MG18 Wang & Li p.55].
- **Texture is the formability bottleneck.**
  - Basal texture limits basal slip and work hardening in AZ31 sheet.
  - **RE or Ca additions weaken or tilt the texture.** Solute or precipitates pin boundaries and change which orientations grow during recrystallisation.
  - ZE10 has higher stretch formability than AZ31 at all temperatures tested [MG18 Dieringa et al. p.3–4].
  - Ca-containing, RE-free twin-roll-cast (TRC) sheets reach ZE10-like textures [MG18 p.6].
  - **TRC Mg–Zn–RE vs AZ31** [MG18 Table 1 p.6]:
    - Mg–Zn–RE: TYS 174/122 MPa (RD/TD), El 26/33 %.
    - AZ31: TYS 130/176 MPa, El 12/11 %.
  - TRC route: 5.6 mm strip → 400 °C/16 h homogenisation → rolling at 400 °C (4 × φ0.1 + 3 × φ0.2) → 2 mm. Grain size goes from 20 µm cast to ~10 µm after 30 min at 400 °C [MG18 p.5].
- **Extrusion:** RE weakens texture, raises ductility and lowers tension/compression yield asymmetry. The process window lies between brittle behaviour and incipient melting (hot cracking) [MG18 p.6].
- **Creep and HPDC alloys:**
  - HPDC alloys contain 4–10 % Al, and β-Mg₁₇Al₁₂ limits their creep.
  - AM-HP2 (3.5 RE + 0.5 Zn) has YS above A380 and creep at 150–175 °C comparable to A380, but low ductility.
  - DieMag422 (4Al–2Ba–2Ca) has a minimum creep rate ~1 order lower than MRI230D at 200 °C/60 MPa. DieMag211/422/633 reach YS 140.6/172.6/202.6 MPa at RT and 111.5/142.6/160.0 MPa at 150 °C [MG18 p.6–9].
  - HPDC Al₈Mn₅ morphology is studied in AM50/AZ91 [MG18 TOC p.137, not read].
- **Grain refinement:** Zr is the most effective refiner for Al-free Mg, but Al poisons it. Use C or SiC inoculation for Al-containing alloys (§1.2) [MG18 Bae et al. p.71].
- **Interface engineering by dissolved O.** O from TiO₂ nanoparticles expands both α-Mg and β, reducing misfit. YS rises from 110 to 143 MPa and K_IC from 10.39 to 12.86 MPa√m [MG18 Kang & Bae p.99].
- **Corrosion** (§1.7). On coatings, Cr(VI)-free conversion coatings are less fault-tolerant, and plasma-electrolytic-oxidation (PEO) porosity aids paint adhesion but not long-term protection [MG18 p.9–10]. ZE41/EZ33 differ by RE precipitate type and film [MG18 AbdelGawad et al. p.43].
- **Production:** Pidgeon/metallothermic reduction with FeSi, Al, Si or CaC₂, with vacuum (~1 mbar) lowering the reaction temperature [HTMP18 Bugdayci et al. p.81].

**Design levers — Mg → Al**
1. **Texture via solute and particles.** Rare earths change recrystallisation-texture selection in Mg. In Al, dispersoid and solute control of cube/Goss/r-value textures is the analogue (inference) [MG18 p.3–4].
2. **Remove the low-melting phase that limits creep, or tie its solute into stable intermetallics** (β-Mg₁₇Al₁₂ → Al–RE / Al–Ba–Ca phases). In Al, Cu/Mg-rich eutectics and low-solvus η limit temperature capability (inference) [MG18 p.6–7].
3. **Inoculant engineering includes delivery.** An extruded master alloy gave even particle distribution and long fade time [MG18 p.71–77]. The parallel is Al–Ti–B / Al–Ti–C refiners (general knowledge).
4. **Twin roll casting as a near-net strip route** with a weak texture as cast [MG18 p.4–5]. It is directly applicable to Al sheet; the TOC also lists *heated TRC Mg strips* [MG18 p.129, not read].

---

## 5. Metal-matrix composites (MMCs)

### 5.1 Evolution and economics (Harrigan, MMC18 pp. 3–17)
- **1970s continuous fibres:**
  - B/Al Space Shuttle truss tubes: compressive strength **2750 MPa** at ⅓ the weight of steel tubes [p.4].
  - Gr/Al Hubble antenna boom: ~zero CTE along the boom, with +100/−150 °C faces [p.5].
  - **The interface was engineered:** a CVD Ti–B coat on the graphite made it spontaneously wettable by molten Al [p.5].
- **1980s SiC whiskers** (0.5 × 10 µm) were dropped for cost and asbestos-like health concerns. Cheap SiC particles + powder metallurgy (PM) gave **isotropic, extrudable, forgeable** MMCs [p.7].
- **Stiffness-driven wins:**
  - U-2 electronics racks: E = 70 GPa (Al), 57.8 (Gr/epoxy), 107.5 (SiC/Al). At equal EI the weight saving was **37.4 %** for the MMC vs 19.2 % for Gr/epoxy [Tables 1–2 pp. 8–9].
  - 6092/SiC/25p extrusions, from 273 tests: **YS 432 ± 17.2 MPa**, normally distributed [p.10].
  - 20 vol% SiC → +20 % modulus → 20 % lighter catamaran beams [p.10–12].
- **The adoption barrier was machinability.** SiC and B₄C dull tools [p.12]. **Spheroidised (melted) alumina** removed sharp corners and avoided the **Mg + Al₂O₃ → spinel** reaction that depletes Mg and kills the heat-treatment response, so standard tools could be used [p.13].
  - CH-53K bearing liners: 2xxx + 20 vol% spherical Al₂O₃, wear ≈ case-hardened steel at ⅓ the density, saving 25 kg [p.13].
- Lesson on cost [p.17]: high-volume "golf-club-shaft" demand is what lowered fibre cost.

### 5.2 Strengthening mechanisms (quantitative)

| Mechanism | Expression / data | Ref |
|---|---|---|
| Orowan | Δσ_OR = 0.13bG_m/λ · ln(d_p/2b); λ = d_p[(1/2V_p)^{1/3} − 1] | MG18 p.8 |
| Load transfer (shear lag) | σ_LT = f_R·σ_R. For 3YSZ (σ_R = 1500 MPa): 33 MPa at 2.2 vol%, 150 MPa at 10 vol% | MMC18 Dussing p.71ff |
| Load transfer (qualitative) | ∝ V_f × matrix YS; needs a clean, defect-free interface | MMC18 Zhang p.22 |
| CTE-mismatch GNDs | α(Al₂O₃) 8.1×10⁻⁶ vs α(Al) 23×10⁻⁶ /°C, cooled from >500 °C | MMC18 Zhang p.22 |
| Hall–Petch | k_HP = 0.165 MPa·m^½ (AA5083); dominant in UFG composites | MMC18 Dussing |
| Orowan not operative | When particle size ≈ grain size (77 nm vs 77 nm) | MMC18 Dussing |
| Rule of mixtures (general knowledge) | Voigt E_c = V_f E_f + (1−V_f)E_m (upper bound); Reuss (lower bound). Check: SiC/Al 107.5 GPa vs Al 70 GPa [MMC18 p.8] | — |

### 5.3 Key data (TMS 2018)
- **Nano-Al₂O₃ (~50 nm) aluminium-matrix nanocomposites (AMnC)** [MMC18 Zhang et al. pp. 19–27]:
  - YS rises linearly with vol% up to ≥12 vol% without agglomeration.
  - At 7.5 vol% the hardness exceeds 7xxx-T6. 6 vol% 2xxx-T6 reaches 107 HRB (+40 %).
  - 2xxx + 6 % Al₂O₃-T6: YS 476, UTS 579 MPa, El 13 %. After 10,000 h at 350 °C: 83/93 MPa.
  - Specific UTS (MPa·cm³/g): 2xxx + 10 % = 250, 7075-T6 = 196, 2024-T6 = 171, 6061-T6 = 115.
  - Good elongation requires cluster-free dispersion and clean interfaces.
- **In-situ Al–TiC** by pneumatic injection of K₂TiF₆ + graphite [MMC18 Gupta et al. p.59]:
  - At 750 °C only Al₃Ti forms; at 950 °C TiC forms.
  - 10 % TiC gives E +15 %. Strength rises and ductility falls roughly linearly. Batch-to-batch hardness varies ±1.1 %.
  - In-situ particles have cleaner interfaces.
- **Cryomilled AA5083 + nano-3YSZ** [MMC18 Dussing et al. p.71]:
  - Grains 77–362 nm.
  - 2.2 vol%: UTS 795 MPa, El 1.84 %.
  - 10 vol%: UCS 611 MPa at 22.5 % strain, with 30 % of strength kept at 400 °C.
- **20 vol% Al₁₈B₄O₃₃ whisker/2024 hot working** [MMC18 Xu et al. p.43]:
  - Q = 286.9 kJ/mol, vs 142 kJ/mol for Al self-diffusion.
  - ε̇ = 5.326×10¹⁸ [sinh(8.4956×10⁻³σ)]^9.978 · exp(−286,900/RT).
  - Safe processing window 460–490 °C, 0.001–0.032 s⁻¹. Dynamic recovery (DRV) and dynamic recrystallisation (DRX) do the softening.
- **CNT wetting:** electroless Cu–Co with colloidal Pd–Sn catalyst. <0.1 % CNT raises Al hardness by +52.1 % [MMC18 Elsharkawi & Esawi p.29].
- **Mg MMCs:** Saffil/AM100 and ZC63 wear less than their matrices against steel. Against SiC abrasive, wear rises again above a certain fibre fraction [MMC18 Jayalakshmi et al. p.135].
- **Ti MMCs:** in SCS-6/Ti-6Al-4V the crack-arrest vs catastrophic-failure transition is governed by the number of intact bridging fibres and falls at 450 °C [MMC18 Stanley et al. p.87].

**Design levers — MMCs → Al**
1. **Choose a reinforcement that is chemically inert toward the matrix's strengthening solutes** (Mg + Al₂O₃ → spinel depletes Mg). Otherwise the composite loses its age-hardening [MMC18 p.13].
2. **The interface decides ductility and load transfer.** Use clean in-situ particles (TiC) or pre-coated reinforcements (Ti–B on C; Cu–Co on CNT) [MMC18 pp. 5, 22, 29, 59].
3. **Nano dispersoids that never dissolve** are the clearest route to Al strength at 300–400 °C [MMC18 p.21–24].
4. **Particle shape controls cost:** spherical particles are machinable [MMC18 p.13].
5. **Raise E where stiffness governs** (SiC/Al 107.5 GPa) [MMC18 p.8; THI p.57].
6. Ultrasound or magnetically induced cavitation de-agglomerates nanoparticles in melts [MG18 p.8; MMC18 TOC p.183, not read].

---

## 6. TMS 2018 highlights relevant to aluminium

### 6.1 Read in full or in part

| Paper (vol., page) | Key finding | Al relevance |
|---|---|---|
| Harrigan, *Aluminum Matrix Composites 1970–2017* (MMC18 p.3) | Fibre → particle → spherical Al₂O₃ → nano-Al₂O₃; 1100 + 8 % nano-Al₂O₃ YS 30 → 260 MPa at RT and 140 MPa at 375 °C (2618: 24 MPa) | High-temperature wrought Al via non-dissolving dispersoids; avoid spinel |
| Zhang et al., *Commercial-Ready … Al Matrix Nanocomposites* (MMC18 p.19) | Scaled PM mixing; linear YS vs vol%; 4–10× strength at 350 °C/10,000 h | Benchmark for "super-aluminium" targets |
| Gupta et al., *In-situ Al–TiC … Pneumatic Powder Injection* (MMC18 p.59) | Al₃Ti → TiC with temperature; +15 % E at 10 % TiC | Scalable melt route for stiffer wrought feedstock |
| Dussing et al., *Cryomilled Al–Mg + nanometric YSZ* (MMC18 p.71) | k_HP = 0.165; 795 MPa UTS but 1.8 % El | UFG strength ceiling and ductility penalty |
| Xu et al., *Al₁₈B₄O₃₃w/2024 processing map* (MMC18 p.43) | Constitutive equation; safe window 460–490 °C | Hot-working windows for MMC extrusion/forging |
| Elsharkawi & Esawi, *Electroless plating of MWCNTs* (MMC18 p.29) | Cu–Co-coated CNTs disperse in molten Al; +52 % HV | Wetting-control strategy |
| Holzmann, Ludwig, Raninger, *Yield strength prediction in 3D during local heat treatment of A356* (MPF18 p.77) | OpenFOAM thermal stress + MatCalc precipitation at tracked points; energy input limited by von Mises and solidus triggers | Ready template for HAZ/local-temper modelling of 6xxx/7xxx |
| Gao et al., *Heat treatment of Al-based anode for air battery* (MPF18 p.99) | Al-0.2Mg-0.2Ga-0.4In-0.15Sn: +300 mV vs pure Al; 1.62 V and ~3180 Wh/kg after 550 °C/12 h | Activation-element design (Ga/In/Sn) for functional Al |
| Wagstaff (editor bio, MPF18 p.xiii) | Turbulent jet erosion cut DC-ingot macrosegregation by >70 % | DC casting of high-solute 7xxx |
| Poole & Nastac, *Coil configuration in EM solidification systems* (CFD18 p.9) | Al 3104; coil translation matters more than turn configuration; EM stirring brings CET earlier | Grain refinement without TiB₂ (scrap-friendly) |
| Chen, Shi, Zhang, *CFD for friction stir welding* (CFD18 p.113) | Coupled heat/mass flow; flow-path history predicts defects | Joining of high-strength Al |
| Mullis et al., *CFD of high-pressure gas atomisation* (CFD18 p.77); Philo et al., L-PBF gas flow (p.65); Shrestha & Chou, SLM (p.85) | Powder sphericity aids flowability; spatter and condensate control; 1600 mm/s scan gives porous tracks | AM-specific Al alloys |
| Kumari et al., *Recovery of REMs from secondary resources* (RMT18 p.53) | 1.5–2.5 t red mud per t alumina (~120 Mt/yr); Sc ~2× enriched vs ore; 1.2 mol HCl/kg leaches >85 % Sc | Sc supply chain for Al–Sc(–Zr) alloys |
| Dieringa et al., *Mg Alloys: Challenges and Achievements* (MG18 p.3) | Texture weakening, TRC, Al-free creep alloys, MMNC Orowan | Cross-light-alloy design analogues (§4) |
| Bae et al., *Grain refinement of AZ91 by carbide inoculation* (MG18 p.71) | Al–30SiC extruded refiner; 550 → 90 µm; fade >8 h | Master-alloy delivery design |
| Zhao et al., *Ageing of a nanoprecipitate-strengthened ferritic steel* (MPF18 p.27) | Peak at 2.5–3 nm Cu clusters; C-curve kinetics | Shearable-cluster design (cf. GP zones) |
| Xu et al., *Matrix microstructure and nanoscale precipitation in UHSS* (SUP18 p.157) | ~494 MPa precipitation strength independent of matrix | Decouple grain/texture control from ageing |
| Dugic et al., *Inclusions and fatigue of case-hardened steel* (SUP18 p.123) | Clean steel +37.5 to +61.4 % σF lim | Melt cleanliness vs fatigue (oxide films in Al) |

### 6.2 Not Al-relevant (skimmed)
- RMT18: REE, PGM, Ga, Li and Mn extraction.
- HTMP18: Cu/Pb smelting, sintering, slags, refractories.
- CFD18: most papers are on steel ladles and continuous casting. The macrosegregation and CET model for 65 t steel ingots, validated by phased-array UT [CFD18 Nastac et al. p.43], is conceptually transferable to DC casting.

### 6.3 Aluminium papers seen in the tables of contents only (text not returned; priority reads)
- **SUP18:**
  - Liao, Wang et al., *Modeling of solute-dependent fluidity and hot tearing sensitivity of conductive aluminum alloys*, p.359.
  - Wang et al., *Die coating thickness vs interfacial heat-transfer coefficient in squeeze casting of Al*, p.341.
  - Fang et al., *Squeeze cast high-strength Al–Si–Cu–Ni–Sr alloys*, p.763.
  - Guo et al., *Hot rolling of B₄C/Al composites*, p.851.
  - Owolabi et al., *UFG 2519 Al*, p.943.
  - Omotosho et al., *Al corrosion in 0.5 M H₂SO₄*, p.909.
  - Siahooei et al., *Al electrolysis cells*, pp. 413 and 721.
  - Dieringa & Hort, *Mg-based MMNCs*, p.679.
  - Mostafaei & Abbasi, *Molecular-orbital incipient-melting map / γ′ for Ni superalloys*, p.453 (Md method).
  - Sadeghpour et al., *β-Ti by d-electron method*, p.377.
- **HTMP18:**
  - Celik, Yücel, Morcali, *Recovery of aluminium and its compounds from non-metallic residue* (dross/salt slag), p.199.
  - Yücel et al., *Exothermic riser sleeve design*, p.345.
  - Fang et al., *Recycling SiO₂ and Al₂O₃ from laterite Ni slag*, p.245.
- **MG18:** Kawalla et al., *Heated TRC Mg strips*, p.129; Zeng et al., *Al₈Mn₅ in HPDC AM50/AZ91*, p.137; Ha et al., *Deformation and recrystallisation in RE-containing Mg sheets*, p.209; *Recrystallization and grain growth behavior of magnesium*, p.275.
- **MMC18:** Sarma et al., *Magnetically induced cavitation for particle dispersion in liquid metals*, p.183; Alipour et al., *Graphene nanoplatelets in Al alloy*, p.233.

---

## 7. Transferable design rules (summary)

| # | Rule | Quantitative anchor | Source | Translation to wrought Al |
|---|---|---|---|---|
| 1 | Grain refinement gives strength and toughness together | k_HP = 0.165 MPa·m^½ (AA5083) | MMC18 Dussing | Use dispersoids + controlled recrystallisation for fine grain; HP is the largest UFG term (inference) |
| 2 | Orowan strength needs fine, closely spaced, non-shearable particles | Δσ = 0.13bG/λ·ln(d/2b); 50–200 nm optimum | MG18 p.8 | Size Mn/Cr/Zr dispersoids and nano-oxides accordingly |
| 3 | Coherent ordered precipitates: optimum fraction and minimum misfit | γ′ 60–70 % (best ~65 %); δ = 2(a′−a)/(a′+a) | SEG p.14–16, 35 | Minimise L1₂ Al₃X misfit for coarsening resistance (general knowledge) |
| 4 | Shearable clusters strengthen without losing ductility; there is a peak size | Cu clusters 2.5–3.0 nm; +100–200 MPa | MPF18 p.28 | GP-zone / pre-ageing design in 6xxx/7xxx (inference) |
| 5 | Matrix and precipitation can be tuned independently | ~494 MPa from precipitation in either matrix | SUP18 p.157 | Optimise texture/grain in TMP, then ageing separately (inference) |
| 6 | Non-dissolving dispersoids give high-temperature strength | 133 MPa at 375 °C/10,000 h vs 11 MPa (1100-O) | MMC18 p.24 | Al–Al₂O₃ / L1₂ dispersoid alloys for 250–400 °C service |
| 7 | Each precipitate has a ceiling temperature | γ″ ≤650 °C; aged K-500 ≈540 °C | SEG p.17; EVE p.40 | Rate Al tempers by precipitate stability, not alloy series (inference) |
| 8 | Slow diffusers buy creep life | Re: 100 h → 1000 h; 10× rupture life 1st → 3rd gen. | SEG p.35–36 | Add Sc/Zr/Er-type slow diffusers to Al (general knowledge) |
| 9 | Too much refractory solute gives brittle intermetallics; set an alloying ceiling | TCP from Cr/Mo/W/Re (Ru mitigates); σ at 400–800 °C at PREn > 40 | SEG p.16; FAR D p.55, 61 | Cap Fe/Mn/Cu/Si totals by constituent-phase fraction (inference) |
| 10 | Microadditions have narrow optima | Ce 0.02 % best, >0.05 % harmful (FeCrAl); 0.5 % Y finest (Mg) | SUP18 p.61; MG18 p.91 | Screen Sc, Zr, Er, Sr and B at fine steps (inference) |
| 11 | Low interstitials/impurities enable toughness and weldability | C ≈ 0.01 (supermartensitic); C ≤ 0.1 for cryogenic Ni steel | FAR C–6, B–1 | Fe/Si limits as design inputs; scrap-tolerant phase design |
| 12 | Strength by TMP instead of composition | YS 300–400 → 500–1100 MPa at the same C | THI p.45 | Strength by TMP/ageing rather than more solute, to keep weldability and recyclability (inference) |
| 13 | Microalloy particles retard recrystallisation | Nb/Ti/V; finish rolling 900–700 °C | THI p.34–35 | Zr/Sc/Mn dispersoids for unrecrystallised extrusion/plate |
| 14 | Weldability is a composition budget | CE(IIW) < 0.45, no preheat; t8/5 controls the HAZ | THI p.72–73 | Define an Al HAZ/hot-cracking index (open) |
| 15 | Corrosion ladders follow an index | PREn 15–21 → 26–32 → ≥35 → >40 | FAR C–5, D–0–D–2 | Build an IGC/SCC index for Al alloys (open) |
| 16 | Peak strength often raises SCC susceptibility | 17-4PH at >1100 MPa is SCC-sensitive | FAR C–4 p.45 | Over-age (T7x) logic; Cu/Zn/Mg ratio windows (general knowledge) |
| 17 | Cold work is useless above the recrystallisation temperature for creep | Annealed Monel creeps less than cold drawn | EVE Table 3-6 | Don't rely on H-tempers for high-T Al parts (inference) |
| 18 | Critical strain gives coarse recrystallised grains | 5–12 % strain → coarse grain at 650–750 °C (steel) | THI p.71 | Avoid 2–10 % local strains before solution heat treatment (inference) |
| 19 | Texture is a design variable (fatigue, formability) | ⟨001⟩ E = 125 vs 294 GPa ⟨111⟩; RE texture doubles Mg El | SEG p.24; MG18 p.6 | Cube/r-value texture control in Al sheet (general knowledge) |
| 20 | Grain refinement through inoculant delivery and agitation | Mg 550 → 90 µm; AlN 1277 → 85 µm; EM stirring brings CET earlier | MG18 p.8, 71; CFD18 p.9 | Scrap-tolerant refining (EM/US) when TiB₂ is poisoned (inference) |
| 21 | Reinforcement must not consume matrix strengtheners | Mg + Al₂O₃ → spinel kills ageing | MMC18 p.13 | Choose inert reinforcements or offset Mg loss |
| 22 | Where E governs, raise E, not YS | SiC/Al 107.5 GPa → 37 % weight saving at equal EI | MMC18 p.8; THI p.57 | Al–Li or particle-stiffened Al for stiffness-limited parts |
| 23 | Melt cleanliness is a fatigue lever | +37.5 to +61 % gear fatigue | SUP18 p.123 | Filtration and oxide-film control in DC casting (inference) |
| 24 | Tramp residuals from scrap must be designed around | EAF route: Cu, S, P hard to remove | THI p.22; FAR B–0 | Fe/Cu-tolerant compositions for high-recycled-content Al |

---

## 8. Open questions / gaps

1. **Truncation.** Several primary sections were never returned:
   - FAR Groups E–J and Appendix 5 (role of individual elements) and Appendix 6 (types of corrosion).
   - EVE Ch. 5 (superalloys) and the stainless and age-hardenable chapters.
   - HIG chapters on alloy steels, Al, Ni/Ti/Mg and composites.
   - THI Ch. 10–11 (Al properties, corrosion).
   - Next step: re-read these by page range, or from a local PDF if one becomes available.
2. **The PREN, Schaeffler/DeLong and Md/Nv formulas are general knowledge here.** They are not cited from the text read. FAR App. 5/6 and the SUP18 molecular-orbital papers (pp. 377, 453) should confirm coefficients and critical values.
3. **The CET grouping is reconstructed** from scrambled German text [THI p.72] and needs checking against EN 1011-2.
4. **No Fe-tolerance or recycled-content Al alloy design paper** was in the returned TMS text. The relevant items (HTMP18 p.199 dross recovery; SUP18 p.359 fluidity/hot tearing) are TOC-only. This is the largest gap for the project's sustainability goal.
5. **No recrystallisation-modelling paper for Al** was found in the returned text. The MG18 recrystallisation papers (pp. 209, 275) and CFD18 DC-casting items need reading.
6. **Transfer hypotheses to test:**
   - Can an Md-type d-electron descriptor rank TCP-like constituent-phase risk in multicomponent recycled Al?
   - Is there an Al analogue of Ru, an element that delays coarsening or harmful-phase formation of L1₂ Al₃(Sc,Zr) without forming primary phases?
   - Can EM/ultrasonic grain refinement replace TiB₂ in high-Zr or high-Si scrap-based melts, where TiB₂ poisoning is reported in general knowledge?
   - Would a PREn-style index (for example from Cu, Zn/Mg and Fe-intermetallic fraction) predict IGC/SCC ranking within 7xxx?
7. **The superalloy compositions table** (SEG Table 1) is mis-aligned in the extraction. Only Re levels are trusted. Re-extract before using compositions.
8. **The HTMP18 Drive ID returned empty text.** A byte-identical copy (`1oBif3n1WXGDbxiHMyU2og1Q4FInjNwzJ`) was used. Confirm that it is the intended file, or clean up the duplicate.
