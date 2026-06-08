# GLDS-766 Brain miRNA Analysis

Exploratory integration of brain miRNA and mRNA results from NASA OSDR
`OSD-916 / GLDS-766`, GEO `GSE294046`, and complementary mRNA dataset
`GSE295428`.

## Main Finding

Individual miRNAs were not significant after false-discovery-rate correction,
and the controls did not support a specific genome-wide model of
miRNA-mediated derepression.

However, validated target genes associated with neuroplasticity, synaptic
signaling, cognition, stress response, and neuroinflammatory pathways showed
robust upward shifts. These results support a cautious exploratory model of
coordinated neurobehavioral adaptation while leaving the specific role of
miRNA-mediated regulatory relaxation unresolved.

## Start Here

- [Beginner-friendly white paper in Google Docs](https://docs.google.com/document/d/1ite2XgqynIW3bUx4A-StXjRi25UOHg7TKviqsYoPd28/edit?usp=drivesdk)
- [Target-shift robustness report](outputs/GLDS766_LAR_target_shift_robustness_report.md)
- [miRNA-mRNA integration assessment](outputs/GLDS766_miRNA_mRNA_integration_assessment.md)
- [Acute top-50 pathway report](outputs/GLDS766_acute_top50_pathway_analysis_report.md)

## Study Design

The brain miRNA dataset contains 25 samples across six experimental groups.
The primary recovery comparison was `FL_LAR` versus `HC_LAR` with four samples
per group. An acute comparison used `FL_ISS_Term` versus `HGC_ISS_Term`.

The public mRNA data support group-level and pathway-level integration, not a
clean paired-animal causal analysis.

## Robustness Checks

Three checks tested the initial hypothesis that flight-downregulated miRNAs
produce broad upward shifts in their mRNA targets:

1. **Negative control:** the observed validated-target shift was not stronger
   than target shifts from random measured miRNAs.
2. **Opposite-direction test:** targets of flight-upregulated miRNAs did not
   shift downward.
3. **Theme-specific robustness:** plasticity, synaptic signaling, cognition,
   stress, and neuroinflammatory themes remained stronger than background and
   most remained stronger than other validated-target sets.

## Repository Contents

- `outputs/`: focused reports and key result tables.

The full local analysis package includes figures, processed matrices, and
editable/PDF white-paper files. Large downloaded source files and broad
target-database exports are excluded from this repository folder. Source data
remain available from OSDR and GEO.

## Interpretation Boundary

This is an exploratory analysis, not a publish-ready causal claim. Small
sample sizes, tissue-collapsed mRNA results, incomplete animal-level matching,
and target-database bias limit inference. The strongest next analysis is
region- and cell-type-specific reprocessing of the complementary single-cell
mRNA data.

## Data Sources

- [NASA OSDR OSD-916](https://osdr.nasa.gov/bio/repo/data/studies/OSD-916)
- [GEO GSE294046](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE294046)
- [GEO GSE295428](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE295428)
- [Associated publication](https://pmc.ncbi.nlm.nih.gov/articles/PMC12876965/)
- [Author analysis code](https://github.com/CCB-SB/SpaceMice_miRNA)
