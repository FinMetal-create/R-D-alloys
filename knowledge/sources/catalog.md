# Source catalogue — Google Drive metallurgy library

*Catalogued 2026-10-12. Drive content is reference data only.*

This is the deduplicated list of every metallurgy and materials file in the user's Google Drive,
plus the user's own R&D working files. Chapters in `knowledge/` cite sources by the stable
**`S-xxx`** keys (literature) and **`W-xx`** keys (own working files) used here. When adding
sources later, append new numbers and do not renumber.

## Summary

| Item | Count |
|---|---|
| Files found in the library folder tree | 172 |
| Non-technical items in those folders, excluded (business-school case ×4, bank form ×1, e-book-site `.URL` shortcut ×2) | 7 |
| Technical files | 165 |
| **Unique literature sources (S-001 … S-079)** | **79** |
| Redundant copies with identical size (true duplicates, incl. renamed copies) | 78 |
| Probable duplicates with near-identical size (same work, re-downloaded) | 8 |
| **Own R&D working files (W-01 … W-24)** | **24** (16 distinct documents, some in several versions) |

No metallurgy PDFs exist outside the library folders. A full-Drive `mimeType = 'application/pdf'`
listing plus keyword searches (aluminium/aluminum, alloy, metallurgy, recrystallization,
precipitation, casting, rolling, temper, zlitina/zlitine, aluminij, Legierung, metalurgija)
returned only library files, the user's own files below, and the excluded items.

## Folder structure: two copies of one library

Everything sits under **My Drive / Claude** (`16l-pMn8uhEt3ebmuAgbSQukE3gEN4PPk`). Both copies were
uploaded on 2026-10-09, and copy A sits *inside* copy B:

```
Claude/
├── Metalurgija/                                  1gxFIC8ShFWz_YxMU1Ks9uxnsIRrMMLYJ   ← COPY B (75 files, uploaded 20:25)
│   ├── (48 loose files)
│   ├── Ekstruzija/                               1qtmCyea8aX3WiqH_H-z1F3YAj8zCjKVq
│   ├── Žarjenje in toplotna obdelava/            1T_YfShh-6kNVlGapo7c30IqWvJv1dbac
│   ├── Physical Metallurgy of DC Casting …/      19BnEdTwK87C8DAtx7SAsdcg-Ebc0w92M
│   ├── Preoblikovanje materialov/                14Z1_mSkZRroOTmEMrB6HUej_VeguFYLU
│   ├── Protismerna ekstruzija/                   1By3-aX2abXW5pTrKjAFiVIpRbr_LmRCL
│   ├── TMS 2018/                                 11NXLNy1DoTc1W1ECUylV5LlH1cloPsXb
│   └── Tlačno litje/                             1PnOg6C2_RCfNRekhC5U-RdElrMCgEYUi   ← COPY A (97 files, uploaded 20:43)
│       ├── (6 loose files)
│       ├── Metalurgija-literatura/               1dl7llfYJdC6FwNAgM7ntT5ZUB8dI5QNs   ← preferred canonical location
│       │   ├── Physical Metallurgy of DC Casting …/  1d0EMX3Hk6xr8GRVrnvu0fzrY6gulwDbD
│       │   ├── Protismerna ekstruzija/           1R5x5DAmzYk3p3Mba0C-1ar9lMgzWO-I9
│       │   ├── TMS 2018/                         1llhcxiE7YssHNSlle2X10c-yXGSYvxbo
│       │   └── Preoblikovanje materialov/        1DkJOLeAJCqO9NQHEdo_9g0wgzzdbsRl3
│       ├── Aluminij/                             16AMGG1kb95R2jRg-TLLbksBwps98tukW
│       │   ├── Žarjenje in toplotna obdelava/    151MkdpvWTIJT9Hw4JkCLKGknZ5j7bERb
│       │   ├── Tlačno litje/                     10yzAu6-l7859mQoKzEMpCdD5X-IUZ3c8
│       │   └── Ekstruzija/                       1yEpYNGQ2VDcyuEyoKRUWHJQun9rvYiry
│       ├── Čakalna vrsta/ ("queue", to-read)     1ea6WBCgm9uLKWRtuggo31G0CxhIZl8JJ
│       └── nikljeve zlitine/ (nickel alloys)     1NJBt2kqlXqDee5HB_8Qk3cH8_K0xOd14
└── Metalurgija-model/                            19BkHZ_-1mtFAbKSqIJIs79NO1zLGOnIj
    └── microstructure-sim-v2.14.0/               1JYDPIh01r4ARoThY6IX4HscM3fARiPiK   ← EXCLUDED (user's stored model: code, node_modules, run CSVs)
```

Copy A is complete: it holds all 79 unique works. Copy B holds 68 of them. The 11 works found only
in copy A are S-011 (Nippon Steel), S-015 (Maggs), S-035 (AluReport EN), S-044 (Löten),
S-055 (MPMA aerosol sheet), S-063 (Segersäll), S-064 (Bombač), S-076 (Thienel), S-078
(Ishikawa/5-Whys), S-079 (`Tlačno litje.pdf` scan) and S-050 (Lehnert). Copy B holds no work
that copy A lacks. 58 canonical copies are in `Metalurgija-literatura`; the other 21 are
elsewhere in copy A.

**How duplicates were resolved.** Files with the same byte size are treated as one work, whatever
their names. For S-053, the first pages of both names were compared and match. Files whose size differs only slightly (≤ 0.5 %) and whose names or first
pages match are listed as *probable* duplicates. The canonical copy is the one in
`Metalurgija-literatura` (or its subfolders) where one exists, otherwise the copy in copy A
(`Tlačno litje/…`), otherwise copy B. All other IDs go in the *Duplicate IDs* column.

**Columns.** *Title* gives the Drive file name in `code`, then the identified work. Authors and
venues come from the file's first page (Drive text snippet) where the name was unclear, and from
the file name otherwise. *Lang* is the language of the content where checked, otherwise a guess
from the title. *Size* is in MB (10^6 bytes).

## Literature sources (79 unique)

### Solidification & DC casting (11)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-001 | `62816_fm.pdf` → Eskin, D.G. — *Physical Metallurgy of Direct Chill Casting of Aluminum Alloys* (CRC Press / Taylor & Francis, 2008), front matter + contents | EN | 0.75 | [15ShzCo5bBJyg0SE7AD50Sst9z_F0v91Z](https://drive.google.com/file/d/15ShzCo5bBJyg0SE7AD50Sst9z_F0v91Z/view) | 1ejdasPz9QY6U1cZsBXZPa4BSiCgFMqpz |
| S-002 | `62816_ch01.pdf` → Eskin (2008) DC-casting book — Chapter 1 | EN | 0.96 | [1T5sCpnxZxg9BFtPmyRqH7zqZjKy0UczL](https://drive.google.com/file/d/1T5sCpnxZxg9BFtPmyRqH7zqZjKy0UczL/view) | 1RKgHgBQNUsxDUKozj5HNPjXShRoN7p8f |
| S-003 | `62816_ch02.pdf` → Eskin (2008) DC-casting book — Chapter 2 | EN | 2.03 | [1MBeZaNbetcIq6Xjcoj2Y56AW9wZPwcb2](https://drive.google.com/file/d/1MBeZaNbetcIq6Xjcoj2Y56AW9wZPwcb2/view) | 1Q05A70dmlMchLLgbG2EGBQUtohCe2DFc |
| S-004 | `62816_ch03.pdf` → Eskin (2008) DC-casting book — Chapter 3 | EN | 2.53 | [1t1R4f3IKhRkid18JooQCMoR5PNhbjsZE](https://drive.google.com/file/d/1t1R4f3IKhRkid18JooQCMoR5PNhbjsZE/view) | 14SFlUWZp9MOu5mkeeuNjsx9jeVD9SDNX |
| S-005 | `62816_ch04.pdf` → Eskin (2008) DC-casting book — Chapter 4 | EN | 1.55 | [1LGAwTkLvuT29WFaaXDgYcKRN31PhMQ7v](https://drive.google.com/file/d/1LGAwTkLvuT29WFaaXDgYcKRN31PhMQ7v/view) | 1kZP6-C_NKVllO1oODJWD-5m2BZI6Ib1J |
| S-006 | `62816_ch05.pdf` → Eskin (2008) DC-casting book — Chapter 5 | EN | 2.56 | [1tYAv85fpfmJ7f5wNBPi3kvky3b1H4ps4](https://drive.google.com/file/d/1tYAv85fpfmJ7f5wNBPi3kvky3b1H4ps4/view) | 1SywPbjKbM3npm4qS-CB3Aw-dakzJYeIt |
| S-007 | `Crcking during csting of hight strenght Al alloys.pdf` → Lalpoor, M. — *Study of Cold Cracking during DC-casting of High Strength Aluminum Alloys* (PhD thesis, TU Delft / M2i, 2010) | EN | 13.88 | [1gLPBgQq0_DICNYuWwMELjPhplKi3aBIo](https://drive.google.com/file/d/1gLPBgQq0_DICNYuWwMELjPhplKi3aBIo/view) | 1ER-5OPOLeTfp--AtIWej9HZ5rzwgQwOq |
| S-008 | `Pre-course-reading.pdf` → Phillion, A.B. & Dantzig, J. — Pre-course reading for ESI's Solidification Course | EN | 0.64 | [1PWxfw0Wekow6uLkk0TBx-OOxw8oaY001](https://drive.google.com/file/d/1PWxfw0Wekow6uLkk0TBx-OOxw8oaY001/view) | 1hQfyuXV0xIOoN7NvsW39mlj5q9r7zIM2 |
| S-009 | `Blister formation.pdf` → "Blister Formation in Rolled Aluminum" — journal article linking ingot discontinuities / gas to blisters in rolled sheet (author not legible in OCR) | EN | 0.63 | [1ng77xl3C81ziOj-F_orl5D5ksh0ryrpZ](https://drive.google.com/file/d/1ng77xl3C81ziOj-F_orl5D5ksh0ryrpZ/view) | 1QtwlU4u3he2eroL4LrynS4Ov_TMfgGJo |
| S-010 | `50291676-Continuous-Roll-Casting-of-Aluminium.pdf` → Krstić Vukelja, E., Duplančić, I. & Lela, B. — "Continuous roll casting of aluminium alloys – casting parameters analysis", *Metalurgija* (c. 2010) | EN | 0.48 | [16xRFXhETDI8_5cYr9x9tuBxUueKkY9q0](https://drive.google.com/file/d/16xRFXhETDI8_5cYr9x9tuBxUueKkY9q0/view) | 10tB40sxbCrc2bOIt0Rh3rvYVbPrLE4Ix |
| S-011 | `nippon steel center line segreggations.pdf` → Miyazaki, M., Isobe, K. & Murao, T. — "Formation mechanism and modeling of centerline segregation", *Nippon Steel Technical Report* No. 104 (2013) — steel continuous casting | EN | 2.57 | [1QsCpR-VkKpP5rtYTqd7QB7P5IAUzFJPg](https://drive.google.com/file/d/1QsCpR-VkKpP5rtYTqd7QB7P5IAUzFJPg/view) | — |

### Intermetallics & phase diagrams (4)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-012 | `Chapter 1 - Alloys of the Al_Fe_Mn_Si System.pdf` → Belov, N.A., Eskin, D.G. & Aksenov, A.A. — *Multicomponent Phase Diagrams: Applications for Commercial Aluminum Alloys* (Elsevier, 2005), Ch. 1 "Alloys of the Al–Fe–Mn–Si System" (book identified from ISBN 978-0-08-044537-3 in the PII) | EN | 2.67 | [1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD](https://drive.google.com/file/d/1vmvHnMKYNqQot_rqfrlOjEJcG7885YjD/view) | 1cxp7nmBMm86c8YcgZIeyQQVuLiomxGzC |
| S-013 | `Fazni diagram AlfeSi.pdf` → Ghosh, G. — "Al–Fe–Si (Aluminium – Iron – Silicon)", Landolt-Börnstein New Series IV/11A2, Ternary Alloy Systems (MSIT). *Drive title is Slovenian ("phase diagram AlFeSi")* | EN | 0.56 | [1ziJfaBKy6slqy6sR6DSdjzImN8UZ4SJz](https://drive.google.com/file/d/1ziJfaBKy6slqy6sR6DSdjzImN8UZ4SJz/view) | 1F78HNS14UJ-uJqhaLVGVGn5VrdN1JzIO |
| S-014 | `AlFeSi faze v gnetnih zlitinah.pdf` → "Determination of α- and β-AlFeSi phases in wrought aluminium alloys" — journal article on telling α/β-AlFeSi apart in 6xxx billets (author not identified). *Drive title is Slovenian* | EN | 1.81 | [10S5-K7dD0IZZXepBfMi_hk0S8Rxzra5C](https://drive.google.com/file/d/10S5-K7dD0IZZXepBfMi_hk0S8Rxzra5C/view) | 1KbpsttUw23k46L8VNJeRorLzBht52O4s |
| S-015 | `fir-tree zone.pdf` → Maggs, S.J. — *Intermetallic Phase Selection in Dilute Al–Fe–Si Alloys* (PhD thesis, Univ. of Leeds, 1996) — fir-tree zone in DC-cast 1xxx ingots | EN | 22.34 | [1Dtgr_aj458cP3-2WGafeXu7LKDYNklva](https://drive.google.com/file/d/1Dtgr_aj458cP3-2WGafeXu7LKDYNklva/view) | — |

### Recovery / recrystallization / grain growth (4)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-016 | `85721252-Ebooksclub-org-Re-Crystallization-and-Related-Annealing-Phenomena-Second-Edition.pdf` → Humphreys, F.J. & Hatherly, M. — *Recrystallization and Related Annealing Phenomena*, 2nd ed. (Elsevier, 2004) | EN | 12.66 | [1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w](https://drive.google.com/file/d/1QvLAUS_TAp3Pqpqsac2bpceRzsEw7w6w/view) | 17tHwICnSZ9xIRALcJHIYXZhVs9mQc-1D |
| S-017 | `CHARACTERISATION AND MODELLING OF STATIC.pdf` → Junit, M.A. — "Characterisation and Modelling of Static Recovery Process of Aluminum Alloy" (BEng report, Universiti Malaysia Pahang, 2008; Friedel recovery model) (also stored as `MODELLING OF STATIC recovery.pdf`). *Two Drive names, identical size* | EN | 2.35 | [1ANzZHinT6byugfeZkXbsNETvmKgc-phK](https://drive.google.com/file/d/1ANzZHinT6byugfeZkXbsNETvmKgc-phK/view) | 1JT7HIwZIGuC5WeJbk1ntYwBd_QJWQbik, 1nZnVC4O3JbimZfTQ8ZZGf1tUrEVT5cdO, 1iJJQ_6zY1ywpKQ80_Qh313_beb1_pXzC |
| S-018 | `simulation-of-recrystallization(1).pdf` → "Modeling recrystallization and grain growth phenomena" — book-chapter excerpt (style suggests D. Raabe; not verified) | EN | 0.30 | [1MN7_BcrlAvTxyiDd_D2MQge-efotHMS6](https://drive.google.com/file/d/1MN7_BcrlAvTxyiDd_D2MQge-efotHMS6/view) | 1vgrqK9ATz72KLNqgr296JDculpuf6AVT |
| S-019 | `Waermebehandlung-und-Rekristallisation-von-Aluminium.pdf` → "Wärmebehandlung und Rekristallisation von Aluminium" — university lab-practical script (Praktikum G3/MW2) | DE | 0.80 | [116AVCkaosrrRKG94_GFBXrHYE3R1EzC4](https://drive.google.com/file/d/116AVCkaosrrRKG94_GFBXrHYE3R1EzC4/view) | 1Yg_fXMRWuphxV1O-kzZ2ujstKMcWbmcy |

### Precipitation / dispersoids / alloying elements (8)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-020 | `Clusters in Al alloys.pdf` → Ivanov, R. — *Solute clustering in multi-component aluminium alloys* (PhD thesis, Univ. Grenoble Alpes, 2017) | EN | 13.30 | [1x56HZKJZm77CxOCd9uFSz4Zlj6UclDIr](https://drive.google.com/file/d/1x56HZKJZm77CxOCd9uFSz4Zlj6UclDIr/view) | 1Om9K9BPTMDIWuzmVyAIqEtz-s_znmRh3 |
| S-021 | `Royset-2005-Scandium Aluminium.pdf` → Røyset, J. & Ryum, N. — "Scandium in aluminium alloys", *International Materials Reviews* (2005), review | EN | 0.68 | [1A_yvqnRq-o1I53m3tieuVp4Sq5zUu1iL](https://drive.google.com/file/d/1A_yvqnRq-o1I53m3tieuVp4Sq5zUu1iL/view) | 12u6Dx6N6_8waemZnK1w4W899FZMbhbwI |
| S-022 | `Scandium and Aluminum alloys.pdf` → Røyset, J. (Hydro Aluminium R&D) — "Scandium in aluminium alloys overview: physical metallurgy, properties and applications" (short overview paper). *Different file from the 2005 review* | EN | 0.12 | [1FizSqhIa3XAhPQpZYt0maHVsHdEsKrhW](https://drive.google.com/file/d/1FizSqhIa3XAhPQpZYt0maHVsHdEsKrhW/view) | 181OcJfn-O92WDSB8CC4P5RVK2rEY5WfI |
| S-023 | `A new model for prediction of dispersoid percipitation in Al, zr, sC alloys.pdf` → Robson, J.D. — "A new model for prediction of dispersoid precipitation in aluminium alloys containing zirconium and scandium" (*Acta Materialia*, 2004; Kampmann–Wagner model for Al3(Sc,Zr)) | EN | 0.36 | [1hVcF0Jxx5hg5BVVJJjPNyGk8o0oslgRk](https://drive.google.com/file/d/1hVcF0Jxx5hg5BVVJJjPNyGk8o0oslgRk/view) | 12-d1td1LKVA0_Y3G8G9-o5fB0s_dit2g |
| S-024 | `Effects of Zr and Sc on Aluminium.pdf` → Williams, C.R. — *The Effects of Scandium and Zirconium Additions on Aluminum Mechanical Properties, Post-Braze Grain Structure, and Extrusion* (MSc thesis, Ohio University, 2012) | EN | 1.56 | [1MYsjf2OwlDfrOtnb1zQas-DV9wfunqne](https://drive.google.com/file/d/1MYsjf2OwlDfrOtnb1zQas-DV9wfunqne/view) | 13YceZlkdfhX1pnDQAEEBGctpdCkUh1g4 |
| S-025 | `Effects of Zr and Sc on al4Cu1,5Mg.pdf` → "Effects of Zr and Sc on Al-4Cu-1.5Mg" — author and source not identified (first page has no text layer). *Needs inspection* | EN? | 5.52 | [1jJDzvzs7Q3LI_cWkEEN0X3DJ45ERtfcE](https://drive.google.com/file/d/1jJDzvzs7Q3LI_cWkEEN0X3DJ45ERtfcE/view) | 1i2i85xzNUoWij5Ju97s5dEcPxh_Bj-64 |
| S-026 | `Influence of alloying elements.pdf` → Rana, R.S., Purohit, R. & Das, S. — "Reviews on the influences of alloying elements on the microstructure and mechanical properties of aluminum alloys and aluminum alloy composites", *IJSRP* 2(6) (2012) | EN | 0.76 | [1eenW1k-qr4_bAY3wtnZBPPDu-uDBzGJC](https://drive.google.com/file/d/1eenW1k-qr4_bAY3wtnZBPPDu-uDBzGJC/view) | 1ZDpW7-gxHNrazzRH3uXMf1LKhQ5_Eq9I |
| S-027 | `Al_Mo.pdf` → Zaid, A.I.O. & Atieh, A.M. — "Effect of molybdenum addition on aluminium grain refined by titanium … as cast and after ECAP", *IOP Conf. Ser.: Mater. Sci. Eng.* 60 (2014) 012052 | EN | 1.09 | [1ON8iVgDGl7jAcEPzomcKjFVIabk8ld_Q](https://drive.google.com/file/d/1ON8iVgDGl7jAcEPzomcKjFVIabk8ld_Q/view) | 1zz13dzs_bHw0nZDri9DVZ6LKDNpGmo7z |

### Aluminium alloy systems / tempers / properties (17)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-028 | `115132137-Light-Alloys.pdf` → Polmear, I.J. — *Light Alloys: From Traditional Alloys to Nanocrystals*, 4th ed. (Butterworth-Heinemann, 2006) | EN | 9.68 | [1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w](https://drive.google.com/file/d/1deTdBlvWinXqm3SyrnA7nrAXfc_V3d1w/view) | 1UDBZmfTtvO9a17fLOgAzBEqZEzgDRH77 |
| S-029 | `ASM Handbook of Aluminium vol. 1.pdf` → Totten, G.E. & MacKenzie, D.S. (eds.) — *Handbook of Aluminum, Vol. 1: Physical Metallurgy and Processes* (Marcel Dekker, 2003) (also stored as `Alminium.pdf`). *Not an ASM handbook despite the Drive name; "Alminium.pdf" is the same file* | EN | 17.66 | [1UsZI7XP3jC8Pu0Mjiqksj2dQEmozI2O2](https://drive.google.com/file/d/1UsZI7XP3jC8Pu0Mjiqksj2dQEmozI2O2/view) | 1uBiRXgXUTxHFChG8lksNf7wDKb3rdBzz, 1wK0HcjucesNhXYzMEDLeRzlfawRuVltq, 1LNDwz9XSVn51tWynCZUvGvbdzEDR23K3 |
| S-030 | `130151317-Introduction-to-Aluminum-Alloys-and-Tempers-pdf.pdf` → Kaufman, J.G. — *Introduction to Aluminum Alloys and Tempers* (ASM International, 2000) | EN | 6.09 | [1cmbbWXoyfHTTlgSDdeFCLHY6IrFl9zRl](https://drive.google.com/file/d/1cmbbWXoyfHTTlgSDdeFCLHY6IrFl9zRl/view) | 1qFZVPgWjRJsDruMotiB6Fg1MVX9Lamrp |
| S-031 | `Aluminum and Aluminum Alloys Davis.pdf` → Davis, J.R. — "Aluminum and Aluminum Alloys", in *Alloying: Understanding the Basics* (ASM International, 2001), pp. 351–416 | EN | 0.54 | [1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z](https://drive.google.com/file/d/1Pp-8Sal4UJRHtlf0r_p1vlinF9sXkO_Z/view) | 1sryuumwmAN83i_NUASf5XkOJvYDMTiSb; probable (near-identical size): 1dRjmIiKwO5ywFQtKHH2AH9iv4aJlFryP (0.536 MB) |
| S-032 | `volume_2_-_properties_and_selection_nonf.pdf` → *ASM Handbook Vol. 2: Properties and Selection: Nonferrous Alloys and Special-Purpose Materials* (ASM International, 1990) | EN | 52.57 | [1Q8XgNClY79wSJvgYi_NaW8KR9hkDjaSP](https://drive.google.com/file/d/1Q8XgNClY79wSJvgYi_NaW8KR9hkDjaSP/view) | 13NTIfbSZDQr93V0M2G0dtTeclSTIvrzv |
| S-033 | `Aalco-Metals-Ltd_Aluminium-Alloy-Temper-Designations_93.pdf` → Aalco Metals Ltd — Aluminium alloy temper designations (datasheet) (also stored as `Aalco-Metals-Ltd_Aluminium-Alloy-Temper-Designations_93 (1).pdf`) | EN | 0.16 | [1xQKanAcmXXqFlEy7NBRPX274_zjaYnil](https://drive.google.com/file/d/1xQKanAcmXXqFlEy7NBRPX274_zjaYnil/view) | 1AQMkYdb4IqZwynHRPlBP4283VFHoTMZ_, 1GoWOVspOdkS7cuAZYJooRfAMqg1Xuw6d, 1Mxf6KRXTBDKj92GSPhQSvajor4TTdnTc |
| S-034 | `Aalco-Metals-Ltd_Aluminium-Alloy-5754-H111-Treadplate_142.pdf` → Aalco Metals Ltd — Aluminium alloy 5754-H111 treadplate (datasheet) | EN | 0.07 | [1knDlSBj70pPp_aybepmNcTgB4lqsB085](https://drive.google.com/file/d/1knDlSBj70pPp_aybepmNcTgB4lqsB085/view) | 1BfCncyg5VJaz9SOK8yMPJFO-YuYr9L5A |
| S-035 | `AR-2014-1-EN-S10-15-Waermebehandlung.pdf` → *AluReport* 1/2014, pp. 10–15 — article on heat treatment of aluminium (English edition) | EN | 2.56 | [1hvicHsqiMWT-C-hsvbMlLlTw0eA6V4ko](https://drive.google.com/file/d/1hvicHsqiMWT-C-hsvbMlLlTw0eA6V4ko/view) | — |
| S-036 | `AR-2014-1-DE-S10-15-Waermebehandlung.pdf` → *AluReport* 1/2014, pp. 10–15 — "Wärmebehandlung" (German edition of the same article) | DE | 2.57 | [1D9DRhJTjetqwamIhaHLaekopweS_mFVt](https://drive.google.com/file/d/1D9DRhJTjetqwamIhaHLaekopweS_mFVt/view) | 1YMK9IxIy3GQrMofT12_Fbg-DLVVfMBVV |
| S-037 | `W7_Waermebehandlung_von_Aluminiumlegierungen.pdf` → Aluminium-Zentrale — Merkblatt W7 *Wärmebehandlung von Aluminiumlegierungen* | DE | 0.53 | [1fEJ6FsDzCDqPZRloFgGFYV-RNudGVd9Y](https://drive.google.com/file/d/1fEJ6FsDzCDqPZRloFgGFYV-RNudGVd9Y/view) | 1XDWQVMOpEXBKSuI7eYZoZFqaoEsGWgoa |
| S-038 | `17_Aluminium.pdf` → "17 Aluminium" — German lecture-notes chapter (EN 573 designations, tempers, hardening mechanisms) | DE | 0.73 | [10KjyazZPV1_BAKghuxzfPlPF2I2PKp5f](https://drive.google.com/file/d/10KjyazZPV1_BAKghuxzfPlPF2I2PKp5f/view) | 1gUrZuhyO16BW12xl44wb4IzOKPAVZLzi |
| S-039 | `Aluminium und seine Legierungen.docx` → "Aluminium und seine Legierungen" (.docx notes compiled from Wollmann, M., Westsächsische Hochschule Zwickau) | DE | 0.07 | [14XZB-lvAZ7cff2kpZgfnvJV3qYvKUOyO](https://drive.google.com/file/d/14XZB-lvAZ7cff2kpZgfnvJV3qYvKUOyO/view) | 1P-3I8xc6TDgVa5ey-sqXZWykJZfvzKPI |
| S-040 | `Al alloys and Mg alloys.pdf` → "Aluminium alloys and magnesium alloys" — lecture slides (PowerPoint export) | EN | 1.84 | [1HhefbsqmLFlItUqRitymP5DGujJU8RIb](https://drive.google.com/file/d/1HhefbsqmLFlItUqRitymP5DGujJU8RIb/view) | 1370VJG2h2zf0ZJ1Lt3hImoBwv2s86NfX |
| S-041 | `116748406-Aluminium-Alloys.pdf` → Dwight, J. — *Aluminium Design and Construction* (E & FN Spon, 1999) | EN | 3.15 | [158y2YRjC0dWVgkEgUCsb0DZ8LAqp2BbY](https://drive.google.com/file/d/158y2YRjC0dWVgkEgUCsb0DZ8LAqp2BbY/view) | 1gDaZXnACgkZvyNHVM4jgC7Df4YtWceyr |
| S-042 | `lastnosti aluminija.pdf` → TALAT Lecture 1101 — *Resources and Production of Aluminium* (Budd, G., EAA, 1999). *Drive title is Slovenian ("properties of aluminium")* | EN | 0.72 | [18RcaS3-hFM9Wts56lekVpEoUht44bmE7](https://drive.google.com/file/d/18RcaS3-hFM9Wts56lekVpEoUht44bmE7/view) | 1yLpqt5gZhIqd5gXrbYeQhZzJ8h-woYLv |
| S-043 | `uporaba v transportu.pdf` → European Aluminium Association — *Aluminium in Commercial Vehicles*. *Drive title is Slovenian ("use in transport"); the 3.64 MB file with the same name is a different work (Sillekens, S-053)* | EN | 3.28 | [1nKCtal3NFz7WMlwE4ijgHl0UwMeCMHJp](https://drive.google.com/file/d/1nKCtal3NFz7WMlwE4ijgHl0UwMeCMHJp/view) | 10khW7r80NUvR21H0FheZupOGT0mIVJMw |
| S-044 | `L_ten_v.Al_und_Al-Legierungen.pdf` → "Löten von Aluminium und Aluminiumlegierungen" — brazing/soldering of Al (Ögussa Löttechnik, C. Apeltauer) | DE | 0.38 | [1nHO48mMTKaEgu8F_9ELnpTFwh_D14g4V](https://drive.google.com/file/d/1nHO48mMTKaEgu8F_9ELnpTFwh_D14g4V/view) | — |

### Thermomechanical processing (rolling / extrusion / forming) (16)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-045 | `Professor Terry Sheppard (auth.)-Extrusion of Aluminium Alloys-Springer US (1999).pdf` → Sheppard, T. — *Extrusion of Aluminium Alloys* (Kluwer / Springer, 1999) (also stored as `Extrusion Of Aluminium Alloys.pdf`) | EN | 10.51 | [195YE0KUFE-yMliXyp304IqoaSdvnxKVU](https://drive.google.com/file/d/195YE0KUFE-yMliXyp304IqoaSdvnxKVU/view) | 1X_XMYDmHZsR3ctJdKvvGgWazOZm4zBHo; probable (near-identical size): 1pJoblJP3s9o7Z_WgFM9dhMmepLi7POET (10.463 MB), 16ZmIrLJKSl6_2eEq9Df4Hm6TeW9Tki0o (10.463 MB) |
| S-046 | `3c-handbook-metal-forming.pdf` → Schuler GmbH — *Metal Forming Handbook* (Springer, 1998) (also stored as `vasevska.pdf`) | EN | 28.58 | [1n5Yidy74bZxj6ZifvCNtq0iRtk2nyh43](https://drive.google.com/file/d/1n5Yidy74bZxj6ZifvCNtq0iRtk2nyh43/view) | 1teLupkO7LoS1-FOQ94WnIhxBeC0kgAwz; probable (near-identical size): 1vbIfSVGbqJfheI2yJKigh5nZAdIK7KI4 (28.583 MB), 19b_ebuImrSgYo2dTvHZQMUxuAaVKJUw_ (28.583 MB) |
| S-047 | `Rolling_Aluminum_From_The_Mine_Through_The_Mill.pdf` → The Aluminum Association — *Rolling Aluminum: From the Mine Through the Mill* | EN | 7.19 | [1w70bnhbLUlg5Tg4tlFIa0pVEI58GRfht](https://drive.google.com/file/d/1w70bnhbLUlg5Tg4tlFIa0pVEI58GRfht/view) | 1i-3uwU8kh3uFXgSm5umZg3Hu0YSH4iAg |
| S-048 | `155680328-Rolling.pdf` → Schröder, K.H. — *A Basic Understanding of the Mechanics of Rolling Mill Rolls* (ESW e-book, 2003) | EN | 3.81 | [1I9Qa_iFiOPw5DMU6sHFW6YAYblFC9Qyu](https://drive.google.com/file/d/1I9Qa_iFiOPw5DMU6sHFW6YAYblFC9Qyu/view) | 1_RYU5z2zcnXb6lVy8-jBtYe8JhjVc8-H |
| S-049 | `Rolling.pdf` → Dünckelmeyer, M.J. — *Ursachen des Walzenaufreißens in Warmbreitbandstraßen* (Dr.-Ing. dissertation, TU München, 2012) — work-roll cracking in hot strip mills | DE | 12.36 | [1ATs2FwzOZ5rq-e97GKKUInQJNSG0lffP](https://drive.google.com/file/d/1ATs2FwzOZ5rq-e97GKKUInQJNSG0lffP/view) | 1d61_XMFJxjja9VBxkGybWRpdXiJ_FMr9 |
| S-050 | `MET_45_3_169_178_Lehnert.pdf` → Lehnert, W., Lehnert, R. & Kawalla, R. — "Herstellung von hochwertigen Bändern und Blechen aus Aluminiumwerkstoffen", *Metalurgija* 45(3) (2006) 169–178 | DE | 2.84 | [18QdmKaIrJQ-coTXVt51rQ5wZqpVDgEdC](https://drive.google.com/file/d/18QdmKaIrJQ-coTXVt51rQ5wZqpVDgEdC/view) | — |
| S-051 | `vasevska.pdf` → Vasevska, T. — "Utrjevanje aluminija in zlitin pri vzdolžnem hladnem valjanju" (Hardening of aluminium and alloys by longitudinal cold rolling), *Materiali in tehnologije* 38(3–4) (2004) 191. *Small "vasevska.pdf"; the 28.6 MB file with the same name is the Schuler handbook* | SL | 0.37 | [1wpVR73nujVXO1OfmvV57CzuvwR__bdRc](https://drive.google.com/file/d/1wpVR73nujVXO1OfmvV57CzuvwR__bdRc/view) | 1l6puxca0vGrU3cSTEGgpRe5lnCeFPaMM |
| S-052 | `uporabno del-2.pdf` → Ryen, Ø. — *Work Hardening and Mechanical Anisotropy of Aluminium Sheets and Profiles* (Dr.Ing. thesis, NTNU, 2003). *Drive title is Slovenian ("useful part 2")* | EN | 11.22 | [1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_](https://drive.google.com/file/d/1Turdjqsi3pv1XbwGMdz6x7NKu-GnADj_/view) | 1UzIUO6x8LEca1klH_1--rFxKuoXwsVhI |
| S-053 | `uporaba v transportu.pdf` → Sillekens, W.H. — *Backward Can Extrusion and Materials Behaviour* (PhD thesis, TU Eindhoven, 1992; DOI 10.6100/IR374925) (also stored as `374925(1).pdf`, `374925.pdf`). *Two copies are misnamed "uporaba v transportu.pdf"; the 3.28 MB file with that name is a different work (EAA brochure, S-043)* | EN | 3.64 | [19TZFzxjO1cFP7k7mwdfrpcEXIbSRYG2z](https://drive.google.com/file/d/19TZFzxjO1cFP7k7mwdfrpcEXIbSRYG2z/view) | 1FgOlZBrGWWfSCsEn9pe44eb10MEYShxy, 1u7fg8Mrxj0ha6NwDE3Z79OHEJ-VLEw2u, 1n2OYmFBOJJitAFgIRO00wbGtSTIEMvWa |
| S-054 | `document.pdf` → Butler, J.F. Jr. (Alcoa) — "Alcoa Micromill: breakthrough technology for next-generation auto sheet" (presentation, 2015) | EN | 1.74 | [1OYezPC_Eif_mKOTmq2xeExuqfcsTai1N](https://drive.google.com/file/d/1OYezPC_Eif_mKOTmq2xeExuqfcsTai1N/view) | 1OVrJiAPc6NgH-xLjwHnzv7EIIe7s9jhp |
| S-055 | `aerosolaluminium.pdf` → MPMA — "How aluminium aerosol cans are made" (slug punching and impact extrusion, info sheet) | EN | 0.50 | [1Ul9kcbJAllC4ufhIsV3Xr2tkhjW6TBSW](https://drive.google.com/file/d/1Ul9kcbJAllC4ufhIsV3Xr2tkhjW6TBSW/view) | — |
| S-056 | `AG-Aerosol-Brochure-1.pdf` → Ardagh Group — *Metal Packaging Solutions: Steel and Aluminium Aerosols* (brochure) (also stored as `AG-Aerosol-Brochure.pdf`) | EN | 2.70 | [1C_DUB748Ikw3LP4pcp97tQmoCn5js5uF](https://drive.google.com/file/d/1C_DUB748Ikw3LP4pcp97tQmoCn5js5uF/view) | 1rNQ3PgzjIzSwg4AchwqvIRGVib-Yqg21; probable (near-identical size): 1YbL_Jcz3iDYJrkWS8PtJ3G7Wxk9c6fAg (2.710 MB) |
| S-057 | `MH_Can_Line_CMC200_250_14.pdf` → Mall + Herlan — CMC 200/250 monobloc aerosol-can production lines (brochure) | EN | 4.71 | [1MFEG_JSZSKkmzXpRJ5lF58iiv7MBxnvX](https://drive.google.com/file/d/1MFEG_JSZSKkmzXpRJ5lF58iiv7MBxnvX/view) | 1MEEircU49oe_v92BCMCyQ_JpJEknQi8w; probable (near-identical size): 1UtMIvNuZr-S0_0qWbxTDLb_kYopOBFov (4.708 MB) |
| S-058 | `N40.2 english.pdf` → Hinterkopf — N40.2 necking machine for aluminium cans (brochure) | EN | 1.90 | [1rox7kzRaTGK_jAjUQrKQIBs06yvEmHQ_](https://drive.google.com/file/d/1rox7kzRaTGK_jAjUQrKQIBs06yvEmHQ_/view) | 1Vo8Qfz61DElfkQxh6LuqIZ1TcJBueVtt; probable (near-identical size): 1lr4XHFvx7cxl3Q6roZ0Xnb94LYWMix5v (1.905 MB) |
| S-059 | `1-basic-punching-theory-tt-2010-62-728.jpg` → "Basic punching theory" — slide image (slide 62). *Image (.jpg)* | EN | 0.06 | [13cVKT8DZmNansFOdGiUpKPv8JrAiXkNY](https://drive.google.com/file/d/13cVKT8DZmNansFOdGiUpKPv8JrAiXkNY/view) | 1y8qqHZdpvItRi33fmje4_WvyMhL-U6OL |
| S-060 | `1-basic-punching-tt-2010-63-728.jpg` → "Basic punching" — slide image (slide 63). *Image (.jpg)* | EN | 0.06 | [15cVOvSbU5hiY7Gkdp7PZg2cOd1ib6CHM](https://drive.google.com/file/d/15cVOvSbU5hiY7Gkdp7PZg2cOd1ib6CHM/view) | 1yeONa3Nz4DnxFtNP1iphikLJCNcXdo8I |

### Other alloy families (steel, Ni, Mg, MMC) (6)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-061 | `A Farrar-The Alloy Tree_ A Guide to Low-alloy Steels, Stainless Steels and Nickel-base Alloys (2004).pdf` → Farrar, J.C.M. — *The Alloy Tree: A Guide to Low-Alloy Steels, Stainless Steels and Nickel-Base Alloys* (Woodhead, 2004) | EN | 0.74 | [1DI6Ec7thYXVhQ_z0ApTBihCCkJy3Heve](https://drive.google.com/file/d/1DI6Ec7thYXVhQ_z0ApTBihCCkJy3Heve/view) | 1gyTCX1WrQYlqq8FDE4offMd10Ei-PkK6 |
| S-062 | `John L. Everhart P. E. (auth.)-Engineering Properties of Nickel and Nickel Alloys-Springer US (1971).pdf` → Everhart, J.L. — *Engineering Properties of Nickel and Nickel Alloys* (Springer US, 1971) | EN | 4.97 | [1yPxmtJr-sKsxhNlEpkEl6xINfBRUg2k_](https://drive.google.com/file/d/1yPxmtJr-sKsxhNlEpkEl6xINfBRUg2k_/view) | 1PvycSDmFu5AXSCtxg_SW4SRFGRgaOfZ_ |
| S-063 | `Nickel supper alloys.pdf` → Segersäll, M. — *Nickel-Based Single-Crystal Superalloys: the crystal orientation influence on high temperature properties* (Licentiate thesis, Linköping Univ., 2013) | EN | 0.62 | [1d1gAovTKmXwAhqINacTcB-qS5fyz6aYT](https://drive.google.com/file/d/1d1gAovTKmXwAhqINacTcB-qS5fyz6aYT/view) | — |
| S-064 | `Microstructure_URN-NBN-SI-DOC-OFLHAUYU.pdf` → Bombač, D., Fazarinc, M., Kugler, G. & Spaić, S. — "Microstructure development of Nimonic 80A superalloy during hot deformation", *RMZ – Materials and Geoenvironment* 55(3) (2008) 319–328 (also stored as `Microstructure_URN-NBN-SI-DOC-OFLHAUYU (1).pdf`) | EN | 1.13 | [1K3jZ3TiJKKk54DiBq9dWya51PKsf_Zq8](https://drive.google.com/file/d/1K3jZ3TiJKKk54DiBq9dWya51PKsf_Zq8/view) | 1g9gN7kJ9YOu60AhuhnL4ZdhiIBfGj5Xl |
| S-065 | `MAGNESIUM TECHNOLOGY.pdf` → TMS 2018 — *Magnesium Technology 2018* (proceedings) | EN | 35.81 | [1ZE6TQOXNnemhdi165P__jiKo9GGRVJtQ](https://drive.google.com/file/d/1ZE6TQOXNnemhdi165P__jiKo9GGRVJtQ/view) | 1Gy8JWLb2GK6sBmpYib8b3EjyIk7g_kmi |
| S-066 | `METAL-MATRIX COMPOSITES.pdf` → TMS 2018 — *Metal-Matrix Composites* (symposium proceedings) | EN | 11.31 | [1Ru1LakxdwSSI0o8r_BvToL2Y3cd3I3Kw](https://drive.google.com/file/d/1Ru1LakxdwSSI0o8r_BvToL2Y3cd3I3Kw/view) | 1DTZVVIdXUkHzLRJ9azn4gF2etEmXgg8u |

### Conference proceedings / general (12)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-067 | `LIGHT METALS.pdf` → TMS 2018 — *Light Metals 2018* (proceedings; aluminium production, casthouse, alloys). *Largest file (115 MB)* | EN | 114.75 | [19pGgeo4aOrHhCgRWFUYQbKlSeiQNKgY4](https://drive.google.com/file/d/19pGgeo4aOrHhCgRWFUYQbKlSeiQNKgY4/view) | 1y1kVxzSHUHKBggrbROJj0-wHdP61_dqP |
| S-068 | `TMS 2018 SUPPLEMENTAL PROCEEDINGS.pdf` → TMS 2018 — *Annual Meeting & Exhibition Supplemental Proceedings* | EN | 35.07 | [1DaSVlWgcExaYNoPctNLnH53hOBBClFd4](https://drive.google.com/file/d/1DaSVlWgcExaYNoPctNLnH53hOBBClFd4/view) | 1ljrL1I8fg5y2_yzoTFKP5S4z5Ij-dbT9 |
| S-069 | `MATERIALS PROCESSINGS FUNDAMENTALS.pdf` → TMS 2018 — *Materials Processing Fundamentals 2018* | EN | 8.28 | [1r1eM2hsO3i-Rj3dYkNQvQT1yUZ5hP6BG](https://drive.google.com/file/d/1r1eM2hsO3i-Rj3dYkNQvQT1yUZ5hP6BG/view) | 1n_KBXOlgrqxH6Cbvl0KBa7FjPcIuVkq4 |
| S-070 | `RARE METAL TECHNOLOGY.pdf` → TMS 2018 — *Rare Metal Technology 2018* | EN | 11.12 | [1DYRsPSD29mVLtfSNcLMvLvXaev4s4OPb](https://drive.google.com/file/d/1DYRsPSD29mVLtfSNcLMvLvXaev4s4OPb/view) | 1n3PLpk4Iu-7I80LD6oF_UG2XtbW85ccy |
| S-071 | `HIGH-TEMPRITURE METALLURGICAL PROCESSING.pdf` → TMS 2018 — *High-Temperature Metallurgical Processing* (9th Int. Symposium) | EN | 35.83 | [1wySzX9KBrTFoD3tBmgrSVLaYk2XWXy3f](https://drive.google.com/file/d/1wySzX9KBrTFoD3tBmgrSVLaYk2XWXy3f/view) | 1oBif3n1WXGDbxiHMyU2og1Q4FInjNwzJ |
| S-072 | `CFD MODELING AND SIMULATION MATERIALS PROCESSING.pdf` → TMS 2018 — *CFD Modeling and Simulation in Materials Processing 2018* | EN | 10.31 | [1QWHQFOooJUKzdA-stsXlijoq6ccASsal](https://drive.google.com/file/d/1QWHQFOooJUKzdA-stsXlijoq6ccASsal/view) | 18OxaipP1nQpZq-b_OXCFB0FHGuvh_0u_ |
| S-073 | `41279889-Alloys.pdf` → TMS 2018 — *Characterization of Minerals, Metals, and Materials 2018* (Li, B. et al., eds.). *Misnamed "41279889-Alloys.pdf"; not the Habashi book* | EN | 26.42 | [1sP4G1PGlES_nFoGSix8aA8MAdCer6gde](https://drive.google.com/file/d/1sP4G1PGlES_nFoGSix8aA8MAdCer6gde/view) | 1KXWd_EAl8OKsD5InOTALsOjdK25cwmmM |
| S-074 | `41279889-Alloys.pdf` → Habashi, F. (ed.) — *Alloys: Preparation, Properties, Applications* (Wiley-VCH, 1998) | EN | 20.60 | [1TCvbTC2LxRkOZQfHu3V-5lOPsIctbTTJ](https://drive.google.com/file/d/1TCvbTC2LxRkOZQfHu3V-5lOPsIctbTTJ/view) | 1mDMc6Jui1CnWbq_IiCi9Q7O4xQSY-yG9 |
| S-075 | `27767685-Materials-Engineers-Technicians.pdf` → Higgins, R.A. — *Materials for Engineers and Technicians*, 4th ed. (Newnes / Elsevier) | EN | 26.90 | [1yZIlYSmfyQIXY3iUdzovF7u1tCHGmWc0](https://drive.google.com/file/d/1yZIlYSmfyQIXY3iUdzovF7u1tCHGmWc0/view) | 1BycJdsJu8cjxT8wMNcYxLSGPg-nLF665 |
| S-076 | `Chemie und Eigenschaften metallischer Werkstoffe 2017.pdf` → Thienel, K.-Ch. — *Werkstoffe I: Chemie und Eigenschaften metallischer Werkstoffe – Stahl und NE-Metalle* (lecture notes, Universität der Bundeswehr München, 2017) | DE | 3.80 | [13ighAAUOs8kif9PuB8fWFy2mkyR3MYH_](https://drive.google.com/file/d/13ighAAUOs8kif9PuB8fWFy2mkyR3MYH_/view) | — |
| S-077 | `74849304-Aluminium.pdf` → "Aluminium – An overview" (Wikipedia article compilation, PediaPress, 2011). *Low authority* | EN | 20.34 | [11M-jMkYSxdMMb5J0sGZaGQCIZgiuWz04](https://drive.google.com/file/d/11M-jMkYSxdMMb5J0sGZaGQCIZgiuWz04/view) | 1p0kgCB2zJOoG_DqHYCKVGPGRyjD24yxu |
| S-078 | `Ishikawa_diagram_in_5x_Zakaj.pdf` → "Ishikawa diagram in 5x Zakaj" — Ishikawa diagram and 5-Whys quality method | SL | 0.23 | [1UyAPbmec3L94_9kfmQXjuzaJ5VlbdBl8](https://drive.google.com/file/d/1UyAPbmec3L94_9kfmQXjuzaJ5VlbdBl8/view) | — |

### Unknown / needs inspection (1)

| Ref | Title (Drive name → identified work) | Lang | Size MB | Canonical Drive link | Duplicate IDs |
|---|---|---|---|---|---|
| S-079 | `Tlačno litje.pdf` → "Tlačno litje" (die casting) — scanned document without a text layer; probably a Slovenian die-casting textbook or lecture. *Needs inspection (OCR)* | SL | 21.12 | [1k5uV4pSjjXMzemzpDSPwyS4dN--uw7W7](https://drive.google.com/file/d/1k5uV4pSjjXMzemzpDSPwyS4dN--uw7W7/view) | 1cUwcQDUa4MQMhdTeEgT9pyvdbTkhcG3v |

## Own R&D working files (24 files, 16 documents)

All are in the My Drive root unless noted. Descriptions are guesses from titles, plus Drive's
first-line text snippet for three files with unclear titles (W-05, W-08, W-24). They were not
read in depth; another pass handles content. Modified times are UTC. Versions of one document
are listed in time order, and the last one is probably the current one.

| Key | Title | Type | Modified | Link | Likely contents |
|---|---|---|---|---|---|
| W-01 | Untitled0.ipynb (folder *Colab Notebooks*) | Colab notebook | 2025-05-26 | [open](https://colab.research.google.com/drive/18nAoePZ0OZsi_ooO9knXnwIlwhL-UlPG) | Unnamed notebook. Full-text search matches "aluminium/aluminum", so it is probably an early Al calculation. **Needs inspection.** |
| W-02 | Modified 3102 Alloy Composition Explained | Google Sheet | 2026-01-19 | [open](https://docs.google.com/spreadsheets/d/1tLOr9HtNx_UJbJOkkBQfU9Ej-tIjQS-xKueHwr_wBwU/edit) | A modified AA3102 composition with the reasoning for each element |
| W-03 | Aluminium_Alloys_CBAM_Presentation.pptx | PowerPoint | 2026-01-22 | [open](https://drive.google.com/file/d/1UQmAOQXlfJI3pv-4Mz3W2K0ESDv2gTxZ/view) | Aluminium alloys under the EU Carbon Border Adjustment Mechanism (embedded emissions, product scope) |
| W-04 | MSA_Analiza_Merilnega_Sistema.docx | Word | 2026-02-12 | [open](https://drive.google.com/file/d/10iYVo_KWXyx1qeRFkkqzSb1Ovk1MHXN6/view) | Measurement-system analysis (Gage R&R) procedure, in Slovenian. *Peripheral (QA / lab metrology)* |
| W-05 | MSA_Kalkulator.xlsx | Excel | 2026-02-12 | [open](https://drive.google.com/file/d/1MVB5DpvBesKmewy144KacLuViI3GwTfX/view) | Gage R&R calculator template (3 appraisers × 10 parts × 3 trials), in Slovenian. *Peripheral* |
| W-06 | mg_dashboard.xlsx (v1) | Excel | 2026-03-23 14:43 | [open](https://drive.google.com/file/d/1FtbQAUJ2JgBpWM_tI8wK_UdP6zzFT3nu/view) | Earlier version of W-08 |
| W-07 | mg_dashboard.xlsx (v2) | Excel | 2026-03-23 14:46 | [open](https://drive.google.com/file/d/1qiRjIGLjR6IlcUF0qCaf1utUnA5tvdG2/view) | Earlier version of W-08 |
| W-08 | mg_dashboard.xlsx (v3, latest) | Excel | 2026-03-23 15:02 | [open](https://drive.google.com/file/d/1-7mxtk6cte3lJ6qknxcP8qKO9SVkOcQQ/view) | "Annealing cycle dashboard – EN AW 3102 (AlMn0.2): MgO and recrystallization optimization". Compares batch-annealing cycles: peak temperature, soak, MgO oxide thickness, risk score, recrystallization result |
| W-09 | 3102_RX_simulation.xlsx | Excel | 2026-03-23 15:17 | [open](https://drive.google.com/file/d/1nnyhJQ5mlPHC2uJupDlVSyyiQ2H1GC6O/view) | Recrystallization (RX) kinetics simulation for AA3102 annealing |
| W-10 | AA3207_Recrystallization_Simulation.xlsx (v1) | Excel | 2026-03-23 16:15 | [open](https://drive.google.com/file/d/1jw-jp7hdKhxk4eKLBnWLu-7gTSehRXpm/view) | Recrystallization simulation for AA3207, early version (61 KB) |
| W-11 | AA3207_Recrystallization_Simulation.xlsx (v2) | Excel | 2026-03-23 16:17 | [open](https://drive.google.com/file/d/1QH-vB1QFvltSsp1cHaffXQSQ6bzwXrhW/view) | Same, version 2 (45 KB) |
| W-12 | AA3207_Recrystallization_Simulation.xlsx (v3) | Excel | 2026-03-23 16:23 | [open](https://drive.google.com/file/d/1t2chD4lXva-h6DdnMQDXoOrfz-xenRSR/view) | Same, version 3 (49 KB) |
| W-13 | AA3207_Recrystallization_Simulation.xlsx (v4, latest) | Excel | 2026-03-23 16:26 | [open](https://drive.google.com/file/d/1L9MDNPrCcWymlvgcowcv6Gf34eLJvwm2/view) | Same, final and largest version (165 KB) |
| W-14 | aluminium_tempers_v2.xlsx | Excel | 2026-03-23 20:39 | [open](https://drive.google.com/file/d/1jujW_zC4r4jPc2HXq6FuyaNhPouPKhqP/view) | Table of aluminium temper designations and properties (v2) |
| W-15 | aluminium_tempers_v3.xlsx | Excel | 2026-03-23 20:45 | [open](https://drive.google.com/file/d/1XYBOGMAvW4uHGHxxecQr3HeGGlQ4EO-k/view) | Same, v3 |
| W-16 | aluminium_tempers_SLO.xlsx | Excel | 2026-03-23 20:52 | [open](https://drive.google.com/file/d/1qg7Mvfi33_I1jax72vUiRI8YPRWyN09j/view) | Same, Slovenian-language version (latest) |
| W-17 | EN_AW_3207_CRM_Reduction_Table.xlsx | Excel | 2026-03-24 08:38 | [open](https://drive.google.com/file/d/1r-GFxL4bVuGG_ZGm_Lix-SQ3Upc7gROk/view) | Critical-raw-material (CRM) reduction options for EN AW-3207. "CRM" read as critical raw materials, as in CLAUDE.md; not verified |
| W-18 | EN_AW_Master_CRM_Reduction_Tables.xlsx | Excel | 2026-03-24 08:39 | [open](https://drive.google.com/file/d/1KN_kyx3RDw0QfLNvi1UHx7UYP5xwLjpq/view) | Master CRM-reduction tables across EN AW alloys |
| W-19 | Aluminum Slug Weight Table (v1) | HTML file | 2026-04-23 20:24 | [open](https://drive.google.com/file/d/12gqu7Q-T3NfPSIvy-s4U5MbC3sxyP-X1/view) | Slug (rondelle) weight vs. diameter × thickness. Tiny file (1 KB) |
| W-20 | Aluminum Slug Weight Table (v2) | HTML file | 2026-04-23 20:25 | [open](https://drive.google.com/file/d/1Fwc-jJfXhjvv2lRkdTUlanuXCWeoz8rX/view) | Same, second version (1 KB) |
| W-21 | Aluminum Slug Specifications Reference | Google Doc | 2026-04-23 21:04 | [open](https://docs.google.com/document/d/1a2PUBN1OpYaCwpsmSeUqfkI8ViHDcYezazENjEMCfHQ/edit) | Reference specs for impact-extrusion slugs. About 1 KB, possibly nearly empty |
| W-22 | Aluminum Slug Specifications - Technical Analysis | Google Doc | 2026-04-23 21:05 | [open](https://docs.google.com/document/d/1GDXMCKCnH1YrBwSuEtkir9aDZA1nRD6pGbPFJX_lKzY/edit) | Technical analysis of slug specifications (alloy, temper, dimensions). About 1 KB |
| W-23 | Aluminum Slug Data Table | Google Doc | 2026-04-23 21:06 | [open](https://docs.google.com/document/d/1vqiAL2AcCpv584C0DPJspPvnRL-8DiPU4iXmY_qM4U8/edit) | Data table for slugs. About 1 KB |
| W-24 | Analiza_ponudbe_MF-50_CitiUS_R3 | Google Slides | 2026-07-14 | [open](https://docs.google.com/presentation/d/1MrE_bXZm5qmGkQtQ6rBP7YT-wo1NZRDSfpwVyRmivAU/edit) | Review of a supplier's offer (rev. R3) for an MF-50 melting furnace for the slug ("rondelice") casthouse: capacity, guarantees, metal yield. *Peripheral (equipment / investment)* |

## Notes and oddities

**Misleading file names.** Identified from the first page of each file:

- `document.pdf` (S-054) is an Alcoa Micromill presentation (J.F. Butler Jr., 2015).
- `Pre-course-reading.pdf` (S-008) is Phillion & Dantzig's reading for the ESI solidification course.
- `uporabno del-2.pdf` ("useful, part 2"; S-052) is Ø. Ryen's NTNU thesis (2003) on work hardening and anisotropy of Al sheet and profiles.
- `fir-tree zone.pdf` (S-015) is S.J. Maggs's Leeds PhD thesis (1996).
- `Rolling.pdf` (S-049) is Dünckelmeyer's TUM dissertation on work-roll cracking in hot strip mills. It is about steel rolls, not aluminium rolling.
- `155680328-Rolling.pdf` (S-048) is Schröder's e-book on rolling-mill rolls.
- `lastnosti aluminija.pdf` ("properties of aluminium"; S-042) is TALAT Lecture 1101.
- `Microstructure_URN-NBN-SI-DOC-OFLHAUYU.pdf` (S-064) is a Bombač et al. paper on Nimonic 80A.
- `ASM Handbook of Aluminium vol. 1.pdf` and `Alminium.pdf` (S-029) are the same file. It is Totten & MacKenzie's *Handbook of Aluminum* Vol. 1 (Marcel Dekker), not an ASM Handbook.
- `116748406-Aluminium-Alloys.pdf` (S-041) is Dwight's *Aluminium Design and Construction*, a structural-design book.
- `74849304-Aluminium.pdf` (S-077) is a Wikipedia compilation. It has low authority; do not cite it for numbers.

**One name, different works.** Three file names are each used for two unrelated works:

- **`vasevska.pdf`**
  - 0.37 MB (2 copies): T. Vasevska's 2004 paper on cold-rolling hardening of Al (S-051).
  - 28.58 MB (2 copies): the Schuler *Metal Forming Handbook* (1998). Its first pages match `3c-handbook-metal-forming.pdf`, and the sizes differ by only 205 bytes, so it is filed as a probable duplicate under S-046.
- **`uporaba v transportu.pdf`** ("use in transport")
  - 3.28 MB: the EAA brochure *Aluminium in Commercial Vehicles* (S-043).
  - 3.64 MB: W.H. Sillekens's thesis *Backward Can Extrusion and Materials Behaviour* (S-053). It is byte-size-identical to `374925.pdf` and `374925(1).pdf`; 374925 is the TU/e repository number in its DOI.
- **`41279889-Alloys.pdf`**
  - 20.6 MB in the library root: Habashi (ed.), *Alloys* (Wiley-VCH) (S-074).
  - 26.4 MB in `TMS 2018/`: the TMS volume *Characterization of Minerals, Metals, and Materials 2018* (S-073).

**Renamed copies with identical size.** These were merged:

- `MODELLING OF STATIC recovery.pdf` = `CHARACTERISATION AND MODELLING OF STATIC.pdf` (S-017)
- `Alminium.pdf` = `ASM Handbook of Aluminium vol. 1.pdf` (S-029)
- `374925.pdf` = `374925(1).pdf` = the 3.64 MB `uporaba v transportu.pdf` (S-053)
- The `(1)` variants of the Aalco temper sheet (S-033) and of the Nimonic paper (S-064)

**Probable duplicates (near-identical size).** These were merged under one key, with the variant
IDs flagged "probable" in the table:

- Sheppard *Extrusion of Aluminium Alloys*: 10.513 MB vs `Extrusion Of Aluminium Alloys.pdf` at 10.463 MB. The first pages are identical (S-045).
- Schuler handbook vs the large `vasevska.pdf` (S-046).
- Davis (S-031), Ardagh aerosol brochure (S-056), Mall + Herlan line brochure (S-057) and Hinterkopf N40.2 brochure (S-058). In each case there is a second download in `Čakalna vrsta/` that differs by 69 B to 7.8 KB (at most 0.5 %), probably a re-download or a minor revision.

**`62816_*.pdf`** (S-001 – S-006) are publisher chapter files of D.G. Eskin, *Physical Metallurgy
of Direct Chill Casting of Aluminum Alloys* (CRC Press, 2008; Advances in Metallic Alloys vol. 6).
Only the front matter and chapters 1–5 are in Drive, in both copies. Any later chapters are
missing, so check the contents list in S-001 before assuming a topic is covered. Each library
copy also has a junk `Download Free Ebooks & much more.URL` shortcut, which was excluded.

**Files that need inspection or OCR.**

- S-079 `Tlačno litje.pdf` (21 MB) has no text layer. It is probably a scanned Slovenian die-casting text.
- S-025 `Effects of Zr and Sc on al4Cu1,5Mg.pdf`: the first page yields only a micrograph caption, so the author and source are unknown.
- S-009 *Blister Formation in Rolled Aluminum*: the author name is garbled in the OCR.
- S-018: a recrystallization-modelling chapter excerpt whose source book is unverified.

**Language.** Several Slovenian file names hold English content (S-013, S-014, S-042, S-043,
S-052, S-053). The German sources are S-019, S-036 to S-039, S-044, S-049, S-050 and S-076. The
Slovenian sources are S-051, S-078 and S-079.

**Coverage relative to the repo's focus (3xxx sheet: AA3102/AA3207).** There is no paper or
book dedicated to Al–Mn (3xxx) dispersoid precipitation or to recrystallization control in 3xxx.
The closest sources are:

- Phase equilibria: Belov/Eskin/Aksenov Ch. 1 on Al–Fe–Mn–Si (S-012), plus S-013 to S-015.
- Recovery and recrystallization: Humphreys & Hatherly (S-016) and Junit (S-017).
- Work hardening: Ryen (S-052) and Vasevska (S-051).
- Casting: the Eskin DC-casting chapters and the continuous roll casting paper (S-010).
- General alloy and temper references: Polmear, Totten, Kaufman and Davis.

The impact-extrusion and slug material (Sillekens, the MPMA, Ardagh, Mall + Herlan and
Hinterkopf brochures, the punching slides) relates to the user's slug and aerosol-can work
(W-19 to W-24).

**Excluded on purpose and not listed.**

- The `microstructure-sim-v2.14.0` folder and everything under it: source, `node_modules`, run CSVs and README files. This follows the user's instruction.
- 7 non-technical items inside the library folders: a business-school case study (4 copies), a bank loan form and 2 e-book-site shortcuts.
- Personal, household, financial and sales documents, and e-mail newsletters, elsewhere in My Drive.
## Ref Royset07 ("Scandium and Aluminum alloys.pdf" 1FizSqhIa3XAhPQpZYt0maHVsHdEsKrhW) J. Røyset (Hydro R&D Sunndal) "Scandium in aluminium alloys overview" Metall. Sci. Technol. 25(2) pp.11-21 (refs to 2007); EN (IT abstract); complete; two-column garbling
- p.13: max Sc solubility ~0.38 wt%; Al3Sc a ≈0.414 vs Al 0.412 nm (~0.5% misfit); Al3Sc precipitates 250-350°C; ≥0.1 wt% Sc significant hardening (~100 MPa order)
- p.14: dispersoids from homogenisation/solution T usually too low number density for strength but very effective in impeding boundaries -> RX resistance after rolling/extrusion/forging
- p.14: Zr: lower coarsening rate of Al3(Sc,Zr); Zr does not affect start of precipitation but slows later stage (C-curves 10% & 60% Al-0.4Sc vs Al-0.4Sc-0.15Zr, Fig 6b); core/shell: Al3Sc core (Sc diffusion), Zr-rich shell (slow Zr diffusion)
- Table 1 p.16: 3xxx Al-0.5Mn-0.2Mg-0.15Zr: Rp0.2 87 / Rm 140; +0.11Sc 119/173; +0.21Sc 152/198; +0.26Sc 168/207 (Riddle, Hallem, Ryum 2002; as-hot-worked or annealed)
- p.19: Al-2%Sc master ~US$50/kg -> Sc ~US$2500/kg; 0.2 wt% Sc adds ~US$5/kg

## Files too large for the Drive connector: split plan (2026-10-12)

The connector downloads whole PDFs only up to **≈ 6 MB**. Kaufman at 6.09 MB worked; 7.19 MB and larger
failed. Larger files are only partly readable as text. Save them in Drive as parts of **≤ 5 MB** each, in the
same folder, named `<title> - part N (pp X-Y).pdf`. Then they can be read in full.

| Priority | Ref | Work | Size (MB) | Parts at ≤ 5 MB | What it would add |
|---|---|---|---|---|---|
| A | S-016 | Humphreys & Hatherly, *Recrystallization* | 12.7 | 3 | RX kinetics, PSN, two-phase alloys, textures (slug anneal) |
| A | S-029 | Totten & MacKenzie, *Handbook of Aluminum* Vol. 1 | 17.7 | 4 | Alloy metallurgy, rolling (Ch. 7), extrusion (Ch. 8), formability/earing |
| A | S-015 | Maggs, *Intermetallic phase selection in dilute Al–Fe–Si* | 22.3 | 5 | β vs α Fe phases vs cooling rate (T11 risk 1) |
| A | S-052 | Ryen, *Work hardening… of Al sheets* | 11.2 | 3 | Per-solute work hardening (Mn, Mg): wall strength per press force |
| A | S-020 | Ivanov, *Solute clustering in Al alloys* | 13.3 | 3 | Mg–Si clustering, natural ageing, bake response (T11 risk 2) |
| A | S-028 | Polmear, *Light Alloys* | 9.7 | 2 | Canstock/foil/conductor alloys, cast and Mg chapters |
| B | S-045 | Sheppard, *Extrusion of Aluminium Alloys* | 10.5 | 3 | Hot-working constants (Ch. 4) |
| B | S-032 | *ASM Handbook Vol. 2* (nonferrous) | 52.6 | only the wrought-Al sections | Property data for 1xxx/3xxx/8xxx |
| B | S-067 | TMS *Light Metals 2018* | 114.8 | only selected casthouse / alloy papers | Continuous casting, recycling, Fe tolerance |
| B | S-047 | AA, *Rolling Aluminum* | 7.2 | 2 | Appendices |
| C | S-046 | Schuler, *Metal Forming Handbook* | 28.6 | only cold-extrusion chapter (pp. 443–480) | Impact-extrusion practice |
| C | S-074 | Habashi, *Alloys* | 20.6 | only the aluminium chapter | Alloy overview |
| C | S-007, S-049, S-075, S-077, S-079, other TMS 2018 volumes | — | 8–36 | as needed | Lower relevance; S-079 is a scan without text (needs OCR) |
