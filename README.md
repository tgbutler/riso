# RiSO: A BFO-Compliant Upper-Domain Risk Science Ontology
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22807603.svg)](https://doi.org/10.5281/zenodo.22807603)

RiSO is an upper-domain ontology for risk science, developed as a top-down realist ontology engineering project grounded in the Basic Formal Ontology (BFO) and aligned with the ISO/IEC 21838 standard for top-level ontologies. It formalizes the concepts of the Society for Risk Analysis (SRA) Glossary and the broader risk science literature as BFO-compliant universals, defined classes, and relations, and expresses their logical commitments as a set of first-order logic axioms (the RiSA axiom set).

## What is in this release

This is RiSO v2.1, a corrected release of v2. Phase 1, the BFO-compliant terminological dictionary and its axiomatization in first-order logic, is complete: 155 terms, 219 axioms across 34 axiom sets, and 57 RiSO-defined relations. Phase 2, translating these specifications into a machine-readable OWL 2 DL ontology, is in progress: every term and relation has a resolved URI (external where RiSO reuses an existing BFO/CCO/IAO/OBI/RO term, newly minted under RiSO's own namespace where it does not), and class generation is underway. The OWL file itself is not included in this release, since it is not yet complete or reasoner-checked; it will follow as its own release once it is.

- `RiSO_Companion_v2.1.pdf` and `RiSO_Companion_v2.1.docx`: the full companion document, covering the methodology, the terminological dictionary, the first-order logic axioms, the reused and RiSO-defined relations, and a discussion of RiSO's role as an upper-domain ontology.
- `RiSO_Workbook_v2.1.xlsx`: the same terminological content in spreadsheet form, for readers who want to search, filter, or reuse it directly rather than read it linearly. Six sheets:
  - **About**: this project, its version, and its license
  - **Table 1 - Dictionary**: the terminological dictionary, with SRA, CCO/IAO/OBI/RO, and RiSA references unpacked into separate columns
  - **Table 2 - Alpha Index**: an alphabetical index to Table 1
  - **Table 3 - Reused Defs**: source definitions for every BFO/CCO/IAO/OBI/RO term RiSO reuses
  - **Table 4 - RiSO Relations**: the relations RiSO coins for its axioms, with their signatures, the axioms that use them, and their definitions
  - **RiSA Index**: every first-order logic axiom, with its axiom set, formula, and gloss
- `RiSO_URI_Mapping_v2.1.csv`: the full term-to-URI resolution table underlying Phase 2, covering every Table 1, Table 3 and Table 4 entry, whether it resolves to a newly minted RiSO URI or an existing external one, and why. The file is UTF-8 encoded and opens correctly in Excel.

## How to cite

If you use RiSO, please cite it using the concept DOI, which always resolves to the latest version:

Butler, T., & Seppälä, S. (2026). *RiSO: A BFO-Compliant Upper-Domain Risk Science Ontology* (Version 2.1.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.22807603

Citation metadata is also available in `CITATION.cff`, and through the "Cite this repository" button on the repository page.

## How RiSO was developed

RiSO's terminological dictionary and axioms were developed through a human-in-the-loop neurosymbolic methodology: a human ontologist and a large language model working in an iterative loop, with the model's output constrained throughout by BFO, the Common Core Ontologies (CCO), the Information Artifact Ontology (IAO), the Relations Ontology (RO), and OBO Foundry principles under ISO/IEC 21838. The human ontologist directed the process, evaluated and corrected every definition and axiom, and re-introduced corrected versions for further refinement, rather than accepting model output directly.

## Architecture and implications

RiSO is designed as the mid-tier of a three-tier stack: BFO provides the top-level categories, RiSO provides the domain-neutral risk-science layer, and a domain-specific ontology specializes RiSO for a particular sector. The Financial Institution Resilience Ontology (FIRO) is the first such specialization. A domain ontology built on RiSO inherits its risk, resilience, and consequence apparatus by declaring its own activities, bearers, and consequences as subtypes of RiSO's corresponding classes, without needing to restate the underlying axioms.

## License

The documents and spreadsheets in this repository are licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**. See `LICENSE`.

Any OWL ontology files and source code added in future releases are licensed separately under the **3-Clause BSD License**. See `LICENSE-CODE`.

## Namespace

RiSO's namespace is `https://w3id.org/riso/`.

