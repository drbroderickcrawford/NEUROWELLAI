# GLDS-766 miRNA-mRNA Integration Assessment

## Can the miRNA findings be connected to mRNA?

Yes, but the public data support group-level and pathway-level integration rather than a clean paired-animal correlation analysis.

- The miRNA data include LAR and immediate-termination brain samples.
- The complementary single-cell mRNA dataset, GSE295428, contains LAR spaceflight and control samples, including forebrain, hippocampus, and cerebellum cell populations.
- GSE295428 does not contain the FL_ISS_Term and HGC_ISS_Term animals used in the acute miRNA analysis.
- Public mRNA identifiers use labels such as `Mouse 1` through `Mouse 4`, whereas the miRNA samples use different animal identifiers. An exact cross-modal animal mapping is not provided.
- The publication's analysis code integrates miRNA and mRNA using group-level differential expression and TargetScan pairs, not mouse-level correlations.

Therefore, the acute-flight miRNA hypothesis can be tested against LAR mRNA only as cross-cohort or cross-time supporting evidence. A paired causal chain cannot be claimed.

## Preliminary LAR Candidate Check

| miRNA | LAR miRNA log2FC | LAR miRNA raw p | Functional targets present | Targets showing inverse direction |
|---|---:|---:|---:|---:|
| mmu-miR-132-3p | -1.58 | 0.287 | 3 | 3/3 |
| mmu-miR-34a-5p | 0.21 | 0.602 | 3 | 1/3 |
| mmu-miR-218-5p | -0.34 | 0.550 | 0 | Not testable |

For `mmu-miR-132-3p`, the three available functional targets were all higher in the LAR flight mRNA results:

| Target | mRNA log2FC | Raw p | Adjusted p |
|---|---:|---:|---:|
| Mapt | 1.59 | 0.057 | 0.962 |
| Rfx4 | 1.89 | 0.629 | 0.988 |
| Mmp9 | 3.30 | 0.857 | 0.991 |

This direction is consistent with reduced miRNA-mediated repression, but none of these signals survives multiple-testing correction.

## Strongest Defensible Next Test

1. Rank all LAR brain miRNAs by signed differential-expression statistic.
2. Define high-confidence TargetScan or functional experimental target sets.
3. Test whether targets of lower-flight miRNAs are collectively shifted toward higher mRNA expression in LAR brain pseudobulks.
4. Repeat separately for forebrain, hippocampus, cerebellum, and major neural or immune cell classes.
5. Test whether inverse miRNA-target pairs concentrate in neuroplasticity, synaptic signaling, circadian regulation, stress response, and cognition pathways.
6. Use permutation tests that preserve target-set size and miRNA expression to control database and selection biases.

## Interpretation Boundary

A finding that lower-flight miRNAs have collectively higher target mRNAs would support coordinated relaxation of miRNA-mediated regulation. It would still not prove direct repression, because miRNAs can affect translation without changing mRNA abundance and both modalities may respond to shared upstream signals.
