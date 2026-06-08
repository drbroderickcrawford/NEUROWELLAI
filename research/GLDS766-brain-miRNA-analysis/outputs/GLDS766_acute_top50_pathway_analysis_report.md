# GLDS-766 Brain miRNA Pathway-Level Analysis

## Comparison

`FL_ISS_Term` versus `HGC_ISS_Term`.

The analysis used the top 50 miRNAs ranked by raw p-value from the filtered voom comparison. None of the individual miRNAs survived FDR correction. Forty-five of the top 50 miRNAs had lower expression in `FL_ISS_Term`.

## Method

- Retrieved mouse-specific miRNA-target interactions using multiMiR 2.4.0.
- Restricted the primary analysis to experimentally supported interactions labeled `Functional MTI` or `Functional MTI (Weak)`.
- Identified 1,523 functional interaction records representing 788 target genes with mouse Gene Ontology Biological Process annotations.
- Tested target-gene enrichment against the annotated mouse-gene background.
- Searched enriched terms for seven prespecified neurobehavioral themes.

## Prespecified Themes

| Theme | Representative enriched term | Target genes | Contributing miRNAs | FDR |
|---|---|---:|---:|---:|
| Neuroplasticity | Axon development | 57 | 27 | 1.12e-14 |
| Synaptic signaling | Synapse organization | 57 | 24 | 2.92e-12 |
| Neuroinflammation | Immune system development | 28 | 21 | 5.90e-09 |
| Stress response | Response to hypoxia | 39 | 20 | 4.46e-12 |
| Circadian biology | Rhythmic process | 32 | 20 | 3.31e-07 |
| Aging | Negative regulation of cellular senescence | 4 | 4 | 0.050 |
| Cognitive function | Behavior | 72 | 26 | 3.37e-15 |

Additional enriched terms included learning or memory, memory, circadian rhythm, circadian regulation of gene expression, axonogenesis, nervous system development, synapse assembly, DNA damage response, and regulation of leukocyte migration.

## Recurrent Candidate miRNAs

- `mmu-miR-34a-5p`
- `mmu-miR-132-3p`
- `mmu-miR-204-5p`
- `mmu-miR-10a-5p`
- `mmu-miR-10b-5p`
- `mmu-miR-30a-5p`
- `mmu-miR-218-5p`
- `mmu-miR-140-5p`
- `mmu-miR-449a-5p`
- `mmu-miR-3473a`

## Interpretation

The top-ranked miRNAs collectively target genes involved in neural development and plasticity, synaptic organization, behavior and memory, rhythmic biology, immune regulation, and cellular stress responses. This is consistent with a distributed regulatory response rather than a strong single-miRNA signature.

Because most top-ranked miRNAs were lower in flight, their target genes could experience reduced miRNA-mediated repression. However, pathway activation or suppression cannot be inferred without matched gene or protein expression.

## Limitations

- No individual miRNA was significant after multiple-testing correction.
- Selecting miRNAs by raw p-value makes this exploratory and potentially unstable.
- miRNA-target databases favor well-studied miRNAs and broadly regulated genes, which can inflate enrichment for large developmental and behavioral categories.
- Whole-brain measurements may conceal region-specific responses.
- Target enrichment indicates regulatory potential, not demonstrated pathway activity.

The pathway findings should therefore be treated as hypothesis-generating evidence for coordinated neurobehavioral adaptation, not confirmation of a flight-induced pathway effect.
