# 18 — Computational alloy-design tools and methods (web survey)

**Source type: online research (not from the user's Drive), retrieved 2026-10-12.**

**Scope.** This chapter surveys the methods and tools that could be used to build and calibrate a *physically based* alloy-design model for wrought aluminium. The main case is the user's lean 3xxx/1xxx slug alloys (EN AW-3102, AA3207, the modified 3102 and 1xxx), taken through the chain composition → solidification → homogenisation → cold rolling → annealing → slug properties. It covers:
- CALPHAD thermodynamics and open Al databases (§1);
- KWN/CNT precipitation codes (§2);
- recrystallisation, grain-growth and texture codes (§3);
- process FEM and through-process (ICME) frameworks (§4);
- data-driven and Bayesian methods (§5);
- a recommended low-cost Python stack (§6);
- a target architecture with a minimal calibration plan and risks (§7).

It complements KB ch.03 (recrystallisation physics), ch.04 §4/§11 (KWN equations and parameters) and ch.07 §10 (process parameters). It answers the problem in KB ch.09 §9: the user's three JMAK models disagree about 7× and none has a documented calibration set.

**Conventions.**
- Every factual claim cites a `[W18-xx]` source from the table below.
- **(general knowledge)** marks a statement not checked against a source in this pass.
- **(assessment)** marks my own design reasoning.
- **(derived)** marks arithmetic done here from cited inputs.
- **(not verified)** marks a capability, version or price that I could not confirm. Version numbers, dates and licences are given **only** where I read them on PyPI, GitHub or a file.

**Access limitations of this pass (important for trust).**
1. The sandbox egress policy blocked direct fetching of most vendor and publisher sites: thermocalc.com, computherm.com, matcalc.at, crct.polymtl.ca, opencalphad.com, kawin.org, ScienceDirect/MDPI/OSTI/PMC, scientific.net and others. Only GitHub, raw.githubusercontent.com, PyPI and Docker Hub could be fetched. For blocked pages I used the search-engine extract of the *official* page. These are flagged **S** in the "Access" column. **F** means I opened and read the page, repository or file myself.
2. The shared web-search budget ran out partway through the survey. As a result:
   - the commercial process-FEM tools (Abaqus, DEFORM, Simufact, QForm), OpenPhase and AFLOW could not be checked at all;
   - Al-specific Bayesian-optimisation and ML case studies could not be checked;
   - these items are marked **(not verified)** and listed in §8 for a follow-up pass.

---

## Sources

| Key | Tool / paper | Organisation / authors | Year | URL | Licence | Access |
|---|---|---|---|---|---|---|
| W18-01 | TCAL (TCS Al-based Alloys Database): product and help pages (TCAL10/TCAL11) | Thermo-Calc Software AB | 2025–2026 | https://thermocalc.com/products/databases/aluminum-based-alloys/ ; https://help.thermocalc.com/2025b/content/databases/tcal/tcal_ele-sys-pha.htm | Commercial | S |
| W18-02 | Thermo-Calc 2026b release notes (TCAL11) | Thermo-Calc Software AB | 2026 | https://thermocalc.com/wp-content/uploads/Documentation/Release_Notes/2026b-thermo-calc-release-notes.pdf | — | S |
| W18-03 | TCAL9/TCAL10 technical information sheets (property data: ELRS, THCD) | Thermo-Calc Software AB (distributor mirror) | 2019–2025 | https://www.engineering-eye.com/THERMOCALC/details/db/pdf/thermo-calc/02/TCAL9_technical_info.pdf | — | S |
| W18-04 | MOBAL8 / MOBAL1 Al mobility database (help pages) | Thermo-Calc Software AB | 2025 | https://help.thermocalc.com/2025b/content/databases/mobal/mobal_about_db.htm ; https://help.thermocalc.com/2025b/content/databases/mobal/mobal1_tcs_al_alloys.htm | Commercial | S |
| W18-05 | Precipitation Module (TC-PRISMA): help and product pages | Thermo-Calc Software AB | 2025 | https://help.thermocalc.com/2025b/content/precipitation/precipitation_module-about.htm | Commercial add-on | S |
| W18-06 | TC-Python API reference 2026b | Thermo-Calc Software AB | 2026 | https://download.thermocalc.com/docs/tc-python/2026b/html/ | Licence required | S |
| W18-07 | Thermo-Calc academia / Educational package and EULA | Thermo-Calc Software AB | 2025–2026 | https://thermocalc.com/academia/ ; https://thermocalc.com/content/uploads/Documentation/Terms_Conditions/eula.pdf | Free, teaching only | S |
| W18-08 | TCAL revision history | Thermo-Calc Software AB | 2025 | https://help.thermocalc.com/2025b/content/databases/tcal/tcal_revision_history-all.htm | — | S |
| W18-09 | PanAluminum (PanAl) database, manual and product page | CompuTherm LLC | 2025 | https://computherm.com/panaluminum ; https://computherm.com/docs/PanAl_DB_Manual.pdf | Commercial | S |
| W18-10 | PanPrecipitation module brochure | CompuTherm LLC | 2020 | https://computherm.com/wp-content/uploads/2020/08/5-Software_PanPrecipiataion-module-2020.pdf | Commercial | S |
| W18-11 | FTlite light-alloy database documentation; FactSage 8.3 database summary | CRCT Montréal / GTT (FactSage) | 2024 | https://www.crct.polymtl.ca/FACT/documentation/FTlite/FTlite_documentation.pdf ; https://www.crct.polymtl.ca/fact/documentation/FSData.htm | Commercial | S |
| W18-12 | JMatPro: Innoval "alloy development insights"; Advanced Science News overview; DDF 263 p.31 (metastable phases in Al alloys) | Sente Software (tool); Innoval Technology; various | 2007–2023 | https://www.innovaltec.com/alloy-development-insights/ ; https://www.advancedsciencenews.com/a-proven-software-for-the-calculation-of-materials-properties/ ; https://www.scientific.net/DDF.263.31 | Commercial | S |
| W18-13 | OpenCalphad repository; Sundman et al., "OpenCalphad – a free thermodynamic software", IMMI (2015) | B. Sundman, U. Kattner, M. Palumbo, S. Fries | 2015–2026 | https://github.com/sundmanbo/opencalphad | GNU GPL v3 (licence file in repo) | F (repo); S (paper) |
| W18-14 | pycalphad (GitHub and PyPI) | R. Otis, Z.-K. Liu and contributors | 2017–2026 | https://github.com/pycalphad/pycalphad ; https://pypi.org/project/pycalphad/ | MIT | F |
| W18-15 | scheil (Scheil–Gulliver on pycalphad), PyPI | pycalphad project | 2025 | https://pypi.org/project/scheil/ | MIT | F |
| W18-16 | ESPEI; Bocklund et al., MRS Commun. 9(2) (2019), doi:10.1557/mrc.2019.59 | Phases Research Lab (Penn State) | 2019–2026 | https://github.com/PhasesResearchLab/ESPEI | MIT | F |
| W18-17 | COST 507 light-alloy thermodynamic database (TDB file "ROUND II, January 1999, frozen version"); COST 507 final report EUR 18499 EN (Ansara, Dinsdale, Rand, eds., 1998) | COST 507 consortium | 1998–1999 | https://raw.githubusercontent.com/pycalphad/pycalphad/develop/pycalphad/tests/databases/COST507.tdb ; https://www.opencalphad.com/databases/CGNA18499ENC_001.pdf ; https://cordis.europa.eu/project/id/507 | "May be used freely but on your own risk" (file header) | F (TDB file read); S (report, CORDIS) |
| W18-18 | NIMS Computational Phase Diagram Database (CPDDB), doi:10.48505/nims.3060 | NIMS (Japan), MatNavi | 2024–2026 | https://cpddb.nims.go.jp/ ; https://mdr.nims.go.jp/datasets/900cd0b1-a574-4385-9e50-70bca1f875d2 | Free with registration; bulk download prohibited | S |
| W18-19 | Critical assessment of thermodynamic data for Al–Fe intermetallics (Al-Fe-Mn-Si context) | A.T. Dinsdale, C. Fang, Z. Fan, A.V. Khvan (Brunel/NPL) | ~2016 | https://bura.brunel.ac.uk/bitstream/2438/15056/1/Fulltext.pdf | Open repository | S |
| W18-20 | MatCalc official Docker image (capabilities, versions, licensing) | MatCalc / TU Wien (matcalctuw) | 2026 | https://hub.docker.com/r/matcalctuw/matcalc | Commercial licence required | F |
| W18-21 | MatCalc general information and open databases (mc_al, mc_fe, mc_ni under ODbL) | MatCalc Engineering GmbH / TU Wien | 2025 | https://www.matcalc.at/wiki/doku.php?id=general ; https://www.matcalc.at/index.php/databases/open-databases | Software commercial; open DBs ODbL | S |
| W18-22 | CAROUSEL (high-throughput MatCalc framework) README | S. Colibri (GitHub) | 2023–2025 | https://github.com/SColibri/CAROUSEL | MIT (framework) | F |
| W18-23 | kawin on PyPI | N. Ury (maintainer) | 2026 | https://pypi.org/project/kawin/ | MIT | F |
| W18-24 | kawin repository: source (`precipitation/coupling/GrainGrowth.py`, `Strength.py`), example notebooks and TDBs | Materials Genome Foundation | 2026 | https://github.com/materialsgenomefoundation/kawin | MIT (per PyPI) | F |
| W18-25 | Ury, Neuberger, Sargent, Xiong, Arróyave, Otis, "Kawin: an open source KWN phase precipitation and coarsening model", Acta Mater. 255 (2023) 118988; NASA software catalogue entry NPO-52029-1 | NASA / Univ. Pittsburgh / Texas A&M | 2023 | https://par.nsf.gov/biblio/10460980 ; https://software.nasa.gov/software/NPO-52029-1 | — | S |
| W18-26 | Du, Poole, Wells, Parson, "Microstructure evolution during homogenization of Al–Mn–Fe–Si alloys: modeling and experimental results", Acta Mater. 61(13) (2013) 4961–4973 | UBC / Rio Tinto Alcan | 2013 | https://www.sintef.no/en/publications/publication/1087594 | Journal | S |
| W18-27 | Homogenisation treatments and softening behaviour of an Al-Mn-Fe-Si model alloy, *Metals* 6(3) 61 | NTNU group (authors not captured) | 2016 | https://www.mdpi.com/2075-4701/6/3/61/htm | Open access | S |
| W18-28 | George, Magidi-Chicuba, "Intermetallic and dispersoid structures in AA3104 aluminium alloy during two-step homogenisation", *Sci. Rep.* (2024) | — | 2024 | https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10844596/ | Open access | S |
| W18-29 | SINTEF conference lecture: KWN modelling of Cr and Zn effects on dispersoid precipitation during AA3xxx homogenisation | SINTEF | n/a | https://www.sintef.no/en/publications/publication/0198cc633ab2-79bb75cd-68eb-4cbe-9697-68f165a10611/ | — | S |
| W18-30 | NTNU Open: "Isothermal and non-isothermal annealing of cold-rolled Al-Mn-Fe-Si alloys with different microchemistry states"; MSF paper on pre-existing dispersoids plus concurrent precipitation | NTNU | ~2016–2017 | https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2468659 ; https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2468664 | Open repository | S |
| W18-31 | ALSOFT softening model tested on Al-Mn-Fe-Si alloys, Mater. Sci. Forum 783–786, p.57 | NTNU / SINTEF (Nes school) | 2014 | https://www.scientific.net/MSF.783-786.57.pdf | Journal | S |
| W18-32 | "The ALFLOW-model – a microstructural approach to constitutive plasticity-modelling of aluminium alloys" (MSF 2000); Marthinsen et al., MSF 715–716 p.543 (2012) | E. Nes, K. Marthinsen et al. (NTNU) | 2000, 2012 | https://www.osti.gov/etdeweb/biblio/20078593 ; https://www.scientific.net/MSF.715-716.543 | Journal | S |
| W18-33 | Preminger, Marthinsen, Manik, "Application of artificial neural networks for microstructure models ALFLOW and ALSOFT", Defect Diffus. Forum 446, 71 | NTNU | 2026 | https://www.scientific.net/DDF.446.71 | Journal | S |
| W18-34 | Furu, "Modeling of recrystallization of commercial particle containing Al-alloys" (thesis, NTNU Open) | T. Furu | n/a | https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2728510 | Open repository | S |
| W18-35 | Dons, "'Alstruc': a model for solidification and homogenisation of industrial aluminium alloys" (NTNU PhD 2002); SINTEF/IFE 2015 paper coupling Alstruc with ALSIM | A.L. Dons; SINTEF/IFE | 2002, 2015 | https://bibsok.no/?tnr=322576 ; https://www.sintef.no/en/publications/publication/0198cc6adea3-5e50bf27-a552-48d7-bac2-cafaba2a1100/ | — | S |
| W18-36 | Hirsch J. (ed.), *Virtual Fabrication of Aluminum Products: Microstructural Modeling in Industrial Aluminum Production*, Wiley-VCH 2006, ISBN 9783527313631, incl. ch.21 "Through process simulation of EN AW-3103 sheet production" and ch.14 on microchemistry | J. Hirsch (ed.); Marthinsen et al.; Miroux et al. | 2006 | https://katalog.bibliothek.kit.edu/bib/285171 ; https://research.tudelft.nl/en/publications/chapter-21-through-process-simulation-of-en-w-3103-sheet-producti | Book | S |
| W18-37 | VIRCAST ("virtual cast house") and VIRFAB (through-process modelling of rolling and extrusion) EU projects (CORDIS) | EU FP5 consortia | ~1999–2004 | https://cordis.europa.eu/article/id/82424-process-modelling-of-aluminium-casting ; https://cordis.europa.eu/project/id/G5RD-CT-1999-00132/results | — | S |
| W18-38 | MOOSE multiphysics FE framework (repo, `modules/`, `phase_field/examples`) | Idaho National Laboratory | 2026 | https://github.com/idaholab/moose | LGPL-2.1 | F |
| W18-39 | PRISMS-PF phase-field framework | PRISMS Center, Univ. Michigan | 2026 | https://github.com/prisms-center/phaseField | LGPL-2.1 | F |
| W18-40 | SPPARKS kinetic/Metropolis Monte Carlo (Potts apps in `src/`) | Sandia National Laboratories | 2026 | https://github.com/spparks/spparks | GPL-2.0 | F |
| W18-41 | DAMASK (GitHub mirror; `damask` Python package on PyPI) | Max-Planck-Institut für Eisenforschung / damask-multiphysics.org | 2026 | https://github.com/eisenforschung/DAMASK ; https://pypi.org/project/damask/ | AGPL-3.0(+) | F |
| W18-42 | VPSC8 polycrystal plasticity code; Tomé & Lebensohn, *Material modeling with the visco-plastic self-consistent (VPSC) approach*, Elsevier 2023 | LANL (Triad National Security) | 2023–2026 | https://github.com/lanl/VPSC_code | BSD-3-Clause | F |
| W18-43 | MTEX texture/EBSD toolbox | MTEX developers | 2026 | https://github.com/mtex-toolbox/mtex | GPL-2.0 | F |
| W18-44 | orix (Python orientation/crystal-symmetry library) | pyxem project | 2026 | https://github.com/pyxem/orix | GPL-3.0 | F |
| W18-45 | PRISMS-Plasticity (crystal-plasticity FEM) | PRISMS Center, Univ. Michigan | 2026 | https://github.com/prisms-center/plasticity | LGPL | F |
| W18-46 | DREAM.3D (deprecated; successor simplnx) | BlueQuartz Software | 2026 | https://github.com/BlueQuartzSoftware/DREAM3D | BSD (per README) | F |
| W18-47 | FEniCSx / DOLFINx finite-element environment | FEniCS Project | 2026 | https://github.com/FEniCS/dolfinx | LGPL-3.0+ | F |
| W18-48 | BoTorch (GitHub `botorch/acquisition`; PyPI) | Meta / PyTorch | 2026 | https://github.com/pytorch/botorch ; https://pypi.org/project/botorch/ | MIT | F |
| W18-49 | Ax adaptive-experimentation platform (PyPI) | Meta | 2026 | https://pypi.org/project/ax-platform/ | MIT | F |
| W18-50 | scikit-optimize (archived) | scikit-optimize developers | 2024 | https://github.com/scikit-optimize/scikit-optimize | BSD-3-Clause | F |
| W18-51 | PyMC (GitHub, PyPI) | PyMC developers | 2026 | https://github.com/pymc-devs/pymc ; https://pypi.org/project/pymc/ | Apache-2.0 | F |
| W18-52 | emcee (PyPI); Foreman-Mackey et al., PASP 125 (2013) 306, doi:10.1086/670067 | D. Foreman-Mackey et al. | 2024 | https://pypi.org/project/emcee/ | MIT | F |
| W18-53 | SALib sensitivity-analysis library (PyPI) | SALib developers | 2026 | https://pypi.org/project/SALib/ | MIT | F |
| W18-54 | lolo / lolopy (random forests with uncertainty) | Citrine Informatics | 2026 | https://github.com/CitrineInformatics/lolo | Apache-2.0 | F |
| W18-55 | matminer (materials data-mining library) | Hacking Materials group (LBNL) | 2026 | https://github.com/hackingmaterials/matminer | see repo LICENSE (not read) | F |
| W18-56 | qmpy (software behind OQMD) | Wolverton group, Northwestern | 2026 | https://github.com/wolverton-research-group/qmpy | MIT | F |
| W18-57 | Materials Project API client (mp-api) | Materials Project (LBNL) | 2026 | https://github.com/materialsproject/api | see repo LICENSE (not read) | F |
| W18-58 | MPDS API client | MPDS / Tilde Materials Informatics | 2026 | https://github.com/mpds-io/mpds_client | MIT (client) | F |
| W18-59 | Study of dispersoid precipitation versus homogenisation heating rate in AlMnFeMgSi alloys, *Metals* 13(10) 1706 (mapping of the search extract to this URL not certain) | authors not captured | 2023 | https://www.mdpi.com/2075-4701/13/10/1706 | Open access | S |
| W18-60 | Review of 6xxx alloys covering CNT of α-Al(Fe,Mn)Si dispersoids versus heating rate, *Crystals* 15(8) 695 (mapping of the search extract to this URL not certain) | authors not captured | vol. 15 (year not captured) | https://www.mdpi.com/2073-4352/15/8/695/xml | Open access | S |
| W18-61 | "Thermo-kinetic computer simulation of differential scanning calorimetry curves of AlMgSi alloys", Int. J. Mater. Res., doi:10.3139/146.110396 (MatCalc-type simulation; software not confirmed) | authors not captured | n/a | https://www.degruyterbrill.com/document/doi/10.3139/146.110396/html | Journal | S |
| W18-62 | "Simulation of the texture evolution of aluminium alloys during primary static recrystallization using a cellular automaton approach", MRS Online Proceedings Library | authors not captured | n/a | https://www.cambridge.org/core/journals/mrs-online-proceedings-library-archive/article/abs/simulation-of-the-texture-evolution-of-aluminium-alloys-during-primary-static-recrystallization-using-a-cellular-automaton-approach/4B502F8771B3B9BF4CABDA40775470C9 | Journal | S |

---

## 0. Executive summary

1. **Thermodynamics.** Commercial CALPHAD databases have the Al-specific depth that 3xxx alloys need: Thermo-Calc TCAL+MOBAL, CompuTherm PanAl, FactSage FTlite and MatCalc's commercial databases [W18-01; W18-04; W18-09; W18-11; W18-21].
   - The free route is pycalphad (MIT) with the COST 507 TDB of 1999 [W18-14; W18-17]. It is usable for screening but has a **verified gap**: in COST 507, α-AlMnSi and α-AlFeSi are two separate phases. Mn cannot substitute on the Fe site and Fe cannot substitute on the Mn site [W18-17]. The α-Al(Mn,Fe)Si phase that controls 3xxx dispersoids is therefore not described as one solution phase (assessment).
2. **Precipitation.** kawin (Python KWN, MIT, v0.5.0 June 2026) is the only open, maintained, CALPHAD-coupled KWN code found [W18-23; W18-24]. It has:
   - non-isothermal T(t) profiles;
   - heterogeneous nucleation sites (dislocations, grain boundaries, edges, corners);
   - a strength model;
   - a grain-growth model with Zener pinning from the computed particle population;
   - a multiphase homogenisation/diffusion model [W18-24].
   Its examples include Al–Zr (Al₃Zr) and Al–Sc (Al₃Sc), plus Al–Mg–Si with a two-step heat treatment [W18-24].
3. **Recrystallisation.** The most relevant validated physics for 3xxx softening is the NTNU/SINTEF **ALSOFT** (recovery + recrystallisation) and **ALFLOW** (work hardening) family. ALSOFT has been tested against Al-Mn-Fe-Si alloys of different microchemistry [W18-31; W18-32]. No public code for these models was found in this pass. They should be re-implemented from the papers (assessment).
   - Full-field codes are open and mature but too expensive for a design loop. They are better used for mechanism studies (assessment). The codes are MOOSE, PRISMS-PF, SPPARKS, DAMASK and VPSC [W18-38–W18-42].
4. **Through-process modelling** of 3xxx sheet has been done before. Hirsch's 2006 book contains a chapter on through-process simulation of EN AW-3103 sheet production [W18-36]. VIRCAST and VIRFAB were EU projects on cast-house and rolling/extrusion through-process models [W18-37].
5. **Calibration and design.** The recommended pieces are:
   - PyMC (Apache-2.0) or emcee (MIT) for Bayesian calibration [W18-51; W18-52];
   - SALib for global sensitivity [W18-53];
   - BoTorch or Ax (MIT) for constrained multi-objective Bayesian optimisation and active learning [W18-48; W18-49].
   scikit-optimize was archived in February 2024 and should not be the basis of new work [W18-50].
6. **Recommended stack (§6).** pycalphad + scheil + kawin + a custom ALSOFT-type recovery/recrystallisation/grain-growth module + PyMC + BoTorch/Ax + orix (or MTEX) for EBSD. The minimal plan to calibrate it and settle the ~7× disagreement between the in-house JMAK models is about **9 isothermal softening curves per alloy plus 2–3 non-isothermal validation cycles**, with conductivity and EBSD on a subset (§7.3, assessment).

---

## 1. Thermodynamics / CALPHAD

### 1.1 What CALPHAD has to deliver for the 3xxx slug chain (assessment)

| Stage | Quantity needed | Why (KB link) |
|---|---|---|
| Solidification | Constituent types and fractions (Al₆(Mn,Fe), α-Al(Mn,Fe)Si, Al₁₃Fe₄); Mn/Si/Fe microsegregation profile (Scheil) | Sets PSN particles (> ~1 µm) and the Mn supersaturation map (KB ch.04 §1.5, §5) |
| Homogenisation | Mn and Si solvus in the presence of Fe; α-phase driving force; mobility of Mn | Sets the dispersoid F_V/r (Zener drag) and the residual Mn in solid solution (KB ch.04 §2, §11) |
| Annealing | Mn solubility at 300–450 °C; driving force for concurrent precipitation | Concurrent precipitation slows recrystallisation and coarsens grain (KB ch.09 §9 item 3) |
| Properties | Solute content (for solid solution strengthening and resistivity) | Hardness and conductivity predictions |

### 1.2 Tool comparison

| Tool | What it does / physics | Inputs → outputs | Licence / cost | Maturity | Al databases and validation | Role in our workflow |
|---|---|---|---|---|---|---|
| **Thermo-Calc** (+ Scheil, Diffusion Module DICTRA, Precipitation Module TC-PRISMA, TC-Python) | Gibbs-energy minimisation; Scheil; diffusion (DICTRA); KWN precipitation (TC-PRISMA, §2) [W18-05; W18-06] | Composition, T → phases, compositions, driving forces; with MOBAL: diffusion profiles, homogenisation kinetics [W18-04] | Commercial; prices not public. Academic discounts are on quotation [W18-07]. The free **Educational** package is capped at 3 components and is for teaching only (EULA) [W18-07] | Industry standard. TC-Python 2026b docs cover equilibrium, Scheil, precipitation, diffusion and property models [W18-06] | **TCAL11**: 48 elements; 2026b notes list 317 binaries, 135 ternaries, 15 quaternaries and 723 phases, plus new elastic properties [W18-01; W18-02] (search extract). Electrical resistivity and thermal conductivity data have been in TCAL since TCAL7 [W18-03]. The TCAL revision history records an Al-Fe-Mn-Si update modelling Mn solubility in Al₈Fe₂Si [W18-08]. MOBAL8 is the Al mobility database for DICTRA/TC-PRISMA [W18-04]. In MOBAL1, diffusion is assessed only in FCC_A1 and LIQUID [W18-04]. | Best "gold-standard" source for α-Al(Mn,Fe)Si solvus, driving forces and Mn mobility. Options are a short-term licence or consultancy runs to generate tables for our Python model (assessment) |
| **FactSage** (FTlite) | Gibbs-energy minimisation; light-metal database | Composition, T → equilibria | Commercial (not verified: price) | Mature | FTlite covers Al, Mg and Ti alloys and is stated to fit the 1000–7000 commercial series. It originated in a 2004–2010 light-alloy consortium with the Al consortium, GM and MagNET [W18-11] | Alternative to TCAL for solvus/Scheil tables; strong in melt/oxide chemistry, possibly useful for MgO/oxidation (assessment) |
| **Pandat** (PanAl, PanPrecipitation) | Equilibrium, Scheil, diffusion, precipitation | Composition, T(t) → phases; PSD, number density, volume fraction [W18-10] | Commercial | Mature | PanAl covers Al, Cu, Fe, Mg, Mn, Si and Zn as major elements, with thermodynamic, mobility (PanAl_MB) and molar-volume/thermophysical parts. Component counts differ by release: 38–40 components and ~1150–1236 phases [W18-09]. The PanPrecipitation example compares simulated particle size and yield strength with experiment for Al-2.3Mg-6.1Zn at 160 °C [W18-10] | Alternative commercial path to Thermo-Calc. PanAl includes an Alpha_AlFeSi phase model [W18-09] (Mn solubility in it not verified) |
| **JMatPro** | CALPHAD + physically based property models; TTT/CCT via Johnson–Mehl–Avrami treatment [W18-12] | Composition → phases, TTT/CCT, physical and thermophysical properties, flow-stress curves [W18-12] | Commercial (not verified: price) | Mature. Al is one supported family; applied to AA319, AA6061, AA7075 metastable phases [W18-12] | Innoval stresses that the model must be validated for the alloy in question [W18-12] | Quick property estimates (density, conductivity, flow stress) for FEM input. Not a precipitation-kinetics engine for Mn dispersoids (assessment) |
| **MatCalc** (thermodynamics part) | CALPHAD equilibrium, Scheil-type microsegregation [W18-20] | See §2 | Commercial licence (MatCalc Engineering GmbH has been TU Wien's exclusive licence agent since 2015) [W18-21]. A free version is reported as limited to 3 elements and free databases (third-party statement) [W18-22] | Mature; current stable Docker image 6.10 [W18-20] | Free **mc_al** basic database under the Open Database License [W18-21]. Its content for α-Al(Mn,Fe)Si is not verified | Main alternative to Thermo-Calc when precipitation and microstructure kinetics are the goal (§2) |
| **OpenCalphad** | Multicomponent equilibria, property and phase diagrams, database assessment; OCASI interface for coupling; OpenMP parallel equilibria [W18-13] | TDB → equilibria | Free; GNU GPL v3 document in repo [W18-13] | Developed since 2013; the developers said it cannot yet replace commercial tools [W18-13] (S) | Uses any TDB, e.g. COST 507 [W18-17] | Not needed if pycalphad is used. Relevant only for Fortran/C coupling (assessment) |
| **pycalphad** (+ scheil, ESPEI) | Gibbs-energy minimisation; reads Thermo-Calc TDB files [W18-14]. `scheil`: Scheil–Gulliver with perfect liquid mixing, local interface equilibrium and **no solid diffusion** [W18-15]. ESPEI: parameter generation (AICc) and Bayesian ensemble-MCMC uncertainty quantification of CALPHAD parameters [W18-16] | TDB + composition, T → equilibria, driving forces, Scheil phase-fraction curves | pycalphad 0.11.2 (5 Jun 2026), MIT, Python ≥ 3.11 [W18-14]. scheil 0.3.0 (3 Nov 2025), MIT [W18-15]. ESPEI MIT [W18-16] | Active open-source projects | Quality depends entirely on the TDB (§1.3) | **Core of the open stack.** Thermodynamic engine for kawin [W18-23]. Scheil initial state. ESPEI to refit an Al-Mn-Fe-Si description to our own solvus/conductivity data with uncertainty (assessment) |

### 1.3 Open Al databases (what is actually usable without a licence)

| Database | Content (verified) | Gaps for 3xxx | Use |
|---|---|---|---|
| **COST 507** TDB ("Round II, January 1999, frozen version") [W18-17] | 27 elements: Al, Ar, B, C, Ce, Cr, Cu, Fe, Hf, Li, Mg, Mn, Mo, N, Nb, Nd, Ni, O, Si, Sn, Ta, Ti, V, W, Y, Zn, Zr. 243 PHASE definitions. Al₆Mn, Al₄Mn, Al₁₂Mn and Al₁₁Mn₄ with sublattice (Al)(Fe,Mn). Al₁₃Fe₄ with (Al)(Fe,Mn)(Al,Si,Va). ALMNSI_ALPHA (Al)₁₆(Mn)₄(Si)₁(Al,Si)₂. ALFESI_ALPHA (Al)(Fe)(Si)(Al,Si). ALFESI_BETA. Al₃Zr; Mg₂Si. No Sc. No mobility (MQ/MF/DQ/DF) or molar-volume parameters found [W18-17] (file read here). The project covered about 70 binary and 20 ternary systems [W18-17] (S) | **α-Al(Mn,Fe)Si is split** into an Fe-free AlMnSi α and an Mn-free AlFeSi α [W18-17]. The continuous Mn↔Fe substitution of industrial α-dispersoids is therefore missing (assessment). Data are 1999-era. Brunel/NPL work notes that key multicomponent datasets had not been revised [W18-19] | Teaching, screening, Scheil trends for 1xxx/3xxx. **Not** for quantitative Mn-solvus/dispersoid work without refitting |
| NIMS **CPDDB** [W18-18] | TDB files from CALPHAD assessments; more than 500 (MDR record) to more than 700 (NIMS page) systems | Free MatNavi registration needed; bulk/automated download prohibited [W18-18]. Al-Mn-Fe-Si availability not verified | Source of individual binary/ternary assessments to assemble a custom TDB |
| pycalphad test databases [W18-14] | Al-containing TDB files: `alfe.tdb`, `Al-Fe_sundman2009.tdb`, `Al-Mg_Zhong.tdb`, `alzn_mey.tdb`, `Al-Cu-Y.tdb`, `COST507.tdb` and others (file names verified in `pycalphad/tests/databases`) | Test fixtures, not curated application databases (assessment) | Examples and quick binaries |
| kawin example TDBs [W18-24] | `AlScZr.tdb` (header: "Al-Zr database", from T. Wang, Z. Jin, J. Zhao, J. Phase Equilib. 22 (2001) 544; phases AL3SC, AL3ZR, FCC_A1; includes a Zr diffusion entry for FCC_A1); `AlMgSi.tdb` | Not 3xxx | Al₃Sc/Al₃Zr dispersoid studies (KB ch.04 §3) |
| MatCalc **mc_al** [W18-21] | Free basic Al thermodynamic database (ODbL); a mobility counterpart is not verified | Coverage of α-Al(Mn,Fe)Si not verified | Usable with MatCalc only. Format compatibility with pycalphad not verified |

### 1.4 Pitfalls (assessment unless cited)

- Free-database Scheil runs for 3xxx will mis-assign Fe between Al₆(Mn,Fe) and the α-phase because of the split α-phase description [W18-17]. **Check every free-database Scheil result against the solubility tables already in KB ch.04 §11** (Belov data).
- Diffusion in intermetallics is usually not assessed. In MOBAL1 only FCC_A1 and LIQUID have assessed diffusion, and other phases are treated as non-diffusing [W18-04]. Homogenisation models therefore treat particle growth and dissolution as matrix-diffusion-controlled.
- The Educational Thermo-Calc licence is restricted to teaching in an academic setting [W18-07]. It cannot legally be used for this industrial R&D.

---

## 2. Precipitation modelling (KWN / CNT)

### 2.1 Tool comparison

| Tool | Physics | Inputs → outputs | Licence / cost | Maturity / validation | Al examples | Role |
|---|---|---|---|---|---|---|
| **MatCalc** | Precipitation kinetics, long-range diffusion and combined diffusion + precipitation. Microsegregation and primary precipitates. Lattice Metropolis/kinetic Monte Carlo. Dislocation-density and grain-size evolution. Vacancy effects. Static and dynamic yield strength. Thermophysical properties [W18-20] | Composition, T(t), deformation → PSD per phase, solute, grain size, dislocation density, yield strength | Commercial licence; Docker image 6.10 stable [W18-20]. Console, Python and GUI interfaces plus an API [W18-20] | Long track record (general knowledge). Used inside CAROUSEL for high-throughput Scheil → precipitation → heat-treatment optimisation [W18-22] | CAROUSEL images are labelled "Example AL alloy" [W18-22]. Thermo-kinetic simulation of DSC curves of AlMgSi alloys has been published [W18-61] (not read; software not confirmed) | **Best commercial all-in-one** for homogenisation → annealing → yield strength in one code, if a licence is affordable (assessment) |
| **TC-PRISMA** (Thermo-Calc Precipitation Module) | Langer–Schwartz + Kampmann–Wagner numerical; concurrent nucleation, growth and coarsening [W18-05] | TCAL+MOBAL, T(t) → PSD, number density, mean radius, volume fraction, compositions, nucleation rate, TTP [W18-05] | Commercial add-on. Included in the Educational package (3 components, teaching only) [W18-07] | Part of Thermo-Calc since 2016 [W18-05]. Training course has an "Al alloys" examples session [W18-05] | Not verified for Mn dispersoids | Reference KWN to benchmark kawin if a licence is available (assessment) |
| **PanPrecipitation** | Diffusion-controlled KWN-type precipitation during heat treatment [W18-10] | PanAl + T(t) → composition, fraction, number density, PSD; yield strength [W18-10] | Commercial | Mature | Al-Zn-Mg ageing example with size and yield-strength comparison [W18-10] | Alternative to TC-PRISMA |
| **kawin** | KWN with CALPHAD (pycalphad) coupling [W18-23]. Nucleation sites: bulk, dislocations, grain boundaries, grain edges, grain corners. Non-spherical shapes (needle, plate, cuboid) with Gibbs–Thomson and growth corrections. Elastic-energy example. Multiphase precipitation. Piecewise T(t) via `TemperatureParameters`. Surrogate models. Mobility fitting [W18-24]. User-defined thermodynamics possible [W18-25] (S) | TDB (or user functions) + composition, T(t) → PSD, N, r̄, f per phase; coupled grain size; yield strength [W18-24] | **MIT**, v0.5.0 (5 Jun 2026), Python ≥ 3.11, depends on numpy, scipy, matplotlib and pycalphad [W18-23] | Acta Mater. 2023 paper reports reproduction of commercial-code results and experiments for several systems [W18-25] (S). The API changed substantially and the examples are the reference [W18-23]. Single maintainer listed on PyPI [W18-23] | Al–Zr (Al₃Zr from 0.4 at.% Zr, 450 °C, dislocation nucleation ρ = 10¹⁵ m⁻², γ = 0.1 J m⁻²) [W18-24]; Al–Sc (Al₃Sc, 400 °C) coupled to grain growth [W18-24]; Al–Mg–Si (β″, β′, B′, U1, U2; 16 h at 175 °C then 1 h ramp to 250 °C) [W18-24] | **Recommended open KWN engine** for (i) α-dispersoid evolution during homogenisation and anneal ramps, (ii) Zener pressure input to the recrystallisation model, (iii) Sc/Zr studies (assessment) |
| **Custom Robson-type KWN** (KB ch.04 §4) | Same equations (Gibbs–Thomson, CNT, flux-balance growth) | — | — | Fully controllable | KB ch.04 has Al₃(Sc,Zr) parameters | Fallback if kawin's multicomponent α-phase handling proves fragile (assessment) |

### 2.2 kawin internals relevant to our model (read from source)

- **Grain growth with Zener pinning** (`coupling/GrainGrowth.py`) [W18-24]:
  - Growth law: dRᵢ/dt = α·M·γ_gb·(1/R_cr − 1/Rᵢ).
  - Pinning term: z = Σⱼ f_j^{m_j}/(K_j·r̄_j), with defaults K = 4/3 and m = 1. z is computed from the moments of the KWN size distribution of each phase.
  - Defaults: γ_gb = 0.5 J m⁻², M = 10⁻¹⁴ m⁴ J⁻¹ s⁻¹ (a **constant**, so a temperature-dependent mobility M₀exp(−Q/RT) must be supplied by the user).
  - Docstring reference: J. Phase Equilib. Diffus. 43 (2022) 866–875 (first author truncated as "K. W"; co-authors J. Jeppsson and P. Mason).
  - (assessment) This handles **grain growth after recrystallisation**, not primary recrystallisation. The recrystallisation step must be added (§3, §7).
- **Strength model** (`coupling/Strength.py`) [W18-24]:
  - Follows Ahmadi et al., Comput. Mater. Sci. 91 (2014) 173–186.
  - Shearing terms: coherency, modulus, APB, SFE, interfacial. Bypass: Orowan.
  - Superposition: exponent 1.8 within a phase; 1.8 or 1.4 across phases; Taylor factor 2.24; solid-solution and base terms added.
  - (assessment) For 3xxx slugs, dispersoid strengthening is mainly Orowan, while grain size and solid solution dominate in the O-temper. Hall–Petch is not in this module and must be added.
- **Homogenisation model** (example 07) [W18-24]:
  - 1-D multiphase diffusion, assuming local equilibrium in each volume element.
  - Effective mobility uses Wiener, Hashin–Shtrikman or labyrinth averaging.
  - The example is Fe–Cr–Ni. (assessment) It can be adapted to dendrite-scale Mn redistribution in a Scheil-initialised cell, but it does not nucleate dispersoids; that requires coupling to the KWN model.
- **Example parameter values** usable as priors [W18-24]:
  - Zr diffusivity D_Zr = 0.0768·exp(−242 000/RT) m² s⁻¹, taken from Robson & Prangnell.
  - Sc diffusivity D = 1.9×10⁻⁴·exp(−164 000/RT) m² s⁻¹.
  - Al₃Sc misfit 0.0125 and shear modulus 67.9 GPa.
  - Al matrix G = 25.4 GPa, b = 0.286 nm, ν = 0.34.

### 2.3 Cross-check against KB ch.04 (derived)

The kawin example diffusivities give the following D_Sc/D_Zr ratios (derived):

| T | D_Sc/D_Zr |
|---|---|
| 400 °C | ≈ 2 800 |
| 450 °C | ≈ 1 070 |
| 480 °C | ≈ 640 |

KB ch.04 §11 lists **D_Sc/D_Zr ≈ 4 at 480 °C** (from Robson 2004), and ch.04 §12 item 1 already flags this as suspicious. The two parameter sets differ by more than two orders of magnitude. The KB value must be reconciled (likely a transcription or definition issue) before any Sc/Zr KWN calibration (assessment).

### 2.4 3xxx dispersoid literature that a model must reproduce

- **Du, Poole, Wells, Parson (2013).** A modelling plus experimental study of microstructure evolution during homogenisation of Al–Mn–Fe–Si alloys [W18-26]. This is the closest published analogue to the homogenisation module we need. Full text not read.
- **Heating rate.** A low heating rate during homogenisation is reported as essential to precipitate fine dispersoids in AlMnFeMgSi alloys [W18-59]. A 6xxx review uses CNT to explain why α-Al(Fe,Mn)Si dispersoids distribute evenly through the grain only when the heating rate to the homogenisation temperature is slow enough [W18-60].
  - (assessment) The KWN model must run on the **real T(t) ramp**, not on soak-only isothermal steps. kawin supports this [W18-24].
- **Homogenisation and softening.** Different homogenisations give different Mn levels in solid solution and different dispersoid densities. These change softening after cold rolling [W18-27]. Pre-existing fine dispersoids plus *concurrent* precipitation slow recrystallisation and give coarse, elongated grains [W18-30]. Isothermal versus non-isothermal annealing of cold-rolled Al-Mn-Fe-Si alloys with different microchemistry states has been studied at NTNU [W18-30].
  - (assessment) This is the direct literature basis for the heating-rate effect that KB ch.07 G5 asks for.
- **Two-step homogenisation (AA3104).** Two-step homogenisation transforms β → α constituents. The sub-micron dispersoids pin grain boundaries by Zener drag [W18-28].
- **KWN of Cr and Zn effects.** SINTEF applied a KWN approach built on computational thermodynamics and diffusion kinetics to Cr and Zn effects on AA3xxx dispersoid precipitation [W18-29]. The software used is not stated in the extract.

---

## 3. Recrystallisation, grain growth and texture

### 3.1 Tool comparison

| Tool | Physics | Inputs → outputs | Licence / cost | Maturity | Al-specific validation | Role |
|---|---|---|---|---|---|---|
| **ALSOFT** (NTNU/SINTEF) | Mean-field model of *recovery and recrystallisation together* during annealing of deformed Al [W18-31]. Lineage: Vatne, Furu, Ørsund, Nes (Acta Mater. 1996), with PSN and cube-band nucleation for hot rolling [W18-31] (S). Furu's thesis uses a JMAK-type treatment with roughly random nucleation sites [W18-34] | Deformation state (subgrain size, dislocation density, misorientation, from ALFLOW), particles, solute, T(t) → softening, X(t), grain size, texture components | Not public (no code found; availability not verified) | Industrial use: applied to AlMgSi extrusions, recrystallisation through the wall thickness [W18-31] (S) | **Tested against Al-Mn-Fe-Si model alloys with different microchemistries** [W18-31] | **Template for our recrystallisation module.** Re-implement the published equations (assessment) |
| **ALFLOW** (NTNU) | Statistical model of athermal dislocation storage plus dynamic recovery (Nes school) [W18-32] | Strain, strain rate, T, solute, particles → flow stress, subgrain size, dislocation density [W18-32] | Not public (not verified) | Fed with FEM strain/strain-rate/T histories of extrusion to predict subgrain size and dislocation density [W18-32] | Al alloys [W18-32] | Template for the cold-rolling stored-energy module (assessment) |
| **ALFLOW/ALSOFT ANN surrogates** | Neural networks trained on model outputs [W18-33] | — | — | 2026 paper [W18-33] | Al | Shows the surrogate pattern for fast optimisation (§5) |
| **MOOSE** (phase_field module) | Phase-field on a multiphysics FE framework. Modules include `phase_field`, `solid_mechanics`, `heat_transfer`, `stochastic_tools`, `optimization`. Phase-field examples include `grain_growth`, `nucleation`, `ebsd_reconstruction` [W18-38] | Initial microstructure (synthetic or EBSD), energies, mobilities → 2-D/3-D grain evolution | LGPL-2.1 [W18-38] | Large, active INL project [W18-38] | Al-specific validation not verified | Mechanism studies: Zener-pinned grain growth from an EBSD start, abnormal growth risk (assessment) |
| **PRISMS-PF** | Phase-field FE on deal.II (≥ 9.6.0, matrix-free), adaptive mesh, MPI. Prebuilt applications for precipitate evolution, grain growth and solidification [W18-39] | Same as above | LGPL-2.1; citation example names v3.0.0 (2026) [W18-39] | Active | Not verified | Same as MOOSE. Choose one (assessment) |
| **OpenPhase** | Multi-phase-field (not verified) | — | Academic/commercial versions (not verified) | — | — | Not verified in this pass |
| **SPPARKS** (Monte Carlo Potts) | Kinetic and Metropolis Monte Carlo [W18-40]. Applications in `src/` include `app_potts`, `app_potts_pin` (particle pinning), `app_potts_strain` and `app_potts_strain_pin` (stored energy; inference from names), `app_potts_grad`, `app_potts_weld`, `app_potts_am_*` [W18-40] | Lattice microstructure + rules → grain evolution in MC steps (needs time calibration) | GPL-2.0, Sandia [W18-40] | Mature | Not verified | Cheap 3-D statistics of pinned grain growth and recrystallisation nucleation clustering, e.g. PSN at constituent stringers (assessment) |
| **Cellular automata** for static recrystallisation texture in Al | CA simulation of texture evolution during primary static recrystallisation of Al alloys [W18-62] | — | No open CA code verified in this pass | — | Al [W18-62] | Literature only |
| **DAMASK** | Crystal-plasticity multiphysics kit (tags: crystal plasticity, multi-physics) [W18-41]. Spectral/FEM solvers and constitutive laws not verified on the fetched pages | Texture + boundary conditions → stress/strain fields, deformed texture | AGPL-3.0(+). Python package `damask` 3.1.0 (10 Jul 2026), Production/Stable [W18-41] | Mature | Not verified | Rolling-texture and stored-energy *distribution* for recrystallisation nucleation; earing studies (assessment) |
| **VPSC8** | Visco-plastic self-consistent polycrystal plasticity; POLE8 pole-figure tool; 15 examples [W18-42] | Texture + strain path → texture evolution, r-values | **BSD-3**, LANL. Documented in Tomé & Lebensohn (2023) [W18-42] | Mature, widely used (general knowledge) | Not verified | Fast deformation-texture prediction for cold rolling → slug texture → earing in impact extrusion (assessment) |
| **PRISMS-Plasticity** | Crystal- and continuum-plasticity FEM on deal.II [W18-45] | — | LGPL [W18-45] | Active | Not verified | Alternative to DAMASK |
| **MTEX** | Texture and EBSD analysis: ODF reconstruction, grain and boundary analysis; script-based [W18-43] | EBSD/pole figures → ODF, grain size distributions, GOS/KAM | GPL-2.0; **requires MATLAB R2022b or later** [W18-43] | De-facto standard (general knowledge) | — | EBSD processing for calibration data (grain size, recrystallised fraction, cube fraction) |
| **orix** | Python orientations and crystal symmetry; inspired by MTEX [W18-44] | Orientation data → symmetry-aware analysis | GPL-3.0, Python ≥ 3.10 [W18-44] | Active | — | MATLAB-free EBSD pipeline in the Python stack (assessment) |
| **DREAM.3D** | Reconstruction and quantification of 3-D/EBSD data, synthetic microstructures [W18-46] | .ang/.ctf/.h5 EBSD → statistics, synthetic volumes [W18-46] | BSD [W18-46]; **deprecated**, successor simplnx [W18-46] | Deprecated | — | Use simplnx if needed |

### 3.2 Choice (assessment)

- **Design loop: mean-field.** An ALSOFT-type model with state variables (ρ, δ_subgrain, X, D_rx) driven by stored energy, Zener drag from kawin and solute drag runs in milliseconds per cycle. That speed allows MCMC calibration (§5) and optimisation over thousands of composition/process candidates.
- **Full-field only to check mean-field assumptions.** Examples:
  - nucleation-site clustering at constituent stringers (SPPARKS `app_potts_strain_pin`);
  - pinned grain growth from a measured EBSD map (MOOSE `ebsd_reconstruction` + `grain_growth`) [W18-38; W18-40].
- **Texture/earing** (secondary for slugs): VPSC8 for rolling texture, plus MTEX or orix for measured ODFs [W18-42; W18-43; W18-44].

---

## 4. Process simulation and through-process (ICME) modelling

### 4.1 FEM tools

| Tool | Scope | Licence / cost | Notes |
|---|---|---|---|
| Abaqus, DEFORM, Simufact Forming, QForm | Commercial FEM for rolling, forging and impact/cold extrusion (general knowledge) | Commercial; prices **not verified** | Capabilities, Al material libraries and microstructure-coupling options **not verified** in this pass (search budget exhausted) |
| **MOOSE** (`solid_mechanics`, `heat_transfer`, `contact` modules) | Open multiphysics FE [W18-38] | LGPL-2.1 [W18-38] | Large-deformation impact-extrusion forming would require significant setup (assessment) |
| **FEniCSx (DOLFINx)** | General FE PDE solver, C++ core with Python interface [W18-47] | LGPL-3.0+ [W18-47] | Good for strip/coil **thermal** models (furnace heating, coil T-gradients) feeding the anneal model (assessment) |

### 4.2 Through-process / ICME precedents in aluminium

- **VIRCAST** ("virtual cast house") modelled DC casting of tailored products through solidification, casting and homogenisation. It produced as-cast microstructure prediction integrated into a software tool [W18-37].
- **VIRFAB** worked on predictive through-process microstructural modelling of rolling and extrusion. Partners were six major aluminium producers and seven academic institutions. Outputs included a benchmark review of microstructure-evolution modelling in wrought Al [W18-37].
- **Hirsch (ed.) 2006** [W18-36] collects the European "virtual fabrication" work. It includes:
  - a chapter by Marthinsen et al. modelling microstructure, texture and properties through EN AW-3103 sheet production — the closest published analogue to our 3102/3207 strip-to-slug chain;
  - a microchemistry chapter (Miroux, Lok, Anselmino, van der Zwaag);
  - extrusion modelling (Furu et al.).
- **Alstruc** (SINTEF; Dons PhD 2002) is a solidification and homogenisation microsegregation model for industrial multicomponent Al alloys [W18-35]:
  - temperature-dependent partition coefficients and liquidus slopes, plus secondary-phase precipitation;
  - phase-diagram data reduced to analytical expressions for CPU-efficient coupling;
  - coupled with the ALSIM continuum model to study macrosegregation in DC billets [W18-35].
- **ALFLOW + ALSOFT** are coupled to FEM histories for extrusion and rolling [W18-32].
  - Specific Hydro in-house tools are **not verified**.

### 4.3 What process simulation the slug problem actually needs (assessment)

1. **The furnace T(t) of each coil/slug load** is the dominant process input for recrystallisation, grain size and MgO. KB ch.09 §9 item 4 already says that ramps and overshoot must be credited. A 1-D/2-D coil thermal model (FEniCSx), or simply the logged thermocouple data, is worth more than any forming FEM in phase 1.
2. **Cold-rolling strain** is known from the pass schedule (ε = ln(t₀/t)). Through-thickness strain gradients matter mainly for texture (VPSC) and surface recrystallisation. FEM of rolling is a phase-3 item.
3. **Impact-extrusion FEM** (QForm/Simufact/DEFORM or MOOSE) becomes relevant once the target is moved from "slug HB and grain size" to "can-wall properties and forming defects". It then needs flow curves of the annealed slug (ALFLOW-type) as input.

---

## 5. Data-driven and ML alloy design

### 5.1 Methods and open tools

| Need | Tool (verified) | Key facts | How we would use it |
|---|---|---|---|
| Bayesian calibration of physics models | **PyMC** 6.3.2 (8 Sep 2026), Apache-2.0. MCMC (incl. NUTS) and variational inference [W18-51] | NUTS handles models with thousands of parameters [W18-51] | Hierarchical calibration of recrystallisation/KWN parameters across alloys (§7.4) |
| Black-box MCMC (non-differentiable simulators) | **emcee** 3.1.6, MIT; affine-invariant ensemble sampler (Goodman & Weare) [W18-52] | — | When kawin/ODE models cannot be differentiated |
| CALPHAD-parameter UQ | **ESPEI**, MIT; Bayesian ensemble MCMC on thermochemical and phase-boundary data [W18-16] | — | Refit Mn solvus/α-phase with our conductivity-derived solubility data (assessment) |
| Global sensitivity | **SALib** 1.6.0, MIT; Sobol, Morris, eFAST [W18-53] | — | Rank which parameters (σ, N₀, Q_rx, M₀, …) drive the slug HB and grain size before calibrating (assessment) |
| Bayesian optimisation / active learning | **BoTorch** 0.18.1, MIT, Python ≥ 3.11 [W18-48]. Acquisition modules include `multi_objective/`, `cost_aware.py`, `fixed_feature.py`, `knowledge_gradient.py`, `active_learning.py`, `bayesian_active_learning.py`, `penalized.py`, `risk_measures.py` [W18-48]. **Ax** 1.3.1, MIT: multiple objectives, parameter and outcome constraints, noisy observations, BoTorch backend [W18-49] | scikit-optimize is BSD-3 but **archived on 28 Feb 2024** (read-only) [W18-50] | Choose the next lab anneals (maximum information) and plant trials (expected improvement under HB/grain-size/MgO constraints) |
| ML with uncertainty on tabular data | **lolo/lolopy** (Citrine), Apache-2.0; random forests with jackknife intervals [W18-54] | — | Residual (model-discrepancy) learning on plant data |
| Feature generation | **matminer** [W18-55] | Featurisers, datasets, retrieval [W18-55] | Low value for our narrow composition window (assessment) |
| Surrogates of expensive physics | kawin `Surrogate.py` (thermodynamic surrogates) [W18-24]; ANN surrogates of ALFLOW/ALSOFT [W18-33] | — | Replace slow CALPHAD calls inside optimisation loops |

### 5.2 Materials databases: relevance for lean wrought Al (assessment)

| Database | What it holds (verified where cited) | Relevance to 3xxx/1xxx slug design |
|---|---|---|
| Materials Project (mp-api) [W18-57] | DFT data for crystalline compounds (general knowledge; content not verified on the fetched page) | **Low.** It gives 0 K formation energies of intermetallics (Al₆Mn, α-phase approximants) useful to CALPHAD assessors. Nothing on processing, recrystallisation or properties of alloys |
| OQMD (qmpy) [W18-56] | DFT database run with qmpy (MIT) [W18-56] | **Low**, same reasons |
| AFLOW | DFT high-throughput (general knowledge) | **Low**. Not verified in this pass |
| MPDS [W18-58] | Materials data platform with an API; the client is MIT and login is via GitHub [W18-58]. Experimental phase-diagram, structure and property content not verified | **Medium-low.** Possibly useful for phase-diagram sections and experimental property points |
| NIMS MatNavi / CPDDB [W18-18] | CALPHAD TDBs (>500–700 systems) with registration [W18-18] | **Medium.** Building blocks for a custom Al-Mn-Fe-Si(-Mg-Cu) TDB |
| Citrine platform | Commercial informatics platform (lolo is its open UQ library [W18-54]) | Platform capabilities and cost not verified |
| **In-house plant and lab data** | KB ch.09 | **Highest.** No public database contains slug HB and grain size versus CR and anneal cycle for 3102/3207 |

### 5.3 Physics-informed ML patterns for our data volume (assessment / general knowledge)

1. **Physics model as the mean, GP for the discrepancy.** y = f_phys(x; θ) + δ(x) + ε. The Kennedy–O'Hagan approach (general knowledge) fits θ (physical parameters) and δ (model inadequacy) together, so plant data improve the prediction without destroying physical meaning. This is implementable in PyMC [W18-51] or with BoTorch GP models [W18-48].
2. **Hierarchical (multilevel) calibration.** Physics constants (activation energies, Avrami-type exponents, interface energies) are shared across 3102, 3207 and modified 3102. Alloy-specific terms (initial Mn in solution, dispersoid N₀) get their own parameters, which shrink toward a common prior. This is the statistical fix for "three models, three parameter sets" (KB ch.09 §9).
3. **Surrogate-assisted optimisation.** Once calibrated, the mean-field chain is fast enough to optimise directly. BO is reserved for *experiments* (lab or plant), where each evaluation is expensive [W18-48; W18-49].
4. **Never pure black-box ML on < 100 data points** in a 10-dimensional composition/process space. It will interpolate badly and not extrapolate (general knowledge).

### 5.4 Design of experiments for calibrating JMAK/recrystallisation models with few experiments (assessment / general knowledge)

- **Identifiability first.**
  - JMAK-type models have strongly correlated parameters: pre-factor ↔ activation energy Q, and Avrami exponent n ↔ time scale.
  - Separating Q needs at least 3 anneal temperatures spanning ≥ 40–60 K.
  - Separating n needs data between ~10 % and ~90 % recrystallised on each curve, i.e. log-spaced times around t₅₀.
  - The strain dependence (t₅₀ ∝ ε^−m) needs at least 3 cold reductions.
- **Use the existing disagreement as the prior.** The three in-house models bracket t₅₀ within about one decade at the plant conditions (KB ch.09 §9). Use that bracket to set the sampling times, two decades wide around the predicted t₅₀.
- **Sequential Bayesian design.** Fit after the first block. Then choose the next anneal (T, t, CR) that maximises posterior predictive variance or expected information gain at **plant-relevant** conditions. Use BoTorch's active-learning acquisitions [W18-48] or a simple grid evaluation.
- **Cheap high-volume signals plus expensive anchors.** Hardness and conductivity on every sample; EBSD and TEM/SEM only at a few anchor points to fix the hardness→X and conductivity→solute mappings.
- **Hold out non-isothermal production-like cycles for validation.** Never use them for fitting. They test whether the model integrates over T(t) correctly.

### 5.5 Al-specific ML/BO case studies

Not verified in this pass because the search budget ran out (§8). Before citing any Al alloy ML/BO paper, a follow-up search should verify one example each for:
- (a) BO of the composition of 7xxx/6xxx age-hardening alloys;
- (b) ML of recrystallisation or grain size in 3xxx/5xxx;
- (c) physics-informed ML for precipitation hardening.

---

## 6. Recommended pragmatic stack (Python-based, low cost)

| Layer | Primary choice | Version / licence (verified) | Why | Paid upgrade path |
|---|---|---|---|---|
| Thermodynamics | **pycalphad** | 0.11.2, MIT [W18-14] | Open; reads TDB; kawin's backend [W18-23] | TCAL+MOBAL via TC-Python [W18-06], or PanAl [W18-09] |
| Database | COST 507 for screening + **custom Al-Mn-Fe-Si(-Mg-Cu) TDB** refitted with ESPEI to KB ch.04 solubility data and our conductivity data | COST 507 free [W18-17]; ESPEI MIT [W18-16] | The open α-phase description is inadequate [W18-17] | Licensed TCAL/PanAl tables exported once and fitted to a reduced model |
| Solidification | **scheil** | 0.3.0, MIT [W18-15] | Gives the initial segregation profile for homogenisation | Thermo-Calc Scheil with back-diffusion (not verified) |
| Dispersoid / precipitation kinetics | **kawin** (effective Al–Mn(–Si) α-phase, dislocation + bulk nucleation, real T(t)) | 0.5.0, MIT [W18-23] | Only open KWN with CALPHAD coupling, T(t), Zener-coupled grain growth and strength [W18-24] | MatCalc [W18-20] or TC-PRISMA [W18-05] |
| Work hardening (cold rolling) | Custom one-internal-variable (Kocks–Mecking / ALFLOW-type) model | — | Literature form in [W18-32]; parameters from KB ch.07 §10 | — |
| Recovery + recrystallisation + grain growth | Custom **ALSOFT-type** module; grain growth via kawin `GrainGrowthModel` with a T-dependent mobility added | — | ALSOFT is validated on Al-Mn-Fe-Si [W18-31]; the kawin GG mobility is constant by default [W18-24] | — |
| Properties | Hall–Petch + solid solution + Orowan (kawin `Strength.py` for the particle part) + conductivity (Matthiessen-type sum) | MIT [W18-24] | Physically interpretable | TCAL resistivity data [W18-03] |
| EBSD / texture analysis | **orix** (Python) or **MTEX** (MATLAB) | GPL-3.0 [W18-44] / GPL-2.0 [W18-43] | Grain size, recrystallised fraction (GOS), cube fraction | — |
| Calibration | **PyMC** (+ emcee for black-box), **SALib** | 6.3.2 Apache-2.0 [W18-51]; 3.1.6 MIT [W18-52]; 1.6.0 MIT [W18-53] | Hierarchical Bayesian with UQ | — |
| Optimisation / experiment selection | **BoTorch** or **Ax** | 0.18.1 MIT [W18-48]; 1.3.1 MIT [W18-49] | Constrained, multi-objective, noisy | — |
| Optional mechanism checks | SPPARKS, MOOSE phase-field, VPSC8 | GPL-2.0 [W18-40]; LGPL-2.1 [W18-38]; BSD-3 [W18-42] | Validate mean-field assumptions; texture | DAMASK (AGPL) [W18-41] |

**Justification (assessment).**
- Every core component is free, Python-native and version-pinnable. Licences are permissive (MIT/Apache/BSD) except the GPL EBSD tools, which are fine for internal use.
- kawin and pycalphad both require Python ≥ 3.11 [W18-14; W18-23].
- The weak link is **thermodynamic data for α-Al(Mn,Fe)Si**, not software. Spending money on a short TCAL/PanAl or MatCalc licence (or a consultancy run) gives the highest return. Use it to produce solvus, driving-force and mobility tables that are then frozen into the open model.
- Avoid building on scikit-optimize (archived [W18-50]) or DREAM.3D (deprecated [W18-46]).

---

## 7. Recommended architecture for a physically based Al alloy-design model

### 7.1 Diagram

```
                 DECISION VARIABLES x  (bounded by EN AW spec / plant limits)
   composition: Mn, Fe, Si, Mg, Cu (+ Zn, Ti pick-up from scrap)
   process:     homogenisation T(t) [if controllable] · hot-band state · cold reduction ε
                anneal cycle T(t): heating rate, soak T, soak t, cooling · atmosphere
                                   │
                                   ▼
 ┌──────────────────────────────── PHYSICS CHAIN f_phys(x; θ) ────────────────────────────────┐
 │ M1 Thermo (pycalphad + custom TDB / TCAL tables)                                           │
 │     solvus c_eq(T), driving force ΔG_v(T,c), Mn mobility ──────────────┐                   │
 │ M2 Solidification (scheil)                                             │                   │
 │     constituent fraction & type, Mn/Si segregation profile c(x) ──┐    │                   │
 │ M3 Homogenisation + dispersoids (kawin KWN on real T(t), slices)  ▼    ▼                   │
 │     Mn_ss, dispersoid N, r̄, f_V; PSN particle density                                     │
 │ M4 Cold rolling (Kocks–Mecking/ALFLOW-type)                                                │
 │     ρ(ε), subgrain δ(ε), stored energy E_s(ε)                                              │
 │ M5 Anneal: recovery + RX (ALSOFT-type) + concurrent precipitation (kawin) + GG (kawin GG)  │
 │     X(t), D_rx, P_Z = f(f_V, r̄), solute drag(Mn_ss), D(t) after RX                       │
 │ M6 Properties                                                                              │
 │     HB/HV = σ0 + σ_ss(Mn,Mg,Cu) + σ_Orowan(N,r̄) + k_HP·D^-1/2 + σ_ρ(1−X)                  │
 │     conductivity = f(Mn_ss, Fe_ss, Si_ss, f_V)        MgO thickness (separate KB ch.14)    │
 └───────────────────────────────────────────┬────────────────────────────────────────────────┘
                                             ▼
             MICROSTRUCTURE + PROPERTIES ŷ  (with posterior uncertainty from θ)
                                             │
            ┌────────────────────────────────┴───────────────────────────────┐
            ▼                                                                ▼
  CALIBRATION (PyMC hierarchical,                                OPTIMISER (direct multi-objective
  δ(x) discrepancy GP, SALib ranking)                            search on calibrated model; BoTorch/Ax
  ← lab data: HB, σ_el, EBSD, DSC                                qNEHVI-type BO for choosing *real*
  ← plant data: HB, grain size, cycles                           lab/plant trials)
            ▲                                                                │
            └──────────── new experiments chosen by active learning ◄────────┘
```

Equations are the KB forms (ch.04 §4–5, §7; ch.07 §10; ch.03). The diagram itself is (assessment). The name "qNEHVI" for BoTorch's multi-objective acquisition is (general knowledge); the `multi_objective` module exists [W18-48].

### 7.2 Modules, state variables and parameters to calibrate (assessment)

| Module | State variables | Parameters calibrated here | Parameters taken from literature/CALPHAD |
|---|---|---|---|
| M2 Scheil | c(x) profile, constituent fraction | — | TDB [W18-15; W18-17] |
| M3 KWN dispersoids | PSD (N, r̄, f_V), Mn_ss | interfacial energy σ, heterogeneous site density N₀ (dislocations), effective solvus offset | D_Mn (KB ch.04/07 — note the 10³ disagreement in ch.07 G9) |
| M4 Work hardening | ρ, δ | storage and recovery coefficients (k₁, k₂ or ALFLOW equivalents) | G, b, M (Taylor) |
| M5 Recrystallisation | X, N_rx, D_rx | nucleation-site efficiency (PSN, GB, cube), boundary mobility M₀ and Q_m, solute-drag constant | P_Z from M3; E_s from M4 |
| M5 Grain growth | D | (shared M₀, Q_m) | Zener constants K, m [W18-24] |
| M6 Properties | — | σ0, k_HP, solid-solution coefficients (check against KB ch.04 §7 slopes), resistivity coefficients | Taylor factor; Orowan form [W18-24] |

### 7.3 Minimal experimental calibration plan (assessment)

Per alloy: 3102 and 3207 first; the modified 3102 when a trial cast exists. Use one well-characterised hot band or cold-rolled coil each.

| Block | Experiment | Samples (per alloy) | Measurements | Calibrates |
|---|---|---|---|---|
| A. Baseline | As-received strip (and ingot if available) | 2–4 | OES chemistry; **electrical conductivity** (eddy current); SEM-BSE + EDS constituent area fraction and Fe/Mn ratio; SEM/TEM dispersoid size and number density (1 sample); EBSD starting grain size and texture | M2/M3 initial state; anchors conductivity → Mn_ss |
| B. Work hardening | Lab or mill cold rolling to 4–5 reductions spanning the plant range (e.g. 0, ~25, ~45, ~60, ~75 %) | 5 | HV/HB; 2–3 tensile tests; conductivity (should be unchanged, which checks the M6 resistivity terms) | M4 storage/recovery; σ_ρ term |
| C. Isothermal softening | 3 CR × 3 T (spanning ≥ 50 °C, bracketing the plant soak) × 6–8 log-spaced times; fast heating (salt bath or preheated thin samples) with a thermocouple on a dummy | ~54–72 (hardness only) | HV/HB on all; conductivity on all (detects concurrent precipitation); EBSD on ~6–9 (near t₅₀ and fully recrystallised for each CR/T) for X (GOS threshold) and D_rx | M5 nucleation/mobility/Q; hardness→X mapping; D_rx(ε, T). **This block alone settles the ~7× t₅₀ disagreement** |
| D. Non-isothermal validation (hold-out) | 2–3 plant-like cycles with logged T(t), heating rates differing ≥ 5× | 3–6 | HB, conductivity, EBSD grain size | Validation only (not fitted). Tests the heating-rate/concurrent-precipitation coupling (M3 ↔ M5) |
| E. DSC (optional, cheap) | Cold-rolled samples at 2 CR, 3–4 heating rates | 6–8 | Recrystallisation/recovery exotherm peak T versus heating rate → Kissinger-type apparent Q (general knowledge). Signal may be weak at low CR in lean alloys | Independent prior/check on Q_rx |
| F. Homogenisation (only if casthouse practice is a lever) | Ingot samples, 2 T × 4 t, plus 2 heating rates | ~10 | Conductivity; SEM dispersoid N, r̄; constituent transformation | M3 σ, N₀, solvus offset |
| G. MgO (link to KB ch.14) | Same Block C/D samples | 6–9 | Oxide thickness (GDOES/XPS) | Parabolic oxide-growth constants (outside the recrystallisation model but in the same optimiser) |

**Sequencing.**
1. Do A → B → C first. Fit the model.
2. Run SALib to confirm which parameters matter.
3. Choose 3–6 extra Block C points by active learning.
4. Only then run D (validation) and decide whether F is needed.

Roughly 80–100 hardness/conductivity samples and about 15–20 EBSD maps per alloy are the minimum to replace the current uncalibrated JMAK sheets with one calibrated model that carries uncertainty.

### 7.4 Bayesian calibration workflow (assessment)

1. **Priors.**
   - Weakly informative, from literature (KB ch.03/ch.04) and the span of the in-house models (KB ch.09).
   - Log-normal priors on positive quantities. Q_rx and Q_m are bounded to physically sensible ranges.
2. **Likelihood.**
   - Hardness and conductivity: Gaussian with a measurement-error term (estimated from repeat indents and readings).
   - Grain size: log-normal.
   - Recrystallised fraction: Beta.
3. **Hierarchy.** Shared physics parameters across alloys; alloy-level offsets for Mn_ss and dispersoid state.
4. **Discrepancy.** Add a GP δ(T, ε) on hardness only if the posterior-predictive checks on Block D fail.
5. **Diagnostics.** R̂, effective sample size, posterior correlations (expect Q ↔ pre-factor). Prior sensitivity.
6. **Output.** The posterior predictive for HB and grain size of any proposed cycle → probability of meeting 23–33 HB and 20–100 µm. This is the quantity the optimiser should use.

### 7.5 Optimiser formulation (assessment)

- **Objectives.** Maximise P(HB ∈ [23, 33]) and P(D ∈ [20, 100] µm). Minimise MgO thickness and cycle time/energy. Optionally maximise the strength margin for thinner walls (modified 3102).
- **Constraints.** EN AW composition limits. Scrap-driven ranges of Fe, Cu, Mg and Zn treated as *noise variables*, i.e. robust optimisation over the composition scatter. Furnace capability (heating rate, T limits). Mill reduction limits (KB ch.09 §5).
- **Method.**
  - Run multi-objective search directly on the calibrated model (cheap evaluations).
  - Use BoTorch/Ax only to choose which candidate cycles or compositions to *test* in the lab or plant, with constrained, noisy, multi-objective acquisition [W18-48; W18-49].

### 7.6 Risks (assessment unless cited)

| Risk | Consequence | Mitigation |
|---|---|---|
| Open TDB lacks α-Al(Mn,Fe)Si solution [W18-17] | Wrong Mn solvus, so wrong Mn_ss, dispersoid f_V and Zener drag | Refit with ESPEI to KB ch.04 solubility tables and Block A/F conductivity; or buy TCAL/PanAl tables once |
| Mn diffusivity uncertainty (KB ch.07 G9: 10³ spread) | KWN time scales off by orders of magnitude | Calibrate an effective D_Mn on Block F/C conductivity kinetics; take a prior from MOBAL if licensed [W18-04] |
| KWN non-identifiability (σ ↔ N₀ ↔ D) | Many parameter sets fit the same data | Fix σ from literature; fit N₀ and an effective D; report posterior correlations |
| Heterogeneous dispersoid nucleation (precursor phases, dislocations, DFZ) not in the mean-field model | Under- or over-prediction of N | Use kawin dislocation sites [W18-24]; slice model across the dendrite (KB ch.04 §4) |
| Hardness→X mapping ignores recovery | Biased n and Q | EBSD anchor points; model recovery explicitly (ALSOFT-type [W18-31]) |
| Single-maintainer open codes (kawin) [W18-23] | API breaks; abandonment | Pin versions; keep our own tests; isolate behind an interface |
| Extrapolation outside the calibration window (new compositions such as modified 3102 at Mn 1.1–1.3 %) | Over-confident designs | Posterior-predictive intervals; at least one lab cast before a plant trial |
| Licence misuse (Educational Thermo-Calc is teaching-only [W18-07]; AGPL for DAMASK if distributed [W18-41]) | Legal exposure | Use commercial licences for industrial runs; keep AGPL/GPL tools internal |
| Over-fitting with ML on few points | Spurious optima | Physics-first model; ML only for residuals; hold-out Block D |

---

## 8. Open questions / not verified

1. **Network and search limits.** Vendor pages (Thermo-Calc, CompuTherm, MatCalc, FactSage, OpenCalphad, kawin.org) could not be opened. All S-flagged facts, especially TCAL11 counts, PanAl counts and the Educational licence terms, should be re-checked on the official pages before procurement.
2. **Not verified at all in this pass** (search budget exhausted):
   - Abaqus, DEFORM, Simufact Forming and QForm: capabilities, Al microstructure coupling, prices;
   - OpenPhase; AFLOW;
   - Citrine platform capabilities;
   - MatCalc's feature list and free-version terms on the official site (the 3-element limit comes from a third-party README [W18-22]);
   - JMatPro's current module list and price;
   - Hydro's in-house through-process tools.
3. **Al-specific ML/BO case studies** (§5.5) need a dedicated search.
4. **ALSOFT/ALFLOW equations.** Retrieve the original papers (Vatne–Furu–Ørsund–Nes 1996; Nes 1997 *Prog. Mater. Sci.*; Nes & Marthinsen 2002 *MSE A*) and the EN AW-3103 through-process chapter [W18-36]. These are the templates for M4/M5. Bibliographic details are partly from search extracts [W18-31; W18-32].
5. **Du et al. (2013) homogenisation model** [W18-26]: read the full text for nucleation treatment, σ and D_Mn values and the validation data. It is the best starting point for M3.
6. **Does PanAl or TCAL11 model Mn in α-AlFeSi as a continuous solution?** The TCAL revision history mentions Mn solubility in Al₈Fe₂Si [W18-08]; PanAl has an Alpha_AlFeSi phase [W18-09]. Check this before buying.
7. **mc_al (MatCalc open database):** content for Mn/Fe/Si phases and whether it can be converted to pycalphad TDB format — not verified [W18-21].
8. **kawin limits:**
   - grain-growth mobility is constant by default [W18-24];
   - primary recrystallisation is not included (inference from source files read);
   - the multicomponent α-phase with Fe↔Mn exchange has not been tested;
   - the possible duplicate-contribution bug noted in `Strength.py` `computeCRSS` (reported by the fetch summary) should be checked against the source before use.
9. **D_Sc/D_Zr conflict** (§2.3): reconcile KB ch.04 (≈ 4) with the Arrhenius sets in the kawin examples (≈ 640 at 480 °C, derived).
10. **DSC sensitivity** for recrystallisation in lean 3xxx at moderate CR — check feasibility on one sample before committing to Block E.
11. **Conductivity coefficients** (resistivity per wt% Mn, Fe, Si in solution and per vol% dispersoid) remain missing (KB ch.04 §12 item 11). They are needed to turn Block A/C/F conductivity into Mn_ss. TCAL resistivity data [W18-03] or the literature are the candidate sources.
