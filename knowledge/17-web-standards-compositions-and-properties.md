# 17 — Web research: standard compositions, designations and property limits (3xxx / 1xxx / 8xxx)

**Source type:** online research (not from the user's Drive), retrieved 2026-10-12.
**Scope.** This file collects registered chemical-composition limits, designation equivalents, EN 485-2 property limits, physical properties and slug-producer datasheets for the alloys the project uses or benchmarks. It covers 1050A, 1070A, 1100, 1200, 3102, 3207 (+3207A), 3003, 3103, 3004, 3104, 3005, 3105, 3006/3015/3016, 8011, 8079 and 8111. It answers the composition questions left open in [05 §4.2 / §11](05-aluminium-alloy-systems-and-tempers.md) and [09 §10–11](09-in-house-rd-data.md) (questions 1–3, 12).
**Rules used.** Every value carries a source key `[W17-xx]`. No number was added from memory. Cells marked "n.r." (not retrieved) had no source in this session. Drive-sourced values from chapter 05 appear only as clearly labelled cross-references `[ch05 / P p.121]`. They are **not** web-verified.

---

## 0. Retrieval method and limitations (read first)

Retrieval in this session was heavily restricted. Every number below must be read with these limits in mind.

1. **No document was opened in full.**
   - The page-fetch tool failed for every domain with a DNS error (`getaddrinfo ENOTFOUND`). This hit aluminum.org, makeitfrom.com, en.wikipedia.org and webstore.ansi.org.
   - A direct download was refused by the environment's network policy. The egress proxy denied the CONNECT to www.aluminum.org, www.makeitfrom.com and en.wikipedia.org.
2. **All values are search-result extracts (SX).** They come from the search engine's indexed text of the cited document, as returned by the search tool. For some Teal Sheets rows the tool warned that the PDF text extraction was garbled, so column alignment is not guaranteed.
3. **"Query-matched" values are weaker evidence.** For some rows the query itself contained candidate numbers, and the extract reported that the row matched them. These values carry an echo risk and are flagged **(QM)**. A value counts as corroborated only if a second extract returned it from a query that did *not* contain the number.
4. **The search budget ran out.** The shared web-search budget for this turn (200 calls, shared by all agents) was exhausted after this task's first ~25 searches. Many target alloys and almost all EN 485-2 tables were therefore **not reached**. See §8.

**Confidence grades used in the tables**
- **A**: two or more independent extracts agree, at least one of them obtained without numbers in the query.
- **B**: a single primary-source extract, or query-matched only.
- **C**: a single secondary source.

---

## 1. Sources

| Key | Organisation | Document | Year / edition | URL | Type |
|---|---|---|---|---|---|
| W17-01 | The Aluminum Association (AA) | *International Alloy Designations and Chemical Composition Limits for Wrought Aluminum and Wrought Aluminum Alloys* ("Teal Sheets"). The Germany section is attributed to the Gesamtverband der Aluminiumindustrie (per extract) | 2025, and the "December 2025" file (posted 2026-01) | https://www.aluminum.org/sites/default/files/2026-01/Teal%20Sheets%20December%202025.pdf · https://www.aluminum.org/sites/default/files/2025-10/Teal%20Sheets%202025.pdf | **Primary** (SX only) |
| W17-02 | AA | Teal Sheets, 2018 edition (August 2018 revision; files posted 2021) | 2018 | https://www.aluminum.org/sites/default/files/2021-10/Teal%20Sheet.pdf · https://www.aluminum.org/sites/default/files/2021-11/TealSheet.pdf | **Primary** (SX only) |
| W17-03 | AA | Addenda to the 2018 Teal Sheets | Dec 2022; Feb 2024; May 2024; 29 Sep 2025 | https://www.aluminum.org/sites/default/files/2022-12/Addendum_to_2018_Teal_Sheets_DECEMBER_2022.pdf · https://www.aluminum.org/sites/default/files/2024-02/Addendum_to_2018%20Teal_Sheets_FEBRUARY_2024.pdf · https://aluminum.org/sites/default/files/2024-05/Addendum_to_2018_Teal_Sheets_MAY_2024.pdf · https://www.aluminum.org/sites/default/files/2025-09/Addendum_to_2018_Teal_Sheets_September_29_2025.pdf | **Primary** (SX only) |
| W17-04 | AA / Matplus GmbH | Teal Sheets landing page; announcement of the digitised Teal Sheets database (teal-sheets.matplus.eu, free after registration) | current | https://www.aluminum.org/teal-sheets · https://www.aluminum.org/news/aluminum-association-matplus-release-digitized-database-international-wrought-aluminum-alloy | Primary (publisher info) |
| W17-05 | ASTM International | ASTM B210-12, *Aluminum and Aluminum-Alloy Drawn Seamless Tubes*: composition table (it notes the Teal Sheets control where values differ) | 2012 | https://store.astm.org/b0210-12.html | **Primary** (standard; SX only) |
| W17-06 | SteelNumber (database) | ENAW-AlMn0.2 / ENAW-3102, citing EN 573-3:2009 | n.d. | http://www.steelnumber.com/en/steel_alloy_composition_eu.php?name_id=1052 | Secondary |
| W17-07 | SteelNumber | ENAW-AlMn0.6 / ENAW-3207, citing EN 573-3:2009 | n.d. | http://www.steelnumber.com/en/steel_alloy_composition_eu.php?name_id=1059 | Secondary |
| W17-08 | SteelNumber | ENAW-AlMn1 / ENAW-3103, citing EN 573-3:2009 | n.d. | http://www.steelnumber.com/en/steel_alloy_composition_eu.php?name_id=1053 | Secondary |
| W17-09 | SteelNumber | ENAW-3104 (id 1055), 3004 (1048), 3005 (1049), 3105 (1056) and 3003 (1047) pages, citing EN 573-3:2009. Composition tables mostly garbled in the extract | n.d. | http://www.steelnumber.com/en/steel_alloy_composition_eu.php?name_id=1055 (and the ids listed) | Secondary (partial) |
| W17-10 | Almet (French supplier) | 3207 (AW-AlMn0,6) product page | n.d. | https://almet-metal.com/aluminium/3207.html | Secondary |
| W17-11 | Euralliage | 3207A (AW-AlMn0,6(A)) page | n.d. | https://www.euralliage.com/3207A_english.htm | Secondary |
| W17-12 | Euralliage | 3102 (AW-AlMn0,2) page | n.d. | https://www.euralliage.com/3102.htm | Secondary |
| W17-13 | EPO | EP 2881477 B1, *Heat-resistant alloy for production of aerosol cans*. It quotes EN AW-3102 limits per EN 573-3 | 2017 (B1) | https://data.epo.org/gpi/EP2881477B1 | Secondary (patent) |
| W17-14 | AZoM | *Aluminum 3102 Alloy (UNS A93102)* | n.d. | https://www.azom.com/article.aspx?ArticleID=8733 | Secondary |
| W17-15 | Wikipedia | *3102 aluminium alloy* | n.d. | https://en.wikipedia.org/wiki/3102_aluminium_alloy | Secondary |
| W17-16 | Aalco Metals Ltd | *Aluminium Alloy 3103 H14 Sheet* datasheet, citing BS EN 573-3:2009 and BS EN 485-2:2008 (updated 13 Nov 2018) | 2018 | https://www.aalco.co.uk/datasheets/Aalco-Metals-Ltd_Aluminium-Alloy-3103-H14-Sheet_298.pdf.ashx | Supplier summary of EN (secondary to EN) |
| W17-17 | Righton Blackburns | 3103 H14 Sheet datasheet (duplicates Aalco) | n.d. | https://www.rightonblackburns.co.uk/datasheets/view/Righton-Blackburns-Ltd_Aluminium-Alloy-3103-H14-Sheet_298.pdf | Secondary |
| W17-18 | Aalco Metals Ltd | *Aluminium Alloy 1050A H14 Sheet* datasheet, citing BS EN 573-3:2009 and BS EN 485-2:2008 | n.d. | https://www.aalco.co.uk/datasheets/Aalco-Metals-Ltd_Aluminium-Alloy-1050A-H14-Sheet_57.pdf.ashx | Supplier summary of EN (secondary to EN) |
| W17-19 | Righton Blackburns | 1050A H14 Sheet datasheet | n.d. | https://www.rightonblackburns.co.uk/datasheets/view/Righton-Blackburns-Ltd_Aluminium-Alloy-1050A-H14-Sheet_57.pdf | Secondary |
| W17-20 | mfgrobots | *BS EN 573-3: Grade 3103 H14* | n.d. | https://www.mfgrobots.com/Article/material/metal/39902.html | Secondary (tertiary) |
| W17-21 | Chalco Aluminum | *Global Aluminum Alloy Conversion Chart* | n.d. | https://www.chalcoaluminum.com/blog/conversion-chart/ | Secondary |
| W17-22 | CEN via iTeh / BSI | EN 573-3:2019 and BS EN 573-3:2019 catalogue entries (edition only; table rows not visible) | 2019 | https://standards.iteh.ai/catalog/standards/cen/22ea55a3-ad41-4b4e-a3de-c580d0eadd23/en-573-3-2019 · https://knowledge.bsigroup.com/products/aluminium-and-aluminium-alloys-chemical-composition-and-form-of-wrought-products-chemical-composition-and-form-of-products-2 | Primary (catalogue only) |
| W17-23 | MakeItFrom | *3102 (AlMn0.2, A93102) Aluminum* | n.d. | https://www.makeitfrom.com/material-properties/3102-AlMn0.2-A93102-Aluminum | Secondary |
| W17-24 | SteelNumber | AA3005 worldwide equivalents | n.d. | http://www.steelnumber.com/en/equivalent_alloy_eu.php?zname_id=1035 | Secondary |
| W17-25 | Total Materia | DIN 3.3207 entry (DIN 1725-1) | n.d. | https://www.totalmateria.com/en-us/material/3000351 | Secondary |
| W17-26 | ISO | ISO 209:2007 catalogue page (status shown as withdrawn in the extract) | 2007 | https://www.iso.org/standard/35310.html | Primary (catalogue only) |

---

## 2. Chemical composition limits (wt %; single value = maximum; "Rem." = remainder)

"—" means no specific limit is shown in the source row. Under the AA/EN convention, such an element is then governed by the "others each / total" limits. The footnote wording of that convention was **not** retrieved here; see §6.1 and §8. "n.r." means not retrieved.

### 2.1 Web-sourced rows

| Alloy | Si | Fe | Cu | Mn | Mg | Cr | Zn | Ti | Others each / total | Al | Registered | Sources | Grade | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **3102** | 0.40 | 0.7 | 0.10 | 0.05–0.40 | — | — | 0.30 | 0.10 | 0.05 / 0.15 | Rem. | **1972** [W17-02 SX]; registrant n.r. | W17-02, W17-05, W17-06, W17-13, W17-14 | **A** | Teal, ASTM B210, EN 573-3:2009 (via W17-06) and the patent quoting EN 573-3 (W17-13) agree. None lists a Mg limit. W17-14 gives "Al ≥ 97.8" and W17-15 "≥ 97.85". Both are derived from 100 − Σmax (0.40+0.7+0.10+0.40+0.30+0.10+0.15 = 2.15) *(recalc.)*; neither is a registered Al minimum. W17-12 and W17-06 class 3102 as *not* a food-contact alloy (secondary; verify against EN 602). |
| **3207** | 0.30 | 0.45 | 0.10 | 0.40–0.8 | 0.10 | n.r. | 0.10 | n.r. | 0.05 / 0.15 | Rem. | **1979, Germany** [W17-01 SX] | W17-01 (QM), W17-07, W17-10 | **A** | W17-07 (EN 573-3:2009) and W17-10 match, and both were obtained without numbers in the query. The Teal row was query-matched for Si–Mg, and its Zn/Ti cells were not visible. W17-07 and W17-10 class 3207 as food-contact suitable (secondary). |
| **3207A** | 0.35 | 0.6 | 0.25 | 0.30–0.8 | 0.40 | 0.20 | **0.25** [W17-01] / **0.20** [W17-11] | n.r. | 0.05 / 0.15 | Rem. | **1990, Germany** [W17-01 SX] | W17-01, W17-11 | B | **Zn discrepancy** between Teal and Euralliage. W17-11 calls 3207A a limited-production alloy for particular fields. |
| **3103** | 0.50 | 0.7 | 0.10 | 0.9–1.5 | 0.30 | 0.10 | 0.20 | Zr+Ti ≤ 0.10 | 0.05 / 0.15 | Rem. | n.r. | W17-08, W17-16, W17-17 | **A** (EN) | SteelNumber and Aalco agree. W17-17 duplicates Aalco. The Teal row was not retrieved. |
| **3104** | 0.6 | 0.8 | 0.05–0.25 | 0.8–1.4 | 0.8–1.3 | n.r. | n.r. | n.r. | n.r. / 0.15 [W17-09] | Rem. | **1978** [W17-02 SX] | W17-02 (QM), W17-09 | B | Ga ≤ 0.05 [W17-09]. The extract could not map the Zn, Ga, V and Ti columns. |
| **3004** | n.r. | n.r. | n.r. | 1.0–1.5 | 0.8–1.3 | n.r. | n.r. | n.r. | n.r. | n.r. | n.r. | W17-09 | C | Partial only. |
| **1050** (AA, not 1050A) | 0.25 | 0.40 | 0.05 | 0.05 | 0.05 | n.r. | 0.05 | 0.03 | n.r. | ≥ 99.50 | **1954** [W17-02 SX] | W17-02 | B | The tool flagged the extract as garbled. |
| **1050A** | 0.25 | 0.40 | n.r.* | n.r.* | n.r.* | n.r. | n.r.* | n.r.* | n.r. | Bal. (min n.r.) | n.r. | W17-18, W17-19 | C | *The extract gave Zn, Mg, Ti, Mn and Cu only as "≈0.05–0.07 each". Individual limits were not recoverable. |
| **1100A** | n.r. | n.r. | 0.05–0.20 | 0.05 | 0.10 | n.r. | n.r. | n.r. | n.r. | ≥ 99.00 | **2005** [W17-02 SX] | W17-02 | B | Retrieved instead of 1100. The extract's mapping of Mn and Mg is uncertain. |

**Not retrieved from the web:** 1070A, 1100, 1200, 3003, 3005, 3105, 3006, 3015, 3016, 8011, 8079, 8111. For the 3xxx rows this also means no registration dates.

### 2.2 Cross-reference: Drive-sourced limits already in chapter 05 (NOT web-verified)

These are reproduced here only so that §6 can compare windows. They come from Polmear Table 3.2 as recorded in chapter 05. They must be checked against the Teal Sheets.

| Alloy | Si | Fe | Cu | Mn | Mg | Cr | Zn | Ti | Al | Source |
|---|---|---|---|---|---|---|---|---|---|---|
| 3003 | 0.60 | 0.70 | 0.05–0.20 | 1.0–1.5 | — | — | 0.10 | — | — | [ch05 / P p.121] |
| 3004 | 0.30 | 0.70 | 0.25 | 1.0–1.5 | 0.8–1.3 | — | 0.25 | — | — | [ch05 / P p.121] |
| 3005 | 0.60 | 0.70 | 0.30 | 1.0–1.5 | 0.20–0.6 | 0.10 (Cr *or* Ti; column ambiguous) | 0.25 | | — | [ch05 / P p.121] |
| 3105 | 0.60 | 0.70 | 0.30 | 0.3–0.8 | 0.20–0.8 | 0.20 | 0.40 | 0.10 | — | [ch05 / P p.121] |
| 1200 | Si+Fe ≤ 1.0 | | 0.05 | 0.05 | — | — | 0.10 | 0.05 | ≥ 99.00 | [ch05 / P p.121] |
| 8011 | 0.50–0.9 | 0.6–1.0 | 0.10 | 0.10 | 0.05 | 0.05 | 0.10 | 0.08 | — | [ch05 / P p.121] |

The web-sourced 3004 Mn and Mg [W17-09] agree with the ch05 values.

### 2.3 Teal Sheets addenda check

The addenda since the 2018 edition [W17-03] list the following, per the extracts:
- 2079 (UK, Jan 2024);
- 5050D (EU, Jul 2025);
- 5081 (Russia, 2019);
- deactivation of 4007, 7064 and 7090 (2018).

None of these concerns a target alloy. The Dec 2022 addendum does not list 3104.

---

## 3. Designation crosswalk

| AA | EN AW number | EN chemical symbol (EN 573-2 style) | Former ISO 209 name | UNS | Other | Sources |
|---|---|---|---|---|---|---|
| 3102 | EN AW-3102 | AlMn0,2 | n.r. | **A93102** | — | W17-06, W17-12, W17-15, W17-21, W17-23 |
| 3207 | EN AW-3207 | AlMn0,6 | n.r. | n.r. | **Warning:** DIN Werkstoff-Nr **3.3207** is a *different* material (Fe 0.10–0.30, Cu ≤ 0.05, DIN 1725-1) [W17-25]. Do not equate it with AA 3207. | W17-07, W17-10, W17-21 |
| 3207A | EN AW-3207A | AlMn0,6(A) | n.r. | n.r. | — | W17-11 |
| 3103 | EN AW-3103 | AlMn1 | AlMn1 | n.r. | — | W17-08, W17-02 |
| 3003 | EN AW-3003 | AlMn1Cu | AlMn1Cu | n.r. | — | W17-09, W17-02 |
| 3004 | EN AW-3004 | AlMn1Mg1 | n.r. | n.r. | — | W17-09 |
| 3104 | EN AW-3104 | AlMn1Mg1Cu | n.r. | n.r. | — | W17-09 |
| 3005 | EN AW-3005 | AlMn1Mg0,5 | AlMn1Mg0.5 | n.r. | DIN 3.0525 | W17-09, W17-24, W17-02 |
| 3105 | EN AW-3105 | AlMn0,5Mg0,5 | AlMn0.5Mg0.5 | n.r. | — | W17-09, W17-02 |
| 1050A, 1070A, 1100, 1200, 8011, 8079, 8111 | n.r. | n.r. | n.r. | n.r. | — | — |

Notes:
- The "former ISO" column comes from the DOA / former-ISO columns of the 2018 Teal Sheets [W17-02 SX].
- ISO 209:2007 shows as withdrawn in the extract [W17-26].
- The current EN 573-3 edition seen is **2019** [W17-22]. The SteelNumber values are from **EN 573-3:2009**, and differences between the editions were not checked.

---

## 4. Mechanical and physical properties

### 4.1 EN 485-2 (sheet/strip) limits retrieved

| Alloy-temper | Thickness range as stated by source | Rm (MPa) | Rp0.2 (MPa) | A (%) | HB | Standard cited | Sources | Notes |
|---|---|---|---|---|---|---|---|---|
| 3103-H14 | 0.2–6.0 mm (datasheet scope) | 140–180 | ≥ 120 | n.r. | 45 | BS EN 485-2:2008 | W17-16, W17-17 | W17-20 gives a yield of **130 MPa**. That is probably a typical value, not the EN minimum. |
| 1050A-H14 | 0.2–6.0 mm (datasheet scope) | 105–145 | ≥ 85 | ≥ 12 (**band not identified**) | 34 | BS EN 485-2:2008 | W17-18, W17-19 | EN 485-2 gives elongation by thickness band. The extract does not show which band the 12 % belongs to, so verify. |

**Not retrieved:**
- O/H111, H12, H16, H18, H19 and H2x for every alloy;
- every temper of 1070A, 3003, 3005 and 3105;
- whether **3102 or 3207 are listed in EN 485-2 at all**.

The "0.2–6.0 mm" range is the datasheet's product scope. It is not necessarily a single EN 485-2 thickness band.

### 4.2 Physical properties

| Alloy | Density (g/cm³) | Melting | Thermal conductivity (W/m·K) | Electrical | E (GPa) | CTE (10⁻⁶/K) | Sources |
|---|---|---|---|---|---|---|---|
| 1050A | 2.71 | 650 °C (single value; range n.r.) | 222 | resistivity 0.0282 µΩ·m ≈ 35.5 MS/m ≈ 61 % IACS *(recalc.)* | 71 | 24 | W17-18 ("generic" values) |
| 3103 | 2.73 | n.r. | n.r. | n.r. | n.r. | n.r. | W17-08 (also gives a max. working temperature of 250 °C) |
| 3207 | 2.71 (0.098 lb/in³) | n.r. | n.r. | n.r. | n.r. | n.r. | W17-01 density table (SX) |
| 3207A | 2.72 | n.r. | n.r. | n.r. | n.r. | n.r. | W17-01 density table (SX) |

---

## 5. Impact-extrusion slug datasheets

**Nothing was retrieved.** The search budget ran out before any slug-producer datasheet was found. No slug alloy, temper, HB range or grain-size value from a producer is available in this file. See §8 for the follow-up.

---

## 6. Composition window comparison (item 4)

### 6.1 Is Mg allowed in 3102?

**Not as a specified element.** No 3102 row retrieved shows a Mg limit:
- Teal Sheets [W17-02];
- ASTM B210 [W17-05];
- EN 573-3:2009 via SteelNumber [W17-06];
- the EN 573-3 quotation in EP 2881477 B1 [W17-13].

The Teal extract explicitly reports the Mg cell as blank, with others ≤ 0.05 each and ≤ 0.15 total [W17-02 SX].

Under the AA/EN convention, an element with no specific limit counts as an "other". Mg in 3102 would then be capped at **0.05 %**, and it would also count towards the 0.15 % total. *(The convention is general knowledge of the AA/ANSI H35.1 practice. Its footnote text was not retrieved in this session, so verify it in the Teal Sheets footnotes or EN 573-3.)*

Two in-house items do not match this:
- The "Spec" column of `3102_RX_simulation` [09 §10] lists a Mg maximum that appears in no registered source retrieved here.
- The same column gives an Al minimum, but the registered rows give Al as "Rem.".

The Mg level used as model input for 3102 [09 §10] is above the 0.05 others-each cap. It is also above the 3207 Mg max (0.10). Among the windows retrieved, it lies only within 3207A (≤ 0.40) and the 3005/3105 Mg windows [ch05].

### 6.2 What distinguishes 3207 from 3102

| Element | 3102 [W17-02/05/06] | 3207 [W17-01/07/10] | Comment |
|---|---|---|---|
| Mn | 0.05–0.40 | **0.40–0.8** | The windows touch only at 0.40. 3207 is the higher-Mn alloy. |
| Mg | — (→ others ≤ 0.05, convention) | **≤ 0.10** (specified) | 3207 explicitly tolerates up to 0.10 Mg. |
| Cu | ≤ 0.10 | ≤ 0.10 | Same. |
| Fe | ≤ 0.7 | **≤ 0.45** | 3207 is tighter. |
| Si | ≤ 0.40 | **≤ 0.30** | 3207 is tighter. |
| Zn | ≤ 0.30 | **≤ 0.10** | 3207 is tighter. |
| Ti | ≤ 0.10 | n.r. | — |
| Registered | 1972 (registrant n.r.) | 1979, Germany | 3207A (1990, Germany) loosens 3207: Mg ≤ 0.40, Cu ≤ 0.25, Cr ≤ 0.20, Fe ≤ 0.6. |
| Food contact (secondary) | not listed [W17-06, W17-12] | listed [W17-07, W17-10] | Verify against EN 602. |

**In-house cross-checks (window statements only):**
- The 3207 model-input Mn, Cu, Fe and Si [09 §4.1] fall inside the 3207 window.
- Its Mg exceeds the 3207 maximum (0.10) but lies within 3207A (≤ 0.40).
- The CRM-table header note "3207 Mn ≤ 0.60" [09 §10] does not match the registered 3207 Mn window of 0.40–0.8.

### 6.3 Where a "modified 3102" with Mn ≈ 1.1–1.3 falls

**Mn windows (wt %):**
- 3102: 0.05–0.40 (A)
- 3207A: 0.30–0.8 (B)
- 3105: 0.3–0.8 (ch05)
- 3207: 0.40–0.8 (A)
- 3104: 0.8–1.4 (B)
- 3103: 0.9–1.5 (A)
- 3003, 3004 and 3005: 1.0–1.5 (ch05; 3004 also W17-09)

A Mn range of 1.1–1.3 therefore lies **outside 3102, 3207, 3207A and 3105**. It lies **inside 3103, 3003, 3004, 3005 and 3104**.

The other element windows of the "modified 3102" recorded in [09 §1/§10] (not restated here) narrow this down:
- **Mg:**
  - excludes 3003 (no specific Mg limit, so others ≤ 0.05 by convention);
  - excludes 3004 and 3104 (Mg ≥ 0.8);
  - lies **entirely inside 3005** (0.20–0.6, ch05);
  - **straddles the 3103 Mg maximum** (0.30): only its lower part fits 3103.
- **Cu:** inside 3003 (0.05–0.20), 3103 (≤ 0.10) and 3005 (≤ 0.30, ch05).
- **Zn:** the upper end exceeds 3003 (≤ 0.10, ch05). It is inside 3103 (≤ 0.20) and 3005 (≤ 0.25, ch05).
- **Si, Fe, Ti, others:** inside the 3103 and 3005 windows.

**Result:** the window is a **3005-type** composition. On the limits available it falls wholly within 3005, but the 3005 limits are Drive-sourced (Polmear) and were not web-verified. Its lower-Mg portion also falls within **3103**. It is not a 3102, 3207 or 3003 composition. This matches the chapter 09 assessment ("lean 3005/3103 variant").

---

## 7. Discrepancies found

| # | Item | Values | Sources | Status |
|---|---|---|---|---|
| D1 | 3207A Zn max | 0.25 vs 0.20 | W17-01 vs W17-11 | Prefer Teal (primary); verify. |
| D2 | 3102 Al minimum | "≥ 97.8" vs "≥ 97.85" vs in-house "≥ 99.0" | W17-14, W17-15, 09 §10 | The registered value is "Rem.". The web figures are derived from 100 − Σmax. |
| D3 | 3102 Mg | no limit (others ≤ 0.05) vs an in-house spec maximum | W17-02/05/06/13 vs 09 §10 | The in-house spec deviates from the registered limits. |
| D4 | 3207 Mn | 0.40–0.8 vs in-house "≤ 0.60" | W17-01/07/10 vs 09 §10 | Correct the in-house header. |
| D5 | 3103-H14 yield | ≥ 120 (EN min) vs 130 | W17-16 vs W17-20 | Likely min vs typical. |
| D6 | DIN 3.3207 vs AA 3207 | different materials | W17-25 | Naming trap. |
| D7 | 1050A-H14 elongation | 12 % with no thickness band | W17-18 | Verify against EN 485-2. |

---

## 8. Open questions / not verified

1. **No primary document was read in full.** All Teal Sheets values are search-index extracts, and some are query-matched. The fastest fix is to open the Teal Sheets PDF (W17-01) or the free Matplus Teal Sheets database (W17-04). That needs aluminum.org or teal-sheets.matplus.eu to be reachable from this environment, or a manual download by the user.
2. **The "others" convention** (blank cell means the element counts under others each/total) has to be confirmed from the Teal Sheets footnotes or EN 573-3. §6.1 depends on it.
3. **3102 registrant country** was not retrieved. The 3102 registration year of 1972 is from a garbled extract.
4. **3207 Ti and Cr cells** and the **3104 Zn/Ga/V/Ti cells** were not retrieved.
5. **Rows not retrieved at all:** 1070A, 1100, 1200, 3003, 3005, 3105, 3006/3015/3016, 8011, 8079 and 8111.
6. **EN 485-2 tables** (O/H111 to H19, H2x, all thickness bands) for 1050A, 1070A, 3003, 3103, 3005 and 3105 were not retrieved. Whether 3102 and 3207 appear in EN 485-2 is unknown. The current EN 485-2 edition was not checked; the suppliers cite 2008.
7. **EN 573-3:2019 vs 2009:** changes to any target row were not checked.
8. **Food-contact status** (3102 not listed, 3207 listed) is from secondary sources only. Verify against EN 602. This matters if slugs go to food, cosmetic or pharma packaging.
9. **Slug-producer datasheets** (alloy, temper, HB, grain size): none retrieved. A follow-up search is needed for published impact-extrusion slug datasheets from slug producers and rolling mills.
10. **Melting range and conductivity** for the 3xxx alloys were not retrieved. Only 1050A has generic physical data.
11. **Session limit:** the web-search budget for this turn was exhausted. A follow-up session (or a higher `CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION`) is needed to complete items 3–10.
