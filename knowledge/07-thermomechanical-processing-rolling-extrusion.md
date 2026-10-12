# 07 — Thermomechanical processing: rolling, extrusion, forming

**Scope.** Physical-metallurgy view of the wrought-Al process chain *after casting*: preheat/homogenisation as a working step → hot breakdown and tandem hot rolling → coiling → cold rolling (sheet, fin, foil) → intermediate/final anneal; continuous-casting routes; direct/indirect extrusion (incl. multi-port heat-exchanger tube); constitutive (hot and cold) flow-stress laws; texture/earing; sheet formability metrics. Priority alloys: 3xxx heat-exchanger/foil/fin (AA3102, AA3207, 3003, 3004/3105), plus 1xxx, 5xxx, 6xxx, 8xxx (8011/8006).

**Status:** literature distillation, 2026-10-12. Every number carries a source tag `[Ref p./§]`. Text marked **(general knowledge)** is not in the accessible sources and is kept minimal. Text marked **(derived)** is arithmetic done here from cited inputs. Text marked **(inference)** is a design conclusion drawn here from cited facts. `[INT-…]` refs are the user's own working spreadsheets — they are *heuristics/models, not literature*, and are flagged as such.

**Biggest caveat (updated 2026-10-12).** Per-alloy hot-working constants (α, n, Q, A) are now available from [SH Table 4.1 p.132] for 31 alloy conditions, including 1050, 1100, 3003, 3004, 3005, 3105, 5xxx, 6xxx and 7xxx (§3.3). They are for **homogenised DC material** tested mainly in torsion. Sheppard warns that cast vs homogenised material can differ considerably [SH p.136]. No constants exist for 3102, 3207 or the user's rotary-cast, unhomogenised strip, and Sheppard states no explicit T/ε̇ validity ranges (G1, narrowed).

**Full-text pass, 2026-10-12 (first attempt).** The PDFs were downloaded whole (base64) and converted locally with `pdftotext`. This worked for [RR] (3.81 MB), which is now read in full. It failed for the whole-book files of [RA] (7.19 MB) and [SH] (10.46 and 10.51 MB); the errors are in the note under §0. **Superseded by the split-part pass below.**

**[SH] and [RA] full-text pass, 2026-10-12 (split parts).** Both books are now available whole as split PDFs in Drive folder "Cloud part book" (§0). [SH] was read for Ch. 2 (equations re-checked), Ch. 3 §3.1–3.7, Ch. 4 (all), Ch. 5 (all) and Ch. 6 §6.1–6.3, §6.6–6.7. [RA] was read for §4–6, the glossary 9-3 to 9-7 and Appendices A–D. Equations and constant tables were checked on rendered page images; where the printed book itself contains an error this is stated ("misprint"). Results: G1 largely filled (§3.3, §10), G2 and G14 closed, G5 partly supported, several corrections ("corrected after full-text pass"). New material: §1, §2.2–2.4, §3.1–3.6 (incl. §3.3a, §3.5a), §4.2–4.3, §5.2, §6, §8.2–8.4a, §8.6, §10, §11.

**[TOT] full-text pass, 2026-10-12.** [TOT] is now available whole as four split PDFs (Drive folder "Cloud part book"), with a repaired text layer. Read in full: Ch. 7 *Rolling of Aluminum* (Karhausen & Korhonen, pp. 351–384) and Ch. 8 *Extrusion* (Støren & Moe, pp. 385–480). Read for specific items: Ch. 18 §5.2 *Anisotropy* (pp. 851–853, 874) and Ch. 4 §6.3 *Hot deformation* (pp. 241–244). Key figures were read from rendered page images and digitised (Ch. 7 Figs. 3, 4, 6, 8, 11; Ch. 4 Fig. 28). Digitised values are marked "(read from Fig. x)" and carry the stated reading uncertainty. All [TOT] citations now use **printed** page numbers (see §0). New material: §2.3, §3.2–3.3, §4.2–4.3, §5.1, §5.4, §7, §8.2a, §9, §10. Gaps G6 and G8 are closed; G1, G3, G4 and G7 are narrowed (§11).

---

## 0. Sources and coverage

| Ref | Title (author, year) | Drive link | Readability / coverage actually read |
|---|---|---|---|
| RA | *Rolling Aluminum: From the Mine Through the Mill*, 3rd ed. (The Aluminum Association, 2007; the copy itself is undated and cites ANSI H35.1-2006) | https://drive.google.com/file/d/1w70bnhbLUlg5Tg4tlFIa0pVEI58GRfht/view · **full text, 2026-10-12, split parts:** x https://drive.google.com/file/d/12UXG7XEDAKxSO-RD49I7SKVKxbzeIpcN/view · xx https://drive.google.com/file/d/16cJWWxpRNOj8XB6_nphTCDrMMcCp6J8o/view · xxx https://drive.google.com/file/d/1kXPDynjfAXp3GNLTGi_-bhCAgPjtQzgH/view | Clean born-digital text, two-column (reading-order text used). **Full text, 2026-10-12:** complete except **glossary p. 9-2** (Casting → Hall–Héroult), which is in none of the parts. Earlier passes had §1–8 and the glossary to "Casting". New: glossary 9-3 to 9-7, Appendix A (alloy and temper designations, ANSI H35.1-2006), **Appendix B (temper definitions, incl. H4 = lacquered/painted)**, Appendix C text (metallurgy of the alloy series), Appendix D (tolerances). **The Appendix C typical-property tables (Tables 2.1/2.1m, 2.3/2.3m, 3.3 on pp. 10C-4, 10C-6 to 10C-19) are vector or raster images with no text layer, so their values were not read** (watermarked "NOT FOR DESIGN"). Page numbers are section-pages (e.g. 5-7). Introductory and mostly qualitative, but it gives the practical plant numbers. |
| RR | *A Basic Understanding of the Mechanics of Rolling Mill Rolls* (K.H. Schröder, 2003). File "155680328-Rolling.pdf" | https://drive.google.com/file/d/1I9Qa_iFiOPw5DMU6sHFW6YAYblFC9Qyu/view | **Read in full, 2026-10-12** (downloaded whole: 3,809,860 B, 116 PDF pages = printed pp. 1–111 plus front matter; printed page = PDF page − 5; pages below are printed pages). Earlier passes had pp. 1–75. New: §4.6–4.12 (fatigue, wear, §4.8.3 bite angle and friction, roll repair, §4.10 design limits, acceptance) and Ch. 5. **§4.8.3 is qualitative.** Its bite-angle vs speed chart (Ill. 47) and campaign-friction chart (Ill. 48) are images, so no numbers can be extracted. The book has **no** rolling-force, torque or roll-flattening model. It is about roll steels and roll damage in (mostly steel) mills; little Al content. |
| SH | *Extrusion of Aluminium Alloys* (T. Sheppard, Springer/Kluwer, 1999; catalogue key S-045) | https://drive.google.com/file/d/195YE0KUFE-yMliXyp304IqoaSdvnxKVU/view (duplicate 1pJoblJP3s9o7Z_WgFM9dhMmepLi7POET) · **full text, 2026-10-12, split parts:** aaa (front matter, pp. 1–190) https://drive.google.com/file/d/1wftQcLJmeD5geAZ5jVIEIO-M351iJlhw/view · bbb (pp. 191–340) https://drive.google.com/file/d/18b3asfmzC6-2nICmwbnZPbra-DOKGV1t/view · ccc (pp. 340–420) https://drive.google.com/file/d/1E0zW4D5lPpPDANxJ_lJhkDRc9MkDNrZT/view · second split of the same edition: w (pp. 1–140) https://drive.google.com/file/d/1XLABNQn11rMti4fw4ou5HBWRH7_BbeDJ/view · ww (pp. 141–290) https://drive.google.com/file/d/1dwrrrzJRHOWCeaQp-jVCNv6YbOGSmqtG/view | OCR of a scan. Body text good; Greek letters, some equations and some table digits unreliable in the text layer. **Full text, 2026-10-12: the whole book (front matter to p. 420) is available.** Read: Ch. 2 equations (re-checked on page images), Ch. 3 §3.1–3.7, **Ch. 4 in full** (§4.2 Zener–Hollomon and flow stress, Table 4.1 constants; §4.6 pressure, Table 4.2; §4.7 surface criteria; §4.8 subgrain size; §4.9 recrystallisation; §4.10 properties; §4.11 flow and substructure; §4.12 press quenching; §4.13 limit diagrams), **Ch. 5 in full** (homogenisation and extrusion conditions per alloy series, §5.10 extrudability and limit diagrams), Ch. 6 §6.1–6.3 and §6.6–6.7 (6xxx homogenisation, quench sensitivity, texture, defects). Not used: §6.4–6.5 (surface generation, alternative diagrams), Ch. 7 (plant), Appendix 1 composition tables (OCR digits unreliable). **Table 4.1 (p. 132) and Table 4.2 (p. 146) were checked digit by digit on the page images**; the same values are in the coordinator-verified text `cloudpart4/txt/w.txt` lines 6757–6793 and `ww.txt` lines 253–265. Printed page = PDF page − 10 (aaa, w) or + 190 (bbb). |
| MFH | *Metal Forming Handbook* (Schuler, Springer 1998). File "3c-handbook-metal-forming.pdf" | https://drive.google.com/file/d/1n5Yidy74bZxj6ZifvCNtq0iRtk2nyh43/view ("vasevska.pdf" 1vbIfSVGbqJfheI2yJKigh5nZAdIK7KI4, 28.6 MB, gives **identical** extracted text, so it was read once) | Clean text, pp. 1–~60 of ~560: Ch. 2 basics and early Ch. 3 press design. Sheet-forming chapters (Ch. 4 deep drawing, bending, etc.) **not returned**. No Al-specific content. |
| POL | *Light Alloys*, 4th ed. (I.J. Polmear, 2006). File "115132137-Light-Alloys.pdf" | https://drive.google.com/file/d/1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w/view | Clean text, pp. 1–~189 (to §3.6.1). Used §2.1 (work hardening, FLC, texture, earing, annealing), §3.1 (casting, homogenisation, fabrication, heat treatment), §3.3, §3.4.3. §3.6.5 canstock **not returned**. |
| TOT | *Handbook of Aluminum Vol. 1: Physical Metallurgy and Processes* (Totten & MacKenzie eds., Dekker 2003; catalogue key S-029). Earlier pass: file "Alminium.pdf". **Full text, 2026-10-12:** the four split parts in Drive folder "Cloud part book": `Al 1-400.pdf` (front matter + pp. 1–388), `ACFROG~1.PDF` (pp. 388–788), `Al 1-800.pdf` (pp. 788–988), `1309.pdf` (pp. 989–1296) | https://drive.google.com/file/d/1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz/view (earlier pass) · parts: https://drive.google.com/file/d/1Yxag4tVsKp2w7GaNvUqpz09wJRuCpLVT/view · https://drive.google.com/file/d/1EwIKZG891qUZJJfloJCpHAP2hJmgXhZE/view · https://drive.google.com/file/d/10ilZD0Rt4LM1rUzaCa9hLB0Up-NaH7a3/view · https://drive.google.com/file/d/1KmVD2fbnjMnPd2M5YfDEQaI0OflR_NMD/view (part 4, not used here) | **Earlier pass:** OCR with substituted glyphs, PDF pp. 1–186 (Ch. 1–3) only. **Full-text pass, 2026-10-12** (text layer repaired; equations and figures checked on rendered page images): **Ch. 7 Rolling (pp. 351–384) and Ch. 8 Extrusion (pp. 385–480) read in full.** Ch. 18 Sheet forming §5.2 (pp. 842, 847, 851–853, 874) and Ch. 4 §6.3 (pp. 241–244) read for specific items. **All [TOT] pages are now printed (book) pages.** Old "PDF p." citations were converted with printed = PDF − 12. The offset was verified on six earlier citations (Tables 2–3, the dispersoid size, the Al₁₂(Fe,Mn)₃Si statement, the texture paragraph, all in Ch. 3). Ch. 7 and Ch. 8 contain **no per-alloy hot-flow constants** and no foil pass schedules (G1, G4). |
| TRC | Krstić Vukelja, Duplančić, Lela, "Continuous roll casting of aluminium alloys – casting parameters analysis", *Metalurgija* 49 (2010) 115–118 | https://drive.google.com/file/d/16xRFXhETDI8_5cYr9x9tuBxUueKkY9q0/view | Read in full (4 pp.). Some printed units look wrong (flagged where used). |
| WIL | C.R. Williams, MSc thesis, Ohio Univ. 2012: *Effects of Sc and Zr additions on Al … post-braze grain structure, and extrusion* (AA3102 multi-port tube) | https://drive.google.com/file/d/1MYsjf2OwlDfrOtnb1zQas-DV9wfunqne/view | Read in full. Industrial MPE-tube extrusion data for AA3102. |
| MM | Alcoa Micromill™ presentation (J.F. Butler, 2015). File "document.pdf" | https://drive.google.com/file/d/1OYezPC_Eif_mKOTmq2xeExuqfcsTai1N/view | Read in full. Investor/marketing slides; treat the numbers as vendor claims. |
| INT-CRM | User spreadsheets "EN_AW_3207_CRM_Reduction_Table.xlsx" and "EN_AW_Master_CRM_Reduction_Tables.xlsx" | https://drive.google.com/file/d/1r-GFxL4bVuGG_ZGm_Lix-SQ3Upc7gROk/view · https://drive.google.com/file/d/1KN_kyx3RDw0QfLNvi1UHx7UYP5xwLjpq/view | Read in full. **Internal heuristics** (HRM/CRM gauge rules for cold-extrusion slugs). No literature backing is given. |
| INT-RX | User spreadsheet "AA3207_Recrystallization_Simulation.xlsx" (newest of 4 versions, 164 kB) | https://drive.google.com/file/d/1L9MDNPrCcWymlvgcowcv6Gf34eLJvwm2/view | Read in full. **Internal calibrated JMAK model.** Used here only for cross-checks. |

**Drive download limit test (2026-10-12).** Whole files were requested with the Drive connector's `download_file_content` tool (base64 output).

| File (bytes) | Result |
|---|---|
| [RR] 3,809,860 | OK (5,079,932-character base64 result, saved to disk and decoded; size matches Drive metadata) |
| S-043 EAA brochure 3,278,124 (ch06) | OK |
| [RA] 7,188,660 | Failed twice: *"The connection to MCP server "Google_Drive" was closed because a message from the server was too large or could not be parsed, so the result of tool "download_file_content" was not read."* |
| [SH] 10,463,104 (1pJoblJP3s9o7Z_WgFM9dhMmepLi7POET) | Failed with the same connection-closed message (the server accepted it, the client transport dropped it) |
| [SH] 10,512,541 (195YE0KUFE-yMliXyp304IqoaSdvnxKVU) | Refused by the server: *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API."* |

So there are two limits. The server enforces a hard 10 MB (10,485,760 B) cap. Below that, the client transport fails somewhere between 3.81 MB and 7.19 MB of file size (≈ 5.1–9.6 M base64 characters). **Practical rule: files ≤ ~3.8 MB can be fetched whole. Larger books must be split (e.g. per chapter) into ≤ ~3.8 MB PDFs on Drive first.**

**Resolved 2026-10-12.** The user put split parts of [SH] and [RA] into Drive folder "Cloud part book". Parts up to 5.07 MB downloaded; parts of 6.6 MB and above failed. [SH] and [RA] are now read from these parts (row notes above).

Drive full-text searches run: `Zener-Hollomon`, `Zener`, `flow stress`, `hot rolling`, `extrusion`, `earing`, `forming limit`, `cold rolling`, `hyperbolic sine / subgrain size / peripheral coarse grain / extrudability`. Hits inside the `microstructure-sim-v2.14.0` tree (`models/*.js`, `*.jsx`, tests) were **not opened**, as instructed. Out of scope: the Nimonic 80A hot-deformation paper ("Microstructure_URN-NBN-SI-DOC-OFLHAUYU.pdf"; Ni superalloy, Z-methodology only). DC-casting, recrystallisation and Sc/Zr books (Eskin, Humphreys & Hatherly, Røyset) are assumed to be covered by companion KB files.

---

## 1. Conventions used in this file

- Thickness true strain in rolling: ε_t = ln(h₀/h₁). The tensile-test true strain ln(A₀/A_f) is the same quantity [POL §2.1.1 p.35–36]. Logarithmic principal strains sum to zero (volume constancy): φ₁+φ₂+φ₃ = 0 [MFH §2.2.2 p.27–28].
- The *principal* deformation φ_g is the one whose sign differs from the other two (= |largest|). It is the input for all force/work estimates [MFH §2.2.2 p.28].
- Von Mises equivalent strain for plane-strain rolling: ε̄ = (2/√3)·ε_t **(general knowledge)**. ⚠ [INT-CRM] and [INT-RX] both use ε_t (57.3 % → 0.85; 45 % → 0.598). This is consistent with each other but is 13 % below ε̄. Check which strain any constitutive or recrystallisation law was fitted with before mixing them.
- Flow stress (Tresca form): k_f = σ_max − σ_min [MFH §2.2.1 p.25]. Von Mises: k = σ̄/√3 [SH §2.1 p.26].
- Homologous temperature T_h = T / T(lowest-melting phase). Above 0.5 T_h aluminium recovers dynamically to a stable polygonised substructure [SH §1.2 p.6].
- Zener–Hollomon parameter: Z = ε̇·exp(ΔH/(G·T)), where ΔH is the activation energy for deformation and G the gas constant, 8.314 J mol⁻¹ K⁻¹ (Sheppard's notation; T in K) [SH §2.2 eq. 2.4 p.28; §4.2.1 p.128]. Same definition, Z = ε̇·exp(Q_def/RT), in [TOT Ch.7 eq. 3 p.359]. Sheppard's ε̇ is the **mean equivalent strain rate**, which is specific to the extrusion geometry [SH p.128].
- Sheppard's units: α in m² MN⁻¹ (= MPa⁻¹), ΔH in J mol⁻¹, A in s⁻¹ (tabulated as ln A), stress in N mm⁻² (= MPa) [SH Table 4.1 p.132; p.133].
- **Z values are only comparable when computed with the same Q.** Q, n and A come from one joint regression and are interrelated; changing Q changes the best-fit A and n [SH p.135]. Never combine a Q from one source with A or n from another (§3.3).
- **Hot vs cold working.** [TOT Ch.7] defines hot working as forming above 0.6 T_m, "which in the case of aluminum is above 300 °C" [p.354]. It puts the cold-working regime below 100 °C, where climb and cross-slip are much restricted [p.362]. The 100–300 °C range between them is called warm working here (inference; [TOT] does not name it).
- Equivalent stress and strain rate (von Mises): σ̄ = √(3/2·s_ij s_ij), ε̄̇ = √(2/3·ε̇_ij ε̇_ij) [TOT Ch.8 eq. 8–9 p.434].

---

## 2. Process routes and plant-level numbers

### 2.1 Mechanisms (what each step does to the microstructure)

- **Melt treatment.** Hydrogen solubility is 0.68 cm³/100 g in the liquid vs 0.036 in the solid at T_m (×19) [POL §3.1.1 p.97]. Solid solubility is ~5 % of the liquid value [RA §3 p.3-1]. Melt H must be < 0.15 cm³/100 g to avoid porosity [POL §3.1.1 p.98]. Inline degassers (SNIF, ALPUR, LARS) use Ar with up to ~3 % Cl₂ [RA §3 p.3-2]; furnace fluxing uses < 10 % Cl₂ [RA §3 p.3-1]. Ceramic foam filters have 20–70 ppi (8–30 per cm); deep-bed filters are 125–380 mm of 6–19 mm alumina media [RA §3 p.3-2].
- **Grain refining.** 5Ti-0.3B or 5Ti-0.15C rod (Ø 10 mm), addition < 0.01 wt %, fed at the last minute because the refiner fades/agglomerates if held [RA §3 p.3-3]. Al-5Ti-1B is now the favoured composition [POL §3.1.3 p.103]. Zr poisons TiB₂ [POL p.104].
- **DC casting.**
  - Holding hearth 700–730 °C; the metal loses 22–28 °C on the way to the pit [RA §3 p.3-5].
  - Mould depth ~150 mm; casting speed 40–100 mm/min; the shell leaves the mould at 300–500 °C [RA §3 p.3-6].
  - Ingots up to ~760 mm thick, 2300 mm wide, 9 m long (~27 t) [RA p.3-6]. Polmear gives ≤ 650 mm sections, ≤ 15 t, cooling 1–5 °C/s [POL §3.1.1 p.99].
  - The shrinkage gap causes a solute-enriched surface zone, which is removed by **scalping** [RA p.3-6]. Surface inverse segregation can cause edge cracking in rolling [POL p.100].
  - EMC (electromagnetic casting) avoids the enrichment zone; 3xxx/5xxx beverage stock has been rolled without scalping [RA p.3-7; POL p.100].
- **Preheat/homogenisation.** Five purposes [RA §3 p.3-8]: (1) put the metal above the recrystallisation temperature so it does not strain-harden; (2) homogenise coring; (3) spheroidise insoluble constituents (better formability); (4) soften; (5) relieve stresses.
  - Example practice: either straight to ~455 °C and held, or overshoot, hold, then fan-cool to rolling temperature [RA p.3-8].
  - Homogenisation window 450–600 °C, typically 6–24 h [POL §3.1.4 p.104–105].
- **Hot rolling.** Welds casting pores. Breaks up and redistributes Fe/Si constituents, turning the brittle cast structure into ductile wrought metal [RA §4 p.4-6/4-7; POL §3.1.5 p.107]. Grains elongate; recovery and partial recrystallisation occur pass-to-pass depending on alloy, temperature and pass reduction [POL p.107]. Most products recover dynamically. Static recrystallisation can happen between or after passes. High-Mg alloys (lower SFE) can recrystallise **dynamically** [TOT Ch.3 p.130]. ⚠ The [TOT] chapters disagree on DRX in commercial alloys (§3.1).
- **Cold rolling** adds dislocations (H-tempers). It has a natural strength limit; a fully cold-worked sheet breaks on small further strain [RA §4 p.4-7].
- **Annealing.** "Recrystallisation temperature" is a range that depends on alloy, prior strain and soak time [RA §5 p.5-6]. Recrystallisation of hard-rolled pure Al takes several hours at 280 °C, a few minutes at 380 °C, and seconds at 500 °C [POL §2.1.6 p.42].

### 2.2 DC-ingot → coil → sheet/foil route: quantitative parameters

| Step | Parameter | Value | Ref |
|---|---|---|---|
| Preheat | Rolling-entry example | ~455 °C (850 °F) | [RA p.3-8] |
| Preheat | Upper limit for hot rolling | 10–50 °C below solidus, to avoid grain-boundary weakening/cracking | [RA p.4-6/4-7] |
| Breakdown (reversing 4-high) | Ingot thickness in → slab out | 200–600 mm → 15–35 mm | [POL §3.1.5 p.107] |
| | | ~760 mm max → 100–125 mm "slab" | [RA §5 p.5-1, 5-3] |
| | Pass example | 380 → 330 → 280 mm, i.e. r = 13 %, ε_t = 0.14 per pass **(derived)** | [RA p.5-3] |
| | First-pass gap | 50–75 mm less than ingot thickness | [RA p.5-1] |
| | Drive power / force | 3730 kW per work roll (7460 kW total); ~3635 t separating force | [RA p.5-1] |
| | Mill size naming | by roll-barrel length, e.g. 3 m and 4.25 m mills | [RA p.5-1] |
| | Coolant | water + ~5 % oil emulsion, filtered and recirculated; off at bite, on during the pass | [RA p.5-2] |
| | Edge control | vertical edger rolls (edge cracking, width spread); cross-rolling to gain width | [RA p.5-3] |
| Intermediate hot / reversing coiler mill | Gauge | to ~25 mm (intermediate) or coiled at < 12 mm on a single-stand reversing hot mill with 1–2 coilers, 1–3 wraps | [RA p.5-3, 5-4] |
| Tandem hot mill | Exit gauge | 2.5–8 mm, then coiled | [POL p.107] |
| | Sheet for < 1 mm final gauge | hot rolled to 3–6 mm first | [RA §5 p.5-7] |
| | Speed | up to ~600 m/min | [RA §4 p.4-6] |
| | Inter-stand control | speed trimmed for tension (fast); gap (slow) | [RA p.5-4/5-5] |
| Hot coil | Dimensions | ID 500–600 mm; OD > 2285 mm (up to 2.4 m) | [RA p.5-4] |
| Cold rolling | First pass | ~50 % reduction; later passes similar or smaller | [RA p.5-7] |
| | Can-body stock | 2.5 → 0.25 mm in 4–5 single-stand passes, or 1 pass on a tandem. ε_t = 2.30, ε̄ = 2.66; ≈37–44 %/pass **(derived)** | [RA §5 p.5-8] |
| | Speed | 1525–1830 m/min single stand; up to 2135 m/min (fastest mills) | [RA p.5-7; p.4-6] |
| | Strip heating | to ~80 °C or more, removed by coolant | [RA p.5-7] |
| | Lubricant | light petroleum distillate + load-bearing additive. Low viscosity removes heat better; the lower limit is set by evaporation/flash point. Emulsions used at high speed | [RA p.5-8] |
| | Bright surface | small final-pass reductions, polished rolls | [RA p.5-7] |
| | Minimum gauge | alloys ~0.05 mm; pure Al foil 0.0025 mm | [RA p.5-7] |
| Annealing (NHT alloys) | Full anneal (O) | 335–405 °C, 0.5–2 h (usually ~1 h), controlled cooling | [RA §5 p.5-7] (page cite corrected after full-text pass; was p.5-6) |
| | Literature windows | 345–415 °C, minutes to 3 h [POL p.107]; 350–420 °C [POL p.109]; 300–420 °C [POL p.42] | |
| Annealing (HT alloys) | Remove cold work / remove heat-treat effects | ~2 h at 335–370 °C / 400–425 °C, slow controlled cool | [RA p.5-6] |
| Stabilisation (5xxx, 3004) | H3x | ~180 °C (350 °F) [RA p.5-7] (page corrected after full-text pass; was p.5-6); **vs** 120–150 °C [POL §3.3.3 p.130]. ⚠ The two sources differ. | |
| Precipitation heat treatment (HT sheet) | Artificial ageing | 115–190 °C, ~5–48 h | [RA §6 p.6-3] |
| Hot rolling of HT alloys | Side effect | the strip may be "sufficiently heated and cooled during hot-rolling to undergo some partial solution heat treatment and precipitation hardening" | [RA §5 p.5-6] |
| Furnace type | Batch coil vs continuous strip | Batch is most common. Continuous strip heats fast and gives a finer grain | [RA p.5-7] |
| Plate | Cold reduction for strength | up to ~30 % (armour, boat) | [RA §7 p.7-1] |
| | Stretch | 1–3 % typical; ≤ 15 % for 2024/2219 T86/T87 | [RA §7 p.7-2] |
| | Reheat (slab) | 2–24 h depending on alloy | [RA p.7-1] |
| Gauge/profile | Mill accuracy | roll Ø tolerance 0.006 mm; stack eccentricity ≤ 0.01 mm | [RA §4 p.4-6] |
| | Typical tolerance | 5052, 0.75 mm, ≤ 1000 mm wide: ±0.045 mm; 1000–1500 mm wide: ±0.06 mm (ANSI H35.2) | [RA §8 p.8-1/8-2] |

**Product definitions** [RA §1 p.1-4]:
- plate > 6 mm (US ≥ 6.3 mm);
- sheet > 0.20 to ≤ 6 mm;
- foil ≤ 0.20 mm.
- By these definitions, 0.115 mm air-conditioner fin stock falls in the foil range [RA §1 p.1-4; self-test 1.11].
- Household foil is ~0.0165 mm [RA p.1-2].

### 2.3 Continuous-casting routes

| Route | Thickness | Cooling rate | Speed / productivity | Ref |
|---|---|---|---|---|
| Twin-roll caster (TRC) | < 25 mm as-cast; typically 4–12 mm; ~3–10 mm in [POL] | 55–555 °C/s [RA]; 10²–10³ °C/s [POL] | 2–3 m/min; 10–18 kg h⁻¹ cm⁻¹ width; width 760–2030 mm | [RA §3 p.3-3/3-4; POL p.102; TRC p.115] |
| Belt (Hazelett) | 12–25 mm [RA]; 12–75 mm, ≤ 2.3 m wide [POL]; **16–20 mm, then tandem hot rolled to 2–3 mm** [TOT] | 19 mm slab: 11–40 °C/s at surface, 4 °C/s at centre | 21–24.5 t m⁻¹ h⁻¹ | [RA p.3-4; POL §3.1.2 p.101–102; TOT Ch.7 p.354] |
| Block caster | slab (plate gauges) | 0.5–5 °C/s; exits ~540 °C (little reheat needed) | ~6 m/min; 180–225 kg h⁻¹ cm⁻¹ | [RA p.3-4] |
| DC (reference) | 400–760 mm | 1–5 °C/s | 40–100 mm/min | [RA p.3-6; POL p.99] |

- **[TOT Ch.7] on strip casting** (read in full 2026-10-12). Thin-slab or thin-strip casting is the option "for still smaller amounts of production" than reversing roughing + Steckel lines [p.352]:
  - **Twin-roll caster:** low-capacity plants, "mainly soft alloys", nominal minimum strip thickness **6 mm** [p.352].
  - **Belt caster + tandem hot mill:** "a full range of alloys including the 1100, 3000 and 5000 series"; cast 16–20 mm, finished to 2–3 mm [p.354].
  - ⚠ **Sources differ on TRC gauge:** 6 mm minimum [TOT, 2003] vs typically 4–12 mm [RA, 2007] and ~3–10 mm [POL]. The difference is probably the publication date, i.e. thin-gauge TRC developments (inference); not resolved here.
  - Plant scale for comparison: reversing roughing + tandem finishing > 600,000 t/a; a single-stand reversing hot mill alone ≤ 160,000 t/a; reversing roughing + Steckel suits small "just-in-time" batches but can cause **longitudinal variation of texture and microstructure** [p.352].
  - No caster cooling rates, no in-line hot-rolling schedules and no strip-cast microstructure data are given.
- Share: ~20 % of North-American sheet and plate is continuously cast [RA p.3-3].
- Glossary definition of a roll caster: "Some hot working takes place as the solidified metal is rolled through the gap, but the product thickness is achieved mainly by the casting, not the rolling, process" [RA §9 p.9-4].
- **Metallurgical differences vs DC** [RA p.3-3]:
  1. much less hot work;
  2. no homogenisation;
  3. no scalping;
  4. faster solidification → higher supersaturation and less segregation ("partly pre-homogenised").
- Dendrite cell size is 30–70 µm in DC vs 5–10 µm in TRC [POL p.102]. Transition-metal (Fe, Mn) supersaturation is retained, so properties differ from DC even at equal composition; sometimes a different or leaner alloy is used [POL p.102].
- Making CC sheet as formable as DC "may significantly reduce the advantages" of CC [RA p.3-3]. Markets include **foil and fin stock** [RA p.3-3].
- **TRC industrial window (AA1235 / AA8011 foil feedstock; Pechiney caster, TLM Šibenik)** [TRC p.115–117]:
  - Ø690 mm rolls, 1740 mm face; tip set-back 35–55 mm.
  - Melt 685 ± 5 °C; roll gap 5.2 mm; contact length ("angle") ~47–50 mm.
  - Strip 6.3–6.5 mm × 1020–1520 mm.
  - Graphite lubricant 2 L per 75 L water; Al-Ti-B wire at 28–35 cm/min.
  - Quality targets: longitudinal gauge < ±2 % per coil, < ±1 % per roll revolution, crown 0–1 %, wedge ≤ 1 %.
  - Trends: narrower strip raises roll force and contact length; thinner strip raises force and contact length.
  - Recommendations: cast close to the liquidus, keep a high melt level, use a lower casting speed, control the nozzle geometry.
  - ⚠ Printed units "0.95–1.50 cm/min" and "5·10³ kN/mm" are implausible. They are probably m/min and kN/m.
- **Micromill (Alcoa) claims** [MM slides 8, 11, 12]:
  - "20-day rolling process to 20 minutes", 50 % less energy, ¼ of the footprint.
  - 6xxx: FLD₀ 26–28 vs 23.6 for DC; LDR 2.08–2.13 vs 1.88–1.98 for DC 6022.
  - "MMHF-T4" 1.5 mm: TYS 152 MPa, UTS 282 MPa, uniform elongation 25.8 %, FLD₀ 33.7, LDR 2.13–2.18 vs 5182-O (124 / 275 / 21.2 %, FLD₀ 23.4).
  - This is a vendor presentation. The route shows that fast solidification plus in-line rolling can *beat* DC formability. It contradicts the [RA] caution, so it is unproven for 3xxx.

### 2.4 Design levers (process route)

1. **CC vs DC for 3xxx fin/foil** (inference from [RA p.3-3; POL p.102]). CC retains Mn/Fe in supersaturation and skips homogenisation. So the Mn-dispersoid population, and with it the recrystallisation temperature, sag resistance and post-braze grain size, is decided **at the first anneal**, not at preheat. Re-tune the Mn/Fe/Si balance and the anneal heating rate for CC; do not copy DC practice.
2. **Hot-band gauge sets the cold strain budget.** [RA p.5-7] gives 3–6 mm hot band for < 1 mm sheet. [INT-CRM] picks the HRM exit gauge so that the CRM ε_t is ≥ 0.85 (3207), ≥ 0.80 (3102), ≥ 0.95 (3003/1070), before the final anneal (internal heuristic).
3. **Preheat practice is an alloy-design variable.** Slow heating (≈ 75 °C/h) is needed to nucleate a fine, uniform dispersoid population (Al₆Mn, Al₁₂Mg₂Cr, Al₃Zr) [POL §3.1.4 p.106]. In the cited Al-Zn-Mg-0.3Mn case, 50 °C/h gave Al₆Mn nucleated on MgZn₂, and 500 °C/h did not [POL Fig. 3.8 p.106]. Al₆(Fe,Mn) → α-Al₁₂(Fe,Mn)₃Si conversion during homogenisation is key for canstock [POL p.107].
4. **Rule of thumb for homogenisation time:** +50 °C → ~⅓ of the time [POL p.105]. This implies an apparent Q ≈ 116 kJ/mol at 500→550 °C **(derived)**, which matches the Mg/Si/Cu entries of [SH Table 2.3] (117–126 kJ/mol) but not slow-diffusing Mn (§3.5).
5. **Homogenisation sets the dispersoid state that controls hot-band RX.** In AA3003 the mean dispersoid size can be varied between 0.03 and 0.17 µm, with number density falling from 740 to 11 µm⁻³ between low- and high-temperature homogenisation [TOT Ch.7 p.355, citing Doko et al.]. The dispersoid size "strongly affects recrystallization during and after hot rolling". Cooling from homogenisation to the rolling temperature lowers the solute further and grows coarser secondary particles [p.355].
6. **Homogenisation windows by series [SH Table 5.1 p.206]** (homogenisation is typically 20–50 °C below the solidus and as close as possible to the first hot-working temperature [p.205]):

   | Series | Solidus (°C) | Homogenisation (°C) | Extrusion (°C) |
   |---|---|---|---|
   | 1xxx | 640–650 | 560–605 | 450–550 |
   | 2xxx | 500–650 | 480–530 | 400–480 |
   | 3xxx | 630–645 | 530–620 | 480–520 |
   | 5xxx | 570–630 | 380–550 | 400–480 |
   | 6xxx | 580–620 | 560–600 | 430–500 |
   | 7xxx | > 500 | 400–500 | 390–450 |

7. **As-cast supersaturation rises with freezing rate; Fe and deformation release it [SH §3.3.2 p.105–106].**
   - Mn, Fe and Sc are the supersaturating species, and "the degree of as-cast supersaturation increases as the freezing rate increases" [p.105].
   - The equilibrium Mn solubility is lowered by Fe, Si, Mg and Cu, so 3003 or 3004 has a lower Mn solubility than binary Al-Mn. Deformation lowers it further, "especially in extrusion where the high strains assist precipitation" [p.105].
   - 3003 (1 % Mn, 0.38 % Fe, 0.14 % Si): about 94 % of the Mn is in solid solution as cast. Printed: supersaturation ≈ 0.30 % Mn at 610 °C and ≈ 0.55 % Mn at room temperature; extrusion lowers the equilibrium Mn concentration to ≈ 0.15 %; an unhomogenised extrudate would carry ≈ 0.56 % Mn supersaturated [p.105; digits checked on the page image]. These figures do not add up to one consistent balance as printed, so use them for direction only.
   - As little as **0.02 % Fe** strongly accelerates the loss of Mn supersaturation (Al-1Mn at 530–550 °C). Without Fe or Cu, up to 0.2 % Si also accelerates it, but the Si effect vanishes when Fe and Si are both present [p.106].
   - The first dispersoids (≤ 0.2 µm) form at the dendrite-cell peripheries, then in the cell interiors. Secondary precipitates are finer (0.1–0.3 µm), mostly plate-like and Fe-poor [p.106]. Si enhances Fe precipitation; Fe, Cu, Mg and Si enhance Mn precipitation [p.106].
   - Faster freezing gives finer constituents, thinner interdendritic stringers and a smaller particle size after homogenisation; Fe additions to Al-Mn give more, smaller particles [p.108].
8. **Leaving out homogenisation.** For 1xxx DC billet, omitting the homogenisation step "yields higher strength and lower ductility" in the as-extruded product [SH §5.2 p.207]. In an Al-0.30Fe-0.15Si alloy, raising the homogenisation temperature *raised* the later recrystallisation temperature (most clearly between 400 and 500 °C), because fine as-cast precipitates redissolve and the solute retards softening and favours coarse imperfect grains [p.206]. Fe-bearing precipitates < 0.2 µm restrain dynamic recovery more than the larger, fewer Mn-bearing ones; more fine precipitates (faster cooling after homogenisation) lower the hot workability [p.207]. Recommended for 1xxx: ≥ 6 h at 600 °C, furnace or air cooled [p.207].
9. **Unhomogenised material needs a higher RX temperature [SH §5.6 p.222–223, Fig. 5.13(a)].** After 50 % hot rolling at 400 °C, the temperature for 100 % RX of *as-cast, unhomogenised* material was 430 °C (AA5252) and 540 °C (AA5454). Homogenising at 600 °C instead of 500 °C lowered it by 40 °C (5252) and 100 °C (5454). "The homogenization treatment can be designed such that subsequent recrystallization may be enhanced or retarded" [p.223].

**Relevance to the slug route (rotary-cast 22 mm strip, ≈ 500 °C → in-line hot rolling → ≈ 380 °C → water bath).** Inference from the sources above.
- [TOT] does not cover rotary (wheel) casters; the belt caster is the closest analogue it describes. The 22 mm cast strip is just above [TOT]'s belt-caster window (16–20 mm) and inside [RA]'s 12–25 mm. [TOT] confirms that belt-cast strip + tandem hot rolling is used industrially for 1100, 3000 and 5000 alloys [Ch.7 p.354]. So the route itself is established; what differs is the short, cool in-line hot schedule and the quench in place of hot coiling.
- With no homogenisation, the user's "homogenisation" is the 500 → 380 °C hot-rolling window plus the final anneal. Item 5 shows that the dispersoid population (0.03–0.17 µm, 11–740 µm⁻³ in DC 3003) is the main RX-control variable, and on this route nothing sets it deliberately before the cold mill. [TOT] notes that falling temperature and deformation-induced vacancies drive "further precipitation of secondary phases" during hot rolling [Ch.7 p.356]. That is a dynamic-precipitation path, but the time in the 500 → 380 °C window is only seconds to about a minute (ch. 19 §1). Expect a largely supersaturated hot band whose Mn dispersoids form mainly during the final anneal (consistent with §2.4 item 1; the size of the in-line precipitation is unquantified).
- **Added after the [SH] full-text pass (inference from items 7–9).**
  - The rotary caster's high freezing rate raises the as-cast Mn/Fe supersaturation [SH p.105]. Trial alloy T11 (Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26) has far more Fe than the 0.02 % that already accelerates Mn precipitation [SH p.106]. Mn release during the slug anneal should therefore be fast once it starts, and the cold strain (which lowers the effective Mn solubility [p.105]) speeds it further. T11's Mn is low, so the *amount* of Mn dispersoid is small. Fine Fe/Si-bearing precipitates are then the more likely RX-retarding particles (compare item 8 and [TOT Ch.7 p.356]).
  - Items 8 and 9 give the direction for unhomogenised strip: higher strength, lower ductility and a **higher RX temperature** than homogenised DC material of the same composition. The magnitude for lean 3xxx is not in any source (5xxx: +40 to +100 °C relative to a 600 °C homogenisation). Budget for it when setting the slug-anneal temperature and confirm it in trials.
  - Sheppard's homogenisation window for 3xxx (530–620 °C) lies above the 500 °C caster exit. The in-line route never reaches it, so the spheroidisation and α-transformation of the constituents that homogenisation would give (§3.5a) do not happen. The constituents stay as cast, broken up only by the hot and cold reduction.

### 2.5 Pitfalls / defects (route)

- Enrichment zone and surface ripples not scalped → slivers rolled in, edge cracks [RA p.3-6/3-7; POL p.100].
- Hot-roll pick-up ("roll coating"): a little helps bite; too much prints or flakes onto the product [RA §4 p.4-3].
- Lubricant too low → sticking; too high → poor bite and dull surface. Reduction marks and "herringbone" appear on the tandem hot mill [RA p.5-2, 5-5].
- **Negative crown** (thick edges) occurs in dilute, soft alloys (1xxx, 3102-type), which spoils flatness in cold rolling. Profile must be built while the strip is hot and thick; final flatness is set by the last (cold) stand [RA §5 p.5-8].
- **Age-softening** of strain-hardened 5xxx and 3004 (Mg leaving solution) → H3x stabilisation [RA p.5-7; POL p.130] (RA page corrected after full-text pass).
- Fire-cracking of work rolls is *more* likely when hot rolling Al than steel. Al conducts heat well and its oxide layer is thin, so the roll surface runs hotter despite the lower strip temperature [RR §4.5.3 p.75]. Fire-cracks are thermal-shock cracks: the hot roll surface is quenched by the coolant in a fraction of a second and cracks once the surface tensile stress reaches the shell strength. The pattern forms in the first roll revolutions. The worst cracking follows mill stops with a slab or strip in the gap [RR p.75].
  - Remedy after a stop, roughing stand: stop the coolant, open the gap, push the slab out and let the roll cool slowly.
  - Remedy after a stop, finishing stand: keep the gap closed and the coolant on until the strip is black, then shut down [RR p.76].
- Friction is governed by the roll *surface* (fire-crack pattern, roughness), not by the roll-grade friction coefficient [RR §3.6 p.51–52] (page cite corrected after full-text pass; was p.50–51).

---

## 3. Hot-deformation constitutive behaviour

### 3.1 Mechanisms

- High SFE (~170 mJ m⁻² [POL §2.1.2 p.36]) → dynamic recovery dominates. Above 0.5 T_h a stable polygonised substructure forms; **subgrains stay equiaxed while grains elongate and do not recrystallise during working** [SH §1.2 p.6].
- Dispersoid-formers (Cr, Mn, Zr) precipitate during homogenisation. They are strung out in the working direction and delay or stop static recrystallisation, which keeps "fibrous" grains [SH §1.2 p.6; TOT Ch.3 p.130].
- At steady state the state variables are constant (dSᵢ/dt = 0), so σ = f(ε̇, T). This is valid for bulk extrusion. It is *not* valid for incremental FE at deformation-zone entry, where elements are not yet at steady state [SH §2.2 eq. 2.3 p.28].
- PSN nucleus size falls as deformation temperature falls and strain rate rises [TOT Ch.3 p.130].
- Hot-worked substructure strengthens via σ = σ₀ + k₁d⁻ᵐ:
  - m = 1 for cells (~1° misorientation, low-temperature working);
  - m → 0.5 for subgrains (recovered).
  - Subgrains from hot working strengthen more effectively [POL §2.1.2 p.36–37; TOT Ch.3 p.102].
- **Hot flow is rate-controlled, not strain-controlled.** At 450–600 °C, recovery and recrystallisation remove dislocation tangles during deformation. The equilibrium dislocation density, and so the yield stress, is set by the rates of creation and destruction. Stress is "almost independent of the total strain, but extremely dependent on the strain rate", with an Arrhenius temperature dependence [TOT Ch.8 p.432–434]. Strain hardening is lowered "considerably" by dynamic recovery to polygonised arrays [TOT Ch.7 p.354].
- ⚠ **Dynamic recrystallisation (DRX): the three [TOT] chapters disagree.**
  - Ch. 7: high-purity Al recrystallises rapidly during processing (DRX). In "customary industrial alloys" DRX appears only at extremely high temperatures, by local grain-boundary bulging, so RX happens between stands or after rolling (post-dynamic/static) [TOT Ch.7 p.356].
  - Ch. 4: DRX-type flow curves were seen only in ≥ 99.999 % Al compressed very slowly (1 mm/min at 341 °C; 0.06 mm/min at 310 °C), and not in 99.99 % Al. But Mg in solid solution raises the DRX tendency in Al-Mg, with "similar behavior" reported for Al-Mn, Al-Mg-Mn and 99.5 % Al [TOT Ch.4 p.242–244].
  - Ch. 3: high-Mg alloys "may recrystallize dynamically" [TOT Ch.3 p.130].
  - [SH] (full text): "the softening mechanism operative in almost all Al-alloys during hot working is dynamic recovery" [p.135]. **AA5456 "has been reported to be the only commercial Al-alloy to exhibit dynamic recrystallization"**, attributed to Mg–vacancy interactions that reduce climb [SH p.165, 167]. Aluminium alloys "do not in general recrystallize during extrusion", but static RX may occur after leaving the die [SH p.196].
  - Working rule here (inference): for 1xxx/3xxx hot-mill models use static/post-dynamic RX after each pass. This is the majority view and matches [SH §1.2 p.6; p.135, 196]. Treat DRX as a possible high-Mg exception (≈ 5 % Mg, 5456 type).
- **Rate control [SH §3.4 p.113; §4.2.3 p.135].** In high-SFE Al alloys, climb aided by cross-slip controls the rate, so the hot-working activation energy is close to that of self-diffusion. Sheppard puts lattice self-diffusion in pure Al at **153 kJ mol⁻¹** and cites McQueen's 152 kJ mol⁻¹ for some Al-Mg alloys. Deviations in weak alloys are "most probably due to the regression analysis"; in highly alloyed or high-Mg alloys they are real [p.132, 135].
- **Steady state and its limits [SH §4.11 p.176–186].** Upsetting deforms the whole billet; subgrains first form at high-angle grain boundaries and at the die mouth. Only after the peak pressure does a quasi-static deformation zone with equiaxed subgrains of constant size and misorientation form; at that point generation and annihilation of dislocations balance and work hardening is zero [p.185]. The peak pressure has an Arrhenius dependence with Q ≈ 160 kJ mol⁻¹, close to self-diffusion [p.185]. Subgrain size did **not** change between billet positions where Z should differ by about an order of magnitude, so "the substructure cannot change as rapidly as any equation of state would dictate": a time term is needed when Z changes quickly [p.184–185].
- **Relevance to the slug route (inference).** The equation-of-state lag above matters for short in-line hot passes with falling temperature (500 → 380 °C). Do not assume the hot-band substructure equilibrates with the exit-pass Z.

### 3.2 Equations available from the sources

| # | Equation | Notes | Ref |
|---|---|---|---|
| H1 | Z = ε̇·exp(ΔH/(G·T)) | ΔH = activation energy for deformation, G = gas constant | [SH §2.2 eq. 2.4 p.28] |
| H2 | **Z = A[sinh(ασ̄)]ⁿ = ε̇·exp(ΔH/GT)**, so **σ̄ = (1/α)·ln{(Z/A)^{1/n} + [(Z/A)^{2/n} + 1]^{1/2}}** = (1/α)·arcsinh[(Z/A)^{1/n}] | **Verified on the page image (corrected after full-text pass; previously reconstructed from general knowledge).** Sellars–Tegart form as modified by Sheppard & Wright (1979) for the **steady-state** flow stress [SH eq. 2.4 p.28; eq. 4.1 p.128]. ⚠ Eq. 4.1 on p.128 prints "− 1" inside the root, i.e. arccosh; that is a **misprint**: eq. 2.4 (p.28) and eq. 4.7 (p.145) print "+ 1". The two forms differ only when (Z/A)^{1/n} is not ≫ 1, and the "−1" form fails for Z < A. Constants: Table 4.1 (§3.3). Used by Al companies "for on-line control in extrusion and tandem mill rolling" [p.128]. Its stated weakness: it "says nothing concerning the structural events" [p.128] | [SH p.28, 128, 145] |
| H2-fit | Regression form for α, n, Q, A | Printed: ln[sinh(ασ)] = ln(A)/n + ln(ε̇)/n + (ΔH/GT)(1/T). ⚠ **Misprinted** (sign of the ln A term, extra 1/T, missing 1/n). The algebraically correct form is **ln[sinh(ασ)] = −ln(A)/n + ln(ε̇)/n + ΔH/(nGT)** (derived from H2). Torsion procedure: stress at 0.72 of the outer radius (Barraclough); correct for the test's temperature rise (finite difference) before regressing; α by Garofalo's method; gauge length:diameter ≤ 1 [SH §4.2.2 p.129] | [SH p.129] |
| H2-hi | High-stress approximation | Printed: σ̄ ≅ (ln 2)/(αn) + (1/n)·ln(Z/A). ⚠ Dimensionally inconsistent as printed. From H2 with sinh x ≈ eˣ/2 the correct form is **σ̄ ≅ (1/α)·[ln 2 + (1/n)·ln(Z/A)]** (derived). Power-law regime for ασ < 0.8, exponential regime for ασ > 1.2 [SH p.133] | [SH eq. 4.7 p.145] |
| H2a | **Zener–Hollomon (sinh) form as printed in [TOT]:** σ̄ = (1/α)·arcsinh(Z/A) = (1/α)·arcsinh[ε̄̇·exp(Q/RT)/A] | Stress independent of total strain; α and A are fitting parameters. Reported "satisfactory both when performing torsion tests on aluminum and during extrusion". Torsion assumes steady state, while extrusion strain rates vary strongly. ⚠ **The printed form has no 1/n exponent** (checked on the rendered page). It is the n = 1 special case of H2, or a misprint. [SH] prints the 1/n exponent (H2), and no alloy in [SH Table 4.1] has n ≈ 1 except 7004 (1.28) and 5182 (1.35), so the [TOT] form is most likely a misprint (inference, after the [SH] full-text pass). Use H2 with Table 4.1 constants. **No constants given in [TOT]** | [TOT Ch.8 eq. 11 p.434] |
| H2b | **Norton–Hoff:** σ̄ = K·ε̄ⁿ·ε̄̇ᵐ·exp(β/T), β = Q/R | "Extensive use" in extrusion simulation. n = 0 removes strain dependence. FEM needs small n and m for numerical reasons, but very low rate sensitivity makes runs long [p.470]. **No constants given** | [TOT Ch.8 eq. 10 p.434, p.470] |
| H2c | Static RX after hot passes (steel-type set): X = 1 − exp[−C(t/t₀.₅)ᵏ]; t₀.₅ = a·ε^(−b)·d₀^c·Z^(−d)·exp(Q_rex/RT); d_rex = e·d₀^f·ε^(−g) | **No constants given.** [TOT] warns that for Al these equations work only "in limited cases". Sellars found they predict unrealistically **large** grain sizes for Al. Al models need particle precipitation/dissolution and explicit nucleation sites (PSN, cube bands, grain boundaries) | [TOT Ch.7 eq. 1–4 p.359–360] |
| H3 | Mean extrusion strain rate (Feltham): **ε̇ = 6·D_B²·V_R·ln R / (D_B³ − D_E³)** | Verified on the page image: [SH] prints it **without** a tan θ factor (corrected after full-text pass; the earlier row gave the general-knowledge form with tan θ, which reduces to this for θ = 45°). D_B, D_E billet and extrudate diameters, V_R ram speed, R = D_B²/D_E² | [SH §2.2 p.28] |
| H4 | Modified Feltham from the minimised upper bound (Tutcher): ε̇ = 6·V_R·D_B²·(0.171 + 1.86 ln R)·tan(38.7 + 6.9 ln R) / (D_B³ − D_E³), angle in degrees | ⚠ [SH] prints D_B³ in the numerator and (D_B² − D_E²) in the denominator, **on both p.37 and p.142**. That is dimensionally inconsistent (ε̇ would not be in s⁻¹). The form above is the dimensionally consistent reading, matching the Feltham base (H3) (inference). Fig. 4.10 shows it tracks a time-averaged upper-bound solution for ln R ≈ 2–5 [p.143]. Used by Sheppard to compute Z | [SH §2.3.2 p.36–37; §4.5 p.142] |
| H5 | FEM mean ε̇ vs ln R is **parabolic**, not linear as in Feltham; agreement worsens at high R (no spin correction) | | [SH §2.3.4 p.44, Fig. 2.8] |
| H6 | Breakthrough (peak) pressure increment **Δp = 6.62 + 0.921·ln(Z/A)/(αn)** (N mm⁻²) | **Verified (G14 closed).** The OCR's "an" is the denominator αn. Fig. 4.11 plots 5456, 2024, 2014 and Al-1 to 4 % Cu (the text says 2xxx, 5xxx, 6xxx and 7xxx data [p.144]), correlation 0.988, over (1/αn)·ln(Z/A) ≈ 0–150 and Δp ≈ 0–150 N mm⁻² [Fig. 4.11 p.145]; "valid over a wide range of Al-alloys" [p.144] | [SH §2.5.4 eq. 2.27 p.57; eq. 4.5 p.144] |
| H9 | Subgrain size vs Z: **d⁻ᵐ = x + y·ln Z** | "Clearly established for most commercial alloys", usually with Z corrected for the temperature rise (Z_c) [SH eq. 4.10 p.156]. Only one fit is given: **AA2014**, printed "d⁻¹ = 0.15 + ln Z_i − 3.5". ⚠ That is a misprint; the reading consistent with Fig. 4.21(a) (d⁻¹ ≈ 0.25–1.2 over ln Z ≈ 25–33) is **d⁻¹ = 0.15·ln Z_i − 3.5** (inference; units read as µm⁻¹). Fitted over ln Z_c = 26.8–34.6, Q from the 2014 constants. Subgrain size and the recrystallised grain size after solution treatment are linearly related (2014), i.e. nucleation by subgrain coalescence [Fig. 4.21(b) p.159]. **No 3xxx subgrain constants in [SH]** | [SH §4.8 p.156–159] |
| H10 | Static RX after hot deformation (Raghunathan et al.): **5056: t₀.₅ = 2.31×10⁻¹⁰·d₀^1.58·ε̄^−1.9·Z^−0.35·exp(212000/RT_ann); 5083: t₀.₅ = 4.5×10⁻¹⁰·d₀^2.45·ε̄^−1.97·Z^−0.58·exp(183000/RT_ann)** | Verified on the page image. Units of t, d₀ not stated. The text says Z = exp(ΔH/GT_def) (no ε̇; probably a misprint) and that Z should be non-dimensionalised by A. Small d₀, high strain, high Z and high T_ann all shorten t₀.₅. Sellars' Al-1Mg data instead give d₀⁴ and ε̇^5.4, which Sheppard calls "contrary" [p.117]. Sheppard regards these forms as empirical, not state-variable laws [p.117] | [SH §3.6 p.116–117] |
| H11 | Avrami: X_v = 1 − exp(−A·tⁿ) and the extrusion forms ln ln[1/(1−X_v)] = −Ω₁ + n·ln t + Ω₂ε + Ω₃·ln(λ²R) + Ω₄·ln(λ²Z/A) − n·ΔH/GT (F temper) and a solution-soak form with a (T_s − T_def) term | n ranges from 0.5 (grain-corner site saturation) to 2.5 (random nucleation) (Christian) [p.116]. λ = peripheral shape factor. Fitted examples: 5456 (F temper) and 2024 (solution-soaked) [§4.9.2 p.166]; the printed coefficients are partly garbled in the OCR, so they are not reproduced here | [SH eq. 3.8–3.12 p.116–118; p.166] |
| H7 | Diffusion: D = D₀·exp(−Q/RT); x ≈ √(Dt) | | [SH §2.6.2 eq. 2.39 p.65; POL §3.1.4 p.105] |
| H8 | Homogenisation relaxation: c(x,t) = c₀ + c_m·cos(πx/l)·exp(−t/τ), τ = l²/(π²D). Halving l cuts time by 4; l/4 cuts it by 16 | | [SH §2.6.2 eq. 2.40–2.42 p.65–66] |

### 3.3 Per-alloy constitutive constants (G1 filled from [SH Table 4.1], 2026-10-12)

**Table 3-1 — Sellars–Tegart / Sheppard–Wright constants for H2** [SH §4.2.3 Table 4.1 p.132; digits checked on the page image; same values in `cloudpart4/txt/w.txt` l. 6757–6793]. G = 8.314 J mol⁻¹ K⁻¹ for all rows. The αn column is **derived** here (it enters H6 and the pressure law, §8.2).

| Alloy | α (MPa⁻¹) | n | ΔH = Q (kJ/mol) | ln A (A in s⁻¹) | αn (derived) | Remarks (as printed) |
|---|---|---|---|---|---|---|
| 1050 | 0.037 | 3.84 | 156.888 | 26.69 | 0.142 | |
| 1100 | 0.045 | 5.66 | 158.300 | 24.67 | 0.255 | |
| 2011 | 0.037 | 3.712 | 142.000 | 19.2 | 0.137 | |
| 2014* | 0.0118 | 5.86 | 176.867 | 31.43 | 0.069 | "PH.-SS [32]" |
| 2014 | 0.0152 | 5.27 | 144.408 | 24.41 | 0.080 | |
| 2024 | 0.016 | 4.27 | 148.880 | 19.6 | 0.068 | |
| **3003** | 0.0316 | 4.45 | 164.800 | 26.9 | 0.141 | |
| **3004** | 0.0344 | 3.6 | 193.850 | 28.21 | 0.124 | |
| **3005** | 0.0323 | 4.96 | 183.100 | 29.87 | 0.160 | |
| **3105** | 0.0248 | 4.83 | 179.300 | 29.98 | 0.120 | |
| 4047 | 0.04 | 2.65 | 129.300 | 20.47 | 0.106 | |
| 5005 | 0.029 | 5.8 | 183.576 | 26.65 | 0.168 | |
| 5052 | 0.016 | 5.24 | 155.167 | 24.47 | 0.084 | |
| 5054 | 0.015 | 5.43 | 173.600 | 26.61 | 0.081 | |
| 5056 | 0.015 | 4.82 | 166.900 | 23.05 | 0.072 | |
| 5083 | 0.015 | 4.99 | 171.400 | 23.11 | 0.075 | |
| 5182 | 0.062 | 1.35 | 174.200 | 22.48 | 0.084 | |
| 5456 | 0.0191 | 3.2 | 161.177 | 23.5 | 0.061 | |
| 6061 | 0.045 | 3.55 | 145.000 | 19.3 | 0.160 | |
| 6082 | 0.045 | 2.976 | 153.000 | 19.29 | 0.134 | |
| 6063 | 0.04 | 5.385 | 141.550 | 22.5 | 0.215 | |
| 6105 | 0.045 | 3.502 | 145.000 | 20.51 | 0.158 | |
| 7004 | 0.035 | 1.28 | 153.000 | 20.12 | 0.045 | |
| 7050 | 0.0269 | 2.86 | 151.500 | 22.85 | 0.077 | |
| 7075 H1 | 0.0141 | 5.41 | 129.400 | 20.75 | 0.076 | 24 h soak |
| 7075 H2 | 0.01 | 6.14 | 158.432 | 26.32 | 0.061 | slow heat, fast cool [23] |
| 7075 H3 | 0.012 | 7.8 | 155.336 | 27.54 | 0.094 | fast heat, slow cool |
| 7075 H4 | 0.01 | 8.5 | 156.325 | 27.14 | 0.085 | fast heat, fast cool |
| 7075 H5 | 0.011 | 6.32 | 156.837 | 26.38 | 0.070 | slow heat, slow cool |
| 7150 H1 | 0.01 | 5.7 | 161.402 | 29.8 | 0.057 | fast heat, fast cool |
| 7150 H2 | 0.013 | 6.1 | 158.806 | 29.2 | 0.079 | fast heat, slow cool |
| 7150 H3 | 0.01 | 5.5 | 159.832 | 30.7 | 0.055 | slow heat, fast cool |

The 7075/7150 H1–H5 rows are homogenisation variants (heating and cooling rate of the homogenisation cycle; "F.Ht/Sl.Ht" = fast/slow heat). The text calls the table "Table 4.2" once [p.131]; the printed caption is Table 4.1.

**Additional equation [SH p.131].** 7075, torsion data corrected for the test's temperature rise: Z = ε̇·exp(155100/GT) = 1.7×10¹²·[sinh(ασ)]^6.4. The α of this fit is not printed with it.

**Validity and how to use the constants.**
- Test basis: hot torsion (most data) and compression; after correction for the test's temperature rise the two agree (7xxx, Fig. 4.1, ln Z ≈ 20–40) [SH §4.2.3 p.130–131]. Sheppard concludes the constants "are adequate to describe the flow stress during extrusion" [p.136].
- **No per-alloy T or ε̇ ranges are printed.** The plotted ranges are 500–800 K (227–527 °C) in Fig. 4.2, 450–850 K at ε̇ = 50 s⁻¹ in Fig. 4.4 (6xxx), and ln Z ≈ 20–40 in Fig. 4.1 [p.130–134]. Treat ≈ 230–530 °C and the extrusion strain-rate range as the validity envelope (inference). They are **steady-state hot-working** constants: do not use them for cold work (impact extrusion at room temperature: use Table 5-1).
- **Material state.** Homogenised DC material. "Care must, however, be exercised if the values are to be utilized as a precision tool because … heating and cooling rates can produce variations in the flow stress. We may presume that there may be considerable variations if the homogenising practices are vastly different (i.e. when considering homogenized versus cast material)" [SH p.136]. Fig. 4.3 shows the 7150 flow stress shifting with the homogenisation heating and cooling rates [p.133].
- **Use each row as a set.** α, n, Q and A are interdependent; fixing Q at the self-diffusion value (153 kJ/mol) changes A and n without changing σ̄ [SH p.135]. The 1050 and 1100 rows cross over (1050 is softer at 500 °C and harder at 380 °C, §3.3a), which illustrates the regression scatter Sheppard mentions for weak alloys [p.132] (inference).
- **Meaning of the constants [SH p.133–136].** α is a reciprocal stress and marks the change from power-law (ασ < 0.8) to exponential (ασ > 1.2) stress dependence; harder alloys have lower α (≈ 0.011 for most hard 7xxx vs 0.04 for 6063). n is the "inverse of the temperature compensated strain rate sensitivity"; a lower α automatically gives a higher n, so n alone is not a measure of Z sensitivity. A is a "structure factor" with no established physical meaning.
- **Q values vs self-diffusion.** Sheppard gives 153 kJ/mol for lattice self-diffusion in pure Al [p.135]. ⚠ Disagreement: the earlier "general knowledge" anchor in this file was ≈ 142 kJ/mol (corrected after full-text pass: the cited value is [SH]'s 153 kJ/mol; the 142 figure stays general knowledge only). The 3xxx rows sit above both (165–194 kJ/mol).
- ⚠ **Q for AA3004/AA3104 differs between sources.** [SH] gives Q = 193.85 kJ/mol for 3004 (flow stress). The cube/PSN boundary of AA3104 in [TOT Ch.7 Fig. 4 p.357] implies Q ≈ 156–160 kJ/mol (derived from the plotted line slope, §4.3; Q is not stated in [TOT]). The two are fitted to different phenomena and data sets. Use Z* = 3×10¹⁴ s⁻¹ only with Q ≈ 156–160 kJ/mol; use [SH] constants only as a full set. Do not mix them.
- **Cross-check of Table 4.1 against Table 4.2 (derived).** The αn values printed in Table 4.2 (§8.2) agree with α·n from Table 4.1 for 5083 (0.075), 5456 (0.059 vs 0.061), 2014 4 % Cu (0.080) and 7075/7150 (H3/H2 rows). They do **not** agree for 1100 (0.192 vs 0.255), 5052 (0.072 vs 0.084) and 5056 (0.035 vs 0.072). So the pressure-equation constants for these three alloys were fitted with a different constitutive set.
- Retrieval leads for alloys not in the table (3102, 3207, Al-1Mn): ch. 13 §1 web leads (e.g. W13-19, Shi et al. 1997: CP-Al, Al-1Mn, Al-1Mg in plane-strain compression) (G1).

#### 3.3a Derived hot flow stress for the in-line hot mill (slug route)

**(derived)** σ̄ from H2 with Table 3-1, at the rotary-cast route's hot-mill window (≈ 500 °C caster exit → ≈ 380 °C mill exit). The strain-rate range 1–50 s⁻¹ is the range used in §4.3; the user's actual pass strain rates are not in the KB. Values in MPa, written ε̇ = 1 / 10 / 50 s⁻¹. Shear yield stress for the Sims load model (§4.2): k = σ̄/√3.

| Alloy | 500 °C | 440 °C | 380 °C | ln Z range (Q of that row) | ασ̄ range |
|---|---|---|---|---|---|
| 1050 | 14 / 24 / 33 | 23 / 35 / 46 | 36 / 51 / 62 | 24.4–32.8 | 0.53–2.30 |
| 1100 | 20 / 26 / 32 | 26 / 34 / 39 | 34 / 43 / 49 | 24.6–33.1 | 0.88–2.19 |
| 3003 | 22 / 33 / 43 | 33 / 46 / 57 | 48 / 63 / 75 | 25.6–34.3 | 0.70–2.36 |
| 3005 | 22 / 32 / 40 | 32 / 44 / 53 | 47 / 61 / 70 | 28.5–37.6 | 0.70–2.27 |
| 3105 | 25 / 37 / 47 | 37 / 53 / 65 | 56 / 74 / 87 | 27.9–36.9 | 0.61–2.15 |
| 3004 | 38 / 55 / 68 | 57 / 75 / 88 | 81 / 99 / 112 | 30.2–39.6 | 1.31–3.86 |
| 5005 | 39 / 51 / 60 | 51 / 64 / 73 | 67 / 81 / 90 | 28.6–37.7 | 1.13–2.61 |
| 6063 | 21 / 29 / 35 | 27 / 36 / 43 | 35 / 45 / 52 | 22.0–30.0 | 0.82–2.10 |

- ασ̄ spans 0.5 to 3.9, i.e. both the power-law and the exponential regime [SH p.133]. A pure power law (Norton–Hoff, H2b) fitted at one end will be wrong at the other; use the sinh form.
- Over 500 → 380 °C at fixed ε̇, σ̄ rises by a factor of ≈ 1.5–2.6. Most of the hot-mill load comes from the cold end of the window.
- **Trial alloy T11 (Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26) — bracket (inference).** No row matches. 1100 (dilute, Fe+Si) is a lower bound. 3005 and 3105, the Al-Mn-Mg members of the 3xxx group [SH p.72], are the closest Mn+Mg rows and serve as an upper bound. 6063 (Mg+Si) sits close to 1100. Expected range: **σ̄ ≈ 20–25 MPa at 500 °C/1 s⁻¹ to ≈ 49–87 MPa at 380 °C/50 s⁻¹** for homogenised material. Rotary-cast, unhomogenised strip with Mn, Mg and Si retained in solution should sit in the **upper half** of the bracket ([SH p.136, 207]: cast and unhomogenised material is stronger). Calibrate on measured hot-mill roll forces.
- **Consistency check with the 3102 extrusion point (§3.4).** At 500 °C, 1100 gives 16 MPa (0.27 s⁻¹) and 25 MPa (5.7 s⁻¹); 3003 gives 17 and 30 MPa. The back-calculated σ̄ ≈ 27–28 MPa for AA3102 (0.24 Mn) falls between 1100 and 3003 **only at the H4 strain rate (≈ 5.7 s⁻¹)**. This supports the modified-Feltham rate (H4) over plain Feltham (H3) for that case, despite R = 817 lying outside H4's fitting range (derived).

### 3.4 Calibration point extracted here: AA3102 multi-port tube (derived from [WIL] + [SH])

Inputs [WIL Table 3 p.19, Table 5 p.38]:
- container 106 mm; billet Ø102 × 203 mm; R = 817;
- billet 495–503 °C; tooling 450 °C;
- ram 0.7 mm/s; exit ~34 m/min; water quench;
- peak specific pressure 445.0 MPa and 460.2 MPa (two 3102 billets); 650.7 and 653.3 MPa (Al-0.19Sc-0.05Zr).

**(derived)** Using [SH §2.3.2 p.36, unnumbered; = eq. 4.4 p.144] p = σ̄(0.171 + 1.86 ln R + 4mL_B/(D_B√3)) with m = 0.88 [SH §2.4] (citation corrected after full-text pass: this is the p.36 equation, not eq. 2.26; the equation is now verified on the page image):
- ln R = 6.706; the bracket is 12.64 + 3.89 = 16.54 (D_B taken as the 106 mm container bore).
- σ̄(3102, ~500 °C) ≈ **27–28 MPa**; σ̄(AlScZr) ≈ **39.4 MPa** (+44 %, as measured).
- Without the friction term, σ̄ would be 35–36 MPa.
- Caveats:
  - porthole/bridge-die pressure includes die-land and port losses, so this σ̄ is an upper estimate. [SH] treats bridge dies as two extrusions in series with shape factors (§8.2, E13);
  - the 0.171 + 1.86 ln R regression is stated to be valid for rod extrusion up to R = 100, and its constant "can assume a negative value for higher ratios" [SH p.144]. R = 817 is far outside that range;
  - the peak (breakthrough) increment Δp (H6) is not subtracted. For 1100–3003 constants at 500 °C and ε̇ ≈ 1–10 s⁻¹ it is only ≈ 6–15 MPa (derived), i.e. < 4 % of 445 MPa. At lower Z the H6 fit leaves its data range ((1/αn)·ln(Z/A) < 0) and should not be used.
- Cross-check with Table 3-1: see §3.3a (the σ̄ is consistent with 1100–3003 constants at the H4 strain rate).
- Strain-rate estimates **(derived)** differ by 20× between models, so report Z only with the model named:
  - H4: ε̇ ≈ 5.7 s⁻¹, but its die angle extrapolates to 85° at R = 817, outside its range;
  - H3 with θ = 45°: ε̇ ≈ 0.27 s⁻¹.

### 3.5 Diffusivities for homogenisation / preheat kinetics

| Element in Al | D₀ (m²/s) | Q (kJ/mol) | D at 475 °C (m²/s) [SH] | D at 500 °C [POL] (converted to m²/s) |
|---|---|---|---|---|
| Cu | 0.29×10⁻⁴ | 125.6 | 4.9×10⁻¹⁴ | 5×10⁻¹⁴ |
| Zn | 0.11×10⁻⁴ | 83.7 | 1.6×10⁻¹¹ | — |
| Mg | 0.11×10⁻³ | 117.2 | 7.2×10⁻¹³ | 1×10⁻¹³ |
| Si | 0.90×10⁻⁴ | 125.6 | 1.5×10⁻¹³ | 1×10⁻¹³ |
| **Mn** | 0.22×10⁻⁴ | 121.4 | 7.3×10⁻¹⁴ | **5×10⁻¹⁷** |
| Cr | 3.00×10⁻¹¹ (as printed) | 62.8 | 1.2×10⁻¹⁵ | — |
| Zr | 7.28×10⁻² | 240.8 | 1.1×10⁻¹⁸ | — |
| Fe | 0.41×10⁻¹⁴ (as printed) | 58.6 | 3.3×10⁻¹⁹ | — |

Sources: [SH Table 2.3 p.65] (the D values recompute correctly from D₀ and Q — **derived** check) and [POL §3.1.4 p.105] (5×10⁻¹³ cm²/s etc.).

⚠ **Mn discrepancy of ~10³×.** Sheppard's Mn entry (Q = 121.4 kJ/mol) gives fast, Mg-like diffusion. Polmear's 500 °C value is ~10³ slower, which matches Mn being a *slow* diffuser (general knowledge). Sheppard's Cr and Fe rows (low D₀ and low Q) also look non-physical. **For 3xxx dispersoid and homogenisation models, use the Polmear-scale Mn diffusivity. Do not use [SH Table 2.3] for Mn, Cr or Fe.**
- **Full-text pass (2026-10-12): Sheppard contradicts his own Table 2.3.** In §3.3.2 he groups Cr, Mn, Ti, V and Zr as "moderate solubility, **very low diffusion rate**", Cu, Mg, Si and Zn as "appreciable solubility, high diffusion rate", and Fe as "extremely low solubility, very low diffusion rate" [SH p.102]. Mg coring in an Al-5.5Mg-0.19Cr casting disappears in 20 h at 430 °C while the Cr segregation "remains virtually untouched"; Ti coring would need about 3 weeks [p.102–103]. This supports the flag above (G9 stays open for primary data).
- **Diffusion distance scales with cell size squared** [SH §3.3.1 p.99]: doubling the distance quadruples the time. Example: Cu across a 0.05 mm dendrite cell at 500 °C homogenises in about 2 h. Rapid solidification gives maximum microsegregation across the dendrite walls but small cells; in commercial ingots large cells are more segregated and slower to homogenise, and an Al-2.5Mg casting with the finer structure approached uniform Mg faster at 425 °C [p.93–94, 99].

#### 3.5a Phase changes during homogenisation (3xxx, 6xxx) [SH]

- **3003:** as cast, (Mn,Fe)Al₆ dominates; heating transforms it to (Fe,Mn)SiAl₁₂ by a delayed peritectic reaction. Mn also supersaturates the cored dendrites and precipitates as a dispersoid. Grains formed by RX after extrusion are more elongated than in 1100 because of the dispersoid [SH §3.1 p.72].
- **3004 (Mg-bearing):** Mg's affinity for Si "tends to shift the phase proportioning toward (Mn,Fe)Al₆" [p.72]. The α-transformation Al₆(Fe,Mn) → α-Al₁₂(Fe,Mn)₃Si starts at the particle/matrix interface and is controlled by Mn diffusion. **High Si accelerates it; high Mg suppresses it** (Si tied up as Mg₂Si; the C-curve nose moves to longer times). Excess Si is the more effective way to get a high α fraction. α is markedly harder than Al₆Mn, Al₆(Fe,Mn) and α-AlMnSi [SH §3.3.2 p.109–110, Fig. 3.12].
- **3004 can-stock practice:** as cast ~5 % second phase, mainly Al₆(Fe,Mn) and α′-Al(Fe,Mn)Si, Mn-cored dendrites with the dendrite peripheries at about half the nominal Mn [p.217]. Critical soak **above 605–610 °C** (Fe phases for scouring in can making and for earing), then cooling at **5–30 °C/h** [p.217–218]. During the soak, fine Al₁₂(Fe,Mn)₃Si dispersoid forms in the dendrite cores, the constituents break up and spheroidise, and PFZs form at grain boundaries and around constituents [p.218–220]. The Mn-rich phase dissolves above about 500 °C, while the Fe-rich phase stays stable and precipitates at 605 °C [p.218].
- **3003/3004 for extrusion:** the very high soak is not needed; "a soak at 575 °C for about 5 h followed by a slow cool (furnace or air)" would suffice to remove the Mn coring [SH §5.4 p.219].
- **6xxx:** β-(Al,Fe,Si) → α-(Al,Fe,Si) transformation releases Si to the matrix, makes the Fe phase less brittle and adds Mg₂Si potential; it is complete after **6 h at 565 °C**. Small Mn additions move the α field to lower Fe:Si and accelerate β → α [SH §6.1 p.256]. Mg₂Si dissolves rapidly above 465 °C (≈ 2 h for complete dissolution), so the soak is set by the Fe phase, not by Mg₂Si [p.257].
- **Al₃Zr:** must be heated slowly between 380 and 420 °C to form the fine metastable superlattice phase; precipitated at high temperature as the tetragonal phase it "has little effect on the alloy structure" [SH p.110].
- **Coarsening:** Al₆Mn coarsens as d ∝ t^(1/3) (lattice-diffusion control), also seen in 3004. Phases with Si, Cu, Mg or Ni coarsen fast; those with Mn, Fe, Cr or Zr only at relatively high temperatures [SH p.108–109].

### 3.6 Design levers (hot deformation)

- To raise recrystallisation resistance in hot-worked product, use small, closely spaced dispersoids, ideally **coherent**:
  - Al₃Zr is more effective than incoherent Al₁₂Mg₂Cr / Al₂₀Mn₃Cu₂ [TOT Ch.3 p.125];
  - useful dispersoid size is < 0.4 µm [TOT Ch.3 p.125] (0.05–0.5 µm [POL p.43]);
  - Zr < 0.18 wt % gives near-spherical Al₃Zr [TOT Ch.3 p.125].
- Sc+Zr (Al-0.19Sc-0.05Zr) keeps the extruded tube **unrecrystallised** at 500 °C extrusion (3102 recrystallises fully during extrusion). It resists recrystallisation up to 575 °C and partially recrystallises at 600 °C / 2 min braze. Cost: **+44 % extrusion pressure** [WIL §5.1–5.2 p.38–41].
- Higher flow stress (more solute) raises press load and deformation heating (ΔT ∝ σ̄·ln R/(ρc_p), §8.2). The extrudability window therefore narrows from both the load side and the temperature side (inference from [SH §2.5.2; WIL]).
- **Mn is the RX inhibitor in dilute 5xxx [SH §4.9.1 p.165].** After extrusion, 5052 (no Mn) "recrystallized completely between die exit and quench for all extrusion conditions", while the Mn-bearing 5456 and 5083 kept an unrecrystallised core inside a recrystallised shell. Sheppard attributes this to drag by the Mn precipitates. Al₆Mn dispersoids pin advancing boundaries, so even recrystallised grains stay elongated along the extrusion direction [p.164–165, Fig. 4.26]. In 5xxx the RX fraction *falls* above ≈ 450 °C extrusion temperature because the driving force (dislocation density) falls while the Mn drag stays roughly constant [p.166].
- **Fine Fe-bearing precipitates restrain dynamic recovery more than Mn-bearing ones [SH §5.2 p.207].** In Al-Fe, Al-Fe-Si and Al-Mn-Mg studies, homogenisation produced more particles < 0.2 µm in the Fe alloys; Mn particles are larger and fewer and very hard to redissolve. Dynamic restoration is high in low-solute alloys (99.99 % Al, Al-Si, Al-Fe, Al-Fe-Si) and low in alloys with much solute in the matrix (Al-Mg, Al-Mn, Al-Mn-Mg) [p.207–208, Fig. 5.1].
- **Relative extrudability [SH Table 5.4 p.239]**, based on flow stress, 6063 = 100, higher = harder to extrude: 1000 77 · 1100 86 · 6063 100 · 3005 106 · 3003 112 · 3105 126 · 4047 128 · 6105 134 · 6061 151 · 5005 154 · 7004 157 · 2011 171 · 3004 180 · 6082 197 · 2014 202 · 5052 229 · 5056 232 · 2024 247 · 5054 265 · 7150 269 · 7050 280 · 5083 281 · 5182 293 · 5456 300 · 7075 316 (checked on the page image). It "in general" agrees with the surface-limit ranking of Fig. 4.18 [p.238].
- **Relevance to the slug route (inference).** Table 5.4 is a hot-extrusion index, but it orders the candidate base alloys by flow stress: going from 1xxx (77–86) to 3003/3005 (106–112), 3105 (126), 5005 (154) and 3004 (180) raises the hot flow stress by up to ~2×. The cold Hollomon K values give a similar step: 3003/1100 = 188/146 = 1.29 (Table 5-1) vs 112/86 = 1.30 in Table 5.4 (derived). As a first screen, the hot index also ranks impact-extrusion press force for annealed slugs; confirm with room-temperature flow curves.

### 3.7 Pitfalls

- Mixing ε_t and ε̄, or Feltham and FEM strain rates, when transferring Z-based laws between rolling and extrusion (§1, H5).
- Constant-stress FEM with m-friction cannot tell m = 0.2 from m = 1.0 at R = 20, because hydrostatic stress dominates. Use σ_interface = m·σ₀ in a boundary layer instead [SH §2.3.4 eq. 2.18–2.19 p.41].

---

## 4. Hot rolling: mechanics and microstructure

### 4.1 Mechanisms

- Roll bite is by friction. Rougher rolls allow larger reductions per pass; smooth (bright) rolls may need less coolant, which shifts the thermal schedule [RA §4 p.4-2].
- Rolling generates heat from friction and from internal deformation. Coolant both lubricates and removes heat, controlling roll camber and temper [RA §5 p.5-1/5-2].
- Spread is small in normal lengthwise rolling (friction restrains it) [RA p.5-3]. Tandem stands must accelerate in proportion to the thickness ratio (volume constancy: 30 → 5 mm runs 6× faster) [RA p.5-3/5-4].
- Texture, grain shape and surface are temperature-dependent:
  - lower hot-rolling temperature → brighter surface, elongated grains;
  - higher temperature → recrystallisation [RA §4 p.4-6/4-7].
  - Through-thickness strain in plate is uneven (surface > centre). Larger pass reductions or pre-forging improve uniformity [POL §3.1.5 p.107].
- Reheat cycles for alloys with recrystallisation-inhibiting elements must avoid **coarse grains in critically strained regions** [POL p.107].

### 4.2 Equations (for pass-schedule models)

- Direct-force forming (upsetting, rolling): F = A·k_w, with forming efficiency η_F = k_f / k_w [MFH §2.2.3 p.29].
- Specific work: w_id = ∫k_f dφ ≈ k_fm·φ_g; W = V·w_id/η_F [MFH §2.2.3 p.29–30].

**Roll-gap friction and bite [RR, read in full 2026-10-12].**
- Inside the gap there is backward and forward slip, with static friction at the neutral point between them. If the speed is too high, flow goes in one direction only, static friction is lost, and the roll slips and then chatters (alternating bite and no-bite) [RR §3.6 p.51].
- Hot rolling with little strip tension needs "high" friction. The permissible bite angle falls as rolling speed rises. Slip is typical with freshly ground rolls after a roll change. Mills therefore roll special schedules for the first slabs to build up a fire-crack pattern. If the schedule asks for too large a bite at the desired speed, reduce the speed or roughen the roll surface (open fire-crack pattern, "ragging") [RR §4.5.3 p.74; §4.8.3 p.92].
- The bite-angle vs speed curve was measured on hot strip mills (steel) with freshly ground rolls. It is an image (Ill. 47), so no values can be extracted [RR p.92].
- Mill friction coefficients are back-calculated from measured vs calculated separating force [RR §3.6 p.51]. They are **much higher than laboratory values**, differ between roll grades, change from slab to slab and **rise during a campaign** (Ill. 48) [RR §4.8.3 p.93]. Laboratory tests (ring compression, CRM Liège) found no significant friction difference between roll grades [RR p.51–52]. So the surface (fire-cracks, oxide) matters more than the roll material [RR p.93].
- **Consequence for pass-schedule models (inference):** a single μ fitted at roll change will drift. Calibrate μ online from measured roll force, as mills do [RR p.51], rather than taking a handbook value.

**Roll elastic data and mill design limits [RR].** These are inputs or checks for any roll-force or roll-flattening model:

| Quantity | Value | Ref |
|---|---|---|
| E, ferritic/bainitic/martensitic steel rolls | 210 000 N/mm² ± 3 % (insensitive to alloying and heat treatment) | [RR §3.2.1 p.18] |
| E, austenitic steel | 180 000 N/mm² ± 3 % | [RR p.18] |
| E, nodular (ductile) iron | 175 000 N/mm² ± 5 % | [RR p.18] |
| E, grey (lamellar) iron | no single value: it "behaves totally differently" (non-linear elasticity, see RR §3.2.3) | [RR p.18] |
| Poisson ratio | 0.3 elastic; 0.5 fully plastic | [RR p.18; §3.7 p.53] |
| Compound (double-poured) rolls | Effective E combines shell and core and changes as the shell is ground away | [RR §3.7 p.53] |
| Safe nominal bending stress (fillet notch factor 1.8 ≤ α_K ≤ 2.2) | grey iron < 60; nodular iron < 90; cast steel < 120; forged steel < 150 N/mm² | [RR §4.10.1 p.100] |
| Static torque strength | 90 % of tensile strength (torque fatigue failures are rare) | [RR §4.5.2 p.74; §4.10.1.1 p.100] |
| Linear load, hot strip vs work roll | traditionally < 1500 t/m of strip width (≈ 14.7 kN/mm, **derived**). Above this, use only work rolls with nodular-iron cores | [RR §4.10.1.2 p.100] |
| Hertzian pressure, work roll vs back-up roll | safe limit 2100 N/mm². Peaks occur near the barrel edges (back-up roll bending), so a back-up roll chamfer is required | [RR §4.10.2.1 p.101] |
| Roll accuracy | roll TIR must be one grade better than the product tolerance; ≤ 0.003 mm is acceptable for tin-plate rolls | [RR §4.11 p.102–103] |

These limits come from steel hot strip and plate mills. For Al they are upper-bound sanity checks, not design values (inference).

**Rolling-force models [TOT Ch.7 §4, read in full 2026-10-12]** (gap G8 closed). [RR] has no force model; [TOT] gives the slab-method set below. It says the simple slab method "is still exploited by industry, e.g. for rolling load calculation". The equations are given "only to illustrate the principle", and the original references (Larke, Roberts, Pietrzyk & Lenard) should be used for real calculations [p.364–365]. Notation: R roll radius, h₁ entry and h₂ exit thickness, Δh = h₁ − h₂, k = shear yield stress = σ̄/√3 (von Mises), φ roll angle.
- **Slab equilibrium (von Kármán–Siebel):** d(σh)/dφ = 2pR(sin φ ± μ cos φ). The sign changes at the neutral plane: backward slip zone from entry, forward slip zone to exit [eq. 5–6 p.364–365]. With modern computers the differential equation can be solved numerically without the classical simplifications [p.365].
- **Hot rolling (Orowan / Sims; sticking friction).** Assume sticking, μp = k; small angles; p − σ = (π/4)·2k [eq. 7–9 p.366]. Load per unit width P = R∫p dφ [eq. 10]. Sims' closed form: **P/w = 2k·√(RΔh)·Q**, where √(RΔh) ≈ the contact length and Q(R/h₂, r) comes from Larke's chart [eq. 11–12, Fig. 11 p.367]. Q includes the friction load. Hot-rolling loads can reach **up to ~4×** those of frictionless flat-platen compression (Q = 1) [p.367]. Roll flattening "may be disregarded" in simplified hot-load calculations, and plane strain is acceptable for thin, wide strip (spread matters for thick slabs) [p.366].
- **Sims Q values (read from Fig. 11, Larke; ±0.05)** at r = 30 % / 50 % reduction:

  | R/h₂ | 2 | 5 | 10 | 20 | 30 | 50 | 100 | 150 | 200 | 300 |
  |---|---|---|---|---|---|---|---|---|---|---|
  | Q at 30 % | 0.93 | 1.05 | 1.18 | 1.37 | 1.51 | 1.73 | 2.12 | 2.44 | 2.72 | 3.2 |
  | Q at 50 % | 0.86 | 1.04 | 1.25 | 1.47 | 1.69 | 1.97 | 2.54 | 2.97 | 3.35 | 3.96 |

  The chart covers 5–60 % reduction and R/h₂ = 2–300. For R/h₂ ≤ 5, Q stays near 0.8–1.05 at all reductions [Fig. 11].
- **Cold rolling (Bland–Ford-type solution).** Small, constant μ and small angles give d(σh)/dφ = 2pR′(φ ± μ) [eq. 13 p.368], with the yield condition p − σ = 2k = (2/√3)σ̄ [eq. 14 p.369]. Integration gives p = C·2k·(h/R′)·e^(±μH), where H = 2√(R′/h₂)·arctan(√(R′/h₂)·φ) [eq. 15]. With back/front tensions t₁, t₂: p⁺ = (2kh/h₂)(1 − t₂/2k₂)e^(μH) on the exit side and p⁻ = (2kh/h₁)(1 − t₁/2k₁)e^(μ(H₁−H)) on the entry side [eq. 16–17]. P = R′(∫₀^φn p⁺dφ + ∫φn^φ₁ p⁻dφ) [eq. 18 p.369]. Different published solutions give visibly different pressure distributions [Fig. 13 p.370].
- **Hitchcock roll flattening (now sourced):** R′ = R·[1 + 16(1 − ν²)P/(πE·b·Δh)], where P is the roll force, b the strip width, and E, ν the roll's elastic constants [eq. 19 p.370]. Take E and ν from [RR] above. It assumes an elliptical pressure distribution and a circular deformed roll. It holds only for "passes of sufficient strip thickness and reduction". It predicts a theoretical minimum gauge, but in practice passes well below it are rolled at lower measured loads. Löffler & Kramer: with **300 mm diameter rolls, exit thicknesses below 13 µm** can be processed [p.370].
- **Projected contact length:** √(RΔh) "represents approximately the contact length" [TOT Ch.7 p.367]. Bite condition μ ≥ tan α_bite **(general knowledge)**.
- Still **general knowledge** (not in [TOT] or [RR]): the Ekelund mean-pressure formula p̄ = (2/√3)·σ̄·[1 + (1.6·μ·√(RΔh) − 1.2Δh)/(h₀ + h₁)] and the Ekelund mean strain rate ε̄̇ ≈ 2·v_R·√(Δh/R)/(h₀ + h₁). [TOT] names "Eklund and Siebel" only as the origin of the temperature-corrected friction formulae below [p.365].

**Friction coefficients for Al [TOT Ch.7 p.365–368].**
- Hot rolling: friction is "usually high", with sticking possible. "Very little generally available information" exists for Al. Values cited are "about μ = 0.3 or 0.4 or even more" [p.365].
- Geleji (via Pietrzyk & Lenard), T in °C, v in m/s: μ = 1.05 − 0.0005T − 0.056v (steel rolls); 0.94 − 0.0005T − 0.056v (cast-iron rolls); 0.82 − 0.0005T − 0.056v (ground steel or cast-iron rolls). The form was originally developed for steel; Geleji added the speed term [p.365].
  - Example **(derived)**: ground rolls, 380–500 °C, 1 m/s → μ ≈ 0.51–0.57.
- Geleji's Al data: 99.5 % Al hot rolled with slight oil lubrication, μ = **0.47–0.60** depending on reduction and thickness. Duralumin with emulsion: μ = 0.3, 0.43 and 0.6 depending on thickness and reduction [p.365].
- Without lubricant, severe sticking occurs: local oxide breakdown, Al coating on the rolls, embedded fragments, even the slab wrapping round the roll. Fortified mineral-oil emulsions are used, kept clean by filtration and protected from bearing-oil contamination [p.365–366].
- Cold rolling: μ is "much lower"; the lowest values may be **< 20 % of hot-rolling values**. Friction must be balanced: low friction cuts load and welding and gives more homogeneous deformation; some friction is needed for stable rolling and to avoid skidding defects, e.g. **herringbone** [p.367–368].
- Mixed lubrication (hydrodynamic pockets plus boundary contact) is the target. It sets the surface appearance (Stribeck curve, Fig. 12) [p.368].
- These handbook μ values are consistent with [RR]'s point that mill friction is far above laboratory values. Calibrate μ from measured roll force (above).

**Relevance to the slug route (in-line hot mill, 22 mm → hot band at ≥ 50 %, ≈ 500 → 380 °C).**
- **(derived)** For 22 → 11 mm (50 %): R/h₂ = 20–50 corresponds to roll radii of 220–550 mm, so Q ≈ 1.5–2.0. Force per width is then P/w ≈ 2k·√(R·11 mm)·Q. The roll radius of the user's mill is not in the KB; insert it to get a number.
- The hot-flow k at 380–500 °C was the missing input (G1). **Updated after the [SH] full-text pass:** k = σ̄/√3 now follows from Table 3-1 (§3.3a). For the T11 bracket (1100 → 3105 constants) at 440 °C, 10 s⁻¹, k ≈ 19–30 MPa; at 380 °C, 10 s⁻¹, k ≈ 25–43 MPa (derived).
- **Illustrative load (derived; the roll radius R = 300 mm is an assumption, not the user's mill).** One 22 → 11 mm pass: √(RΔh) = 57 mm, R/h₂ ≈ 27, Q ≈ 1.6 (§4.2 table), so P/w ≈ 2k·57·1.6 ≈ 190·k N/mm. With k = 19–43 MPa this gives ≈ 3.5–8 kN/mm of strip width, below the ≈ 14.7 kN/mm work-roll experience limit of [RR p.100]. Replace R and ε̇ with the mill's values before use.
- Use Sims (sticking) for the hot mill and the Bland–Ford set with Hitchcock flattening for the 30–50 % cold passes. Calibrate μ, and hence Q, on measured roll forces [RR p.51].

### 4.3 Recrystallisation after hot rolling

- Static recrystallisation between or after passes is typical. Alloys with dispersoids retain dynamically recovered subgrains inside elongated grains [TOT Ch.3 p.130].
- Nucleation sites for subsequent recrystallisation [POL §2.1.6 p.42, Fig. 2.4]:
  1. transition bands (cube nuclei);
  2. coarse particles (PSN, > ~1 µm);
  3. old grain boundaries;
  4. shear bands.
  - The final texture is the result of the (1) vs (2) competition.
- Cube nucleation at transition bands is known after cold rolling and "seems likely" after warm/hot rolling as well [POL p.42]. This is the root of hot-band cube texture, which balances earing in can stock (§7).

**[TOT Ch.7 §2] hot-rolling metallurgy (read in full 2026-10-12).**
- Hot rolling is "a succession of deformation and annealing steps". RX and texture are interrelated and "influenced by ongoing precipitation" [p.356].
- It runs at the highest possible temperature to cut load and allow large reductions (> 50 % is achievable [p.354]). The upper limit is set by RX and precipitation control and by pick-up [p.355–356].
- Falling temperature during rolling and deformation-induced vacancies cause "further precipitation of secondary phases"; coarse primaries are crushed and redistributed [p.356].
- **Solute/particle control of hot-band RX** [p.356]:
  - In AA1050, Fe and Si as finely dispersed precipitates "efficiently obstruct recrystallization".
  - Mn and Cr act the same way "unless the elements are already bound in coarse particles".
  - In Al-Mg-Mn (can body, automotive), RX covers a broad range under industrial conditions, so the rolling parameters can steer it.
- **Self-annealing (G3, partly filled).** The RX structure is obtained either in a separate anneal or, in "more sophisticated technologies", by **self-annealing on the coil from the rolling heat** [p.356].
- **Cube vs inter-stand RX in can stock** [p.356–358]:
  - Can body needs a distinct hot-band cube texture to limit earing.
  - With little inter-stand RX, cube nuclei form at the expense of the rolling-texture components and grow during the following anneal or coil self-anneal.
  - Coarse particle size and large inter-particle spacing help RX during coiling. But they can also cause inter-stand RX, which gives **large cube bands that deform unfavourably** in later passes.
  - Inter-stand RX is suppressed by lowering the rolling temperature or raising the speed. That raises Z, and then PSN (random texture) limits the result.
- **AA3104 cube/PSN boundary (read from Fig. 4 p.357, Engler et al. 1996).** Plotted as ln ε̇ vs 1/T_D for deformation at 150–350 °C and 10⁻³–10 s⁻¹, followed by RX:
  - cube texture for Z below the line **Z* = 3×10¹⁴ s⁻¹**, PSN texture above it;
  - room-temperature cold rolling ("CR") lies in the PSN field;
  - the implied Q ≈ 156–160 kJ/mol (derived, §3.3);
  - valid only for AA3104 "with a given constitution before rolling". Fig. 5 shows that the boundary moves with the precipitation state [p.358].
- **AA5182 RX spectrum (read from Fig. 3 p.357, Hirsch et al. 1994; prior strain not stated; reading ±~50 % in time):**

  | T (°C) | 320 | 400 | 450 | 500 |
  |---|---|---|---|---|
  | RX start (0 %) | ~4–5 s | ~0.4 s | ~0.2 s | ~0.12 s |
  | RX finish (100 %) | ~800 s | ~3 s | ~1 s | ~0.5 s |

  No RX band is drawn below ~320 °C.
- **Heterogeneity.** On reversing mills the head-to-tail delay grows from pass to pass, so the slab may partly recrystallise in some passes. Roughing passes have steep through-thickness gradients of strain rate and temperature. Width heterogeneity grows at low speed without selective cooling [p.358].
- **Modelling status.** Inter-stand RX fractions are computed in industry and used for pass optimisation against earing (§7.2) [p.358]. Steel-type RX equations (H2c) are unreliable for Al [p.360].

**[TOT Ch.4 §6.3] static RX after a hot-rolling window close to the user's line** [p.241–244]:
- Blade's data, super-purity Al with impurity additions: **50 % hot rolling, entry 500 °C, exit 390 °C**, then a 30 s delay before quenching. Read from Fig. 28 p.244 (±3 %):
  - the base metal reached ≈ 76 % RX;
  - **Si raised it** (≈ 97 % at ≈ 0.09 % Si);
  - **Cu had no effect** up to 0.5 %;
  - **Fe cut it sharply**, to ≈ 8 % at ≈ 0.125 % Fe.
- Al-0.0035 % Cu hot rolled from 522 to 294 °C kept a deformed structure. RX appeared only after a separate anneal of the hot band [Fig. 26 p.241–242].

**Relevance to the slug route (inference from the facts above).**
1. **Exit ≈ 380 °C + water bath ≈ unrecrystallised (recovered) hot band.**
   - Even super-pure Al reached only ≈ 76 % static RX after 500 → 390 °C, 50 % and a 30 s hold. ~0.1 % Fe almost suppressed it [TOT Ch.4 Fig. 28].
   - Rotary-cast 3xxx strip carries far more Fe and Mn, much of it in supersaturation (§2.3), and is quenched within seconds of the last pass.
   - So expect little or no hot-band RX. This agrees with the ch. 19 §1 assessment; the facts above now give it a literature basis.
   - The AA5182 spectrum is a different (Al-4.5Mg-type) alloy, so use it only as an order-of-magnitude clock: at ≈ 380 °C RX takes about 0.5 s to start and several seconds to finish. The sources do not say whether lean, Mn-supersaturated 3xxx is faster or slower. The Fe/Mn evidence above (TOT Ch.7 p.356; Ch.4 Fig. 28) points to slower (inference).
2. **Cube/PSN placement.** With the AA3104 boundary (Z* = 3×10¹⁴ s⁻¹, Q ≈ 156–160 kJ/mol), in-line hot passes at 380–500 °C stay below Z* for ε̇ ≲ 50 s⁻¹ **(derived)**: ε̇ = 10 s⁻¹ at 380 °C gives Z ≈ 3–5×10¹³ s⁻¹, and 50 s⁻¹ gives ≈ 1.5–2.8×10¹⁴ s⁻¹. They are therefore on the **cube** side; the 30–50 % cold passes are on the PSN side ("CR"). The hot band's deformation state therefore favours cube nuclei for the final anneal, and the cold reduction adds PSN-random and rolling components. Composition differs from AA3104 (less Mg, more Mn in solution), so treat this as a direction, not a prediction. ⚠ These Z values use Q ≈ 156–160 kJ/mol, the Q implied by the [TOT] boundary line. [SH]'s flow-stress Q for 3004 is 193.85 kJ/mol; computing Z with that Q gives values ≈ 260–730× higher at 500–380 °C (derived) and is **not** comparable with Z* (§3.3). Keep the two sources separate.
3. **Quench vs coiling.** [TOT] describes coil self-annealing as the standard way to get a recrystallised, cube-rich hot band [p.356]. The user's water bath removes that option by design, so cube development and grain size are decided entirely in the final slug anneal. The lever left is the hot/cold split (§7.3).
4. **Added after the [SH] full-text pass.** Unhomogenised as-cast 5xxx needed a substantially higher temperature for 100 % RX after 50 % hot rolling at 400 °C (430 °C for 5252, 540 °C for 5454) than homogenised material [SH p.222–223]. Mn-free 5052 recrystallised between die exit and quench while Mn-bearing 5xxx did not [SH p.165]. Both point the same way for rotary-cast, Fe/Mn-supersaturated strip: the quenched hot band stays unrecrystallised, and the slug anneal must be set hotter than DC-based anneal windows suggest (direction only; inference).

### 4.4 Design levers (hot rolling)

- (inference from [POL p.42; TOT Ch.3 p.130–131]) For **can stock and deep-drawn fin collars**, aim for a hot band with substantial cube (from recrystallisation at transition bands) and limited PSN-random texture. That means controlled coarse-particle fraction (Fe, Si, Mn) and enough finishing temperature to recrystallise in the coil.
- For **long-life fin/tube stock (sag resistance, large post-braze grains)** the opposite applies. Keep Mn in solution or as fine dispersoids through hot rolling, so recrystallisation is pushed to the final anneal or brazing cycle (see §6, §8.5).
- Build profile and crown in the hot mill (thick, hot strip). Dilute soft alloys tend towards negative crown [RA p.5-8].

### 4.5 Pitfalls

- Too high a temperature → grain-boundary weakening and cracking [RA p.4-6/4-7].
- Edge cracking in plate. Edges are trimmed after intermediate rolling so cracks do not run in [RA §7 p.7-1].
- Wedge (side-to-side thickness difference) comes from non-parallel rolls or uneven temperature across the gap [RA p.5-8].
- Herringbone and reduction marks come from lubricant problems [RA p.5-5].
- **Inter-stand RX → coarse cube bands** that deform unfavourably in later passes (can stock) [TOT Ch.7 p.356].
- **Longitudinal property variation** from reversing/Steckel rolling: the head-to-tail delay grows from pass to pass [TOT Ch.7 p.352, 358].
- **Work-roll thermal crown in Al hot mills** changes strongly and "usually grows from strip to strip". Force varies from strip to strip and from head to tail. Al hot mills therefore need profile models more than steel mills do [TOT Ch.7 p.377].
- Shape measures for flatness specifications [TOT Ch.7 p.375–376]: crown C_r = h_m − h_r, a thickness difference [eq. 20] (h_m read here as mid-width and h_r as edge thickness; the subscripts are not defined in the text); steepness S_p = (h/l)·100 % (amplitude/wavelength) [eq. 21]; I-unit = (Δl/l)·10⁵ = (Δσ/E)·10⁵ [eq. 22–23].
- **Al hot-mill roll problems** [RR, full text]:
  - The coolant in Al hot mills contains aggressive chemical (cleaning) additives. These affect roll wear [RR §4.8.1 p.88] and cause **corrosion fatigue at back-up-roll neck fillets**. Corrosion fatigue has no fatigue limit [RR §4.6.1.2 p.80; §4.9.4.1 p.98].
  - Back-up rolls in Al hot mills see almost no wear, so they run much longer campaigns than in steel mills. The fillet must be sealed against coolant. Fillet repair by welding or re-machining is forbidden; cracked rolls can run under fracture-mechanics crack-growth monitoring [RR p.79–80, 98].
  - Broken brush wires in Al hot mills can enter between work and back-up rolls and cause local overload [RR §4.5.4 p.76].

---

## 5. Cold rolling and work hardening

### 5.1 Mechanisms

- Work hardening comes from dislocation multiplication, tangles, cells and subgrain walls. The grain-boundary area grows [POL §2.1 p.32].
- Shear bands (~35° to the rolling plane) form at true strain ≳ 1. At very high strains they can cross the whole thickness and become failure paths [POL p.32–33].
- Coarse particles cause local deformation zones, which are PSN sites [POL p.33–34, Fig. 2.5].
- Solute effects [POL p.34; TOT Ch.3 p.99–100]:
  - Cu is most effective per atom at suppressing dynamic recovery and raising dislocation storage, then Mg ≈ Si; Zn has a negligible effect.
  - Mg has the greatest *practical* value because of its high solubility.
  - In ternary systems (Al-Mg-Si, Al-Zn-Mg, Al-Cu-Mg) hardening is more than additive.
- Work hardening has an alloy-specific limit; strength and ductility trade off [RA §4 p.4-7]. Cold-worked 3003 draws *better* than annealed 3003, which matters for cans [POL p.35].
- **[TOT Ch.7 §3] on cold rolling** [p.362]:
  - Below 100 °C, climb and cross-slip are much restricted, and fracture usually comes before a steady state. Cold rolling also crushes and aligns constituent particles further.
  - 3xxx/5xxx strength rests on solid solution and, "to a lesser degree", dispersoids. Cold rolling can raise it **above 400 MPa**.
  - Mg–dislocation interaction can give peak stresses, serrated (PLC) flow and Lüders lines; the remedies "generally result in a loss in strength".
  - "The microstructural and textural characteristics of the hot rolled band determine the achievable product quality after cold rolling and heat treatments to a large extent."
- **Mill types and capacities** [TOT Ch.7 p.360–362]:
  - 6-high or 4-high heavy-gauge cold mills cover all alloys from 14 to 0.3 mm, up to 100,000 t/a. 2–3-stand tandem lines reach ~300,000 t/a for a limited product range.
  - Light-gauge mills roll down to 0.02 mm (~30,000 t/a). 2-high mills are used for bright polish rolling at low speed.
  - At thin gauges, roll flattening, roll bending and thermal crown cause **edge drop** (tight edges → quarter buckles, edge tearing), which counter-bending cannot fix. Remedies: zone cooling, inflatable back-up rolls, 6-high mills with shifting intermediate rolls.
  - Can-body gauge trend: 0.35/0.30 → 0.25 mm; strip widths up to 2000 mm [p.360].

### 5.2 Quantitative laws and parameters

Hollomon law σ = K·εⁿ [POL §2.1.1 p.35–36; TOT Ch.3 p.98–100]:
- For pre-strained tempers: σ = K(ε₀ + ε)ⁿ, where ε₀ is the prior cold work or the "equivalent cold work" of a hot-worked temper [POL p.36].
- Rolling form (Alcoa): **YS = σ₁·εⁿ**, ε = ln(t_i/t_f). σ₁ = YS at true rolling strain 1 (63 % reduction) [TOT Ch.3 p.98–99, eq. 8].

**Table 5-1 — Hollomon parameters, O-temper** [TOT Ch.3 Table 3, p.100]

| Alloy | n | K (MPa) |
|---|---|---|
| 1100-O | 0.242 | 146 |
| 3003-O | 0.242 | 188 |
| 6061-O | 0.209 | 224 |
| 5052-O | 0.198 | 281 |
| 5454-O | 0.189 | 340 |
| 5086-O | 0.193 | 368 |
| 5456-O | 0.178 | 479 |

Trend: n falls from 0.25 to 0.17 as K rises from 175 to 450 MPa [POL p.36]. Note 3003 has the same n as 1100 but a 29 % higher K.

**Table 5-2 — Solute work-hardening parameters** [TOT Ch.3 Table 2, p.99]

| Solute | K (Cu-equivalent per at %) | Doherty H (GPa) |
|---|---|---|
| Cu | 1.00 | 3.38 ± 0.20 |
| Ge | 0.64 | — |
| Si | — | 1.56 ± 0.05 |
| Mg | 0.37 | 1.52 ± 0.14 |
| Mn | — | 1.03 ± 0.17 |
| Cd | 0.33 | — |
| Ag | 0.15 | — |
| Zn | 0.071 | 0.27 (no ± given; column confirmed in the clean text, corrected after full-text pass) |

- K example: 1 at % Mg behaves like 0.37 at % Cu.
- H normalises the gain in σ₁ by the solute atomic fraction: **H = (k_alloy − k_Al)/(x_solute)^(2/3)**, where k is the YS after a true rolling strain of 1 and x is the atomic fraction [TOT Ch.3 eq. 9 p.100]. The book prints "d_Al" in the numerator, which is read here as k_Al. The 2/3 exponent was checked on the rendered page (corrected after full-text pass; the earlier OCR had garbled it).

Other work-hardening facts:
- Mg vs Mn as hardeners: "about 0.8 percent magnesium being equal to 1.25 percent manganese", and Mg can be added in much larger amounts; Mn is effective only up to about 1.5 % [RA App. C p.10C-2].
- Cryogenic working: 1100 rolled at −196 °C gains up to ~40 % strength but loses ductility [POL p.36].
- Strength gain examples [RA §2 p.2-6]:
  - 3003: UTS 110 → 200 MPa (O → H18);
  - 3004: UTS 180 → 280 MPa (O → H38);
  - NHT alloys span YS 20–500 MPa from O to H19 [POL §3.3 p.128].
- Annealed baselines [POL §3.3 p.129–130]:
  - SP Al proof stress 7–11 MPa;
  - 1100 UTS 90 MPa; 3003 UTS 110 MPa; 3004 UTS 180 MPa;
  - 5005: YS 40 / UTS 125 MPa; 5456: YS 160 / UTS 310 MPa;
  - 8xxx dispersion hardening 30–40 MPa, plus solid solution 2–10 MPa (YS) and 5–20 MPa (UTS) [POL p.131].

### 5.3 Friction, lubrication, rolls

- Friction is set by the roll surface (roughness, fire-crack network), which changes over a campaign. Lab friction coefficients of different roll grades are similar [RR §3.6 p.51–52] (page cite corrected after full-text pass).
- Chrome-plated work rolls are used for hardness, finish and life [RA §4 p.4-3]. Work rolls for Al hot rolling and for cold rolling wear little, but **their surfaces lose roughness**, and this shows on the product. Chrome plating prolongs campaigns [RR §4.9.1 p.95].
- **Cold-mill roll pairing.** Cold strip work-hardens immediately and cannot absorb accidental local overload, and the work roll must not deform. So the back-up roll must be **significantly softer** (lower yield strength) than the work roll and take the overload plastically [RR §4.5.4 p.77; §4.10.2.2 p.101]. Hot mills do not need this [RR p.77, 101].
- Cold-mill back-up rolls develop work-hardened areas, which are checked by hardness readings and ground off. Every regrind should end with eddy-current crack testing [RR §4.9.1 p.95; §4.6.2.3 p.84].
- Sub-surface "crumbly" spalls in cold-mill back-up rolls start at inclusions or micro-porosity at the depth of maximum Hertzian shear. Particle cleanliness of the roll material (e.g. ESR) is the cure [RR §4.6.2.3 p.84].
- Hardness within one roll grade has no effect on work-roll tonnage performance (ICDP data). Carbide *type* matters more than carbide content [RR §4.8.1 p.89–90].
- Roll crown, roll bending, tilting, crossing, axial shifting (CVC-type profiled rolls), stepped and sleeved back-ups, and zoned spray cooling are the flatness/profile actuators [RA §5 p.5-9/5-10].
- Small rolls give larger reductions per pass but deflect more; large rolls are thermally more stable but have more inertia [RA §4 p.4-3/4-4].
- Cold-mill coolant mainly controls roll temperature and dimensions [RA self-test 5.20].
- **Cold-rolling lubricants and annealing stains** [TOT Ch.7 p.368]:
  - The usual lubricants are low-viscosity mineral oils with boundary additives; emulsions are increasingly used for sheet.
  - Heating in rolling **or in the subsequent anneal** can leave **brown or black stains**, "a major problem associated with lubricants".
  - Foil is rolled with purified paraffin (kerosene), "but staining during subsequent annealing can still be a serious problem".
  - Friction values: §4.2.
  - **Relevance to the slug route (inference):** the residue left by the cold mill goes into the slug anneal. It belongs with the MgO/oxide-growth variables (ch. 14), together with the roll-campaign variable in §5.6.

### 5.4 Foil rolling

What is in the sources:
- Al alloys can be rolled to ~0.05 mm, pure Al to 0.0025 mm [RA p.5-7].
- Two-high mills are used mostly for foil and in labs [RA §4 p.4-4].
- 8011 is a deep-drawing bottle-cap alloy; 8006 (Al-1.6Fe-0.65Mn) and other dilute TM-bearing alloys are used for foil and fin stock [POL §3.3.4 p.131].
- TRC is an established foil-feedstock route (1235/8011) [TRC].
- **[TOT Ch.7 §3, §4.3] (read in full 2026-10-12):**
  - Foil is finished in special 4-high mills. Light-gauge 6-high mills with shifting intermediate rolls serve for foil roughing [p.360–361].
  - Speeds above 1000 m/min need high-quality process control. Up to 1500 m/min, 4-row cylindrical plus 2-row axial roller bearings are used; above 1500 m/min, oil-film bearings [p.361–362].
  - **Conventional (circular-arc, Hitchcock) rolling theory fails below an exit thickness of ~100–70 µm** (Löffler & Kramer) [p.370]. The deformed roll is no longer circular (Orowan 1943). Specific foil models use two elastic zones, two plastic zones and a central rigid "no-reduction" zone [Fig. 15 p.371]. The pressure becomes Hertzian, with an exit-side peak like elastohydrodynamic bearings, instead of the friction hill [Fig. 16 p.372–373].
  - Rolls of 300 mm diameter can still reach < 13 µm [p.370].
  - The oil entering the gap sets friction, the possible reduction and the surface. It arrives by three routes: hydrodynamic entrainment, oil trapped in roughness valleys, and adsorbed boundary layers. Foil rolling runs in mixed lubrication after a hydrodynamic inlet; friction models for this regime are still open [p.373].

Gap G4 (narrowed): still no foil pass schedules, pack ("double") rolling, pinhole limits or final-anneal practice for 8011/8006/1235. [TOT Ch.7] has none.

### 5.5 Internal heuristics (user spreadsheets — not literature) [INT-CRM]

| Alloy | CRM ε_t target | Reduction | Final anneal | Expected grain size (µm) | Heating-rate note |
|---|---|---|---|---|---|
| EN AW 1070 | ≥ 0.95 | ≥ 61 % | 280–320 °C, 1–2 h (avoid > 340 °C) | 28–48 | not critical |
| EN AW 1050 | ≥ 0.90 | ≥ 59 % | 300–340 °C, 1–2 h (keep < 360 °C) | 30–50 | moderate |
| EN AW 3102 | ≥ 0.80 | ≥ 55 % | 340–370 °C, 1–2 h | 40–65 (slightly elongated) | moderate |
| EN AW 3207 | ≥ 0.85 | ≥ 57 % | 350–380 °C, 1–2 h | 30–50 | reasonably fast |
| EN AW 3003 | ≥ 0.95 | ≥ 61 % | 370–400 °C, 1–3 h | 35–55 | **fast** — slow heating raises T_rx by ~100 °C |

Context: start strip 22 mm → HRM → CRM → full anneal → cold-extrusion slugs. Below ε_t ≈ 0.85, grains are coarser and more variable (orange-peel risk for 3003). Ideal 3207 CRM ε_t is 0.85–1.10, with diminishing returns above ~1.2.
- Status: plausible, and consistent with [POL p.42] (300–420 °C window) and [RA p.5-6]. **The grain sizes are internal estimates, not measured.**
- Cross-check against [INT-RX]: the JMAK model gives T(50 % RX in 1 h) of 327 °C at 45 % CR and 299 °C at 70 % CR for 3207 (0.45Mn-0.15Mg-0.09Cu). So the 350–380 °C anneal has ~25–50 °C margin (internal model).

### 5.6 Design levers (cold rolling)

- **Final cold reduction before anneal** is the main lever on recrystallised grain size and cube fraction; **cold reduction after anneal** sets the H-temper. Table 5-1 together with YS = σ₁εⁿ [TOT] gives the reduction needed for a target YS (inference).
- [TOT] states the same lever for NHT sheet: cold passes and annealing "need to be designed in order to meet the requirements on both strength and texture". They are adjusted to the condition of the hot band, so that anisotropy is balanced while work hardening reaches the target strength [TOT Ch.7 p.362, 364].
- Per-atom solute choice for work hardening (Table 5-2): Cu ≫ Mg ≈ Si > Mn ≫ Zn. Cu ≤ 0.3 % in NHT alloys [POL p.34]. For 3xxx fin/tube, small Cu/Mg additions add H14/H24 strength cheaply. Watch the corrosion potential (outside scope).
- Avoid excessive total ε before a soft anneal: the risk is shear bands and edge cracks at ε ≳ 1 [POL p.32–33].
- **Roll campaign as a hidden process variable (inference from [RR p.93, 95]).** Work-roll roughness falls and roll-gap friction drifts during a campaign. For slug strip, record the work-roll campaign position (tonnage or km since regrind) with each coil. Friction changes the through-thickness shear, the strip heating and the surface topography, so it can move the surface recrystallised grain size and the lubricant residue left for the anneal (MgO growth). The size of the effect is not quantified in any source.

### 5.7 Pitfalls

- Heat build-up to ≥ 80 °C at high speed allows recovery and lowers the as-rolled temper. Flatness is lost through thermal crown [RA p.5-7].
- Over-rolling beyond the alloy's work-hardening limit → cracking on the next pass; an intermediate anneal is needed [RA p.5-7].
- Lüders bands (Al-Mg O-temper) and PLC serrations: avoid by forming strain-hardened stock or forming above 150 °C [POL §2.1.5 p.40–41].

---

## 6. Annealing after cold rolling (process view)

Physics belongs to the recrystallisation KB; only the process numbers are given here.
- Dislocation density: ~10¹² cm⁻² (heavily cold worked) → ~10¹⁰ cm⁻² after recovery → 10⁷–10⁸ cm⁻² after recrystallisation [POL §2.1.6 p.41].
- Strength falls gradually during recovery, then sharply during recrystallisation. Data for hard-rolled CP-Al: 5 min anneals [POL Fig. 2.10 p.41].
- Batch coil annealing must allow conduction to the innermost wraps. Continuous strip annealing heats fast and gives a finer grain [RA §5 p.5-7].
- Atmosphere: dry N₂ to avoid oxidising lubricant residues and forming MgO on Mg alloys [RA p.5-7].
- **Heating-rate sensitivity in Mn-bearing 3xxx.** The mechanism (Mn precipitating before recrystallisation and pinning the substructure) is stated in [INT-CRM] and [INT-RX] notes. It is consistent with the dispersoid-pinning role in [TOT Ch.3 p.125; POL p.43]. **Partial literature support from [SH §5.4 p.216–217] (full-text pass, 2026-10-12):**
  - Study design: 1100 cast as 2.5 cm slab, homogenised, cold rolled to 1 mm and annealed. 3004 cast as 50 cm ingot, homogenised, hot rolled 460 → 260 °C to 4.2 mm, cold rolled to 1.0 mm and annealed. Two anneals: **batch (25 °C/h heating, 2 h at 350 °C)** and **continuous (25 °C/s heating, a few seconds at 500 °C)** (heating rates checked on the page image; the homogenisation heating rate is printed as 40 °C/s).
  - 1100: 0/90° earing (cube) was achievable **only after continuous annealing**, with a homogenisation hold window of 400–450 °C. 3004: optimum homogenisation hold ≈ 530 °C for the batch anneal and ≈ 610 °C for the continuous anneal. The optima lie near the C-curve nose for Fe and Mn precipitation from the cold-rolled supersaturated matrix. Moving away from the optimum lowered dispersoid density, widened PFZs and *raised* the cube fraction after annealing.
  - In the **continuous** anneal of 3004, "recrystallization occurs without dispersoid interaction", and cube rises monotonically with homogenisation temperature [p.216–217].
  - Ingot-cast 3004, batch anneal: the most cube (lowest 45° earing) came after 535 °C/4 h homogenisation [p.217].
  - What this supports: with slow (batch) heating, Fe/Mn precipitation from a supersaturated, cold-rolled matrix interacts with RX and suppresses cube; with fast heating, RX outruns precipitation. That is the [INT-RX] mechanism. What it does not give: the ~100 °C T_rx shift claimed for 3003 in [INT-CRM], or any grain-size numbers. G5 is narrowed, not closed.
  - **Relevance to the slug route (inference).** The rotary-cast strip is *more* supersaturated than these homogenised ingots (§2.4 items 7–9). So the heating-rate effect should be at least as strong for slugs: a slow batch heat-up gives Fe/Mn precipitation first (pinning, coarser and less cube-rich grains); a fast heat-up favours RX first (finer grains, more cube). Record the slug heating rate in every trial.
- Internal model constants [INT-RX] (internal, calibrated, not literature):
  - Q_rx = Q₀ + Σ dQᵢ·cᵢ = 100 + 100·Mg + 200·Cu + 80·Mn(ss) = 145 kJ/mol for 3207;
  - JMAK n = 3; B₀ = 2.5×10²⁸ s⁻ⁿ; strain exponent m = 2;
  - t₅₀ ≈ 300 s at 350 °C, 70 % CR.
  - ⚠ Internal inconsistency: Zener limit d = 4r/(3F_v) = 17.8 µm and P_Z = 0.0365 MPa both use **r = 80 nm**, while the sheet labels 80 nm as the dispersoid *size*. If 80 nm is a diameter, d_Z = 8.9 µm and P_Z doubles **(derived)**.

**Temper definitions relevant to slugs and cans [RA App. B p.10B-1/10B-2, ANSI H35.1-2006] (full-text pass, 2026-10-12).**
- **O**: fully annealed, softest. Full annealing "converts both heat-treatable and non-heat-treatable wrought alloys into their softest, most ductile, most workable condition" [RA §5 p.5-6].
- **H1x**: strain-hardened only. **H2x**: strain-hardened more than needed, then partially annealed; for alloys that age-soften at room temperature, H2x has the same minimum UTS as H3x, otherwise as H1x with slightly higher elongation. **H3x**: strain-hardened and stabilised "either by a low temperature thermal treatment or as a result of heat introduced during fabrication"; applies only to alloys that age-soften at room temperature; stabilisation "usually improves ductility" [RA App. B p.10B-1/10B-2]. No stabilisation temperature is given in Appendix B (G10).
- **H4x: strain-hardened and lacquered or painted.** "Applies to products which are strain-hardened and which are subjected to some thermal operation during the subsequent painting or lacquering operation." The second digit gives the strain hardening remaining after the cure, and "the corresponding H2X or H3X mechanical property limits apply" [RA App. B p.10B-2].
- **Relevance to the slug route (inference).** The impact-extruded can wall is strain-hardened, and the 220 °C/10 min lacquer bake is exactly the "thermal operation during lacquering" that the H4x temper describes. So specify and test can-wall properties **after** the bake, against H2x/H3x-type limits. Hard-rolled pure Al needs several hours at 280 °C to recrystallise [POL p.42], so a 10 min bake at 220 °C should mainly recover the wall, not recrystallise it. For Mg+Si-bearing T11 the bake also acts as a short artificial age: it is hotter and much shorter than the 115–190 °C, 5–48 h precipitation treatment range for sheet [RA §6 p.6-3].

---

## 7. Texture and earing (can, foil, fin-collar stock)

### 7.1 Mechanisms

- **Rolling (deformation) texture** of FCC sheet [TOT Ch.3 p.131; POL §2.1.4 p.39]:
  - components {110}⟨112⟩ (Brass), {123}⟨634⟩ (S), {112}⟨111⟩ (Copper);
  - Polmear describes them as a "tube" of orientations linking (110)[1̄12], (112)[1̄1̄1] and (123)[4̄1̄2] (indices garbled in the text).
- **Recrystallisation texture** [TOT Ch.3 p.131; POL p.39]:
  - cube {001}⟨100⟩ and Goss {011}⟨100⟩, strong especially in high-purity alloys;
  - PSN from coarse constituents randomises the texture;
  - final texture and grain size depend on cold work, heating rate, temperature/time, composition, and particle size and distribution.
- **Extrusions/rod/wire** develop a ⟨111⟩+⟨001⟩ dual fibre (⟨110⟩ fibre for wire per [POL p.39]). In heat-treatable extrusions this raises longitudinal YS by ~70 MPa over transverse [TOT Ch.3 p.131]. An ideal fibre texture can be ~20 % stronger along the fibre than a random aggregate [POL p.39].
- **Earing** [POL §2.1.4 p.39–40; TOT Ch.3 p.131]:
  - four ears usually form;
  - rolling texture dominant → ears at **45°** to RD;
  - cube (annealing) texture dominant → ears at **0°/90°**;
  - a balanced mix → eight small ears or none.
  - Earing is controlled by careful rolling and annealing schedules, sometimes with cross-rolling [POL p.40].
  - For 3004-H19 can stock, earing is controlled by **balancing the cube texture developed during annealing against the rolling texture added on the way to final temper** [TOT Ch.3 p.131].
  - Can stock also depends on controlling the size, volume fraction and distribution of Al₁₂(Fe,Mn)₃Si constituents [TOT Ch.3 p.123].
- r-value: a large r means few slip modes give through-thickness strain, which resists thinning and is good for deep drawing [POL p.37, 39].
- **[TOT Ch.7 §3] earing by hot-band state** (read in full 2026-10-12) [p.362–364]:
  - A partially recrystallised hot band carries the rolling texture (β-fibre). Printed: it "leads to 0/45° earing". Fig. 8 shows 45° ears for the *unrecrystallised* band, so "0/45°" is read here as **45° ears** (consistent with [POL; TOT Ch.3]).
  - The cube of a fully recrystallised hot band gives 0/90° ears.
  - The **RD-rotated cube** component "produces additional ears at 0/180°", i.e. along RD (as printed).
  - **Six- or eight-ear** cup profiles reflect the relative intensity of the components.
  - Earing is expressed as the percentage earing of a drawn cup. The r-value (width/thickness strain in uniaxial tension) is "another quality measure". Strong texture variations give r differences, which cause **thickness irregularities in any deep-drawing operation** [p.362].

### 7.2 Quantities (gap G6 closed 2026-10-12, for 3104/5182 can stock)

**Definitions [TOT Ch.18 eq. 5–7 p.851].**
- r = ε_width/ε_thickness.
- r̄ = (r₀ + 2r₄₅ + r₉₀)/4.
- Δr = (r₀ − 2r₄₅ + r₉₀)/2.
- Δr "is a measure of earing tendency": higher Δr → more earing → more trimming and less usable draw depth [p.851–853].
- Sign convention (general knowledge, consistent with the definition): Δr > 0 → 0/90° ears; Δr < 0 → 45° ears.

**AA5182, inter-stand RX vs final earing and cube (read from Fig. 6 p.359, Hirsch, Karhausen & Kopp 1994; ±0.1 %-point earing, ±0.5 f(g)).** The x-axis is the *computed* inter-stand RX fraction after the first pass of a three-stand hot mill. The stage at which earing was measured is not stated.

| Inter-stand RX (%) | 22 | 44 | 58 | 69 | 88 | 97 |
|---|---|---|---|---|---|---|
| 0/90° earing (%) | 5.2 | 4.4 | 3.7 | 2.9 | 2.7 | 2.4 |
| Cube intensity f(g) | 15.9 | 15.3 | 14.0 | 11.8 | 10.6 | 9.5 |

- Fitted lines: earing ≈ 5.9 − 0.038·X_RX (%); cube ≈ 18.6 − 0.091·X_RX (derived from the plotted regression lines).
- **More inter-stand RX → less final cube → less 0/90° earing.** This fits the text: inter-stand RX makes coarse cube bands that deform unfavourably [p.356]. Industry used the computed fraction for pass optimisation [p.358].

**AA3104 and AA5182, earing vs hot-band state and cold reduction (read from Fig. 8 p.363, Hirsch, Wagner & Schmiedel 1995; relative cup height = local height / mean; ±0.005).**
- Panel temperature labels are 260 / 280 / 315 °C. The subscript is illegible; it is probably the hot-band finishing or coiling temperature (inference).
- {111} pole-figure maxima: 6.1 / 5.2 / 4.0 (AA3104) and 1.1 (AA5182).

| Hot band | 0 % CR | 50 % CR | 75 % CR | 92 % CR |
|---|---|---|---|---|
| AA3104 unrecrystallised (260 °C) | 45° ears: 1.034 at 45°, 0.984 at 0°, 0.964 at 90° | — | 45°: ≈ 1.057; 90° ≈ 0.94 | 45°: ≈ 1.06 |
| AA3104 partially RX (280 °C) | mixed: ≈ 1.04 at 0°, ≈ 1.02 at 90°, ≈ 0.98 in between | — | 45° ≈ 1.02 (0° ≈ 1.02) | 45° ≈ 1.045 |
| AA3104 fully RX (315 °C) | **0/90° ears:** 1.044 at 0°, 1.035 at 90°, 0.965 at ~50° | 90° ear gone; 0° ear ≈ 1.035; ≈ 0.98–1.0 elsewhere | label at ≈ 1.017 near 45°; curve poorly legible | 45° ≈ 1.04 |
| AA5182 | almost flat: ≈ 1.015 at 0°, ≈ 0.99 at 45–90° | 45° ≈ 1.02 | 45° ≈ 1.04 | 45° ≈ 1.06 |

- So: a fully recrystallised, cube-rich hot band starts with 0/90° ears of about ±4 %. **Somewhere between ~50 % and ~75 % cold reduction the profile is flattest**: at 50 % only the 0° ear is left, and 75 % already peaks near 45°. At 92 % the ears are 45° ears of about +4 %.
- An unrecrystallised hot band has 45° ears from the start, and every cold pass makes them larger.
- AA5182, with an almost random hot band, is flat at 0 % and builds 45° ears steadily with cold reduction.

- Only other quantitative texture values found: [INT-RX] sheet "RX texture vs annealing temperature". It is an **internal assumption table**: cube 5 % at 250 °C → 30 % at 350 °C → 52 % at 500 °C; PSN-random 15–30 %. Do not treat it as data.

### 7.3 Design levers (inference from [POL; TOT])

- To get **low earing in cups and collars**, set the hot-band/annealed cube fraction so that the 45° ears added by the final cold reduction cancel the 0/90° cube ears. Final cold reduction and hot-band cube are coupled design variables.
- **Alloy lever.** More coarse constituents (Fe/Si/Mn, e.g. α-AlFeMnSi) give more PSN, a more random texture and lower earing amplitude, at the cost of formability and surface. Dispersoids suppress PSN and favour cube (also the [INT-RX] assumption). So Fe/Mn/Si in 3xxx foil and fin tunes the cube vs random balance.
- Cross-rolling at breakdown weakens textures [POL p.40; RA p.5-3].
- **Hot-mill lever (can stock):** inter-stand RX fraction, steered by rolling temperature and speed [TOT Ch.7 p.356], moves final earing by about 3.5 %-points (5182, Fig. 6). The coiling/finishing temperature sets the hot-band RX state (3104: unrecrystallised at 260 °C, fully recrystallised at 315 °C in Fig. 8).

**Relevance to the slug route: hot/cold split for grain size and earing (inference from §4.3, §7.2).**
- The quenched hot band from the ≈ 380 °C exit is expected to be **unrecrystallised/recovered** (§4.3). The closest [TOT] analogue is the "AA3104 unrecrystallised" hot band in Fig. 8. It already has 45° ears at 0 % CR, and every further cold reduction raises them (≈ +3.4 % at 0 % → ≈ +5.7 % at 75 %).
- But on the slug route the cold-rolled strip is **fully annealed after cold rolling**. The Fig. 8 sequence (hot band → cold rolling → cup, without a final anneal) does not apply directly. Only the deformation texture going into the anneal carries over. Earing in the slug route is decided by the **post-anneal** cube/PSN/retained-rolling balance.
- What does transfer:
  1. A hot band with no RX (quenched) carries **all** its hot-rolling β-fibre and recovered substructure into the cold mill. The final anneal then starts from hot + cold rolling texture. The extra hot strain adds some stored energy, though much less than the same cold strain because it was dynamically recovered (ch. 19 §1). It also strengthens the retained rolling component if RX is incomplete.
  2. Moving reduction from the hot mill to the cold mill (smaller hot reduction, more cold %) raises the cold stored energy for the final anneal. It also raises PSN activity (cold rolling is in the PSN field of Fig. 4), which randomises the texture and lowers earing amplitude. Moving reduction to the hot mill does the opposite: more low-Z (cube-favouring) deformation, less stored energy, and a coarser and more cube-textured anneal (direction only, magnitudes unquantified for 3102/3207).
  3. The [INT-CRM] rule (ε_t ≥ 0.80–0.85 cold before the anneal) and the 30–50 % cold reduction actually available (ε_t 0.36–0.69) remain the binding constraint for grain size (ch. 19). [TOT] gives no data that relax it.
- **Measure, not model:** add cup-earing or slug r₀/r₄₅/r₉₀ (Δr) to the trial measurement plan (`knowledge/trials/`), with the hot/cold split recorded. No lean-3xxx earing data exist in any source read.

### 7.4 Pitfalls

- Mechanical fibring (grain shape, particle alignment) causes anisotropy that is often larger than crystallographic texture. Do not attribute all anisotropy to texture [POL p.40].
- Orange peel comes from coarse surface grains. Shallow coarse grains are less harmful, and hot-worked products are less prone than cold-worked [POL §2.1.6 p.43].

---

## 8. Extrusion

### 8.1 Modes and equipment

**Direct vs indirect** [SH §1.3 p.7–12; §1.6 p.20–21]:
- Direct extrusion: the billet slides or shears against the container. Up to **50 % of the work** goes into shearing the near-wall layer [SH p.20].
- Aluminium sticks to the container. A close-fitting dummy block leaves little shell; surface impurities and peripheral segregation collect in the **discard** [SH p.10].
- In heavy metals a dummy block ~2 mm under container diameter leaves a shell ("Dick's method") [SH p.10].
- Indirect extrusion [SH p.11–12, 20–21]:
  - **25–50 % lower peak load**; pressure does not depend on billet length;
  - no frictional surface heating, so higher speeds and less edge or surface cracking;
  - no PCG or coarse peripheral zone; possible zero recrystallisation after solution treatment.
  - Penalties: billets must be machined or die-scalped; cross-section is limited by the hollow stem; quench is delayed (product travels through the stem).
  - Best suited to 2xxx/7xxx bars, tubes and heavy sections.
- Load–stroke curve [SH §1.3 p.10–11]:
  - direct: rises steeply on upset, peaks at breakthrough, falls with billet length, then rises at end of stroke;
  - indirect: flat, no length dependence.
- **Bridge/porthole (welding-chamber) dies** are used for hollow and multi-port shapes. They suit 1xxx, 6xxx, dilute 3xxx/5xxx and Al-Zn-Mg 7xxx; they exclude high-strength aerospace alloys [SH §1.5 p.14–15]. Billet-to-billet extrusion works for the same alloy groups [SH p.13].
- Air removal: rapid front heating gives an axial gradient of ~90–100 °C, so upset fills the container front-to-back [SH p.13]. Dummy-block cleaning return load can reach ~10 % of press capacity [SH p.14].
- **Press example (16 MN direct)** [SH Fig. 1.9 p.18]:
  - containers Ø156 mm (840 MPa) and Ø206 mm (480 MPa), 850 mm long;
  - max ram speed under load 20 mm/s.
- Columns are prestressed ~20 % above maximum load [SH p.18]. Containers and liners are 5 % Cr hot-work steel [SH p.20].
- Billet heating [SH §1.6 p.19; §2.5.1 p.49]:
  - 50 Hz induction: centre-to-surface spread ≤ 3–4 %; allows taper heating;
  - modern gas furnaces: 15–20 min cycle with comparable uniformity;
  - the printed induction penetration depth "~18 µm" is likely an OCR or print error (mm order).
- Extrusion ratios up to ~100:1 are common, but most industrial empirical formulas were fitted at R < 10 [SH §2.3.2 p.35; §2.3.3 p.37]. MPE tube runs at R ≈ 817 [WIL].
- **Plant practice, 6xxx profiles [TOT Ch.8 §2] (read in full 2026-10-12):**
  - Deforming metal is at 450–600 °C over the press cycle, with no die lubrication, so the metal sticks to container and die [p.386].
  - Common containers: Ø0.178 m → 16 MN press (643 MPa specific pressure); Ø0.208 m → 22 MN (647 MPa). Billet 5–10 mm under the container bore [p.388, 393].
  - Billet 450–470 °C, taper-heated (hottest at the front) so the run-out temperature stays constant. Profile leaves the die at **550–600 °C** [p.393].
  - **R normally 20–80**; above ~70 multi-hole dies are used (R = A_c/(n·A_s)). Discard 10–20 mm [p.388].
  - Stretch 0.5–2 % on the cooling table; 6 m cut lengths; ageing 3–6 h at 170–190 °C [p.394].
  - Worked example: AA6060, R = 57, 36 m/min run-out, 87.7 % yield, ≈ 1573 kg/h [p.394–397].
  - Die prices (2003): open $1000–2000, hollow $1500–4000 [p.411].
  - Continuous **Conform** extrusion (rotating grooved wheel) makes open and hollow sections, including multi-port tube (ref. Dawson 1996). It is used "for special products in limited quantities" [p.386–387].
  - AA3103 is the generic alloy for cold-drawn tubes in radiators and air conditioning [Table 6 p.409].

### 8.2 Pressure, friction and temperature equations

| # | Equation | Use / numbers | Ref |
|---|---|---|---|
| E1 | p = σ̄·ln R (homogeneous work, Siebel) | **Underestimates by ~60 %**: ignores the peak, friction and redundant work | [SH §2.3 eq. 2.5 p.29] |
| E2 | p = σ̄(a + b·ln R + c·L) | Generic form: a = redundant work, b = inhomogeneity, c = friction | [SH eq. 2.6 p.29] |
| E3 | p_T = σ̄·(a + b ln R + 4mL/(√3·D_B)) | Bulk (slab) analysis with sticking factor m | [SH §2.3.1 eq. 2.7 p.31] |
| E4 | **P = σ̄·[0.171 + 1.86 ln R + 4m·L_B/(√3·D_B)]** | Minimised axisymmetric upper bound (double-triangle field). **Verified on the page image** [p.36]. Without friction, **p/σ̄ = 0.171 + 1.8594 ln R**, a linear regression "valid for rod extrusion up to a ratio of 100"; at higher R the constant can turn negative, so it is not a measure of redundant work [SH eq. 4.3 p.144]. m was observed between 0.8 and 0.9 [p.144]. ⚠ Eq. 4.4 on p.144 prints "171" for 0.171 (misprint) | [SH §2.3.2 p.36; eq. 4.3–4.4 p.144] |
| E4′ | As printed: **p = σ̄·[0.171 + 1.86 ln R + 4m·((D_B − D_E)/(2 tan δ))/(D_B√3)]**, m = 0.88 (average) | **Corrected after full-text pass.** The page image shows the friction length as (D_B − D_E)/(2 tan δ), with **no L_B term**; the earlier reconstruction "L_B − (D_B − D_E)/(2 tan α)" is not what is printed. Whether the printed form omits L_B by mistake cannot be settled from the book; for full-length billets use E4 | [SH eq. 2.26 p.57] |
| E5 | Deformation-zone depth **X_D = 0.35·D_B·(1 + 0.15√R − 0.0145R)**; semi-angle **δ = 38.7 + 6.9 ln R (°)** | **Verified on the page image** (G14 closed). δ "is normally assumed to be 45°" | [SH eq. 2.28–2.29 p.57] |
| E4a | Total pressure with constitutive constants: **p = (1/αn)·[A + B·ln R + C·ln(Z/A) + D·(L_B/D_B)·ln(Z/A)]** | The ln R × ln(Z/A) cross term was dropped as statistically insignificant. Laboratory-scale constants (A, B, C, D, αn) for 5456, 5083, 5056, 5052, 2014 (5 % and 4 % Cu), 1100, 7049, 7075, 7150 in [SH Table 4.2 p.146] (checked on the page image; `cloudpart4/txt/ww.txt` l. 253–265), e.g. **1100: A = −3.9056, B = 3.849, C = 1.728, D = 0.0179, αn = 0.192**; 7075: 14.176, 11.60, 1.757, 2.211, 0.093. ⚠ **Derived check:** at R = 30, L_B/D_B = 2, ε̇ = 1 s⁻¹, E4a gives pressures 1.2–1.8× lower than E4 + H6 with Table 3-1 constants for 5052, 5083, 5456 and 7075, and **≈ 4.3× lower for 1100** (e.g. 63 vs 272 MPa at 450 °C). The 1100 row's αn also disagrees with Table 3-1 (§3.3). Do not use the 1100 row of Table 4.2 without recalibration (G15) | [SH eq. 4.6–4.8 p.145–146] |
| E13 | Shaped sections and bridge dies | Peripheral ratio λ = periphery of the section / periphery of a round of equal area; λ² multiplies R and Z in the pressure, surface and RX equations [SH §4.6.3 p.146–148]. For 2024 the fitted direct-extrusion law is p = (1/αn){1.76 + 10.92 ln λ²R + 4.56 ln(λ²Z/A) + 2.86(L/D)·ln(λ²Z/A)}, correlation 0.975 [p.147]. Multi-hole dies: λ from all holes, corrected by the pitch-circle diameter [p.148]. **Bridge/porthole dies are treated as two extrusions in series** (into the weld chamber, then through the die), R_t′ = λ₁²R₁·λ₂²R₂ [p.148–149]. Laue's difficulty classes with Sheppard's "modified shape factor": simple bar 2.8, standard sections 4.8, semi-hollows 21.16, tubes 40, simple hollows 82, tubes with projections 120 [SH Table 5.5 p.239] | [SH p.146–149, 239] |
| E14 | Surface-limit criteria | 5456 rod: acceptable surface if **ln(Z_i/A) ≤ 6.35×10²⁰/T^7.06** (T in K) [SH p.154, Fig. 4.16]. General form (1/n)·ln(Z_i/A) ≤ a·T⁻ᵇ. 2024 shapes: (1/n)·ln(λ²Z_i/A) ≤ 2.113×10⁹/T^2.866 (direct) and ≤ 2.4×10¹⁰/T^3.57 (indirect) [p.154]. Points above and right of the locus give defects (Fig. 4.18, many alloys) [p.154–155]. Mechanism: die-land friction vs flow stress, and local melting if the solidus is exceeded [p.151–154] | [SH §4.7 p.151–156] |
| E6 | Friction: τ = m·k (m = 0 perfect lubrication, m = 1 sticking) or τ = μp | **Design m ≈ 0.85**; measured m = 0.88 (1100, 2014 at 300–475 °C). The shear layer at the container is ~40–100 µm thick | [SH §2.4 p.48–49] |
| E7 | Table 2.2 μ values (R = 30, P = aL + C) | 1100, 8 mm/s: μ = 0.075 (300 °C), 0.092 (400 °C). 2014, 5 mm/s: μ = 0.048 (300 °C), 0.055 (400 °C), 0.098 (475 °C). μ *rises* with T, contrary to earlier reports | [SH Table 2.2 p.49] |
| E8 | Stüwe ΔT₁ (adiabatic deformation heat): ∝ σ̄·ln R/(ρc_p) | Exact prefactor illegible. Temperature rise ∝ flow stress × ln R | [SH §2.5.2 p.51] |
| E9 | Stüwe ΔT₂ (container friction) ∝ (σ̄/√3)/(ρc_p)·√(V_R L_B/a). Die-land ΔT₃ ∝ (σ̄/√3)/(ρc_p)·√(V_E L_D/a); heated depth y_D ∝ √(a L_D/V_E) | Die-land contact time < 0.005 s for 6xxx, so heat concentrates in a thin surface layer that forms the product surface | [SH p.51] |
| E10 | Lange: edge ΔT ≈ 2 × mid-face ΔT; ΔT grows with exit speed and die-land length | | [SH p.52, Fig. 2.11] |
| E11 | Integral-profile heat balance: 95 % of work → heat. Material constants: Al k = 201 W/m·K, ρ = 2800 kg/m³, c_p = 1063.9 J/kg·K; Cr-V tool steel k = 32.65 W/m·K, ρ = 7860 kg/m³, c_p = 489.76 J/kg·K | Real-time capable; matches FEM for 7075 (R = 30, 3 mm/s, billet 300–425 °C) | [SH §2.5.4 p.55–58] |
| E12 | Interface temperature T_I = f(T_B, T_C, effusivities √(kρc_p)) | Billet–container contact | [SH eq. 2.25 p.56] |

**Exit temperature** is the controlling variable. It rises when deformation and friction heat exceed losses, so above a certain ram speed heat generation dominates [SH §2.5.2 p.50–51]. Exit temperature rises steeply with both R and ram speed (7075, R = 30) [SH Figs 2.18–2.19 p.60]. Die-land friction adds a significant surface ΔT for 6063 at R = 60, 25–55 mm/s, 400 °C [SH Fig. 2.20 p.61].

### 8.2a Analytical results from [TOT Ch.8 §4] (Støren & Moe; read in full 2026-10-12)

| # | Result | Use / validity | Ref |
|---|---|---|---|
| T1 | **F = a + b·ln R** (upper-bound sum of deformation, shear-discontinuity and dead-zone friction terms) | "Experiments confirm this relationship for various metals over a range of extrusion speeds". a and b depend on profile geometry: complex sections need more force at the same R (higher friction-surface/volume ratio). a and F vary over the stroke (container friction falls; final rise as the dead zone empties). The slab method gives the same form, but only for small R | [p.447–448, 463] |
| T2 | Lower bound (statically admissible field, frictionless): **p = 5k(R − 1)/R** | Valid for R ≥ 3 | [p.444] |
| T3 | Slip-line, frictionless plane strain, R = 3: pressure rises from k to k(1 + π) through the fan; die pressure **σ_x = −2k(1 + π/2)** | Analytical test case. Also gives flow lines, residence times and adiabatic ΔT = 2√2·(k/ρc)·[arctan terms] | [p.455–460, eq. 62–72] |
| T4 | Slip-line field with **full sticking** breaks down at **R ≈ 12.5** (the outer fan line becomes tangential to the die) | Limits on analytical solutions; use FEM above it | [p.462] |
| T5 | Logarithmic strain ε_z = ln R ≈ 4 for the usual R ≥ 50; locally much higher from shear. Marker technique works to ε ≈ 10 | | [p.421, 423] |
| T6 | **Strain rates:** up to ~10,000 s⁻¹ in the shear layer at the die/bearing entry vs ~0.1 s⁻¹ at the bearing-channel centre. Sticking zone on bearings: 1000–10,000 s⁻¹ | So a constitutive law must cover ≥ 5 decades of ε̇. Partial recrystallisation across the section follows from this | [p.429–431, 474] |
| T7 | **Stored energy of cold work ≤ ~5 %** of the deformation work. In hot extrusion the stored part "may be neglected", so ρc·Ṫ = σ̄·ε̄̇ (adiabatic) | Same heat-fraction basis as [SH] E11 (95 % → heat) | [p.459–460] |
| T8 | Velocity-discontinuity heating ΔT = k·Δγ/(ρc); shear strain across a discontinuity Δγ = Δv/v_n (2 for the R = 3 die-face line) | Adiabatic upper estimate; real profiles are cooler and more uniform | [p.460–461] |
| T9 | **Bearing-channel slab example:** sticking for the first 4 mm (τ = k = 30 MPa), then τ falling linearly to 5 MPa at the 8 mm outlet. Gives σ_x ≈ **−190 MPa at the bearing inlet**, a surface-to-centre ΔT of 75 °C in the sticking zone, and a centre rise of ≈ 85 °C at the outlet (v = 1 m/s, λ = 200 W/m·K, ρ = 2700 kg/m³, c = 1100) | Illustrative inputs. ⚠ c is printed with unit "W/mK"; read as J/(kg·K). Bearing lengths run from "a couple of millimeters to about a centimeter" | [p.464–467] |
| T10 | Hot-flow forms: Norton–Hoff and Zener–Hollomon sinh (no constants) | See H2a/H2b in §3.2 | [p.434] |
| T11 | Thermal: ρ(Al) = 2700 kg/m³ | ⚠ [SH] E11 uses 2800 kg/m³. 2700 is the usual value for Al (general knowledge); prefer it unless the alloy density is known | [p.388; SH p.56] |

**Metallurgical speed limits [TOT Ch.8].**
- Too high a bearing temperature (billet preheat or speed) partially melts Mg₂Si particles → surface cracking ("hot tearing") [p.403].
- For AA6060 the billet should be prepared (homogenise, controlled cooling, preheat) so that Mg and Si are fully in solution before leaving the die. If eutectic remains, its melting point of **585 °C** is the maximum temperature; otherwise the solidus is [p.429, Fig. 29].
- A hot container makes the outer billet layer flow more easily, so oxidised or segregated surface material can flow into the profile [p.402, 425].
- Higher-strength alloys extrude more slowly, need thicker minimum walls and wear dies more [Fig. 18 p.413].
- 6xxx alloys make up ~80 % of all extruded products; 6082-T6 TS ≈ 340 MPa [p.413].
- The limit of extrudability for thin walls is reached when the **self-stabilisation** of bearing flow fails: buckling in compression, thinning or cracking in tension, or die deflection that works against stabilisation [p.475].

### 8.3 Microstructure during extrusion

- Strain-rate and hydrostatic-stress gradients are steep. The main strain-rate line M1 (die entry) controls the product microstructure via the Z it imposes. M2 (container shear) shortens as the ram advances [SH §2.3.4 p.46–47].
- In unlubricated direct extrusion, strain accumulates at the border streamline. Slow loading along M2 favours **static recrystallisation at the periphery** after passing M1. This is the mechanistic origin of peripheral coarse grain (PCG) heterogeneity [SH p.47].
- PCG concentrates at the **back end** of the extrudate and lowers longitudinal tensile strength by **10–15 %** [POL §3.1.5 p.108]. In strong alloys (2024, 7075) the heavily sheared outer layer becomes a coarse-grained low-strength zone after heat treatment [SH p.20].
- Avoid unnecessarily high temperatures and long solution treatments for extrusions and forgings made from extruded stock: non-uniform strain makes them prone to local grain growth [POL §3.1.6 p.109].
- Large surface recrystallised grains are slightly cathodic to the unrecrystallised core, so machining that exposes the core can trigger preferential attack [POL §2.4 p.76–77].
- Hydrostatic-stress gradient at the billet rear drives flow towards the axis, causing the **piping** defect. It is more likely in direct extrusion [SH p.47].

**Structure after extrusion and the recrystallised shell (PCG) — [SH] full-text pass, 2026-10-12.**
- **Ideal structure:** "fibrous" — the cast grains elongated with an aspect ratio roughly equal to R, recovered but not statically recrystallised. Incorrect conditions give a recrystallised surface layer of **large grains** with "very poor fracture toughness and corrosion properties", the least desirable structure (7075, Fig. 3.14) [SH §3.5.1 p.115].
- **Two as-extruded structure types** after press quench [SH §4.9.1 p.160–161]: (1) fibrous core with heavily sheared peripheral grains, normally at low extrusion temperature; (2) fibrous core inside a **shell of recrystallised grains**. Indirect extrusion recrystallises "to a much smaller extent". Above ~350 °C the surface was predominantly recrystallised; below 350 °C the surface RX was "very fine and equiaxed" [p.161]. Near **re-entrant corners the recrystallised shell is thicker**, in proportion to the standard stress-concentration factors of the geometry [p.161].
- **Origin of the shell:** surface layers receive much higher strains than the core, which gives a driving force for RX that the core lacks; nucleation probably at subgrain boundaries by rapid subgrain coalescence, assisted by second-phase particles in commercial alloys [SH §4.11.3 p.183]. In unlubricated direct extrusion the billet surface is held by the container, and the surface of the extrudate comes from the shear zones; in the last ~10 % of the stroke a heavily deformed outer ring reaches almost to the middle of the bar [SH §4.3 p.137–138]. Shear at the container interface extends over about 40–60 µm [p.148].
- **After solution treatment (2024 example):** low-temperature extrudates recrystallised right through to the core, while high-temperature extrudates kept an unrecrystallised core with grown subgrains and a thin PFZ at the subgrain boundaries [SH p.161–165]. High-temperature extrusion therefore gave better T6 toughness and ~16 % higher T6 proof stress and UTS in 2014 [SH §4.10 p.172–176].
- **Kinetics:** RX fraction is lower for 2024 than for 5xxx and can be made zero (high temperature, low ram speed); shape factor strongly raises it; indirect extrusion gives a much better solution-treated structure [SH p.166–169, Figs. 4.29–4.33]. 6xxx kinetics are reported closer to 2024 than to 5xxx, with more RX at *lower* temperature because the highly deformed outer layers are reheated by the interior before the quench [p.167].
- **6xxx surface layer:** a transition from lamellar grains to broken-up grains about 200 µm below the surface, and a shear texture near (113)[332] in the surface layer vs a rolling-type texture in the bulk (AA6082, Aukrust et al.) [SH §6.6 p.302].
- **Back-end defect (6xxx):** the billet skin (nominally 100–200 µm deep, with coarse Fe-rich intermetallics and Mg/Si-rich inverse segregate) collects at the pad and flows in after ~70 % of the billet; 5–20 % discard is typical. A billet–container temperature difference of 25–50 °C keeps the skin in the discard [SH §6.7.2 p.307–311]. Surface defects deeper than ~200 µm can pass into the product anywhere along the length [p.311].
- **Relevance to the slug route (inference).**
  - Back extrusion of a slug also shears the surface layers far more than the wall core, so by the same mechanism as the recrystallised shell, the can surfaces carry the highest stored energy. The 220 °C/10 min bake is too cold for static RX (§6), so this matters only if the wall is reheated harder.
  - Unlike billet extrusion, impact extrusion has no discard to collect the original surface (general knowledge). Oxide (MgO from the slug anneal) and any segregated skin from the caster therefore end up in the most strained layer of the can. [SH] reports that billet-surface defects deeper than ~200 µm escape the discard [p.311]; for slugs there is no such buffer, which raises the importance of strip surface quality and slug-anneal oxide control (ch. 14).

### 8.4 6xxx and quench sensitivity

- Balanced Mg+Si 0.8–1.2 % alloys (6063) extrude easily and are **press-quenched** with water spray or trough; thin sections < 3 mm can be air-cooled. Ageing at 160–190 °C. 6063-T6: 215 / 245 MPa [POL §3.4.3 p.138–140].
- Mg+Si > 1.4 %: quench-sensitive, so separate solution treatment and water quench [POL p.140].
- Low-Mg 6060 (Al-0.35Mg-0.5Si) gives properties comparable to 6063 at **up to 20 % higher extrusion speed** [POL p.141].
- Delay between quench and ageing:
  - > 1 % Mg₂Si: 24 h delay → up to −10 % tensile properties;
  - < 0.9 % Mg₂Si: properties enhanced;
  - ~0.25 % Cu reduces the penalty [POL p.141–142].
- Quench sensitivity [POL §3.1.6 p.112–113]:
  - critical range **290–400 °C**;
  - worse for concentrated alloys;
  - worse with dispersoids that nucleate coarse precipitates (Mg₂Si needles on Mn-bearing particles, Fig. 3.14);
  - ranking: Al₁₂Mg₂Cr (worst) > Al₆Mn > Al₃Zr (least) [POL p.112].
  - Cr (6151) and Mn (6351) refine grain and inhibit recrystallisation during solution treatment [POL p.141].
- **6xxx homogenisation vs extrudability (G2, closed 2026-10-12 from [SH Ch. 4–6]).**
  - Mg₂Si solubility: 1.85 % at 595 °C, 1.08 % at 500 °C, 0.097 % at 200 °C (alloy with Mg:Si = 1.73:1) [SH §4.12 p.187]. Balanced alloy: Si = Mg/1.7038; e.g. 0.4 Mg + 0.38 Si → 0.63 % Mg₂Si + 0.15 % excess Si [SH §6.1 p.255].
  - β → α Fe-phase transformation complete after 6 h at 565 °C; Mn accelerates it; Mg₂Si dissolves above 465 °C in ~2 h, so the Fe phase sets the soak [p.256–257] (§3.5a).
  - **Cooling after homogenisation:** 38 °C/h gives ~2 µm Mg₂Si ("quite unacceptable": pick-up, poor properties); 315 °C/h gives 0.25 µm. Usual practice **575 °C/6 h, then 150 °C/h to 250 °C, then air** [p.257; repeated p.261]. Older recommendation for 6063: 6 h at 575 °C, forced cooling between 480 and 250 °C [SH p.189].
  - **Extrudability falls with Mg and Si in solid solution** (more alloy or faster cooling) and also with coarse Mg₂Si (slow cooling) [p.258–259]. Mg raises the maximum extrusion pressure "regardless of silicon content"; excess Si lowers extrudability less than Mg; Si is a good strengthener up to ~0.4 %; Fe has negligible effect on extrudability and strength but harms surface finish; Cu < 0.1 % has little effect [p.256].
  - **Industrial trial (Reiso):** air-cooled billets tear by eutectic melting of Mg₂Si at low preheat, with a sharp speed increase above a transition billet temperature. Water-quenched billets showed no eutectic melting and extruded **≈ 60–90 % faster** below that transition, at higher pressure, but lost strength after ageing through higher quench sensitivity. Recommendation: cool as fast as possible short of water quenching; preheat just above the transition temperature [p.260–261].
  - Avoid holding billets at **330–360 °C** during reheating (coarse Mg₂Si); after such a delay re-homogenise or re-solutionise at 530 °C [SH §6.7.1 p.306–307]. Minimum exit temperature for 6063 ≈ 495 °C (probe at the die tunnel end) for full ageing response [p.306].
  - **Press-quench economics and limits [SH §4.12 p.186–198]:** most 6xxx are press quenched; the critical quench region is 450–250 °C with the nose near 350 °C [p.193]. Heat-transfer coefficients: still air 10, forced air 30–120, water 200–40,000 W m⁻² K⁻¹; with water the coefficient rises from ~2000 to 40,000 when the vapour film breaks down [p.195]. Plastic deformation speeds solute dissolution: a tensile stress of only 1 N mm⁻² lowered the dissolution activation energy from 268 to 153 kJ mol⁻¹ in an Al-Cu alloy [p.190]. Cr, Mn and Zr dispersoids raise quench sensitivity (Cr most); Mn is needed for transgranular fracture and toughness in Al-0.8Mg-0.65Si (Table 4.5) [p.191].
  - Low-temperature homogenisation of Mn-bearing 6351/6082 gives a dense dispersoid: higher flow stress, less RX (less coarse grain in forging stock) but higher quench sensitivity [SH p.265].
- **Relevance to the slug route, T11 (Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26) (derived and inference).**
  - Stoichiometry: Mg₂Si potential = 0.26 + 0.26/1.7038 = **0.41 %**, leaving 0.23 % Si in excess before any Si is bound in α-Al(Fe,Mn)Si (derived from [SH p.255]).
  - 0.41 % Mg₂Si lies between the solubilities at 200 °C (0.097 %) and 500 °C (1.08 %) [SH p.187]. The strip leaves the caster at ≈ 500 °C and the hot mill at ≈ 380 °C, then is water quenched, so much of the Mg and Si is retained in solution, as CLAUDE.md states. Per [SH p.258], Mg and Si in solution **raise the flow stress**; this applies to the hot mill and, after the slug anneal, to impact-extrusion force if the anneal leaves them in solution.
  - High excess Si accelerates and high Mg suppresses the α-transformation (§3.5a). T11's excess Si favours α-Al(Fe,Mn)Si over Al₆(Fe,Mn) wherever there is time for it, which on this route is only the slug anneal.

### 8.4a Limit diagrams and productivity (G2, closed 2026-10-12) [SH §4.13 p.198–202; §5.10 p.238–250; §6.7.1 p.303–306]

- **Concept (Hirst & Ursell 1958):** a pressure-limit line (press capacity) and a temperature-limit line (originally incipient melting, adiabatic ΔT vs R) bound the operating area [p.198]. Sheppard & Raybould added constant-strain-rate curves and structure loci; Stenger used ram speed vs temperature at fixed R [p.199–200].
- **Construction:** flow stress from torsion with the test's temperature rise corrected [p.200]; the pressure line must include the **breakthrough increment Δp** (H6). Leaving it out over-states the maximum R by almost 40 % [p.243, Fig. 5.26]. "The assumption that a temperature-limiting line is the curve at which incipient melting occurs is false": the real limit is cosmetic or structural (pick-up, tearing) [p.200].
- **Equations [SH eq. 4.14–4.15 p.200–202]:** the pressure limit solved for T or V_R uses the strain-rate factor K₁ = (0.171 + 1.86 ln R)·tan(38.7 + 6.9 ln R); the surface limit has the form ln(6K₁V_B/D_B) + ΔH/GT = a/b + ln A. Sheppard replaces K₁ by the regression **K₁ ≈ 5.62 ln R − 5.6** (r = 0.998). ⚠ Derived check: that regression deviates from the exact K₁ by up to ~18 % over R = 5–100 (−8 % at R = 5, +17 % at R = 10, +10 % at R = 30, ≈ 0 at R = 50, −18 % at R = 100); use the exact K₁ in code.
- **Temperature control limits productivity:** in an AA2014 example, ±20 °C billet-temperature control cut the achievable R to about 60 and 45 at the two ram speeds shown [p.240]. At fixed R, ±20 °C control costs about 10 % of the optimum ram speed and ±50 °C about 50 % [p.241].
- **Structure on the diagram:** subgrain-size lines follow from d⁻¹ = a + b·ln(Z/A) (H9), and property lines such as an optimum subgrain size for toughness (e.g. d = 2 µm) can be drawn [p.241–243, Fig. 5.25].
- **6xxx:** a Stenger-type diagram suggests only press capacity limits 6063, which "clearly cannot be correct". Bridge/porthole shape factors and the need to dissolve Mg₂Si (extrude at 450–475 °C) shrink the working area [p.243–244]. Alcan's schematic 6063 window has three limits: surface (pick-up, tearing; the product surface temperature rises roughly with log of exit speed), breakthrough pressure, and minimum exit temperature for Mg₂Si dissolution [SH §6.7.1 p.303–306]. Diluting the alloy (6063 → 6060) raises the pick-up speed by raising the solidus and lowering the deformation work [p.305].
- **Homogenisation and extrudability (7xxx):** for 7075, heating at 15 °C/min and cooling at 10 °C/min gave the widest extrusion window of four homogenisation variants; for 7049, slow cooling widened the window; for 7150 the heating rate mattered more than the cooling rate [p.244–245]. Slowly cooled billets had lower flow stress and higher productivity; maximum productivity falls as R rises [p.247–249].
- **Relevance to the slug route (inference).** A limit diagram for the *slug line* would have the same structure: a press-force limit (scales with σ̄ of the annealed slug, §8.6), a surface limit (pick-up, galling and lubricant breakdown in impact extrusion rather than tearing) and a structure limit (grain size and earing from the anneal). Sheppard's point that ±20–50 °C temperature scatter costs 10–50 % of the speed window suggests that slug-anneal temperature uniformity deserves the same attention as its mean value.

### 8.5 Heat-exchanger multi-port tube (AA3102) — process and post-braze data [WIL]

| Item | Value | Ref |
|---|---|---|
| AA3102 composition used | Si 0.07, Fe 0.41, Mn 0.24 wt % | [WIL Table 2 p.18] |
| Tube | 12.0 × 1.30 mm, Ø0.76 mm ports, 0.30–0.40 mm walls | [WIL Fig. 1/7 p.11, 19] |
| Billet / container | Ø102 × 203 mm / Ø106 mm | [WIL Table 3 p.19] |
| Billet / tooling temperature | 495–503 °C / 450 °C | [WIL Tables 3, 5] |
| Ram / exit speed | 0.7 mm/s / ~34 m/min; R = 817 | [WIL Table 3] |
| Peak specific pressure | 445–460 MPa (3102); 651–653 MPa (Al-0.19Sc-0.05Zr, +44 %) | [WIL Table 5 p.38] |
| Exit temperature, 0.3 m after platen | 499–529 °C (3102); 504–517 °C (AlScZr) | [WIL Table 5] |
| Billet homogenisation (AlScZr) | 400 °C/8 h or 450 °C/4 h; heat 50 °C/h, cool 350 °C/h. No measurable effect on extrusion or post-braze properties | [WIL p.18–19, 43] |
| As-extruded structure | 3102: fine, equiaxed, **recrystallised**. AlScZr: unrecrystallised, heavily deformed, some fine recrystallised grains at edges | [WIL §5.2 p.39–40] |
| Sizing/straightening strain | 3–7 % thickness reduction typical. At ~3 % reduction, post-braze strength falls by ~22 % (coarse grains in inner walls) | [WIL §1.1 p.13] |
| Braze simulation | 600 °C, 2 min, air cool. Inner webs fail first | [WIL §3.2 p.21; p.12] |
| Burst pressure, 3102 | 0 % red., no braze 38 MPa; brazed 39 MPa; 5 % red., no braze 48 MPa; 5 % red. + braze 39 MPa | [WIL Table 6 p.50] |
| Burst pressure, AlScZr | 0 % 50 MPa; brazed 39 MPa; 5 % red. 60–63 MPa; 5 % red. + braze 42 MPa. Braze then 288 °C/8 h age: YS 154 vs 60 MPa (brazed AlScZr) vs 39 MPa (brazed 3102) | [WIL Table 6; §5.3 p.48] |
| Design pressure context | R744 (CO₂) ~13 MPa vs R134a ~2 MPa | [WIL p.10] |

### 8.6 Design levers (extrusion)

- **Extrudability ↔ alloy.** Every MPa of σ̄ at ~500 °C costs ln-R-scaled pressure (E4) and adds heat (E8). Dilute 3102 runs at ~27 MPa effective σ̄; AlScZr needs ~39 MPa (derived, §3.4). For R ≈ 800 MPE tubes, a strengthening addition must be weighed against press capacity and exit-temperature limits (inference).
- **Post-braze grain size in tubes** is set by (i) as-extruded state (recrystallised vs fibrous) and (ii) post-extrusion strain (sizing 3–7 %). Small strains → few nuclei → giant grains after braze. Options (inference from [WIL]):
  1. minimise or homogenise sizing strain;
  2. keep the structure unrecrystallised with stable dispersoids (Sc/Zr), recognising Al₃Sc dissolution near 595 °C [WIL p.41];
  3. use precipitation (post-braze ageing) for strength.
- **6xxx speed lever:** reduce Mg towards the 1:1 Mg:Si cluster stoichiometry (6060 concept), +20 % speed [POL p.141]. Prefer Zr or Mn over Cr where quench sensitivity matters [POL p.112].
- **Indirect extrusion** is the process lever against PCG and surface-temperature-limited speed in hard alloys [SH p.11–12, 20–21].
- **Taper heating / isothermal extrusion:** induction taper or rear spray cooling offsets the late-stroke temperature rise [SH p.19, 49]. Real-time integral-profile control of ram speed for constant exit temperature [SH p.55].
- **Alloy strength vs productivity:** stronger alloys run slower, need thicker walls and wear dies faster. Speed is limited both by flow resistance and by low-melting phases [TOT Ch.8 Fig. 18 p.413–414].

**Relevance to the slug route.** Impact extrusion of slugs is *cold* extrusion. [TOT Ch.8] treats hot extrusion of profiles, so only its mechanics transfer (inference unless cited):
1. F = a + b·ln R is a general upper-bound result, confirmed "for various metals" [T1, p.447]. For a fixed can geometry (fixed R and die), press force scales with the slug flow stress. A stronger slug alloy raises the force about in proportion, and the a-term (geometry and friction) does not change. This is the quantitative core of the strength-vs-press-force trade-off in the design goal.
2. Stored energy of cold work ≤ ~5 % [T7, p.459], so ≈ 95 % of the impact-extrusion work becomes heat. Impact extrusion is close to adiabatic, consistent with ch. 10 §2.7.
3. Sticking-zone strain rates of 10³–10⁴ s⁻¹ [T6] show the range a constitutive law for the can wall must cover. Rate sensitivity is low in the cold regime (ch. 10 §2.7), so strain hardening dominates; use Hollomon K, n (Table 5-1) rather than the sinh law.
4. Retrieval lead: [TOT Ch.8 ref. 68] Furu, Pedersen & Abtahi, "Microstructurally based modeling applied to cold extrusion of aluminum", Proc. 6th Int. Al Extrusion Technology Seminar 1996, Vol. I, pp. 341–347 (citation only, not read).
5. **[SH] full-text additions.** The axisymmetric upper bound p/σ̄ = 0.171 + 1.8594 ln R (E4) is the same structure as F = a + b ln R. Sheppard states it is valid for rod extrusion up to R = 100 [p.144]; check the can's equivalent R against that before using his constants. Section complexity raises pressure through the peripheral ratio λ (E13); a thin-walled can is a high-λ "tube" geometry. Sheppard's hot-working constants (Table 3-1) do **not** apply at room temperature; for the slug, use room-temperature flow curves (Table 5-1, measured slug curves).
6. **As-extruded properties vs Z (5083, direct extrusion, negligible RX) [SH §4.10 eq. 4.11 p.170–171]:** σ_proof = 323 − 5.25·ln Z, σ_UTS = 498 − 5.25·ln Z, elongation (%) = −40 + 2.29·ln Z, fitted over ln Z_i ≈ 25–34 (initial-condition Z) and checked on the page image and Fig. 4.34(a). Sheppard notes that this substructural strengthening "would be more important in 1XXX, 3XXX and 5XXX series alloys", because heat treatment removes much of it in the heat-treatable alloys [p.171]. Relevance to the slug route (inference): the slug is fully annealed before impact extrusion, so hot-band substructure does not survive into the can; this lever applies only if a recovery (not RX) anneal is ever used.

### 8.7 Pitfalls (extrusion)

- **Surface tearing.** Starts at edges and corners, where the temperature rise is about double, then spreads over the surface as exit temperature or speed rises [SH §2.5.2 p.52, Fig. 2.10].
- Lubrication: too much or too little graphite grease on die and dummy block causes surface defects not seen in normal unlubricated practice [SH p.10].
- Back-end defects: oxide and dross pipe; discard must be long enough [SH p.10].
- PCG at the back end [POL p.108]. Coarse peripheral zone in 2024/7075 [SH p.20].
- Blisters in solution treatment come from humid atmosphere, hydrogen, unhealed porosity or overheating [POL §3.1.6 p.110–111].

---

## 9. Formability metrics and forming basics

- **n-value:** Tables 5-1/5-2.
- **r-value** = width strain / thickness strain. r > 1 resists thinning; high r helps deep drawing [POL §2.1.3 p.37; §2.1.4 p.39].
- **r̄, Δr and LDR [TOT Ch.18 §5.2 p.851–853]** (gap G7 partly filled):
  - r̄ = (r₀ + 2r₄₅ + r₉₀)/4 is "a good measure of the drawability": higher r̄ increases flange flow, reduces wall thinning and delays necking.
  - **ln(LDR) = η·√((r̄ + 1)/2)**, with efficiency η = 0.74–0.79 depending on lubrication, blank-holder force, thickness and die radius [eq. 8 p.852].
  - Δr has "a minor but important effect": more earing and trimming, less draw depth. High r̄ and low Δr also reduce wrinkling. r has "very little effect" on stretchability.
  - Aluminium sheet typically has lower normal anisotropy than steel [p.842]. The steel cases in the table below sit at r̄ = 1.0–1.9.
- **Table 9-1 — sheet properties [TOT Ch.18 Table 4 p.853, source its Ref. 46; Ch.18 Table 7 p.874]:**

  | Material | E (GPa) | YS (MPa) | UTS (MPa) | e_u / e_t (%) | n | r̄ | Δr (as printed, "planar anisotropy") | m (rate sens.) |
  |---|---|---|---|---|---|---|---|---|
  | **3003-O** | 69 | 48 | 110 | 23 / 33 | 0.24 | **0.6** | 0.2 | 0.005 |
  | 6009-T4 | 69 | 131 | 234 | 21 / 26 | 0.23 | 0.6 | 0.1 | 0.002 |
  | 6111-T4 (FE input, 1 mm) | 70 | — | — | — | 0.238 (K = 533 MPa) | 0.59 | — | — |
  | AK drawing-quality steel (reference) | 207 | 193 | 296 | 24 / 43 | 0.22 | 1.8 | 0.7 | 0.013 |

  - 3003-O: K and n agree with Table 5-1 (n 0.24 vs 0.242). r̄ = 0.6 gives **LDR ≈ 1.94–2.03** for η = 0.74–0.79 **(derived)**.
  - The Δr column header prints "Planar Anisotropy r". It is read as Δr.
- **Relevance to the slug route (inference).** Back-extrusion of slugs is not a deep-drawing operation, so LDR does not apply directly. But r̄ ≈ 0.6 and Δr ≈ 0.1–0.2 for O-temper 3003/6xxx sheet show the anisotropy level to expect in annealed 3xxx. Δr of the annealed slug strip is a plausible, measurable proxy for rim-height variation of the can (§7.3); check it against measured rim profiles. No r-values exist for 3102/3207 or for the slug O-temper in any source read.
- **FLC/FLD:** grid-strain measurement of the boundary between safe and necked/failed strain states [POL §2.1.3 p.38, Fig. 2.8]:
  - positive minor strain = stretching, from uniaxial to equi-biaxial;
  - negative minor strain = drawing (tension–compression, e.g. cup walls).
  - Steel normally out-forms Al sheet.
  - 5052 forms better in O than H24, but **3004 forms better strain-hardened** (canstock).
- **Hydrostatic pressure controls formability:**
  - formability depends on the mean pressure p_m = (σ₁+σ₂+σ₃)/3 [MFH §2.2.4 p.31];
  - EC-Al elongation is ~30 % in tension, ~400 % in cold rolling, and "several 1000 %" in extrusion [SH §2.1 p.24];
  - extrusion is triaxially compressive; ram stress ≥ 2σ̄ before friction if the radial stress is 50 % of the axial [SH §2.1 p.26].
- **Process classification (DIN 8582–8587):** compressive (rolling, forging, extrusion), tensile + compressive (drawing, deep drawing, ironing, spinning, flanging), tensile (stretching, stretch forming, expanding), bending (die, roll, swivel), shear [MFH §2.1 p.6–19]. Forming forces [MFH §2.2.3 p.28–30]:
  - direct (upsetting, rolling): F = A·k_w;
  - indirect (drawing, deep drawing): F = A·k_fm·φ_g/η_F.
- Industrial formability benchmarks [MM slides 11–12]: FLD₀ 23.4 (5182-O) to 33.7 (MMHF-T4); LDR 1.88–2.18 (vendor data).
- Lüders and PLC stretcher-strain markings: avoid with strain-hardened stock or forming above 150 °C [POL p.40–41]. Orange peel comes from coarse grains [POL p.43].

**Design levers (inference).** For deep-drawn fin collars and foil containers, aim for high n and r and low Δr (balanced cube/rolling texture, §7), and a fine, uniform recrystallised grain (enough final cold reduction before anneal, §5.5). For tube stock that sees small sizing strains before braze, prioritise grain-size stability over n and r.

---

## 10. Model-ready constitutive and process parameters

| Group | Parameter | Value | Validity / note | Ref |
|---|---|---|---|---|
| Cold flow | Hollomon K, n (O-temper) | 1100: 146 MPa, 0.242 · 3003: 188, 0.242 · 6061: 224, 0.209 · 5052: 281, 0.198 · 5454: 340, 0.189 · 5086: 368, 0.193 · 5456: 479, 0.178 | RT tensile; σ = K(ε₀+ε)ⁿ for pre-strained material | [TOT Ch.3 p.100; POL p.36] |
| Cold flow | Rolling YS law | YS = σ₁·εⁿ, ε = ln(t_i/t_f); σ₁ = YS at ε = 1 (63 % CR) | per alloy (Alcoa) | [TOT Ch.3 p.98–99] |
| Cold flow | Solute K and Doherty H | Cu 1.00 / 3.38 GPa; Mg 0.37 / 1.52; Si — / 1.56; Mn — / 1.03; Zn 0.071 / 0.27 | H = (k_alloy − k_Al)/(x_solute)^(2/3), x = atomic fraction, k = YS at ε = 1 (corrected after full-text pass) | [TOT Ch.3 Table 2, eq. 9, p.99–100] |
| Cold flow | Cryogenic gain | +~40 % strength at −196 °C (1100) | | [POL p.36] |
| Substructure | σ = σ₀ + k₁d⁻ᵐ | m = 1 (cells) → 0.5 (subgrains) | | [POL p.36–37] |
| Physical | SFE (Al) | ~170 mJ/m² | | [POL p.36] |
| Hot flow | Z | ε̇·exp(Q/RT); G = R = 8.314 J mol⁻¹ K⁻¹, T in K, ε̇ = mean equivalent strain rate | Z values are only comparable with the same Q (§1) | [SH eq. 2.4 p.28, p.128; TOT Ch.7 eq. 3 p.359] |
| Hot flow | Flow law (use this) | **σ̄ = (1/α)·arcsinh[(Z/A)^{1/n}]**, Z = A[sinh(ασ̄)]ⁿ (verified on page images; eq. 4.1 p.128 misprints "−1") | steady state; power-law regime ασ̄ < 0.8, exponential > 1.2 | [SH eq. 2.4 p.28; eq. 4.1 p.128; p.133] |
| Hot flow | Other forms | [TOT] σ̄ = (1/α)·arcsinh(Z/A) (no 1/n: most likely a misprint); Norton–Hoff σ̄ = Kε̄ⁿε̄̇ᵐexp(β/T), β = Q/R | forms only, no constants in [TOT] | [TOT Ch.8 eq. 10–11 p.434] |
| Hot flow | Hot/cold working limits (Al) | hot > 0.6 T_m ("above 300 °C"); cold < 100 °C | definitions | [TOT Ch.7 p.354, 362] |
| Hot flow | α (MPa⁻¹), n, Q (kJ/mol), ln A (A in s⁻¹) — **1050** | 0.037, 3.84, 156.888, 26.69 | All rows: homogenised DC material, hot torsion (temperature-rise corrected); no per-alloy range printed — plotted envelope ≈ 230–530 °C (500–800 K; 450–850 K at 50 s⁻¹), ln Z ≈ 20–40; steady state; not for cold work; use each row as a set | [SH Table 4.1 p.132; cloudpart4 w.txt l. 6757–6793] |
| Hot flow | same — **1100** | 0.045, 5.66, 158.300, 24.67 | as above | [SH Table 4.1] |
| Hot flow | same — **3003** | 0.0316, 4.45, 164.800, 26.9 | as above | [SH Table 4.1] |
| Hot flow | same — **3004** | 0.0344, 3.6, 193.850, 28.21 | as above. ⚠ Q differs from the Q ≈ 156–160 implied by the [TOT] AA3104 cube/PSN line; do not mix | [SH Table 4.1] |
| Hot flow | same — **3005** | 0.0323, 4.96, 183.100, 29.87 | as above | [SH Table 4.1] |
| Hot flow | same — **3105** | 0.0248, 4.83, 179.300, 29.98 | as above | [SH Table 4.1] |
| Hot flow | same — **5005 / 5052 / 5083 / 5182 / 5456** | 0.029, 5.8, 183.576, 26.65 / 0.016, 5.24, 155.167, 24.47 / 0.015, 4.99, 171.400, 23.11 / 0.062, 1.35, 174.200, 22.48 / 0.0191, 3.2, 161.177, 23.5 | as above | [SH Table 4.1] |
| Hot flow | same — **6061 / 6063 / 6082 / 6105** | 0.045, 3.55, 145.0, 19.3 / 0.04, 5.385, 141.55, 22.5 / 0.045, 2.976, 153.0, 19.29 / 0.045, 3.502, 145.0, 20.51 | as above | [SH Table 4.1] |
| Hot flow | same — **7075** (5 homogenisation variants) / **7050** | H1 (24 h soak) 0.0141, 5.41, 129.4, 20.75 … H4 (fast heat, fast cool) 0.01, 8.5, 156.325, 27.14 (full list §3.3) / 0.0269, 2.86, 151.5, 22.85 | homogenisation heating/cooling rate changes the constants | [SH Table 4.1] |
| Hot flow | 7075 temperature-corrected torsion fit | Z = ε̇·exp(155100/GT) = 1.7×10¹²[sinh(ασ)]^6.4 | α not printed with it | [SH p.131] |
| Hot flow | Q of self-diffusion (Al) | 153 kJ mol⁻¹ [SH]; McQueen 152 kJ mol⁻¹ (some Al-Mg) | ⚠ the earlier general-knowledge anchor 142 kJ/mol differs | [SH p.135] |
| Hot flow | σ̄ for the slug-route hot mill (380–500 °C, 1–50 s⁻¹) | 1100: 20–49 MPa; 3003: 22–75; 3105: 25–87; 3004: 38–112; 6063: 21–52 (full table §3.3a); T11 bracket ≈ 20–25 (500 °C, 1 s⁻¹) to ≈ 49–87 MPa (380 °C, 50 s⁻¹), upper half expected for unhomogenised strip | **(derived)** from Table 4.1; k = σ̄/√3 for Sims | §3.3a |
| Hot flow | Subgrain size vs Z | d⁻ᵐ = x + y ln Z; only fit: AA2014 d⁻¹ ≈ 0.15·ln Z_i − 3.5 (µm⁻¹ read; printed with a misprint) over ln Z_c 26.8–34.6 | **no 3xxx constants**; substructure lags fast Z changes | [SH eq. 4.10 p.156; p.184–185] |
| Hot flow | Static RX t₀.₅ (5xxx) | 5056: 2.31×10⁻¹⁰ d₀^1.58 ε̄^−1.9 Z^−0.35 exp(212000/RT_ann); 5083: 4.5×10⁻¹⁰ d₀^2.45 ε̄^−1.97 Z^−0.58 exp(183000/RT_ann) | units not stated; empirical | [SH p.116–117] |
| Hot flow | DRX | only AA5456 reported among commercial alloys; others dynamically recover | | [SH p.135, 165, 167] |
| Hot flow / texture | AA3104 cube/PSN boundary | Z* = 3×10¹⁴ s⁻¹ (cube below, PSN above); implied Q ≈ 156–160 kJ/mol **(derived from the figure)** | deformation 150–350 °C, 10⁻³–10 s⁻¹, then RX; one constitution only | [TOT Ch.7 Fig. 4 p.357] |
| Hot flow | σ̄ AA3102, ~500 °C, MPE extrusion | ≈ 27–28 MPa (36 MPa if no friction term) | back-calculated **(derived)** from E4 + WIL data | [WIL; SH] |
| Hot flow | σ̄ Al-0.19Sc-0.05Zr, same | ≈ 39 MPa (+44 %) | **(derived)** | [WIL; SH] |
| Extrusion | Pressure | P = σ̄[0.171 + 1.86 ln R + 4mL_B/(√3 D_B)]; frictionless p/σ̄ = 0.171 + 1.8594 ln R | upper bound, **verified**; valid for rod extrusion up to R = 100; m = 0.8–0.9 | [SH p.36; eq. 4.3–4.4 p.144] |
| Extrusion | Pressure with constitutive constants | p = (1/αn)[A + B ln R + C ln(Z/A) + D(L_B/D_B) ln(Z/A)]; constants for 10 alloys (e.g. 1100: −3.9056, 3.849, 1.728, 0.0179, αn 0.192) | laboratory fit; ⚠ 1.2–1.8× (5xxx, 7075) and ≈ 4.3× (1100) below E4 + H6 at R = 30 **(derived)**; 1100 row not usable without recalibration | [SH Table 4.2 p.146; ww.txt l. 253–265] |
| Extrusion | Homogeneous lower bound | p = σ̄ ln R (−~60 %) | | [SH p.29] |
| Extrusion | Friction factor | m = 0.85 (design); 0.88 measured | sticking regime | [SH p.48–49] |
| Extrusion | Coulomb μ | 1100: 0.075–0.092 · 2014: 0.048–0.098 (300–475 °C) | R = 30 | [SH Table 2.2] |
| Extrusion | Shear-layer thickness | 40–100 µm | | [SH p.49] |
| Extrusion | Deformation-zone geometry | δ = 38.7 + 6.9 ln R (°); X_D = 0.35 D_B(1 + 0.15√R − 0.0145R) | **verified**; δ normally assumed 45° | [SH eq. 2.28–2.29 p.57] |
| Extrusion | Breakthrough increment | **Δp = 6.62 + 0.921·ln(Z/A)/(αn)** (MPa) | **verified** (corrected after full-text pass: the 1/(αn) factor was missing); fitted to 2xxx, 5456, Al-Cu over (1/αn)ln(Z/A) ≈ 0–150; leaving Δp out of a limit diagram overstates max R by almost 40 % | [SH eq. 2.27 p.57; eq. 4.5 p.144; Fig. 4.11 p.145; p.243] |
| Extrusion | Strain rate | Feltham ε̇ = 6D_B²V_R ln R/(D_B³ − D_E³) (H3, verified) or modified (H4: printed with D_B³/(D_B² − D_E²), dimensionally inconsistent; use D_B²/(D_B³ − D_E³)) | FEM: parabolic in ln R | [SH p.28, 36–37, 44, 142] |
| Extrusion | Surface-limit criterion | 5456: ln(Z_i/A) ≤ 6.35×10²⁰/T^7.06; 2024 shapes: (1/n)ln(λ²Z_i/A) ≤ 2.113×10⁹/T^2.866 (direct), ≤ 2.4×10¹⁰/T^3.57 (indirect); T in K | alloy-specific | [SH p.154] |
| Extrusion | Relative extrudability (6063 = 100) | 1000 77; 1100 86; 3005 106; 3003 112; 3105 126; 6061 151; 5005 154; 3004 180; 6082 197; 5052 229; 5083 281; 7075 316 (full list §3.6) | based on hot flow stress | [SH Table 5.4 p.239] |
| Extrusion | Temperature-control cost | ±20 °C → ~10 % lower optimum ram speed; ±50 °C → ~50 % | AA2014 limit diagram | [SH p.241] |
| Extrusion | Properties vs Z (5083, F temper) | σ_proof = 323 − 5.25 ln Z; UTS = 498 − 5.25 ln Z; El % = −40 + 2.29 ln Z | ln Z_i ≈ 25–34; negligible RX | [SH eq. 4.11 p.171] |
| Extrusion | Indirect vs direct load | −25 to −50 % | | [SH p.11–12] |
| Extrusion | Force law | F = a + b·ln R (a, b depend on section geometry) | upper bound; experimentally confirmed | [TOT Ch.8 p.447] |
| Extrusion | Lower bound | p = 5k(R − 1)/R | frictionless, R ≥ 3 | [TOT Ch.8 p.444] |
| Extrusion | Strain-rate range | ~10⁴ s⁻¹ (die/bearing entry shear) to ~0.1 s⁻¹ (bearing-channel centre); 10³–10⁴ s⁻¹ in the bearing sticking zone | | [TOT Ch.8 p.429–431, 474] |
| Extrusion | Plant window (6xxx) | billet 450–470 °C; exit 550–600 °C; R 20–80; 16 MN/Ø178 mm (643 MPa), 22 MN/Ø208 mm (647 MPa) | | [TOT Ch.8 p.388, 393] |
| Extrusion | Bearing-channel friction (example) | sticking τ = k = 30 MPa over the first 4 mm, then linear to 5 MPa at the outlet; inlet σ_x ≈ −190 MPa | illustrative slab model | [TOT Ch.8 p.464–466] |
| Extrusion | Speed limit (6060) | 585 °C if eutectic remains, otherwise the solidus | | [TOT Ch.8 p.429] |
| Thermal | Al: k, ρ, c_p | 201 W/m·K, 2800 kg/m³, 1063.9 J/kg·K | for extrusion heat balance. ⚠ ρ: [TOT] uses 2700 kg/m³ (λ = 200 W/m·K, c = 1100); prefer 2700 (general knowledge) | [SH p.56; TOT Ch.8 p.388, 466] |
| Thermal | Tool steel: k, ρ, c_p | 32.65 W/m·K, 7860 kg/m³, 489.76 J/kg·K | | [SH p.56] |
| Thermal | Work → heat | 95 % [SH]; stored energy of cold work ≤ ~5 % [TOT] | applies to cold (impact) extrusion too | [SH p.55; TOT Ch.8 p.459] |
| Diffusion | D₀, Q (Cu, Zn, Mg, Si, Zr) | Table §3.5 | Mn/Cr/Fe rows of SH suspect; Sheppard himself classes Mn, Cr, Zr, Fe as very slow diffusers [p.102] | [SH Table 2.3 p.65; p.102] |
| Diffusion | D(500 °C), cm²/s | Mn 5×10⁻¹³; Cu 5×10⁻¹⁰; Mg, Si 1×10⁻⁹ | use for 3xxx | [POL p.105] |
| Homogenisation | Window / time | 450–600 °C; 6–24 h; +50 °C → ~⅓ time (Q_app ≈ 116 kJ/mol, **derived**) | | [POL p.104–105] |
| Homogenisation | Window by series (solidus / homogenisation / extrusion, °C) | 1xxx 640–650 / 560–605 / 450–550; 3xxx 630–645 / 530–620 / 480–520; 5xxx 570–630 / 380–550 / 400–480; 6xxx 580–620 / 560–600 / 430–500; 7xxx > 500 / 400–500 / 390–450 | typically 20–50 °C below solidus | [SH Table 5.1 p.206] |
| Homogenisation | 3004 can stock / 3xxx extrusion | ≥ 605–610 °C, cool 5–30 °C/h / 575 °C ≈ 5 h, slow cool | | [SH p.217–219] |
| Homogenisation | 6xxx | 575 °C/6 h, 150 °C/h to 250 °C, then air; β→α complete 6 h at 565 °C; Mg₂Si dissolves > 465 °C (~2 h); 38 °C/h → 2 µm Mg₂Si (bad), 315 °C/h → 0.25 µm | avoid 330–360 °C holds | [SH p.256–257, 306–307] |
| Homogenisation | Mg₂Si solubility | 1.85 % (595 °C), 1.08 % (500 °C), 0.097 % (200 °C); balanced Si = Mg/1.7038 | | [SH p.187, 255] |
| Homogenisation | 3003 as-cast Mn in solution | ≈ 94 % of 1 % Mn; ≥ 0.02 % Fe accelerates Mn precipitation | direction only (printed balance inconsistent) | [SH p.105–106] |
| Recrystallisation | Unhomogenised vs homogenised (5xxx, 50 % HR at 400 °C) | 100 % RX at 430 °C (5252) / 540 °C (5454) as cast; homogenising at 600 instead of 500 °C lowers it by 40 / 100 °C | | [SH p.222–223] |
| Recrystallisation | 3004 / 1100 anneal heating rate | batch 25 °C/h vs continuous 25 °C/s: cube (0/90° earing) in 1100 only with continuous anneal; continuous anneal of 3004 RX "without dispersoid interaction" | supports G5 mechanism, no magnitudes | [SH p.216–217] |
| Quench | Heat-transfer coefficient | still air 10; forced air 30–120; water 200–40,000 W m⁻² K⁻¹ (≈ 2000 → 40,000 when the vapour film breaks) | press quench | [SH p.195] |
| Homogenisation | Heating rate for dispersoid nucleation | slow, e.g. ~75 °C/h (50 °C/h vs 500 °C/h example) | | [POL p.106] |
| Homogenisation | Relaxation time | τ = l²/(π²D) | | [SH p.66] |
| Preheat | Max hot-working temperature | 10–50 °C below solidus | | [RA p.4-6/4-7] |
| Hot rolling | Breakdown in/out | 200–600 mm → 15–35 mm | | [POL p.107] |
| Hot rolling | Tandem exit | 2.5–8 mm (3–6 mm for < 1 mm final) | | [POL p.107; RA p.5-7] |
| Hot rolling | Pass example | ~13 % (ε_t 0.14) per breakdown pass | **(derived)** | [RA p.5-3] |
| Hot rolling | Mill speed | ≤ ~600 m/min | | [RA p.4-6] |
| Hot rolling | Achievable reduction | > 50 % (dynamic recovery keeps flow stress low) | | [TOT Ch.7 p.354] |
| Hot rolling | Load model (Sims) | P/w = 2k√(RΔh)·Q; Q at 50 % reduction: 0.86 (R/h₂ = 2), 1.04 (5), 1.25 (10), 1.47 (20), 1.69 (30), 1.97 (50), 2.54 (100), 2.97 (150), 3.35 (200), 3.96 (300); full table §4.2 | sticking friction; plane strain; roll flattening neglected; Q read from chart ±0.05; 5–60 % reduction | [TOT Ch.7 eq. 11, Fig. 11 p.367] |
| Hot rolling | Load vs frictionless compression | up to ~4× | | [TOT Ch.7 p.367] |
| Hot rolling | Friction μ (Al) | typically 0.3–0.4 or more; 99.5 % Al, light oil: 0.47–0.60; Duralumin, emulsion: 0.3/0.43/0.6 | depends on reduction and thickness | [TOT Ch.7 p.365] |
| Hot rolling | Geleji μ(T, v) | μ = 1.05 / 0.94 / 0.82 − 0.0005T − 0.056v (steel / cast-iron / ground rolls) | T in °C, v in m/s; a steel-origin form; gives 0.51–0.57 for ground rolls at 380–500 °C, 1 m/s **(derived)** | [TOT Ch.7 p.365] |
| Hot rolling | AA5182 static RX after rolling | start/finish ≈ 4–5 s / ≈ 800 s (320 °C); 0.4 / 3 s (400 °C); 0.2 / 1 s (450 °C); 0.12 / 0.5 s (500 °C); none below ~320 °C | read from figure, ±~50 % in time; prior strain not stated | [TOT Ch.7 Fig. 3 p.357] |
| Hot rolling | Static RX, super-pure Al, 50 % at 500 → 390 °C + 30 s | ≈ 76 % (base); ≈ 97 % at 0.09 % Si; unchanged with Cu ≤ 0.5 %; ≈ 8 % at 0.125 % Fe | read from figure ±3 % | [TOT Ch.4 Fig. 28 p.243–244] |
| Hot rolling | Inter-stand RX → earing (AA5182) | 0/90° earing ≈ 5.9 − 0.038·X_RX (%); cube f(g) ≈ 18.6 − 0.091·X_RX; X_RX 22–97 % | X_RX = computed fraction after pass 1 of 3; read from figure | [TOT Ch.7 Fig. 6 p.359] |
| Hot rolling | Hot-band RX state vs temperature label (AA3104) | unrecrystallised 260 °C; partially 280 °C; fully 315 °C | panel labels; subscript illegible (probably finishing/coiling T) | [TOT Ch.7 Fig. 8 p.363] |
| Homogenisation | AA3003 dispersoid control | mean size 0.03–0.17 µm; density 740 → 11 µm⁻³ (low → high homogenisation T) | DC ingot | [TOT Ch.7 p.355] |
| Belt casting | Gauge / route | 16–20 mm cast → tandem hot to 2–3 mm; 1100, 3xxx, 5xxx | 2003 practice | [TOT Ch.7 p.354] |
| TRC | Minimum gauge | nominal 6 mm, mainly soft alloys (⚠ vs 4–12 mm [RA], ~3–10 mm [POL]) | 2003 statement | [TOT Ch.7 p.352] |
| Rolls | Young's modulus (for roll flattening, stack deflection) | steel 210 GPa ± 3 %; nodular iron 175 GPa ± 5 %; austenitic steel 180 GPa ± 3 %; ν = 0.3 | grey-iron cores are non-linear; compound-roll E drifts as the shell is ground away | [RR §3.2.1 p.18; §3.7 p.53] |
| Rolls | Safe nominal bending stress | grey iron 60; nodular 90; cast steel 120; forged steel 150 MPa | fillet notch factor 1.8–2.2 | [RR §4.10.1 p.100] |
| Rolls | Linear load, strip vs work roll (hot strip) | < 1500 t/m width (≈ 14.7 kN/mm, **derived**) | steel-mill experience limit; above it only nodular-core rolls | [RR §4.10.1.2 p.100] |
| Rolls | Hertzian pressure, work roll vs back-up roll | ≤ 2100 MPa | peaks near barrel edges; chamfer the back-up roll | [RR §4.10.2.1 p.101] |
| Rolls | Static torque strength | 0.9 × tensile strength | torque treated as static load | [RR p.74, 100] |
| Rolls | Roll accuracy | TIR one grade finer than product tolerance; ≤ 0.003 mm (tin plate) | | [RR p.102–103] |
| Roll gap | Friction coefficient μ, behaviour | Mill μ ≫ lab μ and rises during a campaign. Allowed bite angle falls with speed. Numbers: hot rows above; cold row below | back-calculate μ from measured roll force | [RR p.51–52, 92–93] |
| Roll gap | Roll flattening (Hitchcock) | R′ = R[1 + 16(1 − ν²)P/(πE·b·Δh)] | circular-arc assumption; fails for foil below ~100–70 µm exit | [TOT Ch.7 eq. 19 p.370] |
| Roll gap | Cold-rolling pressure (Bland–Ford type) | p = C·2k(h/R′)e^(±μH), H = 2√(R′/h₂)·arctan(√(R′/h₂)φ); with tensions eq. 17a/b | small constant μ, small angles | [TOT Ch.7 eq. 13–18 p.368–369] |
| Roll gap | Contact length | ≈ √(RΔh) | | [TOT Ch.7 p.367] |
| Cold rolling | First pass | ~50 % | | [RA p.5-7] |
| Cold rolling | Friction μ | lowest values < 20 % of hot-rolling μ; mixed lubrication targeted | herringbone if unstable | [TOT Ch.7 p.367–368] |
| Cold rolling | Strength reachable (3xxx/5xxx) | > 400 MPa | | [TOT Ch.7 p.362] |
| Cold rolling | Mill ranges | heavy-gauge 14 → 0.3 mm (≤ 100 kt/a); tandem 2–3 stands ~300 kt/a; light-gauge to 0.02 mm | | [TOT Ch.7 p.360] |
| Foil | Theory limit / minimum gauge | circular-arc theory fails below ~100–70 µm exit; < 13 µm reachable with Ø300 mm rolls | | [TOT Ch.7 p.370] |
| Foil | Speed / bearings | > 1000 m/min needs high process control; ≤ 1500 m/min roller bearings; above that, oil-film bearings | | [TOT Ch.7 p.361–362] |
| Cold rolling | Speed | 1525–1830 m/min (≤ 2135) | | [RA p.5-7, 4-6] |
| Cold rolling | Strip temperature rise | to ≥ ~80 °C | | [RA p.5-7] |
| Annealing | O-temper NHT | 335–405 °C, 0.5–2 h | | [RA p.5-7] (page corrected after full-text pass) |
| Tempers | H1x / H2x / H3x / H4x | strain-hardened only / + partially annealed / + stabilised / + lacquered or painted (H4x takes the H2x or H3x property limits) | H4x describes the can after the 220 °C bake | [RA App. B p.10B-1/10B-2] |
| Ageing | Precipitation heat treatment (HT sheet) | 115–190 °C, ~5–48 h | | [RA §6 p.6-3] |
| Hardening | Mg vs Mn | ≈ 0.8 % Mg ≡ 1.25 % Mn | | [RA App. C p.10C-2] |
| Annealing | Pure Al RX time | hours at 280 °C; minutes at 380 °C; seconds at 500 °C | hard-rolled | [POL p.42] |
| Annealing | Dislocation density | 10¹² → 10¹⁰ → 10⁷–10⁸ cm⁻² | CW → recovered → recrystallised | [POL p.41] |
| Stabilisation | H3x | 120–150 °C [POL] vs ~180 °C [RA] | conflict | |
| Microstructure | Effective dispersoid size | < 0.4 µm [TOT]; 0.05–0.5 µm [POL]; coarse PSN particles > ~1 µm [POL] | | [TOT Ch.3 p.125; POL p.42–43] |
| Microstructure | PCG penalty | −10–15 % longitudinal TS | | [POL p.108] |
| Texture | Extrusion fibre strengthening | +~70 MPa longitudinal vs transverse | HT extrusions | [TOT Ch.3 p.131] |
| Texture | Earing vs cold reduction (AA3104, AA5182) | fully RX 3104 hot band: 0/90° ears ±4 % at 0 % CR, flattest between ~50 and 75 % CR, 45° ears ≈ +4 % at 92 %; unrecrystallised band: 45° ears +3.4 % → ≈ +6 % (0 → 92 %) | relative cup height, read from figure ±0.005; no final anneal | [TOT Ch.7 Fig. 8 p.363] |
| Formability | r̄, Δr definitions; LDR | r̄ = (r₀ + 2r₄₅ + r₉₀)/4; Δr = (r₀ − 2r₄₅ + r₉₀)/2; ln LDR = η√((r̄ + 1)/2), η = 0.74–0.79 | | [TOT Ch.18 eq. 5–8 p.851–852] |
| Formability | 3003-O sheet | E 69 GPa; YS 48, UTS 110 MPa; e_u 23 %, e_t 33 %; n 0.24; r̄ 0.6; Δr 0.2; m 0.005 (6009-T4: r̄ 0.6, Δr 0.1; 6111-T4: r̄ 0.59, K 533 MPa, n 0.238) | LDR(3003-O) ≈ 1.94–2.03 **(derived)** | [TOT Ch.18 Table 4 p.853; Table 7 p.874] |
| Quench | Critical range | 290–400 °C. Sensitivity: Cr > Mn > Zr dispersoids | | [POL p.112–113] |
| Casting | DC cooling / DAS | 1–5 °C/s; 30–70 µm | | [POL p.99, 102] |
| Casting | TRC cooling / DAS | 10²–10³ °C/s (55–555); 5–10 µm | | [POL p.102; RA p.3-4] |
| Casting | TRC window (1235/8011) | 685 ± 5 °C melt; 5.2 mm gap; ~50 mm contact; Ø690 mm rolls | | [TRC p.116] |
| HX tube | Sizing strain → post-braze strength | 3–7 % typical; ~3 % → −22 % | AA3102 MPE | [WIL p.13] |
| HX tube | Extrusion window | 495–503 °C billet, R = 817, 0.7 mm/s, ~34 m/min, 445–460 MPa | AA3102 | [WIL Tables 3, 5] |
| Internal | CRM ε_t targets / anneal | 1070 ≥ 0.95 / 280–320 °C · 1050 ≥ 0.90 / 300–340 · 3102 ≥ 0.80 / 340–370 · 3207 ≥ 0.85 / 350–380 · 3003 ≥ 0.95 / 370–400 | **heuristic** | [INT-CRM] |
| Internal | 3207 Q_rx, JMAK | 145 kJ/mol; n = 3; B₀ = 2.5e28; m = 2 | **internal calibration** | [INT-RX] |

---

## 11. Open questions / gaps

| ID | Gap | Why it matters | Where to get it |
|---|---|---|---|
| **G1 (narrowed)** | Constants for the **user's alloys and state**: 3102, 3207, T11-type lean Al-Mn-Mg-Si, and the effect of rotary casting without homogenisation (supersaturated Mn/Fe, Mg+Si in solution) on α, n, Q, A; explicit T/ε̇ validity ranges; **subgrain size vs Z for any 3xxx alloy** | Hot-mill force and k (§4.2), Z-based hot-band models. [SH] constants are for homogenised DC material, and Sheppard warns cast vs homogenised can differ considerably [p.136] | **Largely filled 2026-10-12** from [SH Table 4.1 p.132] (31 rows incl. 1050, 1100, 3003, 3004, 3005, 3105, 5xxx, 6xxx, 7xxx; §3.3, §10) and the 2014 subgrain fit [SH p.156]. Remaining: hot compression or torsion of rotary-cast strip (as-cast and after the slug anneal) at 350–500 °C, 0.1–50 s⁻¹; calibrate against measured hot-mill roll forces; ch. 13 §1 web leads (W13-19, Shi et al. 1997: Al-1Mn, Al-1Mg) |
| G3 (narrowed) | Coil cooling rates, and RX kinetics of **lean 3xxx (3102/3207) hot band** vs exit temperature and quench delay, especially for supersaturated strip-cast material | Decides whether the quenched in-line hot band is recrystallised (expected: not, §4.3) | **Partly filled 2026-10-12 from [TOT]:** coil self-annealing is standard practice [Ch.7 p.356]; AA3104 hot-band RX state vs temperature label 260/280/315 °C [Fig. 8]; AA5182 RX spectrum 320–500 °C [Fig. 3]; super-pure Al ± Fe/Si/Cu after 500 → 390 °C [Ch.4 Fig. 28]. **[SH] adds:** unhomogenised 5xxx needs a 40–100 °C higher 100 %-RX temperature after 50 % hot rolling at 400 °C [p.222–223]; Mn-free 5052 recrystallises between die and quench, Mn-bearing 5xxx do not [p.165]. **[RA] full text (2026-10-12) has no coil cooling rates or hot-band RX data.** Still missing: 3102/3207 data. Best route: plant measurement (EBSD of a quenched hot-band sample in the trial plan); ch. 15 web sources |
| G4 (narrowed) | Foil rolling practice: pass schedule, pack/double rolling, pinholes, final-anneal practice for 8011/8006/1235 | Foil and fin stock | Not in [TOT Ch.7] (mill types, speeds, the ~100–70 µm theory limit and lubrication only, §5.4), [RR], or the [RA] full text (2026-10-12: only the minimum gauges and two-high foil mills). Needs a foil-specific source, e.g. [RA ref.] Barten, "Aluminum Strip & Foil Rolling" (citation only, not read) [RA §11] |
| G5 (narrowed) | Literature magnitude of the heating-rate effect (Mn/Fe precipitation before RX) on anneal grain size and T_rx in 3xxx | [INT-CRM]/[INT-RX] assume it; the 3003 "~100 °C T_rx increase" is unsourced | **Mechanism supported 2026-10-12** by [SH p.216–217]: batch (25 °C/h) vs continuous (25 °C/s) anneals of 1100 and 3004, with continuous-anneal RX "without dispersoid interaction" and cube/0-90° earing only with fast heating in 1100 (§6). Still missing: grain-size and T_rx magnitudes. Recrystallisation KB (Humphreys & Hatherly); slug trials with recorded heating rate |
| G7 (narrowed) | r-values, Δr and FLDs for **3102/3207** fin, foil and slug O-tempers; earing of lean 3xxx after the slug anneal | Formability and can-rim uniformity | **Partly filled 2026-10-12:** definitions, LDR law and 3003-O / 6xxx-T4 values [TOT Ch.18 p.851–853, 874] (§9). Lean-3xxx values: measure on trial strip (r₀, r₄₅, r₉₀) |
| G9 | Correct Mn, Cr, Fe diffusivities | Sheppard Table 2.3 Mn is ~10³× faster than Polmear; Cr/Fe rows look non-physical. **Sheppard's own text classes Mn, Cr, Zr and Fe as very slow diffusers [p.102]**, contradicting his table (2026-10-12) | Recrystallisation/diffusion KB; primary diffusion data |
| G10 | Stabilisation temperature for H3x: 120–150 °C [POL] vs ~180 °C [RA p.5-7] | Temper practice for 5xxx/3004 | Primary temper spec (EN 515). The EAA brochure (S-043, ch06 §5) and **[RA App. B p.10B-1/10B-2] (full text, 2026-10-12)** both define H3x as stabilised "by a low temperature thermal treatment or as a result of heat introduced during fabrication" and give no temperature, so the gap is still open |
| G11 | Units in [TRC] (strip speed "cm/min", load "kN/mm", productivity "t/(m·h)") | Caster modelling | Original thesis [TRC ref 7] |
| G12 | [INT-RX] Zener limit uses r = 80 nm while the sheet labels 80 nm as "size". [INT-CRM] grain sizes are unvalidated | Internal model consistency | Measure dispersoid radius by TEM/SEM; EBSD grain-size validation |
| G13 | Strain-measure consistency: [INT-*] use ε_t; constitutive and RX literature may use ε̄ = 1.155·ε_t | Systematic error if mixed | Fix the convention in the model code |
| G15 | [SH Table 4.2] pressure-equation constants for 1100 (and 5052, 5056) are inconsistent with [SH Table 4.1] (αn 0.192 vs 0.255; pressures ≈ 4× below the E4 + H6 route, §8.2) | A model using E4a for dilute alloys would under-predict press load | Recalibrate on plant or laboratory extrusion data; until then use E4 + H6 with Table 3-1 |
| G16 | [RA] gaps that remain after the full-text pass: **Appendix C typical-property tables (pp. 10C-4, 10C-6 to 10C-19) are images without text**; **glossary p. 9-2** is in none of the parts | Typical O/H-temper properties of 1xxx/3xxx/5xxx for comparison | Render the pages (`pdftoppm -r 150 -f 26 -l 41` on part xxx) and read the 3003/3004/3005/3105 rows by eye; or use ASM/AA Standards & Data |

**Resolved 2026-10-12 ([SH] and [RA] full-text pass), removed from the table:**
- **G2**, 6xxx homogenisation (β → α, Mg₂Si dissolution, cooling rate) vs extrudability, limit diagrams, and 3xxx homogenisation practice. Filled from [SH §3.3, §4.12–4.13, Ch. 5, §6.1, §6.7.1] (§2.4 items 6–9, §3.5a, §8.4, §8.4a).
- **G14**, Sheppard eqs. 2.4, 2.26–2.29 and 2.27 (Δp). Checked on the page images (§3.2, §8.2): eq. 2.4 confirmed (+1 form; eq. 4.1 misprints −1); Δp contains 1/(αn); eq. 2.26 has no L_B term as printed; eqs. 2.28–2.29 confirmed; the modified-Feltham rate is printed with dimensionally inconsistent exponents (H4).

**Resolved 2026-10-12 ([TOT] full-text pass), removed from the table:**
- **G6**, quantitative earing vs cube vs cold reduction (3104/5182). Filled from [TOT Ch.7 Figs. 6 and 8] (§7.2). The lean-3xxx/slug part moved into G7.
- **G8**, rolling-force models with Al friction data. Filled from [TOT Ch.7 §4]: von Kármán–Siebel, Sims + Q chart, Bland–Ford-type cold solution, Hitchcock, Al hot/cold μ (§4.2). Only the Ekelund formulas in §4.2 remain general knowledge.

**Top 5 implications for alloy design (summary).**
1. Per-atom work hardening Cu ≫ Mg ≈ Si > Mn ≫ Zn [TOT] gives cheap H-temper strength in 3xxx fin/tube. Cu ≤ 0.3 % in NHT alloys [POL].
2. Earing control is a texture-balance problem: hot-band/annealed cube against final-reduction rolling texture. Coarse constituents (PSN) randomise the texture; dispersoids favour cube [POL; TOT].
3. Dispersoid state (size < 0.4 µm, coherent better; Cr worst for quench sensitivity) decides fibrous vs recrystallised extrusions, PCG, and the quench penalty. Tune the homogenisation heating rate (~75 °C/h for nucleation) [POL; TOT].
4. Heat-exchanger tube: small sizing strains (3–7 %) plus brazing produce coarse grains and ~22 % strength loss in 3102. Sc+Zr keeps the tube unrecrystallised to ~575 °C but costs +44 % extrusion pressure [WIL].
5. Continuous-cast 3xxx/8xxx keeps Mn/Fe supersaturated (no homogenisation). Its anneal response and formability need alloy and process re-tuning, not DC practice [RA; POL; MM].

**Implications for the rotary-cast slug route from the [TOT] full-text pass (2026-10-12; inference from the cited facts).**
1. **The quenched in-line hot band is very probably unrecrystallised.** In the closest literature window (50 % at 500 → 390 °C, 30 s hold), even super-pure Al reaches only ~76 % static RX, and ~0.1 % Fe nearly stops it [TOT Ch.4 Fig. 28]. Industrial practice gets a recrystallised, cube-bearing hot band from coil **self-annealing** [TOT Ch.7 p.356], which the water bath rules out. Grain size and texture are therefore set only in the final slug anneal, by the cold strain and the dispersoids that precipitate during it (§4.3).
2. **The hot/cold split is the remaining texture/grain-size lever.** Hot passes at 380–500 °C lie on the cube side of the AA3104 boundary (Z* = 3×10¹⁴ s⁻¹; derived Z ≈ 10¹⁰–10¹⁴ s⁻¹ for ε̇ = 1–50 s⁻¹, approaching Z* only at ≈ 380 °C and the highest rates); cold passes lie on the PSN side [TOT Ch.7 Fig. 4]. More cold reduction gives more stored energy and PSN (finer, more random, lower earing). More hot reduction gives a weaker drive for RX and probably more cube. Because the 30–50 % cold reduction is below the ε_t ≥ 0.8 rule, prefer the largest cold share the customer gauge allows. Measure earing/Δr on trials (§7.3).
3. **Press force scales with slug flow stress at fixed geometry.** Both hot rolling (Sims: P/w = 2k√(RΔh)·Q) and extrusion (F = a + b·ln R) loads are linear in the flow stress [TOT Ch.7 p.367; Ch.8 p.447]. A stronger alloy costs proportionally more hot-mill force and impact-extrusion force, and ≈ 95 % of the extrusion work becomes heat. Updated after the [SH] full-text pass: the hot-flow constants are now available for the base alloys ([SH Table 4.1], §3.3a), so a first quantitative hot-mill load check is possible; alloy-specific constants for rotary-cast strip remain open (G1, narrowed).

**Implications for the rotary-cast slug route from the [SH] and [RA] full-text pass (2026-10-12; inference from the cited facts).**
1. **Hot-mill flow stress is now bounded.** For T11-type lean Al-Mn-Mg-Si, [SH Table 4.1] brackets σ̄ between the 1100 and 3105 rows: ≈ 20–25 MPa at 500 °C/1 s⁻¹ rising to ≈ 49–87 MPa at 380 °C/50 s⁻¹ (§3.3a). Most of the hot-mill load comes from the cold end of the 500 → 380 °C window (σ̄ × 1.5–2.6). Unhomogenised, supersaturated strip should sit in the upper half [SH p.136, 207]. The same constants reproduce the back-calculated AA3102 extrusion flow stress (§3.4), which gives some confidence in using them.
2. **Skipping homogenisation shifts the anneal, not just the strength.** [SH] shows that unhomogenised material recrystallises at a higher temperature (5xxx: +40–100 °C relative to a 600 °C homogenisation) and that Fe ≥ 0.02 % accelerates Mn precipitation [p.106, 222–223]. With T11's 0.52 % Fe, Mn and Fe/Si precipitation will compete with RX during the slug anneal, and [SH p.216–217] shows that the outcome depends on heating rate (batch vs continuous). **Record slug heating rate and peak temperature in every trial**; expect a fast heat-up to give finer, more cube-rich grains.
3. **Mg and Si retained by the water quench raise flow stress and the lacquer bake is an ageing step.** T11 carries ≈ 0.41 % Mg₂Si potential plus ≈ 0.23 % excess Si (derived), largely in solution after the quench [SH p.187, 255]. Mg and Si in solution lower extrudability by raising the flow stress [SH p.256, 258], which carries over to impact-extrusion force unless the slug anneal precipitates them. The 220 °C/10 min bake is the "thermal operation during lacquering" of the H4x temper [RA App. B p.10B-2]: specify can properties after the bake.
