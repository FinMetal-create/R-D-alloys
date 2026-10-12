# R-D-alloys

A physical-metallurgy knowledge base for alloy R&D, aimed at designing alloys with the best achievable
combination of properties. The current focus is lean Al–Mn (3xxx) and 1xxx alloys processed into
impact-extrusion slugs for aerosol cans.

Built on 2026-10-12 from the user's Google Drive literature library (79 unique sources), their own R&D files,
and online research. Each chapter cites its sources (Drive links, URLs or DOIs) and marks inferences and
general knowledge explicitly.

## Start here

- [`knowledge/00-alloy-design-framework.md`](knowledge/00-alloy-design-framework.md) is the synthesis.
  It covers requirements, a mechanism map per process stage, the element playbook, quantitative rules of
  thumb with evidence grades, an assessment of the in-house alloys and models, ranked development
  hypotheses, and a calibration plan.
- [`CLAUDE.md`](CLAUDE.md) gives the working rules for AI-assisted work in this repo.

## Chapters

| # | Chapter | Basis |
|---|---|---|
| 01 | [Solidification and DC casting](knowledge/01-solidification-and-dc-casting.md) | Drive (Eskin) |
| 02 | [Intermetallics, phase diagrams, casting defects](knowledge/02-intermetallics-phase-diagrams-and-casting-defects.md) | Drive |
| 03 | [Recovery, recrystallisation, grain growth](knowledge/03-recovery-recrystallization-grain-growth.md) | Drive (Humphreys & Hatherly and others) |
| 04 | [Precipitation, dispersoids, alloying elements](knowledge/04-precipitation-dispersoids-and-alloying-elements.md) | Drive |
| 05 | [Aluminium alloy systems and tempers](knowledge/05-aluminium-alloy-systems-and-tempers.md) | Drive (Polmear, Davis, Kaufman) |
| 06 | [Aluminium properties, processing, applications](knowledge/06-aluminium-properties-processing-and-applications.md) | Drive (Totten, Ryen, TALAT) |
| 07 | [Thermomechanical processing: rolling, extrusion](knowledge/07-thermomechanical-processing-rolling-extrusion.md) | Drive |
| 08 | [Other alloy families and transferable principles](knowledge/08-other-alloy-families-and-general-principles.md) | Drive |
| 09 | [In-house R&D data](knowledge/09-in-house-rd-data.md) | User's own files |
| 10 | [Impact extrusion and slug metallurgy](knowledge/10-impact-extrusion-and-slug-metallurgy.md) | Drive (Sillekens, Ryen) |
| 11 | [Aerosol-can slugs: industry and specifications](knowledge/11-web-aerosol-can-slugs-industry-and-specs.md) | Web (snippet level) |
| 12 | [3xxx homogenisation, dispersoids, recrystallisation](knowledge/12-web-3xxx-homogenisation-dispersoids-recrystallisation.md) | Web (abstract level) |
| 13 | [Model-ready data: constitutive, diffusion, resistivity](knowledge/13-web-model-ready-data-constitutive-diffusion-resistivity.md) | Web (partial) |
| 14 | [MgO oxidation during annealing](knowledge/14-web-annealing-oxidation-mgo.md) | Web (abstract level) |
| 15 | [Continuous casting of strip](knowledge/15-web-continuous-casting-of-strip.md) | Web (abstract level) |
| 16 | [Recycling, CBAM, sustainable alloy design](knowledge/16-web-recycling-cbam-sustainable-alloy-design.md) | Web (snippet level) |
| 17 | [Standards: compositions and properties](knowledge/17-web-standards-compositions-and-properties.md) | Web (partial) |
| 18 | [Computational alloy-design tools](knowledge/18-web-computational-alloy-design-tools.md) | Web |
| — | [Source catalogue](knowledge/sources/catalog.md) | Drive inventory (S-001…S-079, W-01…W-24) |

## Known limitations

- **Web chapters (11–18)** were written while the environment's network policy blocked publisher sites, so
  they rest on abstracts and search snippets. Each chapter lists the documents to fetch to verify its claims.
- **Large Drive books** (above ≈ 10 MB) were only partly readable through the Drive connector. The
  chapters record exactly how far each text went.
- The `microstructure-sim` code stored in Drive is intentionally not part of this repository.
