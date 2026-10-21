# 20 — Aluminium foam (closed-cell): routes, metallurgy, properties, relevance

**Scope.** This chapter covers what closed-cell aluminium foam is, how it is made, the physical metallurgy that
controls foaming, the main properties and applications, and what it could mean for the user's rotary-cast,
scrap-based route.

**Basis.** Web research on 2026-10-21, at snippet and abstract level. The Drive library has no foam source; a
Drive search for "aluminium foam", "metal foam" and "TiH2" found only general aluminium books. Content not from a
listed source is marked *(general knowledge)*. Each claim below needs checking against the full papers before it
is used for a decision.

**Trigger.** The user showed a foam sample (photo, 2026-10-21) and confirmed it is aluminium foam. See §6.

## Sources

| Key | Source | URL | Level |
|---|---|---|---|
| W20-01 | Review: "Fabrication, Processing, Properties, and Applications of Closed-Cell Aluminum Foams" (2024) | https://pmc.ncbi.nlm.nih.gov/articles/PMC10856566/ | snippet |
| W20-02 | "Metal Foam by Powder Metallurgy Routes: A Review Paper" | https://stmjournals.nanoschool.in/index.php/JoPRM/article/view/6662 | snippet |
| W20-03 | PM foam theses and papers, İzmir Institute of Technology (TiH2 pre-treatment, Al2O3 / SiC additions) | https://gcris.iyte.edu.tr/bitstream/11147/2979/1/T000848.pdf ; https://gcris.iyte.edu.tr/bitstream/11147/3774/1/T000022.pdf | snippet |
| W20-04 | TiH2 decomposition vs Al melting; Sn alloying; CaCO3 vs heat-treated TiH2 (thesis and papers) | https://digitalarchive.library.bogazici.edu.tr/bitstreams/474f86b8-b8e5-40a6-9a68-58eab5bdd7b5/download ; https://matsc.ktu.lt/index.php/MatSc/article/view/6082/4359 ; https://www.mdpi.com/1996-1944/17/3/710/html | snippet |
| W20-05 | US 5,482,533 A, "Method for manufacturing foam aluminum product" (Ca thickener + TiH2, closed-vessel melt foaming; assignee not verified) | https://patents.google.com/patent/US5482533A | snippet |
| W20-06 | Gas-injection (SiC-stabilised) foam studies | https://scientiairanica.sharif.edu/article_1726.html ; https://rmme.ijournals.cn/rmmeen/article/pdf/20250062 | snippet |
| W20-07 | FORMGRIP (cast SiCp-MMC precursor with passivated TiH2; Gergely & Clyne 2000, as cited) and Formgrip-type A356 work | https://arxiv.org/pdf/1708.01613 ; https://mt.ujep.cz/artkey/mft-201901-0020_theoretical-calculations-of-the-foaming-properties-of-powder-agents-for-the-production-of-aluminium-foams.php ; https://www.scientific.net/MSF.817.42 | snippet |
| W20-08 | Foam from scrap: swarf + TiH2; UBC + TiH2; Ti build-up on recycling foam | https://advancedsciencenews.com/aluminum-foam-from-scrap ; https://test.greenmetallurgy.rwth-aachen.de/wp-content/uploads/2025/06/friedrich_al_fo_id_9209.pdf ; https://publica.fraunhofer.de/entities/publication/8a8fac47-07c5-430f-a6ed-6cc617127b33 | snippet |
| W20-09 | Gibson–Ashby fits and Alporas compression (Kádár et al.) | https://www.kfki.hu/anyagokvilaga/tartalom/2005/jan/06_Kadar.pdf ; https://epub.uni-bayreuth.de/8347/2/1-s2.0-S0142941824000655-main.pdf | snippet |
| W20-10 | Aluminium foam sandwich (AFS): automotive review 2024, Fraunhofer IWU railcar AFS, commercial products (Alulight, Pohltec AFS) | https://link.springer.com/article/10.1007/s11837-024-06460-2 ; https://publica.fraunhofer.de/handle/publica/379173 ; https://www.mdpi.com/2075-4701/1/1/98 | snippet |

## 1. What it is

- **Closed-cell aluminium foam** is a cellular metal of separate gas-filled cells. Typical values [W20-01]:
  - density ≈ 0.05–1.3 g/cm³, porosity up to 98 %;
  - cell size ≈ 1–25 mm;
  - compressive plateau stress ≈ 2–30 MPa.
- Foams made by heating a **precursor inside a mould** grow a dense **integral skin** where the expanding metal
  meets the mould wall (general knowledge). Foam cut from a **block** has open cut faces.
- In an **aluminium foam sandwich (AFS)**, two solid aluminium face sheets are held apart by a foam core, bonded
  metallurgically rather than glued [W20-10].

## 2. Production routes

| Route | How it works | Typical features | Source |
|---|---|---|---|
| **Powder metallurgy (PM)** | Al-alloy powder + TiH2 (or another blowing agent) → dense precursor by hot extrusion or pressing → heated above the melting range in a mould | Integral skin; near-net shapes; AFS by roll-bonding precursor between sheets. Examples: Alulight, Pohltec AFS | [W20-02; W20-10] |
| **Melt route with thickener (Alporas-type)** | Ca stirred into the melt to raise viscosity, then TiH2; foamed in a closed vessel | Block foam; only the stable, uniform middle of the block is cut out and used. TiH2 and granulated Ca add cost; CaCO3 proposed as a cheaper agent | [W20-05; W20-04] |
| **Gas injection** | Gas blown into a melt that contains ceramic particles (SiC); particles stabilise the bubbles; foam skimmed off and solidified as slab or panel | Large cells. Cell size rises with gas flow rate; one study found the best stability at ≈ 6 wt % SiC | [W20-06] |
| **Cast precursor (FORMGRIP)** | Passivated TiH2 stirred into a SiC-particle-reinforced melt, which is **cast** into a foamable precursor; the precursor is later reheated and foams near the liquidus | Melt-route precursor without powder; needs particles and fast solidification | [W20-07] |
| **Scrap-based** | Remelted machining swarf or used beverage cans + TiH2; or thixocast briquetted chips | Surface oxides from scrap act as a thickener (helps foaming) but distort the cells | [W20-08] |

## 3. Physical metallurgy that controls foaming

1. **Matching the blowing agent to the alloy's melting range** (the central issue).
   - TiH2 releases hydrogen from about 450 °C, with a range of about 450–650 °C, i.e. below pure Al's ≈ 660 °C.
     Gas released before the metal melts escapes or makes crack-like pores [W20-04].
   - Al–Si alloys melt over about 570–615 °C; TiH2 starts decomposing at about 465 °C; one study got uniform
     cells at 565 °C [W20-04].
   - Ways to delay the gas: heat-treating TiH2 in air at 400–500 °C forms an oxide shell and shifts
     decomposition up by up to ≈ 75 °C [W20-03; W20-04]. Results conflict, though: one study found heat-treated
     TiH2 foamed worst and **CaCO3** (decomposes from about 660 °C, which suits unalloyed Al) foamed best
     [W20-04]. Alloying with ≤ 5 % Sn has also been used [W20-04].
   - **Consequence (inference):** low-melting Al–Si alloys (AlSi7, AlSi10, AlSi6Cu4 class, general knowledge)
     and 6xxx are the natural foaming alloys. Lean 1xxx/3xxx (liquidus ≈ 655–660 °C) are poorly matched to TiH2.
2. **Bubble stabilisation.** Liquid foam drains and its cells coalesce unless the cell walls carry fine solid
   particles or oxides. Al2O3 additions prevented drainage and coalescence [W20-03]; SiC particles reduced
   drainage [W20-07]. In melt routes, Ca (forming oxides) or SiC do this job [W20-05; W20-06].
3. **Ti build-up on recycling.** Foam made with TiH2 can raise Ti in the remelted metal to about 0.7 %, which has
   to be diluted [W20-08]. *(Relevance: the user's alloys limit Ti to ≤ 0.10 and Talum 1 targets 0.043. Any
   foam scrap in the charge needs tracking.)*

## 4. Properties

- **Plateau stress rises with relative density** in both closed- and open-cell Al foams. Dynamic compression at
  ≈ 700 s⁻¹ raised the plateau stress markedly compared with quasi-static tests [W20-01; W20-03].
- **Scaling (Gibson–Ashby).**
  - Plateau stress ∝ (relative density)^n with n ≈ 1.5 (general knowledge). One study used C ≈ 0.3 and n = 1.5 as
    the reference curve when fitting its own Al foams [W20-09].
  - Stiffness scales roughly with (relative density)² (general knowledge).
  - Real foams fall below the ideal closed-cell model because of wall curvature, wrinkles and uneven density
    (general knowledge).
- **Cell structure.** Collapse starts at the weakest, largest cells. Uniform cell size and wall thickness give a
  flatter, higher plateau (general knowledge; consistent with [W20-09]). In one study SiC raised the plateau
  stress [W20-03].

## 5. Applications and market

- **Automotive:** AFS for battery boxes [W20-10]. Crash elements such as bumpers and pillars, where impact energy
  is converted into plastic collapse [W20-10].
- **Railway:** 3D AFS parts for railcars without glued joints (Fraunhofer IWU) [W20-10].
- **Other uses:** sound and vibration damping, fire walls, architecture (general knowledge).
- **Market status:** a 2024 review states that the "industrial breakthrough" of metal foams "is yet to come"
  [W20-10]. The market remains niche.

## 6. The user's sample (photo, 2026-10-21)

*Observation from the photo; no measurements yet.*
- ≈ 20 mm thick piece with a **dense integral skin of ≈ 1–2 mm on both faces**. This points to a precursor
  foamed in a mould (PM or cast precursor) or an AFS-type panel, not a cut block.
- **Rounded closed cells of ≈ 0.5–6 mm**, with some **merged large cells** and broken walls, showing coalescence
  and drainage during foaming. The cell walls look relatively thick, suggesting a fairly high density for a foam.
- **To characterise it:**
  - density (mass / volume → relative density, using 2.70 g/cm³ for solid Al);
  - cell-size distribution and wall thickness from a polished section;
  - skin thickness;
  - chemistry, to identify the alloy and blowing-agent residues such as Ti and Ca;
  - quasi-static compression for plateau stress and energy absorbed up to densification.

## 7. Relevance to the user's route (inference)

1. **Rotary-cast foamable precursor (a research idea, not a known route).** A FORMGRIP-type melt precursor needs
   passivated TiH2 dispersed in a particle-containing melt and **fast solidification**, so that little gas
   escapes before the metal freezes [W20-07]. The rotary caster solidifies a 22 mm strip in seconds, and the
   in-line mill could densify it. Unknowns:
   - how much TiH2 decomposes in the launder and caster;
   - particle handling;
   - safety (hydrogen).
2. **Alloy choice.** Foaming suits Al–Si (and 6xxx) melting ranges (§3.1). Talum's lean 1xxx/3xxx alloys are
   poorly matched unless the gas release is delayed (pre-oxidised TiH2 or CaCO3). An AlSi7-type alloy from scrap
   would be the starting point.
3. **Scrap and recycling.** Scrap oxides can help stabilise foam [W20-08]. In the other direction, foam scrap
   brings Ti (up to ≈ 0.7 %) into a remelt [W20-08], which matters for the Ti limits of Talum's slug and disc
   alloys.
4. **Business case.** The market is niche and still developing [W20-10]. A low-cost, high-recycled-content foam
   precursor strip would be a differentiator, but only after a lab feasibility study.

## 8. Gaps

- No full-text source has been read yet. Missing:
  - quantitative process windows (TiH2 content, foaming temperature and time, particle fraction);
  - the full Gibson–Ashby closed-cell equations;
  - property data for commercial foams;
  - an authoritative Alporas recipe (the 1.5 % Ca / 1.6 % TiH2 figure often quoted was not confirmed).
- **Network note:** publisher sites were blocked for full text in earlier sessions (see README). A foam handbook
  (e.g. Banhart's reviews; Ashby et al., *Metal Foams: A Design Guide*) on Drive would close most gaps.
