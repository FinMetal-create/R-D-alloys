# 08 — Other alloy families & general physical-metallurgy principles (transfer to wrought Al)

**Scope.** Distils steels (low-alloy creep and cryogenic steels, structural/HSLA, stainless, nanoprecipitate/AHSS), Ni and Ni-base superalloys, Mg alloys and metal-matrix composites (MMCs) into **design principles that transfer to wrought-aluminium alloy design**. It also skims the TMS 2018 proceedings for aluminium-relevant results. It is not a full handbook of these families. It keeps only the mechanisms, quantitative anchors and "levers" useful for designing better wrought Al alloys.

**Conventions.** `[REF, p./§]` = source citation (page numbers are the printed book pages unless noted "PDF p."). **(general knowledge)** = not in the sources read here. Keep these minimal and verify them before quantitative use. **(inference)** = my reasoning that carries a source result over to Al. It is a hypothesis to test, not a source fact. Compositions are in wt% unless stated otherwise.

**Status.** Extracted 2026-10-12. The Drive text reader truncated every source. **Full-text pass 2026-10-12:** FAR, EVE and THI were then downloaded whole as PDFs (byte sizes match the Drive metadata), converted locally with `pdftotext -layout` and read in full. Coverage of the other sources is still partial (see table). German text is translated to English. Items changed by the full-text pass are marked **[FT 2026-10-12]**. Statements that the full text showed to be wrong are marked "corrected after full-text pass".

## Sources

| Ref | Title (author/editor, year) | Drive link | Lang. | Readability / coverage actually read |
|---|---|---|---|---|
| FAR | *The Alloy Tree: A Guide to Low-alloy Steels, Stainless Steels and Nickel-base Alloys* (J.C.M. Farrar, Woodhead/CRC 2004) | https://drive.google.com/file/d/1DI6Ec7thYXVhQ_z0ApTBihCCkJy3Heve/view | EN | **Full text read [FT 2026-10-12]**: PDF downloaded whole (206 PDF pages, 735,221 B, clean text layer). Read: front matter, Groups A–J data sheets (pp. 1–171), App. 1 (abbreviations, incl. the PRE formulas), App. 2–3, App. 4 (alloying costs), App. 5 (role of elements) and App. 6 (types of corrosion), pp. 172–186. **The book prints no Schaeffler, DeLong or WRC diagram and no Cr/Ni-equivalent formula anywhere** (full-text search). Earlier pass: Groups A–D only. |
| EVE | *Engineering Properties of Nickel and Nickel Alloys* (J.L. Everhart, Plenum/Springer 1971) | https://drive.google.com/file/d/1yPxmtJr-sKsxhNlEpkEl6xINfBRUg2k_/view | EN | **Full text read [FT 2026-10-12]**: PDF downloaded whole (240 PDF pages, 4,968,962 B, CVISION OCR text layer). Read: Ch. 1–11 (pp. 1–218) and the appendices. Graph axes are OCR-garbled, so numbers are taken only from the prose and tables. Units are imperial (ksi, °F); SI conversions in this chapter are mine. Earlier pass: Ch. 1–3 and Ch. 4 to p. 68. |
| SEG | "Nickel supper alloys.pdf" = M. Segersäll, *Nickel-Based Single-Crystal Superalloys – the crystal orientation influence on high temperature properties*, Linköping Lic. Thesis 1568 (2013) | https://drive.google.com/file/d/1d1gAovTKmXwAhqINacTcB-qS5fyz6aYT/view | EN | Clean LaTeX text. **Read: complete Part I (pp. 1–56) and bibliography.** Part II appended papers (p. 57+) **not returned**. The tables of alloy compositions are partly mis-aligned in the extraction, so only Re levels are quoted. |
| THI | *Werkstoffe I – Chemie und Eigenschaften metallischer Werkstoffe – Stahl und NE-Metalle* (K.-Ch. Thienel, lecture notes, UniBw München, HT 2017) | https://drive.google.com/file/d/13ighAAUOs8kif9PuB8fWFy2mkyR3MYH_/view | **DE → EN** | **Full text read [FT 2026-10-12]**: PDF downloaded whole (114 PDF pages, 3,795,647 B, good text layer). Read: Ch. 1–12 (pp. 1–114), incl. Ch. 10 non-ferrous metals (Al pp. 80–89, Cu pp. 89–93, Zn pp. 93–95) and Ch. 11 corrosion (pp. 96–112). The equations are embedded objects that `pdftotext` scrambles. The carbon-equivalent formulas were verified from the word bounding boxes (`pdftotext -bbox`, PDF p. 72). Table 13 (the six DIN 4113 Al alloys) and Bild 85 (Al alloy overview) are images with no text layer, so they could not be read (no OCR available). Earlier pass: pp. 1–80. |
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
  - Ni–Cu is completely miscible [EVE p.33; FAR J–1 p.166, App. 5 p.182].
  - About 30 % Cr dissolves in Ni [EVE p.58].
  - **The solvent sets the alloying ceiling [FT 2026-10-12].** Ni "can accommodate into solid solution larger quantities of critical elements such as chromium, molybdenum, tungsten … than can iron" [FAR App. 5 p.182]. Mo up to almost 30 % fits in Ni-base alloys, but "there are limits as to how much can be accommodated in the iron-base matrix" [FAR App. 5 p.183; J–3 p.170]. The highest-Mo stainless grade in the book carries 7.5 % Mo (654 SMO) [FAR F–4 p.90]. This is why the most corrosion-resistant grades leave the Fe base for the Ni base [FAR F intro p.81; G intro p.99]. *Al transfer (inference):* Al has a low equilibrium solubility for most transition metals (Mn, Fe, Cr, Zr, Sc). The usable "ceiling" is therefore set by primary-intermetallic formation during casting, not by the solid-solution limit at the homogenisation temperature.
  - Ba has a radius 1.36 × that of Mg. It is therefore a strong solid-solution strengthener at small additions and also forms Ba–Al/Mg intermetallics for Orowan strengthening [MG18 Dieringa et al. p.7].
  - Ca is chosen to strengthen Mg–Li "due to its significant size mismatch" [MG18 p.63].
- **Solid-solution strengthening as a creep lever.**
  - In ferritic steels, 0.5 % Mo provides "matrix strengthening" and extends useful creep strength to ~450 °C [FAR A–0 p.4–5]. Cr + Mo strengthen the matrix and form carbides that pin grain boundaries and dislocations [FAR A–1 p.6].
  - In Ni, Cr gives oxidation resistance plus solid-solution strengthening [EVE p.58]. Ni–Mo alloys (Hastelloy B ≈ 61Ni–28Mo; C ≈ 54Ni–16Mo–15.5Cr–4W; X ≈ 47Ni–22Cr–18.5Fe–9Mo) are solid-solution strengthened. They keep >50 % of room-temperature (RT) strength to ≥1200 °F (649 °C) [EVE Table 3-9 p.47, p.46, p.50].
  - In superalloys, Re, W and Mo strengthen γ. For creep the ranking is **Re > W > Ta > Cr > Co** [SEG §3.2.3 p.18].
  - **Nitrogen in austenite [FT 2026-10-12].** Raising N from ~0.05 % to ~0.15 % in 304L/316L raises the specified minimum yield strength by about 30 %. The real gain is only about 15 %, because standard 304L already exceeds its specified minimum comfortably [FAR F intro p.81]. With ~0.5 % N (654 SMO, UR B66) the 0.2 % proof stress is about 30 % above the 6 % Mo superaustenitics and comparable with 22Cr duplex [FAR F–4 p.91].
- **Solid solution costs conductivity [FT 2026-10-12].** In Cu–Ni the resistivity rises with Ni: 115, 163 and 225 Ω·cmil/ft for 10, 20 and 30 % Ni (≈19, 27 and 37 µΩ·cm), and 300 Ω·cmil/ft (≈50 µΩ·cm) at 45 % Ni [EVE Table 6-2 p.102]. Nickel silvers measure 115–189 Ω·cmil/ft, against 38 (≈6.3 µΩ·cm) for yellow brass [EVE p.115]. *Al transfer (inference):* this is the same trade-off that Mn in solid solution imposes on 3xxx conductivity, and it is why conductor and heat-exchanger alloys strengthen with particles rather than solute (§1.4).
- **Solutes also change stacking-fault energy and plastic anisotropy.** In Mg, density functional theory (DFT) shows that Y's unique effect, compared with Al or Zn, is a large drop in the pyramidal-I stacking-fault energy. Y's effect on the basal I1 fault can be matched by twice as much Al, yet Mg–Al alloys are not ductile. So the "basal-I1" explanation of RE ductility is not supported [MG18 Yin, Wu, Curtin p.15].
- **Interstitial control as a design lever.**
  - Very low C and N enabled weldable, tough supermartensitic stainless steels (C ≈ 0.01) [FAR C–6 p.48–49] and superferritic steels (C ≤ 0.02 plus Ti/Nb ≈ 0.6) [FAR C–7 p.50].
  - In cryogenic Ni steels, C is cut to ~0.1 % because "it is not required for alloy strengthening and has a detrimental effect on toughness" [FAR B–1 p.28].
  - In Ni, 0.02 % C instead of 0.15 % C lowers the work-hardening rate for deep drawing and improves creep above 600 °F [EVE p.8–9, p.20–22].
  - Sulfur, even at normal impurity levels, reduces both hot and cold workability of Ni [EVE p.9].
  - **Carbon sets a service ceiling in pure Ni [FT 2026-10-12].** Alloy 200 (C ≤ 0.15 %) graphitises during long exposure and is limited to below ~300 °C. Alloy 201 (C ≤ 0.02 %) does not, and is usable to ~650 °C [FAR J–0 p.165].
  - **Low C + Si to keep weld HAZs clean.** The original Hastelloy C and B had C and Si levels high enough to form intermetallics and grain-boundary precipitates in weld HAZs. The very-low-C/Si C-276 and B-2 grades fixed this and can be used as-welded [FAR G–1 p.102; G–2 p.104–105; J–3 p.170–171]. Si is kept as low as possible in complex Ni alloys to avoid detrimental intermetallics [FAR App. 5 p.181].
  - **P cannot be refined out of Cr-bearing melts.** Cr oxidises in preference to P, so stainless steels carry 0.01–0.02 % P. Where temper embrittlement matters, P is held below 0.01 % "by careful selection of raw materials and recycled scrap" [FAR App. 5 p.184]. This is a direct precedent for controlling an unrefinable residual through scrap selection (§1.9).
  - *Al transfer (inference):* the Al equivalent is tight control of Fe and Si and of trace Na/Ca/P for formability and toughness. Treat impurity specification as a design variable, not as given.

### 1.2 Grain size, grain boundaries and grain-boundary engineering

- **Hall–Petch:** σ_HP = k_HP·d^(−1/2). For cryomilled AA5083, **k_HP = 0.165 MPa·m^1/2** (with the Mg solid-solution effect folded in). It gives 274–595 MPa for grain sizes of 77–362 nm and is the dominant term in ultrafine-grained (UFG) Al–Mg/3YSZ composites [MMC18 Dussing et al. p.71ff].
- **Grain size in the 15–70 µm range (a datum in the user's slug window) [FT 2026-10-12].** Annealed nickel silver CA 745 (65Cu–10Ni–Zn) flat product: grain size 0.070 mm gives UTS 49 ksi (≈338 MPa) and El 49 %; 0.015 mm gives UTS 60 ksi (≈414 MPa) and El 36 %. "Generally, the larger the grain, the softer the material" [EVE p.117]. The implied slope is ≈0.55 MPa·m^½ on UTS (my calculation, fcc Cu-base). It is not transferable to Al numerically, but the direction matches the 20–100 µm slug window: coarser grain gives a softer slug.
- **Coarse grain for creep [FT 2026-10-12].** A solution anneal at 2050 °F (1121 °C) coarsens the grain of Incoloy 800 and 804 and "markedly improves the creep and rupture properties". For alloy 800, the stress for 0.0001 %/h at 1600 °F (871 °C) more than doubles. For alloy 804 the 100-h rupture stress at 1400 °F (760 °C) rises from 6.2 to 12.5 ksi (≈43 → 86 MPa). At 1800 °F and only 1 ksi, the advantage vanishes: 29,026 h (mill-annealed) vs 29,460 h [EVE p.77–79, Table 4-14]. Alloy 800HT is specified with **minimum grain-size limits** [FAR I–0 p.149]. Grain size is therefore a strength/creep trade-off whose sign depends on temperature and stress.
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
  - **γ′ itself has a ceiling [FT 2026-10-12].** γ′-hardened wrought superalloys "are very strong within the temperature range in which the precipitated phase is stable". Above ~1800 °F (982 °C) the precipitates begin to dissolve and strength falls rapidly [EVE p.85]. In short-time tests they keep much of their RT strength to ~1200 °F (649 °C) but only ~40 % at 1600 °F (871 °C) [EVE p.89].
- **More precipitate former buys temperature, and short-time tests hide it [FT 2026-10-12].** Above 1200 °F the short-time tensile strengths of five wrought γ′ alloys were indistinguishable, yet rupture strength rose steadily with Al + Ti [EVE p.89]:
  - M-252 (3.6 % Al+Ti): 1000-h rupture strength 10 ksi (≈69 MPa) at 1600 °F.
  - Nimonic 115 (9 % Al+Ti): 27 ksi (≈186 MPa) at 1600 °F. Its 1000-h strength at 1800 °F almost equals M-252's at 1600 °F, a ~110 °C gain in useful temperature.
  - Cast alloys show the same trend: the 1000-h/1500 °F rupture stress rises from 33.5 ksi (GMR-235D) to 56 ksi (IN-100), about +75 %. Adding W matrix strengthening on top (MAR-M200, MAR-M246) gives 60–62 ksi [EVE Table 5-8 p.98–99].
  - Co is added to MAR-M200 "to increase the solvus temperature of the gamma-prime phase" [EVE p.94]. B and Zr improve creep and hot workability [EVE p.82].
  - *Al transfer (inference):* rank heat-resistant Al alloys by creep/stress-rupture tests, not by short-time hot tensile tests. A solute that raises the solvus of the strengthening phase is a separate lever from one that raises its volume fraction.
- **Precipitation costs less ductility than cold work [FT 2026-10-12].** Ni-Span Hi: ageing from the solution-annealed state almost doubles strength with only a moderate drop in elongation. Cold work gives almost the same strength but "drastically" reduces ductility [EVE p.184–185]. Ni-Span C: ageing alone triples YS and doubles UTS "while retaining good ductility" [EVE p.188–189]. *Al transfer (inference):* where formability after strengthening matters, a precipitation route (T-temper) preserves more elongation than a work-hardened H-temper of equal strength.
- **Over-ageing for toughness.** Berylco Nickel 440 aged to peak reaches UTS 225 ksi (≈1550 MPa). Over-aged for maximum impact energy it has 151 ksi (≈1040 MPa) [EVE p.211]. The 17-4PH SCC trade-off in §1.7 is the same logic.
- **Service inside the ageing range keeps ageing [FT 2026-10-12].** Precipitation-hardening stainless steels are used at 600–1000 °F (316–538 °C). Because that range overlaps their ageing range, "additional aging may occur in service" [EVE p.148]. Alloy 625 loses ductility and toughness during long-term exposure around 700 °C as precipitates form and grow [FAR G–0 p.101].
- **Resistivity tracks precipitation.** Ageing lowers resistivity because solute leaves solution. Duranickel 301 falls from 273 to 259 Ω·cmil/ft (≈45 → 43 µΩ·cm) [EVE p.204]. Martensitic PH stainless Stainless W shows the same effect [EVE p.146]. *Al transfer (general knowledge):* electrical-conductivity tracking of Mn or Mg₂Si precipitation is standard Al practice.
- **Shearable nanoclusters give strength without losing ductility.**
  - Cu-rich bcc nanoprecipitates in ferritic steel: ageing at 450–600 °C historically adds **100–200 MPa** YS, with the hardening peak at **2.5–3.0 nm** [MPF18 Zhao et al. p.28].
  - The peak comes after 2 h at 500 °C, 1 h at 550 °C and 30 min at 600 °C (classic C-curve kinetics). After 500 °C/1 h: YS 1135.5 MPa, UTS 1159.8 MPa, El 11.9 %. Fracture stays dimpled and ductile because dislocations cut the Cu clusters [MPF18 p.32–35].
- **Matrix and precipitates can be tuned independently.** In a 1.64 GPa / 14 % El steel, the precipitation contribution (~494 MPa) was the same in hot-rolled and annealed matrices [SUP18 Xu et al. p.157].
- **Ageing usually lowers fatigue endurance ratios.** Monel K-500 rod falls from 0.43 (annealed) to 0.37 (cold drawn) to 0.28 (cold drawn + aged) [EVE Table 3-4 p.39]. Ageing also lowers the endurance ratio of IN718 [EVE p.65]. Long exposure of Hastelloy X at 1500–1600 °F drops Charpy from 54 to 9 ft-lb [EVE Table 3-12 p.49].
  - **More data [FT 2026-10-12]:** Duranickel 301's endurance ratio is "considerably lower" aged than unaged, whether aged after hot rolling or after cold drawing [EVE p.208].
  - Process route matters as much as ageing. Incoloy 800 endurance ratio: hot rolled 0.51, annealed 0.38, cold drawn 0.29 [EVE p.76].
  - Cold work raises fatigue strength less than it raises UTS. Annealed 70/30 Cu–Ni: 25 ksi at 10⁸ cycles (UTS 58.5 ksi). Cold drawn: 33 ksi (UTS 87.3 ksi) [EVE p.105].
  - For comparison, annealed austenitic stainless steels have endurance ratios of 0.40–0.48 (0.32–0.33 for 301 and 310, 0.54 for 216), and they are not notch-sensitive. A 60° notch even raised the endurance limit of 304 from 36 to 43 ksi [EVE p.137–138].
- **Precipitation hardening in stainless steel.** 17-4PH (16.5Cr–4Ni–3.5Cu–0.2Nb, C 0.03) reaches proof stress >1100 MPa (≈3 × 300-series) or is over-aged to ~600 MPa. At the highest strengths, toughness falls and **SCC susceptibility rises** [FAR C–4 p.44–45].

### 1.4 Thermally stable dispersoids, the high-temperature lever

- **Particles that do not dissolve keep Orowan strengthening at temperature.**
  - 1100 Al + 8–9 % nano-Al₂O₃ reaches YS 251–260 MPa at RT, against 30–34 MPa for 1100-O [MMC18 Harrigan p.14–15; Zhang et al. Table 1 p.24].
  - At **375 °C after 10,000 h** it keeps 133 MPa, against 11 MPa for 1100-O. At 350 °C, 2618-T6 has only 28 MPa [MMC18 Zhang et al. p.24].
  - Nanocomposites are **4–10 × stronger at 350 °C** than their matrices [MMC18 p.21]. No grain growth occurred after 500 °C/5 h [MMC18 p.21].
- **The Ni precedent: TD Nickel vs γ′ superalloys [FT 2026-10-12].** TD Nickel is Ni + 2.2 % ThO₂, made by powder metallurgy (aqueous reduction with a thoria sol, compaction, H₂ sintering, rolling, annealing). It is hardened by "stable, insoluble particles" rather than by γ′ [EVE Table 5-1 p.84; p.85, p.89]:
  - At RT it is much weaker: YS 48–87 ksi (≈330–600 MPa), against 97–154 ksi (≈670–1060 MPa) for the aged γ′ alloys [EVE Table 5-3 p.88]. In short-time tests it keeps only ~25 % of its RT strength at 1600 °F [EVE p.89].
  - In long-time tests it wins. Its 1000-h rupture strength at 2000 °F (1093 °C) equals that of Nimonic 115 at 1800 °F (982 °C), "a very significant advance" [EVE p.90]. In jet-engine burner-can service tests it beat Hastelloy X "by a wide margin" after 151 h [EVE p.90–91].
  - It is thermally stable: Charpy V fell only from 34 to 30 ft-lb (≈46 → 41 J) after 100 h at 2400 °F (1316 °C) [EVE p.89].
  - **It keeps the conductivity of the pure matrix.** Thermal conductivity is 48 Btu/h·ft·°F (≈83 W/m·K) against 5.2–6.8 (≈9–12 W/m·K) for the γ′ alloys. Resistivity is 46 Ω·cmil/ft (≈7.6 µΩ·cm) against 722–803 (≈120–133 µΩ·cm) [EVE Table 5-2 p.86].
  - Its modulus is lower than wrought Ni (22,000 vs ~30,000 ksi), comparable with cast Ni [EVE p.85, Table 5-2].
  - *Al transfer (inference):* this is the same trade that 1100 + nano-Al₂O₃ shows in MMC18. Insoluble dispersoids give up RT strength in exchange for strength at the temperature where precipitates dissolve, and they leave the matrix nearly solute-free and conductive. For Al heat exchangers and conductors that must keep strength after brazing or at 200–350 °C, this is the argument for dispersoids (Al₃Zr, Al–Al₂O₃) over more solute.
- **Layer solid solution behind the particles [FT 2026-10-12].** In cast 22H/Supertherm heat-resistant alloys, Co and W are added "to maintain matrix strength at temperatures where carbides begin to dissolve" [FAR H–9 p.138]. HP40Nb adds Nb to form a network of stable carbides. Ti/Zr microalloying then adds "secondary networks of fine carbides". The result is +50 % 100,000-h rupture life at 1000 °C over HK40, and the microalloyed versions add another 5–10 % [FAR H–8 p.136–137]. Gains are temperature-specific. Alloy 35/45 gives ~30 % more rupture stress at 1100 °C but no real gain below ~1000 °C [FAR H–10 p.141].
- **Carbonitride microalloying in steels.**
  - V, Nb and N additions turn 9Cr–1Mo into P91. For the same duty (600 °C, 30 MPa, 100,000 h) the pipe wall drops from **115 mm (P22) to 77 mm (X20) to 49 mm (P91)** [FAR A–3 Fig. 1 p.11].
  - Adding W (P92/E911) raises creep-rupture strength up to ~30 % above P91 [FAR A–4 p.13]. 12Cr P122 has ~30 % higher allowable stress than P91 at 600 °C [FAR A–8 p.21].
- **Microalloy precipitates also control recrystallisation.** Nb, Ti and V retard austenite recrystallisation during thermomechanical (TM) rolling, which finishes at 900–700 °C [THI §4.6.1 p.34–35]. V, Nb and Ti nitrides/carbides hinder γ grain growth and act as nuclei for transformation. The result is fine grain, higher YS at lower C, and better weldability [THI §6.2.2 p.56].
  - *Al transfer (inference):* this is the direct analogue of Al₃Zr / Al₃(Sc,Zr) / Mn- and Cr-dispersoids for recrystallisation control in 7xxx/6xxx extrusions. Dussing et al. also cite strong Al₃(Sc,Zr) strengthening in Al–Mg [MMC18 p.71ff].

### 1.5 Phase stability: avoiding deleterious phases

- **Topologically close-packed (TCP) phases (σ, µ, P) in Ni superalloys** are promoted by high Cr, Mo, W and Re. **~2 % Ru lowers the TCP precipitation rate** [SEG §3.2.2 p.16]. TCP formation takes Re and W out of the matrix and so lowers creep resistance [SEG p.34, p.36].
- **The alloying ceiling in stainless steel is set by intermetallics.** Superduplex (PREn > 40, plus Cu/W) "probably represent[s] the limit of alloy development". More alloying would cause rapid intermetallic formation in the HAZ and weld metal [FAR D intro p.55]. σ and other intermetallics form quickly at **~400–800 °C** [FAR D–2 p.61]. The same ceiling applies on the austenitic side [FT 2026-10-12]. The highest-alloyed superaustenitics "probably represent the limit of development", and further gains need a Ni base [FAR F intro p.81]. PREn ≈ 55 "is about as high as is achievable with stainless steels" [FAR F–4 p.91].
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
  - The Group E tree builds austenite with "Cr + Ni to form austenite" and "+Mn +N minus Ni for strong austenite" [FAR Group E tree p.66; page corrected after full-text pass, previously "p.~67"].
  - **More from the full text [FT 2026-10-12]:**
    - Mo is a ferrite former, so 316 needs more Ni than 304 to stay fully austenitic [FAR E–3 p.74].
    - Mn and N "can be used together as a direct substitute for nickel". In 201/202 about half the Ni is replaced by Mn [FAR E–4 p.76–77; App. 5 p.182].
    - Type 310 has 20 % Ni "to maintain a fully austenitic microstructure and avoid ferrite, which would transform to sigma during long-term service" [FAR H–4 p.128]. Cast 330 may contain ferrite pockets that transform to σ [FAR H–6 p.132].
    - Fully austenitic alloys with Ni ≈ Fe resist σ. Alloy DS "can be heated in the critical 600–900 °C range, for indefinite periods of time" [FAR H–5 p.131]. Incoloy 800 does not form σ even after long exposure at 1200–1600 °F (649–871 °C) [EVE p.73].
- **Schaeffler / DeLong (general knowledge; still not sourced).** Cr_eq = Cr + Mo + 1.5Si + 0.5Nb; Ni_eq = Ni + 30C + 0.5Mn, and DeLong adds +30N. The diagrams map weld-metal phase (A / A+F / F / M). **Full-text check [FT 2026-10-12]:** none of FAR, EVE or THI prints a Schaeffler, DeLong or WRC diagram, or any Cr/Ni-equivalent formula. FAR only describes the constituent roles qualitatively, quoted above. These coefficients therefore stay general knowledge and need a primary source (e.g. the WRC-1992 diagram) before quantitative use.
- **High Mo segregates and destabilises [FT 2026-10-12].** In the 6 % Mo superaustenitics, "the high molybdenum level [tends] to destabilise the austenite, give rise to segregation, and so reduce corrosion resistance". This is countered with more Ni and ~0.2 % N [FAR F–3 p.88]. Matching weld consumables are not used for 6–7.5 % Mo grades "because of molybdenum segregation in the as-welded condition". Over-alloyed Ni-base fillers are used instead [FAR F–3 p.89; F–4 p.91]. *Al transfer (inference):* slow-diffusing solutes segregate in as-cast Al too (Mn, Cr, Zr, Sc in dendrite cores or interdendritic regions). The options are the same: over-alloy to cover the depleted regions, or homogenise.
- **Composition variants that trade strength for phase stability [FT 2026-10-12].**
  - C-4 (no W) has corrosion resistance similar to C-276 but better high-temperature stability and resistance to ageing up to 1050 °C [FAR G–2 p.104].
  - G-30 has more Cr, less Mo and Nb, and more W than G-3. The change is "claimed to improve weldability and particularly to increase corrosion resistance by reducing segregation and precipitation in weld HAZs" [FAR G–6 p.112–113].
  - Alloy 617 replaces part of the Ni with ~12 % Co, drops Nb, and adds ~1 % Al + Ti. It has 625-like tensile properties but better creep rupture and long-term stability above ~900 °C [FAR I–4 p.156–157].
- **Alloying for process robustness, not peak properties [FT 2026-10-12].**
  - Most commercial Ni–Fe soft-magnetic alloys add Mo, Cr, Cu or V "to reduce the sensitivity of the nickel-iron alloys to variables occurring during heat treatment, thus simplifying the control of cooling rates" [EVE p.194].
  - W–7.5Ni–2.5Cu heavy metal gives UTS 56 ksi with <1 % El after slow cooling, but 90 ksi with 1–2 % El after fast cooling. Replacing Cu with Fe (W–7Ni–3Fe) gives 59 ksi/19 % slow-cooled and 54 ksi/7 % fast-cooled. The point of the substitution was to "overcome this sensitivity to cooling rate" [EVE p.218].
  - *Al transfer (inference):* for slug annealing, the composition goal can be a recrystallised grain size and hardness that are insensitive to coil position and furnace heating rate, not the highest possible value of either.
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
   - The strength that cold work gives 70/30 Cu–Ni "is lost completely at about 1200 F" (649 °C). Above that, cold-worked and annealed material behave alike [EVE p.106] [FT 2026-10-12].
6. **Rafting and morphology** (SX superalloys):
   - Rafting is directional γ′ coarsening, diffusion-controlled near ~900 °C. In CMSX-4 at 100 MPa/1150 °C it completes in 10 h [SEG §3.3 p.19].
   - Negative misfit plus tension gives N-type rafts. The rafting parameter is R = L/(2T), with R = 0.5 for cubes (eq. 2, p.20).
   - Rafted structures lost ~25 % YS. Pre-rafts parallel to the stress improve creep and fatigue [SEG p.20].
7. **Data:**
   - 0.2C steel rupture in 1000 h: 295 MPa at 400 °C, 118 MPa at 500 °C [HIG §3.5 p.37].
   - Low-C Ni (0.02C) at 1000 °F creeps less than 0.15C Ni at 800 °F [EVE p.20–22].
   - Larson–Miller P = T(C + log t_r) is the usual time–temperature parameter (general knowledge; not given in FAR, EVE or THI).
8. **More cross-family creep data [FT 2026-10-12]:**
   - **Stabilised carbides beat plain austenite.** The 0.0001 %/h creep stress of 347 at 1200 °F is twice that of 304. Above 1500 °F (816 °C) all the wrought austenitic stainless grades have very low creep resistance [EVE p.139–140].
   - **Cast beats wrought in long-time properties** at equal composition: cast superalloys tend to have higher rupture strengths [EVE p.83]. Cast stainless steels have the long-time advantage too: the 0.0001 %/h creep stress of cast HK at 1600 °F is 1.5 × that of wrought 310 at 1500 °F [EVE p.155]. The most highly alloyed grades are cast because their hot strength makes hot working difficult, and cast grades tend to carry less Cr and more Al than wrought ones [EVE p.82–83].
   - **Absolute numbers at the top of the Fe–Ni–Cr range.** HK40 (0.4C–25Cr–20Ni): 100,000-h rupture stress ~4 MPa at almost 1100 °C [FAR H–7 p.135]. ~1150 °C is "about the practical upper limit" for fabricable heat-resistant alloys [FAR H–10 p.141]. 80Ni–20Cr has a 100-h rupture stress at 1800 °F of only about two-thirds of X-750's [EVE p.167].
   - **Austenitic creep steel by stable-carbide design.** Esshete 1250 (15Cr–10Ni–6Mn–1Mo–0.25V–1Nb–0.005B) uses V, Nb and B carbides "as long-term ageing takes place" for service to 675 °C [FAR H–1 p.122–123].

### 1.7 Corrosion design rules

- **Passivity threshold.** Stainless steel needs **≥10.5 % Cr** and ≤1.2 % C. The passive Cr-oxide film is ~10 atomic layers thick [THI §6.2.4 p.58]. 11–12 % Cr is "just stainless" [FAR C–1 p.38–39]. **Source difference [FT 2026-10-12]:** EVE (1971) states that Cr "must be present in amounts above 11.5 %" [EVE p.129]. THI's 10.5 % matches the current EN definition (general knowledge). Use 10.5 % as the definition and ~11–12 % as the practical minimum.
- **Pitting-resistance indices: now sourced [FT 2026-10-12; replaces the earlier "task brief / general knowledge" formulas]** [FAR App. 1 p.172–173]:
  - **PRE = Cr + 3.3Mo**: the original formula, for austenitic stainless steels without N additions.
  - **PREn = Cr + 3.3Mo + 16N**: "the formula most widely used for duplex, superduplex and superaustenitic stainless steels". Some authorities consider an N multiplier of **30** more appropriate for high-N superaustenitics.
  - **PREw = Cr + 3.3(Mo + 0.5W) + 16N**: for W-bearing superduplex grades.
  - **PREN (Ni alloys) = Cr + 1.5(Mo + W + Nb) + 30N − 0.5Cu**: used by "some authorities" for corrosion-resistant Ni alloys. It gives 45 to >50 for the most resistant grades. FAR notes "some debate" about extending the stainless formulas to Ni alloys.
  - Values in the source (FAR sheet, printed page):

| Family (FAR sheet) | Typical composition | PRE(N) |
|---|---|---|
| Soft martensitic CA6NM (C–5, p.47) | 0.04C–13Cr–4.5Ni–0.75Mo | 15–21 |
| 304L (E–3, p.75) [FT] | <0.03C–19Cr–9Ni | ~18 |
| 316L (E–3, p.75) [FT] | <0.03C–17Cr–12Ni–2.5Mo | ~26 (Mo adds ~8) |
| Lean duplex 2304/UR50 (D–0, p.56) | 23Cr–4.5Ni–0.15N … 22Cr–7Ni–2.5Mo–1.5Cu–0.1N | 26–32 |
| 317L / 317LMN (F–0, p.83) [FT] | 19Cr–13Ni–3.5Mo / 19Cr–15Ni–4.5Mo–0.15N | 316L + ~5 / ~35 |
| Alloy 20 (F–5, p.93) [FT] | 20Cr–34Ni–2.5Mo–3.5Cu–Nb | ~30 |
| Standard duplex 2205 (D–1, p.58) | 22Cr–5Ni–3Mo–0.17N | ≥35 |
| Alloy 28 (G–5, p.111) [FT] | 27Cr–31Ni–3.5Mo–1.2Cu–0.05N | 36–38 |
| 904L (F–2, p.87) [FT] | 21Cr–26Ni–4.5Mo–1.5Cu | ~37 |
| Superduplex 2507 (D–2, p.60) | 25Cr–7Ni–4Mo–0.25N | >40 (defining criterion) |
| Superferritic AL 29-4C (C–7, p.51) | 0.02C–29Cr–4Mo–0.6(Ti+Nb) | ~40 |
| 6 % Mo superaustenitic, e.g. 254 SMO (F–3, p.89) [FT] | 20/24Cr–18/25Ni–6.5Mo–~1Cu–0.22N | 43–45 (16N); ~50 (30N) |
| 654 SMO / UR B66 (F–4, p.91) [FT] | 24Cr–22Ni–7.5Mo–0.5N / 24Cr–23Ni–6Mo–2W–2Cu–0.5N | ~55 (16N); >60 (30N) |
| Most resistant Ni alloys (App. 1, p.173) [FT] | e.g. C-276, C-22, alloy 59/686 | 45 to >50 (Ni-alloy formula) |

- **What the index does not capture [FT 2026-10-12].**
  - Alloy C-22 has more Cr but less Mo, W and Fe than C-276. FAR calls the net effect on chloride pitting "effectively neutral", but the extra Cr improves resistance in oxidising media [FAR G–3 p.106–107].
  - The general rule: "high chromium contents are required to provide resistance to oxidising media", while reducing acids "require high molybdenum and tungsten" [FAR G–4 p.109].
  - Alloy 20 has a pitting index like 316L (~30) but was designed with Cu for general corrosion in sulfuric acid [FAR F–5 p.93].
- **Sensitisation is a heat-treatment window [FT 2026-10-12].** Holding Cr–Ni stainless steel, or cooling it slowly, through 1450–800 °F (788–427 °C) deposits Cr carbides on the grain boundaries. This depletes Cr next to the boundaries and leads to intergranular failure, often next to welds [EVE p.131]. The fixes are:
  - Re-dissolve the carbides at 1800–2050 °F (982–1121 °C) and water quench [EVE p.131].
  - Cut C to low-carbon (<0.03 %) or extra-low-carbon (<0.02 %) levels [EVE p.131; FAR App. 1 p.172]. AOD made this economic from ~1970 [FAR E–1 p.70–71; App. 1 p.172].
  - Stabilise with Ti or Nb at about 10 × C, e.g. 0.06 C needs ~0.7 % [FAR E–0 p.68].
  - *Al transfer (inference):* 5xxx alloys with >3 % Mg have the same kind of window, in which the boundary phase is β-Al₃Mg₂ itself rather than a Cr-depleted zone (general knowledge). The same three levers apply: thermal history, composition limit and a "stabilising" addition that changes the boundary phase.
- **SCC resistance from Ni [FT 2026-10-12].** Austenitic stainless steels are sensitive to chloride SCC "when residual stresses are present and temperatures are within the critical range (above about 65 °C)" [FAR E–3 p.75]. Higher Ni raises SCC resistance [FAR App. 5 p.182]. Alloy 690 (29–30 % Cr) replaced 600 in steam generators because it resists high-temperature SCC in water better [FAR G–7 p.115].

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
- **Local cells in Al and other metals [FT 2026-10-12]** [THI §11.2 pp.99–107]:
  - Electrochemical corrosion needs a potential difference, a closed circuit with an electrolyte, and unhindered electrode reactions. Different crystal phases are one listed source of the potential difference [THI §11.2 p.99–100].
  - Pitting runs faster as the cathode-to-anode area ratio rises (small defect, large passive cathode) [THI §11.2.3.2 p.102].
  - On Al alloys, "the heterogeneous microstructure of the alloys causes heterogeneous oxide layers … with different electrochemical behaviour", which can lead to local pitting unless the protective film stops it [THI §11.2.4.2 p.107].
  - The Al film is nearly pore-free, a few molecular layers thick, insoluble at neutral pH and self-healing. Acids (pH < 4) and alkalis (pH > 10) attack it [THI p.107]. Al is not resistant to alkaline building materials such as cement [THI §11.1.2 p.98].
  - Aggressiveness of salt ions toward Al: Cl⁻ > NO₃⁻ > SO₄²⁻ > Na⁺ > K⁺ > NH₄⁺ > Ca²⁺ > Mg²⁺ [THI §11.1.2 p.98].
  - Zn–Cu contact is singled out as especially critical because of the large potential difference [THI §11.2.3.4 p.103].

#### 1.7.1 Oxide growth and scale engineering (relevant to MgO growth during slug annealing) [FT 2026-10-12]

- **Oxide/metal volume decides protectiveness.** THI ties protectiveness to the oxide/metal density difference and the "transition from metal to oxide" [THI §11.1 p.96]. Its Table 14 gives the densities (g/cm³): Mg 1.7, MgO 3.6; Al 2.7, Al₂O₃ 3.4 and 4.0 (the two polymorph labels were lost in extraction); Fe 7.9, FeO 5.7, Fe₂O₃ 5.3, Fe₃O₄ 5.2; Zn 7.1, ZnO 5.7 [THI Table 14 p.97].
  - Converted with molar masses to the **Pilling–Bedworth ratio** (PBR = V_oxide/V_metal consumed; the concept and molar masses are general knowledge, the arithmetic is mine): **MgO 0.78**; Al₂O₃ 1.28 (4.0 g/cm³) to 1.50 (3.4 g/cm³); ZnO 1.55; FeO 1.78; Fe₂O₃/Fe₃O₄ ≈ 2.1.
  - **Flag: the THI argument conflicts with general knowledge.** THI says that Mg and Al oxides are denser than their metals and that a dense, insoluble oxide such as Al₂O₃ stops corrosion [THI p.96]. For MgO, however, the higher density is exactly why it is *not* protective. A PBR below 1 means the oxide cannot cover the metal it consumes, so the film is porous or cracked and growth continues (general knowledge).
  - *Al transfer (inference):* this is the geometric reason, on top of Mg's higher oxygen affinity (general knowledge), why Mg that segregates to the surface of Al–Mg strip during annealing builds MgO that keeps growing, rather than self-limiting like Al₂O₃.
- **An inner barrier oxide can stop the outer oxide growing.** In alloy 45TM (28Cr–45Ni–3Si–0.1REM), Si and REM "act synergistically" to form "a very stable oxide layer that is adjacent to and just below the chromium oxide film. This silicon oxide layer prevents growth of the primary chromium oxide layer and therefore reduces the risk of spalling" [FAR I–2 p.152]. In 253MA, Si + REM likewise stabilise the oxide film against spalling [FAR H–2 p.125]. REMs "help to stabilise and prevent growth and spalling of the oxide film" [FAR App. 5 p.183].
  - *Al transfer (inference, to test):* look for a minor addition, or a pre-oxidation step, that forms a dense layer under or in the Al₂O₃ film and blocks outward Mg transport. Small Be additions to Al–Mg melts are used to limit oxidation (general knowledge; Be carries occupational-health restrictions).
- **Atmosphere selects which element oxidises.** 80Ni–20Cr suffers "selective oxidation in partially reducing atmospheres" at 1500–1800 °F (816–982 °C), which reduces ductility and causes hot spots. The cure is to keep the atmosphere oxidising or to lower the Ni content [EVE p.161]. "Green rot" in Ni–Cr alloys arises when furnace atmospheres alternate between reducing and oxidising [FAR H–5 p.131].
  - *Al transfer (inference):* in a batch-annealing furnace the dew point and O₂ partial pressure decide whether Mg or Al oxidises preferentially at the strip surface. Atmosphere control is a first-order lever on MgO, alongside alloy Mg content and annealing time and temperature.
- **Refractory-metal oxides can run away.** Mo-bearing alloys such as 316 can suffer catastrophic oxidation in oxygen above about 700 °C, because the oxidation is exothermic and self-accelerating [FAR App. 6 p.186; E–3 p.75].

### 1.8 Carbon equivalent, hardenability and weldability (steels)

- **Effect of alloying on steel properties** [THI §5.2 p.44]:
  - Strength: C ⇑, Mn ↑, V/Nb ↑. The list also has a group "Cr, Ni, Cu, Al" under strength.
  - Hardenability: C ⇑, Mn ↑, Si ↑.
  - Corrosion: Cr ⇑, Cu+P ↑, with Ni and Mo also listed. *(Corrected after full-text pass: Al is listed under strength, not corrosion, and Cu under corrosion only as "Cu + P". The arrow glyphs are not extractable from the PDF, so the ⇑/↑ magnitudes come from the earlier pass and are unverified.)*
  - Cold formability: C ↓, Si ↓, P/S ↓.
  - Weldability: C ⇓, Mn ↓.
- **Carbon-equivalent formulas** [THI §7.3.2 p.72]. **Verified [FT 2026-10-12]:** in the PDF each formula is an embedded equation object. Its numerator and denominator positions were read from the word bounding boxes (PDF p. 72), so the term grouping below is now confirmed rather than reconstructed:
  - IIW, for steel with C > 0.18 %: **CE = C + Mn/6 + (Cr+Mo+V)/5 + (Ni+Cu)/15**.
  - "For alloyed high-strength steels, e.g. quenched-and-tempered fine-grain structural steels": **CET = C + (Mn+Mo)/10 + (Cr+Cu)/20 + Ni/40**. This matches the EN 1011-2 form. The earlier note that the grouping was garbled and only general knowledge is superseded.
  - Ito–Bessyo, for steel with C < 0.18 %: **C + Si/30 + (Mn+Cu+Cr)/20 + Ni/60 + Mo/15 + V/10 + 5B**. THI labels this formula "CE_V". *Terminology flag (general knowledge):* the Ito–Bessyo expression is usually called P_cm, while "CEV" in EN 10025 denotes the IIW formula. Check which one a specification means.
  - THI adds that other weightings exist depending on the purpose, and that CE also indicates cold-crack sensitivity. Any CE-based statement "must always be judged cautiously", because CE does not capture steelmaking route, fabrication or design [THI p.72].
- **Preheat rule** [THI Table 9 p.72–73]:
  - CE(IIW) < 0.45 needs no preheat.
  - 0.45–0.60 needs 100–200 °C.
  - >0.60 needs 200–500 °C.
  - Unalloyed steel welds without preheat to 0.22 % C [THI p.72].
  - Procedures use **t8/5**, the 800 → 500 °C cooling time. Too low a preheat risks cold cracks; too high a preheat lowers HAZ toughness [THI p.73].
- **The HAZ is a sequence of thermal zones** (cast → coarse γ → fine normalised → intercritical, partly re-hardened → tempering/ageing) [THI Fig. 70 p.71].
  - *Al transfer (inference):* the same zonation (fusion → partially melted → solutionised → over-aged → unaffected) explains 6xxx/7xxx HAZ softening. A local yield-strength map can be computed with the A356 local-heat-treatment framework [MPF18 Holzmann et al. p.77].
  - When welding treated steels, especially cold-formed ones, heat input must be limited "to prevent softening through the change of the microstructure" [THI p.72].
- **Al welding in THI [FT 2026-10-12]** [THI §10.1.6 p.88]:
  - Because of its high thermal conductivity, Al needs about the same heat to melt as steel, despite its lower melting point.
  - The oxide skin only melts at ~2000 °C. Gas or manual metal-arc welding therefore gives lack-of-fusion defects, and Al is welded under argon by MIG or TIG.
  - In the HAZ the welding heat causes solution annealing and recrystallisation, and strength drops sharply. The size of the drop depends on the alloying elements, weld size and heat input.
  - Age-hardenable alloys lose less strength than non-age-hardenable ones and can regain base-metal strength by heat treatment and ageing. The strength that cold work gives non-age-hardenable alloys is lost on welding.
  - These points give source support to the Al HAZ inference above. The "Al weldability equivalent for hot cracking" (§2 lever 4) is still general knowledge.

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
- **Composition tuned for the forming operation: work-hardening rate as a design target [FT 2026-10-12].**
  - In the AISI 300 series "the chromium-nickel ratio has been altered to change the forming characteristics". 301 is adjusted for a high work-hardening rate. 305, 384 and 385 are adjusted for a low rate. Mn-bearing 211 matches 304's rate for deep drawing and roll forming [EVE p.129–131, 133–135].
  - Commercial Ni (0.15 % C) work hardens quickly. "To reduce the effect of work hardening, a low carbon modification was developed", which "facilitates deep drawing and other severe cold forming operations" [EVE p.9].
  - 36Ni–Fe (Invar) hardens at about the rate of mild steel, "much lower" than 304 [EVE p.180].
  - *Al transfer (inference):* for impact-extrusion slugs, a low work-hardening rate and a low recrystallised hardness are the composition targets, not maximum strength. In 3xxx the levers are Mn kept in solid solution (raises work hardening and the recrystallisation temperature) versus Mn precipitated as dispersoids (Zener pinning, finer grain), and Mg (strong solute hardener).
- **Free-machining additions cost weldability.** S or Se at up to ~0.3 %, "at least 10 times" the normal level, form sulfide films that help chip breaking. Both promote weld-metal and HAZ hot cracking [FAR E intro p.67]. 303/303Se machine about 15 % better than 302 [EVE p.131]. *Al transfer (general knowledge):* Pb, Bi and Sn play the same role in free-machining Al alloys, with the same trade-off against hot shortness.
- **Cost and supply as design inputs [FT 2026-10-12].**
  - Relative element cost (Fe = 1): Mn 4, Cr 8, Cu 10, Ni 40, W 50, Mo 60, V 70, Nb 90, Co 110. Alloy cost (mild steel = 1): 304L 3, superaustenitic 6, alloy 625 15 [FAR App. 4 Tables 1–2 p.178–179]. FAR notes that prices change daily, so these are indicative only.
  - The 200 series (Mn substituting for Ni) was developed "to conserve nickel" [EVE p.131; FAR E–4 p.76–77]. Alloy 800 was designed with low Ni because Ni was then a "strategic" metal [FAR I–0 p.148–149].
  - The Soviet superalloy route replaced scarce Mo with W "wherever possible", restricted Co, reduced Al and Ti, and added V. It apparently reached properties comparable with Western alloys [EVE p.84].
  - *Al transfer (inference):* this is the template for designing around Sc (cost/supply) with Zr, Er or Mn-dispersoid substitutes, and for ranking CRM exposure per unit of property gained.
- **Melting practice: cleanliness helps toughness but not always fatigue [FT 2026-10-12].** Vacuum casting raised the Charpy V of alloy 713C from 7.0 to 9.4 ft-lb (≈9.5 → 12.7 J) compared with inert-atmosphere casting [EVE p.98]. In contrast, vacuum melting "made no significant improvement" in the fatigue properties of Ni-Span C Bourdon elements [EVE p.189]. Compare the clean-steel gear-fatigue gain [SUP18 p.123]: the payoff depends on whether inclusions are what initiates failure.
- **Heat treatment must fit the product form.** X-750 bar gets a three-step treatment (2100 °F solution anneal, then ageing at 1550 °F and 1300 °F). Sheet is not given it, "because the 2100 F solution anneal could cause distortion". A furnace-ageing cycle from 1350 °F gives about the same stress-rupture strength [EVE p.69].
- **Solidification texture as a property lever.** Casting Alnico V against a chill plate (partly columnar grains) raises the maximum energy product by ~20 %. A fully columnar structure (Alnico V-7) gives the highest value for that composition [EVE p.199–200]. Sintered Alnico V has ~10 × the tensile strength of cast material at a similar hardness [EVE p.201].
- **Casting routes** [HIG §5 p.55–60]:
  - Si for fluidity in cast Ni alloys [FT 2026-10-12]. Cast Ni–Cr raises Si from 0.25 % (wrought 600) to 1.5–1.6 % (alloy 610; text and Table 4-8 differ slightly) or 5.5 % (alloy 705). The 5.5 % Si alloy becomes age-hardenable: YS 80–100 ksi against 30–45 ksi, but elongation falls to 3–1 % against 30–10 % [EVE p.71–73, Table 4-9]. Cast Ni–Cu uses Si the same way [EVE p.44].
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
| Insoluble dispersoids instead of precipitates [FT] | Orowan strength above the precipitate solvus; matrix stays pure and conductive | TD-Ni 1000-h rupture at 1093 °C = Nimonic 115 at 982 °C; k ≈ 83 vs 9–12 W/m·K [EVE pp.85–90] |
| More precipitate former / higher solvus [FT] | γ′ fraction; Co raises the γ′ solvus | Al+Ti 3.6 → 9 %: 1000-h/871 °C rupture 69 → 186 MPa [EVE p.89] |
| Grain size vs temperature [FT] | Hall–Petch at RT; coarse grain for creep | 70 → 15 µm: UTS +22 %, El 49 → 36 % [EVE p.117]; 804 coarse grain 2 × rupture stress at 760 °C [EVE Table 4-14] |
| Work-hardening rate by composition [FT] | Austenite stability (Cr/Ni), low C | 301 high vs 305/384/385 low WH [EVE p.129–135]; low-C Ni for deep drawing [EVE p.9] |
| Oxide-scale engineering [FT] | PBR; inner barrier oxide; atmosphere | MgO PBR 0.78 vs Al₂O₃ 1.28–1.50 (from THI Table 14); Si/REM sub-layer [FAR I–2 p.152] |
| Process-robust composition [FT] | Reduce sensitivity to cooling rate | Mo/Cr/Cu/V in Ni–Fe magnetic alloys [EVE p.194]; W–Ni–Fe vs W–Ni–Cu [EVE p.218] |

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

### 2.6 Austenitic, superaustenitic and heat-resistant stainless steels (FAR Groups E, F, H; EVE Ch. 7) [FT 2026-10-12]
- **Two branches from one base, split by carbon** [FAR E intro p.67; H intro p.119]:
  - The **low-C branch** is for weldability and aqueous corrosion: 304L → 316L → 317L/317LMN → 904L → 6 % Mo → 654 SMO.
  - The **controlled-C branch** (0.04–0.08 % C, "H" grades) is for creep and scaling: 304H/316H → 253MA → 310 → HK40 → HP40Nb → 35/45 → 50Cr–50Ni.
  - The same base composition becomes two products by C level alone. 304L and 316L should not be used above ~450 °C; 304H/316H take over [FAR E–1 p.71; E–3 p.75; H–0 p.120–121].
- **Austenite is weak but tough.** It "is relatively weak and soft unless it is deliberately strengthened by nitrogen additions … or by work hardening". It "does not show any transitional behaviour", which gives useful cryogenic properties [FAR E–0 p.69; E–1 p.71]. Annealed austenitic grades more than double their RT strength at −320 °F (−196 °C) [EVE p.141]. Cr–Mn–N Nitronic grades are preferred to duplex below about −50 °C, because duplex toughness falls there [FAR E–4 p.77].
- **Weld metal often must be over-alloyed or Ni-base.** 904L in severe chloride service, and all the 6–7.5 % Mo grades, are welded with Ni-base consumables (e.g. 625) [FAR F–2 p.87; F–3 p.89].
- **Heat-resistant grades: what each element does** [FAR H–0–H–11 pp.120–143]:
  - C was raised "to improve hot strength" (310) [FAR H–4 p.128] and forms carbides with strong carbide formers [FAR App. 5 p.180].
  - Cr gives scaling resistance up to ~1100 °C (310). Prolonged exposure above 1000 °C with thermal cycling breaks down the oxide film [FAR H–4 p.129].
  - Ni stabilises austenite against σ and raises thermal-shock resistance through lower CTE (330/HT) [FAR H–6 p.133].
  - Si + REM stabilise the oxide (253MA) [FAR H–2 p.125].
  - Nb forms a stable carbide network, and Ti/Zr microalloying adds secondary fine-carbide networks (HP40Nb, 35/45) [FAR H–8 p.136; H–10 p.140].
  - Co and W keep the matrix strong where carbides dissolve [FAR H–9 p.138].
  - 50Cr–50Ni–Nb (IN-657) resists V₂O₅/alkali-sulfate fuel-ash attack, whose melting point "can be as low as 630 °C" [FAR H–11 p.143].
- **Precipitation-hardening stainless (EVE Ch. 7)** [EVE pp.143–150]:
  - Three groups: martensitic (17-4PH, Stainless W), semi-austenitic (17-7PH, AM-355; they need a conditioning treatment, transformation to martensite, then ageing), and austenitic (A-286, HNM).
  - The martensitic and semi-austenitic types can exceed 200 ksi (≈1380 MPa). The austenitic types reach only ~140 ksi but stay tough when aged.
  - Elongation of 17-7PH in Condition A is four times that after TH-1050 [EVE p.148].

**Design levers — steels → Al (all inference unless cited)**
1. **Layered strengthening for creep:** solid solution, then stable carbide, then microalloy carbonitride, then a slow-diffusing heavy element (W). The Al parallel is Mg/Cu solid solution, then Al₃(Zr,Sc,Er) dispersoids, then slow diffusers [FAR A series].
2. **Cut the embrittling interstitial or impurity and recover strength by processing (TM rolling).** In Al this means low Fe/Si plus controlled hot-rolling and extrusion recrystallisation [THI p.34; FAR C–6].
3. **Grade ladders tied to an index** (PREn 26 → 35 → 40) make alloy families legible. A similar index for Al, for example a quench-sensitivity or intergranular-corrosion index, is an open idea [FAR D].
4. **Weldability is a composition budget** (CE < 0.45 needs no preheat). An "Al weldability equivalent" for hot-cracking (Si, Cu, Mg windows) would be the analogue (general knowledge).
5. **One base, two products by one element [FT 2026-10-12].** 304L vs 304H differ only in C, which is set for weldability or for creep [FAR E–1, E–2, H–3]. The Al analogue is the same base alloy with Mn or Fe split between solid solution and dispersoids by homogenisation practice, aimed either at formability (slugs) or at sag and creep (fin stock) (inference).
6. **Tune the work-hardening rate for the forming operation** (301 vs 305/384/385; §1.9) [EVE p.129–135].

---

## 3. Nickel and Ni-base superalloys

### 3.1 Commercial Ni and solid-solution / age-hardenable Ni alloys (Everhart)
- **Pure Ni:**
  - fcc (a = 3.5238 Å), Tm 1453 °C, E ≈ 30,000 ksi (207 GPa), ν = 0.26 [EVE pp. 8–13]. SC Ni elastic anisotropy: E⟨001⟩ 125, E⟨011⟩ 220, E⟨111⟩ 294 GPa, against 207 GPa polycrystalline [SEG §3.5.1 p.24].
  - Hardens only by cold work: annealed 55 ksi → up to 145 ksi [EVE p.13–14]. Work-hardening rate is similar to mild steel [EVE p.16].
  - Fatigue ratio 0.31–0.42 [EVE p.18]. Like other fcc metals it has no ductile–brittle transition [EVE p.23].
- **Ni–Cu (Monel):**
  - Monel 400: 66.5Ni–31.5Cu.
  - **K-500** adds ~3Al–0.6Ti and precipitates Ni₃(Al,Ti) at ~1100 °F (593 °C). UTS reaches 220 ksi; ageing adds ~30 ksi at 60 % cold work [EVE Table 3-1 p.33; pp. 34–37]. FAR gives "about 2.5 % aluminium and 0.5 % titanium", which "effectively doubles the tensile strength to more than 1000 MPa" over alloy 400 [FAR J–1 p.167]. The Al/Ti values differ slightly between the 1971 nominal composition and the 2004 typical one [FT 2026-10-12].
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
- **Source discrepancy on alloy 600 [FT 2026-10-12].** FAR's G–7 sheet describes 600 as having "a higher nickel content (75%) and lower chromium content (21%)" than 690 [FAR G–7 p.115]. FAR's own I–1 sheet gives 16 % Cr [FAR I–1 p.150], and EVE gives 15.5 % [EVE Table 4-1]. Treat the 21 % in G–7 as an error and use 15.5–16 % Cr.
- **Ni–Fe–Cr (Incoloy 800/804/825) [FT 2026-10-12]** [EVE pp.73–80; FAR I–0 p.148–149]:
  - Lower Ni and higher Cr than the Inconels; not hardenable by heat treatment, only by cold work [EVE p.75].
  - Short-time strength: alloy 800 keeps >80 % of RT strength to ~1000 °F and has lost 50 % by 1250 °F [EVE p.77].
  - Coarse grain improves creep (§1.2). Alloy 800H tightened the C control; 800HT also controls Al + Ti tightly and sets minimum grain size [FAR I–0 p.149].
- **Ni-rich age-hardenable alloys (>90 % Ni) [FT 2026-10-12]** [EVE pp.203–211]:
  - Permanickel 300 (C + Mg): hot-finished 100 ksi aged to 180 ksi.
  - Duranickel 301 (Al + Ti): 60 % cold reduction adds ~50 % strength; cold work plus ageing more than doubles it.
  - Berylco Nickel 440 (Be + Ti): the strongest of the three, but much less ductile.
  - Spring service limits: 300 to 600 °F, 301 to 650 °F [EVE p.210].
  - Cast Be–Ni (2–3 % Be) reaches the strength of the wrought alloy after ageing, but with much lower elongation [EVE p.212].

### 3.1a Corrosion- and heat-resistant Ni alloys (FAR Groups G, I, J) [FT 2026-10-12]
*(Previously: "listed in the contents but data sheets not returned". Now read in full.)*

| Sheet | Alloy (typical wt %) | Design idea | Ref |
|---|---|---|---|
| G–0 / I | 625: 22Cr–62Ni–9Mo–3.8Nb, Fe 2–3 | Mo + Nb hardeners; proof >500 MPa at RT; long-term ageing near 700 °C costs ductility and toughness | FAR G–0 p.100–101 |
| G–1 → G–2 | C → C-276: 16–17Cr–55/57Ni–16Mo–4W–6Fe | Same base; C and Si cut to very low levels to stop HAZ intermetallics and grain-boundary precipitates. C-4 (no W) is more stable up to 1050 °C | FAR G–1 p.102–103; G–2 p.104–105 |
| G–3 | C-22: 22Cr–56Ni–13Mo–3W–3Fe | More Cr for oxidising media; pitting "effectively neutral" | FAR G–3 p.106–107 |
| G–4 | C-2000 / 59 / 686: 21–23Cr–16Mo (+1.6Cu or +4W) | Combine oxidising (Cr) and reducing (Mo, W) resistance "and still retain metallurgical stability" | FAR G–4 p.108–109 |
| G–5 | Alloy 28: 27Cr–31Ni–3.5Mo–1.2Cu–0.05N | More Cr and Mo, less Ni than 825; N gives ~10 % more UTS than 825/20 | FAR G–5 p.110–111 |
| G–6 | G-30: 30Cr–44Ni–5.5Mo–2Cu–1.7W–2Nb–15Fe | More Cr and W, less Mo and Nb than G-3, to cut weld-HAZ segregation | FAR G–6 p.112–113 |
| G–7 | 690: 29Cr–61Ni, no Mo | High-temperature SCC resistance in water; replaces 600 in PWR steam generators | FAR G–7 p.114–115 |
| I–0 | 800/800H/800HT: 21Cr–32Ni–Al–Ti | Low-Ni economic grade; controlled C, Al + Ti and grain size for creep | FAR I–0 p.148–149 |
| I–1 | 600: 16Cr–75Ni–8Fe | Very stable microstructure; dry Cl₂ to ~550 °C; poor chloride pitting (no Mo) | FAR I–1 p.150–151 |
| I–2 | 45TM: 28Cr–45Ni–23Fe–3Si–0.1REM | Si-oxide sub-layer stops Cr₂O₃ growth (§1.7.1) | FAR I–2 p.152–153 |
| I–3 | 333: 25Cr–46Ni–3Mo–3Co–3W–1.2Si–18Fe | Three solid-solution elements at 3 % each; Si against spalling | FAR I–3 p.154–155 |
| I–4 | 617: 22Cr–54Ni–9Mo–12Co–1.2Al–0.3Ti | Co replaces Ni, Nb removed; better creep and stability above ~900 °C | FAR I–4 p.156–157 |
| I–5 | Alloy X: 22Cr–47Ni–9Mo–17Fe–2Co–0.7W–0.15C (+0.2Al, 0.15Ti) | First Ni–Cr–Fe "superalloy"; easier to weld than high-Al+Ti alloys | FAR I–5 p.158–159 |
| J–0 | Ni 200 / 201 | C limits service temperature (graphitisation) | FAR J–0 p.164–165 |
| J–3 | B-2/B-3/B-4: ~28Mo, very low C and Si | HCl resistance; B-3/B-4 add Cr and Fe for SCC resistance and weldability | FAR J–3 p.170–171 |

### 3.1b Wrought and cast γ′ superalloys and ODS nickel (EVE Ch. 5) [FT 2026-10-12]
- **Definition and roles** [EVE p.82–83]:
  - Superalloys are "modifications of the corrosion- and heat-resisting alloys" made age-hardenable by Al + Ti.
  - Cr gives oxidation resistance and some strengthening. Nb, Mo, W and Ta give solid-solution strengthening.
  - Co replaces part of the Ni. B and Zr improve creep properties and hot workability.
  - Heat treatment: solution anneal at 1900–2150 °F (1038–1177 °C), then ageing in steps to develop γ′ and complex carbides. Cast parts are often just aged (e.g. 1400 °F).
- **Wrought alloys ranked by Al + Ti** (M-252 → Waspaloy → René 41 → Udimet 500 → Nimonic 115) [EVE Table 5-1 p.84]:
  - RT YS 97–154 ksi, UTS 140–206 ksi, El 9–28 % depending on alloy, product form and heat treatment [EVE Table 5-3 p.88].
  - Rupture strength rises with Al + Ti (§1.3) [EVE Table 5-4 p.91].
- **Cast alloys** (GMR-235D, 713C, IN-100, MAR-M200, MAR-M246) [EVE pp.94–99]:
  - As-cast RT elongation is only 3–7 % [EVE Table 5-7 p.97].
  - Strength rises with Al + Ti. The W-bearing MAR-M alloys break the pattern and sit between 713C and IN-100, "probably because of" W matrix strengthening [EVE p.98].
  - At 1800 °F all five have short-time strengths of 70–80 ksi [EVE p.99].
- **ODS route:** TD Nickel (§1.4).
- **Cryogenic behaviour:** strength rises at low temperature, most in the solution-annealed condition. René 41 bar goes from 188 ksi at RT to 255 ksi at −400 °F, with no ductile–brittle transition [EVE pp.91–94].

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
7. **Dispersoids beat precipitates above the precipitate solvus and keep conductivity [FT 2026-10-12].** TD Nickel vs Nimonic 115 [EVE pp.85–90]. For Al: Al₃Zr or oxide dispersoids for post-braze and 200–350 °C strength in conductor or heat-exchanger alloys (inference).
8. **Clean up a good alloy by cutting the residuals that cause HAZ precipitation, not by adding alloy** (C → C-276; B → B-2) [FAR G–1/G–2, J–3]. For Al: Fe and Si caps in 6xxx/7xxx weldable grades (inference).
9. **Solvent choice sets the ceiling.** Ni accommodates far more Cr/Mo/W than Fe [FAR App. 5 p.182–183]. For Al, the low solubility of transition metals means the ceiling is set by primary-phase formation in casting (inference; §1.1).

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

## 6. TMS 2018 highlights relevant to aluminium (plus THI's non-ferrous chapter, §6.4)

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

### 6.4 Aluminium, copper and zinc in the THI lecture notes (Ch. 10–11) [FT 2026-10-12]
THI is a civil-engineering materials course, so its Al content is introductory and construction-oriented. Designations follow superseded DIN standards. It is useful as a consistency check, not as design data.

- **Production** [THI §10.1.1–10.1.2 pp.80–81]:
  - Al makes up 7.5 mass % of the Earth's crust and occurs only as oxide compounds.
  - Bayer digestion uses 35–38 % NaOH, leaves red mud as the residue, and calcines the hydroxide at 1200 °C.
  - The electrolyte is Al₂O₃ (mp 2045 °C) dissolved in cryolite (mp 1000 °C). The eutectic (18.5/81.5) melts at 935 °C. THI names the 18.5 % component "aluminium hydroxide", which is presumably an error for Al₂O₃.
  - Liquid Al (2.35 g/cm³) is denser than the melt (2.15 g/cm³), so it collects underneath, protected from re-oxidation. Purity is 99.8–99.9 %.
  - 1 t Al needs ~2 t Al₂O₃ ≈ 4.5 t bauxite and ~14,000 kWh.
- **Strengthening** [THI §10.1.3 pp.81–85]:
  - Pure Al (~80 N/mm²) is too weak for structures. Alloy hardening, precipitation hardening and cold work work "in principle similarly to steel", by blocking slip.
  - Precipitation hardening = solution anneal, quench, age. Natural ageing takes hours, days or weeks depending on the alloy. Artificial ageing at about 200 °C is faster, but "temperature and holding time must be matched, otherwise softening occurs again" (AlMgSi, Bild 84).
  - Non-heat-treatable alloys form stable solid solutions that "cannot be further saturated and therefore not further hardened" by solution annealing. They are easier to form, "insensitive to temperature", lower in strength, and are strengthened by cold work.
  - Both classes can be cold-work strengthened, but "then have very low formability" [p.85].
  - THI states that the heat-treatable AlMgSi and AlZnMg alloys have higher corrosion resistance, without saying compared with what, and must be re-aged after heat treatment. AlCu alloys are poorly weldable and have low corrosion resistance [p.84].
  - Wrought alloys contain up to 5 % alloying elements; casting alloys 5 to >20 % [p.85].
- **Properties** [THI §10.1.4 pp.85–86]:
  - Strength is adjustable from 80 to 550 N/mm². There is no pronounced yield point, so Rp0.2 is used.
  - E = 70,000 N/mm² ≈ ⅓ of steel. A10 is still ~10 % at 520 N/mm².
  - Strength rises at low temperature "without noticeable influence on formability".
  - At elevated temperature strength falls "earlier and more strongly than for steel". Allowable stresses apply only up to +80 °C, and softening from about 150 °C makes fire-resistance requirements hard to meet.
  - Fatigue: S–N curves of non-heat-treatable alloys become nearly horizontal beyond N > 5·10⁶, like structural steel. Those of age-hardened alloys only flatten above 10⁸. Welded joints always have lower fatigue strength than the base metal [p.86].
- **Welding and HAZ:** see §1.8 [THI §10.1.6 p.88].
- **Corrosion protection:**
  - The dense, adherent Al₂O₃ film protects in free weathering. Anodising (Eloxal) thickens it artificially [THI §10.1.7 p.89]. A sulfuric/oxalic-acid anodising bath gives a hard, insulating, dyeable layer of 0.02 mm [THI §11.3.2.1 p.111].
  - Al needs protection from fresh lime plaster and concrete [p.89]. See also §1.7 and §1.7.1.
- **Not readable:** Bild 85 (common Al alloys), Bild 86 (effect of Mg content on strength and elongation) and Table 13 (properties of the six DIN 4113 standard alloys) are images with no text layer.
- **Cross-metal points with Al relevance:**
  - "Alloys with foreign metals that have a high solubility in copper cannot be age-hardened" [THI §10.2.4 p.91]. This restates the precipitation-hardening prerequisite: solubility must fall with temperature.
  - Cu alloys reach ~700 MPa (1500 MPa in special cases), "but the conductivity then falls considerably" [THI p.91].
  - Zn is hcp, with fewer slip planes and brittle at RT. Cold hardening is "largely excluded", and formability can only be improved by alloying [THI §10.3.1 p.93].
  - Titanium-zinc (0.1–0.2 % Ti + a little Cu) has higher creep strength than pure Zn and, THI states, 50 % lower thermal expansion [THI §10.3.3 p.94]. This is a microalloying-for-creep example.
  - Hot-dip galvanising grows a brittle Fe–Zn intermetallic layer under a ductile Zn layer. A short dip with rapid cooling (Sendzimir) suppresses the Fe–Zn layer [THI pp.94–95]. *Al transfer (inference):* the same time–temperature control governs Fe–Al intermetallic layers in Al–steel joints and Al-coated steel.

---

## 7. Transferable design rules (summary)

| # | Rule | Quantitative anchor | Source | Translation to wrought Al |
|---|---|---|---|---|
| 1 | Grain refinement gives strength and toughness together | k_HP = 0.165 MPa·m^½ (AA5083) | MMC18 Dussing | Use dispersoids + controlled recrystallisation for fine grain; HP is the largest UFG term (inference) |
| 2 | Orowan strength needs fine, closely spaced, non-shearable particles | Δσ = 0.13bG/λ·ln(d/2b); 50–200 nm optimum | MG18 p.8 | Size Mn/Cr/Zr dispersoids and nano-oxides accordingly |
| 3 | Coherent ordered precipitates: optimum fraction and minimum misfit | γ′ 60–70 % (best ~65 %); δ = 2(a′−a)/(a′+a) | SEG p.14–16, 35 | Minimise L1₂ Al₃X misfit for coarsening resistance (general knowledge) |
| 4 | Shearable clusters strengthen without losing ductility; there is a peak size | Cu clusters 2.5–3.0 nm; +100–200 MPa | MPF18 p.28 | GP-zone / pre-ageing design in 6xxx/7xxx (inference) |
| 5 | Matrix and precipitation can be tuned independently | ~494 MPa from precipitation in either matrix | SUP18 p.157 | Optimise texture/grain in TMP, then ageing separately (inference) |
| 6 | Non-dissolving dispersoids give high-temperature strength, and keep the matrix conductive | 133 MPa at 375 °C/10,000 h vs 11 MPa (1100-O). [FT] TD-Ni (2.2 % ThO₂) 1000-h rupture at 1093 °C = Nimonic 115 at 982 °C; thermal conductivity ≈83 vs 9–12 W/m·K | MMC18 p.24; EVE pp.85–90 | Al–Al₂O₃ / L1₂ dispersoid alloys for 250–400 °C service and for post-braze strength in conductive alloys |
| 7 | Each precipitate has a ceiling temperature | γ″ ≤650 °C; aged K-500 ≈540 °C | SEG p.17; EVE p.40 | Rate Al tempers by precipitate stability, not alloy series (inference) |
| 8 | Slow diffusers buy creep life | Re: 100 h → 1000 h; 10× rupture life 1st → 3rd gen. | SEG p.35–36 | Add Sc/Zr/Er-type slow diffusers to Al (general knowledge) |
| 9 | Too much refractory solute gives brittle intermetallics; set an alloying ceiling | TCP from Cr/Mo/W/Re (Ru mitigates); σ at 400–800 °C at PREn > 40 | SEG p.16; FAR D p.55, 61 | Cap Fe/Mn/Cu/Si totals by constituent-phase fraction (inference) |
| 10 | Microadditions have narrow optima | Ce 0.02 % best, >0.05 % harmful (FeCrAl); 0.5 % Y finest (Mg) | SUP18 p.61; MG18 p.91 | Screen Sc, Zr, Er, Sr and B at fine steps (inference) |
| 11 | Low interstitials/impurities enable toughness and weldability | C ≈ 0.01 (supermartensitic); C ≤ 0.1 for cryogenic Ni steel | FAR C–6, B–1 | Fe/Si limits as design inputs; scrap-tolerant phase design |
| 12 | Strength by TMP instead of composition | YS 300–400 → 500–1100 MPa at the same C | THI p.45 | Strength by TMP/ageing rather than more solute, to keep weldability and recyclability (inference) |
| 13 | Microalloy particles retard recrystallisation | Nb/Ti/V; finish rolling 900–700 °C | THI p.34–35 | Zr/Sc/Mn dispersoids for unrecrystallised extrusion/plate |
| 14 | Weldability is a composition budget | CE(IIW) < 0.45, no preheat; t8/5 controls the HAZ. [FT] CE, CET and Ito–Bessyo groupings verified from the PDF | THI p.72–73 | Define an Al HAZ/hot-cracking index (open). Al HAZ: solutionising + recrystallisation; work-hardening strength lost [THI p.88] |
| 15 | Corrosion ladders follow an index | PREn = Cr + 3.3Mo + 16N (30N for high-N austenitics; PREw with Mo + 0.5W). Ladder [FT]: 304L ~18 → 316L ~26 → duplex 26–35 → 904L ~37 → superduplex >40 → 6Mo 43–45 → 654 SMO ~55, the stainless ceiling; Ni alloys 45 to >50 on their own formula | FAR App. 1 p.172–173; C–5, D–0–D–2, E–3, F–0–F–4 | Build an IGC/SCC index for Al alloys (open). The index ignores oxidising vs reducing media [FAR G–3, G–4] |
| 16 | Peak strength often raises SCC susceptibility | 17-4PH at >1100 MPa is SCC-sensitive | FAR C–4 p.45 | Over-age (T7x) logic; Cu/Zn/Mg ratio windows (general knowledge) |
| 17 | Cold work is useless above the recrystallisation temperature for creep | Annealed Monel creeps less than cold drawn. [FT] 70/30 Cu–Ni loses all cold-work strength by ~649 °C | EVE Table 3-6; EVE p.106 | Don't rely on H-tempers for high-T Al parts (inference) |
| 18 | Critical strain gives coarse recrystallised grains | 5–12 % strain → coarse grain at 650–750 °C (steel) | THI p.71 | Avoid 2–10 % local strains before solution heat treatment (inference) |
| 19 | Texture is a design variable (fatigue, formability) | ⟨001⟩ E = 125 vs 294 GPa ⟨111⟩; RE texture doubles Mg El | SEG p.24; MG18 p.6 | Cube/r-value texture control in Al sheet (general knowledge) |
| 20 | Grain refinement through inoculant delivery and agitation | Mg 550 → 90 µm; AlN 1277 → 85 µm; EM stirring brings CET earlier | MG18 p.8, 71; CFD18 p.9 | Scrap-tolerant refining (EM/US) when TiB₂ is poisoned (inference) |
| 21 | Reinforcement must not consume matrix strengtheners | Mg + Al₂O₃ → spinel kills ageing | MMC18 p.13 | Choose inert reinforcements or offset Mg loss |
| 22 | Where E governs, raise E, not YS | SiC/Al 107.5 GPa → 37 % weight saving at equal EI | MMC18 p.8; THI p.57 | Al–Li or particle-stiffened Al for stiffness-limited parts |
| 23 | Melt cleanliness is a fatigue lever | +37.5 to +61 % gear fatigue | SUP18 p.123 | Filtration and oxide-film control in DC casting (inference) |
| 24 | Tramp residuals from scrap must be designed around | EAF route: Cu, S, P hard to remove. [FT] P in stainless held <0.01 % "by careful selection of raw materials and recycled scrap" | THI p.22; FAR B–0; FAR App. 5 p.184 | Fe/Cu-tolerant compositions for high-recycled-content Al; scrap sorting as a composition-control tool |
| 25 | [FT] Rank high-temperature alloys by creep or rupture tests, not short-time tensile tests | γ′ alloys had equal short-time strength above 649 °C, but 1000-h/871 °C rupture went 69 → 186 MPa as Al+Ti rose 3.6 → 9 % | EVE p.89 | Screen heat-resistant Al (fin stock, pistons, 2618-type) by creep/stress-relaxation tests (inference) |
| 26 | [FT] Precipitation strengthening costs less ductility than cold work | Ni-Span Hi: ageing ≈ 2 × strength with moderate El loss; cold work gives similar strength with drastic El loss. Ni-Span C: ageing 3 × YS | EVE p.184–185, 188–189 | Prefer T-tempers over H-tempers where post-strengthening formability matters (inference) |
| 27 | [FT] The grain-size optimum flips with temperature | 70 → 15 µm: UTS 338 → 414 MPa, El 49 → 36 % (Cu–Ni–Zn); coarse-grain 800/804 has 2 × the creep/rupture stress at 760–871 °C, but the gain vanishes at 982 °C/7 MPa | EVE p.117; EVE Table 4-14 p.78–79; FAR I–0 | Slugs: coarser grain = softer slug, set within 20–100 µm against surface roughening (inference). Creep parts: coarse grain |
| 28 | [FT] Work-hardening rate is a composition target for forming | 301 (high WH) vs 305/384/385 (low WH); low-C Ni 201 for deep drawing | EVE p.9, p.129–135 | For impact-extrusion slugs, minimise solute-driven work hardening (Mn, Mg in solid solution); see §1.9 (inference) |
| 29 | [FT] Oxide protectiveness follows the oxide/metal volume ratio; inner barrier oxides and atmosphere control growth | PBR from THI densities: MgO 0.78 (non-protective), Al₂O₃ 1.28–1.50; Si-oxide sub-layer stops Cr₂O₃ growth in 45TM; selective oxidation of 80Ni–20Cr in partly reducing atmospheres | THI Table 14 p.97 (PBR my calculation); FAR I–2 p.152; EVE p.161 | MgO growth on Al–Mg strip during annealing: control dew point/O₂ and Mg surface supply; test barrier-forming microadditions (inference) |
| 30 | [FT] Alloy for process robustness, not only peak values | Mo/Cr/Cu/V cut the cooling-rate sensitivity of Ni–Fe magnetic alloys; W–Ni–Fe vs W–Ni–Cu: 19 % vs <1 % El after slow cooling | EVE p.194, p.218 | Choose Mn/Fe/Si so that slug grain size and HB are insensitive to coil position and heating rate (inference) |
| 31 | [FT] Fix HAZ precipitation by cutting residuals, not by adding alloy | C → C-276 and B → B-2: very low C + Si remove HAZ intermetallics and grain-boundary precipitates | FAR G–1/G–2 p.102–105; J–3 p.170 | Fe/Si caps for weldable 6xxx/7xxx (inference) |
| 32 | [FT] Slow-diffusing solutes segregate in solidification: over-alloy or homogenise | 6–7.5 % Mo superaustenitics are welded with over-alloyed Ni-base fillers because of Mo segregation | FAR F–3 p.88–89; F–4 p.91 | Mn/Cr/Zr/Sc coring in DC ingots: homogenisation practice sets the dispersoid distribution (inference) |
| 33 | [FT] Sensitisation is a time–temperature window with three exits | Cr-carbide grain-boundary precipitation at 427–788 °C; exits: re-solution + quench, low C (<0.03 %) or ELC (<0.02 %), Ti/Nb at ≈10 × C | EVE p.131; FAR E–0 p.68, E–1 p.70, App. 1 p.172 | 5xxx β-phase sensitisation: thermal history, Mg cap, stabilising tempers (general knowledge/inference) |
| 34 | [FT] Service inside the ageing range keeps ageing the alloy | PH stainless at 316–538 °C ages further in service; 625 loses ductility near 700 °C | EVE p.148; FAR G–0 p.101 | 2xxx/6xxx at 100–200 °C drift in service; design to the over-aged state (inference) |
| 35 | [FT] Supply-driven substitution is a standing design mode | Mn + N for Ni (200 series, Nitronics); W for Mo and less Co (Soviet superalloys); element cost index Fe 1 … Co 110 | FAR E–4 p.76–77, App. 4 p.178–179; EVE p.84, p.131 | Sc → Zr/Er/Mn-dispersoid substitution; CRM exposure per unit of property (inference) |
| 36 | [FT] Solute costs conductivity, dispersoids keep it, and ageing restores part of it | Cu–Ni resistivity ≈19 → 50 µΩ·cm from 10 to 45 % Ni; TD-Ni 7.6 vs γ′ alloys 120–133 µΩ·cm; ageing lowers resistivity (Duranickel 301: 45 → 43 µΩ·cm) | EVE p.102, Table 5-2 p.86, p.204 | Conductivity as a process-control signal for Mn precipitation in 3xxx (general knowledge) |

---

## 8. Open questions / gaps

1. **Truncation (partly resolved 2026-10-12).** FAR, EVE and THI are now read in full (§Sources). Still unread:
   - HIG chapters on alloy steels, Al, Ni/Ti/Mg and composites.
   - SEG Part II (appended papers).
   - The TMS 2018 volumes beyond the page ranges in the sources table.
   - SEG (S-063, 0.62 MB) can be downloaded and converted locally the same way. HIG (S-075, 26.90 MB) is above the ~10 MB whole-download limit and needs another route [catalog.md].
2. **Schaeffler/DeLong (Cr_eq/Ni_eq) and Md/Nv are still general knowledge.** PREN/PREw/PRE are now sourced [FAR App. 1 p.172–173]. A full-text search confirmed that FAR, EVE and THI print no constitution diagram and no Cr/Ni-equivalent formula. A primary source is needed: e.g. WRC-1992 or the original Schaeffler/DeLong papers, and the SUP18 molecular-orbital papers (pp. 377, 453) for Md critical values.
3. *(Resolved 2026-10-12: the CET grouping was verified from the PDF's word positions [THI p.72]; see §1.8. The number is kept so that cross-references from other chapters stay valid.)*
4. **No Fe-tolerance or recycled-content Al alloy design paper** was in the returned TMS text. The relevant items (HTMP18 p.199 dross recovery; SUP18 p.359 fluidity/hot tearing) are TOC-only. This is the largest gap for the project's sustainability goal.
5. **No recrystallisation-modelling paper for Al** was found in the returned text. The MG18 recrystallisation papers (pp. 209, 275) and CFD18 DC-casting items need reading.
6. **Transfer hypotheses to test:**
   - Can an Md-type d-electron descriptor rank TCP-like constituent-phase risk in multicomponent recycled Al?
   - Is there an Al analogue of Ru, an element that delays coarsening or harmful-phase formation of L1₂ Al₃(Sc,Zr) without forming primary phases?
   - Can EM/ultrasonic grain refinement replace TiB₂ in high-Zr or high-Si scrap-based melts, where TiB₂ poisoning is reported in general knowledge?
   - Would a PREn-style index (for example from Cu, Zn/Mg and Fe-intermetallic fraction) predict IGC/SCC ranking within 7xxx?
   - **[FT 2026-10-12]** Can a barrier-forming microaddition or a pre-oxidation step slow MgO growth on Al–Mg slugs during annealing, by analogy with the Si-oxide sub-layer under Cr₂O₃ in alloy 45TM [FAR I–2 p.152]? Test it against the atmosphere lever (dew point/O₂; selective oxidation [EVE p.161]) and the Mg-content lever. The MgO PBR of 0.78 (§1.7.1) predicts non-protective, continuing growth.
   - **[FT 2026-10-12]** Can the 3102/3207 slug composition be chosen to make recrystallised grain size and HB insensitive to furnace heating rate and coil position (§1.5 process robustness), rather than to hit a single optimum?
   - **[FT 2026-10-12]** Does the TD-Ni lesson (§1.4) hold quantitatively for Al₃Zr-dispersoid conductor alloys: how much RT strength is given up for strength retained after a braze cycle, at what conductivity?
7. **The superalloy compositions table** (SEG Table 1) is mis-aligned in the extraction. Only Re levels are trusted. Re-extract before using compositions.
8. **The HTMP18 Drive ID returned empty text.** A byte-identical copy (`1oBif3n1WXGDbxiHMyU2og1Q4FInjNwzJ`) was used. Confirm that it is the intended file, or clean up the duplicate.
9. **[FT 2026-10-12] THI image-only content.** Table 13 (the six DIN 4113 Al standard alloys with Rp0.2), Bild 85 (common Al alloys) and Bild 86 (effect of Mg content on strength and elongation) have no text layer. They need OCR or a visual read. Bild 86 is the most relevant to the Al–Mg work.
10. **[FT 2026-10-12] Source inconsistencies to keep in view.**
    - Alloy 600 Cr: 21 % in FAR G–7 vs 16 % in FAR I–1 and 15.5 % in EVE. Taken as an error in G–7 (§3.1).
    - Stainless threshold: 10.5 % Cr [THI] vs >11.5 % [EVE] (§1.7).
    - THI's density argument for oxide protectiveness conflicts with the Pilling–Bedworth view for MgO (§1.7.1).
    - THI labels the Ito–Bessyo formula "CE_V" (§1.8).
11. **[FT 2026-10-12] EVE figures.** Many EVE property data exist only as graphs (S–N curves, hot-tensile and cryogenic curves) whose axes are OCR-garbled. Only the values stated in the prose or tables are used here. Digitising the figures would need a visual read of the PDF pages.
