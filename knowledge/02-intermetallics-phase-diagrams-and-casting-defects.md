# 02 — Fe/Mn/Si intermetallics, phase diagrams and casting defects (DC & roll casting)

**Scope.** Al–Fe–Si, Al–Fe–Mn, Al–Mn–Si and Al–Fe–Mn–Si phase equilibria in the Al corner; stable and metastable Fe-bearing phases and how cooling rate, Fe:Si, Mn:Fe and trace elements select them; fir-tree zone (FTZ); twin-roll / continuous roll casting (TRC/CRC); centreline macrosegregation; hot and cold cracking; blistering, hydrogen and inclusion defects. The focus is wrought 1xxx/3xxx/8xxx foil and heat-exchanger alloys (AA3102, AA3207, 8006/8011/8111), with links to 5xxx and 6xxx.
**Conventions.** Compositions are in wt.% (mass %) unless marked at.%. A citation reads [Ref, p.X], with page numbers as printed in the source (thesis or book pagination). "(general knowledge)" marks statements that do not come from the sources. "(derived)" marks arithmetic done on source numbers. "(garbled)" marks values reconstructed from corrupted text extraction. Check these against the original PDF before relying on them.

## 0. Sources

| Ref | Title (author, year) | Drive link | Lang. | Readability / coverage |
|---|---|---|---|---|
| R1 | Belov, Eskin, Aksenov, *Multicomponent Phase Diagrams: Applications for Commercial Al Alloys* (2005), Ch. 1 "Alloys of the Al–Fe–Mn–Si System", pp. 1–46 | https://drive.google.com/file/d/1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD/view | EN | Text good. Figures are not readable. Read fully. **Full-text pass 2026-10-12:** the PDF was downloaded (2,668,517 B, 46 pp., OCR text layer; PDF page = printed page) and converted with `pdftotext -layout`. Tables 1.4, 1.6, 1.7, 1.9–1.15 and 1.17–1.20 are now legible and verified (§2.2, §2.4, §2.5). Tables 1.2 (Al–Fe–Si invariants, p.3), 1.5 (metastable phases, p.9) and 1.16 (Al–Fe–Mn–Si mono/bivariant, p.18) are printed rotated and their OCR layer is garbage, so they are **still missing** (no OCR tool available). |
| R2 | Rosefort, Matthies, Buck, Koch (TRIMET), "Determination of α- and β-AlFeSi phases in wrought Al alloys" (file name SL: "AlFeSi faze v gnetnih zlitinah") | https://drive.google.com/file/d/10S5-K7dD0IZZXepBfMi_hk0S8Rxzra5C/view | EN (one DE caption) | Text good, 7 pp. Tables 1–3, the alloy compositions and the numeric Si/(Fe+Mn) separator are in images and **not extracted**. Read fully. |
| R3 | Ghosh G., "Al–Fe–Si", Landolt-Börnstein New Series IV/11A2 (MSIT), pp. 359–409 (file name SL: "Fazni diagram AlFeSi") | https://drive.google.com/file/d/1ziJfaBKy6slqy6sR6DSdjzImN8UZ4SJz/view | EN | Text and tables good. Greek letters are encoded ("J"=τ, `"`=α, `$`=β, `(`=γ). Figures are not readable. Read fully. |
| R4 | Krstić Vukelja, Duplančić, Lela, "Continuous roll casting of Al alloys – casting parameters analysis", *Metalurgija* 49 (2010) 115–118 | https://drive.google.com/file/d/16xRFXhETDI8_5cYr9x9tuBxUueKkY9q0/view | EN (+HR abstract) | Text good. The paper covers process parameters only: no microstructure, cooling-rate or segregation data. Read fully. **2026-10-12:** PDF downloaded (482,542 B, 4 pp.); `pdftotext -layout` recovers Table 1 with its column assignment (§4.2). |
| R5 | Maggs S.J., *Intermetallic Phase Selection in Dilute Al–Fe–Si Alloys*, PhD thesis, Univ. Leeds (1996) ("fir-tree zone.pdf", 22 MB) | https://drive.google.com/file/d/1Dtgr_aj458cP3-2WGafeXu7LKDYNklva/view | EN | Scanned and OCR'd. **The text stops at thesis p. 71** (Chs 1–3). The DSC and Bridgman chapters (4–5) and the conclusions (6) are **not available**. Many phase names are garbled. 2026-10-12: at 22.34 MB the file is above the download-tool limit (see the note below the table), so it is still truncated. |
| R6 | Miyazaki, Isobe, Murao, "Formation mechanism and modeling of centerline segregation", *Nippon Steel Tech. Rep.* 104 (2013) 48–53 | https://drive.google.com/file/d/1QsCpR-VkKpP5rtYTqd7QB7P5IAUzFJPg/view | EN | Text good. The subject is **steel** CC slabs and blooms; only the mechanisms transfer. Eq. (1) is missing. Read fully. |
| R7 | Lalpoor M., *Study of Cold Cracking during DC-Casting of High-Strength Al Alloys*, PhD thesis, TU Delft / M2i (2010) (catalogue S-007). Subject: AA7050 and AA7475 DC-cast round billets (Ø 200–400 mm), plus one undisclosed "newly developed" 7xxx alloy | Whole file: https://drive.google.com/file/d/1gLPBgQq0_DICNYuWwMELjPhplKi3aBIo/view. Split parts in Drive folder "Cloud part book": aa (front matter, pp. 1–30) https://drive.google.com/file/d/1FFgfcyuB32-gT2WemtEA16x3-zjGRqrd/view; bb (pp. 31–70) https://drive.google.com/file/d/1FuOX-Ry_o5Q5Q5-1QECzW3EDFKhK2I78/view; cc (pp. 71–110) https://drive.google.com/file/d/1ryKcdWC8xlfHsfg2Y_-9mRs8EE3dwlB2/view; dd (pp. 110–148 + CV) https://drive.google.com/file/d/1UEW9pzBQSF2iYBlMnerlZKpMZkN9u6lZ/view | EN | **Full text 2026-10-12** (Chs 1–8, Conclusions, Summary). Parts aa, cc and dd were downloaded and converted with `pdftotext -layout`; Symbol-font Greek letters were remapped, so the equations read. Part bb (pp. 31–70) failed to download and is available only as Drive's text rendering: prose is clean, but figures are dropped, tables are flattened and there are no page breaks, so pages are located by the bare page numbers in the text. Values that exist only in figures (e.g. K_IC at 100 °C, Fig. 2.23; critical-crack-size curves, Figs. 6.9, 7.6, 7.7) are not recoverable. The acknowledgments page (p. 149) is missing (non-technical). p. 110 appears in both cc and dd. Earlier passes read only to p. 70. Cited with **printed** page numbers. |
| R8 | O'Dette J.H., "Blister formation in rolled aluminum", *J. Metals / Trans. AIME*, July 1957, pp. 924–925 | https://drive.google.com/file/d/1ng77xl3C81ziOj-F_orl5D5ksh0ryrpZ/view | EN | **Full-text pass 2026-10-12:** the PDF was downloaded (625,299 B; the duplicate 1QtwlU4u3he2eroL4LrynS4Ov_TMfgGJo has the identical size). **The Drive file itself has only 2 pages** (pp.924–925, a 600-dpi scan with an OCR layer), so the earlier "2-page" result was not a reader truncation. The abstract and Table I are legible in the layout extraction and are now verified (§7). The continuation (p.926 onward, with the explanation of the ≥40 % cold-reduction route and the control methods) is **not in the Drive library**. Author: J.H. O'Dette, Aluminium Laboratories Ltd., Kingston, Ont.; TP 4460E, manuscript 13 Sept 1956. |
| R9 | Eskin D.G., *Physical Metallurgy of Direct Chill Casting of Al Alloys* (CRC 2008), Ch. 2 "Solidification of Al alloys", pp. 19–78 (file 62816_ch02) | https://drive.google.com/file/d/1MBeZaNbetcIq6Xjcoj2Y56AW9wZPwcb2/view | EN | Found by Drive search. Text good apart from interleaved figure labels. Read fully. |
| R10 | Eskin (2008) Ch. 3 "Solidification patterns and structure formation during DC casting", pp. 79–124 (62816_ch03) | https://drive.google.com/file/d/1t1R4f3IKhRkid18JooQCMoR5PNhbjsZE/view | EN | Found by Drive search. Read fully. Table 3.2 is partly scrambled. |
| R11 | Eskin (2008) Ch. 4 "Macrosegregation", pp. 125–182 (62816_ch04) | https://drive.google.com/file/d/1LGAwTkLvuT29WFaaXDgYcKRN31PhMQ7v/view | EN | Found by Drive search. Read fully. |
| R12 | Eskin (2008) Ch. 5 "Hot tearing", pp. 183–274 (62816_ch05) | https://drive.google.com/file/d/1tYAv85fpfmJ7f5wNBPi3kvky3b1H4ps4/view | EN | Found by Drive search. Read fully. Most criterion equations are images and **missing**. |
| R13 | Davis J.R., "Aluminum and Aluminum Alloys", in *Alloying: Understanding the Basics*, ASM (2001), pp. 351–416 | https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view | EN | Found by Drive search. First pass read only the passages that matched Fe/Mn/Si/H keywords. **2026-10-12:** PDF downloaded (536,308 B, 66 pp. = pp.351–416) and read in full; the additions are in §7 (hydrogen sources). |
| TOT | Totten & MacKenzie (eds.), *Handbook of Aluminum, Vol. 1: Physical Metallurgy and Processes*, Marcel Dekker 2003, ISBN 0-8247-0494-0 (catalogue S-029). Read: Ch. 12 *Castings* (Colás, Velasco, Valtierra), pp. 591–642; Ch. 13 *Molten Metal Processing* (Otsuka), pp. 643–694; Ch. 9 *Aluminum Welding* (Cross, Olson, Liu), §§3–5, pp. 485–507; Ch. 3 (Tiryakioğlu & Staley), §2.2.1–2.2.2 and §2.4.1 Al–Fe–Si / §2.4.4 Al–Mn, pp. 118–120, 138–140, 159–160; Ch. 2 §6 hydrogen solubility, pp. 73–75; Ch. 7 *Rolling*, pp. 352–355 | Drive folder "Cloud part book": part 1 https://drive.google.com/file/d/1Yxag4tVsKp2w7GaNvUqpz09wJRuCpLVT/view (pp. 1–388); part 2 https://drive.google.com/file/d/1EwIKZG891qUZJJfloJCpHAP2hJmgXhZE/view (pp. 388–788) | EN | **Full text, 2026-10-12.** Born-digital PDF; the broken font maps were rebuilt before text extraction. Cited as [TOT p.X] with **printed** page numbers. Figures are not readable (e.g. Ch. 9 Figs. 11–12 hot-cracking peaks, Ch. 12 Figs. 18–19 Fe-phase micrographs). Most of the Fe-phase rules in Ch. 12 are for Al–Si **foundry** alloys (5–12% Si); transfer to lean wrought alloys is marked as inference. |

**Not used.** Duplicate copies in folder `1gxFIC8S…`, and everything inside `microstructure-sim-v2.14.0` (the `.js` files and the AA3207_Recrystallization_Simulation `.xlsx`, excluded as instructed). The broad handbooks (ASM Handbook vol. 1, "Alminium.pdf", "Light Alloys", "Alloys", TMS 2018 proceedings, "vasevska.pdf") also matched the search terms but were not mined. AMAG "AR-2014 Wärmebehandlung" was checked by snippet only (general heat treatment). Eskin Ch. 1 and the front matter were not read.

**Full-text pass (2026-10-12).** The Drive text reader truncates long files, so sources under 10 MB were downloaded whole and converted locally (`pdftotext -layout`): R1, R4, R8 and R13. The Drive download tool refuses larger files with the message *"File too large for download, over limit of 10 MB. For downloading larger files, use the standard Google Drive API."* (tested on a 12.66 MB file). R5 (22.34 MB) therefore remains truncated. R7 (13.88 MB) became available later on 2026-10-12 as four split parts (§0 row R7) and was read in full; its additions are in §6.1, §6.2 and the new §6.6, and the related gaps in §10 are closed. No OCR tool is available, so tables printed as images or rotated pages remain unreadable. **TOT** (Totten & MacKenzie, S-029) became available as split PDFs on 2026-10-12 and was read in full for the sections listed above. Its additions are §2.4, §2.6, §3.7, §4.3, §5.2, §6.5, §7.4–7.5, §8, §9 and §10, with notes on the user's rotary strip caster and trial alloy T11 marked **Relevance**.

---

## 1. Phase nomenclature crosswalk (read first: labels conflict between sources)

| Common name | Formula variants | wt.% (nominal) | Crystal | Notes |
|---|---|---|---|---|
| Al3Fe | Al13Fe4, Fe4Al13, FeAl3, Fe2Al7 | ~37–40 Fe (Fe4Al13 = 39.2 Fe, 0.8 Si in R3 Table 4) | monoclinic C2/m, a≈1.549, b≈0.808, c≈1.247 nm, β≈107.7° | Equilibrium. Dissolves Si from <0.2 up to ~6% [R1, p.1; R3, p.360, 388]. Melts congruently at 1152 °C [R3, p.359] |
| Al6Fe | FeAl6 | — | orthorhombic | Metastable [R5, p.8; R13, p.388]; dissolves <0.5% Si [R5, p.8–9] |
| AlmFe | m≈4–4.4 | — | body-centred tetragonal, a=0.884, c=2.106 nm | Metastable, heavily faulted; up to 3% Si [R5, p.6, 8–9]. R10 writes "AlmFe (Al9Fe2)" [R10, p.116], whereas R5 lists Al9Fe2 as a separate monoclinic phase [R5, p.6, 9] → conflict |
| AlxFe | x≈5–5.8 (R10: "Al5Fe") | — | monoclinic (Clyne & Young) or orthorhombic (Skjerpe), disputed | Metastable, appears at intermediate cooling rates [R5, p.9; R10, p.116] |
| α-AlFeSi (hexagonal, αh) | Al8Fe2Si = Al12Fe3Si2 = Al7.4Fe2Si = τ5 = Fe2Al7.4Si | 31.6 Fe, 7.8 Si; range 30–33 Fe, 6–12 Si | hexagonal P63/mmc, a=1.23–1.24, c=2.62–2.63 nm, ρ=3.58 g/cm³ | Equilibrium [R1, p.1; R3, p.361, 391]. "Crystallises only in high-purity alloys" [R2, p.2] |
| α-AlFeSi (cubic, αc) | Al12Fe3Si, Fe5Al20Si2, α(AlFeMnSi) | 27–35 Fe, 4–8 Si (R9 Table 2.2) | cubic (bcc or primitive), a≈1.25–1.256 nm | Metastable in ternary Al–Fe–Si. Stabilised by ≥~0.3% dissolved Mn or Cu [R3, p.361–362] and by Mn, Cr, Mo, V, W, Cu [R5, p.11] |
| α-Al(Fe,Mn)Si | Al15(Fe,Mn)3Si2, Al12(Fe,Mn)3Si, Al16(FeMn)4Si3 (Zakharov) | Mn end: 26.3 Mn, 8.9 Si; Fe end: 31 Fe, 1.5 Mn, 8 Si | cubic Pm3, 138 atoms, a=1.265 (0% Fe) → 1.25 nm (31.1% Fe) | Equilibrium in Al–Fe–Mn–Si [R1, p.12–19] |
| β-AlFeSi | Al5FeSi = Al9Fe2Si2 = FeAl4.5Si = τ6 | 25.6 Fe, 12.8 Si; range 25–30 Fe, 12–15 Si | monoclinic a=b=0.612, c=4.148–4.150 nm, β=91° (orthorhombic by CBED) | HV 5.8 GPa, ρ 3.3–3.6 [R1, p.1; R3, p.362] |
| δ-AlFeSi | Al4FeSi2 = FeAl3Si2 = τ4 | 25.4 Fe, 25.5 Si | tetragonal PdGa5, a=0.607–0.63, c=0.941–0.953 nm | Si-rich, non-equilibrium in commercial alloys [R1, p.2] |
| γ-AlFeSi | Al3FeSi, τ2 Fe2Al5Si2 | 33.9 Fe, 16.9 Si | monoclinic, a=1.78, b=1.025, c=0.890 nm, β=132° | [R1, p.2; R3, p.361, 389] |

**Pitfalls in naming**
- R9 p.43 labels the phases "α(Al5FeSi), β(Al8Fe2Si)", which inverts the usual convention used in R1, R3 and R2 (α = Al8Fe2Si, β = Al5FeSi) [R9, p.43 vs R1, p.1].
- R13 uses "cubic αAl12Fe3Si / monoclinic β-Al9Fe2Si2" [R13, p.388], i.e. it names the cubic Mn/Cu-stabilised α.
- Identifying a phase from its morphology alone is error-prone. The same phase can be primary, peritectic or eutectic and look different in each case [R1, p.6; R9, p.43; R2, p.1]. EBSD or EDX ratios are needed (§3.5).

---

## 2. Phase equilibria in the Al corner

### 2.1 Al–Fe–Si: mechanisms
- The phases in equilibrium with (Al) are (Si), Al3Fe, Al8Fe2Si (α) and Al5FeSi (β) [R1, p.1]. The ternary phases exist in the solid state mostly outside their primary fields, so many peritectics must go to completion before equilibrium is reached. Real castings therefore show Al3Fe, Al6Fe, α, β and δ **together** [R1, p.6; R9, p.43].
- Lowering the Al-rich liquidus and solidus is mainly an effect of Si; the effect of Fe is much smaller [R1, p.4]. The solid solubility of Fe in (Al) is ≤0.05% [R1, p.2], 0.052% [R3, p.366] or 0.04% [R5, p.7]. In the (Al)+Al3Fe field much less Si dissolves in (Al) than in the (Al)+(Si)+β field [R1, p.2].
- The equilibrium and as-cast phase distributions differ. At ~10⁻¹ K/s the field map contains 4- and 5-phase regions (Phillips). At ~10 K/s (chill) Al8Fe2Si and (Si) are present while Al3Fe and Al5FeSi are absent at 2–3% Fe and 2–3% Si, because L→(Al)+Al3Fe needs a larger undercooling than L→(Al)+Al8Fe2Si [R1, p.6–8].
- Langsrud: as the cooling rate Vc rises, the primary Al3Fe, Al8Fe2Si and Al5FeSi fields drift to lower Si, so Al3Fe becomes less likely at high Vc [R1, p.6].
- Under slow solidification of alloys with >0.5% Fe, the sequence of phase regions with rising Si is: Al3Fe → Al3Fe+α → Al3Fe+α+β → Al3Fe+α+β+(Si) → α+β+(Si) → β+(Si) [R1, p.7].
- For most alloys the non-equilibrium solidus is 576 °C (L→(Al)+(Si)+Al5FeSi) [R1, p.6; R9, p.45].

### 2.2 Al–Fe–Si: quantitative data

**Invariant reactions involving (Al)** (CALPHAD set of Liu & Chang as accepted by MSIT) [R3, p.396–397]

| Reaction | Type | T (°C) | Liquid Fe / Si | (Al) Fe / Si |
|---|---|---|---|---|
| L + Fe4Al13 → (Al) + τ5(α, Al8Fe2Si) | U10 | 632 | 2.0 / 4.2 | 0.05 / 0.64 |
| L + τ5(α) → (Al) + τ6(β, Al5FeSi) | U11 | 613 | 1.8 / 6.2 | 0.04 / 1.0 |
| L + τ4(δ) → τ6(β) + (Si) | U12 | 600 | 1.5 / 14.3 | — |
| L → τ6(β) + (Al) + (Si) | E1 | 573 | 0.5 / 11.7 | 0.01 / 1.65 |
| L + τ4 + τ5 → τ6 | P6 | 700 | 7.2 / 14.0 | — |
| L → (Al) + Fe4Al13 (binary) | e11 | 655 | — | — |
| L → (Al) + (Si) (binary) | e12 | 577 | — | — |

The binary e11 and e12 temperatures are taken from the labels on R3 Fig. 6 (liquidus surface).

**Monovariant eutectics (Phillips, as used in R1)** [R1, p.4]: L→(Al)+Al3Fe 655–629 °C; L→(Al)+Al8Fe2Si 629–611 °C; L→(Al)+Al5FeSi 611–576 °C; L→(Al)+(Si) 577–576 °C.
**Pitfall:** the two data sets disagree by 2–3 °C (629/611/576 in Phillips vs 632/613/573 in CALPHAD). Use one set consistently.

**Other Al–Fe–Si equilibria data**
- Fe4Al13 dissolves 0.2–6 mass% Si (scatter between reports; 4 at.% Si at 550 °C). The lattice parameters vary with composition: a(pm) = 1505.0 + 1.14·W_Fe − 0.41·W_Si and b(pm) = 862.8 − 1.41·W_Fe − 1.3·W_Si [R3, p.360].
- Fe and Si solubility in (Al) at 550 °C is each <1 at.% [R3, p.360].
- **Limit solid solubility of Fe and Si in (Al) in the three-phase fields** (Drits et al. 1977) [R1, p.6, Table 1.4; verified against the PDF 2026-10-12]:

| T (°C) | (Al)+Al3Fe+α: Fe / Si | (Al)+α+β: Fe / Si | (Al)+β+(Si): Fe / Si |
|---|---|---|---|
| 629 | 0.052 / 0.64 | — | — |
| 611 | — | 0.04 / 0.82 | — |
| 600 | 0.033 / 0.4 | 0.033 / 0.82 | — |
| 578 | — | — | 0.01 / 1.65 |
| 550 | 0.016 / 0.2 | 0.016 / 0.42 | 0.008 / 1.3 |
| 500 | 0.009 / 0.11 | 0.008 / 0.22 | 0.005 / 0.8 |
| 450 | 0.004 / 0.06 | 0.004 / 0.11 | 0.003 / 0.44 |
| 400 | 0.002 / 0.03 | 0.002 / 0.06 | 0.002 / 0.30 |

  - In the (Al)+β+(Si) field the Si solubility follows the binary Al–Si solvus. The 629 °C (Al)+Al3Fe+α point (0.052 Fe, 0.64 Si) matches the U10 composition of R3 (0.05 Fe, 0.64 Si at 632 °C).
  - **Corrected after full-text pass:** the earlier text gave Fe in the (Al)+β+(Si) field as "≈0.016 → 0.002 %". The value 0.016 % at 550 °C belongs to the other two fields; in the (Al)+β+(Si) field Fe is 0.008 % at 550 °C and 0.01 % at 578 °C.
  - (derived) Between 400 and 550 °C Fe solubility in (Al) is only 0.002–0.016 %. At any anneal in this range (which includes the 3xxx soft-anneal window of 380–420 °C in ch. 03 §4.3), practically all Fe in 1xxx/3xxx is present as constituent particles, the potential PSN sites, rather than in solution.
- Al8Fe2Si ↔ Fe/Si ratio ≈ 4.05 and Al5FeSi ↔ 2.0 (mass, derived from R1 compositions). In homogenised 6063, measured α2 had Fe/Si 2.75–5.5 (~3 µm particles) and β had 1.6–2.25 (~8 µm). Particles between 2.25 and 2.75 were "indeterminate" [R3, p.362, 383].

**Effect of cooling rate on the 1050 solidification path** (0.37 Fe, 0.05 Si; Bäckerud) [R1, p.31; R9, p.46]

| Reaction | 0.4 K/s | 1.2 K/s | 18 K/s |
|---|---|---|---|
| L → (Al) | 659 °C | 659 | 659 |
| L → (Al) + Al3Fe | 650 | 649 | 647 |
| L + Al3Fe → (Al) + Al8Fe2Si | — | 642–638 | 630 |
| Solidus | 642 | 638 | 630 |

- Metastable Al6Fe can form in 1050 cast at >1 K/s [R1, p.31; R9, p.46]. At low Cu and >8–10 K/s Al6Fe can form during solidification [R1, p.8].
- **Al–1.7Fe–Si:** the probability of Al3Fe first rises and then falls with increasing Vc. At high Vc, Al3Fe forms only when Fe:Si > 2 [R1, p.29].
- Cooling-rate regimes: Vc1 = 10⁻²–10⁻¹ K/s, where the equilibrium diagram predicts the onset of solidification well; Vc2 = 10⁰–10² K/s, which is relevant to DC casting [R9, p.44–45].
- Metastable phases can also **precipitate** during ingot homogenisation (α′, α″ modifications of Al8Fe2Si). They normally transform to the equilibrium phases at sufficiently high temperature. Because Fe solubility is so low, secondary Fe phases can never exceed 0.1–0.2 vol.% [R1, p.10; R9, p.46].

### 2.3 Metastable Al–Fe–Si phases (R9 Table 2.2; R3 Tables 1, 3)

| Phase | Composition | Structure, lattice (nm) | Source |
|---|---|---|---|
| α (cubic) | Al12.7–12.9Fe3Si1–1.5 (27–35 Fe, 4–8 Si) | primitive cubic or bcc, a=1.256 | [R9, p.45] |
| α′ | Al12–12.6Fe3Si1.6–2 | hexagonal, a=1.23, c=2.62 | [R9, p.45] |
| α″ (q1) | — | tetragonal or orthorhombic, a=1.26–1.3, c=3.70 | [R9, p.45]. Fe/Si 7–9 in DC CP-Al [R3, p.383] |
| β′ (β*) | Fe/Si ≈ 1 | monoclinic 0.89 / 0.49 / 4.16, 92° | [R9, p.45; R3, p.383] |
| αv | ~29 Fe, 5.5 Si | monoclinic 0.847–0.869 / 0.635 / 0.610–0.632, 93.4° | [R9, p.45; R3, p.384] |
| αT | Fe3Al13Si1–1.5 | C-centred monoclinic 2.81 / 3.08 / 2.08, 97.74° | [R3, p.384] |
| q2 | — | monoclinic 1.250 / 1.230 / 1.970, 111° | [R9, p.45] |
| αC in a 6xxx model alloy (0.3Fe–0.6Si–0.8Mg) | Al:Fe:Si 7:4:1 to 9:5:1 | cubic | Forms by L + Fe4Al13 → (Al) + αC or by L → (Al) + αC [R3, p.387] |

**Observed solid-state transformations**
- In commercial-purity Fe/Si = 2 alloys, q1 → q2 at 600 °C. In high-purity Fe/Si = 2 alloys, cubic α persists after long anneals at 600 °C [R3, p.384–385].
- αC decomposes to Fe4Al13 + Si, which then react to form αH (equilibrium) [R3, p.385].
- In Al–0.2Fe–0.55Mg–0.6Si, as-cast β → α′ on annealing at 580 °C for 1 h [R3, p.383].
- δ → β (Fe2Al9Si2) at 500 °C [R3, p.386].
- During heat treatment of as-cast alloys, Fe4Al13 + τ5 + (Si) react to form τ6, but incompletely [R3, p.366].

### 2.4 Al–Fe–Mn (8006, low-Si 3xxx)
- Only Al3Fe and Al6(Fe,Mn) are in equilibrium with (Al). Fe substitutes in Al6Mn up to Al12FeMn (12.85 Fe, 12.64 Mn). The maximum Mn in Al3Fe is Al3Fe0.88Mn0.12 (4–5% Mn). Al6(Fe,Mn) is orthorhombic, a=0.75518, b=0.64978, c=0.88703 nm [R1, p.10].
- **Ternary eutectic** L → (Al) + Al3Fe + Al6(Fe,Mn) at 654 °C, with liquid ≈0.75 Mn and 1.75 Fe (Mondolfo). Denholm reported ~0.43 Mn and ~1.7 Fe, with tie-triangle vertices Al3Fe (36.9 Fe, 4.6 Mn), Al6(FeMn) (19.6 Fe, 7.1 Mn) and (Al) (0.044 Fe, 0.23 Mn) [R1, p.11]. The higher-temperature invariant is **L + Al3Fe + Al4Mn → Al6(FeMn) at 727 °C, with liquid 3.45 Mn and 2.5 Fe** (Mondolfo; Ran) [R1, p.11, Table 1.7; legible after the 2026-10-12 full-text pass, previously garbled]. Table 1.7 labels the 727 °C reaction "E" and the 654 °C eutectic "P", which looks like an inversion of the usual point labels; the reaction equations are unambiguous.
- Monovariant reactions: L→(Al)+Al3Fe 655–654 °C; L→(Al)+Al6(FeMn) 658–654 °C [R1, p.12].

**Limiting solubility of Mn and Fe in (Al) in the three-phase field**, with the binary values in brackets [R1, p.12, Table 1.9]

| T (°C) | Mn | Fe |
|---|---|---|
| 654 | 0.23 (1.8) | 0.044 (0.05) |
| 627 | 0.13 (1.0) | — |
| 527 | 0.05 (0.42) | — |
| 427 | 0.026 (0.2) | — |

- **At Vc > ~10 K/s only Al6(Fe,Mn) is expected besides (Al).** Fe lowers the as-cast Mn supersaturation because part of the Mn is tied up in Al6(Fe,Mn) [R1, p.12].
- In 8006, primary Al3Fe and Al6(FeMn) (generally undesirable) can form at the upper Fe limit. Faster solidification shifts that boundary to higher Fe and Mn [R1, p.31].
- The non-equilibrium Mn in (Al) is set by cooling rate and composition, and it fixes the amount of dispersoid formed on annealing above **300–350 °C**. These dispersoids are mostly Al6Mn, not Al6(FeMn) [R1, p.31–32].
- In 8006 foil (0.6Mn, 1Fe, 0.1Si, 100 µm) the main phases are Al3(FeMn) and Al6(FeMn) [R1, p.38].
- **Additions from [TOT] (full-text pass 2026-10-12)** [TOT p.159–160]:
  - Binary Al–Al6Mn eutectic at about 1.9 wt% Mn and 657 °C. Up to 1.82 wt% Mn is soluble in (Al).
  - Commercial Al–Mn alloys usually stay below 1.25 wt% Mn because **Fe lowers the solubility of Mn** and so raises the chance of large primary Al6(Mn,Fe) particles, which harm ductility.
  - **A higher Fe/Mn ratio may promote Al13(Fe,Mn)4 in as-cast alloys** [TOT p.160]. This qualifies the R1 statement above that only Al6(Fe,Mn) is expected at > 10 K/s; R1 made that statement for the ternary Al–Fe–Mn system.

### 2.5 Al–Mn–Si (3xxx dispersoid chemistry)
- Al15Mn3Si2 (α(MnSi)) has a homogeneity range of 25–29 Mn and 8–13 Si. It is cubic Pm3 with a=1.265–1.268 nm (1.260 in another report), ρ=3.55 g/cm³ and microhardness 8.8 GPa. The solubility of Mn in it is 0.7–0.8% (as printed). Si dissolves only slightly in Al6Mn [R1, p.12–13].

**Invariant reactions** [R1, p.15, Table 1.11]

| Reaction | T (°C) | Liquid Mn / Si |
|---|---|---|
| L + Al4Mn → Al6Mn + Al10Mn3Si (P3) | 690 | 3.4–3.8 / 0.5–0.7 |
| L + Al10Mn3Si → Al6Mn + Al15Mn3Si2 (P2) | 655–657 | 2.7–2.8 / 1.3–1.6 |
| L + Al6Mn → (Al) + Al15Mn3Si2 (P1) | 648–649 | 2.5–2.8 / 1.5–1.7 |
| L → (Al) + (Si) + Al15Mn3Si2 (E) | 573–574 | 1.0–1.2 / ~12 |

Monovariant reactions: L→(Al)+Al6Mn 658–649 °C; L→(Al)+Al15Mn3Si2 649–574 °C [R1, p.15].

**Limit solubility of Mn and Si in (Al) in the three-phase fields** (Drits et al. 1977; Phillips 1959) [R1, p.15, Table 1.13; **verified against the PDF 2026-10-12**: the earlier reconstruction was correct in every cell]

| T (°C) | (Al)+Al6Mn+α: Mn / Si | (Al)+(Si)+α: Mn / Si |
|---|---|---|
| 649 | 1.3 / 0.1 | — |
| 600 | 0.73 / 0.09 | — |
| 573 | — | 0.08 / 1.66 |
| 550 | 0.44 / 0.08 | 0.07 / 1.36 |
| 500 | 0.25 / 0.08 | 0.06 / 0.85 |
| 450 | 0.15 / 0.08 | 0.05 / 0.45 |
| 400 | 0.06 / 0.08 | 0.04 / 0.25 |

Text check: in the Al6Mn+α field Mn solubility is close to the binary Al–Mn value and Si is very low; in the (Si)+α field Si is close to binary Al–Si and Mn is ≤0.1% [R1, p.13].
- (derived) **Annealing relevance.** Equilibrium Mn in (Al) is 0.25 % at 500 °C, 0.15 % at 450 °C and 0.06 % at 400 °C when the alloy sits in the Al6Mn+α field, and only 0.04–0.06 % when free (Si) is present. Any Mn retained in solution above these values (from fast casting or a short homogenisation) is supersaturated at a 400–500 °C anneal and can precipitate as dispersoids during that anneal. This is the concurrent-precipitation case of ch. 03 §5. The 3207 range (0.4–0.8 Mn) and the upper half of the 3102 range (0.05–0.4 Mn) exceed the 400–450 °C solubility.
- **Pitfall:** Mondolfo's 527 °C section shows 1% Mn in the (Al)+Al6Mn+α field, but the table gives ~0.4%. The calculated 550 °C section (Du et al. 2004) agrees with the table [R1, p.13].
- Under non-equilibrium solidification, Al4Mn and Al10Mn3Si appear at Mn > ~2.5% [R1, p.13]. As the cooling rate rises, Mn in (Al) can reach 1% in alloys with up to 4% Si [R1, p.13–15].
- **In Al–Mn alloys a non-equilibrium eutectic containing (Si) already appears at 0.2–0.3% Si** [R1, p.15].

### 2.6 Al–Fe–Mn–Si quaternary (3003/3102/3207/8006)
- Accepted version (Mondolfo, supported by Davignon et al. 1996, who studied 24 alloys after 12 weeks at 550 °C): there is no separate quaternary phase. Al15(Fe,Mn)3Si2 has a wide homogeneity range in which Fe replaces Mn up to 31 Fe, 1.5 Mn, 8 Si, and a falls from 1.265 to 1.25 nm. Zakharov proposed Al16(FeMn)4Si3, fcc a=1.252 nm [R1, p.16–19].

**Invariant reactions** [R1, p.17, Table 1.15]

| Reaction | T (°C) | Liquid Si / Fe / Mn |
|---|---|---|
| L + Al6(FeMn) + Al3Fe → (Al) + Al15(FeMn)3Si2 (P4) | 648 | 1.75 / 2.0 / 0.35 |
| L + Al3Fe → (Al) + Al8Fe2Si + Al15(FeMn)3Si2 (P3) | ~628 (estimate) | 3–5 / 2–2.5 / <0.2 |
| L + Al8Fe2Si → (Al) + Al5FeSi + Al15(FeMn)3Si2 (P2) | ~607 (estimate) | 5–10 / 1–2 / 0.1–0.5 |
| L + Al5FeSi → (Al) + (Si) + Al15(FeMn)3Si2 (P1) | 575 | 11.7 / 0.6 / 0.2 |

**3003 non-equilibrium solidification** (1.19 Mn, 0.55 Fe, 0.18 Si; Bäckerud) [R1, p.38; R9, p.47]

| Reaction | 0.5 K/s | 17 K/s |
|---|---|---|
| L → (Al) | 655 °C | 655 |
| L → (Al) + Al6(FeMn) | 653 | 646–615 |
| L + Al6(FeMn) → (Al) + Al15(FeMn)3Si2 and/or L → (Al) + Al15(FeMn)3Si2 | 641–634 | 589 |
| Solidus | **634** | **589** |

- In the as-cast state the amount of Al15(FeMn)3Si2 increases with Si. At 0.6% Si with low Fe, free (Si) can form and the solidus drops to 573 °C [R1, p.37; R9, p.47].
- Extruded 3003 tube (1.3Mn, 0.5Fe, 0.3Si) has Al15(FeMn)3Si2 as its main phase [R1, p.38].
- Once all Fe and Si are bound in Al15(FeMn)3Si2, dispersoid formation can be analysed with the Al–Mn–Si diagram [R1, p.37].
- Al15Mn3Si2 forms both during solidification and during annealing, as dispersoids [R1, p.32]. In commercial 3xxx ingots, eutectic Al6(Mn,Fe) and cubic Al12(Fe,Mn)Si form during solidification. The rest of the Mn stays in solution and precipitates during the ingot preheat as Al12(Mn,Fe)Si and Al6(Mn,Fe) dispersoids, which control the recrystallised grain size [R13, p.388–389].
- **[TOT] on 3xxx ingots** [TOT p.160]:
  - Typical as-cast 3003 ingot holds **0.7–0.9 wt% Mn in solution**. The rest is in Al–Mn–Fe and Al–Mn–Fe–Si constituents.
  - During homogenisation, Al12(Mn,Fe)3Si or Al6(Mn,Fe) dispersoids (< 1 µm) precipitate from the supersaturated matrix. **Below 0.07 wt% Si the dispersoid is usually Al6(Mn,Fe).**
  - Si accelerates Mn precipitation, giving a denser Al12(Mn,Fe)3Si dispersion and less Mn retained in solution. With enough Si, some or all of the as-cast Al6(Mn,Fe) transforms to Al12(Mn,Fe)3Si.
- **3003 can be single-phase** if Mn < 1% and Si < 0.1%. Mn microsegregation can then be removed by annealing above 540–550 °C. Higher Si puts the alloy in 1- or 2-excess-phase fields at the same temperature [R1, p.32–33].
- **Partial melting of Si-bearing 3xxx is possible ~60 °C below the solidus of binary Al–Mn** [R1, p.33–35]. Si lowers the Al–Mn solidus "dramatically, by 60 °C" [R9, p.46].
- 3009 (1.5 Mn) does not form Al6Mn, either during solidification or during annealing [R1, p.35].
- Mn binding of Fe, as known from 4xx.x castings: the peritectics are incomplete, so the Mn:Fe needed to suppress β needles is much higher than the equilibrium value of ~1:20 (from 1.5 Mn and 31 Fe in α). Fe+Mn > 2.0–2.5% gives primary polygonal α clusters [R1, p.43].
- For 10–14% Si alloys (Zakharov): Mn:Fe = 1:1 ends solidification at 576 °C; Mn:Fe < 1 at 574 °C, with Al5FeSi present; Mn:Fe > 1 at 575 °C, with Al15Mn3Si2 present [R1, p.19].

**Typical composition limits** [R1, p.10, Table 1.6]

| Alloy | Mn | Fe max | Si max | Other (max) |
|---|---|---|---|---|
| 3102 | 0.05–0.4 | 0.7 | 0.4 | Cu 0.1 |
| 3207 | 0.4–0.8 | 0.45 | 0.3 | Mg 0.1, Cu 0.1 |
| 8006 | 0.3–1.0 | 1.2–2.0 (range) | 0.4 | Mg 0.1, Cu 0.3 |

The "Other" column was read from the clean layout extraction of 2026-10-12 [R1, p.10, Table 1.6; same 3102/3207 rows in Table 1.10, p.13].

### 2.7 Design levers (phase diagrams)
- **Fe:Si > 1.** This keeps free (Si) out and avoids the low-melting L→(Al)+β+(Si) eutectic, which widens the freezing range and causes hot tearing [R1, p.29; R9, p.46; R12, p.208].
- **8111 / foil (1% Fe).**
  - With Si near the **lower** limit (~0.4%), only Al8Fe2Si forms. It spheroidises on annealing: globular after 550 °C / 10 h on twin-roll-cast strip [R1, p.23, 27].
  - With Si near the **upper** limit (0.8–1.1%), coarse (Si) persists into 6–14 µm foil and causes scratches and perforation. Needle Al3Fe and Al5FeSi do not spheroidise even after long anneals [R1, p.23, 27].
  - If Si is high, anneal at ≥500 °C to dissolve eutectic Si [R1, p.23]. At 620 °C only part of the 8111 range can be annealed without melting [R1, p.23].
- **3xxx homogenisation ceiling.** Set the maximum homogenisation temperature from the Si content, because Si can lower the effective solidus by up to ~60 °C [R1, p.33–35; R9, p.46]. Single-phase (Mn<1, Si<0.1) 3003 tolerates >540–550 °C [R1, p.33].
- **Primary intermetallics.** Keep Fe+Mn < ~2.0 (3003) and < ~1.7 (3004) to avoid primary (Fe,Mn)Al6 in the trough or sump [R13, p.383]. Faster solidification raises these limits, which matters for TRC [R1, p.31].
- **Fe consumes Mn.** Fe lowers the Mn supersaturation and hence the dispersoid potential; Si consumes Mn into α [R1, p.12, 19].
- **Corrosion.**
  - Al6(Mn,Fe) and Al12(Mn,Fe)3Si have solution potentials close to the matrix and are not initiation sites. Al6Fe, Al3Fe and Al12Fe3Si2 in 1xxx are cathodic [R13, p.399, 402].
  - Al–Fe–Si alloys with a lower Fe/Si ratio corrode less in industrial and marine environments [R3, p.368].
- **Mn modifies the shape of acicular or plate-like Fe constituents** and reduces their embrittling effect [R13, p.382].

### 2.8 Pitfalls (phase diagrams)
- Equilibrium sections overstate how far the peritectics go. Non-equilibrium analysis assumes suppressed peritectics and equilibrium eutectics (Belov method) [R3, p.368; R1, p.6].
- In 4xx.x, Mn-bearing α grows **on** β needles instead of nucleating separately, so equilibrium Mn:Fe targets do not apply [R1, p.43].
- Tables 1.4, 1.7 and 1.13 of R1 were verified against the PDF on 2026-10-12. Tables 1.2, 1.5 and 1.16 (rotated pages) are still unreadable; verify those against the printed book.

---

## 3. Cooling rate, metastable Fe phases and the fir-tree zone (DC 1xxx/5xxx)

### 3.1 Mechanisms
- **What the FTZ is.** After caustic etching or anodising, a vertical ingot section shows light and dark regions shaped like a fir tree. These give a patchy anodised or lithographic surface when scalping exposes the intermediate zone [R5, p.4–5].
- **Cause.** The binary Al–Fe eutectic phase changes with position in the ingot, because cooling rate and local solidification velocity vary [R5, p.5–6]. The defect is a *mixture* of competing stable and metastable phases formed under uneven sub-surface cooling, not merely the presence of metastable phases [R10, p.116].
- **Sequence with falling cooling rate:** AlmFe → Al6Fe → Al3Fe. AlxFe appears at intermediate rates, from near the upper limit of Al3Fe to just above the lower limit of Al6Fe [R5, p.6].
- **Nucleation versus growth.**
  - The cooling rate sets the nucleation temperature, and the local growth velocity sets the growth temperature [R5, p.12, 26–27].
  - Al3Fe needs a large undercooling to nucleate on α-Al. Al6Fe nucleates easily, via a low-energy, partially coherent interface [R5, p.12].
  - The Al–Al3Fe eutectic is "anomalous": faceted, with rigid spacing. Al–Al6Fe is "normal" and diffusion-controlled, so it can adjust its spacing and outgrow Al3Fe at high velocity [R5, p.13].
- **Grain refiner (TiB2).** Hexagonal TiB2 favours nucleation of the higher-symmetry phases (cubic α, tetragonal AlmFe) over orthorhombic Al6Fe and monoclinic Al3Fe. This extends the cooling-rate window of the favoured phase [R5, p.62–63].
- **Trace elements** at sub-0.05% levels can move transitions in two ways [R5, p.60–61]:
  1. by poisoning attachment sites on a faceted interface;
  2. by segregating to the interdendritic liquid, which raises the solutal undercooling.
- **Annealing.** 590 °C / 5 h removed the differential etching: Al6Fe and AlmFe transformed fully or partly to Al3Fe, while α″ and AlxFe remained. In that case the FTZ was caused by the Al6Fe vs AlmFe etch response [R5, p.16–17; R10, p.116–118].

### 3.2 Quantitative data

| Quantity | Value | Source |
|---|---|---|
| Al–Al3Fe eutectic | 655 °C, 1.8 Fe. Spacing λ^2.6·U = 3180 µm^3.6/s | [R5, p.7–8, 13] |
| Al–Al6Fe eutectic | 650 °C, 3.5 Fe. Spacing λ²·U = 10.2 µm³/s | [R5, p.8, 13] |
| Extrapolated eutectic growth T | 655.1±0.1 °C (Al3Fe), 652.9±0.2 °C (Al6Fe) | [R5, p.14] |
| Critical cooling rate Al3Fe → Al6Fe (hypoeutectic) | ≈2 °C/s (range 1–3.3). Al–1Fe ≤3.3 °C/s for Al3Fe. Al–2Fe 2.5 °C/s. Al–3.5Fe (hypereutectic) 11.6 °C/s | [R5, p.12–13] |
| Critical growth velocity Al3Fe → Al6Fe | 100 µm/s (2–6 Fe, G = 20 °C/mm). 110 µm/s (Al–3Fe) | [R5, p.13–14] |
| Al6Fe → AlmFe | >10 °C/s (Al–0.6Fe, wedge). 20 °C/s (unidirectional). >35 °C/s (Al–0.5Fe). Up to >500 °C/s in 4N Al–0.25/0.5Fe | [R5, p.14, 57–58] |
| AlxFe window | ~0.5–5 (or 6) K/s, Al–0.5Fe | [R5, p.15–16] |
| Miki, Al–0.6Fe | <1 °C/s Al3Fe; 1–10 °C/s Al6Fe; >10 °C/s AlmFe | [R5, p.16] |
| DC 1050 (Westengen, grain-refined, 100 mm/min) | 15 mm from edge, ~10 °C/s: α″ + AlmFe. 50 mm, ~5 °C/s: Al6Fe (+AlxFe). FTZ border ≈8 °C/s | [R5, p.16; R10, p.118 table] |
| R10 summary | AlmFe and α″ need ~20 K/s. At 2–5 K/s, AlxFe + Al6Fe + cubic α form | [R10, p.116] |
| Commercial DC cooling rates | 1 to 10–20 °C/s. 200-mm billet: centre 3–5 K/s, periphery 15–20 K/s | [R5, p.59; R10, p.113] |
| Maggs DC simulator | 16 °C/s at 20 mm, 3 °C/s at 50 mm, 0.7 °C/s at 100 mm from chill | [R5, p.59] |
| Fe partition coefficient | k = 0.027 [R5, p.6]; K_Fe = 0.03 [R11, p.172] | |
| Westengen/Skjerpe ingot (0.25Fe, 0.13Si, 600×1350 mm) | As-cast surface: α(+), α″(+++), AlmFe(+++). Inner: Al6Fe(+++), AlxFe(+++), Al3Fe(+), β′(+), Si(+). After 590 °C / 5 h, surface: Al3Fe(+++), α″(+++), AlmFe(+) | [R10, p.118] (table partly garbled) |

**Maggs DC-simulator phase sequences** (99.999% Al base; from high to low cooling rate) [R5, p.53]

| Alloy | Fe / Si (Fe:Si) | Sequence | Visible FTZ |
|---|---|---|---|
| A1 | 0.2 / 0.1 (2) | cubic α → AlxFe → Al3Fe | double: α/AlxFe and AlxFe/Al3Fe |
| A2 | 0.4 / 0.1 (4) | Al6Fe → Al3Fe | Al6Fe/Al3Fe gives no visible response |
| A3 | 0.4 / 0.2 (2) | cubic α → Al6Fe → Al3Fe | single: α/Al6Fe |
| Binary 0.2 and 0.4 Fe | — | Al6Fe only in bulk | none |

### 3.3 Composition and trace-element effects

**Fe:Si**
- Brusethaug (DC 99.5% Al): FTZ depth is maximal at Fe:Si = 2 (dominant AlmFe at the edge). Fe:Si = 5 gives dominant Al6Fe and no FTZ. Fe:Si = 1 removes the FTZ but spoils electrograining [R5, p.18–19].
- Cutting the casting speed from 75–80 to 60–65 mm/min widened the FTZ beyond the scalping depth [R5, p.19].
- R10 recommends Fe:Si ≈ 3, small Cr and Mn additions, and low-head casting with less air gap [R10, p.118].

**Si level**
- Tezuka & Kamino (0.3 Fe): Si > 0.1 changes the dominant phase Al3Fe → AlmFe → cubic α (Si ≥ 0.25). An FTZ appeared only at 0.15 Si [R5, p.19–20].
- Lower Fe:Si favours α-AlFeSi over the binary phases [R5, p.17].
- In superpure alloys, Si suppresses Al6Fe and favours Al3Fe at lower rates. Al3Fe dissolves significant Si, whereas Al6Fe does not [R5, p.56–57].
- Up to 0.11% Si in Al–0.5Fe (printed as "Al–0.5 Si", probably a typo) is reported to favour metastable FeAl6 [R3, p.368]. This conflicts with the previous point, so the outcome depends on purity and test method.

**Trace elements: effect on the critical cooling rate Φc for Al6Fe → AlmFe**
- Lowered by: Mg up to 2.9%, Si up to 0.17%, Cu up to 0.3%, and Ti-B [R5, p.22–23].
- No effect: 0.1–2.1 Zn, 0.1–0.3 Mn, 0.1–0.3 Cr, 0.01–0.1 Ti [R5, p.22–23].

**Ca, Co, Mg, Ti-B and B**
- Ca: 30–50 ppm moves the FTZ boundary towards the centre (more so with grain refiner) [R5, p.23]. With Ca < 0.03% and grain size < 100 µm the FTZ was eliminated (Otani) [R5, p.23]. 0.04–0.11% Ca promoted Al3Fe [R5, p.24].
- Co: 0.044–0.053% gives AlmFe; 0.067% gives AlmFe only and no FTZ; 0.13% gives Al9(Fe,Co)2 [R5, p.24].
- Mg: 0.5% in Al–0.3Fe–0.15Si suppressed AlmFe [R5, p.24].
- Mg + Ti-B: adding 0.03Ti–0.005B to that Mg alloy made cubic α dominant everywhere [R5, p.24].
- B alone: up to 50 ppm removed the FTZ; at 150 ppm only AlmFe formed [R5, p.25].

**Maggs DC-simulator trace additions** (0.02 Mg/Mn/V; 0.04 Ti or Ti-B)
- 0.02 Mn and 0.04 Ti removed the **visible** FTZ boundary with little change in phases, i.e. they changed the etch response [R5, p.54].
- V, Ti and Mn eliminated AlxFe in A1. Mg hindered cubic α and promoted Al3Fe [R5, p.54, 58].
- Ti-B made cubic α dominant in A1 and A3 (no FTZ). In A2 it produced the most vivid FTZ, with AlmFe → Al6Fe [R5, p.55–56].
- Bigger grain-refiner additions move the FTZ boundary towards the centre [R5, p.23].

**Anodising and etching response** (OCR table; partly garbled)
- Al6Fe and β-AlFeSi are "not oxidised" and give a darker film. Al3Fe and α-AlFeSi oxidise and give a light film [R5, p.12].
- Al6Fe regions turned black after anodising, while Al3Fe regions stayed white (Hollingsworth) [R5, p.12].

### 3.4 Design levers (FTZ and Fe-phase selection)
- For anodising or litho-quality 1xxx, **avoid Fe:Si ≈ 2**. Use Fe:Si ≥ ~3–5 [R5, p.18–19; R10, p.118].
- Watch trace elements (Ca, Co, B, Ti-B, Mg) at ppm level. Specify ranges, because they can move FTZ boundaries [R5, p.22–25].
- **Casting speed** moves the FTZ: slower pushes it towards the surface (reliable but costs output); faster pushes it towards the centre but causes surface defects [R5, p.4–5].
- **Homogenisation** at ~590 °C converts Al6Fe and AlmFe to Al3Fe. α″ and AlxFe can persist [R5, p.16–17; R10, p.116–118].
- **For 6xxx extrusion billet, promote α over β.** Use Mn, fast cooling, and β→α conversion in homogenisation (β→α′ at 580 °C / 1 h observed) [R2, p.1–3; R3, p.383].

### 3.5 Phase identification method (TRIMET)
- β platelets lower the mechanical properties of extrusion billet. α "Chinese script" is preferred [R2, p.1].
- In 6xxx the particles are too few and too small for reliable morphology-based identification. EBSD is reliable but expensive [R2, p.1].
- **EDX method.** Plot Si against (Fe+Mn) for many particles. α and β fall on distinct Si/Fe lines (Griger) separated by a "free area", so a separator line can be drawn. The numeric separator is in an image and was not extracted [R2, p.2–5].
  - Mn is added to Fe because αc contains Mn [R2, p.2].
  - β data scatter more: the plates are thin, and free Si near β adds a Si background [R2, p.5].
  - Many measurements are required, and points with low Si and Fe must be discarded [R2, p.6].
- **Reference alloys and results.**
  - Pandat 8.1 predicted no α between 615 °C and RT for a high-Si/Fe alloy on 99.95% Al [R2, p.3].
  - A Mn-bearing alloy was predicted to contain only α between ~300 and 120 °C. In practice this needed fast cooling to 200–250 °C and holding at 200 °C [R2, p.3–5].
  - Samples were cast in 40 mm Ø × 35 mm steel moulds [R2, p.4].
  - Production 6xxx: alloys A and B were mainly α with some β; alloy C was all β [R2, p.5–6].
- Cross-check against the R3 numbers: α2 Fe/Si 2.75–5.5 vs β 1.6–2.25 (homogenised 6063) [R3, p.383].
- **Gap:** R2 cites Kuijpers' thesis on the kinetics of β-AlFeSi → α-Al(FeMn)Si in Al–Mg–Si [R2, p.6], but that thesis is not on Drive.

### 3.6 Pitfalls
- **Directional solidification is not DC casting.** DC ingots often contain 3 (up to 6) phases at one location, while high-purity directional samples contain 1–2 [R5, p.19–21].
- **Etch contrast is not phase identity.** Mn and Ti removed the visible FTZ without changing the phases [R5, p.54].
- **Thermocouple cooling rates mislead** in the centre of an ingot. Floating grains have longer, mixed thermal histories ("coarse-cell" grains) [R10, p.97–101].

### 3.7 Fe-phase selection: additions from [TOT] (full-text pass 2026-10-12)
**β versus α in Al–Si foundry alloys (Ch. 12)**
- **β-Al5FeSi is the most damaging Fe phase,** because of its needle (platelet) shape and its low coherency with the matrix [TOT p.609].
- **Mn converts β into α-Al15(Fe,Mn)3Si2** ("Chinese script"). The drawback: for a given Fe content, Mn raises both the hardness and the amount of intermetallic. The better crack-propagation resistance of the script morphology is therefore offset by a larger volume of brittle α [TOT p.609].
- **Cooling rate and composition are the two controls** [TOT p.610]:
  - Low cooling rates favour β needles; higher rates favour Chinese script.
  - The β-to-α transition moves to *slower* cooling rates as Fe falls, i.e. a leaner-Fe alloy still forms α at a slower cooling rate.
  - Fe promotes β; Mn and Cr stabilise α.
- **Guidelines** [TOT p.610]: keep Fe low; keep **Mn/Fe > 0.5**; solidify faster; limit the degree of eutectic modification.
- **Formation stages in Al–Si alloys** (Table 3) [TOT p.609–610]: pre-dendritic Al15(Fe,Mn)3Si2; post-dendritic Al15(Fe,Mn)3Si2 + Al5FeSi; eutectic Al5FeSi + Mg2Si; post-eutectic Al5Mg8Cu2Si6 + CuAl2. Complex eutectics can freeze as low as 480 °C.
- **Heat treatment** [TOT p.626]: during solution treatment β platelets fragment and dissolve at their tips, while α does not change. Temperature matters more than time once a minimum time is passed; 535 °C is quoted as the optimum for Al–Si castings.

**Dilute Al–Fe(–Si) wrought alloys (Ch. 3)**
- Commercial 1xxx solidification gives metastable Al6Fe or AlmFe instead of the equilibrium Al3Fe [TOT p.138].
  - Binary Al–Fe ingot preheated 16 h at 607 °C contains Al3Fe; 16 h at 482 °C gives Al6Fe.
  - With Si present, α (Al12Fe3Si) or β (Al9Fe2Si2) can appear in 1xxx sheet.
- Constituent particles raise yield strength by about 7 MPa per vol%, whatever the temper or phase type [TOT p.138].
- Coarse Al3Fe cracks and creates notches that lower formability and fatigue resistance. Finely dispersed Al6Fe does not [TOT p.139].
- **Front velocity** (alloys with 4.6–6.1% Fe) [TOT p.139]:
  - Al3Fe dominates below 0.5 mm/s, Al6Fe above.
  - Si raises the stability of Al3Fe against increasing front velocity, and 0.75% Mg raises it further. Ce and La suppress Al3Fe.
  - **This supports R5 (Si promotes Al3Fe) in the contradiction listed in §10 item 8**, and agrees with Mg promoting Al3Fe in the Maggs simulator (§3.3).

**Relevance: trial T11 (Si 0.38, Fe 0.52, Mn 0.14, Mg 0.26) on the rotary strip caster** (derived or inference, as marked)
- **Mn/Fe = 0.27** (derived), about half of TOT's > 0.5 guideline. Meeting it at 0.52 Fe would need Mn ≥ 0.26 (derived), close to the "Mn ≈ 0.25" sister-cast option in trials/T11.md §3. The guideline comes from Al–Si foundry alloys, so for T11 it gives a direction, not a threshold.
- **Fe:Si = 1.4** (derived) is below the Fe/Si of β (≈ 2) and of hexagonal α (≈ 4) (§2.2). There is enough Si for all Fe phases to be ternary.
  - (derived) If all Fe formed β, β would take ≈ 0.26 Si and leave ≈ 0.12 Si for Mg2Si and solid solution.
  - (inference) Tezuka & Kamino found cubic α dominant at Si ≥ 0.25 with 0.3 Fe (§3.3) [R5, p.19–20], so binary Al3Fe or Al6Fe should be minor in T11.
- **The closest measured path is 6063** (0.39 Si, 0.43 Mg, 0.2 Fe; Bäckerud) [R9, p.49; ch. 01 §4.1]:
  - Cubic α forms first (618–615 °C). β then forms by L + α → (Al) + Al5FeSi at 613 / 610 °C, at both 0.5 and 15 K/s.
  - T11 has the same Si, less Mg and 2.6 × the Fe (derived). (inference) **Expect α followed by peritectic β even at DC-type cooling rates.** Only strip regions cooled well above 15 K/s may suppress β.
- **Through-thickness gradient.** (general knowledge) A strip cast between two chills cools fastest at its faces and slowest at mid-thickness. TOT's rate rule (slow cooling gives β) therefore predicts **α script near the wheel and band faces and β platelets toward mid-thickness** (inference).
- **β persists to the slug.** β does not spheroidise [R1, p.23]. TOT reports β fragmenting and dissolving at its tips during solution treatment of castings (535 °C quoted as the optimum) [TOT p.626]. (inference) Unless the slug anneal approaches solution-treatment conditions, do not count on it to change β.
- **Fe/Mn = 3.7** (derived). A high Fe/Mn may give Al13(Fe,Mn)4 in the as-cast state [TOT p.160]. With only 0.14 Mn, Al6(Fe,Mn) should be minor (inference).
- **Mg 0.26** promotes Al3Fe over cubic α in the Maggs simulator (§3.3) and stabilises Al3Fe in TOT's front-velocity data [TOT p.139]. At T11's Si level its main effect is more likely Mg2Si or π-type phases late in solidification (inference; π(Al8FeMg3Si6) is listed for 6xxx in R9 [R9, p.47–48] via ch. 01 §4.5).
- **Test.** The trial plan's surface-versus-centre metallography (trials/T11.md §3) is the right check. Add the EDX Si/(Fe+Mn) classification of §3.5, because β plates and α script can look alike in a thin strip.

---

## 4. Twin-roll / continuous roll casting (TRC/CRC) versus DC

### 4.1 Mechanisms (from sources)
- Solidification and hot deformation both happen in the narrow roll gap. Once solidification is complete, the strip is reduced (hot worked) while still in contact with the rolls. This step is "essential for the final quality" [R4, p.115].
- Steel roll shells are used, with a lubricant (graphite in water) sprayed to prevent sticking. The strip is coiled hot. Strip thickness is 4–12 mm [R4, p.115–116].
- The roll gap, contact angle (arc length), rolling force, casting speed and roll-shell grade are interdependent [R4, p.117]:
  - A narrower strip width gives a larger contact angle and a higher rolling force.
  - A thinner strip (6.3 vs 6.5 mm) gives a larger contact angle and force.
  - Roll-shell grade II (MO22) gives a lower contact angle and force than grade I (CMYV).
- Over successive campaigns the casting widths step from wide to narrow, restarting at a smaller roll diameter [R4, p.117].
- Material-side requirements (no numbers given) [R4, p.118]:
  - clean charge, homogeneous composition and inlet temperature;
  - casting close to the liquidus;
  - a high metal level in the headbox;
  - low casting speed;
  - controlled nozzle (tip) geometry;
  - good heat conduction from melt to shell to coolant.

### 4.2 Quantitative data (Pechiney horizontal caster, AA1235 "Al99.2" and AA8011 "Al99.5" as labelled in R4)

| Parameter | Value | Source |
|---|---|---|
| Roll diameter / working width | 690 mm / ~1740 mm | [R4, p.116] |
| Strip width / thickness | 1020–1520 mm / 6.5–8 mm. Trial strips 6.3 (AA1235) and 6.5 mm (AA8011) | [R4, p.116–117] |
| Tip setback | 35–55 mm | [R4, p.116] |
| Separating force | 2.5–5·10³ kN/mm. Total load 5·10³ kN/mm (per mm strip width) | [R4, p.115–116] |
| Roll gap / contact arc | 5.2 mm for both alloys. "Contact angle" (given in mm) 50 mm for AA8011 and 47 mm for AA1235 (Table 1, 6.3 × 1200 (×1520) mm strip) | [R4, p.116, Table 1; column assignment recovered 2026-10-12] |
| Melt temperature | 685 ± 5 °C | [R4, p.116] |
| Strip speed | 1.30 (AA8011) and 1.25 (AA1235); stated casting range 0.95–1.50. **The unit is printed as "cm/min" both in the text and in Table 1; probably m/min, unverified.** (derived) At 1.30 m/min × 6.3 mm the output would be ≈1.3 t per m of strip width per hour; at 1.30 cm/min it would be ≈0.013 t/(m·h). The paper's own productivity figure, printed as "≈2.86·10⁶ t/(m·h)", is itself implausible and cannot settle the unit | [R4, p.116, Table 1] |
| Grain refiner ("modifier") | Al–Ti–B wire fed at 35 cm/min (AA8011) and 28 cm/min (AA1235) | [R4, p.116, Table 1] |
| Graphite lubricant | 2 l per 75 l water (the AA1235 cell is printed "2 l on l water") | [R4, p.116, Table 1] |
| Gauge targets | longitudinal ±2% per coil, ±1% per roll revolution; crown 0–1%; edge tilt ≤1% | [R4, p.116] |

Strips are 1–2 m wide [R4, p.115].

### 4.3 Microstructural consequences found in the sources
- Faster solidification moves the boundaries for primary Al3Fe and Al6(Fe,Mn) to higher Fe and Mn. TRC therefore tolerates more Fe+Mn before primaries form [R1, p.31]. This is inferred from the effect of cooling rate in general, not from a TRC measurement.
- Higher cooling rates raise Mn supersaturation, and with it the dispersoid potential on annealing above 300–350 °C. Fe and Si lower it [R1, p.12–15, 31–32; R13, p.382].
- On TRC 8111 strip after 550 °C / 10 h: 1Fe–0.8Si gave non-spheroidising Al5FeSi needles; 1Fe–0.4Si gave globular Al8Fe2Si [R1, p.27].
- At ~10 K/s and above, metastable Al6Fe, AlmFe and cubic α become likely in Al–Fe–Si (see §3.2) [R5, p.14–16; R1, p.8].
- (general knowledge) TRC strip solidifies at roughly 10²–10³ K/s. It shows mid-thickness (centreline) segregation of solute-rich liquid squeezed out during roll-gap deformation, and typical surface defects such as heat lines and tip marks. **None of the sources quantifies these points.**
- [TOT] treats strip casting only as a rolling-mill feed route [TOT p.352–354]:
  - Twin-roll casters suit low-capacity plants, mainly for soft alloys, down to a nominal minimum strip thickness of 6 mm. R4 gives 4–12 mm for its caster (§4.1); the two figures need not conflict, since they describe different machines.
  - A belt-type caster followed by tandem hot rolling handles 1100, 3000 and 5000 series at 16–20 mm and rolls them down to 2–3 mm.
  - **Relevance:** (derived) the user's 22 mm wheel-cast strip with in-line hot rolling is closest in gauge and layout to the belt-caster route, not to TRC. TOT gives no solidification or phase data for either route.

### 4.4 Design levers
- Use TRC's higher cooling rate to run higher Fe+Mn without primaries, and to retain Mn in solution for controlled dispersoid precipitation [R1, p.12, 31]. Choose Si so that α-Al(Fe,Mn)Si or Al8Fe2Si forms rather than β (8111: Si ≈ 0.4 at 1% Fe) [R1, p.23, 27].
- Process side (R4, qualitative): cast near the liquidus, at low speed, with stable headbox level and tip geometry, controlled lubricant rate, and a matched roll gap and force for each width [R4, p.117–118].

### 4.5 Pitfalls
- R4 has no microstructure, cooling-rate or segregation data. Do not use it to set metallurgical windows.
- The DC fir-tree and phase-selection data (§3) were measured at 0.5–20 K/s. Extrapolating them to TRC rates is unverified.

---

## 5. Centreline segregation and macrosegregation

### 5.1 Mechanisms
- Macrosegregation is relative movement of liquid and solid during solidification. Its length scale is centimetres, versus micrometres for microsegregation, so **homogenisation cannot remove it** [R11, p.125–128].
- DC billets usually show **inverse** segregation: negative at the centreline, positive at the surface, and a strongly depleted sub-surface layer [R11, p.126].

**Contributing flows**

| Flow | Effect | Source |
|---|---|---|
| Thermo-solutal convection | Washes solute-rich liquid out of the slurry zone around the outer quarter of the radius and carries it to the centre → **positive** centreline | [R11, p.136–138] |
| Shrinkage-driven flow in the mushy zone | ~10⁻⁴ m/s (6 mm/min) vs casting 100–200 mm/min. Its horizontal component removes solute from the centre → **negative** centreline | [R11, p.143–145] |
| Floating, solute-lean grains settling at the sump bottom | Always contributes **negative** segregation | [R11, p.145–150] |
| Deformation of the coherent network | ~2% volumetric strain can match shrinkage segregation. Drives surface and sub-surface segregation and exudation | [R11, p.151] |

**Mechanisms in steel continuous casting [R6], and what transfers**
- *Shrinkage alone* (steel: 2.5–3.8 vol.%; flow 0.1 to several cm/s) produces **no** positive centreline segregation [R6, p.49].
- *Bulging between rolls* pumps enriched liquid to the centre. Each bulge enriches the centre, and the enrichment scales with the bulging amount. The result is strong positive centre segregation with negative segregation around it [R6, p.49–50].
- *Soft reduction* (a pressure gradient) worked at 0.1 mm bulging but only "moderated" segregation at 1.0 mm. It has to be matched to the bulging [R6, p.50–51].
- *Bridging* of uneven shells works in four steps: the high-fs region constricts the channel; negative pressure develops under the bridge; enriched liquid is sucked in; linear and V segregates form [R6, p.51].
- *Mould EMS* gives negative segregation by washing the solute boundary layer [R6, p.52].
- The mixed diffusion coefficient near the crater end is E ≈ 20 cm²/s, 10⁴–10⁵ × D(Fe–C). With L = 20 cm, E/L ≈ 1 cm/s, which is comparable with shrinkage convection of 5–10 cm/s [R6, p.52].
- Transfer to Al (general knowledge): roll-gap pressure in TRC and gap variation in roll casting play the role of soft reduction and bulging. Matching the reduction to the mush state is the analogue of "soft reduction matched to bulging".

### 5.2 Quantitative data

**Permeability** [R11, p.133–136]
- Kozeny–Carman: K = (1−fs)³ / (k_KC·Sv²·fs²), with k_KC = 5 for equiaxed structures.
- In terms of the secondary DAS d: K = d²(1−fs)³ / (180·fs²).
- Reliable to about an order of magnitude for 0.6 < fs < 0.9.

**Partition coefficients K** [R11, p.172]

| Fe | Si | Cu | Mg | Zn | Mn | Ti | Cr |
|---|---|---|---|---|---|---|---|
| 0.03 | 0.13 | 0.17 | 0.43 | 0.45 | 0.82 | 9.0 | 2.0 |

- Fe segregates much more than Mn. Ti and Cr (K > 1) segregate in the opposite direction, i.e. positive at the centre [R11, p.170–172].
- [TOT] Table 3 gives k = Fe 0.022, Si 0.14, Cu 0.17, Mg 0.43, Mn 0.95, Sc 0.52 [TOT p.491]. Fe agrees within scatter (R5: 0.027 [R5, p.6]); **Mn differs (0.95 vs 0.82).** Both confirm Fe as the strongest segregant and Mn as nearly non-segregating.

**Speed rule**
- Vcast ≤ A/D, with A = 25,000–33,300 mm²/min. For a 200 mm billet this gives 125–167 mm/min and limits relative segregation to 3–6% [R11, p.152].

**Shrinkage-flow model** [R11, p.154–155]
- Vshr = Vcast·fl·β·cos α
- Vh = Vcast·fl·β·sin2α/2
- For Al–Cu (K = 0.171, β = 0.1): Lh = 0.78·C0·Lm·β·sin2α/2

**Sump slope α** (between the solidification front and the horizontal): segregation is negligible below 30° and acceptable below 60° [R11, p.158].

**Scaling criterion (Livanov)**
- SC = Vcast·D/a, with a ≈ 12,000 (no hot top) [R11, p.161].
- SC < 1 gives normal (positive) centre segregation; SC > 1 gives inverse (negative).
- For a 200 mm billet the transition is at ~60 mm/min.
- Empirical thresholds: Vcast·D = 12,465 mm²/min without grain refiner and 21,774 mm²/min with grain refiner [R11, p.161].
- Zero-segregation cooling rate: 2.3 K/s for D = 300 mm, ~11 K/s for D = 168 mm [R11, p.161].

**Regression on sump geometry** [R11, p.166]
- CS = −0.06124 − 4.341×10⁻²·Th + 1.64×10⁻³·A (R = 0.65)
- Th = transition-region thickness / radius; A = solidus slope angle in degrees.
- In sheet ingots of 400–600 mm, thickness affects sump depth more than casting speed does [R11, p.168].

**Grain refinement**
- Coherency fs rises from 0.23 to 0.45 with 0.05% Ti (Al–4Cu). Rigidity fs rises from 0.75 to 0.82 (2024) [R11, p.172].
- **3104, 5182 and 6009 sheet ingots: centreline segregation increases with Ti (0.001–0.006%).** The more potent Al5Ti0.2B gives worse segregation than Al–6Ti or no refiner (5182) [R11, p.173–174].
- In 2024, floating coarse-cell grains rose from 35% to 65–70 vol.% with grain refiner [R11, p.175].

**Melt feeding**
- A combo-bag gives the least segregation. A headscreen reinforces natural convection.
- Directing flow **downward at the centre** minimises segregation [R11, p.179].
- Forced convection (EMC or stirring) shifts the pattern towards normal (positive) segregation [R11, p.169–170].

**Melt temperature**
- A higher melt temperature raises sub-surface segregation and leaves the rest unchanged. Overall, segregation tends to fall as casting temperature rises [R11, p.159].

### 5.3 Design levers
- Keep Vcast·D below the empirical limit and keep the sump flat (α < 30–60°) [R11, p.152, 158, 161].
- For sheet ingot (3104/5182-type), choose the grain refiner type and amount with segregation in mind as well as grain size. Use a feeding system that drives a downward central flow [R11, p.173–179].
- For TRC by analogy with steel (general knowledge plus R6): control set-back, roll force and gap so that solute-rich liquid is not squeezed to mid-thickness. Matched reduction works; excessive reduction or gap variation pumps liquid [R6, p.50–51].

### 5.4 Pitfalls
- Duplex or floating grains are **not** a prerequisite for negative centreline segregation. In 5182 the grain-refined ingot was more segregated and had no duplex structure [R11, p.174–175].
- Grain refinement can push segregation either way, depending on the balance between convection, shrinkage flow and floating grains [R11, p.178].

---

## 6. Hot tearing and cold cracking

### 6.1 Mechanisms

**Where and when hot tears form**
- Hot tears form near the solidus at fs > 0.9 (85–95%), in liquid films between grains of a coherent network that carries tensile stress [R12, p.185].
- Feeding stages: mass feeding → interdendritic feeding → interdendritic separation (the vulnerable stage) → solid bridging (fs > 0.9) [R12, p.184].
- The mush has a "brittle temperature range" whose upper limit is set by the onset of linear contraction (rigidity) and lower limit by the non-equilibrium solidus [R12, p.185–186].
- Thermal contraction accumulated in the freezing range ranks alloys by hot-tear sensitivity. It reproduces the "lambda" curve with composition [R12, p.217].

**Microstructural factors**
- Liquid-film wetting: the dihedral angle θ in Al alloys is <20–25°. 1% liquid covers ~30% of grain boundaries and 10% liquid covers ~85%. The relation is σss = 2·σsl·cos(θ/2) [R12, p.212].
- Fe-bearing particles help when they are compact and break up the films, and hurt when they bridge early or block feeding:
  - Adding 0.8% Fe to Al–0.7Cu raised mush strength because the films became less continuous [R12, p.205].
  - Adding 0.2% Fe to Al–1.5Mn replaced elongated Al6Mn with compact Al6Mn + Al3Fe and raised the softening curve [R12, p.205].
  - Large early α(AlFeMn) crystals bridge dendrites, raise mush strength at low fs and block feeding, which **increases** hot-tear susceptibility (Nagaumi) [R12, p.243].
- A Fe:Si > 1 keeps the β + Si low-melting eutectic and free Si off grain boundaries [R12, p.207–208].

**Cold cracking (7xxx)**
- Cold cracking is catastrophic brittle failure of the whole ingot in the fully solid state. In R7's alloys it runs along grain boundaries and interdendritic spaces that are almost continuously covered by brittle non-equilibrium eutectics and intermetallics [R7, p.8, 71]. The fracture is mainly intergranular, with transgranular features where cracks cross interdendritic bridges [R7, p.61–62, 71].
- **Two ways the intermetallics fail** [R7, p.64–65]:
  - by cleavage under resolved normal stress;
  - by decohesion from the matrix, driven by the CTE mismatch (low-CTE particle, high-CTE matrix) and helped by shrinkage pores that form preferentially at particle–matrix interfaces.
- **Impurity constituents act as stress raisers and crack initiators** (Al7Cu2Fe from Fe, Mg2Si from Si) [R7, p.64–65]. *Corrected after full-text pass:* the earlier text called both "Fe-rich particles". Only Al7Cu2Fe is Fe-bearing; Mg2Si is the Si-bearing constituent.
- **Hot tears can seed cold cracks.** Centre hot tears may propagate after solidification and cause catastrophic failure [R7, p.69–70]. A sound 7050 billet nevertheless contained centre hot cracks a few mm long that did not reach critical conditions [R7, p.70, 141]. Cracks follow the intermetallic network in a "river-like" pattern and stop where they reach ductile matrix (§6.6) [R7, p.71, 101].

### 6.2 Quantitative data

**Thermal contraction at rigidity** (melt 720–730 °C, 12–18 K/s) [R12, p.196, Table 5.1]

| Alloy | Onset T (°C) | fs at onset | Expansion (%) | Contraction in freezing range (%) |
|---|---|---|---|---|
| 1050 | 657 | 0.38 | 0 | 0.03 |
| 2024 | 515 | 0.875 | 0.035 | 0.2 |
| 5182 | 528 | 0.93 | 0.08 | 0 |
| 6082 | 563 | 0.95 | 0.025 | 0.02 |
| 7075 | 525 | 0.87 | 0.03 | 0.27 |

**Contraction onset and grain refinement**
- Rigidity fs falls from 0.95 at 0.3% Cu to 0.8 at 4% Cu at 3–4 K/s, and is 0.9 at 4% Cu at 8–15 K/s [R12, p.192].
- In 6061-type alloys, grain refinement lowers the onset temperature by 20–60 °C and cuts thermal strain 2–3× [R12, p.193–194].
- The structure factor SF = Vc^−0.33/Dgr: in coarse, non-refined structures, linear contraction rises with SF [R12, p.190–191].

**Freezing range by alloy** (TL − TS, °C) [R7, p.48]

| Alloy | 1350 | 1100 | 3003 | 3004 | 5056 | 6063 | 7050 | 7075 |
|---|---|---|---|---|---|---|---|---|
| ΔT (°C) | 10 | 12 | 12 | 25 | 70 | 40 | 140 | 160 |

Thermal conductivity: 3003 193 W/mK, 3004 163 W/mK. CTE: 3003 23.2, 3004 23.9 ×10⁻⁶/K [R7, p.48–49].

**Mush properties**
- 3004 hardens after strength develops (it cannot accommodate stress) and reaches zero strength at fs = 0.81 [R12, p.206, 215].
- Al–1.4% Mn loses ductility sharply above the solidus [R12, p.208].
- A 7075 mush with Fe:Si = 5 is stronger than one with Fe:Si = 1 [R12, p.207–208].
- 10 h of melt holding (H from 0.30 to 0.19 cm³/100 g, coarser structure) worsened mush ductility. More gas means less linear contraction [R12, p.214].

**Composition effects on hot-crack susceptibility (HCS)**

| System | Effect | Source |
|---|---|---|
| 2038 | Fe up to 0.65% raises HCS, but HCS stays low at 0.95% Si. Mn > 0.5% raises HCS | [R12, p.217–218] |
| 6xxx (0.5Mg–0.5Si–0.15Ti) | HCS peaks at 0.3–0.4% Fe | [R12, p.220] |
| 6111-type | HCS minimum at 0.7–0.8% Cu | [R12, p.220] |
| Al–Cu DC billets | Maximum hot tearing at 0.5–1.5% Cu. No tears above 4% Cu at up to 220 mm/min | [R12, p.253] |
| Al–1% Cu | ~1 vol.% eutectic; ~90% of grain boundaries bridged | [R12, p.267] |
| High-purity Al–Si | Hot short up to 3% Si, critical range 0.17–0.8% Si | [R13, p.384] |

**Criteria**
- *Clyne–Davies CSC* = t_V/t_R, with t_V spent between fs 0.9 and 0.99 and t_R between 0.4 and 0.9 [R12, p.234].
- *RDG*: a pore forms when the pressure drop exceeds ΔPcr, ~2 kPa for Al–1.4Cu [R12, p.234]. RDG over-predicts tears in DC, because ΔP > 2 kPa under most conditions [R12, p.238–239].
- *Katgerman index*: combines t0.99, t0.40 and the time t_cr when after-feeding fails (Feurer criterion) [R12, p.235]. The index takes the form (t0.99 − t_cr)/(t_cr − t0.40) (general knowledge; the equation image is missing).
- *Sensitivity to the process*: Clyne–Davies and Novikov capture composition but not casting speed. Feurer, Katgerman, Magnin, Prokhorov, RDG, Braccini and Suyitno respond to speed. Only RDG and Suyitno respond to ramping, and only Suyitno responds to all parameters tested [R12, p.237–238].

**DC process effects**
- Casting speed matters most; water flow less; the effect of melt temperature is disputed [R12, p.246].
- Billets tear at the centre. Flat ingots tear near the short side and corners, and in the sub-surface layer because of rolling-face pull-in [R12, p.246–248].
- Maximum tearing occurs during **deceleration**, so sump depth is the governing variable [R12, p.254].
- 7075 cracking stopped when grain refiner was fed (1080 → 165 µm) [R12, p.256]. Grain refinement also cut hot tearing in 1050, 3104 and 5182 (Lin et al.) [R12, p.256].
- The benefit holds while grains stay dendritic. For >100 µm, finer is always better; non-dendritic grains <50 µm may raise HCS. Ultrasonically treated 20–80 µm non-dendritic ingots did not crack [R12, p.258].
- In Al–2.8Cu, raising the furnace melt temperature from 700 to 760 °C (superheat 47 to 107 °C) **reduced** hot cracking through healing by eutectic. More eutectic means less tearing [R12, p.259–262].

**Cold cracking (AA7050 as-cast)** (more detail, the criterion and the process effects are in §6.6)
- Yield (fracture) strength of radial billet samples: 279 MPa at RT, 30 MPa at 400 °C. Ductility falls from 23% to 2.5% below 300 °C (~90% loss). The material is brittle below 200 °C [R7, p.26–27, 64].
  - Table 6.1 of the same thesis (10⁻⁴ s⁻¹) gives 266 ± 12 MPa at RT and 23 ± 2 MPa at 400 °C instead (§6.6.1) [R7, p.94]. This is a source-internal difference; use the Table 6.1 set, which R7 itself uses for the simulations.
- CTOD: 6.4 µm at 25 °C, 7.8 at 100, 11.7 at 200, 495 at 300, 780 at 400 °C [R7, p.40].
- **K_IC of as-cast DC 7050 (ASTM E399): 8.9 ± 0.3 MPa√m at RT and 8.29 MPa√m at 200 °C** [R7, p.41, 111]. K_IC falls slightly with temperature, but within the error bars the differences are insignificant [R7, p.40]. Compare **20.9–27.5 MPa√m, the minimum K_IC of precipitation-hardened 7050 at RT** [R7, p.41].
  - *Corrected after full-text pass:* the RT value 8.9 ± 0.3 was previously marked "garbled, reconstructed". It is confirmed by the full text: the two-column paragraph on p.41 is interleaved in the Drive text but reads unambiguously. The 200 °C value (8.29) is stated on p.111. The 100 °C value exists only in Fig. 2.23, which is not readable.
  - (derived) Back-calculating K_IC from R7's own critical crack sizes with Eqs. 6.2/6.3 (§6.6.3) gives 8.2 MPa√m (10.1 mm penny crack at σ11 = 73 MPa) and 8.3 MPa√m (4.2 mm thumbnail crack at 100 MPa). Both agree with 8.29 at 200 °C.
  - Above 200 °C plane-strain conditions were no longer valid, because the yield strength drops from 154 MPa at 200 °C to 73 MPa at 300 °C; CTOD was used instead [R7, p.40].
  - Chang et al.'s earlier 7050 tests did not give valid K_IC (Pmax/PQ > 1.10). Their stress intensities at failure were K_Q = 10.4 and K_c = 12.4 MPa√m at RT (a/W = 0.55), measured on homogenised or stress-relieved billet, which is why they are higher [R7, p.41].
  - Test geometry: three-point bend, 150 × 30 × 15 mm, chevron notch, fatigue pre-crack to 15 mm total, K rate 0.55–2.75 MPa√m/s, 20 min soak at temperature [R7, p.38–39].
- DC strain rates are 10⁻⁵–10⁻² s⁻¹. Below 200 °C behaviour is strain-rate independent [R7, p.32].
- **Livanov's rule:** no cold cracking if the room-temperature tensile elongation of the as-cast material exceeds 1.5%. R7 calls it a rule of thumb from industrial experience, not a scientifically based criterion [R7, p.8, 16]. Livanov's slab rule: lower casting speed avoids hot cracks; higher speed avoids cold cracks [R7, p.8, 119–120]. R7's own billet simulations point the other way for cold cracking (§6.6.4; conflict in §10 item 8).
- Remedies: anneal at ~400 °C for a few hours immediately after casting (it cannot stop cracking during casting, but prevents failure on sawing); ingot wipers; EMC [R7, p.9–10]. The wiper practice was developed into the patented "in-situ homogenisation" [R7, p.120].
- Stress state: billets are tensile at the centre and compressive at the surface. Slabs are compressive on the rolling face and tensile in the interior; the narrow side can be tensile, increasingly so with width/thickness ratio and cross-section [R7, p.4].

### 6.3 Design levers
- Keep **Fe:Si > 1**. Avoid low-melting β + Si and free Si, which matter most in 1xxx and 8xxx [R12, p.208; R1, p.29].
- Avoid **coarse primary or early α(AlFeMn)** in Mn-rich alloys. It bridges dendrites early and blocks feeding [R12, p.243].
- Grain refine while staying dendritic (>~100 µm) [R12, p.256–258].
- Ramp the start-up speed gently (sump overshoot). Avoid fast deceleration [R12, p.251, 254; R10, p.82–86].
- 3xxx alloys have a narrow freezing range (12–25 °C) and are intrinsically less hot-tear prone than 2xxx and 7xxx [R7, p.47–48]. The 3004 data warn that the mush builds strength early (fs 0.81) [R12, p.215].
- **Cold cracking** (§6.6) [R7, p.142]:
  - keep the melt clean of inclusions, because a 7 mm Mg-oxide inclusion triggered the one validated failure;
  - choose the casting speed (and size) so that the smallest critical crack size predicted by the model is larger than the typical inclusion size;
  - design the bottom block so that it does not create local stress peaks;
  - handle cast product carefully, and do not remove the compressive surface shell (sawing) before a stress-relief anneal (~400 °C) [R7, p.9, 101].

### 6.4 Pitfalls
- Many criteria predict only *probability*, not *occurrence*. Do not rank DC process windows with CSC alone [R12, p.237–239].
- Properties of stress-relieved or homogenised material differ from as-cast. Simulations need genuine as-cast data [R7, p.24, 31].
- Higher purity is not always better. A high-purity 7010 was more cold-crack prone, and more Si in 7050 raised RT ductility (literature cited) [R7, p.16]. R7 did not test this itself: its "low-purity" and "high-purity" 7050 melts ended up with almost the same Fe and Si (0.16–0.20 Fe, 0.04–0.07 Si), probably supplied by the master alloys [R7, p.17].
- **Tensile-test Young's modulus is not elastic modulus at temperature.** In as-cast 7050 the tensile E fell from 73 GPa at 20 °C to 5.8 GPa at 400 °C because of creep, while torsion at high rate (69.5 → 54.5 GPa) agreed with JMat-Pro (67.9 → 53.6 GPa). R7 used the calculated values in its stress model [R7, p.43]. (inference) The same applies to any quench-stress or hot-mill model of the rotary route.
- **The thermal-stress model is not the fracture model.** R7's critical crack sizes assume a homogeneous, isotropic, grain-refined material with cracks normal to σ11 [R7, p.96]. Real cracks follow the intermetallic network, may not align with σ11 and may arrest in the matrix, which is why cold cracking looks random [R7, p.101, 138]. R7's mush rheology also borrowed Al–2Cu parameters, because none existed for 7050 [R7, p.80].
- **K_IC is measurable on as-cast 7050 only up to 200 °C** (plane strain fails above it) [R7, p.40]. The criterion therefore covers only the brittle range below 200 °C.

### 6.5 Hot cracking vs composition: additions from [TOT] (full-text pass 2026-10-12)
**Mechanism (welding chapter; same physics as casting hot tears)** [TOT p.499–500]
- Hot cracks tear liquid films formed by low-melting eutectics. A large gap between the liquidus and the lowest eutectic means more shrinkage across the film and longer feeding paths.
- A crack forms when grain separation outpaces back-filling. The interdendritic pressure then drops, and tearing starts by **decohesion at oxide inclusions** or by cavitation. The same pressure drop nucleates pores (details in ch. 01 §9.7).

**Peak susceptibility and eutectic quantity** [TOT p.490–491, 501–502]
- Susceptibility peaks at intermediate solute. At low solute the dendrite network is incomplete and the films are thin; at high solute there is plenty of eutectic to back-fill. The binary peaks (Varestraint, Fig. 11) are figure-only.
- Si gives the least cracking of the binary additions, because it makes a lot of eutectic for back-filling. Mg, despite a wide freezing range, makes very little eutectic, which gives resistance; Al–Mg alloys weld well at ≥ 4% Mg.
- **Eutectic fraction by Scheil** f = (C0/CE)^(1/(1−k)) (Table 3): Al–1Cu 1.48%; Al–1Mg 0.20%; Al–1Si 5.56%; Al–0.1Fe 5.21%; Al–0.1Sc 2.39%; Al–0.1Mn ≈ 0 (10⁻²⁴).
  - **Fe makes large amounts of eutectic even at 0.1% and "can have a profound effect on solidification, blocking the flow of interdendritic fluid to feed shrinkage"** [TOT p.491].
  - Mn at 0.1% makes essentially none.
- **Eutectic reactions** (Table 2) [TOT p.490]:
  - Al–Mg–Si: 595 °C (Mg2Si); 555 °C (Mg2Si + Si, high Si); 449 °C (Mg2Si + Mg5Al8, high Mg).
  - Binary: Al–Fe 655 °C (FeAl3); Al–Mn 657 °C (MnAl6); Al–Si 577 °C; Al–Mg 450 °C; Al–Cu 547 °C.
  - Mg lowers melting temperatures; high-Mg Al–Mg, Al–Mg–Cu, Al–Mg–Zn and Al–Mg–Si systems all form low-melting eutectics.
- Ternary crack maps: the Al–Mg–Cu ring-casting map (Fig. 12) shows a 3-D peak. "Similar cracking diagrams exist for Al–Mg–Si and Al–Mg–Zn alloys" [TOT p.502], but the book reproduces none of them (gap, §10).
- **Commercial alloys** [TOT p.505–507]: welded without filler, 6061, 7005 and 2014 give long crack lengths. 6060, 7030 and 6061 are "generally considered unweldable" without filler, while 7108 and 6082 weld readily.

**Foundry view (Ch. 12)** [TOT p.592, 602]
- Fe "improves hot tear resistance" and reduces die soldering, but lowers ductility.
- Si improves fluidity, hot-tear resistance and feeding. At least 5% Si gives a low crack tendency, because of the large eutectic fraction and a low coherency temperature.
- Cu harms hot-tear resistance and castability.

**Conflict on Fe.** TOT Ch. 12 says Fe improves hot-tear resistance [TOT p.592]. Against that: Fe raises HCS in 2038 up to 0.65%, the 6xxx HCS peaks at 0.3–0.4% Fe [R12, p.217–220], early coarse α(AlFeMn) raises susceptibility (Nagaumi) [R12, p.243], and Fe-rich eutectic blocks feeding [TOT p.491].
- (inference) A consistent reading: in eutectic-rich Al–Si foundry alloys, compact Fe phases add solid bridges (cf. 0.8% Fe in Al–0.7Cu [R12, p.205]); in lean wrought alloys, early Fe-rich eutectic networks block feeding.
- **For lean wrought alloys such as T11, use the wrought data (R12), not the foundry rule.**

**Relevance: hot-tearing risk of T11 (Mg 0.26 + Si 0.38, Fe 0.52) on the rotary caster** (inference unless cited)
- **Si.** 0.38 Si lies inside the critical hot-short range of high-purity Al–Si (0.17–0.8% Si) [R13, p.384]. T11 is on the lean side of the peak, far from the ≥ 5% Si where Si helps [TOT p.602].
- **Mg + Si.** The pair resembles a very lean 6060 or 6063 (6060 typically 0.35–0.6 Mg and 0.3–0.6 Si, general knowledge). 6060 and 6061 are crack-sensitive without filler [TOT p.505–507]. On the other side, the measured freezing-range contraction of 6082 is small (0.02%) [R12, p.196].
- **Fe is the main eutectic-maker in T11.** (derived, binary Scheil with TOT Table 3) About 28% of the liquid would end in Al–Fe eutectic reactions at 0.52 Fe, versus ≈ 1.8% for Si at 0.38 and ≈ 0.02% for Mg at 0.26. Such early Fe-rich eutectic blocks feeding [TOT p.491]. T11's 0.52 Fe lies above the 0.3–0.4% Fe HCS peak measured in 0.5Mg–0.5Si 6xxx [R12, p.220]; no data exist for higher Fe.
- **Last liquid.** The lowest-melting reactions available are Mg2Si + Si at 555 °C if free Si forms [TOT p.490; R9, p.47] and β + Si at 573–576 °C (§2.2). (derived) A strip exit temperature of ≈ 500 °C is ≥ 55 K below both, so the in-line hot mill acts on solid metal, provided the reading represents mid-thickness.
- **Levers for the caster:**
  - TiB2-refined, dendritic grains (§6.3).
  - A clean melt, because oxide films initiate tears [TOT p.500].
  - Keep Fe:Si > 1, which T11 already does (1.4), to avoid free Si.
  - Avoid mechanical strain on the strip in the wheel–band contact while fs > 0.9 (ch. 01 §9.1).
- **No hot-tear measurement exists for T11 or any comparable Fe-rich lean Mg–Si alloy.** The trial's crack inspection of the cast strip (trials/T11.md §3) is the first data point.

---

## 7. Blister formation, hydrogen and inclusion defects

### 7.1 Mechanism
- Hydrogen above its solid solubility is immobile at RT and mobile at high temperature. It diffuses to internal discontinuities and recombines to H2, and the pressure rises until it balances the dissolved gas. Because solubility ∝ √p (Sieverts), large pressures build up. On annealed sheet the pressure deforms the softened surface into a blister [R8, p.924].
- **Both gas and discontinuities are required.** The discontinuity factor, mainly **micro-shrinkage**, dominates control [R8, p.925].
- Blisters are expanded lamellar discontinuities parallel to the sheet surface. They develop from ingot shrinkage cavities that rolling flattens. Entrapped oxide is possible but hard to detect, because X-ray absorption is almost the same as for Al [R8, p.924–925].
- Hydrogen also causes secondary porosity, blistering and high-temperature deterioration during heat treatment [R13, p.378].
- **Where the hydrogen comes from** [R13, p.372, 377–378; full-text pass 2026-10-12]:
  - It is produced by the reduction of atmospheric water vapour by aluminium and by the decomposition of hydrocarbons.
  - Pickup "in both solid and liquid aluminum" is enhanced by impurities such as sulfur compounds on the surface and in the atmosphere.
  - Hydride-forming elements raise pickup in the liquid, whereas Be, Cu, Sn and Si lower it. As little as 10 ppm Ca increases the tendency of molten alloys to pick up hydrogen.
  - The melt level is controlled by fluxing with hydrogen-free gases or by vacuum degassing.
- **How the defect was traced** [R8, p.924–925]:
  - Blister-raising discontinuities in sheet ingots were located by radiography and ultrasonics and followed through every production stage.
  - Blisters were seen forming *during annealing* at the sites of ingot porosity, which fabrication had turned into lamellar discontinuities.
  - In the DC-casting-variables programme, NDT failed to locate the (finer) discontinuities. Density measurements on ¾ × 3/16 × 6 in. strips cut across the ingot width found low-density regions that matched the blister sources, and metallography showed them to be micro-shrinkage.
  - Very few oxide inclusions were seen in the ingot sections, but they could not be ruled out, because the methods detect cavities far better than oxide.

### 7.2 Quantitative data (Alcan 2S ≈ 1100)
- **Route:** HR at 500 °C to 6.35 mm (0.250 in), CR to 1.0 mm (0.040 in), anneal 2 h at 500 °C, inspect 5-in squares. One blister on either surface scraps a square [R8, p.924–925].
- **Gas content:**
  - Melts were deliberately gassed by adding water, which reacts to Al2O3 + H. Gas was measured by vacuum fusion.
  - Gassed melts at 1.7–2.7 ml/270 g gave 100% scrap. Fluxing with Cl2, N2 or Ar at 680–750 °C cut gas to 0.20–0.50 ml/270 g and scrap to 0–4%. Multi-stream fine bubbles beat a single stream, and C2Cl6 worked similarly [R8, p.924–925].
- **Ingot type:** tilt-mould ingots had large shrinkage cavities and large blisters. DC ingots had small cavities and small blisters. Low-density regions corresponded to micro-shrinkage [R8, p.924–925].

**Ingot preheat, gas (ml/270 g) and % blister scrap** [R8, p.925, Table I. Verified on 2026-10-12 against the layout extraction: the earlier column assignment was correct. Each cell gives the original ingot gas → the gas after preheating, then the % blister scrap.]

| Preheat time | 500 °C: gas before → after; scrap | 550 °C | 600 °C |
|---|---|---|---|
| 6 h | 1.35 → 1.55; 89% | 1.65 → 1.11; 93% | 1.63 → 0.35; 34% |
| 12 h | 1.32 → 1.22; 87% | 1.51 → 1.23; 100% | 1.50 → 0.19; 17% |
| 18 h | 1.53 → 1.27; 80% | 1.38 → 0.87; 94% | 1.90 → 0.14; 33% |
| 24 h | 1.43 → 1.28; 84% | 1.39 → 0.42; 64% | 1.70 → 0.28; 27% |

- A 500 °C preheat did not lower the gas: it rose at 6 h (1.35 → 1.55) and fell only slightly at longer times [R8, p.925, Table I].
- (derived) After the 600 °C preheat the ingots held 0.14–0.35 ml/270 g, no more than the fluxed melts (0.20–0.50), yet still gave 17–34% scrap versus 0–4%. Removing hydrogen from a solid ingot does not remove the porosity it has already formed, which agrees with the source's conclusion that the discontinuity dominates.
- **Abstract (now legible; corrected after full-text pass):** *"The use of a fabricating technique based on at least 40 pct cold reduction of the as cast ingot prior to the application of normal hot and cold rolling procedures has been shown to eliminate blisters. An explanation for this is offered."* [R8, p.924].
  - The explanation and the process details are on p.926 onward, which **is not in the Drive file** (§0).
  - (general knowledge; a hypothesis, not R8's text) A plausible mechanism is that cold reduction at RT, where the hydrogen is immobile, collapses and presses together the shrinkage cavities before any preheat can let H2 diffuse into them and pressurise them. The flattened cavities can then bond during hot rolling instead of persisting as gas-filled lamellae.

### 7.3 Design levers and pitfalls
- Degas (fine-bubble inert or chlorinating flux) and minimise micro-shrinkage, i.e. feeding and casting practice. Low gas alone does not stop blistering when shrinkage porosity is present [R8, p.924–925].
- A high-temperature ingot preheat (600 °C) lowers the H content and the scrap rate. 500–550 °C was much less effective [R8, p.925].
- Heavy (≥40 %) cold reduction of the as-cast ingot before hot rolling eliminated blisters in R8's trials [R8, p.924]. The process window is not available (p.926+ missing).
- **Pitfall:** X-ray NDT finds pores but misses oxides. Fine micro-shrinkage may escape both radiography and ultrasonics, so density profiling across the ingot is the fallback [R8, p.925].
- **Annealing-stage hydrogen** is relevant to slugs and coils, because blisters form when the metal softens during the anneal [R8, p.924].
  - Water vapour, decomposing hydrocarbons and sulfur compounds on the surface or in the atmosphere are hydrogen sources or pickup promoters for **solid** as well as liquid Al [R13, p.377–378].
  - (general knowledge, inference) Applied to annealing, this points to rolling-oil residues and humid furnace atmospheres as the likely in-process sources. The practical consequences are clean, degreased strip or slugs and a dry atmosphere.
  - The source is **qualitative only**: no dew-point, lubricant-residue or H-pickup numbers exist in the Drive library for *solid* metal. *Update 2026-10-12:* [TOT] adds melt-side pick-up versus humidity (ch. 01 §10.1) and a weld shielding-gas dew-point threshold (§7.4), but still nothing for slug or coil anneals.

### 7.4 Hydrogen and inclusion defects: additions from [TOT] (full-text pass 2026-10-12)
Melt-treatment detail (solubility equations, pick-up, degassing, filtration, alkali removal) is in ch. 01 §10.1–10.4. This section gives the defect view.

**Hydrogen**
- **Solid solubility.** TOT quotes 0.03 ml/100 g at 600 °C [TOT p.661]. (derived) The solid-solubility equations in TOT give 0.025 (Ransley) and 0.030 (Eichenauer) cm³/100 g at 600 °C, and 0.005 / 0.003 at 400 °C [TOT p.74–75].
- **Supersaturation, then pores.** Excess hydrogen frozen into supersaturated solid solution precipitates as pores during later heat treatment [TOT p.644].
  - In 99.99% Al slab, pores grew during homogenisation at 600 °C by annihilation of micro-porosity and precipitation of hydrogen at grain boundaries. They caused cracks in hot rolling. The experience limit is **< 0.10 ml/100 g** [TOT p.661–662].
  - Solid Al can also take up hydrogen and form pores when heated at high temperature in humid environments [TOT p.119].
- **Organic contamination** (welding chapter) [TOT p.497]: oil, drawing compounds and shop grease cause pores through their hydrogen; tests with graphite showed the carbon is not responsible. A pre-weld vacuum heat treatment is suggested, and shielding-gas dew points above about −40 °C promote porosity.
  - (inference) The same chemistry applies to rolling-oil residue on strip or slugs entering an anneal. The −40 °C figure is for weld shielding gas, not a furnace specification.
- **In-line melt treatment helps downstream.** Combined degassing and inclusion removal (GBF) cut pinholes, scratch-like stringers and blisters in foil, sheet and extrusions [TOT p.674].
- **Cross-check with R8** (derived; assumes R8's "ml/270 g" means per 270 g of metal, as printed): fluxed melts at 0.20–0.50 ml/270 g = 0.07–0.19 ml/100 g; gassed melts at 1.7–2.7 ml/270 g = 0.63–1.0 ml/100 g; ingots after the 600 °C preheat at 0.14–0.35 ml/270 g = 0.05–0.13 ml/100 g. R8's nearly blister-free fluxed melts therefore straddle TOT's 0.10 ml/100 g limit.

**Inclusions** [TOT p.118–119, 664–666]
- **Oxides are the main class:** Al2O3, MgO and spinel MgAl2O4 (sizes in ch. 01 §10.3).
  - "Old" oxides come from the crucible. They are thick, filtration controls them, and they cause defects from pinholes in foil to reduced fatigue life.
  - "Young" oxides are folded in by surface turbulence above **0.5 m/s**. The double films do not bond, so they act as cracks.
- **Where young oxides end up.** They lie on grain boundaries, because dendrites cannot grow across them, and on intermetallics, because **intermetallics formed by peritectic reactions deposit on floating oxide films** [TOT p.118].
- **Detection.** Oxide films can be 1 µm wide and 10 nm thick, below NDT sensitivity [TOT p.119]. Entrained oxides also act as nucleation sites for hydrogen pores [TOT p.119].
- **Size thresholds.** Inclusions generally harm properties above about 30 µm. Drawn-and-ironed can stock needs smaller ones removed, and inclusions below 10 µm cause pinholes in foil a few µm thick [TOT p.664].

### 7.5 Relevance: rotary-cast strip, slug anneal and trial T11 (inference unless cited)
- **Hydrogen reaches the slug anneal.** The rotary route has no ingot homogenisation, and the 22 mm strip cools fast. Hydrogen above the solid solubility stays in supersaturated solution [TOT p.644], and the **slug anneal is the first long high-temperature step**. There it can precipitate into micro-shrinkage, oxide films and particle interfaces, giving blisters on annealed slugs (R8 mechanism, §7.1).
  - Starting melt specification: < 0.10 ml/100 g (TOT's 99.99% slab limit, adopted here as a working value).
  - Keep slugs clean and dry, and keep the anneal atmosphere dry.
- **Reduction does not cure everything.** (derived) 22 mm to a 6.1–7.4 mm slug is a total thickness reduction of 66–72%, before impact extrusion. Pores close with sufficient rolling [TOT p.120]. Oxide double films do not bond [TOT p.118], so they should survive into the can wall.
- **More oxide classes than in 1xxx.** T11's 0.26% Mg makes MgO and spinel inclusions more likely than in 1xxx metal [TOT p.666].
- **Oxide films may carry Fe intermetallics.** In a scrap-rich melt, intermetallics that deposit on oxide films [TOT p.118] would place the oxide films and the coarse Fe phases at the same sites. That makes filtration doubly important for T11: for slug-base damage and die wear (ch. 10), and for β-AlFeSi (§3.7).
- **Filtration and wheel feed.** Use ≥ 50 ppi foam, a deep bed or a cartridge filter (30 ppi counts only as a pre-filter for can-grade metal [TOT p.677]). Keep free-surface velocities feeding the wheel below 0.5 m/s [TOT p.118]. See ch. 01 §10 for the melt-side measures.
---

## 8. Supporting solidification relations (DC)

| Relation | Formula / value | Source |
|---|---|---|
| Grain size | Dgr = A·ΔT0^0.25·Vs^−0.25·G^−0.5 | [R9, p.21] |
| Dendrite arm spacing | d = B·tf^n = C·Vc^−n, n = 0.2–0.4. For Al–Cu, n ≈ 0.4 (DAS) and ≈ 0.3 (grain size) | [R9, p.24] |
| Scheil | CL = C0·(1−fs)^(K−1) | [R9, p.29] |
| Growth restriction | Q = m·C0·(K−1). Undercooling parameter P = m·C0·(K−1)/K. Ti: Q ≈ 35 at 0.15% Ti. Ti is added as Al–Ti–B at 0.001–0.005% | [R9, p.59–60, 65] |
| Al–Ti–B | L + Al3Ti → (Al) at 665 °C. TiB2 hexagonal, a = 0.3032, c = 0.3231 nm. The Al3Ti layer on TiB2 nucleates (Al) via (0001)TiB2 ∥ (112)Al3Ti ∥ (111)Al | [R9, p.69–73] |
| Sump depth | H = A·Vcast·R²/(4·λs·(Tm − Tsurf)). Typical Pe 1.8–4.5, Bi 1–25 | [R10, p.80–81] |
| Maximum mean solidification rate | Vs,max = 4·λ·(Tm − Tsurf)/(ΔH·ρ·R) | [R10, p.92] |
| Heat-transfer coefficients | mould 1–2.5 kW/m²K → air gap ~0.5 → impingement ~48 → falling film 30–40. Nucleate boiling ~40 kW/m²K, up to 6000 kW/m² | [R10, p.87, 94–96] |
| Ramp rate | A ramp of 11.32 mm/min² gives near real-time sump response; 113.2 mm/min² lags strongly | [R10, p.86] |
| Feathery grains | Form at >10 K/s, with superheated melt against a water-cooled mould. Favoured in pure alloys (1xxx) and by Cr, Zr, Ti, Mg, Cu, Zn, Si. Consist of <110> twinned dendrites → anisotropy and inhomogeneous recrystallisation. Remedy: grain refiner, lower superheat, slower casting | [R10, p.118–120] |
| Bleed-out | A grain-refined alloy has a wider slurry zone and a narrower mush, which increases the risk | [R10, p.121] |
| Primary dendrite spacing | χ = K1·(dT/dt)^−1/2 = K1·(R·G)^−1/2. Rough anchors: ~10 µm at ~100 °C/s (welds), ~100 µm at ~10 °C/s (castings) | [TOT p.489, 744] |
| Secondary DAS (coarsening form) | ds = B·(M·tf)^(0.3–0.4), B = 4.36–5.5; M(AlSi7) = 16.3×10⁻¹² cm³/s | [TOT p.745–746] |
| Scheil eutectic fraction | f = (C0/CE)^(1/(1−k)); 0.1% Fe → 5.2%, 1% Si → 5.6%, 1% Mg → 0.2%, 0.1% Mn → ≈ 0 | [TOT p.491] |
| Pore condition | Pg > Pa + Ph + 2γ/r | [TOT p.494–495] |
| Niyama | N = G/R^0.5 at the solidus. As printed, porosity when "a critical value is exceeded"; usually below a critical value (general knowledge). Check before use | [TOT p.632] |

---

## 9. Key numbers cheat-sheet

| Phase | Composition (wt.%) | Formation reaction, T, cooling rate | Morphology | Effect / note |
|---|---|---|---|---|
| Al3Fe (Al13Fe4) | ~37–40 Fe (39.2 Fe, 0.8 Si at U10); 0.2–6 Si dissolved | L→(Al)+Al3Fe 655 °C, 1.8 Fe. Below ~2 °C/s (hypoeutectic) | Faceted plates or needles, anomalous eutectic | Does not spheroidise in foil; cathodic; light anodising response [R5, p.7–13; R1, p.23; R13, p.399; R5, p.12] |
| Al6Fe | Orthorhombic, <0.5 Si | L→(Al)+Al6Fe 650 °C, 3.5 Fe. ~1–10 °C/s; >1 K/s in 1050 | Fine rods, normal eutectic | Dark anodising response (FTZ). → Al3Fe at 590 °C / 5 h [R5, p.8, 12, 16; R1, p.31] |
| AlmFe (m ≈ 4–4.4) | bct, ≤3 Si | >10–35 °C/s; ~20 K/s | "Dendrite-like", regular eutectic | Outer FTZ zone; promoted by Co, Ti-B and B >50 ppm [R5, p.8–9, 14, 24–25; R10, p.116] |
| AlxFe (x ≈ 5–5.8) | Disputed | ~0.5–6 K/s | — | Survives 590 °C / 5 h [R5, p.9, 15–17] |
| Al6(Fe,Mn) | 19.6 Fe, 7.1 Mn (eutectic vertex); orth. a = 0.755 nm | L→(Al)+Al6(FeMn) 658–654 °C; E 654 °C with Al3Fe. Sole phase at >10 K/s (low Si). 3003: 653 °C (0.5 K/s), 646–615 °C (17 K/s) | Eutectic plates or script | Potential ≈ matrix (good corrosion). Primary if Fe+Mn >2.0 (3003) or >1.7 (3004) [R1, p.10–12, 38; R13, p.383, 402] |
| α-Al15(Fe,Mn)3Si2 (cubic) | 26.3 Mn, 8.9 Si → 31 Fe, 1.5 Mn, 8 Si; a 1.265 → 1.25 nm | P4 648 °C; in 3003 peritectic 641–634 °C (0.5 K/s) or 589 °C (17 K/s); also as dispersoids on preheat | Chinese script or skeleton | Preferred over β. Binds Fe, Si and Mn, lowering Mn supersaturation [R1, p.12–19, 38, 43; R13, p.388]. Stabilised by Mn and Cr (Mn/Fe > 0.5), but Mn raises the hardness and volume of α [TOT p.609–610] |
| α-AlFeSi hexagonal (Al8Fe2Si, τ5) | 31.6 Fe, 7.8 Si (30–33 Fe, 6–12 Si); Fe/Si ≈ 4 | U10 L+Al3Fe→(Al)+α 632 °C (629 Phillips); monovariant 629–611 °C | Script; spheroidises at 550 °C | 8111 at ~0.4 Si with 1 Fe is the best case for foil [R1, p.1, 4, 23, 27; R3, p.396] |
| α-AlFeSi cubic (αc, metastable) | Al:Fe:Si 7:4:1 to 9:5:1; a ≈ 1.25–1.256 nm | High cooling rates; Fe:Si ≈ 2; stabilised by Mn, Cr, V, W, Cu and ~0.3% Mn/Cu; TiB2 promotes it | Script | Light anodising response; in 6xxx formed by L+Fe4Al13 or eutectically [R3, p.361, 387; R5, p.11, 53–56] |
| β-AlFeSi (Al5FeSi, τ6) | 25.6 Fe, 12.8 Si (25–30 Fe, 12–15 Si); Fe/Si ≈ 2 | U11 L+α→(Al)+β 613 °C; E1 L→(Al)+β+(Si) 573 °C (576 °C in Phillips); monovariant 611–576 °C | Plates (needles in section), HV 5.8 GPa | Avoid: hurts properties and foil; non-spheroidising; low-melting eutectic → hot tearing [R1, p.1, 4, 6, 23; R2, p.1; R3, p.397; R12, p.208]. Most detrimental Fe phase (needles, low coherency); favoured by slow cooling and high Fe; fragments and dissolves at its tips during solution treatment [TOT p.609–610, 626] |
| δ-AlFeSi (Al4FeSi2, τ4) | 25.4 Fe, 25.5 Si | U12 600 °C (high Si) | Tetragonal plates | → β at 500 °C [R1, p.2; R3, p.386, 397] |
| (Si) | — | Eutectic 577 °C; with Mn-α at 573–574 °C; appears at 0.2–0.3 Si in Al–Mn alloys | Particles or veins | Foil perforation; lowers solidus [R1, p.15, 23; R3, p.397] |
| Al6Mn / Al15Mn3Si2 dispersoids | — | Precipitate on annealing above 300–350 °C | Sub-µm | Control recrystallisation; the amount is set by as-cast Mn supersaturation [R1, p.31–32; R13, p.389] |

**Process numbers**

| Item | Value | Source |
|---|---|---|
| Fe solubility in (Al) | ≤0.04–0.052% | [R5, p.7; R3, p.366; R1, p.2] |
| Mn solubility in (Al), three-phase vs binary | 0.23% vs 1.8% at 654 °C | [R1, p.12] |
| DC cooling rates | 1–20 K/s | [R5, p.59; R10, p.113] |
| FTZ border | ≈8 °C/s | [R5, p.16] |
| Al3Fe → Al6Fe critical rate | ≈2 °C/s | [R5, p.13] |
| Al3Fe → Al6Fe critical growth velocity | 100–110 µm/s | [R5, p.13–14] |
| Macrosegregation speed limit | Vcast·D ≤ 25,000–33,300 mm²/min | [R11, p.152] |
| Positive/negative segregation threshold | Vcast·D ≈ 12,000–12,465 (no refiner) or 21,774 (refined) | [R11, p.161] |
| CSC fractions | t_V at fs 0.9–0.99; t_R at fs 0.4–0.9 | [R12, p.234] |
| Hot tearing | fs > 0.9 | [R12, p.185] |
| Blister prevention | Gas ≤ ~0.2–0.5 ml/270 g (fluxed melt), plus low micro-shrinkage. A 600 °C ingot preheat lowers gas (to 0.14–0.35) but leaves 17–34 % scrap. ≥40 % cold reduction of the as-cast ingot before hot rolling eliminated blisters | [R8, p.924–925] |
| Fe solubility in (Al) at 400–550 °C (three-phase fields) | 0.002–0.016 % | [R1, p.6, Table 1.4] |
| Mn solubility in (Al) at 400 / 450 / 500 °C | 0.06 / 0.15 / 0.25 % (Al6Mn+α field); 0.04 / 0.05 / 0.06 % ((Si)+α field) | [R1, p.15, Table 1.13] |
| Mn/Fe to favour α over β | > 0.5 (Al–Si foundry alloys). T11: 0.27 (derived) | [TOT p.610] |
| β vs α with cooling rate | Slow → β needles; fast → α script; transition shifts to slower rates at lower Fe | [TOT p.610] |
| Al3Fe vs Al6Fe front velocity | Al3Fe below 0.5 mm/s, Al6Fe above (4.6–6.1% Fe). Si and 0.75% Mg stabilise Al3Fe | [TOT p.139] |
| Mn in solution, as-cast 3003 ingot | 0.7–0.9 wt% | [TOT p.160] |
| Dispersoid type vs Si (3xxx) | Si < 0.07% → Al6(Mn,Fe); more Si → Al12(Mn,Fe)3Si | [TOT p.160] |
| Constituent strengthening (1xxx) | ≈ 7 MPa per vol% | [TOT p.138] |
| Partition coefficients, TOT | Fe 0.022, Si 0.14, Cu 0.17, Mg 0.43, Mn 0.95, Sc 0.52 | [TOT p.491] |
| H solid solubility | 0.03 ml/100 g at 600 °C | [TOT p.661] |
| H limit against pores and hot-rolling cracks | < 0.10 ml/100 g (99.99% Al slab) | [TOT p.661] |
| Critical free-surface velocity (young oxide films) | 0.5 m/s | [TOT p.118] |
| Harmful inclusion size | > 30 µm generally; < 10 µm in thin foil | [TOT p.664] |
| Al–Mg–Si eutectics | 595 °C (Mg2Si); 555 °C (Mg2Si + Si); 449 °C (Mg2Si + Mg5Al8) | [TOT p.490] |

---

## 10. Open questions / gaps
1. **Al6(Fe,Mn) → α-Al(Fe,Mn)Si transformation during 3xxx homogenisation.** None of the sources gives kinetics (temperature, time, Si dependence) for AA3102 or AA3207. [TOT] adds only the qualitative facts that Si accelerates Mn precipitation and that, with enough Si, as-cast Al6(Mn,Fe) transforms to Al12(Mn,Fe)3Si [TOT p.160] (§2.6). R1 and R13 cover the phases only qualitatively. Kuijpers' thesis on β→α in 6xxx is cited by R2 but is not on Drive. *Action:* locate dedicated 3003/3xxx homogenisation papers.
2. **TRC metallurgy is essentially missing.** R4 gives only process parameters. Its Table 1 is now legible (2026-10-12), but the speed unit is still printed as "cm/min" and remains unverified (§4.2). The cooling rate, Mn/Fe/Si supersaturation, centreline segregation, and surface or bulk defects of TRC (cf. Sun et al. 2006 on TRC AA3105; Monaghan et al. 1993, both cited in R4) need sourcing. [TOT] (2026-10-12) adds no strip-casting metallurgy, only that twin-roll casters reach a nominal 6 mm minimum and belt casters cast 16–20 mm [TOT p.352–354] (§4.3).
3. **PSN and recrystallisation.** No source quantifies the particle-size threshold for particle-stimulated nucleation, or how constituent morphology affects texture and earing. Particle effects on formability appear only qualitatively, for foil [R1, p.23].
4. **Truncated or incomplete sources** (status after the 2026-10-12 full-text pass):
   - Maggs (R5) Chs 4–6, with the DSC and Bridgman critical-rate data for Mg, Ti and Ti-B, are still missing. Lalpoor (R7) Chs 5–8 (cold-cracking criterion, critical crack size) are still missing. Both files exceed the 10 MB download-tool limit. *Action:* the user splits the PDFs (e.g. per chapter) and uploads the parts, or downloads them through the standard Drive API.
   - O'Dette (R8): the Drive file holds only pp.924–925, so the ≥40 % cold-reduction explanation (p.926 onward) cannot be recovered from Drive. *Action:* obtain the complete article (J. Metals / Trans. AIME, July 1957, TP 4460E).
5. **Tables still unreadable.** R1 Tables 1.2 (Al–Fe–Si invariants), 1.5 (metastable phases) and 1.16 (quaternary mono/bivariant reactions) are on rotated pages with a garbage OCR layer; they need OCR or the printed book. The R7 KIc numbers remain unverified because R7 is too large to download. *Resolved 2026-10-12:* R1 Tables 1.4, 1.7 and 1.13 and R8 Table I (§2.2, §2.4, §2.5, §7.2).
6. **Mn:Fe threshold for wrought 3xxx/8xxx.** There is no quantitative Mn:Fe or Si window for forming α instead of β or Al6(Fe,Mn) at DC versus TRC cooling rates. The only number found is the 4xx.x statement that "≫1:20" is needed [R1, p.43].
   - *Partly addressed 2026-10-12:* [TOT] gives **Mn/Fe > 0.5** together with the rule that slow cooling favours β, and that lower Fe moves the β→α transition to slower cooling rates [TOT p.610] (§3.7). These numbers come from Al–Si foundry alloys. A window for lean wrought or strip-cast alloys (DC vs strip cooling rates) is still missing; the T11 trial metallography will give the first in-house point.
7. **Hot-tear data for 3xxx.** Only 3004 mush strength (fs 0.81), the Al–1.4Mn ductility drop and the benefit of grain refinement in 3104 are available. No CSC or measured HCS exists for 3102 or 3207.
   - [TOT] (2026-10-12) adds the mechanism, binary peak behaviour and Scheil eutectic fractions (§6.5). It states that Al–Mg–Si crack maps exist [TOT p.502] but reproduces none, and it has no 3xxx data. Still missing: hot-tear data for lean, Fe-rich Mg–Si alloys such as T11.
8. **Contradictions to resolve:**
   - Si promotes Al3Fe [R5, p.57] vs Si promotes FeAl6 [R3, p.368]. *Partly resolved 2026-10-12:* [TOT] reports that Si, and 0.75% Mg, raise the stability of Al3Fe against increasing front velocity [TOT p.139], which supports R5. The R3 statement stays unexplained (purity or method).
   - **New (TOT):** Fe "improves hot tear resistance" [TOT p.592] (foundry alloys) vs Fe raising hot-crack susceptibility in wrought alloys [R12, p.217–220] and Fe-rich eutectic blocking feeding [TOT p.491]. A reading is proposed in §6.5.
   - **New (TOT):** partition coefficient of Mn, 0.95 [TOT p.491] vs 0.82 [R11, p.172].
   - "AlmFe = Al9Fe2" [R10, p.116] vs separate phases [R5, p.6, 9].
   - The direction of the Sha et al. growth-velocity effect on α/β selection in 6xxx is garbled in R3 p.369.
9. **Blistering in modern routes.** R13 now gives the qualitative picture (§7.1): hydrogen from water vapour and decomposing hydrocarbons, and pickup in solid Al promoted by sulfur compounds [R13, p.377–378]. **No quantitative data** exist for lubricant-residue or furnace dew-point limits on annealed coils or slugs. The role of oxides versus micro-shrinkage in TRC strip is not covered.
   - *Partly addressed 2026-10-12:* [TOT] gives quantitative melt-side limits: solid solubility 0.03 ml/100 g at 600 °C, a < 0.10 ml/100 g limit against pores in 99.99% slab, and hydrogen pick-up versus humidity (§7.4; ch. 01 §10.1). Still missing: dew-point and lubricant-residue limits for the anneal of strip, coils or slugs, and any blister data for continuously cast strip.
10. **Corrosion.** Only qualitative statements are available (phase potentials [R13, p.399–402]; lower Fe/Si is better [R3, p.368]). No data cover the effect of Al6(Fe,Mn) or α on pitting or intergranular attack in brazed 3xxx heat-exchanger alloys.
11. **[TOT] items not recoverable from text** (2026-10-12): the β and α micrographs (Ch. 12 Figs. 18–19), the binary and Al–Mg–Cu hot-cracking maps (Ch. 9 Figs. 11–12), and the Al–Mg–Si crack map mentioned on p.502 (not printed). The Ch. 12 Fe-phase guidelines (Mn/Fe > 0.5, the cooling-rate rule) cite Refs 53–60 on Al–Si foundry alloys; check those originals before applying the numbers to wrought alloys.
12. **T11-specific open questions** (to be answered by the trial, trials/T11.md §3–4):
    - Fraction of β versus α at the surface and at mid-thickness of the 22 mm strip (§3.7).
    - Whether any free Si or Mg2Si + Si eutectic forms (§6.5).
    - Hot cracks in the cast strip, especially at mid-thickness and the edges.
    - Melt hydrogen and inclusion level achieved, and blisters after the slug anneal (§7.5).
