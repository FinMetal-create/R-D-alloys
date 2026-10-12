# 11 — Aerosol-can slugs: industry practice, alloys, specifications and requirements (online research)

> **Source type: online research (not from the user's Drive), retrieved 2026-10-12.**
>
> **Scope.** This chapter covers the industry, application and specification side of aluminium slugs for cold
> backward impact extrusion of monobloc aerosol cans, plus tubes and bottles where the sources overlap:
> - which alloys are used and why;
> - slug specifications and annealing practice;
> - slug production routes and producers;
> - legal and industry pressure requirements and lacquer-bake softening;
> - published lightweighting cases.
>
> Extrusion mechanics (loads, strain paths, ductile failure) are **not** covered here. They are in
> `knowledge/10-impact-extrusion-and-slug-metallurgy.md` (Sillekens thesis). The user's own data are in
> `knowledge/09-in-house-rd-data.md`. This chapter only *points* to chapter 09 sections by number and never
> repeats their numbers.
>
> **Access limitation. Read this before using any number below.** During this session the network policy
> blocked every page fetch: WebFetch returned DNS failures and the egress proxy refused HTTPS CONNECT for
> patents.google.com, ball.com, eur-lex.europa.eu, wikipedia.org and other sites. The session's web-search budget
> also ran out before the planned follow-up queries could run, including the full Turk et al. paper, the Tubex
> datasheet, EN 570 tables and FEA standards. **Every finding in this chapter therefore rests on search-engine
> result text, not on a fetched page, and is marked "(snippet only)".** Search summaries can mis-attribute text
> between documents that appear in the same result list. Where the snippet did not say clearly which document a
> statement came from, the citation says so. Treat all numbers as *leads to verify against the primary document*
> before design use.
>
> **Conventions.**
> - `[W11-xx]` cites the sources table below.
> - *(derived)* marks arithmetic I did on cited numbers, such as unit conversions or ratios.
> - *(inference)* marks a design conclusion drawn from cited facts.
> - *(general knowledge)* marks physical-metallurgy background not taken from the W11 sources. Such statements
>   are kept to mechanisms and are not used as specification values.
> - Marketing claims are labelled **[marketing]**.

---

## 0. Sources

Types:
- **patent**: technical disclosure by an industrial applicant. Treat it as an industry source; examples are
  real data, but claims are drafted broadly.
- **peer-reviewed**
- **standard / regulation**
- **industry**: company technical page or trade press
- **marketing**: product page or sales claim

"Verified" means seen in search-result text only. No page was fetched (see the access limitation above).

| Key | Title | Author / organisation | Year | URL | Type | What was seen (all snippet only) |
|---|---|---|---|---|---|---|
| W11-01 | US 10,584,402 B2, *Aluminum alloy slug for impact extrusion* | Ball Corporation (assignee per Justia listing) | 2020 (issued 10 Mar 2020) | https://patents.justia.com/patent/10584402 ; https://patents.google.com/patent/US10584402B2/en | patent | Claim-1 composition ranges; 1070 (or 1050) + 3104/3105 blend ratios; Table 5 slug HB (1050 reference vs two recycled materials); batch anneal window; finishing (shot-blasted vs tumbled) |
| W11-02 | US 11,519,057 B2, *Aluminum alloy for impact extruded containers and method of making the same* | Ball Corporation | filed 2016-12-30, granted 2022-12-06 | https://patents.google.com/patent/US11519057B2/de | patent | Stated aim of greater back-annealing resistance, enabling higher-temperature cure linings; list of 3xxx scrap alloys; existence of Table 6 (buckle and burst pressures, 1070 + 3104 blends) and HB before/after annealing (values **not** captured); lightweighting claim |
| W11-03 | WO 2013/040339 A1 family: *Impact extruded containers from recycled aluminum scrap* (US 9,663,846 B2; US 12,385,112 B2; EP 3141624; EP 3144403; AU 2018241184) | Ball Corporation | priority 2011-09-16 | https://patents.google.com/patent/WO2013040339A1/en ; https://patents.google.com/patent/AU2018241184B2/en | patent | 40 % 3104 + 1070 example; HB about 35 % and 43 % above 1050; punching tonnage; lower container weight; "ReAl" naming; continuous-anneal description; MgO abrasion; casting-route (twin-belt vs wheel-belt) text |
| W11-04 | US 2014/0298641 (US 9,517,498; US 9,844,805; US 12,330,201), *Aluminum impact extruded bottle with threaded neck made from recycled aluminum and enhanced alloys* | Ball Corporation | 2014 (application) | https://patents.justia.com/patent/20140298641 | patent | Back-annealing-resistance statement, shared with W11-01 |
| W11-05 | EP 3075875 A1, *Aluminium alloy for aerosol cans manufactured by the impact extrusion and the process for preparation thereof* | TALUM d.d. Kidričevo | filed 2016-03-29, publ. 2016-10-05 | https://www.freepatentsonline.com/EP3075875.html ; https://patents.google.com/patent/EP3075875A1/en | patent | Claimed composition (Al–Fe–Mn–Zr, very low Mg/Cu/Zn); recrystallisation-threshold shift; properties kept through lacquer polymerisation; about 5 bar higher burst pressure |
| W11-06 | J. Turk et al., "Development of aluminium alloys for aerosol cans", *Materiali in tehnologije / Materials and Technology* 50(4) 601–605, doi:10.17222/mit.2015.330 | J. Turk et al. (affiliation not captured) | 2016 | http://mit.imt.si/Revija/izvodi/mit164/kores.pdf ; https://www.researchgate.net/publication/306242504 | peer-reviewed | Narrow strip from a rotary strip caster used for slugs; up to 15 % loss of mechanical properties during can manufacture; deformation and burst pressure raised by > 10 % with the new alloys |
| W11-07 | EP 3031941 B1, *Heat resistant alloy for production of aerosol cans* (related: EP 2881477 B1, same title) | Moravia Cans a.s.; inventors J. Sedláček, R. Divoký, J. Křovina, V. Foksová | filed 2013-12-06, B1 publ. 2017 | https://patents.google.com/patent/EP3031941B1/en ; https://data.epo.org/gpi/EP2881477B1 | patent | EN AW-3207 modified with Zr as an anti-recrystallisation addition (ranges **not** captured) |
| W11-08 | US 12,453,995, *Method for manufacturing an aluminium tube, a method for manufacturing an aluminium slug, an aluminium tube and an aluminium slug* | applicant not captured | n/a | https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/12453995 | patent | Example: slugs containing post-industrial EN AW-1070A tube scrap, annealed about 500–520 °C for about 2–3 h, then cooled at < 0.05 K/s. *Attributed to this document by search ranking; verify.* |
| W11-09 | US 4,243,438, *Production of aluminum impact extrusions* | assignee not captured | n/a | https://patents.google.com/patent/US4243438A/en | patent | Slugs "typically softened" by heating to about 300–600 °C, with time set by the extrusion work required |
| W11-10 | US 7,520,044 B2, *Aerosol can fabrication process* | assignee not captured | n/a | https://patents.google.com/patent/US7520044 | patent | Melt, continuous casting on a casting wheel, hot and cold rolling, slugs cut on a cutting press. *Attributed by search ranking; verify.* |
| W11-11 | EN 570:2007, *Aluminium and aluminium alloys – Impact extrusion slugs obtained from wrought products – Specification* (CEN/TC 132/WG 11) | CEN (BSI / DIN editions) | 2007 | https://standards.iteh.ai/catalog/standards/cen/788a1dbb-6332-487e-a0f1-f31f27977c5b/en-570-2007 ; https://knowledge.bsigroup.com/products/aluminium-and-aluminium-alloys-impact-extrusion-slugs-obtained-from-wrought-products-specification | standard | Scope (punched from rolled or cut from extruded product; flat or preformed slugs); contents (composition, mechanical properties, Brinell test to EN ISO 6506-1, tolerances); O-temper supply with approximate HB "for guidance"; replaces EN 570:1994. **Tables not seen.** |
| W11-12 | Council Directive 75/324/EEC on aerosol dispensers, consolidated text (incl. Directive 2008/47/EC) | European Union | 1975; consolidated 2013 / 2018 | https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:01975L0324-20180212 ; https://publications.europa.eu/resource/cellar/77ad1ca4-5035-4b21-8d2a-754724319a87.0029.02/DOC_1 | regulation | Definitions of test and bursting pressure; 6.7 bar threshold; 10 bar minimum test pressure; test pressure = 1.5 × pressure at 50 °C; burst ≥ 20 % above test pressure; 12 bar at 50 °C maximum (2008 amendment) |
| W11-13 | Commission Directive (EU) 2016/2037 amending 75/324/EEC (maximum allowable pressure) | European Commission | 2016 | https://eur-lex.europa.eu/eli/dir/2016/2037/oj | regulation | Pressure at 50 °C: 12 / 13.2 / 15 bar by propellant category; purpose: non-flammable propellants (N₂, compressed air, CO₂) |
| W11-14 | 49 CFR § 173.306, *Limited quantities of compressed gases* | US DOT / PHMSA (via Cornell LII) | current | https://www.law.cornell.edu/cfr/text/49/173.306 | regulation | Pressure tiers at 130 °F (54.4 °C) for non-DOT, 2P, 2Q and 2Q1 containers; 180 psig ceiling; no burst at ≥ 1.5 × equilibrium pressure at 130 °F |
| W11-15 | US 10,843,864 / US 11,511,929, *Metallic container dome configured to deform at a predetermined pressure* | assignee not captured | n/a | https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/11511929 | patent | Dome designed to roll outward at about 225–230 psig and vent at ≥ about 240 psig, to meet the DOT 2P1 bottom specification |
| W11-16 | Aerosol formulation patents returned for the DOT query (US 8,191,739; US 5,124,395) | assignees not captured | n/a | https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/8191739 | patent (secondary on regulation) | Descriptions of DOT 2P (no distortion < 160 psig, no burst < 240 psig) and 2Q (< 180 / < 270 psig). *Exact member not identified.* |
| W11-17 | *ReAl lightweight aerosol* product page | Ball Corporation | accessed 2026 | https://ball.com/packaging/aerosol-cans/aluminum-aerosol-cans/real-lightweight-aerosol | marketing | About 15 % lighter than the standard can, with higher strength |
| W11-18 | *Ball and Henkel launch an even more sustainable aluminum aerosol package* (press release) | Ball Corporation | c. 2015 (date not captured) | https://investors.ball.com/news-presentations/press-releases/detail/366/ball-and-henkel-launch-an-even-more-sustainable-aluminum-aerosol-package | marketing | 2014 ReAl: 25 % recycled, 11 % lighter; later iteration 15 % lighter; about 12 % carbon-footprint cut; Henkel Fa 150/200 ml |
| W11-19 | Trade press on ReAl: CanTech "Ball's even lighter ReAl cans"; Packaging Digest "Breakthrough creates recycled-content aluminum aerosol can"; AlCircle "Ball–Unilever partnership to bring a lighter weight aluminium aerosol can" | CanTech International; Packaging Digest; AlCircle | 2014–2017 | https://www.cantechonline.com/news/8265/balls-even-lighter-real-cans/ ; https://www.packagingdigest.com/sustainability/breakthrough-creates-recycled-content-aluminum-aerosol-can ; https://www.alcircle.com/news/ball-unilever-partnership-to-bring-a-lighter-weight-aluminium-aerosol-can-27543 | industry (reports marketing figures) | Unilever Rexona/Sure 2017: about 20 % lighter, 18 % lower carbon footprint (150 ml) |
| W11-20 | SprayTM, "Ball launches lighter, aluminum aerosol can with up to 50 % recycled content" | SprayTM | 2022 | https://spraytm.com/?p=19291 | industry (reports marketing figures) | re:generation can: up to 50 % recycled content plus low-carbon (renewable-power) primary aluminium |
| W11-21 | CanTech "Tubex launches lightweighted aerosol can"; The Canmaker "Innovative aluminium aerosol can is 20 per cent lighter" | CanTech International; The Canmaker | 2018–2019 (approx.) | https://www.cantechonline.com/news/24074/tubex-launches-lightweighted-aerosol-can/ ; https://canmaker.com/innovative-impact-extruded-aluminium-aerosol-is-20-per-cent-lighter/ | industry (reports marketing figures) | Tubex + Neuman Aluminium patented slug (2018); wall thickness and shoulder reworked; close to 20 % lighter than a standard Al 99.5 can; higher dent susceptibility in transit |
| W11-22 | Tubex product pages, *Technical Data AEROSOL-CANS Aluminium, monobloc* (07/2022), World Star award news | Tubex GmbH; CanTech | 2022–2023 | https://tubex.de/en/products-overview/products/ ; https://tubex.de/wp-content/uploads/TUBEX-Download-Aluminiumdosen-Datenblatt-ENG-07_2022-1.pdf ; https://www.cantechonline.com/news/26596/tubex-receives-world-star-award-for-aerosol-deodorant-can/ | marketing / datasheet (datasheet **not** read) | "Neucan 3.1" slug; "up to 20 % less weight with the same stability"; up to 60 % PCR; "real PCR / Standard PCR" options; Rexona can with 25 % real PCR, 14 % lighter than its predecessor |
| W11-23 | *Impact extrusion* technology page | Neuman Aluminium | n/a | https://neuman.at/technology/impact-extrusion | industry | Cold forming on mechanical knuckle-joint presses; strain hardening |
| W11-24 | *Twin-belt casting machine* listing | Hazelett Corporation (AlCircle business directory) | n/a | https://www.alcircle.com/biz/hazelett-corporation-products/30553/twinbelt-casting-machine | marketing | Twin-belt strip offered for impact-extrusion slugs; surface quality from controlled heat transfer through the belts |
| W11-25 | *What we do* | Aluman S.A. (Greece) | n/a | https://www.aluman.gr/about-us/what-we-do/ | industry | Casthouse, casting wheel, hot rolling, quench, cold rolling; slugs for monobloc aerosol cans and collapsible tubes |
| W11-26 | *Aluminium Rheinfelden* (group geography page) | UC RUSAL | n/a | https://www.rusal.ru/en/about/geography/aluminium-rheinfelden-en/ | industry | Rheinfelden semis: slugs, aerosol cans, tube; semis capacity 31,000 t/y |
| W11-27 | "CCL to invest in new plant to produce aluminum slugs in Clinton, North Carolina" | AlCircle | 2014 | https://www.alcircle.com/news/ccl-to-invest-in-new-plant-to-produce-aluminum-slugs-in-clinton-north-carolina-20472 | industry | CCL–Rheinfelden Semis JV slug plant; about US$18 M; 25,000 t by 2018 (plan) |
| W11-28 | *Technical punch slugs* | Ball Corporation | n/a | https://ball.com/packaging/aluminum-slugs/technical-punch-slugs | marketing | A slug supplier listing 1050A and 3102; QMS monitors hardness, chemistry, temperature and dimensions. *Attribution to this page inferred from search ranking.* |
| W11-29 | Chinese slug-supplier product pages (Chalco 1050 slug; Tomorrow Aluminium; Fuchuan Metal; Haomei; Sigma Aluminum 3003 slug; Qichuang) | various | n/a | https://www.chalcoaluminum.com/product/aluminum-slug/1050-aluminum-slug/ ; https://www.tomorrowal.com/aluminium-slug ; https://www.fuchuanmetal.com/ ; http://aluminium-slugs.com/Products.html ; https://www.sigma-aluminum.com/products/3003-alloy-aluminum-slug/ ; https://www.qichuangal.com/ | marketing | Example HB values; alloys offered (1050, 1070, 3003, 6061, 6063); process lists; dimension ranges |
| W11-30 | "Use of epoxy–phenolic lacquers in food can coatings: characterization of lacquers and cured films" | authors not captured (CONICET repository) | n/a | https://ri.conicet.gov.ar/bitstream/handle/11336/70449/CONICET_Digital_Nro.bccfd85a-3d22-4aa1-800a-e8673c7bde87_A.pdf | peer-reviewed (food cans, not aerosol) | Industrial cure 200 °C / 12 min; study range 170–220 °C, 12–36 min |
| W11-31 | *Internal lacquer of aluminum tubes* | Beautysky Packaging (tube supplier blog) | n/a | https://beautyskypackaging.com/internal-lacquer-of-aluminum-tubes/ | marketing | Internal spray coat baked at, for example, 250 °C for 5 min |
| W11-32 | Monobloc aerosol interior-coating patent returned for the PAM query (likely US 12,139,297, *Coating composition for packaging articles*) | assignee not captured | n/a | https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/12139297 | patent | Epoxy-phenolic control softened after 12–24 h in chloroform; polyamide-imide (PAM) control did not after 3 days. *Exact member not confirmed.* |
| W11-33 | *Aluminum aerosol cans* | CCL Container | n/a | https://cclcontainer.com/aluminum-packaging/aluminum-aerosol-cans/ | marketing | Liner options: PAM, epoxy-phenolic, beverage-compatible |
| W11-34 | Paper on oven-control system for AA1050 collapsible-tube annealing | Universitas Diponegoro (J. Teknik Mesin) | n/a | https://ejournal3.undip.ac.id/index.php/jtm/article/view/53689 | academic (control engineering) | Tube annealing oven at 350–450 °C |
| W11-35 | "2026 Essential Guide: Safety standards for aerosol can top and bottom ends" | Worunda Metal Packaging | 2026 | https://www.worunda.com/2026-professional-safety-standards-for-aerosol-can-top-and-bottom-ends-withstanding-high-burst-pressure-in-chemical-packaging/ | marketing | Claims an EU "1.5 × burst" rule. **Conflicts with W11-12; listed only as a caution.** |
| W11-36 | Explainers of the EU Aerosol Dispensers Directive: F2 Labs technote; CanTech "Europe versus US on aerosol can regulation" | F2 Labs; CanTech International | 2017; n/a | https://f2labs.com/technotes/aerosol-dispensers-directive-75-324-eec ; https://www.cantechonline.com/feature/11888/europe-versus-us-aerosol-can-regulation/ | industry | One of the two restates "burst ≥ 20 % above test pressure". *Which one could not be pinned down.* |
| W11-37 | BS 3914-1:1974, *Specification for aerosol dispensers – non-returnable metal containers up to 1400 cm³ and 85 mm diameter* | BSI | 1974 (withdrawn 1991) | https://knowledge.bsigroup.com/products/specification-for-aerosol-dispensers-non-returnable-metal-containers-up-to-1400-cm-sup-3-sup-and-85-mm-diameter | standard (withdrawn) | Existence, scope and withdrawal date only |

Source count by type:
- patent: 12 keys (W11-01 to 05, 07 to 10, 15, 16, 32; EP 2881477 is folded into W11-07)
- peer-reviewed / academic: 3 (W11-06, W11-30, W11-34)
- standard / regulation: 5 (W11-11 to 14, W11-37)
- industry (company technical or trade press): 8 (W11-19 to 21, 23, 25 to 27, 36)
- marketing: 9 (W11-17, 18, 22, 24, 28, 29, 31, 33, 35)

---

## 1. Alloys for impact-extruded aerosol cans and tubes: what is used and why

### 1.1 Findings

- **The baseline is near-pure aluminium.**
  - Conventional impact extrusion uses "almost pure or 'virgin' aluminum", typically 1070 or 1050
    [W11-01, W11-03] (snippet only).
  - The Talum patent and paper name EN AW-1070A (A7, 99.7 % Al) and EN AW-1050A (A5) as the conventional can
    materials [W11-05, W11-06] (snippet only).
  - The search summary gave "99.9 %" for A5/1050A. That conflicts with the 99.50 % minimum of 1050A
    *(general knowledge)* and is probably an extraction error.
  - Tube slugs are typically 1070 or 1050 [W11-29] (snippet only, marketing).
- **Why aerosol cans are heavy.** Ball's patents describe aerosol cans as pressure vessels that "require high
  strength, and thus use thicker gage and heavier materials than traditional aluminum beverage containers"
  [W11-01–W11-03] (snippet only; exact family member not identified). The wall is thickened mainly to meet
  pressure resistance and safety standards (same family, snippet only).
- **Why recycled 3xxx was historically excluded.**
  - The process needs very pure, soft alloys. Recycled 3104, 3105 or 3004 "have not been used in this
    application" [W11-03, W11-01] (snippet only).
  - Higher-alloyed scrap such as beverage-can **cupper offal** "complicates casting" [W11-01] (snippet only).
  - Higher tensile and yield strength raise the **tonnage needed to punch slugs** [W11-03] (snippet only).
- **Ball's "ReAl" route: dilute 3104 scrap into 1070.**
  - "ReAl"/"RE" is an identifier for metal containing recycled aluminium, typically 3104 recycled together with
    1070. The number after "ReAl" gives the percentage of 3104 [W11-01, W11-02] (snippet only).
  - The 3104 scrap is commonly sourced from beverage-can plants [W11-03] (snippet only).
  - Claimed blends: 40–90 wt % 1070 (or 1050) with 10–60 wt % 3xxx (3104/3105). Dependent claims narrow this to
    60–80 % 1070, balance 3104. Examples include "ReAl 3104 25 %" and a 40 % 3104 blend [W11-01, W11-03]
    (snippet only).
  - The listed scrap sources are 3104, 3004, 3003, 3013, 3103 and 3105 [W11-02, W11-03] (snippet only).
- **Strength gain and its purpose.** The added strength "allows standard container specifications to be met at
  significant lower container weights and/or wall thicknesses". Patent claims say light-weighted (thinned
  wall and bottom) recycled-blend cans meet burst requirements where 1070/1050 cans cannot [W11-02, W11-03]
  (snippet only). The numerical buckle/burst data (W11-02 Table 6, Figs 6–8) were **not** captured.
- **Back-annealing resistance is an explicit design goal in three independent patent families:**
  - Ball: the alloy has "higher back annealing resistance", which "supports coatings that require higher curing
    temperatures" [W11-01, W11-02, W11-04] (snippet only).
  - Talum: EP 3075875 claims an **Al–Fe–Mn–Zr** alloy (very low Mg, Cu, Zn). It "moves the recrystallization
    threshold to higher temperatures", so mechanical properties survive the post-forming lacquer
    *polymerisation*, and cans tolerate burst pressures "about 5 bar higher" [W11-05] (snippet only).
  - Moravia Cans: EP 3031941 claims a "heat resistant" **EN AW-3207 modified with Zr** as an
    anti-recrystallisation addition [W11-07] (snippet only).
- **Peer-reviewed confirmation of the problem.** Turk et al. (2016) report that can manufacture "can reduce the
  material's mechanical properties by up to 15 %", lowering deformation and burst pressures. Their new alloys
  (slugs from narrow strip cast on a rotary strip caster) give "constant mechanical properties during
  manufacture" and raise deformability and burst pressure by > 10 % [W11-06] (snippet only; full paper not read,
  alloy chemistry not captured).
- **Other families.**
  - Al–Mg–Si aerosol-can alloys were proposed in older patents, but their "mechanical characteristics … drop
    substantially in the application step of a lacquer inside the can". This comes from patent background text
    in the W11-01/W11-10 result set; exact member not identified (snippet only).
  - Suppliers also offer 3003, 6061 and 6063 slugs [W11-29] (marketing, snippet only).
  - A Ball slug page appears to list 1050A and 3102 among offered alloys [W11-28] (marketing; attribution
    inferred, snippet only).

**Table 1.1 — Alloy families documented for aerosol/tube slugs (wt %; claim ranges, not specifications)**

| Family / designation | Si | Fe | Mn | Mg | Cu | Zn | Other | Strengthening / thermal-stability idea | Source |
|---|---|---|---|---|---|---|---|---|---|
| EN AW-1070A / 1050A (baseline) | n/c | n/c | n/c | n/c | n/c | n/c | Al ≥ 99.7 / ≥ 99.5 *(general knowledge)* | Soft, high extrudability; strength only from extrusion work hardening | W11-01, W11-05, W11-06 |
| Ball "ReAl" (1070 + 10–60 % 3104/3105), claim 1 of US 10,584,402 | 0.10–0.38 | 0.25–0.5 | 0.07–0.61 | 0.05–0.73 | 0.05–0.19 | 0.03–0.25 | Cr 0.02–0.13; Ti ≈ 0.01 | Solute Mg (+ Mn, Cu) from scrap; Mn dispersoids; claimed back-anneal resistance | W11-01 |
| Talum Al–Fe–Mn–Zr, claim of EP 3075875 A1 | 0.05–0.2 | 0.1–0.55 | 0.01–0.6 | < 0.01 | < 0.01 | < 0.02 | Zr 0.05–0.2; Ti ≤ 0.03 | Zr (with Mn) raises the RX threshold so the work-hardened wall survives the lacquer cure | W11-05 |
| Moravia Cans "heat resistant" 3207 + Zr, EP 3031941 B1 | n/c | n/c | n/c | n/c | n/c | n/c | Zr addition (range n/c) | Same idea on an EN AW-3207 base | W11-07 |
| EN AW-3102 | n/c | n/c | n/c | n/c | n/c | n/c | — | Listed as a slug alloy by a supplier | W11-28 (marketing) |
| 3003, 6061, 6063 slugs | n/c | n/c | n/c | n/c | n/c | n/c | — | Offered by Chinese suppliers (use not stated) | W11-29 (marketing) |

n/c = not captured (snippet did not include it). All rows are snippet only.

*Consistency check (derived; general-knowledge 3104 limits, verify against EN 573-3).* AA3104 typically has
Mn ≈ 0.8–1.4 % and Mg ≈ 0.8–1.3 % *(general knowledge)*. Diluting 10–60 % of it into 1070 gives Mn ≈ 0.08–0.8 %
and Mg ≈ 0.08–0.8 %, which brackets the claim-1 ranges in Table 1.1. A **25 % ReAl blend** would carry roughly
0.2–0.35 % Mn and 0.2–0.3 % Mg *(derived)*. Chemically that is a *lean Al–Mn–Mg alloy*, close to the 3102/3207
space, but with Mg and Cu levels that standard 3102 and 3207 do not deliberately contain *(inference)*.

**Table 1.2 — Recycled-content and impurity-tolerance evidence**

| Item | Value | Source |
|---|---|---|
| 3xxx scrap share claimed in a 1070 base | 10–60 wt % (claims 2–3: 20–40 % 3104) | W11-01 (snippet only) |
| ReAl launch recycled content | 25 % | W11-18 (marketing, snippet only) |
| Ball re:generation can | up to 50 % recycled plus low-carbon primary | W11-20 (trade press, snippet only) |
| Tubex Neucan 3.1 | up to 60 % "high-purity" PCR; "real PCR" vs "Standard PCR" grades | W11-22 (marketing, snippet only) |
| Tubex Rexona can | 25 % real PCR, "patented alloy" | W11-22 (marketing, snippet only) |
| Recycled tube slugs | post-industrial EN AW-1070A tube scrap as feed | W11-08 (snippet only) |
| Talum alloy residual limits | Mg < 0.01, Cu < 0.01, Zn < 0.02 | W11-05 (snippet only) |

No source captured explicit **maximum Fe, Si, Cu or Zn pick-up limits** for recycled slug alloys (see §6).

### 1.2 Design levers for slug alloy design

The levers below mix inference and general knowledge, anchored on the cited facts.

1. **Design for post-bake wall strength, not slug strength.** All three patent families (Ball, Talum,
   Moravia) and Turk et al. target the property loss during lacquer cure [W11-01, W11-05–W11-07]. The
   performance-relevant property is the work-hardened can wall *after* the bake. The slug only needs to be soft
   and uniform.
2. **Three routes to back-anneal resistance have been published:**
   - (a) **Solute route** (Ball): Mg, Mn and Cu from 3104 scrap.
     - Benefit: solute drag slows recovery and recrystallisation (RX) of the extruded wall during the bake
       *(general knowledge)*.
     - Costs: slug HB rises by about 35–43 % [W11-03], punching and extrusion tonnage rise [W11-03], and Mg
       drives abrasive MgO on annealed slugs [W11-01–W11-03, see §2].
   - (b) **Zr dispersoid route** (Talum, Moravia): Zr in a low-Mg, low-Cu base [W11-05, W11-07].
     - Mechanism: coherent Al₃Zr dispersoids pin (sub)grain boundaries during the cure without adding much
       solute hardening to the slug *(general knowledge)*.
     - Costs: the slug anneal must still fully recrystallise, so the same pinning that protects the wall also
       raises the slug-anneal temperature or the cold reduction needed *(inference)*. Zr also tends to poison
       Ti–B grain refiners *(general knowledge, verify)*.
   - (c) **Mn dispersoid/solute route** (3102/3207 class): the lean Al–Mn path that the in-house work follows.
     It is the "middle" option: it sits between 1xxx and the Zr alloys in RX resistance *(inference)*.
3. **Lightweighting payoff.** For a thin cylinder, hoop stress is σ = p·D/(2t) *(general knowledge)*. So at a
   fixed pressure requirement, wall thickness scales as 1/σ_allowable. A 10 % gain in post-bake strength allows
   roughly 9 % less wall *(derived)*. This is consistent in magnitude with the published > 10 % burst gains and
   about 11–20 % weight savings (§5) [W11-06, W11-18, W11-21].
4. **Scrap acceptance.** If the 1070-plus-3104-scrap route is adopted, the composition limits are set by the
   scrap mix. Claim ranges (Table 1.1) show the industry tolerates Mg up to about 0.7 % and Zn up to about 0.25 %
   in such blends [W11-01]. The trade-off is MgO, slug hardness, and corrosion/lacquer compatibility; the last
   was not covered by any source captured.

### 1.3 Relevance to in-house work

- **Chapter 09 §1 (Modified 3102)** raises Mn and Mg for strength. The patents in §1.1 show that the
  industrial goal of such modifications is **back-anneal resistance during the lacquer cure**, not slug
  strength. The Zr routes (W11-05, W11-07) are an alternative that adds less Mg, and therefore less MgO; see
  ch09 §3.
- **Chapter 09 §10 (consolidated compositions) and §11 Q1–Q3:**
  - The Ball claim ranges give an external benchmark for how much Mg, Cu and Zn pick-up a commercial recycled
    slug alloy carries.
  - The Talum claim shows the opposite philosophy: ultra-low Mg, Cu and Zn, with Zr.
  - Answering ch09 §11 Q1 (targets for wall UTS, burst pressure and bake softening) is the prerequisite for
    choosing between these routes.
- **Chapter 10** covers why harder slugs raise extrusion load (mechanics). This chapter only records that
  industry cites punching tonnage as a cost of stronger alloys [W11-03].

---

## 2. Slug specifications: hardness, grain, geometry, surface, annealing, lubrication, defects

### 2.1 Findings

- **Standard framework: EN 570:2007.** It specifies inspection and delivery conditions, dimensional and form
  tolerances, chemical composition, mechanical properties and the Brinell hardness test (EN ISO 6506-1) for
  **flat or preformed** slugs. The slugs are produced **by punching rolled products or by cutting extruded
  products** [W11-11] (snippet only).
  - Slugs are supplied in **O temper**, and approximate Brinell values are given per alloy "for guidance"
    [W11-11] (snippet only).
  - One third-party page says EN 570 covers 21 alloys [W11-11] (snippet only).
  - The 2007 edition replaces EN 570:1994 [W11-11] (snippet only).
  - **The per-alloy HB table was not obtained.**
- **Published slug hardness data points:**
  - In Ball's Table 5, a **1050 reference slug measured 21.5 HB**. Two "ReAl 3104 25 %" materials measured
    **29 HB** (Material 1: re-melt secondary ingot from briquetted cupper scrap, *shot-blasted* finish) and
    **30.7 HB** (Material 2, *tumbled* finish). That is about 35 % and 43 % harder than 1050 [W11-01, W11-03]
    (snippet only; same table appears in the US, EP and WO members).
  - W11-02 contains HB before and after annealing for four 1070 + 3104 blends; the values were not captured.
  - Supplier pages give, for pure-Al slugs: **23 HB** (a 1050 slug example), **17–19 HB after a 520 °C / 4 h
    anneal**, and **16–21 HB** for annealed slugs. For comparison, 6063 slugs are **60–70 HB** [W11-29]
    (marketing, snippet only; exact page per value not pinned down).
- **Annealing practice published by industry:**
  - Ball batch anneal of punched slugs: target furnace temperature **about 470–600 °C for about 5–9 h**, to
    recrystallise into a "homogeneous, equiaxed grain structure" [W11-01] (snippet only).
  - Ball **continuous annealing** is "the preferred process for producing ReAl slugs". Slugs ride a **metal
    mesh belt through a multi-zone furnace** at a **peak metal temperature of about 450–570 °C**. Two stated
    benefits:
    - (1) shorter time at temperature means **less surface oxide**;
    - (2) grains are "equiaxed and uniform size" [W11-01–W11-03] (snippet only).
  - Ball gives the recrystallisation/recovery temperature for ReAl material as about **350–550 °C**
    [W11-01–W11-03] (snippet only).
  - Tube-slug patent example: **about 500–520 °C for about 2–3 h, then cooling at < 0.05 K/s**, for slugs
    containing 1070A tube scrap [W11-08] (snippet only; attribution by search ranking).
  - Generic patent statement: slugs are softened at about **300–600 °C**, with time set by the extrusion work
    required [W11-09] (snippet only).
  - Supplier example: **520 °C / 4 h** for pure-Al slugs [W11-29] (marketing, snippet only).
- **Surface oxide.** Ball's patents single out **magnesium oxide**, "a major concern due to its extreme
  abrasive nature". Increased MgO on punched slugs "may cause excessive scratching during the impact extrusion
  process. On extended runs these scratches are an unacceptable quality defect." Shorter anneal time reduces it
  [W11-01–W11-03] (snippet only).
- **Surface finish.** Both **shot-blasted** and **tumbled** finishes appear in Ball's examples [W11-01]
  (snippet only). Sources were not captured for a smooth/as-punched finish or for the finish's effect on
  lubricant pick-up.
- **Geometry.**
  - EN 570 covers flat and preformed slugs [W11-11] (snippet only).
  - One supplier offers 3003 slugs at **1.5–30 mm thick and 3–240 mm diameter** [W11-29] (marketing, snippet
    only).
  - Some tube slugs are supplied **with a central hole** (supplier product title) [W11-29] (snippet only).
  - Rectangular slugs and dimple geometries were not covered by captured sources.
- **Collapsible tubes** are also annealed *after* extrusion. An academic control paper describes an AA1050 tube
  oven at **350–450 °C** [W11-34] (snippet only). (This is a post-forming soft anneal, unlike aerosol cans,
  which must keep their work hardening *(general knowledge)*.)
- **Not verified (no captured source):**
  - zinc-stearate (or other) lubricant type and coating weight;
  - grain-size acceptance limits;
  - specific defect catalogues (orange peel, splits, pick-up/galling, laminations, blisters) and their causes.
  See §6.

**Table 2.1 — Slug hardness data points found**

| Material | Condition / finish | HB | Source | Evidence |
|---|---|---|---|---|
| 1050 (reference) | annealed slug | 21.5 | W11-01/W11-03 Table 5 | snippet only |
| ReAl 3104 25 % – Material 1 (RSI from cupper scrap) | annealed, shot-blasted | 29 | W11-01/W11-03 | snippet only |
| ReAl 3104 25 % – Material 2 | annealed, tumbled | 30.7 | W11-01/W11-03 | snippet only |
| 1050 slug (supplier example) | "moderate hardness" | 23 | W11-29 | marketing, snippet only |
| pure-Al slug | after 520 °C / 4 h | 17–19 | W11-29 | marketing, snippet only |
| pure-Al slug | annealed | 16–21 | W11-29 | marketing, snippet only |
| 6063 slug | not stated | 60–70 | W11-29 | marketing, snippet only |

**Table 2.2 — Published slug annealing practice**

| Practice | Temperature | Time | Cooling | Stated purpose / note | Source |
|---|---|---|---|---|---|
| Batch, ReAl punched slugs (Ball) | ≈ 470–600 °C furnace target | ≈ 5–9 h | n/c | RX to homogeneous equiaxed grain | W11-01 |
| Continuous, mesh-belt multi-zone (Ball, preferred for ReAl) | PMT ≈ 450–570 °C | short (n/c) | n/c | Less oxide (MgO); uniform equiaxed grain | W11-01–03 |
| ReAl RX / recovery range | ≈ 350–550 °C | — | — | Material property statement | W11-01–03 |
| Tube slugs with 1070A recycled content | ≈ 500–520 °C | ≈ 2–3 h | < 0.05 K/s | Patent example | W11-08 |
| Generic slug softening | ≈ 300–600 °C | per extrusion work | — | Patent background | W11-09 |
| Pure-Al slug (supplier) | 520 °C | 4 h | n/c | Gives 17–19 HB | W11-29 (marketing) |

All rows are snippet only. n/c = not captured.

### 2.2 Design levers

- **Hardness window comes from the customer and EN 570.** The only public comparative HB numbers show that a
  25 % 3104 dilution adds about 8–9 HB over a 1050 reference [W11-01]. Hardness should be specified together
  with its consequence for extrusion load (ch10) and for wall strength after bake (§4).
- **Anneal temperature and time drive oxide.** Industry anneals are hot: hundreds of °C above the RX start,
  for hours in batch [W11-01, W11-08]. Ball's response to the MgO problem was **continuous annealing**
  (minutes-scale, mesh belt) rather than lowering the temperature [W11-01–03].
  - *Inference:* for Mg-bearing slugs, time at temperature is the main oxide lever. Mg diffusion to the surface
    and selective oxidation scale with √t at a given temperature *(general knowledge)*.
  - Cold reduction (which lowers the needed RX temperature) and atmosphere are additional levers that the
    sources did not address.
- **Slow cooling after a high-temperature anneal** (< 0.05 K/s, W11-08) is consistent with precipitating Mn and
  Fe out of solid solution to minimise slug hardness and resistivity *(inference / general knowledge; the
  patent's stated reason was not captured)*.
- **Finish.** Shot-blasting and tumbling are both industrial. The 29 vs 30.7 HB difference in W11-01 confounds
  finish with feedstock, so no finish effect on HB can be inferred *(inference)*.

### 2.3 Relevance to in-house work

- **Chapter 09 §3 (MgO dashboard) and §11 Q8 ("why is MgO minimised?").** W11-01–03 give one documented
  industrial reason: **abrasive MgO scratches the extrusion tooling and parts on long runs**. They also confirm
  continuous annealing as the industrial countermeasure.
- **Chapter 09 §2–§5 (RX models, CRM tables):**
  - The published industrial anneal temperatures (Table 2.2) are markedly **hotter** than the windows in
    ch09 §5. The batch times (5–9 h) are of the same order as the long soaks that the in-house JMAK models
    predict (ch09 §11 Q7).
  - This should be reconciled. Higher-temperature anneals give faster RX but more oxide and grain-growth risk
    in 1xxx; continuous annealing decouples temperature from time.
- **Chapter 09 §8 (slug specification documents)** contains no hardness, grain, surface or temper
  requirements. **EN 570:2007** is the natural framework to adopt (O temper, HB per EN ISO 6506-1, tolerances).
  Its tables should be purchased and checked (see §6).

---

## 3. Slug production routes and producers

### 3.1 Findings

- **Two standard routes** [W11-11] (snippet only):
  - punching slugs from **rolled** strip;
  - **cutting** (sawing) slugs from **extruded** bar.
- **Continuous casting dominates the published rolled-slug routes:**
  - **Casting wheel, then hot rolling, quench and cold rolling.** Aluman S.A. (Greece) describes this line for
    slugs for monobloc aerosol cans and collapsible tubes [W11-25] (snippet only). A patent describes the
    sequence: alloy melted, "continuously cast, in liquid form, on a casting wheel", rolled, strip "cut on a
    cutting press to form slugs or disks", then annealed [W11-10] (snippet only; attribution by ranking).
  - **Rotary strip caster with narrow strip.** Turk et al. (2016) produced new aerosol-slug alloys from narrow
    strips cast on a rotary strip caster [W11-06] (snippet only).
  - **Twin-belt (Hazelett) casting, then hot and cold rolling** (Ball patents):
    - Molten metal solidifies between two flexible steel belts, with chain-mounted dam blocks forming the
      sides.
    - High-pressure water on the belt backs controls heat extraction and keeps the belts against the
      shrinking slab.
    - The process is "commonly used for architectural strip, and may be used for impact extrusion slugs".
    - Slab exit temperature is kept **above about 520 °C and below about 582 °C**, followed by rolling from
      **about 28–35 mm to 3–14 mm** [W11-01–03] (snippet only).
    - The patents contrast this with **wheel-belt casters**, whose thick belt "cannot deflect to keep contact
      with the shrinking slab". They say this is worse for recycled alloys with **wider solidification ranges**
      [W11-01–03] (snippet only).
    - Hazelett markets twin-belt strip for slugs, attributing surface quality to belt heat-transfer control
      [W11-24] (marketing, snippet only).
  - **Generic Chinese supplier line:** continuous strip casting, hot and cold rolling, automatic punching
    presses, annealing ovens [W11-29] (marketing, snippet only). One supplier starts from AA1070 (99.7 %) ingot
    [W11-29] (snippet only).
- **Producers named in captured sources** (technical content only):
  - **Neuman Aluminium** (Austria): slug supplier to Tubex; co-developed the "Neucan 3.1" patented slug; impact
    extrusion on knuckle-joint presses [W11-21–W11-23] (snippet only).
  - **TALUM d.d.** (Kidričevo, Slovenia): applicant of the Al–Fe–Mn–Zr aerosol alloy patent [W11-05]. The
    rotary-strip-caster study W11-06 is on the same topic; the authors' affiliation was not captured.
  - **Aluman S.A.** (Greece): wheel-cast slug line [W11-25].
  - **Aluminium Rheinfelden / Rheinfelden Semis** (Germany): slugs, aerosol cans and tube; 31,000 t/y semis
    capacity [W11-26]. In 2014 it announced a CCL–Rheinfelden Semis slug JV in Clinton, North Carolina (about
    US$18 M; 25,000 t planned by 2018) [W11-27] (snippet only; whether the plan was met is not verified).
  - **Ball Corporation**: makes its own ReAl slugs (continuous anneal) and markets "technical punch slugs"
    [W11-01, W11-28].
  - **Moravia Cans** (Czech Republic): can maker holding a 3207 + Zr alloy patent [W11-07].
  - Chinese slug suppliers (Chalco and others) [W11-29] (marketing).

### 3.2 Design levers

- **Caster choice for recycled feed.** For wide-freezing-range recycled blends, a caster that keeps mould
  contact through shrinkage (twin-belt) is presented as superior to a rigid wheel-belt [W11-01–03].
  - *Inference:* better contact gives more uniform heat extraction, finer and more uniform as-cast structure,
    fewer surface segregates, and fewer laminations and blisters.
  - The defect link is general knowledge and was **not** verified in any captured source.
- **Thin-strip casting keeps Mn, Zr and Fe supersaturated** *(general knowledge)*. For Zr/Mn alloys (W11-05,
  W11-06) the dispersoid population is therefore set *in the rolling and slug-anneal path*, not by a DC
  homogenisation. This puts the slug anneal (heating rate, temperature, time) in control of both slug RX and the
  later back-anneal resistance *(inference)*.
- **Slab exit temperature and hot reduction.** Ball's 520–582 °C exit window and 28–35 → 3–14 mm rolling
  [W11-01–03] are the only published numbers for a belt-cast slug route.

### 3.3 Relevance to in-house work

- **Chapter 09 §5** assumes a 22 mm starting strip through HRM, then CRM, then full anneal. Chapter 09 §11 Q9
  asks whether this strip is continuously cast and on which caster.
  - The published belt-cast route starts at 28–35 mm, and the wheel- and rotary-cast routes start at thinner
    gauges.
  - Knowing the caster type decides whether the twin-belt vs wheel-belt arguments above apply.
  - It also decides whether Mn (and any Zr) enter the anneal largely in solid solution. That is the heating-rate
    sensitivity flagged in ch09 §5 and §9.

---

## 4. Can performance requirements

### 4.1 Findings: legal pressure requirements

- **EU, Council Directive 75/324/EEC as amended** [W11-12, W11-13] (snippet only):
  - *Test pressure*: the pressure an **unfilled** container withstands **for 25 s** without leakage or, for
    metal and plastic containers, "any visible or permanent distortion except as allowed under 6.1.1.2". The
    text of 6.1.1.2 was not captured.
  - *Bursting pressure*: the minimum pressure that causes the container to burst or rupture.
  - **Test pressure rule:**
    - containers filled at < 6.7 bar at 50 °C: test pressure ≥ **10 bar**;
    - containers at ≥ 6.7 bar: test pressure **50 % higher than the internal pressure at 50 °C**.
  - Some extracts print the threshold as "6 77"; this is an OCR artefact.
  - **Bursting pressure must be at least 20 % higher than the test pressure** [W11-12; restated by an industry
    explainer, W11-36] (snippet only).
  - **Maximum pressure at 50 °C:**
    - 12 bar for all gases (2008/47/EC);
    - since **(EU) 2016/2037**: **12 bar** for flammable liquefied gas, **13.2 bar** for non-flammable liquefied
      gas, and **15 bar** for non-flammable **compressed or dissolved** gas (N₂, compressed air, CO₂)
      [W11-13] (snippet only).
  - A commercial guide claims a "1.5 × burst" rule [W11-35]. That conflicts with the legal text and should not
    be used.
- **USA, 49 CFR 173.306** [W11-14] (snippet only):
  - Pressure tiers at 130 °F (54.4 °C): ≤ 140 psig allows non-DOT, 2P, 2Q or 2Q1; 140–160 psig allows 2P, 2Q
    or 2Q1; 160–180 psig allows 2Q or 2Q1. The maximum is 180 psig.
  - The container must not burst at ≥ **1.5 ×** the equilibrium pressure at 130 °F.
  - Secondary patent text describes 2P as no distortion < 160 psig and no burst < 240 psig, and 2Q as < 180 and
    < 270 psig [W11-16] (snippet only; verify against 49 CFR 178.33/178.33a).
- **Dome (base) behaviour.** A US patent designs a metallic dome that "rolls outward" at about **225–230 psig**,
  below a controlled venting pressure of about **240–280 psig**, to meet the DOT **2P1 bottom specification**
  [W11-15] (snippet only).
  - *Inference:* the base dome is the designed deformation (reversal) element. Dome thickness and the slug's
    base material govern the deformation pressure, while the wall governs burst.
- **Historical UK standard.** BS 3914-1:1974 covered non-returnable metal aerosol containers up to 1400 cm³ and
  85 mm diameter, including deformation and test pressure. It was withdrawn in 1991 [W11-37] (snippet only).
- **FEA / AEROBAL technical standards:** none was captured (see §6). Patents state that burst and buckle
  requirements are set by DOT in the USA and by the European Aerosol Federation in Europe [patent text in the W11-02
  result set] (snippet only; exact document not identified).

**Table 4.1 — EU minimum test and burst pressures implied by 75/324/EEC as amended (derived from W11-12/W11-13)**

| Max. pressure at 50 °C (P₅₀) | Typical propellant category (2016/2037) | Min. test pressure = max(10 bar, 1.5 × P₅₀) *(derived)* | Min. burst = 1.2 × test *(derived)* |
|---|---|---|---|
| < 6.7 bar | any | 10 bar | 12 bar |
| 12 bar | flammable liquefied gas | 18 bar | 21.6 bar |
| 13.2 bar | non-flammable liquefied gas | 19.8 bar | 23.8 bar |
| 15 bar | non-flammable compressed / dissolved gas (N₂, air, CO₂) | 22.5 bar | 27.0 bar |

Notes on Table 4.1:
- The rules come from the consolidated text seen as snippets. Verify against EUR-Lex.
- The industry habit of quoting can "classes" such as **12 / 15 / 18 bar deformation** with burst about 20 %
  higher fits these numbers. For example, an 18 bar test pressure corresponds to a 12 bar product. **However, no
  source defining such classes (FEA or manufacturer datasheet) was captured.**

**Table 4.2 — US DOT tiers (W11-14; bar values derived, 1 psi = 0.06895 bar)**

| Container | Max. product pressure at 130 °F | ≈ bar | Min. no-burst (1.5 ×) | ≈ bar | Patent description of spec (W11-16) |
|---|---|---|---|---|---|
| non-DOT | ≤ 140 psig | 9.65 | 210 psig | 14.5 | — |
| DOT 2P | ≤ 160 psig | 11.0 | 240 psig | 16.5 | no distortion < 160 psig; no burst < 240 psig |
| DOT 2Q / 2Q1 | ≤ 180 psig | 12.4 | 270 psig | 18.6 | no distortion < 180 psig; no burst < 270 psig |

### 4.2 Findings: lacquer curing and softening

- Aerosol cans carry internal liners. Offered types include **polyamide-imide (PAM)**, **epoxy-phenolic (EP)**
  and beverage-compatible liners [W11-33] (marketing, snippet only).
  - A monobloc-coating patent reports that EP control cans softened after 12–24 h in chloroform, while a PAM
    control did not soften after 3 days [W11-32] (snippet only). That is the chemical-resistance reason for
    PAM.
  - **No PAM cure schedule was captured.**
- **Cure schedules found:**
  - Epoxy-phenolic **food-can** lacquers cure industrially at **200 °C for 12 min**; a study range of 170–220 °C
    and 12–36 min was investigated [W11-30] (peer-reviewed, food cans, snippet only).
  - A tube supplier quotes internal spray baked at, for example, **250 °C for 5 min** [W11-31] (marketing,
    snippet only).
- **Metallurgical consequence:**
  - Can manufacture lowers mechanical properties by **up to 15 %**, reducing deformation and burst pressure
    [W11-06] (snippet only). (Inference: this is mainly bake softening of the extruded wall.)
  - Ball, Talum and Moravia all designed alloys for **back-annealing resistance / RX-threshold shift** so that
    higher-cure linings can be used and the properties are kept [W11-01, W11-02, W11-05, W11-07] (snippet only).
  - Older Al–Mg–Si proposals lose strength in the lacquer step (§1.1).
- **No captured source gives quantitative bake-softening curves** (strength vs cure T/t) comparing 1xxx with
  3xxx.

**Table 4.3 — Lacquer-cure conditions found (none specific to aerosol monobloc cans)**

| Coating / product | Temperature | Time | Source | Evidence |
|---|---|---|---|---|
| Epoxy-phenolic, food cans (industrial) | 200 °C | 12 min | W11-30 | peer-reviewed, snippet only |
| Epoxy-phenolic, food cans (study range) | 170–220 °C | 12–36 min | W11-30 | peer-reviewed, snippet only |
| Internal lacquer, aluminium tubes (example) | 250 °C | 5 min | W11-31 | marketing, snippet only |
| PAM, aerosol monobloc | not captured | — | — | — |

### 4.3 Design levers

- **Specify post-bake wall and dome properties** (UTS/YS after the customer's actual cure cycle) as the alloy
  design target. A loss of up to 15 % [W11-06] is larger than many composition-driven strength gains, so cure
  stability is a primary lever *(inference)*.
- **Back-anneal resistance mechanisms**, in order of thermal robustness *(general knowledge)*:
  - Zr (Al₃Zr) dispersoids are the most stable;
  - then Mn-bearing dispersoids;
  - then solute drag from Mg, Cu and Mn in solid solution;
  - pure 1xxx, whose recovery and RX are controlled only by Fe/Si and trace solutes, is the least stable.
  
  The extruded wall is heavily strained (ch10), so its RX temperature is low. The cure (about 200–250 °C) is
  where 1xxx loses the most *(inference; the 1xxx vs 3xxx bake response was not quantified in any captured
  source)*.
- **Pressure class drives gauge.** Moving a product from a 12 bar to a 15 bar (non-flammable compressed gas)
  category raises the minimum test pressure from 18 to 22.5 bar (Table 4.1, derived), i.e. +25 %. That is the
  same order as the strength gains claimed for the newer alloys (§5). Compressed-gas (N₂, air) formulations are
  therefore a market pull for higher-strength, bake-stable slug alloys *(inference)*.
- **Base vs wall.** Deformation (dome rollout) and burst are different failure modes [W11-15]. The slug's base
  zone sees much less extrusion strain than the wall (ch10), so base strength depends more on alloy and slug
  temper than on work hardening *(inference)*.

### 4.4 Relevance to in-house work

- **Chapter 09 §11 Q1** asks for burst-pressure, wall-UTS and lacquer-bake-softening targets. Tables 4.1–4.2
  give the legal floor that those targets must sit above. The customer's cure schedule and pressure category
  are needed to close the loop.
- **Chapter 09 §4.8 / §6** (hardness vs time; temper tables) model **slug** softening during annealing. No
  in-house model covers **wall** softening during the lacquer cure. That gap matters most for the "Modified
  3102" decision (ch09 §1, §9 item 5).

---

## 5. Lightweighting trends and published case studies

### 5.1 Findings

**Table 5.1 — Published lightweighting numbers (most are manufacturer claims)**

| Case | Year | Recycled content | Weight saving | Other claims | Source | Type |
|---|---|---|---|---|---|---|
| Ball ReAl launch (replacing standard Al aerosol can) | 2014 | 25 % | 11 % | — | W11-18 | marketing |
| Ball ReAl next iteration (Henkel Fa 150/200 ml) | c. 2015 | "comparable" | 15 % vs standard can | ≈ 12 % carbon-footprint cut; "lightest commercially available" at the time | W11-18, W11-19 | marketing / trade press |
| Ball ReAl product page | current | n/c | ≈ 15 % | "higher strength" | W11-17 | marketing |
| Unilever Rexona / Sure (Ball) | 2017 | n/c | ≈ 20 % | 18 % carbon-footprint cut (150 ml) | W11-19 | trade press |
| Ball re:generation | 2022 | up to 50 % + low-carbon primary | weight claim not reliably captured | — | W11-20 | trade press |
| Tubex + Neuman "Neucan 3.1" slug | 2018 (dev.) | up to 60 % PCR (company claim) | "close to 20 %" vs standard Al 99.5 can; "up to 20 % less weight with the same stability" | Wall thickness and shoulder reworked; more dent-prone in transit (extra packaging) | W11-21, W11-22 | trade press / marketing |
| Tubex Rexona deodorant can | c. 2022 | 25 % real PCR, patented alloy | 14 % vs predecessor | — | W11-22 | marketing |
| Ball patents, general | 2011– | 10–60 % 3xxx in 1070 | sidewall or bottom thickness reduced by ≈ 5–40 % | slug HB +35 % / +43 % vs 1050 | W11-01–03 | patent |
| Talum Al–Fe–Mn–Zr alloy | 2016 | — | — | burst pressure ≈ 5 bar higher | W11-05 | patent |
| Turk et al. new alloys | 2016 | — | — | deformation and burst pressure > 10 % higher; constant properties through manufacture | W11-06 | peer-reviewed |

All rows are snippet only. "Standard can" is not defined consistently between sources, so savings are not
directly comparable.

- **Trend 1: alloy-enabled lightweighting.** Every published lightweighting case pairs a **stronger, more
  bake-stable alloy than 1070/1050** with geometry changes (wall, shoulder) [W11-01–03, W11-05, W11-06, W11-21]
  (snippet only).
- **Trend 2: recycled content is coupled to the alloy.** Recycled content has risen from 25 % (2014) to "up to"
  50–60 % (2022–23) [W11-18, W11-20, W11-22] (marketing, snippet only). Two philosophies exist:
  - accept 3xxx scrap chemistry (Ball);
  - use "high-purity" PCR, such as tube scrap or sorted streams (Tubex/Neuman "real PCR", W11-08 tube-scrap
    slugs).
- **Side effect:** thinner walls make cans **more dent-prone in transit**, so packaging had to change [W11-21]
  (snippet only).

### 5.2 Design levers

- **Benchmark target** *(inference from Table 5.1)*: to be competitive, a new lean 3xxx slug alloy needs to
  support about **15–20 % can-weight reduction** relative to a 1070/1050 can. With the hoop-stress scaling of
  §1.2 this requires roughly **15–25 % higher post-bake wall strength** *(derived, assuming weight ∝ wall
  thickness, which overstates the saving because the base and shoulder do not scale)*.
- **Dent resistance** depends on yield strength × thickness² *(general knowledge)*. A thinner wall needs a
  disproportionate gain in yield strength to keep dent and handling resistance, so YS after bake is as important
  as UTS *(inference)*.
- **Recycled-content claims** require either scrap-tolerant chemistry (Mg/Cu/Zn windows as in W11-01) or access
  to clean, sorted PCR. This ties the alloy specification to scrap sourcing *(inference)*.

### 5.3 Relevance to in-house work

- **Chapter 09 §8:** the in-house slug sizes and wall values can be benchmarked against the 11–20 % savings
  claimed for ReAl and Neucan once the reference "standard can" wall is defined (ch09 §11 Q11).
- **Chapter 09 §7 (CBAM)** and §11 Q10: the carbon-footprint claims in Table 5.1 (−12 %, −18 %, "half")
  combine lighter weight with recycled or low-carbon metal. A lean-3xxx, high-scrap slug alloy contributes on
  both fronts.

---

## 6. Open questions / what could not be verified

**Access-related.** Every item in this chapter is snippet-level. Fetching the following primary documents would
upgrade the evidence:

1. US 10,584,402 B2 and US 11,519,057 B2 full text (Ball): Table 6 buckle and burst pressures for 1070 + 3104
   blends; HB before and after anneal; tensile and yield vs 1070; Figs 6–8; exact continuous-anneal cycle;
   Hazelett process description. Also confirm which family member each statement comes from.
2. EP 3075875 A1 (Talum): full examples, anneal and homogenisation route, burst data, polymerisation cycle.
   One snippet called the alloy "Al-Mg-Si", which contradicts the claimed Mg < 0.01 %; check.
3. Turk et al. 2016 (doi:10.17222/mit.2015.330): alloy compositions, caster parameters, slug HB, cure cycle,
   deformation and burst data, authors' affiliation.
4. EP 3031941 B1 / EP 2881477 B1 (Moravia Cans): Zr and other ranges for the "heat resistant" 3207.
5. **EN 570:2007** tables: alloy list, approximate HB per alloy, tolerances, surface requirements. These need
   purchasing from CEN, BSI or DIN.
6. 75/324/EEC Annex §6.1.1.2: permitted distortion. Also confirm the "bursting ≥ 20 % above test pressure"
   wording in the current consolidated text.
7. Tubex datasheet 07/2022 (W11-22): alloy, wall thickness, deformation and burst classes per can size.

**Not found in any captured source:**

8. FEA / AEROBAL technical standards for aluminium monobloc cans: dimensions; deformation and burst test
   methods; the commonly quoted 12 / 15 / 18 bar classes and whether burst = 1.2 × deformation in practice.
9. Grain-size acceptance limits for slugs and their link to orange peel on the can wall.
10. Lubricant: zinc stearate vs alternatives, coating weight, interaction with surface oxide and finish.
11. Defect catalogue with metallurgical causes: splits, pick-up/galling, laminations, blisters, orange peel,
    pinholes, discolouration. Only MgO-related scratching is documented [W11-01–03].
12. Maximum Fe, Si, Cu and Zn pick-up limits for recycled slug alloys, and their effect on extrudability and
    corrosion and lacquer compatibility. Only claim ranges were found (Table 1.1).
13. PAM liner cure schedules for aerosol monobloc cans, and quantitative bake-softening curves for 1xxx vs
    3xxx can walls.
14. Necking and shaping formability requirements: shoulder forming, contour shaping, and the effect of slug
    alloy on necking splits.
15. Competing **coil-fed** aluminium aerosol routes appeared only as patent titles and were not examined:
    - EP 2119515 A2, *Method for manufacturing an aluminium aerosol can from coil feedstock*;
    - US 9,789,992, *Drawn and ironed aerosol can*;
    - US 10,577,683 / EP 2997171 B1, *Aluminium alloy sheet for metallic bottle or aerosol container*.
    
    They are relevant as a competitive benchmark to slug-based cans.
16. The plastic-aerosol patent figure of steel and Al cans deforming at about 8 bar and bursting at about 10 bar
    (search result, US 8,960,503 / 9,969,543) was **not used**. It is below the directive's 10 bar minimum test
    pressure and looks unreliable or outdated.
