# JNE Memristive SNN Study: Supplementary Data

This repository contains the supplementary data tables, model configurations, and derived outputs assembled for a *Journal of Neural Engineering* study of literature-constrained memristive synapses in spiking neural networks (SNNs) for surface electromyography (sEMG) classification.

The package supports inspection of the device models, preprocessing and network settings, stationary S1 benchmark, continual-learning analyses, timescale-matching analysis, and hybrid fast-persistent synapse analysis. A file-by-file description and provenance map is provided in [`README_files.md`](README_files.md).

## Repository contents

| Directory | Contents |
|---|---|
| `device_data/` | Literature-derived programming and memory trajectories, empirical PCHIP representations, parametric-fit outputs, device descriptors, quality-control tables, and runtime validation files. |
| `preprocessing_network_config/` | NinaPro DB6 S1 data-split definitions, preprocessing settings, selected channels, encoding thresholds, SNN configuration, random seeds, and hyperparameter-search results. |
| `stationary_S1_results/` | Stationary S1 participant- and seed-level metrics, model summaries, learning curves, programming burden, state occupancy, mapping errors, and validation gates. |
| `continual_learning_results/` | Inter-session adaptation and retention tables, balanced-accuracy matrices, forgetting, backward transfer, and stability-plasticity summaries. |
| `timescale_sweep_LOPO/` | Controlled memory/drift timescale grids, full sweep tables, dimensionless timescale-ratio summaries, and leave-one-participant-out model comparisons. |
| `hybrid_results/` | Fast, persistent, and hybrid-condition results, paired comparisons, and hardware/pulse-count summaries. |

The root-level `file_manifest.csv` records the source mapping, SHA-256 checksum, and size of each included data or documentation file.

## Data provenance

Device-level programming and memory data were obtained from machine-readable author data when available and otherwise reconstructed from figures and numerical information already extracted from the cited source articles within the project. The repository separates:

- article-derived programming and memory trajectories;
- derived device representations and descriptors, including PCHIP knots and fit diagnostics;
- preprocessing and SNN configuration files;
- stationary benchmark and downstream analysis tables.

No unsupported numerical values were added during repository assembly. Device-to-source mappings are listed in `device_data/device_source_map.csv`, and the provenance of every packaged file is documented in `README_files.md` and `file_manifest.csv`.

## Important data-status notice

Files derived from the project folders for Figures 5–8 retain their original `notice` fields. Where those fields identify a table as an illustrative or conceptual scenario rather than measured or simulated results, the table must be interpreted accordingly and must not be presented as empirical validation data. The stationary S1 benchmark files are kept in a separate directory to preserve this distinction.

## Formats and use

Most tables are provided as UTF-8 CSV files. Configuration and provenance records use JSON, YAML, TXT, or Markdown as appropriate. Relative paths are used throughout the package so that the repository can be cloned and inspected on any system.

For a detailed definition and source of each file, begin with [`README_files.md`](README_files.md). Before analysis, verify file integrity against `file_manifest.csv`. Column names and embedded status fields should be retained when redistributing or transforming the tables so that provenance and interpretation remain traceable.

## Citation

When using this repository, cite the associated JNE manuscript and the original device publications from which the literature-derived data were obtained. The complete manuscript citation and DOI should be added here when they become available.

