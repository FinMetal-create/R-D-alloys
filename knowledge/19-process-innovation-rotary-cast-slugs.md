# 19 — Process innovation for rotary-cast slug alloys

**Purpose.** This chapter proposes process changes that let the plant make **stronger** alloys that still
**impact-extrude well**, on the user's route. It includes the option of building homogenisation into the
anneal.

**Route (user, 2026-10-12):** rotary (wheel-type) strip caster → **22 mm cast strip** → **in-line hot rolling,
≥ 50 % reduction** → **cooling bath (quench)** → **cold rolling (CRM) 30–50 %** → slugs (≈ 6.1–7.4 mm) → slug
anneal → impact extrusion → lacquer bake **220 °C / 10 min**.

**Evidence grades:** as in ch00.
- **D**: Drive literature, full text.
- **W**: web, abstract or snippet level.
- **I**: in-house data.
- **G**: derived or general knowledge.

Every proposal is a hypothesis to trial, not a validated result. The kinetic numbers in §1 are
order-of-magnitude estimates.

---

## 1. Kinetic facts that decide what is possible

### 1.1 What the slug anneal can and cannot do (G)

Mn diffusivity is anchored at D(500 °C) = 5×10⁻¹³ cm²/s [ch05 §4.2; ch07 §10]. The activation energy Q is
taken as 182–227 kJ/mol, the range implied in [ch13]. Homogenisation relaxation time is τ = l²/(π²D)
[ch07 H8], with l = half the dendrite-cell spacing.

**Mn diffusion distance √(Dt)** (Q = 200 kJ/mol; the full range of Q changes it by about ±30 %):

| T (°C) | 10 min | 1 h | 4 h |
|---|---|---|---|
| 220 (lacquer bake) | ≈ 0 | ≈ 0 | ≈ 0 |
| 350 | 0.004 µm | 0.010 µm | 0.020 µm |
| 400 | 0.017 µm | 0.042 µm | 0.084 µm |
| 450 | 0.06 µm | 0.15 µm | 0.29 µm |
| 500 | 0.17 µm | 0.42 µm | 0.85 µm |
| 550 | 0.45 µm | 1.1 µm | 2.2 µm |
| 600 | 1.0 µm | 2.5 µm | 5.0 µm |
| 620 | 1.4 µm | 3.4 µm | 6.9 µm |

**Time to remove Mn microsegregation, τ, for cell half-spacing l** (hours; Q range 182–227 kJ/mol):

| T (°C) | l = 5 µm | l = 10 µm |
|---|---|---|
| 450 | ≈ 100–160 h | ≈ 400–650 h |
| 500 | ≈ 14 h | ≈ 56 h |
| 550 | ≈ 1.7–2.5 h | ≈ 6.6–10 h |
| 580 | ≈ 0.5–1.0 h | ≈ 2–4 h |
| 600 | ≈ 0.25–0.55 h | ≈ 1–2.2 h |
| 620 | ≈ 0.12–0.3 h | ≈ 0.5–1.3 h |

**Consequences**
1. **At normal slug-anneal temperatures (350–420 °C), Mn cannot homogenise.** It only moves tens of
   nanometres per hour. That is enough to **nucleate fine dispersoids on the deformation substructure**,
   which is exactly the "precipitation before RX → slow RX, coarse pancake grains" problem of rotary-cast,
   non-homogenised strip [ch03 §5.2; ch15 §3].
2. **Real homogenisation needs ≈ 580–620 °C for ≈ 0.5–4 h,** depending on the cell spacing. The rotary
   caster's faster cooling gives finer cells than DC (DC 30–70 µm, belt/twin-roll 5–10 µm [ch03 §5.1]), which
   makes this short.
   - **Gap:** the cell size of the 22 mm rotary-cast strip has not been measured. It is the single most
     useful number for this chapter.
3. **Precipitation without homogenisation** happens at ≈ 450–520 °C on a timescale of hours (diffusion
   distances 0.1–1 µm vs dispersoid spacing of order 0.1–0.5 µm) (G).
4. **During the 220 °C / 10 min bake** Mn is frozen. Mg and Si still move ≈ 30–45 nm (Q = 117–126 kJ/mol,
   D(500 °C) = 10⁻⁹ cm²/s [ch05 §4.2]). That is enough for **strain-ageing (solute atmospheres on
   dislocations) and cluster formation** in the heavily worked can wall (G).

### 1.2 Equilibrium targets
- **Mn solubility** is only 0.06 / 0.15 / 0.25 % at 400 / 450 / 500 °C [ch02, Belov]. With Fe and Si
  present it is lower still [ch04 §0].
  - Rotary-cast strip keeps most of its Mn in solution. A 3207 (Mn ≈ 0.45) is therefore strongly
    supersaturated at every anneal temperature.
  - A modified 3102 (Mn 1.1–1.3) is far more so.
- **Fe** is essentially all in constituent particles (solubility 0.002–0.016 % at 400–550 °C [ch02]). Those
  particles are the PSN sites that give fine, equiaxed grains [ch03 §3].

### 1.3 What the actual line does to the metal (Inference + G)

**Strain budget** (ε = ln(h₀/h)):

| Step | Gauge | Reduction | ε | Fate of the strain |
|---|---|---|---|---|
| Hot rolling, straight after casting | 22 → ≤ 11 mm | ≥ 50 % | ≥ 0.69 | Mostly lost to dynamic recovery at hot-rolling temperature; it leaves a recovered subgrain structure [ch03 §9] |
| Cooling bath | ≈ 11 mm | — | — | **Quench** freezes the state: Mn, Mg, Si (and Fe traces) stay supersaturated, and no precipitation or self-annealing happens in the coil |
| Cold rolling | ≤ 11 → 6.1–7.4 mm (slugs, ch09 §8) | 33–45 % (range 30–50 %) | 0.40–0.59 (0.36–0.69) | This is the stored energy that drives slug RX |

**Consequences**
1. **The slug anneal starts from a fully supersaturated, only moderately cold-worked state.** That is the
   least favourable combination for Mn-bearing alloys: precipitation can win the race against RX, giving coarse
   grains [ch03 §5].
2. **The cold strain is below the in-house CRM-table targets** (ε ≥ 0.80–0.85 [ch09 §5]). Expect coarser,
   more variable grains and higher anneal temperatures (so more MgO) than the tables predict.
   - The RX grain size falls with strain, and ≈ 15 % is the critical strain [ch03 §4.4; ch06].
   - At low strain, fewer constituent particles act as PSN nuclei: the critical particle size grows as stored
     energy falls (general knowledge; HH ch. 9 not extracted [ch03 §12]).
3. **The quench is a design variable.**
   - Slow cooling or hot coiling instead would let Mn (and Mg₂Si) precipitate in the coil, using the casting
     heat (P2).
   - For Mg–Si alloys like T11, the quench keeps Mg and Si in solution. That helps bake response but makes
     slug hardness sensitive to the anneal cooling rate and to storage time [trials/T11 §2.3].

---

## 2. Innovation options, ranked

Ranking is expected benefit per unit of risk and capex (inference).

### P10 — Rebalance reduction: less hot, more cold ★ quickest lever (no new equipment if the mill allows it)

- **What.** Lower the hot reduction so that the cold mill gives ε ≥ 0.80–0.85, the in-house CRM-table targets
  [ch09 §5]. For 6.1–7.4 mm slugs the tables give hot-band gauges of ≈ 13.6–17.3 mm, i.e. 21–38 % hot
  reduction instead of ≥ 50 %.
- **Mechanism.** More cold stored energy gives:
  - more nuclei (PSN on Fe constituents, plus boundary nucleation);
  - finer, more equiaxed RX grains;
  - lower RX temperature and time, so less MgO and less time for Mn to precipitate before RX
  [ch03 §1, §4.4, §5.4].
- **Feasibility (user, 2026-10-12):** the hot/cold split is **flexible** and is set per order by the
  customer's final thickness. So P10 needs no new equipment, only a rule for choosing the split.
- **Rule** (the in-house CRM-table logic [ch09 §5.2]): hot-band gauge h_HB = t_final × e^(ε_target), capped at
  22 mm. The cold mill then delivers exactly ε_target.

  | Slug t_final (mm) | ε 0.80 (3102-type): h_HB / hot % / cold % | ε 0.85 (3207-type) | ε 0.90 (1xxx/T11-type, inference) |
  |---|---|---|---|
  | 5.5 | 12.2 / 44 % / 55 % | 12.9 / 42 % / 57 % | 13.5 / 39 % / 59 % |
  | 6.1 | 13.6 / 38 % / 55 % | 14.3 / 35 % / 57 % | 15.0 / 32 % / 59 % |
  | 6.6 | 14.7 / 33 % / 55 % | 15.4 / 30 % / 57 % | 16.2 / 26 % / 59 % |
  | 7.4 | 16.5 / 25 % / 55 % | 17.3 / 21 % / 57 % | 18.2 / 17 % / 59 % |
  | 8.0 | 17.8 / 19 % / 55 % | 18.7 / 15 % / 57 % | 19.7 / 11 % / 59 % |
  | 9.0 | 20.0 / 9 % / 55 % | 21.1 / 4 % / 57 % | 22 (cap) / 0 % / 59 % |
  | 10.0 | 22 (cap): cold 54.5 %, ε 0.79, below the 0.85–0.90 targets | | |

  *(derived)*
- **Caveat: minimum hot reduction.** For thick slugs (≥ ≈ 8 mm) the rule leaves < 20 % hot reduction. Some hot
  work is needed to break up the cast structure and close casting porosity. The required minimum for this caster
  is not in the knowledge base; this may be where the "≥ 50 %" habit comes from. Find it by trial: blister and
  porosity checks, and grain uniformity.
  - Related data point: ≥ 40 % cold reduction of as-cast DC ingot eliminated blisters [ch02 §7].
  - Where the cap or the hot-work minimum prevents ε_target, compensate with P1/P5 (Mn out before cold
    rolling) and P3/P4 (fast heating).
- **Other constraints.** Cold-mill load and strip hardness rise with more cold reduction.
  - Higher cold reduction also raises cold-mill load and strip hardness.
- **If the hot reduction cannot be lowered for a given order:**
  - (a) finish hot rolling **cooler** (warm) before the quench, so part of the hot strain is retained as stored
    energy (general knowledge; verify);
  - (b) make thinner slugs where the product allows;
  - (c) compensate with P3/P4 (fast heating) and P1.
- **Trial.** At one slug gauge, compare the current split (≥ 50 % hot / ≈ 35–45 % cold) with ≈ 30 % hot /
  ≈ 55–60 % cold. Measure grain size and scatter, HB, anneal temperature needed, and MgO.

### P1 — High-temperature treatment of the hot band before cold rolling ("at-gauge homogenisation") ★ highest metallurgical value

- **What.** Batch-anneal the quenched **hot-band coil (≈ 11–17 mm)** at ≈ 580–620 °C for ≈ 1–4 h (§1.1).
  The thinner hot band heats faster than the 22 mm cast strip. Then cool **slowly or in
  steps** through ≈ 550 → 450 °C so the Mn precipitates as fewer, coarser dispersoids. Then cold roll and
  anneal the slugs as now, or shorter.
- **Mechanism.**
  - Removes Mn supersaturation and microsegregation before deformation.
  - Coarsens dispersoids, giving low Zener drag.
  - Spheroidises and, with Si, converts constituents (Al₆ → α), giving more effective PSN sites and better
    ductility at the can base corner.
  - Sources: [ch03 §5.4 table, "fine equiaxed" route]; [ch06 §6] (AA3103 stepped cooling: Mn_ss 0.40 → 0.15
    at %); [ch10 §5].
- **Evidence.** In twin-roll-cast 3105, homogenised strip recrystallised at a **lower** temperature with
  finer, quasi-equiaxed grains by PSN. The non-homogenised strip showed sluggish RX and very coarse grains;
  440 °C did worse than high-T treatment [ch15 §3] (W). The DC analogue is well established [ch03 §5.4] (D).
- **Expected effect.**
  - The slug anneal becomes fast and low-T (less MgO, shorter cycles), with fine equiaxed grains.
  - **Higher Mn alloys (e.g. modified 3102) become workable**, because their extra Mn no longer slows the
    slug anneal. This is the route to "stronger and still extrudable".
- **Costs and risks.**
  - Energy and time. A 22 mm coil heats far faster than a DC ingot, but it is still a coil-scale batch.
  - Surface oxide forms at 600 °C: use a protective atmosphere, or rely on the following cold reduction to
    break it up. Check surface quality.
  - Danger of incipient melting if Si is high: the solidus can fall towards ≈ 573–590 °C with free Si
    [ch01 §11; ch02].
  - Lower Mn_ss means slightly lower slug strength. Compensate with Mg or Cu (P6).
- **Trial.**
  - As-cast vs 600 °C / 2 h + 20 °C/h to 450 °C vs 550 °C / 4 h.
  - Measure conductivity (Mn_ss proxy [ch13]), HB, and grain size after the standard slug anneal.

### P2 — Replace or shorten the cooling-bath quench: hot coiling plus controlled coil cooling ("free" precipitation)

- **What.** The line currently quenches the hot band in a cooling bath, which preserves full supersaturation
  (§1.3). For Mn-bearing alloys:
  - bypass or shorten the bath;
  - coil hot (≈ 450–520 °C if the hot-mill exit allows);
  - cool the coil slowly under an insulated hood or in a holding furnace.

  For Mg–Si alloys (T11), keep the quench if bake response is wanted, or use slow cooling for soft, stable
  slugs.
- **Mechanism.** Precipitates a large part of the Mn supersaturation (diffusion distance 0.15–0.85 µm in
  1–4 h, §1.1) using heat already in the metal. It does not fully homogenise. This is a cheap partial version
  of P1 (G; analogous to self-annealing of hot-rolled coils).
- **Needs.** The strip or coil temperature at the caster or in-line mill exit. **Unknown: please provide.**
- **Risk.** Precipitation at too low a temperature gives a fine, dense dispersion (strong Zener drag). Aim for
  ≥ 480–500 °C, and test.
- **Trial.** Simulate in a lab furnace on as-cast strip with 3 cooling profiles. Compare with P1 after the
  standard slug anneal.

### P3 — Two-stage slug anneal: "recrystallise first, precipitate second"

- **What.**
  1. **Fast** heating, which needs P4 equipment or a pre-heated furnace with loose slugs, to ≈ 450–520 °C.
     Recrystallisation then completes before Mn can precipitate on the deformation substructure.
  2. A hold at ≈ 420–480 °C to precipitate Mn **inside the new grains**.
  3. Cool.
- **Mechanism.** It goes past the nose of the precipitation C-curve during heating. That gives RX-first
  sequencing with fine equiaxed grains [ch03 §5.2, R10]. The hold then lowers Mn_ss (softer, stable slug),
  and the new dispersoids limit grain growth.
- **Evidence.**
  - Fast heating (≈ 50 °C/s) gives fine equiaxed grains; ≤ 3 °C/s gives coarse grains in CC 3xxx [ch15 §3]
    (W).
  - AA3103: fully RX in 45 s at 400 °C with no Mn precipitation [ch03 §4.3] (D).
- **Risk.**
  - Batch furnaces with packed slugs cannot heat fast.
  - Higher peak temperature raises MgO, so keep the time short and use atmosphere control (P8).

### P4 — Fast continuous slug annealing (mesh belt, induction, infrared or fluidised bed)

- **What.** Replace hours of batch annealing with minutes in a continuous furnace. This decouples
  temperature from time.
- **Evidence.**
  - Ball moved its ReAl slugs to a **continuous multi-zone mesh-belt furnace** (peak metal temperature
    ≈ 450–570 °C). The stated reasons were uniform equiaxed grains and less abrasive MgO. Its batch practice
    was ≈ 470–600 °C for 5–9 h [ch11 §2] (W).
  - Heating rate controls grain size in 3xxx [ch12; ch15] (W).
- **Fit.** P4 is the hardware that makes P3 possible. Induction and fluidised beds give the highest heating
  rates and uniformity for small parts (G).
- **Risk.** Capex. Slug-to-slug uniformity must be proven.

### P5 — Hot-band or intermediate anneal (lower-capex alternative to P1)

- **What.** The simplest form on this line: anneal the **quenched hot band** at ≈ 450–520 °C to precipitate Mn
  before cold rolling. With only 30–50 % cold reduction available, a true intermediate anneal between cold
  passes is hard to fit. The original variant: cold roll to an intermediate gauge. Anneal at ≈ 450–520 °C to recrystallise and precipitate
  Mn on a refined structure. Then do the final cold rolling and a fast slug anneal.
- **Mechanism.** Precipitation is faster on the deformed structure. After the intermediate anneal, Mn_ss is
  lower and the dispersoids are already formed, so the final anneal recrystallises quickly [ch03 §5.2] (D).
  This is the classic route for continuously cast strip that is not homogenised [ch15 §3] (W).
- **Trade-off.**
  - It does not remove microsegregation, unlike P1.
  - It uses up part of the total cold reduction, so check the final strain stays above the ≈ 15 % critical
    strain [ch06] and above the in-house CRM ε targets [ch09 §5].

### P6 — Make the 220 °C / 10 min bake work for you

- **What.** Keep some **Mg (and a little Cu and Si) in solid solution** in the slug, so the bake causes
  **strain ageing and clustering** in the heavily worked wall. That would offset recovery softening, or even
  harden the wall.
- **Mechanism.**
  - Mg and Cu pin dislocations by strain ageing [ch05 §6, Davis].
  - Mg and Si move ≈ 30–45 nm in the bake (§1.1).
  - Mg also gives the most wall strength per unit of press force [ch10 §8].
- **Alternative.** A dispersoid route (Zr, or fine Mn dispersoids) pins the wall substructure during the bake
  [ch11 §1.2]. Check the Talum EP 3075875 claims first.
- **Evidence.** Mechanism-level only (G). The known industrial target is reducing cure softening of up to
  ≈ 15 % [ch11].
- **Trial.** Cold roll strip of candidate alloys to ε ≥ 2 to mimic the can wall. Bake at 220 °C for 10 min.
  Measure HV or tensile before and after.

### P7 — Alloy–process co-design enabled by P1, P2 and P5

Once Mn precipitation is moved upstream:
- higher Mn (≈ 0.8–1.2 %) and modest Mg (≈ 0.2–0.4 %) become workable without slow, coarse slug RX;
- Fe from scrap is better tolerated, because constituents are spheroidised and converted to α at 580–620 °C;
- the fast-cooled cast structure already refines the constituents [ch16 §5].

This is the combination most likely to give "stronger, extrudable, rotary-castable" (Inference).

Check against each candidate:
- castability on the caster (freezing range, hot tearing [ch01 §9]);
- registered designation windows [ch17];
- patent windows [ch11; ch16].

### P8 — Surface and atmosphere control (MgO, hydrogen, blisters)

- Anneal **degreased** slugs in a **dry, low-O₂** atmosphere.
  - Inert gas needs O₂ below a few hundred ppm [ch14] (W).
  - Hydrogen from moisture and hydrocarbons feeds blisters [ch02 §7] (D).
- P1 and P4 move time at temperature away from the finished slug surface, which further reduces MgO.

### P9 — In-line conductivity as a process-control signal (quick win)

- Eddy-current conductivity on cast coils, strip and slugs tracks **Mn in solid solution**: Mn has a large
  resistivity increment in solution and a small one out of it [ch13; ch03 §5.2].
- It is cheap and fast, and gives a direct read-out of whether P1, P2 or P5 worked and of where a coil sits on
  the precipitation curve before annealing.
- It can also feed the self-improving model loop (ch00 §8; ch18).

---

## 3. Recommended first trial matrix (lab scale)

| Factor | Levels |
|---|---|
| Alloy | current 3207-type; strong-lean (+Mg 0.25–0.40, Cu ≈ 0.1); modified 3102 (Mn 1.1–1.3) |
| Hot/cold split (P10) | current (≥ 50 % hot / ≈ 35–45 % cold); shifted (≈ 25–35 % hot / ≈ 55–60 % cold) at the same slug gauge |
| Hot-band treatment before cold rolling | quenched (current); P2 simulation (slow cool from ≈ 500 °C instead of the bath); P1 (600 °C / 2 h + stepped cool); P5 (hot-band anneal 450–520 °C) |
| Slug anneal | current batch cycle; fast two-stage (P3) in a pre-heated furnace or salt or fluidised bath |
| Responses | conductivity; HB; RX fraction and grain size (EBSD or optical); MgO (colour or abrasion, XPS on a subset); wall simulation (ε ≥ 2 + 220 °C / 10 min) HV; later, press force and burst on real cans |

Start with two cheap comparisons on the current alloy:
- **P10:** the current hot/cold split vs more cold reduction.
- **P1/P5:** quenched hot band vs annealed hot band.

Together they test the two core hypotheses: more cold strain, and Mn precipitated before cold rolling, make
the slug anneal fast and fine.

---

## 4. Open questions for the user

1. Strip temperature entering and leaving the hot mill, and the temperature after the cooling bath (needed for
   P2 and P10). *(Route confirmed by the user: 22 mm → hot ≥ 50 % → cooling bath → cold 30–50 %.)*
2. Why is ≥ 50 % hot reduction a minimum? Could the hot/cold split be shifted towards ≈ 25–35 % hot and
   ≈ 55–60 % cold for 6–7.5 mm slugs (P10)?
3. Available equipment: coil batch furnaces (maximum T, atmosphere), slug furnaces (batch or continuous,
   heating rate).
4. A measured cell or dendrite spacing of the 22 mm cast strip, at the surface and centre (sets the P1 time,
   §1.1).
5. Quantitative "stronger" target: burst-pressure gain, or wall-thickness reduction.
