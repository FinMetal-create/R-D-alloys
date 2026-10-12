# 01 — Solidification and DC casting of wrought Al alloys (physical-metallurgy knowledge base)

**Scope.** This file distils the physical metallurgy of direct-chill (DC) casting into data we can use for alloy design and process modelling. The chain covered is: composition → solidification path → as-cast structure (grain size, DAS, intermetallics, eutectic) → segregation and casting defects (macrosegregation, hot tearing, porosity, surface defects) → what this means for homogenisation. The main targets are wrought 3xxx heat-exchanger and foil alloys (AA3102/AA3207 type), with 1xxx, 5xxx, 6xxx and 8xxx as secondary targets. The source works mostly with Al–Cu model alloys, 2024 and 7075, so any transfer to our alloys is labelled **Inference**.

**Compiled:** 2026-10-12. **Single source:** D.G. Eskin, *Physical Metallurgy of Direct Chill Casting of Aluminum Alloys*, CRC Press / Taylor & Francis, 2008 (ISBN 978-1-4200-6281-6), supplied as chapter PDFs.

## Sources

| Ref | File | Content (printed book pages) | Drive link | What was readable |
|---|---|---|---|---|
| fm | 62816_fm.pdf | Title, TOC, list of symbols, preface (pp. i–xix) | https://drive.google.com/file/d/15ShzCo5bBJyg0SE7AD50Sst9z_F0v91Z/view | Full text. The TOC lists *Concluding Remarks* (p. 275), and internal links point to `62816_CH06.pdf`. **That file is not in the Drive folder**, so it was not read. |
| ch1 | 62816_ch01.pdf | Ch. 1, DC casting: development of the technology (pp. 1–18) | https://drive.google.com/file/d/1T5sCpnxZxg9BFtPmyRqH7zqZjKy0UczL/view | Full text. Figures survive only as stray axis labels. |
| ch2 | 62816_ch02.pdf | Ch. 2, Solidification of Al alloys: cooling rate, microsegregation, phase selection, grain refinement (pp. 19–78) | https://drive.google.com/file/d/1MBeZaNbetcIq6Xjcoj2Y56AW9wZPwcb2/view | Full text (~139 k chars, read 100%). Sub- and superscripts are flattened. Several tables (2.2, 2.4–2.9) and some two-column passages are scrambled; values were reconstructed only where unambiguous, and partial reconstructions are flagged "(garbled)". Figures are not readable. |
| ch3 | 62816_ch03.pdf | Ch. 3, Sump geometry, solidification and cooling rates, structure vs process parameters, casting defects (pp. 79–124) | https://drive.google.com/file/d/1t1R4f3IKhRkid18JooQCMoR5PNhbjsZE/view | Full text (~105 k chars, 100%). Same caveats as ch2. |
| ch4 | 62816_ch04.pdf | Ch. 4, Macrosegregation (pp. 125–182) | https://drive.google.com/file/d/1LGAwTkLvuT29WFaaXDgYcKRN31PhMQ7v/view | Full text (~126 k chars, 100%). Eqs. 4.8–4.10 and 4.18–4.19 are garbled and only partly reproduced. |
| ch5 | 62816_ch05.pdf | Ch. 5, Hot tearing: thermal contraction, semi-solid properties, criteria, process effects (pp. 183–274) | https://drive.google.com/file/d/1tYAv85fpfmJ7f5wNBPi3kvky3b1H4ps4/view | Full text (~229 k chars, 100%). Cleanest of the extractions, with page markers. Fraction bars are linearised and a few exponents may be lost (flagged). |

**Not used.** (i) A second Drive folder (`19BnEdTwK87C8DAtx7SAsdcg-Ebc0w92M`) holds copies of the same six PDFs, with identical names and byte sizes; they were not re-read. (ii) "Download Free Ebooks & much more.URL" in the source folder is a web shortcut, not a source. (iii) The book has no index or back matter in Drive.

**Conventions.**
- `[chN, p.X]` cites the printed book page. Equation numbers are the book's.
- "(general knowledge)" marks a statement that is not in the source.
- "**Inference:**" marks my own reasoning that links source facts to our alloys. It is not a source claim.
- "(derived)" marks arithmetic on source numbers.
- The source does **not** mention AA3102, AA3207, foil gauges, or twin-roll / continuous casting and rolling.

---

## 0. Vocabulary: zones of a DC billet and feeding stages

- **Molten pool:** above the liquidus. **Transition region:** liquidus → solidus. **Sump:** pool + transition region. **Slurry zone:** liquidus → coherency isotherm (grains float freely). **Mushy zone:** coherency → solidus. In the simulations the coherency isotherm is drawn at 30% solid [ch3, p.79–80].
- **Coherency:** solid grains begin to interact. It is reached at fs = 0.25–0.6 depending on grain morphology [ch5, p.183].
  **Rigidity:** a continuous solid skeleton forms. Below it the mush transmits stress and shows linear contraction [ch5, p.185].
- The book warns that calling the whole transition region the "mushy zone" is misleading [ch5, p.183].
- **Four feeding stages** [ch5, p.184]:
  1. Mass feeding.
  2. Interdendritic feeding: a pressure drop develops, but pores do not yet form.
  3. Interdendritic separation: pores and hot tears are possible.
  4. Interdendritic bridging / solid feeding (fs > 0.9): only creep accommodates further strain.
- In an Al–1%Cu model, grain clusters form at fs ≈ 0.97 and large clusters with isolated films at fs ≈ 0.99. Above 0.97, feeding localises and permeability falls faster than Kozeny–Carman predicts [ch5, p.184].
- **Grain refinement (GR) delays coherency and rigidity.** Coherency fs in Al–4%Cu goes from 0.23 to 0.45 with 0.05% Ti. Rigidity fs in 2024 goes from 0.75 to 0.82 [ch4, p.172].

---

## 1. Heat extraction, sump geometry, solidification and cooling rates

### 1.1 Mechanisms
- **Why DC works.** Heat leaves mainly through the solid shell via the direct water chill. This gives a shallow sump, a flat front, high solidification rate and a fine, uniform structure [ch1, p.8–9].
  - Compared with Junghans mould casting at the same speed and diameter, the sump is about 4× shallower. At equal sump depth, DC can therefore cast about 4× faster, with about 4× the solidification rate [ch1, p.13].
- **Cooling zones down the billet** [ch3, p.94–96]:
  - **Primary (mould):** this is where the shell forms.
  - **Air gap:** the shell shrinks away from the mould. The HTC drops from 1–2.5 to about 0.5 kW/m²K, and the shell reheats and may remelt (risk of bleed-out and liquation).
  - **Water impingement (secondary):** the HTC rises by 1–2 orders of magnitude, e.g. 48 kW/m²K.
  - **Downstream free-falling water:** 30–40 kW/m²K.
- **Boiling regime.**
  - Nucleate boiling gives an HTC of about 40 kW/m²K and heat flux up to 6000 kW/m² [ch3, p.86–87].
  - It is maintained in steady state because the surface stays below 300°C. There, water flow rate has negligible effect.
  - At start-up the water flow is reduced to limit stresses. Film boiling can then occur, and water flow does matter [ch3, p.87].
- **Solidification rate along the front.** It is maximum at the centre and the periphery, where the front is flat, and minimum around mid-radius, where it is steepest. Casting speed mainly affects the centre and periphery [ch3, p.91–92].
- **Cooling curve at the billet centre** [ch3, p.96–97]:
  - First a near-isothermal plateau in the slurry. Latent heat causes it: more than 50% of the solid forms within a few degrees below the liquidus.
  - Then faster cooling in the lower mushy zone. The centre can cool faster than mid-radius in the mush.
- **Thermocouple cooling rates are not structural cooling rates in the centre.** Flow carries grains from the periphery and the slurry to the centre, so their solidification time is longer than their final position suggests. A dendrite-arm-spacing (DAS) derived cooling rate therefore records the grain's history [ch3, p.97–101].

### 1.2 Quantitative relations

| Eq. | Relation | Variables / notes | Source |
|---|---|---|---|
| 1.1 | H = A·Vcast·R² | H = sump depth; Vcast = casting speed; R = billet radius (Roth; confirmed by Livanov and Dobatkin) | [ch1, p.12] |
| 3.3 | H = A·Vcast·R² / [4 λs (Tm − Tsurf)] | λs = solid thermal conductivity; Tm = melting T; Tsurf = surface or coolant T. Use ingot thickness instead of R for slabs. | [ch3, p.80–81] |
| 3.4 | A = ΔHf ρs + ½ cs ρs (Tm − Tsurf) | ΔHf = latent heat; ρs, cs = solid density and specific heat | [ch3, p.81] |
| 3.5 | Vcast·R = const ⇒ H/R = const | Scale-up rule | [ch3, p.82; ch1, p.12] |
| 1.2 | Vs = Vcast·cos αn | αn = angle between the billet axis and the normal to the front | [ch1, p.12; ch3, p.91] |
| 3.6 | Vs,max = 4 λ (Tm − Tsurf) / (ΔH ρ R) | Maximum *average* solidification rate, assuming a conical sump. ΔH = enthalpy difference between liquid at Tm and solid at (Tm − Tsurf)/2. | [ch3, p.92–93] |
| 3.1 | Pe = ρ c Vcast R / λ | Thermal Péclet number (advection / conduction) | [ch3, p.79] |
| 3.2 | Bi = q R / λ | q = HTC | [ch3, p.79–80] |
| 3.7 | q/A = α T − β | Impingement-zone heat flux; α, β in the table below | [ch3, p.96] |
| 3.8 | q/A = (−1.67×10⁵ + c T*) Qw^(1/3) ΔT + 100 ΔTx³, with c = −4.01×10⁶ Qw² + 6.9×10⁴ Qw + 628 | Downstream zone. T* = mean of water and surface T (K); ΔT = their difference; ΔTx = Tsurf − 90°C (saturation); Qw = water flow (m³/(m·s)) | [ch3, p.96] |

Table 3.1 coefficients for Eq. 3.7 [ch3, p.96]. The printed units are "α, 10⁴ m²/W°C" and "β, 10⁶ °C". **Inference:** for q/A in W/m², dimensional consistency implies W/(m²·°C) and W/m²; check against the original.

| Surface T range | α (×10⁴) | β (×10⁶) |
|---|---|---|
| < 120°C | 2.73 | −1.27 |
| 120–150°C | 9.43 | −9.24 |
| > 150°C | 1.23 | 3.06 |

**Numbers.**
- Typical DC ranges are 1.8 < Pe < 4.5 and 1 < Bi < 25 [ch3, p.80]. H/R rises linearly with Pe, so H ∝ 1/λ [ch3, p.82].
- For Bi < 4, stronger cooling makes the sump much shallower. Above that the gain is slight [ch3, p.86]. Coolant temperature matters only above about 70°C [ch3, p.86].
- Cutting water flow by 20% deepens the sump by only 4% (Prasso). Water flow affects the sump only at low casting speeds [ch3, p.88].
- Vs,max for 2024 billets: R = 97.5 mm → 103 mm/min; R = 185 mm → 54 mm/min [ch3, p.93].
- Dobatkin's optimum speed for 400-mm high-strength billets was 40–85 mm/min [ch1, p.12].
- Cooling rates measured in DC billets:
  - 200-mm extrusion billet: about 3–5 K/s at the centre and 15–20 K/s at the periphery [ch3, p.113].
  - 470-mm 2024 billet at 30–60 mm/min: isolines of 0.7–3.9 K/s [ch5, p.249].
  - Cooling rates and their radial gradients increase with casting speed [ch5, p.248].
- **Start-up transient** [ch3, p.82–86]:
  - The sump overshoots its steady depth, with thermal inertia.
  - 200-mm Al–4%Cu billet: ramping at 113.2 mm/min² lags strongly; ramping at 11.32 mm/min² gives an almost real-time response.
  - After ramping to 200 mm/min, steady state is reached after about 45 s (about 150 mm of cast length).
  - Mushy-zone length responds to speed even more strongly than sump depth [ch3, p.83].
- **Melt temperature.**
  - A higher temperature lowers the liquidus isotherm more than the solidus. The transition region narrows, the mushy zone is essentially unchanged, and flow toward the surface is stronger [ch3, p.88–90].
  - Al–2.8%Cu, 200 mm: furnace 700–760°C corresponds to 660–740°C at the hot-top inlet [ch3, p.88–90].
  - Shestakov's models recommended 150–200 K superheat instead of the usual 60–80 K, but the effect showed only in slow-solidifying alloys [ch3, p.88].
- **Alloy freezing range.** A wider range widens the transition region, nonlinearly for large ranges. A higher Bi narrows it [ch3, p.91].

### 1.3 Design levers
- **Casting speed and section size are the master variables.** Sump depth scales with Vcast·R² (thickness² for slabs). Keep Vcast·R constant when scaling [ch3, p.80–82].
- Higher alloy thermal conductivity gives a shallower sump [ch3, p.82]. **Inference:** dilute 1xxx/3xxx alloys, which have high λ (general knowledge), tolerate higher speeds than 2xxx/7xxx at equal sump geometry.
- **Do not chase water flow.** Above Bi ≈ 4 there is no gain; what matters is staying in nucleate boiling [ch3, p.86–87].
- **Start-up.** Ramp the speed gently and design the starting block; both suppress the sump overshoot (see §9 for hot tearing) [ch3, p.82–86].
- **Mould technology** [ch1, p.14–17]:
  - Hot top and air-slip reduce the effective metal head.
  - Dual-jet moulds (22° and 45° jets) shrink the slow-cooled air-gap zone.
  - EMC removes the air gap, stirs the sump, gives a shallower sump with lower gradients, a finer structure and less macrosegregation, and a scalp-free surface.
- Shop rule: **"melt hot, cast cold."** High casting temperatures coarsen the structure, increase porosity and raise bleed-out risk [ch3, p.88].

### 1.4 Pitfalls
- The air-gap zone produces a coarser subsurface band and reheating that can reach remelting (liquation, bleed-out) [ch1, p.14; ch3, p.94, 102].
- Thermocouple-based cooling rates should not be assigned to the structure found at the thermocouple position in the billet centre [ch3, p.101].

---

## 2. Structure scale: grain size, dendrite arm spacing, cooling rate, superheat

### 2.1 Mechanisms
- Grain size is set by nucleation (undercooling, heterogeneous substrates) and growth (crystallography, heat and mass transfer). Higher cooling rate means more undercooling, which gives finer grains [ch2, p.19–20].
- Constitutional undercooling has its maximum **at some distance ahead of the interface**. This matters for the columnar-to-equiaxed transition (CET) and for grain refinement [ch2, p.21–22].
- Secondary DAS is set by coarsening (ripening) once diffusion fields overlap [ch2, p.22–24].
- In 2D PFT simulations, DAS *decreases* early in solidification (branching dominates), then *increases* once ripening and coalescence take over at fs > ~0.7. Fast cooling gives tertiary arms that remelt and coalesce [ch2, p.40].

### 2.2 Quantitative

| Eq. | Relation | Notes | Source |
|---|---|---|---|
| 2.1 | Dgr = A·ΔT0^0.25·Vs^−0.25·G^−0.5 | ΔT0 = solidification range; Vs = interface velocity; G = gradient; A = alloy constant. For a given alloy **G is the most decisive factor**, and a larger ΔT0 gives finer grains. | [ch2, p.21] |
| 2.2 | d = B·tf^n | tf = local solidification time = ΔT0/(G·Vs) | [ch2, p.24] |
| 2.3 | d = C·Vc^−n | Vc = cooling rate (= G·Vs); n = 0.2–0.4 for Al alloys. In Al–Cu, n ≈ 0.4 for DAS and ≈ 0.3 for grain size, and C falls as Cu rises. | [ch2, p.24] |
| 2.6 | d(t) = d0·(t/tf)^n | Coarsening during solidification. n = 0.33 is the default for Al alloys. | [ch2, p.37–38] |

- The coarsening exponent n rises from 0.33 to 0.5 when coarsening becomes convection-controlled (simulation). Experimentally, Al–4.5%Cu goes from 0.3 to 0.5 under forced flow. In situ Al–30%Cu shows 0.4 during front deceleration and 0.28–0.5 during acceleration [ch2, p.38].
- **Superheat** [ch2, p.24–28]:
  - Commercial melts are seldom heated above 800°C (coarsening, columnar grains, gas) [ch2, p.24].
  - In pure Al the grain coarsens up to 950°C and stabilises or slightly refines above 1000–1050°C, because alumina becomes wettable and active above 950°C [ch2, p.25].
  - A 2024 alloy cooled at 5.5 K/s: grain size 63 µm (pour at 700°C) → 622 µm (980°C) → 332 µm (1030°C), then coarser again [ch2, p.25].
  - Refinement by superheating needs about 200–250°C superheat to dissolve melt heterogeneities, which is impractical in production [ch2, p.27–28].
- **Grain size and DAS across DC billets.**
  - Grain size coarsens from surface to centre. It also coarsens with higher melt temperature and lower speed [ch3, p.104–108].
  - DAS is more responsive than grain size to casting speed and water flow [ch3, p.104].
  - 7075, 200 mm: grain size 1080 µm without GR → 165 µm with GR (80 mm/min) and 95 µm with GR at 120 mm/min. DAS at the centre is 22–23 µm for both GR and non-GR [ch5, p.256].
  - Chu and Jacoby, 7xxx ingot: counting fine-cell grains only, DAS *decreases* from 55 µm at mid-thickness to 40 µm at the centre; the average including coarse cells would be 80 µm [ch3, p.105].
- **Structure zones across a billet** [ch3, p.101–106]:
  - Fine surface zone (mould contact).
  - Coarser band (air gap).
  - Finer band (water impingement plus intense flow at the slurry/mush border, i.e. fragmentation).
  - General coarsening to the centre.
  - Possible DAS refinement at the very centre in fine-cell grains, mostly in GR alloys, plus a duplex coarse/fine-cell structure.
- Low-alloyed alloys tend to coarser grains and peripheral columnar growth (e.g. Al–Cu billets as Cu falls) [ch3, p.104].

### 2.3 Design levers
- **DAS is a process lever.** Casting speed refines DAS across the whole billet; peripheral zones respond most [ch3, p.108].
  **Inference:** a finer DAS gives finer constituent intermetallics and a shorter homogenisation diffusion distance (∝ d²) (general knowledge for the d² scaling).
- **Grain size is mainly a composition lever** (refiner and solute Q; see §5). Process parameters change it only modestly [ch3, p.104].
- Keep superheat moderate. Very high superheat to refine the structure is impractical [ch2, p.28].

### 2.4 Pitfalls
- Average DAS in the centre mixes coarse-cell "floating" grains and fine-cell grains. Measure them separately [ch3, p.102, 105].

---

## 3. Microsegregation and non-equilibrium solidification

### 3.1 Mechanisms
- Three diffusion processes control solidification: bulk liquid transport, dissipation of the solute pile-up at the front, and diffusion in the solid. When they are incomplete, the result is microsegregation, excess (non-equilibrium) eutectic and incomplete peritectics [ch2, p.28–29].
- **Gulliver–Scheil assumptions:** complete liquid mixing, no solid diffusion, local interface equilibrium. They are often taken as valid for shape and DC casting rates [ch2, p.29].
- The liquid left at the eutectic temperature forms a **non-equilibrium eutectic**. The temperature at which it vanishes is the **non-equilibrium solidus (NES)** [ch2, p.29–31].
- The real response of eutectic fraction to cooling rate is non-monotonic. Back diffusion is aided by fine structure, dendrite coarsening dissolves fine arms, the eutectic can undercool, and solute accumulates in tertiary arms. All of these can *reduce* the eutectic at higher cooling rates [ch2, p.35–40].

### 3.2 Quantitative
- **Eq. 2.4 (Scheil):** CL = C0·(1 − fs)^(K−1) [ch2, p.29]. For Al–4%Cu, about 8 vol% liquid remains at the eutectic temperature and forms eutectic [ch2, p.31].
- **Eq. 2.5 (Brody–Flemings Fourier number):** α′ = 4·DS·tf/d². Back diffusion becomes appreciable if α′K ≥ 0.1. At 0.1–10 K/s, α′ ≈ 10⁻² and falls only slowly with cooling rate [ch2, p.33].
  - Al–2.5%Cu: α′ = 0.009 at 16 K/s and 0.0165 at 0.8 K/s [ch2, p.39–40].
- **Coarsening effect:** with no coarsening (n = 0), the predicted eutectic fraction is almost double that at n = 0.33 [ch2, p.38].
- **Eutectic vs cooling rate** [ch2, p.31–37]:
  - Reported trends conflict (Table 2.1).
  - Novikov and Zolotorevsky found a peak at *low* cooling rates.
  - Recent Al–Cu data confirm the eutectic fraction can fall with cooling rate in the 0.4–16 K/s range.
  - Brody–Flemings, Alstruc and 1D PFT models all wrongly predict a monotonic increase. Example (1D PFT, Al–1.8%Cu): 2.72 wt% eutectic at 0.4 K/s vs 3.22 wt% at 13 K/s, with DAS 20 µm.
  - 2D PFT reproduces the experimental trend, though it overestimates the eutectic amount [ch2, p.38].
  - Coarsening starts to affect the liquid fraction at fL ≈ 0.46 [ch2, p.40].
- **DC billets** [ch3, p.113–115]:
  - The non-equilibrium eutectic fraction has a persistent **minimum at the billet centre**.
  - The centre-vs-periphery cooling-rate difference (3–5 vs 15–20 K/s) cannot explain this. The proposed causes are convection-enhanced coarsening and back diffusion in the stagnant centre, flow, and negative centreline macrosegregation; the last alone accounts for up to about 0.3 vol% of eutectic variation in an Al–4.25%Cu billet.
  - Eutectic fraction rises with casting speed and falls with water flow.
  - High melt temperature concentrates eutectic in the centre.
  - More solute gives more eutectic, and the central dip is stronger in leaner alloys.

### 3.3 Design levers
- The **NES**, not the equilibrium solidus, sets the safe temperature for first homogenisation and solution treatment. Examples: 5182 NES 470°C vs equilibrium solidus 576–578°C; 3003 NES 589°C at 17 K/s (§4) [ch2, p.47, 53].
  **Inference:** use step heating or ramping through the NES window.
- The **amount of last eutectic** indicates hot-tear resistance: more last liquid means more healing (§9) [ch5, p.256, 262].

### 3.4 Pitfalls
- Scheil models over-predict eutectic at DC rates and do not capture the non-monotonic cooling-rate effect [ch2, p.31–38].

---

## 4. Solidification paths and phase selection in wrought alloys

General points: real as-cast phase assemblages differ from equilibrium (suppressed peritectics, extra eutectics, metastable phases). Identifying phases by morphology alone is risky [ch2, p.43, 53].

### 4.1 Non-equilibrium reaction temperatures vs cooling rate (Bäckerud data, as compiled)

| Alloy (wt%) | Cooling rate (K/s) | Start of (Al) (°C) | Key intermediate reactions (°C) | NES / end (°C) | Source |
|---|---|---|---|---|---|
| 1050 (0.37 Fe, 0.05 Si) | 0.4 / 1.2 / 18 | 659 / 659 / 659 | L→(Al)+Al3Fe: 650 / 649 / 647. L+Al3Fe→(Al)+Al8Fe2Si: — / 642–638 / 630 | 642 / 638 / 630 | [ch2, p.46] |
| 3003 (1.19 Mn, 0.55 Fe, 0.18 Si) | 0.5 / 17 | 655 / 655 | L→(Al)+Al6(FeMn): 653 / 646–615. L+Al6(FeMn)→(Al)+Al15(FeMn)3Si2 and/or L→(Al)+Al15(FeMn)3Si2: 641–634 / 589 | **634 / 589** | [ch2, p.47] |
| 6063 (0.43 Mg, 0.39 Si, 0.2 Fe) | 0.5 / 15 | 655–653 / 654 | L→(Al)+α(AlFeSi, cubic, metastable): 618–615 / 617. L+α→(Al)+Al5FeSi: 613 / 610. L+α→(Al)+Al5FeSi+Mg2Si: 576 (est.) | 576 | [ch2, p.49] |
| 5182 (4.74 Mg, 0.34 Mn, 0.28 Fe, 0.10 Si) | 0.3 / 11 | 632 / 632–623 | (Al)+Al6(FeMn) and/or Al3(FeMn): 621–617 / 620. (Al)+Al3Fe+Mg2Si: 586 / 583. (Al)+Al3Fe+Mg2Si+Al8Mg5: 557–470 / 543–470 | **470 / 470** (equil. 576–578) | [ch2, p.53] |
| 2024 (4.44 Cu, 1.56 Mg, 0.55 Mn, 0.21 Si, 0.23 Fe) | 0.8 / 13 | 637–633 / 637–627 | (Al)+Al15(MnCuFe)3Si2: 633–613 / 613. Peritectic to Al20Cu2Mn3 + Al2Cu: 551–538 / 544. Final eutectic(s) with Al2Cu, Al2CuMg, Mg2Si (garbled) | 486 / 480 | [ch2, p.54] |
| 7005 (5.14 Zn, 1.12 Mg, 0.18 Mn, 0.19 Fe, 0.08 Si) | 0.3 / 15 | 641 / 638 | Al3Fe: 632–596 / 610. Mg2Si: 596 / 560. Al2Mg3Zn3: 470 (reaction starts) | 470 | [ch2, p.55] |
| 7075 (5.72 Zn, 2.49 Mg, 1.36 Cu, 0.19 Cr, 0.28 Fe, 0.11 Si) | 0.3 / 2.3 | 630–623 / 628 | Al3Fe: 618–615 / —. Mg2Si: 568–563 / 558–550 | 469 / 466 | [ch2, p.56] |

### 4.2 1xxx (Al–Fe–Si) and 8xxx
- Suppressed peritectics let Al3Fe, Al6Fe, α-Al8Fe2Si, β-Al5FeSi and δ-Al4FeSi2 **coexist** in commercial castings [ch2, p.43].
- Metastable variants (α cubic, α′, α″, q1, q2, β′ and others; Table 2.2) form in commercially pure Al with ≤ 0.5% Fe and ≤ 0.5% Si at industrial cooling rates [ch2, p.45–46].
- The equilibrium diagram predicts solidification onset adequately only at 10⁻²–10⁻¹ K/s.
  - At DC-relevant rates (10⁰–10² K/s), phase-field boundaries shift.
  - The primary fields of Al3Fe, Al8Fe2Si and Al5FeSi drift toward lower Si as the rate rises, so Al3Fe formation becomes less probable at high rates.
  - Some eutectic reactions are suppressed at certain Fe/Si levels (text partly garbled) [ch2, p.44–45].
- The NES of most Al–Fe–Si alloys is **576°C** (ternary eutectic L → (Al) + (Si) + Al5FeSi) [ch2, p.45].
- **Fe:Si > 1** is the usual practice. It avoids free Si and the low-melting ternary eutectic, and therefore hot tearing [ch2, p.46].
- Metastable Al6Fe can form in 1050 cast at > 1 K/s [ch2, p.46].
- Because Fe solubility in (Al) is low, Fe-containing phases of **secondary** origin (precipitated during homogenisation) cannot exceed 0.1–0.2 vol% [ch2, p.46].
- **8006** with low Si may contain Al6(FeMn) and Al3Fe from secondary (eutectic) reactions. *Primary* crystals of these phases form only at low cooling rates and high Fe [ch2, p.46].
- **Fir-tree zone** in 1xxx and 5xxx ingots: a zone of differing NaOH etching response [ch3, p.116–118]:
  - **Cause:** nucleation and growth competition among metastable and stable Fe phases under the variable subsurface cooling.
  - Metastable AlmFe (Al9Fe2) and α″(AlFeSi) need about 20 K/s.
  - At 2–5 K/s (air gap and deeper), a mixture of AlxFe (Al5Fe), Al6Fe and cubic α(AlFeSi) forms, and faster-growing Al6Fe overgrows AlmFe.
  - Equilibrium for 0.25 Fe–0.13 Si is (Al) + Al3Fe + α(Al8Fe2Si) (600 × 1350 mm ingots, 100 mm/min).
  - Annealing at 590°C for 5 h converts much of the surface metastables, but α″ persists.
  - **Remedies:** Fe:Si ≈ 3, small Cr and Mn additions, low-head casting and a reduced air gap.
  - Fir-tree structure can also appear in the centre of small ingots and billets.

### 4.3 3xxx (Al–Mn–Fe–Si)
- The combined presence of Mn, Fe and Si gives Al6(FeMn) plus **Al15(FeMn)3Si2**. The latter forms through eutectic and peritectic (bi-/monovariant) reactions [ch2, p.46–47].
- 3009 and 3003 at low Fe contain the ternary Al15Mn3Si2 [ch2, p.46].
- **Silicon strongly lowers the solidus of Al–Mn alloys** (the extraction reads "by 60°C", partly garbled) [ch2, p.46].
- The amount of Al15(FeMn)3Si2 rises with Si. At upper-limit Si (0.6%) with low Fe, free (Si) can form and the solidus drops to **573°C** (L → (Al) + (Si) + Al15(FeMn)3Si2) [ch2, p.47].
- For 3003, raising the cooling rate from 0.5 to 17 K/s lowers the solidus from 634 to 589°C (Table above) [ch2, p.47].
- **Inference for AA3102/AA3207-type lean alloys:** keep Si low and Fe:Si high. This keeps the NES high, avoids free Si (the low-melting eutectic that drives hot tearing; see [ch2, p.46]), and favours Al6(FeMn) over α-Al15(FeMn)3Si2. The phase balance should be checked by CALPHAD/Scheil, because the source gives no data for these specific grades.

### 4.4 5xxx (Al–Mg–Mn)
- Mg affects the liquidus and solidus much more strongly than Mn. Fig. 2.19 serves as a directory for choosing casting and annealing temperatures [ch2, p.51].
- **5083/5182/5456 (4–7% Mg, 0.3–0.8% Mn)** [ch2, p.51]:
  - (Al) starts at 635–640°C, and the (Al) + Al6Mn eutectic forms at 627–617°C.
  - **Mn usually stays in supersaturated solid solution after casting**, because of its low diffusivity, and precipitates as **dispersoids** during annealing.
  - Equilibrium at > 4% Mg and > 0.1% Mn: (Al) + Al8Mg5 + Al10(MgMn)3. At < 2–3% Mg: (Al) + Al6Mn + traces of Al10(MgMn)3.
- With Fe present, the (Al) + Al6(FeMn) eutectic forms at 600–570°C, and solidification ends at about 570°C with (Al) + Al6(FeMn) + Al3Fe [ch2, p.52].
- With Fe and Si (5182), equilibrium solidification ends at 576–578°C with Mg2Si. In reality liquid persists to **470°C**, extending the range by about 100°C [ch2, p.52–53].
- Thompson et al.: raising the cooling rate from 0.5 to 2 K/s lowers the (Al) + Al6(FeMn) eutectic from 588 to 575°C and the solidus from 510 to 461°C [ch2, p.53].

### 4.5 6xxx (Al–Mg–Si–Fe–(Cu))
- All phases are of eutectic origin. The NES is **555°C** when the ternary (Al) + (Si) + Mg2Si forms [ch2, p.47].
- Fe phases are α(Al8Fe2Si), β(Al5FeSi), Al3Fe and π(Al8FeMg3Si6) [ch2, p.47–48].
  - High Mg:Si binds Fe as Al3Fe; the inverse ratio gives β and π.
  - α has the most favourable morphology but a narrow composition window [ch2, p.48].
- A small Si increase within 0.4–0.8% Si (at 0.9% Mg) lowers the solidus by up to **25°C**. Mg has a weaker effect. Up to 0.1% Si is bound in Fe phases at 0.2% Fe [ch2, p.48–49].
- Al–0.8Mg–0.6Si–0.3Fe at about 0.1 K/s: Al3Fe at 625°C and metastable α(AlFeSi) at 593°C. Al–0.5Mg–0.5Si–0.2Fe forms α instead of the equilibrium Al3Fe [ch2, p.49].
- **Cu-bearing 6xxx:** the Q phase (Al5Cu2Mg8Si6, formula partly garbled) forms by peritectic reaction at 512–514°C or by a multiphase eutectic at 505–507°C. It is stable even at 0.25% Cu with excess Si.
  - Mondolfo's equilibrium conditions: Mg:Si < 1.73, [Mg] > 2[Cu], [Cu] > 1% [ch2, p.50–51].

### 4.6 2xxx, 7xxx, Al–Li (brief)
- 2618: Al9FeNi forms over about 640–645 → 505–515°C and only changes morphology on later treatment. Al2CuMg (non-equilibrium) dissolves fully on homogenisation. NES is 515°C, or about 505°C at maximum Cu [ch2, p.54–55].
- 7xxx: Zr and Cr enter (Al) during solidification and do not change the as-cast phase assemblage [ch2, p.56]. 7075 non-equilibrium solidification ends at 466–469°C (ch2 also cites 435–445°C in connection with dissolution during homogenisation; garbled) [ch2, p.56].
- Al–Li NES values:
  - Al–Cu–Li: can drop to 518–528°C [ch2, p.57].
  - Al–Li–Mg–Zr: 530°C [ch2, p.57].
  - Lowest Al–Cu–Li–Mg eutectic: 484°C [ch2, p.59].
  - Weldalite-type: minimum solidus 507–513°C [ch2, p.59].

---

## 5. Grain refinement and growth restriction

### 5.1 Mechanisms
- **Solute effect.** Rejected solute restricts growth and builds constitutional undercooling that lets nuclei activate ahead of the front [ch2, p.59–63].
  - Above some level of Q, grains become highly branched and solute escapes sideways, so effective growth restriction falls [ch2, p.63–64].
  - Solute brought to the interface by convection, or by local supersaturation, can remelt dendrite roots and fragment them ("grain multiplication") [ch2, p.61–63].
- **Inoculants: Al–Ti–B.** Borides survive dissolution of the master alloy, while Al3Ti dissolves. The excess Ti segregates to boride surfaces and forms a thin metastable Al3Ti layer on which (Al) nucleates. Orientation: (0001)TiB2 ∥ (112)Al3Ti ∥ (111)Al [ch2, p.73].
  - In situ diffraction: metastable Al3Ti appears about 10 K above (Al) nucleation and is consumed. Nucleation is essentially finished by about 20% solid, because latent heat stops further nucleation. The source states that solute Ti enhances nucleation "not by a growth-restriction mechanism" but through improved wetting of TiB2 by the melt [ch2, p.73–74]. The growth-restriction school is described as an alternative view [ch2, p.74–75].
- **Al–Sc–Zr analogue.** Al3Sc forms a rim on primary Al3Zr and "activates" it, so less Sc is needed [ch2, p.69].
- **Other routes:**
  - Melt superheat (§2) [ch2, p.24–28].
  - Ultrasonic cavitation, which activates oxide "plankton", deagglomerates borides and gives non-dendritic grains [ch2, p.75]. It produced 20–80 µm non-dendritic grains in large 2xxx/7xxx ingots and billets **with no hot or cold cracks**, while dendritic counterparts cast the same way always cracked [ch5, p.258].

### 5.2 Quantitative

| Eq. | Relation | Notes | Source |
|---|---|---|---|
| 2.7 | P = m·C0·(K − 1)/K = ΔT0 | Undercooling parameter = equilibrium freezing range | [ch2, p.59] |
| 2.8 | Q = m·C0·(K − 1) = K·ΔT0 | Growth restriction factor; m = liquidus slope at C0; K = partition coefficient | [ch2, p.60] |
| 2.9 | ΔTc = Ξ·Q, with Ξ = (C_L^ss − C0)/(C_L^ss·(1 − K)) | Constitutional undercooling; Ξ = solutal supersaturation | [ch2, p.60] |
| 2.10 | Vgrowth = Ds·ΔTc²/(Q·Γ), with Γ = σls/Δsf | Maximum growth velocity | [ch2, p.60] |
| 2.11 | Ω = 1/(N·f)^(1/3) + b·ΔTn/Q | Grain-size criterion. N = particle density; f = active fraction; ΔTn = nucleation undercooling | [ch2, p.65] |
| 2.12 | Ω = 1/(Nd·nd) | d-shell criterion: Sc 0.333, Ti 0.167, Zr 0.125, Mn 0.067, Fe 0.055 (larger = better refiner) | [ch2, p.65] |
| 2.14 | na = J·ΔHv/ΔHf | Atoms in a stable cluster; J = 1/4 (fcc/hcp), 9/16 (bcc) | [ch2, p.66] |

- **Q and P values.** Ti: Q ≈ 35 at C0 = 0.15%. Sc: Q = 2.5 at 0.6% Sc, yet Sc is the most powerful refiner. P: Sc ≈ 5, Ti ≈ 4.4 [ch2, p.65].
  - **(derived)** m(K − 1) ≈ 233 K/wt% for Ti and ≈ 4.2 K/wt% for Sc.
- **Additivity of Q is questionable.** Elements interact, and hypoeutectic elements add solute while "hypoperitectic" ones (Ti) add solvent. It still works in practice, because individual constitutional-undercooling effects are similar [ch2, p.64–65].
- **Concentrations.** Ti added via Al–Ti–B is typically 0.001–0.005% [ch2, p.65], and total Ti is usually < 0.05% with excess Ti over TiB2 [ch2, p.72–73]. Binary refinement on primary phases needs > 0.15% Ti or > 0.6% Sc [ch2, p.68]. Master alloys are 3–5% Ti, 1–3% B [ch2, p.73], or Al–Ti–C with about 3% Ti and 0.15% C [ch2, p.74].
- **Lattices** [ch2, p.68–70]:
  - Al3Ti: tetragonal I4/mmm, a = 0.385 nm, c = 0.86 nm.
  - Al3Sc: L1₂, a = 0.4104 nm, vs (Al) a = 0.404 nm.
  - AlB2: a = 0.3003 nm, c = 0.3251 nm. TiB2: a = 0.3032 nm, c = 0.3231 nm.
- **Al–Ti–B reactions** [ch2, p.71]: L + Al3Ti → (Al) at 665°C; L + Al3Ti → (Al) + TiB2 at about 665°C; L → (Al) + AlB2 at 659°C; L + TiB2 → (Al) + AlB2 at about 659°C.
- **Al–Ti–C** [ch2, p.71–72]: L + TiC → Al3Ti + Al4C3 at 693°C (700 and 812°C are also reported). TiCx has 0.48 < x < 0.98, Fm3m, a = 0.43176 nm.
- **Al–Sc–Zr** [ch2, p.68–69]:
  - Al3Sc forms peritectically at 1320°C and dissolves Zr up to Al3Sc0.6Zr0.4.
  - Al3Zr (D0₂₃) melts congruently at 1577°C and dissolves Sc up to Al3Zr0.8Sc0.2.
  - L + Al3Zr → (Al) + Al3Sc at 659°C.
  - Mutual solubility in (Al): 0.06% Zr + 0.03% Sc at 550°C; 0.09% Zr + 0.06% Sc at 600°C.
  - Commercial levels are < 0.3% Sc and < 0.15% Zr (< 0.45% total), typically 0.15 Sc + 0.15 Zr. The primary phase is Al3Sc if Zr:Sc < 1 and Al3Zr if Zr:Sc > 1.

### 5.3 Design levers
- **Partition coefficients** (Table 4.9; see §8) [ch4, p.172]: Fe 0.03, Si 0.13, Cu 0.17, Mg 0.43, Zn 0.45, Mn 0.82, Ti 9.0, Cr 2.0.
  **Inference:** Mn (K ≈ 0.8) contributes little growth restriction per wt% and Fe (K ≈ 0.03) a lot, so lean 3xxx/1xxx alloys rely on TiB2 inoculation for equiaxed grains. The source gives no m values to compute Q here (gap).
- **GR reduces hot tearing** while grains stay dendritic (§9) [ch5, p.256–258].
- **GR can worsen centreline macrosegregation**, especially with potent Al5Ti0.2B [ch4, p.173]. It also widens the slurry zone and narrows the mushy zone, which can cause bleed-out unless melt temperature and speed are adjusted [ch3, p.121].

---

## 6. Grain-structure anomalies: floating grains, duplex structure, feathery grains

- **Floating ("coarse-cell") grains** [ch3, p.108–110]. Three origins:
  1. Grains formed on the free melt surface, distribution bag or hot top. These are coarse and large, and can be avoided by good practice.
  2. Fragments or dendrites detached at the slurry/mush border by remelting or flow.
  3. Grains that nucleate at the periphery liquidus and grow while travelling to the centre.
- In round billets, inward currents peak at about 2/3 of the radius from the centre and form a central vortex [ch3, p.109].
- They give a **duplex** centre: coarse-cell grains, sometimes with fine-cell rims [ch3, p.99–100].
- **Process sensitivity** [ch3, p.109–110]:
  - Higher casting speed gives more floating grains, because of a deeper sump, stronger flows and a larger stagnant centre.
  - Water flow has no effect.
  - Melt temperature acts differently with speed: at low speed, higher temperature *reduces* them and confines them to the axis; at high speed, higher temperature *increases* them.
- Coarse-cell grains are **solute-poor** (§8, Table 4.4) [ch4, p.148]. In 200-mm 2024 billets, GR raised the volume fraction of coarse-cell grains from 35% to 65–70% [ch4, p.175].
- **Feathery grains** [ch3, p.118–120]:
  - **Structure:** ⟨110⟩ dendrites with trunks split by coherent {111} twin planes, instead of normal ⟨100⟩ growth.
  - **Favoured by:** cooling rate > 10 K/s, or overheated melt contacting the water-cooled mould (high G); forced flow; high melt temperature; pure alloys (1xxx); growth restrictors Cr, Zr, Ti; and strongly segregating Mg, Cu, Zn, Si.
  - **Consequences:** anisotropic, inhomogeneous recrystallisation, intermetallic segregates, low directional ductility.
  - **Remedies:** proper grain refinement, less superheat and slower casting (lower G in the liquid).
  - Grün and Schneider: in GR commercial Al billets poured at 700–740°C, higher temperature gave feathery columnar grains and higher gradients near the mould [ch5, p.259].
  - **Inference:** this is a real risk for lean 1xxx/3xxx foil and fin-stock ingots cast hot. Keep superheat down and refine.

---

## 7. Transition-element supersaturation and homogenisation implications

**What the source gives** (qualitative; no supersaturation-vs-cooling-rate data in this book):
- **Mn** usually stays in supersaturated solid solution after DC casting, because of its low diffusion coefficient. It precipitates as Mn-bearing **dispersoids** during annealing of the cast material [ch2, p.51].
- **Sc and Zr** enter (Al) during solidification at real casting rates. On high-temperature annealing they precipitate as coherent Al3Sc (stable) and Al3Zr (metastable) [ch2, p.57].
  - Zr and Cr likewise enter (Al) in 7xxx without changing the as-cast phases [ch2, p.56].
  - Equilibrium Zr/Sc solubility limits are listed in §5.2 [ch2, p.68].
- **Fe:** solubility is so low that secondary Fe-phase precipitation is ≤ 0.1–0.2 vol% [ch2, p.46].
  - Metastable Fe(Si) phases from casting transform to equilibrium ones if the homogenisation temperature is high enough [ch2, p.46].
  - α″ survived 590°C for 5 h in ingot surfaces [ch3, p.116–118].
- **Peritectic formers (K > 1: Ti, Zr, Cr)** concentrate in dendrite cores and at the billet centre: positive centreline macrosegregation, the opposite of K < 1 elements [ch4, p.170].
- **Non-equilibrium eutectics** dissolve during proper homogenisation [ch3, p.111]. Examples: Al2CuMg in 2618 [ch2, p.55]; Al2Cu and AlLi in Al–Li alloys [ch2, p.57]. Insoluble constituents such as Al9FeNi only change morphology [ch2, p.55].
- **Macrosegregation is not removed by homogenisation.** Diffusion lengths are µm for microsegregation and cm for macrosegregation [ch4, p.125–126].
- **Inference (for 3xxx homogenisation design):**
  - The as-cast Mn supersaturation and its *dendritic* distribution set the dispersoid density and the dispersoid-free zones after homogenisation.
  - Mn has K ≈ 0.82 [ch4, p.172], so its microsegregation is mild, whereas Fe (K = 0.03) sits almost entirely in constituents.
  - Higher DC cooling rates (smaller DAS, finer constituents) should raise supersaturation and shorten diffusion distances (general knowledge).
  - The Fourier number α′ = 4·D·t/d² [ch2, p.33] can be reused as a homogenisation-completeness metric with d = DAS (inference).
  - The NES values in §4.1 bound the first heating step.

---

## 8. Macrosegregation

### 8.1 Mechanisms
- Macrosegregation is caused by **relative movement of solid and liquid** [ch4, p.128]:
  - Thermosolutal convection penetrating the slurry.
  - Transport of solid (floating grains).
  - Shrinkage-driven flow in the mush.
  - Metallostatic-pressure flow.
  - Deformation (thermal-contraction) driven flow.
  - Forced flows from pouring, stirring or EMC.
- **Typical DC pattern = inverse segregation:** negative at the centreline, positive at the surface, with a strongly depleted subsurface layer [ch4, p.126].
  - The composition difference across the section is ≤ ~1%, versus tens of percent between solid and liquid [ch4, p.125].
  - Inverse segregation increases with freezing range, hydrogen, and coarse or columnar structure [ch4, p.127–128].
- **Thermosolutal convection** washes solute-rich liquid out of the slurry in the outer quarter of the billet and carries it to the centre. This **enhances normal (positive-centre) segregation** [ch4, p.136–138].
  - Screw-pump experiments: flow aligned with natural convection increases positive centreline segregation; flow opposed to it almost eliminates macrosegregation [ch4, p.138–140].
  - **Multicomponent buoyancy:** Mg lowers liquid density, the opposite of Cu. In a 2024-type billet, Cu relative segregation was 0.017 with Mg buoyancy vs 0.020 without (about 20% less). The relative upward flow at the centre was about 0.8 mm/s [ch4, p.140–141].
- **Shrinkage-driven flow** runs normal to the solidification front, from centre to periphery.
  - Velocity is about 10⁻⁴ m/s (6 mm/min), versus casting speeds of 100–200 mm/min, but it carries highly enriched liquid [ch4, p.143].
  - Flemings' criterion: no segregation when the flow exactly feeds shrinkage; inverse segregation when the flow is faster than the solidification rate; normal segregation when it is slower or reversed [ch4, p.143–144].
  - Only the **horizontal component** depletes the centre [ch4, p.144–145].
  - Livanov's partition experiments (330-mm 2024 billet): at 30 mm/min, solute-rich liquid moved toward the centre; at 60 mm/min, toward the periphery [ch4, p.142–143].
- **Floating grains** contribute only negatively (solute-poor solid accumulates) [ch4, p.146–149].
  - Chilled-cavity tests with flow at 0.03–0.3 m/s: negative segregation rose downstream as flow velocity increased [ch4, p.149].
  - The literature on duplex structure vs segregation direction is contradictory (Table 4.5) [ch4, p.150].
- **Deformation-driven flow:** about 2% volumetric thermal strain can segregate as much as shrinkage does [ch4, p.151].
  - Compression squeezes liquid out (negative); tension (billet centre) sucks it in (positive).
  - Together with metallostatic pressure and air-gap remelting, it drives **surface exudation plus subsurface depletion** [ch4, p.151].

### 8.2 Quantitative

**Permeability** [ch4, p.133–136]:

| Eq. | Relation |
|---|---|
| 4.1 | Darcy: Q = kD·A·ΔP′/L |
| 4.2 | Specific permeability: K = µ·kD |
| 4.3 | v = −(K/(µ·fl))·(ΔP/L + ρl·g) |
| 4.5 | Kozeny–Carman: K = (1 − fs)³/(kKC·Sv²·fs²), with kKC = 5 for equiaxed structures |
| 4.6 | K = d²·(1 − fs)³/(180·fs²); use Dgr for globular grains |
| 4.7 | Columnar, flow parallel to trunks: K = C·λ1²·(1 − fs)³/fs; doubtful above fs ≈ 0.35 |
| 4.11 | Blake–Kozeny: K = k0·(1 − fs)³/fs² |

Kozeny–Carman is adequate, to order of magnitude, for 0.6 < fs < 0.9. Near fs → 1 there is a percolation limit [ch4, p.136]. Simulations used K = 6.67×10⁻¹¹ to 5×10⁻¹⁰ m² [ch4, p.145].

**Analytical shrinkage-segregation model** [ch4, p.153–155]:
- ε = Lm·cos α·S·β·fl.
- Vshr = Vcast·fl·β·cos α.
- Vh = Vcast·fl·β·sin2α/2.
- Solute flux F = CL·Vh.
- fl = 1 − (Vcast/Lm)·t.

Here Lm = vertical mushy-zone dimension, α = slope of the coherency isotherm to the horizontal, and β = volumetric shrinkage (about 0.1 for Al alloys; up to 0.117 for Al–4%Cu). For Al–Cu (K = 0.171, β = 0.1) this gives **Lh = 0.78·C0·Lm·β·sin2α/2**, and the relative segregation is −(dLh/dR)/C0.

**Practical sump-slope rule:** macrosegregation is negligible if α < 30° and acceptable if α < 60° [ch4, p.158].

**Speed limit for billets:** Vcast ≤ A/D, with A = 25,000–33,300 mm²/min (alloy dependent) and D in mm. For a 200-mm billet this gives 125–167 mm/min, with a maximum relative segregation of 3–6% of nominal [ch4, p.152].

**Similarity criterion (Livanov):** SC = Vcast·D/a, with a ≈ 12,000 mm²/min for moulds without hot top. SC < 1 gives normal (positive-centre) segregation and SC > 1 inverse [ch4, p.161].
- For a 200-mm billet the transition is at about 60 mm/min.
- The threshold cooling rate for zero centreline segregation is about 2.3 K/s for D = 300 mm and about 11 K/s for D = 168 mm [ch4, p.161].
- The literature map gives a threshold Vcast·D of **12,465 mm²/min (non-GR) and 21,774 mm²/min (GR)**. GR billets are more prone to positive centrelines [ch4, p.161].

**Regression on simulated sumps (Eq. 4.22):** CS = −0.06124 − 4.341×10⁻²·Th + 1.64×10⁻³·A (R = 0.65), where Th = liquidus–solidus distance / R and A = angle between the billet axis and the solidus tangent at mid-radius (°) [ch4, p.166].

Simulated test cases (Al–4.5%Cu, Table 4.8) [ch4, p.166–167]:

| Vcast (mm/min) | D (mm) | Centreline segregation | Sump depth (mm) / normalised | L–S distance at centre (mm) / normalised | Angle A (°) |
|---|---|---|---|---|---|
| 300 | 100 | −0.04 | 153 / 3.06 | 70.5 / 1.41 | 15 |
| 200 | 200 | −0.16 (strongly negative) | 220 / 2.2 | 117 / 1.17 | 16 |
| 60 | 500 | −0.02 | 383.5 / 1.534 | 82.4 / 0.33 | 23 |
| 60 | 200 | +0.01 | 88 / 0.47 (as printed) | 47 / 0.47 | 55 |

**Other numbers:**
- Macrosegregation profiles at different speeds collapse when normalised by the vertical transition-region thickness, except near the surface [ch4, p.152].
- Melt temperature: segregation rises near the surface but changes little elsewhere. The consensus (Dobatkin, Tarapore, Reese) is that macrosegregation decreases as casting temperature increases [ch4, p.159].
- Water flow is insignificant if cooling is sufficient [ch4, p.158].
- Ingot thickness of 400–600 mm affects sump depth more than casting speed does (Flood and Davidson) [ch4, p.168].
- **Forced convection** (EMC, mechanical stirring) can turn segregation normal and raises the threshold Vcast·D (2024, 7075) [ch4, p.169–170].
- **Element ranking (K < 1: lower K, more segregation):** Fe (0.03) segregates much more than Mn (0.8). Ti (K = 9) segregates positively at the centre. The extent depends more on the base alloy than on the element's concentration [ch4, p.170–172].
- **Floating-grain composition** (EPMA, 2024 billet, 3.6 Cu–1.4 Mg, 200 mm, 80 mm/min) [ch4, p.148]:
  - Minimum Cu in cell centres: coarse 0.72% vs fine 1.1%.
  - Minimum Mg: coarse 0.47% vs fine 0.7%. GR does not change this.
- **Bulk grain compositions** (nominal 3.5 Cu–1.4 Mg; line scans) [ch4, p.177]:
  - Coarse-cell grains: 2.55 Cu / 0.96 Mg (non-GR) and 2.19 / 0.94 (GR).
  - Fine-cell grains: 3.9 / 1.48 (non-GR) and 4.01 / 1.56 (GR).
  - All-coarse vs all-fine structures would give ΔCu of −0.27 vs +0.11 (non-GR) and −0.37 vs +0.15 (GR) [ch4, p.177].
- **Historical permanent-mould duralumin ingots** (Table 4.1) [ch4, p.127]. Centre–surface ΔCu:
  - Casting temperature 750/730/700°C: 0.28 / 0.37 / 0.57%.
  - Ingot thickness 20/90 mm: 0.24 / 0.54%.
  - In other words, faster cooling gave more inverse segregation.

### 8.3 Grain refinement, feeding system and macrosegregation
- **Competing GR effects** [ch4, p.172–173]:
  - Lower permeability hinders shrinkage flow.
  - Later coherency means a wider slurry zone, more convective wash-out and more floating grains.
  - Smaller grains settle less.
  - Net effect: GR alloys tend toward positive centrelines, but results are diverse.
- **Sheet ingots of 3104, 5182 and 6009** (Gariepy and Caron): centreline segregation *increases* with Ti content (Mg segregation in 3104 rises over 0–0.006% Ti). The more potent **Al5Ti0.2B** gives more segregation than Al–6%Ti or no GR in 5182 [ch4, p.173–174].
- **5182 commercial ingots** (1850 × 550 mm at 60 mm/min with 0.003% Ti; 1050 × 550 mm with 0.015% Ti): GR gave more severe centreline depletion. The duplex structure was seen only in the *non-GR* ingot, so negative centrelines are not tied to floating grains alone [ch4, p.174–175].
- **Al3Ti1B in 200-mm 2024 billets** (80–120 mm/min): no effect on macrosegregation, despite more floating grains [ch4, p.175].
- **Feeding system** [ch4, p.179]:
  - A combo bag gave the least macrosegregation.
  - A headscreen enhances natural convection.
  - Directing flow **downward in the centre** minimises macrosegregation (also seen for 5182).

### 8.4 Design levers and pitfalls
- **Main levers:** sump depth and slope (speed, section size), feeding and flow pattern, EMC or stirring, and the alloy partition coefficients.
  **Inference for 3xxx sheet ingots:** Fe (K = 0.03) is the dominant macrosegregant, so expect Fe-rich surfaces and liquation bands and Fe-lean centres. Mn is mild, and Ti/Cr/Zr segregate positively to the centre.
- Positive or negligible centrelines need low speeds and small diameters, well below commercial rates [ch4, p.169]. Expect inverse segregation in production.
- **Pitfall:** results depend on a fragile balance among mechanisms. Attributing segregation to one cause (e.g. floating grains) without checking the sump geometry and flow is error-prone [ch4, p.150, 179].

---

## 9. Hot tearing

### 9.1 Mechanisms
- Hot tears initiate above the solidus and propagate through interdendritic liquid films or solid bridges.
  - They need **tensile stress** from uneven thermal contraction plus **insufficient feeding** in the vulnerable range, at fs above about 0.85–0.95 (fs > 0.9) [ch5, p.184–185].
  - The most vulnerable range is 90–95% solid, where many boundaries are already bridged [ch5, p.241].
- **Thermal contraction begins at rigidity** [ch5, p.185–197]:
  - Above it, volume changes show only as a falling melt level (fed continuously in DC).
  - Below it, linear contraction starts. Pre-shrinkage **expansion** (from gas evolution and the pressure drop) precedes it [ch5, p.186–190].
- **Liquid distribution matters** [ch5, p.212]:
  - The dihedral angle in Al alloys is < 20–25°.
  - 1% liquid wets about 30% of grain boundaries, and 10% liquid wets about 85%.
- **Alloys with plenty of last liquid self-heal.** The most susceptible alloys are *lean* ones with little eutectic, large thermal strain and a long time in the vulnerable range [ch5, p.241, 253].
- **Crack path:** through liquid films in richer alloys (smooth surface with eutectic) and through **solid bridges** (liquid-metal embrittlement) in lean alloys [ch5, p.241, 263–267].
  - In Al–1%Cu, eutectic is only about 1 vol% and about 90% of grain boundaries are bridged; fracture runs through the bridges [ch5, p.267].
- **Early, large intermetallics are harmful.** Nagaumi: α(AlFeMn) particles formed just after (Al) bridge dendrites, so the mush gains strength at lower fs (zero-strength temperature 623 → 631°C as Fe rises, alloy HS65). They also block feeding channels, so hot-tear susceptibility increases [ch5, p.215, 243].
- **Fine, compact intermetallics can help:**
  - 0.8% Fe in Al–0.7%Cu strengthened the semi-solid state (less continuous films, more bridges).
  - 0.2% Fe in **Al–1.5%Mn** shifted the softening curve to higher temperature. Elongated Al6Mn at grain boundaries was replaced by small compact Al6Mn + Al3Fe eutectic particles, which give many solid bridges [ch5, p.205].
- **Fe:Si ratio.** Raising Fe:Si from 1 to 5 in 7075 strongly strengthened the lower mush, because free-Si low-melting eutectics were suppressed. Recommendation: Fe:Si > 1 [ch5, p.207–208].

### 9.2 Thermal contraction data

Table 5.1: melt 720–730°C, cooling 12–18 K/s [ch5, p.196]

| Alloy | T at onset (rigidity) (°C) | fs at onset (%) | Pre-shrinkage expansion (%) | Contraction in freezing range εth (%) |
|---|---|---|---|---|
| 1050 | 657 | 38 | 0 | 0.03 |
| 2024 | 515 | 87.5 | 0.035 | 0.2 |
| 5182 | 528 | 93 | 0.08 | 0 |
| 6082 | 563 | 95 | 0.025 | 0.02 |
| 7075 | 525 | 87 | 0.03 | 0.27 |

- **Eq. 5.1:** εth = [(ls + Δlexp − lf)/ls]·100% [ch5, p.189].
- **Eq. 5.2:** SF = Vc^−0.33/Dgr [ch5, p.190]. In non-GR coarse structures (7–18 K/s, 700–800°C, Dgr 120–220 µm), contraction increases with SF: smaller grains and coarser arms give more contraction [ch5, p.191].
- In real DC casting, contraction exceeds the theoretical (LTEC-based) value by up to 50% at high casting speeds [ch5, p.191].
- **fs at contraction onset** [ch5, p.192]:
  - At 3–4 K/s: 0.95 at 0.3% Cu down to 0.8 at 4% Cu.
  - At 8–15 K/s: 0.9 at 4% Cu.
  - Accumulated contraction peaks where the non-equilibrium freezing range is largest, and is larger in Al–Mg than in Al–Cu.
- **6061 + Cu** [ch5, p.193–194]:
  - Contraction peaks at 0.2–0.3% Cu.
  - Onset is at 600–610°C, falling to 585°C as Cu goes from 0.2 to 3.8% (non-GR).
  - GR lowers the onset by 20–60°C and cuts total thermal strain 2–3 times, but increases pre-shrinkage expansion (maximum at 0.7–1.5% Cu). Expansion maxima coincide with porosity maxima.
- **Commercial alloys at 2–5.5 K/s** [ch5, p.196–197]: GR raises fs at rigidity and lowers contraction, except in 7075. Extra alloying (+1% Mg, Cu, Zn or Si) lowers fs at rigidity and raises contraction.
- **Eq. 5.3 (constitutive):** ε̇th = (1/3)·ψ(fs)·βT·Ṫ·**I** [ch5, p.197–198].
  - ψ = 0 for fs ≤ fs_th, and ψ = [(fs − fs_th)/(1 − fs_th)]^n above it.
  - n ≈ 0 (a step function) for most commercial alloys.
  - For Al–4%Cu: n = 0 (non-GR, 4 K/s), 0.3 (GR, 4 K/s), 0.1 (non-GR, 8 K/s).
- **Linear thermal expansion coefficient, near solidus, as-cast** [ch5, p.198–200]:
  - Al–Mg (300–450°C): falls from 29 to 25.5 ×10⁻⁶ K⁻¹ as Mg increases. Annealed dilatometer data instead *increase* with Mg; hydrogen and the non-equilibrium structure are suspected.
  - Al–Cu (300–550°C): 30 → 28.5 ×10⁻⁶ K⁻¹. Ellwood and Silcock: 32.4 at 0.95% Cu → 28.2 at 4.97% Cu.

### 9.3 Semi-solid mechanical properties
- **Strength** [ch5, p.205–207]:
  - Coarser grains and dendrites lower strength.
  - GR shifts strength build-up to higher fs.
  - Faster cooling (in the DC range) shifts strength onset to higher temperature and raises it.
  - Strength rises with deformation rate.
  - In high-Cu alloys, continuous films override the benefit of GR.
- **Zero-strength temperature > zero-ductility temperature.** The mush can carry stress while it still has zero ductility [ch5, p.216].
- **3004** shows marked hardening once strength builds, suggesting it cannot fully accommodate thermal stresses. 2024 and 7075 gain strength slowly until a few degrees above the solidus (fs = 0.8 and 0.95) [ch5, p.206–207].
- **Ductility** is U-shaped in temperature, with a brittle range where elongation differs among alloys by only tenths of a percent [ch5, p.208].
  - **Eq. 5.4:** δig ≈ 0.6·Δl/Dgr, where Δl = displacement of adjacent grains [ch5, p.209].
  - GR usually raises ductility.
  - Equiaxed-to-columnar transition lowers it and shifts the brittle range up [ch5, p.209].
  - Slow cooling lowers the bottom of the brittle range; lower-purity base metal lowers its lower bound [ch5, p.210–212].
- **Hydrogen and holding** [ch5, p.214]: holding a 2037 melt for 10 h instead of 20 min coarsened the structure and cut hydrogen from 0.30 to 0.19 cm³/100 g. Both reduced semi-solid plasticity. More gas means less linear contraction and a larger "plasticity reserve".
- **Selected Table 5.2 values** [ch5, p.215]:
  - 3004: zero strength at fs = 0.81.
  - 6063: UTS 0.85–1.75 MPa and El 0.075–0.18% at 610°C (GR); UTS 0.6 MPa and El 0.1% (non-GR). Zero strength at 620°C (GR, fs 0.9) and 630°C (non-GR).
  - 6061: zero strength at 623°C (fs 0.82).
  - 5456: UTS 1.0 MPa at 550°C; zero strength at 570°C.

### 9.4 Hot-tearing criteria

| Type | Criterion | Key expression | DC sensitivity (Table 5.4) | Source |
|---|---|---|---|---|
| Stress (liquid film) | Saveiko / Novikov / Dickhaus | σfr = 2γ/b (Eq. 5.6). Healy: FZ = (3πµR⁴/8t)·(1/b1² − 1/b2²) (5.7). b = (1 − fs)·Dgr/2 (5.8) | — | [ch5, p.225–226] |
| Stress | Lahaie–Bouchard | σfr = (4µ/3b)·[1 + (fs^m/(1 − fs^m))·ε]^−1 (5.9, as extracted). m = 1/3 equiaxed, 1/2 columnar. Predicts fracture strain poorly | — | [ch5, p.226] |
| Stress (Griffith) | Williams–Singer | σfr = √[8Gγ/(π(1 − ν)·A·VL^½)] (5.10, as extracted). Predicts higher strength for coarse grains, which is wrong | — | [ch5, p.226–227] |
| Feeding + Griffith | Suyitno et al. | Feeding rate fe = K·Ps/(µ·Lm²) (5.11). Shrinkage/contraction rate fr = (ρs/ρl − 1)·∂fl/∂t + (ρs/ρl)·ε̇ (5.12). A pore forms if fr > \|fe\| (5.13) and grows if fr − \|fe\| ≥ ζcr ≈ 0 (5.14). A crack forms if a > acr (5.15), with acr = 4γE/(πσfr) (5.16, as extracted; standard Griffith has σ², general knowledge). HCS = a/acr (5.17) | Speed ✓, centre ✓, ramping ✓, practice ✓ (**only one passing all tests**) | [ch5, p.227–228, 237–239] |
| Strain | Novikov reserve of plasticity | pr = S/ΔTbr (5.18), or (S1 − S2)/ΔTbr if the curves cross (5.19). S = area between ductility εp and thermal contraction εth over the brittle range ΔTbr | ✗ for DC dynamics; good for composition ranking | [ch5, p.229–230] |
| Strain | Magnin et al. | Crack if maximum principal plastic strain at the solidus > fracture strain near the solidus | Speed ✓ | [ch5, p.229] |
| Strain rate | Prokhorov | ε̇res = ε̇min − ε̇free − ε̇app (5.24). Tear if ε̇min ≤ ε̇free + ε̇app (5.25) | Speed ✓, centre ✓ | [ch5, p.231–233] |
| Strain rate / pressure | RDG (Rappaz–Drezet–Gremaud) | ΔP = ΔPsh + ΔPmech − ρgh (5.26). ΔPsh + ΔPmech = (180µΔT/(G·λ2²))·[A·Vcast·β + B·(1 + β)·ε̇·ΔT/G] (5.27, as extracted). Pore/tear if ΔP > ΔPcr (5.28); ΔPcr = 2 kPa used for Al–1.4%Cu. HCS = 1/ε̇max (5.29) | Speed ✓, centre ✓, ramping ✓. **Over-predicts:** ΔP > 2 kPa in most DC cases that did not crack | [ch5, p.233–234, 238–239] |
| Time-based | Clyne–Davies | CSC = (t0.99 − t0.90)/(t0.90 − t0.40) (5.30) | ✗ for DC; reproduces the composition "lambda" curve | [ch5, p.234] |
| Feeding | Feurer | SPV = fl²·λ2²·Ps/(24π·c³·η·Lm²) (5.31). SRG = ∂lnV/∂t = −(1/ρ̄)·∂ρ̄/∂t (5.32). Tear possible if SPV < SRG (5.33) | Speed ✓, centre ✓ | [ch5, p.235] |
| Hybrid | Katgerman | HCS = (t0.99 − tcr)/(tcr − t0.40) (5.34), with tcr from Feurer's SPV = SRG | Speed ✓, centre ✓ | [ch5, p.235–236] |

- Suyitno: HCS falls with GR (simulated for grain sizes of 600, 300, 100 and 30 µm, and below some grain size no hot cracking is possible) and with lower speed and slower ramping. Its accuracy depends on mush Young's modulus, surface tension and permeability, all of which are poorly known [ch5, p.228, 238–239].
- Proposed failure modes by solid fraction (Table 5.5) [ch5, p.244]:
  - 50–80% solid: film rupture or healing.
  - 80–99%: film rupture, liquid-metal embrittlement of bridges, ductile bridge failure.
  - 98–100%: liquid-metal embrittlement, creep.

### 9.5 Hot tearing in DC casting: process and composition
- **Stress state** [ch5, p.246–250]:
  - Round billets: tension at the centre (radial and circumferential components dominate above the solidus) and compression at the periphery, except the circumferential component. Cracks are central and spider-like (radial).
  - Rolling ingots: tension near the short faces and corners. Rolling-face **pull-in** puts the near-mush shell in tension, so modern moulds are convex.
- **Casting speed is the most important process parameter.** Water flow matters much less, and melt-temperature data in the literature conflict [ch5, p.246]. Higher speed deepens the sump and pushes tensile strain into the mush [ch5, p.255].
- **Start-up is the most critical stage** [ch5, p.248–251]:
  - Butt curl (fast cooling of the bottom lifts the edges, causing loss of contact, remelting, bleed-out or cracks) and butt swell [ch5, p.248].
  - A gentle speed ramp lowers peak centre stress and strain [ch5, p.249–251].
- **DC trials on 200-mm Al–Cu billets** (Cu = 1.03, 1.98, 2.93, 4.49; Fe 0.16–0.19; Si 0.04–0.10) [ch5, p.251–254]:
  - Cracks formed only at 1–3% Cu, with **maximum susceptibility at 0.5–1.5% Cu**. Almost none formed above 4% Cu even at 220 mm/min (tested up to 5.6% Cu).
  - The speed that starts a crack is higher than the speed at which it stops or heals.
  - Maximum tearing occurred during *deceleration*, because of the sump's thermal inertia. **Sump depth, not speed itself, is the controlling variable.**
  - The transition region widens with higher speed and lower Cu.
- **Grain refinement** [ch5, p.256–258]:
  - 7075, 200 mm: non-GR billets cracked from start-up at 80 mm/min. Feeding GR rod stopped the crack, which reappeared at 120 mm/min. GR added in the furnace gave no cracks at any speed (grain 1080 → 165 µm).
  - GR reduces susceptibility **as long as grains stay dendritic**. Below 300 µm the permeability loss is offset by delayed strain and thinner films.
  - Non-dendritic cellular grains below 50 µm may raise susceptibility again, while fine grains above 100 µm are almost always better than coarse ones.
  - Lin et al. showed GR benefits in **1050, 3104 and 5182** [ch5, p.256].
- **Melt temperature** (Al–2.8%Cu, 200 mm, furnace 700/720/740/760°C = superheat 47/67/87/107°C) [ch5, p.259–262]:
  - Hot tearing *decreased* with temperature: at 700°C macrocracks at 150–200 mm/min; at 760°C only pores and healed cracks at 200 mm/min.
  - Sump geometry hardly changed (Table 5.7: steady 200 mm/min; transition zone 145 vs 138 mm at the centre; mushy zone 24.5 vs 23 mm; sump depth 166 vs 169 mm).
  - Explanation: more central eutectic, a deeper liquid head that improves feeding, wider channels in the coarser structure, and more gas expansion.
  - In shape castings with < 250 K superheat, by contrast, higher temperature coarsens grains and raises hot cracking [ch5, p.259].
- **Composition rules for families** (special hot-tear tests) [ch5, p.217–220]:
  - Hot-tear susceptibility follows a "lambda" curve versus solute, mirroring accumulated thermal contraction [ch5, p.217].
  - **Al–Cu–Mg–Si:** Si shifts the peak to lower Cu/Mg and reduces it. Fe up to 0.65% raises susceptibility in 2038 (low at 0.95% Si). Mn helps up to 0.5% and harms above. The 2017 peak is at about 0.2% Si.
  - **Al–Cu–Mg:** Ti strongly reduces susceptibility. The peak moves from 0.5% Cu at 0.5% Mg to 1.5% Cu at 4% Mg.
  - **6xxx:** maximum at 0.3–0.4% Fe (0.5 Mg–0.5 Si–0.15 Ti). For 6111-type (0.5 Mg, 1.2 Si, 0.2 Fe) the minimum is at 0.7–0.8% Cu. Ti helps.
  - **7xxx:** Cu raises susceptibility, and Mn is harmful. Minimum tearing at 0.005% Ti for 7010 and 0.3% Ti for 7050 (as printed).

### 9.6 Design levers and pitfalls
- **Levers:**
  - Avoid the lean-solute peak of the lambda curve, or add enough eutectic for healing.
  - Keep Fe:Si > 1 and avoid free Si.
  - Prefer fine, compact eutectic intermetallics over coarse, early, plate-like or primary ones.
  - Grain refine, keeping grains dendritic.
  - Limit speed and sump depth, and ramp gently at start-up.
  - A moderately higher melt temperature can help in DC.
- **Inference for 3xxx:** lean Al–Mn–Fe–Si alloys have a narrow freezing range and little eutectic, and sit near 1050 in contraction behaviour (1050 εth ≈ 0.03% [ch5, p.196]). Hot tearing is therefore usually less critical than in 2xxx/7xxx, *unless* Si (free-Si eutectic) or Cu (wider range) is raised, or coarse early α/Al6(FeMn) forms at high Fe + Mn and slow central cooling [ch2, p.46–47; ch5, p.205, 243].
- **Pitfalls:**
  - Composition-ranking criteria (Clyne–Davies, Novikov) do not respond to DC process dynamics.
  - RDG over-predicts tearing [ch5, p.237–239].
  - Porosity and hot tears are inversely related, because tears consume pores. Low porosity in a cracked region does not mean good feeding [ch5, p.268–269].

---

## 10. Porosity, cold cracking, surface and shape defects

- **Porosity** [ch5, p.194–195, 267–269]:
  - Caused by shrinkage plus hydrogen evolution when the mush can neither be fed nor let gas escape.
  - Concentrates in the billet centre.
  - In 200-mm Al–Cu billets it peaks at about 3% Cu (porosity axis 0–0.1%). It rises with speed from 100 to 160 mm/min, then plateaus.
  - At high speed, pores are irregular and lie along solute-rich boundaries; at low speed they are rounder.
  - Above about 3.5% Cu, porosity and tearing both fall (better feeding).
- **Hydrogen** promotes exudation and inverse segregation when trapped in the mush at moderate cooling rates (Masing and Dahl) [ch4, p.127]. Superheat increases gas pick-up [ch2, p.24]. **No hydrogen-solubility data are in the source** (gap).
- **Cold cracking:** only touched on.
  - Early DC of duralumin and Zn-bearing alloys suffered splitting (cold cracks) and hot tears, attributed to the steep surface-to-interior gradient [ch1, p.9].
  - Large 7075-type ingots used *air* secondary cooling until the mid-1950s to cut thermal stress [ch5, p.216].
  - Sub-solidus "cold" cracks may start at locally remelted, intensely deformed zones and resemble hot tears [ch5, p.241–242].
  - Ultrasonically refined non-dendritic ingots had no cold cracks [ch5, p.258].
  - No cold-crack criterion is given (gap).
- **Bleed-out / flashing / butt separation:** the shell is too weak or remelted in the air gap. Cause: casting too hot or insufficient mould cooling. Remedy: lower melt temperature and uniform primary and secondary cooling; GR can promote bleed-out (wider slurry, narrower mush) [ch3, p.120–121].
- **Hang-up:** the section freezes in the mould, which is harmful in hot tops. Remedy: higher melt temperature, lubrication, correct speed [ch3, p.121].
- **Cold folds:** the meniscus freezes in the mould periodically; folds carry oxides and pores. Remedy: higher melt temperature and speed, lower water; EMC and air-slip moulds are less prone [ch3, p.121].
- **Liquation / exudation bands:** air-gap reheating plus metallostatic pressure push eutectic-composition liquid through the shell, giving strong positive surface segregation and periodic bands.
  - Worse with wider freezing range.
  - Remedies: cooler casting, smaller air gap, stronger oxide skin, mould lubrication [ch3, p.121–122; ch4, p.151].
- **Distortions:** butt curl, butt swell and rolling-face pull-in [ch5, p.246–248]. Butt curl reduces stability and contact (safety hazard) [ch5, p.187].

---

## 11. Synthesis for our alloy families (actionable checklist)

Every bullet combines source facts (cited) with **Inference** where it extrapolates to our grades.

1. **3xxx (AA3102/AA3207-type lean Al–Mn–Fe–Si; also 3003/3104)**
   - Phase selection: Al6(FeMn) and Al15(FeMn)3Si2; Si raises the α fraction and lowers the NES (3003: 634 → 589°C from 0.5 to 17 K/s). Free Si at high Si / low Fe drops the solidus to 573°C [ch2, p.46–47].
     **Inference:** specify maximum Si and minimum Fe:Si so the NES stays high and free Si is avoided.
   - Mn stays supersaturated after DC and gives dispersoids on annealing [ch2, p.51]. Its partitioning is mild (K ≈ 0.82) [ch4, p.172].
     **Inference:** the as-cast Mn supersaturation is the main lever for dispersoid-controlled strength, sag resistance and recrystallisation. Higher cooling rate and finer DAS help, so model it with Scheil plus back-diffusion, not equilibrium.
   - Fe (K = 0.03) is the strongest macrosegregant [ch4, p.170–172]. GR with Ti increases centreline segregation in 3104 sheet ingots (0–0.006% Ti), and feeding system choice matters [ch4, p.173–174, 179].
     **Inference:** use the minimum effective TiB2 addition and a flow-reversing (combo-bag type) distributor.
   - Hot tearing: GR benefits shown for 3104 [ch5, p.256]. 3004 semi-solid shows hardening and zero strength at fs = 0.81 [ch5, p.206, 215]. Fine compact Al6Mn + Al3Fe (0.2% Fe in Al–1.5Mn) strengthens the mush [ch5, p.205]. Early coarse α(AlFeMn) is harmful [ch5, p.243].
   - Feathery grains are a risk in lean, hot-cast alloys with high gradients [ch3, p.118–120].
2. **1xxx / 8xxx (Al–Fe–Si)**
   - Metastable Fe phases at DC rates [ch2, p.45–46]; Al6Fe at > 1 K/s [ch2, p.46].
   - Fir-tree zone: control with Fe:Si ≈ 3, traces of Mn/Cr, low-head casting [ch3, p.116–118].
   - 8006: primary Al6(FeMn) and Al3Fe appear only at low cooling rate and high Fe [ch2, p.46].
     **Inference:** the slowly cooled centre of thick ingots sets the Fe + Mn ceiling for avoiding primary intermetallics, which matters for pinholes and rolling defects in foil (general knowledge).
   - Negligible thermal contraction in the freezing range (1050) [ch5, p.196]. Hot tearing is rarely limiting.
3. **5xxx**
   - Very wide non-equilibrium freezing range (5182 NES 470°C), so homogenisation must start below the NES [ch2, p.53].
   - Al–Mg alloys accumulate more contraction than Al–Cu [ch5, p.192]. 5182 contraction in the freezing range is small at 12–18 K/s [ch5, p.196].
   - GR worsens centreline Mg segregation in sheet ingots [ch4, p.173–175].
4. **6xxx**
   - NES 555°C with free Si; the solidus is very sensitive to Si (−25°C within the 6162 range) [ch2, p.47–49].
   - Fe-phase type depends on Mg:Si [ch2, p.47–48].
   - Hot-tear maximum at 0.3–0.4% Fe (6063 type) and Cu optimum at 0.7–0.8% (6111) [ch5, p.220].
5. **Process (all families)**
   - Respect Vcast·D thresholds and sump-slope rules (α < 30–60°) for segregation [ch4, p.152, 158, 161].
   - Ramp start-up gently [ch3, p.86; ch5, p.249–251].
   - Keep nucleate boiling but do not over-water [ch3, p.86–88].
   - Moderate superheat [ch2, p.24; ch5, p.259–262].

---

## 12. Key numbers cheat-sheet

| Quantity | Value | Conditions | Source |
|---|---|---|---|
| DAS–cooling-rate exponent n (d = C·Vc^−n) | 0.2–0.4 (Al alloys); 0.4 DAS, 0.3 grain size (Al–Cu) | — | [ch2, p.24] |
| Default coarsening exponent | 0.33; 0.5 under convection | — | [ch2, p.38] |
| Back-diffusion threshold | α′K ≥ 0.1; α′ ≈ 10⁻² at 0.1–10 K/s | Brody–Flemings | [ch2, p.33] |
| Scheil eutectic, Al–4%Cu | ~8 vol% | — | [ch2, p.31] |
| Superheat to dissolve melt heterogeneities | ~200–250°C | — | [ch2, p.27] |
| Typical Pe, Bi in DC | 1.8–4.5; 1–25 | — | [ch3, p.80] |
| Bi beyond which cooling gains little | ~4 | 2024 billet model | [ch3, p.86] |
| HTC: mould / air gap / impingement / downstream | 1–2.5 / ~0.5 / ~48 / 30–40 kW/m²K | — | [ch3, p.94–96] |
| Nucleate boiling | HTC ~40 kW/m²K; flux up to 6000 kW/m²; surface < 300°C | — | [ch3, p.87] |
| Vs,max (2024) | 103 mm/min (R 97.5 mm); 54 mm/min (R 185 mm) | Eq. 3.6 | [ch3, p.93] |
| Cooling rate, 200-mm billet | centre 3–5 K/s; periphery 15–20 K/s | — | [ch3, p.113] |
| Ramp rate for no sump lag | 11.32 mm/min² (vs 113.2 lagging) | 200 mm Al–4Cu | [ch3, p.86] |
| Feathery-grain risk | cooling rate > 10 K/s, high G, flow | — | [ch3, p.118] |
| Fir-tree metastables | AlmFe/α″ need ~20 K/s; Al6Fe/AlxFe/α at 2–5 K/s | 1xxx, 5xxx | [ch3, p.116] |
| Fe:Si targets | > 1 (avoid free-Si eutectic); ≈ 3 (against fir-tree) | — | [ch2, p.46; ch3, p.118; ch5, p.208] |
| Max secondary Fe-phase fraction | 0.1–0.2 vol% | Low Fe solubility | [ch2, p.46] |
| NES: 1050 / 3003 / 6063 / 5182 / 2024 / 7075 | 630–642 / 589–634 / 576 / 470 / 480–486 / 466–469°C | See §4.1 | [ch2, p.46–56] |
| NES of Al–Fe–Si and 6xxx with free Si | 576°C; 555°C | — | [ch2, p.45, 47] |
| Partition coefficients K | Fe 0.03, Si 0.13, Cu 0.17, Mg 0.43, Zn 0.45, Mn 0.82, Ti 9.0, Cr 2.0 | Table 4.9 | [ch4, p.172] |
| Growth restriction Q | Ti ≈ 35 at 0.15%; Sc 2.5 at 0.6% | — | [ch2, p.65] |
| Undercooling parameter P | Sc 5; Ti 4.4 | — | [ch2, p.65] |
| Ti from Al–Ti–B in practice | 0.001–0.005% (total Ti < 0.05%) | — | [ch2, p.65, 72–73] |
| Coherency fs with GR | 0.23 → 0.45 (Al–4Cu + 0.05% Ti) | — | [ch4, p.172] |
| Rigidity fs with GR | 0.75 → 0.82 (2024) | — | [ch4, p.172] |
| Kozeny–Carman | kKC = 5; valid 0.6 < fs < 0.9 | — | [ch4, p.133, 136] |
| Shrinkage-flow velocity | ~10⁻⁴ m/s | vs Vcast 100–200 mm/min | [ch4, p.143] |
| Solidification shrinkage β | 6–8 vol% (Al alloys); model 0.1; Al–4Cu up to 0.117 | — | [ch5, p.186; ch4, p.155] |
| Sump slope for acceptable macrosegregation | < 30° negligible; < 60° acceptable | — | [ch4, p.158] |
| Billet speed limit | Vcast ≤ (25,000–33,300)/D mm/min | D in mm | [ch4, p.152] |
| Positive/negative centreline threshold | Vcast·D ≈ 12,465 (non-GR), 21,774 (GR) mm²/min; Livanov a ≈ 12,000 | — | [ch4, p.161] |
| Thermal strain causing deformation-driven segregation | ~2% volumetric | — | [ch4, p.151] |
| Hot-tear vulnerable range | fs > 0.9 (85–95%); most vulnerable 90–95% | — | [ch5, p.185, 241] |
| Coherency fs range | 0.25–0.6 | Morphology dependent | [ch5, p.183] |
| Dihedral angle in Al alloys | < 20–25°; 1% liquid wets ~30% of GBs, 10% wets ~85% | — | [ch5, p.212] |
| Contraction in freezing range: 1050 / 2024 / 5182 / 6082 / 7075 | 0.03 / 0.2 / 0 / 0.02 / 0.27% | 12–18 K/s | [ch5, p.196] |
| LTEC near solidus (as-cast) | Al–Cu 30 → 28.5; Al–Mg 29 → 25.5 ×10⁻⁶ K⁻¹ | — | [ch5, p.199–200] |
| RDG critical pressure drop | 2 kPa (Al–1.4%Cu) | — | [ch5, p.234] |
| Peak DC hot tearing, Al–Cu | 0.5–1.5% Cu; none > 4% Cu | 200 mm, ≤ 220 mm/min | [ch5, p.253] |
| GR grain-size window vs hot tearing | Dendritic GR beneficial; cellular < 50 µm may worsen; > 100 µm fine is better | — | [ch5, p.258] |
| Hydrogen after long holding | 0.30 → 0.19 cm³/100 g | 2037 melt, 10 h | [ch5, p.214] |
| Zr/Sc solubility in (Al) | 0.06 Zr + 0.03 Sc (550°C); 0.09 Zr + 0.06 Sc (600°C) | — | [ch2, p.68] |

---

## 13. Open questions and gaps

1. **Missing chapter:** *Concluding Remarks* (p. 275, `62816_CH06.pdf`) is referenced but absent from Drive. Ask the user whether it exists.
2. **No liquidus slopes (m) and no Q table for Mn, Fe, Si, Mg, Cu, Zn, Cr, Zr.** Only K values (Table 4.9) and Q for Ti and Sc are given. To compute Q = Σ m·(K − 1)·C for AA3102/AA3207 we need an m/K table, e.g. Easton and StJohn or CALPHAD (general knowledge). Do not reuse binary K values blindly in multicomponent 3xxx.
3. **No quantitative transition-metal supersaturation (Mn, Fe, Cr, Zr, Sc) vs cooling rate.** Neither is there dispersoid-precipitation or homogenisation kinetics. These must come from other sources, such as Belov et al. *Iron in Aluminum Alloys* (cited [ch2, ref 31]), 3xxx homogenisation literature, or Alstruc-type models (mentioned [ch2, p.33]).
4. **No hydrogen-solubility data, and no gas-porosity model beyond qualitative statements.** Porosity data are for Al–Cu billets only [ch5, p.267–269].
5. **Cold-cracking criteria and residual-stress data** are essentially absent; there are only historical remarks.
6. **No coverage of twin-roll / continuous casting and rolling.** The cooling-rate ranges given (0.1–20 K/s in DC) do not include strip-casting rates, so extrapolating the phase-selection data to CC&R is unverified.
7. **No 3xxx-specific DC data** beyond 3003 reaction temperatures, 3004 semi-solid behaviour and 3104 macrosegregation/hot-tear observations. Nothing exists for AA3102/AA3207 compositions.
8. **Extraction artefacts to verify against the PDF before quantitative use:**
   - Eq. 4.8 (columnar permeability).
   - Eqs. 4.18–4.19 (lever-rule CL with shrinkage correction).
   - Eqs. 5.9, 5.10, 5.16 and 5.27 (exponents and symbols).
   - Units in Table 3.1.
   - Several values in Tables 2.2, 2.7 and 2.8.
   - The 7075 "435–445°C" statement [ch2, p.56].
   - Table 4.8 normalised sump depth for 60 mm/min / 200 mm (printed 0.47; 88/100 would be 0.88).
   - The 7050 "0.3% Ti" optimum [ch5, p.220].
9. **Figure-only data were not recoverable**, e.g. Fig. 1.5 DAS vs solidification rate, Fig. 2.3 grain size and DAS vs cooling rate for Al–Cu, Fig. 3.19/3.23 radial grain-size and DAS profiles, and Fig. 2.19 Al–Mg–Mn liquidus and solidus isotherms. Digitise them from the PDFs if the model needs them.
10. **Unresolved physics flagged by the author:**
    - The cause of the eutectic-fraction minimum at the billet centre [ch3, p.113].
    - The coarsening-exponent dependence on cooling rate and convection [ch2, p.38].
    - Ranking of the macrosegregation mechanisms (floating grains vs shrinkage vs convection) [ch4, p.150, 179].
    - Hot-crack nucleation mechanisms [ch5, p.240, 244].
    - A DC-robust hot-tearing criterion with reliable mush properties (E, γ, K) [ch5, p.239].
