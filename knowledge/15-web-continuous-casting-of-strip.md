# 15 — Continuous casting of strip (TRC, twin-belt, block, wheel) vs DC: metallurgy for lean 3xxx/1xxx slug stock

**Source type: online research (not from the user's Drive), retrieved 2026-10-12.**

**Scope.** This chapter covers continuous strip casting of aluminium and how it changes downstream annealing. The casters covered are twin-roll (TRC), twin-belt (Hazelett), block (Alusuisse Caster II / Lauener) and wheel or narrow-strip (Properzi/Rigamonti type). The topics are:
- process windows;
- the as-cast microstructure: Mn supersaturation, through-thickness gradients, centreline segregation and surface bleeds;
- what the CC route does to homogenisation, concurrent precipitation, recrystallisation kinetics, grain shape and texture;
- alloy-design levers.

The focus is lean 3xxx (AA3003/3105/3015-type) and 1xxx strip, about 20 mm thick at the start. The strip is cold rolled, blanked into slugs, annealed and impact-extruded into aerosol cans. This chapter fills the TRC/CC gap flagged in ch. 02 §10 item 2 and ch. 07 §2.3 / §11 (G3, G5, G11).

**Conventions.**
- Every claim carries a `[W15-xx]` key from the table below.
- "(derived)" marks arithmetic on source numbers, such as unit conversions (K → °C, inch → mm).
- "(inference)" marks reasoning by the author of this chapter, not a statement in a source.
- Cross-references to Drive-based chapters use "ch. 0x §y".

**⚠ Access limitation — read before using any number.** No full text could be read for this chapter, for two reasons:
- The session's network policy denied every publisher and repository host tried: mdpi.com, link.springer.com, sciencedirect/ncbi/pmc, scientific.net, jmst.org, hal.science, d-nb.info, researchgate.net, osti.gov, patents.google.com, uspto.gov, aluminium-guide.com (TALAT) and dergipark.org.tr.
- The shared web-search budget ran out part-way through the work.

Every entry is therefore **(abstract only)** or **(snippet only)**: text returned in search results, which the search tool may have paraphrased. Numbers are reproduced as they appeared there. Check each one against the original before using it in a model or a specification.

---

## 0. Sources

"read" column: **abstract** = the publisher abstract or highlights came back in the search result. **snippet** = only fragments or third-party summaries came back. No source was read in full.

| Key | Authors | Year | Title | Journal / publisher | DOI / URL | Read |
|---|---|---|---|---|---|---|
| W15-01 | EAA TALAT (author not shown) | n.d. | TALAT Lecture 3210 "Continuous casting of aluminium" | TALAT training series | https://www.aluminium-guide.com/wp-content/uploads/2020/01/3210.pdf | snippet |
| W15-02 | Properzi S.p.A. | n.d. | "About us" (company history) | company web page | https://properzi.com/company/about-us/ | snippet |
| W15-03 | (assignee not shown) | n.d. | "Aerosol can fabrication process", US 7,520,044 | US patent | https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/7520044 | snippet |
| W15-04 | (assignee not shown) | various | Patent family on CC slug stock: "Impact extruded containers from recycled aluminum scrap" (US 9,663,846; US 12,385,112), "Aluminum alloy slug for impact extrusion" (US 10,584,402), "Aluminum alloy for impact extruded containers and method of making the same" (US 11,519,057) | US patents | https://patents.google.com/patent/US10584402B2/en ; https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/9663846 | snippet. The search result did not say which family member carries which number |
| W15-05 | Total Materia (editorial) | n.d. | "Twin belt casting" | Total Materia article (secondary) | https://www.totalmateria.com/en-us/articles/twin-belt-casting | snippet |
| W15-06 | Farouk B., Kim (initial not shown), Apelian D. | 1991 (per result) | Numerical study on the solidification processes in a twin-belt (Hazelett) caster (title truncated) | Drexel research record | https://researchdiscovery.drexel.edu/esploro/outputs/journalArticle/NUMERICAL-STUDY-ON-THE-SOLIDIFICATION-PROCESSES/991019173527804721 | abstract (record) |
| W15-07 | Kim (initial not shown) | 1988 (per result) | Coupled heat transfer and fluid flow … (Hazelett caster, doctoral dissertation; title truncated) | Drexel University | https://researchdiscovery.drexel.edu/esploro/outputs/doctoral/991021888906704721 | abstract (record) |
| W15-08 | Sahoo S. | 2016 | Review on vertical twin-roll strip casting: a key technology for quality strips | J. Metallurgy 2016, art. 1038950 | https://doi.org/10.1155/2016/1038950 | snippet |
| W15-09 | (authors not shown) | 2025 | Multi-field coupling analysis of twin-roll casting process for achieving thin aluminum strip high-speed casting and fabricating laminated metal cladding materials | ScienceDirect, PII S2214157X25006835 | https://www.sciencedirect.com/science/article/pii/S2214157X25006835 | snippet |
| W15-10 | (authors not shown in result) | n.d. | "High speed twin roll casting of 6016 aluminium alloy strip"; "Twin roll casting of aluminum alloy strips"; "Twin roll casting of aluminium alloys" (MSEA, PII S0921509399006760) | research-caster papers (cluster) | https://www.researchgate.net/publication/42339085 ; https://www.researchgate.net/publication/229420652 ; https://www.sciencedirect.com/science/article/abs/pii/S0921509399006760 | snippet. ⚠ **Cluster:** the search tool merged several TRC papers, so the attribution of each number to an individual paper is unresolved |
| W15-11 | Sun N., Patterson B.R., Suni J.P., Simielli E.A., Weiland H., Allard L.F. | 2006 | Microstructural evolution in twin roll cast AA3105 during homogenization | Mater. Sci. Eng. A 416(1–2) 232–239 | https://www.sciencedirect.com/science/article/abs/pii/S0921509305012426 | abstract |
| W15-12 | Sun N. et al. | 2008 | Effect of heating rate on recrystallization of twin roll cast aluminum | Metall. Mater. Trans. A 39, 165–170 | https://doi.org/10.1007/s11661-007-9367-3 | abstract |
| W15-13 | Lv, Du, An, Huang, Xu, Sun (initials not shown) | 2015 | Centerline segregation mechanism of twin-roll cast A3003 strip | J. Alloys Compd. 643, 270–274 | https://www.sciencedirect.com/science/article/abs/pii/S0925838815011470 | abstract |
| W15-14 | Ullmann M., Stirl (initial not shown), Prahl U. | 2024 | Twin-roll casting defects in light metals | J. Mater. Sci. 59, 19003–19022 | https://doi.org/10.1007/s10853-024-10211-8 | snippet |
| W15-15 | Lockyer S.A., Yun M., Hunt J.D., Edmonds D.V. | 1996 | Micro- and macrodefects in thin sheet twin-roll cast aluminum alloys; companion paper "Microstructural defects in thin sheet twin roll cast aluminium alloys", Mater. Sci. Forum 217–222, 367–372 | Mater. Charact. 37, 301–310 | https://doi.org/10.1016/S1044-5803(97)80019-8 | snippet, via citing papers only |
| W15-16 | (authors not shown) | n.d. | The formation of surface bleeds in twin roll cast aluminium sheet | (journal not shown) | https://www.researchgate.net/publication/282591961 | snippet |
| W15-17 | Hadadzadeh A., Wells M.A. | 2015 | Inverse and centreline segregation formation in twin roll cast AZ31 magnesium alloy | Mater. Sci. Technol. | https://doi.org/10.1179/1743284714Y.0000000750 | snippet (Mg alloy; mechanism only) |
| W15-18 | (Brunel University thesis; author not shown) | n.d. | Twin roll casting and melt conditioned twin-roll casting of magnesium alloys | Brunel Univ. thesis | https://bura.brunel.ac.uk/bitstream/2438/2686/1/ | snippet (Mg alloy; mechanism only) |
| W15-19 | (authors not shown) | 2020 | A novel approach to improve the microstructure and mechanical properties of Al–Mg–Si aluminum alloys during twin-roll casting | Materials 13, 1713 | https://doi.org/10.3390/ma13071713 | snippet |
| W15-20 | (authors not shown) | 2022 | Kirkendall effect in twin-roll cast AA 3003 aluminum alloy | Crystals 12(5), 607 | https://doi.org/10.3390/cryst12050607 | snippet |
| W15-21 | (authors not shown; Jeonbuk National Univ.) | n.d. | Microstructural evolution of twin roll cast Al-Mn alloy during cold [rolling …] (title truncated) | (journal not shown) | https://pure.jbnu.ac.kr/en/publications/microstructural-evolution-of-twin-roll-cast-almn-alloy-during-col/ | snippet |
| W15-22 | Kuang, Zhao, Zhang, Zhang, Liu, Sun, Xu, Wang (initials not shown) | 2022 | Impact of thermal exposure on the microstructure and mechanical properties of a twin-roll cast Al-Mn-Fe-Si strip | J. Mater. Sci. Technol. 107, 183–196 | https://doi.org/10.1016/j.jmst.2021.07.022 | snippet |
| W15-23 | Birol Y. | 2009 | Homogenization of a twin-roll cast thin Al–Mn strip | J. Alloys Compd. 471, 122–127 | https://doi.org/10.1016/j.jallcom.2008.04.005 | snippet (from a third-party "cited-by" listing) |
| W15-24 | (authors not shown) | 2013 | Effect of homogenization on recrystallization of twin roll cast AA3003 alloy | Appl. Mech. Mater. 404, 122 | https://www.scientific.net/AMM.404.122 | snippet |
| W15-25 | Işıksaçan C., Atar (initial not shown) et al. | 2026 | Recrystallization and softening kinetics of an EN AW-3105 aluminum alloy produced via twin-roll casting | J. Alloys Compd. 1065 | https://www.sciencedirect.com/science/article/abs/pii/S0925838826021043 | abstract |
| W15-26 | Gülver (initial not shown), Meydanoğlu O., Işıksaçan C. | 2019 | Softening behavior of direct chill and twin-roll cast AA 3105 alloy | Light Metals 2019 (Springer), ch. 140 | https://doi.org/10.1007/978-3-030-05864-7_140 | abstract |
| W15-27 | Spathis D., Tsiros J., Mavroudis (initial not shown) (ELVAL) | 2016 | Annealing curve of 3105 alloy produced by twin roll and belt casting method | Light Metals 2016, pp. 1031–1035 | https://doi.org/10.1002/9781119274780.ch172 (also Springer 10.1007/978-3-319-48251-4_172) | abstract |
| W15-28 | Liu W.C. et al. | 2008 | Effect of heating rate on the microstructure and texture of continuous cast AA 3105 aluminum alloy | Mater. Sci. Eng. A 478, 173–180 | https://www.sciencedirect.com/science/article/abs/pii/S0921509307011215 | abstract |
| W15-29 | (authors not shown) | n.d. | Evolution of recrystallization and recrystallization texture in continuous-cast AA 3015 aluminum alloy | (journal not shown) | https://www.researchgate.net/publication/226530663 | abstract |
| W15-30 | (authors not shown) | n.d. | Recrystallization textures of continuous cast AA 3015 alloy: development of the P orientation {011}⟨566⟩ | (journal not shown) | https://www.researchgate.net/publication/225625265 | abstract |
| W15-31 | (authors not shown) | n.d. | Quantifying the recrystallization of cold rolled AA 3015 aluminum alloy by X-ray diffraction | OSTI ETDE record 22049594 | https://www.osti.gov/etdeweb/biblio/22049594 | abstract |
| W15-32 | Wang W.X., Zhang J.X., Wang Z.J., Liu W.C. | 2018 | A comparative study of the transformation kinetics of recrystallization texture of CC and DC 3003 aluminum alloys | Mater. Charact. 141, 412–422 | https://www.sciencedirect.com/science/article/abs/pii/S1044580318300135 | abstract |
| W15-33 | (same group as W15-32; first author "Z…") | 2020 | Effect of processing method on the recrystallization behavior of cold-rolled AA3003 aluminum alloy | J. Mater. Eng. Perform. 29, 4286 | https://doi.org/10.1007/s11665-020-04963-y | snippet |
| W15-34 | Slámová M., Sláma P., Cieslar M. | 2006 | The influence of alloy composition on phase transformations and recrystallization in twin-roll cast Al-Mn-Fe alloys | Mater. Sci. Forum 519–521, 365–370 | https://www.scientific.net/MSF.519-521.365 | abstract |
| W15-35 | (authors not shown) | ~2016–17 | Influence of pre-recovery on the subsequent recrystallization and mechanical properties of a twin-roll cast Al-Mn alloy | Mater. Sci. Eng. A | https://www.sciencedirect.com/science/article/abs/pii/S0921509316313685 | abstract (partial) |
| W15-36 | (authors not shown) | 2018 | Effect of pre-recovery on subsequent recrystallization kinetics in moderately deformed and supersaturated Al-Mn alloys | J. Cent. South Univ. | https://doi.org/10.1007/s11771-018-3758-z | snippet |
| W15-37 | (authors not shown) | n.d. | Recrystallization behavior of twin-roll cast 3xxx series aluminum alloy | (journal not shown) | https://www.researchgate.net/publication/282585506 | snippet (text partly garbled) |
| W15-38 | Šlapáková Poková M., Cieslar M., Zimina M. | 2015 | Grain refinement in Al-Mn-Fe-Si alloys by severe plastic deformation; plus Charles Univ. thesis record on TRC Al-Mn(-Zr) sheets with two-step precipitation anneal | Manuf. Technol. 15(4), 679–684; dspace.cuni.cz 20.500.11956/68959 | https://doi.org/10.21062/ujep/x.2015/a/1213-2489/MT/15/4/679 | snippet |
| W15-39 | (authors not shown) | 2022 | Single-belt casting of AA6111 strip (gauge effect on grain size and SDAS) | Metall. Mater. Trans. A | https://doi.org/10.1007/s11661-022-06675-5 | snippet |

**Located but not read (title or record only; no claims are drawn from them; leads for follow-up):**
- Birol Y. (2009), "Recrystallization of twin-roll cast Al–Fe–Si foil stock processed without homogenization", J. Alloys Compd. 488, 112–116, doi:10.1016/j.jallcom.2009.08.135. **This is the key 1xxx/8xxx lead.**
- Birol Y., "Thermomechanical processing of a twin-roll cast Al–1Fe–0.2Si alloy", J. Mater. Process. Technol. (PII S0924013607009144).
- "3D analysis of macrosegregation in twin-roll cast AA3003 alloy", Mater. Charact. (PII S1044580316301255).
- "Segregation mechanisms and their effects on the aluminium flat rolled products (sheet/foil) produced by twin roll casting technology", Light Metals 2023, doi:10.1007/978-3-031-22532-1_138.
- "Abating recrystallization inhomogeneity in twin-roll cast 3003 aluminum sheet by electromagnetic fields", Appl. Phys. A (2017), doi:10.1007/s00339-017-1449-5.
- "Effect of roll-separating force and Mg content on recrystallization behavior of twin-roll cast AA3105 aluminum alloys", Light Metals 2026, doi:10.1007/978-3-032-13832-3_43.
- "Improved iron-tolerance in recycled aluminum alloys via direct strip casting process", arXiv:2310.06327.
- "Technical issues impeding the proliferation of continuous casting processes in the aluminum industry" (ResearchGate 236202278).
- "Texture evolution of continuous cast and direct chill cast AA 3003 aluminum alloys during cold rolling", Scripta Mater. (PII S1359646204002192).
- "Effect of rolling reduction on the P{011}⟨455⟩ recrystallization texture in a supersaturated Al-Mn-Mg alloy".
- "Influence of Si and Fe on the distribution of intermetallic compounds in twin-roll cast Al–Mn–Zr alloys", J. Alloys Compd. (PII S0925838811021888).
- "Effect of annealing on microstructure and properties of twin-roll-cast Al–Mn alloys with different copper content", Int. J. Mater. Res., doi:10.3139/146.110044.
- "Heating rate effect on microstructure evolution during annealing of twin roll cast AA3105" (ORNL record).
- Sun N., PhD thesis, Univ. Alabama at Birmingham (2006), "Microstructure evolution in twin roll cast AA3105" (ProQuest 305351598).
- "Production of 3004 aluminum alloy sheet for structural applications from twin roll casting", Light Metals 2017.
- "Corrosion of EN-AW 3105 aluminum strip produced via twin-roll casting with a steel/copper roll pair", Light Metals 2024.
- "Effects of Si, Fe, Mn and Mg on solidification characteristics of EN-AW 3105: a CALPHAD-based multi-objective optimization", Engineering Perspective 6(3) (2026).
- "Effect of casting conditions and composition on microstructural gradients in roll cast aluminum alloys" (academia.edu).
- ABM Proceedings (Brazil), "Otimização da estampabilidade da liga AA3003 obtida pelo processo de vazamento contínuo". This is the only circle/drawing-stock lead found.
- "Mechanical properties of three typical aluminum alloy strips prepared by twin-roll casting", J. Mater. Res. Technol. (2023).

---

## 1. Process types and windows

### 1.1 Mechanisms
- **TRC.** The two solidifying shells meet at the "kiss point" in the roll gap. Solutes accumulate there, and the height of the kiss point controls centreline segregation [W15-13]. Solidification and hot reduction happen in the same roll gap (ch. 02 §4.1).
- **Twin-belt (TBC, Hazelett).** Solidification takes place over a **longer sump depth and more slowly than in TRC**. This changes both the work-hardening rate and the final annealing response of 3105 [W15-27]. Hazelett lines include in-line hot rolling directly coupled to the caster, with at least two hot-rolling stands [W15-05].
- **Block casters.** Chain-mounted, water-cooled steel blocks form the sides of the mould [W15-01].
- **Wheel / narrow-strip casters (Properzi- and Rigamonti-derived).** TALAT says these narrow strip casters are mostly used for the production of small discs ("slugs") for impact extrusion of aerosol containers, cans and tubes [W15-01]. Properzi rod is usually delivered at 12 mm diameter and drawn to wire [W15-01].
- **Integrated slug lines.** For mass production of collapsible tubes and cans, slug blanking or extrusion equipment can be placed directly after the caster, so that production is continuous [W15-01].
- A patented aerosol-can route [W15-03] runs as follows:
  1. The alloy is cast continuously on a wheel.
  2. The strip is hot rolled and wound on a winder.
  3. The coil is unwound and cold rolled.
  4. The strip is cut into slugs.
  5. The slugs are annealed.
- **Twin-belt slug route (patents).** The slab is cast and then hot-milled in line to slug-strip gauge; it is not homogenised as a separate step [W15-04]. *(inference from the snippet; check the claims text)*

### 1.2 Quantitative data

| Process | As-cast gauge | Width | Casting speed | Cooling rate | In-line rolling / exit T | Alloy-range notes | Slug relevance | Ref |
|---|---|---|---|---|---|---|---|---|
| TRC, industrial | final product 3–8 mm | – | 0.8–2 m/min | – | hot reduction in roll gap | – | not cited for slugs | [W15-09] |
| TRC, older commercial sheet casters | normally ≥ ~6 mm | – | normally ≤ ~1.5 m/min | – | – | traditional process: "low productivity, restricted to a limited range of alloys" | – | [W15-10] cluster; [W15-08] |
| TRC (vertical), review | – | – | – | 100–1000 °C/s | – | – | – | [W15-08] |
| TRC, through-thickness (one study) | – | – | – | ~4500 °C/s near surface vs ~100 °C/s at mid-thickness | – | casting speed and roll gap are the main variables for cooling rate | – | [W15-10] cluster |
| TRC, research high-speed casters | down to 1.25 mm | – | 15 m/min (good quality); 6016 at 60 m/min; "A5182" up to 150 m/min; Al-20Si at 20 m/min | – | – | wide-freezing-range alloys reportedly castable on research casters | – | [W15-10] cluster |
| Twin-belt (Hazelett), secondary source | 15–25 mm | ≤ 2000 mm | 5–9 m/min | not given | ≥ 2 hot stands; exit strip temperatures 420 °C and 460 °C (text truncated) | – | – | [W15-05] |
| Twin-belt slug patents | cast slab ~1.10–1.38 in = **27.9–35.1 mm (derived)** → hot-milled to ~0.236–0.709 in = **6.0–18.0 mm (derived)** | – | not given | – | caster exit > ~520 °C; maximum temperature of any part of the slab < ~582 °C | "recycled aluminum scrap" in the title | yes: impact-extrusion slugs | [W15-04] |
| Twin-belt, modelling | – | – | – | local cooling rates computed → DAS predicted for 3105 and 5182 (no numbers in snippet) | – | casting speed matters more for cooling rate and cell size as the mushy interval widens | – | [W15-06; W15-07] |
| Block: Alusuisse Caster II (Lauener twin-block) | 10–40 mm | ≤ 1750 mm | 0.5–10 m/min | – | – | Mg limit: "AlMg at max. 2 to 3 % Mg, with the exception of Alusuisse Caster II at max. 5 % Mg". Another passage gives a general block-caster maximum of 3.5 % Mg. ⚠ It is ambiguous which caster class the 2–3 % applies to | – | [W15-01] |
| Block caster (machine not identified) | ~16 mm | – | 2–4 m/min | – | – | – | – | [W15-01] |
| Narrow wheel strip (Properzi/Rigamonti-derived) | strip up to 500 × 20 mm cross-section | ≤ 500 mm | – | – | hot rolled before coiling [W15-03] | – | **mostly slugs** for aerosol containers, cans, tubes | [W15-01; W15-03] |
| Properzi (company) | – | – | – | – | continuous casting + direct rolling; first Al rod line 1949; ~300 Al and alloy lines sold | – | – | [W15-02] |
| Single-belt (AA6111) | 2.49 → 0.55 mm | – | – | – | – | thinner strip cut grain size by ~56 % and SDAS by ~56.7 % | – | [W15-39] |

**Cross-check against the Drive chapters (ch. 07 §2.3, ch. 02 §4.2):**
- **TRC speed.** ch. 07 gives 2–3 m/min [RA]; the web gives 0.8–2 m/min industrial [W15-09] and ≤ ~1.5 m/min for older casters [W15-10]. The R4 speed printed as "0.95–1.50 cm/min" (ch. 02 §4.2, ch. 07 G11) **falls inside the web m/min ranges**. This supports reading it as m/min (inference; it does not verify R4 itself).
- **Hazelett gauge.** 12–25 mm [RA] and 12–75 mm [POL] in ch. 07, vs 15–25 mm [W15-05]. The slug patents cast ~28–35 mm (derived) [W15-04], above both secondary ranges. Flagged; not resolved.
- **Block-caster speed.** ~6 m/min [RA] in ch. 07 vs 0.5–10 m/min for Caster II [W15-01]. These are consistent.

### 1.3 Design levers
1. **Choose the caster by gauge.** A starting strip of about 20 mm lies above the industrial TRC product range (3–8 mm [W15-09]). It lies inside the ranges given for twin-belt [W15-05], block [W15-01] and narrow wheel strip [W15-01]. The narrow wheel-strip route is the one TALAT associates with slugs [W15-01] (inference on the match).
2. **Plan the in-line hot reduction.** The patented belt route takes ~28–35 mm cast slab down to ~6–18 mm (derived) [W15-04]. The hot reduction on CC lines is limited, so how much of the cast structure is broken up depends on the in-line mill (inference).
3. **TRC only.** Specific roll-separating force and casting speed are the primary knobs for surface bleeds and centreline segregation (§2) [W15-13; W15-14].

### 1.4 Pitfalls
- The Hazelett speed and gauge figures come from one secondary article [W15-05]. The patent figures are claim ranges, not plant data [W15-04].
- The 100–1000 °C/s review range is for **vertical** TRC [W15-08]. It may not transfer to horizontal industrial casters.
- No source found maps freezing range systematically against attainable speed and gauge (search-result statement for [W15-10]).

### 1.5 Relevance to in-house work
- ch. 09 §5 describes a "starting strip → HRM → CRM → full anneal → cold extrusion" route. Its structure matches the continuous-cast-plus-in-line-hot-mill slug routes in [W15-01; W15-03; W15-04] (inference). Whether the user's starting strip is CC, and on which caster, decides which of §§2–3 below applies.
- The ch. 09 §5 *Assessment* assumes a fully recrystallised hot band. On CC lines with limited in-line hot reduction (above), that assumption needs checking first (inference).

---

## 2. As-cast microstructure

### 2.1 Mechanisms
- **Supersaturation.** High solidification and post-solidification cooling rates in TRC leave **Mn supersaturated throughout the strip**, with **very fine constituent particles near the surface** [W15-11]. The cooling rate falls steeply from surface to mid-thickness (~4500 vs ~100 °C/s in one study) [W15-10 cluster], which explains the gradient (inference).
- **Centreline segregation, TRC.**
  - When the solidification fronts meet at the centre, the enriched residual melt solidifies there [W15-15, via citing papers].
  - The centreline segregates contain low-melting-point material and generally have an equiaxed microstructure [W15-16, describing W15-15].
  - Centreline segregation **increases with solute content, and hence with freezing range** [W15-15, via a citing paper]. It is the main internal defect for wide-freezing-range alloys (6xxx, Mg alloys) [W15-14].
- **Segregation form in A3003.**
  - With increasing casting speed, the centre segregation changes from **channel segregation** to a **segregation band**.
  - The location of the kiss point is the main factor: segregation decreases as the kiss point rises [W15-13].
  - Fe is much higher in the kiss-point zone than elsewhere (follow-on summary of [W15-13]).
- **Mechanical squeeze.** The roll force that welds the two shells squeezes solute-rich liquid between the dendrites. This was shown in Mg-alloy TRC [W15-18], and centreline and inverse segregation are classed together as damaging micro-defects [W15-17]. Forced cooling "obviously suppresses" centreline segregation in TRC AA6022 [W15-19].
- **Surface bleeds.** A small cavity forms between the roll and the already-solidified shell and is filled by enriched residual melt. Low specific roll-separating force promotes bleeds; higher force or lower casting speed suppresses them [W15-14].
- **Corrosion.** The centre-plane macrosegregation zone of TRC AA3003 is more corrosion-prone [W15-20].
- **Twin-belt.** TBC cools more slowly than TRC, over a longer sump [W15-27]. ch. 07 §2.3 [POL] gives the Drive values for a 19 mm belt slab (surface vs centre). Belt-cast strip should therefore be less supersaturated than TRC but more than DC (inference; not measured in the sources found).

### 2.2 Quantitative data

| Item | Value | Alloy / caster | Ref |
|---|---|---|---|
| Cooling rate, near surface vs mid-thickness | ~4500 vs ~100 °C/s | TRC (one study) | [W15-10] cluster |
| Cooling-rate range | 100–1000 °C/s | vertical TRC | [W15-08] |
| Mn supersaturation | "high … throughout the strip" (no number in abstract) | TRC AA3105 | [W15-11] |
| Constituent size gradient | very fine near surface; homogenisation reduces it but does not remove it | TRC AA3105 | [W15-11] |
| Grain gradient after homogenisation | much coarser grains and more particles at the surface than at the centre | TRC Al-Mn | [W15-21] |
| Bleeds and centre segregates appear | when casting gauge < 2.5 mm **and** specific load < 0.6 t/mm | TRC Al-Mg-Mn (study quoted in the review) | [W15-14] |
| Centre-segregation suppression by speed | centreline segregation partly or fully disappears at 1.5 m/min | TRC WZ73 (Mg alloy) | [W15-14] |
| Segregation type vs speed | channel segregation → segregation band as speed rises | TRC A3003 | [W15-13] |
| TRC vs DC chemistry used in a comparison | TRC strip had notably higher Fe and lower Si than the DC comparator | Al-Mn-Fe-Si | [W15-22] |

**Not obtained (searched for, but no number in any snippet):**
- dendrite-cell or grain size of CC 3xxx/1xxx;
- intermetallic type (Al₆(Mn,Fe) vs α-Al(Mn,Fe)Si) and size in as-cast TRC/TBC strip;
- measured Mn/Fe/Si in solution;
- centreline enrichment factors;
- as-cast texture.

The only Drive value is DAS of 5–10 µm (TRC) vs 30–70 µm (DC) (ch. 07 §2.3 [POL]).

### 2.3 Design levers
- **Raise the kiss point** (casting speed and setback) to reduce centreline segregation [W15-13].
- Use **higher specific separating force or lower speed** against bleeds [W15-14].
- Use **forced cooling** against centreline segregation (shown for 6xxx) [W15-19].
- **Narrow-freezing-range alloys** (1xxx, lean 3xxx) segregate less at the centreline than solute-rich alloys [W15-15; W15-14]. This is a structural advantage of the user's alloy family on CC routes (inference).

### 2.4 Pitfalls
- **The surface layer and the mid-thickness are different materials.** Particle size [W15-11], post-homogenisation grain size [W15-21; W15-23] and Fe level (kiss-point zone [W15-13]) all differ through the thickness. A slug blanked from such strip carries the gradient into the extrusion (inference).
- A Fe-enriched centreline in a high-Fe (recycled) melt may cross the threshold for primary-intermetallic formation locally, even when the bulk composition is safe (inference from [W15-13] + ch. 02 §4.3).
- Twin-belt data (cooling, segregation) for 3xxx were not found online. Do not transfer TRC magnitudes to a ~20 mm belt strip.

### 2.5 Relevance to in-house work
- ch. 09 §5 sets CRM strain targets per alloy with a single grain-size band per strain. On CC stock, expect **surface-to-centre** differences in nucleation density (particle size) and in solute. Specify grain size at both surface and mid-thickness when validating (inference; see the grain-size band notes in ch. 09 §5.2).
- The user's ch. 09 §8 slug specifications should be checked for whether they constrain centreline quality (inclusions, segregation) for CC stock (open; see §6).

---

## 3. Downstream metallurgy: homogenisation, precipitation during annealing, recrystallisation, texture

### 3.1 Mechanisms
- **Concurrent precipitation is the central CC effect.** In TRC AA3105 that is rolled and annealed without homogenisation, dispersoids precipitate during the anneal and inhibit the formation of recrystallisation nuclei. The result is **sluggish recrystallisation and a very coarse grain structure** [W15-11].
- Across CC 3xxx, precipitation during annealing gives "strong resistance to recrystallisation", producing **coarse, elongated (pancake) grains** with strong **P {011}⟨455⟩/⟨566⟩**, **M** and/or **ND-rotated cube {001}⟨310⟩** textures [W15-28; W15-29; W15-30; W15-31; W15-32].
- **If recrystallisation finishes before precipitation**, the grain is fine with a weak cube texture [W15-28; W15-29]. This is a TTT competition between the dispersoid-precipitation and recrystallisation curves, so the heating rate decides the outcome [W15-12].
- **Homogenisation reverses the DC logic.**
  - For TRC 3105, homogenised strip recrystallises at a **lower** temperature than non-homogenised strip, with finer, quasi-equiaxed grains by **PSN** [W15-26].
  - For DC hot-rolled 3105, homogenisation **slowed** recrystallisation [W15-26].
  - In TRC strip, high-T homogenisation removes the supersaturation and coarsens the constituents and dispersoids (weaker Zener drag, more PSN sites) [W15-11; W15-37; W15-25].
- **Low-temperature homogenisation of supersaturated strip is the worst case.** It produces dense fine dispersoids, partly strain-induced. After it, a *more* heavily reduced strip softened *more slowly*: a kinetic reversal, because pinning outweighed the extra stored energy [W15-25].
- **Si matters, not just Mn.** In four TRC Al-Mn(-Fe-Si) alloys, Si changed the temperature and kinetics of the phase transformations. Low-Si alloys decomposed the solid solution and transformed the primary phases over a wider temperature range. Mn and Si precipitation during recrystallisation slowed it most in alloys rich in both [W15-34]. α-Al(Mn,Fe)Si forms during annealing of Al-Mn-Fe-Si alloys [W15-38].
- **Pre-recovery (two-step anneal).** A recovery step forms **precipitate-free zones around constituent particles**. There, randomly oriented subgrains can reach critical size, which restores PSN, weakens the texture and reduces planar anisotropy [W15-35]. Pre-recovery speeds the early stage of recrystallisation but slows the later stage [W15-36].
- **Route effect on work hardening and annealing.** TRC and TBC 3105 differ in work-hardening rate and annealing curve because of their different solidification [W15-27].

### 3.2 Quantitative data

**(a) Homogenisation of CC strip**

| Alloy / form | Treatment | Result | Ref |
|---|---|---|---|
| TRC AA3105 | 600 °C, 5–120 h | supersaturation reduced, constituents coarsened; surface-to-centre particle-size gradient reduced, not removed | [W15-11] |
| TRC AA3105 | cyclic homogenisation up to 620 °C | further coarsening; **uniform fine grain structure through the thickness** | [W15-11] |
| TRC thin Al-Mn strip | homogenised vs not, then annealed | unhomogenised strip **stayed strong after 3 h at 375 °C**; homogenised strips **fully softened below 350 °C**; homogenisation also gave coarse surface grains; **homogenising at cast gauge** is preferred (cold rolling first improved neither grain structure nor softening) | [W15-23] |
| TRC EN AW-3105, 6 and 9 mm strip, cold rolled to 0.7 mm (≈ 88 % and 92 % reduction, ε ≈ 2.15 and 2.55, **derived**) | homogenised at 713 K (**440 °C, derived**) or 853 K (**580 °C, derived**); isothermal anneal 563–583 K (**290–310 °C, derived**) | apparent Q after 580 °C homogenisation: **≈ 233 kJ/mol (6 mm), ≈ 222 kJ/mol (9 mm)**; after 440 °C: **≈ 362 and ≈ 389 kJ/mol**; after 440 °C the 9 mm (more reduced) strip softened **more slowly** (strain-induced precipitation) | [W15-25] |
| TRC AA3003 | homogenisation at increasing T | lower Mn supersaturation; more and larger intermetallic particles; grain shape changes from pancake to equiaxed above 520 °C (snippet does not say whether 520 °C is the homogenisation or the anneal temperature) | [W15-24] |
| TRC Al-Mn(-Fe-Si), 4 alloys | homogenisation at 450 and 610 °C, followed by conductivity and hardness | Si-dependent transformation kinetics (no numbers in abstract) | [W15-34] |
| TRC 3xxx | higher homogenisation T; higher cold reduction | both give finer recrystallised grain | [W15-37] |

**(b) Heating rate and annealing practice**

| Alloy / state | Heating / anneal | Result | Ref |
|---|---|---|---|
| CC AA3105 hot band | **slow:** air furnace, 11 °C/min (≈ 0.18 °C/s, **derived**), 6 h at 482–599 °C | **coarse elongated** recrystallised grains at every temperature; relatively strong P and 22.5° ND-rotated cube | [W15-28] |
| CC AA3105 hot band | **fast:** salt bath ≈ 50 °C/s, 30 min | finer, more equiaxed grains as T rises; **fine equiaxed at 599 °C**; weak cube; higher UTS **and** elongation than the slow anneal | [W15-28] |
| TRC AA3105, cold rolled | 0.01, 0.5, 3 and 50 °C/s (air furnace, infrared, lead bath) | faster heating → finer, more equiaxed grains. At **50 °C/s, grain growth followed recrystallisation at 500 °C**; at 3, 0.5 and 0.01 °C/s there was no growth (more dispersoids precipitated) | [W15-12] |
| TRC 3003, cold rolled | **two-step:** 450 °C / 5 h pre-recovery + 530 °C / 15 h | fine quasi-equiaxed grains; very weak ND-rotated cube; **Δr = 0.03** vs **0.31** for single-step 530 °C / 15 h | [W15-35] |
| CC AA3015 | "dual" treatment 872 K → 644 K (**599 → 371 °C, derived**) vs single 872 K | dual: faster recrystallisation, coarser grains, stronger cube (attributed to precipitate size) | [W15-30] |
| CC AA3015, cold rolled, no pre-treatment | annealing at increasing T | low T: coarse elongated grains + strong P; higher T: smaller, equiaxed grains, weaker P. JMAK n **2.0 → 0.5** and Q **225 → 539 kJ/mol** as concurrent precipitation (Zener drag) takes over (snippet; the controlling variable for these ranges is not stated) | [W15-29] |

**(c) JMAK kinetics: CC vs DC**

| Alloy | Anneal T range | Avrami n | Apparent Q | Ref |
|---|---|---|---|---|
| CC AA3003, cold rolled | 371 → 427 °C | **~2.9 → ~0.8** (falls with T) | "significantly higher" than DC (no number in abstract) | [W15-32] |
| DC AA3003, cold rolled | same | **~1.5** (stable) | lower | [W15-32] |
| CC AA3003 (2020 paper, same group) | same range | **4.3 → 0.8** | – | [W15-33] |
| CC AA3015 | (see above) | 2.0 → 0.5 | 225 → 539 kJ/mol | [W15-29] |
| TRC EN AW-3105 | 290–310 °C after homogenisation | – | 222–233 (580 °C homog.) / 362–389 kJ/mol (440 °C homog.) | [W15-25] |

### 3.3 Earing and texture
- CC 3xxx annealed at low T or with slow heating develops strong P, M and ND-rotated-cube components [W15-28; W15-29; W15-31; W15-32]. Fast heating to a high T gives a weak cube [W15-28].
- The pre-recovery route cut Δr from 0.31 to 0.03 [W15-35]. That is the only quantitative anisotropy number found.
- No CC-specific earing percentages were found (Engler's TRC 3xxx earing work was not located in the search results).
- For backward impact extrusion of slugs, anisotropy shows up as uneven wall height or rim (inference; no source found).

### 3.4 Design levers
1. **Homogenise at cast gauge, at high temperature.** Use this if a fine, equiaxed, isotropic slug grain is needed from CC 3xxx. High-T homogenisation (580–620 °C class [W15-11; W15-25]) removes the supersaturation, so the final anneal recrystallises by PSN without concurrent precipitation [W15-23; W15-26]. Cost: energy and furnace time, which removes part of the CC route's advantage (inference; cf. ch. 07 §2.3 [RA]).
2. **Avoid "half" homogenisation.** A ~440 °C treatment of supersaturated strip produced the slowest, most strain-insensitive kinetics [W15-25] (inference: a dispersoid-nucleation treatment).
3. **Without homogenisation, heat fast and soak high.** Fine equiaxed grain needs heating that outruns the precipitation nose: ~50 °C/s to ~600 °C in [W15-28]. Batch slug annealing cannot do this (inference), so expect coarse elongated grains at batch-furnace rates [W15-28; W15-12].
4. **Watch post-recrystallisation grain growth after very fast heating.** Fewer dispersoids are left to pin the boundaries [W15-12].
5. **Raise the cold reduction.** Higher CR refines the recrystallised grain in TRC 3xxx [W15-37] and reduces the surface-to-centre grain-size gap [W15-21]. But in strip that is supersaturated or low-T-homogenised, more strain can *slow* softening (strain-induced precipitation) [W15-25].
6. **Use a two-step anneal for isotropy.** Recovery below the precipitation-driven recrystallisation range, then recrystallise [W15-35]. Published times (5 h + 15 h) are far longer than slug practice; the mechanism, not the cycle, is the transferable part (inference).

### 3.5 Pitfalls
- **The Avrami n is not constant for CC material.** It drops strongly with temperature (2.9 → 0.8; 4.3 → 0.8), while DC stays near 1.5 [W15-32; W15-33]. A single-n JMAK model calibrated on DC or homogenised material will mispredict CC strip (inference).
- **The apparent Q depends on the precipitation state:** 222 to 539 kJ/mol across [W15-25; W15-29]. Q is not a material constant here.
- **Homogenisation helps in opposite directions on the two routes:** it accelerates TRC recrystallisation but slowed DC hot-band recrystallisation [W15-26]. Do not copy DC homogenisation practice onto CC strip.
- Homogenisation can **coarsen surface grains** [W15-23; W15-21]. That is a surface-finish risk for slugs (inference).

### 3.6 Relevance to in-house work
- **ch. 09 §5 heating-rate warnings** ("avoid slow heating, Mn precipitation before recrystallisation, coarse elongated grains"). These are the documented behaviour of CC 3105/3015/3003 [W15-12; W15-28; W15-29; W15-32]. This answers ch. 07 gap G5 for CC material. The magnitude for low-Mn alloys such as 3102 was **not** found online.
- **ch. 09 §§2–4 JMAK models** (n, Q and the precipitation term). If the slug stock is CC and not homogenised, the CC literature shows n falling with temperature and Q from ~220 to ~540 kJ/mol depending on the precipitation state [W15-25; W15-29; W15-32]. Re-fit the in-house parameters on CC material rather than reusing DC-derived values (inference).
- **ch. 09 §5 CRM strain targets.** Higher CR refines the grain [W15-37], but the kinetic-reversal result [W15-25] means raising CR is not guaranteed to lower the anneal temperature on supersaturated CC strip. Check it with an isothermal series on the actual strip.
- **ch. 09 §3 (anneal cycles, MgO).** Soak windows near the precipitation range of supersaturated strip are where concurrent precipitation is strongest [W15-25; W15-29] (inference on overlap; not quantified for the user's alloys).

---

## 4. Alloy design for CC routes

### 4.1 Mechanisms and findings
- **Mn + Si.** In TRC Al-Mn-Fe-Si, Si (not just Mn) sets the temperature and kinetics of solid-solution decomposition. Alloys rich in both Mn and Si showed the strongest retardation of recrystallisation by concurrent precipitation [W15-34]. The abstract does not say whether higher Si shifts precipitation earlier or later; ch. 02 §2.5 covers the Drive view of Al-Mn-Si dispersoid chemistry.
- **Freezing range.** Centreline segregation grows with solute content and freezing range [W15-15, via a citing paper] and dominates in wide-freezing-range alloys [W15-14]. Lean 3xxx and 1xxx have narrow freezing ranges and are the "easy" end for TRC and other CC routes (inference).
- **Mg limits on block casters** are 3.5 % generally and 5 % on Caster II [W15-01] (ambiguous quote, §1.2). This is irrelevant to the user's lean alloys except as a castability bound.
- **Fe tolerance and recycled content.**
  - Faster solidification raises the Fe+Mn level at which primaries form (Drive: ch. 02 §4.3 [R1]).
  - A 2023 preprint title claims "improved iron-tolerance in recycled aluminum alloys via direct strip casting" (title only; see the list in §0).
  - The patents for CC slug stock are explicitly framed around **recycled aluminum scrap** [W15-04] (title level; alloy windows not obtained).
  - Counterpoint: Fe concentrates in the kiss-point zone of TRC A3003 [W15-13], so the local centreline Fe is higher than the ladle analysis (inference on the consequence).
- **Comparator chemistries.** A published TRC-vs-DC Al-Mn-Fe-Si comparison used **higher Fe and lower Si** for the TRC strip [W15-22]. That is a hint, not a rule, that CC producers shift Fe up and Si down.
- **Grain refiner.** No web data was obtained on TiB₂ use for CC 3xxx/1xxx. The Drive source (ch. 02 §4.2, R4) gives Al-Ti-B wire feeding on an industrial TRC.
- **Slugs, discs, circles.**
  - CC narrow strip is the TALAT-documented feedstock for slugs [W15-01], and patented aerosol routes use wheel-cast [W15-03] or belt-cast [W15-04] strip.
  - **No open quantitative study of CC slug or circle metallurgy was found.** The Brazilian ABM paper on drawability of continuously cast AA3003 was located by title only.

### 4.2 Quantitative data

| Item | Value | Ref |
|---|---|---|
| Alloys studied for the Si effect | 4 TRC Al-Mn alloys with varied Mn, Si, Fe (contents not in abstract) | [W15-34] |
| TRC vs DC comparator | TRC: notably higher Fe, lower Si (numbers not in snippet) | [W15-22] |
| Block-caster Mg ceiling | 3.5 % (general); 5 % (Caster II) | [W15-01] |
| CC slug patent hot-mill window | cast ~27.9–35.1 mm → ~6.0–18.0 mm (derived); exit > ~520 °C; max < ~582 °C | [W15-04] |

### 4.3 Design levers
1. **Keep Mn lean on unhomogenised CC routes.** Less supersaturated Mn means less concurrent precipitation during the slug anneal [W15-11; W15-34] (inference on magnitude). This favours 3102-type over 3003-type chemistry for CC slugs if homogenisation is skipped.
2. **Treat Si as a kinetic knob, not a trace element.** Si changes the precipitation temperature and kinetics [W15-34]. Specify it in a narrow band on CC stock (inference).
3. **Fe up for recycled content.** CC tolerates more Fe in the bulk (ch. 02 §4.3; preprint title), but check **centreline** primaries [W15-13] (inference).
4. **Homogenisation decision.** If chemistry cannot be leaned, use the cast-gauge high-T homogenisation of §3.4 [W15-23; W15-25].

### 4.4 Pitfalls
- No web source gave quantitative Mn/Fe/Si windows for CC 3xxx/1xxx slug or circle stock. The "levers" above are mechanistic inferences anchored to [W15-34; W15-13; W15-11].
- No data was found for **1xxx** CC strip annealing (Fe supersaturation, Fe precipitation during anneal). The key lead, Birol 2009, J. Alloys Compd. 488, was found by title only.

### 4.5 Relevance to in-house work
- ch. 09 §5 assigns 1070/1050 "no Mn precipitation risk" and calls 3102 "less sensitive to heating rate". On a CC route, Fe (and Si) supersaturation in 1xxx and the low Mn in 3102 should still be checked by conductivity or resistivity before and after the anneal. TRC studies use resistometry and conductivity tracking for exactly this purpose [W15-34] (inference on the application).
- The modified-3102 and 3207 compositions (ch. 09 §§1, 4, 10) should be screened for Mn+Si level against the "Mn- and Si-rich → slowest recrystallisation" finding [W15-34] if the strip is CC (inference).

---

## 5. DC vs CC comparison table

| Attribute | DC ingot → hot mill | CC strip (TRC / belt / block / wheel) | Ref |
|---|---|---|---|
| As-cast thickness | 400–760 mm (ch. 07 §2.3) | TRC 3–8 mm industrial; belt 15–25 mm (secondary; patents ~28–35 mm derived); block 10–40 mm; wheel strip ≤ 20 mm × 500 mm | [W15-09; W15-05; W15-04; W15-01] |
| Cooling rate | 1–5 °C/s (ch. 07 §2.3) | TRC 10²–10³ °C/s, with a surface ≫ centre gradient (~4500 vs ~100 °C/s in one study); belt slower than TRC | [W15-08; W15-10; W15-27] |
| Mn in solution after casting | lower; reduced further by homogenisation | high and supersaturated throughout the TRC strip | [W15-11] |
| Through-thickness gradient | scalped surface; centre macrosegregation (ch. 02 §5) | fine constituents at the surface vs coarser at the centre; kiss-point centreline segregation (Fe-rich); bleeds | [W15-11; W15-13; W15-14] |
| Homogenisation | standard (ch. 07 §2.1) | often skipped. If done at high T, it **accelerates** recrystallisation (TRC 3105) | [W15-26; W15-23] |
| Effect of homogenisation on recrystallisation | slowed it (DC hot-rolled 3105) | sped it up; finer grains via PSN (TRC 3105) | [W15-26] |
| Concurrent precipitation in the final anneal | limited (Mn already precipitated) | strong unless homogenised or heated fast | [W15-11; W15-28; W15-32] |
| JMAK n (3003, 371–427 °C) | ~1.5, stable | ~2.9 → ~0.8 (or 4.3 → 0.8), falls with T | [W15-32; W15-33] |
| Apparent Q for recrystallisation | lower | significantly higher; 222–539 kJ/mol depending on precipitation state | [W15-32; W15-25; W15-29] |
| Grain after slow-heated anneal | – | coarse, elongated (pancake) | [W15-28; W15-11] |
| Texture after a low-T or slow anneal | – | strong P, M, ND-rotated cube; weak cube after fast high-T anneal | [W15-28; W15-29; W15-32] |
| Heating-rate sensitivity | – | critical: 50 °C/s → fine equiaxed; ≤ 3 °C/s → coarse | [W15-12; W15-28] |
| Planar anisotropy | – | Δr 0.31 (single-step) → 0.03 (pre-recovery two-step), TRC 3003 | [W15-35] |
| Work hardening and annealing curve | – | route-dependent even between TRC and TBC | [W15-27] |
| Fe tolerance | baseline | higher bulk tolerance (ch. 02 §4.3; preprint title) but a Fe-rich centreline | [W15-13] |
| Slug use | conventional (sheet → blanks) | TALAT: narrow wheel-cast strip is mostly used for slugs; patent aerosol routes | [W15-01; W15-03; W15-04] |

---

## 6. Open questions / not verified

1. **No full text was read.** Every number here comes from search-result abstracts or snippets (see the access note at the top). Priority PDFs to obtain:
   - [W15-11] Sun 2006, for supersaturation levels and particle sizes;
   - [W15-12] Sun 2008, for the TTT diagram and grain sizes per heating rate;
   - [W15-23] Birol 2009 (471);
   - Birol 2009 (488, foil stock);
   - [W15-25] Işıksaçan 2026, for full kinetics;
   - [W15-27] Spathis 2016, for the TRC vs TBC annealing curves and the reduction–grain-size data;
   - [W15-32] Wang 2018;
   - [W15-35], for Δr and the cycle;
   - [W15-14] Ullmann 2024, Table 1, for the defect classification;
   - TALAT 3210 [W15-01] in full, for caster specifications;
   - the slug patents [W15-04], for alloy windows and anneal practice.
2. **Cluster attribution [W15-10].** The numbers for commercial TRC (≤ ~1.5 m/min, ≥ ~6 mm), research casters (15 m/min, 1.25 mm; 60 m/min 6016; 150 m/min 5182; 20 m/min Al-20Si) and the 4500/100 °C/s gradient came from one merged search answer. Each needs tying to its own paper (likely candidates: Haga's high-speed TRC papers; Yun, Lockyer, Hunt, MSEA 2000; "Effect of casting conditions and composition on microstructural gradients in roll cast aluminium alloys"). **Unverified.**
3. **Not found at all:**
   - as-cast grain or cell size, intermetallic type (Al₆(Mn,Fe) vs α) and size, and dissolved Mn/Fe/Si levels for CC 3xxx/1xxx;
   - centreline enrichment factors;
   - as-cast texture;
   - twin-belt-specific 3xxx microstructure data;
   - grain-refiner practice on belt or wheel casters.
4. **Ambiguous snippet statements:**
   - whether "> 520 °C" in [W15-24] is the homogenisation or the anneal temperature;
   - what variable drives the n 2.0 → 0.5 and Q 225 → 539 kJ/mol change in [W15-29];
   - which caster class the "AlMg max 2–3 %" limit refers to in [W15-01];
   - whether [W15-23]'s "coarse surface grains" refers to grains after homogenisation or after the final anneal.
5. **Two unattributed statements were seen in search answers and are deliberately not used above.** They need a source before use:
   - (a) "centre segregation cannot be eliminated by homogenisation and subsequent rolling";
   - (b) homogenised-before-CR TRC strip starts recrystallising near 225 °C vs ~300 °C without homogenisation, while strip homogenised only at cast gauge "recrystallises through growth".
6. **Conflicts with Drive chapters** (flagged, not resolved):
   - Hazelett gauge: 12–25 / 12–75 mm (ch. 07 [RA]/[POL]) vs 15–25 mm [W15-05] vs ~28–35 mm cast slab in the slug patents [W15-04].
   - TRC speed: 2–3 m/min (ch. 07 [RA]) vs 0.8–2 m/min [W15-09].
7. **Low-Mn alloys (3102-type, ≤ ~0.4 Mn) and 1xxx on CC routes.** No published concurrent-precipitation data was found. The ch. 09 §5 statement that 3102 is "less sensitive to heating rate" is plausible by the mechanism but **unverified** for CC stock.
8. **Slug, disc and cookware-circle specifics** (earing %, grain-size specifications, homogenise-or-not practice at slug producers) were not found in open sources. Only the TALAT statement and the patent routes were located.
9. **Engler's TRC 3xxx texture and earing work and Li & Arnberg's CC/DC dispersoid studies** were named in the brief but not surfaced by the searches that ran before the budget was exhausted. Search these next.
10. **Kinetic reversal [W15-25].** Does strain-induced precipitation also occur at the CR levels and soak temperatures used for slugs? Measure it: isothermal series on the user's actual strip, with conductivity plus EBSD at the surface and at mid-thickness.
