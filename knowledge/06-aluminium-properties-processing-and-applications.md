# 06 — Aluminium: physical properties, physical metallurgy, processing and applications (general references)

**Scope.** This file distils the *general* aluminium references in the Drive library into design-relevant physical metallurgy: composition → processing → microstructure → properties. The main target is wrought alloys, especially 3xxx heat-exchanger and foil alloys (AA3102/AA3207 class), but it also covers the 1xxx, 5xxx, 6xxx, 7xxx and 8xxx families. Specialised literature on brazing sheet and 3xxx alloys is handled in other knowledge files. This file supplies the baseline data and mechanisms.

**Conventions.** Every claim carries a citation `[Ref p./§]`. **Derived** marks arithmetic I did on source numbers, such as unit conversions or slopes. **Inference** marks a design conclusion I drew from cited facts. **(general knowledge)** marks content that is not in the sources; I kept it to a minimum. Several source texts lost `%`, minus signs and units during PDF extraction. Values affected by this are flagged ⚠.

**Update 2026-10-12 (Polmear full text).** Polmear's *Light Alloys* (S-028, cited here as **[POL p.x]**, the key used in ch07) was read in full from the user's two-part split copy (Section 1) and added to this chapter. New material: conductor-alloy data and a Zr conductivity coefficient (Section 2), canstock phase and texture practice (Sections 3, 5, 6), paint-bake behaviour (Section 7), continuous casting, castability, hot tearing and recycling (Section 8), oxide/MgO statements (Section 11) and the packaging and electrical rows of Section 12.2. Where POL and HB disagree, both are given and flagged (Section 14, item 5). ch05 §4.10 and §4.12 hold the fuller canstock, foil, conductor and cast-alloy summaries.

---

## 1. Sources

| Ref | Identified document (Drive file name) | Drive link | Lang. | Readability / coverage achieved |
|---|---|---|---|---|
| **HB** | G.E. Totten & D.S. MacKenzie (eds.), *Handbook of Aluminum Vol. 1: Physical Metallurgy and Processes*, Marcel Dekker 2003, ISBN 0-8247-0494-0 (catalogue key **S-029**; "Alminium.pdf"). "ASM Handbook of Aluminium vol. 1.pdf" (1LNDwz9XSVn51tWynCZUvGvbdzEDR23K3) is the **same file**: same size (17,664,014 B) and same front matter. The Drive folder "Cloud part book" holds the same book split into four PDFs (IDs 1Yxag4tV…, 1EwIKZG8…, 10ilZD0R…, 1KmVD2fb…), which together cover printed pp. 1–1296 without gaps. | https://drive.google.com/file/d/1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz/view | EN | **Full text read 2026-10-12** from the four split PDFs, after the broken font maps were repaired and the text re-extracted. Earlier passes used the Drive text reader, which stopped at ≈ p.174 and dropped `%`, minus signs and some ligatures; values flagged ⚠ from that pass were rechecked, and changes are marked "corrected after full-text pass". **Read in full:** Ch.1 Introduction (Sverdlin, pp.1–31; production, low metallurgical content), **Ch.2 Properties of pure Al (Sverdlin, pp.33–79)**, **Ch.3 Physical metallurgy and alloying effects (Tiryakioğlu & Staley, pp.81–210)**, Ch.5 §3 transition-metal precipitation and commercial Al–Mn alloys (Katgerman & Eskin, pp.293–299), **Ch.19 Heat treating processes and equipment (Howard, Bogh & MacKenzie, pp.881–970)**. **Spot reads:** Ch.6 p.334 and Ch.18 *Sheet Forming of Aluminum Alloys* pp.851–853 (earing, r-values). **Not used here:** Ch.4 (recrystallisation), the rest of Ch.5, Ch.7 (rolling), Ch.8 (extrusion), Ch.20 (quenching) and later chapters; these belong to other knowledge files. Citations give **printed** page numbers (printed page = PDF page − 12 in part 1, PDF page + 787 in part 3). |
| **DW** | J. Dwight, *Aluminium Design and Construction*, E&FN Spon 1999 ("116748406-Aluminium-Alloys.pdf") | https://drive.google.com/file/d/158y2YRjC0dWVgkEgUCsb0DZ8LAqp2BbY/view | EN | Clean text. **Ch.1–3 in full plus Ch.4 up to §4.1.7** (≈ book p.1–70 of ~370). Tables 1.1, 3.1, 3.2, 4.1–4.3 are images and were not extracted. Ch.4.2–12 (properties, durability ratings, HAZ, design) not reached. |
| **EAA** | European Aluminium Association, *Aluminium in Commercial Vehicles* (≈2007–2011; cites EN 1999, EAA 2005) ("uporaba v transportu.pdf", SL file name but **English** content) | https://drive.google.com/file/d/1nKCtal3NFz7WMlwE4ijgHl0UwMeCMHJp/view | EN | **Read in full, 2026-10-12.** Downloaded whole (3,278,124 B = Drive size; 162 pp.; PDF page = printed page) and converted with `pdftotext -layout`, which gives clean two-column text. Earlier passes reached p.80. New: Ch. VI end (fatigue examples, ADR tanks, tipper wear), VII fabrication, VIII welding, IX other joining, X finishing, **XI corrosion (pp.145–151)**, XII cleaning, XIII repair. Ch. XI is short and qualitative: no corrosion rates or potentials. |
| **RY** | Ø. Ryen, *Work Hardening and Mechanical Anisotropy of Aluminium Sheets and Profiles*, Dr.Ing. thesis, NTNU, Nov. 2003 ("uporabno del-2.pdf", SL name, **English** content) | https://drive.google.com/file/d/1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_/view | EN | Good. **Read to p.70 of ~190**: background (Ch.2), materials, homogenisation, processing (Ch.3), as-received state and texture (Ch.4.1–4.2). Mechanical results for AA1050/3103/5xxx, the discussion, and all of **Part B (6063/6082/7030/7108 extrusions)** were not reached; only the abstract was read. |
| **VA** | T. Vasevska (Impol, Slovenska Bistrica), "Utrjevanje aluminija in zlitin pri vzdolžnem hladnem valjanju / Hardening of aluminium and alloys by longitudinal cold rolling", *Materiali in tehnologije* 38(3–4) 191–196 (2004) ("vasevska.pdf") | https://drive.google.com/file/d/1wpVR73nujVXO1OfmvV57CzuvwR__bdRc/view | **SL** (EN abstract) | Read in full and translated. Property-versus-reduction figures cannot be read numerically from the text. |
| **TAL** | TALAT Lecture 1101, *Resources and Production of Aluminium*, G. Budd, EAA 1999 ("lastnosti aluminija.pdf", SL name, **English** content) | https://drive.google.com/file/d/18RcaS3-hFM9Wts56lekVpEoUht44bmE7/view | EN | Read in full (25 p). Introductory; low physical-metallurgy content. |
| **WP** | *Aluminium – An overview*, Wikipedia articles compiled by PediaPress, 5 Dec 2011, 122 p ("74849304-Aluminium.pdf") | https://drive.google.com/file/d/11M-jMkYSxdMMb5J0sGZaGQCIZgiuWz04/view | EN | Complete. Tertiary source with low authority. Used for the property infobox, composition limits, foil, wire, porosity and inclusions. |
| **HAB** | F. Habashi (ed.), *Alloys: Preparation, Properties, Applications*, Wiley-VCH 1998, ISBN 3-527-29591-7 ("41279889-Alloys.pdf", 20.6 MB) | https://drive.google.com/file/d/1TCvbTC2LxRkOZQfHu3V-5lOPsIctbTTJ/view | EN | **Truncated at ≈ p.72 (copper chapter). The aluminium chapter (Ch.10, p.165–212) was not reached.** Only the general introduction is usable. |
| — | The 26 MB "41279889-Alloys.pdf" is a **different document**: *Characterization of Minerals, Metals, and Materials 2018* (TMS series, B. Li et al. eds.) | https://drive.google.com/file/d/1sP4G1PGlES_nFoGSix8aA8MAdCer6gde/view | EN | Read to ≈ PDF p.188, mostly slags, ceramics and composites. The only aluminium-alloy paper ("Ultra-high-speed FSW of AA6111-T4", p.249) lies beyond the truncation point. **No data used.** |
| **SIL** | W.H. Sillekens, *Backward Can Extrusion and Materials Behaviour*, PhD TU Eindhoven 1992, DOI 10.6100/IR374925 ("374925.pdf"). This is **not** the same document as "uporaba v transportu". | https://drive.google.com/file/d/1FgOlZBrGWWfSCsEn9pe44eb10MEYShxy/view | EN (NL summary) | Read to ≈ p.66 of ~105 (Ch.1–4). Ch.5 (ductile failure in backward can extrusion) not reached. Material studied is rapidly solidified recycled shredder scrap. |
| **MM** | J.F. Butler Jr. (Alcoa), "Alcoa Micromill™ – Breakthrough Technology for Next Generation Auto Sheet", presentation, 3 Sep 2015 ("document.pdf") | https://drive.google.com/file/d/1OYezPC_Eif_mKOTmq2xeExuqfcsTai1N/view | EN | All 14 slides read. Marketing claims; table column mapping partly ambiguous. |
| **PC** | A.B. Phillion & J. Dantzig, "Pre-Course Reading for ESI's Solidification Course" ("Pre-course-reading.pdf") | https://drive.google.com/file/d/1PWxfw0Wekow6uLkk0TBx-OOxw8oaY001/view | EN | Text cut off after ≈ 5 pages. Generic solidification nomenclature only. |

**Coverage caveat.** The Drive text reader returns at most ≈ 110–390 k characters per file. In every large book, the processing chapters most relevant to rolling, extrusion, heat treatment, welding and corrosion fell beyond that limit (Section 14).

**Whole-file route (tested 2026-10-12).** Files can be downloaded whole (base64) and converted locally. This works up to at least 3.81 MB. A 7.19 MB file broke the connector transport ("message from the server was too large"), and the server refuses anything over 10 MB. HB is now available as four split PDFs and was read in full for the chapters listed above (2026-10-12). HAB (20.6 MB) and the other large books still need splitting into ≤ ~3.8 MB PDFs. Details are in ch07 §0.

---

## 2. Physical properties of aluminium and the effect of purity and solutes

### Mechanisms
- Electrical and thermal conduction are electronic. Impurities and solutes in solid solution, vacancies and dislocations scatter electrons, so purity mainly affects resistivity and thermal conductivity and barely affects the other physical properties [HB p.36].
- The ranking of impurities from most to least damaging to conductivity is **Cr > V > Mn > Ti > Mg > Ag > Cu > Zn > Si > Fe > Ni** (Fridlyander) [HB p.52]. Elements with very low solubility (Fe, Ni: 0.025 and 0.023 at.%) sit mostly in constituent particles and therefore cost little conductivity. Transition metals retained in supersaturated solution (Cr, V, Mn, Ti) cost the most [HB p.52, p.92]. *(The link to solubility is an inference.)*
- Vacancies and interstitials add 3.4 µΩ·cm per at.% to resistivity [HB p.39]. Grain size affects resistivity only slightly, but strain hardening raises the conductivity along the deformation direction by 0.5–1.0 % [HB p.51] (the `%` is confirmed in the full text; ⚠ removed after the full-text pass). Table 12 of the same source shows the opposite trend for commercial-purity cold-worked versus annealed material (see the pitfall below).
- Alloying lowers the thermal conductivity of Al by up to ~50 % for some alloys, and resistivity can double [DW §1.2]. Cu, Mg and Mn lower thermal conductivity; for example 2 % Mn reduces it from 209 to 126 W/m·K [HB p.45] (the 209 W/m·K base is the 99.49 % Al value quoted on p.44; ⚠ removed after the full-text pass).
- **Thermal from electrical conductivity.** HB states that the best thermal-conductivity values are obtained by calculation from room-temperature electrical conductivity. It gives four empirical relations of the form K = a·λ·T×10⁻⁹ + c, e.g. **K = 4.65·λ·T×10⁻⁹ + 0.05** (a = 4.65/5.02/5.3, c = 0.05/0.03/0.025; a fourth form uses 4.9 and +1.2·T×10⁻⁴) [HB p.42–43]. Units are not printed. **Derived check:** with λ in Ω⁻¹·cm⁻¹ (pure Al ≈ 3.8×10⁵, i.e. 1/2.65 µΩ·cm), T in K (293) and K in cal·cm⁻¹·s⁻¹·°C⁻¹, the first relation gives ≈ 0.56, which matches HB's Table 11 (0.57–0.62 at 25 °C). So the relations are a Wiedemann–Franz-type route from a measured conductivity to thermal conductivity (1 cal·cm⁻¹·s⁻¹·°C⁻¹ = 418.4 W/m·K).
- Electron versus lattice conduction: k = k_phonon + k_electron, and in metals the electronic part dominates. From 120 to 700 K the thermal conductivity of Al changes by less than 50 %, while the electrical conductivity changes by 1300 % over the same range [HB p.44].

### Quantitative data

**Table 2.1 – Pure Al, reference values**

| Property | Value | Source |
|---|---|---|
| Density, 20 °C | 2.70 g/cm³ (99.99–99.999 %); 2.71 (99.5–99.0 %); theoretical 2.69872; measured 2.6984 | [HB p.37, p.40] |
| Density, wrought alloys | 2.67–2.80 g/cm³; 2.7 used in design | [DW §1.2] |
| Density effect of Mg | −0.5 % per wt.% Mg in solid solution | [HB p.160] |
| Liquid density at m.p. | 2.375 g/cm³ (WP); 2.3 g/cm³ (molten cathode Al) | [WP p.1; HB p.29] (*page corrected after the full-text pass; was p.28*) |
| Boiling point | 2480 °C (99.999 %) | [HB p.37] |
| Melting point | 660.32 °C [WP p.1]; 660.37 °C [HB p.57]; 660.2 (99.999) → 657.0 °C (99.0) [HB p.37]; 657 (99.2 %), 658 (99.5 %) [HB p.59] | — |
| dT_m/dp | 6.41×10⁻² °C/MPa | [HB p.59] |
| Volume change on melting | 5.4 % | [HB p.59] |
| Latent heat | 94.6 cal/g (99.999) / 93.0 (99.0) [HB p.37]; 397 J/g [HB p.59]; 10.71 kJ/mol [WP p.1] | — |
| Specific heat | 0.2226 cal/g·K at 100 °C (99.999), 0.2297 (99.0) [HB p.37]; 24.20 J/mol·K at 25 °C [WP p.1] (≈ 0.90 J/g·K, derived) | — |
| Young's modulus | 69 GPa pure (DW); wrought alloys 69–72, design value 70 GPa [DW §1.2]; extreme purity 69–72, commercial 70–72.5, thin clad sheet 68.5–70 [HB p.66]; Varley table 9.9×10⁶ psi (99.999 %) and 10.0×10⁶ psi (99.0 %) [HB p.37] (≈ 68.3 / 68.9 GPa, derived) | — |
| E versus T | 67 GPa at 100 °C; 59 GPa at 200 °C | [DW §1.2] |
| Shear modulus / Poisson | G 25–26.5 (extreme purity), 27–28 GPa (commercial); ν 0.31–0.33 [HB p.66]; G_Al = 23 GPa in Ch.3's stacking-fault calculation [HB p.85]; design ν = 0.33 [DW §1.2]; WP gives G 26, K 76 GPa, ν 0.35 [WP p.1] | — |
| Critical resolved shear stress | 0.79 MPa (pure Al single crystal); theoretical shear strength 0.9–2.62 GPa | [HB p.82, p.89] |
| CTE | 23.1 µm/m·K at 25 °C [WP]; pure 23.5×10⁻⁶ K⁻¹, alloys 22–24.5, design 23, 26×10⁻⁶ at 200 °C [DW §1.2] | — |
| Mean CTE, 99.99x Al | 20–100 °C: 23.4–23.9; 20–200: 24.3–24.6; 20–300: 25.3–25.5; 20–400: 26.5 ×10⁻⁶ K⁻¹ | [HB p.42] |
| Thermal conductivity | 237 W/m·K at 300 K [WP]; ~240 W/m·K, ~4× steel [DW §1.2]; 0.57→0.54 cal/(cm·s·K) at 100 °C from 99.999→99.0 % (≈ 238→226 W/m·K, derived) [HB p.37]; commercial 99.49 / 99.70 % Al: 209 / 222 W/m·K "at 200°" (unit not printed, presumably °C) [HB p.44] (*corrected after the full-text pass: the temperature is readable*). Calculated pure-Al averages (Table 11): 0.59 / 0.56 / 0.54 / 0.53 / 0.52 cal/(cm·s·°C) at 25 / 100 / 200 / 400 / 600 °C [HB p.46] (≈ 247 / 234 / 226 / 222 / 218 W/m·K, derived). ⚠ HB also prints 343 W/m·K for 99.9 % electrolytic Al at 190 °C [HB p.45]; this is far above every other pure-Al value here and should not be used | — |
| Resistivity, 20 °C | 2.63 (99.999) / 2.68 (99.990) / 2.74 (99.80) / 2.80 (99.50) / 2.87 µΩ·cm (99.0) | [HB p.37] |
| Conductivity, high purity | 99.997 %: 65.45 % IACS (2.6434 µΩ·cm); 99.996 %: 64.94 % IACS (2.6548); 99.993 %: 65.1 % IACS | [HB p.50] |
| Temperature coefficient of resistivity | 0.0042 (99.99x) → 0.0040 K⁻¹ (99.0); dρ/dT = 0.0115 µΩ·cm/K, 0–300 °C (Matthiessen) | [HB p.37, p.50] |
| Resistivity jump on melting | 99.99 %: solid 10.8, liquid 26.6 ×10⁻⁸ Ω·m; commercial purity: liquid 27.1×10⁻⁸ Ω·m (~+164 %) [HB p.52]; ρ_liquid/ρ_solid = 1.9 at the melting point [HB p.59 Table 15]. ⚠ The same page prints ρ_s = 1.65×10⁻⁸ Ω·m for commercial-purity solid Al, which does not fit the 10.8 value or the +164 % | — |
| Lattice / atomic | fcc, a = 4.04963 Å at 25 °C (99.99 %, Figgins) [HB p.39]; HB p.38 also prints "4.0414 Å at room temperature", which disagrees with the measured value on the next page. Nearest neighbour 2.863 Å; atomic radius 1.43 Å; b = 0.286 nm | [HB p.38–39, p.83; WP p.3] |
| Stacking-fault energy | **135 erg/cm² (= mJ/m²) [HB p.40] versus 200 mJ/m² [HB p.85]**: the two chapters of HB disagree (⚠). Partial-dislocation separation in Al is only 1–2 atom diameters, so cross-slip is frequent [HB p.85]. Alloying lowers the SFE [HB p.85] | *corrected after the full-text pass: this table previously gave ≈ 200 only* |
| Vacancies | E_f 0.76 eV, E_m 0.65 eV, E_SD 1.4 eV; di-vacancy binding 0.17 eV; equilibrium concentration near m.p. 9.4×10⁻⁴ [HB p.39–40]. Quenching from 900 K to 300 K with E_f ≈ 0.7 eV gives a "chemical stress" of about 3 GPa, relieved by vacancy loss to sinks and by vacancy-loop formation; Li and Si bind vacancies strongly and retard loop formation [HB p.86–87]. Quenched Al single crystals have a CRSS about 5× that of annealed ones [HB p.39] | — |
| Reflectance / emissivity | bright dip R 90 % / ε 3 %; clear anodic R 80 % / ε 35–65 %; black anodic R 5 % / ε 95 %; sand-blasted 15–25 % of polished reflectance; rough finish ε 20–30 % | [HB p.55–56] |
| Superconducting T_c | 1.187 K | [HB p.51] |

### Design levers
- **Conductivity (fin and foil heat transfer, EC conductors).** Keep Cr, V, Mn and Ti out of solid solution. For EC aluminium, Cr+V+Mn+Ti ≤ 0.015 % (preferably 0.01 %) with Si 0.12–0.16 % [HB p.52]. Boron treatment removes V and Ti as (Ti,V)B₂ to raise conductivity [WP p.73]. *Inference for 3xxx:* the Mn that remains in solution after homogenisation (Section 4) is the main conductivity lever.
- **Fe.** At Si ≈ 0.15–0.16 %, raising Fe from 0.16 to 0.57 % raises resistivity only from 0.02767 to 0.02788 Ω·mm²/m in the annealed state, about 0.05 µΩ·cm per wt.% Fe (derived). Fe is therefore a cheap way to add constituents for grain-size control and strength (Section 4) at very little conductivity cost [HB p.53].
- At very low Si (≤ 0.006 %), the Fe/Si ratio (0.8–3.8) has only a slight effect on resistivity. At Si 0.15–0.16 % its effect becomes strong [HB p.52].
- **Stiffness.** E is fixed by the base metal; all Al alloys have about the same E [EAA p.34, p.59]. Si, Cu and Li in solution raise E by **8.5, 4.4 and 1.5 % per at.%** in solution [HB p.95] (*units corrected after the full-text pass; they were lost in the first extraction*). The mechanism given is that solutes anchor mobile dislocations, removing their contribution to elastic strain [HB p.95].
- **O-temper conductivity as a process check.** Typical conductivity ranges of annealed products (unit not printed; the values are consistent with % IACS, general knowledge) [HB p.928 Table 25]:

  | Alloy-O | Typical conductivity | Rockwell H, max |
  |---|---|---|
  | 1100 | 57.0–62 | 50 |
  | 3003 | 44.5–50.5 | 65 |
  | 5052 | 34–37 | 95 (HRE 70 max) |
  | 6061 | 42.0–49 | 75 (HB 40 max) |
  | 6063 | 57.0–65.0 | 70 |

  *Inference:* the ≈ 12-point gap between 1100-O and 3003-O is the conductivity cost of 3003's Mn and Si (solid solution plus dispersoids). A lean slug alloy should read between these two bands. Where its reading falls, at a given composition, tracks how much Mn, Fe, Si and Mg the anneal left in solution.
- **Natural ageing lowers conductivity.** After solution treatment and quenching, electrical conductivity *falls* during natural ageing. HB attributes this to GP-zone formation and vacancy consumption, not to true precipitation [HB p.910]. *Relevance (inference):* for Mg + Si-bearing slug alloys such as T11, a conductivity drift between the in-line quench and cold rolling or annealing would signal Mg–Si clustering. It should not be read as a change in Mn in solution.

### Pitfalls
- **Cold-worked versus annealed conductivity.** HB Table 12 shows cold-worked commercial Al with *higher* resistivity than annealed: 0.02812 vs 0.02767 Ω·mm²/m, i.e. 35.56 vs 36.14 MS/m [HB p.53]. This conflicts with the claimed +0.5–1 % gain in the deformation direction [HB p.51]. Always specify temper when quoting conductivity.
- **Unreliable values.** PC gives pure Al solidifying at "661 °C" [PC p.1]. Do not use it; the accepted value is 660.3 °C [WP p.1]. DW's specific heat ("22 cal/g°C") and resistivity units ("2.7 W cm") are typographic errors [DW §1.2]. HB prints the melting of 99.996 % Al as "933.4 °C" [HB p.58]; 933.4 is the value in kelvin.
- **Still no per-element coefficients (checked in the full HB text).** HB Ch.2, Ch.3 and Ch.19 give the Fridlyander ranking, the Fe/Si table, the vacancy increment and the O-temper conductivity ranges above. None of them gives per-wt.% resistivity or thermal-conductivity increments for solutes in solution. The gap in Section 14 stays open.

**Relevance (slug route, inference).** Conductivity is the cheapest in-line check of how much Mn, Fe, Si and Mg the caster, the in-line quench and the slug anneal leave in solution. Without per-element coefficients, calibrate it against the user's own alloys (ch09) rather than against literature.

---

## 3. Solubility, phase equilibria and the phases that form

### Mechanisms
Particles fall into four classes [HB p.120–125]:
- **Primary particles:** primary Si; Al₇Cr, Al₃Ti or Al₃Zr from peritectics; primary Fe phases in hypereutectic 8xxx.
- **Constituents (1–30 µm):** form by eutectic reaction. Fe/Si-bearing constituents are insoluble; Al₂Cu, Al₂CuMg and Mg₂Si are soluble.
- **Dispersoids (< 1 µm; 5–200 nm in RY):** Mn, Cr and Zr precipitate during ingot preheat and are practically impossible to redissolve.
- **Precipitates:** form on ageing.

Sources: [HB p.120–125; RY p.28].

### Quantitative data

**Table 3.1 – Maximum solid solubility in Al (at.%)** [HB p.92, Table 1]

| Ag | Co | Cr | Cu | Fe | Ge | Li | Mg | Mn | Ni | Si | Zn |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 23.8 | 0.01 | 0.40 | 2.48 | 0.025 | 2.30 | 13.9 | 16.26 | 0.90 | 0.023 | 1.59 | 66.4 |

**Table 3.2 – Key invariants and solubilities (wt.%)**

| System | Data | Source |
|---|---|---|
| Al–Fe | Max solubility of Fe ≈ 0.05 %. Eutectic forms α + Al₃Fe (monoclinic); metastable Al₆Fe/AlₘFe form in commercial 1xxx and with Mn or faster solidification. | [HB p.117, p.138] |
| Al–Fe phase selection | Preheat 16 h at 607 °C gives Al₃Fe; 16 h at 482 °C gives Al₆Fe. With Si: α-Al₁₂Fe₃Si or β-Al₉Fe₂Si₂. Solidification front < 0.5 mm/s favours Al₃Fe (alloys with 4.6–6.1 % Fe); Si and 0.75 % Mg stabilise Al₃Fe; Ce/La suppress it. | [HB p.138–139] |
| Al–Mn | Eutectic Al–Al₆Mn at ≈ 1.9 % Mn and 657 °C. Max solubility 1.82 % Mn. Commercial Mn kept < 1.25 % because Fe lowers Mn solubility and promotes coarse primary Al₆(Mn,Fe). | [HB p.159–160] |
| Al–Mn as-cast | 3003 ingot retains 0.7–0.9 % Mn in solution [HB p.160]. AA3103 (1.0 % Mn, 0.57 % Fe, 0.12 % Si) retains 0.81 % Mn (0.40 at.%) [RY p.54]. | — |
| Al–Mn dispersoids | Homogenisation precipitates Al₁₂(Mn,Fe)₃Si (α) or Al₆(Mn,Fe). Si < 0.07 % gives Al₆(Mn,Fe). Si accelerates Mn precipitation (denser α, less Mn left in solution) and converts Al₆(Mn,Fe) to α. A higher Fe/Mn ratio can give Al₁₃(Fe,Mn)₄ in the as-cast state. | [HB p.160] |
| Al–Mg | Eutectic with Mg₅Al₈ (β) at 35 % Mg. Solubility 14.9 % at 450 °C, about 1.7 % at RT, but decomposition is very slow, so all Mg stays in solution in commercial alloys. | [HB p.160–161] |
| Al–Cr | Peritectic at 661 °C, 0.41–0.77 % Cr; primary Al₇Cr is retained under commercial solidification. | [HB p.116] |
| Al–Cu | Eutectic at 548 °C, 33.2 % Cu, with Al₂Cu. | [HB p.115–116] |
| Al–Mg₂Si | Pseudo-binary eutectic at 595 °C; max solubility 1.85 % Mg₂Si; balanced Mg:Si = 1.73 (wt). With excess Si, %Mg₂Si = 1.578 × %Mg. Si available for Mg₂Si = %Si − ¼(%Fe + %Mn). | [HB p.169–171] |
| Al–Mg–Si with Fe, Mn | Mn forms insoluble "Al₁₀Mn₂Si" (as printed) particles that take Si out of the matrix and lower the ageing response [HB p.177]. Mn and Cr (and Sr) favour Chinese-script α-Al(Fe,Mn)Si (α-Al₈Fe₂Si, α-Al₁₅(Mn,Fe)₃Si₂) over plate-like β-Al₅FeSi, which causes large misfit strain [HB p.179]. Fe gives mild strengthening up to 0.8–0.9 % in Al–Mg–Si alloys [HB p.179] | — |
| Transition-metal (TM) supersaturation versus cooling rate | Solid-solution content after solidification (Table 33, "%", wt. presumably): at 10⁻¹ K/s Mn 1.82, Cr 0.82, Zr 0.28; at 10¹ K/s Mn 2.5; at 10² K/s Mn 2.8, Zr 0.15–0.17; at 10³ K/s Mn 3.0–5.0, Cr 1.5–3.5, Zr 0.5–0.7. Ingot and casting practice runs at 10–100 K/s, which saturates Al with TM up to the equilibrium limit (eutectic systems) or the liquid concentration (peritectic systems). Peritectic formers need a threshold of about 10² K/s; supersaturation in eutectic systems (Mn, Fe, Sc, Ni) rises continuously with cooling rate | [HB p.294–295] |
| Al–TM decomposition | Al–TM supersaturated solutions are far more stable than those of Cu, Mg, Zn, Si or Li and decompose between 250 and 650 °C. Al–Mn (Al₆Mn) 300–350 °C; Al–Sc 250–350; Al–Zr 400–450; Al–Cr 450–500; Al–V 500–550 °C (Table 34). Commercial Al–Mn supersaturated by ingot casting (< 10² K/s) decomposes above 325 °C to Al₆Mn, (AlFeMn) and (AlFeMnSi) dispersoids, with "no real precipitation hardening" | [HB p.293, p.295, p.299] |
| TM diffusion and segregation | D(TM) ≈ 10⁻¹⁴–10⁻¹² cm²/s at 500 °C (printed "cm³/sec"). Dendritic segregation of TM "cannot be easily eliminated by homogenization". Eutectic-type TM diffuse about an order of magnitude faster than peritectic-type TM | [HB p.295] |
| Al–Si | Eutectic temperature is lowered 10 °C by 0.1 % Mg. Mg reduces Si solubility, so Mg₂Si is insoluble in 7075 but soluble in 6013. | [HB p.122, p.172] |
| H in Al | Solubility falls about 10× on solidification [HB p.119]. Minus signs confirmed in the full text (the ⚠ from the first pass is removed): liquid log S = 2.796 − 2760/T; solid log S = 0.788 − 2080/T (Ransley–Neufeld); liquid 2.620 − 2550/T (Opie–Grant); liquid 2.969 − 3086/T, solid 1.961 − 3042/T (Eichenauer). S in cm³/100 g, T in K. | [HB p.73–75] |

**Table 3.3 – Observed constituents and dispersoids** [HB p.123 Table 6, p.125 Table 7]

| Alloy | Constituents | Dispersoids |
|---|---|---|
| 1350 | Al₁₂Fe₃Si, Al₆Fe | — |
| 3xxx (3003) | Al₆(Fe,Mn), Al₁₂(Fe,Mn)₃Si | Al₁₂(Mn,Fe)₃Si, Al₆(Mn,Fe) |
| 5083 | Mg₂Si, Al₁₂(Fe,Mn)₃Si, Al₇Cr | Al₁₁Cr₂ (as printed in HB Table 7), Al₆(Fe,Mn) |
| 6061 / 6013 | Mg₂Si, Al₁₂(Fe,Mn)₃Si / Al₁₂(Fe,Mn)₃Si | 6013: Al₁₂Mn₃Si |
| 2x24 | Al₇Cu₂Fe, Al₁₂(Fe,Mn)₃Si, Al₂CuMg, Al₂Cu, Al₆(Fe,Cu) | Al₂₀Cu₂Mn₃ |
| 7x75 / 7x50, 7055 | Al₇Cu₂Fe, Al₁₂(Fe,Mn)₃Si, Mg₂Si, … | Al₁₂Mg₂Cr / Al₃Zr |

### Design levers
- **Constituents are permanent.** Insoluble constituents cannot be removed by preheat. Their size falls with faster solidification, lower Fe and Si, and more deformation [HB p.122]. Low-Fe/Si alloys (7475, 2124) are used where toughness matters [HB p.122].
- **3004-H19 can body.** Its success depends on controlling the size, volume fraction and distribution of Al₁₂(Fe,Mn)₃Si constituents [HB p.123].
- **Choice of dispersoid former.** Coherent Al₃Zr is more effective against boundary migration than incoherent Al₁₂Mg₂Cr or Al₂₀Mn₃Cu₂. Particles < 0.4 µm retard recrystallisation, and small, closely spaced particles are most effective [HB p.125].
- **Mn/Fe budget in 3xxx.** Mn + Fe must stay below the level that nucleates primary Al₆(Mn,Fe); hence the industrial Mn < 1.25 % [HB p.159–160].
- **Al₃Zr** has only ~0.6 % misfit with Al and stays roughly spherical below 0.18 wt.% Zr; it can be coherent or semi-coherent depending on process history [HB p.125]. Excess Si strongly promotes Al₃Zr formation in Al–Mg–Si alloys [HB p.179].
- **Relevance: Mg₂Si bookkeeping for T11 (derived from the HB rules above).** T11 (Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26): Si available for Mg₂Si = 0.38 − ¼(0.52 + 0.14) ≈ 0.22 %. Mg 0.26 needs only 0.26/1.73 ≈ 0.15 % Si, so Mg is limiting. That gives Mg₂Si ≈ 1.578 × 0.26 ≈ 0.41 % and ≈ 0.07 % excess Si. T11 is therefore a lean, slightly Si-excess Al–Mg–Si alloy in which about 40 % of the Si (0.165 of 0.38) is assigned to Fe and Mn constituents. The ¼ factor is an empirical rule for DC-cast alloys; on a fast rotary caster more Fe stays in solution (row above), so the real constituent fraction is uncertain (inference).
- **Relevance: rotary-cast strip.** The supersaturation table shows the direction: the faster the casting, the more Mn (and, by the same eutectic-type logic, Fe) stays in solution. Without ingot homogenisation, that Mn and Fe can precipitate during later heating, from 300–350 °C for Al₆Mn [HB p.295] (inference for the route; the cooling rate of the user's caster is not known here).

### Pitfalls
- Peritectic formers (Cr, Ti, Zr) give coarse primary particles if the composition is not tightly controlled [HB p.121].
- In 5xxx alloys Si is consumed as Mg₂Si, which is nearly insoluble at high Mg and harms ductility and formability, so Si is kept low [HB p.167–168].

---

## 4. Strengthening mechanisms: quantitative coefficients

### Mechanisms
- **Solid solution.** The yield-stress increment follows τ = τ₀ + k·c^(2/3) for single crystals [RY p.25]. For Mg, the increment scales as c^(2/3) below 1 at.% and c^(1/3) above [HB p.162]. Effects are roughly additive in dilute alloys. Size misfit dominates; valence difference matters for Zn and Ag [HB p.90].
  - To strengthen by solid solution in a non-heat-treatable alloy, the element must be appreciably soluble at the annealing temperature, must stay in solution after a slow cool from the anneal, and must not react with other elements to form insoluble particles [HB p.91–92].
  - **Ternary synergy.** In Al–Mg–Si, Al–Cu–Mg and Al–Zn–Mg, both the solution strengthening and the work hardening are *greater* than the sum of the individual solutes [HB p.95, p.101]. *Relevance (inference):* for Mg + Si alloys such as T11, a linear sum of binary Mg and Si coefficients will underestimate strength and press force.
- **Indirect solute effect (dominant for work hardening).** Solutes slow dynamic recovery, so dislocation storage rises [RY p.26; HB p.98]. Adding solute has the same effect on substructure as lowering the deformation temperature [HB p.98]. Mg suppresses cell formation and produces a Taylor lattice [RY p.14].
- **Dislocation strengthening.** Δσ_y = M·α·G·b·√ρ, with α 0.2–0.3 and M ≈ 3 (Taylor factor) [HB p.89, p.96] (*corrected after the full-text pass: the earlier entry omitted M*). Dislocation density inside subgrains saturates at about 10¹⁴ m⁻² for ε = 0.03–2 in AA1050 and AA3207 (0.4 % Mn), higher in 3207 [RY p.16].
- **Strain hardening of quenched metal.** In quenched Al foil, all quenched-in dislocation loops are gone after 5 % cold reduction; with more cold work the jogged tangles turn into well-defined subgrains [HB p.97].
- **Grain and subgrain size.** Hall–Petch σ_y = σ_f + k·d^(−1/2), with σ_f = 10 MPa for pure Al [HB p.101]. Substructure strengthening scales as d^(−m) with m between ½ (hot-work subgrains) and 1 (cold-work cells) [HB p.101–102].
- **Constituents.** In Al–0.05Si–Fe (0.15–1.17 % Fe), annealed yield strength rises about 7 MPa per vol.% constituent [HB p.122, p.138].
- **Precipitates.** Shearable precipitates give localised slip; non-shearable ones give Orowan looping and higher work hardening. Maximum hardening occurs at a particle spacing of about 10 nm [HB p.104–108]. Combine precipitate contributions with exponent q = 1.5 (better fit than q = 2) [HB p.113].

### Quantitative data

**Table 4.1 – Solute strengthening and work-hardening coefficients**

| Quantity | Value | Source |
|---|---|---|
| Mn in solution, O temper | +21 MPa YS, +42 MPa UTS per wt.% Mn in solution (binary Al–Mn sheet in which the Mn was kept in solution by a high-temperature anneal and rapid quench, HB Fig. 62) | [HB p.160] |
| Mn in solution, H19 | +35 MPa YS per wt.%. Mn gives "modest" solid-solution strengthening but is more effective at promoting work hardening during cold rolling; it is still less effective than Mg, which is why many 3xxx alloys add Mg and/or small Cu | [HB p.159–160] |
| Mg, H19 | +70–85 MPa YS per wt.% | [HB p.160, p.164] |
| Mg, O temper | Up to 6 % Mg gives annealed YS up to 175 MPa | [HB p.94] |
| Mn in solution in 3xxx after preheat and hot work | only 0.2–0.3 wt.% (0.1–0.15 at.%) | [HB p.94] |
| Cu limit in non-heat-treatable alloys | about 0.3 wt.%, to avoid Al–Cu–Fe constituents, grain-boundary precipitates or ageing | [HB p.94] |
| Most effective strengthener | Per atom: Mn and Cu (≤ 0.5 at.%). Per weight: Mg. Least efficient: Zn. | [HB p.94–95] |
| Cu-equivalent K (tensile work hardening of 1 at.% solute) | Cu 1.00, Ge 0.64, Mg 0.37, Cd 0.33, Ag 0.15, Zn 0.071 | [HB p.99 Table 2] |
| Doherty work-hardening parameter H (GPa) | **Cu 3.38 ± 0.20, Si 1.56 ± 0.05, Mg 1.52 ± 0.14, Mn 1.03 ± 0.17, Zn 0.27**. H = (k_alloy − k_Al)/(at. fraction solute)^(2/3) (exponent read from the equation layout), where k is the YS after a true rolling strain of 1 (63 % cold reduction) in YS = k·εⁿ | [HB p.99–100] (*corrected after the full-text pass: the "unassigned third column" is the ± uncertainty of each value*) |
| Hall–Petch k | Pure Al 0.065–0.07 MPa·m^½ [RY p.33; HB p.101]; many alloys 0.1–0.2 [HB p.101]; AlNi6 0.14 [RY p.33]; Mg-free alloys ≤ 0.15; 5754: k = 0.22, σ₀ = 42.5 MPa; 5182: k = 0.30, σ₀ = 57.6 MPa | [HB p.167] |
| Hall–Petch friction stress, Al–Mg | **σ_f = 15.5 × (wt.% Mg)** (HB Eq. 24). Derived check: 3 % Mg gives 46.5 MPa (5754 printed: 42.5); 4.5 % Mg gives 70 MPa (5182 printed: 57.6). So it is an approximation only | [HB p.167] (*corrected after the full-text pass: the "+ 24" read earlier is the equation number*) |
| Total strength | σ = σ_f + ΣΔσ_i, with σ_f = 10 MPa for pure Al; several precipitate contributions combine as (ΣΔσ_i^q)^(1/q), q ≈ 1.5 | [HB p.113] |
| Maximum ageing increments (Table 36) | ΔYS_max: Al–1Mg–0.6Si–0.25Cu 140 MPa (79 MPa per at.% total solute); Al–4Cu–1.5Mg 260; Al–4.5Zn–1.8Mg 230; Al–5Zn–2.3Mg–1.7Cu 290; Al–0.5Sc 120 MPa (1000 MPa per at.%) | [HB p.298] |
| Hollomon σ = Kεⁿ, O temper (n / K in MPa) | 1100: 0.242/146 · **3003: 0.242/188** · 6061: 0.209/224 · 5052: 0.198/281 · 5454: 0.189/340 · 5086: 0.193/368 · 5456: 0.178/479 | [HB p.100 Table 3] |
| Initial work-hardening rate, pure Al | about G/20 | [HB p.97] |
| Stage IV | θ_IV ≈ 0.1·τ_IV | [RY p.31] |
| Taylor factor | M = 3.06 (random fcc polycrystal) | [RY p.50] |
| Strength range | 45 MPa (1199-O) to about 700 MPa (7055-T77 extrusion) | [HB p.81] |

**Table 4.2 – Typical properties of commercially pure Al** [HB p.71 Table 20; psi → MPa derived]

| Alloy-temper | UTS | YS | El % | HB | Fatigue (rotating beam) |
|---|---|---|---|---|---|
| 1199-O / H18 | 45 / 117 | 10 / 110 | 50 / 5 | — | — |
| 1060-O / H14 / H18 | 69 / 97 / 131 | 28 / 90 / 124 | 43 / 12 / 6 | 19 / 26 / 35 | 21 / 34 / 45 |
| EC-O / H19 | 83 / 186 | 28 / 165 | 23 / 2.5 (in 10 in.) | — | — |
| 1145-O / H18 | 76 / 145 | 34 / 117 | 40 / 5 | — | — |
| 1100-O / H14 / H18 | 90 / 124 / 165 | 34 / 117 / 152 | 35 / 9 / 5 | 23 / 32 / 44 | 34 / 48 / 62 |
| 1180-O / H18 | 62 / 124 | 21 / 117 | 45 / 5 | — | — |
| EC-H14 | 110 | 97 | — | — | — |

*Added after the full-text pass:* the 1180 and EC-H14 rows, and shear strengths from the same table: 1060-O/H14/H18 48/62/76; EC-O/H14/H19 55/69/103; 1145-O/H18 55/83; 1100-O/H14/H18 62/76/90 MPa [HB p.71] (psi → MPa derived). Hardness is HB 500 kg/10 mm/30 s; fatigue limit is R.R. Moore rotating beam, printed as "based on 5000 million cycles" [HB p.71].

Further reference values:
- Commercially pure Al sheet fatigue at 2×10⁷ cycles: annealed (UTS 80 MPa) σ₋₁ = 35 MPa; strain-hardened (UTS 150 MPa) σ₋₁ = 50 MPa [HB p.72].
- Pure Al: yield strength 7–11 MPa; alloys 200–600 MPa [WP p.3]. UTS 90–140 MPa depending on temper [DW §1.1.4].
- Non-heat-treatable alloys: UTS is roughly linear in total wt.% of alloying additions, whatever the element, for both O and H18/H38 tempers. 5xxx is dominated by solid solution, 1xxx/8xxx by particles, and 3xxx by both [RY p.7, after Aluminium Standards & Data 1986; the equation is in an image and was not extracted].
- AA3004: strength = solute component (grows with strain) + second-phase component (roughly constant after early strain) [RY p.29, Suni 1994].

### Design levers (3xxx and foil focus)
- **Strength versus conductivity in 3xxx.** Mn in solution gives the most strength per wt.% of any route in the O temper and moderate strength in H19. It also costs the most conductivity (Section 2). Mg costs less conductivity per unit of strength in H tempers *(inference from the coefficients and ranking above)* but brings other drawbacks (Sections 9 and 11).
- **Raising H-temper strength without Mn in solution.** Use Si (1xxx/8xxx: Si in solution impedes dynamic recovery and raises strength [HB p.140]), Cu (most efficient work-hardening promoter, but ≤ 0.3 % in non-heat-treatable alloys [HB p.94, p.98]) or Mg [HB p.160].
- **Constituent strengthening.** About 7 MPa per vol.% from Fe-rich constituents, at a low conductivity penalty [HB p.138; Section 2].
- **Grain size matters more in 5xxx** (k > 0.2) than in heat-treatable alloys, where grain size gives little strengthening [HB p.101, p.167].
- **Avoid ultrafine grains (< 1 µm).** They lose work-hardening capacity and ductility [HB p.102].
- **Relevance: ageing headroom of T11 (inference).** For a 6061-type alloy, full solution treatment and peak ageing add ≈ 79 MPa per at.% of solute [HB p.298]. T11's Mg plus available Si is ≈ 0.29 + 0.21 ≈ 0.5 at.% (derived from 0.26 wt.% Mg and ≈ 0.22 wt.% available Si, Section 3), against 1.77 at.% in the HB example. Applying 79 MPa/at.% gives a full-T6 ceiling of ≈ 40 MPa. The cure at 220 °C/10 min is far shorter than a T6 age (Section 7), so bake hardening of T11 should be well below that ceiling, and only if the anneal left Mg and Si in solution. Plant data are needed.

### Pitfalls
- *Corrected after the full-text pass:* the Hall–Petch friction-stress formula for Al–Mg is σ_f = 15.5·(wt.% Mg) (HB Eq. 24). The earlier "+ 24" was the equation number. It still reproduces the 5754/5182 σ₀ values only roughly (table above) [HB p.167].
- **Constituents crack early.** 25–50 % of constituent particles are cracked after 7 % plastic strain in uniaxial tension [HB p.122]. *Inference for slugs:* impact extrusion imposes strains far above 7 %, under mostly compressive stress. Coarse Fe-rich constituents are therefore likely void and crack sites in the can wall and at the bottom radius, so constituent size control (casting rate, Fe and Si level, rolling reduction [HB p.122]) is a formability lever, not only a recrystallisation lever.

---

## 5. Cold rolling, work hardening, recovery, recrystallisation and texture

### Mechanisms
- **Rolling temperature.** Commercial cold rolling heats the strip to 100–150 °C at strain rates of 50–100 s⁻¹. "Cold" rolling of Al is therefore well above 0.3 T_m and involves dynamic recovery [RY p.10].
- **Grain subdivision.** Cell blocks form, bounded by geometrically necessary boundaries (dense dislocation walls and microbands at ε < 0.7, ~40° to the rolling direction; lamellar boundaries at ε > 0.7). GNB misorientation rises to 15–20°; incidental boundaries reach about 3° [RY p.11–13]. Subgrain-misorientation data for AA3207 and AA1xxx (Forbord, Sæter) are in [RY p.11, Fig 2.3].
- **Shear bands** (±35° to the rolling direction) become frequent above a critical Mg content of 2–3 % (Inagaki & Kohara, 0.5–5 % Mg, up to 95 % reduction). They are most intense in the room-temperature dynamic-strain-ageing regime and less frequent at 77 K and 473 K in AlMg4.5 [RY p.17–19]. Al–Mg alloys show Portevin–Le Chatelier serrations and negative strain-rate sensitivity at RT [RY p.27].
- **Rolling textures** are the β-fibre (Copper {112}<111>, S {123}<634>, Brass {011}<211>).
  - Mg weakens the texture; at 3–5 % Mg, Brass grows at the expense of Cu/S through shear banding [RY p.19–22].
  - Non-shearable 0.1–5 µm particles sharpen the Cu texture; particles > 5 µm weaken it [RY p.20–21].
  - Fine grains develop the rolling texture faster [RY p.21].
  - Recrystallisation produces cube/Goss, especially in high-purity alloys. Particle-stimulated nucleation (PSN) at constituents randomises the texture [HB p.131].
- **Recrystallisation nucleation and retardation.** PSN occurs at constituents and coarse particles; the critical particle size decreases at lower deformation temperature and higher strain rate [HB p.130]. Fe in solution raises the recrystallisation start temperature through fine Al–Fe precipitation during the anneal; Si precipitation also impedes early recrystallisation [HB p.140].
  - The full text adds the mechanism: when Si precipitates before or during annealing, fine Al–Fe–Si or Si particles impede early recrystallisation inside the deformation zones and reduce the number of zones that can act as nuclei. Conversely, the more Fe and Si sit *out* of solution as constituents during deformation, the larger the volume fraction of particles big enough to nucleate grains, which refines the 1xxx grain (HB Fig. 47) [HB p.140].
  - Most products dynamically recover during hot working. Static recrystallisation may occur between or after rolling passes, and high-Mg alloys (lower stacking-fault energy) may recrystallise dynamically [HB p.130]. Cold-rolled sheet, rod and tube "almost invariably" recrystallise during annealing to O temper [HB p.131].
- **Transition-metal effect on the recrystallisation temperature (Yelagin, binary alloys).** Maximum increments of the recrystallisation onset/finish temperatures (Table 35): **Mn (0.77 at.%) +30/+25 K; Fe (0.04 at.%) +65/+35 K**; Cr (0.35) +45/+30; Zr (0.09) +105/+240; Sc (0.20) +120/+320; Ti (0.25) +5/+180; V (0.21) +15/+15; Ni (0.04) −10/+5 K [HB p.296]. The alloys were cast, annealed at 500 °C, hot rolled at 420–450 °C, annealed at 450 °C and cold rolled. For Period IV elements (Mn, Fe, Cr, …) the effect sets in only above a threshold close to their solubility at the solution-treatment temperature, and some elements show a maximum versus concentration [HB p.296].
  - An element is an efficient anti-recrystalliser if it has an incomplete 3d shell with few electrons, a large atomic-radius difference to Al, forms a supersaturated solution on solidification, and that solution decomposes into thermally stable fine dispersoids [HB p.296].
- **Al–Mn alloys specifically.** The Mn dispersoids hinder grain growth on recrystallisation and give fine-grained sheet. "High iron and silicon content and small amounts of copper and magnesium also tend to refine the grain size" [HB p.299]. Fe also controls texture and "prevents the formation of earing upon deep drawing" [HB p.299]. In 3xxx can alloys Mn (up to 1.25 %) allows high deformation and prevents grain growth through slowed recrystallisation and uniformly distributed Mn precipitates; Mn is "the cheapest addition in aluminum" [HB p.297].
- **Annealing of Al–Mg.** High-Mg alloys lose more strength by recovery, low-Mg alloys by recrystallisation. At equal partially annealed strength, the higher-Mg alloy keeps more elongation [HB p.168]. The data are binary Al–Mg alloys cold rolled 70 % and annealed 2 h at each temperature (HB Fig. 69). Higher Mg and lower annealing temperature give smaller recovered subgrains and higher retained strength [HB p.168–169].
- **Industrial annealing practice (HB Ch.19).**
  - Annealing is done above the recrystallisation temperature, so the required temperature depends on the prior strain. In commercial practice the annealing temperature is "the lowest temperature that yields the softest state in the minimum amount of time" [HB p.887].
  - **Non-heat-treatable alloys "are heated to temperature very quickly to avoid grain growth"**; a fine grain is the aim, and the cooling rate from the annealing temperature is unimportant [HB p.887].
  - Heat-treatable alloys: if the hardness comes from working, anneal at ≈ 650 °F (343 °C) and cool in any way. If it comes from prior heat treatment or hot work, anneal at ≈ 775 °F (413 °C) for 2–3 h, cool at ≈ 50 °F/h (28 °C/h) to 450 °F (232 °C) or lower; 7xxx get an extra 4 h at 450 °F. "To achieve proper control of the resulting annealed properties, it is best to resort to trial and error" [HB p.887].
  - Typical full-anneal temperatures (Table 7): **1060, 1100, 1350, 3004, 3105 and all listed 5xxx: 650 °F (343 °C); 3003: 775 °F (413 °C)**; for these, the time at temperature "should not be any longer than to get the center of the furnace load up to temperature", and the cooling rate is unimportant [HB p.888]. Heat-treatable wrought alloys: 760 °F (404 °C) for 2–3 h, then 50 °F/h to 500 °F (260 °C). Alclad material gets shorter times to limit diffusion into the cladding [HB p.888]. (°F → °C conversions derived.)
- **Work-hardening structure in 1xxx.** In 1145-H19 foil stock, cells reach a limiting size of a little under 1 µm at a true strain of about 0.15. Further strain raises misorientation [HB p.139–140].

### Quantitative data
- **Strain conversion** [RY p.56]:

  | Reduction | 39 % | 63 % | 78 % | 87 % | 92 % | 95 % | 98 % |
  |---|---|---|---|---|---|---|---|
  | ε = ln(t₀/t) | 0.5 | 1 | 1.5 | 2 | 2.5 | 3 | 4 |
- **Reversing the rolling direction (Al99.5, VA).**
  - Reversing direction by 180° between passes changes neither properties nor microstructure. Rm and Rp0.2 differ by 0.1–5 MPa longitudinally and 5–8 MPa transversely; HB and A10 are identical. The same holds for alloys and drawn wire [VA p.194–196].
  - Transverse Rm and Rp0.2 exceed longitudinal values by 7–20 MPa in unidirectional rolling and by 3–9 MPa with reversals. Transverse A10 is lower at small reductions; the difference disappears at higher reductions [VA p.194–195].
  - Up to 30 % reduction the only change is flattening of equiaxed grains. Above 50 %, longitudinal and transverse microstructures look alike. Pronounced banding appears only above 90 % [VA p.195].
- **Annealing windows.**
  - Recovery from 150–350 °C; rapid softening (recrystallisation) above about 280 °C [EAA p.52].
  - Fine recrystallised grain requires ≥ 15 % prior reduction ("critical work hardening"), fast heating, no exposure above 350–380 °C, and holding ≤ 2 h. 5xxx: 320–380 °C for 30–120 min [EAA p.52–53].
    - The heating-rate wording is now checked in the clean full text: "A rapid temperature gradient of 20 to 60°C per hour" [EAA p.53]. The number is printed as such, not an extraction error. That 20–60 °C/h is called "rapid" is still odd (it is batch-furnace slow), so treat it as an unexplained source value.
    - Below the critical work hardening, "heat treatment must be restricted to restoration without recrystallization" [EAA p.53].
  - **Golden rule for interstage annealing.** Anneal only when the work hardening has reached at least the critical work-hardening rate. Annealing metal that is "only slightly work-hardened" risks grain enlargement [EAA §VII.1.1 p.92; §VII.2.6 p.97]. Shop practice is torch annealing with tallow as indicator, which turns light brown at 340 °C [EAA p.92]. In 5xxx with > 3 % Mg, anneal "very carefully" to avoid sensitisation to intergranular corrosion (Section 11) [EAA p.92 fn 2, p.97 fn 1].
  - Grains above about 100 µm cause orange peel and reduce formability [EAA p.52].
  - Minimum annealing temperatures: 1xxx 360 °C, 3xxx 400 °C, 5xxx 350 °C [DW §3.1.4]. HB Table 7 is consistent for 3003 (413 °C) but anneals 1xxx, 3004 and 3105 at 343 °C, below DW's minima [HB p.888]. HB's Al–Mn table gives 3003 "400–600 °C", 3004 415 °C and 3105 345 °C [HB p.299]; the 3004 figure conflicts with Table 7's 343 °C (⚠ two chapters of the same book).
  - Salt-bath recrystallisation at 400 °C: AlMgX 25 s, AA3103 45 s after ε = 2. Conductivity did not change, so no Mn dispersoids precipitated [RY p.56–57].
  - Foil final anneal up to 340 °C for 12 h, which also burns off rolling oil [WP p.61].
- **Grain sizes** [RY p.66].
  - Cast and homogenised: AA1050 117 µm; AlMg0.5 86; AlMg1 79; AlMg3 68; AA3103 65 µm (random texture).
  - Transfer gauge: AA5005 175 µm (strong cube, 36× random); AA5182 50 µm (weak cube).
  - After cold rolling to ε = 2 and recrystallisation: AA3103-B 6 µm, AlMg3 8 µm, AlMg0.5 10 µm.
- **Effect of Mg on annealed grain size.** Mg up to 3.5 % progressively refines the annealed grain after 89 % cold reduction [HB p.166].

### Design levers
- **Get a fine O-temper grain (foil and fin stock).** Combine:
  - large prior strain (≥ 15 % critical; practice usually much more) [EAA p.53];
  - fast heating and a limited peak temperature [EAA p.53];
  - Fe and Si present as constituents for PSN, since more constituent particles give more nuclei and a finer grain [HB p.140, Fig. 47];
  - controlled dispersoid density, since fine dispersoids retard recrystallisation and coarsen the final grain [HB p.125].
- **Temper choice.** H2x (temper-annealed) and H3x (stabilised) give the same UTS as H1x with lower proof stress and higher elongation [DW §4.1.5]. Use H2x to recover ductility at a given strength. Al–Mg alloys, which recover strongly, benefit most [HB p.168].
  - **Definitions** [EAA §V.4 p.42–43]:
    - H1x: work-hardened only. H2x: work-hardened beyond the target, then partially annealed down to it. H3x: work-hardened and stabilised "either by a low temperature heat treatment or as a result of heat introduced during fabrication". **No stabilisation temperature is given** (cf. ch07 G10).
    - Second digit (UTS-based): HX8 is the hardest temper normally produced; HX4 is midway between O and HX8; HX2 midway between O and HX4; HX6 midway between HX4 and HX8; odd digits are intermediate.
    - HX11: strain-hardened after the final anneal, too much to count as annealed but not enough or consistently enough to qualify as HX1. H112: some strain hardening from hot working or limited cold work, with no upper property limits. H116: see Section 11.
- **Mill scheduling.** Reversing-mill passes can be taken without re-coiling to keep the rolling direction, which saves time and energy [VA p.196].
- **Earing.** Control it by balancing the annealing cube texture against the rolling texture of the final reduction, as done for 3004-H19 [HB p.131]. Fe in Al–Mn alloys suppresses earing through texture control [HB p.299]. The quantitative definitions (r̄, Δr = (r₀ − 2r₄₅ + r₉₀)/2, LDR) and 3003-O values (r̄ 0.6, Δr 0.2) are in ch05 §4.11 [HB p.851–853].
- **Relevance: slug anneal (inference from HB Ch.19 practice and the Fe/Si effects above).**
  - Heat the slugs fast and hold only until the coldest slug reaches temperature [HB p.887–888]. A basket or coil that heats slowly in its centre gives the centre slugs a slow-heating anneal, the condition that coarsens the grain [EAA p.53].
  - On a fast rotary caster with no homogenisation, part of the Fe (and Mn, Si) stays in solution [HB p.294–295]. That dissolved Fe raises the recrystallisation onset during the slug anneal by precipitating finely [HB p.140], by up to ≈ 65 K in Yelagin's binary data [HB p.296]. Constituent Fe and Si, by contrast, refine the grain by PSN [HB p.140, p.299]. Measure T11's anneal curve (hardness and conductivity against temperature) instead of assuming 1xxx-like recrystallisation.

### Pitfalls
- Slow heating or too little strain gives coarse grains; holding above 350–380 °C causes grain growth [EAA p.53]. Repeated interstage anneals of lightly strained metal enlarge the grain [EAA p.97]. *Inference for slugs:* the same applies to any small strain picked up between the final anneal and a later heat exposure (levelling, slug sizing). It parallels the 3–7 % sizing-strain coarse-grain effect in brazed MPE tube (ch07 §8.5).
- Processing heat-treatable 1xxx/3xxx stock at 400 °C can precipitate Mn and change properties. Check it with conductivity [RY p.56].
- **Very fine grains.** Stable grains < 10 µm are what superplastic sheet needs [HB p.131]. At ~1 µm (particle-stabilised 8xxx) the strong grain-size hardening (m ≈ 1) comes with a loss of work-hardening capacity that limits tensile ductility [HB p.102]. Neither is a target for slugs.
- 5xxx with high Mg develops shear bands and is "notoriously hard to fabricate" hot and cold [RY p.17; HB p.166].

---

## 6. Homogenisation and the as-cast → homogenised state (3xxx focus)

**Table 6.1 – AA3103 homogenisation and Mn in solid solution** [RY p.54, after Sjølstad 2003] (wt.% conversion derived; 1.0 wt.% Mn = 0.49 at.%)

| Code | Cycle | Mn in solid solution |
|---|---|---|
| AC | As cast | 0.40 at.% (≈ 0.81 wt.%) |
| A | 100 °C/h to 610 °C, hold 14 h, quench | 0.24 at.% (≈ 0.49 wt.%) |
| B | A + cool 20 °C/h to 550 °C, hold 16 h, quench | 0.20 at.% (≈ 0.41 wt.%) |
| C | B + cool 20 °C/h to 500 °C, hold 24 h, then to 450 °C, hold 32 h, quench | 0.15 at.% (≈ 0.31 wt.%) |

- AA1050 and AlMgX: 100 °C/h to 550 °C, 6 h, cool 6 °C/h to 350 °C, quench [RY p.54].
- **Derived design estimate.** Going from AC to C removes about 0.5 wt.% Mn from solution. At +21 MPa/wt.% [HB p.160], that is roughly −10 MPa annealed yield strength, with a large gain in conductivity (Section 2 ranking). This assumes the linear coefficient applies.
- A homogenised 500 mm 3004 ingot becomes progressively more homogeneous through hot rolling to 47 mm and cold rolling to 0.33 mm [HB p.160 Fig. 61].
- **HB on 3xxx homogenisation (full text).** Typical as-cast 3003 ingot holds 0.7–0.9 % Mn in solution; the rest sits in Al–Mn–Fe and Al–Mn–Fe–Si constituents. Homogenisation precipitates Al₁₂(Mn,Fe)₃Si or, below 0.07 % Si, Al₆(Mn,Fe) dispersoids, "typically less than 1 µm" in diameter, with the size set by the thermal cycle [HB p.160]. Si speeds Mn precipitation, densifies the α dispersoids and lowers the Mn left in solution; with enough Si, as-cast Al₆(Mn,Fe) converts to Al₁₂(Mn,Fe)₃Si; a higher Fe/Mn ratio favours Al₁₃(Fe,Mn)₄ in the as-cast state [HB p.160].
- **Furnace terms (HB Ch.19).**
  - *Preheat:* heating logs or billets to a uniform intermediate temperature before extrusion or forging, as fast as the allowable surface condition permits; some tolerate direct flame, others need tight surface-temperature control to avoid surface melting, which causes tearing and die sticking [HB p.886–887].
  - *Reheat:* heating slabs before rolling, repeated as the slab is reduced [HB p.887].
  - *Homogenisation:* a long soak, "generally the 15–20 hour range", after casting [HB p.887].
  - Pit furnaces are the usual equipment for homogenising or preheating ingots and coils [HB p.927].
- **Limits of homogenisation for transition metals.** Dendritic segregation of Mn, Cr, Zr and similar elements "cannot be easily eliminated by homogenization" because they diffuse at only 10⁻¹⁴–10⁻¹² cm²/s at 500 °C [HB p.295].
- **Levers.**
  - High-temperature soak followed by stepped slow cooling lowers Mn in solution (higher conductivity, more and coarser dispersoids).
  - A single-step treatment with a quench keeps more Mn in solution [RY p.54].
  - Si accelerates Mn precipitation [HB p.160].
- **Relevance: rotary-cast strip, no homogenisation (inference).** The user's route replaces the 15–20 h soak with in-line hot rolling from ≈ 500 °C and a water quench at ≈ 380 °C. The Al–Mn decomposition window starts at 300–350 °C [HB p.295] and 325 °C [HB p.299]. So the slug anneal, not a homogenisation step, is where most supersaturated Mn and Fe can precipitate, and it must do so alongside recrystallisation (concurrent precipitation). With T11's low Mn (0.14 %) this matters less than for 3102/3207; Fe supersaturation is the open question (Section 5).
- **Pitfall.** Dispersoid size and number density are not reported in the read portion of RY. HB gives only "< 1 µm" for 3xxx dispersoids [HB p.160], so they still cannot be linked quantitatively to recrystallisation behaviour here (gap).

---

## 7. Heat treatment of heat-treatable alloys (2xxx/6xxx/7xxx) and heat-treatment equipment

### Mechanisms
- Precipitation sequences:
  - 6xxx: SSSS → separate Mg and Si clusters → co-clusters → GP zones → (Si-rich phase) → β″ → β′ → β (Mg₂Si) [RY p.8; HB p.173–174]. HB Ch.19 gives the shorter form GP zones → β′ → β, with needle GP zones along ⟨001⟩ [HB p.916].
  - Al–Mg–Si GP zones are single-atomic-layer plates (2.5 nm thick, ~30 nm long) with Mg:Si = 1, only partially coherent, and stable up to ≈ 260 °C. β″ is a needle phase (Si:Al:Mg = 6:3:1 as printed); GP zones and β″ form in parallel and compete. Both are sheared by dislocations and localise slip; β′ rods are bypassed by Orowan looping [HB p.174–175].
  - 7xxx: SSSS → GP → η′ → η (MgZn₂) [RY p.8].
  - Al–Cu: GP zones → θ″ → θ′ → θ; GP zones dissolve above 190 °C; θ′ misfit 4.5 % [HB p.141–144].
- In 6xxx, Si clusters form within the first minute at 200 °C. Excess Si lowers Mg₂Si solubility, speeds precipitation and raises GP-zone density [HB p.174].
- **Ageing delay and the GP-zone critical temperature (Al–Mg₂Si).**
  - Below about 0.9 at.% Mg₂Si, supersaturation is low and precipitation on ageing straight after the quench is heterogeneous (on dislocations); a room-temperature delay then *refines* the final structure. Above about 1.1 at.% Mg₂Si, precipitation is homogeneous and a delay coarsens it [HB p.175–176].
  - The critical temperature above which GP zones do not form is **T_v (°C) = 111 + 71 × (wt.% Mg₂Si)** (HB Eq. 28) [HB p.177].
  - ~0.25 % Cu lessens the delay penalty; a short pre-age above the ageing temperature dissolves delay-formed zones; 0.5 h at 160 °C straight after the quench, before the delay, removed the penalty in an Al–1.2 % Mg₂Si alloy [HB p.177].
  - Deformation before artificial ageing changes properties only slightly, but it lowers precipitation temperatures and accelerates ageing; alloys with excess Si respond more because Si nucleates on dislocations [HB p.180].
  - At room temperature, dislocations *slow* precipitation by annihilating quenched-in vacancies; at 120–180 °C they speed precipitation and coarsening by pipe diffusion [HB p.904].
- **Quench sensitivity of Al–Mg₂Si.** HB compares still-air cooling (0.65 °C/s) with cold-water quenching (> 1000 °C/s). Mn- and Cr-bearing alloys are the most quench sensitive because their dispersoids nucleate β″; homogenised material is less sensitive [HB p.177–179]. Mn, Cr, Zr, V and Fe *reduce* the ageing-delay penalty, especially at slow quench rates (15 °C/min), by lowering supersaturation [HB p.177].
- **Quench sensitivity** comes from loss of solute to coarse heterogeneous precipitates and loss of vacancies to sinks. Cr dispersoids cause the most sensitivity, Mn-bearing dispersoids less, and coherent Al₃Zr the least [HB p.126–127].
- **Precipitate-free zones (PFZ)** narrow with higher solution temperature and faster quench. Ageing at 93 °C removed PFZs in Al–Zn–Mg–Cu even after a 2 °C/s quench [HB p.129–130]. Pre-ageing at low temperature recovers strength in slowly quenched material [HB p.127–128].

### Quantitative data – see the master table in Section 13.3
- 6xxx extrusions:
  - Press spray quench for thin sections; air quench gives T5 for some 6xxx.
  - Thick 6xxx, 2xxx and 7xxx need a separate furnace solution treatment and tank quench.
  - Age 150–180 °C for several hours [DW §2.3.2].
- 6xxx alloy groups [HB p.171]:
  - (1) Balanced Mg + Si = 0.8–1.2 % (6063): extrudable and air-quenchable.
  - (2) Mg + Si > 1.4 %: stronger and quench sensitive; water quench.
  - (3) Excess Si: extra ageing response, but Si segregates to grain boundaries and causes intergranular embrittlement, countered by Cr/Mn.
  - 6061 = Al–1Mg–0.6Si + 0.25Cu.
- T8 (cold work before ageing) raises 2xxx yield strength by up to 35 % over T6. In 2519, Mg plus cold work adds 190 MPa against 150 MPa expected from additivity [HB p.149, p.151] (*page corrected after the full-text pass; was p.148–149*).
- **Solution heat treatment (HB Ch.19).**
  - The temperature sits just below the eutectic melting point; for 2xxx the margin is only a few degrees (2014: 496–507 vs 510 °C; 2017: 496–507 vs 513 °C; 2024: 488–507 vs 502 °C) [HB p.889].
  - Local solute concentrations or too-fast heating (undissolved Al₂Cu in 2xxx) cause incipient melting and solidified "rosettes", which NDT cannot detect [HB p.889].
  - Example windows (°F): 6061 960–1075; 6066 960–1010; 6262 960–1050; 2024 910–930; 7075 860–930 (sheet) [HB p.892].
  - Soak time is counted from when the load thermocouple recovers to within 6 °C of the set point. Minimum soaks (Table 12): ≤ 0.016 in: 10 min salt bath / 20 min air furnace; 0.125–0.250 in: 35 / 50 min; 0.251–0.500 in: 45 / 60 min [HB p.891, p.894].
- **Quenching (HB Ch.19).**
  - Heterogeneous precipitation during the quench is fastest at intermediate temperatures, where both supersaturation and diffusion are high [HB p.895]. The critical range for 7075 is 400–290 °C. Above 450 °C/s gives maximum strength and corrosion resistance; 450–100 °C/s lowers strength only; 100–20 °C/s gives the worst corrosion resistance; below 20 °C/s strength drops but corrosion resistance recovers [HB p.895–896].
  - Required cooling rate for heat-treatable alloys: 200–1000 °F/s through 800–500 °F (≈ 110–560 °C/s through ≈ 427–260 °C, derived) [HB p.936].
  - Quench Factor method: τ = Σ Δtᵢ/Cᵢ along the cooling path, with property p = p_max·exp(K₁τ), K₁ = ln 0.995 [HB p.897–898]. For 1.6 mm 7075-T6 sheet, τ = 0.46 (cold water, strongly agitated) gave YS 73.4 ksi, against 66–69 ksi for interrupted quenches with τ = 8.5–21 [HB p.899] (Table 15; printed "MPa", but the values are ksi magnitudes).
  - Maximum quench delays: 5 s (≤ 0.41 mm), 7 s (0.41–0.79), 10 s (0.79–2.29), 15 s (> 2.29 mm). Delays may be exceeded if the part stays above ≈ 413 °C (482 °C for 2219) [HB p.899].
  - **Water temperature controls the cooling rate** (Table 17, probe data): maximum cooling rate 153 °C/s with 40 °C water, 115 at 60 °C, 79 at 80 °C, 48 °C/s at 90 °C. At a part temperature of 343 °C the rate is 97 / 87 / 77 / 26 °C/s for 40 / 60 / 80 / 90 °C water [HB p.901]. The cooling rate depends on water temperature and agitation, not on the metal's conductivity or heat capacity [HB p.900].
  - Water below ≈ 50–60 °C often quenches non-uniformly (unstable vapour blanket: spotty hardness, distortion, cracking). Distilled water forms a more persistent vapour blanket than hard water [HB p.900–901]. PAG polymer quenchants give rates between water and oil [HB p.901–902]. Spray quenching is mainly a plate and sheet-mill technique; optimum droplet ≈ 0.8 mm [HB p.903].
- **Natural and artificial ageing (HB Ch.19).**
  - Natural ageing stabilises after ≈ 4–5 days; T3/T4 are based on 4 days. 6xxx and 7xxx keep changing for years. Natural ageing is almost fully suppressed at −40 °C [HB p.907–908].
  - Artificial ageing runs at 95–205 °C [HB p.920] (200–450 °F, i.e. 93–232 °C, on p.911). YS rises faster than UTS, so ductility and toughness fall [HB p.920].
  - Higher ageing temperatures reach peak faster, so production uses lower temperatures to keep the fastest-heating parts of a load from over-ageing [HB p.920].
  - Table 22 practices: 6xxx AQ/W → T4 at ambient, 96 h minimum; 6061/6063/6066 T4 → T6 at 350 °F (177 °C) for 8–10 h; 6013 T4 → T6 at 375 °F (191 °C) for 4–5 h; 6951 T4 → T6 at 320 °F (160 °C) for 17–19 h [HB p.924–925].

### Design levers
- Form heat-treatable alloys in T4/W and age afterwards: larger allowable strain and almost no work hardening [EAA p.53]. W temper lasts typically ≤ 15 min at ambient [WP p.47].
  - [EAA §VII.1.2–1.3 p.92–93]: 6xxx and 7xxx extrusions should be shaped in T1/T4 "within a short time window of a few days" after solution treatment, and very extensive shaping "a few minutes" after it, before natural ageing hardens the metal. T6 must be shaped cold: heating "will considerably reduce mechanical properties (approx. 40 %)".
  - Bending is possible within about 2 h of the quench, or 4–5 days if stored at −6 to −10 °C [DW §3.1.4].
- Prefer Zr over Cr/Mn dispersoids in thick, slowly quenched products [HB p.127].
- Paint-bake-responsive 6xxx auto sheet (Micromill MMHF-T4): yield strength 152 MPa in T4, rising to 165 MPa and 249 MPa after the two paint-bake simulations (0 % + 180 °C/20 min and 0 % + 225 °C/30 min; column mapping ⚠) [MM sl.12].
- As-quenched (AQ) material is nearly as ductile as O temper, so parts are often formed between the quench and ageing [HB p.904]. Refrigerated storage keeps the AQ condition (Table 19): 2014/2024/2219 must be chilled within 15 min and then last 1 / 30 / 90 days at −12 / −18 / −23 °C; 6061/7075 within 30 min and then 7 / 30 / 90 days [HB p.910].
- **Relevance: T11, in-line quench, slug anneal and the 220 °C/10 min bake (inference from the HB data above).**
  - T11 holds ≈ 0.41 wt.% Mg₂Si (Section 3). That is ≈ 0.15 at.% counted as Mg₂Si units, or ≈ 0.45 at.% counted as Mg + Si atoms (derived), so either way it is well below the ≈ 0.9 at.% threshold for homogeneous precipitation, so on any later heating Mg–Si precipitation will be heterogeneous, on dislocations [HB p.175–176]. Its GP-zone critical temperature is T_v ≈ 111 + 71 × 0.41 ≈ 140 °C (derived) [HB p.177], well below the 220 °C bake. During the bake, clustering or β″ formation is therefore expected mainly on the dislocations of the heavily extruded can wall. Excess Si raises that response [HB p.180]. Whether it outweighs bake recovery is unknown.
  - The bake can act only on Mg and Si that are still in solution after the slug anneal. HB's rule that the cooling rate after annealing is unimportant [HB p.887–888] holds for non-heat-treatable alloys. For a lean Al–Mg–Si alloy such as T11, slow furnace cooling from the anneal should precipitate Mg₂Si and remove most of the bake response; a faster cool should keep it. The anneal cooling rate is therefore a design variable for T11.
  - In-line cooling bath: HB's probe data show the cooling rate at 343 °C dropping from 77 °C/s (80 °C water) to 26 °C/s (90 °C water) [HB p.901]. Keeping the bath well below boiling is therefore one lever for retaining Mg, Si and Mn in solution after hot rolling (probe data; strip cooling also depends on agitation and contact time). Very cold water (< 50–60 °C) risks non-uniform quenching and strip-shape problems [HB p.900–901]. The strip enters the bath at ≈ 380 °C, already inside the 400–290 °C critical range quoted for 7075 [HB p.895–896]. So both the transfer time from the hot mill and the bath temperature matter; HB gives no critical range for lean Al–Mg–Si.

### Pitfalls
- 7xxx in T6 must not be bent (stress-corrosion cracking risk); 2xxx in T6 accepts very little deformation [DW §3.1.4].
- Long delays at room temperature before artificial ageing of Al–Cu can coarsen the precipitates and lower properties [HB p.143].
- Peak-ageing always lowers toughness monotonically from the under-aged state. Over-ageing restores toughness only when matrix microstructure controls fracture [HB p.134].
- **"High-temperature oxidation" is really hydrogen from moisture.** During solution treatment, moisture in the furnace air supplies hydrogen that diffuses into the metal, gathers at inclusions and discontinuities, and forms surface blisters. 7xxx (especially 7050) is most susceptible, then 2xxx; extrusions blister most, then forgings. Remedies: dry and clean loads and racks, sequence doors over quench tanks, use ammonium fluoroborate (≈ 5 g per m³ of workload space; corrosive, so stainless furnace panels are recommended), or anodise large parts first [HB p.892–894]. HB Ch.3 adds that hydrogen porosity can also form in *solid* products heated to high temperature in humid environments [HB p.119].
- Under-heating leaves solute out of solution and lowers aged strength; 2024-T4 properties rise steeply above ≈ 488 °C [HB p.889].
- Overshoot above the upper uniformity limit is not allowed in aluminium heat-treating furnaces [HB p.921].

### Heat-treatment equipment and furnace practice (HB Ch.19; relevance to slug annealing)
- **Furnace families** [HB p.920, p.922–938]:

  | Type | Batch or continuous | Typical use in HB | Notes |
  |---|---|---|---|
  | Roller hearth, pusher, belt, chain | Continuous | High-volume work with little change in alloy, process or part | Two roller-hearth lines solution treat 150 cast wheels/h each with one operator [HB p.929, p.931] |
  | Car-bottom | Batch | Annealing large forgings and plates; ageing and homogenising | Sand seals against cold-air leaks; a three-zone unit holds ±5 °F (±2.8 °C) on 40,000 lb (≈ 18 t) loads [HB p.922, p.930] |
  | Pit (below grade) | Batch | Homogenising or preheating ingots and coils; **annealing ingots and coils** | "Excellent temperature uniformity", simple to run; large pits use several control zones; rarely used for solution treatment because the quench delay is hard to meet [HB p.927] |
  | Vertical tower | Batch | Long extrusions | Several zones, each with its own controller [HB p.922] |
  | Drop-bottom / pusher | Batch | Solution treatment (drop-bottom is the most common) | Indirect gas radiant tubes or electric elements, shielded from the parts; air goes down past the elements and up through the load via adjustable louvers. HB lists pusher furnaces under both continuous and batch types [HB p.920, p.929, p.931] |
  | Salt bath | Batch | Solution treatment | Molten K/Na nitrate–nitrite, often with chromate; rapid heating; uniformity "usually much better than ±5 °F"; best kept at one temperature [HB p.937–938] |
  | Fluidised bed | Batch | Solution treatment | Sand fluidised by a burning gas/air mix; rapid, even heat-up; uniform heat transfer reduces warping [HB p.938] |

- **Common specifications** [HB p.920–922]: operating range 830–1080 °F (443–582 °C) for solution furnaces; uniformity ±5 °F or ±10 °F (±2.8 or ±5.6 °C); no overshoot; ceramic-fibre insulation up to 8 in (≈ 200 mm); control accuracy within 2 °F; high- and low-air temperature recorded in each zone; electric, indirect radiant-tube or direct-fired gas heating; high-velocity recirculated air through stainless ductwork. Large ovens (10 × 12 × 60 ft) certify to ±5 °F and must recover within 30 min after loads above 25,000 lb (≈ 11 t) [HB p.934]. Recuperators on radiant tubes give up to 15 % efficiency gains [HB p.934]. (°F and lb conversions derived.)
- **Temperature uniformity** [HB p.936–937]:
  - Uniformity is "directly proportional to recirculated airflow".
  - It degrades with cold-air aspiration through openings, poorly mixed hot air, air bypassing the heat source, a changed load, misplaced or inaccurate thermocouples, or damaged insulation.
  - Cold spots are almost always near doors or far from the fan.
  - Louvers are typically designed for a 1 in water-column pressure drop, about 4000 ft/min outlet velocity (≈ 20 m/s, derived).
  - Fan-motor current shows whether the air path is too open or too restricted.
- **Loading and heating** [HB p.887–891]:
  - Air furnaces need about 2 in (≈ 50 mm) between parts, placed in line with the airflow so that no part shades another.
  - Soak time is counted from when the load thermocouple is within 6 °C of the set point.
  - Non-heat-treatable alloys should be heated "very quickly to avoid grain growth".
- **Atmosphere.** HB Ch.19 treats air furnaces only. The atmosphere problem it covers is moisture, as hydrogen pick-up and blistering (Pitfalls above). It says nothing about nitrogen or other protective atmospheres, or about oxide (MgO) growth during annealing; for those see ch14.
- **Quality control and pyrometry** [HB p.964–966]:
  - A temperature-uniformity survey (TUS) is required when the furnace enters service and after major changes. Typical bands are ±10 °F for solution treatment and ±5 °F for precipitation hardening.
  - Survey density: at least one thermocouple per 25 ft³ (≈ 0.7 m³), minimum 9 and up to 40, at the corners and centre of the work zone; furnaces under 9 ft³ use 3 thermocouples.
  - The survey must mimic normal practice (cold-charged or hot-charged). Readings every 2 min until equilibrium, then every 5 min for at least 15 min; maximum spread 20 °F.
  - Solution furnaces are surveyed monthly, ageing furnaces every 6 months. Continuous furnaces are surveyed with load thermocouples or judged from part properties.
  - The control thermocouple is checked against a test thermocouple within 3 in; a mismatch above ±3 °F means shut-down and quarantine of the work since the last check. Thermocouples are calibrated weekly against NIST-traceable standards.
  - Records are kept for at least four years.
- **Relevance: slug annealing (inference from the HB practice above; no HB data on slugs).**
  - *Batch versus continuous.* A belt or roller-hearth furnace that heats slugs in a single layer meets HB's "heat quickly, hold only until the centre reaches temperature" rule for non-heat-treatable alloys [HB p.887–888] better than a pit or car-bottom furnace loaded with deep baskets. In a basket the outer slugs over-soak (grain growth, more MgO) while the centre slugs heat slowly (coarse grain). If batch annealing is kept, use shallow loads with spacing in line with the airflow [HB p.891] and qualify the load, not only the empty furnace.
  - *Uniformity target.* The recrystallised grain size depends on heating rate and peak temperature [EAA p.53], so slug-to-slug temperature spread becomes grain-size and hardness spread. HB's ±5.6 °C (±10 °F) solution-furnace band is a sensible minimum and its ±2.8 °C (±5 °F) ageing-furnace band is preferable. Survey with load thermocouples placed in slugs at the corners and centre of the load [HB p.964–966].
  - *Atmosphere.* Humid furnace air is a hydrogen source [HB p.892] and Mg-bearing alloys oxidise faster in the melt [HB p.168]. Dry, oil-free slugs and a controlled dew point (or N₂, ch14) should therefore be part of the anneal specification for Mg-bearing slugs such as T11. The dew-point limit is not given in HB.
  - *Cooling after the anneal.* For 3102/3207-type alloys, the cooling rate is unimportant [HB p.888]. For T11 it is a lever on bake response (Design levers above).

---

## 8. Casting, melt quality and solidification

### Mechanisms
- Hydrogen solubility falls about 10× on freezing, which causes gas porosity. Hydrogen enters from oxide-film moisture, the atmosphere and refractories [HB p.75, p.119; WP p.70]. Shrinkage pores are elongated and more damaging than spherical gas pores [HB p.119].
- **Oxide films.** "Old" oxides come from the crucible and are removed by filtration. "Young" oxides are entrained when melt velocity exceeds 0.5 m/s. Double films act as cracks: bending strength of turbulently filled castings is about 10 % of quiescently filled ones, about 80 % of casting scrap is attributed to oxides, and fatigue life falls by orders of magnitude [HB p.118–119].
- **Defect hierarchy for fatigue.** Oxides > porosity > constituents > persistent slip bands. In wrought alloys, microporosity and constituents head the list [HB p.132].
- **Inclusions.**
  - Types: γ-Al₂O₃ films, Al₄C₃, MgO/MgAl₂O₄ spinel (in Mg-bearing melts; increase with time and temperature), refractories, liquid chlorides and flux salts, TiB₂ (grain refiner), AlP, and (Ti,V)B₂ from boron treatment.
  - Effects: pinholes in light-gauge foil, flange cracks in cans, streaks on litho and bright trim, wire breaks.
  - Measurement: PoDFA, Prefil, K-mould, LiMCA.
  - Removal: ceramic foam, porous tube, bonded and deep-bed filters [WP p.71–74].
- Mg-containing melts form much thicker oxide; Be or Li reduce oxidation [HB p.168].
- **Oxide-film detectability.** Entrained oxide defects can be as small as 10⁻⁶ m wide with films down to 10⁻⁸ m thick, below the sensitivity of current NDT [HB p.119]. Real-time radiography shows that surface turbulence during filling is the main source of porosity, because entrained oxides nucleate hydrogen pores [HB p.119–120].
- **Primary-metal refining (HB Ch.1).** Raw smelter Al carries non-metallics (α/γ-Al₂O₃, Al carbide and nitride, graphite), metallics (Fe, Si from raw materials and cell parts) and hydrogen. Filtration through a fluxing filter while blowing nitrogen lowers H from 0.22 to 0.16 cm³/100 g. Bubbling N₂ with 2–10 % Cl₂ removes Na, H and non-metallics together and brings Na to 0.0003–0.001 % (gas use printed as 0.8–1.5 m³ per gram of metal, presumably per tonne) [HB p.23]. Mn and Sc do not change the melting point of Al and are not removed by zone refining [HB p.29].

### Quantitative data and process facts
- **Direct-chill (DC) casting route.** DC casting produces rolling slab and extrusion log. Slabs are scalped on both faces and slowly preheated; the hot line is a breakdown mill plus a tandem mill. Plate is ≥ 6 mm; sheet is cold reduced with interpass anneals [DW §2.2; TAL p.20–21].
- **Continuous casting.**
  - Foil: continuous casting plus cold rolling uses much less energy and has become the preferred foil route [WP p.61].
  - Micromill (continuous cast + roll) claims: 20-day processing reduced to 20 minutes, 50 % less energy, ¼ of the footprint [MM sl.8].
  - Micromill C6A0 6xxx (0.85–1.2 mm) vs DC 6022 (0.95 mm): FLD₀ ≈ 26–28 vs 23.6; LDR 2.08–2.13 vs 1.88–1.98 [MM sl.11].
- **Recycled shredder scrap** (Si 5.5–6.5, Mg 0.5–1.0, Zn 1.5, Cu 2.8–3.8, Fe 0.7, Mn < 0.3 %).
  - Conventionally cast: coarse intermetallics, brittle at zero plastic strain.
  - Melt-spun at 10⁵–10⁶ °C/s (ribbons 50–100 µm, wheel 25 m/s, melt 750 °C), cold compacted and extruded at 450 °C: about 40 % fracture strain [SIL p.32–36].
  - Ductility roughly doubles from RT to 200 °C, with most of the gain between 200 and 300 °C [SIL p.43].
  - Extruded sheet section: r₀ 0.56, r₄₅ 1.09, r₉₀ 0.63; r̄ = 0.84; Δr = −0.50 [SIL p.45–46].
- **Primary energy (for comparison with remelting).** US average electrolysis consumption ≈ 15.18 kWh/kg Al; modern high-amperage lines reach ≈ 13.0 kWh/kg, at 94–96 % current efficiency [HB p.22]. In 1995 secondary (recycled) metal was a little over one third of the US supply [HB p.2].
- **Remelting.** Recycling uses about 5 % of primary energy, but up to 15 % of the charge is lost as dross [WP p.6]. Can scrap is remelted at 750 ± 100 °C and degassed with Cl₂/N₂ [WP p.26].
- **Solidification basics.** Lever rule f_s = (C_l* − C₀)/(C_l* − C_s*); k₀ = C_s*/C_l*; tip and eutectic undercoolings are typically ≤ 0.1 °C; length scales are PDAS λ₁, SDAS λ₂ and λ_eut [PC p.1–5].
- **Grain refinement.** Ti and/or B inoculants are standard [HB p.130]. Sr modifies eutectic Si; P refines primary Si [HB p.120–121].

### Design levers
- **Foil and can stock.** Filtration, degassing and online H measurement (closed-loop recirculation analysers; RPT is only semi-quantitative) directly control pinholes and flange cracks [WP p.70–74].
- **Ingot porosity.** Healed by extrusion, forging or adequate rolling reduction. Thick plate is the hard case because rolling can generate tensile stresses [HB p.120].
- **Scrap selection.** Airframe scrap (high Cu/Zn) is unsuitable for non-aerospace alloys [DW §2.1.2]. Cans recycle back into can stock [TAL p.16].

### Pitfalls
- A grain refiner adds Ti, which ranks high among conductivity-damaging impurities [HB p.52]. Balance grain refinement against conductivity in fin and conductor alloys *(inference)*.

---

## 9. Hot working (extrusion, rolling) and product forms

**Table 9.1 – Extrusion window** [DW §2.3]

| Item | Value |
|---|---|
| Temperature | about 500 °C |
| Extrusion ratio, 6xxx | ideal 30–50; ≤ 7 lowers properties; ≥ 80 gives excessive pressure and die failure |
| Press | 10–120 MN; container 100–700 mm; die-face pressure up to about 700 MPa; 85–90 % of billet used; lengths up to 40 m |
| Speed | 6063 ≥ 25 m/min |
| Minimum wall | 6063 non-hollow: max(1.2 mm, 1 % of section size); hollows about 25 % more; thicker for strong 6xxx, weldable 7xxx, and much more for 2xxx, strong 7xxx and 5xxx |
| Tongue aspect ratio | < about 3.0 for 6063 with rounded tips; lower for stronger alloys |
| Bridge (porthole) dies | Fine for 6xxx and weldable 7xxx; not for 2xxx, strong 7xxx or 5083. Seam welds are potential weak lines, so keep fabrication welds away from them. |
| Correction | Stretch 1–2 %. In non-heat-treatable extrusions this lowers the compressive proof stress (Bauschinger effect). |
| Extrudability ranking | 6xxx ≈ pure Al > weldable 7xxx >> 2xxx, strong 7xxx, 5xxx (5083 poor). Non-heat-treatable extrusions are only available as F/O. |

- Extruded and drawn rod develops a dual <001>+<111> fibre texture. Longitudinal yield strength is then about 70 MPa above transverse; recrystallisation removes the gain [HB p.131]. In 6082 and 7108 (not recrystallised), texture explains most of the strength anisotropy; recrystallised 6063 and 7030 need other explanations. A relaxed-constraints Taylor model predicts r-values [RY p.iii].
- **Clad sheet.** Cladding plates are roll-bonded on the slab at the hot mill, about 5 % per face. 2xxx is clad with pure Al, 7xxx with Al–1 % Zn [DW §2.2.5]. This is the same principle used for braze-clad 3xxx (general knowledge).
- **Thin products.** Very thin foil (< 0.025 mm) is pack-rolled double, which gives one bright and one matte side [WP p.61]. Thickness tolerance is estimated as ±(0.11√t + 0.00004w − 0.06) mm for sheet and ±(0.000014wt + 0.3) mm for plate [DW §2.2.4].
- **Mill productivity.** Over about 25 years, rolling speed rose from 150 to > 600 m/min and coils from 1–2 t to 15–20 t [TAL p.24].
- **Tube routes.** Welded tube is made from 3xxx/5xxx coiled strip [DW §2.4.3]. Drawn (seamless) tube is made from mandrel-pierced blooms, giving about 10 % wall-thickness variation from eccentricity [DW §2.4.2].

---

## 10. Joining

- **Arc welding (MIG/TIG).**
  - Suitable for 1xxx, 3xxx, 5xxx and 6xxx. Not for 2xxx (cracking) or strong 7xxx; weldable 7xxx needs good technique [DW §3.3.1].
  - TAL: 2014 and 7075 are virtually unweldable, as are most Cu-containing alloys; 6082 is weldable [TAL p.11].
- **HAZ softening.** 6xxx-T6 is nearly halved in strength over ≥ 25 mm from the weld; 7xxx softens less but over a wider zone. Control interpass temperature [DW §3.3.1]. Design HAZ strengths are given in EN 1999-1-1 Table 3.2 [EAA p.69].
- **Fillers** [DW §3.3.4].
  - 4043A (≈ 5 % Si) prevents cracking for 1xxx, 3xxx and 6xxx.
  - 4047A (≈ 12 % Si) for high restraint, with some loss of corrosion resistance.
  - Al–Si fillers give **no** crack protection if the parent metal has > 2 % Mg.
  - 5556A gives the best weld-metal strength on 7xxx and 5083.
  - Filler Mg should broadly match the parent: lower is weaker, higher is a corrosion risk.
- **Friction-stir welding (TWI 1991).** Plates 3–12 mm; fine-grained nugget; stronger and better in fatigue than arc welds; joins 2xxx and 7075. Needs rigid backing and leaves an exit hole [DW §3.4]. Al₃Sc limits HAZ grain growth and narrows PFZs in welds [WP p.53].
  - [EAA §VIII.8 p.120–121] adds: welds up to 50 mm thick from one side and 100 mm from two; one tool lasts up to ~1000 m of weld in 6xxx; no filler, gas or porosity; machines up to 20 m long. It cannot make joints that need deposited metal, such as fillet welds.
- **Why Al welds differently from steel** [EAA §VIII.1 p.108; p.161]:
  - The oxide melts at ~2000 °C against 630–660 °C for the metal, so it must be removed or broken up.
  - High conductivity and melting energy mean arc welding needs about the same energy as steel.
  - Thermal expansion is 2× steel, and the weld bead contracts ~6 % in volume from liquid to RT. Both cause distortion and hot-crack risk.
- **Process windows** [EAA Table VIII.3 p.117; p.109–119]:
  - TIG-AC: 0.8 ≤ t ≤ 5 mm in the table (1–6 mm in the text); preheat above 6 mm. TIG-DC: 0.2 ≤ t ≤ 10 mm, machine welding only. The He-shielded DC variant welds 10–12 mm in one pass but needs the arc height held within 0.5 mm.
  - MIG: smooth current t ≥ 3 mm (butt welds need a backing bar); pulsed t ≥ 2 mm (2 < t ≤ 5 mm without backing); wire pulsation 1–5 mm; CMT t ≤ 1 mm.
  - Laser: 1–4 mm, up to 12 m/min at ~1 mm and 1–3 m/min at 1.5–3 mm. Laser-MIG (70 % He / 30 % Ar): one pass up to 10 mm. Plasma-MIG: one pass up to 10 mm, practically pore-free.
- **Filler selection notes** [EAA Table VIII.2 p.116]:
  - (a) 5xxx with > 3.5 % Mg is sensitive to intergranular corrosion above 65 °C in aggressive environments. ⚠ Ch. XI uses > 3 % (Section 11).
  - (b) **5xxx with < 3 % Mg and Mg-containing 3xxx "may be sensitive to hot cracking."**
  - (e) Avoid welding Al–Si castings to 5xxx: Mg₂Si forms in the weld and weakens it.
  - Store filler sealed; humidity on the wire causes porosity. Dry reels left open for months at ~80 °C overnight [EAA p.117].
- **Weld preparation** [EAA §VIII.9 p.122; §VII.2.3 p.96]:
  - Machine edges cut by water jet, plasma or laser to remove the rough, thick-oxide, micro-cracked layer. The thermal-cut HAZ is < 1 mm, but short-transverse cracks up to ~2 mm deep occur. Removing 2 mm restores the metal, as it does for sheared plate > 10 mm.
  - Degrease with acetone or industrial alcohol, never trichloroethylene (forms phosgene in the arc). Then stainless-steel brush. Bring parts into the shop two days ahead so condensation dries.
  - Deburr with milling tools, not grinding discs, whose residues cause weld porosity [EAA p.111].
- **Weld-defect causes** [EAA Table VIII.4 p.124–125]:
  - wormholes/porosity: poor degreasing, dirty or wet wire, poor gas cover, cold start, fast cooling;
  - oxide inclusions: poor shielding, metal stored badly;
  - cracks: unsuitable base or filler, welding sequence, over-clamping, sudden cooling;
  - crater cracks: abrupt arc stop.
  - Quality levels follow EN ISO 10042 and EN 1090-3 [EAA p.123–124].
- **Repair** [EAA Ch. XIII p.158–161]: use the same (or a compatible) alloy as the original. Cut out with plasma or carbide wheels, not HSS or abrasive wheels, which leave inclusions. Enlarge patches slightly by hammering to offset weld contraction; small patches crack more readily.
- **Brazing.** Al is brazed with an Al–Si eutectic filler; brazing alloys melt above 400 °C [HAB p.10]. Wrought 4xxx is used almost exclusively for welding wire and braze cladding [TAL p.10]. Al–Si alloys serve as brazing sheet and welding rod [HB p.169]. Brazing sheet dates from the 1960s [MM sl.4]. **No brazing metallurgy is in the read portions** (gap).
- **Adhesive bonding.** One-component epoxies cure from 1 h at 120 °C to 10 min at 180 °C [DW §3.6.4]. Best pretreatment is a sulphuric–dichromate etch or anodising, not hard anodising [DW §3.6.2]. Bonded bicycle frames failed when slight corrosion undercut the adhesive [WP p.45].
- **Mechanical fastening.** Use stainless or Al bolts; Al bolts are 6xxx in T6/T8 [DW §3.2.1]. Rivets are 5154A/5056A (5056A not recommended in the tropics), hot-driven at about 350 °C, or 6082 in T4 within 2 h of the quench [DW §3.2.3].
  - Steel bolts on Al need insulating gaskets against galvanic corrosion [EAA §IX.2 p.133].
  - Use threaded holes in Al only when there is no alternative and the YS exceeds 200 N/mm². Thread length is 1–2× the major diameter (≈ 1.2× for 6xxx-T6, longer for softer alloys). Use inserts (e.g. Helicoil) for repeated assembly [EAA §VII.5 p.103–104].
  - Adhesive bonding insulates dissimilar metals and gives high fatigue strength and damping. Its drawbacks are low peel strength, ageing (creep, humidity, UV) and the need for surface pre-treatment [EAA §IX.1 p.130–132].
- **Design factors (EN 1999).**
  - Partial factors: γ_M1 = 1.10 for members, γ_M2 = γ_Mw = 1.25 for connections. Commercial-vehicle load factors: 1.1 dead, 1.5 live [EAA p.63].
  - Weld fatigue detail categories range from 63-4.3 to 40-4.3 depending on weld quality [EAA p.79–80].
  - Parent-metal properties have very little effect on the fatigue strength of real structures, and none at connections [EAA p.78].

---

## 11. Corrosion behaviour and alloying effects

### Mechanisms and data
- **Passive film.** It forms in about 10⁻⁴ s and is 5–20 nm thick [HB p.60]. The oxide's molecular volume is about 1.3× that of the Al consumed; the film thickens in the presence of water vapour and has a "complex structure" at elevated temperature [HB p.60–61]. Under normal conditions the first layer, no more than 10 nm thick, is amorphous oxide, and the second is a composite of bayerite and boehmite whose thickness depends on environment and exposure time [HB p.62]. In water below 60 °C, amorphous hydroxide plus bayerite forms; boehmite forms at 60–80 °C [HB p.62]. Standard potential E⁰ = −1.663 V vs SHE [HB p.61–62]. Passivity starts at pH ≈ 2.67 for unit Al³⁺ activity, and the boehmite solubility boundary lies at pH 12.3 (activity 1) to 6.3 (activity 10⁻⁶) [HB p.64].
  - EAA gives "around 1–10 nm" for the natural oxide. It calls it chemically very stable, well adherent and self-repairing [EAA §XI.2.1 p.146]. ⚠ This does not match HB's 5–20 nm. The overlap is 5–10 nm; film thickness depends on age and environment (general knowledge).
  - Strong acids or alkalis destroy the film. So do aggressive ions locally, chloride being the typical case (seawater, road salt), which leads to pitting. "Some alloying elements might increase the corrosion resistance of the oxide layer, while others can weaken it"; the elements are not named [EAA p.146].
  - Anodising thickens the film ~1000× over the natural film. It is done in sulphuric acid, and the porous cells are sealed in boiling water [EAA §X.4.1 p.141].
- **Chemical resistance lists (HB Tables 17–18).**
  - *Good resistance:* acetic acid, acetone, alum, ammonia, detergents, emulsifiers, essential oils, fatty acids, fruit juices, glycerin, milk products, strong nitric acid, seawater, sugar syrups, sulfur and SO₂ (dry and wet), vegetable oils, vinegar, water, among others [HB p.61].
  - *Not resistant:* caustic soda and potash, hydrochloric, hydrobromic, hydrofluoric, phosphoric and sulfuric acids, dilute nitric acid, wet chlorine and fluorine, copper, nickel and mercury salts, zinc chloride, hypochlorites, sodium sulphite and hydrogen peroxide [HB p.61].
  - ⚠ The text later says Al has "very high resistance" to *concentrated* hydrogen peroxide [HB p.66], which conflicts with its listing in Table 18; concentration probably decides. Dilute H₂SO₄ (1–20 %) attacks all grades even at room temperature. Glacial acetic acid has little effect, but the attack grows at low concentrations. Formic, oxalic and some chlorinated organic acids attack Al [HB p.66].
- **Potentials in other electrolytes (0.1 N calomel scale)** [HB p.63 Table 19]: Al −0.86 (1 M NaCl), −0.50 (1 M Na₂SO₄), −0.71 (1 M Na₂CrO₄), −0.80 (1 M HCl), −0.49 (1 M HNO₃), −1.50 (1 M NaOH), −0.80 V (1 M NH₄OH). The Al potential therefore shifts by about 1 V with the electrolyte.
- **Pitting.** Caused by film breakdown, mainly by halides. Oxidisers (H₂O₂, free Cl) accelerate it, more strongly in acid. Sn in the film raises ionic conductivity and dissolution [HB p.65].
- **Effect of purity.** 99.99 % Al has a lower pitting probability, and refined 99.99 % Al is 3–15× more corrosion resistant than commercial purity [HB p.65]. At ≥ 99.99 %, corrosion in HCl is governed by Cu: sheet with > 2×10⁻³ % Cu perforated in 1 week in 20 % HCl, against 2 weeks at 0.9–3×10⁻⁴ % Cu (1.5 mm sheet; exponents confirmed in the full text). Fe also raises the corrosion rate; Al with ≤ 0.003 % Fe corrodes at 0.10–0.157 g/(m²·h) (medium not restated; the context is HCl). Ga (0.5 % → 120 g/m²·h) and Re (0.3 % → 250 g/m²·h) are very harmful; 0.14–0.19 % Nb reduces resistance; Ti has no effect; 0.05–0.5 % Be has a slight effect [HB p.66].
- **Potentials in 1 M NaCl (V vs 0.1 N calomel):** Mg −1.72, Zn −1.15, **Al −0.86**, Fe −0.72, Cu −0.35. Al is cathodic to Mg and Zn and anodic to Fe and Cu in most electrolytes [HB p.63].
- Pure Al is less noble than most alloys, which is why it is used as a protective cladding that cathodically protects the core [HB p.60, p.77].
- **Al–Mg.** β (Al₃Mg₂) nucleates on grain boundaries at ambient temperature in alloys with more than about 3 % Mg, reducing ductility and SCC resistance. Above 4 % Mg, cold work promotes grain-boundary precipitation. Alloys above 5 % Mg need special tempers [HB p.161–162].
  - H116 applies to 5xxx with ≥ 3 % Mg. It must pass accelerated intergranular and exfoliation tests and is suited to continuous service ≤ 65 °C [EAA p.42–43].
  - High-Mg alloys can suffer intergranular corrosion and SCC [HB p.166].
  - Cr is often added to 5xxx for corrosion protection [HB p.168].
  - **Sensitisation kinetics** [EAA §XI.2.2.6 p.151]:
    - Al–Mg alloys with > 3 % Mg held long at 65–200 °C can form a **continuous bead of Al₈Mg₅** along grain boundaries. EAA's Al₈Mg₅ and HB's Al₃Mg₂ name the same β phase (general knowledge). The bead is anodic to the matrix.
    - Intergranular corrosion needs **both** this sensitisation **and** an aggressive electrolyte (e.g. saline) on the bare surface.
    - Kinetics depend on Mg content and production route. Forming and welding can raise susceptibility.
    - The **thermal load (temperature × time) matters more than temperature alone**: sensitising 5086 takes ~2 years at 65 °C and several months at 100 °C; the fastest sensitisation is at 130–200 °C.
    - Field data: heavy-fuel-oil road tankers ran ≥ 20 years, 8–10 h/day, i.e. ≥ 50 000 h cumulative at 65–70 °C, without problems.
    - Guideline: use alloys with **≤ 3 % Mg** where long exposure above ~75 °C occurs; consult the producer for higher Mg.
    - ⚠ EAA is internally inconsistent on the threshold: > 3 % Mg in Ch. XI but > 3.5 % Mg in the filler-metal table [EAA p.116].
  - *Relevance to lean 3xxx (inference):* the user's 3102/3207 alloys hold 0.12–0.15 % Mg; variants under discussion have 2–3× that (ch09). All are an order of magnitude below the 3 % threshold, so β sensitisation is not a mechanism for them. It matters only if a 5xxx slug alloy is considered. EAA does flag a different Mg risk for welding: **Mg-containing 3xxx may be sensitive to hot cracking** [EAA p.116].
- **Corrosion forms in service (EAA Ch. XI).** EAA lists galvanic, crevice, pitting and filiform corrosion for commercial vehicles. It states that other forms exist, but the alloys and tempers most used in vehicles are not prone to them [EAA §XI.2.2 p.147, §2.2.7 p.151].
  - **Galvanic.** Needs (1) two materials of different potential, (2) an electrolyte and (3) direct or indirect contact. Al is the anode and dissolves, leaving a white alumina layer [EAA §XI.2.2.1 p.147–148]. Prevention: insulating elastomer (e.g. neoprene) sleeves, washers and gaskets, plus sealing compounds that close gaps and stop water entrapment [EAA p.148, Fig. XI.3].
  - **Crevice.** Capillary forces hold moisture and aggressive deposits in narrow gaps. The rate is "normally very low" because the stable alumina product seals the crevice. Still, close or seal gaps in the road-splash zone [EAA §XI.2.2.2 p.149].
  - **Pitting** is the most common form on Al [EAA §XI.2.2.3 p.149].
    - Pit size and depth depend on the alloy, the degree of cold work and the heat treatment, and on aggressive ions in the environment.
    - Pits start where the oxide film is damaged or imperfect, e.g. ground areas or weld discontinuities.
    - Pits deepen quickly after initiation and then slow down, because insoluble alumina adheres inside the pit and blocks access of the medium. This is why bare Al can serve for decades in rural, marine or sea-water exposure.
    - EAA concludes that pitting "is quite normal and does not impact the durability of vehicles". That holds for structural sections; it is not a criterion for thin-walled or appearance-critical parts (inference).
  - **Filiform (under-film) corrosion** grows as worm-like filaments under paint or enamel [EAA §XI.2.2.5 p.150].
    - The mechanism is similar to pitting: moisture penetrates the coating and an oxygen-concentration cell makes the filament head anodic.
    - The metal is barely attacked, so the effect is mainly cosmetic, but it can delaminate the coating.
    - It depends mostly on the environment and on **the quality of the pre-treatment before painting**. Follow the paint supplier's pre-treatment and use a suitable primer.
  - **Design rules** [EAA §XI.2.2.4 p.150]: avoid constructive gaps or seal them; avoid water traps (open side downwards); avoid weld discontinuities; separate dissimilar metals with coatings or insulation.
- **Fabrication- and handling-induced corrosion** [EAA]:
  - Traces of ferrous or cuprous metal from shared tools cause localised corrosion. Use tools and equipment dedicated to Al [EAA §VII.2 p.93; §VII.1 p.92].
  - Iron particles embedded by blasting or grinding are galvanic cells that cause "superficial micro-pitting" in moisture. Use iron-free abrasives (e.g. non-recycled corundum) [EAA §X.4.2.1 p.142, fn 1].
  - Store sheet under cover in a ventilated area, separated by timber blocks, never directly on the floor and away from splash water and condensation, to prevent **condensation (water) stains**. Sheets thicker than 0.8 mm are stored upright, thinner ones flat [EAA §VII.2.1 p.93; §VII.3.1 p.98].
- **Paint pre-treatment** [EAA §X.4.2 p.141–143]:
  - Degreasing alone is not enough. The **natural oxide must also be removed**, because it disturbs paint adhesion.
  - Chemical route: alkaline etch (NaOH-based; concentration and temperature set the rate) or acid etch (phosphoric or nitric), then a ~20 min fresh-water rinse, because the etched surface is rough and moisture-sensitive.
  - Mechanical route: grinding (grit 120–180) or blasting. Stock removal is < 0.1 mm, similar to etching.
  - Prime straight after pre-treatment: wash or reaction primer ~10 µm (8–10 µm), then basecoat 60–70 µm, then topcoat 50–60 µm within 2 h.
  - "Problems with the paint decoration often are not related to the paint or the aluminium itself, but more with an insufficient pre-treatment."
- **Cleaning** [EAA Ch. XII p.154–155]: detergents must be compatible with Al (not too acidic or alkaline). Test them first on bare Al, do not clean in direct sunlight, do not let detergent dry on the surface, and rinse with de-ionised water. Some tank-cleaning regulations prescribe strong acids or alkalis that exclude Al as a tank material.
- **Strong alloys.** Cu-bearing alloys are less corrosion resistant (galvanic effect of Cu) [WP p.3]. 2xxx is prone to SCC and is being replaced by 7xxx [WP p.48]. Field failures: a 6 % Cu torpedo boat (Yarrow) and a 2xxx bascule bridge (Sunderland, marine/industrial atmosphere) [DW §1.4–1.5].
- **Corrosion ratings** (A very good … D poor).
  - All listed 3xxx, 5xxx and 6xxx sheet and extrusions are rated A [EAA p.46–47].
  - 7020-T6: C; 7003 and 7108 (T6/T7): B [EAA p.47].
  - Castings: 21100 D; 42000 B/C; 42100, 43000 and 44000 B [EAA p.48].
- **Zn for potential control.** Zn is present at about 1 wt.% in some non-heat-treatable alloys **to adjust solution potential** [HB p.95]. 7072 contains 0.8–1.3 % Zn (composition only) [WP p.50]. 7xxx clad uses Al–1 % Zn [DW §2.2.5].
- **Other corrosion facts.**
  - As-cast surfaces resist corrosion better than machined ones (thicker oxide) [EAA p.54].
  - Chromates, dichromates, silicates and borates inhibit corrosion in closed water systems [HB p.66].
  - Al resists NH₄OH even at pH 13 but not most mineral acids. Concentrated HNO₃ (> 80 %) corrodes it at < 0.1 mm/yr [HB p.66].
- **Bimetallic contact.**
  - Insulate with primer, impervious tape or a gasket; protect from green concrete, soil, oak and some insulation boards [DW §3.7.5].
  - Primers must not contain Cu, Hg, Sn, Pb or carbon compounds [DW §3.7.4].
  - Al wiring failures came from CTE mismatch, creep and galvanic action [WP p.46, p.65–67].
- **Anodising** [DW §3.7.3].
  - Film thickness: 10–15 µm indoors; ≥ 25 µm outdoors (architectural grade).
  - Chromic process: ≤ 10 µm, but better corrosion resistance per µm.
  - Hard anodising: up to 125 µm.

### Design levers (heat-exchanger relevance)
- **Sacrificial layer.** *Inference:* Zn (≈ 1 %) and high-purity or Zn-bearing clads lower the potential of an outer layer relative to the core, so attack stays lateral and sacrificial [HB p.95, p.60; DW §2.2.5]. Core alloys should avoid Cu-free pitting initiators such as coarse Fe-rich constituents *(inference from [HB p.66])*.
- **Cu control.** Keep Cu low in non-heat-treatable alloys (≤ 0.3 % [HB p.94]). Cu ennobles the alloy and drives corrosion of high-purity Al [HB p.66; WP p.3]. *Inference:* where a more noble core is wanted, a small controlled Cu addition is the potential lever; the source does not quantify this.

### Design levers (packaging: impact-extruded aerosol cans) — *inference from EAA Ch. VII, X, XI and HB*
- **Pitting and filiform start at surface damage and contamination.** Pits nucleate at damaged or imperfect oxide [EAA p.149]. Embedded Fe particles act as galvanic micro-pitting sites [EAA p.142], and filiform corrosion under organic coatings is governed by pre-treatment quality [EAA p.150].
  - For slugs and cans this means: limit Fe pick-up from rolls, shears and slug-handling equipment; keep slug surfaces free of embedded debris; treat lacquer pre-treatment (oxide removal or conversion) as part of corrosion design, not only adhesion.
  - None of this is quantified for 3xxx/1xxx can stock in the sources.
- **Oxide on the annealed slug.** Paint adhesion requires removing the natural oxide [EAA p.141]. Annealing-grown oxide (the MgO issue in this KB) is therefore something the coating pre-treatment must remove or tolerate. Its thickness should be controlled with that in mind. HB adds that the film thickens with water vapour and has a complex structure at elevated temperature [HB p.60–61], and that Mg-bearing *melts* carry much thicker oxide than pure Al [HB p.168]. Both point the same way for annealing Mg-bearing slugs in humid air (inference). The sources give no MgO growth data for solid annealing; see ch14.
- **Product-side resistance (inference from HB Tables 17–18).** Typical aerosol-relevant media (water, vegetable and essential oils, fatty acids, detergents, acetone, glycerin) are on HB's "good resistance" list, while alkalis, halide acids, hypochlorites, Cu/Ni/Hg salts and dilute sulfuric acid are on the "cannot resist" list [HB p.61, p.66]. These are generic statements for bare Al, without alloy, temperature, concentration or time. They do not replace pack testing of the internal lacquer system.

### Pitfalls
- **Missing topics.** No source read so far covers long-life or sacrificial 3xxx brazing-sheet concepts, post-braze corrosion (brown band), exfoliation of 7xxx, or SWAAT/SAAT testing. EAA Ch. XI is now read in full (2026-10-12) and does not cover them either. It is a qualitative guide for 5xxx/6xxx vehicle structures, with no corrosion rates, potentials or test data, and nothing on 3xxx packaging alloys or internal-lacquer/product corrosion of cans.
- **Oxide-thickness values disagree:** 1–10 nm [EAA p.146] vs 5–20 nm [HB p.60]. HB's own layer model (amorphous inner layer ≤ 10 nm plus a variable bayerite/boehmite layer [HB p.62]) partly reconciles them: the inner barrier layer matches EAA, and the total film matches HB's 5–20 nm (inference).
- **HB is generic on chemicals.** The full HB text has the chemical-resistance lists above, but nothing on lacquered or internally coated containers, filiform corrosion or aerosol formulations.
- **Mg threshold for sensitisation:** EAA uses both 3 % [p.151] and 3.5 % [p.116].

---

## 12. Temperature effects, fatigue and application requirements

### 12.1 Temperature (EAA Tables V.6/V.7; properties at test temperature after 10,000 h exposure)

| T (°C) | −196 | −80 | −28 | 20 | 100 | 150 | 200 |
|---|---|---|---|---|---|---|---|
| 5086-O Rm / Rp0.2 / A % | 390/140/34 | 280/120/26 | 270/120/24 | 270/120/22 | 270/120/26 | 210/110/35 | 155/105/45 |
| 6082-T6 Rm / Rp0.2 / A % | 380/330/16 | 330/295/13 | 330/285/12 | 320/285/12 | 300/265/15 | 240/220/18 | 130/105/28 |

- **Elevated temperature.** Strength loss is negligible up to 100 °C for short exposure or 80 °C for long exposure. Above 100 °C, H12/H16 and T5/T6 lose strength strongly, while O/H111 and T1/T4 lose moderately [EAA p.51]. Some alloys lose strength above 100 °C [DW §1.3.2].
- **Low temperature.** There is no ductile–brittle transition; strength and elongation improve at low temperature [EAA p.51; HB p.72; WP p.51 (5083 cryogenic)].
- **Overheating.** Al does not glow before melting [WP p.45]. Overheated cylinder heads and welded frames creep and distort later [WP p.45].
- **Fatigue.** There is no fatigue limit, so design for finite life. Al alloys are rarely used where high-cycle life above 10⁷ cycles is required [WP p.45; HB p.72]. Endurance in tension–compression is 0.85–0.95 of the bending value; in torsion 0.55–0.65 [HB p.72]. Al is more fatigue-prone than steel [DW §1.3.2]. A 2xxx crane jib designed at stresses that were too high failed early in fatigue [DW §1.5.3].
- **Elevated temperature, 3xxx.** Al–Mn alloys gain strength at low temperature and keep "sufficient" tensile properties up to 200 °C [HB p.299]. *Relevance:* the 220 °C/10 min bake sits just above that range, so a small strength loss by recovery of the extruded wall is possible (inference; not quantified in HB).
- **Ductile damage in pure Al.** In pure Al (A99) necking is not accompanied by porosity, and at room temperature cracks appear only close to failure. Strain localises into micro-centres at ε < 1–2 % at 20 °C but only at ε > 10–15 % at 300 °C, and no microcracks form up to 50–70 % deformation at 300 °C; failure is transcrystalline [HB p.73].

### 12.2 Application-driven requirements

| Application | Requirements and targets in sources | Alloys and tempers cited |
|---|---|---|
| **Commercial vehicles** | Weight saving, measured as fuel per tonne saved: 0.6 l/100 km [EAA p.16]; 1,500 l/100,000 km (heavy goods) or 600 l (voluminous) [EAA p.22]; bus 1,700–1,900 l/100,000 km [EAA p.22]. 1 kg Al saves 28 kg CO₂ in a truck and 40–45 kg in a bus [EAA p.22]. Average 800 kg saved per articulated vehicle [EAA p.12]. Payback < 2 years [EAA p.30]. Service life > 20 years [EAA p.34]. IRTE Class A: 7° tilt at 44 t [EAA p.20]. Design for deflection: E is ⅓ of steel and CTE 2× [EAA p.59]. | Tipper floor 5083 H32/H321/H34, 5086 H24, 5383 H34, 5454 H22/H24, 5456 H34; 6 / 8 / 10 / ≤ 12 mm for light / medium / heavy / extreme duty [EAA p.35]. ADR tanks to EN 14286 in O/H111: 5083, 5086, 5383, 5454, 5754, 5182, 5186, 5059, 5088 [EAA p.37, p.49]. Extrusions 6060, 6005A, 6008, 6106, 6082, 6061, 7020 [EAA p.47]. Crash boxes and bumpers 7003/7108; crash modules 6008; wheels 6061/6082; diesel tanks 5052/5754; bus sides 3003/5005 (coated); suspension parts cast 21100 [EAA p.49]. |
| **Beam efficiency** | YS: mild steel 350, HSS 760, Al 250 MPa. Equal strength: weight 1 / 0.71 / 0.42. Equal stiffness: weight 1 / 1 / 0.55, with Al section 1.40× higher [EAA p.18]. Example: an IPE240 steel beam (30.7 kg/m) is matched in EI by an Al I330×200×6×10 at 15.8 kg/m (51 %), with stress 161 vs 73 MPa at equal deflection [EAA p.60–61]. | 6082-T6 |
| **Automotive body** | Formability (FLD₀, LDR), hemming, paint-bake response; Micromill claims a 25–35 % weight reduction vs HSS [MM sl.9–14]. ~131 kg Al per car in 2005 [EAA p.11]. | Outer panels 6111, 2008, 6016, 6022; inner 5083, 5754; structures 5182/5754 sheet and 6061/6063 extrusions [WP p.55; MM sl.4]. MMHF-T4 (YS 152, UTS 282 MPa, uniform elongation 25.8 %, FLD₀ 33.7) vs 5182-O (124 / 275 / 21.2 / 23.4) [MM sl.12]. |
| **Packaging** | Can body relies on constituent control and earing control [HB p.123, p.131]. Foil: impermeable above 25 µm, pinholes below; gauges 6–200 µm (household 22 µm, heavy-duty 33 µm); inclusions cause pinholes [WP p.59–61, p.71]. Cans recycle can-to-can [TAL p.16]. **Impacts:** HB's standard-products chart lists impacts for **1100 and 1199** only among the 1xxx grades (not 1060, EC, 1145, 1180) [HB p.76]. | 3004-H19, 1145 (foil) [HB p.123, p.75]; 3004 "the main material for beverage cans" [HB p.299]. Alloys of 92–99 % Al for foil and cans [WP p.9]. |
| **Electrical** | EC ≥ 99.45 % Al [HB p.70]. ISO E-Al annealed conductivity > 35.4–35.7 m/(Ω·mm²) [HB p.36]. Cr+V+Mn+Ti ≤ 0.01–0.015 % [HB p.52]. An Al conductor carries the same current with 50 % more area at half the weight of Cu [WP p.66]. | 1350; 8xxx conductor alloys (Alcoa 1972, 8030, 8176), which keep strength after current-cycle tests [WP p.65]. |
| **Heat exchangers** | Al is a valid alternative to Cu, with conductivity about 4× steel, but alloying can cut it by up to ~50 % [DW §1.2]. Foil is used for heat exchangers (conduction) [WP p.62]. Heat exchangers are listed as an automotive Al application [MM sl.5; TAL p.15]. | 4xxx braze cladding [TAL p.10]; 3102 composition: Si ≤ 0.40, Fe ≤ 0.7, Cu ≤ 0.10, Mn 0.05–0.40, Zn ≤ 0.30, Ti ≤ 0.10 [WP p.49]; 3003: Mn 1.0–1.5, Cu 0.05–0.20, Fe 0.7, Si 0.6 [WP p.48]; AA3207 (0.4 % Mn) studied in [RY p.11, p.16]. |
| **Building and marine** | Durability, extrudability, finish [TAL p.13]. | 3xxx hard-rolled trapezoidal cladding; 6063 windows [DW §1.5.4]. Marine: 5xxx plate (5083, 5086, 5052, 5059) plus 6xxx extrusions [DW §1.5.6; WP p.54]. |

Additions from EAA Ch. VI §8–9 (read 2026-10-12):
- **Abrasive wear (tipper floors)** [EAA §VI.9.2.2 p.88–89]:
  - The hardness of a work-hardened alloy cannot always be linked to its wear resistance; the type of load decides.
  - Mineral loads (stone, cement, chalk) wear far more than agricultural loads. Changing the sand type alone raised wear by 35 % in lab tests.
  - Mass loss is linear in the number of tipping cycles.
- **ADR tank shells** [EAA §VI.9.1 p.86–87]:
  - Equivalent thickness e = 464·e₀ / ∛(R_m·A)². Minimum 4.00 mm (Al, protected shell ≤ 1.80 m) or 5.00 mm (> 1.80 m).
  - EN 14286 alloys allow e = 5.3 mm at R_m·A = 6600 and 5.0 mm at R_m·A ≥ 7152. The arithmetic reproduces these values with e₀ = 4 mm (derived check).
- **Detail fatigue** [EAA §VI.8.2 p.83–85]:
  - In the FE example, a chassis gooseneck radius of 1000 mm gives σ_max 43 MPa, 450 mm gives 73 MPa and 300 mm gives 85 MPa. The text says stress rises ~70 % and deflection ~23 %, and that reducing the radius "from the normal radius of 450 mm to 350 mm" halves the life. ⚠ The figure shows 300 mm, not 350 mm.
  - A Ø20 mm hole in the flange cuts life by > 80 %, and a welded fixture on the flange by > 90 %. The same features on the web have no effect.

---

## 13. Key data tables

### 13.1 Physical properties (consolidated)

| Property | Pure / high-purity Al | Commercial purity and alloys |
|---|---|---|
| ρ (g/cm³) | 2.6984–2.70 | 2.71 (99.0 %); alloys 2.67–2.80; −0.5 % per wt.% Mg |
| E (GPa) | 69–72 | 69–72 (design 70); 67 at 100 °C, 59 at 200 °C |
| ν | 0.31–0.33 (0.35 WP) | 0.33 design |
| CTE (10⁻⁶ K⁻¹), 20–100 °C | 23.4–23.9 | 22–24.5 (design 23); 26 at 200 °C |
| k (W/m·K) | 237–240 (calculated ≈ 247 at 25 °C, HB Table 11) | 209–222 (99.49–99.70 %, at "200°"); −up to 50 % in alloys; 2 % Mn: 126 |
| ρ_el (µΩ·cm), 20 °C | 2.63–2.65 (≈ 65 % IACS) | 2.74 (99.8), 2.80 (99.5), 2.87 (99.0); alloys up to 2× pure |
| T_m (°C) | 660.2–660.4 | 657–658 (99.0–99.5 %); alloys lower |
| SFE (mJ/m²) | 135 [HB p.40] or 200 [HB p.85] (⚠ HB disagrees with itself) | lowered by solutes (e.g. Ag, Mg) |
| O-temper conductivity (% IACS, unit inferred) | — | 1100-O 57–62; 3003-O 44.5–50.5; 5052-O 34–37; 6063-O 57–65 [HB p.928] |

Sources: [HB p.37–66, p.928; DW §1.2; WP p.1–3]

### 13.2 Solute effects on conductivity and strength (what the sources quantify)

| Element | Max solid solubility (at.%) | Conductivity penalty (ranked, 1 = worst) | Strength effect (quantified) | Work-hardening effect | Notes |
|---|---|---|---|---|---|
| Cr | 0.40 | 1 | dispersoid former; Al₁₂Mg₂Cr / E phase | — | worst for quench sensitivity [HB p.127] |
| V | — | 2 | — | — | removed by B treatment [WP p.73] |
| Mn | 0.90 (1.82 wt.%) | 3 | O: +21 YS / +42 UTS MPa per wt.% in solution; H19: +35 YS | H = 1.03 ± 0.17 GPa | only 0.2–0.3 wt.% stays in solution after preheat; recrystallisation onset/finish up to +30/+25 K (0.77 at.%) [HB p.296] |
| Ti | — | 4 | grain refiner | — | — |
| Mg | 16.26 | 5 | O: up to 175 MPa YS at 6 %; H19: +70–85 YS per wt.%; Hall–Petch σ_f ≈ 15.5 MPa per wt.% | K = 0.37; H = 1.52 ± 0.14 GPa | shear bands > 2–3 %; β phase on grain boundaries > 3 % |
| Ag | 23.8 | 6 | — | K = 0.15 | lowers SFE |
| Cu | 2.48 | 7 | most effective per atom ≤ 0.5 at.%; E +4.4 %/at.% | K = 1.00; H = 3.38 ± 0.20 GPa (highest) | ≤ 0.3 wt.% in non-heat-treatable alloys; ennobles; corrosion of high-purity Al |
| Zn | 66.4 | 8 | least efficient | K = 0.071; H = 0.27 GPa | ~1 wt.% to lower potential |
| Si | 1.59 | 9 | raises strain hardening (impedes recovery) | H = 1.56 ± 0.05 GPa | E +8.5 %/at.%; accelerates Mn precipitation; binds vacancies |
| Fe | 0.025 | 10 | +7 MPa per vol.% constituent | particle-induced recovery | ≈ 0.05 µΩ·cm per wt.% (as constituent, derived); in solution raises recrystallisation onset/finish up to +65/+35 K (0.04 at.%) [HB p.140, p.296] |
| Ni | 0.023 | 11 | clusters (hardens more than size model predicts) | — | — |

Sources: [HB p.52–53, p.92–100, p.122, p.138–168, p.296; WP p.73]. **Per-wt.% resistivity increments for solutes in solution, and the corresponding thermal-conductivity coefficients, are NOT given in the sources read (gap). The full HB text was checked on 2026-10-12 and does not contain them either.**

### 13.3 Heat-treatment and thermal windows

| Operation | Alloy | Window | Source |
|---|---|---|---|
| Homogenisation | AA3103 (1 % Mn) | 610 °C/14 h (+ step cool 550/16 h, 500/24 h, 450/32 h) → Mn in solution 0.24 → 0.15 at.% | [RY p.54] |
| Homogenisation | AA1050, AlMgX | 550 °C/6 h, cool 6 °C/h to 350 °C | [RY p.54] |
| Preheat (phase selection) | Al–Fe | 607 °C/16 h → Al₃Fe; 482 °C/16 h → Al₆Fe | [HB p.138] |
| Homogenisation (general) | logs, billets | long soak, "generally the 15–20 hour range" | [HB p.887] |
| Mn precipitation from supersaturated solution | Al–Mn (3xxx) | Al₆Mn decomposition 300–350 °C; commercial Al–Mn solution decomposes above 325 °C | [HB p.295, p.299] |
| Full anneal (Table 7) | 1060, 1100, 1350, 3004, 3105, 5xxx / 3003 | 650 °F (343 °C) / 775 °F (413 °C); hold only until the load centre reaches temperature; cooling rate unimportant | [HB p.888] |
| Full anneal (Al–Mn table) | 3003 / 3004 / 3105 | "400–600 °C" / 415 °C / 345 °C (⚠ 3004 conflicts with Table 7) | [HB p.299] |
| Full anneal, heat-treatable alloys | 2xxx, 6xxx, 7xxx wrought | 760 °F (404 °C) 2–3 h, cool 50 °F/h (28 °C/h) to 500 °F (260 °C); 7xxx add 450 °F (232 °C)/4 h | [HB p.887–888] |
| Full anneal | 5xxx | 320–380 °C, 30–120 min; ≥ 15 % prior strain; avoid > 350–380 °C | [EAA p.53] |
| Minimum anneal temperature | 1xxx / 3xxx / 5xxx | 360 / 400 / 350 °C | [DW §3.1.4] |
| Recovery / recrystallisation onset | non-heat-treatable | recovery 150–350 °C; rapid softening > 280 °C | [EAA p.52] |
| Flash recrystallisation | AlMgX / AA3103 (ε = 2) | 400 °C salt bath, 25 s / 45 s | [RY p.56] |
| Foil final anneal | 1xxx foil | up to 340 °C/12 h | [WP p.61] |
| Solution treatment | 6xxx (shop practice) | "slightly above 500 °C", 20–30 min, water quench | [DW §3.1.4] |
| Solution treatment | Al–4Cu | 550 °C, water quench | [HB p.143] |
| Solution treatment | 6061 / 2024 / 7075 sheet | 960–1075 / 910–930 / 860–930 °F (516–579 / 488–499 / 460–499 °C) | [HB p.892] |
| Solution soak (minimum) | wrought, 0.125–0.250 in / 0.251–0.500 in | salt bath 35 / 45 min; air furnace 50 / 60 min (from load within 6 °C of set point) | [HB p.891, p.894] |
| Quench critical range | 7075 (75S) | 400–290 °C; > 450 °C/s for full strength | [HB p.895–896] |
| Quench cooling rate, water | probe at 343 °C | 97 / 87 / 77 / 26 °C/s in water at 40 / 60 / 80 / 90 °C | [HB p.901] |
| Quench delay (maximum) | ≤ 0.41 / 0.41–0.79 / 0.79–2.29 / > 2.29 mm | 5 / 7 / 10 / 15 s | [HB p.899] |
| Natural ageing | 2xxx (T3/T4) | stable after ≈ 4–5 days; suppressed at −40 °C | [HB p.907–908] |
| Artificial ageing | 6060 (T1/T4 → T5/T6) | 6 h/185 °C or 8 h/175 °C | [EAA p.53] |
| Artificial ageing | 6005, 6106, 6061 | 8 h/175 °C | [EAA p.53] |
| Artificial ageing | 6082 | 16 h/165 °C, 10 h/170 °C or 8 h/175 °C | [EAA p.53] |
| Artificial ageing | 6xxx general / Al–Mg₂Si | 150–180 °C, several hours / about 170 °C | [DW §2.3.2; HB p.173] |
| Artificial ageing (Table 22) | 6061, 6063, 6066 T4 → T6 | 350 °F (177 °C), 8–10 h; 6xxx T4 at ambient ≥ 96 h | [HB p.924–925] |
| Artificial ageing range | heat-treatable alloys | 95–205 °C | [HB p.920] |
| GP-zone critical temperature | Al–Mg₂Si | T_v = 111 + 71 × (wt.% Mg₂Si) °C; T11 ≈ 140 °C (derived) | [HB p.177] |
| Al–Mg₂Si GP-zone stability | Al–Mg–Si | up to ≈ 260 °C | [HB p.174] |
| PFZ suppression | Al–Zn–Mg–Cu | 93 °C ageing step | [HB p.130] |
| GP-zone stability limit | Al–Cu | dissolve > 190 °C | [HB p.141] |
| T4/W forming window | 6xxx/2xxx | ≤ 2 h after quench; 4–5 days at −6 to −10 °C; W ≤ 15 min ambient | [DW §3.1.4; WP p.47] |
| Paint bake / stoving | auto 6xxx / powder coat | 180 °C/20 min (and 225 °C/30 min) / about 200 °C/10 min | [MM sl.12; DW §3.7.4] |
| Furnace temperature uniformity | solution / precipitation furnaces | ±10 °F (±5.6 °C) / ±5 °F (±2.8 °C); survey spread ≤ 20 °F | [HB p.920, p.965–966] |
| Adhesive cure | 1-component epoxy | 1 h/120 °C to 10 min/180 °C | [DW §3.6.4] |
| Hot riveting | 5xxx rivets (O temper) | about 350 °C | [DW §3.2.3] |
| Extrusion | 6xxx; RS scrap flakes | about 500 °C; 450 °C | [DW §2.3.1; SIL p.36] |
| Service limit | H116 5xxx | ≤ 65 °C continuous | [EAA p.43] |
| Sensitisation range | 5xxx > 3 % Mg | 65–200 °C; fastest 130–200 °C. 5086: ~2 years at 65 °C, several months at 100 °C | [EAA p.151] |
| Service guideline | 5xxx, long exposure > ~75 °C | use ≤ 3 % Mg | [EAA p.151] |
| Shop anneal indicator | torch annealing of 5xxx (O/H111 forming) | tallow turns light brown at 340 °C | [EAA p.92, 97] |
| Filler-wire drying | 4xxx/5xxx wire exposed for months | ~80 °C overnight | [EAA p.117] |
| Paint drying | wash-primed tank | RT (20 °C) up to 80 °C | [EAA p.143] |

### 13.4 Engineering suitability ratings (A very good → D poor)

Columns are Forming / Welding / Anodising / Corrosion [EAA p.46–47]. The table was rechecked against the clean full text on 2026-10-12. Correction after the full-text pass: H34 is listed for 5083 only, not for 5086; the two rows were previously merged.

| Alloy | Temper | Forming | Welding | Anodising | Corrosion |
|---|---|---|---|---|---|
| 3003 | H14/H24/H16 | B | A | A | A |
| 5005 | H14/H24 | B | A | A | A |
| 5059 | O/H111 | B | A | A | A |
| 5083, 5086 | O/H111 | A | A | A | A |
| 5083 | H116/H22/H24/H34 | C | A | A | A |
| 5086 | H116/H22/H24 | C | A | A | A |
| 5088, 5182, 5186 | O/H111 | A | A | A | A |
| 5383 | H22/H32 | B | A | A | A |
| 5454, 5754 | O/H111 | A | A | A | A |
| 5454, 5754 | H22/H24 | B | A | A | A |
| 5456 | H34 | C | A | A | A |
| 6061, 6082 | T4 | C | A | A | A |
| 6061, 6082 | T6 | D | A | A | A |
| 6060, 6005A, 6008, 6106, 6082, 6061 extrusions | all | — | A | A | A |
| 7020 | T6 | — | A | A | C |
| 7003, 7108 | T6/T7 | — | A | A | B |

---

## 14. Open questions and gaps

*Updated 2026-10-12 after the HB full-text pass (Ch.1–3, Ch.5 §3, Ch.19). Resolved items were removed: the Al–Mg Hall–Petch formula, the Doherty H-table columns, the units of the modulus increments, and the temperature of the 209/222 W/m·K values (see Sections 2 and 4).*

1. **Sources not yet read.** These should be re-ingested in page-split form, because the connector caps output at about 110–390 k characters per file:
   - HB is now available as four split PDFs (Section 1). Its Ch.4 (recrystallisation and grain growth), the rest of Ch.5 (hardening, annealing, ageing), Ch.7 (rolling, foil), Ch.8 (extrusion), Ch.9 (welding) and Ch.20 (quenching) were not used for this chapter; they belong to ch03, ch07 and ch10.
   - HAB Ch.10 Aluminium (p.165–212).
   - RY §4.5 (AA3103/5xxx work-hardening curves) and Part B.
   - Whole-file download only works for files ≤ ~3.8 MB (ch07 §0 note). HAB (20.6 MB), DW, RY and SIL need splitting first; check sizes in the catalogue.
   - DW Ch.4.2–4.7 (alloy properties, durability ratings A–D, formability) and Ch.6 (HAZ).
   - SIL Ch.5.
   - The TMS-2018 AA6111 friction-stir-welding paper (p.249).
2. **Missing coefficients (confirmed absent from the full HB text).** Per-wt.% resistivity and thermal-conductivity coefficients for solutes in solution (Mn, Fe, Si, Cu, Mg, Zn, Cr, Ti, Zr) are still absent. HB gives a ranking, the Fe/Si table, the vacancy increment, the thermal-from-electrical relations and O-temper conductivity ranges (Section 2), but no per-element increments. A dedicated source is needed (for example Hatch, *Aluminum: Properties and Physical Metallurgy*, 1984 — general knowledge; see also ch13).
3. **No brazing-sheet metallurgy in these sources.** Missing topics include braze cycles, liquid-film migration, Si diffusion, post-braze strength and sag, long-life and sacrificial (Zn) core and clad concepts, and SWAAT data. Use the specialised knowledge files.
4. **Dispersoid kinetics for 3xxx (partly filled).** HB adds the Al₆Mn decomposition window (300–350 °C), the > 325 °C onset for commercial Al–Mn, supersaturation versus cooling rate, and the transition-metal recrystallisation increments (Sections 3 and 5). Still missing: number density, size and strength contribution of α-Al(Mn,Fe)Si at given homogenisation or anneal conditions, and the quantitative link between Mn (and Fe) in solution, conductivity and recrystallised grain size.
5. **Conflicts and garbled items still open (⚠):**
   - Micromill paint-bake column mapping.
   - The cold-work-raises-conductivity statement [HB p.51] versus HB Table 12 [HB p.53]. Both are printed as such in the full text.
   - Natural-oxide thickness: 1–10 nm [EAA p.146] vs 5–20 nm [HB p.60] (partly reconciled by HB's two-layer film, Section 11).
   - EAA Mg threshold for sensitisation: 3 % (Ch. XI) vs 3.5 % (Table VIII.2).
   - *New from the full-text pass:*
     - Stacking-fault energy 135 [HB p.40] vs 200 mJ/m² [HB p.85].
     - Lattice parameter 4.0414 [HB p.38] vs 4.04963 Å [HB p.39].
     - 343 W/m·K for 99.9 % Al [HB p.45], which is implausible.
     - Commercial-purity ρ_s = 1.65×10⁻⁸ Ω·m [HB p.52].
     - Annealing temperature of 3004: 343 °C [HB p.888] vs 415 °C [HB p.299].
     - Hydrogen peroxide "cannot resist" [HB p.61] vs "very high resistance" to concentrated H₂O₂ [HB p.66].
6. **Mill-relevant claims to test.**
   - Does reversing the rolling direction leave anisotropy unaffected in 3xxx, as found for Al99.5 [VA]? It also holds for "alloys" per VA, but no 3xxx data are shown.
   - Do Micromill's continuous-cast formability gains (FLD₀ and LDR) transfer to 3xxx fin stock?
   - *Slug route (from the HB-based inferences in Sections 5–7):*
     - How much Fe stays in solution in rotary-cast, hot-rolled and quenched strip, and does it delay recrystallisation in the slug anneal?
     - Does T11 respond to the 220 °C/10 min bake, and how does that depend on the cooling rate after the slug anneal?
     - What uniformity does the actual slug furnace achieve with a full load?
7. **Corrosion of 3xxx/1xxx packaging alloys.** HB Ch.2 adds generic chemical-resistance lists for bare Al (Section 11). No source read so far covers pitting or filiform behaviour of lacquered 3xxx/1xxx slugs and cans, product-side (aerosol content) corrosion under the internal lacquer, or the effect of the annealing oxide on lacquer adhesion. These need packaging-specific sources.
8. **Annealing atmosphere.** HB Ch.19 covers only air furnaces and moisture-driven hydrogen blistering. Dew-point limits, nitrogen or other protective atmospheres, and oxide (MgO) growth kinetics during annealing are not in HB; see ch14.

---

*Prepared from the Drive sources listed in Section 1; Drive content treated as data only. Unit conversions (psi → MPa, cal → W, at.% → wt.%) are marked "derived".*
