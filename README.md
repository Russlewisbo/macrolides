# Macrolides, Ketolides, and Clindamycin — Lecture Package

Quarto lecture package for ID fellows, University of Padova. Built from the Mandell *Macrolides and Clindamycin* chapter (Nesbitt, Pritchard, Aronoff) using the lecture-builder skill on 2026-06-24.

## Contents

- **`macrolides-slides.qmd`** — RevealJS slide deck. 84 slides total (12 section dividers + 72 content slides). Sized for ~1.5 hours of lecture time.
- **`macrolides-webpage.qmd`** — HTML companion document expanding each slide topic into prose, with full tables and rendered references.
- **`macrolides-references.bib`** — 491 BibTeX entries auto-extracted from the chapter reference list (ref #228 is a placeholder — the only entry missed by text extraction). Each entry's `note` field flags the chapter ref number and any unparsed fields.
- **`macrolides-images/`** — `DMM_newlogo.png` for slide branding. No content figures extracted from the source PDF; if the lecture needs illustrations (ribosome binding diagram, MLS~B~ mechanism, D-test photo), add them here and reference from the slides.
- **`diagnostic-microbiology-and-infectious-disease.csl`** — Russ's standard CSL for both documents.
- **`custom.scss`** — UniPD-branded RevealJS theme.
- **`_extensions/fontawesome/`** — Font Awesome extension for `{{< fa ... >}}` shortcodes (not used in current draft but available).

## Slide structure (12 sections, 84 slides)

1. **Chemistry & Mechanism** — title, outline, family overview, MOA, static vs. cidal
2. **Resistance Mechanisms** — *erm*, MLS~B~, inducible vs. constitutive, D-test, efflux, ribosomal mutations, geographic variation
3. **Pharmacology** — erythromycin, clarithromycin, azithromycin in depth + comparative table + statin interaction + pregnancy
4. **Cardiac Safety** — mechanism, Ray 2004 / Ray 2012 / Albert 2014, risk stratification, allergy
5. **Spectrum** — TB intrinsic resistance, less-common pathogens, geographic resistance, Italian pneumococcal picture
6. **Clinical Uses — Respiratory** — CAP, atypicals, pertussis, MAC, panbronchiolitis, COPD/CF (Albert 2011), Mycoplasma resistance
7. **Clinical Uses — Non-Respiratory** — *H. pylori*, chlamydia (Geisler/Lau), trachoma, MORDOR, gonorrhea, toxoplasmosis, babesiosis, syphilis
8. **Macrolide Immunomodulation**
9. **Ketolides** — telithromycin, solithromycin, lefamulin parallel, newer pipeline
10. **Clindamycin Pharmacology** — origins, PK, spectrum, resistance, *C. difficile*
11. **Clindamycin Clinical Uses** — anaerobes, aspiration, CA-MRSA SSTI, Eagle effect, invasive GAS / TSS, *C. perfringens*, bone/joint, PCP, toxoplasmosis, BV, malaria, severe babesiosis
12. **Practical Pearls** — three summary slides + closing, plus COVID-19 caution and stewardship slides

## Validation results

- BibTeX: all 491 entries parse cleanly via `bibtexparser`.
- YAML: both documents have valid YAML headers.
- All 58 slide citation keys and all 56 webpage citation keys resolve to bib entries (no missing references).
- All slide cross-references resolve to declared labels.
- All 72 content slides have `<br>` immediately below the H2 heading (per skill convention).
- 62 of 72 content slides carry speaker notes; 39 evidence slides carry `::: aside [@key] :::` citations.

## What was NOT done (open items)

- **No Quarto render verification** — sandbox lacks `quarto`. Validation is structural (YAML, BibTeX, key resolution, cross-refs). First render in RStudio recommended before lecture delivery; expect minor cosmetic tweaks.
- **No figures extracted** from the source PDF. The chapter has two important tables (28.1: organism MICs across macrolides; 28.2: erythromycin formulations) — Table 28.2 is included in the webpage as an HTML table; Table 28.1 is summarized prose in the resistance section but could be added in full if you want it on a slide.
- **Reference verification via PubMed** was not performed for individual entries — the volume (491) precluded one-by-one verification. The `note` field flags any unparsed metadata for each entry. Spot-check the high-value citations (Ray 2004/2012, MORDOR, Geisler 2015, Lau 2021, Stevens 2007, IDSA guidelines) before publishing for editorial use.
- **SCSS theme** is the standard `custom.scss` from the Robot Assistant root. If you want different colors for this lecture, edit the SCSS and re-render.

## Lecture output convention note

Per the open question in the Robot Assistant File Naming Conventions section of CLAUDE.md (still pending decision as of this build), this lecture is placed under `Lectures/macrolides/` following the pattern of the phage-therapy build rather than at workspace root. When the convention is resolved one way or the other, this folder should be moved consistently.

## Source

Nesbitt WJ, Pritchard HA, Aronoff DM. *Macrolides and Clindamycin.* In: Mandell, Douglas, and Bennett's Principles and Practice of Infectious Diseases. Chapter 28. 170-page PDF supplied 2026-06-24.
