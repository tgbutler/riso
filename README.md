# RiSO: A BFO-Compliant Upper-Domain Risk Science Ontology

RiSO is an upper-domain ontology for risk science, developed as a top-down realist ontology engineering project grounded in the Basic Formal Ontology (BFO) and aligned with the ISO/IEC 21838 standard for top-level ontologies. It formalizes the concepts of the Society for Risk Analysis (SRA) Glossary and the broader risk science literature as BFO-compliant universals, defined classes, and relations, and expresses their logical commitments as a set of first-order logic axioms (the RiSA axiom set).

## What is in this release

This is RiSO v2. Phase 1, the BFO-compliant terminological dictionary and its axiomatization in first-order logic, is complete: 150 terms, 216 axioms across 34 axiom sets. Phase 2, translating these specifications into a machine-readable OWL 2 DL ontology, is in progress: every term and relation has a resolved URI (external where RiSO reuses an existing BFO/CCO/IAO/OBI/RO term, newly minted under RiSO's own namespace where it doesn't), and class generation is underway. The OWL file itself isn't included in this release yet, since it isn't complete or reasoner-checked; it will follow as its own release once it is.

- `RiSO_Companion_v2.pdf` and `RiSO_Companion_v2.docx` — the full companion document: methodology, terminological dictionary, first-order logic axioms, and a discussion of RiSO's role as a mid-tier ontology.
- `RiSO_Workbook_v2.xlsx` — the same terminological content in spreadsheet form, for readers who want to search, filter, or reuse it directly rather than read it linearly. Five sheets:
  - **About** — this project, its version, and its license
  - **Table 1 - Dictionary** — the terminological dictionary, with SRA, CCO/IAO/OBI/RO, and RiSA references unpacked into separate columns
  - **Table 2 - Alpha Index** — an alphabetical index to Table 1
  - **Table 3 - Reused Defs** — source definitions for every BFO/CCO/IAO/OBI/RO term RiSO reuses
  - **RiSA Index** — an index of every first-order logic axiom, with its formula and a one-line paraphrase
- `RiSO_URI_Mapping.csv` — the full term-to-URI resolution table underlying Phase 2: every Table 1 and Table 3 entry, whether it resolves to a newly minted RiSO URI or an existing external one, and why.

## How RiSO was developed

RiSO's terminological dictionary and axioms were developed through a human-in-the-loop neurosymbolic methodology: a human ontologist and a large language model working in an iterative loop, with the model's output constrained throughout by BFO, the Common Core Ontologies (CCO), the Information Artifact Ontology (IAO), the Relations Ontology (RO), and OBO Foundry principles under ISO/IEC 21838. The human ontologist directed the process, evaluated and corrected every definition and axiom, and re-introduced corrected versions for further refinement, rather than accepting model output directly.

## Architecture and implications

RiSO is designed as the mid-tier of a three-tier stack: BFO provides the top-level categories, RiSO provides the domain-neutral risk-science layer, and a domain-specific ontology specializes RiSO for a particular sector. The Financial Institution Resilience Ontology (FIRO) is the first such specialization. A domain ontology built on RiSO inherits its risk, resilience, and consequence apparatus by declaring its own activities, bearers, and consequences as subtypes of RiSO's corresponding classes, without needing to restate the underlying axioms.

## License

The documents and spreadsheets in this repository are licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**. See `LICENSE`.

Any OWL ontology files and source code added in future releases are licensed separately under the **3-Clause BSD License**. See `LICENSE-CODE`.

## Namespace

RiSO's namespace is `https://w3id.org/riso/`.

## Citing RiSO

See `CITATION.cff`, or use the "Cite this repository" option on this repository's GitHub page.
