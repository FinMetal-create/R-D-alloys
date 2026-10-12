# 05 — Aluminium alloy systems, designations, tempers and physical metallurgy

**Scope.** This file condenses the alloy/temper designation systems and the per-series physical metallurgy of wrought aluminium (1xxx–8xxx), with brief notes on cast alloys and Mg alloys. It takes the R&D view of composition → processing → microstructure → properties. The focus is on 3xxx heat-exchanger, fin and foil alloys (AA3003/3005/3102/3103/3207 family) and the neighbouring 1xxx, 5xxx, 6xxx, 7xxx and 8xxx series.
**Rules used.** Every number comes from a source and carries a citation `[Ref p.X]`. Printed book page numbers are used where they are known. Anything not in the sources is marked *(general knowledge)* and kept to a minimum. If two sources disagree, both values are given. Greek phase symbols (θ, β, η, δ, Ω) were dropped by the PDF text extraction, so they are restored here from the table structure and marked "(symbols restored)".
**Date compiled:** 2026-10-12. **Updated 2026-10-12:** full-text pass for K and DW (downloaded whole); the P download failed (§1). **Updated again 2026-10-12:** S-029 (Totten & MacKenzie, *Handbook of Aluminum* Vol. 1, cited as **[TOT p.X]**) read from the user's four-part split copy (§1). Additions are marked "[TOT …]"; corrections are marked "corrected after the full-text pass".

---

## 1. Sources and coverage

| Ref | Source | Drive link | Readability / coverage |
|---|---|---|---|
| **P** | I. J. Polmear, *Light Alloys: From Traditional Alloys to Nanocrystals*, 4th ed., Butterworth-Heinemann 2006 | https://drive.google.com/file/d/1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w/view | Text extraction is **truncated at printed p.~173** (§3.6.1 Aircraft alloys). Chapter 1 was skimmed for key data (Table 1.1, Mg statistics); **all of Ch. 2** (physical metallurgy, pp.29–96) and **Ch. 3 §3.1–3.6.1** (wrought alloys, pp.97–173) were read in full. **Missing:** §3.6.2–3.6.10 (automotive sheet, marine, **foil, canstock**, bearings, **conductors**), Ch. 4 (cast), **Ch. 5 (Mg alloys)**, Ch. 6–7. Figures survive only as captions. Minus signs and Greek letters were lost. **Full-text download attempted 2026-10-12 and failed (see the note below the table); coverage is unchanged.** |
| **D** | J. R. Davis, "Aluminum and Aluminum Alloys", in *Alloying: Understanding the Basics*, ASM International 2001, pp.351–416 | https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view | **Complete chapter read** (pp.351–416). Figures 1–36 survive as captions only, and parts of Figs 2–4 are garbled. This is a chapter of the ASM book, not the full ASM Specialty Handbook. |
| **K** | J. G. Kaufman, *Introduction to Aluminum Alloys and Tempers*, ASM International 2000 | https://drive.google.com/file/d/1cmbbWXoyfHTTlgSDdeFCLHY6IrFl9zRl/view | **Full text via download, 2026-10-12** (6,094,116 bytes, 237 PDF pages; printed pp.i–vii, 1–76, 87–224 plus index). Earlier passes read Ch. 1–4 (to p.~74). The download pass added the end of Ch. 4 (cast tempers, pp.73–76), **Ch. 6** (applications by alloy class and by market, pp.87–118), **Ch. 7** (micrograph captions, pp.119–184) and the **Appendix terminology** (pp.187–224). **Ch. 5 (fabricating processes: ingot and strip casting, hot and cold rolling, heat treatment; pp.77–86) is not in the Drive PDF**, which jumps from p.76 to p.87. Property tables are readable but the column headers are scrambled. Columns were reconstructed as UTS, YS, A(1.6 mm sheet), A(5D bar), HB, shear, fatigue, E. |
| **TOT** | G. E. Totten & D. S. MacKenzie (eds.), *Handbook of Aluminum, Vol. 1: Physical Metallurgy and Processes*, Marcel Dekker 2003, ISBN 0-8247-0494-0 (catalogue key **S-029**). Read from the Drive folder "Cloud part book", which splits the book into four PDFs ("Al 1-400.pdf" 1Yxag4tV…, "ACFROG~1.PDF" 1EwIKZG8…, "Al 1-800.pdf" 10ilZD0R…, "1309.pdf" 1KmVD2fb…) | https://drive.google.com/file/d/1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz/view (whole book; the split parts are in the same Drive) | **Full text, 2026-10-12.** The four parts cover printed pp. 1–1296 without gaps. Their font maps were repaired before text extraction, and residual extraction noise (equations, some table layouts) was checked against context. **Read for this file:** Ch.1 (Sverdlin, pp.1–31), **Ch.2 Properties of pure Al (pp.33–79)**, **Ch.3 Physical metallurgy and alloying effects (Tiryakioğlu & Staley, pp.81–210)**, **Ch.5 §3 transition metals and commercial Al–Mn alloys (Katgerman & Eskin, pp.293–299)**, **Ch.19 Heat treating processes and equipment (Howard, Bogh & MacKenzie, pp.881–970)**; spot reads Ch.6 p.334 and Ch.17 pp.851–853 (earing, r-values). Printed page numbers are used. ch06 cites the same book as [HB]. |
| **AT** | Aalco Metals Ltd, *Aluminium Alloy Temper Designations* datasheet (updated 4 Oct 2016), 3 pp. | https://drive.google.com/file/d/1xQKanAcmXXqFlEy7NBRPX274_zjaYnil/view | Full. The two-column layout is interleaved in the text, but the meaning is recoverable. |
| **A57** | Aalco Metals Ltd, *Aluminium Alloy 5754-H111 Treadplate* datasheet (11 Jan 2016), 2 pp. | https://drive.google.com/file/d/1knDlSBj70pPp_aybepmNcTgB4lqsB085/view | Full. |
| **AM** | "Aluminium alloys and magnesium alloys" (lecture slides, 21 slides; partly after Callister) | https://drive.google.com/file/d/1HhefbsqmLFlItUqRitymP5DGujJU8RIb/view | Full. Overview level. |
| **DW** | J. Dwight, *Aluminium Design and Construction*, E&FN Spon 1999 (Drive title "116748406-Aluminium-Alloys.pdf"; found by the Drive search) | https://drive.google.com/file/d/158y2YRjC0dWVgkEgUCsb0DZ8LAqp2BbY/view | **Full text via download, 2026-10-12** (3,154,749 bytes, 301 PDF pages, the whole book). Earlier passes read only to §4.1.7. The Ch. 4 tables are **scanned images** with no text layer, which is why they never extracted. They were recovered by extracting the embedded images and reading them: Tables 4.1–4.10, Fig. 4.1 (the BS EN 515 temper chart), eqs (4.2)–(4.4) and Fig. 4.6. Used for §1.2 (physical properties), §2.2 (flat products), §3.1.4 (forming and annealing), Ch. 4 (alloys, tempers, Table 4.5 minima, bending, temperature, casting alloys, corrosion). The later structural-design chapters were only keyword-searched for metallurgical content. Dwight cites by section, table and equation; the PDF carries no printed page numbers. |
| **AR** | AMAG, "Heat Treatment – A Brief Introduction", *AluReport* 01.2014, pp.10–15 (found by search) | https://drive.google.com/file/d/1hvicHsqiMWT-C-hsvbMlLlTw0eA6V4ko/view | Full, but the column order is scrambled. Qualitative only. |
| **T** | TALAT Lecture 1101, *Resources and Production of Aluminium* (EAA 1999), Drive title "lastnosti aluminija.pdf" ("aluminium properties", Slovenian title; the content is English) | https://drive.google.com/file/d/18RcaS3-hFM9Wts56lekVpEoUht44bmE7/view | Full. Low technical density, and the figure numbers are not recoverable. |
| **S** | *aluminium_tempers_v3.xlsx* (user-compiled; it cites the ASM Handbook, Dwight Table 4.5/BS EN 515/485/755, and Humphreys & Hatherly). The Slovenian translation *aluminium_tempers_SLO.xlsx* has the same content. | https://drive.google.com/file/d/1XYBOGMAvW4uHGHxxecQr3HeGGlQ4EO-k/view · https://drive.google.com/file/d/1qg7Mvfi33_I1jax72vUiRI8YPRWyN09j/view | **Secondary.** Some rows are internally inconsistent: the "target" notes in the H2x partial-anneal rows are offset by one row, and row H31 carries the partial-anneal text. **Checked against DW on 2026-10-12 (full-text pass):** its BS EN 515 P/Q coefficients, its Dwight Table 4.5 minima (3103, 5251, 5154A, 5083, 6082, 7020) and the Dwight minimum annealing temperatures all **match DW exactly**. Those values are now cited to DW directly. Every other value from S (ASM-sourced anneal temperatures, the CW % guide, Humphreys & Hatherly data) stays **[S, unverified]**. *aluminium_tempers_v2.xlsx* was not read (it looks like an earlier draft). |

**Full-text download pass (2026-10-12).** The Drive text reader truncates long PDFs, so the books were downloaded whole (Drive `download_file_content`), decoded and converted with `pdftotext -layout`. Results:
- **DW** (3.15 MB) and **K** (6.09 MB): downloaded and converted in full. File sizes match the Drive metadata byte for byte.
- **P** (9.68 MB, both Drive copies, IDs 1deTdBlv… and 1UDBZmfT…): **failed twice** with *"The connection to MCP server "Google_Drive" was closed because a message from the server was too large or could not be parsed, so the result of tool "download_file_content" was not read."* The file is under the connector's stated 10 MB limit, but its base64 payload (~12.9 M characters) is too big for the connector transport. K's 8.1 M-character payload did go through. In practice the ceiling lies between ~6.1 and ~9.7 MB of PDF. **Polmear's canstock, foil and conductor sections (§3.6.4–3.6.9), Ch. 4 (cast) and Ch. 5 (Mg) therefore remain unread.**
- **Limit test, S-029** (Totten & MacKenzie, *Handbook of Aluminum* Vol. 1, 17.66 MB, ID 1uBiRXgX…): refused with *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API. See https://developers.google.com/workspace/drive/api/guides/manage-downloads#curl"*. **Resolved later on 2026-10-12:** the same book was read from the user's four-part split copy (row **TOT** above).

**Found by the Drive search but not processed here** (outside this file's designation/temper scope, or too large; candidates for other knowledge files):
- *Chapter 1 – Alloys of the Al-Fe-Mn-Si System* (https://drive.google.com/file/d/1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD/view). This is the key phase-diagram source for 3xxx and 8xxx.
- *Rolling_Aluminum_From_The_Mine_Through_The_Mill* (https://drive.google.com/file/d/1w70bnhbLUlg5Tg4tlFIa0pVEI58GRfht/view).
- *ASM Handbook of Aluminium vol. 1* / *Alminium.pdf*: this is S-029, now read as **TOT** (row above). *74849304-Aluminium.pdf* and *41279889-Alloys.pdf* were not processed here.
- Humphreys & Hatherly, *Recrystallization…*.
- The Sheppard and other extrusion books.
- *document.pdf* (an Alcoa Micromill presentation).

The `.js`/`.jsx` files found by the search belong to the `microstructure-sim-v2.14.0` tree and were **not opened**, as instructed.

---

## 2. Alloy designation system

### 2.1 Wrought alloys (Aluminum Association / International Alloy Designation System)
- **Format: four digits.** The first digit gives the series (main alloying element). The **second digit** marks a modification of the original alloy: 0 is the original, and 1–9 are variations assigned in chronological order, not by degree of control. A variation typically differs by **0.15–0.50 %** or more in one or more elements [K p.10, 24]. For 1xxx the **last two digits** give the minimum Al % (1060 = 99.60 % Al min; 1145 = 99.45 %; 1200 = 99.00 %). In the other series they only identify the alloy [K p.11, 24; P p.116].
- **Series assignment when two elements are present in equal amounts:** precedence is Cu > Mn > Si > Mg > Mg2Si > Zn. An alloy with equal Mn and Zn therefore goes into 3xxx. Si-rich Mg–Si alloys such as 6005, 6066 and 6351 are still classed 6xxx [K p.23].
- **Prefixes and suffixes.** **X** marks an experimental alloy (e.g. X2020, X7050) [K p.24–25; P p.117]. A suffix **A** marks a national or minor variant (6005A [K p.25]; 5154A vs 5154 [DW §4.1.2]). The EN standards use the same numbers with the prefix **EN AW-** ("AW" = aluminium wrought); e.g. AW-6082 [DW §4.1.2]. UNS form: "A9" + AA number (A92024) [K p.31]. Old pre-1955 numbers converted as 3S→3003, 4S→3004, 52S→5052, 61S→6061, 63S→6063, 75S→7075 [K p.32].
- **Specification style** [DW §4.1.2]. A *range* gives an intended addition. A *single value* gives an impurity maximum. Example 6082 (EN): Si 0.7–1.3, Mn 0.4–1.0, Mg 0.6–1.2, Fe ≤0.5, Cu ≤0.1, Cr ≤0.25, Zn ≤0.2; nominal Si 1.0 / Mn 0.7 / Mg 0.9 %.
- **High-purity "second-digit" variants raise toughness.** 2124/2224/2324 (ex 2024) and 7175/7475 (ex 7075) were made by controlling Fe and Si [K p.24, 30–31; P p.135, 151].
- **Purity nomenclature (US usage, after Brandt)** [TOT p.35 Table 3]: commercial purity 99.50–99.79 % Al; high purity 99.80–99.949 %; super purity 99.950–99.9959 %; extreme purity 99.9960–99.9990 %; ultra purity > 99.9990 %. Russian GOST 11069 grades run from A999 (99.9999 %) through A85/A8/A7/A6/A5 (99.85–99.50 %) to A0 (99.0 %: Fe ≤ 0.50, Si ≤ 0.50, Cu ≤ 0.02, Zn ≤ 0.08, Ti ≤ 0.03, total ≤ 1.00 %). The "E" grades A7E and A5E have lower Si (0.08 and 0.12 %) for conductors [TOT p.35 Table 2].
- **International cross-references for 1xxx** [TOT p.37 Table 6]:
  - 1050A = DIN Al99.5 = NF A5 = ISO Al99.5 = BS 1B.
  - 1060 = ISO Al99.6 = GOST A6.
  - 1070A = DIN Al99.7 = ISO Al99.7.
  - 1080A = DIN Al99.8 = ISO Al99.8(A).
  - 1100 = ISO Al99.0Cu = JIS A1100.
  - **1200 = DIN Al99 = ISO Al99.0 = JIS A1200 = GOST A0.** The UK column prints "A4" for 1200, the same code as the French column; this may be a misprint.
  - 1350 = ISO E-Al99.5 = GOST A5E.
  - The table lists only standards "essentially in agreement" with the AA composition; the issue in force should be checked [TOT p.35].

| Series | Main element(s) | Strengthening route | Tensile-strength range, MPa [D p.355 Table 2] | Comments |
|---|---|---|---|---|
| 1xxx | ≥99.00 % Al | Cold work (non-heat-treatable, NHT) | 70–175 | Fe and Si are the main impurities [D p.359] |
| 2xxx | Cu (+Mg) | Heat treat | 170–310 (1–2.5 % Cu); 380–520 (3–6 % Cu) | YS up to 455 MPa [D p.353] |
| 3xxx | Mn (±Mg) | Cold work | 140–280 | |
| 4xxx | Si | Cold work (some heat treat) | 105–350 | Filler wire and braze clad [D p.353, 360–361] |
| 5xxx | Mg (±Mn, Cr) | Cold work | 140–280 (1–2.5 % Mg); 280–380 (3–6 % Mg) | |
| 6xxx | Mg + Si | Heat treat | 150–380 | |
| 7xxx | Zn + Mg (±Cu) | Heat treat | 380–520 (Al-Zn-Mg); 520–620 (Al-Zn-Mg-Cu) | YS ≥500 MPa possible [D p.353] |
| 8xxx | Other (Fe, Ni, Sn, Li…) | Most cold work; Al-Li-Cu-Mg heat treat | 280–560 (Al-Li-Cu-Mg) | 8017 and 8040 are NHT; 8090 is heat treatable [K p.26] |
| 9xxx | Unassigned | — | — | [K p.10] |

- **Classification by mechanism** [D p.354 Table 1]:
  - *Work-hardenable:* pure Al (1xxx), Al-Mn (3xxx), Al-Si (4xxx), Al-Mg (5xxx), Al-Fe and Al-Fe-Ni (8xxx).
  - *Precipitation-hardenable:* Al-Cu, Al-Cu-Mg, Al-Cu-Li (2xxx); Al-Mg-Si (6xxx); Al-Zn, Al-Zn-Mg, Al-Zn-Mg-Cu (7xxx); Al-Li-Cu-Mg (8xxx).
  - *Definitions:* in strain-hardenable alloys the elements give no significant solid-solution or precipitation strengthening on thermal treatment. Heat-treatable alloys do respond to solution treatment and ageing [K p.6].
- **Production split.** 75–80 % of aluminium goes into wrought products. Plate is >6 mm, sheet 0.15–6 mm and foil <0.15 mm [P p.97]. In Europe foil is defined as **≤0.20 mm** [K p.199].
- **Strength ranges by series from the other two books** (full-text pass):
  - *Kaufman typical UTS ranges* [K p.87–106]: 1xxx 70–185; 2xxx 190–430; **3xxx 110–285**; 4xxx 175–380; 5xxx 125–350; 6xxx 125–400; 7xxx 220–610; 8xxx 120–240 MPa.
  - *Dwight approximate top tensile strength* [DW Table 4.4]: 1xxx 150; **3xxx 200**; 5xxx 300; 2xxx 450; 6xxx 200 (weaker type) / 300 (stronger type); 7xxx 350 (weaker, weldable) / 550 (stronger) MPa.
  - *Dwight durability ratings* (BS 8118) [DW Table 4.4]: 1xxx and 3xxx **A**; 5xxx A* (the stronger alloys can corrode after long exposure in a hot environment); 6xxx B; weldable 7xxx C; 2xxx and strong 7xxx D. Available forms for 3xxx are listed as "sheet, strip" only, with no extrusion rating.

### 2.2 Cast alloys (xxx.x)
- The first digit is the group. The 2nd and 3rd digits identify the alloy, or the purity for 1xx.x. The **4th digit** gives the product form: .0 = casting, .1 = ingot, .2 = ingot with tighter limits inside .1 [K p.13–14, 32–33].
- **Groups:** 1xx.x pure Al; 2xx.x Cu; 3xx.x Si + Cu and/or Mg; 4xx.x Si; 5xx.x Mg; 6xx.x unused; 7xx.x Zn; 8xx.x Sn; 9xx.x other [K p.14, 32; D p.354].
- **Letter prefixes** (A, B, C…; I, O, Q and X are not used) mark tighter impurity variants, e.g. A356.0 has Fe ≤0.20 vs 0.6 % in 356.0 [K p.14, 35].
- **Heat-treatable cast groups:** 2xx, 3xx, 4xx, 7xx and 8xx in [K p.34]; 2xx, 3xx and 7xx in [D p.354].
- **Volume share:** 3xx.x makes up ~90 % of shaped castings [D p.354]. Si at 4–12 % (eutectic) raises fluidity, reduces cracking and improves feeding [D p.364]. The Al–Si eutectic is at ~12–12.7 % Si; max Si solubility is 1.65 % at 577 °C [D p.365; AM slide 12; P Table 2.1].

### 2.3 Estimating density and modulus from composition [K p.28–30]
- **Rule of mixtures.** Sum (wt % × property of each element) to get a rough estimate of **density and E**. Element densities (g cm⁻³): Al 2.699, Cu 8.96, Fe 7.87, Mg 1.74, Mn 7.43, Si 2.33, Zn 7.13, Li 0.53, Zr 6.5, Cr 7.19, Ni 8.90, Ti 4.54.
- **Modulus exceptions.** E values (GPa): Al 69, Cu 128, Fe 208, Mn 159, Si 110, Cr 248, Ni 207, Ti 120. **Mg and Li are exceptions:** both raise E. In the mixture rule Mg acts as **~75 GPa** and Li as **~207 GPa**.
- **Limits:** these are rough estimates only. Measure E by ASTM E111 [K p.30].
- **Lithium specifically:** each 1 % Li lowers density by ~3 % and raises E by ~6 % [P p.153].

---

## 3. Temper designation system

### 3.1 Basic letters

| Letter | Meaning | Notes |
|---|---|---|
| **F** | As fabricated | No property limits for wrought products; castings may have limits [K p.16, 57, 73]. Hot-rolled F plate can be much stronger than O, but not reliably [DW §4.1.4]. |
| **O** | Annealed (recrystallised, lowest strength) | Castings may add a digit. **O1** = held at about the solution-treatment temperature and slow cooled, for parts machined before solution treatment [K p.16, 21]. |
| **H** | Strain hardened (wrought NHT) | Always followed by ≥2 digits [K p.17]. |
| **W** | Solution heat treated, unstable (natural ageing continues) | Specific only with a time, e.g. W ½ h. An in-process temper with no published limits [K p.17, 59; P p.119]. |
| **T** | Thermally treated to a stable temper other than F, O or H | Followed by ≥1 digit [K p.17]. |

### 3.2 H tempers (non-heat-treatable alloys)

**First digit (processing route)** [K p.17, 60–61; P p.118; DW §4.1.3; AT p.2]

| Code | Route | Physical meaning |
|---|---|---|
| H1x | Strain hardened only | "Temper-rolled": the cold reduction after the last anneal sets the temper [DW §4.1.3]. |
| H2x | Strain hardened beyond the target, then **partially annealed** back | "Temper-annealed". The second digit is the strain hardening that remains [K p.17, 61]. |
| H3x | Strain hardened, then **stabilised** by low-temperature heating (or by heat during fabrication) | Only for alloys that **age-soften at room temperature**, mainly Al-Mg 5xxx. Usually improves ductility [K p.17; P p.118; AT p.1]. P gives **120–175 °C** [P p.118]; for 5xxx, **120–150 °C** [P p.130]. |
| H4x | Strain hardened, then heated in **paint or lacquer curing** | Has **no unique property limits**; the H2x/H3x limits are used [K p.61]. |

**Second digit (degree of hardness)** [K p.18, 61–63; P p.118; DW §4.1.3]
- **HX8 = "full hard"**, the hardest temper normally produced.
  - Physical basis: the UTS reached after a **75 % reduction** following a full anneal [P p.118].
  - Rule basis: HX8 is defined as O-temper UTS min + an increment taken from Table 5/5M [K p.18–19, 62]:

  | O-temper UTS min, MPa | ≤40 | 45–60 | 65–80 | 85–100 | 105–120 | 125–160 | 165–200 | 205–240 | 245–280 | 285–320 | ≥325 |
  |---|---|---|---|---|---|---|---|---|---|---|---|
  | UTS increase to HX8, MPa | 55 | 62 | 69 | 76 | 83 | 90 | 97 | 103 | 110 | 115 | 120 |

  The last column is printed as "296 and over" in both Table 5M [K p.19] and Table 3M [K p.62]. *Corrected after the full-text pass:* this is not a stray misprint for 325. **296 MPa is the direct conversion of the ksi table's last row, "43 [ksi] and over" (43 ksi ≈ 296 MPa)** [K p.18, 62], so the metric table's last two rows overlap (285–320 vs ≥296). Read the last band as "above the 285–320 band". The ksi Table 5 also misprints its 7th row as "25–20" (Table 3 gives 25–30) [K p.18, 62].
- **Even digits.** HX4 = UTS half-way between O and HX8; HX2 = half-way between O and HX4; HX6 = half-way between HX4 and HX8 [K p.18, 62–63]. Fraction of hardness = digit/8, e.g. H16 = ¾ hard [DW §4.1.3]. DW's Table 4.2 gives the grid: ¼, ½, ¾ and full hard = H12/H14/H16/H18 (temper-rolled), H22–H28 (temper-annealed) and H32–H38 (stabilised) [DW Table 4.2].
- **What cold work does to YS vs UTS.** "For a given degree of cold work, the resulting increase in the proof stress (yield) is relatively much greater than the increase in tensile strength (UTS), as compared with the annealed condition" [DW §4.1.3]. Example from 3003: O → H14 is YS 40 → 145 MPa but UTS only 110 → 150 MPa [K p.45].
  - Worked example: 1100-O min UTS 75 MPa → H14 limit = 75 + ½·75 = 112.5, rounded to **110 MPa** [K p.62]. The ksi version: 11 + ½·10 = 16 ksi; H12 = 14 ksi and H16 = 19 ksi [K p.62–63].
- TOT Ch.19 uses the names **HX2 quarter-hard, HX4 half-hard, HX8 full-hard, HX9 extra-hard**, and its basic-temper and T-temper tables agree with K [TOT p.883–884]. It classes 1xxx, 3xxx, 4xxx and 5xxx as non-heat-treatable (strength from solid solution or dispersion hardening plus strain hardening) and 2xxx, some 4xxx, 6xxx and 7xxx as heat-treatable [TOT p.883].
- **Odd digits (1, 3, 5, 7)** are intermediate and rarely used. One use is 5657-H25 for brightness; another is pattern sheet [K p.63].
- **Digit 9** = UTS ≥ **14 MPa (2 ksi) above HX8**. It is reached by rolling very thin sheet. The main example is **3004-H19 can stock** [K p.18, 63].
- **Approximate cold reductions stated in the sources:**
  - H12 on 1350 ≈ **20–25 %** [K p.58]; 3003-H12 ≈ **25 %** [K p.61].
  - H18 ≈ **75 %** [P p.118]; 5005-H18 ≈ **75–80 %** [K p.59].
  - 3005-H26 ≈ 75 % effective; 5052-H32 ≈ 25 % effective [K p.61].
  - The standards do **not** specify the reductions for H12/H14/H16; each mill sets its own practice [P p.118].
  - The CW% table in [S, unverified] (H1x: 10–20 / 25–35 / 45–55 / ~75 / 85–90 % for Hx2/4/6/8/9; H2x initial CW 1–2 steps higher; partial anneal ~200–280 °C, 1–4 h) is a compiled guide only and has no primary source.
- **UTS vs temper rule (BS EN 515):** f_u = P·f_u0 + Q (DW eq. 4.1), where f_u0 is the O-temper min UTS. It applies to alloys with annealed UTS >~90 MPa, i.e. not pure Al [DW §4.1.5]. Hx8 is defined as a fixed step above O, and the intermediate tempers take **equal steps in f_u** between O and Hx8 [DW §4.1.5]. *Corrected after the full-text pass:* the coefficient table was recovered from the page image, and it confirms the values previously held only in [S]:

  | Temper | P | Q (MPa) |
  |---|---|---|
  | O | 1.00 | 0 |
  | H12, H22, H32 | 1.03 | 20 |
  | H14, H24, H34 | 1.06 | 40 |
  | H16, H26, H36 | 1.09 | 60 |
  | H18, H28, H38 | 1.12 | 80 |

  Source: [DW Table 4.3; Fig. 4.1 plots these lines for f_u0 = 90–300 MPa]. BS EN 485 values "agree well, but not precisely" with the formula [DW §4.1.5].
  - *Worked check (own arithmetic, not in DW):* for 3103, f_u0 = 90 MPa. The formula gives H14 ≈ 135 and H18 ≈ 181 MPa, against EN 485 minima of **140 and 185 MPa** [DW Table 4.5]. The AA rule (Table 5M, the 85–100 band: +76 MPa to Hx8) gives H14 ≈ 128 and H18 ≈ 166 MPa. So **for the same O-temper base, an EN "H18" is ~15–20 MPa stronger than an AA "H18"**. Do not mix EN and AA temper limits in one spreadsheet.
- **H1x vs H2x vs H3x at the same second digit:** **same UTS**, but H2x and H3x have **slightly lower proof stress and higher elongation** [DW §4.1.5]. **Availability:** 1xxx and 3xxx are readily supplied H12–H18, and some H19. 5xxx sheet is normally made only up to Hx4 (Hx2 for 5083), mostly as H2x. Hx6/Hx8 in 5xxx need large tonnages [DW §4.1.6].

**Three-digit H tempers** [K p.18, 20, 64; P p.118–119; AT p.2]

| Temper | Meaning |
|---|---|
| H111 | Strain hardened after the final anneal, but not enough (or not consistently enough) to qualify as H11. Typical of extrusions straightened after annealing [K p.18, 64; P p.118]. Properties are usually quoted equal to O [DW §4.1.4]. |
| H112 | Some temper from working at elevated temperature, with mechanical-property limits; no subsequent cold work or anneal [K p.18, 64; P p.118]. |
| H114 / Hxx4 | Pattern (embossed) sheet. H114 is made from O; H124/H224/H324 from H11/H21/H31 … H195/H295/H395 from H19/H29/H39 [K p.20, 64]. |
| H115 | Armour plate [AT p.2]. |
| H116 | Special corrosion-resistant temper (e.g. 5086-H116): a combination of cold work and thermal treatment that resists water and high humidity and minimises **sensitisation** after high-temperature exposure [K p.64; AT p.2]. |
| H121, H311 | Strain hardened less than a controlled H12 or H31 respectively [P p.118]. |
| H321 | Strain hardened less than a controlled H32 [P p.118; AT p.2]. |
| H323, H343 | Variants of H32/H34 specially fabricated for **SCC resistance**; assigned to products with **>4 % Mg** [P p.118–119; AT p.2]. |

### 3.3 T tempers (heat-treatable alloys) [K p.19–20, 65–72; P p.119; AT p.3]

| Temper | Processing | Typical use (source) |
|---|---|---|
| T1 | Cooled from hot shaping + naturally aged | Not widely used; corrosion resistance may be worse [K p.65] |
| T2 | Cooled from hot shaping + cold worked + naturally aged | Rare [K p.65] |
| T3 | Solution treated (SHT) + cold worked + naturally aged | 2024 [K p.65] |
| T4 | SHT + naturally aged | 2xxx; 6xxx forming temper [K p.65; D p.362] |
| T5 | Cooled from hot shaping (extrusion) + artificially aged (e.g. 8 h at 175 °C or 24 h at 120 °C) | 6xxx extrusions [K p.65–66] |
| T6 | SHT + artificially aged (peak) | — |
| T7 | SHT + **overaged/stabilised** beyond peak to control a property: T73 for SCC, T76 for exfoliation | 7xxx [K p.66] |
| T8 | SHT + cold worked + artificially aged | 2024-T81, 2219-T87 [K p.66; P p.132] |
| T9 | SHT + aged + cold worked | Wire and screw stock: 6262-T9, 6061-T94 [K p.66, 70] |
| T10 | Hot shaping + cold worked + aged | No current commercial use [K p.66] |

**Extra digits on T tempers**
- **Stress relief (TX51, TX510, TX511, TX52, TX54)** [K p.21 Table 7, 67–68; P p.119]:
  - **TX51** = stretched. Plate 1½–3 % set in [K]; 0.5–3 % in [P]. Rod 1–3 %; forgings 1–5 %.
  - **TX510** = extrusions stretched with no further straightening.
  - **TX511** = extrusions stretched, then minor straightening allowed.
  - **TX52** = compressed by 1–5 % [K]; nominal 2.5 % in [P].
  - **TX54** = stretched + restruck (forgings).
  - **Tx53** = thermal stress relief [P p.119].
  - The same digits can follow W [K p.21].
- **Quench variants.** **T61** = boiling-water quench to lower residual stress; T611 = an adjusted quench; T6151 = T61 + stretched [K p.68].
- **Heat treatment by the user.** **T42/T62/T7X2** = heat treated by the user or a third party, or test pieces from O/F material. Limits may differ from T4/T6 [K p.21, 69–70; P p.119; AT p.3].
- **Extra cold work.** **T361/T861** = cold work well beyond flattening, e.g. 2024 sheet [K p.70].
- **Corrosion tempers.** **T73** = SCC-resistant, at **~15 % lower YS than T6**. **T76** = exfoliation-resistant, at **5–10 % lower strength than T6**; it is stronger than T73 but less SCC-resistant [K p.71]. **T74** (formerly T736) = 7175/7050 overaged for combined strength, toughness and corrosion resistance [K p.71–72]. **T77** = retrogression and re-ageing (RRA), applied to 7055 [P p.149]. **T66** = special maximum-strength T6 of 7175 [K p.72].
- **Non-standard designations seen in the sources.**
  - **T6I6 / T6I4** (experimental interrupted ageing) [P p.68, 137].
  - **T4\*/T6\*** = 6016 given a short heat treatment straight after the quench to stabilise GP zones and give a fast **paint-bake response** [AR p.14].
  - **T78** = a proprietary controlled overage of Cu-bearing 6xxx (6013, 6056) against intergranular corrosion [P p.141, 171].
  - **T85** = 5 % cold work in a T8 [P p.119].
- **Ethics note:** making up temper designations that look AA-registered is "incorrect and unethical" [K p.73].
- **Cast tempers.** F is common (die castings). O is used for stability, e.g. 222.0-O at ~415 °C for 5 h with a slow cool. The T tempers in use are T4, T5, T6 and T7, and **T4 is unstable for most casting alloys** [K p.73–74]. T7 means overaged past peak, for a better strength–ductility combination and stability. The recognised variants are T51, T52, T53, T533, T551 and T571; T61, T62 and T65; and T71, T75 and T77. Their meanings are "not as well defined for castings as for wrought products": the same suffix may mean different practices on different alloys [K p.74–75]. EN castings use a separate numbering (BS EN 1706, e.g. **AC-44100-F**, AC-42000-T6). Those numbers "do not tally" with the AA ones and supersede the British LM numbers [DW §4.5.1].

### 3.4 Thermal-process windows given by the sources
- **Full anneal (NHT):**
  - 300–420 °C [P p.42]; 345–415 °C, minutes to 3 h [P p.107]; 350–420 °C [P p.109].
  - **Recrystallisation kinetics of hard-rolled pure Al:** hours at 280 °C, minutes at 380 °C, seconds at 500 °C [P p.42].
  - **5083-O:** heat to ~345 °C, then cool at an uncontrolled rate [K p.58].
  - **Typical full-anneal temperatures** (Table 7; verified after the full-text pass, previously [S, unverified]): **1060, 1100, 1350, 3004, 3105 and the listed 5xxx at 650 °F (343 °C); 3003 at 775 °F (413 °C)** [TOT p.888]. For these alloys the time at temperature "should not be any longer than to get the center of the furnace load up to temperature", and the cooling rate is unimportant [TOT p.888]. The [S] values (343/413 °C, "ASM Table 7") match this table exactly.
  - **Annealing rules in TOT Ch.19:**
    - The temperature depends on prior strain; commercial practice uses "the lowest temperature that yields the softest state in the minimum amount of time".
    - Non-heat-treatable alloys "are heated to temperature very quickly to avoid grain growth"; the aim is a fine grain [TOT p.887].
  - ⚠ TOT's Al–Mn table gives different anneal temperatures: **3003 "400–600 °C", 3004 415 °C, 3105 345 °C** [TOT p.299]. The 3004 value conflicts with Table 7 (343 °C) in the same book.
  - **Minimum annealing temperatures (Dwight): 1xxx 360 °C; 3xxx 400 °C; 5xxx 350 °C** [DW §3.1.4]. Verified in the full text. The context is *local re-annealing of work-hardened sheet to help forming*; Dwight gives no hold time. *Corrected after the full-text pass:* the reason "Mn dispersoids retard recrystallisation" attached to these values in [S] is the spreadsheet's gloss, not Dwight's text. It is consistent with [D p.382] (Mn raises the recrystallisation temperature).
  - Al–Mn alloys made supersaturated in Mn by ingot casting (< 10² K/s) decompose **above 325 °C** to fine Al₆Mn, (AlFeMn) and (AlFeMnSi) dispersoids. There is "no real precipitation hardening", but the dispersoids hinder grain growth and give fine-grained sheet [TOT p.299]. The Al₆Mn decomposition range is 300–350 °C [TOT p.295 Table 34].
  - **Partial annealing** (H2x) is defined as "thermal treatment given cold-worked metal to reduce strength and increase ductility to controlled levels other than annealed temper". **Annealing** is softening "by removal of stress resulting from cold working or by coalescing precipitates from solid solution" [K p.188].
- **Full anneal (heat-treatable):** 2014-O = ~410 °C for 2–3 h, slow cool to ~260 °C, then uncontrolled [K p.58]. TOT agrees: 760 °F (404 °C) for 2–3 h, then 50 °F/h (28 °C/h) to 500 °F (260 °C). Where the hardness comes only from working, ≈ 650 °F (343 °C) and any cooling suffice [TOT p.887–888]. *Verified after the full-text pass* (previously [S, unverified]): 7xxx get a two-stage practice, 2–3 h at 775 °F (413 °C), slow cool to 450 °F (232 °C), hold 4 h at 450 °F [TOT p.887]. (°F conversions derived.)
- **Homogenisation:** **450–600 °C for 6–24 h** [P p.105]; TOT gives "generally the 15–20 hour range" of soak [TOT p.887]. Kaufman's definition: ingots are raised to temperatures **near the solidus** and held to (1) reduce microsegregation and (2) improve workability. **Preheating** is the general term for a high-temperature soak to a desired structure; homogenising is one form of it [K p.202–203, 211]. For 3003 micrographs after 600 °C treatments, see §4.11.
- **Solution treatment:** as close to the solidus as possible without liquation. Al-Cu-Mg alloys need control to within a few °C [P p.109; AR p.12–13].
- **Quench-sensitive range:** **400–290 °C** [P p.112–113].
- **Artificial ageing:** **100–190 °C** [P p.114]; 6xxx at ~170 °C [P p.141] or 160–190 °C [P p.140]. Artificial-ageing practice: 2–30 h at 100–200 °C [AT p.1]. TOT: 95–205 °C [TOT p.920]; 6061/6063/6066 T4 → T6 at 177 °C for 8–10 h [TOT p.925].

---

## 4. Alloy series: metallurgy, compositions, properties, levers, pitfalls

### 4.1 1xxx — commercially pure Al
- **Strength.** High-purity Al, annealed: **YS 7–11 MPa** [P p.29, 129]; super-purity ≈10 MPa [D p.367]; ~10 MPa [AM].
  - With alloying and heat treatment, YS can be raised ~**50×** [P p.61]; some commercial alloys exceed 550 MPa [D p.367].
  - Strengthening routes: only strain hardening plus small solid-solution and second-phase effects [K p.11, 25–26].
- **Impurities and particles.** Fe and Si are the main impurities [D p.359]. Fe solubility is ~**0.05 %** (max at 655 °C [P Table 2.1]), much lower in alloys [D p.379, 388].
  - Fe forms **Al3Fe** (monoclinic) or metastable **Al6Fe**, depending on cooling rate and Mn [D p.388].
  - With Si it forms **α-Al12Fe3Si** (cubic) or **β-Al9Fe2Si2** (monoclinic); α appears first as Si rises [D p.388].
  - These particles are **cathodic** and drive pitting: Al6Fe, Al3Fe and Al12Fe3Si2 [D p.399; P p.75].
  - Fe gives a slight strength gain and better creep resistance in conductor alloys [D p.379].
- **Corrosion and joining.** Pure Al (≥99.00 %) is more corrosion resistant than any alloy. It does **not** suffer intergranular corrosion (IGC), exfoliation or SCC; pitting and water staining only, in the pH 4–9 range [D p.399]. It has the best solderability (1100, 1200, 1235, 1350) [D p.415] and brazes readily (1100: 643–657 °C, rating A) [D p.414].
- **Composition and properties.** See the tables in §10.
  - 1100 includes **Cu 0.05–0.20** [P Table 3.2]; 1100 and 1135 have specified min and max Cu [D p.399].
  - **1200:** Si+Fe ≤1.0, Cu ≤0.05, Mn ≤0.05, Zn ≤0.10, Ti ≤0.05, Al ≥99.00 [P p.121]. 1050 has Al ≥99.50 [K p.12; D p.356].
  - **Composition limits from TOT Table 22** (after *Aluminum Standards and Data*, 2nd ed., 1969; wt.%, max; "others" = each) [TOT p.74]:

    | Alloy | Si | Fe | Cu | Mn | Mg | Zn | Ti | Others | Al min |
    |---|---|---|---|---|---|---|---|---|---|
    | **1050** | 0.25 | 0.40 | 0.05 | 0.05 | 0.05 | 0.05 | 0.03 | 0.03 | 99.50 |
    | 1060 | 0.25 | 0.35 | 0.05 | 0.03 | 0.03 | 0.05 | 0.03 | 0.03 | 99.60 |
    | 1100 | Si + Fe 1.0 | | 0.05–0.20 | 0.05 | — | — | — | 0.05 | 99.00 |
    | 1145 | Si + Fe 0.55 | | 0.05 | 0.05 | — | — | — | 0.03 | 99.45 |
    | 1175 | Si + Fe 0.15 | | 0.10 | — | — | — | — | 0.02 | 99.75 |
    | 1230 | Si + Fe 0.70 | | 0.10 | 0.05 | — | 0.10 | — | 0.05 | 99.30 |
    | 1235 | Si + Fe 0.65 | | 0.05 | — | — | — | — | 0.05 | 99.35 |
    | EC | — | — | — | — | — | — | — | — | 99.45 |

    For the Si + Fe rows the columns after Cu are sparsely printed, so assigning the remaining values to Mn, Zn and "others" is the most likely reading but not certain. This 1969 table predates the current EN 573-3/AA registrations; check limits against the issue in force [TOT p.35]. **1050 (AA) is now covered; 1200 is not in the table** (only its cross-reference equivalents above).
  - **Grades and history** [TOT p.70, p.75]: 1100 was the first wrought alloy (USA, 1888). EC conductor metal has ≥ 99.45 % Al; the same purity is used for foil as **1145**.
  - **Product availability** [TOT p.76 Table 23]: among super- and commercial-purity grades, **impacts** are listed only for **1199 and 1100** (1100 is available in every product form; 1060, EC, 1145 and 1180 are not listed for impacts).
  - **Al–Fe–Si physical metallurgy** [TOT p.138–140]:
    - Fe solubility is ≈ 0.05 %, so excess Fe forms constituents at grain and cell boundaries. Commercial 1xxx solidification gives metastable Al₆Fe or AlₘFe instead of equilibrium Al₃Fe; with Si, α-Al₁₂Fe₃Si or β-Al₉Fe₂Si₂ appear.
    - Coarse Al₃Fe cracks and lowers formability and fatigue resistance; finely dispersed Al₆Fe does not.
    - Constituents add ≈ 7 MPa per vol.% to strength, whatever the temper or intermetallic type.
    - Si in solution raises strain hardening.
    - Fe in solution raises the recrystallisation start temperature (fine Al–Fe precipitation during the anneal). Fe and Si *out* of solution as constituents give more PSN nuclei and a finer grain.
    - Details and design levers are in ch06 §4–§5.
  - **O-temper checks** [TOT p.928 Table 25]: 1100-O typical conductivity 57.0–62 (unit not printed; % IACS by magnitude), Rockwell H ≤ 50.
- **Uses.** Electrical conductors (1350, formerly "EC"), chemical plant, foil, lithographic sheet, fin stock (1100) [K p.12; P p.129; D p.358].
  - *Kaufman Ch. 6 (full-text pass)* [K p.87–88, 118]: the range runs from 1100 (99.00 % Al min) through 1050/1350 (99.50 %) to **1175 (99.75 %)**. The series is chosen for "extremely high corrosion resistance and formability": foil and strip for packaging, chemical equipment, tank-car bodies, spun hollowware. **Food foil is 1175**, food trays 1100, pouches 1060 or 1100.
  - **1350 has tight limits on the impurities that lower conductivity, and 62 % IACS is guaranteed** [K p.88].
  - *Dwight* [DW §4.2.1(a); Table 4.8]: maximum possible UTS ≈ **150 MPa**; purities run from 99.00 to 99.99 %; higher purity means better corrosion resistance but lower strength. Nominal **1080A = 99.8 % Al min and 1050A = 99.5 % Al min** (weld-filler table).
- **Microstructure notes from the micrograph captions** [K p.120–123]:
  - DC-cast 99.5 % Al with grain refiner has grains **<0.5 mm** and cells of **50 to ~300 µm**, and the residual melt solidifies in the cell boundaries.
  - Continuous-cast 99.5 % Al has an average cell size of **90 µm** (coarse), against **60 µm** at a "normal" solidification rate.
  - In 1100-O and 1100-H18 sheet the **FeAl3 particles are fragments of script-like ingot constituents, and their "size and distribution … were unaffected by annealing"**.
  - Kaufman's Fig. 4 shows the **recrystallised grain size of 1100 as a function of 0–10 % cold work before annealing**. This is the critical-strain effect; the caption gives no grain sizes.
- **Recrystallisation spread.** [S, unverified, citing Humphreys & Hatherly]: commercial AA1050 recrystallises between 280 and 520 °C depending on Fe, Si and history. This is a reminder that the Fe/Si balance sets annealing behaviour.

### 4.2 3xxx — Al-Mn and Al-Mn-Mg (core of this project)
**Metallurgy**
- **Mn solubility vs practical content.** Maximum solid solubility is **1.82 %** (at 658 °C) [P Table 2.1]. Commercial Al-Mn alloys stay at **≤1.25 %** (P) or **≤1.2 %** (K), because Fe lowers Mn solubility and coarse **primary Al6Mn** would form, with a "disastrous effect on local ductility" [P p.129; K p.27]. Davis: only up to **~1.5 %** Mn can be added effectively [D p.360]. In 3xxx Mn is the main addition up to 1.25 % [D p.382].
- **Primary-intermetallic limit.** Fe + Mn must stay **< ~2.0 % in 3003** and **< ~1.7 % in 3004** to prevent primary (Fe,Mn)Al6 in the casting system or ingot sump [D p.383]. The combined Mn + Fe + Cr + other transition metals must be limited for the same reason [D p.383].
- **Solidification and homogenisation phases.**
  - During DC casting some Mn forms **Al6(Mn,Fe)** and cubic **α-Al12(Fe,Mn)Si** by eutectic reactions. The rest stays supersaturated and precipitates during ingot preheat as **Al12(Mn,Fe)Si and Al6(Mn,Fe) dispersoids**. These strengthen the alloy and control the recrystallised grain size [D p.388].
  - Homogenisation also converts Al6(Fe,Mn) to the harder **α-Al12(Fe,Mn)3Si** by reaction with dissolved Si, which matters for can stock [P p.107].
  - In Cu-bearing alloys Mn forms **Al20Cu2Mn3** [D p.369, 388–389].
- **Mn left in solid solution.** Only **0.2–0.3 % Mn** typically stays in solid solution after preheat and hot processing, because Mn precipitates as Al6Mn [P p.30]. Mn in solid solution is a **highly effective** strengthener in binary alloys, but contributes less in commercial alloys because it is largely precipitated [D p.368].
- **Supersaturation vs cooling rate.** Rapid DC solidification retains Mn and Cr far above equilibrium solubility [D p.369]. Twin-roll and other continuous casting (10²–10³ °C/s vs 1–5 °C/s for DC) gives much higher supersaturation of slow diffusers such as **Fe**, and different properties at the same composition [P p.99, 102].
- **Diffusion rates.** D at 500 °C: **Mn 5×10⁻¹³**, Cu 5×10⁻¹⁰, Mg and Si 1×10⁻⁹ cm² s⁻¹ [P p.105]. Mn is **~1000× slower than Cu**, which is why Mn dispersoids resist dissolution and coarsening.
- **Dispersoid nucleation.** Slow heating (e.g. **75 °C/h**) to the homogenisation temperature gives a fine, uniform dispersion. The dispersoids nucleate heterogeneously on transient precipitates formed during the slow heat-up [P p.106, Fig 3.8 for Al6Mn in Al-Zn-Mg]. Electrical conductivity is "an effective measure of the completeness" of preheat precipitation [D p.370].
- **Recrystallisation and grain control.** Mn raises the recrystallisation temperature, promotes a fibrous structure in hot working, slows recovery and prevents grain growth as a dispersoid [D p.382]. Mn also **corrects the shape of acicular or platelike Fe constituents** and reduces their embrittling effect [D p.382].
- **Calcium.** 0.2 % Ca alters the recrystallisation of 3003 [D p.372].
- **Strength level.**
  - 3xxx is about **20 % stronger than 1xxx** [D p.360]. Annealed 3003 UTS is ~110 MPa vs 90 MPa for 1100, from dispersion hardening by fine Mn intermetallics [P p.129].
  - Dwight instead calls 3xxx "**half as strong again** as pure aluminium", with UTS "up to 200 N/mm² or more" and very high corrosion resistance [DW §4.2.1(b)]. The two statements fit different baselines (see §11). Against 1100, the K data give ~+20 % (3003-O 110 vs 1100-O 90; H18 200 vs 165 MPa [K p.44–45]). Dwight compares with purer 1xxx (top UTS 150 vs 200 MPa [DW Table 4.4]).
  - Mg adds solid-solution strength: 3105 (Al-0.55Mn-0.5Mg) and 3004 (O-temper UTS 180 MPa) [P p.129–130].
  - **Davis compares Mn and Mg two ways:** "about **0.8 % Mg** = **1.25 % Mn** as hardener" [D p.361], but in 13 mm Al-Mg-Mn plate "**Mn is about twice as effective as Mg**" (Mg adds ~35 MPa UTS per 1 %) [D p.380]. See §11.
- **Work hardening and forming.**
  - The work-hardening curves of 3003 resemble those of 1100 and 5050/5052 [P p.34–35, Fig 2.6].
  - **3003 draws better in the cold-worked than in the annealed condition** [P p.34]. For can-stock 3004, rolled sheet out-forms annealed sheet, the reverse of 5052 [P p.38].
  - The cube texture nucleates at transition bands, and the rolling vs cube texture balance controls **earing**: 45° ears for a rolling texture; 0/90° ears for a cube texture [P p.39–40].
  - The coarse constituents in can stock are useful [P p.78]. *(General knowledge: hard α-particles clean the dies during ironing. Polmear's canstock §3.6.5 is still not available; the 2026-10-12 full download of P failed, see §1.)*
  - **Earing, as defined by the AA** [K p.196–197]: ears form "in groups of four or eight with the peaks … at 45° and/or at 0 and 90° to the rolling direction". **Degree of earing (%) = 100 × (mean peak height − mean valley height) / mean valley height.** The cause is "nonuniform directional properties … and/or … improperly adjusted tooling". See §4.11.
- **Corrosion.**
  - Very high resistance. The Al6(Mn,Fe) and Al12(Mn,Fe)3Si particles have **almost the same potential as the matrix**, so they do not initiate attack; pitting is the main mode [D p.402].
  - **MnAl6 at −0.85 V equals pure Al** [P Table 2.5], and Al6Mn **dissolves Fe**, reducing its harm [P p.75]. (Potential signs restored.)
  - **Small Cu (0.05–0.2 %)** makes corrosion more general and **retards perforation by pitting**, although total weight loss increases [P p.73]. This is relevant to 3003's Cu 0.05–0.20 window.
  - 3xxx is immune to SCC [P p.90]. Clad with **7072 (Al-1Zn)** [P p.108].
- **Brazing (heat-exchanger route).**
  - 3003 melts at 643–654 °C, rated A, and is "used both plain and as the core of brazing sheet". 3004 melts at 629–652 °C, rated B [D p.414 Table 10].
  - Alloys with a **solidus >595 °C** are readily brazed with Al-Si fillers (7–12 % Si) [D p.414]. Brazing runs at **560–610 °C** (furnace ~595 °C) [P p.167–168].
  - **CAB** (nitrogen + non-corrosive K-Al-F flux): the flux is **inactivated by Mg**, so the filler must be Mg-free and the base alloys low in Mg. **Vacuum brazing** needs Mg in the filler to disrupt the oxide [P p.168].
  - **Automotive heat-exchanger alloys for CAB** [P p.168]:
    - Tubes **3005**: Al-1.2Mn-0.40Mg-0.35Fe-0.30Si-0.15Cu.
    - Fins **FA6815**: Al-1.6Mn-1.5Zn-0.85Si-0.25Fe-0.15Zr.
    - Headers **FA7827**: Al-0.7Si-0.45Mg-0.3Cu-0.25Fe-0.15Ti.
    - Strength comes from solid solution + dispersion hardening, "supplemented in some instances by precipitation hardening" [P p.169].
    - *(General knowledge, not stated by P: Zn in fin alloys makes the fin anodic, so it protects the tube sacrificially; this is consistent with the Zn effect on potential in [P p.73].)*
  - Solderability: 3003 excellent, 3004 good [D p.415].
- **Applications.** 3003 is the "most popular general-purpose alloy", used for fin stock, cooking utensils, pressure vessels and chemical equipment. 3004 for sheet and containers; 3105 for siding [D p.358]. 3003 for foil and roofing [P p.129]. 3004 for beverage cans, "the largest single use of the metals aluminium and magnesium" [P p.130]. 3xxx is "among the best for brazing and soldering" [K p.27].
  - *Kaufman Ch. 6 (full-text pass)* [K p.90, 93–95, 116, 118]:
    - Profile: high formability and corrosion resistance at medium strength; typical UTS 110–285 MPa; readily joined by all commercial methods.
    - **3104 is a modification of 3004.** "Alloy 3004 and its modification 3104 are the principals for the bodies of drawn and ironed" beverage cans, in excess of **1.6 billion kg (3.5 billion lb) per year**. This makes 3004/3104 "the largest volume alloy combination in the industry".
    - **3002** for automotive radiators; **3003** for power-plant heat-exchanger tubing and automotive A/C tubes; 3003 for cooking utensils, chemical equipment and builders' hardware.
    - **3105** "a principal for roofing and siding"; building sheet and siding in 3005, 3105 and 5005.
  - *Dwight* [DW §4.2.1(b)]: in construction the main use is **fully hard profiled cladding sheet**, plus 3xxx strip for welded tube (e.g. irrigation pipe).

**Composition (wt %; max unless a range)**

| Alloy | Si | Fe | Cu | Mn | Mg | Zn | Other | Source |
|---|---|---|---|---|---|---|---|---|
| 3003 | 0.60 | 0.70 | 0.05–0.20 | 1.0–1.5 | — | 0.10 | — | [P p.121] |
| 3003 nominal | — | — | 0.12 | 1.2 | — | — | — | [K p.12; D p.356] |
| 3004 | 0.30 | 0.70 | 0.25 | 1.0–1.5 | 0.8–1.3 | 0.25 | — | [P p.121]; nominal 1.2Mn-1.0Mg [K p.12] |
| 3005 | 0.60 | 0.70 | 0.30 | 1.0–1.5 | 0.20–0.6 | 0.25 | 0.10 (Cr or Ti; column ambiguous) | [P p.121]; nominal 1.2Mn-0.40Mg [K p.12] |
| 3005 (CAB tube, as quoted) | 0.30 | 0.35 | 0.15 | 1.2 | 0.40 | — | — | [P p.168] |
| 3105 | 0.60 | 0.70 | 0.30 | 0.3–0.8 | 0.20–0.8 | 0.40 | Cr 0.20, Ti 0.10 | [P p.121]; nominal 0.55–0.6Mn-0.5Mg [K p.12; D p.356] |
| 3103 | — | — | — | nominal 1.2 | — | — | — | [DW Table 4.5, Table 4.8] (verified in the full-text pass; DW gives only the nominal Mn) |
| FA6815 (fin) | 0.85 | 0.25 | — | 1.6 | — | 1.5 | Zr 0.15 | [P p.168] |
| **3102, 3207, 3104** | **not given in any source read** | | | | | | | 3104 is named as "a modification of 3004" for can bodies [K p.93], with no composition; 3104-H19 appears only in [S]. 3102 and 3207 appear in neither K nor DW (full text searched). |

**Design levers (3xxx), as stated by the sources**
- Mn content limited by Fe through the primary-phase ceiling [P p.129; D p.383].
- Si level (α vs Al6 constituent, and Mn solubility) [P p.107; D p.388].
- Homogenisation heating rate and temperature for the dispersoid population [P p.105–106]. The 3003 ingot micrographs show the two extremes: a long soak at 600 °C spheroidises the constituents, and slow cooling from 600 to 450 °C precipitates fine Al-Mn-Fe from supersaturation [K p.131] (§4.11).
- Mg for solid solution (3004/3005/3105), limited by CAB brazing [P p.168].
- Cu 0.05–0.2 for a general rather than pitting corrosion mode [P p.73].
- Zn for galvanic grading of fins vs tubes [P p.168; P p.73].
- Zr (FA6815) for recrystallisation control [P p.168; D p.390].
- Temper route (H1x vs H2x) for the strength–elongation trade-off [DW §4.1.5].

**Pitfalls**
- Primary Al6(Fe,Mn) [P p.129; D p.383].
- Coarse constituents reduce fracture strain (Fe, Ni and Mn particles promote voids) [D p.408]. **Primary (large, angular) Mn-bearing particles** survive into 3003-F hot band next to the small eutectic ones, together with oxide stringers from ingot inclusions [K p.131]. In 5083, brittle "(Fe,Mn)3Al12" particles (as extracted; the Si subscript may have been lost) break up during cold rolling and leave voids [K p.132].
- Earing [P p.39; K p.196–197].
- Coarse grains give **orange peel** (surface roughening on formed products when large grains are present) [K p.210]. This is the upper-bound grain-size risk for slugs (§4.11).
- Higher Mg degrades CAB brazeability [P p.168].

### 4.3 4xxx — Al-Si (filler and braze cladding; brief)
- **Si content and use.** Up to **12 % Si** lowers the melting range without brittleness. Used for weld wire and brazing sheet [D p.360–361]. Brazing cladding holds up to 12 % Si [D p.384].
- **Hot shortness.** High-purity Al-Si is hot short up to 3 % Si, most critically at **0.17–0.8 % Si** [D p.384].
- **Heat-treatability asymmetry.** A little Mg makes any Si-bearing alloy heat treatable, but excess Mg sharply reduces Mg2Si solubility [D p.384].
- **Anodising.** Anodises grey to black (~5 % Si) [D p.361, 384].
- **Forging alloy.** 4032 (12.2Si-0.9Cu-1.0Mg-0.9Ni) has low thermal expansion and is used for forged pistons [K p.12; D p.361].
- **Brazing fillers (AWS).** BAlSi-2 to BAlSi-11 contain 6.8–13 % Si. Solidus 521–577 °C, brazing at 571–621 °C. The Mg-bearing grades (BAlSi-6 to -11) are for vacuum brazing [D p.415 Table 11].

### 4.4 5xxx — Al-Mg (±Mn, Cr)
**Metallurgy**
- **Mg solubility.** Maximum **17.4 % at 450 °C**; **~2 % at 20 °C** [P Table 2.1]. Wrought alloys carry **≤5.5 % Mg** [D p.380]; commercial wrought range 0.8 to >5 % [P p.130].
- **Strength from Mg.**
  - Mg is the most effective strengthener on a weight basis because of its high solubility. Annealed sheet with up to **6 % Mg reaches YS ≤175 MPa** [P p.30].
  - In O-temper 13 mm plate, Mg adds **~35 MPa UTS per 1 %** [D p.380].
  - Mg in solid solution sharply raises the work-hardening rate, and the rate grows with Mg content [P p.130]. 5456-H19 approaches **YS ~500 MPa** [P p.130]; heavily cold-worked Al-Mg exceeds **400 MPa** [P p.34].
  - Adding a little Mg causes a **large initial drop in elongation** [D p.408].
- **No precipitation hardening.** Al3Mg2 (fcc) is hard to nucleate, so binary Al-Mg is not commercially heat treatable [D p.389]. The GP solvus lies below room temperature for <5 % Mg, so there is **no hardening below 5–6 % Mg** [P p.47, 57].
- **β phase.** Mg5Al8, "formerly Mg2Al3" [P Table 2.3]; also written Al8Mg5, Mg5Al3 [D p.380, 402–403] or Al3Mg2 [D p.389]. Fcc, a = 2.824 nm, incoherent; forms as plates or laths in grain boundaries [P p.57]. It is **strongly anodic: −1.24 V** vs **−0.88 V** for Al-5 % Mg solid solution [P Table 2.5].
- **Sensitisation, IGC and SCC.**
  - **>3–4 % Mg:** β precipitates in slip bands and grain boundaries, giving **IGC and SCC**. It forms slowly at room temperature but faster after **heavy cold work or at higher temperature** [P p.130].
  - **≥~3 % Mg** with an almost continuous grain-boundary Al8Mg5 film leads to **exfoliation or SCC**. The corrective tempers put the precipitate mostly *inside* the grains [D p.402–403].
  - **>3 % Mg:** not recommended for elevated-temperature service; use 5052, 5454 or **5754** instead [K p.28].
  - **>~3.5 % Mg above ~65 °C:** limit cold work and temperature [D p.361]. 5083 and 5456 are restricted to **<65 °C** in pressure vessels and welded structures [D p.358].
  - Al-Mg alloys with **<3 % Mg are immune to SCC** [P p.90].
- **Mn and Cr additions.**
  - They raise the recrystallisation temperature and the strength at a given Mg level. This allows **lower Mg** and so avoids β: **5454 (2.7Mg-0.7Mn-0.12Cr) ≈ the properties of a binary alloy with ~4 % Mg** [P p.130].
  - Mn makes Mg-phase precipitation "more general throughout the structure" and gives more stability for a given strength [D p.380].
  - Cr dispersoid: Al18Mg3Cr2 (fcc) in 5xxx [D p.389–390]; Al12Mg2Cr is a "submicroscopic precipitate" [D p.403].
  - Cr ≤0.35 %; more than that gives coarse constituents, and the limit falls as total transition metals rise [D p.373].
- **Instabilities.**
  - **Age softening** of work-hardened alloys comes from localised recovery; H3x stabilisation is the cure, and it also reduces β precipitation [P p.130].
  - **Lüders lines** form in annealed or solution-treated Al-Mg. **Portevin–Le Chatelier serrations** appear during stretching. Avoid them by forming strain-hardened sheet or forming above **150 °C** [P p.40–41; D p.380]. Lüders lines limit Al-Mg alloys to inner panels [P p.131].
  - Mg (and Cu) **strain-age**: work hardening rises at low strain and falls at large strain [D p.408].
- **Melt and casting issues.**
  - Na traces cause hot cracking; add **Bi 20–200 ppm** (or Sb) [D p.371, 380].
  - Be (wrought products) reduces oxidation and discolouration. It is held to **8 ppm** in filler and not used in food contact [D p.371].
- **Fatigue.** Al-5Mg with Mg in solution has a high fatigue ratio; the endurance limit is ≈ the proof stress [P p.88].
- **Joining.**
  - Excellent weldability. The weld strength of NHT alloys ≈ their **annealed** strength, whatever the prior temper, which is why the alloys strong in O (5083) are popular [P p.163]. Filler 5356 = Al-5Mg-0.1Cr-0.1Mn [P p.164].
  - High-Mg alloys (5083, 5086, 5154, 5456) are **hard to flux-braze** (poor wetting, filler penetration) [D p.413]. 5052 brazeability is C [D p.414].
  - Solderability: alloys with **>1 % Mg** cannot be soldered with organic flux, and >2.5 % Mg is difficult; molten solder penetrates the grain boundaries above **0.5 % Mg** [D p.415]. 5754-H111 brazability is "poor" [A57 p.2].
- **Zn additions.** Up to 1.5 % Zn (5059) raises strength and corrosion resistance, but may cause **localised HAZ corrosion** in welds [P p.130–131].

**Composition (wt %)**

| Alloy | Si | Fe | Cu | Mn | Mg | Cr | Zn | Ti / other | Source |
|---|---|---|---|---|---|---|---|---|---|
| 5005 | 0.30 | 0.70 | 0.20 | 0.20 | 0.50–1.1 | 0.10 | 0.25 | — | [P p.121] |
| 5052 | 0.25 | 0.40 | 0.10 | 0.10 | 2.2–2.8 | 0.15–0.35 | 0.10 | — | [P p.121] |
| 5454 | 0.25 | 0.40 | 0.10 | 0.50–1.0 | 2.4–3.0 | 0.05–0.20 | 0.25 | 0.20 | [P p.121] |
| **5754** | 0.40 | 0.40 | 0.10 | ≤0.50 (Mn+Cr 0.10–0.60) | 2.60–3.60 | ≤0.30 | 0.20 | Ti 0.15 | [A57 p.1, BS EN 573-3:2009] |
| 5083 | 0.40 | 0.40 | 0.10 | 0.40–1.0 | 4.0–4.9 | 0.05–0.25 | 0.25 | 0.15 | [P p.121]; nominal 4.4Mg-0.7Mn-0.15Cr [K p.12] |
| 5383 | 0.25 | 0.25 | 0.20 | 0.70–1.0 | 4.0–5.2 | 0.25 | 0.40 | 0.15, Zr 0.20 | [P p.121] |
| 5059 | 0.45 | 0.50 | 0.25 | 0.60–1.2 | 5.0–6.0 | ? | ? | Zr 0.05–0.20 | [P p.121]. Extraction gives "0.20 0.25 0.20" for the Zn/Cr/Ti columns; the deliberate Zn range (up to 1.5 %, [P p.130–131]) seems lost, so the values are not assigned |
| 5086 | 0.40 | 0.50 | 0.10 | 0.20–0.7 | 3.5–4.5 | 0.05–0.25 | 0.25 | 0.15 | [P p.121] |
| 5182 | 0.20 | 0.35 | 0.15 | 0.20–0.50 | 4.0–5.0 | 0.10 | 0.25 | 0.10 | [P p.121] |

**Design levers:** Mg level (strength vs β sensitisation; threshold ~3 %); Mn and Cr to substitute for Mg; H3x/H116/H321 tempers; Zr/Sc [P p.52–53]. **Pitfalls:** sensitisation, Lüders lines, age softening, HAZ annealing, brazing and soldering limits.

### 4.5 6xxx — Al-Mg-Si (±Cu, Mn, Cr)
**Metallurgy**
- **Stoichiometry and solubility.** Mg2Si forms a quasi-binary section with Al [K p.28; P p.62]. The balanced ratio is **Mg:Si = 1.73:1 by weight** [D p.380; P p.138]. Mg and Si are each up to **1.5 %**. Maximum Mg2Si solubility is **1.85 %**, falling with temperature [D p.380].
- **Three alloy groups** [D p.381; P p.138–141]:
  1. **Balanced, Mg + Si ≈ 0.8–1.2 %** [P p.138], or ≤1.5 % [D p.381]. Example **6063 (~1.1 % Mg2Si)**. Solution treatment just over **500 °C**. **Low quench sensitivity**, so it is **press-quenched**: water spray or trough, or **air cooling for sections <3 mm**. Then aged at 160–190 °C [D p.381; P p.140].
  2. **Mg + Si ≥1.4–1.5 %, ±0.3 % Cu** (6061: 0.25 Cu + 0.2 Cr to offset Cu's corrosion effect). About **70 MPa stronger** in T6 than group 1. **Quench sensitive**, so it needs a separate solution treatment and water quench [D p.381; P p.140].
  3. **Excess Si** (6009, 6010, 6351, 6082-type). **0.2 % excess Si raises the strength of a 0.8 % Mg2Si alloy by ~70 MPa**; more excess helps less [D p.381]. Excess Si refines Mg2Si and also precipitates as Si [P p.140].
     - Downside: Si segregates to grain boundaries and causes grain-boundary fracture in recrystallised structures [D p.381–382; P p.140–141].
     - Mn, Cr or Zr counter this by preventing recrystallisation (6151 with Cr, 6351 with Mn) [D p.382; P p.141].
- **Excess Mg** helps only at low Mg2Si, because it **reduces Mg2Si solubility** [D p.381, 384].
- **Precipitation sequence** [P Table 2.3 p.58–59; symbols restored]: Mg and Si clusters and co-clusters → GP zones (solvus normally above the ageing temperature) → **β''** (monoclinic needles along ⟨100⟩, the **main strengthener, composition ≈ MgSi**) → **β'** (hexagonal rods, ≈Mg1.7Si) and **B'** (laths, favoured by high Si:Mg) → **β-Mg2Si** (fcc platelets). With Cu, the **Q phase Al5Cu2Mg8Si6** precipitates as well [P p.141]; it is written Al4CuMg5Si4 in [D p.388].
- **The Mg:Si ratio of β'' is ~1:1, not 2:1** [P p.45, 66, 141]. "Balanced" alloys therefore have **surplus Mg**. **6060 (Al-0.35Mg-0.5Si)** matches 6063 (Al-0.5Mg-0.4Si) in properties with **up to 20 % faster extrusion** [P p.141].
- **Room-temperature delay before artificial ageing (natural pre-ageing):**
  - **>1 % Mg2Si:** a 24 h delay costs **up to 10 %** of tensile properties.
  - **<0.9 % Mg2Si:** the delay can **raise** properties. The cause is solute–vacancy clustering at room temperature, with the GP solvus above 170 °C in richer alloys [P p.141–142; P p.63–64].
  - **~0.25 % Cu** lessens the penalty [P p.142].
  - Industrial fix for 6016 sheet: a short heat treatment right after the quench (**T4\***) gives stable GP nuclei and a fast **paint-bake response** [AR p.14].
- **Quench sensitivity.** Mg2Si needles nucleate on Mn-bearing dispersoids during slow quenching and deplete the fine precipitate around them [P p.113, Fig 3.14]. Ranking: **Cr > Mn > Zr** [P p.112].
- **Corrosion.**
  - Mg2Si is anodic but has a negligible potential effect in solution or as a fine precipitate (Al-Mg-Si solid solution −0.83 V) [D p.403; P Table 2.5].
  - **Cu >0.5 %** brings IGC in T4/T6 (no exfoliation or SCC) [D p.403]. Cu-rich 6013/6111 are prone to IGC through Cu/Si-depleted, anodic precipitate-free zones (PFZs); remedied by **T78** overageing [P p.141].
  - **Excess Si or cathodic impurities raise IGC susceptibility** [D p.403].
  - SCC is only "rarely" observed [P p.90].
- **Other element effects.** **Ca lowers age hardening** in Al-Mg-Si [D p.372]. Pb + Bi (6262) for machinability [D p.382].
- **Welding.** The HAZ drops to ~T4 strength after welding [P p.163]. Weldable with 4043 or 5356 [P p.164].

**Composition (wt %; [P p.124–125] unless noted)**

| Alloy | Si | Fe | Cu | Mn | Mg | Cr | Zn | Ti | Other |
|---|---|---|---|---|---|---|---|---|---|
| 6060 | 0.30–0.6 | 0.10–0.3 | 0.10 | 0.10 | 0.35–0.6 | 0.05 | 0.15 | 0.10 | |
| 6063 | 0.20–0.6 | 0.35 | 0.10 | 0.10 | 0.45–0.9 | 0.10 | 0.10 | 0.10 | nominal Si 0.40, Mg 0.7 [K p.13] |
| 6061 | 0.40–0.8 | 0.70 | 0.15–0.40 | 0.15 | 0.8–1.2 | 0.04–0.35 | 0.25 | 0.15 | nominal 0.6Si-0.28Cu-1.0Mg-0.20Cr [K p.13] |
| **6082** | 0.70–1.3 | 0.50 | 0.10 | 0.40–1.0 | **0.60–1.0 (P)** / **0.6–1.2 (DW)** | 0.25 | 0.20 | 0.10 | conflict noted; DW gives the EN spec [DW §4.1.2] |
| 6005 | 0.60–0.9 | 0.35 | 0.10 | 0.10 | 0.40–0.6 | 0.10 | 0.10 | — | |
| 6016 | 1.0–1.5 | 0.50 | 0.20 | 0.20 | 0.25–0.6 | 0.10 | 0.20 | 0.15 | |
| 6111 | 0.60–1.1 | 0.40 | 0.50–0.9 | 0.10–0.45 | 0.50–1.0 | 0.10 | 0.15 | 0.10 | |
| 6013 | 0.60–1.0 | 0.50 | 0.60–1.1 | 0.20–0.8 | 0.80–1.2 | 0.10 | 0.25 | 0.10 | |

**Design levers:** Mg2Si level; Mg:Si ratio (lean-Mg for extrudability); excess Si plus a recrystallisation inhibitor; Cu with T78; choice of dispersoid former for quench sensitivity (Zr < Mn < Cr) [P p.112]; ageing delay and pre-ageing; T5 vs T6 route.

### 4.6 7xxx — Al-Zn-Mg(-Cu)
- **Ageing potential.** The Al-Zn-Mg system has "the greatest potential of all aluminium alloys for age-hardening" [P p.142]. Zn alone gives little solid-solution or work hardening [D p.389; P p.30]. Zn 1–8 % [D p.362]. MgZn2 gives "a far greater response to heat treatment than … binary Al-Zn", especially at **3–7.5 % Zn** [D p.385–386].
- **Precipitation sequence** [P Table 2.3 p.59; symbols restored]: GP zones (GP[I] spherical, 1–1.5 nm; GP[II] Zn-rich {111} discs) → **η'** (hexagonal, semi-coherent; Mg:Zn **≈1:1–1:1.15**, not 1:2 [P p.66]) → **η-MgZn2**. At high Mg:Zn ratios, or ageing above ~190 °C: **T' → T-Mg32(Al,Zn)49** [P p.59; D p.389].
  - In Al-Zn-Mg-Cu, Cu and Al substitute in Mg(Zn,Cu,Al)2, and Al2CuMg may also form [D p.389].
  - Plates on {111} make 7xxx stronger than {100}-hardened Al-Cu: YS >600 MPa [P p.60].
- **Weldable (low-Cu) 7xxx** [P p.142–144]:
  - Composition: **3–7 % Zn, 0.8–3 % Mg (Zn + Mg = 4.5–8.5 %)**, 0.1–0.3 % Cr/Mn/Zr, **Cu <0.3 %** (to limit weld hot cracking and corrosion).
  - Natural ageing restores the weld: ~**320 MPa UTS without further heat treatment**, and the HAZ YS is up to 2× that of Al-Mg or Al-Mg-Si welds.
  - SCC rules: **Zn + Mg <6 %** for adequate SCC resistance; optimum **Zn:Mg ≈ 2.7–2.9** [P p.143–144]. Davis: adjust Zn:Mg "closer to 3:1" [D p.386].
  - Process controls: air cooling after solution treatment; Zr (0.08–0.25 %) instead of Cr/Mn for low quench sensitivity; T73-type duplex ageing [P p.144].
  - Failure mode in welds: SCC in the partially melted "**white zone**". The weld bead is *cathodic*, the reverse of other Al alloys [P p.144–146].
- **High-strength 7xxx (Al-Zn-Mg-Cu):**
  - **Cu** speeds ageing and raises quench sensitivity. It **lowers general corrosion resistance but raises SCC resistance** [D p.387; D p.404], and it allows ageing at higher temperature (T73) without large strength loss [D p.404].
  - **Upper limit on Cu:** large Al2CuMg particles hurt toughness. Modelling gives **Cu + Mg ≈ 3.6** for ~6 % Zn [P p.149].
  - **Trend in Zn:Mg ratio:** **2.25 (7075) → 2.7 (7050) → 3.9 (7055) → 5.0 (7085)**. Fe, Si, Mn and Cr are each cut to ≤0.1 %. 7085 has very low quench sensitivity, so **~150 mm** sections can be heat treated [P p.151].
  - **SCC controls:** overageing; cooling rate after solution treatment; an unrecrystallised structure (Zr); Cu or Cr additions; Zn:Mg ratio [D p.386].
  - **T73 performance:** 7075-T73 short-transverse specimens remain **uncracked at 300 MPa**, whereas T6 fails at 50 MPa [P p.147]. RRA (T77): 5 min to 1 h at 200–280 °C, then re-age [P p.149].
  - **Low-melting phases in 7075** (MgZn2, Al2Mg3Zn3, Al6CuMg4) must be dissolved during homogenisation [AR p.10–11].
- **Composition and properties.**
  - **7020:** Si 0.35, Fe 0.40, Cu 0.20, Mn 0.05–0.5, Mg 1.0–1.4, Zn 4.0–5.0, Cr 0.10–0.35, Zr 0.08–0.20, (Zr+Ti) 0.08–0.25 [P p.125]. Table 3.8: Zn 4.3, Mg 1.2, Zn+Mg 5.5, **Zn/Mg 3.6** [P p.143].
  - **7075:** Si 0.40, Fe 0.50, Cu 1.2–2.0, Mn 0.30, Mg 2.1–2.9, Zn 5.1–6.1, Cr 0.18–0.28 [P p.125]; nominal 5.6Zn-2.5Mg-1.6Cu-0.23Cr [K p.13].
  - **7072:** Zn 1.0, used for cladding and fins [K p.13; P p.129].

### 4.7 2xxx — Al-Cu(-Mg) (brief, for completeness)
- **Cu solubility.** Maximum **5.65 % at 548 °C** [P Table 2.1; AM slide 4]. Strengthening peaks at **4–6 % Cu** [D p.373].
- **Precipitation sequence** [P Table 2.3 p.57; symbols restored]: GP zones (Cu monolayers on {100}) → **θ''** → **θ'-Al2Cu** (semi-coherent {100} plates on dislocations) → **θ-Al2Cu**.
- **Cu:Mg ratio and the main strengthening phase.**
  - θ'-type for <1 % Mg (2014, 2219); **S-Al2CuMg** for >1 % Mg (2024); Mg2Si for low-Cu alloys [D p.401].
  - As little as **~0.5 % Mg** changes the ageing characteristics [D p.374].
  - With 0.1 at.% Ag (0.4 wt %): **Ω** forms at high Cu:Mg (Al-4Cu-0.3Mg), **X** at medium (Al-2.5Cu-1.5Mg) and **Z** at low (Al-1.5Cu-4Mg) [P Table 2.2, p.52]. Ω gives creep resistance up to ~200 °C [P p.132–133].
  - Al-Cu-Mg shows rapid "**cluster hardening**", 60–70 % of the total response within 60 s [P p.64].
- **Fe in 2xxx.** In Al-4Cu-0.5Mg, **Fe ≥0.5 % ties up Cu as Cu2FeAl7** unless Si is present to form αFeSi [D p.374–376]. **Fe + Si <0.5 %** roughly **doubles K_IC** compared with >1.0 % [P p.81].
- **Corrosion and SCC.** Lowest corrosion resistance of the series; sheet is clad [D p.359, 400]. T3/T4 are prone to SCC in the short-transverse direction [K p.27; P p.137].

### 4.8 8xxx — Fe, Ni, Sn, Li and other alloys
- **Strengthening.** Dilute Fe(-Mn, Si) alloys get **30–40 MPa from dispersion hardening**, plus **2–10 MPa YS (5–20 MPa UTS) from solid solution** [P p.131].
- **Named alloys** [P p.121, 131]:
  - **8011** (Al-0.75Fe-0.7Si): bottle caps (good deep drawing).
  - **8006** (Al-1.6Fe-0.65Mn): foil and **heat-exchanger fin stock**.
  - **8001** (Al-1.1Ni-0.6Fe): nuclear water service; its mechanical properties resemble 3003.
  - **8280/8081**: Al-Sn bearing alloys.
- **Fe-Mn near the ternary eutectic (8006).** Fine grain stabilised by a dispersed Fe-rich phase gives good room-temperature strength and ductility and retained elevated-temperature strength [D p.379].
- **Compositions** (wt %, max unless a range) [P p.121]:
  - 8006: Si 0.40, Fe 1.2–2.0, Cu 0.30, Mn 0.30–1.0, Mg 0.10, Zn 0.10.
  - 8011: Si 0.50–0.9, Fe 0.6–1.0, Cu 0.10, Mn 0.10, Mg 0.05, Zn 0.10, Cr 0.05, Ti 0.08.
  - 8017, 8030, 8176 and 8177 are conductor alloys (Fe 0.35–0.7) [K p.13]. 8176-H24 = 160/95 MPa, 15 % [K p.49].
- **PM and Li alloys.** 8019 (Al-Fe-Ce) and 8009 (Al-Fe-V-Si) are powder-metallurgy alloys for elevated-temperature dispersion strengthening. 8090 is Al-Li (helicopters) [D p.363; P p.159].
- **Kaufman Ch. 6** [K p.105–107]: 8xxx covers "lesser-used alloying elements such as iron, nickel, and lithium". Profile: high conductivity, strength and hardness; typical UTS **120–240 MPa**. "Iron and nickel provide strength with little loss in electrical conductivity", hence the conductor family represented by **8017**. Kaufman's bullet list labels the whole series "heat treatable", which contradicts his own p.26 (8017 and 8040 are NHT; only Al-Li 8090 is heat treatable). Treat the bullet as an error.
- **8079 and 8111** are still **not covered** by any source read. K and DW were searched in full on 2026-10-12.

### 4.9 Al-Li alloys (2xxx/8xxx)
- **Basic effects.** Li solubility is ~4 % (16 at.%) at 610 °C; each 1 % Li gives −3 % density and +6 % E; specific stiffness rises up to 25 % [P p.153].
- **Strengthening phases.** δ'-Al3Li (L12, coherent, low misfit, easily sheared, so strain localises). Co-precipitated T1-Al2CuLi ({111}) and S' homogenise slip. T8 tempers are used because T1 and S' nucleate on dislocations [P p.153–157].
- **Example alloys.** 2090 (2.2Li-2.7Cu-0.12Zr); 8090 (2.4Li-1.3Cu-0.9Mg-0.10Zr); 2195 (1.0Li-4.0Cu-0.5Mg-0.4Ag-0.12Zr); 2099 (2.7Cu-1.8Li-0.7Zn-0.3Mg-0.3Mn-0.08Zr). Specific gravity 2.53–2.60; E 78–82 GPa [P p.154–158].
- **Pitfalls.**
  - Low short-transverse toughness.
  - **Alkali impurities (Na, K) >3–5 ppm** form brittle grain-boundary "islands"; vacuum refining brings them to <1 ppm [P p.158].
  - Cost ~3× that of conventional high-strength alloys [P p.159].
  - Even <5 ppm Li impurity in ordinary Al can cause "blue corrosion" of foil [D p.380].

### 4.10 Foil, can stock, impact slugs and conductors: application map (added in the full-text pass)
Polmear's dedicated sections (§3.6.4 foil, §3.6.5 canstock, §3.6.9 conductors) are **still unread** because the download failed (§1). This map is assembled from K Ch. 6, the K terminology appendix, DW and the parts of P already read.

| Product | Alloys named | Source |
|---|---|---|
| Food foil | **1175** (99.75 % Al); household foil "1100 or similar"; pouches 1060 or 1100 | [K p.89, 118] |
| Other foil | 1145 (foil), 1199 (electrical foil), 3003, 3005 ("high-strength foil"), **8006** (Al-1.6Fe-0.65Mn), 8011 (bottle caps) | [P p.122, 129, 131] |
| Beverage-can body (drawn and ironed) | **3004 and its modification 3104**; 3004-H19 is the textbook H19 temper | [K p.18, 63, 93, 118] |
| Can end | **5182** | [K p.96, 101, 118] |
| Impact-extruded parts | No alloy or temper named in K or DW (definitions only, below) | [K p.203, 217] |
| Conductor wire / bus | **1350** (62 % IACS guaranteed); 6201 (high-strength wire); 6101 (bus); 8017 family (Fe/Ni, little conductivity loss) | [K p.88, 99, 107, 115–116] |
| Heat exchangers | 3003 (power-plant tubing, auto A/C tubes); 3002 (radiators); brazing sheet ("12-O" in the caption) = **3003 core clad on both sides with 4343** filler | [K p.94, 116, 163] |
| Building sheet | 3005, 3105, 5005; 3xxx fully hard profiled cladding | [K p.116; DW §4.2.1(b)] |

- **Definitions (AA terminology)** [K p.199, 203, 211, 217]:
  - *Foil* is a rolled product <0.15 mm thick (US), or ≤0.20 mm in Europe. It is supplied annealed, in an intermediate temper or hard. A *pinhole* is a minute hole in foil.
  - **Impact**: "a part formed in a confining die from a metal **slug**, usually cold, by rapid single-stroke application of force through a punch, causing the metal to flow around the punch and/or through an opening in the punch or die".
  - **Slug**: "a metal blank for forging or impacting".
- **Recycling.** Aluminium alloys "may be recycled directly back into the same high-quality products, such as rigid containers, sheet" [K p.4]. Casting alloy 332.0 "can be made almost exclusively from recycled scrap" [K p.111–112]. Polmear's treatment of recycling and Fe/Si accumulation was not reached.

### 4.11 3xxx/1xxx constituents, homogenisation, annealing and earing (added in the full-text pass)
**Source statements**
1. **Homogenisation of 3003 DC rolling ingot (micrographs)** [K p.131, Fig. 40]:
   - *As cast:* angular Al-Mn-Fe particles inside the cast grains and at grain boundaries.
   - **72 h at 600 °C, then quenched:** the particles "have grown and rounded off (spheroidized)".
   - **6 h at 600 °C, then furnace cooled over 15 h to 450 °C:** "a **fine AlMnFe precipitate** originated from the supersaturated solid solution due to the slow cooling". The cast particles spheroidised less than after 72 h.
2. **Constituents are fixed before the final anneal.** In 3003-O the dispersion of "(Fe,Mn)Al6 (large) and aluminum-manganese-silicon (both large and small) was not changed by annealing" [K p.132]. The same holds for FeAl3 in 1100-O vs 1100-H18 [K p.123]. In 3003-F hot band, primary (large, angular) and eutectic (small) Mn-bearing particles coexist [K p.131].
3. **Recrystallised 3003-O grains stay elongated in the rolling direction**, although the elongation "indicates rolling direction, but not the crystallographic orientation" [K p.131–132].
4. **Critical strain.** The recrystallised grain size of 1100 depends strongly on 0–10 % cold work before annealing [K p.121, Fig. 4; sizes not given in the caption].
5. **Recovery without recrystallisation.** Hard-rolled 99.99 % Al foil (0.1 mm) forms a subgrain structure after **2 h at 150 °C** [K p.120, Fig. 1].
6. **Partial recrystallisation from residual heat after hot rolling** is shown in 5456 plate [K p.134, Fig. 49]. The caption calls it "dynamic recrystallization"; *(general knowledge: recrystallisation after the pass is better called static or metadynamic)*.
7. **Annealing temperatures.** The minimum for 3xxx is **400 °C vs 360 °C for 1xxx** [DW §3.1.4]. 5457-O plate annealed at **345 °C** gives equiaxed grains [K p.135].
8. **Earing:** the definition and degree-of-earing formula are in §4.2 [K p.196–197]. The texture mechanism (45° ears from rolling texture, 0/90° from cube) is in [P p.39–40].
9. **Orange peel** occurs "when large grains in the metal are present" [K p.210].
10. **Mg-bearing variants (3004/3104/3105)** can **age-soften**: a spontaneous drop in strength at room temperature in strain-hardened Mg-containing alloys. The cure is **stabilising**, a low-temperature treatment [K p.187, 218]. A 5086-H34 plate stabilised at 120–175 °C shows an "undesirable continuous network of Mg2Al3" at its grain boundaries [K p.134]. Stabilising does not by itself prevent β precipitation in high-Mg alloys.
11. **Bendability of 1xxx/3xxx sheet** [DW §4.3.4, Table 4.6, eq. 4.2]: r/t_min = A + B·√t, with A = 0.3a − 1.7 and B = 0.08a + 0.5 (t in mm). Valid for 90° cold bends at t = 1.5–10 mm. Index a: **1200-O 3, H12 5, H14 6; 3103-O 4, H12 5, H14 6**; 5251-O 5; 5083-O 6; 6082-T6 13. H2x and H3x bend slightly better than H1x.

**Assessment for lean 3xxx slugs (inference, not source statements)**
- *Hardness calibration.* The user accepts slugs around **35 HB** as a stronger alloy; this is not a cap (stated 2026-10-12; the earlier "23–33 HB" was inferred from model files). For reference, the typical hardness is **1100-O 23 HB, 3003-O 28 HB and 3003-H12 35 HB** [K p.44–45]. A slug at the limit is therefore as hard as lightly strain-hardened (H12) 3003. A fully recrystallised lean Al-Mn slug should therefore read between 1100-O and 3003-O. Readings well above ~30 HB in an "O" slug point to incomplete recrystallisation (recovered substructure) or high Mn in solid solution. Readings near 23 HB point to a 1xxx-like matrix with little Mn effect. The K values are typical hardnesses (500 kg load, 10 mm ball). Check that the in-house test conditions match, and compare with the in-house HB data in chapter 09.
- *Where the particle structure is set.* Items 1–2 mean the constituent and dispersoid populations that drive PSN and Zener drag are set by **casting and homogenisation/preheat**, not by the final anneal. The final anneal can only act on stored energy and grain structure. The two 600 °C micrographs bracket the options: a long soak coarsens and spheroidises; slow cooling to 450 °C adds fine Al-Mn-Fe precipitate. The second option is expected to raise the recrystallisation temperature and can coarsen or elongate the annealed grain (consistent with [D p.382; P p.105–106]).
- *Grain-size control.* Item 4 (critical strain) and item 9 (orange peel) set the risks at the coarse end of the 20–100 µm target. Avoid annealing material carrying only small or uneven strains, such as lightly levelled edges.

### 4.12 Cast alloys (brief; Polmear Ch. 4 still unread)
- **General.** Casting alloys carry more Si and Cu, so their structures are heterogeneous. Coarse, sharp, brittle constituents act as internal notches, and fatigue is "very sensitive to large heterogeneities" [K p.108].
- **AA cast series** [K p.108–115]:

  | Series | Character | Approx. UTS, MPa | Workhorse alloys |
  |---|---|---|---|
  | 2xx.x | Heat treatable; strong at RT and high T | 130–450 | 201.0 (strongest; prone to microporosity and hot tearing); 203.0 (highest strength at ~200 °C) |
  | 3xx.x | Heat treatable; excellent fluidity | 130–275 | 319.0, 356.0/A356.0 (sand, permanent mould); 360.0, 380.0/A380.0, 390.0 (die); 357.0/A357.0; 332.0 (from scrap) |
  | 4xx.x | Non-heat-treatable; fluid | 120–175 | B413.0 (eutectic) |
  | 5xx.x | Non-heat-treatable; corrosion resistance, anodising | 120–175 | 512.0, 514.0 (seawater); 520.0 (decorative die castings). The long freezing range means 355.0 often replaces them |
  | 7xx.x | Harder to cast; machinability and finish | 210–380 | — |
  | 8xx.x | Al-Sn bearings | 105–210 | — |

  Kaufman gives B413.0 "a low melting point of 700 °C" [K p.112]. This conflicts with the Al–Si eutectic at ~577 °C [D p.365; P Table 2.1]. It is probably a pouring temperature or a misprint.
- **Three EN casting alloys** (minimum UTS / elongation of separately cast test bars; chill casting is always stronger than sand) [DW §4.5.2, Table 4.7]:
  - **AC-44100 (LM6, Si 11.5)**, durability B: F sand 160 MPa / 5 %; F chill 190 MPa / 7 %. The most popular casting alloy, for its fluidity.
  - **AC-51400 (LM5, Mg 4.5 Mn 0.5)**, durability A: F sand 140 / 3; F chill 170 / 5.
  - **AC-42000 (LM25, Si 7.0 Mg 0.4)**, durability B: F sand 130 / 2; F chill 160 / 3; **T6 sand 230 / 2; T6 chill 280 / 2**.

---

## 5. Cross-cutting physical metallurgy

### 5.1 Microstructural features that control properties [P p.77–80]

| Feature | Size | Origin | Role |
|---|---|---|---|
| Constituent particles (insoluble Al6(Fe,Mn), Al3Fe, Al(Fe,Mn,Si), Al7Cu2Fe; soluble Al2Cu, Al2CuMg, Mg2Si) | 0.5–10 µm after breakdown, aligned as stringers | Eutectic during solidification | Little effect on YS/UTS, but they **reduce ductility and toughness** by cracking into voids. Also sites for particle-stimulated nucleation (PSN, >~1 µm) [P p.42, 80] |
| Dispersoids (Al20Mn3Cu2, Al12Mg2Cr, Al3Zr, Al6Mn) | 0.05–0.5 µm | Solid-state precipitation during homogenisation | Zener pinning; retard recovery, recrystallisation and grain growth; affect ageing response and slip homogeneity [P p.43, 79] |
| Age-hardening precipitates | ≤0.1 µm | Ageing | Dominant strengthening in heat-treatable alloys [P p.79] |
| Grain size and shape (recrystallised vs unrecrystallised) | — | Thermomechanical history | Toughness, SCC, anisotropy [P p.79, 82] |
| Dislocation substructure | — | Cold work | Strength of NHT alloys [P p.80] |
| Texture | — | Rolling and annealing | Formability, **earing**, anisotropy [P p.38–40, 80] |

### 5.2 Dispersoid-forming elements compared

| Element | Phase(s) | Grain control | Quench sensitivity | Toughness | Source |
|---|---|---|---|---|---|
| Mn | Al6(Mn,Fe), Al12(Mn,Fe)3Si; Al20Cu2Mn3 (with Cu) | Raises recrystallisation temperature; fibrous structure | Intermediate | Coarser particles nucleate voids | [D p.382, 388; P p.112, 144] |
| Cr | Al12Mg2Cr (7xxx), Al18Mg3Cr2 (5xxx); primary Al7Cr if excessive | Prevents grain growth in 5xxx and recrystallisation in 6xxx/7xxx | **Highest** | — | [D p.373, 389–390; P p.112] |
| Zr | Metastable cubic Al3Zr (~20 nm), usually <0.15 % | Strong recrystallisation inhibitor | **Lowest** | Better than Cr/Mn | [D p.387, 390; P p.83, 112, 151] |
| Sc | Al3Sc (L12, coherent), precipitates at ~350 °C, coarsening-resistant; **Al3(Sc,Zr)** more homogeneous than Al3Zr | Inhibits recrystallisation up to ~600 °C | — | Adds dispersion strengthening | [P p.52–53, 156] |

Zr side-effect: it **poisons TiB2 grain refiners**, so more Ti-B is needed [D p.387; P p.104].
[S, unverified, citing Humphreys & Hatherly]: recrystallisation temperature (fast / slow heating) is 575/550 °C for Al-0.25Sc, 380/480 °C for Al-0.25Zr and 425/500 °C for Al-1.3Mn.

### 5.3 Fe and Si impurities: summary
- Fe and Si are present in every commercial alloy [D p.387]. Total impurities are usually <0.15 % [D p.370].
- **Phase selection:** Al3Fe or Al6Fe at low Si → α-Al12Fe3Si → β-Al9Fe2Si2 as Si rises. Mn stabilises α-type Al12(Fe,Mn)3Si [D p.388, 406].
- **Effects:**
  - They are cathodic and cause pitting [P p.75; D p.399].
  - They cut fracture toughness: K_IC roughly doubles when Fe + Si <0.5 % [P p.81]. 7475 has Fe+Si ≤0.22 vs 0.90 in 7075, giving K_IC >50 vs ~30 MPa√m [P p.151].
  - Iron refines the wrought grain size [D p.379].
- **Commercial-purity alloys have better smooth-specimen fatigue** than high-purity ones, because slip is dispersed, but **faster fatigue-crack growth** [P p.86].

### 5.4 Processing → microstructure chain (wrought)
1. **Melt treatment** [P p.97–99]:
   - H solubility is 0.68 (liquid) vs 0.036 (solid) cm³/100 g, a factor of 19. Melts need **<0.15 cm³/100 g H** to be porosity-free.
   - Degassing with Ar/N2/Cl2 or FILD; ceramic foam filtration.
2. **Casting.** DC cooling rate is 1–5 °C/s, with dendrite cells **30–70 µm**. Twin-roll casting runs at 10²–10³ °C/s with **5–10 µm** cells and higher transition-metal supersaturation [P p.99, 102].
3. **Grain refinement.** Al-5Ti-1B (Ti:B 3:1 to 50:1) [P p.103]. Commercial refiners hold 3–10 % Ti with Ti:B from 5:1 to 50:1 [D p.390].
4. **Homogenisation** (450–600 °C, 6–24 h) [P p.105]. Purposes:
   - reduce microsegregation;
   - remove low-melting eutectics;
   - precipitate dispersoids;
   - transform constituents (Al6 → α).

   Raising the temperature by **50 °C cuts the time to about one third** [P p.105].
5. **Hot rolling.** The reversing mill takes 200–600 mm ingot down to 15–35 mm slab; the tandem mill takes it to 2.5–8 mm hot band [P p.107]. Temperature variations of **±5 °C** "may have a clearly measurable impact" [AR p.12–13].
6. **Cold rolling with interpass anneals; temper rolling or temper annealing** [DW §2.2.3; P p.107]. Cladding is ~5 % of the thickness per side and ≥100 mV more anodic than the core [P p.108].
7. **Heat-treatable route.** Solution treatment, quench, stretch 1–3 %, then age [P p.90, 109–114]. A process anneal at 300–400 °C for 2–5 h before solution treatment gives a coarse elongated grain in 2xxx sheet, with **lower fatigue-crack growth rates** [AR p.14].

---

## 6. Strengthening mechanisms: summary and quantitative relations

| Mechanism | Relation / value given | Source |
|---|---|---|
| **Solid solution** (annealed super-purity binaries) | ΔYS per wt %: **Mg 18.6**, **Mn 30.3**, **Cu 13.8**, **Si 9.2**, **Zn 2.9 MPa**. ΔUTS per wt %: Mg 50.3, Mn 53.8, Cu 43.1, Si 39.6, Zn 15.2 MPa. Per at %: YS Mg 17.2, Cu 16.2, Si 9.3, Zn 6.6 MPa (1 at % Mn is not soluble). Size misfit vs Al: Si −3.8, Zn −6.0, Cu −10.7, Mn −11.3, Mg +11.8 %. Small additions have larger unit effects. Multiple solutes are **less than additive**. | [D p.367–368 Table 8] |
| Solid solution, practical notes | On an atomic basis Mn and Cu are the most effective at ≤0.5 %. Mg is most effective by weight (high solubility). Zn gives little. Cu in NHT alloys is kept ≤0.3 % to avoid Al-Cu-Fe phases. | [P p.30] |
| Mg in Al-Mg(-Mn) plate | ~**35 MPa UTS per 1 % Mg**, and Mn "about twice as effective" (O temper, 13 mm plate) | [D p.380] |
| Additivity of contributions | Solid solution + second phase + dispersoid contributions are **roughly additive** (Al-Mg-Mn, Fig 9) | [D p.370] |
| Second-phase (constituent) hardening | Rate per unit weight is similar to, but usually lower than, solid solution | [D p.369] |
| Dispersion (8xxx) | 30–40 MPa from dispersoids; 2–10 MPa YS from solid solution | [P p.131] |
| **Work hardening** | σ = K εⁿ. As K rises over **175–450 MPa**, **n falls from 0.25 to 0.17**. For pre-strained material σ = K(ε0 + ε)ⁿ. Cold-worked NHT tempers harden much more slowly than annealed material. | [P p.35–36] |
| Stress–strain shape (Ramberg–Osgood) | e = σ/E + 0.002·(σ/σ_o)ⁿ, where σ_o is the actual 0.2 % proof stress (DW eq. 4.3, read from the page image). **n ≈ 40 down to 5** for Al materials. For minimum-property material, **n = log(5·el) / log(f_u/f_o)** (el in %) [DW eq. 4.4]. n depends strongly on f_u/f_o and hardly on el. Fully hard or fully heat-treated tempers (f_u/f_o < 1.2) have an abrupt knee; O and T4 have a rounded one. | [DW §4.4.1–4.4.2] |
| Cryogenic work hardening | Working at −196 °C gives up to **+40 %** strength (1100), at lower ductility | [P p.36] |
| Solute effects on work hardening | Cu is the most effective at raising dislocation multiplication; Mg has the greatest practical value; Zn has negligible effect | [P p.34] |
| Strain ageing | Mg and Cu pin dislocations: higher work hardening at low strain, lower at large strain, which reduces diffuse necking. Zn does not strain-age. | [D p.408] |
| **Substructure (Hall–Petch type)** | σ = σ0 + k1·d⁻ᵐ, with d the cell or subgrain size. **m changes from 1 (cells) to 0.5 (subgrains)** after recovery. Stacking-fault energy ≈ **170 mJ m⁻²**, so cells form rather than twins. **No grain-size Hall–Petch constants for Al are given in any source read.** | [P p.36–37] |
| Texture | Ideal fibre texture: up to ~20 % higher strength along the fibre | [P p.39] |
| **Precipitation – shearing** | Maximum strength when particle spacing ≈ the limiting dislocation curvature, **~10 nm (~50 atomic spacings)**. GP zones are sheared; their strength comes from the high volume fraction plus "chemical hardening". Shearing gives planar slip and pile-ups. | [P p.53] |
| **Precipitation – Orowan bypass** | Δτ = [Gb / (2π√(1−ν))]·(1/λ)·ln(D_p/r0). G = shear modulus, b = Burgers vector, ν = Poisson's ratio, λ = effective inter-particle spacing, D_p = planar particle diameter, r0 = dislocation core radius. The spacing for volume fraction f, *as extracted* (π symbols and minus signs lost): {100} plates "0.931(0.306·D·T/f)^½ · D/8 · 1.061D"; {111} plates "0.931(0.265·D·T/f)^½ · D/8 · 0.919T"; ⟨100⟩ rods "1.075D(0.433/f)^½ · (1.732D)^½". **{111} plates > {100} plates > rods > spheres**, and the advantage grows with aspect ratio (closed-network entrapment above a critical aspect ratio). | [P p.56–61] (equation layout reconstructed; check the original, Nie & Muddle 1996/1998) |
| Peak strength | At the crossover of the shearing and bypass curves. Higher volume fraction raises both curves; finer non-shearable particles raise the peak. | [P p.55–56] |
| Strength ceilings | Al-Zn-Mg-Cu: YS >600 MPa; Al-Cu-Li-Mg-Ag: >700 MPa; theoretical limit for Al ~**900 MPa** | [P p.60–61] |

---

## 7. Corrosion and SCC summary relevant to alloy design
- **Oxide film.** About **2.5 nm** on fresh rolled sheet and protective at **pH 4.5–8.5** [P p.70]. Davis gives ~5 nm and pH 4–9 [D p.399]. Dwight prints "typical thickness **0.005 mm**" [DW §4.7.1], i.e. 5 µm. That is three orders of magnitude above P and D, and is almost certainly a unit slip for 0.005 µm (5 nm). Do not use the DW figure (this matters for the MgO annealing-oxide work, where film thickness is a measured quantity).
- **Atmospheric pitting of 3103 (Alcan data)** [DW §4.7.1, Fig. 4.12]: pit depth grows quickly in the first year and almost stops after **~5 years**, as corrosion products stifle the pits. Worst 5-year pit depths: **~0.04 mm rural, 0.08 mm inland industrial, ~0.16 mm industrial by the sea**.
- **When to protect (BS 8118 ratings)** [DW Table 4.9]: A-rated alloys (1xxx, 3xxx, 5xxx) need protection only in **severe industrial** atmospheres, inland or by the sea. B-rated 6xxx always needs it in severe industrial sites. In inland moderate-industrial and in marine rural or moderate-industrial sites it needs protection only if thinner than 3 mm. Weldable 7xxx (C) needs it everywhere except inland rural; 2xxx and strong 7xxx (D) need it everywhere.
- **Electrode potentials** (V vs 0.1 M calomel, NaCl–H2O2; all negative, signs restored) [P Table 2.4–2.5]:
  - **Phases and solid solutions:** Mg5Al8 −1.24; Al-Zn-Mg solid solution −1.07; MgZn2 −1.05; Al2CuMg −1.00; Al-5Mg solid solution −0.88; **MnAl6 −0.85 = Al (99.95 %) −0.85**; Al-Mg-Si solid solution −0.83; Al-1Si −0.81; Al-2Cu −0.75; Al-4Cu −0.69; FeAl3 −0.56; CuAl2 −0.53; NiAl3 −0.52; Si −0.26.
  - **Alloys:** Alclad 6061/7075 −0.99; 5456/5083 −0.87; 5052/5086 −0.85; 3004/1060/5050 −0.84; 1100/3003/6063/6061/Alclad 2024 −0.83; 2014-T4 −0.69.
- **Element by element.**
  - Cu is the most damaging element, mainly through microconstituents. Zn makes Al anodic, which is why 7072 cladding and sacrificial anodes contain it. Mg in solid solution is anodic but dilute Al-Mg alloys stay resistant. Cr, Si and Zn in solution have a minor effect [P p.73].
  - **Mg:Si at 2:1 gives Mg2Si with about the matrix potential** [P p.75].
- **SCC.**
  - **Susceptible:** 2xxx; 5xxx with >3 % Mg; 7xxx. **Rare** in 6xxx. **Absent** in 1xxx, 3xxx and Al-Mg <3 % [P p.90].
  - Temperature thresholds for 5xxx differ by source: **>3 % Mg with continuous exposure above 100 °C** [K p.96]; **Mg >3.5 % operating long-term above ~70 °C** [DW §4.7.1]; Mg above "about 3.5 or 4 %" in hot environments [DW §4.3.3]. Compare >~3.5 % above ~65 °C [D p.361].
  - The mechanism is intergranular. Electrochemistry dominates, with a role for hydrogen [P p.90–92].
  - It is worst in recrystallised structures and short-transverse loading [P p.90; K p.27–28].
  - Resistance rises in the underaged and overaged conditions [P p.90–91].
- **Corrosion fatigue.** The fatigue strength is ~60 % of the in-air value in fresh water and **25–35 % in NaCl**, roughly independent of alloy and temper [P p.93–94].

---

## 8. Magnesium alloys (brief)
- **Pure Mg** [AM slide 14; P p.5 Table 1.1]: hcp, a = 0.3209–0.3203 nm, c = 0.5211–0.5199 nm; melting point 650 °C; density 1.736–1.74 g cm⁻³; E = 45 GPa; specific modulus 26, the same as Al; electrode potential −2.31 V [AM slide 19]. Mg is −1.73 V vs Al −0.85 V in [P Table 2.4].
- **Advantages:** lowest density of the structural metals (~1.8 g cm⁻³ for alloys), castability (high-pressure die casting), machinability, damping, EMI shielding, recyclability [AM slide 15].
- **Disadvantages:** low E; limited cold workability and toughness (hcp); limited creep resistance; high solidification shrinkage; reactivity; corrosion [AM slide 19].
- **ASTM letter code** [AM slide 15]:

  | Letter | A | M | W | E | Q | S | K | Z | L | H | Y |
  |---|---|---|---|---|---|---|---|---|---|---|---|
  | Element | Al | Mn | Y | Rare earths | Ag | Si | Zr | Zn | Li | Th | Sb (as given) |

  Examples: AZ91 = Mg-9Al-1Zn; AM60 = Mg-6Al-0.3Mn; AE42 = Mg-4Al-2RE; AS21 = Mg-2Al-1Si.
- **Service-temperature ladder** [AM slide 19]: AZ91 125 °C; AS21 150 °C; AE42 150–175 °C; Mg-Al-Ca ≤200 °C; EZ (Mg-RE-Zn-Zr) ≤200 °C; QE (Mg-Ag-RE-Zr) 200–250 °C; WE (Mg-Y-RE-Zr) 250–300 °C; Mg-Sc-Mn ~300 °C; HZ22 (Th) ≤350 °C, but radioactive.
- **Die casting.** Cooling at 100–1000 °C/s produces coring in Mg-Al [AM slide 20].
- **Market** [P p.10, 13]:
  - In 2004 roughly half of world Mg went into Al alloys. Less than 20 % went into Mg alloys, mostly die castings.
  - Die-casting tonnage grew 16 %/yr over 1994–2004, to 152,000 t in 2004.
  - Wrought Mg is limited by the hcp structure.
- **Coverage gap.** Polmear Ch. 5 (Mg alloys) is **not in the extracted text**, and the 2026-10-12 full download of P failed (§1). This section therefore has no Polmear physical metallurgy (Zr grain refinement, Mg-Al β-Mg17Al12 and so on). K mentions Mg only as an alloying element; DW does not cover Mg alloys.

---

## 9. Alloy-design principles stated by the authors
1. **Target microstructure for high strength plus fracture resistance:** "a small volume fraction of very fine, hard particles", with shear-resistant **plate-shaped precipitates on {111} or {100}**, or ⟨100⟩ rods. {111} plates are best, and the benefit grows with aspect ratio [P p.56–60].
2. **Ways to obtain fine non-shearable precipitates** [P p.56]:
   - duplex ageing (below, then above, the GP solvus);
   - co-precipitation of a fine strengthening phase plus coarser shear-resistant particles;
   - several phases on different habit planes;
   - **trace-element nucleation** (Sn, Cd, In, Ag, Sc) [P p.49–53].
3. **Duplex particle structure for fatigue:** fine precipitates for tensile strength plus coarse particles to spread slip [P p.89]. Dispersoids do this in commercial 7075 [P p.86].
4. **Purity for toughness.** Cut Fe + Si (and excess Cu) to shrink the coarse constituents. This is the "major step" in fracture-toughness improvement [P p.81, 135, 151; K p.24]. Toughness is highest when underaged; avoid coarse grain-boundary precipitates and wide PFZs [P p.84].
5. **Choose the recrystallisation inhibitor by side-effect.** Zr has the least quench sensitivity and the best toughness, ahead of Mn and then Cr. Keep Cr ≤0.35 % and lower when other transition metals are present [P p.83, 112, 144; D p.373, 387].
6. **NHT alloys: replace Mg by Mn/Cr** to reach strength without β sensitisation (5454 ≈ 4 % Mg binary) [P p.130]. Keep Mg ≤3 % for elevated-temperature or sensitising service [K p.28; P p.90].
7. **6xxx: re-balance Mg:Si** on the basis of the ~1:1 composition of β''. Leaner Mg improves extrudability at equal strength (6060 vs 6063) [P p.66, 141]. Excess Si gives strength but needs a grain-structure control element [D p.381–382].
8. **Weldable 7xxx window:** Zn + Mg <6 %, Zn:Mg ≈2.7–2.9, Cu <0.3 %, Zr in place of Cr/Mn, slower quench, duplex ageing [P p.143–144].
9. **SCC is mainly electrochemical,** so control it through composition and temper rather than stress level alone. Stretch 1–3 % to remove quench stresses [P p.90].
10. **Process design for dispersoids.** A slow heating rate to homogenisation (~75 °C/h) gives a fine, uniform dispersion [P p.106]. Use electrical conductivity to track precipitation completeness [D p.370].
11. **Interrupted or secondary ageing (T6I6, T6I4)** can raise strength and toughness at the same time [P p.68–70, 136–137]. Measured K_IC gains: 2014 +34.5 %; 6061 +58.6 % (T6I6) and +17.4 % (T6I4); 7050 +9.3 % and +38.3 %; 8090 +28.1 % [P p.136]. Underageing can improve creep: 2024 time to failure 260 h → 480 h at 150 °C and 300 MPa [P p.94].
12. **Formability cannot be optimised alone;** the function of the part (strength, machinability) must be weighed [D p.408]. Precipitation-hardened sheet is formed in O or T4, rarely T6 [D p.408].
13. **Joinability.**
    - Brazing needs a solidus >595 °C and low Mg for CAB [D p.414; P p.168].
    - Solderability drops with Mg (>0.5–1 %) and Si (>5 %) [D p.415].
    - NHT alloys welded lose their temper, so design on O-temper strength [P p.163].
14. **Do not fixate on familiar specifications;** choose from the full "menu" of alloys [T §1101.02]. Alloy-design trade-offs are multi-property: fatigue, toughness, SCC, weldability, strength [T Fig 1101.02.06].
15. **Lithium alloys:** control alkali impurities to <1–5 ppm [P p.158]. The economics need weight-saving cost models (Boeing formula) [P p.172].

---

## 10. Property reference table
Typical values unless marked *min*. **UTS/YS in MPa; A = elongation % in 50 mm on 1.6 mm sheet ([K]) or in 50 mm ([P]).** HB = Brinell (500 kg, 10 mm). σf = fatigue endurance limit at 5×10⁸ cycles (R.R. Moore). E in GPa.
[K Table 1M] values are typical and "not intended for design"; for non-O tempers they exceed the specified minima [K p.40–49].

**1xxx / 3xxx / 4xxx**

| Alloy-temper | UTS | YS | A % | Other | Source |
|---|---|---|---|---|---|
| 1060-O / H12 / H14 / H16 / H18 | 70 / 85 / 100 / 115 / 130 | 30 / 75 / 90 / 105 / 125 | 43 / 16 / 12 / 8 / 6 | HB 19→35; E 69 | [K p.44] |
| 1100-O / H12 / H14 / H16 / H18 | 90 / 110 / 125 / 145 / 165 | 35 / 105 / 115 / 140 / 150 | 35 / 12 / 9 / 6 / 5 | HB 23 / 28 / 32 / 38 / 44; σf 35–60 | [K p.44] |
| 1100-O / H18 | 90 / 165 | 35 / 150 | 35 / 5 | — | [P p.122] |
| 1145-O / H18 | 75 / 145 | 35 / 115 | 40 / 5 | Foil | [P p.122] |
| 1199-O / H18 | 45 / 115 | 10 / 110 | 50 / 5 | Electrical foil | [P p.122] |
| 1350-O / H12 / H14 / H16 / H19 | 85 / 95 / 110 / 125 / 185 | 30 / 85 / 95 / 110 / 165 | 23 (O wire, in 250 mm); 1.5 (H19 wire, in 250 mm) | Conductor | [K p.44] |
| **3003-O / H12 / H14 / H16 / H18** | **110 / 130 / 150 / 175 / 200** | **40 / 125 / 145 / 170 / 185** | **30 / 10 / 8 / 5 / 4** | HB 28 / 35 / 40 / 47 / 55; σf 50 / 55 / 60 / 70 / 70; E 69 | [K p.45] |
| 3003-O / H18 | 110 / 200 | 25 / 185 | 30 / 4 | — | [P p.122] (O-temper YS differs from K) |
| **3004-O / H32 / H34 / H36 / H38** | **180 / 215 / 240 / 260 / 285** | **70 / 170 / 200 / 230 / 250** | **20 / 10 / 9 / 5 / 5** | HB 45 / 52 / 63 / 70 / 77; σf 95–110 | [K p.45] |
| 3004-O / H38 | 180 / 280 | 70 / 250 | 20 / 5 | — | [P p.122] |
| 3005-O / H18 | 130 / 240 | 55 / 225 | 25 / 4 | High-strength foil, roofing | [P p.122] |
| **3105-O / H12 / H14 / H16 / H18 / H25** | **115 / 150 / 170 / 195 / 215 / 180** | **55 / 130 / 150 / 170 / 195 / 160** | **24 / 7 / 5 / 4 / 3 / 8** | Shear 85–115 | [K p.45] |
| 3105-O / H18 | 120 / 215 | 55 / 195 | 24 / 3 | — | [P p.122] |
| 3103-O / H14 / H18 (*min*, plate/sheet; t <50 / <25 / <3 mm) | 90 / 140 / 185 | 35 / 120 / 165 | 17–28 / 2–5 / 1–2 | BS EN 485 basis; no extrusion data | [DW Table 4.5] (verified 2026-10-12; matches [S]) |
| 4032-T6 | 380 | 315 | 9 (5D) | HB 120; E 79 | [K p.45] |

**5xxx**

| Alloy-temper | UTS | YS | A % | Other | Source |
|---|---|---|---|---|---|
| 5005-O / H12 / H14 / H16 / H18 | 125 / 140 / 160 / 180 / 200 | 40 / 130 / 150 / 170 / 195 | 25 / 10 / 6 / 5 / 4 | — | [K p.45] |
| 5005-H32 / H34 / H36 / H38 | 140 / 160 / 180 / 200 | 115 / 140 / 165 / 185 | 11 / 8 / 6 / 5 | HB 36 / 41 / 46 / 51 | [K p.46] |
| 5050-O / H32 / H34 / H36 / H38 | 145 / 170 / 190 / 205 / 220 | 55 / 145 / 165 / 180 / 200 | 24 / 9 / 8 / 7 / 6 | HB 36 → 63 | [K p.46] |
| **5052-O / H32 / H34 / H36 / H38** | **195 / 230 / 260 / 275 / 290** | **90 / 195 / 215 / 240 / 255** | **25 / 12 / 10 / 8 / 7** | HB 47 / 60 / 68 / 73 / 77; σf 110–140; E 70 | [K p.46] |
| 5052-H38 | 270 | 255 | 7 | — | [P p.122] (UTS differs from K) |
| 5056-O / H18 / H38 | 290 / 435 / 415 | 150 / 405 / 345 | 32 / 9 / 13 (5D) | — | [K p.46] |
| **5083-O / H321, H116** | **290 / 315** | **145 / 230** | **20 / 14 (5D)** | σf 160; E 71 | [K p.46] |
| 5083-O / H343 | 290 / 360 | 145 / 280 | 22 / 8 | — | [P p.123] |
| 5083-O / H22 / H24 (*min*, plate/sheet; t <50 / <40 / <25 mm) | 275 / 305 / 340 | 125 / 215 / 250 | 10–16 / 5–10 / 4–7 | Extrusions O (all t): 270 / 110 | [DW Table 4.5] (verified; matches [S]) |
| 5383-O / H321 | 290 / 305 | 145 / 220 | 17 / 10 | — | [P p.123] |
| 5086-O / H32, H116 / H34 / H112 | 260 / 290 / 325 / 270 | 115 / 205 / 255 / 130 | 22 / 12 / 10 / 14 | — | [K p.46] |
| 5154-O / H32 / H34 / H36 / H38 / H112 | 240 / 270 / 290 / 310 / 330 / 240 | 115 / 205 / 230 / 250 / 270 / 115 | 27 / 15 / 13 / 12 / 10 / 25 | HB 58 → 80 | [K p.46] |
| 5454-O / H32 / H34 / H111 / H112 | 250 / 275 / 305 / 260 / 250 | 115 / 205 / 240 / 180 / 125 | 22 / 10 / 10 / 14 / 18 | HB 62 / 73 / 81 / 70 / 62 | [K p.46–47] |
| 5456-O / H25 / H321, H116 | 310 / 310 / 350 | 160 / 165 / 255 | 22 / 20 / 14 (5D) | HB 90 (H321) | [K p.47] |
| 5457-O / H25 / H38, H28 | 130 / 180 / 205 | 50 / 160 / 185 | 22 / 12 / 6 | — | [K p.47] |
| 5657-H25 / H38, H28 | 160 / 195 | 140 / 165 | 12 / 7 | Bright trim | [K p.47] |
| **5754-H111** (*min*, BS EN 485-2, 0.2–6 mm) | **160–200** | **≥60** | **≥12 (A50)** | 44 HB; ρ 2.66; E 68; k 147 W m⁻¹K⁻¹; ρ_el 0.049 µΩ·m; α 24×10⁻⁶ K⁻¹; melting point 600 °C | [A57 p.1–2] |
| 5154A (Mg 3.5)-O / H22 / H24 / H26 (*min*; t <50 / <40 / <25 / <6 mm) | 215 / 250 / 270 / 290 | 85 / 180 / 200 / 230 | 12–16 / 5–9 / 4–7 / 3–5 | Extrusions O (<25 mm): 200 / 85 | [DW Table 4.5] (verified; matches [S]) |
| 5251 (Mg 2.0, Mn 0.3)-O / H22 / H24 / H26 (*min*; t <50 / <25 / <12 / <4 mm) | 160 / 190 / 210 / 230 | 60 / 120 / 140 / 170 | 13–18 / 4–12 / 3–10 / 3–7 | Extrusions O (all t): 160 / 60. DW ranks 5052 slightly stronger than 5251, 5754 between 5251 and 5154A, and 5454 ≈ 5154A [DW §4.3.3] | [DW Table 4.5] (verified; matches [S]) |

**6xxx**

| Alloy-temper | UTS | YS | A % | Other | Source |
|---|---|---|---|---|---|
| 6060-T5 | 215 | 195 | 17 | — | [P p.126] |
| **6063-O / T1 / T4 / T5 / T6** | **90 / 150 / 170 / 185 / 240** | **50 / 90 / 90 / 145 / 215** | **– / 20 / 22 / 12 / 12** | HB 25 / 42 / – / 60 / 73 | [K p.47] |
| 6063-T83 / T831 / T832 | 255 / 205 / 295 | 240 / 185 / 270 | 9 / 10 / 12 | — | [K p.47] |
| 6063-O / T1 / T4 / T5 / T6 / T81 / T82 / T83 | 90 / 150 / 170 / 220 / 240 / 250 / 260 / 280 | 50 / 90 / 90 / 180 / 215 / 230 / 255 / 270 | 30 / 20 / 22 / 12 / 12 / 11 / 9 / 8 | T3x and H rows of P Table 3.1 garbled, so omitted | [P p.120] |
| 6063-T6 | 240–245 | 215 | 12 | — | [P p.126, 140] |
| **6061-O / T4 / T6** | **125 / 240 / 310** | **55 / 145 / 275** | **25 / 22 / 12** | HB 30 / 65 / 95; σf 60 / 95 / 95 | [K p.47] |
| **6082-T5 / T6** | **300 / 315** | **260 / 285** | **15 / 12** | Extrusions (T5), plate (T6) | [P p.126] |
| 6082-T4 / T6 (*min*, plate/sheet; T4 <12 mm, T6 <6 mm and 6–12 mm) | 205 / 310 and 300 | 110 / 260 and 255 | 12–14 / 6–10 | Extrusions: T4 (<25 mm) 205/110; T5 (<5 mm) 270/230; T6 (<5 mm) 290/250; T6 (5–25 mm) 310/260 | [DW Table 4.5] (verified; matches [S]) |
| 6063-T4 / T5 / T6 (*min*, extrusions) | 130; 175 (<3 mm), 160 (3–25 mm); 215 (<10 mm), 195 (10–25 mm) | 65; 130, 110; 170, 160 | 12–14; 5–8, 6–8; 6–8 | No sheet data | [DW Table 4.5] |
| 6061-T4 / T6 (*min*; sheet <12 mm \| extrusions <25 mm) | 205 / 290 \| 180 / 260 | 110 / 240 \| 110 / 240 | 12–18 / 6–10 | — | [DW Table 4.5] |
| 6005-T5 | 305 | 270 | 12 | — | [P p.126] |
| 6016-T4 | 210 | 105 | 26 | Automotive sheet | [P p.126] |
| 6111-T4; 6013-T4; 6013-T6 | 290; 315; — | 160; 185; 330 | 25; 25; — | — | [P p.126, 141] |
| 6351-T6; 6066-T6; 6262-T9 | 310; 395; 400 | 285; 360; 380 | 14; 10; 9 | — | [K p.47] |

**7xxx / 2xxx / 8xxx**

| Alloy-temper | UTS | YS | A % | Other | Source |
|---|---|---|---|---|---|
| **7020-T4 / T6** | **340 / 370** | **225 / 310** | **18 / 15** | Weldable | [P p.127] |
| 7020-T4 / T6 (*min*, plate/sheet <12 mm) | 320 / 350 | 210 / 280 | 11–14 / 7–10 | Extrusions T6 (t 40 mm as printed): 350 / 290 | [DW Table 4.5] (verified; matches [S]) |
| 7019 (Zn 4.0, Mg 2.0)-T6 (*min*) | 380 | 330 | 8 | Top of the practical range for welded construction; military bridging [DW §4.3.3] | [DW Table 4.5] |
| 7005-T53; 7039-T61; 7016-T6 | 395; 415; 360 | 345; 345; 315 | 15; 13; 12 | — | [P p.127] |
| **7075-O / T6, T651** | **230 / 570** | **105 / 505** | **17 / 11** | HB 60 / 150; σf 160; E 72 | [K p.49] |
| 7075-T6 / T73 / T76 | 570 / 500 / 540 | 500 / 430 / 470 | 11 / 13 / 12 | — | [P p.127] |
| 7075-T73 die forging | 500 | 430 | 13 | — | [AM slide 10] |
| 7050-T7451 / T7651; 7475-T651; 7178-T6 | 525 / 550; 585; 605 | 470 / 490; 510; 540 | 10 / 10; 13; 10 | — | [K p.49] |
| 7055-T7751; 7085-T7651 | 630; 510 | 610; 475 | 12; 7 | — | [P p.127] |
| 2024-T3 / T4; 2014-T6; 2219-T87 | 485 / 472; 485; 475 | 345 / 325; 415; 395 | 18 / 20; 11 (5D); 10 | — | [K p.44–45] |
| 8176-H24 | 160 | 95 | 15 | Conductor | [K p.49] |
| 8001-O / H18 | 110 / 200 | 40 / 185 | 30 / 4 | — | [P p.123] |
| **3102, 3207, 3104, 8006, 8011, 8079, 8111, 1050, 1200** | **no tabulated property values in any source read** (K and DW searched in full, 2026-10-12) | | | 3104-H19 ~2 % elongation, ~87 % cold reduction: [S, unverified] only. DW Fig. 4.3 plots minimum f_o/f_u bars for 1080A, 1200 and 3105 (O/H14/H18), but the scan is too coarse (~100–170 dpi) to read numbers from | — |

**Physical properties**
- **Pure Al** [P Table 1.1 p.5; DW §1.2; K p.29–30]:
  - Density 2.70 (2.699) g cm⁻³; E 69–70 GPa; ν 0.33.
  - α = 23.5×10⁻⁶ K⁻¹; k = 238–240 W m⁻¹K⁻¹; ρ_el = 2.67–2.7 µΩ·cm; melting point 660 °C; fcc, a = 0.4041 nm.
- **Wrought alloys** [DW §1.2]:
  - Density 2.67–2.80; E 69–72 GPa. E falls to 67 GPa at 100 °C and 59 GPa at 200 °C.
  - α = 22–24.5×10⁻⁶ K⁻¹.
  - Conductivity: alloying can cut thermal conductivity by up to ~50 %, and resistivity is about twice the pure-Al value for some alloys.
- **Davis:** alloys have 50–60 % of the thermal conductivity of Cu, and Al has nearly 2× the electrical conductivity of Cu per unit weight [D p.352].
- **Modulus by series** [K Table 1M]: 1xxx/3xxx 69; 5052/5154/5454 70; 5083/5086/5456 71; 2xxx 70–74; 7xxx 70–72 GPa.
- **Strength vs temperature** [DW §4.3.5, Fig. 4.6]. These are typical-material curves (Aluminium Federation data), tested at temperature after long exposure at that temperature.
  - 6082-T6 UTS falls by **70 % at 200 °C** and rises by **40 % at −200 °C**. There is no low-temperature brittleness.
  - Read approximately from the figure: 5083-O, 5251-H24 and 6063-T6 hold roughly constant UTS up to ~100 °C. **3103-H18**, the lowest curve at ~200 MPa near room temperature, declines gradually up to ~150 °C. By 300 °C all of these curves are below ~100 MPa.
  - Above 100 °C, 6082 loses strength much faster than 5083 [DW Fig. 4.7]. 2618 has twice the strength of 2014A-T6 after prolonged heating at 200 °C.
- **Melting ranges** [D p.414 Table 10]: 1350 646–657; 1100 643–657; **3003 643–654**; **3004 629–652**; 5005 632–652; 5050 627–652; 5052 593–649; 6061 593–649; 6063 616–654; 6951 616–654; 7005 607–649 °C.

---

## 11. Open questions and gaps
*Updated 2026-10-12 after the full-text pass. Former item 12 (the Kaufman "296 and over" row) was resolved and removed; see §3.2. Former item 6 is reduced to what is still open.*
1. **Target alloys missing from the sources.** AA3102, AA3207, AA3104, AA8079, AA8111 and AA1050/1200 have **no tabulated compositions or properties** in any source read. K and DW were searched in full: K names 3104 only as "a modification of 3004" for can bodies [K p.93], and DW plots 1200 only in an unreadable bar chart and gives its bend index [DW Table 4.6]. A primary source is needed: EN 573-3/485-2, AA Teal Sheets, or the unprocessed *Al-Fe-Mn-Si System* chapter.
2. **Polmear truncation.** The canstock (§3.6.5), foil (§3.6.4), conductor (§3.6.9) and automotive sheet (§3.6.2) sections, plus Ch. 4 (cast), are still unread. They are exactly the 3xxx/8xxx processing know-how this project needs. **The 2026-10-12 full download failed** for both Drive copies (connector message too large, §1). Options: download outside the connector (Drive API/curl with the user's credentials); have the user upload a split PDF (e.g. pp.170–260) under 6 MB; or use another copy of the book.
3. **Mn vs Mg effectiveness conflict.** Davis gives "0.8 % Mg ≡ 1.25 % Mn" [D p.361] but also "Mn ≈ 2× Mg" in Al-Mg-Mn plate [D p.380]. Table 8 gives the solid-solution YS coefficients Mn 30.3 > Mg 18.6 MPa/wt %. Hypothesis: the difference comes from how much Mn is in solution vs dispersoids and from the product form. This needs quantification for 3xxx at the actual Mn-in-solution level (0.2–0.3 % [P p.30]).
4. **Hall–Petch constants** (σ0, k_y) for Al and 3xxx grain sizes, and precipitate-free numbers for dispersoid (Orowan) strengthening in 3xxx, are not in these sources. K and DW contain none either.
5. **6082 Mg range:** P gives 0.60–1.0 and DW (EN) gives 0.6–1.2. Check against EN 573-3.
6. **Still-unverified spreadsheet values.** The ASM-sourced anneal temperatures (343/413 °C), the CW % guide, the H2x partial-anneal windows (200–280 °C, 1–4 h) and the Humphreys & Hatherly recrystallisation data in [S] have no primary source yet. Check them against the ASM Handbook / H&H (both in Drive, unread here). The Dwight-sourced values in [S] are now verified (§1, §3.2, §3.4, §10).
7. **O-temper YS differences.** P (3003-O YS 25 MPa) and K (40 MPa) disagree. The 5052-H38 UTS also differs (P 270 vs K 290 MPa). The likely causes are different data bases or the typical-vs-specified basis; record the product form when building models.
8. **Davis Table 8 per-atomic-% coefficients** for Cu (16.2 at % vs 13.8 wt %) look inconsistent with atomic-mass scaling, possibly a source error. Prefer the wt % values with caution.
9. **Kinetic data still needed:** Mn dispersoid precipitation kinetics as a function of heating rate, and recrystallisation temperature vs dispersoid density in 3xxx. The sources give only qualitative statements, single D values [P p.105–106] and the two 3003 homogenisation micrographs [K p.131]. The [S] recrystallisation temperatures from Humphreys & Hatherly need checking against that book, which is in Drive but unread.
10. **Zn in fin alloys.** The galvanic role of Zn in fins (FA6815) is inferred from general principles and needs a source.
11. **Mg alloy metallurgy.** Polmear Ch. 5 is missing (download failed), so the Mg section rests on lecture slides only.
12. **Kaufman Ch. 5 (fabricating processes, pp.77–86) is absent from the Drive PDF**, which jumps from p.76 to p.87. Its sections on strip and slab casting, hot and cold rolling and heat treatment are unread. A complete copy is needed.
13. **"3xxx vs 1xxx" strength gain.** Davis says ~20 % [D p.360]; Dwight says "half as strong again" [DW §4.2.1(b)]. The K data support ~20 % against 1100 (§4.2). Always state the 1xxx baseline (1100 vs 1050A/1080A) when quoting the Mn benefit.
14. **Source errors found in the full-text pass** (flagged in place, not silently fixed):
    - DW oxide thickness "0.005 mm" (5 µm), which conflicts with 2.5–5 nm in P/D (§7).
    - K's B413.0 "melting point of 700 °C", which conflicts with the 577 °C eutectic (§4.12).
    - K's 8xxx bullet "heat treatable", which conflicts with K p.26 (§4.8).
    - K's Table 5 row "25–20" for 25–30 ksi (§3.2).
15. **S-029 (Totten & MacKenzie, *Handbook of Aluminum* Vol. 1, 17.66 MB) is not reachable through the Drive connector:** "File too large for download, over limit of 10 MB" (§1). Its Ch. 3 (alloy metallurgy) and its rolling and annealing chapters would need an out-of-connector download or a user-supplied split.
