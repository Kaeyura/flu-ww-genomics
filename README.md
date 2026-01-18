# Influenza Surveillance via Genomics & Wastewater

## Project Status
**Week 1 – Project initialization & scoping**

This repository documents the early-stage development of a computational research project exploring how **viral genomics** and **wastewater surveillance** could be used to estimate influenza disease burden in settings with limited clinical reporting.

At this stage, the project is focused on **problem formulation, data discovery, and methodological design**. No final conclusions are claimed.

---

## Motivation
Influenza surveillance traditionally relies on **clinical reporting**, which depends on healthcare access, testing availability, and reporting compliance. In many regions (e.g., India), these systems significantly undercount true infections.

Wastewater surveillance offers a population-level signal that does not depend on individual testing behavior. Viral genomics provides additional context about circulating strains and their biological characteristics.

This project asks:

> *If wastewater viral load and viral genomic data were available, could they be used to estimate the true clinical burden of influenza in under-reported settings?*

---

## Initial Research Questions
This project is **not** focused on early outbreak detection.

Instead, the guiding questions are:

1. How do influenza viral genomic characteristics (conserved vs variable genes) behave within a single season?
2. How does wastewater influenza viral load relate to reported clinical indicators?
3. Can wastewater + genomics be used to **correct or calibrate** clinical case counts?
4. Can a model trained on U.S. data be conceptually extended to countries with weaker surveillance infrastructure?

---

## Scope (Week 1)

### Included
- Influenza A virus
- Publicly available datasets only
- Computational and statistical analysis
- No wet-lab or experimental work

### Excluded
- Human subjects research
- Individual-level clinical prediction
- Claims of causality or real-time forecasting

---

## Data Identified (Preliminary)

### Viral Genomics
- Source: **NCBI GenBank**
- Genes of interest:
  - **Segment 4: Hemagglutinin (HA)** – antigenically variable
  - **Segment 5: Nucleoprotein (NP)** – conserved structural gene
- Metadata: accession IDs, collection dates

### Wastewater Surveillance
- Source: **CDC National Wastewater Surveillance System (NWSS)**
- Metric: Influenza A viral concentration (PCR-based)
- Aggregation: weekly, state-level (California as pilot)

### Clinical Surveillance
- Source: **CDC FluView / ILINet**
- Metric: weekly influenza-like illness (ILI) percentages
- Aggregation: weekly, state-level

*Note: These datasets are being used initially to understand feasibility and relationships, not to build a production model.*

---

## Planned Methodological Approach (Draft)

### Phase 1 – Genomics (Current)
- Align HA and NP sequences
- Quantify within-season variability
- Compare conserved vs variable genes

### Phase 2 – Wastewater Signal
- Clean and aggregate viral load data
- Identify sustained detection periods
- Compare temporal trends with clinical data

### Phase 3 – Integration
- Combine genomics, wastewater, and clinical signals
- Evaluate correlations and structural relationships
- Explore burden correction models

### Phase 4 – Conceptual Extension
- Assess applicability to India
- Identify data gaps and assumptions
- Propose a transferable modeling framework

---

## Tools & Environment
- Python (pandas, numpy, scipy)
- BioPython for sequence handling
- Matplotlib / seaborn for visualization
- Reproducible scripts (no notebooks required)

---

## Ethics & Compliance
- All data are public and de-identified
- No personal health information
- Computational research only

---

## Week 1 Goals
- Finalize project scope and non-goals
- Validate data availability and quality
- Establish a clean, reproducible code structure
- Avoid premature claims or conclusions

---

## Next Steps (Week 2)
- Finalize genomic variability metrics
- Establish consistent weekly time indexing
- Produce first exploratory plots (no interpretation yet)

---

## Notes
This README will evolve weekly to reflect the project’s current state. Claims and conclusions will only be added once supported by analysis.
