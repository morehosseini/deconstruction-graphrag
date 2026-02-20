# Deconstruction GraphRAG

[![DOI](https://img.shields.io/badge/DOI-pending-lightgrey)]() [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) ![GitHub last commit](https://img.shields.io/github/last-commit/morehosseini/deconstruction-graphrag)

## Overview

This repository contains the implementation of a Graph Retrieval-Augmented Generation (GraphRAG) governance intelligence pipeline. The project maps and analyses the fragmented regulatory landscape of building deconstruction and material salvage across Australia's federal, state, and local jurisdictions.

While Australia is transitioning toward a circular built environment, deconstruction efforts are often hindered by definitional ambiguity and a fragmented policy landscape. This tool replaces manual, unscalable document reviews with an automated, evidence-linked pipeline that converts unstructured policy instruments into a queryable Knowledge Graph (KG).

**Authors:** M. Reza Hosseini¹, Ruoyu Jin², Mazdak Nik-Bakht³

¹ Faculty of Architecture, Building and Planning, The University of Melbourne, Australia
² Brunel University London, UK
³ Concordia University, Canada

**Status:** Journal/conference — to be decided | DOI — pending

## Key Features

- **Heterogeneous Data Processing:** Converts complex government PDFs (Acts, regulations, and local policies) into machine-actionable text.
- **Precision Filtering:** Uses LLM-driven filtering to distinguish specific deconstruction/salvage clauses from generic "waste diversion" narratives.
- **Evidence-Linked Knowledge Graph:** Populates a schema-constrained KG encoding Who governs What, Where, and How, preserving strict provenance (source, page, and chunk ID) for every claim.
- **Automated Gap Analysis:** Identifies jurisdictional fragmentation and governance deficits where industry practices lack institutional support.

## The Pipeline

1. **Ingestion** — Processes unstructured PDF corpora from three tiers of government.
2. **Extraction** — Performs semantic retrieval and deterministic filtering of salvage-relevant requirements.
3. **Graph Construction** — Maps entities and relations (Authority → Instrument → Requirement → Practice → Outcome).
4. **Intelligence Layer** — Supports graph traversal and query-driven synthesis for jurisdictional comparison and barrier identification.

## Research Contributions

| ID | Contribution |
|----|-------------|
| C1 | An end-to-end GraphRAG workflow for regulatory corpus processing |
| C2 | An auditable knowledge graph with full metadata provenance |
| C3 | Graph-enabled tracing of governance pathways and policy gaps |
| C4 | A schema-constrained extraction strategy and comprehensive audit logs |

## Repository Structure

```
deconstruction-graphrag/
├── README.md
├── LICENSE
├── .gitignore
├── notebooks/
│   ├── 1_Deconstruction_Filter_Pilot.ipynb
│   ├── 2_Deconstruction_Semantic_Filter_Pipeline.ipynb
│   ├── 3_KG_Extraction_v2_EntityRegistry.ipynb
│   ├── 4_KG_Cleanup_MultiCountry_Schema.ipynb
│   ├── 5_Governance_Intelligence_Backend.ipynb
│   ├── 6_Presentation_Outputs.ipynb
│   └── Table_F1_Figure_F1.ipynb
├── data/
│   ├── graph_built_v2/
│   │   ├── edge_triples.csv
│   │   ├── edges.csv
│   │   └── nodes.csv
│   ├── kg_cleaned/
│   │   ├── edges_clean.csv
│   │   ├── nodes_clean.csv
│   │   └── triples_clean.csv
│   ├── corpus_summary/
│   │   └── Table_F1_corpus_deconstruction_summary.csv
│   └── records.xlsx
└── figures/
    ├── fig1_architecture.png
    ├── fig2_schema.png
    ├── fig3_dashboard.png
    ├── fig4_dfd_pathway.png
    ├── fig5_jurisdiction_heatmap.png
    ├── fig6_gap_analysis.png
    ├── fig7_demo_cards.png
    └── Figure_F1_corpus_deconstruction_composite.png
```

## Getting Started

### Prerequisites

- Python >= 3.10
- Jupyter Notebook / JupyterLab
- LangChain
- FAISS (faiss-cpu)
- OpenAI or compatible LLM API key

### Installation

```bash
git clone https://github.com/morehosseini/deconstruction-graphrag.git
cd deconstruction-graphrag
pip install -r requirements.txt
```

### Usage

```bash
jupyter notebook notebooks/
```

Run notebooks in order (1 → 6) to reproduce the full pipeline.

## Technologies

- **Python 3.10+** — Core language
- **Jupyter** — Interactive notebooks for reproducible analysis
- **LangChain** — LLM orchestration for retrieval and extraction
- **FAISS** — Vector similarity search for semantic retrieval
- **NetworkX / Neo4j** — Knowledge graph construction and traversal
- **Pandas** — Data manipulation and CSV I/O
- **Matplotlib / Seaborn** — Visualisation

## Citation

```bibtex
@misc{hosseini2026deconstruction,
  author  = {Hosseini, M. Reza and Jin, Ruoyu and Nik-Bakht, Mazdak},
  title   = {Deconstruction GraphRAG: A Graph Retrieval-Augmented Generation Pipeline for Australian Deconstruction Governance},
  year    = {2026},
  doi     = {pending},
  url     = {https://github.com/morehosseini/deconstruction-graphrag}
}
```

## Licence

This project is licensed under the **MIT** Licence — see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome. Please open an Issue first to discuss proposed changes.

## Contact

**Dr. M. Reza Hosseini**
Senior Lecturer in Construction Technology
Faculty of Architecture, Building and Planning, The University of Melbourne
For questions, open a [GitHub Issue](https://github.com/morehosseini/deconstruction-graphrag/issues).

---
*This repository was prepared in accordance with open-science and FAIR-data principles.*
