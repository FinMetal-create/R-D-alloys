# 03 — Recovery, Recrystallisation (RX) & Grain Growth in Wrought Al Alloys

**Scope.** Physical metallurgy of softening after deformation, written for alloy and process design. The main focus is lean 3xxx alloys (AA3102, AA3103, AA3003, AA3207, AA3005), both as heat-exchanger, fin and foil alloys and as **annealed impact-extrusion slugs** (lean Al–Mn and Al–Fe–Si–Mg chemistries such as trial T11), with 1xxx, 8xxx (foil), 5xxx and 6xxx where the sources allow. The chain covered is: stored energy, then recovery, then nucleation of RX, then growth and kinetics, then particle and solute interaction (Zener, solute drag, concurrent precipitation), then grain growth, then texture, then hot working.

**Citation rules.** Every claim cites `[Key, section/page]`. Page numbers are the printed book or journal pages unless marked "PDF p.". Anything not found in the sources below is marked **(general knowledge)** and kept to a minimum. Values marked **(derived)** were calculated in this file from cited inputs; the assumptions are stated next to them. Translations from DE/SL are by the compiler.

**Coverage warning.** The Drive text extractor truncates large PDFs at about 400 k characters. As a result, Humphreys & Hatherly (HH) is available only up to §6.5.1 (p.188). Its chapters on RX kinetics, PSN, Zener effects on RX, grain growth, RX textures and hot working (ch. 7, 9, 11–13, 15) are **not** in this extraction. The same truncation affects Sheppard (ch. 3–5 missing) and Polmear (§3.6 foil, canstock and finstock missing). Where the requested topic sits in a missing chapter, this document says so explicitly (see §12 Gaps). **The Handbook of Aluminum (HBAL03) is no longer affected:** the whole book was read as full text on 2026-10-12 (next paragraph and §0), so Mao's ch. 4 "Recrystallization and Grain Growth" is now used throughout §1–§11.

**Application notes.** Paragraphs headed **"Relevance to the slug route"** apply the physics to the user's route: rotary caster 22 mm strip (≈500 °C) → in-line hot rolling (flexible split, exit ≈380 °C) → water-bath quench → cold rolling 30–50 % (up to 60 % under discussion; ε ≈ 0.36–0.92) → slug anneal → impact extrusion → lacquer bake 220 °C/10 min. Reference alloy: trial T11 (Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26 wt %; `knowledge/trials/T11.md`). These notes are inferences unless a citation is given.

**Full-text pass (2026-10-12).** Sources under 10 MB were downloaded whole and converted locally (`pdftotext -layout`). The results were:
- **HH (12.66 MB):** the one download attempt was refused with *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API."* HH therefore stays truncated at §6.5.1, and ch. 7, 9, 11–13 are still unavailable.
- **Pol06 (9.68 MB):** below the limit, but the transfer failed ("message from the server was too large or could not be parsed"), so §3.6 is still missing.
- **Junit08:** the Drive PDF itself is a 35-page excerpt ending at printed p.24, so nothing more exists on Drive. Its method was re-assessed in §2.4.
- **Dav01, Leh06 and Bel05:** re-checked from the PDFs. The Leh06 tables are raster images and cannot be read without OCR. The Bel05 solubility tables were verified and added to §5.1 and §11 row 25.
- Sheppard (10.46–10.51 MB) and Ryen (11.22 MB) are over the limit and were not attempted.
- **HBAL03, second full-text pass (2026-10-12).** The whole book was obtained as a four-part copy (Drive folder "Cloud part book", see §0) and converted to text after a font-map repair. Read in full: **ch. 4 Mao, pp.211–258**. Also read: ch. 5 Katgerman & Eskin §1 (pp.259–264) and §3 incl. §3.1 commercial Al–Mn alloys (pp.293–299); ch. 7 Karhausen & Korhonen pp.355–360 (homogenisation, hot-rolling RX, AA3104 cube/PSN, Avrami model); ch. 19 Howard et al. §3.2 annealing (pp.887–888); ch. 22 Ridley pp.1114–1116 (Zener, PSN route); spot checks of ch. 3. Equations and tables used below (Mao eq.9–12, 22, 38; Katgerman & Eskin Tables 33–35, 37) were checked against rendered page images. **New content cites printed pages as [HBAL03 p.x].**

---

## 0. Sources

| Key | Source (author, title, year) | Drive link | Lang. | Readability / coverage |
|---|---|---|---|---|
| HH | F.J. Humphreys & M. Hatherly, *Recrystallization and Related Annealing Phenomena*, 2nd ed., Elsevier 2004 | [1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w](https://drive.google.com/file/d/1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w/view) | EN | Good text, but equations lose symbols (Greek letters and minus signs dropped). **Truncated at §6.5.1, book p.188 (PDF p.220) of ~600 pp.** Ch. 1–5 complete and ch. 6 to §6.5.1. TOC only for ch. 7–16. Duplicate copy 17tHwICnSZ9xIRALcJHIYXZhVs9mQc-1D. **Download limit test 2026-10-12** (one call, ID 1QvLAUS…): refused with *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API. See https://developers.google.com/workspace/drive/api/guides/manage-downloads#curl"*. |
| Junit08 | M.A. bin Junit, *Characterisation and Modelling of Static Recovery Process of Aluminum Alloy*, BEng thesis, Univ. Malaysia Pahang, 2008 | [1JT7HIwZIGuC5WeJbk1ntYwBd_QJWQbik](https://drive.google.com/file/d/1JT7HIwZIGuC5WeJbk1ntYwBd_QJWQbik/view) (same file as 1ANzZHinT6byugfeZkXbsNETvmKgc-phK) | EN/MS | **Full-text pass 2026-10-12:** the PDF was downloaded (2,349,034 B). It has **35 PDF pages only**: front matter plus printed pp.1–24, ending in the middle of Table 4.3. It is a repository excerpt; the TOC lists ch. 4 to p.36, ch. 5 at pp.37–39 and appendices to p.43. The earlier "truncation" was therefore **in the file, not in the reader**. Tables 4.4–4.14 and the Q calculations (pp.25–36), and the conclusions (pp.37–39), are **not in the Drive library**. Low scientific quality; re-assessed in §2.4. |
| SimRX | "Modeling Recrystallization and grain growth phenomena" (review chapter; no author or date in text; refs 306–348) | [1MN7_BcrlAvTxyiDd_D2MQge-efotHMS6](https://drive.google.com/file/d/1MN7_BcrlAvTxyiDd_D2MQge-efotHMS6/view) | EN | Complete: 11 pp of text plus a long reference list. Qualitative modelling overview. |
| Prakt05 | Y. Rudnik, *Praktikum G3/MW2: Wärmebehandlung und Rekristallisation von Aluminium* (lab instruction), Oct 2005 | [116AVCkaosrrRKG94_GFBXrHYE3R1EzC4](https://drive.google.com/file/d/116AVCkaosrrRKG94_GFBXrHYE3R1EzC4/view) | DE | Complete (9 pp). Figures (RX diagram of pure Al) not extractable. Basic level. |
| AMAG14 | AMAG, "Heat Treatment – A Brief Introduction", *AluReport* 01.2014, pp.10–15 | [1hvicHsqiMWT-C-hsvbMlLlTw0eA6V4ko](https://drive.google.com/file/d/1hvicHsqiMWT-C-hsvbMlLlTw0eA6V4ko/view) | EN | Complete. Two-column text interleaved but decipherable. DE version exists (1D9DRhJTjetqwamIhaHLaekopweS_mFVt), not re-read. |
| Bom08 | D. Bombač, M. Fazarinc, G. Kugler, S. Spajić, "Microstructure development of Nimonic 80A superalloy during hot deformation", *RMZ – Mater. Geoenviron.* 55(3) 319–328, 2008 | [1K3jZ3TiJKKk54DiBq9dWya51PKsf_Zq8](https://drive.google.com/file/d/1K3jZ3TiJKKk54DiBq9dWya51PKsf_Zq8/view) | EN (SL abstract) | Complete. **Ni superalloy, not Al.** Only the methodology (Z-sinh, DRX onset, processing maps) transfers. |
| Leh06 | W. Lehnert, R. Kawalla, D. Hübgen, "Herstellung von hochwertigen Bändern und Blechen aus Aluminiumwerkstoffen", *Metalurgija* 45(3) 169–178, 2006 | [18QdmKaIrJQ-coTXVt51rQ5wZqpVDgEdC](https://drive.google.com/file/d/18QdmKaIrJQ-coTXVt51rQ5wZqpVDgEdC/view) | DE (EN/HR abstr.) | Text complete. Tables 4–6 and figures 10–14 not extracted. 2026-10-12: PDF downloaded (2,844,699 B, 10 pp.); the tables and figures are embedded raster images with no text layer, so they are not recoverable without OCR. |
| Pol06 | I.J. Polmear, *Light Alloys*, 4th ed., Butterworth-Heinemann 2006 | [1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w](https://drive.google.com/file/d/1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w/view) | EN | Good. **Truncated at about book p.174** (ch. 1–3 up to §3.5.3). §3.6 (foil, canstock, finstock) missing. 2026-10-12: a download was attempted (9,683,385 B, under the 10 MB limit), but the Drive connector closed the connection ("a message from the server was too large or could not be parsed"), so the file is still truncated. |
| HBAL03 | G.E. Totten & D.S. MacKenzie (eds.), *Handbook of Aluminum, Vol. 1: Physical Metallurgy and Processes*, Marcel Dekker 2003, ISBN 0-8247-0494-0 (catalog **S-029**). Chapters used: ch. 3 M. Tiryakioğlu & J.T. Staley, "Physical Metallurgy and the Effect of Alloying Additions" (pp.81–210); **ch. 4 W. Mao, "Recrystallization and Grain Growth" (pp.211–258)**; ch. 5 L. Katgerman & D. Eskin, "Hardening, Annealing, and Aging" (pp.259–304); ch. 7 K.F. Karhausen & A.S. Korhonen, "Rolling of Aluminum" (from p.351); ch. 19 R. Howard, N. Bogh & D.S. MacKenzie, "Heat Treating Processes and Equipment" (pp.881–970); ch. 22 N. Ridley, "Superplastic Forming" (pp.1105–1158) | Truncated copy: [1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz](https://drive.google.com/file/d/1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz/view) ("Alminium.pdf"; identical size to "ASM Handbook of Aluminium vol. 1.pdf" 1LNDwz9XSVn51tWynCZUvGvbdzEDR23K3). **Full text:** Drive folder "Cloud part book" [1fzmh9OxDx3E92Sq2FLDNQ9AkCKrWvP-G](https://drive.google.com/drive/folders/1fzmh9OxDx3E92Sq2FLDNQ9AkCKrWvP-G): part 1 "Al 1-400.pdf" [1Yxag4tVsKp2w7GaNvUqpz09wJRuCpLVT](https://drive.google.com/file/d/1Yxag4tVsKp2w7GaNvUqpz09wJRuCpLVT/view) (pp.1–388), part 3 "Al 1-800.pdf" [10ilZD0Rt4LM1rUzaCa9hLB0Up-NaH7a3](https://drive.google.com/file/d/10ilZD0Rt4LM1rUzaCa9hLB0Up-NaH7a3/view) (pp.788–988), part 4 "1309.pdf" [1KmVD2fbnjMnPd2M5YfDEQaI0OflR_NMD](https://drive.google.com/file/d/1KmVD2fbnjMnPd2M5YfDEQaI0OflR_NMD/view) (pp.989–1296) | EN | **Full text, 2026-10-12.** Born-digital; the broken font maps were repaired before text conversion. Equations keep the PDF layout and rare Greek letters are best guesses, so the equations used here were checked against page images. **Citation convention:** older entries cite **[HBAL03 PDF p.x]** of the truncated "Alminium.pdf" (ch. 3 only); **PDF p. = printed p. + 12** (confirmed against the full text for PDF pp.142–143, 152 and 171–172, whose content matches printed pp.130–131, 140 and 159–160). New entries cite **printed** pages as **[HBAL03 p.x]**. Mao's chapter is a textbook-level review (pure Al, Al–Mn, Al–Mg examples); some of its constants disagree with HH (§1.4). |
| Ryen03 | Ø. Ryen, *Work Hardening and Mechanical Anisotropy of Aluminium Sheets and Profiles*, Dr.ing. thesis, NTNU 2003 (supervisor E. Nes) | [1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_](https://drive.google.com/file/d/1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_/view) ("uporabno del-2.pdf") | EN | Good. **Truncated at about §4.2.2 (p.70)**. AA3103 results (§4.5.2) and the solute discussion (ch. 5) are missing. Contains the Nes model equations, partly garbled. |
| Røy05 | J. Røyset & N. Ryum, "Scandium in aluminium alloys", *Int. Mater. Rev.* 50(1) 19–44, 2005 | [1A_yvqnRq-o1I53m3tieuVp4Sq5zUu1iL](https://drive.google.com/file/d/1A_yvqnRq-o1I53m3tieuVp4Sq5zUu1iL/view) | EN | Complete. Inequality symbols mangled (`,`=<, `.`=>, `&`=≫, `%`=≲), decoded by context. |
| Røy07 | J. Røyset, "Scandium in aluminium alloys overview: physical metallurgy, properties and applications", *Metall. Sci. Technol.* 25(2) 11–21 (c. 2007) | [1FizSqhIa3XAhPQpZYt0maHVsHdEsKrhW](https://drive.google.com/file/d/1FizSqhIa3XAhPQpZYt0maHVsHdEsKrhW/view) | EN (IT abstr.) | Complete. Column garbling. |
| Rob04 | J.D. Robson, "A new model for prediction of dispersoid precipitation in aluminium alloys containing zirconium and scandium", *Acta Mater.* 52 (2004) 1409–1421 | [1hVcF0Jxx5hg5BVVJJjPNyGk8o0oslgRk](https://drive.google.com/file/d/1hVcF0Jxx5hg5BVVJJjPNyGk8o0oslgRk/view) | EN | Complete. Equations partly garbled. |
| W7 | Aluminium-Zentrale/GDA, *Merkblatt W7: Wärmebehandlung von Aluminiumlegierungen* (edition year not in text) | [1fEJ6FsDzCDqPZRloFgGFYV-RNudGVd9Y](https://drive.google.com/file/d/1fEJ6FsDzCDqPZRloFgGFYV-RNudGVd9Y/view) | DE | Complete, including Table 2 (soft-annealing practice per alloy). |
| Bel05 | ch. 1 "Alloys of the Al–Fe–Mn–Si System" in *Multicomponent Phase Diagrams: Applications for Commercial Aluminum Alloys*, Elsevier 2005 (authors not in text; Belov, Eskin, Aksenov (general knowledge)) | [1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD](https://drive.google.com/file/d/1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD/view) | EN | Complete. Phase-diagram figures garbled. 2026-10-12: the PDF was downloaded (46 pp.) and Tables 1.4, 1.7, 1.9 and 1.13 were verified in the layout extraction (used in §5.1 and §11 row 25). Tables 1.2, 1.5 and 1.16 are on rotated pages and remain unreadable. |
| Wil12 | C.R. Williams, *Effects of Sc and Zr Additions on Al Mechanical Properties, Post-Braze Grain Structure, and Extrusion*, MSc thesis, Ohio Univ. 2012 | [1MYsjf2OwlDfrOtnb1zQas-DV9wfunqne](https://drive.google.com/file/d/1MYsjf2OwlDfrOtnb1zQas-DV9wfunqne/view) | EN | Complete. Directly relevant to **AA3102 MPE tube braze grain growth**. |
| Dav01 | J.R. Davis, "Aluminum and Aluminum Alloys", in *Alloying: Understanding the Basics*, ASM 2001, pp.351–416 | [1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z](https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view) | EN | Complete. Qualitative alloying-element roles. Re-read from the downloaded PDF on 2026-10-12 (536,308 B, 66 pp.); additions in §4.4 and §7.3. |
| Shep99 | T. Sheppard, *Extrusion of Aluminium Alloys*, Kluwer 1999 | [195YE0KUFE-yMliXyp304IqoaSdvnxKVU](https://drive.google.com/file/d/195YE0KUFE-yMliXyp304IqoaSdvnxKVU/view) | EN | **Truncated at about p.70** (ch. 1–2 only). Ch. 3.5 (recovery/RX), 4.2 (Zener–Hollomon), 4.9 (RX), 4.11.4 (subgrain size) and 5.4 (3xxx) are missing. Second copy 1pJoblJP3s9o7Z_WgFM9dhMmepLi7POET has the same truncation. |

**Found by search but not used for content** (out of scope or not literature):
- `62816_ch02.pdf` (DC-casting solidification; Eskin): belongs in a solidification KB file.
- "Influence of alloying elements.pdf" (Rana et al. 2012): generic review.
- "Chemie und Eigenschaften metallischer Werkstoffe 2017" (civil-engineering lecture, mostly steel).
- TALAT 1101 ("lastnosti aluminija"), Wikipedia compilation ("74849304-Aluminium"), Dwight "Aluminium Design and Construction".
- "Clusters in Al alloys", TMS 2018 proceedings, MMC, Ni, Mg and rare-metal books.
- User spreadsheets in Drive root (`AA3207_Recrystallization_Simulation.xlsx` ×4, `3102_RX_simulation.xlsx`, `EN_AW_*CRM_Reduction_Table*.xlsx`, `aluminium_tempers_*.xlsx`). These are user models, not literature; one is commented on in §12.
- The `microstructure-sim-v2.14.0` folder was **not** read, as instructed.

---

## 1. The deformed state: stored energy, dislocation density and substructure (driving force for everything below)

### 1.1 Mechanisms
- Only a small fraction of plastic work is stored; the rest becomes heat. HH puts it at "~1 %" [HH §2.2.1 p.12]. Prakt05 says "<5 %" [Prakt05 p.7]. HH Table 2.1 gives a stored/expended ratio of 0.022 for 99.999 % Al [HH Tab.2.1 p.16].
- Stored energy is almost entirely dislocations, located in cell/subgrain walls and in cell interiors, plus the new grain-boundary area created by grain-shape change. A cube grain rolled 50 / 90 / 99 % gains +16 / +270 / +3267 % boundary area [HH §2.2.1 p.13].
- Al has a high stacking-fault energy (166 mJ m⁻² [HH Tab.2.4 p.26]; "~170" [HH §2.3.1 p.25; Pol06 p.36]). This makes cross-slip and dynamic recovery easy, so Al forms cells or subgrains during deformation. Stored energy is therefore low: Al 69.6 J mol⁻¹ against 216 J mol⁻¹ for Cu at similar strain [HH Tab.2.1 p.16].
- Substructure hierarchy [HH §2.4.1–2.4.2 pp.27–34; Ryen03 §2.2.2 pp.10–13]:
  - transient cells (incidental dislocation boundaries, IDBs) of 0.5–1 µm and below 1° misorientation;
  - cell blocks and cell bands bounded by dense dislocation walls and microbands (geometrically necessary boundaries, GNBs), inclined about 25–40° to the rolling plane;
  - microshear (S) bands at 0.3 < ε < 1;
  - a lamellar structure of largely high-angle boundaries (HAGB) at ε > 2.
- In Al the cell size falls to about 0.5 µm and then stays nearly constant for ε > 0.5 [HH §2.4.2.1 p.30]. Mao gives "generally 1–3 µm or less" with < 2° between neighbouring cells, shown for 80–86 % cold-rolled Al–1.3 wt % Mn; cells elongate with further strain [HBAL03 p.213].
- Of the stored energy, about 80–90 % is due to dislocations; the vacancy share is negligible because deformation vacancies migrate out at RT [HBAL03 pp.214, 216]. Impurity atoms, a finer initial grain size and second-phase particles all raise the stored energy at a given strain, because they increase dislocation multiplication [HBAL03 p.215].
- **Solute (Mg ≥3–5 %) suppresses cell formation** [HH §2.4.3 p.35; Ryen03 §2.2.3 p.14]. Dislocations then form a "Taylor lattice" with domain boundaries parallel to {111} (0.5–1°) and microbands, which develop into shear bands.
- In Al–Mn, cells form whether Mn is in solid solution or present as dispersoids. Adding Mg (3004 vs 3003) gives a finer substructure and a higher dislocation content after 90 % cold rolling (CR) [HBAL03 PDF p.172].
- Deformation heterogeneities are the RX nucleation sites:
  - **Deformation and transition bands:** more frequent in coarse grains; in Al they do not occur for grain size < 20 µm; bands per grain scale with √d [HH §2.7.4 p.43]. Transition bands in Al alloys can be only 1–2 cells wide yet carry a large orientation change [HH §2.7.3 p.42].
  - **Shear bands** at about 35° to RD [HH §2.8 p.44; Ryen03 §2.2.5 p.17]. They are promoted by Mg (critical about 2–3 % Mg [Ryen03 p.17–18], Inagaki & Kohara), by coarse grains, by deformable particles and by RT dynamic strain ageing. They are reduced at high deformation T [HH §2.8.4 p.47].
  - **Particle deformation zones** at non-deformable particles above about 0.1 µm (§3).
- "Cold" rolling of Al is not truly cold. 0.3 T_m is about 6 °C, and commercial cold-rolled strip reaches 100–150 °C at strain rates of 50–100 s⁻¹, so dynamic recovery operates [Ryen03 §2.2.1 p.10].

### 1.2 Quantitative relations

| Quantity | Relation | Variables / units | Al values | Source |
|---|---|---|---|---|
| Strain vs density | ε = ρ b L | ρ (m⁻²), b (m), L mean slip distance (m) | — | [HH eq.2.1 p.14] |
| Flow stress (Taylor) | σ = c₁ G b ρ^½ | c₁ ≈ 0.5 | G = 25.4 GPa, b = 0.286 nm [HH Tab.5.1 p.129] | [HH eq.2.2 p.17] |
| — alternative forms | Δτ = α G b ρ^½ | α 0.2–0.3, composition dependent | — | [HBAL03 eq.6 PDF p.108] |
| — Nes composite | τ = τ_t + τ_p + α₁ G b ρ_i^½ + α₂ G b φ (1/δ + 1/D) | α₁ ≈ 0.3, α₂ ≈ 2; φ sub-boundary misorientation (rad); δ subgrain size; D grain size | — | [Ryen03 eq.2.22 p.37] |
| Taylor factor | σ = M τ | M = σ/τ_c (orientation factor) | **M ≈ 3.06 for random fcc (general knowledge)**; no numerical M in the extracted sources | [HH §3.7.1.2 p.84; Ryen03 p.44] |
| Dislocation line energy | E_dis ≈ c₂ G b², c₂ ≈ 0.5 (full form: (G b² f(ν)/4π) ln(R/R₀)) | R ≈ ρ^-½, R₀ = b…5b | — | [HH eq.2.3–2.5 pp.17–18] |
| Stored energy, dislocations | E_D = c₂ ρ G b² (≈ ρΓ, Γ ≈ G b²/2) | J m⁻³ | — | [HH eq.2.6 p.18; Ryen03 eq.2.1–2.2 p.9] |
| Stored energy, subgrains | E_D ≈ 3γ_s/D = αγ_s/R, α ≈ 1.5 | γ_s LAGB energy, D subgrain diameter | — | [HH eq.2.7 p.18] |
| — with Read–Shockley | E_D = (3γ_m θ/(D θ_m))(1 − ln(θ/θ_m)) | θ_m = 15° | — | [HH eq.2.8 p.19] |
| LAGB energy (Read–Shockley) | γ_s = γ_m (θ/θ_m)(1 − ln(θ/θ_m)); θ ≈ b/h | h dislocation spacing | confirmed for Al foils (Yang 2001); <100> axes highest energy, <111> lowest | [HH eq.4.4–4.6 pp.95–97] |
| HAGB energy | γ_b | J m⁻² | **0.324** (Murr 1975); coherent twin 0.075 | [HH Tab.4.2 p.104; Tab.5.1 p.129] |
| Nes total density | ρ = ρ_i + κ₀ φ/(b δ) | κ₀ ≈ 3 | — | [Ryen03 eq.2.16 p.35] |
| Cell size vs strain | δ ∝ 1/ε for ε > 1 | — | D at ε = 1.5: **Al 0.5 µm** (Cu, Ni, Fe 0.3) | [HH §2.2.3.2 pp.19–20, Fig.2.4] |
| Interior density saturation | ρ_i ≈ const for ε > 0.3 (Al) | — | **~10¹⁴ m⁻² for ε = 0.03–2** in AA1050 and AA3207 (higher in 3207, 0.4 % Mn) | [HH p.18; Ryen03 §2.2.4 p.16] |
| Misorientation | θ saturates at 2–3° at ε ≈ 1 (Nes) **vs** continues to rise (TEM/EBSD) | — | IDB about 3° at large ε; GNB up to 15–20° and becomes HAGB | [HH p.20; Ryen03 p.11–13] |
| Densities | annealed → recovered → heavy CW | m⁻² | ~10¹¹–10¹² → 10¹⁴ → 10¹⁶ | [Pol06 p.41; HH p.4; Ryen03 p.16] |
| — Mao's set | annealed → heavily deformed → after recovery | m⁻² | 10¹⁰ → 10¹⁵ → 1.5×10¹⁴ | [HBAL03 pp.214, 216] (citing Hornbogen & Warlimont) |
| Stored energy, heavily deformed Al (Mao) | E ≈ 0.5 ρ G b² | ρ = 10¹⁵ m⁻², G = 2.5×10¹⁰ N m⁻², b = 3.5×10⁻¹⁰ m (as printed) | "about 2×10⁶ J m⁻³" (1.53×10⁶ in the nucleation estimate); annealed ≈ 20 J m⁻³. **With HH's G = 25.4 GPa and b = 0.286 nm: 1.0×10⁶ J m⁻³ (derived)** | [HBAL03 pp.215, 221] |
| Measured stored energy, 99.999 % Al | torsion at 77 K, shear 6.75 | — | **69.6 J mol⁻¹**, ρ ≈ 3.1×10¹⁵ m⁻² (from E/Gb²) | [HH Tab.2.1 p.16] |
| → as pressure | 69.6 J mol⁻¹ ÷ V_m(Al) ≈ 1.0×10⁻⁵ m³ mol⁻¹ | — | **≈ 7 MPa (derived)** | derived from HH Tab.2.1 |
| Typical P_RX (Cu example) | ρ = 10¹⁵–10¹⁶ | — | 2–20 MPa | [HH §1.3.2 p.10] |
| Particle-generated GNDs | ρ_G = 3 F_V s/(r b) (Ashby) | F_V volume fraction, s shear strain, r radius | upper bound; holds only at small strain | [HH eq.2.17–2.19 pp.52–53] |
| Shear-band instability | (1/σ)dσ/dε = n/ε + m/ε̇·… + (1/M)dM/dε … < 0 | geometric softening (dM/dε < 0) dominates near 35° | — | [HH eq.2.10 p.47; Ryen03 eq.2.3 p.17] |

### 1.3 Design levers
- **More strain gives more driving force and more nucleation sites.** It also brings finer and more misoriented substructure, and more transition bands, shear bands and deformation zones [HH §2.4; §2.9.4].
- **Mg in solution** (3004/3005/3105 vs 3003/3102) raises stored energy and dislocation density. It suppresses dynamic recovery [HH §2.4.3; HBAL03 PDF p.172, 178] and promotes shear bands, which push texture toward Brass/Goss [HH §3.6.4 p.82; Ryen03 p.21–22].
- **Fine non-shearable particles at a spacing similar to the cell size** homogenise deformation. In Al–0.8Si (d = 0.10 µm, F_V = 8×10⁻³, λ = 0.8 µm) the subgrain misorientation was 1.4° vs 2.1° and the 10×10 µm orientation spread 7° vs 12° compared with Al–0.1Mg [HH Tab.2.7 p.56]. Fewer large misorientations means **fewer viable RX nuclei**.
- **Initial grain size below about 20 µm** suppresses deformation banding in Al [HH §2.7.4 p.43]. A fine hot-band or intermediate-anneal grain therefore gives more homogeneous rolling and faster rolling-texture development: fine-grained (15 µm) AlMg0.5 shows a strong C–S texture already at ε = 0.6 [Ryen03 §4.2.1 p.69].
- **Roll-gap geometry and friction** (small rolls, light passes, thick gauge, no lubricant) create through-thickness texture gradients. Unlubricated AA3003 forms a strong surface shear {001}<110> component [HH §3.6.1 pp.79–80, Fig.3.15].

### 1.4 Pitfalls
- X-ray line broadening gives 8–80 J mol⁻¹ where calorimetry gives 250–800 J mol⁻¹ (heavily cold-worked metals, all metals) [HH §2.2.2.2 p.16]. Do not mix the two methods.
- **Local stored energy matters more than the average** [HH §2.2.3 p.16; SimRX p.1].
- **Particle-enhanced stored energy is real only at small strain.** It is about 10× pure Al in Al–Mg–Si at ε = 0.1 [HH p.54]. At RX-relevant strains dynamic recovery brings ρ back near the single-phase value [HH §2.9.2.1 p.54].
- The misorientation-saturation assumption (3–4° in the Nes model [Ryen03 p.38]) is contested [HH p.20].
- **Constants in Mao's chapter disagree with HH (flagged after the full-text pass; this KB keeps the HH values):**
  - stacking-fault energy **250 mJ m⁻²** [HBAL03 p.212] vs 166 mJ m⁻² [HH Tab.2.4];
  - Burgers vector **b = 3.5×10⁻¹⁰ m** [HBAL03 pp.215, 221] vs **0.286 nm** [HH Tab.5.1]. 0.35 nm is not the Al Burgers vector (b = a/√2 with a = 0.404 nm [HBAL03 pp.294, 297] gives 0.286 nm, derived), so Mao's stored-energy figures are about 1.5× too high;
  - HAGB energy **0.6–1.9 J m⁻²** (99.99 % Al, nucleation estimate) and **≈1.0 J m⁻²** (grain-growth estimate) [HBAL03 pp.221, 245], both citing Mondolfo 1976, vs **0.324 J m⁻²** [HH Tab.4.2]. Every quantity linear in γ (critical nucleus radius, Zener pressure, grain-growth pressure) changes by the same factor of 2–6, so state which γ a model uses.

---

## 2. Recovery (static) and recovery-controlled softening (H2x/H3x tempers)

### 2.1 Mechanisms
- Recovery and RX compete for the same stored energy. Recovery lowers the RX driving force and can change both the nature and the kinetics of RX [HH §6.1.1 p.170]. Recovery mechanisms (subgrain growth and coalescence) also *nucleate* RX [HH p.170; Pol06 p.42].
- **What recovery does in Al (Mao)** [HBAL03 pp.216–220]:
  - it starts immediately on annealing, with **no incubation period**, and involves **no HAGB migration**;
  - the dislocation density drops from ~10¹⁵ to ~1.5×10¹⁴ m⁻², but the deformed grain shape and the **deformation texture are retained**;
  - electrical resistivity falls only slightly, and in deformed pure Al **up to 40 % of the work-hardening increment in hardness** can be recovered (Lücke & Rixen 1968);
  - mechanisms: annihilation of unlike edge dislocations by glide (same plane) or climb (adjacent planes), and alignment of like dislocations into tilt walls (polygonisation; edge-dislocation interaction force eq.1–3); cells coarsen and their walls sharpen into subgrain boundaries;
  - the recovered density (~1.5×10¹⁴ m⁻²) is **still enough to drive RX** [HBAL03 p.220].
- The sequence is: dipole annihilation; cell walls to sharp sub-boundaries (polygonisation, no scale change); subgrain coarsening [HH §6.3–6.5 pp.178–188].
  - In situ HVEM on 10 %-deformed Al (2 min at 250 °C): tangles become LAGB networks [HH §6.4.2 p.187]. The yield stress falls but the work-hardening rate rises [HH p.187].
  - Subgrain rather than cell structure is favoured by high SFE, low solute, large strain and high deformation T [HH p.188].
- Al: high SFE gives rapid climb and cross-slip, so recovery is significant before RX [HH §6.2.1.3 p.173]. For 99.998 % Al compressed 75 % (DSC at 6 °C min⁻¹), dislocation recovery gives a broad heat release at **100–250 °C** and RX peaks at **≈300 °C** [HH Fig.6.3 p.172].
- 99.999 % Al deformed at 77 K recrystallises below RT, with no separate dislocation-recovery peak [HH §6.1.2 p.172]. (Minus signs were lost in extraction; the peaks are read as ≈ −70 °C for point defects and ≈ −20 °C for RX.)
- **Solute: two opposing effects.** Mg pins dislocations, which suppresses dynamic recovery and raises stored energy. Yet static recovery of Al–Mg is rapid, possibly faster than pure Al [HH §6.2.1.3 p.173].
  - Higher-Mg 5xxx alloys lose more strength by recovery; lower-Mg alloys lose more by RX. At equal partially annealed strength, the higher-Mg alloy has higher elongation [HBAL03 PDF p.180].
- **Dispersoids** (0.05–0.5 µm) "also delay recovery" [Pol06 p.43]. Mn as dispersed precipitate "is effective in slowing recovery" [Dav01 p.382]. Zr precipitates inhibit recovery and RX [Dav01 p.387]. Recovery on scales finer than the interparticle spacing λ is unaffected; recovery on larger scales is hindered [HH §2.9.2.2 p.54].
- **Room-temperature age softening of work-hardened 5xxx** (localised recovery) is the reason for **H3x stabilisation at 120–150 °C** [Pol06 p.130] (120–175 °C [Pol06 p.118]). **H2x** is cold-worked plus partially annealed [Pol06 p.118; W7 Tab.4–5 p.22].
- **LAGB migration** (the rate-controlling step of subgrain coarsening) is climb controlled by solute lattice diffusion.
  - Mobility rises steeply with misorientation (Al–0.05Si: ×50 from 2.5° to 5.5°) and saturates around 14–20° [HH §5.2.2 pp.127–134].
  - In the 2–5° range LAGB mobility is **10–500× lower** than that of a random HAGB [HH p.134].

### 2.2 Kinetic laws (model-ready)

| Law | Equation | Notes / parameters | Source |
|---|---|---|---|
| Fractional recovery (Friedel/Drouard form) | R = (σ_m − σ)/(σ_m − σ₀); R = c₁ ln t − Q/kT (as printed) | Zn crystals: Q = 83.7 kJ mol⁻¹ ≈ self-diffusion; Al crystals also obey type-1. To extract Q, divide the 1/T-slope by c₁ (§2.4; §11 row 24) | [HH eq.6.6–6.7 p.176]; same in [Junit08 §2.6 p.11] |
| Type 1 (logarithmic) | dX/dt = −c₁/t → X = c₂ − c₁ ln t | invalid at t→0 and t→∞ | [HH eq.6.1–6.2 p.175] |
| Type 2 (power) | dX/dt = −c₁ X^m → X^(1−m) − X₀^(1−m) = (m−1)c₁t | dipole annihilation gives m = 2; Cu/Ni m = 3 | [HH eq.6.3–6.5, 6.11–6.12 pp.175–180] |
| Second-order dislocation recovery (Mao) | dρ/dt = −kρ² → ρ = 1/(kt + 1/ρ₀) ≈ 1/(kt) for ρ₀ ≫ ρ, i.e. dρ/dt ≈ −1/(kt²) | k depends on T only. Confirmed for zone-refined Al–0.0068 at % Cu (Vandermeer & Gordon 1963). Same form as HH type 2 with m = 2, and with σ ∝ ρ^½ it gives 1/σ² − 1/σ₀² ∝ t, the form of the climb-coarsening law below (derived) | [HBAL03 eq.4–6 pp.219–220] |
| Network coarsening by climb | R² = R₀² + c₁t, c₁ = 2 D_s G b³ c_j/kT → 1/ρ − 1/ρ₀ = c₁t → 1/σ² − 1/σ₀² = c₃t | c_j jog concentration. Q_climb = Q_s at high T; plus jog formation at low T; core diffusion Q_c ≈ 0.5 Q_s | [HH eq.6.13–6.18 pp.182–183] |
| Thermally activated glide (Cottrell–Aytekin, logarithmic) | dσ/dt = −c₁ exp(−(Q₀ − c₂σ)/kT) → σ = σ₀ − (kT/c₂) ln(1 + t/t₀) | **Al–1Mg Q₀ = 277, Al–5Mg Q₀ = 231 kJ mol⁻¹** (independent of strain; Barioz 1992; Al–3Mg, ε = 3) vs Q_s(Al) = 142 | [HH eq.6.19–6.22 pp.183–184] |
| Climb of extended dislocations | v = c₀ D_x F γ_SFE²/(kT…) → recovery rate ∝ γ_SFE² | Argon & Moffat | [HH eq.6.23 p.184] |
| Nes static subgrain growth | dδ/dt = ν_D B_δ b exp(−U*/kT) · 2 sinh(P V_δ/kT), P = 4γ_sb/δ | V_δ ∝ b³ (pure) or ∝ ξ_δ b³ c^(−e) (solid solution); U* = U_s + ΔU_s with solute | [Ryen03 eq.2.39 p.42] (written per unit shear strain; multiply by γ̇ for the time rate) |
| Nes interior-density recovery | dρ_i/dt = −ρ_i^(1+x) b^y l_a ξ_ρ B_ρ ν_D exp(−U*/kT) · 2 sinh(V_ρ G b ρ_i^z/kT) | pure metal: x = 1, y = 1, z = ½, l_a ≈ b; solid solution with glide: x = ½, y = 0, z = 2π, V_ρ ∝ ξ_s b³ c^(−e); with climb: l_a = b/c | [Ryen03 eq.2.38 p.42] (garbled; check against Nes & Marthinsen 2002) |
| LAGB mobility | M = C D_s b/kT (C ~1); very-low-angle limit M = D_s c_j b²/(4c₁ kT θ) | Al–0.05Si: Q_LAGB **125–154 kJ mol⁻¹** (≈ Si lattice diffusion), θ-dependent up to 14°, then constant | [HH eq.5.4, 5.11; Fig.5.7 pp.129–133] |

**Diffusion data for Al** [HH Tab.5.1 p.129]: Q_self = 142, Q_core = 82, Q_boundary = 84 kJ mol⁻¹. At 500 °C: D(Mn) = 5×10⁻¹³, D(Cu) = 5×10⁻¹⁰, D(Mg, Si) = 1×10⁻⁹ cm² s⁻¹ [Pol06 p.105]. **Mn diffuses about 10³× slower than Cu and about 2×10³× slower than Mg or Si.** This is the root of Mn dispersoid stability and of its slow solute-drag kinetics.

### 2.3 Design levers (H-temper softening and stability)
- Partial annealing (H2x) works because recovery precedes RX in high-SFE Al [HH §6.2.1.3]. **Retained Mg/Mn in solution and fine dispersoids widen the recovery window before RX**, which gives a flatter softening curve and more robust H2x [HBAL03 PDF p.180; Pol06 p.43; Dav01 p.382].
- Increasing Mg and lowering the anneal T both give smaller recovered subgrains and higher retained strength [HBAL03 PDF p.180].
- Use **σ ∝ 1/δ** for recovered or hot-worked products (AA3104 hot-worked: linear σ vs 1/δ [Ryen03 Fig.2.25 p.34]). For cells (low T, Hall–Petch-type exponent m ≈ 1) vs subgrains (m ≈ ½) see [Pol06 p.36–37; HBAL03 PDF p.113–114].
- **Work-hardening anchors for H tempers** (sheet, UTS / YS / El.) [HBAL03 Tab.3 p.264]: 1100-O 75 / 25 MPa / 30 %; 1100-H14 110 / 95 / 5; 1100-H18 150 / – / 4; 5052-O 170 / 65 / 19; 5052-H34 235 / 180 / 6; 5052-H38 270 / 220 / 4. Temper codes: H1 strain-hardened, H2 strain-hardened and partially annealed, H3 strain-hardened and stabilised [HBAL03 Tab.2 p.263]. *Conflict flagged:* 1100-O UTS is 75 MPa here but ≈ 90 MPa in [Pol06 p.129]; both are within a normal supplier spread, so do not calibrate to either alone.

**Relevance to the slug route.**
- The **lacquer bake (220 °C/10 min)** sits in the recovery range of the DSC anchor (100–250 °C for 99.998 % Al [HH Fig.6.3]). Recovery needs no incubation [HBAL03 p.217], so the heavily worked can wall will start to recover at once. In pure Al recovery can remove up to ~40 % of the work-hardening increment [HBAL03 p.217]; how much happens in 10 min at 220 °C is not quantified in the sources. In Mg + Si-bearing slugs (T11) solute clustering may offset part of this (T11 §2.2 item 3; hypothesis).
- A **slow heat-up of the slugs** spends time in the recovery range and lowers the RX driving force before nucleation; §4.3 and §8.2 show the cost (10× slower RX in 99.998 % Al) [HBAL03 p.236].

### 2.4 Pitfalls
- **Apparent Q from recovery data is often meaningless** [HH p.185]:
  - property ≠ microstructure;
  - annihilation and rearrangement run concurrently;
  - recovery is heterogeneous (Kuhlmann);
  - Q rises during the anneal (Fe: 91 → 220 kJ mol⁻¹ [HH p.177]).
- Junit08 fitted "Friedel's model" to AA1100 (5 % compression; 100–250 °C; 1–4 h) and obtained **Q = 733 kJ mol⁻¹ (X vs 1/T) and 225 kJ mol⁻¹ (X vs ln t)**. A reverse calculation from Nes's graph gave 518 kJ mol⁻¹ [Junit08 abstract p.vii; §2.7 pp.13–14]. All three exceed Q_self = 142 kJ mol⁻¹ [HH Tab.5.1] by up to 5×.
  - **Method, now confirmed by the full-text pass:**
    - Specimens were AA1100 cylinders, Ø10 × 25 mm (about 50 of them), annealed at 413 °C for 1 h (heated at 5 °C min⁻¹, furnace cooled) [Junit08 §3.2–3.3 pp.15–19].
    - They were pre-strained in compression by 2.5, 5, 7.5 or 10 % (50 kN machine, triplicates) [§3.4 p.20].
    - Recovery anneals were done in a box furnace: 100/150/200/250 °C for 1 h at 5 % strain; 1–4 h at 150 °C; and the strain series at 150 °C/1 h. All were heated at 5 °C min⁻¹ [§3.5 pp.20–21].
    - The specimens were then re-compressed. The degree of recovery is X_rec = (σ_m − σ_r)/(σ_m − σ_o), using yield stresses [§2.6 p.11; §3.7 p.21].
    - The model used is X_rec = C₁ ln t − Q/RT, with R = 8.314 J mol⁻¹ K⁻¹ [§2.6 p.11]. Q was taken as **−(slope of X_rec in % vs 1/T) × R**. For example, the Nes graph read at 1 h gives y = −62303x + 168.6, so Q = 62303 × 8.314 = 518 kJ mol⁻¹ [§2.7 pp.13–14].
  - **Re-assessment (corrected after full-text pass).** The values are not activation energies, for three reasons:
    1. **C₁ is ignored.** (general knowledge) In the dimensionally consistent form X = C₁ ln(t/t₀) with t₀ = τ₀ exp(Q/RT), the 1/T-slope at fixed t is −C₁Q/R. The correct extraction is therefore Q = −R·(∂X/∂(1/T))_t / C₁, with C₁ = (∂X/∂ ln t)_T in the same units. In the printed form [HH eq.6.7; Junit08 p.11] the Q/kT term carries no C₁. The "Q" read from its 1/T-slope is therefore C₁ times the time–temperature-equivalence activation energy (general knowledge).
    2. **The result depends on units.** (derived) Expressing X in % instead of as a fraction multiplies the "Q" by 100. The same Nes slope with X as a fraction gives 5.2 kJ mol⁻¹.
       - A least-squares fit of the nine data points that are in the file (Tables 4.1–4.3, 100–200 °C, 1 h, 5 %) gives a slope of −9.2×10⁴ K with X in %. That is 767 kJ mol⁻¹ by Junit's rule, close to the reported 733 (which also used the 250 °C points, not in the file). With X as a fraction the same rule gives 7.7 kJ mol⁻¹.
       - C₁ would come from the 150 °C time series (Tables 4.5–4.8, pp.27–28), which is not in the file. A corrected Q therefore **cannot be computed** from this source.
    3. **The data are noisy and the anneals non-isothermal.** (derived from Tables 4.1–4.3, p.24)
       - The annealed reference σ_o scatters from 22.8 to 64.7 MPa between nominally identical specimens, while σ_m is 107–113 MPa. The denominator σ_m − σ_o (45.9–90.1 MPa) therefore drives the X scatter: X_rec spans 7–26 % at 100 °C and 54–87 % at 200 °C.
       - At 5 °C min⁻¹ the ramp to 250 °C takes about 45 min, comparable with the 1 h hold, so "t" is ill-defined.
  - **Usable content only:** mean X_rec after 1 h at 5 % compression is 14 % (100 °C), 19 % (150 °C) and 68 % (200 °C) (derived means). These are a qualitative anchor showing that lightly strained CP Al softens substantially by recovery at about 200 °C/1 h.
  - **Do not use these Q values.** Use the Q-extraction rule in §11 row 24 instead.

---

## 3. Nucleation of recrystallisation

### 3.1 Mechanisms (Al-relevant)
- **Classical criteria:**
  - *thermodynamic*: the local stored energy must exceed a critical fraction of the maximum;
  - *kinetic*: a mobile HAGB (>15°) must exist next to the nucleus.
  - These are implemented in CA models as "ρ > ρ_crit and Δθ > 15° to 1st–3rd neighbour shell". Such models create no new orientations [SimRX pp.6–7].
- **Sites in rolled Al** [Pol06 p.42, Fig.2.4]:
  - (a) transition bands;
  - (b) coarse intermetallics (PSN);
  - (c) prior grain boundaries;
  - (d) shear bands.
  - **(a) and (b) dominate, and the final texture is a competition between them.**
  - New grains may also form by extended recovery: subgrain growth and coalescence until HAGBs develop [Pol06 p.42].
- **Cube nuclei form preferentially at transition bands** (EBSD-confirmed) after cold rolling and probably also after warm or hot rolling [Pol06 pp.39, 42]. The Dillamore–Katoh mechanism (cube-centred transition bands) is the origin of cube RX texture [HH §2.7.3 p.42].
- **Shear bands** are "a major nucleation site for recrystallized grains" [HH §2.8.2 p.46]. They give a random nucleus texture with a non-random misorientation distribution [SimRX p.3].
- **Grain-boundary bulging** is shown for DRX onset in Nimonic 80A [Bom08 p.323], a method illustration only.
- **Strain-induced boundary migration (SIBM) in Al** (corrected after full-text pass: previously marked general knowledge). Where the dislocation density differs strongly across an existing HAGB (low strains with uneven strain partitioning between grains, or orientation-dependent recovery after heavy strain), the boundary bulges into the side of higher density. The subgrain behind it grows beyond the critical size and becomes a nucleus. Observed in **20 %-compressed 99.99 % Al** (Bellier & Doherty 1977) [HBAL03 pp.222–223].
- **Subgrain coalescence** produces a subgrain larger than the critical size by climb-out of the dislocations in the shared walls (with a slight rotation); repeated coalescence turns its boundary into a mobile HAGB [HBAL03 p.222, Fig.11].
- **Classical critical nucleus radius** [HBAL03 eq.7–8 p.221]: ΔF = −(4/3)πR³F_s + 4πR²γ, so R_c = 2γ/F_s.
  - Mao's estimate: F_s = 1.53×10⁶ J m⁻³ (ρ = 10¹⁵ m⁻²) and γ = 0.6–1.9 J m⁻² give **R_c ≈ 1–3 µm**, "approaching the size order of deformation cells" [HBAL03 p.221].
  - With this KB's constants (γ = 0.324 J m⁻² [HH Tab.4.2]; F_s ≈ 1.0–7 MPa, §1.2) R_c ≈ 0.09–0.6 µm (derived).
  - R_c is smaller where ρ is locally higher; this is why **grain boundaries and particles are the preferred (heterogeneous) sites** [HBAL03 pp.222–223]. Shown: nuclei along grain boundaries (high-purity Al–0.008 Cu; forged Al–0.01 Ti) and **around second-phase particles in rolled Al–1.3 wt % Mn** (P. Yang 1996; Engler, Yang & Kong 1996) [HBAL03 p.223, Fig.12].
- **Particles can accelerate RX.** Particles normally retard boundary migration, but where they trigger "drastic heterogeneous nucleation" RX is faster overall; observed with Al₂Cu and Al₃Fe particles [HBAL03 p.226].
- **Continuous (in-situ) RX** [HBAL03 pp.228–229]: when HAGB migration is blocked (e.g. by precipitates), only "extremely strong recovery" occurs; HAGBs form slowly by subgrain coalescence and the **deformation orientations are kept** (no new texture).
  - 99.9 % Al forged 25 % in two perpendicular directions: continuous RX complete after ~40 min at 350 °C; Fe- and Si-bearing precipitates on the original boundaries blocked migration [HBAL03 pp.228–229, Fig.15].
  - High-purity Al–Fe (Ito, Musick & Lücke 1983): continuous RX is obvious **around 400 °C once Fe exceeds 0.01 wt %**, because many FeAl₃ particles form on the boundaries [HBAL03 p.229].
- **PSN (particle-stimulated nucleation)** [HH §2.9.3–2.9.4 pp.57–64; Pol06 p.42; HBAL03 PDF p.142]:
  - Requires non-deformable particles that develop a **deformation zone**: a rotated, finely subdivided, highly misoriented region about one particle diameter thick.
  - **d < 0.1 µm: no zones** (relaxation by prismatic loops).
  - **0.1–2.5 µm: zone misorientation depends on size and strain.**
  - **d > 2.5 µm: zone misorientation depends on strain only** (Humphreys 1979a, single crystals) [HH pp.60–61].
  - In rolled polycrystals the zone is elongated in RD, holds subgrains below 0.1 µm close to the particle, and shows 30–40° misorientation to the matrix even after large strains [HH §2.9.4.3 p.62; Fig.2.38 AA1200 75 % CR, 3 µm particle].
  - Practical PSN threshold: **"coarse intermetallic compounds having sizes generally greater than about 1 µm"** [Pol06 p.42].
  - Two conditions apply [Pol06 p.42]:
    - (i) the zone's stored energy must allow rapid subgrain migration;
    - (ii) the nucleus must be large and stable enough to grow into the lower-energy matrix.
  - The PSN-capable particle size **decreases with lower deformation T and higher strain rate** [HBAL03 PDF p.142].
  - PSN generally **randomises texture** (it deviates from cube) [HBAL03 PDF p.143; Leh06 p.177].
  - **Supply of PSN-size particles.** Constituent diameters are "usually from 1 to 30 µm". They become **smaller with faster solidification, with lower Fe and/or Si, and with more deformation** [HBAL03 p.122].
  - **Hot-rolled AA3104** (can body): lowering the rolling T or raising the speed to suppress inter-stand RX brings in PSN, and the texture moves from cube to the random PSN texture. Where that transition lies depends on the forming conditions and on the state of precipitation [HBAL03 pp.356–358, Figs.4–5]. Only the figures carry the numbers, and they are not extractable.
  - **Industrial PSN route (AA7475 superplastic sheet)** [HBAL03 p.1116]: overaged coarse precipitates, then ~80 % warm work at ~200 °C, then **rapid heating** to 480 °C. This gives many PSN nuclei and 10–15 µm grains; 0.1–0.2 µm Cr dispersoids then limit grain growth.
- **Fine dispersoids or precipitates inside deformation zones suppress PSN.**
  - In 1xxx, Si precipitating before or during annealing (fine Al–Fe–Si or Si) impedes RX within deformation zones, giving fewer effective nuclei [HBAL03 PDF p.152].
  - "Through secondary fine precipitates during RX the effect of primary particles can be suppressed", so RX texture is controllable by alloying and processing [Leh06 p.178].
- Nucleation in statistical texture models falls into three classes [SimRX pp.2–3]:
  - random (random texture and misorientation);
  - shear-band (random texture, non-random misorientation);
  - pre-existing nuclei (texture similar to the deformation texture, narrow misorientation).

### 3.2 Quantitative (deformation zones, from HH)
- Misorientation decay from the particle surface: tan θ = tan θ_max · exp(−c₁x/d), c₁ = 1.8 [HH eq.2.21 p.61].
- d > 2.5 µm: θ_max = c₂ tan⁻¹ s, c₂ ≈ 1 (s = shear strain) [HH eq.2.22 p.61].
- 0.1 < d < 2.5 µm: θ'_max = 0.8 θ_max (d − 0.1)^0.2, d in µm [HH eq.2.23 p.61].
- Orientation gradient: dθ/dx = (c₁ tanθ_max cos²θ/d) · exp(−c₁x/d).
- Dislocation density in the zone: ρ(x) = (2c₁ tanθ_max cos²θ/(b d)) · exp(−c₁x/d) [HH eq.2.24–2.25 p.62].
- Brown (1997) dislocation model: tan θ = (tan s/2) · ln(d/x) [HH eq.2.26 p.63].
- CPFEM reproduces the zone rotations but lacks a length scale; gradient plasticity does not reproduce the small-particle cutoff [HH §2.9.4.4 pp.63–65].
- **PSN nucleation efficiency (nuclei per particle) and the strain dependence of the critical particle size** sit in HH §9.3, which is **not extracted**. The full HBAL03 text (2026-10-12) does not supply them either: Mao treats particle nucleation only qualitatively [HBAL03 pp.223, 226]; ch. 3 gives only the direction of the T and strain-rate dependence [HBAL03 p.130]; ch. 7 gives the AA3104 cube/PSN maps as figures [HBAL03 pp.357–358]. Hence it is still a gap (§12 item 4). As an orientation only: **(general knowledge) efficiency is typically ≤ 1 nucleus per particle, with a critical diameter of order 1 µm at moderate strains, decreasing with strain.**

### 3.3 Design levers
- **For fine, equiaxed, near-random grains** (formability, low earing contribution from PSN, uniform anodising/brazing response):
  - maximise the number density of particles **> ~1 µm** (Fe- and Si-bearing constituents, α-Al(Fe,Mn)Si);
  - use high cold reduction;
  - avoid fine precipitation inside the deformation zones before RX (i.e., anneal fast, with Mn and Si already precipitated or kept in solution, see §5).
  - In 1xxx sheet, more Fe/Si as constituents gives more PSN-capable particles and finer annealed grain [HBAL03 PDF p.152, Fig.47].
- **For strong cube** (cube/rolling-texture balance for earing; directional properties): promote transition-band nuclei and suppress PSN. This means lower constituent density, or **fine dispersoids/secondary precipitates that neutralise deformation zones** [Leh06 p.178; HBAL03 PDF p.143].
- **For coarse grains** (sag resistance, crack deflection, creep; see §5): reduce nucleus density. Use few large particles, low strain, and precipitation that pins sub-boundaries before nucleation.

**Relevance to the slug route.**
- Three features of the route each push toward **fewer PSN nuclei**, and hence a coarser slug grain:
  1. the cold reduction is low (30–50 %, ε ≈ 0.36–0.69), which raises the critical particle size (general-knowledge direction, §3.2);
  2. rotary-caster solidification is faster than DC, which makes the constituents finer [HBAL03 p.122];
  3. fine Fe/Mn/Si precipitates forming in the deformation zones during a slow heat-up cancel nuclei [HBAL03 PDF p.152].
- Against this, stored energy that survives from the hot mill (§9) adds driving force (inference).
- T11's ≈ 1.5–2 vol % of Fe-rich constituents (T11 §2.2) is a large PSN reservoir only if a good share of them is ≥ ~1 µm. **Measure the constituent size distribution in the cold-rolled strip** (fraction ≥ 1 µm, number per mm²); it is the main input for a nucleation-density grain-size model (§4.2, eq.22).

### 3.4 Pitfalls
- Measured angle–axis misorientations at particles (30–40°) can underestimate the physical rotation, because random cubic orientations average about 40° [HH p.63].
- Large inclusions also nucleate *deformation bands* [HH §2.9.2.3 p.56].
- Constituent stringers are aligned in RD after breakdown [Pol06 p.78], so PSN nuclei come in clusters, which gives banded grain sizes.

---

## 4. Growth of RX grains, RX kinetics (JMAK) and RX temperature

### 4.1 Boundary mobility and growth
- Boundary velocity is v = M P, with P the net pressure: stored energy minus Zener and solute retarding pressures. This is valid for Al: Demianczuc & Aust; in-situ SEM by Huang & Humphreys [HH eq.5.1 p.123].
- M = M₀ exp(−Q/RT) [HH eq.5.2]. In a subgrain-forming alloy, P can be computed from EBSD subgrain size and misorientation with eq.2.8 [HH §5.1.4 p.124].
- **HAGB migration Q in high-purity Al:** 63 kJ mol⁻¹ (RX, 273–350 K) and 67 kJ mol⁻¹ (capillarity, 615–705 K). This is about Q_boundary-diffusion, i.e. about half of bulk diffusion [HH Tab.5.2 p.135].
  - With solute, Q at higher concentration approaches self-diffusion or solute diffusion [HH §5.3.3 p.147].
  - Turnbull reaction-rate form: M = (A_J A_A ν b/kT) exp(−H_a/kT) exp(ΔS/k) [HH eq.5.18 p.155].
- **Mao's atomic-jump estimate of the RX front velocity** [HBAL03 eq.9–12 p.224]:
  - net jump rate across the boundary, biased by the stored energy per atom F_sa: V = b ν c_v [exp(−(Q_a − F_sa)/kT) − exp(−(Q_a + F_sa)/kT)] ≈ **2 b ν c_v (F_sa/kT) exp(−Q_a/kT)**, because F_sa ≪ kT. This is v = M·P with M ∝ c_v exp(−Q_a/kT)/kT (derived);
  - inputs: ν ≈ 10¹³ s⁻¹; vacancy fraction c_v ≈ 10⁻⁵ at 700 K and 10⁻⁴ at 800 K; **Q_a ≈ 45 kJ mol⁻¹** (printed "4.5×10⁴ J/m", i.e. 7.47×10⁻²⁰ J per atom, so J mol⁻¹ is meant);
  - results: **0.08 µm s⁻¹** (heavily deformed, ρ = 10¹⁵ m⁻²) and **0.01 µm s⁻¹** (recovered) at **700 K (427 °C)**; **1.85 and 0.28 µm s⁻¹** at **800 K (527 °C)**; ≈ 0.8 µm s⁻¹ for ρ = 10¹⁶ m⁻². Mao says these "approach the order of practically observed velocity" in Al;
  - check (derived): the printed values are reproduced with F_sa = F_s·a³/4 (a = 0.404 nm, i.e. the atomic volume) and F_s = 1.53 MPa;
  - limits: the model ignores solute, particles and misorientation [HBAL03 p.225]. Its Q_a (45 kJ mol⁻¹) is below the measured 63–67 kJ mol⁻¹ for high-purity Al [HH Tab.5.2]. Use it only for **trends**: v ∝ stored energy (recovery cuts v by ~7×), and v rises ~23× from 427 to 527 °C (derived from the printed values).
- **Orientation dependence:**
  - **40°<111> boundaries** grow fastest in deformed Al, with a broad peak (±10°) in RX vs ±0.2° in curvature-driven bicrystals [HH §5.3.2.1 pp.137–142].
  - Tilt boundaries are about 10× faster than twist boundaries, which gives lenticular grains [HH §5.3.2.2 p.143].
  - High-purity Al below 150 °C: 28–38°<100> growth instead [HH p.138].
  - The orientation dependence arises mainly from **orientation-dependent solute segregation**: in 99.99995 % Al the mobility is orientation-independent above 20° [HH §5.3.3.3 p.149]. It disappears at high T (atmosphere evaporation) [HH p.150].
  - SimRX models set average HAGB mobility = 20 % of the special (40°<111>) maximum and treat LAGBs as immobile [SimRX p.3–4].
- **Solute drag (Cahn–Lücke–Stüwe)** [HH §5.4.2 pp.159–165]:
  - Atmosphere: c = c₀ exp(−U/kT). Segregation increases as solubility decreases (Hondros–Seah).
  - Low velocity: P = v/M + α c₀ v, so **v ∝ 1/c₀** (confirmed for Al–Cu, Gordon & Vandermeer). Q ≈ that of solute diffusion.
  - Breakaway at high v: P = v/M + c₀/(α′v)-type; mobility returns to the intrinsic value.
  - Combined: P = v/M + α c₀ v/(1 + β² v²).
  - The drag force peaks at an intermediate v. The S-shaped v–P curve gives discontinuous velocity jumps at high c₀. Solute drag weakens at high T.
  - Valid for dilute solutions (c₀ < 0.1 %). Molodov 1998: Q rises with small additions in high-purity Al (interaction of adsorbed atoms).
  - **Cu and Mg in Al** show a very sharp low/high-mobility transition with concentration, and the apparent Q peaks at the transition (an artefact, not a mechanism). Ag and Fe show gradual transitions (Frois & Dimitrov; Montariol) [HH §5.3.3.1–2 pp.145–148].
  - Numeric drag coefficients per element (Mn, Mg, Cu, Fe, Si) are **not extractable** (figures only); see Gaps.
  - **Confirmed in HBAL03** [pp.225–226, 248]: v is inversely proportional to the Cu content (Gordon & Vandermeer); raising Cu in zone-refined Al from 4.3 to 258 at. ppm clearly lowers the boundary velocity; the boundary breaks free when the driving force makes it too fast for the solute atmosphere to follow (Lücke et al. 1972); segregation c_B = c·exp(−Q_B/kT), with Q_B < 0 for attracted solute (Lücke & Detert 1957, eq.36). In 99.99995 at % Al the HAGB velocity is high and orientation-independent; at 99.9992 at % it drops clearly except near low-Σ coincidence orientations (Fridman et al. 1975).
  - **Fe in solution is extraordinarily potent** [HBAL03 p.220] (Därmann 1984, as quoted): deformed high-purity Al recrystallises in **50 s at 150 °C**, while deformed **Al–0.01 at % Fe would need more than 10 billion years** at 150 °C. The figure is an extrapolation, not a measurement, but it shows that ~100 at. ppm of Fe changes the RX time at a fixed temperature by many orders of magnitude. Commercially pure Al recrystallises at 200–300 °C; zone-refined Al even at room temperature [HBAL03 p.220].
- Triple-junction drag matters only for nanocrystalline material (≤ 50 atomic spacings). Grain- and subgrain-growth Q in Al ≈ self-diffusion, i.e. boundary-controlled [HH §5.5 pp.165–167].

### 4.2 JMAK kinetics
- Statistical JMAK models convert an "extended" (unimpinged) RX volume into the real volume, assuming random spatial nucleation. Orientation-resolved versions (Bunge–Köhler; Sebald–Gottstein growth selection) predict RX texture but ignore topology and neighbourhood [SimRX pp.2–4].
- **Johnson–Mehl derivation (now sourced; corrected after full-text pass, previously general knowledge)** [HBAL03 eq.13–22 pp.226–228]:
  - definitions: N = (dn/dt)/(1 − X), the nucleation rate per unit volume of *untransformed* matrix; v = dR/dt;
  - for constant N and v and spherical growth from random sites: **X = 1 − exp(−(π/3) N v³ t⁴)**, i.e. **n = 4**;
  - characteristic time t_c = (3/(π N v³))^¼, so X = 1 − exp(−(t/t_c)⁴); X(t_c) ≈ 63 %;
  - **RX grain size:** grains impinge at about t_c, so d = 2 v t_c. Printed as **d = 2(2v/(πN))^¼** [eq.22]; consistency with eq.20 requires 2(3v/(πN))^¼ (derived; the difference is a factor 1.11). Either way **d ∝ (v/N)^¼**: the RX grain size rises with growth rate and falls with nucleation rate, but only with the fourth root;
  - N and v are **not constant** in real Al [HBAL03 p.227] (Anderson & Mehl 1945), so the derivation is a guide, not a fit law.
- **Industrial (steel-type) form used for hot-rolling models** [HBAL03 eq.1–4 pp.359–360]:
  - X = 1 − exp(−C (t/t₀.₅)^k), where C = ln 2 if t₀.₅ is the time to X = 0.5 (derived);
  - t₀.₅ = a·ε^(−b)·d₀^c·Z^(−d)·exp(Q_rex/RT), with Z = ε̇·exp(Q_def/RT) (the rate dot is lost in the printed eq.3);
  - d_rex = e·d₀^f·ε^(−g);
  - a–g, Q_rex and Q_def are fitted constants; **no Al values are given**. For Al these equations work "in limited cases"; Sellars found them to predict **unrealistically large grain sizes**. Al models need particle precipitation/dissolution and the nature of the nucleation sites [HBAL03 p.360].
- **Still general knowledge:** n = 3 for site-saturated 3D growth; t₅₀ = (ln2/k)^(1/n) for X = 1 − exp(−k tⁿ) with k = k₀ exp(−nQ/RT); measured n in commercial Al alloys commonly 1–2 because of clustered nucleation, recovery during annealing and concurrent precipitation. A literature value from the web chapter: n fell from 3.0 at 371 °C to 0.8 at 427 °C in deformed, supersaturated Al–Mn under concurrent precipitation (ch12 §4, [W12-19], abstract only). HH §7.3–7.4 (Cahn–Hagel, microstructural path methods) is still **not extracted**, and HBAL03 gives **no Q_rex or n values for Al alloys**.
- Spatially resolved alternatives [SimRX pp.4–11]:
  - cellular automata (probabilistic switching from a linearised rate equation; can be coupled to CPFEM for Al);
  - Potts Monte Carlo (H = J/2 Σ(1 − δ) + H_El·f; Metropolis W = exp(−ΔE/kT));
  - vertex/front tracking (overdamped v = M·p, Herring junction equilibrium).
  - "Discreteness ≠ precision: the physics is in the constitutive description" [SimRX p.4–5].

### 4.3 RX temperature and time: anchor data for calibration

| Material / state | RX observation | Source |
|---|---|---|
| Hard-rolled pure Al sheet | RX complete in "several hours at 280 °C, a few minutes at 380 °C, seconds at 500 °C" | [Pol06 p.42] |
| → apparent Q from the above | **≈110–150 kJ mol⁻¹ (derived; assuming 3–5 h / 2–3 min / ~5 s)**, i.e. close to Q_self = 142 | derived |
| Commercial Al alloys | anneal 300–420 °C [Pol06 p.42]; 345–415 °C intermediate anneal for minutes to 3 h [Pol06 p.107]; 350–420 °C [Pol06 p.109] | Pol06 |
| Non-heat-treatable alloys, general | above ~350 °C RX in addition to recovery | [W7 §1.2 p.5] |
| 99.998 % Al, 75 % compression, 6 °C min⁻¹ | recovery 100–250 °C, RX peak ≈300 °C | [HH Fig.6.3 p.172] |
| AA3103 (Mn_ss 0.20 at %, hom. B), ε = 2 | fully RX in **45 s at 400 °C** (salt bath) to **6 µm**, weak cube, no change in conductivity, i.e. no concurrent Mn precipitation | [Ryen03 §3.4 p.56; Tab.4.2 p.66] |
| AlMg0.5 / AlMg3, ε = 2 | RX in 25 s at 400 °C; finest grain sizes listed are 10 / 8 µm (attributing these to the ε = 2 route is the compiler's inference) | [Ryen03 §3.4; Tab.4.2] |
| AA1100 (CP Al), 5 % compression | recovery-only 100–250 °C / 1–4 h; after 1 h X_rec is 7–26 % (mean 14 %) at 100 °C, 17–22 % (19 %) at 150 °C and 54–87 % (68 %) at 200 °C. The 250 °C data (Table 4.4, p.25) are not in the Drive file. Noisy (§2.4) | [Junit08 Tab.4.1–4.3 p.24; means derived] |
| Deformed high-purity Al vs Al–0.01 at % Fe | 150 °C: 50 s vs > 10¹⁰ years (extrapolated, Därmann) | [HBAL03 p.220] |
| Commercially pure Al; zone-refined Al | RX at 200–300 °C; zone-refined even at RT | [HBAL03 p.220] |
| 99.998 % Al, 95 % CR, 300 °C | "after primary RX" at **316 s** by direct annealing; after a 240 °C/600 s recovery pre-anneal (no RX) it needed **3162 s** at 300 °C (~10× slower). Fig.24 of the same chapter still shows grains growing into deformed matrix at 316 s, so treat 316 s as order of magnitude | [HBAL03 pp.236, 238; Tab.2, Figs.22, 24] |
| 99.9 % Al, forged 25 % in two directions | continuous (in-situ) RX complete after ~40 min at 350 °C | [HBAL03 p.228] |
| High-purity Al–Fe, Fe > 0.01 wt % | continuous RX around 400 °C (FeAl₃ on boundaries) | [HBAL03 p.229] |
| **Al–1 wt % Mn, 95 % CR** | primary RX **complete after 1 s at 620 °C**, 87 % cube | [HBAL03 p.251] |
| Al–3 wt % Mg, 95 % CR | primary RX complete after 200 s at 300 °C | [HBAL03 p.252] |

**Soft-annealing practice (O temper) [W7 Tab.2 p.21].** Metal temperature, time at metal temperature. Heat-up "as short as possible" (avoid coarse grain); below 250 °C cool at any rate.

| Alloy | T (°C) | t (h) | Cooling |
|---|---|---|---|
| 1098 (Al99.98) | 290–310 | 0.5–1 | furnace |
| Al99.9 | 320–350 | 0.5–1 | furnace |
| 1080A / 1070A / 1050A | 320–350 | 0.5–2 | furnace |
| 1350A / 1200 | 340–360 | 0.5–2 | furnace |
| **8011A (AlFeSi)** | **340–400** | 1–2 | furnace |
| **3207, 3103, 3003, 3105, 3005, 3004** | **380–420** | **0.5–1** | furnace |
| 5005A…5754, 5049, 5454 | 360–380 | 1–2 | furnace |
| 5086 / 5083 / 5182 | 380–420 | 1–2 | 5083/5182: 30–50 °C h⁻¹ |
| 6xxx | 360–420 | 1–2 | ≤30 °C h⁻¹ to 250 °C |
| 2xxx / 7xxx | 380–420 | 2–3 | ≤30 °C h⁻¹ (7xxx + 230 °C hold) |

**Annealing practice in HBAL03 (added after full-text pass).**
- **Principles** [HBAL03 §3.2 p.887]:
  - annealing is done above the RX temperature, which depends on the prior strain;
  - commercial practice uses "the lowest temperature that yields the softest state in the minimum amount of time";
  - **non-heat-treatable wrought alloys are heated to temperature very quickly to avoid grain growth**, because a fine grain size is wanted;
  - the cooling rate after the anneal is "unimportant" for these alloys.
- **Table 7 (°F converted to °C, derived)** [HBAL03 p.888]. Footnote /1 on the NHT entries: hold "no longer than to get the center of the furnace load up to temperature"; cooling rate not important.

| Alloy | Anneal T (°F) | ≈ °C (derived) | Time |
|---|---|---|---|
| 1060, 1100, 1350 | 650 | 343 | load at temperature |
| **3003** | **775** | **413** | load at temperature |
| **3004, 3105** | **650** | **343** | load at temperature |
| 5005–5652 (all 5xxx listed) | 650 | 343 | load at temperature |
| 2xxx (except 2036 at 725 °F), 6xxx, 7xxx | 760 | 404 | 2–3 h, then slow cool (footnotes /2, /3) |

- **Al–Mn alloys** [HBAL03 Tab.37 p.299]:

| Alloy | Mn (wt %) | Mg (wt %) | Anneal | UTS O / H (MPa) | YS O / H (MPa) | El. O / H (%) |
|---|---|---|---|---|---|---|
| 3003 | 1.0–1.5 | — | 400–600 °C | 110 / 150 (H14) | 42 / 145 | 35 / 12 |
| 3004 | 1.0–1.5 | 0.8–1.3 | 415 °C | 180 / 240 (H34) | 70 / 200 | 22 / 11 |
| **3105** | **0.2–0.8** | **0.2–0.8** | **345 °C** | **115 / 170 (H14)** | **55 / 150** | **24 / 5** |

  Footnote: all contain up to 0.25 % Cu, 0.70 % Fe "and 0.3–0.6 % as impurities" (the element is missing in the print).
- **Conflict flagged (within HBAL03 and against W7):**
  - 3004: 415 °C [p.299] vs 343 °C [p.888];
  - 3003: "400–600 °C" [p.299] vs 413 °C [p.888];
  - W7 gives 380–420 °C for the whole 3xxx group [W7 Tab.2].
  - The 343 °C entries fit the "lowest T for softest state" rule with time only to bring the load to temperature; 400–420 °C fits the 0.5–1 h holds of W7. **Treat 345–420 °C as the commercial window for lean 3xxx and set the actual value by an isochronal trial.**
- **Relevance to the slug route.**
  - 3105 (Mn 0.2–0.8, Mg 0.2–0.8) is the registered alloy closest to the lean slug alloys. Its O-anneal of 345 °C [p.299; p.888] is a useful lower anchor for T11 (Mn 0.14, Mg 0.26), but T11's Fe and Si retained in solution by the quench (§5) can push the RX temperature up.
  - "Cooling rate unimportant" [p.888] does **not** hold for Mg + Si-bearing slugs: T11 has a Mg₂Si potential, so the cooling rate after the anneal sets the hardness (T11 §2.3 item 2).

### 4.4 Factors controlling RX (sourced)
- **Strain.** A critical strain exists (Sauveur 1912). Grain size falls with prior strain (Charpy; Carpenter & Elam) [HH §1.2.1.3 pp.5–6]. The "Rekristallisationsschaubild" (grain size vs strain and T at fixed time) is the standard design map [Prakt05 p.9].
- **Temperature/time.** RX starts at a "definite temperature" that depends on composition, time and work hardening [Pol06 p.41]. Too-long annealing gives coarse grain [W7 p.5].
- **Heating rate.**
  - Texture and final grain size depend on heating rate, T and time [Pol06 p.39].
  - Slow heating lets dispersoids form before RX [Røy05 p.35].
  - The AMAG coil anneal (300–400 °C, 2–5 h) before a fast continuous solution treatment gave coarse elongated grains vs fine equiaxed grains without it (AA2024) [AMAG14 p.14].
  - Non-heat-treatable alloys are heated "very quickly to avoid grain growth" [HBAL03 p.887].
  - **Recovery before RX** lowers the driving force: RX of 95 % CR 99.998 % Al at 300 °C took ~10× longer after a 240 °C/600 s pre-anneal, and the texture became sharper (§8.2) [HBAL03 p.236].
- **Strain and temperature in the JM picture.** d ∝ (v/N)^¼ [HBAL03 eq.22 p.228]. *Inconsistency flagged:* the text says Anderson & Mehl found "the ratio v/N is increased with increasing tensile deformation or with arising annealing temperature, which would result in refined grain size" [HBAL03 p.228]. By the chapter's own eq.22 a larger v/N gives a **coarser** grain, so either "v/N" should read "N/v" or "refined" is wrong. Do not quote this sentence as evidence. That the RX grain size falls with prior strain is supported independently [HH §1.2.1.3 pp.5–6].
- **Solute.** Fe in solid solution raises the RX start temperature by precipitating fine Al–Fe particles during the anneal (high-purity 1xxx) [HBAL03 PDF p.152]. Mn raises the RX temperature and promotes fibrous structures [Dav01 p.382]. Cr and Mn raise RX temperatures in 5xxx [Pol06 p.130].
  - **Fe reduces the grain size in wrought products.** In 8006-type Fe+Mn alloys near the ternary eutectic, the fine grain is "stabilized by the finely dispersed iron-rich second phase" [Dav01 p.379].
  - **Ca at the 0.2 % level "alters the recrystallization characteristics of 3003"**; the direction and size of the effect are not stated [Dav01 p.372]. As a trace element, 10 ppm Ca also raises hydrogen pickup in the melt (ch. 02 §7.1).
  - Mn is a common impurity in primary Al at 5–50 ppm [Dav01 p.382].
  - **Transition-metal effect on the RX temperature (Yelagin, binary alloys cast → 500 °C anneal → hot rolled 420–450 °C → 450 °C anneal → cold rolled)** [HBAL03 p.296, Tab.35]. Maximum increments of RX start / finish temperature:

    | Element | at % at the maximum | ΔT_start (K) | ΔT_finish (K) |
    |---|---|---|---|
    | Mn | 0.77 | +30 | +25 |
    | **Fe** | **0.04** | **+65** | **+35** |
    | Cr | 0.35 | +45 | +30 |
    | Ni | 0.04 | −10 | +5 |
    | Ti | 0.25 | +5 | +180 |
    | V | 0.21 | +15 | +15 |
    | Zr | 0.09 | +105 | +240 |
    | Sc | 0.20 | +120 | +320 |
    | Nb / Mo | 0.12 | +35 / +70 | +35 / +45 |

    - **Period-IV TMs (the 3d row, incl. Mn, Fe, Cr) raise T_RX only above a threshold close to their solubility limit "at a temperature of solution treatment"** (in this series presumably the 500 °C anneal; compiler's reading). Period-V TMs (Zr, Nb, Mo) act even at very small additions, and some TMs show maxima tied to the solubility limit [HBAL03 p.296].
    - Effective "antirecrystallisers" have an incomplete 3d shell with few electrons, a large atomic-radius misfit, a solid solution supersaturated by solidification, and decompose into thermally stable fine dispersoids [HBAL03 p.296].
    - Interpretation (inference): the small Mn increment (+30 K at 0.77 at %) reflects a route in which Mn was largely precipitated and coarsened at 500/450 °C **before** cold rolling. In a route without homogenisation (rotary casting + quench), Mn and Fe stay in solution and can precipitate **during** the anneal, which is the more retarding sequence (§5.2). Expect larger increments than Table 35 shows.
- **Particles.** See §3 and §5.
- **Furnace accuracy.** Modern furnaces hold ±2.5 K [Leh06 p.172]. ±5 °C variations in rolling temperature have measurable property effects [AMAG14 p.12].

### 4.5 Pitfalls
- A JMAK fit with one Q over a temperature range that crosses the precipitation C-curve (3xxx) is invalid (see §5).
- Lab salt-bath RX (seconds) ≠ batch coil annealing (hours of ramp), because the precipitation path differs.
- Steel-type t₀.₅/d_rex regressions (§4.2) over-predict Al grain sizes [HBAL03 p.360]. Do not use them without a particle and nucleation-site term.

**Relevance to the slug route.**
- Grain size is set mainly by the **nucleation density** (d ∝ (v/N)^¼ [HBAL03 eq.22]); v enters only weakly. So slug-grain control is about keeping nuclei alive: enough PSN-size constituents (§3), no recovery-dominated slow ramp (§2.3), and no precipitation on the substructure before RX (§5).
- **Anneal-temperature anchors for lean slugs:** 3105 O at 345 °C [HBAL03 p.299]; 3003 at 413 °C and 3004/3105 at 343 °C with time only to bring the load to temperature [HBAL03 p.888]; 380–420 °C for 0.5–1 h [W7]. Al–1Mn at 95 % CR is fully recrystallised in 1 s at 620 °C [HBAL03 p.251], which shows how fast RX can be once the driving force is high and precipitation is avoided.

---

## 5. Concurrent precipitation and RX: the 3xxx key topic

### 5.1 Mn in Al: what is available to precipitate
- Al–Mn eutectic at **1.9 wt % Mn, 657 °C**. Maximum solubility **1.82 wt %**. Commercial Mn is kept **≤1.25 %** because Fe lowers Mn solubility and risks coarse primary Al₆(Mn,Fe), which is "disastrous" for ductility [HBAL03 PDF p.171–172; Pol06 p.129].
- **As-cast 3003 holds 0.7–0.9 wt % Mn in supersaturated solution.** The rest is in Al–Mn–Fe(–Si) constituents [HBAL03 PDF p.172]. AA3103 (1.0 Mn, 0.57 Fe, 0.12 Si) as cast: 0.81 wt % (0.40 at %) Mn_ss [Ryen03 §3.2 p.54]. Chill casting retains most Mn in solution even in large ingots [Dav01 p.382].
- After preheat/hot processing typically **only 0.2–0.3 wt % Mn remains in solution** in 3xxx [HBAL03 PDF p.106; Pol06 p.30].
- **Homogenisation sets Mn_ss** for AA3103 (Sjølstad 2003) [Ryen03 Tab.3.2 p.54]:

| Code | Cycle | Mn_ss (at %) |
|---|---|---|
| AC | as cast | 0.40 |
| A | 100 °C h⁻¹ → 610 °C, 14 h, quench | 0.24 |
| B | A + 20 °C h⁻¹ → 550 °C, 16 h, quench | 0.20 |
| C | B + 20 °C h⁻¹ → 500 °C 24 h → 450 °C 32 h, quench | 0.15 |

- **Equilibrium Mn solubility that sets the supersaturation at the anneal T** [Bel05 Tab.1.13 p.15 and Tab.1.9 p.12; tables verified against the PDF 2026-10-12, see ch. 02 §2.4–2.5]:
  - Mn in (Al) in the (Al)+Al₆Mn+Al₁₅Mn₃Si₂ field: 1.3 wt % at 649 °C, 0.73 at 600, 0.44 at 550, 0.25 at 500, 0.15 at 450 and 0.06 at 400 °C.
  - With free (Si) present: only 0.04–0.08 wt % (400–573 °C).
  - In the Fe-bearing (Al)+Al₃Fe+Al₆(FeMn) field: 0.05 wt % at 527 °C and 0.026 at 427 °C (extrapolated values).
  - (derived; 1 at % Mn ≈ 2.04 wt % in dilute Al) Even the most precipitated AA3103 condition (C-type, 0.15 at % ≈ 0.30 wt % Mn_ss) is supersaturated relative to the 400–450 °C solubility (0.06–0.15 wt %).
  - A 400–450 °C anneal therefore always has a chemical driving force for Mn precipitation. Whether it acts before RX is a question of kinetics: no conductivity change after 45 s at 400 °C in AA3103 [Ryen03 §3.4 p.56], and D_Mn is low (§2.2).
- **Dispersoid phases.** Homogenisation precipitates α-Al₁₂(Mn,Fe)₃Si (or Al₁₅(FeMn)₃Si₂) or Al₆(Mn,Fe) dispersoids, typically < 1 µm; Si < 0.07 % gives Al₆(Mn,Fe) [HBAL03 PDF p.172; Tab.7 p.137].
  - **Si accelerates Mn precipitation**: a denser α dispersion and lower Mn_ss. Si also transforms Al₆(Fe,Mn) into α (harder, important for canstock) [HBAL03 PDF p.172; Pol06 p.107].
  - Higher Fe/Mn favours Al₁₃(Fe,Mn)₄ [HBAL03 PDF p.172].
  - **The non-equilibrium Mn in (Al) after casting (set by composition and cooling rate) determines the amount of dispersoids formed during annealing above 300–350 °C.** In 8006, these are mostly Al₆Mn (negligible Fe solubility) [Bel05 §1.6].
  - When Fe and Si are fully bound in Al₁₅(FeMn)₃Si₂, the Mn and Si in solid solution fix the dispersoid amount; use the Al–Mn–Si diagram for this [Bel05 §1.6].
  - 3003 can be single-phase (Mn < 1 %, Si < 0.1 %), and Mn microsegregation is removable above 540–550 °C. More Si gives excess phases, and a risk of partial melting about 60 °C below the binary Al–Mn solidus [Bel05 §1.6].
- **Faster solidification** (belt or twin-roll casting: 11–40 °C s⁻¹ surface for a 19 mm slab; 10²–10³ °C s⁻¹ for twin-roll) gives finer dendrite cells (5–10 µm vs 30–70 µm DC) and higher supersaturation of Fe/Mn. Different properties result, and a leaner alloy may substitute [Pol06 p.102; Leh06 p.171]. Preheat and hot-rolling practice must be matched to the casting route [Leh06 p.171].
- **Transition-metal (TM) solid solutions** [HBAL03 pp.293–295, 299]:
  - TM supersaturation forms during **solidification** and rises with cooling rate. These solutions are **far more stable** than those of Cu, Mg, Zn, Si or Li after quenching; they decompose between 250 and 650 °C depending on the TM [p.293].
  - **Maximum Mn in (Al) vs cooling rate** (Table 33; "%", presumably wt % since 1.82 equals the equilibrium maximum): 1.82 at 10⁻¹ K s⁻¹; 2.5 at 10 K s⁻¹; 2.8 at 10² K s⁻¹; 3.0–5.0 at 10³ K s⁻¹ [p.294]. The text says that at the 10–100 K s⁻¹ of "modern ingot and casting metallurgy" (Al) is saturated up to the equilibrium limit [p.294], which sits uneasily with the 2.5–2.8 % in the table (flagged).
  - **Al₆Mn:** limit solubility 0.88 at %; decomposition range **300–350 °C**; hardening ΔH/C = 10 per at % (Zr 154, Sc 208) [Tab.34 p.295].
  - In 3xxx ingots (V_c < 10² K s⁻¹) the Mn solid solution **decomposes above 325 °C** to fine Al₆Mn or (AlFeMn) and (AlFeMnSi) dispersoids. There is "no real precipitation hardening", but the dispersoids **hinder grain growth upon RX** and give a fine-grained sheet. High Fe and Si and small Cu and Mg additions also refine the grain [p.299].
  - TMs that form eutectics with Al (**Mn, Fe**, Sc, Ni) decompose at lower T and faster than peritectic formers (Cr, V, Zr, Ti, Mo), whose diffusion coefficients are about an order of magnitude lower [p.295].
  - **TM dendritic segregation is not easily removed by homogenisation**; TM diffusion coefficients are 10⁻¹⁴–10⁻¹² cm² s⁻¹ at 500 °C (printed "cm³/sec") [p.295]. This is consistent with D_Mn = 5×10⁻¹³ cm² s⁻¹ [Pol06 p.105].
- **Homogenisation sets the dispersoid population (AA3003)** [HBAL03 p.355]: mean dispersoid size **0.03 µm at a density of 740 µm⁻³** (low-T anneal) vs **0.17 µm at 11 µm⁻³** (high-T anneal). Derived, assuming spheres and "size" = diameter:
  - F_V ≈ 1.0 % vs 2.8 %;
  - F_V/r ≈ 0.70 vs 0.33 µm⁻¹;
  - P_Z = 3F_Vγ/2r ≈ 0.34 vs 0.16 MPa (γ = 0.324 J m⁻²).
  
  The low-T population pins about twice as hard. The size range "strongly affects recrystallization during and after hot rolling" [p.355]. *Caution:* the implied F_V *rises* after the high-T anneal, although Mn solubility rises with T. The source's size or density definitions may therefore differ from the assumptions above, so treat these derived values as order-of-magnitude only.

**Relevance to the slug route (Mn/Fe budget).**
- Any realistic caster cooling rate keeps far more Mn soluble than T11 (0.14 Mn) or lean 3xxx (≤ 0.5 Mn) contain [HBAL03 Tab.33]. Whatever Mn is not tied up in Fe-rich constituents during solidification therefore stays in solid solution through casting, the short in-line hot-mill exposure (≈ 500 → 380 °C) and the quench.
- Fe solubility is tiny (max ≈ 0.05 % [HBAL03 PDF p.150]), but rapid solidification also retains some Fe in supersaturation (general knowledge; not quantified in HBAL03 Tab.33). Per at % present, Fe gives the largest RX-start increment in Table 35 (+65 K at only 0.04 at %; ranking derived).
- Both decompose in the slug-anneal range (Mn above ~325 °C [p.299]; Al₆Mn 300–350 °C [p.295]). That is the classical "precipitation competes with RX" situation of §5.2 (inference).

### 5.2 Physical principle of the precipitation/RX interaction
- Stored energy (~10⁵ J m⁻³ lightly deformed; ~7 MPa for heavily deformed Al, derived) is tiny compared with phase-transformation energies (~1 kJ mol⁻¹). Precipitation at the annealing temperature can therefore have "a profound effect" on RX [HH §2.2.1 p.13; §1.3.2 p.10].
- **Sequencing rule (sourced for Al–Sc/Zr; transferable to Al–Mn)** [Røy05 pp.34–35]:
  1. Solute in solid solution before deformation means dispersoids may nucleate **before** RX nuclei: on direct up-quench, during ramp-up, or in a pre-anneal at intermediate T.
  2. Dispersoids formed **before** deformation at T_disp:
     - if T_ann < T_disp, P_Z ≈ constant while recovery lowers the driving force. If RX does not start quickly, the material stays unrecrystallised "for infinite time".
     - If T_ann > T_disp, the dispersoids coarsen, and the material stays unRX only if recovery lowers P_D at least as fast as coarsening lowers P_Z.
  3. **Experimental ranking:**
     - poorest RX resistance with solute in solid solution plus an up-quench to T_ann, or dispersoids formed at T_disp ≫ T_ann;
     - **best RX resistance** with dispersoids formed in an intermediate anneal of solutionised and deformed material, or formed at T_disp < T_ann. The Zener decay from coarsening is usually slower than the recovery decay of the driving force, so a high number density of small dispersoids formed at T_disp ≲ T_ann wins.
- **Same principle in an industrial 2xxx route:** a 300–400 °C / 2–5 h coil anneal before solution treatment gave **coarse grains elongated in RD**, vs fine equiaxed grains without it. The coarse grains brought lower crack growth and better corrosion [AMAG14 pp.13–14].
- **Fe/Si in 1xxx:** Fe or Si precipitating before or during annealing raises the RX start temperature and kills PSN nuclei [HBAL03 PDF p.152].
- **3xxx RX-temperature shift by Mn:** Mn "increases the recrystallization temperature … promote[s] fibrous structure upon hot working" [Dav01 p.382]. The fibrous structure is retained because dispersoids are strung out in the working direction (mechanical fibering) [HBAL03 PDF p.135; Shep99 §1.2].
- **Conductivity as a precipitation probe.** Electrical conductivity verified that a 45 s / 400 °C RX anneal of AA3103 caused no Mn precipitation [Ryen03 §3.4 p.56]. Use it to place your anneal relative to the precipitation C-curve.
- **Further support from the HBAL03 full text (2026-10-12):**
  - **Commercial-purity alloys:** in AA1050, Fe and Si "efficiently obstruct recrystallization when present as finely dispersed precipitates". **Mn and Cr "cause the same effect unless the elements are already bound in coarse particles"** [HBAL03 p.356]. This is the industrial statement of the sequencing rule: Mn or Cr that is still in solution (or present as fine dispersoids) retards RX; Mn already in coarse particles does not.
  - **High-purity Al–Fe:** above 0.01 wt % Fe, FeAl₃ forms on boundaries during annealing and RX becomes **continuous (in situ)** around 400 °C [HBAL03 p.229]. This is the extreme case of "precipitation before RX".
  - **Texture:** impurity atoms generally weaken cube and strengthen R {124}<211>, "**especially when they precipitate during the recrystallization annealing**"; avoiding the precipitation temperature raises the cube fraction, so the annealing temperature is decisive (Ito et al. 1983) [HBAL03 p.235].
  - **Hot rolling:** Fe clearly inhibits static RX after hot rolling (super-purity Al with Fe, Si, Cu additions; 50 % pass, 500 → 390 °C, 30 s before quench; Blade 1979) [HBAL03 pp.243–244, Fig.28]. Only the figure carries the numbers.
- **(general knowledge)** The resulting time–temperature map for supersaturated 3xxx has two C-curves, one for RX start and one for dispersoid precipitation start. Above their crossing T_c, RX precedes precipitation and gives fine equiaxed grains (dispersoids then form inside the RX grains). Below T_c, precipitation on the deformation substructure precedes RX: RX is retarded, nuclei are few, and grains are coarse and elongated (pancake). This is the user's "precipitation before RX → coarse/elongated grains". It is consistent with [Røy05 p.34–35; AMAG14 p.14; HBAL03 PDF p.152; HBAL03 pp.229, 235, 356]. The quantitative 3xxx T–t–T curves (HH §9.8) are **not extracted**, and HBAL03 gives only the precipitation onset (Mn above ~325 °C [p.299]; Al₆Mn 300–350 °C [p.295]), not RX-start/precipitation-start curves.

**Relevance to the slug route.**
- The quenched strip carries Mn, Fe, Si (and Mg) in solution into cold rolling and the slug anneal. Mn and Fe start to precipitate in the same 300–400 °C range in which a batch slug anneal ramps and holds [HBAL03 pp.229, 295, 299].
- **A slow ramp or a low hold therefore invites precipitation on the recovered substructure before RX.** The expected result is fewer nuclei, coarse or elongated grains and, in the extreme, continuous RX with the deformation texture kept [HBAL03 pp.228–229].
- **Fast heating to a temperature above the precipitation "nose"** (position unknown for this chemistry; measure it) lets RX run first. Dispersoids then form inside the new grains and cap later grain growth (§6) (inference consistent with [HBAL03 p.887; Ryen03 §3.4]).
- Use **conductivity before and after the anneal** to check which sequence occurred (§5.2 above).

### 5.3 Dispersoid spatial distribution
- DC-cast segregation gives non-uniform dispersoids. **RX starts in dispersoid-depleted regions**, such as the dispersoid-free zone at dendrite edges when the former segregates to dendrite centres (Zr: Scheil k = 1.4; Sc: k = 0.9) [Rob04 pp.1410–1418].
- The **RX fraction is estimated as the volume fraction where F_V/r falls below a critical value**. In Robson's 7050 example, the critical F_V/r matched 30 % RX in the Sc-free alloy; with 0.02 wt % Sc RX is predicted to almost disappear (assuming unchanged driving force) [Rob04 p.1419–1420].
  - For Mn (k < 1 (general knowledge)) the depleted regions would instead be cell centres. This needs verification for your alloy (see Gaps).
- **Banded particle distributions** (common in rolled commercial Al) give anisotropic pinning: P_PZ = P_Z L/t for boundaries parallel to the bands (bands of thickness t, spacing L). This yields **elongated (pancake) RX grains** [HH §4.6.2.3 eq.4.35 pp.117–119; Fig.4.28].
- **Precipitation onto existing boundaries** gives P_X = D F_V γ/(4r²) (all particles on boundaries) [HH eq.4.36 p.119]. This is much stronger than random pinning, which is why "precipitation on the recovered substructure before RX" is so effective.

### 5.4 Design levers: fine equiaxed vs coarse elongated 3xxx grains

| Target | Homogenisation / preheat | Cold work and final anneal | Mechanism (sources) |
|---|---|---|---|
| **Fine, equiaxed, weak texture** (formability, deep drawing, fin/tube with low critical-strain risk) | **High-T homogenisation with slow cool / stepped holds** (AA3103 C-type → Mn_ss 0.15 at %) to precipitate and **coarsen** Mn dispersoids: lower F_V/r, low Mn_ss; Si present for α-phase (denser early, coarser after soak) [Ryen03 Tab.3.2; HBAL03 PDF p.172] | High reduction (ε ≥ 2); **fast heating, high T** (continuous line, salt bath, induction) so RX precedes any residual precipitation [Ryen03 §3.4: 400 °C/45 s → 6 µm] | many PSN sites (>1 µm constituents) and low Zener; no precipitation in deformation zones [Pol06 p.42; HBAL03 PDF p.152] |
| **Coarse, elongated ("long-life"/sag-resistant fin) grains** | **Low-T or short homogenisation** (retain Mn_ss, i.e. supersaturation from casting; TRC strip retains more) [Pol06 p.102; Bel05 §1.6] | Moderate reduction; **slow heating or a low-T pre-anneal** in the precipitation window (300–400 °C class, cf. AMAG14) so dense fine dispersoids precipitate on sub-boundaries **before** RX; then RX at higher T with few nuclei | Zener on subgrains is near its maximum when D ≈ D_c (§6); RX starts only at sparse sites → few, large, RD-elongated grains [HH eq.4.27–4.29, 4.35–4.36; Røy05 p.35; AMAG14 p.14]. **(general knowledge)** Coarse, elongated, braze-surviving grains reduce Si/liquid-filler penetration along boundaries and improve sag resistance. |
| **Unrecrystallised / recovered (H2x/H24-like) fin** | Retain or precipitate a high number density of small dispersoids (≤0.4 µm effective [HBAL03 PDF p.137]) | Final anneal below the RX start; rely on recovery | Dispersoids retard recovery and RX [Pol06 p.43; Dav01 p.382] |
| **Avoid** | — | **Small, non-uniform strains (3–7 %, e.g. tube sizing) followed by a high-T cycle (braze ~600 °C)** | Critical-strain abnormal coarse grains: AA3102 MPE tube, about −22 % burst strength at ~3 % sizing [Wil12 pp.11–13]; §7 |

### 5.5 Pitfalls
- Over-coarsened dispersoids (homogenisation too hot or too long) lose pinning, because P_Z ∝ f/r falls rapidly with coarsening [Røy05 p.34].
- Dispersoid-free zones (segregation) seed coarse RX grains [Rob04].
- Mn dispersoids increase quench sensitivity (intermediate between Cr- and Zr-dispersoids) [Pol06 p.112; HBAL03 PDF p.137]. This matters for 6xxx/7xxx, and for 3xxx only if a later precipitation step exists.
- Long annealing produces coarse grain [W7 p.5].

---

## 6. Zener pinning and particle–boundary interactions (model-ready)

| Quantity | Equation | Notes | Source |
|---|---|---|---|
| Force of a single incoherent sphere | F = 2πrγ cosθ sinθ; F_S,max = πrγ (θ = 45°) | ∝ γ: pinning of LAGBs/special boundaries is weaker (Cu Σ7: −10 %) | [HH eq.4.11–4.12 p.109] |
| Coherent particle | F_C = 2πrγ (2× incoherent) | can dissolve or reprecipitate, rotate, or be cut (Al₃Sc: [Røy05 p.35]) | [HH eq.4.19 p.112] |
| Ellipsoid (aspect e) | F₁ = F_S·2/((1+e)e^(1/3)); F₂ = F_S(1+2.14e)/e^½ (e ≥ 1); F₂ = F_S e^0.47 (e ≤ 1) | only plates face-on or needles edge-on pin much more than spheres. The inequality signs were lost in extraction; the range assignment is the compiler's reading of Nes et al. 1985 | [HH eq.4.13–4.15 p.110] |
| Number density | N_V = 3F_V/(4πr³); N_S = 2rN_V = 3F_V/(2πr²) | random distribution | [HH eq.4.21–4.22 p.113] |
| **Zener pressure** | **P_Z = 3F_Vγ/(2r)** | Zener's original was half of this; refined treatments give a similar result; confirmed by simulations (Miodownik 2000) | [HH eq.4.24 p.114] |
| Generic form | p_Z ≈ k f/r | k contains the interface energy | [Røy05 eq.3 p.34] |
| Correlated (D ≤ D_c) | P′_Z = 3DF_Vγ/(4r²) (particles at vertices, β = 3) | rises with D | [HH eq.4.27 p.116] |
| Crossover size | D_c = N_V^(−1/3) = (4πr³/3F_V)^(1/3) | — | [HH eq.4.28 p.116] |
| Maximum pinning | P′_Z,max ≈ 1.2 F_V^(2/3) γ/r | at D ≈ D_c | [HH eq.4.29 p.116] |
| Transition D > D_c | P″_Z = πrγ[X N_V D + (1 − X) 2N_V r], X = 1/(N_V D³) | falls back to Zener | [HH eq.4.30–4.34 pp.116–117] |
| Banded particles | P_PZ = P_Z L/t (boundary parallel to bands) | elongated grains | [HH eq.4.35 p.119] |
| Particles on boundaries | P_X = D F_V γ/(4r²) | precipitation onto substructure | [HH eq.4.36 p.119] |
| Dissolving coherent particle | F depends on ln(C₀/C_eq) | — | [HH eq.4.20 p.112] |
| Limiting grain size (derived from the sources) | 3γ/D (growth pressure, [HH §1.3.2]) = 3F_Vγ/(2r) gives **D_lim ≈ 2r/F_V** | consistency estimate | derived |
| Limiting grain size (classical; corrected after full-text pass) | **R_c = 2γ/P_Z = 4r/(3f)** with ΔP = 2γ/R; R is the grain (curvature) radius, so the diameter is **D = 2R_c = 8r/(3F_V) ≈ 2.7 r/F_V (derived)** | Mao calls R_c the "stable average grain size", but his eq.31–32 define R as a radius. The same 4r/3F_V is often quoted as a **diameter** (general knowledge), a factor-2 ambiguity. The range of estimates is therefore D_lim ≈ (1.3–2.7)·r/F_V. The HH ch.11 variants are still not extracted | [HBAL03 eq.37–38 p.250] |
| Zener pressure (second source) | P_z = 3fγ/(2r) | same as HH eq.4.24 | [HBAL03 eq.37 p.250; Ridley eq.8 HBAL03 p.1114] |
| Empirical pinning criterion | Zener pinning "will occur when F_V/r ≥ 2" (for groups of fine particles) | **units not printed** (presumably µm⁻¹; then P_Z ≈ 1 MPa with γ = 0.324 J m⁻², derived). Treat as uncertain | [HBAL03 p.1114] |

**Worked example (derived; inputs assumed: r = 50 nm, F_V = 0.01, γ = 0.324 J m⁻²):**
- P_Z = 0.097 MPa.
- D_c = 0.37 µm and P′_Z,max ≈ 0.36 MPa.
- D_lim: 10 µm (2r/F_V), 13 µm (8r/3F_V, i.e. twice Mao's radius 4r/3F_V) or 6.7 µm (4r/3F_V read as a diameter).
- Compare:
  - RX driving pressure in heavily deformed Al: ≈7 MPa (derived);
  - subgrain-growth pressure for 1 µm subgrains: ≈0.6 MPa [HH §1.3.2];
  - growth pressure for 100 µm grains: ≈0.01 MPa [HH §1.3.2].
- **Conclusion:** a typical 3xxx dispersoid population cannot stop growth of an established RX front driven by stored energy. It *can* (a) arrest subgrain coarsening and therefore *nucleation* (pinning is near its maximum because D_subgrain ≈ D_c), and (b) cap post-RX grain growth at about 10 µm. This is why the **timing** of precipitation relative to nucleation (§5) is decisive.
- HBAL03 states the same mechanism: aluminide dispersoids (fine, "not necessarily coherent") hinder RX by **pinning small-angle boundaries and dislocations** [HBAL03 p.296]. Mn dispersoids in 3xxx "efficiently hinder grain growth upon recrystallization" [HBAL03 p.299]. Size anchors: after 350–450 °C for up to 200 h, Al₃Zr is 5–11 nm and Al₃Sc 25–35 nm [HBAL03 p.298].

**Relevance to the slug route.** With 0.14 Mn (T11) the Mn dispersoid fraction is small. If, say, F_V ≈ 0.2 % and r ≈ 50 nm (assumed, not measured), D_lim ≈ (1.3–2.7)·r/F_V ≈ 33–67 µm (derived), inside the 20–100 µm slug window. A lean alloy is therefore close to the regime where post-RX grain growth is **not** dispersoid-capped. Hold time and heat-up rate then control the final size [HBAL03 p.887]. Measure F_V and r of dispersoids in annealed slugs before relying on a Zener cap.

**Dispersoid size classes:**

| Size class | Source |
|---|---|
| Mn/Cr/Zr dispersoids "<1 µm" | [HBAL03 PDF p.135] |
| 0.05–0.5 µm | [Pol06 pp.43, 79] |
| 5–200 nm | [Ryen03 §2.4 p.28] |
| Effective for RX retardation: **< 0.4 µm, closely spaced** (coherent Al₃Zr > incoherent Al₁₂Mg₂Cr, Al₂₀Mn₃Cu₂) | [HBAL03 PDF p.137] |
| Al₃Sc from 400–600 °C processing: 20–100 nm (good RX resistance) | [Røy05 p.33] |
| Al₃Sc from 250–350 °C ageing: 2–6 nm (hardening) | [Røy05 p.33] |
| Al₃(Sc,Zr) at 475–480 °C: r ≈ 10–13 nm | [Rob04 pp.1413–1416] |

**Sc/Zr add-on options for 3xxx/1xxx (if cost allows; Sc ≈ US$2500 kg⁻¹, i.e. +US$5 kg⁻¹ at 0.2 wt % [Røy07 p.19]):**
- 0.3 Sc raises RX onset by about 220 °C in pure Al, and somewhat less in Al–Mn [Røy05 p.34].
- Al–0.5Mn–0.2Mg–0.15Zr: Rp0.2 87 MPa, rising to 119 / 152 / 168 MPa with 0.11 / 0.21 / 0.26 Sc [Røy07 Tab.1 p.16].
- Al–1Mn–0.15Sc (89 % CR + 288 °C/8 h): YS 216 MPa [Røy05 Tab.7 p.37].
- Zr slows the late-stage precipitation and coarsening (core/shell Al₃(Sc,Zr)) [Røy07 p.14; Røy05 p.34].
- Sc lowers Mn solubility (Al–Mn–Sc α-corner: 0.08 Sc/0.2 Mn at 500 °C; 0.2 Sc/0.55 Mn at 600 °C) [Røy05 p.23].
- **Caution for brazed parts:** in AlScZr MPE tube (0.19 Sc, 0.05 Zr), extrusions stayed unRX but recrystallised and coarsened between 575 and 600 °C (2 min), attributed to dispersoid dissolution near the solvus. Ageing 288 °C/8 h *before* braze gave no benefit; ageing *after* braze gave ≥69 MPa burst (+65 %) [Wil12 pp.40–51].

**Pitfalls**
- P_Z assumes random, uncorrelated particles. For D ≲ λ the pinning is several times higher [HH §4.6.2.2].
- Coherent pinning is double the incoherent value.
- Boundaries are *attracted* to particles [HH p.109].
- Correlation of particles with the dendritic structure invalidates mean-field F_V/r [Rob04].

---

## 7. Grain growth, abnormal grain growth and critical-strain coarsening

### 7.1 Mechanisms
- The driving force is boundary energy, P ≈ 3γ/D [HH §1.3.2 p.10]. It is far below the RX driving force, so migration is much slower [Pol06 p.42].
- **Normal growth** is uniform. **Abnormal growth** (secondary RX) means a few grains consume the matrix and give a bimodal distribution [Pol06 p.43; HH §1.1.1 p.3].
  - It occurs after very large deformation plus very high T [Prakt05 p.8]. Jeffries (1916): abnormal growth is promoted where normal growth is inhibited [HH §1.2.1.3 pp.5–6].
  - The correlated pinning curve (P_Z vs D peaks at D_c [HH Fig.4.26]) is the classical trigger: grains that escape the correlated regime grow against reduced pinning.
- **Critical-strain coarsening** is the practical failure mode in heat-exchanger and extruded products:
  - AA3102 MPE tube sized 3–7 % (typical) recrystallises into very large grains in the inner walls at ~600 °C braze [Wil12 pp.11–13].
  - 5 % sizing gives a **sigmoidal strength loss** with braze T (500–625 °C). With 0 % sizing the loss is only a small linear decrease [Wil12 pp.46–47].
  - Burst pressure (MPa): 3102 0 %/no braze 38; 0 %/braze 39; 5 %/no braze 48; 5 %/braze 39 [Wil12 Tab.6 p.50]. About 3 % sizing gives about −22 % post-braze strength [Wil12 p.13].
  - Similarly: coarse peripheral RX grains in extrusions (−10–15 % longitudinal strength) [Pol06 p.108]; peripheral RX in unlubricated direct extrusion from strain accumulation at the dead-zone border [Shep99 p.47]. Reheat cycles of RX-inhibited alloys must avoid coarse grains in critically strained regions [Pol06 p.107]. Locally different deformation followed by annealing gives coarse grain with optical and mechanical defects [W7 p.5].
- Orange peel arises from coarse surface grains. Shallow coarse surface grains are less harmful, and hot-worked products are less prone [Pol06 p.43].
- **Normal grain growth (Mao)** [HBAL03 pp.244–248]: homogeneous coarsening by curvature-driven HAGB migration toward the centres of curvature, distinct from subgrain coalescence. In 2D sections the boundaries meet at about 120°. Shrinking grains vanish ever faster as they get small. **The largest grains are often 3–4× the average size** (95 % CR Al–3 Mg annealed at 500 °C for 40–160 s).
- **Abnormal grain growth (secondary RX): three triggers** [HBAL03 pp.250–254]:
  1. **Particles** that coarsen, coalesce or dissolve at high T, lowering P_Z. Grains above an upper size limit then escape, while the matrix stays pinned.
  2. **Texture.** A strong single component means most of its grains are bordered by low-mobility LAGBs; grains of a weak component meet mobile HAGBs and, once larger than the matrix grains, grow as secondary grains.
     - **Al–1 wt % Mn**, 95 % CR: primary RX complete after **1 s at 620 °C** with **87 % cube**. On further annealing at 620 °C two AGG stages followed: first {011}<133> replaced cube, then {001}<320> replaced {011}<133>, each with a jump in mean grain size (Eichelkraut 1988) [pp.251–252, Fig.35].
     - **Al–3 wt % Mg**, 95 % CR: RX complete after 300 °C/200 s with strong cube. After 300 °C/600 s plus 400 °C/20 s the cube maximum reached 119.9× random. At 400 °C the cube grains were then consumed by {112}<312> and {001}<490> grains after ≈ 3000 s (Zhao 1990) [pp.252–253, Figs.36–37].
  3. **Free surface** in thin foil (< 0.1 mm, > 99.99 % Al): grains through the thickness and a very sharp cube, because the {001} surface energy is lowest [p.254].

### 7.2 Quantitative
- **Growth law (now sourced; corrected after full-text pass, previously general knowledge)** [HBAL03 eq.31–35 pp.245–248]:
  - boundary energy per unit volume F_b = 4πR²γ/(2·(4/3)πR³) = **3γ/(2R)** (R = mean grain radius);
  - curvature pressure **ΔP = 2γ/R**; v = −dR_s/dt ∝ ΔP, which gives R_s² = R_s0² − Cγt for a shrinking grain and **R² = R₀² + Cγt** for the mean grain, i.e. **R ∝ √t (n = 2)**, C depending on T;
  - example: with γ ≈ 1.0 J m⁻² (Mao's value, §1.4), coarsening from R = 50 to 100 µm releases 1.5×10⁴ J m⁻³ [p.245]; with γ = 0.324 J m⁻² it is 4.9×10³ J m⁻³ (derived). Both are ~100–1000× below the RX driving force (§1.2), which is why grain growth is slow and easily pinned.
- Still **general knowledge**: n is often 2–4 with solute or particles; k = k₀ exp(−Q_gg/RT). The HH ch.11 text is not extracted.
- **Solute drag in grain growth** [HBAL03 pp.248–250]: segregation c_B = c·exp(−Q_B/kT) (Lücke & Detert) falls with rising T and weaker binding, and a high driving force lets the boundary break away; both restore near-pure-Al mobility.
- Q for grain/subgrain growth in Al ≈ self-diffusion (boundary control) [HH §5.5.2 p.167].
- Limiting size with particles: see §6.
- Hall–Petch for designing grain size:
  - pure Al k = 0.065–0.07 MPa m^½ [Ryen03 eq.2.12 p.33];
  - Mg-free alloys ≤ 0.15, Al–Mg > 0.2 (5754: k = 0.22, σ_f = 42.5 MPa; 5182: k = 0.30, σ_f = 57.6 MPa; σ_f = 15.5·wt %Mg + 24 MPa) [HBAL03 PDF p.179];
  - AlNi6 k = 0.14 [Ryen03 p.33].
  - In Al, k is about **5× smaller than in ferrous alloys**, so grain size is a weak strengthener except at very fine sizes, where Hall–Petch still holds [HBAL03 p.263].

### 7.3 Design levers
- Keep pre-braze or pre-anneal strains **away from the critical-strain window**. Either deform enough to recrystallise fine, or not at all.
- Alternatively, **pre-recrystallise** before the strain-inducing operation and pin with dispersoids.
- Alternatively, provide **dispersoids stable at the braze T**. Al₃(Sc,Zr) dissolves at 575–600 °C [Wil12 p.41]. Mn "as a dispersed precipitate … is effective in slowing recovery and in preventing grain growth" [Dav01 p.382], but the source gives no temperature limit, so survival at braze T stays **(general knowledge)**.
- Short anneal times at the minimum effective T, and fast heat-up, limit coarse grain [W7 Tab.2 footnote]. HBAL03 gives the same rule for non-heat-treatable alloys: heat very quickly and hold only until the load centre reaches temperature [HBAL03 pp.887–888].
- Avoid a **single very strong texture component** if long high-T exposures follow; it is a trigger for texture-induced AGG [HBAL03 pp.251–253].

**Relevance to the slug route.**
- Slugs need 20–100 µm grains. Grain growth after RX follows R² − R₀² ∝ t [HBAL03 eq.35], so **soak time matters less than nucleation density** once RX is complete. Doubling the soak enlarges a growing grain by at most √2× (derived, ideal n = 2).
- Lean alloys have few dispersoids to cap growth (§6), so the "heat fast, hold only to temperature" rule [HBAL03 p.888] is the main guard against coarse or duplex grains in the slug centre of a large batch load.
- A mixed PSN texture is unlikely to trigger texture-induced AGG. A strongly cube-textured slug (low PSN) held long at high T could (inference from [HBAL03 pp.251–253]).

### 7.4 Pitfalls
- Sc/Zr dispersoid pinning fails at braze temperature: AlScZr RX and coarsening between 575 and 600 °C. Ageing before braze did not help [Wil12 pp.41, 50–51].
- Repeated high-T solution cycles carry a risk of grain coarsening [W7 pp.17, 19] (castings and heat-treatable alloys).
- Coarse grain in formed parts gives orange peel [Pol06 p.43].

---

## 8. Textures (deformation, RX) and their control

### 8.1 Deformation (rolling) texture of Al [HH §3.2 pp.68–73; Ryen03 §2.2.6 pp.19–23]

| Component | {hkl}<uvw> | φ₁, Φ, φ₂ (°) |
|---|---|---|
| Copper C | {112}<111> | 90, 35, 45 |
| S | {123}<634> | 59, 37, 63 |
| Brass B | {011}<211> | 35, 45, 90 |
| Goss G | {011}<100> | 0, 45, 90 |
| Cube | {001}<100> | 0, 0, 0 |
| Dillamore D | {4 4 11}<11 11 8> | 90, 27, 45 |
| Rotated cube (shear) | {001}<110> | 45, 0, 0 |
| **R (RX component)** | **{124}<211>** | **57, 29, 63** |
| — | {111}<112> | 90, 55, 45 |

The last three rows are from [HBAL03 Tab.1 p.234]. *Flags:* that table prints copper as {112}<**112**>, a misprint for {112}<111> (as above and in [HBAL03 PDF p.143]); it gives Brass and Goss with φ₂ = 0° instead of 90°, which is a symmetry-equivalent setting (general knowledge).

- β-fibre (C–S–B) plus α-fibre (G–B). At high strain S becomes dominant [HH pp.70–71]. In 95 %-rolled 99.998 % Al, S exceeds 60 % of the volume [HBAL03 p.238].
- Relaxed-constraints theory explains C+S (ND–RD and ND–TD shears) [HH §3.7.1.4 p.85]. Cube and Goss are *metastable*, so they persist to large strain [HH p.85].
- Most of the rolling texture is formed by ε = 2 in AA1050 [Ryen03 §4.2.1 p.68].
- Mg weakens texture and destabilises S. At 3–5 % Mg, shear bands raise Brass; above about 5 % the texture randomises [Ryen03 p.21–22].
- Medium non-shearable particles (0.1–5 µm) *sharpen* C. Large particles (>5 µm) in high amounts weaken texture [Ryen03 p.21].
- Age-hardenable Al–Li gives an alloy-type strong {110}<112> texture [HH §3.2.2 p.73].
- Higher rolling T increases Brass. **Cube is more stable during hot deformation of Al** (retained cube) [HH §3.6.2 p.81].
- Surface shear texture {001}<110> (rotated cube) and {111}<110> appear with high friction (AA3003, no lubricant) [HH §3.6.1 p.80].

### 8.2 RX texture
- Rolled Al gives cube grains plus grains with retained rolling texture [Pol06 p.39]. Cube or Goss is strong especially in high purity. Substantial constituent fractions mean PSN, which randomises [HBAL03 PDF p.143].
- Pure Al and some alloys "always form cube texture by RX". PSN deviates from cube. Fine secondary precipitates during RX suppress the primary-particle (PSN) effect [Leh06 p.177–178].
- Growth selection via 40°<111> mobility [HH §5.3.2; SimRX p.3].
- **Mechanisms in rolled Al (Mao)** [HBAL03 pp.234–238]:
  - Rolled and annealed pure Al gives **cube {001}<100>, R {124}<211> and sometimes Goss {011}<100>** [p.235].
  - **Oriented nucleation (Dillamore & Katoh):** cube lies in a *divergent* zone of orientation space. During rolling, cube-oriented regions split into transition bands with steep orientation gradients. After polygonisation and coalescence their subgrains acquire mobile HAGBs and nucleate cube (and R). Cube is metastable in rolling, so some cube subgrains survive heavy reductions (Ridha & Hutchinson) [pp.234–238].
  - **Growth selection (Lücke):** cube and R are both ~40°<111> from S, the main rolling component, so their boundaries are the fastest [pp.235, 238]. In 95 % CR 99.998 % Al at 300 °C, nuclei appear in the transition bands between cube and S after 100 s, and by 316 s all the very large grains are cube or R [p.238, Fig.24].
  - **The initial texture carries over:** in Al–0.01 Ti with a strong initial Goss, 95 % rolling and 300 °C annealing gave Goss + cube. TiAl₃ on the original boundaries stopped growth across them, so the nucleation pattern of the original grains survived [pp.237–238].
- **Recovery before RX sharpens the texture** [HBAL03 Tab.2 p.236]. 95 % CR 99.998 % Al:
  - 240 °C/600 s (recovery only) then 300 °C/3162 s: **cube 54 %, R 26 %**;
  - direct 300 °C/316 s: **cube 12 %**, with the rest spread over {011}<611>, {013}<100>, {149}<511>, {225}<554>, {239}<311> and {269}<354> (6–23 % each).
  - Explanation: the lowered driving force makes RX slow, so specially oriented (cube, R) nuclei win. A high driving force makes RX "rash", and many orientations grow [pp.236–237].
- **Impurities/precipitation** weaken cube and strengthen R, especially when they precipitate during the anneal. Avoiding the precipitation temperature raises cube [HBAL03 p.235].
- **3xxx:** Fe "prevents the formation of earing upon deep drawing due to the control of texture" [HBAL03 p.299]. A plausible mechanism is more Fe-rich constituents giving more PSN, which randomises (inference, consistent with [HBAL03 PDF p.143]).
- **Hot-band cube for can body (AA3104/AA5182)** [HBAL03 pp.356–358]:
  - can-body stock needs a distinct cube in the hot band to reduce earing;
  - with little inter-stand RX, cube nuclei form at the expense of the rolling components and grow during the later anneal or coil self-anneal. Coarse dispersoids at large spacing help RX during coiling;
  - inter-stand RX instead forms **large cube bands that deform unfavourably** in later passes; lowering the T or raising the speed restrains it but brings in PSN (random texture);
  - the computed fraction of inter-stand RX correlates with cube intensity and 0/90° earing (AA5182), and is used for pass optimisation [HBAL03 p.358, Fig.6].
- Hot-band textures: technically pure Al hardly recrystallises dynamically, so hot band shows pronounced cube {100}<001> [Leh06 p.175].
  - AA5005 transfer gauge: cube 36× random plus minor Bs. AA5182: weak cube [Ryen03 Tab.4.1 p.66].
  - The hot-band texture influences Lüders strain, uniform elongation and strength [Leh06 p.175].

### 8.3 Earing and r-value control
- Al r-values are 0.6–0.9 [Leh06 p.175].
- Rolling texture gives **45° ears**. Cube (annealing) texture gives **0/90° ears**. A balance gives eight small ears or none [Pol06 p.40; Leh06 p.175].
- For pure-Al strip the planar anisotropy Δr decreases with cold reduction and passes an optimum at the transition from cold-rolling to RX texture. **Earing ≤ 3 % (usual limit) is best reached at about 50 % cold reduction** [Leh06 pp.175–176].
- 3004-H19 canstock: control earing by balancing anneal cube against final rolling texture; control size, F_V and distribution of α-Al₁₂(Fe,Mn)₃Si [HBAL03 PDF p.135, 143; Pol06 p.39].
- Texture strengthening: ideal fibre texture gives about +20 % strength [Pol06 p.39]. Extrusion dual fibre gives about +70 MPa longitudinal, lost on RX [HBAL03 PDF p.143].

### 8.4 Pitfalls
- Taylor-type models predict textures that are too sharp and form too fast; heterogeneity (deformation bands) is the cause [HH §3.7.1.5 p.86].
- Surface ≠ mid-plane texture under high friction or light passes [HH §3.6.1 p.80].
- A strong initial (hot-band) cube delays β-fibre development: AA5005 shows no β-fibre up to ε = 1 [Ryen03 §4.2.2 p.70].
- Mechanical fibring (grain shape, particle stringers) can dominate anisotropy over crystallographic texture [Pol06 p.40].

### 8.5 Gaps
- **The P-texture {011}<566> and ND-rotated cube** (typical PSN- or particle-related RX components in 3xxx) are **not described** in the extracted text; HH ch.12 is missing. The full HBAL03 text (2026-10-12) does not list them either (Mao's Table 1 has cube, rotated cube {001}<110>, R, Goss and the rolling components only [HBAL03 p.234]). The R component, the oriented-nucleation vs growth-selection mechanisms and the cube/PSN competition in AA3104 are now covered (§8.1–8.2).

**Relevance to the slug route.** Impact extrusion is not limited by earing the way deep-drawn cans are. The texture questions for slugs are: (i) uniform wall flow and a uniform surface after forming (general knowledge), and (ii) the AGG risk of a single strong cube component (§7). A PSN-dominated, near-random slug texture is the safer target. That is also what a high constituent count and an anneal without precipitation give [HBAL03 PDF p.143; HBAL03 p.235].

---

## 9. Hot working: dynamic recovery, Zener–Hollomon, static/metadynamic RX between passes

### 9.1 Mechanisms and observations
- Al dynamically recovers above about 0.5 T_h to a stable polygonised substructure, with equiaxed subgrains in elongated grains that do not recrystallise. T_h is the homologous temperature relative to the **lowest-melting phase** [Shep99 §1.2]. Most Al products dynamically recover during hot working; static RX may occur between or after passes; **high-Mg alloys (lower SFE) may recrystallise dynamically** [HBAL03 PDF p.142].
- Technically pure Al hardly undergoes DRX in hot forming [Leh06 p.175]. AMAG notes that "dynamic recrystallization may occur as early as in the rolling process … subgrain formation", with subgrain formation and coarsening controllable by alloying [AMAG14 p.12].
- Dispersoid-forming elements precipitate in homogenisation or preheat and are strung out in the working direction. They **delay or prevent static RX** and retain fibrous grains [Shep99 §1.2; HBAL03 PDF p.142].
- Hot rolling route: a 200–600 mm DC ingot goes to 15–35 mm in a reversing mill, then to 2.5–8 mm in tandem and coiling. Recovery and **partial RX** occur in hot rolling, depending on composition, T and pass reduction. Plate strain decreases from surface to centre [Pol06 p.107].
- Deformation heating raises the strip T [AMAG14 p.12].
- At hot-working T, work hardening vanishes through dynamic recovery and RX [Pol06 p.36]. The Nes model gives dynamic recovery as dipole collapse plus subgrain growth with sinh-type rate laws [Ryen03 eq.2.37–2.39 pp.41–42].
- Flow stress ∝ 1/δ for hot-worked AA3104 [Ryen03 Fig.2.25 p.34].
- **Dynamic recovery and DRX (Mao)** [HBAL03 pp.240–244]:
  - DRV works by cross-slip and climb, which need the narrow partials of high-SFE Al to recombine; its activation energy is "inversely proportional to the stacking fault energy" [p.240];
  - DRX shows single-peak (low T, high rate) or multiple-peak (high T, low rate) flow curves [pp.240–241];
  - in Al, DRX was long thought absent. Yamagata found it only in ≥ 99.999 % Al at very low compression speeds (341 °C, 1 mm min⁻¹), and **not** in 99.99 % Al (Cu 10, Fe 36, Si 26 ppm; 310 °C, 0.06 mm min⁻¹) [pp.242–243];
  - hot-rolled (522 → 294 °C) Al–0.0035 Cu kept a deformed structure and recrystallised only in a later anneal [p.241, Fig.26];
  - Mao argues that solute segregating to dislocations lowers the effective SFE, so DRV removes less stored energy and DRX can start; the DRX tendency rises with Mg in solution (Al–Mg at 0.9 T_m, Gardner & Grimes), and "similar behaviour" is reported for Al–Mn, Al–Mg–Mn and 99.5 % Al [p.244].
- **Industrial view (Karhausen & Korhonen)** [HBAL03 p.356]: in customary industrial alloys DRX "may be observed only at extremely high temperatures", mainly by local bulging of grain boundaries. RX normally takes place **between stands or after rolling (post-dynamic or static)**, or by **self-annealing on the coil** from the rolling heat. *Conflict flagged:* this is hard to reconcile with Mao's report of DRX-type behaviour in Al–Mn and 99.5 % Al [p.244], which rests on flow-curve shape only. This KB follows the industrial view and [HBAL03 PDF p.142]: dilute and Mn-bearing alloys dynamically recover; high-Mg alloys may DRX.
- **Hot-rolling model status** [HBAL03 pp.359–360]: steel-type Avrami/t₀.₅/d_rex regressions (§4.2) are of limited use for Al. Physically based models with nucleation-site efficiency and precipitation are under development.

### 9.2 Quantitative (method from Bom08, not Al data)
- Activation energy from the **Zener–Hollomon hyperbolic-sine law**, with peak stress fitted over T and ε̇. Nimonic 80A: Q = 379 kJ mol⁻¹ [Bom08 p.323].
- Form: Z = ε̇ exp(Q/RT) [HBAL03 eq.3 p.359, there written with Q_def, the apparent activation energy for deformation; no Al value given] = A [sinh(α_s σ)]^n' (the sinh law is **general knowledge**).
- Subgrain size **(general knowledge)**: δ⁻¹ = a + b ln Z. HH ch.13 and Sheppard §4.2/4.11.4 with Al values are not extracted, and HBAL03 gives no Al constants.
- For dilute Al alloys Q_HW is usually close to Q_self = 142 kJ mol⁻¹ [HH Tab.5.1] (**general knowledge** that it is used as such).
- DRX onset by interrupted tests and metallography: GB bulging at ε ≈ 0.175 (1080 °C, 0.1 s⁻¹, Nimonic). The peak strain shifts to higher ε at higher ε̇ or lower T [Bom08 pp.323–327]. Processing maps (DMM) locate stable windows [Bom08 p.324].
- Critical PSN particle size in hot working decreases with lower T and higher ε̇ [HBAL03 PDF p.142]. **(general knowledge)**: at high T and low Z, particle zones recover and PSN can be suppressed entirely.

### 9.3 Design levers
- **Hot-band grain and texture set the cube reservoir for cold rolling and annealing:**
  - fully RX hot band (high exit T, high Mn_ss precipitated) gives a strong cube;
  - unRX or recovered hot band (low exit T, fine dispersoids) gives a retained deformation texture.
  - Earing balance follows (§8).
- Exit and coiling T accuracy matters at ±5 °C [AMAG14 p.12].
- **Static RX in coil (self-annealing)** depends on stored energy at the coiling T and on the dispersoid state. HBAL03 confirms the industrial use of self-annealing on the coil from the rolling heat and that **coarse dispersoids at large spacing help RX during coiling** [HBAL03 p.356].
- **Inter-stand RX control:** lower the rolling T or raise the speed to restrain it (but watch for PSN replacing cube) [HBAL03 p.356].
- **Metadynamic RX** (completion after DRX nuclei formed in the pass) is relevant only for high-Mg alloys in Al per [HBAL03 PDF p.142] **(definition: general knowledge)**.

### 9.4 Pitfalls
- Bom08 constants (Q = 379 kJ mol⁻¹, critical strains, processing-map optimum 1000–1080 °C) are for Nimonic 80A and **must not be transferred to Al**. Only the method transfers.
- Homologous temperature should be referenced to the lowest-melting phase, not to pure-Al T_m [Shep99 §1.2]. Low-melting eutectics set the upper hot-working limit [AMAG14 p.11; Bel05 §1.6].
- Deformation heating raises the actual T above the set-point [AMAG14 p.12].
- Steel-type hot-rolling RX regressions predict unrealistically coarse Al grains [HBAL03 p.360].

**Relevance to the slug route (in-line hot mill → quench).**
- Blade's experiment (50 % hot rolling of super-purity Al with Fe, Si or Cu additions; **entry 500 °C, exit 390 °C**; 30 s delay; quench) is almost the user's hot-mill window (≈ 500 → ≈ 380 °C, ≥ 50 %, then a water bath). **Fe clearly inhibited static RX** in it [HBAL03 pp.243–244, Fig.28]. Hot-rolled dilute Al with no hold also stayed deformed until a separate anneal [HBAL03 p.241].
- So the quenched hot band of an Fe-bearing slug alloy is expected to be **dynamically recovered, not recrystallised** (inference). Two consequences:
  1. its recovered substructure and any surviving stored energy add to the 30–50 % cold reduction at the slug anneal (more driving force than the cold strain alone suggests);
  2. the cast-strip grain and its texture are not reset before cold rolling. Coarse columnar cast grains could then carry through as banding (inference; check by EBSD of the hot band).
- If a fully recrystallised hot band is wanted (e.g. to reset the cast structure), it needs a higher exit T or a short hold before the quench, against the user's choice to retain Mn, Mg and Si in solution (trade-off; see ch19).

---

## 10. Alloy-family specifics

**1xxx / 8xxx foil and fin [HBAL03 PDF pp.150–152; Bel05 §1.5–1.6; Pol06 p.131]**
- Fe solubility in (Al) is ≤ 0.05 %, so secondary Fe phases are ≤ 0.1–0.2 vol % [Bel05 §1.1].
- Fe in solid solution (DC vs strip cast) raises the RX start T through Al–Fe precipitation during annealing [HBAL03 PDF p.152].
- Constituents add about +7 MPa per vol % [HBAL03 PDF p.134, 150].
- Coarse Al₃Fe cracks and harms formability; fine Al₆Fe does not. For alloys with 4.6–6.1 wt % Fe, Al₃Fe forms below a solidification-front velocity of 0.5 mm s⁻¹ and Al₆Fe above it; Si and Mg stabilise Al₃Fe [HBAL03 PDF p.151].
- 1145-H19 cells reach about 1 µm at ε ≈ 0.15, after which misorientation increases. Si in solid solution impedes dynamic recovery [HBAL03 PDF p.152].
- 8111 (Fe 0.4–1.0, Si 0.3–1.1):
  - eutectic Si at the upper Si limit survives into 6–14 µm foil and causes perforation, so anneal ≥ 500 °C;
  - needle Al₃Fe/Al₅FeSi do not spheroidise; Al₈Fe₂Si (low Si) spheroidises;
  - anneal at 620 °C only within a narrow composition window [Bel05 §1.5].
- 8006 (Al–1.6Fe–0.65Mn) and 8011 (Al–0.75Fe–0.7Si): foil and finstock. Dispersion hardening gives 30–40 MPa of proof and tensile strength; solid solution gives 2–10 MPa of proof stress and 5–20 MPa of tensile strength [Pol06 p.131].
- 8011A soft anneal: 340–400 °C, 1–2 h [W7].
- In high-purity Al–Fe with > 0.01 wt % Fe, FeAl₃ on boundaries makes RX continuous around 400 °C [HBAL03 p.229]. In AA1050, finely dispersed Fe/Si precipitates obstruct RX in hot rolling [HBAL03 p.356].
- 8xxx (Fe + Mn): good strength–ductility and retained elevated-T strength through a fine grain size stabilised by dispersed Fe-rich precipitates [HBAL03 p.297].

**3xxx [HBAL03 PDF pp.171–172; Pol06 pp.129–130; W7; Wil12]**
- Mn_ss in annealed sheet: YS +21 MPa per wt % and UTS +42 MPa per wt %. In H19: YS +35 MPa per wt % Mn, compared with **+70–85 MPa per wt % Mg** [HBAL03 PDF p.172].
- 3003 annealed TS ≈ 110 MPa (1100: 90). 3004 annealed TS ≈ 180 MPa [Pol06 p.129–130].
- 3003 draws better in the cold-worked than in the annealed state (cans) [Pol06 p.35].
- In AA3004 the second-phase strengthening rises fast early and then stays constant, while the solute contribution grows with strain [Ryen03 §2.4 p.29].
- AA3102 (tube, as tested: Si 0.07, Fe 0.41, Mn 0.24) extrudes into fine RX equiaxed grains [Wil12 pp.18, 40].
- Mn (up to 1.25 %) in can alloys "allow[s] high deformation degrees and … prevent[s] grain growth", by slowing RX and through a fairly uniform distribution of Mn precipitates [HBAL03 p.297]. Commercial Al–Mn alloys (3003, 3004, 3105) anneal at 345–415 °C (3003: "400–600 °C"); O/H-temper properties in §4.3 [HBAL03 Tab.37 p.299]. Retained strength is "sufficient … up to 200 °C" [HBAL03 p.299].
- Brazing heat exchangers: braze at 560–610 °C (CAB ~595 °C, Mg-free filler, low-Mg base) [Pol06 p.167–168].
  - Tube 3005: Al–1.2Mn–0.40Mg–0.35Fe–0.30Si–0.15Cu.
  - Fin FA6815: Al–1.6Mn–1.5Zn–0.85Si–0.25Fe–0.15Zr. Heat-exchanger alloys rely on solid solution plus dispersion [Pol06 p.168].

**5xxx [HBAL03 PDF pp.173–180; Pol06 p.130; Ryen03]**
- Mg suppresses dynamic recovery: 5182-H19 has a dense uniform network vs subgrains in 1145.
- More Mg (up to 3.5 %) gives a finer annealed grain (89 % CR, HP Al–Mg) [HBAL03 PDF p.178].
- Mn above its solubility forms Al₆Mn dispersoids that retard RX [HBAL03 PDF p.179].
- Mg ≥ 3–4 % gives β-phase on GBs at 60–200 °C [Leh06 p.174; Pol06 p.130].
- Lüders type A/B. Avoid with strain-hardened sheet or by forming > 150 °C [Pol06 p.40–41].
- Shear bands appear readily above about 2–3 % Mg [Ryen03 p.18].
- 95 % CR Al–3 Mg: RX at 300 °C/200 s gives a strong cube; a long 400 °C anneal brings texture-induced abnormal growth ({112}<312> and {001}<490> grains consume cube) [HBAL03 pp.252–253].
- DRX tendency rises with Mg in solution in hot compression [HBAL03 p.244].

**6xxx (brief)**
- Mn, Cr and Zr prevent RX in solution treatment (fine grain counters excess-Si GB embrittlement) [Dav01 p.381; HBAL03 PDF p.184].
- Si available for Mg₂Si = Si − ¼(Fe + Mn) [HBAL03 eq.26 PDF p.183].
- Outer panels need Lüders-free AA6016 [Prakt05 p.2].

---

## 11. Model-ready equations and parameters: summary

| # | Process | Equation | Key parameters (Al) | Source |
|---|---|---|---|---|
| 1 | Taylor hardening | σ = σ₀ + α M G b ρ^½ | α: c₁ ≈ 0.5 [HH]; 0.2–0.3 [HBAL03]; α₁ ≈ 0.3 (interior) + α₂ ≈ 2 (boundary term) [Ryen03]; **M ≈ 3.06 (general knowledge)**; G = 25.4 GPa; b = 0.286 nm | HH eq.2.2, Tab.5.1; HBAL03 eq.6; Ryen03 eq.2.22 |
| 2 | Stored energy | E = 0.5 ρ G b² + 3γ_s/D | γ_s from Read–Shockley; γ_b = 0.324 J m⁻²; θ_m = 15° | HH eq.2.6–2.8, 4.6; Tab.4.2 |
| 3 | Substructure vs strain | δ ∝ 1/ε (ε > 1); ρ_i ≈ 10¹⁴ m⁻² (saturated) | δ(ε = 1.5) ≈ 0.5 µm; φ → 3–4° (Nes) | HH p.19; Ryen03 p.16, 38 |
| 4 | Strength from substructure | σ = σ₀ + k₁ d^(−m) | m = 1 (cells) to 0.5 (subgrains) | Pol06 p.36; HBAL03 PDF p.113 |
| 5 | Hall–Petch | σ = σ_i + k D^(−½) | k = 0.065–0.07 (pure Al); ≤0.15 (Mg-free alloys); 0.22–0.30 (5754/5182) MPa m^½ | Ryen03 p.33; HBAL03 PDF p.179 |
| 6 | Logarithmic recovery | σ = σ₀ − (kT/c₂) ln(1 + t/t₀) | Q₀ = 277 (Al–1Mg) to 231 (Al–5Mg) kJ mol⁻¹ | HH eq.6.22 |
| 7 | Climb recovery | 1/σ² − 1/σ₀² = c₃ t; Q = Q_self | Q_self = 142, Q_core = 82 kJ mol⁻¹ | HH eq.6.17–6.18 |
| 8 | Subgrain coarsening (Nes) | dδ/dt = ν_D B_δ b e^(−U*/kT)·2 sinh(4γ_sb V_δ/(δ kT)) | U* = U_s + ΔU_s; V_δ ∝ b³ c^(−e) | Ryen03 eq.2.39 |
| 9 | LAGB mobility | M = C D_s b/kT; region 2–5°: 10–500× below HAGB | Al–0.05Si: Q 125–154 kJ mol⁻¹ | HH eq.5.4; pp.129–134 |
| 10 | Boundary migration | v = M(P_D − P_Z − P_sol); M = M₀ e^(−Q/RT) | HP Al HAGB Q = 63–67 kJ mol⁻¹; with solute → Q_self or Q_solute | HH eq.5.1–5.2; Tab.5.2 |
| 11 | Solute drag (CLS) | P = v/M + α c₀ v/(1 + β² v²) | v ∝ 1/c₀ (drag regime); breakaway at high v or T | HH eq.5.23–5.25 |
| 12 | Deformation zone (PSN) | tanθ = tanθ_max e^(−1.8x/d); θ′_max = 0.8 θ_max (d − 0.1)^0.2 | zone only for d > 0.1 µm; strain-only for d > 2.5 µm; practical PSN for d ≳ 1 µm | HH eq.2.21–2.23; Pol06 p.42 |
| 13 | JMAK | X = 1 − exp(−k tⁿ), k = k₀ e^(−nQ/RT); Johnson–Mehl X = 1 − exp(−(π/3)N v³ t⁴); industrial X = 1 − exp(−C(t/t₀.₅)^k) | **n = 4 for constant N, v (sourced)**; n = 3 site saturation and 1–2 typical in Al alloys (general knowledge); n 3.0 → 0.8 under concurrent precipitation in Al–Mn (ch12 [W12-19]); apparent Q of pure Al RX ≈ 110–150 kJ mol⁻¹ (derived from Pol06 p.42) | HBAL03 eq.19–21 pp.227–228, eq.1 p.359; SimRX (concept) |
| 14 | Zener | P_Z = 3F_Vγ/2r; P′_Z,max ≈ 1.2F_V^(2/3)γ/r at D_c = (4πr³/3F_V)^(1/3) | coherent ×2; bands ×L/t; on boundaries D F_V γ/4r² | HH eq.4.24–4.36 |
| 15 | Limiting grain size | R_c = 4r/(3f) as a **radius** (sourced), i.e. D = 8r/3F_V; D_lim ≈ 2r/F_V (derived from 3γ/D); 4r/3F_V when read as a diameter (general knowledge) | range (1.3–2.7)·r/F_V; state the convention used | HBAL03 eq.38 p.250; §6 |
| 16 | Dispersoid KWN | Gibbs–Thomson c_r = c_∞ exp(2σV_m/(R_g T r)); classical nucleation (Q ≈ 2.07 eV atom⁻¹ for Sc/Zr); dr/dt = (D/r)(c − c_α(r))/(c_β − c_α(r)); LSW r³ − r₀³ = a(t − t₀) | σ(Al₃(Sc,Zr)) = 0.1 J m⁻² (fitted; 0.06–0.18 measured) | Rob04 eq.1–5 |
| 17 | RX fraction from F_V/r | X_RX = vol. fraction where F_V/r < (F_V/r)_crit | (F_V/r)_crit calibrated on one condition | Rob04 p.1419 |
| 18 | Mn solid-solution budget (3103) | Mn_ss = f(homogenisation) | 0.40 → 0.24 → 0.20 → 0.15 at % (Table §5.1) | Ryen03 Tab.3.2 |
| 19 | Diffusion (500 °C) | — | D_Mn = 5×10⁻¹³; D_Cu = 5×10⁻¹⁰; D_Mg,Si = 10⁻⁹ cm² s⁻¹; +50 °C → ~⅓ homogenisation time | Pol06 p.105 |
| 20 | Anneal anchors | — | 3xxx O-anneal 380–420 °C/0.5–1 h; 1050 320–350 °C; 8011 340–400 °C; AA3103 ε = 2 → RX 45 s at 400 °C | W7 Tab.2; Ryen03 §3.4 |
| 21 | Strain measures | ε = ln(t₀/t); ε_vM = (2/√3)ε | 39 % → 0.5; 63 % → 1; 87 % → 2; 95 % → 3 | Ryen03 eq.3.2–3.4, Tab.3.3 |
| 22 | Grain growth | D^n − D₀^n = k₀ e^(−Q/RT) t; ideal R² = R₀² + Cγt with ΔP = 2γ/R | **n = 2 ideal (sourced)**; n 2–4 with solute/particles (general knowledge); Q ≈ Q_self; largest grains 3–4× mean | HBAL03 eq.32–35 pp.247–248; HH §5.5.2 |
| 23 | Hot working | Z = ε̇ e^(Q/RT) (sourced) = A sinh(ασ)^n′; δ⁻¹ = a + b ln Z; t₀.₅ = a ε^(−b) d₀^c Z^(−d) e^(Q_rex/RT); d_rex = e d₀^f ε^(−g) | Al constants not given in any extracted source; Q_HW ≈ 142 kJ mol⁻¹ assumed (general knowledge); the steel-type t₀.₅/d_rex set over-predicts Al grain size | HBAL03 eq.1–4 pp.359–360; Bom08 (method) |
| 24 | Q from logarithmic recovery data (added 2026-10-12) | X = C₁ ln(t/t₀), t₀ = τ₀ e^(Q/RT) → C₁ = (∂X/∂ln t)_T; **Q = −R (∂X/∂(1/T))_t / C₁** (X as a fraction or in %, but the same in both derivatives) | Valid only in the logarithmic regime (not t → 0 or ∞), for isothermal holds long compared with the heat-up, and for a recovery-only state (no RX or precipitation in the window). A single-slope fit without C₁ (Junit08) gives unit-dependent numbers (§2.4) | HH eq.6.6–6.7 (form); t₀ form **general knowledge** |
| 25 | Mn supersaturation at anneal T (added 2026-10-12) | ΔMn = Mn_ss − Mn_eq(T) | Mn_eq (wt %), (Al)+Al₆Mn+α field: 0.73 / 0.44 / 0.25 / 0.15 / 0.06 at 600 / 550 / 500 / 450 / 400 °C; ≤0.08 with free (Si); 0.026–0.05 at 427–527 °C with Al₃Fe present. Valid for equilibrium three-phase fields; real 3xxx with Fe and Si lies between these bounds | Bel05 Tab.1.9, 1.13 |
| 26 | Second-order recovery (added, HBAL03 pass) | dρ/dt = −kρ² → ρ = 1/(kt + 1/ρ₀) | ρ: 10¹⁵ → 1.5×10¹⁴ m⁻² in recovery; up to 40 % of the work-hardening hardness recovered in pure Al | HBAL03 eq.4–5 pp.219–220; pp.216–217 |
| 27 | RX front velocity (atomic-jump model) | v = 2bνc_v (F_sa/kT) e^(−Q_a/kT), F_sa = F_s·Ω | ν = 10¹³ s⁻¹; c_v = 10⁻⁵ (700 K), 10⁻⁴ (800 K); Q_a ≈ 45 kJ mol⁻¹; v = 0.08 / 1.85 µm s⁻¹ at 427 / 527 °C (ρ = 10¹⁵). Trend use only (no solute or particles) | HBAL03 eq.9–12 p.224 |
| 28 | RX grain size from N and v | d = 2v t_c ∝ (v/N)^¼ (printed 2(2v/πN)^¼; 2(3v/πN)^¼ for consistency, derived) | grain size set mainly by nucleation density | HBAL03 eq.20–22 pp.227–228 |
| 29 | Critical nucleus radius | R_c = 2γ/F_s | Mao: 1–3 µm (γ 0.6–1.9 J m⁻²); 0.09–0.6 µm with γ = 0.324 J m⁻², F_s = 1–7 MPa (derived) | HBAL03 eq.8 p.221 |
| 30 | TM effect on RX temperature | ΔT_RX,start / ΔT_RX,finish (max) | Mn 0.77 at %: +30 / +25 K; Fe 0.04 at %: +65 / +35 K; Zr 0.09: +105 / +240 K; Sc 0.20: +120 / +320 K (after a 500 °C anneal + hot rolling + 450 °C anneal, i.e. pre-precipitated) | HBAL03 Tab.35 p.296 |
| 31 | Mn retained vs cooling rate; Mn decomposition | max Mn in (Al): 1.82 / 2.5 / 2.8 / 3–5 % at 10⁻¹ / 10 / 10² / 10³ K s⁻¹; decomposes > 325 °C (Al₆Mn 300–350 °C) | sets Mn_ss for a non-homogenised (strip-cast) route | HBAL03 Tab.33 p.294; Tab.34 p.295; p.299 |
| 32 | NHT anneal practice | T = lowest giving the softest state; fast heat-up; hold only until the load reaches T; cooling rate unimportant (not for Mg + Si alloys) | 1xxx, 3004, 3105, 5xxx 343 °C; 3003 413 °C [p.888]; 3105 345 °C, 3004 415 °C [p.299]; 3xxx 380–420 °C/0.5–1 h [W7] | HBAL03 pp.887–888, 299; W7 Tab.2 |

---

## 12. Open questions / gaps (prioritised)

1. **Missing core text:**
   - HH ch.7 (RX kinetics: JMAK n, Q, strain/T/heating-rate effects), ch.9 (PSN efficiency, Zener during RX, bimodal particles, **§9.8 precipitation–RX interaction and T–t–T**), ch.11 (grain growth and Zener variants), ch.12 (cube, P, ND-rotated cube), ch.13 (DRV, Z–subgrain relation, annealing after hot deformation) and ch.15 (industrial Al processing, can body).
   - Sheppard ch.3–5; Polmear §3.6 (foil/fin/canstock); Ryen §4.5.2 (AA3103 work hardening) and ch.5 (solute effects).
   - **Resolved 2026-10-12: Handbook of Aluminum** (full text read; Mao ch.4 integrated into §1–§11). It closes the "not extracted" notes on SIBM, the Johnson–Mehl n = 4 derivation, the parabolic grain-growth law and the classical Zener limit (now sourced), and adds anneal practice, TM effects on T_RX and the AA3104 cube/PSN competition. It does **not** close the HH-dependent items below: Mao is textbook-level and gives no Al values of k₀, n, Q_rex, PSN efficiency or T–t–T curves.
   - **Status 2026-10-12 for HH, Sheppard, Polmear, Ryen: still missing.**
     - The Drive download tool refuses HH (12.66 MB): *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API."*
     - Polmear (9.68 MB) is under that limit but still failed in transfer (the connector closed: "message from the server was too large or could not be parsed"), so the practical ceiling lies between a 2.84 MB PDF (3.8 M base64 characters, received intact) and a 9.68 MB PDF (failed).
   - Remedy: the user splits the PDFs into chapter files of a few MB (HH ch.7, 9, 11, 12, 13, 15; Polmear ch.3; Sheppard ch.3–5; Ryen ch.4–5) and uploads them to Drive, or downloads them via the standard Drive API outside this tool, then re-runs the extraction.
2. **3xxx-specific RX kinetics are not in hand:** k₀, n and Q of RX for AA3102, AA3103, AA3207 vs Mn_ss, Fe/Si, strain and heating rate. The C-curve for Mn dispersoid precipitation in cold-rolled 3xxx (start and finish vs T) is also missing. These need dedicated papers (e.g. Sjølstad, Nes/Marthinsen, Engler, Tangen, Somerday & Humphreys), none found in Drive.
   - Anchors added 2026-10-12 (HBAL03): model forms (Johnson–Mehl; industrial t₀.₅ form) [pp.227–228, 359]; Mn decomposition onset > 325 °C and Al₆Mn 300–350 °C [pp.295, 299]; T_RX increments of Mn and Fe after pre-precipitation [Tab.35 p.296]; Al–1Mn 95 % CR RX in 1 s at 620 °C [p.251]. Web chapter: JMAK n 3.0 → 0.8 (371 → 427 °C) under concurrent precipitation [ch12 §4]. **Still no (k₀, n, Q) set for a lean 3xxx or for T11-type chemistry**; for the slug route the trial programme (isochronal and isothermal hardness + conductivity on cold-rolled strip) is the realistic source.
3. Quantitative **solute-drag coefficients for Mn, Fe and Si in Al** (only Cu and Mg are shown qualitatively). Interaction of Mn_ss with recovery kinetics (U*, V in the Nes model).
   - HBAL03 adds v ∝ 1/c_Cu, the Lücke–Detert segregation form and the extreme Fe effect (Al–0.01 at % Fe at 150 °C) [pp.220, 225, 248], but **no drag coefficients** for Mn, Fe or Si.
4. **PSN nucleation efficiency** and the critical particle diameter as a function of strain for Al₁₅(FeMn)₃Si₂ and Al₆(Mn,Fe) constituents. HBAL03 checked in full (2026-10-12): qualitative only (§3.2). For the slug route, also the size distribution of Fe-rich constituents in rotary-cast, hot- and cold-rolled strip (needed with d*).
5. **Microsegregation of Mn** (k < 1, so cell centres are depleted (general knowledge)). Where do dispersoid-free zones form in DC vs twin-roll 3xxx, and are they the coarse-grain seeds (cf. Rob04 for Zr)? HBAL03 confirms that TM dendritic segregation is not easily removed by homogenisation (TM diffusivities 10⁻¹⁴–10⁻¹² cm² s⁻¹ at 500 °C) [p.295]; this matters more for the non-homogenised strip route. The location of dispersoid-free zones is still open.
6. Sag resistance, braze erosion vs grain size and shape: no quantitative source in Drive.
7. Taylor factor and texture-dependent stored energy for Al rolling components (only qualitative for Al [HH p.23]).
8. **User model check.** `AA3207_Recrystallization_Simulation.xlsx` has four saved versions; see chapter 09 §4.11 for the full comparison.
   - **Early versions (16:15, 16:17 — the only ones visible to this chapter's agent, via a search snippet):** for 70 % CR they predict
     - t₅₀ ≈ 2×10¹¹ s at 350 °C;
     - a "T_rx(50 % in 1 h)" of ≈812 °C (above the solidus);
     - a constant 5.6 µm Zener-capped grain size.

     This contradicts the literature anchors (3xxx O-anneal 380–420 °C/0.5–1 h [W7]; AA3103 ε = 2 RX in 45 s at 400 °C [Ryen03]; pure Al minutes at 380 °C [Pol06]). Their additive "Q_eff = 140 + 80·Mg + 667·Cu + 40·Mn" kJ mol⁻¹ is not supported by the sources: solute drag is non-linear (CLS, breakaway), and HP-Al HAGB migration Q is 63–67 kJ mol⁻¹ [HH Tab.5.2].
   - **Later versions (16:23, 16:26) are recalibrated:**
     - Q_eff = 145 kJ mol⁻¹, B₀ = 2.5×10²⁸, Zener cap 17.8 µm;
     - t₅₀ ≈ 298 s at 350 °C for 70 % CR, and ≈1,210 s for 45 % CR (chapter 09 §4.4–4.5, §4.11).

     These are in the range of the literature anchors above, but they rest on a single unsourced calibration point (chapter 09 §4, Assessment).
   - **Further literature anchors (HBAL03 full text, 2026-10-12):**
     - commercially pure Al recrystallises at 200–300 °C [HBAL03 p.220];
     - 95 % CR 99.998 % Al at 300 °C: primary RX at about 316 s, or 3162 s after a recovery pre-anneal [HBAL03 p.236];
     - Al–1Mn 95 % CR: RX complete in 1 s at 620 °C [HBAL03 p.251];
     - O-anneal practice 3105 345 °C, 3004 415 °C, 3003 "400–600 °C" [HBAL03 Tab.37 p.299]; 3003 413 °C and 3004/3105 343 °C, held only until the load reaches temperature [HBAL03 Tab.7 p.888];
     - Mn increases the RX start T by at most +30 K (0.77 at %, pre-precipitated) and Fe by +65 K (0.04 at %) [HBAL03 Tab.35 p.296];
     - HP-Al boundary velocity estimate 0.08 µm s⁻¹ at 427 °C for ρ = 10¹⁵ m⁻² [HBAL03 p.224];
     - RX grain size d ∝ (v/N)^¼ [HBAL03 eq.22 p.228]; Zener limit R_c = 4r/(3f) [HBAL03 eq.38 p.250].
9. Junit08's activation energies are unreliable (§2.4). Do not reuse them.
   - Re-assessed after the 2026-10-12 full-text pass: they are artefacts of fitting without C₁ and with X in %.
   - The pages that would allow a corrected Q (the 150 °C time series, Tables 4.5–4.8) are not in the Drive file. The file is a 24-page excerpt, so this item can only be closed with the complete thesis.
   - A clean recovery-kinetics data set for 1xxx/3xxx (σ or hardness vs t at ≥3 temperatures, the same strain, isothermal holds) is still needed for H-temper and recovery modelling. HBAL03 supplies only the functional form (second-order, ρ = 1/(kt + 1/ρ₀) [eq.5 p.220]), not Al rate constants.
10. **Data conflicts flagged in the HBAL03 full-text pass (2026-10-12)**. Resolve before using these numbers in models:
    - Mao's SFE 250 mJ m⁻², b = 0.35 nm and γ_HAGB 0.6–1.9 / 1.0 J m⁻² vs HH's 166 mJ m⁻², 0.286 nm and 0.324 J m⁻² (§1.4). This KB uses the HH values.
    - O-anneal temperatures for 3003/3004 differ between HBAL03 ch.5 (Tab.37), ch.19 (Tab.7) and W7 (§4.3).
    - DRX in Al–Mn and 99.5 % Al: Mao (flow curves) vs Karhausen & Korhonen (industrial: post-dynamic/static RX only) (§9.1).
    - Zener limit 4r/3F_V as a radius (Mao) or a diameter (common usage) (§6).
    - 1100-O UTS 75 MPa [HBAL03 Tab.3] vs ≈ 90 MPa [Pol06].
    - Mao's eq.22 coefficient and his Anderson–Mehl sentence are internally inconsistent (§4.2, §4.4).
11. **Slug-route data needed (new 2026-10-12):** Blade's figure (Fe effect on static RX after 50 % hot rolling, 500 → 390 °C) [HBAL03 Fig.28 p.244] is the closest literature analogue to the in-line hot mill, but its values are figure-only. Obtain Blade, *Metal Science* 13 (1979) 206–210, or measure the hot-band state (EBSD fraction RX, conductivity) on rotary-cast strip directly.
