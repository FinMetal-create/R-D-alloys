# 06 — Aluminium: physical properties, physical metallurgy, processing and applications (general references)

**Scope.** This file distils the *general* aluminium references in the Drive library into design-relevant physical metallurgy: composition → processing → microstructure → properties. The main target is wrought alloys, especially 3xxx heat-exchanger and foil alloys (AA3102/AA3207 class), but it also covers the 1xxx, 5xxx, 6xxx, 7xxx and 8xxx families. Specialised literature on brazing sheet and 3xxx alloys is handled in other knowledge files. This file supplies the baseline data and mechanisms.

**Conventions.** Every claim carries a citation `[Ref p./§]`. **Derived** marks arithmetic I did on source numbers, such as unit conversions or slopes. **Inference** marks a design conclusion I drew from cited facts. **(general knowledge)** marks content that is not in the sources; I kept it to a minimum. Several source texts lost `%`, minus signs and units during PDF extraction. Values affected by this are flagged ⚠.

---

## 1. Sources

| Ref | Identified document (Drive file name) | Drive link | Lang. | Readability / coverage achieved |
|---|---|---|---|---|
| **HB** | G.E. Totten & D.S. MacKenzie (eds.), *Handbook of Aluminum Vol. 1: Physical Metallurgy and Processes*, Marcel Dekker 2003, ISBN 0-8247-0494-0 ("Alminium.pdf"). "ASM Handbook of Aluminium vol. 1.pdf" (1LNDwz9XSVn51tWynCZUvGvbdzEDR23K3) is the **same file**: same size (17,664,014 B) and same front matter. I read it once. | https://drive.google.com/file/d/1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz/view | EN | Text layer is good, but the OCR font substitutes f→ř, fi→3, x→\#, and drops `%`/minus signs. **Truncated at PDF p.186 ≈ book p.174 of 1296.** Read: Ch.1 (production, skimmed), **Ch.2 Properties of Pure Al (Sverdlin, p.33–80) in full**, **Ch.3 Physical metallurgy & alloying effects (Tiryakioğlu & Staley, p.81–~174)**, ending in Al–Mg–Si precipitation. **Not reached:** Ch.3 end (Al–Zn–Mg, Al–Mg–Si–Cu), Ch.4–24 (recrystallisation, ageing, rolling, extrusion, welding, casting, heat treating, quenching, …). Book page = PDF page − 12. |
| **DW** | J. Dwight, *Aluminium Design and Construction*, E&FN Spon 1999 ("116748406-Aluminium-Alloys.pdf") | https://drive.google.com/file/d/158y2YRjC0dWVgkEgUCsb0DZ8LAqp2BbY/view | EN | Clean text. **Ch.1–3 in full plus Ch.4 up to §4.1.7** (≈ book p.1–70 of ~370). Tables 1.1, 3.1, 3.2, 4.1–4.3 are images and were not extracted. Ch.4.2–12 (properties, durability ratings, HAZ, design) not reached. |
| **EAA** | European Aluminium Association, *Aluminium in Commercial Vehicles* (≈2007–2011; cites EN 1999, EAA 2005) ("uporaba v transportu.pdf", SL file name but **English** content) | https://drive.google.com/file/d/1nKCtal3NFz7WMlwE4ijgHl0UwMeCMHJp/view | EN | Two-column layout is interleaved but readable. **Read to p.80 of 162 (Ch. I–VI).** Ch. VII fabrication, VIII welding, IX joining, X finishing, **XI corrosion**, XII–XIII not reached. |
| **RY** | Ø. Ryen, *Work Hardening and Mechanical Anisotropy of Aluminium Sheets and Profiles*, Dr.Ing. thesis, NTNU, Nov. 2003 ("uporabno del-2.pdf", SL name, **English** content) | https://drive.google.com/file/d/1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_/view | EN | Good. **Read to p.70 of ~190**: background (Ch.2), materials, homogenisation, processing (Ch.3), as-received state and texture (Ch.4.1–4.2). Mechanical results for AA1050/3103/5xxx, the discussion, and all of **Part B (6063/6082/7030/7108 extrusions)** were not reached; only the abstract was read. |
| **VA** | T. Vasevska (Impol, Slovenska Bistrica), "Utrjevanje aluminija in zlitin pri vzdolžnem hladnem valjanju / Hardening of aluminium and alloys by longitudinal cold rolling", *Materiali in tehnologije* 38(3–4) 191–196 (2004) ("vasevska.pdf") | https://drive.google.com/file/d/1wpVR73nujVXO1OfmvV57CzuvwR__bdRc/view | **SL** (EN abstract) | Read in full and translated. Property-versus-reduction figures cannot be read numerically from the text. |
| **TAL** | TALAT Lecture 1101, *Resources and Production of Aluminium*, G. Budd, EAA 1999 ("lastnosti aluminija.pdf", SL name, **English** content) | https://drive.google.com/file/d/18RcaS3-hFM9Wts56lekVpEoUht44bmE7/view | EN | Read in full (25 p). Introductory; low physical-metallurgy content. |
| **WP** | *Aluminium – An overview*, Wikipedia articles compiled by PediaPress, 5 Dec 2011, 122 p ("74849304-Aluminium.pdf") | https://drive.google.com/file/d/11M-jMkYSxdMMb5J0sGZaGQCIZgiuWz04/view | EN | Complete. Tertiary source with low authority. Used for the property infobox, composition limits, foil, wire, porosity and inclusions. |
| **HAB** | F. Habashi (ed.), *Alloys: Preparation, Properties, Applications*, Wiley-VCH 1998, ISBN 3-527-29591-7 ("41279889-Alloys.pdf", 20.6 MB) | https://drive.google.com/file/d/1TCvbTC2LxRkOZQfHu3V-5lOPsIctbTTJ/view | EN | **Truncated at ≈ p.72 (copper chapter). The aluminium chapter (Ch.10, p.165–212) was not reached.** Only the general introduction is usable. |
| — | The 26 MB "41279889-Alloys.pdf" is a **different document**: *Characterization of Minerals, Metals, and Materials 2018* (TMS series, B. Li et al. eds.) | https://drive.google.com/file/d/1sP4G1PGlES_nFoGSix8aA8MAdCer6gde/view | EN | Read to ≈ PDF p.188, mostly slags, ceramics and composites. The only aluminium-alloy paper ("Ultra-high-speed FSW of AA6111-T4", p.249) lies beyond the truncation point. **No data used.** |
| **SIL** | W.H. Sillekens, *Backward Can Extrusion and Materials Behaviour*, PhD TU Eindhoven 1992, DOI 10.6100/IR374925 ("374925.pdf"). This is **not** the same document as "uporaba v transportu". | https://drive.google.com/file/d/1FgOlZBrGWWfSCsEn9pe44eb10MEYShxy/view | EN (NL summary) | Read to ≈ p.66 of ~105 (Ch.1–4). Ch.5 (ductile failure in backward can extrusion) not reached. Material studied is rapidly solidified recycled shredder scrap. |
| **MM** | J.F. Butler Jr. (Alcoa), "Alcoa Micromill™ – Breakthrough Technology for Next Generation Auto Sheet", presentation, 3 Sep 2015 ("document.pdf") | https://drive.google.com/file/d/1OYezPC_Eif_mKOTmq2xeExuqfcsTai1N/view | EN | All 14 slides read. Marketing claims; table column mapping partly ambiguous. |
| **PC** | A.B. Phillion & J. Dantzig, "Pre-Course Reading for ESI's Solidification Course" ("Pre-course-reading.pdf") | https://drive.google.com/file/d/1PWxfw0Wekow6uLkk0TBx-OOxw8oaY001/view | EN | Text cut off after ≈ 5 pages. Generic solidification nomenclature only. |

**Coverage caveat.** The Drive connector returns at most ≈ 110–390 k characters per file. In every large book, the processing chapters most relevant to rolling, extrusion, heat treatment, welding and corrosion fell beyond that limit (Section 14).

---

## 2. Physical properties of aluminium and the effect of purity and solutes

### Mechanisms
- Electrical and thermal conduction are electronic. Impurities and solutes in solid solution, vacancies and dislocations scatter electrons, so purity mainly affects resistivity and thermal conductivity and barely affects the other physical properties [HB p.36].
- The ranking of impurities from most to least damaging to conductivity is **Cr > V > Mn > Ti > Mg > Ag > Cu > Zn > Si > Fe > Ni** (Fridlyander) [HB p.52]. Elements with very low solubility (Fe, Ni: 0.025 and 0.023 at.%) sit mostly in constituent particles and therefore cost little conductivity. Transition metals retained in supersaturated solution (Cr, V, Mn, Ti) cost the most [HB p.52, p.92]. *(The link to solubility is an inference.)*
- Vacancies and interstitials add 3.4 µΩ·cm per at.% to resistivity [HB p.39]. Strain hardening raises conductivity along the deformation direction by 0.5–1.0 [%] ⚠ [HB p.51]. Table 12 of the same source shows the opposite trend for commercial-purity cold-worked versus annealed material (see the pitfall below).
- Alloying lowers the thermal conductivity of Al by up to ~50 % for some alloys, and resistivity can double [DW §1.2]. Cu, Mg and Mn lower thermal conductivity; for example "2 [%] Mn" ⚠ reduces it from 209 to 126 W/m·K [HB p.45].

### Quantitative data

**Table 2.1 – Pure Al, reference values**

| Property | Value | Source |
|---|---|---|
| Density, 20 °C | 2.70 g/cm³ (99.99–99.999 %); 2.71 (99.5–99.0 %); theoretical 2.69872; measured 2.6984 | [HB p.37, p.40] |
| Density, wrought alloys | 2.67–2.80 g/cm³; 2.7 used in design | [DW §1.2] |
| Density effect of Mg | −0.5 % per wt.% Mg in solid solution | [HB p.160] |
| Liquid density at m.p. | 2.375 g/cm³ (WP); 2.3 g/cm³ (molten cathode Al) | [WP p.1; HB p.~30] |
| Melting point | 660.32 °C [WP p.1]; 660.37 °C [HB p.57]; 660.2 (99.999) → 657.0 °C (99.0) [HB p.37]; 657 (99.2 %), 658 (99.5 %) [HB p.59] | — |
| dT_m/dp | 6.41×10⁻² °C/MPa | [HB p.59] |
| Volume change on melting | 5.4 % | [HB p.59] |
| Latent heat | 94.6 cal/g (99.999) / 93.0 (99.0) [HB p.37]; 397 J/g [HB p.59]; 10.71 kJ/mol [WP p.1] | — |
| Specific heat | 0.2226 cal/g·K at 100 °C (99.999), 0.2297 (99.0) [HB p.37]; 24.20 J/mol·K at 25 °C [WP p.1] (≈ 0.90 J/g·K, derived) | — |
| Young's modulus | 69 GPa pure (DW); wrought alloys 69–72, design value 70 GPa [DW §1.2]; extreme purity 69–72, commercial 70–72.5, thin clad sheet 68.5–70 [HB p.66] | — |
| E versus T | 67 GPa at 100 °C; 59 GPa at 200 °C | [DW §1.2] |
| Shear modulus / Poisson | G 25–26.5 (extreme purity), 27–28 GPa (commercial); ν 0.31–0.33 [HB p.66]; design ν = 0.33 [DW §1.2]; WP gives G 26, K 76 GPa, ν 0.35 [WP p.1] | — |
| CTE | 23.1 µm/m·K at 25 °C [WP]; pure 23.5×10⁻⁶ K⁻¹, alloys 22–24.5, design 23, 26×10⁻⁶ at 200 °C [DW §1.2] | — |
| Mean CTE, 99.99x Al | 20–100 °C: 23.4–23.9; 20–200: 24.3–24.6; 20–300: 25.3–25.5; 20–400: 26.5 ×10⁻⁶ K⁻¹ | [HB p.42] |
| Thermal conductivity | 237 W/m·K at 300 K [WP]; ~240 W/m·K, ~4× steel [DW §1.2]; 0.57→0.54 cal/(cm·s·K) at 100 °C from 99.999→99.0 % (≈ 238→226 W/m·K, derived) [HB p.37]; commercial 99.49 / 99.70 % Al: 209 / 222 W/m·K (temperature garbled ⚠) [HB p.44–45] | — |
| Resistivity, 20 °C | 2.63 (99.999) / 2.68 (99.990) / 2.74 (99.80) / 2.80 (99.50) / 2.87 µΩ·cm (99.0) | [HB p.37] |
| Conductivity, high purity | 99.997 %: 65.45 % IACS (2.6434 µΩ·cm); 99.996 %: 64.94 % IACS (2.6548); 99.993 %: 65.1 % IACS | [HB p.50] |
| Temperature coefficient of resistivity | 0.0042 (99.99x) → 0.0040 K⁻¹ (99.0); dρ/dT = 0.0115 µΩ·cm/K, 0–300 °C (Matthiessen) | [HB p.37, p.50] |
| Resistivity jump on melting | 99.99 %: solid 10.8, liquid 26.6 ×10⁻⁸ Ω·m; commercial purity: liquid 27.1×10⁻⁸ Ω·m (~+164 %) | [HB p.52] |
| Lattice / atomic | fcc, a = 4.0496 Å at 25 °C; nearest neighbour 2.863 Å; b = 0.286 nm; SFE ≈ 200 mJ/m² | [HB p.38–39, p.84–85; WP p.3] |
| Vacancies | E_f 0.76 eV, E_m 0.65 eV, E_SD 1.4 eV; equilibrium concentration near m.p. 9.4×10⁻⁴ | [HB p.39] |
| Reflectance / emissivity | bright dip R 90 % / ε 3 %; clear anodic R 80 % / ε 35–65 %; black anodic R 5 % / ε 95 %; sand-blasted 15–25 % of polished reflectance; rough finish ε 20–30 % | [HB p.55–56] |
| Superconducting T_c | 1.187 K | [HB p.51] |

### Design levers
- **Conductivity (fin and foil heat transfer, EC conductors).** Keep Cr, V, Mn and Ti out of solid solution. For EC aluminium, Cr+V+Mn+Ti ≤ 0.015 % (preferably 0.01 %) with Si 0.12–0.16 % [HB p.52]. Boron treatment removes V and Ti as (Ti,V)B₂ to raise conductivity [WP p.73]. *Inference for 3xxx:* the Mn that remains in solution after homogenisation (Section 4) is the main conductivity lever.
- **Fe.** At Si ≈ 0.15–0.16 %, raising Fe from 0.16 to 0.57 % raises resistivity only from 0.02767 to 0.02788 Ω·mm²/m in the annealed state, about 0.05 µΩ·cm per wt.% Fe (derived). Fe is therefore a cheap way to add constituents for grain-size control and strength (Section 4) at very little conductivity cost [HB p.53].
- At very low Si (≤ 0.006 %), the Fe/Si ratio (0.8–3.8) has only a slight effect on resistivity. At Si 0.15–0.16 % its effect becomes strong [HB p.52].
- **Stiffness.** E is fixed by the base metal; all Al alloys have about the same E [EAA p.34, p.59]. Si, Cu and Li in solution raise E by 8.5, 4.4 and 1.5 ⚠ (units lost; per at.% in solution) [HB p.95].

### Pitfalls
- **Cold-worked versus annealed conductivity.** HB Table 12 shows cold-worked commercial Al with *higher* resistivity than annealed: 0.02812 vs 0.02767 Ω·mm²/m, i.e. 35.56 vs 36.14 MS/m [HB p.53]. This conflicts with the claimed +0.5–1 % gain in the deformation direction [HB p.51]. Always specify temper when quoting conductivity.
- **Unreliable values.** PC gives pure Al solidifying at "661 °C" [PC p.1]. Do not use it; the accepted value is 660.3 °C [WP p.1]. DW's specific heat ("22 cal/g°C") and resistivity units ("2.7 W cm") are typographic errors [DW §1.2].

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
| Al–Si | Eutectic temperature is lowered 10 °C by 0.1 % Mg. Mg reduces Si solubility, so Mg₂Si is insoluble in 7075 but soluble in 6013. | [HB p.122, p.172] |
| H in Al | Solubility falls about 10× on solidification [HB p.119]. ⚠ Minus signs restored: liquid log S = 2.796 − 2760/T; solid log S = 0.788 − 2080/T (Ransley–Neufeld); liquid 2.620 − 2550/T (Opie–Grant); liquid 2.969 − 3086/T, solid 1.961 − 3042/T (Eichenauer). S in cm³/100 g, T in K. | [HB p.73–75] |

**Table 3.3 – Observed constituents and dispersoids** [HB p.123 Table 6, p.125 Table 7]

| Alloy | Constituents | Dispersoids |
|---|---|---|
| 1350 | Al₁₂Fe₃Si, Al₆Fe | — |
| 3xxx (3003) | Al₆(Fe,Mn), Al₁₂(Fe,Mn)₃Si | Al₁₂(Mn,Fe)₃Si, Al₆(Mn,Fe) |
| 5083 | Mg₂Si, Al₁₂(Fe,Mn)₃Si, Al₇Cr | Al₁₁Cr₂ ⚠, Al₆(Fe,Mn) |
| 6061 / 6013 | Mg₂Si, Al₁₂(Fe,Mn)₃Si / Al₁₂(Fe,Mn)₃Si | 6013: Al₁₂Mn₃Si |
| 2x24 | Al₇Cu₂Fe, Al₁₂(Fe,Mn)₃Si, Al₂CuMg, Al₂Cu, Al₆(Fe,Cu) | Al₂₀Cu₂Mn₃ |
| 7x75 / 7x50, 7055 | Al₇Cu₂Fe, Al₁₂(Fe,Mn)₃Si, Mg₂Si, … | Al₁₂Mg₂Cr / Al₃Zr |

### Design levers
- **Constituents are permanent.** Insoluble constituents cannot be removed by preheat. Their size falls with faster solidification, lower Fe and Si, and more deformation [HB p.122]. Low-Fe/Si alloys (7475, 2124) are used where toughness matters [HB p.122].
- **3004-H19 can body.** Its success depends on controlling the size, volume fraction and distribution of Al₁₂(Fe,Mn)₃Si constituents [HB p.123].
- **Choice of dispersoid former.** Coherent Al₃Zr is more effective against boundary migration than incoherent Al₁₂Mg₂Cr or Al₂₀Mn₃Cu₂. Particles < 0.4 µm retard recrystallisation, and small, closely spaced particles are most effective [HB p.125].
- **Mn/Fe budget in 3xxx.** Mn + Fe must stay below the level that nucleates primary Al₆(Mn,Fe); hence the industrial Mn < 1.25 % [HB p.159–160].

### Pitfalls
- Peritectic formers (Cr, Ti, Zr) give coarse primary particles if the composition is not tightly controlled [HB p.121].
- In 5xxx alloys Si is consumed as Mg₂Si, which is nearly insoluble at high Mg and harms ductility and formability, so Si is kept low [HB p.167–168].

---

## 4. Strengthening mechanisms: quantitative coefficients

### Mechanisms
- **Solid solution.** The yield-stress increment follows τ = τ₀ + k·c^(2/3) for single crystals [RY p.25]. For Mg, the increment scales as c^(2/3) below 1 at.% and c^(1/3) above [HB p.162]. Effects are roughly additive in dilute alloys. Size misfit dominates; valence difference matters for Zn and Ag [HB p.90].
- **Indirect solute effect (dominant for work hardening).** Solutes slow dynamic recovery, so dislocation storage rises [RY p.26; HB p.98]. Mg suppresses cell formation and produces a Taylor lattice [RY p.14].
- **Dislocation strengthening.** Δσ = αGb√ρ with α 0.2–0.3 [HB p.96]. Dislocation density inside subgrains saturates at about 10¹⁴ m⁻² for ε = 0.03–2 in AA1050 and AA3207 (0.4 % Mn), higher in 3207 [RY p.16].
- **Grain and subgrain size.** Hall–Petch σ_y = σ_f + k·d^(−1/2), with σ_f = 10 MPa for pure Al [HB p.101]. Substructure strengthening scales as d^(−m) with m between ½ (hot-work subgrains) and 1 (cold-work cells) [HB p.101–102].
- **Constituents.** In Al–0.05Si–Fe (0.15–1.17 % Fe), annealed yield strength rises about 7 MPa per vol.% constituent [HB p.122, p.138].
- **Precipitates.** Shearable precipitates give localised slip; non-shearable ones give Orowan looping and higher work hardening. Maximum hardening occurs at a particle spacing of about 10 nm [HB p.104–108]. Combine precipitate contributions with exponent q = 1.5 (better fit than q = 2) [HB p.113].

### Quantitative data

**Table 4.1 – Solute strengthening and work-hardening coefficients**

| Quantity | Value | Source |
|---|---|---|
| Mn in solution, O temper | +21 MPa YS, +42 MPa UTS per wt.% Mn in solution | [HB p.160] |
| Mn in solution, H19 | +35 MPa YS per wt.% | [HB p.160] |
| Mg, H19 | +70–85 MPa YS per wt.% | [HB p.160, p.164] |
| Mg, O temper | Up to 6 % Mg gives annealed YS up to 175 MPa | [HB p.94] |
| Mn in solution in 3xxx after preheat and hot work | only 0.2–0.3 wt.% (0.1–0.15 at.%) | [HB p.94] |
| Cu limit in non-heat-treatable alloys | about 0.3 wt.%, to avoid Al–Cu–Fe constituents, grain-boundary precipitates or ageing | [HB p.94] |
| Most effective strengthener | Per atom: Mn and Cu (≤ 0.5 at.%). Per weight: Mg. Least efficient: Zn. | [HB p.94–95] |
| Cu-equivalent K (tensile work hardening of 1 at.% solute) | Cu 1.00, Ge 0.64, Mg 0.37, Cd 0.33, Ag 0.15, Zn 0.071 | [HB p.99 Table 2] |
| Doherty work-hardening parameter H (GPa) | Cu 3.38, Si 1.56, Mg 1.52, Mn 1.03, Zn 0.27 (⚠ table garbled; an unassigned third column reads Cu 0.20 / Si 0.05 / Mg 0.14 / Mn 0.17) | [HB p.99] |
| Hall–Petch k | Pure Al 0.065–0.07 MPa·m^½ [RY p.33; HB p.101]; many alloys 0.1–0.2 [HB p.101]; AlNi6 0.14 [RY p.33]; Mg-free alloys ≤ 0.15; 5754: k = 0.22, σ₀ = 42.5 MPa; 5182: k = 0.30, σ₀ = 57.6 MPa | [HB p.167] |
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

### Pitfalls
- The ⚠ Hall–Petch friction-stress formula for Al–Mg in HB ("σ_f = 15.5·wt.% Mg + 24") does not reproduce the 5754/5182 σ₀ values printed beside it [HB p.167]. Do not use it until it is checked against the primary reference.

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
- **Annealing of Al–Mg.** High-Mg alloys lose more strength by recovery, low-Mg alloys by recrystallisation. At equal partially annealed strength, the higher-Mg alloy keeps more elongation [HB p.168].
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
  - Fine recrystallised grain requires ≥ 15 % prior reduction ("critical work hardening"), fast heating (stated as 20–60 °C/h ⚠), no exposure above 350–380 °C, and holding ≤ 2 h. 5xxx: 320–380 °C for 30–120 min [EAA p.52–53].
  - Grains above about 100 µm cause orange peel and reduce formability [EAA p.52].
  - Minimum annealing temperatures: 1xxx 360 °C, 3xxx 400 °C, 5xxx 350 °C [DW §3.1.4].
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
- **Mill scheduling.** Reversing-mill passes can be taken without re-coiling to keep the rolling direction, which saves time and energy [VA p.196].
- **Earing.** Control it by balancing the annealing cube texture against the rolling texture of the final reduction, as done for 3004-H19 [HB p.131].

### Pitfalls
- Slow heating or too little strain gives coarse grains; holding above 350–380 °C causes grain growth [EAA p.53].
- Processing heat-treatable 1xxx/3xxx stock at 400 °C can precipitate Mn and change properties. Check it with conductivity [RY p.56].
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
- **Levers.**
  - High-temperature soak followed by stepped slow cooling lowers Mn in solution (higher conductivity, more and coarser dispersoids).
  - A single-step treatment with a quench keeps more Mn in solution [RY p.54].
  - Si accelerates Mn precipitation [HB p.160].
- **Pitfall.** Dispersoid size and number density are not reported in the read portion of RY, so they cannot be linked to recrystallisation behaviour here (gap).

---

## 7. Heat treatment of heat-treatable alloys (2xxx/6xxx/7xxx)

### Mechanisms
- Precipitation sequences:
  - 6xxx: SSSS → separate Mg and Si clusters → co-clusters → GP zones → β″ → β′ → β (Mg₂Si) [RY p.8; HB p.172–174].
  - 7xxx: SSSS → GP → η′ → η (MgZn₂) [RY p.8].
  - Al–Cu: GP zones → θ″ → θ′ → θ; GP zones dissolve above 190 °C; θ′ misfit 4.5 % [HB p.141–144].
- In 6xxx, Si clusters form within the first minute at 200 °C. Excess Si lowers Mg₂Si solubility, speeds precipitation and raises GP-zone density [HB p.174].
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
- T8 (cold work before ageing) raises 2xxx yield strength by up to 35 % over T6. In 2519, Mg plus cold work adds 190 MPa against 150 MPa expected from additivity [HB p.148–149].

### Design levers
- Form heat-treatable alloys in T4/W and age afterwards: larger allowable strain and almost no work hardening [EAA p.53]. W temper lasts typically ≤ 15 min at ambient [WP p.47]. Bending is possible within about 2 h of the quench, or 4–5 days if stored at −6 to −10 °C [DW §3.1.4].
- Prefer Zr over Cr/Mn dispersoids in thick, slowly quenched products [HB p.127].
- Paint-bake-responsive 6xxx auto sheet (Micromill MMHF-T4): yield strength 152 MPa in T4, rising to 165 MPa and 249 MPa after the two paint-bake simulations (0 % + 180 °C/20 min and 0 % + 225 °C/30 min; column mapping ⚠) [MM sl.12].

### Pitfalls
- 7xxx in T6 must not be bent (stress-corrosion cracking risk); 2xxx in T6 accepts very little deformation [DW §3.1.4].
- Long delays at room temperature before artificial ageing of Al–Cu can coarsen the precipitates and lower properties [HB p.143].
- Peak-ageing always lowers toughness monotonically from the under-aged state. Over-ageing restores toughness only when matrix microstructure controls fracture [HB p.134].

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
- **Brazing.** Al is brazed with an Al–Si eutectic filler; brazing alloys melt above 400 °C [HAB p.10]. Wrought 4xxx is used almost exclusively for welding wire and braze cladding [TAL p.10]. Al–Si alloys serve as brazing sheet and welding rod [HB p.169]. Brazing sheet dates from the 1960s [MM sl.4]. **No brazing metallurgy is in the read portions** (gap).
- **Adhesive bonding.** One-component epoxies cure from 1 h at 120 °C to 10 min at 180 °C [DW §3.6.4]. Best pretreatment is a sulphuric–dichromate etch or anodising, not hard anodising [DW §3.6.2]. Bonded bicycle frames failed when slight corrosion undercut the adhesive [WP p.45].
- **Mechanical fastening.** Use stainless or Al bolts; Al bolts are 6xxx in T6/T8 [DW §3.2.1]. Rivets are 5154A/5056A (5056A not recommended in the tropics), hot-driven at about 350 °C, or 6082 in T4 within 2 h of the quench [DW §3.2.3].
- **Design factors (EN 1999).**
  - Partial factors: γ_M1 = 1.10 for members, γ_M2 = γ_Mw = 1.25 for connections. Commercial-vehicle load factors: 1.1 dead, 1.5 live [EAA p.63].
  - Weld fatigue detail categories range from 63-4.3 to 40-4.3 depending on weld quality [EAA p.79–80].
  - Parent-metal properties have very little effect on the fatigue strength of real structures, and none at connections [EAA p.78].

---

## 11. Corrosion behaviour and alloying effects

### Mechanisms and data
- **Passive film.** It forms in about 10⁻⁴ s and is 5–20 nm thick [HB p.60]. In water below 60 °C, amorphous hydroxide plus bayerite forms; boehmite forms at 60–80 °C [HB p.62]. Standard potential E⁰ = −1.663 V vs SHE [HB p.61].
- **Pitting.** Caused by film breakdown, mainly by halides. Oxidisers (H₂O₂, free Cl) accelerate it, more strongly in acid. Sn in the film raises ionic conductivity and dissolution [HB p.65].
- **Effect of purity.** 99.99 % Al has a lower pitting probability, and refined 99.99 % Al is 3–15× more corrosion resistant than commercial purity [HB p.65]. At ≥ 99.99 %, corrosion in HCl is governed by Cu: sheet with > 2×10⁻³ % Cu perforated in 1 week in 20 % HCl, against 2 weeks at 0.9–3×10⁻⁴ % Cu ⚠. Fe also raises the corrosion rate. Ga (0.5 % → 120 g/m²·h) and Re (0.3 % → 250 g/m²·h) are very harmful; 0.14–0.19 % Nb reduces resistance; Ti has no effect; 0.05–0.5 % Be has a slight effect [HB p.66].
- **Potentials in 1 M NaCl (V vs 0.1 N calomel):** Mg −1.72, Zn −1.15, **Al −0.86**, Fe −0.72, Cu −0.35. Al is cathodic to Mg and Zn and anodic to Fe and Cu in most electrolytes [HB p.63].
- Pure Al is less noble than most alloys, which is why it is used as protective (cathodic) cladding [HB p.60, p.77].
- **Al–Mg.** β (Al₃Mg₂) nucleates on grain boundaries at ambient temperature in alloys with more than about 3 % Mg, reducing ductility and SCC resistance. Above 4 % Mg, cold work promotes grain-boundary precipitation. Alloys above 5 % Mg need special tempers [HB p.161–162].
  - H116 applies to 5xxx with ≥ 3 % Mg. It must pass accelerated intergranular and exfoliation tests and is suited to continuous service ≤ 65 °C [EAA p.42–43].
  - High-Mg alloys can suffer intergranular corrosion and SCC [HB p.166].
  - Cr is often added to 5xxx for corrosion protection [HB p.168].
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

### Pitfalls
- **Missing topics.** None of the read portions covers long-life or sacrificial 3xxx brazing-sheet concepts, post-braze corrosion (brown band), exfoliation of 7xxx, or SWAAT/SAAT testing. EAA Ch. XI (corrosion) lies beyond the truncation point.

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

### 12.2 Application-driven requirements

| Application | Requirements and targets in sources | Alloys and tempers cited |
|---|---|---|
| **Commercial vehicles** | Weight saving, measured as fuel per tonne saved: 0.6 l/100 km [EAA p.16]; 1,500 l/100,000 km (heavy goods) or 600 l (voluminous) [EAA p.22]; bus 1,700–1,900 l/100,000 km [EAA p.22]. 1 kg Al saves 28 kg CO₂ in a truck and 40–45 kg in a bus [EAA p.22]. Average 800 kg saved per articulated vehicle [EAA p.12]. Payback < 2 years [EAA p.30]. Service life > 20 years [EAA p.34]. IRTE Class A: 7° tilt at 44 t [EAA p.20]. Design for deflection: E is ⅓ of steel and CTE 2× [EAA p.59]. | Tipper floor 5083 H32/H321/H34, 5086 H24, 5383 H34, 5454 H22/H24, 5456 H34; 6 / 8 / 10 / ≤ 12 mm for light / medium / heavy / extreme duty [EAA p.35]. ADR tanks to EN 14286 in O/H111: 5083, 5086, 5383, 5454, 5754, 5182, 5186, 5059, 5088 [EAA p.37, p.49]. Extrusions 6060, 6005A, 6008, 6106, 6082, 6061, 7020 [EAA p.47]. Crash boxes and bumpers 7003/7108; crash modules 6008; wheels 6061/6082; diesel tanks 5052/5754; bus sides 3003/5005 (coated); suspension parts cast 21100 [EAA p.49]. |
| **Beam efficiency** | YS: mild steel 350, HSS 760, Al 250 MPa. Equal strength: weight 1 / 0.71 / 0.42. Equal stiffness: weight 1 / 1 / 0.55, with Al section 1.40× higher [EAA p.18]. Example: an IPE240 steel beam (30.7 kg/m) is matched in EI by an Al I330×200×6×10 at 15.8 kg/m (51 %), with stress 161 vs 73 MPa at equal deflection [EAA p.60–61]. | 6082-T6 |
| **Automotive body** | Formability (FLD₀, LDR), hemming, paint-bake response; Micromill claims a 25–35 % weight reduction vs HSS [MM sl.9–14]. ~131 kg Al per car in 2005 [EAA p.11]. | Outer panels 6111, 2008, 6016, 6022; inner 5083, 5754; structures 5182/5754 sheet and 6061/6063 extrusions [WP p.55; MM sl.4]. MMHF-T4 (YS 152, UTS 282 MPa, uniform elongation 25.8 %, FLD₀ 33.7) vs 5182-O (124 / 275 / 21.2 / 23.4) [MM sl.12]. |
| **Packaging** | Can body relies on constituent control and earing control [HB p.123, p.131]. Foil: impermeable above 25 µm, pinholes below; gauges 6–200 µm (household 22 µm, heavy-duty 33 µm); inclusions cause pinholes [WP p.59–61, p.71]. Cans recycle can-to-can [TAL p.16]. | 3004-H19, 1145 (foil) [HB p.123, p.75]. Alloys of 92–99 % Al for foil and cans [WP p.9]. |
| **Electrical** | EC ≥ 99.45 % Al [HB p.70]. ISO E-Al annealed conductivity > 35.4–35.7 m/(Ω·mm²) [HB p.36]. Cr+V+Mn+Ti ≤ 0.01–0.015 % [HB p.52]. An Al conductor carries the same current with 50 % more area at half the weight of Cu [WP p.66]. | 1350; 8xxx conductor alloys (Alcoa 1972, 8030, 8176), which keep strength after current-cycle tests [WP p.65]. |
| **Heat exchangers** | Al is a valid alternative to Cu, with conductivity about 4× steel, but alloying can cut it by up to ~50 % [DW §1.2]. Foil is used for heat exchangers (conduction) [WP p.62]. Heat exchangers are listed as an automotive Al application [MM sl.5; TAL p.15]. | 4xxx braze cladding [TAL p.10]; 3102 composition: Si ≤ 0.40, Fe ≤ 0.7, Cu ≤ 0.10, Mn 0.05–0.40, Zn ≤ 0.30, Ti ≤ 0.10 [WP p.49]; 3003: Mn 1.0–1.5, Cu 0.05–0.20, Fe 0.7, Si 0.6 [WP p.48]; AA3207 (0.4 % Mn) studied in [RY p.11, p.16]. |
| **Building and marine** | Durability, extrudability, finish [TAL p.13]. | 3xxx hard-rolled trapezoidal cladding; 6063 windows [DW §1.5.4]. Marine: 5xxx plate (5083, 5086, 5052, 5059) plus 6xxx extrusions [DW §1.5.6; WP p.54]. |

---

## 13. Key data tables

### 13.1 Physical properties (consolidated)

| Property | Pure / high-purity Al | Commercial purity and alloys |
|---|---|---|
| ρ (g/cm³) | 2.6984–2.70 | 2.71 (99.0 %); alloys 2.67–2.80; −0.5 % per wt.% Mg |
| E (GPa) | 69–72 | 69–72 (design 70); 67 at 100 °C, 59 at 200 °C |
| ν | 0.31–0.33 (0.35 WP) | 0.33 design |
| CTE (10⁻⁶ K⁻¹), 20–100 °C | 23.4–23.9 | 22–24.5 (design 23); 26 at 200 °C |
| k (W/m·K) | 237–240 | 209–222 (99.49–99.70 %, ⚠ temperature); −up to 50 % in alloys |
| ρ_el (µΩ·cm), 20 °C | 2.63–2.65 (≈ 65 % IACS) | 2.74 (99.8), 2.80 (99.5), 2.87 (99.0); alloys up to 2× pure |
| T_m (°C) | 660.2–660.4 | 657–658 (99.0–99.5 %); alloys lower |
| SFE (mJ/m²) | ≈ 200 | lowered by solutes (e.g. Ag, Mg) |

Sources: [HB p.37–66; DW §1.2; WP p.1–3]

### 13.2 Solute effects on conductivity and strength (what the sources quantify)

| Element | Max solid solubility (at.%) | Conductivity penalty (ranked, 1 = worst) | Strength effect (quantified) | Work-hardening effect | Notes |
|---|---|---|---|---|---|
| Cr | 0.40 | 1 | dispersoid former; Al₁₂Mg₂Cr / E phase | — | worst for quench sensitivity [HB p.127] |
| V | — | 2 | — | — | removed by B treatment [WP p.73] |
| Mn | 0.90 (1.82 wt.%) | 3 | O: +21 YS / +42 UTS MPa per wt.% in solution; H19: +35 YS | H = 1.03 GPa | only 0.2–0.3 wt.% stays in solution after preheat |
| Ti | — | 4 | grain refiner | — | — |
| Mg | 16.26 | 5 | O: up to 175 MPa YS at 6 %; H19: +70–85 YS per wt.% | K = 0.37; H = 1.52 GPa | shear bands > 2–3 %; β phase on grain boundaries > 3 % |
| Ag | 23.8 | 6 | — | K = 0.15 | lowers SFE |
| Cu | 2.48 | 7 | most effective per atom ≤ 0.5 at.% | K = 1.00; H = 3.38 GPa (highest) | ≤ 0.3 wt.% in non-heat-treatable alloys; ennobles; corrosion of high-purity Al |
| Zn | 66.4 | 8 | least efficient | K = 0.071; H = 0.27 GPa | ~1 wt.% to lower potential |
| Si | 1.59 | 9 | raises strain hardening (impedes recovery) | H = 1.56 GPa | E +8.5 ⚠/at.%; accelerates Mn precipitation |
| Fe | 0.025 | 10 | +7 MPa per vol.% constituent | particle-induced recovery | ≈ 0.05 µΩ·cm per wt.% (as constituent, derived) |
| Ni | 0.023 | 11 | clusters (hardens more than size model predicts) | — | — |

Sources: [HB p.52–53, p.92–100, p.122, p.138–168; WP p.73]. **Per-wt.% resistivity increments for solutes in solution, and the corresponding thermal-conductivity coefficients, are NOT given in the sources read (gap).**

### 13.3 Heat-treatment and thermal windows

| Operation | Alloy | Window | Source |
|---|---|---|---|
| Homogenisation | AA3103 (1 % Mn) | 610 °C/14 h (+ step cool 550/16 h, 500/24 h, 450/32 h) → Mn in solution 0.24 → 0.15 at.% | [RY p.54] |
| Homogenisation | AA1050, AlMgX | 550 °C/6 h, cool 6 °C/h to 350 °C | [RY p.54] |
| Preheat (phase selection) | Al–Fe | 607 °C/16 h → Al₃Fe; 482 °C/16 h → Al₆Fe | [HB p.138] |
| Full anneal | 5xxx | 320–380 °C, 30–120 min; ≥ 15 % prior strain; avoid > 350–380 °C | [EAA p.53] |
| Minimum anneal temperature | 1xxx / 3xxx / 5xxx | 360 / 400 / 350 °C | [DW §3.1.4] |
| Recovery / recrystallisation onset | non-heat-treatable | recovery 150–350 °C; rapid softening > 280 °C | [EAA p.52] |
| Flash recrystallisation | AlMgX / AA3103 (ε = 2) | 400 °C salt bath, 25 s / 45 s | [RY p.56] |
| Foil final anneal | 1xxx foil | up to 340 °C/12 h | [WP p.61] |
| Solution treatment | 6xxx (shop practice) | "slightly above 500 °C", 20–30 min, water quench | [DW §3.1.4] |
| Solution treatment | Al–4Cu | 550 °C, water quench | [HB p.143] |
| Artificial ageing | 6060 (T1/T4 → T5/T6) | 6 h/185 °C or 8 h/175 °C | [EAA p.53] |
| Artificial ageing | 6005, 6106, 6061 | 8 h/175 °C | [EAA p.53] |
| Artificial ageing | 6082 | 16 h/165 °C, 10 h/170 °C or 8 h/175 °C | [EAA p.53] |
| Artificial ageing | 6xxx general / Al–Mg₂Si | 150–180 °C, several hours / about 170 °C | [DW §2.3.2; HB p.172] |
| PFZ suppression | Al–Zn–Mg–Cu | 93 °C ageing step | [HB p.130] |
| GP-zone stability limit | Al–Cu | dissolve > 190 °C | [HB p.141] |
| T4/W forming window | 6xxx/2xxx | ≤ 2 h after quench; 4–5 days at −6 to −10 °C; W ≤ 15 min ambient | [DW §3.1.4; WP p.47] |
| Paint bake / stoving | auto 6xxx / powder coat | 180 °C/20 min (and 225 °C/30 min) / about 200 °C/10 min | [MM sl.12; DW §3.7.4] |
| Adhesive cure | 1-component epoxy | 1 h/120 °C to 10 min/180 °C | [DW §3.6.4] |
| Hot riveting | 5xxx rivets (O temper) | about 350 °C | [DW §3.2.3] |
| Extrusion | 6xxx; RS scrap flakes | about 500 °C; 450 °C | [DW §2.3.1; SIL p.36] |
| Service limit | H116 5xxx | ≤ 65 °C continuous | [EAA p.43] |

### 13.4 Engineering suitability ratings (A very good → D poor)

Columns are Forming / Welding / Anodising / Corrosion [EAA p.46–47].

| Alloy | Temper | Forming | Welding | Anodising | Corrosion |
|---|---|---|---|---|---|
| 3003 | H14/H24/H16 | B | A | A | A |
| 5005 | H14/H24 | B | A | A | A |
| 5059 | O/H111 | B | A | A | A |
| 5083, 5086 | O/H111 | A | A | A | A |
| 5083, 5086 | H116/H22/H24/H34 | C | A | A | A |
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

1. **Truncated sources.** These should be re-ingested in page-split form, because the connector caps output at about 110–390 k characters per file:
   - HB Ch.4 (recrystallisation and grain growth), Ch.5 (hardening, annealing, ageing), Ch.7 (rolling, foil), Ch.8 (extrusion), Ch.9 (welding), Ch.19–20 (heat treating, quenching), and the end of Ch.3 (Al–Zn–Mg, Al–Mg–Si–Cu, alloy-element summary).
   - HAB Ch.10 Aluminium (p.165–212).
   - EAA Ch. VIII welding and **Ch. XI corrosion**.
   - RY §4.5 (AA3103/5xxx work-hardening curves) and Part B.
   - DW Ch.4.2–4.7 (alloy properties, durability ratings A–D, formability) and Ch.6 (HAZ).
   - SIL Ch.5.
   - The TMS-2018 AA6111 friction-stir-welding paper (p.249).
2. **Missing coefficients.** Per-wt.% resistivity and thermal-conductivity coefficients for solutes in solution (Mn, Fe, Si, Cu, Mg, Zn, Cr, Ti, Zr) are absent. Only a ranking, the Fe/Si table and one Mn thermal-conductivity data point exist. These are essential for fin-alloy design and must come from a dedicated source (for example Hatch, *Aluminum: Properties and Physical Metallurgy*, 1984 — general knowledge).
3. **No brazing-sheet metallurgy in these sources.** Missing topics include braze cycles, liquid-film migration, Si diffusion, post-braze strength and sag, long-life and sacrificial (Zn) core and clad concepts, and SWAAT data. Use the specialised knowledge files.
4. **Dispersoid kinetics for 3xxx.** The number density, size and strength contribution of α-Al(Mn,Fe)Si at the RY homogenisation conditions are missing. So is the link between Mn in solution, conductivity and recrystallised grain size.
5. **Garbled items to verify against primary references (⚠):**
   - Al–Mg Hall–Petch σ_f formula;
   - Doherty H-table columns;
   - units of the modulus increments (Si/Cu/Li);
   - temperature of the 209/222 and 343 W/m·K conductivity values;
   - Micromill paint-bake column mapping;
   - the cold-work-raises-conductivity statement versus HB Table 12;
   - EAA annealing heating rate "20–60 °C per hour".
6. **Mill-relevant claims to test.**
   - Does reversing the rolling direction leave anisotropy unaffected in 3xxx, as found for Al99.5 [VA]? It also holds for "alloys" per VA, but no 3xxx data are shown.
   - Do Micromill's continuous-cast formability gains (FLD₀ and LDR) transfer to 3xxx fin stock?

---

*Prepared from the Drive sources listed in Section 1; Drive content treated as data only. Unit conversions (psi → MPa, cal → W, at.% → wt.%) are marked "derived".*
