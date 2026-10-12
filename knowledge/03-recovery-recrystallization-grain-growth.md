# 03 — Recovery, Recrystallisation (RX) & Grain Growth in Wrought Al Alloys

**Scope.** Physical metallurgy of softening after deformation, written for alloy and process design. The main focus is lean 3xxx alloys (AA3102, AA3103, AA3003, AA3207, AA3005), both as heat-exchanger, fin and foil alloys and as **annealed impact-extrusion slugs** (lean Al–Mn and Al–Fe–Si–Mg chemistries such as trial T11), with 1xxx, 8xxx (foil), 5xxx and 6xxx where the sources allow. The chain covered is: stored energy, then recovery, then nucleation of RX, then growth and kinetics, then particle and solute interaction (Zener, solute drag, concurrent precipitation), then grain growth, then texture, then hot working.

**Citation rules.** Every claim cites `[Key, section/page]`. Page numbers are the printed book or journal pages unless marked "PDF p.". Anything not found in the sources below is marked **(general knowledge)** and kept to a minimum. Values marked **(derived)** were calculated in this file from cited inputs; the assumptions are stated next to them. Translations from DE/SL are by the compiler.

**Coverage warning.** The Drive text extractor truncates large PDFs at about 400 k characters. Humphreys & Hatherly (HH) was therefore first available only up to §6.5.1 (p.188). **Resolved 2026-10-12: HH is now read as full text** (printed pp.1–574: all 16 chapters and both appendices; only the tail of the reference list and the subject index, pp.575–end, are missing). Its chapters on RX kinetics (ch. 7), two-phase alloys and PSN (ch. 9), grain growth (ch. 11), RX textures (ch. 12), hot deformation (ch. 13), continuous RX (ch. 14) and industrial control (ch. 15) are now used throughout; new content is marked "(added after full-text pass)" or "(corrected after full-text pass)". The truncation still affects Sheppard (ch. 3–5 missing; only pp.291–420 exist as text) and, for this chapter, Polmear §3.6 (a complete Polmear text now exists in the same Drive batch but was not read for this chapter). Where a topic is still missing, this document says so (see §12 Gaps). **The Handbook of Aluminum (HBAL03) is also complete:** the whole book was read as full text on 2026-10-12 (next paragraph and §0), so Mao's ch. 4 "Recrystallization and Grain Growth" is used throughout §1–§11.

**Application notes.** Paragraphs headed **"Relevance to the slug route"** apply the physics to the user's route: rotary caster 22 mm strip (≈500 °C) → in-line hot rolling (flexible split, exit ≈380 °C) → water-bath quench → cold rolling 30–50 % (up to 60 % under discussion; ε ≈ 0.36–0.92) → slug anneal → impact extrusion → lacquer bake 220 °C/10 min. Reference alloy: trial T11 (Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26 wt %; `knowledge/trials/T11.md`). These notes are inferences unless a citation is given.

**Full-text pass (2026-10-12).** Sources under 10 MB were downloaded whole and converted locally (`pdftotext -layout`). The results were:
- **HH (12.66 MB):** the one download attempt of the whole file was refused with *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API."* **Resolved later on 2026-10-12:** the user uploaded HH split into three parts (Drive folder "Cloud part book", files "11.pdf", "22.pdf", "33.pdf"; 4.0–4.6 MB each). They were downloaded and converted with `pdftotext -layout`. Coverage: front matter and pp.1–169 (11), pp.169–369 (22), pp.369–574 (33). Extraction caveats: "=" often prints as "¼", Greek letters, minus signs, the degree sign and µ are frequently lost ("mm" in the text usually means µm). **Every HH equation and every number read from an HH figure that is used below was checked against a rendered page image** (`pdftoppm`); values read from figures are marked "(read from figure)" with their reading uncertainty.
- **Pol06 (9.68 MB):** below the limit, but the transfer failed ("message from the server was too large or could not be parsed"). A complete two-part split ("111.pdf", "222.pdf") now exists in the "Cloud part book" folder, but it was not read for this chapter, so Pol06 §3.6 is still not used here.
- **Junit08:** the Drive PDF itself is a 35-page excerpt ending at printed p.24, so nothing more exists on Drive. Its method was re-assessed in §2.4.
- **Dav01, Leh06 and Bel05:** re-checked from the PDFs. The Leh06 tables are raster images and cannot be read without OCR. The Bel05 solubility tables were verified and added to §5.1 and §11 row 25.
- Sheppard (10.46–10.51 MB) and Ryen (11.22 MB) are over the limit and were not attempted. Sheppard part 2 of a later split (pp.291–420) is readable; part 1 (front matter to p.290, incl. ch.3–5) could not be downloaded.
- **HBAL03, second full-text pass (2026-10-12).** The whole book was obtained as a four-part copy (Drive folder "Cloud part book", see §0) and converted to text after a font-map repair. Read in full: **ch. 4 Mao, pp.211–258**. Also read: ch. 5 Katgerman & Eskin §1 (pp.259–264) and §3 incl. §3.1 commercial Al–Mn alloys (pp.293–299); ch. 7 Karhausen & Korhonen pp.355–360 (homogenisation, hot-rolling RX, AA3104 cube/PSN, Avrami model); ch. 19 Howard et al. §3.2 annealing (pp.887–888); ch. 22 Ridley pp.1114–1116 (Zener, PSN route); spot checks of ch. 3. Equations and tables used below (Mao eq.9–12, 22, 38; Katgerman & Eskin Tables 33–35, 37) were checked against rendered page images. **New content cites printed pages as [HBAL03 p.x].**

---

## 0. Sources

| Key | Source (author, title, year) | Drive link | Lang. | Readability / coverage |
|---|---|---|---|---|
| HH | F.J. Humphreys & M. Hatherly, *Recrystallization and Related Annealing Phenomena*, 2nd ed., Elsevier 2004 | [1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w](https://drive.google.com/file/d/1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w/view) | EN | **Full text, 2026-10-12 (catalog S-016).** Read from the user's three-part split in Drive folder "Cloud part book": "11.pdf" [1kdcjLTArHpJbXG4jMyHg8Vh7_SPiUhYe](https://drive.google.com/file/d/1kdcjLTArHpJbXG4jMyHg8Vh7_SPiUhYe/view) (front matter, pp.1–169), "22.pdf" [1F0KV8xyy8Qc1TEWmGA3h9DHAJV8hQisp](https://drive.google.com/file/d/1F0KV8xyy8Qc1TEWmGA3h9DHAJV8hQisp/view) (pp.169–369), "33.pdf" [1TIMU95pEW20oXXzITlKaeWGMTtTTdRRF](https://drive.google.com/file/d/1TIMU95pEW20oXXzITlKaeWGMTtTTdRRF/view) (pp.369–574). Missing: pp.575–end (rest of the references, subject index). Born-digital text; equations lose symbols, so all equations and figure readings used here were checked on rendered page images. Before the split, the whole file (12.66 MB, duplicate 17tHwICnSZ9xIRALcJHIYXZhVs9mQc-1D) was readable only to §6.5.1 (p.188) and its download was refused (*"File too large for download, over limit of 10 MB…"*). **Citations are printed pages [HH p.x].** |
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
| RX driving pressure, HH's working estimate (added after full-text pass) | P_d = E_D ≈ αρGb², α ≈ 0.5 | ρ = 10¹⁵ m⁻², Gb² ≈ 10⁻⁹ N | **≈ 1 MPa** "typical of a metal". The curvature back-pressure of a new grain, P_c = 2γ_b/R, equals P_d at **R ≈ 1 µm** (γ_b = 0.5 J m⁻² assumed by HH) | [HH eq.7.2–7.3 pp.219–220] |
| Matrix stored energy implied by the PSN growth criterion (added) | E_D = 4γ_b/d_g (inverting eq.9.2) | d_g read from Fig.9.13a (cold-rolled Al–Si) | ≈ 0.2 / 0.3 / 0.4 / 0.5 / 0.6 MPa at 30 / 40 / 50 / 60 / ≥ 80 % reduction (γ_b = 0.324 J m⁻²; **derived**) | derived from [HH eq.9.2, Fig.9.13 p.297] |
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
- **Scale of the driving pressure (added after full-text pass).** HH's own working value for RX is ≈ 1 MPa [HH eq.7.2 p.219]. The ≈ 7 MPa derived above from HH Tab.2.1 refers to torsion at 77 K to a shear of 6.75, an extreme state. For room-temperature rolling of Al to ε < 1 the PSN growth criterion implies only ≈ 0.2–0.6 MPa (row above, derived). Use ≤ 1 MPa for the slug route, not 7 MPa.
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
- **Subgrain coarsening kinetics (added after full-text pass)** [HH §6.5.2–6.5.3 pp.189–200]:
  - measured as D^n − D₀^n = c₁t. **n ≈ 2 in Al–1 % Mn** (Sandström et al. 1978), 99.99 % Al and Al–0.2 % Mg, but **n ≈ 4 in commercial-purity (99.5 %) Al** (Furu & Nes 1992); high-purity Al also gives large n or log D ∝ t [p.189];
  - the high n comes from the falling mean misorientation (hence falling γ_s and M) during growth where there is no orientation gradient [pp.190–192, 196];
  - usually only D/D₀ ≲ 2 is measured, because RX cuts subgrain growth short [p.190];
  - **in an orientation gradient** (Ω = dθ/dR) the misorientation rises as a subgrain grows, so growth stays fast: dR/dt = (Mγ_m/θ_m R)[θ₀ + Ω(R − R₀)] [HH eq.6.38 p.200]. Gradients > 5° µm⁻¹ occur at deformation heterogeneities; this is the physics of nucleation at transition bands and particle deformation zones (§3).
- **Particles and recovery (added)** [HH §6.6 pp.207–213]:
  - a fine dispersion pins subgrains: dR/dt = Mγ_s(α/R − 3F_V/2r) (α a geometric factor of order 1), which HH state gives a **limiting subgrain diameter of 4r/3F_V** for particle spacings ≪ subgrain size [HH eq.6.45–6.46 p.209];
  - **precipitation on the recovered substructure of a supersaturated alloy** occurs in **Al–Mn** (Morris & Duggan 1978); the particles sit on the LAGBs and pin strongly [HH §6.6.2.3 p.211];
  - **extended recovery:** if the pinning particles later coarsen, subgrains grow at the rate the particles coarsen, and a mainly LAGB structure persists (Al–6Ni: subgrains 0.8 µm at 100 °C → 2 µm at 500 °C with an unchanged misorientation distribution) [HH §6.6.2.4 pp.211–213]. Only if HAGBs come to dominate is "continuous RX" the right term.

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
| Subgrain growth, empirical (added after full-text pass) | D^n − D₀^n = c₁t; ideal (constant γ_s, no gradient) R² − R₀² = 2Mγ_s t | n ≈ 2 (Al–1Mn, Sandström 1978); n ≈ 4 (99.5 % Al, Furu & Nes 1992) | [HH eq.6.27, 6.35 pp.189–195] |
| Particle-pinned subgrain growth (added) | dR/dt = Mγ_s(α/R − 3F_V/2r) (α geometric, order 1) → D_lim = 4r/3F_V as stated by HH | valid when particle spacing ≪ subgrain size; for spacing ≈ subgrain size use the correlated forms of §6 | [HH eq.6.46 p.209] |
| Substructure strength (added) | σ = σ₀ + c₃D^(−m) | m ≈ 1 for well-developed subgrains, ≈ 0.5 for cells (Thompson review); "little agreement" | [HH eq.6.29–6.33 pp.192–193] |

**Diffusion data for Al** [HH Tab.5.1 p.129]: Q_self = 142, Q_core = 82, Q_boundary = 84 kJ mol⁻¹. At 500 °C: D(Mn) = 5×10⁻¹³, D(Cu) = 5×10⁻¹⁰, D(Mg, Si) = 1×10⁻⁹ cm² s⁻¹ [Pol06 p.105]. **Mn diffuses about 10³× slower than Cu and about 2×10³× slower than Mg or Si.** This is the root of Mn dispersoid stability and of its slow solute-drag kinetics.

### 2.3 Design levers (H-temper softening and stability)
- Partial annealing (H2x) works because recovery precedes RX in high-SFE Al [HH §6.2.1.3]. **Retained Mg/Mn in solution and fine dispersoids widen the recovery window before RX**, which gives a flatter softening curve and more robust H2x [HBAL03 PDF p.180; Pol06 p.43; Dav01 p.382].
- Increasing Mg and lowering the anneal T both give smaller recovered subgrains and higher retained strength [HBAL03 PDF p.180].
- Use **σ ∝ 1/δ** for recovered or hot-worked products (AA3104 hot-worked: linear σ vs 1/δ [Ryen03 Fig.2.25 p.34]). For cells (low T, Hall–Petch-type exponent m ≈ 1) vs subgrains (m ≈ ½) see [Pol06 p.36–37; HBAL03 PDF p.113–114].
  - *Conflict flagged (full-text pass):* HH quotes Thompson's review the other way round, **m ≈ 1 for well-developed subgrain boundaries and m ≈ 0.5 for cell structures**, and adds that there is "little agreement" [HH §6.5.2.3 p.193]. For hot-worked subgrains HH gives σ ∝ 1/D, σD/(Gb) = K ≈ 10 for fcc metals [HH eq.13.7 p.423], which supports m = 1 for subgrains. Fit m to your own data rather than assuming either assignment.
- **Work-hardening anchors for H tempers** (sheet, UTS / YS / El.) [HBAL03 Tab.3 p.264]: 1100-O 75 / 25 MPa / 30 %; 1100-H14 110 / 95 / 5; 1100-H18 150 / – / 4; 5052-O 170 / 65 / 19; 5052-H34 235 / 180 / 6; 5052-H38 270 / 220 / 4. Temper codes: H1 strain-hardened, H2 strain-hardened and partially annealed, H3 strain-hardened and stabilised [HBAL03 Tab.2 p.263]. *Conflict flagged:* 1100-O UTS is 75 MPa here but ≈ 90 MPa in [Pol06 p.129]; neither source explains the basis (minimum vs typical values are not stated), so do not calibrate to either alone.

**Relevance to the slug route.**
- The **lacquer bake (220 °C/10 min)** sits in the recovery range of the DSC anchor (100–250 °C for 99.998 % Al [HH Fig.6.3]). Recovery needs no incubation [HBAL03 p.217], so the heavily worked can wall will start to recover at once. In pure Al recovery can remove up to ~40 % of the work-hardening increment [HBAL03 p.217]; how much happens in 10 min at 220 °C is not quantified in the sources. In Mg + Si-bearing slugs (T11) solute clustering may offset part of this (T11 §2.2 item 3; hypothesis).
- A **slow heat-up of the slugs** spends time in the recovery range. *Corrected after full-text pass:* the earlier statement that this by itself markedly slows RX rested on one HBAL03 example (a 240 °C/600 s isothermal pre-anneal of 99.998 % Al made RX at 300 °C ~10× slower [HBAL03 p.236]). HH states that **for single-phase alloys there is no experimental evidence that slow heating retards RX through recovery**, because recovery and boundary migration have similar activation energies; prior recovery treatments of Al (Perryman 1955) had little effect, and uniform recovery in Al amounted to only ~20 % at X_V = 0.1 (Furu & Nes 1992) [HH §7.2.6.2 p.231; §7.4.2.2 pp.243–245]. **The heating-rate effect that matters for the slug route acts through precipitation from the supersaturated, quenched strip** (§5.2), where slow heating raised the 1 h RX temperature of Al–1.3Mn by 75 °C [HH Tab.9.1 p.312].

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
  - **Strain window (added after full-text pass):** in rolled Al SIBM is the **dominant mechanism below ~20 % reduction** (Bellier & Doherty 1977); above ~40 % reduction in pure Al it is replaced by nucleation of new orientations (Beck & Sperry 1950). The new grains keep the parent orientation, so SIBM-dominated RX keeps a texture close to the deformation texture [HH §7.6.2 pp.251–252].
  - **After hot deformation SIBM is again very important**, because the hot-deformed substructure is more homogeneous; the **cube texture of hot-rolled and annealed Al alloys forms by SIBM from cube bands** (Vatne & Nes 1994; Vatne et al. 1996) [HH pp.252–253; §12.4.1.2 p.404].
  - **Critical bulge size:** multiple-subgrain SIBM R_crit = 2γ_b/(P(1 − f)) (Bailey & Hirsch) or 2γ_b/(P(1 − f)^½) (Bate & Hutchinson), f = stored-energy ratio of the two grains; single-subgrain SIBM R_crit = 2γ_b/P = 4γ_bR₂/(3γ₂) with R₂, γ₂ the subgrain size and LAGB energy of the consumed grain [HH eq.7.41–7.44 pp.254–255].
  - With equal subgrain sizes and a mean misorientation > ~2°, subgrains ≥ 2.5× the mean (subgrains up to 3–4× the mean are normally present) can trigger SIBM; **single-subgrain SIBM dominates when misorientations exceed ~1°** and stored energies are similar. Al–0.1Mg cold rolled 20 % and annealed at 300 °C shows single-subgrain SIBM [HH §7.6.2.2–7.6.2.3 pp.255–257, Fig.7.31].
  - A particle dispersion replaces P by P − P_Z, raises both critical sizes and favours multiple-subgrain ("broad-front") SIBM; bulges then reach several hundred µm and favour cube grains [HH §9.4.1.2 pp.305–306].
- **Subgrain coalescence** produces a subgrain larger than the critical size by climb-out of the dislocations in the shared walls (with a slight rotation); repeated coalescence turns its boundary into a mobile HAGB [HBAL03 p.222, Fig.11].
  - *Conflict flagged (full-text pass):* HH find "no convincing evidence" that rotation and coalescence play a significant role in subgrain coarsening or in nucleation; all in-situ TEM/HVEM observations of nucleation show **LAGB migration**, with no significant role for coalescence. HH model both subgrain coarsening and nucleation as LAGB-migration controlled [HH §6.5.5 pp.206–207; §7.6.3 p.258]. This KB follows HH.
- **Classical critical nucleus radius** [HBAL03 eq.7–8 p.221]: ΔF = −(4/3)πR³F_s + 4πR²γ, so R_c = 2γ/F_s.
  - Mao's estimate: F_s = 1.53×10⁶ J m⁻³ (ρ = 10¹⁵ m⁻²) and γ = 0.6–1.9 J m⁻² give **R_c ≈ 1–3 µm**, "approaching the size order of deformation cells" [HBAL03 p.221].
  - With this KB's constants (γ = 0.324 J m⁻² [HH Tab.4.2]; F_s ≈ 1.0–7 MPa, §1.2) R_c ≈ 0.09–0.6 µm (derived).
  - *Added after full-text pass:* HH discount classical (fluctuation) nucleation for RX because the driving force is small and the HAGB energy large; the critical radius (> 0.1 µm) makes the nucleation rate negligible. **RX "nuclei" are pre-existing subgrains or cells** that grow by LAGB migration where there is a **large orientation gradient**, so that a HAGB forms after a little growth: nucleation is "no more than discontinuous subgrain growth at sites of high strain energy and orientation gradient" [HH §7.6.1–7.6.3 pp.250–259]. Mao's R_c is therefore a size criterion for a pre-existing subgrain, not a fluctuation nucleus.
  - R_c is smaller where ρ is locally higher; this is why **grain boundaries and particles are the preferred (heterogeneous) sites** [HBAL03 pp.222–223]. Shown: nuclei along grain boundaries (high-purity Al–0.008 Cu; forged Al–0.01 Ti) and **around second-phase particles in rolled Al–1.3 wt % Mn** (P. Yang 1996; Engler, Yang & Kong 1996) [HBAL03 p.223, Fig.12].
- **Particles can accelerate RX.** Particles normally retard boundary migration, but where they trigger "drastic heterogeneous nucleation" RX is faster overall; observed with Al₂Cu and Al₃Fe particles [HBAL03 p.226].
- **Continuous (in-situ) RX** [HBAL03 pp.228–229]: when HAGB migration is blocked (e.g. by precipitates), only "extremely strong recovery" occurs; HAGBs form slowly by subgrain coalescence and the **deformation orientations are kept** (no new texture).
  - *Terminology corrected after full-text pass:* HH call particle-controlled subgrain growth on precipitates "no more than recovery" and state that describing it as "continuous recrystallization" or "recrystallization in situ" is incorrect; the right term is **extended recovery** unless the final structure is mainly HAGBs [HH §9.8.2.2 p.313; §6.6.2.4 pp.211–212]. True continuous RX in Al needs **very large strains** (> 95 % rolling; Oscarsson et al. 1992); AA8006 cold rolled to ε = 0.69 and annealed at 250 °C recrystallised **discontinuously** [HH §14.3 pp.453, 457–458, Fig.14.5]. The slug route (ε ≤ 0.92) is therefore in the discontinuous regime.
  - 99.9 % Al forged 25 % in two perpendicular directions: continuous RX complete after ~40 min at 350 °C; Fe- and Si-bearing precipitates on the original boundaries blocked migration [HBAL03 pp.228–229, Fig.15].
  - High-purity Al–Fe (Ito, Musick & Lücke 1983): continuous RX is obvious **around 400 °C once Fe exceeds 0.01 wt %**, because many FeAl₃ particles form on the boundaries [HBAL03 p.229].
- **PSN (particle-stimulated nucleation)** [HH §2.9.3–2.9.4 pp.57–64; Pol06 p.42; HBAL03 PDF p.142]:
  - Requires non-deformable particles that develop a **deformation zone**: a rotated, finely subdivided, highly misoriented region about one particle diameter thick.
  - **d < 0.1 µm: no zones** (relaxation by prismatic loops).
  - **0.1–2.5 µm: zone misorientation depends on size and strain.**
  - **d > 2.5 µm: zone misorientation depends on strain only** (Humphreys 1979a, single crystals) [HH pp.60–61].
  - In rolled polycrystals the zone is elongated in RD, holds subgrains below 0.1 µm close to the particle, and shows 30–40° misorientation to the matrix even after large strains [HH §2.9.4.3 p.62; Fig.2.38 AA1200 75 % CR, 3 µm particle].
  - Practical PSN threshold: **"coarse intermetallic compounds having sizes generally greater than about 1 µm"** [Pol06 p.42]. HH give the same absolute lower bound ("usually only … greater than approximately 1 µm"; 0.8 µm inferred for Fe–C) [HH §9.3 p.293]. *Refined after full-text pass:* **1 µm is the large-strain limit. At the 30–60 % cold reductions of the slug route the critical diameter is ≈ 3–7 µm** (§3.2b, [HH Fig.9.13 p.297]).
  - Two conditions apply [Pol06 p.42]:
    - (i) the zone's stored energy must allow rapid subgrain migration;
    - (ii) the nucleus must be large and stable enough to grow into the lower-energy matrix.
  - The PSN-capable particle size **decreases with lower deformation T and higher strain rate** [HBAL03 PDF p.142].
  - PSN generally **randomises texture** (it deviates from cube) [HBAL03 PDF p.143; Leh06 p.177]. HH refine this: PSN nuclei lie inside the deformation-zone orientation spread; in single crystals or after small strains PSN gives a fairly sharp texture rotated ~30–40° about <112>, and only in **heavily deformed polycrystals** do the nuclei become weakly textured or near-random [HH §9.3.2 pp.298–300; §12.2.4.1 pp.391–392].
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
- *Resolved after full-text pass (2026-10-12):* the PSN efficiency and the strain dependence of the critical particle size are now sourced from HH §9.3 (§3.2b below). The previous general-knowledge placeholder ("critical diameter of order 1 µm at moderate strains") was **too optimistic for moderate strains** and is withdrawn. HBAL03 treats particle nucleation only qualitatively [HBAL03 pp.130, 223, 226, 357–358].

### 3.2b PSN criteria, critical particle diameter and efficiency (added after full-text pass)

**Mechanism** [HH §9.3.1 pp.294–298]:
- In-situ HVEM annealing of rolled Al and Al–Si (Humphreys 1977): RX starts at a pre-existing subgrain **inside the deformation zone** (not necessarily at the interface) by rapid sub-boundary migration. The grain may stop growing when the zone is consumed.
- Two conditions must both be met:
  1. **formation**: the zone misorientation must reach a HAGB. The time to form a nucleus scales as 1/Ω² (Ω the orientation gradient), so sites next to the particle surface are favoured [p.296];
  2. **growth**: the nucleus, of size ≈ the particle diameter, must outgrow its own curvature pressure using the stored energy of the matrix beyond the zone.
- **Growth criterion:** D ≥ 4γ_b/(αρGb²), α ≈ 0.5 [HH eq.9.1]; with the nucleus size set equal to the particle diameter, **d_g ≥ 4γ_b/(αρGb²) = 4γ_b/E_D** [HH eq.9.2 p.297]. E_D rises with strain, so **d_g falls with strain**. After low-temperature deformation the **growth** condition, not formation, decides whether PSN occurs [p.298].
- **Measured critical diameter vs cold-rolling reduction** (Al–Si single crystals, Humphreys 1977) [HH Fig.9.13a p.297] (read from figure):

| Rolling reduction | ε = ln(t₀/t) (derived) | Particles without PSN (µm) | Particles with PSN (µm) | d_g on HH's boundary curve (µm; read ±0.5) |
|---|---|---|---|---|
| 25 % | 0.29 | 4.6, 4.9 | 10 | ≈ 8–9 |
| 30 % | 0.36 | — | — | ≈ 7 |
| 40 % | 0.51 | — | — | ≈ 4.5–5 |
| 50 % | 0.69 | ≤ 3.0 | 4.6, 4.9, 10 | ≈ 3.3–3.5 |
| 60 % | 0.92 | — | — | ≈ 2.7 |
| 80 % | 1.61 | ≤ 1.5 | ≥ 2.3 | ≈ 2.1 |
| 95 % | 3.0 | ≤ 1.5 | ≥ 2.3 | ≈ 1.9 |

  Rows without data points are interpolated on HH's experimental curve. The growth criterion calculated with the zone dislocation density (eq.2.25) reproduces the trend [Fig.9.13b]. *Caveat:* single crystals; polycrystals add grain-boundary sites and particles at grain boundaries are favoured [p.302], so d_g in commercial strip may be somewhat lower (inference).
- **Efficiency** [HH §9.3.3 pp.301–302; §9.3.5 pp.302–303]:
  - normally **at most one grain per particle**; several grains per particle only for particles > 5–10 µm;
  - with efficiency 1 the grain size is **D ≈ d·F_V^(−1/3)** [HH eq.9.3]. The minus sign of the exponent is lost in the PDF; HH Fig.9.17 confirms −1/3 (d = 10 µm, F_V = 0.1 → ≈ 21 µm; d = 2 µm, F_V = 0.1 → ≈ 4 µm; read from figure);
  - near the critical size the efficiency is "very low" (Humphreys 1977; Wert et al. 1981; Ito 1988). High efficiency needs site saturation and similar growth rates;
  - measured: Al–0.8Si {110}<001> crystals with 3 µm Si particles: at ε = 0.7 the PSN grains survive only as small "island" grains inside much larger grains; at ε = 1.4 the structure is equiaxed with a grain size corresponding to **efficiency 0.85** (Ferry & Humphreys 1996) [Fig.9.19];
  - **derived:** Al–Si, 50 % cold rolled, annealed at 300 °C, F_V = 0.01 of 4.9 µm particles → D = 44 µm [HH Tab.11.3 p.374; Fig.9.2b]. Eq.9.3 with efficiency 1 gives 22.7 µm, so the implied **efficiency ≈ (22.7/44)³ ≈ 0.14** (D ∝ N^(−1/3)). Here d is only ~1.5× d_g;
  - particles at grain boundaries, shear bands and similar sites are favoured, which lowers the overall efficiency (Al–Mn and Al–Fe–Si; Sircar & Humphreys 1994) [p.302].
- **Particle clusters** [HH §9.3.4 p.302]: nucleation is favoured at pairs or groups of particles **even when each particle is below the critical size** (Al–Si near the critical size, Koken et al. 1988). Clustering also makes RX macroscopically inhomogeneous [HH §7.4.1 p.241].
- **Growth disadvantage of PSN grains** [HH §9.3.5 pp.303–304, Fig.9.20]: PSN grains nucleate early but may grow more slowly (restricted orientations, smaller nuclei with a larger P_c). Mobility ratios of 1.2–3 between grain classes leave the slow grains as small boundary grains or islands.
- **Kinetics and grain size vs particle size** (Al–Si, 50 % cold rolled, annealed at 300 °C; Humphreys 1977) [HH Fig.9.2 p.288] (read from figure):

| Particle diameter (µm) | 0 (single phase) | 0.7 | 1.5 | 2.4 | 3.1 | 4.6–4.9 |
|---|---|---|---|---|---|---|
| t₀.₅ (s) | ≈ 5000 | ≈ 1000 | ≈ 500 | ≈ 240 | ≈ 80 | ≈ 30–60 |
| RX grain size (µm) | ≈ 200 | ≈ 160 | ≈ 145 | ≈ 95 | ≈ 90 | ≈ 45 |

  Particles below d_g (≤ 3 µm at 50 %) still accelerated RX and halved the grain size. This fits HH's rule that dispersions with F_V/r below ≈ 0.2 µm⁻¹ often **accelerate** RX even when the particles are too small for PSN (extra stored energy from geometrically necessary dislocations) [HH §9.2.1 p.289]. The 0.7 µm alloy had F_V = 0.0012 [HH Tab.11.3]; the F_V of the other alloys is not given.
- **Bimodal particles (coarse constituents + fine dispersoids)** [HH §9.5 pp.306–307]: d_g = 4γ_b/(P_D − P_Z) = **4γ_b/[(ρGb²/2) − (3F_Vγ_b/2r)]** [HH eq.9.8], F_V and r of the fine particles. Fine particles raise d_g, so fewer constituents qualify and the grain is coarser: **D_N ≈ N_d^(−1/3)**, N_d = number per unit volume of particles larger than d_g [HH eq.9.9]. The RX kinetics then follow the fine dispersion; island grains and a stronger (cube-dominated) texture are typical [pp.307; §12.4.3.3].

**PSN after hot deformation** [HH §13.6.4 pp.448–450]:
- At high temperature dislocations bypass particles without building a deformation zone. Critical strain rate for zone formation (Humphreys & Kalu 1987): **ε̇_c = K₁exp(−Q_s/RT)/(T d²) + K₂exp(−Q_b/RT)/(T d³)**, with **K₁ = 1712 m² s⁻¹ K, K₂ = 3×10⁻¹⁰ m³ s⁻¹ K** for Al alloys [HH eq.13.23]. For d > 1 µm the first term dominates and **d_f = (K₁/(TZ))^½** [HH eq.13.24].
- The growth criterion becomes d_g = 4γ_bD/(3γ_s) with the hot-deformed subgrain size D, i.e. d_g ∝ Z^(−1/m) through σD/(Gb) = K [HH eq.13.25–13.27].
- **Map** [HH Fig.13.31 p.450] (read from figure): below Z ≈ 10¹² s⁻¹ PSN is limited by **zone formation** (critical d ≈ 15 µm at Z = 10¹⁰, ≈ 1.7 µm at 10¹²); above it by **nucleus growth** (≈ 1.7 µm at 10¹² falling to ≈ 0.3 µm at 10¹⁶ s⁻¹). Al–Si at 10⁸ < Z < 10¹² was zone-formation controlled (Kalu & Humphreys 1986); AA3004 and AA3003 at 10¹² < Z < 10¹⁶ were growth controlled (Oscarsson et al. 1987; Furu et al. 1992).
- Low Z (hot, slow) therefore suppresses PSN and lets cube grains dominate; PSN-derived random texture rises with Z [HH §12.4.3.2 p.409; §15.2.2.3 p.475].

**Relevance to the slug route (PSN, added after full-text pass).**
- **Cold strain.** At 30 / 40 / 50 / 60 % cold reduction the critical PSN diameter is ≈ 7 / 4.5–5 / 3.3–3.5 / 2.7 µm (table above). Only the coarse tail of the Fe-rich constituent population counts, and particles just above d_g nucleate with low efficiency (≈ 0.14 derived for d ≈ 1.5 d_g).
- **Illustrative grain-size estimate (derived; inputs assumed, not measured).** With D ≈ d·(η·F_V,>d_g)^(−1/3) (eq.9.3 with efficiency η), d = 4 µm and η = 0.14: F_V,>d_g = 0.0005 / 0.001 / 0.003 / 0.01 gives D ≈ 97 / 77 / 53 / 36 µm (with η = 1: 50 / 40 / 28 / 19 µm). T11's ≈ 1.5–2 vol % of Fe-rich constituents [T11 §2.2] lands in the 20–100 µm slug window only if roughly 0.05–1 vol % of it is coarser than d_g. **The slug grain size is therefore set by the size-distribution tail above ≈ 3–7 µm, which is exactly what fast rotary-caster solidification shrinks** [HBAL03 p.122]. If too few constituents exceed d_g, nucleation falls back on grain boundaries, transition bands and SIBM, and the grain coarsens toward the ≈ 200 µm of particle-free Al–Si at 50 % (Fig.9.2b) or becomes duplex.
- **In-line hot mill (derived from HH eq.13.24 with Q = Q_self = 142 kJ mol⁻¹ [HH Tab.5.1] and assumed strain rates of 1–30 s⁻¹, which are not measured):** Z ≈ 4×10⁹–1×10¹¹ s⁻¹ at 500 °C gives d_f ≈ 24–4 µm; Z ≈ 2×10¹¹–7×10¹² s⁻¹ at 380 °C gives d_f ≈ 3.4–0.6 µm. Deformation zones (and hence hot-band PSN sites) form mainly in the cooler, later part of the hot pass and only at the coarser constituents. Because the hot band is quenched, these zones are recovered rather than consumed by static RX (inference; §9).
- **Levers:** (i) raise ε_cold (at ε ≥ 1.6, d_g ≈ 2 µm), as already proposed for the T11 trial [T11 §2.4]; (ii) keep fine precipitates out of the anneal (bimodal eq.9.8 raises d_g); (iii) measure the constituent size distribution (number per mm² above 2, 3, 5 and 7 µm, and clustering) in the cold-rolled strip.

### 3.3 Design levers
- **For fine, equiaxed, near-random grains** (formability, low earing contribution from PSN, uniform anodising/brazing response):
  - maximise the number density of particles **larger than the strain-dependent d_g** (≈ 2 µm at ≥ 80 % cold reduction, ≈ 3.5 µm at 50 %, ≈ 7 µm at 30 % [HH Fig.9.13]; Fe- and Si-bearing constituents, α-Al(Fe,Mn)Si);
  - use high cold reduction (it lowers d_g and raises the efficiency, e.g. 0.85 at ε = 1.4 vs islands at ε = 0.7 [HH §9.3.5]);
  - keep the fine-dispersoid level low: F_V/r below ≈ 0.15–0.2 µm⁻¹ [HH §9.2.1, eq.9.5], and below the optimum level A of HH Fig.9.21 (§4.6);
  - avoid fine precipitation inside the deformation zones before RX (i.e., anneal fast, with Mn and Si already precipitated or kept in solution, see §5).
  - In 1xxx sheet, more Fe/Si as constituents gives more PSN-capable particles and finer annealed grain [HBAL03 PDF p.152, Fig.47].
- **For strong cube** (cube/rolling-texture balance for earing; directional properties): promote transition-band nuclei and suppress PSN. This means lower constituent density, or **fine dispersoids/secondary precipitates that neutralise deformation zones** [Leh06 p.178; HBAL03 PDF p.143]. HH confirm all three routes in Al alloys: small particles present during deformation, bimodal particles, and precipitation during the anneal all strengthen cube, because Zener drag raises the critical nucleus size and favours broad-front SIBM from cube bands [HH §12.4.3.3 pp.410–411]. After hot rolling, cube comes from cube bands by SIBM, and is favoured by low Z [HH §12.4.1.2 p.404; §13.2.4].
- **For coarse grains** (sag resistance, crack deflection, creep; see §5): reduce nucleus density. Use few large particles, low strain, and precipitation that pins sub-boundaries before nucleation.

**Relevance to the slug route.**
- Three features of the route each push toward **fewer PSN nuclei**, and hence a coarser slug grain:
  1. the cold reduction is low (30–50 %, ε ≈ 0.36–0.69), which raises the critical particle size to ≈ 3.5–7 µm (sourced after the full-text pass: [HH Fig.9.13], §3.2b);
  2. rotary-caster solidification is faster than DC, which makes the constituents finer [HBAL03 p.122];
  3. fine Fe/Mn/Si precipitates forming in the deformation zones during a slow heat-up cancel nuclei [HBAL03 PDF p.152].
- Against this, stored energy and misorientation that survive from the hot mill (§9) add driving force and nucleation sites (inference; see §9 for the HH evidence on hot-deformed substructures).
- T11's ≈ 1.5–2 vol % of Fe-rich constituents (T11 §2.2) is a large PSN reservoir only if enough of it is **coarser than d_g (≈ 3–7 µm at 30–60 % cold reduction)**; ≥ 1 µm is not enough (corrected after full-text pass). **Measure the constituent size distribution in the cold-rolled strip** (number per mm² above 2, 3, 5 and 7 µm; clustering); it is the main input for the PSN grain-size estimate of §3.2b and §4.6.

### 3.4 Pitfalls
- Measured angle–axis misorientations at particles (30–40°) can underestimate the physical rotation, because random cubic orientations average about 40° [HH p.63].
- Large inclusions also nucleate *deformation bands* [HH §2.9.2.3 p.56].
- Constituent stringers are aligned in RD after breakdown [Pol06 p.78], so PSN nuclei come in clusters, which gives banded grain sizes.
- **Do not use the 1 µm PSN threshold at moderate strain** (added after full-text pass): it applies to heavy reductions; at 50 % reduction 3 µm Si particles did not nucleate [HH Fig.9.13a].
- **Do not assume efficiency 1.** Near d_g the efficiency is very low (≈ 0.14 derived at d ≈ 1.5 d_g), and PSN grains can end up as islands inside faster-growing grains at low strain [HH §9.3.3, §9.3.5].
- **Bimodal grain structures are typical** when PSN competes with other sites: heavily rolled AA1050 with 0.5 % of 1–7 µm particles gave small PSN grains (< 10 µm) at particles and clusters next to large cube grains (> 100 µm) (Juul Jensen et al. 1985) [HH §12.4.3.1 p.409].

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
- **JMAK theory and exponents (sourced after full-text pass; previously general knowledge)** [HH §7.3 pp.232–239]:
  - X_V = 1 − exp(−B tⁿ), B = f Ṅ Ġ³/4 for constant nucleation and growth rates (f = 4π/3 for spheres) [HH eq.7.16–7.17];
  - ideal exponents [HH Tab.7.3 p.234]: **3-D growth n = 3 (site saturation) or 4 (constant Ṅ)**; 2-D: 2 or 3; 1-D: 1 or 2. A decreasing Ṅ gives 3 < n < 4; random grain-boundary nucleation gives n falling from 4 to 1 during the transformation (Cahn 1956);
  - **JMAK assumes randomly distributed nuclei**, which real materials rarely have [p.234];
  - JMAK plot: ln ln(1/(1 − X_V)) vs ln t; slope = n. Global growth rate from the RX/unRX interface area S_V (Cahn & Hagel): **Ġ = (1/S_V)(dX_V/dt)** [HH eq.7.18 p.234]. The microstructural-path method (Vandermeer & Rath) adds S_V and the largest-grain size to separate nucleation and growth [HH §7.3.2 pp.235–238].
- **Exponents measured in Al (added)** [HH §7.3.1.2, §7.4 pp.234–248; §13.6.2 p.447]:
  - n ≈ 4 only for fine-grained Al lightly strained in tension (Anderson & Mehl 1945), where there is < 1 successful nucleus per old grain;
  - **n = 1.7 for Al–0.0068 at % Cu cold rolled 40 %**, with negative curvature at long times at the lower annealing temperatures (Vandermeer & Gordon 1962) [Fig.7.12 p.235]; "numerous" Al studies give n of the order of 1;
  - **static RX after hot deformation: n ≈ 1.5–2** (Roberts 1984, 1985) [HH p.447];
  - cause: mainly **inhomogeneity** (non-random nucleation sites, a stored energy that varies between and within grains), with recovery a secondary factor. If Ġ = C t^(−r) under site saturation, **n = 3(1 − r)**; n = 2 implies r = 0.33 [HH eq.7.33–7.35 pp.242–243]. In Al, uniform recovery was only ~20 % at X_V = 0.1 (Furu & Nes 1992) and could not explain the falling growth rate [p.245]. Nucleation at large particles gave **two-stage growth kinetics** in an Al alloy (Vandermeer & Juul Jensen 2001) [p.246].
- **Activation energy (added)** [HH §7.2.6.1 pp.229–231]: t₀.₅⁻¹ = C exp(−Q/kT) [HH eq.7.5] fits isothermal data, but the apparent Q refers to the whole process, depends on strain and is very sensitive to purity: **0.0068 at % Cu raised Q_RX of pure Al from 60 to 120 kJ mol⁻¹** (Vandermeer & Gordon 1963). Only the growth term (Ġ = C₂ exp(−Q_G/kT)) has a clear atomistic meaning; a constant nucleation rate is rarely found [eq.7.6–7.7].
- A literature value from the web chapter: n fell from 3.0 at 371 °C to 0.8 at 427 °C in deformed, supersaturated Al–Mn under concurrent precipitation (ch12 §4, [W12-19], abstract only); this fits HH's Regime II description of §5.2 (RX amount set by temperature, almost independent of time) (inference). HBAL03 gives **no Q_rex or n values for Al alloys**.
- t₅₀ = (ln2/k)^(1/n) for X = 1 − exp(−k tⁿ) with k = k₀ exp(−nQ/RT) remains (general knowledge, algebra).
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
| **Rows below added after HH full-text pass** | | |
| Commercial-purity vs zone-refined Al, large rolling reductions | RX temperature **200 °C vs 50 °C** (Dimitrov et al. 1978) | [HH Tab.7.2 p.228] |
| Super-pure Al vs Al + 0.004 / 0.007 / 0.020 % Fe in solution, 80 % CR, 30 min anneals | super-pure: microhardness ≈ 36 as rolled, softening from ≈ 150–200 °C, soft (≈ 20) at 300 °C. Fe-bearing grades: ≈ 40–44 as rolled, still ≈ 30–33 at 300 °C, soft (≈ 20–22) only at 350 °C (Marshall & Ricks 1992). HH: very small Fe contents in solution "may increase the recrystallization temperature by 100 °C" | [HH Fig.7.10 p.229; p.228] (read from figure) |
| Al–0.0068 at % Cu, 40 % CR | JMAK n = 1.7; Q_RX 120 vs 60 kJ mol⁻¹ for pure Al | [HH Fig.7.12 p.235; p.231] |
| Al–Si, 50 % CR, 300 °C | t₀.₅ ≈ 5000 s particle-free → ≈ 30–60 s with 4.6–4.9 µm Si (PSN); grain 200 → 45 µm | [HH Fig.9.2 p.288] (read from figure) |
| Al–1.3 Mn supersaturated, cold rolled (80 % in HH Fig.9.24) | RX complete in 1 h at **425 ± 5 °C with fast heating (500 °C s⁻¹)** vs **500 ± 20 °C with slow heating (10 °C h⁻¹)**; Al–0.25Zr 380 vs 480 °C; Al–0.25Sc 575 vs 550 °C (Humphreys et al. 2003) | [HH Tab.9.1 p.312] |
| CP Al hot deformed to ε = 3, annealed at 410 °C | t₀.₅ ≈ 95 s (Z = 6.3×10¹³ s⁻¹), ≈ 140 s (1.08×10¹³), ≈ 1500 s (1.16×10¹² s⁻¹) (Gutierrez et al. 1988) | [HH Fig.13.29 p.446] (read from figure) |
| AA8006 cold rolled ε = 0.69, 250 °C | discontinuous RX (continuous RX only after ε = 3.9, 300 °C) | [HH Fig.14.5 p.458] |
| Hot-rolled AA3004/3104 can-body hot band | no RX between finishing passes; RX on coiling (3–4-stand mills, 2.5 mm) or in a separate furnace anneal at **350 °C** (single-stand mills) | [HH §15.2.2.2–15.2.2.3 pp.474–475] |

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
  - *Added after full-text pass:* the minimum strain is **typically 1–3 %**; above it the RX rate rises and **levels out at true strains of 2–4** [HH §7.2.1.1 p.222]. The slug route (ε_cold ≈ 0.36–0.92) is therefore on the steep part of the rate–strain curve, where small changes in reduction matter.
  - **"Laws of recrystallization"** (Mehl; Burke & Turnbull) [HH §7.1.2 pp.220–221]: (i) a minimum strain is needed; (ii) T_RX falls as the anneal time rises; (iii) T_RX falls as the strain rises; (iv) **the RX grain size depends primarily on strain** (nucleation is more strain-sensitive than growth); (v) a larger starting grain size or a higher deformation temperature raises T_RX.
  - **Strain path:** redundant (reversed) strain is less effective. In Cu the equivalent strain is ε_perm + 0.65·ε_red [HH eq.7.4 p.223]. In Al, reversed or multi-axis deformation to the same strain recrystallised more slowly and **to a much larger grain size** (Embury et al. 1992; Zhu & Sellars 1997), because strain reversal lowers the dislocation density [pp.223–224]. Shear in the roll gap changes sign near the surface [p.223], so surface layers may behave as if less strained (inference).
  - **Initial grain size:** fine-grained material recrystallises faster (more boundary sites; at ε < 0.5 higher stored energy), but coarse grains form more deformation and shear bands; in a Cu study the 20× faster growth in fine-grained material was mainly an orientation effect [HH §7.2.3 pp.227–228].
- **Temperature/time.** RX starts at a "definite temperature" that depends on composition, time and work hardening [Pol06 p.41]. Too-long annealing gives coarse grain [W7 p.5].
- **Heating rate.**
  - Texture and final grain size depend on heating rate, T and time [Pol06 p.39].
  - Slow heating lets dispersoids form before RX [Røy05 p.35].
  - The AMAG coil anneal (300–400 °C, 2–5 h) before a fast continuous solution treatment gave coarse elongated grains vs fine equiaxed grains without it (AA2024) [AMAG14 p.14].
  - Non-heat-treatable alloys are heated "very quickly to avoid grain growth" [HBAL03 p.887].
  - **Recovery before RX** lowers the driving force: RX of 95 % CR 99.998 % Al at 300 °C took ~10× longer after a 240 °C/600 s pre-anneal, and the texture became sharper (§8.2) [HBAL03 p.236].
  - *Corrected after full-text pass (conflict flagged):* HH state that the recovery mechanism for a heating-rate effect "is frequently cited" but has **no experimental support in single-phase alloys**, since recovery and boundary migration share similar activation energies; in very pure metals slow heating might even promote RX. Prior recovery anneals had little effect on Al (Perryman 1955) and Fe (Rosen et al. 1964) [HH §7.2.6.2 p.231; §7.4.2.2 pp.244–245]. The HBAL03 example above is a single 99.998 % Al case; do not generalise it.
  - **The heating-rate effect that is well documented acts through precipitation** [HH §7.2.6.2 pp.231–232; §9.8.2.1 p.312]: in a supersaturated alloy, slow heating lets precipitation occur before RX; rapid heating lets RX finish first. Industrially, **rapid heating accelerates RX and gives a smaller grain size** (Al–Li, Bowen 1990; Al–Zn–Mg, Wert et al. 1981). Slow heating (10 °C h⁻¹) raised the 1 h RX temperature of cold-rolled Al–1.3Mn from 425 to 500 °C and of Al–0.25Zr from 380 to 480 °C (§5.2) [HH Tab.9.1 p.312].
- **Strain and temperature in the JM picture.** d ∝ (v/N)^¼ [HBAL03 eq.22 p.228]. *Inconsistency flagged:* the text says Anderson & Mehl found "the ratio v/N is increased with increasing tensile deformation or with arising annealing temperature, which would result in refined grain size" [HBAL03 p.228]. By the chapter's own eq.22 a larger v/N gives a **coarser** grain, so either "v/N" should read "N/v" or "refined" is wrong. Do not quote this sentence as evidence. That the RX grain size falls with prior strain is supported independently [HH §1.2.1.3 pp.5–6].
- **Solute.** Fe in solid solution raises the RX start temperature by precipitating fine Al–Fe particles during the anneal (high-purity 1xxx) [HBAL03 PDF p.152]. Mn raises the RX temperature and promotes fibrous structures [Dav01 p.382]. Cr and Mn raise RX temperatures in 5xxx [Pol06 p.130].
  - *Added after full-text pass:* solutes usually hinder RX, mainly by lowering the boundary mobility (growth) rather than nucleation [HH §7.2.4 pp.228–229]. HH single out Fe in Al as "a very potent solute": 40–200 ppm Fe in solution raised the softening temperature of 80 % cold-rolled Al by ≈ 50–100 °C, and HH state that very small Fe contents "may increase the recrystallization temperature by 100 °C" (Fig.7.10, §4.3 table). In AA1xxx, < 100 ppm Fe in solution strongly slows RX, and more Fe precipitates on the RX front [HH §15.2.1.1 p.470].
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
- **Measuring X_V (added after full-text pass)** [HH App.2 pp.545–549]: hardness or resistivity give only indirect RX fractions (Al softens extensively by recovery before RX, Fig.7.18b). Point counting needs ≈ 500 points at X_V = 0.5 (σ²/X_V² = (1 − X_V)/n_r) and is impractical below X_V ≈ 0.1. **EBSD pattern-quality methods do not work reliably in Al** because its subgrains are clean; use HAGB-based linear-intercept or map analysis instead. For ≈ 5 % accuracy in EBSD grain size use ≥ 10 pixels per grain [HH eq.A2.1; §A2.3.2, §A2.5.1].
- **A single JMAK n or Q from Al data is not a material constant** (added): n varies with strain, grain size and inhomogeneity (often 1–2), and Q_RX doubles with 68 at. ppm Cu [HH pp.231, 235]. Calibrate per alloy and route.

**Relevance to the slug route.**
- Grain size is set mainly by the **nucleation density** (d ∝ (v/N)^¼ [HBAL03 eq.22]); v enters only weakly. So slug-grain control is about keeping nuclei alive: enough constituents above d_g (§3.2b), and no slow ramp through the precipitation window that would put precipitates on the substructure before RX (§5.2). *Corrected after full-text pass:* the slow ramp hurts through precipitation; the "recovery lowers the driving force" argument is weak in single-phase Al (§2.3, §4.4).
- **Anneal-temperature anchors for lean slugs:** 3105 O at 345 °C [HBAL03 p.299]; 3003 at 413 °C and 3004/3105 at 343 °C with time only to bring the load to temperature [HBAL03 p.888]; 380–420 °C for 0.5–1 h [W7]. Al–1Mn at 95 % CR is fully recrystallised in 1 s at 620 °C [HBAL03 p.251; HH Fig.12.21 p.412], which shows how fast RX can be once the driving force is high and precipitation is avoided. Cold-rolled supersaturated Al–1.3Mn needs 425 °C/1 h with fast heating [HH Tab.9.1].

### 4.6 Recrystallised grain size: what sets it and how to predict it (added after full-text pass)

- **Principle** [HH §7.5.2 p.248; §7.1.2 law (iv)]: anything that raises the number of nuclei (higher strain, finer initial grain size) gives a finer grain; the **annealing temperature has little effect** on the final RX grain size (α-brass data, Fig.7.23) **unless a change in temperature or heating rate shifts the nucleation/growth balance, which is "most likely in two-phase alloys"**. RX grain-size distributions are close to **log-normal** (Al–0.3Fe, Saetre et al. 1986) [Fig.7.24 p.249]; the largest grains are typically ≈ 2.5× the mean [HH §11.5.2.1 p.371].
- **Particle-controlled grain size: three regimes** [HH §9.6 pp.307–309, Fig.9.21] (Nes 1985; Wert & Austin 1985; Nes & Hutchinson 1989). The controlling parameter is the fine-particle level F_V/r, because it sets the Zener drag, the number of viable nuclei (eq.9.8–9.9) and the stagnation size D_lim (§6, §7):
  1. **F_V/r < A — grain-growth limited:** RX grain size D_N is set by the nuclei and may be small, but grains can then grow to D_lim at high temperature. The **smallest stable grain size is reached at F_V/r = A**;
  2. **A < F_V/r < B — nucleation limited:** D_N > D_lim, so normal growth is suppressed; an inhomogeneous structure is then **prone to abnormal grain growth** at high temperature (§7);
  3. **F_V/r > B — no discontinuous RX:** the deformed/recovered structure is stabilised (extended recovery).
  Higher strain shifts A and B to higher F_V/r (arrows in Fig.9.21).
- **Equations for prediction:** PSN with efficiency 1: D ≈ d·F_V^(−1/3) [HH eq.9.3]; general site-saturated case: D ≈ N^(−1/3) with N = number of viable nuclei per unit volume [HH eq.9.9]; JM form d ∝ (v/N)^¼ [HBAL03 eq.22]. Hot-working regressions D_R = c₂D₀^C′ε^(−n′)Z^(−K′) exist for steels (§9) [HH eq.13.22 p.447].
- **Anchors for Al:** Al–Si 50 % CR at 300 °C: 200 µm without particles, 145 µm with 1.5 µm particles, 45 µm with 4.6–4.9 µm particles (F_V = 0.01) [HH Fig.9.2b; Tab.11.3]; coarse-grained Al–0.05Mn: neighbouring deformed grains recrystallised to 15 µm and 30 µm while a Goss grain did not recrystallise at all [HH Fig.7.15 p.240]; AA3103, ε = 2, 400 °C/45 s salt bath: 6 µm [Ryen03, §4.3 table].

**Relevance to the slug route (grain size vs cold strain, added).**
- The **20–100 µm slug window corresponds to a nucleus density of only ≈ 10⁻⁶–1.25×10⁻⁴ µm⁻³** (N = D⁻³; derived), i.e. only ≈ 0.1–12 successful nuclei per 10⁵ µm³ (a cube of ≈ 46 µm edge). At ε_cold ≈ 0.36–0.92 the supply of such nuclei depends on the constituent tail above d_g (§3.2b), on prior grain boundaries (the cast grain structure is not reset if the hot band does not recrystallise, §9), and on transition bands/SIBM.
- **Annealing temperature is not a strong grain-size lever** for a stable particle population [HH §7.5.2]; the strong levers are ε_cold, the constituent size distribution and avoiding precipitation before RX (heating rate). Temperature matters through the precipitation C-curve (§5.2) and through post-RX growth at long holds (§7).
- **Expect a log-normal distribution with maxima ≈ 2.5× the mean**, plus orientation-dependent RX (Goss-type deformed grains are slow; Fig.7.15). Report the grain-size distribution, not only the mean, and compare surface and centre (surface shear and strain reversal give fewer effective nuclei, §4.4).

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
  - **High-purity Al–Fe:** above 0.01 wt % Fe, FeAl₃ forms on boundaries during annealing and RX becomes **continuous (in situ)** around 400 °C [HBAL03 p.229]. This is the extreme case of "precipitation before RX" (HH would call it extended recovery, i.e. Regime I below; §3.1).
  - **Texture:** impurity atoms generally weaken cube and strengthen R {124}<211>, "**especially when they precipitate during the recrystallization annealing**"; avoiding the precipitation temperature raises the cube fraction, so the annealing temperature is decisive (Ito et al. 1983) [HBAL03 p.235].
  - **Hot rolling:** Fe clearly inhibits static RX after hot rolling (super-purity Al with Fe, Si, Cu additions; 50 % pass, 500 → 390 °C, 30 s before quench; Blade 1979) [HBAL03 pp.243–244, Fig.28]. Only the figure carries the numbers.
- **The T–t–T framework (sourced after full-text pass; previously general knowledge)** [HH §9.8 pp.310–316] (Humphreys et al. 2003; Somerday & Humphreys 2003; Engler & Yang 1995):
  - **Schematic TTT diagram** for cold-rolled supersaturated Al alloys **rapidly heated** to temperature [HH Fig.9.23 p.311]: RX-start and RX-finish lines (as for dilute alloys without precipitation) and a C-shaped precipitation line (enough precipitation to affect RX). The precipitation curve has a different temperature dependence because its driving force falls at high T. It crosses RX-finish at **A (T_A)** and RX-start at **B (T_B)**.
  - **Al–1.3 Mn and Al–0.25 Zr (cold rolled; the Al–1.3Mn micrographs are for 80 %): T_A ≈ 400 °C, T_B ≈ 350 °C; Al–0.25 Sc: both above 500 °C** [HH p.311; Fig.9.24].
  - **Regime I, T < T_B — precipitation before RX.** RX is prevented; in principle coarsening would eventually allow it, but for T_A, T_B ≈ 400 °C "extremely slow". Microstructure in three stages: (1) precipitates pin HAGBs and LAGBs (Al–1.3Mn heated at 10 °C h⁻¹: **incoherent MnAl₆ plates on the subgrain boundaries at 400 °C**); (2) particle coarsening or transformation with subgrain growth (this is recovery, *not* continuous RX); (3) RX once enough coarsening has occurred, by **broad-front SIBM** from a few long boundary segments: L_C ≥ 4γ/(P_D − P_Z) [HH eq.9.10–9.11 p.314]. Result: **very large grains, elongated in RD** (Al–1.3Mn fully recrystallised at 550 °C after slow heating) [Fig.9.24 p.313]. The RX front advances at the rate of particle coarsening or spheroidisation on the boundary (MnAl₆ plates spheroidise at the migrating HAGB at 500 °C), **not** at the boundary-mobility rate, so RX stays slow even at 500–600 °C [pp.313–314].
  - **Regime II, T_B < T < T_A — concurrent.** RX starts but precipitation stops it before completion. The RX fraction depends mainly on temperature and is **almost independent of time**; RX is very inhomogeneous, with broad-front SIBM along ~40°<111> boundaries and elongated "tombstone" grains [HH §9.8.3 pp.314–315].
  - **Regime III, T > T_A — RX before precipitation.** Behaves like a single-phase alloy: **equiaxed grains, smaller than in Regime I**, but they may grow rapidly afterwards at the high temperature [HH §9.8.4 p.316].
  - **Heating rate** [HH §9.8.2.1 p.312, Tab.9.1]: with slow heating (dotted path in Fig.9.23) precipitation can occur during the ramp and inhibit RX even at high T. **RX complete in 1 h: Al–1.3Mn 425 ± 5 °C (500 °C s⁻¹) vs 500 ± 20 °C (10 °C h⁻¹); Al–0.25Zr 380 ± 10 vs 480 ± 20 °C; Al–0.25Sc 575 ± 5 vs 550 ± 20 °C** (Sc precipitates before RX even with fast heating). HH: this "is in agreement with the known effects of heating rate" in industrial Al alloys (Bampton et al. 1982; Bowen 1990).
  - **Fe at trace levels shows the same intermediate-temperature trap.** 95 % cold-rolled Al–0.007 % Fe annealed at 280, 360 and 520 °C: at **360 °C the rolling texture was retained** (precipitation of an Fe-rich phase during RX hindered boundary migration), whereas at 280 and 520 °C (precipitation after or before RX) cube dominated (Hirsch & Lücke 1985) [HH §15.2.1.1 p.470, Fig.15.1].
  - This confirms, with numbers, the user's rule "precipitation before RX → coarse, elongated grains", consistent with [Røy05 p.34–35; AMAG14 p.14; HBAL03 PDF p.152; HBAL03 pp.229, 235, 356]. HBAL03 adds only the precipitation onset (Mn above ~325 °C [p.299]; Al₆Mn 300–350 °C [p.295]).

**Relevance to the slug route.**
- The quenched strip carries Mn, Fe, Si (and Mg) in solution into cold rolling and the slug anneal. Mn and Fe start to precipitate in the same 300–400 °C range in which a batch slug anneal ramps and holds [HBAL03 pp.229, 295, 299]. For Al–1.3Mn this is exactly the band between T_B ≈ 350 °C and T_A ≈ 400 °C [HH p.311].
- **A slow ramp or a low hold therefore invites precipitation on the recovered substructure before RX.** The expected result is fewer nuclei, coarse or elongated grains (Regime I, broad-front SIBM) or a partly recrystallised, inhomogeneous slug whose RX fraction does not rise with hold time (Regime II) [HH §9.8.2–9.8.3]. The HBAL03 term "continuous RX" for this case is better read as extended recovery (§3.1).
- **Fast heating to above T_A** lets RX run first (Regime III). Precipitates then form inside the new grains and can cap later grain growth (§6) [HH §9.8.4; HBAL03 p.887; Ryen03 §3.4]. For cold-rolled Al–1.3Mn the price of a 10 °C h⁻¹ ramp was +75 °C on the 1 h RX temperature [HH Tab.9.1]. A batch load brought to ≈ 400 °C in 2–4 h (assumed; measure the load-centre thermocouple) heats at ≈ 100–200 °C h⁻¹ (derived): 10–20× faster than HH's slow case but some 10⁴× slower than the fast one, so whether a batch slug anneal behaves as "fast" or "slow" can only be settled against the measured C-curve.
- **Where T_A and T_B lie for T11 (inference, to be measured).** T11 has far less supersaturation than Al–1.3Mn: Mn 0.14 wt %, Fe in solution limited by its tiny solubility, and Mg + Si (0.26/0.38) that can form Mg₂Si-type precipitates. A smaller supersaturation lowers the precipitation driving force, which moves the precipitation C-curve to longer times and its upper limb to lower temperatures; T_A and T_B should therefore lie **below** the Al–1.3Mn values, widening Regime III. Two caveats: (i) Fe at only tens of ppm in solution already raised T_RX by ~50–100 °C in 80 % cold-rolled Al [HH Fig.7.10] and produced the 360 °C texture trap above; (ii) fine Mg–Si precipitation before RX inhibits PSN more than cube nucleation and gives a strong cube texture in AA6xxx [HH §15.2.3.3 p.477] (§8). The HH framework is therefore expected to apply to T11 with Fe and Mg–Si, not Mn, as the main precipitating species (inference).
- **Measurement plan that maps T_A/T_B for the strip (proposal):** isochronal (e.g. 1 h) and isothermal anneals of cold-rolled strip at 300–450 °C at two heating rates (salt bath or induction vs furnace ramp), with conductivity (precipitation), EBSD HAGB fraction (RX, §4.5) and grain size/aspect ratio. Regime II shows up as an RX fraction that plateaus with time.
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
| **Fine, equiaxed, weak texture** (formability, deep drawing, fin/tube with low critical-strain risk) | **High-T homogenisation with slow cool / stepped holds** (AA3103 C-type → Mn_ss 0.15 at %) to precipitate and **coarsen** Mn dispersoids: lower F_V/r, low Mn_ss; Si present for α-phase (denser early, coarser after soak) [Ryen03 Tab.3.2; HBAL03 PDF p.172] | High reduction (ε ≥ 2); **fast heating, high T** (continuous line, salt bath, induction) so RX precedes any residual precipitation [Ryen03 §3.4: 400 °C/45 s → 6 µm] | many PSN sites (constituents > d_g, ≈ 2 µm at ε ≥ 1.6 [HH Fig.9.13]) and low Zener; no precipitation in deformation zones; Regime III anneal (T > T_A) [Pol06 p.42; HBAL03 PDF p.152; HH §9.8.4] |
| **Coarse, elongated ("long-life"/sag-resistant fin) grains** | **Low-T or short homogenisation** (retain Mn_ss, i.e. supersaturation from casting; TRC strip retains more) [Pol06 p.102; Bel05 §1.6] | Moderate reduction; **slow heating or a low-T pre-anneal** in the precipitation window (300–400 °C class, cf. AMAG14) so dense fine dispersoids precipitate on sub-boundaries **before** RX; then RX at higher T with few nuclei | Zener on subgrains is near its maximum when D ≈ D_c (§6); RX starts only at sparse sites → few, large, RD-elongated grains [HH eq.4.27–4.29, 4.35–4.36; Røy05 p.35; AMAG14 p.14]. **(general knowledge)** Coarse, elongated, braze-surviving grains reduce Si/liquid-filler penetration along boundaries and improve sag resistance. |
| **Unrecrystallised / recovered (H2x/H24-like) fin** | Retain or precipitate a high number density of small dispersoids (≤0.4 µm effective [HBAL03 PDF p.137]) | Final anneal below the RX start; rely on recovery | Dispersoids retard recovery and RX [Pol06 p.43; Dav01 p.382] |
| **Avoid** | — | **Small, non-uniform strains (3–7 %, e.g. tube sizing) followed by a high-T cycle (braze ~600 °C)** | Critical-strain abnormal coarse grains: AA3102 MPE tube, about −22 % burst strength at ~3 % sizing [Wil12 pp.11–13]; §7 |

### 5.5 Pitfalls
- Over-coarsened dispersoids (homogenisation too hot or too long) lose pinning, because P_Z ∝ f/r falls rapidly with coarsening [Røy05 p.34].
- Dispersoid-free zones (segregation) seed coarse RX grains [Rob04].
- Mn dispersoids increase quench sensitivity (intermediate between Cr- and Zr-dispersoids) [Pol06 p.112; HBAL03 PDF p.137]. This matters for 6xxx/7xxx, and for 3xxx only if a later precipitation step exists.
- Long annealing produces coarse grain [W7 p.5].
- **Regime II looks like "incomplete RX that needs a longer hold" but is not** (added after full-text pass): the RX fraction is almost time-independent, so raising the hold time does not help; only a higher temperature (or faster heating) does [HH §9.8.3 p.314].
- Regime-I RX is controlled by particle coarsening on the moving boundary, so a boundary-mobility (v = MP) model will badly over-predict its rate [HH p.314].

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
| Limiting grain size, superseded estimate | 3γ/D = 3F_Vγ/(2r) gives D_lim ≈ 2r/F_V | *superseded after full-text pass* by the HH treatment below (it corresponds to α = 1.5 in eq.11.30) | derived (earlier pass) |
| Limiting grain size, Mao | R_c = 2γ/P_Z = 4r/(3f) with ΔP = 2γ/R; as a radius the diameter is 8r/(3F_V) | Mao's R is a radius. *Resolved after full-text pass:* this is **Hillert's (1965) result** (limiting **radius** 4r/3F_V, i.e. a diameter twice Zener's) [HH p.358] | [HBAL03 eq.37–38 p.250] |
| **Zener limiting grain size (HH; corrected after full-text pass)** | ΔP: αγ_b/R = 3F_Vγ_b/(2r) → **D_Z = 4αr/(3F_V)** (diameter); α = 1 gives the classical **Zener D = 4r/(3F_V)** | α is a geometric constant: Hillert 1965 corresponds to a diameter of 8r/3F_V; Gladman (tetrakaidecahedra, Z = 2) α ≈ 0.375 [eq.11.32]; refined theories 0.25 < α < 0.5; **experiments (Fe and Al alloys, F_V < 0.05; Manohar et al. 1998) α ≈ 0.26; HH use α = 0.35** → **D_Z ≈ 0.35–0.47 r/F_V**, i.e. 3–8× below the 1.3–2.7 r/F_V range previously used here. *Text flag:* HH write "α = 0.5" for Hillert's doubled diameter, which with eq.11.30 would need α = 2; the eq.11.30 form was checked on the page image | [HH eq.11.29–11.32 pp.358–359; Fig.11.12 p.361] |
| Cellular-stability limit (HH) | R̄_LIM = d/(12F_V) (d particle diameter) | identical to eq.11.30 with α = 0.25 | [HH eq.11.42 p.370] |
| Correlated limit, large F_V | **D_ZC = βr/F_V^(1/3)**, β ≈ 3 (Hillert 3.6; steels 3.3; Al–Ni 3.4; Anand & Gurland subgrains 2.7) | applies above **F_V ≈ 0.05** (transition between 0.01 and 0.1); use the larger of D_Z and D_ZC | [HH eq.11.34 pp.360–362, Fig.11.11–11.12] |
| Lower bound, all particles at corners | D_Z1 = r(8/3F_V)^½ ≈ 1.6r/F_V^½ | lower bound; growth continues until all corners are pinned (D_ZC) | [HH eq.11.33 p.360] |
| Precipitation after grain/subgrain formation | **D_ZP = r(8/F_V)^½** (all particles on boundaries) | expected mainly for subgrains (Al–Mn precipitation on substructure, §2.1); not yet tested quantitatively | [HH eq.11.35 p.363] |
| Particle-limited growth kinetics | dR/dt = M(αγ_b/R − 3F_Vγ_b/2r) [eq.11.26]; Hillert: dR/dt = cMγ_b(1/R_crit − 1/R ± z/c), z = 3F_V/4r [eq.11.27] | parabolic at first, stagnates when P = P_Z | [HH eq.11.26–11.28 p.357] |
| Growth controlled by particle coarsening | dR/dt = c·dr/dt, c = 2/3F_V (low F_V) or β/2F_V^(1/3) (high F_V); r³ − r₀³ = c₁D_s t (volume diffusion) or r⁴ − r₀⁴ = c₂D_b t (boundary diffusion) | Al–6Ni (F_V = 0.1 NiAl₃, 0.3 µm): grain size ∝ particle size, constant 3.4 | [HH eq.11.36–11.38 pp.363–364] |
| **RX retardation criterion (empirical)** | **retarded if F_V/r > ≈ 0.2 µm⁻¹**; below this RX is often accelerated, even without PSN (Humphreys 1979b); alternatively a critical spacing ∝ F_V^½/r (Ito 1988) | Al shows acceleration by small particles less often than Cu (dynamic recovery removes particle GNDs). MMCs: discontinuous RX suppressed above F_V/r ≈ 0.2 µm⁻¹ | [HH §9.2.1 p.289; §9.7 p.310] |
| **Nucleation-suppression criterion** | nucleation fails if D_lim < θ_m/Ω [eq.9.4] → **F_V/r > 4αΩ/(3θ_m)** (F_V < 0.05) [eq.9.5]; F_V^(1/3)/r > βΩ/θ_m (F_V > 0.05) [eq.9.6] | α = 0.35, θ_m = 15°, Ω = 5° µm⁻¹ (Ørsund et al. 1989) → **F_V/r > 0.15 µm⁻¹**; the critical value rises with strain (Ω grows) | [HH §9.4.1.1 p.305] |
| Net RX pressure with particles | P = P_D − P_Z − P_C = ρGb²/2 − 3F_Vγ_b/d − 2γ_b/R (d = particle diameter) | Zener alone is often too small to stop an RX front; the retardation is mainly via nucleation. The controlling parameter is F_V^n/r with 1/3 < n < 1 | [HH eq.9.7 p.306] |
| Zener pressure (second source) | P_z = 3fγ/(2r) | same as HH eq.4.24 | [HBAL03 eq.37 p.250; Ridley eq.8 HBAL03 p.1114] |
| Empirical pinning criterion | Zener pinning "will occur when F_V/r ≥ 2" (for groups of fine particles) | **units not printed** (presumably µm⁻¹; then P_Z ≈ 1 MPa with γ = 0.324 J m⁻², derived). Treat as uncertain | [HBAL03 p.1114] |

**Worked example (derived; inputs assumed: r = 50 nm, F_V = 0.01, γ = 0.324 J m⁻²):**
- P_Z = 0.097 MPa.
- D_c = 0.37 µm and P′_Z,max ≈ 0.36 MPa.
- D_lim (corrected after full-text pass): **≈ 1.7–2.3 µm with the experimentally calibrated α = 0.26–0.35** [HH pp.359–361]; 6.7 µm for classical Zener (α = 1); 13 µm for Hillert's 8r/3F_V. (The earlier 10 µm from 2r/F_V is superseded.)
- F_V/r = 0.2 µm⁻¹, i.e. right at HH's empirical boundary between accelerated and retarded RX [HH §9.2.1], and above the 0.15 µm⁻¹ nucleation-suppression level of eq.9.5.
- Compare:
  - RX driving pressure: ≈ 1 MPa as HH's working value [HH eq.7.2]; ≈ 0.2–0.6 MPa implied for 30–80 % cold rolling (§1.2); ≈ 7 MPa only for extreme strains (derived);
  - subgrain-growth pressure for 1 µm subgrains: ≈0.6 MPa [HH §1.3.2];
  - growth pressure for 100 µm grains: ≈0.01 MPa [HH §1.3.2].
- **Conclusion:** a typical 3xxx dispersoid population cannot stop growth of an established RX front driven by stored energy. It *can* (a) arrest subgrain coarsening and therefore *nucleation* (pinning is near its maximum because D_subgrain ≈ D_c; HH reach the same conclusion: Zener pressure is "too small" to explain retarded growth, but F_V/r of 0.2–0.6 µm⁻¹ suppresses nucleation [HH §9.4.2 p.306]), and (b) cap post-RX grain growth at a few µm (corrected after full-text pass; previously "about 10 µm"). This is why the **timing** of precipitation relative to nucleation (§5) is decisive.
- HBAL03 states the same mechanism: aluminide dispersoids (fine, "not necessarily coherent") hinder RX by **pinning small-angle boundaries and dislocations** [HBAL03 p.296]. Mn dispersoids in 3xxx "efficiently hinder grain growth upon recrystallization" [HBAL03 p.299]. Size anchors: after 350–450 °C for up to 200 h, Al₃Zr is 5–11 nm and Al₃Sc 25–35 nm [HBAL03 p.298].

**Relevance to the slug route (corrected after full-text pass).** With 0.14 Mn (T11) the Mn dispersoid fraction is small. If, say, F_V ≈ 0.2 % and r ≈ 50 nm (assumed, not measured), F_V/r = 0.04 µm⁻¹, well below the 0.15–0.2 µm⁻¹ levels that suppress nucleation or retard RX [HH eq.9.5; §9.2.1]: such a dispersion would **not** stop RX. Its growth cap, however, is D_Z ≈ 9–12 µm with the calibrated α = 0.26–0.35 (33 µm for classical Zener, 67 µm for Hillert; derived), and the no-growth limit is D_M = 2d/(3F_V) = 33 µm (§7.1). The previous conclusion ("D_lim ≈ 33–67 µm, a lean alloy is barely dispersoid-capped") used α = 1–2 and is withdrawn. Consequences:
- If such dispersoids exist **before or during RX**, a slug that recrystallises to > 33 µm cannot coarsen further, and one between ≈ 10 and 33 µm cannot grow normally but **can grow abnormally** (Ψ between 0.25 and 1; §7.1) during a long hold — a duplex-grain risk.
- If they form **after** RX (Regime III), they mainly freeze the RX grain size.
- Which case applies depends on F_V and r of the Fe/Mn/Mg–Si precipitates that actually form in the anneal. **Measure F_V and r (TEM/SEM) in annealed slugs** before relying on, or excluding, a Zener cap. Hold time and heat-up rate then decide the final size [HBAL03 p.887].

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
  - *Added after full-text pass:* **AGG cannot occur in an "ideal" grain assembly** (equal boundary energies and mobilities): a large grain always grows more slowly, relative to the assembly, than the mean and rejoins the distribution [HH §11.5.1 pp.369–370, eq.11.40]. AGG therefore needs inhibited normal growth (particles, texture, surface) or a growth advantage other than size. Example shown: Al–1Mg–1Mn annealed at 600 °C [HH Fig.11.19 p.369].
  - **Particles: five regimes** of Ψ = 3F_V R̄/d (R̄ mean grain radius, d particle diameter) [HH §11.5.2.1 pp.370–372]: Ψ = 0 normal growth; **0 < Ψ < 0.1 only a broadening of the size distribution**; **0.1 < Ψ < 0.25 abnormal and normal growth**; **0.25 < Ψ < 1 abnormal growth but no normal growth**; **Ψ > 1 no growth of any kind**, i.e. above the mean grain size **D_M = 2d/(3F_V)** [eq.11.44], four times the normal-growth limit R̄_LIM = d/(12F_V). With a log-normal distribution (largest grain ≈ 2.5× mean) the practical upper limit for AGG is Ψ ≈ 0.6 [p.371].
  - **AGG is usually triggered when the dispersion becomes unstable** (coarsening or dissolution at higher T, classic MnS/AlN cases in steels), and is suppressed if the primary RX grain size already exceeds D_M (Hillert 1965) [HH §11.5.2.2 pp.372–374]. *Data flag:* the D_M and D_Z columns of HH Tab.11.3 do not reproduce from eq.11.42/11.44 with the tabulated F_V and d (derived check); use only its measured columns.
  - **Texture:** a single strong component (e.g. **cube in Al**, Beck & Hu 1952) gives low-angle, low-mobility boundaries inside the component, so grains of other orientations grow abnormally. With a diffuse texture (mean misorientation ≈ 10°) the abnormal grains reach only ≈ 5× the mean (size broadening rather than true AGG); grain growth in Al–Mn showed larger grains in the main texture components (Distl et al. 1982; Weiland et al. 1988) [HH §11.5.3 pp.374–375].
  - **Prior deformation:** AGG after a small prior strain is best interpreted as **primary RX by SIBM**, not as grain growth [HH §11.5.5 p.378] — the mechanism behind critical-strain coarsening below.
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
       - *Conflict flagged (full-text pass):* HH describe the same Al–1Mn/620 °C experiment (Abbruzzese et al. 1988) with cube lost after 120 s and replaced first by **{011}<122> (P)** and later by **{013}<231> (Q)** (7700 s); the model fitted until the grain size approached the sheet thickness [HH §12.4.4 pp.412–413, Figs.12.21–12.22]. The Miller indices differ between the two books; the sequence (cube → a {011} component → a third component) agrees.
     - **Al–3 wt % Mg**, 95 % CR: RX complete after 300 °C/200 s with strong cube. After 300 °C/600 s plus 400 °C/20 s the cube maximum reached 119.9× random. At 400 °C the cube grains were then consumed by {112}<312> and {001}<490> grains after ≈ 3000 s (Zhao 1990) [pp.252–253, Figs.36–37].
  3. **Free surface** in thin foil (< 0.1 mm, > 99.99 % Al): grains through the thickness and a very sharp cube, because the {001} surface energy is lowest [p.254].

### 7.2 Quantitative
- **Growth law (now sourced; corrected after full-text pass, previously general knowledge)** [HBAL03 eq.31–35 pp.245–248]:
  - boundary energy per unit volume F_b = 4πR²γ/(2·(4/3)πR³) = **3γ/(2R)** (R = mean grain radius);
  - curvature pressure **ΔP = 2γ/R**; v = −dR_s/dt ∝ ΔP, which gives R_s² = R_s0² − Cγt for a shrinking grain and **R² = R₀² + Cγt** for the mean grain, i.e. **R ∝ √t (n = 2)**, C depending on T;
  - example: with γ ≈ 1.0 J m⁻² (Mao's value, §1.4), coarsening from R = 50 to 100 µm releases 1.5×10⁴ J m⁻³ [p.245]; with γ = 0.324 J m⁻² it is 4.9×10³ J m⁻³ (derived). Both are ~100–1000× below the RX driving force (§1.2), which is why grain growth is slow and easily pinned.
- **Measured exponents (sourced after full-text pass; previously general knowledge)** [HH §11.1.3–11.1.4 pp.335–338]: the Burke–Turnbull analysis gives R̄² − R̄₀² = c₂t (n = 2) [HH eq.11.5], generalised to R̄ⁿ − R̄₀ⁿ = c₂t [eq.11.7]. Measured n is "generally well above 2"; zone-refined metals give n = 2–4, mean 2.4 ± 0.4, and **n = 4 for high-purity Al** (Gordon & El Bassyoumi 1965) [HH Tab.11.1 p.338]. n tends to fall as the homologous temperature rises [Fig.11.2]. The grain-growth driving pressure is typically ≈ 10⁻² MPa, about 100× below that of primary RX [HH §11.1.1 p.334]. After hot working: Dⁿ = D_Rⁿ + ct·exp(−Q_g/kT) [HH eq.13.28 p.450]. k₀ and Q_gg for lean 3xxx are not given; Q ≈ Q_self (below).
- **Specimen thickness:** growth slows once the grain size exceeds the sheet thickness (curvature in one direction only, thermal grooving) [HH §11.1.2 p.335].
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
- Slugs need 20–100 µm grains. Grain growth after RX follows R² − R₀² ∝ t [HBAL03 eq.35], so **soak time matters less than nucleation density** once RX is complete. Doubling the soak enlarges a growing grain by at most √2× (derived, ideal n = 2); with the measured n = 4 for high-purity Al [HH Tab.11.1] only by 2^¼ ≈ 1.19× (derived).
- Lean alloys have few dispersoids to cap growth (§6), so the "heat fast, hold only to temperature" rule [HBAL03 p.888] is the main guard against coarse or duplex grains in the slug centre of a large batch load.
- A mixed PSN texture is unlikely to trigger texture-induced AGG. A strongly cube-textured slug (low PSN) held long at high T could (inference from [HBAL03 pp.251–253]; HH confirm cube-texture AGG in Al [HH §11.5.3]).
- **Particle-induced duplex grains (added after full-text pass):** if fine precipitates (Fe-, Mn- or Mg–Si-bearing) form during the anneal and the RX grain size lies between ≈ D_M/4 and D_M (Ψ = 0.25–1), normal growth stops but abnormal growth stays possible; a subsequent rise in temperature that coarsens or dissolves the precipitates is the classic trigger [HH §11.5.2]. A slow batch ramp followed by a hotter hold fits that pattern (inference). Check slugs for a bimodal grain-size distribution.

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
| **P (RX component)** | **{011}<122>** | **70, 45, 0** |
| **Q (RX component)** | **{013}<231>** | **58, 18, 0** |

The rows "Rotated cube", "R" and "{111}<112>" are from [HBAL03 Tab.1 p.234]; P and Q are from [HH Tab.12.1 p.381] (added after full-text pass; HH list R with the same angles, 57, 29, 63). *Flags:* that table prints copper as {112}<**112**>, a misprint for {112}<111> (as above and in [HBAL03 PDF p.143]); it gives Brass and Goss with φ₂ = 0° instead of 90°, which is a symmetry-equivalent setting (general knowledge).

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
- **HH full-text additions (2026-10-12)** [HH ch.12, §13.2.4, §15.2]:
  - **Purity, strain and temperature.** Very-high-purity Al (< 10 ppm Fe) recrystallises to almost 100 % cube [HH §15.2 p.469]. In high-purity Al the cube is **strengthened by high rolling reductions and high annealing temperatures** [HH §12.2.1.2 p.386]; for fcc metals generally, cube is weakened by small reductions with intermediate anneals, a large grain size before the penultimate rolling stage and a low final annealing temperature [p.383]. Increasing Fe raises T_RX and weakens cube in AA1xxx [HH §15.2.1 p.470].
  - **Mg in solution** (Al–Mg) suppresses recovery and forms shear bands that cut the cube bands and nucleate Goss, P and Q; Al–3Mg keeps a dominant cube after 90 % reduction but forms strong Q + Goss after 97.5 % (Engler 2001) [HH pp.386–387].
  - **Cube after hot rolling: the cube-band model.** In commercial Al alloys the RX cube is stronger after hot rolling than after cold rolling. Cube is more stable at high temperature (low Z), survives as long ribbon-like bands, and these recrystallise by **SIBM** into neighbouring (often S-oriented) material; the RX cube strength scales with the hot-deformation cube strength (Vatne & Nes 1994; Samajdar & Doherty 1995; Vatne et al. 1996). No Dillamore–Katoh transition-band mechanism is needed after hot deformation [HH §12.4.1.2 p.404].
  - **Why cube subgrains win:** in Al–1Mg deformed at 400 °C to ε = 1 the cube subgrains have the lowest stored energy (7.6 vs 12.2–13.3 mJ cm⁻³ for Brass, Copper, S) and are larger, with some exceptionally large ones; the adjacent S material supplies the driving pressure; 40°<111> cube/S boundaries may be mobile and of low energy [HH Tab.13.1 p.427; §12.4.1.4 pp.405–406]. The cube fraction after hot plane-strain compression falls with increasing Z and strain [HH Fig.13.11 p.426].
  - **Compromise-texture (40°<111> growth selection) model:** the transformed AA3004 rolling texture does produce cube, Goss and P peaks, but about 4× too weak (14R → 3.5R maximum), so it cannot be the dominant cause of strong cube [HH §12.4.1.5 p.406, Fig.12.16]. HH conclude that prolific early formation of cube nuclei, not a later growth advantage, gives the cube texture.
  - **Particles** [HH §12.2.4, §12.4.3 pp.390–392, 408–411; Tab.12.3]: PSN in heavily deformed polycrystals gives near-random nuclei, but even random PSN nuclei produce a *weakened rolling texture*, not a random one (simulation: peak 5.5 → 3.1× random) [p.392]. Only MMCs with F_V > 0.1 become random. Tabulated Al alloys: 99.9965 % Al 90 % → cube; Al–FeSi (F_V 0.005, 0.2–7 µm) and Al–Si (0.008, 2 µm) 90 % → cube + rolling + random; Al–Al₂O₃ (0.004, 0.1 µm) → deformation texture; Al–Ni (0.10, 1 µm) → rolling + random [Tab.12.3 p.391].
  - **AA3004 hot-rolled:** cube falls from ≈ 19 % to ≈ 12 % and random rises from ≈ 51 % to ≈ 59 % as the number of PSN-capable ("supercritical") constituents rises from ≈ 500 to ≈ 1400 per mm (unit as printed, probably per mm²) (Bolingbroke et al. 1993) [HH Fig.12.18 p.409] (read from figure).
  - **Zener drag strengthens cube** in Al alloys in all three cases: small particles present during deformation, bimodal particles, and **precipitation during the RX anneal** (Daaland & Nes 1996; Engler 1997; Vatne et al. 1997). Reasons: pinning raises the critical nucleus size, which favours broad-front SIBM from cube bands; precipitation may occur preferentially on the "random" boundaries of PSN nuclei rather than on special cube/S boundaries [HH §12.4.3.3 pp.410–411].
  - **AA1050, heavily rolled, 0.5 % of 1–7 µm particles:** PSN grains nucleated first with random orientations, cube grains later but grew rapidly; final structure small (< 10 µm) PSN grains plus large (> 100 µm) cube grains (Juul Jensen et al. 1985) [HH p.409].
  - **AA6xxx sheet (Mg–Si):** fine Mg₂Si precipitated in the hot band before cold rolling inhibits PSN more than cube nucleation and gives a **strong cube** after solution treatment (20–30 µm grains); an intermediate anneal that coarsens Mg₂Si lets PSN contribute and gives the desired **weak cube** (less roping) [HH §15.2.3.3 pp.477–478, Tab.15.3].
  - **Grain growth after RX usually sharpens the existing texture** (cube in fcc metals, Hutchinson & Nes 1992) rather than changing it; large changes need AGG [HH §12.4.4 pp.411–413, Fig.12.19].
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
- **Can-body practice (added after full-text pass)** [HH §15.2.2 pp.472–476]:
  - can makers specify ears of **0.5–3 % of the can height**; a minimum of ≈ 0.5 % is kept on purpose, because eliminating the 45° ears exposes **two-fold 0/180° Goss ears**, which pinch under the blank holder and jam the body maker (Malin 1993);
  - earing per component (Tab.15.2): cube {100}<001> 4-fold 0/90°; Goss {110}<001> 2-fold 0/180°; Brass, Copper and S 4-fold 45°;
  - the strong RX cube of the hot band is "relatively stable" in cold rolling but weakens as Brass, Copper and S grow; 45° earing is minimised by maximising hot-band cube;
  - AA3104 route: DC ingot, homogenisation > 550 °C, breakdown 500 → 300 °C to 25 mm (constituents broken up, partly recrystallised), hot finishing without inter-pass RX, RX on coiling or at 350 °C, then **87 % cold rolling to H19** (UTS 295, YS 285 MPa, 2 % elongation; 0.3 mm). Homogenisation transforms β-(FeMn)Al₆ to the harder α-Al₁₅(FeMn)₃Si₂ (die cleaning, anti-galling) and precipitates α-Al₁₅Mn₃Si₂ dispersoids that control RX after hot rolling;
  - high hot-rolling temperature (low Z) promotes cube retention and restricts PSN [HH Fig.13.31].
- Texture strengthening: ideal fibre texture gives about +20 % strength [Pol06 p.39]. Extrusion dual fibre gives about +70 MPa longitudinal, lost on RX [HBAL03 PDF p.143].

### 8.4 Pitfalls
- Taylor-type models predict textures that are too sharp and form too fast; heterogeneity (deformation bands) is the cause [HH §3.7.1.5 p.86].
- Surface ≠ mid-plane texture under high friction or light passes [HH §3.6.1 p.80].
- A strong initial (hot-band) cube delays β-fibre development: AA5005 shows no β-fibre up to ε = 1 [Ryen03 §4.2.2 p.70].
- Mechanical fibring (grain shape, particle stringers) can dominate anisotropy over crystallographic texture [Pol06 p.40].

### 8.5 Gaps
- *Partly resolved after full-text pass:* HH define **P = {011}<122>** (70°, 45°, 0°) and **Q = {013}<231>** [HH Tab.12.1 p.381]; P appears in AA3004 recrystallisation and in the 40°<111>-transformed rolling texture, and P/Q replace cube during grain growth of Al–1Mn (§8.1–8.2, §7.1). The often-quoted P = {011}<566> is not used by HH; the two are close but not identical, so state the indices used when comparing ODFs. The **ND-rotated cube** is described by HH only for 70:30 brass annealed at 900 °C [HH Tab.12.2 p.386], not for Al; its role in particle-containing 3xxx remains a gap.

**Relevance to the slug route.** Impact extrusion is not limited by earing the way deep-drawn cans are. The texture questions for slugs are: (i) uniform wall flow and a uniform surface after forming (general knowledge), and (ii) the AGG risk of a single strong cube component (§7). A PSN-dominated, near-random slug texture is the safer target. That is also what a high constituent count and an anneal without precipitation give [HBAL03 PDF p.143; HBAL03 p.235].
- *Added after full-text pass:* even with PSN the RX texture of a rolled Al alloy is a **weakened rolling texture plus cube**, not random, unless F_V of PSN particles exceeds ≈ 0.1 [HH p.392; Tab.12.3]. Three features of the slug route push toward **more cube**: an unrecrystallised, quenched hot band that may carry cube bands from hot deformation (SIBM sources, [HH §12.4.1.2]); low cold reduction (fewer PSN-capable particles, §3.2b); and any Fe or Mg–Si precipitation during a slow ramp (Zener drag favours cube [HH §12.4.3.3; §15.2.3.3]). Fast heating and a higher ε_cold push toward PSN and a weaker texture (inference). Check by EBSD/XRD on annealed slugs (cube volume fraction, random fraction).

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
- **Hot-rolling model status** [HBAL03 pp.359–360]: steel-type Avrami/t₀.₅/d_rex regressions (§4.2) are of limited use for Al. Physically based models with nucleation-site efficiency and precipitation are under development. HH give the same reasons: strain accumulates over several passes before RX, the history matters more than in steels (no phase transformation to wipe it out), and particles change during processing [HH §16.3.3.3 p.526].
- **HH ch.13 additions (full-text pass, 2026-10-12)** [HH §13.2–13.3 pp.415–437]:
  - in Al and its alloys **dynamic recovery is rapid and usually the only form of dynamic restoration**; the flow curve rises to a steady-state plateau; above ε̇ ≈ 1 s⁻¹ deformation heating can lower the flow stress [pp.416–417];
  - DRX in Al is confined to very high purity (review by Kassner & Evangelista 1995), where the boundary mobility is very high [p.431]. **Particle-stimulated DRX is not observed in Al alloys**: small misoriented grains form at large particles, but the matrix stored energy is too low for them to grow; DRX reported in Al–Mg is more likely progressive lattice rotation (continuous DRX) [pp.436–437]. This supports the KB's industrial view above (*conflict with Mao resolved in favour of DRV*);
  - the **subgrain size becomes independent of strain above ε ≈ 0.5**, while the **subgrain misorientation keeps rising with strain** (Al–0.1Mg, 350 °C) [HH §13.2.3.1 pp.419–420, Fig.13.4];
  - at low Z the HAGBs become serrated with a wavelength ≈ subgrain size; small particles keep them planar [pp.420–421];
  - **deformation is more homogeneous at higher temperature**: fewer large-scale deformation bands in Al–0.3Mn as T rises (Ball & Humphreys 1996), smaller long-range misorientation gradients at lower Z, fewer shear bands [HH §13.2.3.3 pp.420–422, Fig.13.6]. Fewer such heterogeneities means fewer RX nucleation sites on later annealing (inference from §7.6.4);
  - **cube and Brass are more stable at low Z**; the cube fraction after hot plane-strain compression falls as Z and strain rise [HH §13.2.4 pp.424–427, Fig.13.11];
  - commercially hot-rolled Al–1Mg–1Mn shows a strong Brass plus a significant cube component in addition to the normal rolling texture [Fig.13.10]. Partial RX before quenching can contaminate "hot-deformation" textures, especially in Al–Mg [p.425].

### 9.2 Quantitative (method from Bom08, not Al data)
- Activation energy from the **Zener–Hollomon hyperbolic-sine law**, with peak stress fitted over T and ε̇. Nimonic 80A: Q = 379 kJ mol⁻¹ [Bom08 p.323].
- Form: Z = ε̇ exp(Q/RT) [HBAL03 eq.3 p.359, there written with Q_def, the apparent activation energy for deformation; no Al value given; HH eq.13.1 p.417] = c₁[sinh(c₂σ)]ⁿ [HH eq.13.2] (*sourced after full-text pass*; previously general knowledge). At low stress this reduces to a power law ε̇ = c₃σᵐexp(−Q₁/RT), at high stress to Z = c₄exp(c₅σ) [HH eq.13.3–13.5 pp.417].
- **Flow stress and substructure (added; replaces the general-knowledge δ⁻¹ = a + b ln Z)** [HH §13.2.3.4 pp.422–424]:
  - σ = c₁ + c₂Gbρ_i^½ with ρ_i the free dislocation density inside the subgrains (Al–1Mg–1Mn; Castro-Fernandez et al. 1990) [eq.13.6];
  - **σD/(Gb) = K ≈ 10 for fcc metals** (Derby 1991) [eq.13.7], i.e. σ ∝ 1/D for hot-worked subgrains;
  - **D = K₁ − K₂ log Z** for Al alloys over 10¹³ < Z < 10¹⁷ s⁻¹ (Furu et al. 1992) [eq.13.8 p.423]; HH give no values for K₁, K₂ (Sheppard ch.4 is still missing);
  - ρ_i^½ = c₃/D with c₃ = 10–20 [eq.13.9];
  - (derived example, assumed σ) with G = 25.4 GPa and b = 0.286 nm, Gb = 7.3 N m⁻¹, so D ≈ 73/σ µm with σ in MPa: σ = 30 / 50 MPa → D ≈ 2.4 / 1.5 µm.
- After a strain-rate decrease, ≈ 0.5 further strain is needed to reach the new steady state, and subgrains grow by LAGB migration much faster than under static annealing [HH §13.2.3.5 p.424, Fig.13.9].
- For dilute Al alloys Q_HW is usually close to Q_self = 142 kJ mol⁻¹ [HH Tab.5.1] (**general knowledge** that it is used as such).
- DRX onset by interrupted tests and metallography: GB bulging at ε ≈ 0.175 (1080 °C, 0.1 s⁻¹, Nimonic). The peak strain shifts to higher ε at higher ε̇ or lower T [Bom08 pp.323–327]. Processing maps (DMM) locate stable windows [Bom08 p.324].
- Critical PSN particle size in hot working decreases with lower T and higher ε̇ [HBAL03 PDF p.142]. *Sourced after full-text pass:* d_f = (K₁/(TZ))^½, K₁ = 1712 m² s⁻¹ K; zone formation controls below Z ≈ 10¹² s⁻¹ and nucleus growth above; critical d ≈ 15 µm at Z = 10¹⁰ and ≈ 1.7 µm at 10¹² s⁻¹ [HH eq.13.23–13.27, Fig.13.31 pp.448–450] (details in §3.2b).
- **Static restoration after hot deformation (added)** [HH §13.6 pp.444–450]:
  - static recovery after hot working is generally small (DRV has already acted), with kinetics like ordinary static recovery [§13.6.1];
  - static RX is driven by the lower hot-work stored energy and is **strongly Z-dependent**: CP Al deformed to ε = 3 and annealed at 410 °C had t₀.₅ ≈ 95 s at Z = 6.3×10¹³, ≈ 140 s at 1.08×10¹³ and ≈ 1500 s at 1.16×10¹² s⁻¹ (Gutierrez et al. 1988) [Fig.13.29 p.446] (read from figure);
  - static RX follows JMAK approximately with **n ≈ 1.5–2** (Roberts 1984, 1985) [p.447];
  - empirical (C–Mn and HSLA steels, Sellars & Whiteman 1979): **t₀.₅ = c₁D₀^C ε^(−n) Z^(−K) exp(Q_rex/RT)** and **D_R = c₂D₀^C′ ε^(−n′) Z^(−K′)**; if DRX preceded, C, C′, n and n′ tend to zero [HH eq.13.21–13.22 p.447]. Same forms as [HBAL03 eq.1–4]; HH give no Al constants;
  - after hot deformation, RX nucleates mainly at old grain boundaries (equiaxed grains) and, in Al, cube grains come from elongated cube remnants by SIBM (Vatne et al. 1996) [p.446];
  - metadynamic RX requires DRX nuclei (strain above ε_c for DRX), so it is not expected in dilute or Mn-bearing Al (§13.6.3; inference with the DRV-only conclusion above);
  - grain growth after hot working: Dⁿ = D_Rⁿ + ct·exp(−Q_g/kT) [eq.13.28].

### 9.3 Design levers
- **Hot-band grain and texture set the cube reservoir for cold rolling and annealing:**
  - fully RX hot band (high exit T, high Mn_ss precipitated) gives a strong cube;
  - unRX or recovered hot band (low exit T, fine dispersoids) gives a retained deformation texture.
  - Earing balance follows (§8).
- Exit and coiling T accuracy matters at ±5 °C [AMAG14 p.12].
- **Static RX in coil (self-annealing)** depends on stored energy at the coiling T and on the dispersoid state. HBAL03 confirms the industrial use of self-annealing on the coil from the rolling heat and that **coarse dispersoids at large spacing help RX during coiling** [HBAL03 p.356].
- **Inter-stand RX control:** lower the rolling T or raise the speed to restrain it (but watch for PSN replacing cube) [HBAL03 p.356].
- **Metadynamic RX** (completion after DRX nuclei formed in the pass) is relevant only for high-Mg alloys in Al per [HBAL03 PDF p.142]. Definition now sourced: growth, without incubation, of DRX nuclei present when straining stops above the critical DRX strain (Djaic & Jonas 1972) [HH §13.6.3 p.447].
- **Low Z (higher T, lower rate) in the last hot pass** promotes cube retention and suppresses PSN; high Z does the opposite [HH §12.4.3.2; §15.2.2.3 p.475].

### 9.4 Pitfalls
- Bom08 constants (Q = 379 kJ mol⁻¹, critical strains, processing-map optimum 1000–1080 °C) are for Nimonic 80A and **must not be transferred to Al**. Only the method transfers.
- Homologous temperature should be referenced to the lowest-melting phase, not to pure-Al T_m [Shep99 §1.2]. Low-melting eutectics set the upper hot-working limit [AMAG14 p.11; Bel05 §1.6].
- Deformation heating raises the actual T above the set-point [AMAG14 p.12].
- Steel-type hot-rolling RX regressions predict unrealistically coarse Al grains [HBAL03 p.360].

**Relevance to the slug route (in-line hot mill → quench).**
- Blade's experiment (50 % hot rolling of super-purity Al with Fe, Si or Cu additions; **entry 500 °C, exit 390 °C**; 30 s delay; quench) is almost the user's hot-mill window (≈ 500 → ≈ 380 °C, ≥ 50 %, then a water bath). **Fe clearly inhibited static RX** in it [HBAL03 pp.243–244, Fig.28]. Hot-rolled dilute Al with no hold also stayed deformed until a separate anneal [HBAL03 p.241].
- So the quenched hot band of an Fe-bearing slug alloy is expected to be **dynamically recovered, not recrystallised** (inference). *Quantitative support added after full-text pass:* even CP Al hot deformed to ε = 3 needed t₀.₅ ≈ 1500 s at 410 °C for Z ≈ 10¹² s⁻¹ [HH Fig.13.29]. The in-line mill gives Z ≈ 10¹⁰–10¹³ s⁻¹ (derived, §3.2b), a smaller strain (ε ≈ 0.69 for 50 %), a falling temperature toward 380 °C and a quench within seconds, and the alloy carries Fe in solution. Static RX before the bath should therefore be negligible (derived order-of-magnitude argument; confirm by EBSD).
- **Does the recovered hot band change the slug anneal? (added after full-text pass; inference built on HH).** Four effects, partly opposed:
  1. **More misorientation, not much more stored energy.** Hot-deformed subgrains keep a constant size above ε ≈ 0.5 while their misorientation rises with strain [HH Fig.13.4]. Cold rolling of 30–60 % refines this into a cold cell structure (Al cell size saturates near 0.5 µm by ε ≈ 0.5 [HH p.30]), but the accumulated misorientations and orientation gradients carried over from the hot pass should make nucleation easier than the cold strain alone suggests. The extra stored energy is modest: with σ_hot ≈ 30–50 MPa (assumed), D ≈ 1.5–2.4 µm from σD/(Gb) ≈ 10, and for 2–3° boundaries (γ_s ≈ 0.13–0.17 J m⁻² from Read–Shockley with γ_m = 0.324 J m⁻², θ_m = 15°) 3γ_s/D ≈ 0.15–0.35 MPa (derived), comparable with the ≈ 0.2–0.4 MPa implied for 30–50 % cold rolling (§1.2).
  2. **Cube reservoir.** Hot deformation at low Z stabilises cube bands, which are the SIBM sources of cube after annealing [HH §12.4.1.2, §13.2.4]. An unrecrystallised hot band therefore probably raises the cube fraction of the slug (§8).
  3. **No reset of the cast grain structure.** The prior grain boundaries are the cast-strip grain boundaries. Coarse initial grains mean fewer grain-boundary nucleation sites, slower and more inhomogeneous RX, and orientation-dependent behaviour (Goss-type grains may not recrystallise at all) [HH §7.2.3; §7.4.1, Fig.7.14–7.15]. In Al, deformation banding needs a grain size above ≈ 20 µm [HH §2.7.4], so coarse cast grains will band, which adds transition-band sites.
  4. **PSN sites from the hot pass.** Deformation zones form only at constituents above d_f (≈ 0.6–24 µm along the pass, derived in §3.2b) and are recovered by the quench and later cold-worked; they do not lower the cold-strain d_g of Fig.9.13 (inference).
  Net expectation: the hot band adds nucleation-favouring misorientation and cube sources but does **not** substitute for cold strain in activating PSN. Measure the hot band (EBSD: HAGB fraction, cube fraction, grain size; conductivity) and anneal cold-rolled strip from a quenched and a deliberately recrystallised hot band side by side.
- *Previous version of this note (kept for traceability):* "its recovered substructure and any surviving stored energy add to the 30–50 % cold reduction at the slug anneal (more driving force than the cold strain alone suggests)"; and "the cast-strip grain and its texture are not reset before cold rolling. Coarse columnar cast grains could then carry through as banding (inference; check by EBSD of the hot band)". Both are refined by items 1 and 3 above.
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
- *Added after full-text pass* [HH §15.2.1 pp.469–472]: AA1050 typically has Fe + Si > 1 wt %; its annealing texture depends on the pre-rolling heat treatment, the Fe/Si ratio and the annealing temperature. Fe in solution (< 100 ppm) strongly slows RX; more Fe precipitates on the RX front and lets the R component compete with cube; Si forms plate- or rod-like α-Al–Fe–Si constituents up to 10 µm, lowers the Fe in solution and adds PSN (random component). Al–0.007Fe at 95 %: rolling texture retained at 360 °C, cube at 280 and 520 °C (Hirsch & Lücke 1985). Higher deformation temperature reduces PSN and the random component in Al–Fe–Si (Oscarsson et al. 1991).
- AA8006 (Al–Fe–Mn): cold rolled ε = 0.69 → discontinuous RX at 250 °C; ε = 3.9 → continuous RX at 300 °C; a fine initial grain size (3–12 µm) and > 1 µm particles lower the strain needed for continuous RX [HH §14.3 pp.455–458, Tab.14.1].

**3xxx [HBAL03 PDF pp.171–172; Pol06 pp.129–130; W7; Wil12]**
- Mn_ss in annealed sheet: YS +21 MPa per wt % and UTS +42 MPa per wt %. In H19: YS +35 MPa per wt % Mn, compared with **+70–85 MPa per wt % Mg** [HBAL03 PDF p.172].
- 3003 annealed TS ≈ 110 MPa (1100: 90). 3004 annealed TS ≈ 180 MPa [Pol06 p.129–130].
- 3003 draws better in the cold-worked than in the annealed state (cans) [Pol06 p.35].
- In AA3004 the second-phase strengthening rises fast early and then stays constant, while the solute contribution grows with strain [Ryen03 §2.4 p.29].
- AA3102 (tube, as tested: Si 0.07, Fe 0.41, Mn 0.24) extrudes into fine RX equiaxed grains [Wil12 pp.18, 40].
- Mn (up to 1.25 %) in can alloys "allow[s] high deformation degrees and … prevent[s] grain growth", by slowing RX and through a fairly uniform distribution of Mn precipitates [HBAL03 p.297]. Commercial Al–Mn alloys (3003, 3004, 3105) anneal at 345–415 °C (3003: "400–600 °C"); O/H-temper properties in §4.3 [HBAL03 Tab.37 p.299]. Retained strength is "sufficient … up to 200 °C" [HBAL03 p.299].
- *Added after full-text pass:* can-body alloys AA3004 (Si ≤ 0.3, Fe ≤ 0.7, Cu ≤ 0.25, Mn 1–1.5, Mg 0.8–1.3, Zn ≤ 0.25) and AA3104 (Si ≤ 0.6, Fe ≤ 0.8, Cu 0.05–0.25, Mn 0.8–1.4, Mg 0.8–1.3, Zn ≤ 0.25) [HH Tab.15.1 p.474]; full DC route, texture logic and earing limits in §8.3 [HH §15.2.2]. As-cast DC cells are ≈ 100 µm, decorated with (FeMn)Al₆ and Mg₂Si constituents, with much Mn in solution [p.474].
- Cold-rolled supersaturated **Al–1.3Mn**: T_A ≈ 400 °C, T_B ≈ 350 °C; RX complete in 1 h at 425 °C (fast heating) vs 500 °C (10 °C h⁻¹); slow heating gives MnAl₆ plates on subgrain boundaries at 400 °C and large RD-elongated grains at 550 °C (§5.2) [HH §9.8 pp.311–314].
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
| 4 | Strength from substructure | σ = σ₀ + k₁ d^(−m); hot-worked subgrains σD/(Gb) = K | m = 1 (cells) to 0.5 (subgrains) [Pol06; HBAL03] **vs** m ≈ 1 subgrains, ≈ 0.5 cells [HH, Thompson] (conflict, §2.3); K ≈ 10 for fcc | Pol06 p.36; HBAL03 PDF p.113; HH eq.6.29–6.33, 13.7 |
| 5 | Hall–Petch | σ = σ_i + k D^(−½) | k = 0.065–0.07 (pure Al); ≤0.15 (Mg-free alloys); 0.22–0.30 (5754/5182) MPa m^½ | Ryen03 p.33; HBAL03 PDF p.179 |
| 6 | Logarithmic recovery | σ = σ₀ − (kT/c₂) ln(1 + t/t₀) | Q₀ = 277 (Al–1Mg) to 231 (Al–5Mg) kJ mol⁻¹ | HH eq.6.22 |
| 7 | Climb recovery | 1/σ² − 1/σ₀² = c₃ t; Q = Q_self | Q_self = 142, Q_core = 82 kJ mol⁻¹ | HH eq.6.17–6.18 |
| 8 | Subgrain coarsening (Nes) | dδ/dt = ν_D B_δ b e^(−U*/kT)·2 sinh(4γ_sb V_δ/(δ kT)) | U* = U_s + ΔU_s; V_δ ∝ b³ c^(−e) | Ryen03 eq.2.39 |
| 9 | LAGB mobility | M = C D_s b/kT; region 2–5°: 10–500× below HAGB | Al–0.05Si: Q 125–154 kJ mol⁻¹ | HH eq.5.4; pp.129–134 |
| 10 | Boundary migration | v = M(P_D − P_Z − P_sol); M = M₀ e^(−Q/RT) | HP Al HAGB Q = 63–67 kJ mol⁻¹; with solute → Q_self or Q_solute | HH eq.5.1–5.2; Tab.5.2 |
| 11 | Solute drag (CLS) | P = v/M + α c₀ v/(1 + β² v²) | v ∝ 1/c₀ (drag regime); breakaway at high v or T | HH eq.5.23–5.25 |
| 12 | Deformation zone and PSN criteria | tanθ = tanθ_max e^(−1.8x/d); θ′_max = 0.8 θ_max (d − 0.1)^0.2; **growth criterion d_g = 4γ_b/(αρGb²) = 4γ_b/E_D**, α ≈ 0.5 | zone only for d > 0.1 µm; strain-only for d > 2.5 µm; **measured d_g (cold-rolled Al–Si): ≈ 8–9 / 7 / 4.5–5 / 3.3–3.5 / 2.7 / 2.1 / 1.9 µm at 25 / 30 / 40 / 50 / 60 / 80 / 95 % reduction**; absolute lower bound ≈ 1 µm (0.8 µm) at large strain | HH eq.2.21–2.23, 9.1–9.2, Fig.9.13 p.297; §9.3 p.293; Pol06 p.42 |
| 13 | JMAK | X = 1 − exp(−B tⁿ), B = fṄĠ³/4; Johnson–Mehl X = 1 − exp(−(π/3)N v³ t⁴); industrial X = 1 − exp(−C(t/t₀.₅)^k); Cahn–Hagel Ġ = (1/S_V)dX_V/dt; with Ġ = Ct^(−r): n = 3(1 − r) | **ideal n: 3 (site saturation) / 4 (constant Ṅ) in 3-D; 2/3 in 2-D; 1/2 in 1-D (sourced)**; Al measured: **n = 1.7** (Al–0.0068Cu, 40 % CR), often ≈ 1; SRX after hot deformation 1.5–2; n 3.0 → 0.8 under concurrent precipitation in Al–Mn (ch12 [W12-19]); **Q_RX 60 → 120 kJ mol⁻¹** with 0.0068 at % Cu; apparent Q of pure Al RX ≈ 110–150 kJ mol⁻¹ (derived from Pol06 p.42) | HH Tab.7.3, eq.7.16–7.18, 7.33–7.35, pp.231, 235, 447; HBAL03 eq.19–21 pp.227–228, eq.1 p.359 |
| 14 | Zener | P_Z = 3F_Vγ/2r; P′_Z,max ≈ 1.2F_V^(2/3)γ/r at D_c = (4πr³/3F_V)^(1/3); net RX pressure P = ρGb²/2 − 3F_Vγ_b/d − 2γ_b/R | coherent ×2; bands ×L/t; on boundaries D F_V γ/4r²; **RX retarded if F_V/r > ≈ 0.2 µm⁻¹, nucleation suppressed if F_V/r > 4αΩ/(3θ_m) ≈ 0.15 µm⁻¹** (α 0.35, Ω 5° µm⁻¹, θ_m 15°) | HH eq.4.24–4.36, 9.4–9.7; §9.2.1 |
| 15 | Limiting grain size (corrected after full-text pass) | **D_Z = 4αr/(3F_V)** (diameter; F_V < 0.05); D_ZC = βr/F_V^(1/3) (F_V > 0.05); D_ZP = r(8/F_V)^½ (particles on boundaries); no-growth limit D_M = 2d/(3F_V) | **α ≈ 0.26 (experiments, Manohar 1998) – 0.35 (HH) → D_Z ≈ 0.35–0.47 r/F_V**; α = 1 classical Zener (4r/3F_V); Hillert = 8r/3F_V; β ≈ 3; the earlier KB range (1.3–2.7)·r/F_V over-predicts by 3–8× | HH eq.11.30–11.35, 11.44, Fig.11.12 pp.358–371; HBAL03 eq.38 p.250 |
| 16 | Dispersoid KWN | Gibbs–Thomson c_r = c_∞ exp(2σV_m/(R_g T r)); classical nucleation (Q ≈ 2.07 eV atom⁻¹ for Sc/Zr); dr/dt = (D/r)(c − c_α(r))/(c_β − c_α(r)); LSW r³ − r₀³ = a(t − t₀) | σ(Al₃(Sc,Zr)) = 0.1 J m⁻² (fitted; 0.06–0.18 measured) | Rob04 eq.1–5 |
| 17 | RX fraction from F_V/r | X_RX = vol. fraction where F_V/r < (F_V/r)_crit | (F_V/r)_crit calibrated on one condition | Rob04 p.1419 |
| 18 | Mn solid-solution budget (3103) | Mn_ss = f(homogenisation) | 0.40 → 0.24 → 0.20 → 0.15 at % (Table §5.1) | Ryen03 Tab.3.2 |
| 19 | Diffusion (500 °C) | — | D_Mn = 5×10⁻¹³; D_Cu = 5×10⁻¹⁰; D_Mg,Si = 10⁻⁹ cm² s⁻¹; +50 °C → ~⅓ homogenisation time | Pol06 p.105 |
| 20 | Anneal anchors | — | 3xxx O-anneal 380–420 °C/0.5–1 h; 1050 320–350 °C; 8011 340–400 °C; AA3103 ε = 2 → RX 45 s at 400 °C; CP Al 200 °C vs zone-refined 50 °C; Al–1.3Mn (80 % CR) 1 h RX at 425 °C (fast heating) / 500 °C (10 °C h⁻¹) | W7 Tab.2; Ryen03 §3.4; HH Tab.7.2, Tab.9.1 |
| 21 | Strain measures | ε = ln(t₀/t); ε_vM = (2/√3)ε | 39 % → 0.5; 63 % → 1; 87 % → 2; 95 % → 3 | Ryen03 eq.3.2–3.4, Tab.3.3 |
| 22 | Grain growth | D^n − D₀^n = k₀ e^(−Q/RT) t; ideal R² = R₀² + Cγt with ΔP = 2γ/R; after hot work Dⁿ = D_Rⁿ + ct·e^(−Q_g/kT) | n = 2 ideal (sourced); **measured n 2–4 in zone-refined metals (mean 2.4), n = 4 for high-purity Al (sourced)**; n falls with rising T/T_m; driving pressure ≈ 10⁻² MPa; Q ≈ Q_self; largest grains 2.5× (HH) to 3–4× (HBAL03) the mean | HBAL03 eq.32–35 pp.247–248; HH eq.11.5–11.7, Tab.11.1 pp.336–338, eq.13.28; HH §5.5.2 |
| 23 | Hot working | Z = ε̇ e^(Q/RT) = c₁[sinh(c₂σ)]ⁿ; σD/(Gb) = K ≈ 10; **D = K₁ − K₂ log Z** (Al, 10¹³ < Z < 10¹⁷); σ = c₁ + c₂Gbρ_i^½, ρ_i^½ = c₃/D (c₃ 10–20); SRX t₀.₅ = c₁D₀^C ε^(−n) Z^(−K) e^(Q_rex/RT); D_R = c₂D₀^C′ε^(−n′)Z^(−K′) | K₁, K₂, Q for Al not given in HH or HBAL03; Q_HW ≈ 142 kJ mol⁻¹ assumed (general knowledge); SRX in CP Al (ε = 3, 410 °C): t₀.₅ ≈ 95 / 140 / 1500 s at Z = 6.3×10¹³ / 1.1×10¹³ / 1.2×10¹² s⁻¹; JMAK n 1.5–2; the steel-type t₀.₅/d_rex set over-predicts Al grain size | HH eq.13.1–13.9, 13.21–13.22, Fig.13.29; HBAL03 eq.1–4 pp.359–360; Bom08 (method) |
| 24 | Q from logarithmic recovery data (added 2026-10-12) | X = C₁ ln(t/t₀), t₀ = τ₀ e^(Q/RT) → C₁ = (∂X/∂ln t)_T; **Q = −R (∂X/∂(1/T))_t / C₁** (X as a fraction or in %, but the same in both derivatives) | Valid only in the logarithmic regime (not t → 0 or ∞), for isothermal holds long compared with the heat-up, and for a recovery-only state (no RX or precipitation in the window). A single-slope fit without C₁ (Junit08) gives unit-dependent numbers (§2.4) | HH eq.6.6–6.7 (form); t₀ form **general knowledge** |
| 25 | Mn supersaturation at anneal T (added 2026-10-12) | ΔMn = Mn_ss − Mn_eq(T) | Mn_eq (wt %), (Al)+Al₆Mn+α field: 0.73 / 0.44 / 0.25 / 0.15 / 0.06 at 600 / 550 / 500 / 450 / 400 °C; ≤0.08 with free (Si); 0.026–0.05 at 427–527 °C with Al₃Fe present. Valid for equilibrium three-phase fields; real 3xxx with Fe and Si lies between these bounds | Bel05 Tab.1.9, 1.13 |
| 26 | Second-order recovery (added, HBAL03 pass) | dρ/dt = −kρ² → ρ = 1/(kt + 1/ρ₀) | ρ: 10¹⁵ → 1.5×10¹⁴ m⁻² in recovery; up to 40 % of the work-hardening hardness recovered in pure Al | HBAL03 eq.4–5 pp.219–220; pp.216–217 |
| 27 | RX front velocity (atomic-jump model) | v = 2bνc_v (F_sa/kT) e^(−Q_a/kT), F_sa = F_s·Ω | ν = 10¹³ s⁻¹; c_v = 10⁻⁵ (700 K), 10⁻⁴ (800 K); Q_a ≈ 45 kJ mol⁻¹; v = 0.08 / 1.85 µm s⁻¹ at 427 / 527 °C (ρ = 10¹⁵). Trend use only (no solute or particles) | HBAL03 eq.9–12 p.224 |
| 28 | RX grain size from N and v | d = 2v t_c ∝ (v/N)^¼ (printed 2(2v/πN)^¼; 2(3v/πN)^¼ for consistency, derived) | grain size set mainly by nucleation density | HBAL03 eq.20–22 pp.227–228 |
| 29 | Critical nucleus radius | R_c = 2γ/F_s | Mao: 1–3 µm (γ 0.6–1.9 J m⁻²); 0.09–0.6 µm with γ = 0.324 J m⁻², F_s = 1–7 MPa (derived) | HBAL03 eq.8 p.221 |
| 30 | TM effect on RX temperature | ΔT_RX,start / ΔT_RX,finish (max) | Mn 0.77 at %: +30 / +25 K; Fe 0.04 at %: +65 / +35 K; Zr 0.09: +105 / +240 K; Sc 0.20: +120 / +320 K (after a 500 °C anneal + hot rolling + 450 °C anneal, i.e. pre-precipitated) | HBAL03 Tab.35 p.296 |
| 31 | Mn retained vs cooling rate; Mn decomposition | max Mn in (Al): 1.82 / 2.5 / 2.8 / 3–5 % at 10⁻¹ / 10 / 10² / 10³ K s⁻¹; decomposes > 325 °C (Al₆Mn 300–350 °C) | sets Mn_ss for a non-homogenised (strip-cast) route | HBAL03 Tab.33 p.294; Tab.34 p.295; p.299 |
| 32 | NHT anneal practice | T = lowest giving the softest state; fast heat-up; hold only until the load reaches T; cooling rate unimportant (not for Mg + Si alloys) | 1xxx, 3004, 3105, 5xxx 343 °C; 3003 413 °C [p.888]; 3105 345 °C, 3004 415 °C [p.299]; 3xxx 380–420 °C/0.5–1 h [W7] | HBAL03 pp.887–888, 299; W7 Tab.2 |
| 33 | PSN grain size (added after full-text pass) | efficiency 1: **D ≈ d·F_V^(−1/3)**; with efficiency η: D ≈ d·(ηF_V)^(−1/3); general: **D_N ≈ N_d^(−1/3)**, N_d = number of particles > d_g per unit volume | ≤ 1 grain per particle (several only for d > 5–10 µm); η = 0.85 (Al–0.8Si, 3 µm, ε = 1.4); η ≈ 0.14 (Al–Si, 4.9 µm, F_V 0.01, 50 % CR; derived); η "very low" near d_g; islands at ε = 0.7 | HH eq.9.3, 9.9, Fig.9.17, Fig.9.19, Tab.11.3 |
| 34 | PSN with a fine dispersion (bimodal) | **d_g = 4γ_b/[(ρGb²/2) − (3F_Vγ_b/2r)]** (F_V, r of the fine particles) | fine particles raise d_g and the RX grain size; kinetics follow the fine dispersion; stronger cube | HH eq.9.8 p.307 |
| 35 | PSN after hot deformation | ε̇_c = K₁e^(−Q_s/RT)/(Td²) + K₂e^(−Q_b/RT)/(Td³); **d_f = (K₁/(TZ))^½**; d_g = 4γ_bD/(3γ_s) | **K₁ = 1712 m² s⁻¹ K, K₂ = 3×10⁻¹⁰ m³ s⁻¹ K**; zone formation controls below Z ≈ 10¹² s⁻¹, growth above; critical d ≈ 15 µm (Z = 10¹⁰), ≈ 1.7 µm (10¹²), ≈ 0.3 µm (10¹⁶) | HH eq.13.23–13.27, Fig.13.31 pp.448–450 |
| 36 | Concurrent precipitation and RX (rapid heating) | Regime I T < T_B: precipitation first, RX blocked, later broad-front SIBM, L_C ≥ 4γ/(P_D − P_Z); Regime II T_B–T_A: partial RX, X_V ≈ f(T) not t; Regime III T > T_A: RX first, equiaxed | **Al–1.3Mn and Al–0.25Zr: T_A ≈ 400 °C, T_B ≈ 350 °C**; Al–0.25Sc both > 500 °C; slow heating (10 °C h⁻¹) raises the 1 h RX temperature by 75 °C (Al–1.3Mn) or 100 °C (Al–0.25Zr) | HH §9.8, Fig.9.23, eq.9.10–9.11, Tab.9.1 pp.310–316 |
| 37 | Particle-controlled RX grain size regimes | F_V/r < A grain-growth limited; A–B nucleation limited (AGG-prone); > B no discontinuous RX | optimum (smallest stable) grain at F_V/r = A; A and B rise with strain | HH §9.6 Fig.9.21 pp.307–309 |
| 38 | Abnormal grain growth with particles | Ψ = 3F_V R̄/d: 0–0.1 broadening; 0.1–0.25 AGG + normal; 0.25–1 AGG only; > 1 none | practical AGG limit Ψ ≈ 0.6 (largest grain ≈ 2.5× mean); AGG mainly when particles coarsen or dissolve | HH eq.11.40–11.44 pp.369–374 |
| 39 | SIBM critical size | multiple-subgrain: R_crit = 2γ_b/(P(1 − f)) or 2γ_b/(P(1 − f)^½); single-subgrain: R_crit = 2γ_b/P = 4γ_bR₂/(3γ₂); with particles P → P − P_Z | dominant below ≈ 20 % reduction in rolled Al; single-subgrain SIBM for misorientations > ≈ 1° | HH eq.7.41–7.44 pp.253–257 |
| 40 | Subgrain growth | D^n − D₀^n = c₁t; in a gradient dR/dt = (Mγ_m/θ_mR)[θ₀ + Ω(R − R₀)]; pinned: dR/dt = Mγ_s(α/R − 3F_V/2r) | n ≈ 2 (Al–1Mn), ≈ 4 (99.5 % Al); limiting subgrain diameter 4r/3F_V | HH eq.6.27, 6.38, 6.46 |
| 41 | RX driving and curvature pressures | P_d = αρGb² (α ≈ 0.5); P_c = 2γ_b/R | P_d ≈ 1 MPa for ρ = 10¹⁵ m⁻²; P_c = P_d at R ≈ 1 µm | HH eq.7.2–7.3 |
| 42 | Strain and strain-path rules | critical strain 1–3 %; RX rate saturates at ε = 2–4; ε_equiv = ε_perm + 0.65ε_red (Cu) | reversed strain in Al: slower RX and larger grains | HH §7.2.1 pp.222–224 |
| 43 | Measurement of X_V and grain size | σ²/X_V² = (1 − X_V)/n_r (≈ 500 points at X_V = 0.5); EBSD: HAGB-based, ≥ 10 pixels per grain | EBSD pattern-quality point counting unreliable in Al | HH eq.A2.1; App.2 pp.545–549 |

---

## 12. Open questions / gaps (prioritised)

1. **Missing core text:**
   - **Resolved 2026-10-12: Humphreys & Hatherly** (full text pp.1–574 read from the user's three-part split; only the reference tail and subject index are missing). It closes the former HH gaps on RX kinetics (JMAK exponents, Q, strain, solute and heating-rate effects; ch.7), PSN criteria and efficiency, Zener effects on RX, bimodal particles and the **precipitation–RX T–t–T framework** (ch.9), grain growth and the Zener-limit variants (ch.11), RX textures incl. P/Q and the cube mechanisms (ch.12), hot deformation and static RX/PSN after hot working (ch.13), continuous RX (ch.14) and the industrial Al routes incl. can body and AA6xxx (ch.15). Integrated into §1–§11 ("added/corrected after full-text pass").
   - **Resolved 2026-10-12: Handbook of Aluminum** (full text read; Mao ch.4 integrated into §1–§11). It closed the notes on SIBM, the Johnson–Mehl n = 4 derivation, the parabolic grain-growth law and the classical Zener limit, and added anneal practice, TM effects on T_RX and the AA3104 cube/PSN competition.
   - **Still missing:** Sheppard ch.3–5 (hot-working constants, subgrain size vs Z for Al: needed for K₁, K₂ of HH eq.13.8 and Q_HW; only Sheppard pp.291–420 exist as text); Ryen §4.5.2 (AA3103 work hardening) and ch.5 (solute effects). Polmear §3.6 is now available as full text in the same Drive batch but has not yet been read into this chapter.
   - Remedy for Sheppard: split part 1 ("1.pdf", 7.73 MB, refused by the Drive connector) into pieces of ≤ 5 MB and re-upload.
2. **3xxx- and T11-specific RX kinetics are not in hand:** k₀, n and Q of RX for AA3102, AA3103, AA3207 or T11 vs solute in solution, Fe/Si, strain and heating rate, and the precipitation C-curve (positions of T_A and T_B) for the actual strip.
   - Anchors now available: the HH framework and **Al–1.3Mn values** (T_A ≈ 400 °C, T_B ≈ 350 °C; 1 h RX at 425 vs 500 °C for fast vs slow heating) [HH §9.8, Tab.9.1]; JMAK n of 1–2 in Al and Q_RX 60 → 120 kJ mol⁻¹ with trace Cu [HH pp.231, 235]; trace Fe raising T_RX by up to ~100 °C [HH Fig.7.10]; HBAL03 model forms and Mn/Al₆Mn decomposition onsets [pp.227–228, 295, 299, 359]; web chapter JMAK n 3.0 → 0.8 under concurrent precipitation [ch12 §4].
   - **Still no (k₀, n, Q) set and no T_A/T_B for a lean, non-homogenised, Fe- and Mg–Si-bearing strip.** The literature anchors are for Al–1.3Mn (much more Mn supersaturation) and dilute binaries. The realistic source is the trial programme proposed in §5.2 (isochronal and isothermal anneals at two heating rates; conductivity + EBSD HAGB fraction + grain size/aspect ratio).
3. Quantitative **solute-drag coefficients for Mn, Fe and Si in Al** (only Cu and Mg are shown qualitatively). Interaction of Mn_ss with recovery kinetics (U*, V in the Nes model).
   - HBAL03 adds v ∝ 1/c_Cu, the Lücke–Detert segregation form and the extreme Fe effect (Al–0.01 at % Fe at 150 °C) [pp.220, 225, 248]; HH (full text) adds the macroscopic Fe effect on T_RX [Fig.7.10] and the Cu effect on Q_RX [p.231], but **neither gives drag coefficients** for Mn, Fe or Si.
4. **PSN for the actual constituents and strip.** *Largely resolved for generic Al (full-text pass):* d_g vs strain [HH Fig.9.13], efficiency (≤ 1 per particle, 0.85 at ε = 1.4, very low near d_g; ≈ 0.14 derived at 50 %), clustering, bimodal d_g and PSN after hot deformation (§3.2b). **Still open:** (i) d_g and efficiency for plate- or rod-shaped Al₁₅(FeMn)₃Si₂, Al₆(Mn,Fe) and α-AlFeSi constituents in polycrystalline strip (HH's data are mostly equiaxed Si in Al–Si single crystals); (ii) the **size distribution and clustering of Fe-rich constituents in rotary-cast, hot-rolled, quenched and 30–60 % cold-rolled strip** (number per mm² above 2, 3, 5, 7 µm). Item (ii) is the main input for the slug grain size and must be measured.
5. **Microsegregation of Mn** (k < 1, so cell centres are depleted (general knowledge)). Where do dispersoid-free zones form in DC vs twin-roll 3xxx, and are they the coarse-grain seeds (cf. Rob04 for Zr)? HBAL03 confirms that TM dendritic segregation is not easily removed by homogenisation (TM diffusivities 10⁻¹⁴–10⁻¹² cm² s⁻¹ at 500 °C) [p.295]; this matters more for the non-homogenised strip route. The location of dispersoid-free zones is still open; HH note only that precipitation and RX interact more strongly where precipitation is slow or boundaries are very mobile (§9.8.3).
6. Sag resistance, braze erosion vs grain size and shape: no quantitative source in Drive.
7. Taylor factor and texture-dependent stored energy for Al rolling components (only qualitative for cold-rolled Al [HH p.23]). Partial anchor added: in hot-deformed Al–1Mg (400 °C, ε = 1) cube subgrains store ≈ 7.6 vs 12–13 mJ cm⁻³ for Brass, Copper and S [HH Tab.13.1 p.427].
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
   - **Further literature anchors (HH full text, 2026-10-12):**
     - RX temperature of commercial-purity Al 200 °C vs 50 °C for zone-refined Al (large reductions) [HH Tab.7.2 p.228];
     - Q_RX of pure Al 60 kJ mol⁻¹, 120 kJ mol⁻¹ with 0.0068 at % Cu (Vandermeer & Gordon 1963) [HH p.231];
     - JMAK n = 1.7 for Al–0.0068Cu cold rolled 40 % [HH Fig.7.12 p.235]; n ≈ 1.5–2 for static RX after hot deformation [HH p.447];
     - Al–Si, 50 % CR, 300 °C: t₀.₅ ≈ 5000 s without particles, ≈ 30–60 s with 4.6–4.9 µm particles [HH Fig.9.2 p.288] (read from figure);
     - cold-rolled supersaturated Al–1.3Mn: RX complete in 1 h at 425 ± 5 °C (fast heating) and 500 ± 20 °C (10 °C h⁻¹) [HH Tab.9.1 p.312];
     - CP Al hot deformed to ε = 3, annealed at 410 °C: t₀.₅ ≈ 95–1500 s for Z = 6.3×10¹³ to 1.16×10¹² s⁻¹ [HH Fig.13.29 p.446] (read from figure);
     - RX rate rises with strain and saturates at true strains of 2–4 [HH p.222];
     - Zener limit D_Z = 4αr/(3F_V) with experimentally calibrated α ≈ 0.26–0.35, i.e. 0.35–0.47 r/F_V [HH pp.358–361], which is relevant to any fixed "Zener cap" used in a model (§6, §11 row 15).
9. Junit08's activation energies are unreliable (§2.4). Do not reuse them.
   - Re-assessed after the 2026-10-12 full-text pass: they are artefacts of fitting without C₁ and with X in %.
   - The pages that would allow a corrected Q (the 150 °C time series, Tables 4.5–4.8) are not in the Drive file. The file is a 24-page excerpt, so this item can only be closed with the complete thesis.
   - A clean recovery-kinetics data set for 1xxx/3xxx (σ or hardness vs t at ≥3 temperatures, the same strain, isothermal holds) is still needed for H-temper and recovery modelling. HBAL03 supplies only the functional form (second-order, ρ = 1/(kt + 1/ρ₀) [eq.5 p.220]), not Al rate constants.
10. **Data conflicts flagged in the HBAL03 full-text pass (2026-10-12)**. Resolve before using these numbers in models:
    - Mao's SFE 250 mJ m⁻², b = 0.35 nm and γ_HAGB 0.6–1.9 / 1.0 J m⁻² vs HH's 166 mJ m⁻², 0.286 nm and 0.324 J m⁻² (§1.4). This KB uses the HH values.
    - O-anneal temperatures for 3003/3004 differ between HBAL03 ch.5 (Tab.37), ch.19 (Tab.7) and W7 (§4.3).
    - DRX in Al–Mn and 99.5 % Al: Mao (flow curves) vs Karhausen & Korhonen (industrial: post-dynamic/static RX only) (§9.1). *Resolved by the HH full text in favour of dynamic recovery:* DRX only in very-high-purity Al; no particle-stimulated DRX in Al alloys [HH pp.416, 431, 436–437].
    - Zener limit 4r/3F_V as a radius (Mao) or a diameter (common usage) (§6). *Resolved by the HH full text:* Zener's 4r/3F_V is a diameter (α = 1); Mao's radius form is Hillert's result; experiments favour α ≈ 0.26–0.35 [HH pp.358–361].
    - 1100-O UTS 75 MPa [HBAL03 Tab.3] vs ≈ 90 MPa [Pol06].
    - Mao's eq.22 coefficient and his Anderson–Mehl sentence are internally inconsistent (§4.2, §4.4).
    - *Added in the HH full-text pass (2026-10-12):*
      - subgrain coalescence as a nucleation mechanism: Mao (yes) vs HH (no convincing evidence; LAGB migration) (§3.1);
      - recovery-driven heating-rate effect: HBAL03 (10× slower RX after a recovery pre-anneal of 99.998 % Al) vs HH (no evidence in single-phase alloys; heating-rate effects act through precipitation) (§2.3, §4.4);
      - "continuous RX" for precipitate-pinned structures (Mao) vs "extended recovery" (HH) (§3.1);
      - substructure-strength exponent: m ≈ 1 cells / 0.5 subgrains [Pol06; HBAL03] vs m ≈ 1 subgrains / 0.5 cells [HH] (§2.3);
      - Zener limit: the classical 4r/3F_V (α = 1) and Mao/Hillert 8r/3F_V vs the experimental α ≈ 0.26–0.35 (§6); this KB now uses the HH-calibrated value;
      - Al–1Mn/620 °C grain-growth texture sequence: {011}<133> → {001}<320> [HBAL03] vs {011}<122> → {013}<231> [HH] (§7.1);
      - P component indices: {011}<122> [HH Tab.12.1] vs the {011}<566> used elsewhere (§8.5);
      - HH internal: Hillert's doubled diameter is said to correspond to α = 0.5 in eq.11.30 but would need α = 2 (§6); the D_M and D_Z columns of HH Tab.11.3 do not reproduce from eqs.11.42/11.44 (§7.1); eq.9.3 prints F_V^(1/3) where the exponent must be −1/3 (§3.2b).
11. **Slug-route data needed (new 2026-10-12):** Blade's figure (Fe effect on static RX after 50 % hot rolling, 500 → 390 °C) [HBAL03 Fig.28 p.244] is the closest literature analogue to the in-line hot mill, but its values are figure-only. Obtain Blade, *Metal Science* 13 (1979) 206–210, or measure the hot-band state (EBSD fraction RX, conductivity) on rotary-cast strip directly. HH add the Z-dependence of static RX in CP Al [Fig.13.29] and the PSN map vs Z [Fig.13.31] (§9.2), which support, but do not replace, a direct measurement. The in-line mill's strain rate and roll-gap temperature are also needed to place it on the Z axis (§3.2b used assumed 1–30 s⁻¹).
12. **Measurements that turn the HH framework into slug-route numbers (new, full-text pass):**
    - constituent size distribution and clustering above 2, 3, 5 and 7 µm in cold-rolled strip (gap 4);
    - RX fraction (EBSD, HAGB-based) and grain-size distribution vs ε_cold (30 / 45 / 60 % and, if possible, ≥ 80 %), surface and centre, to calibrate d_g and the PSN efficiency (§3.2b, §4.6);
    - isochronal and isothermal anneals at two heating rates with conductivity, to locate T_A and T_B (§5.2);
    - F_V and r of precipitates formed during the anneal (Zener cap and AGG window, §6, §7.1);
    - hot-band EBSD (RX fraction, HAGB fraction, cube fraction, prior grain size) and a comparison of slugs made from a quenched vs a deliberately recrystallised hot band (§9).
