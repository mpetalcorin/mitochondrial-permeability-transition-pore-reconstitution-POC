# mitochondrial-permeability-transition-pore-reconstitution-POC
Synthetic, literature-benchmarked computational framework for prioritizing candidate mPTP reconstitution components, stress conditions, perturbations, and readouts in cardiac injury and cancer.
<img width="1236" height="806" alt="Screenshot 2026-03-30 at 11 24 35" src="https://github.com/user-attachments/assets/127f3b13-5c85-4555-b540-6c95d9728fb7" />

# mPTP Reconstitution Proof-of-Concept

This repository contains a synthetic, literature-benchmarked proof-of-concept framework for studying the mitochondrial permeability transition pore (mPTP) through an in vitro reconstitution perspective. The project does not claim biochemical reconstitution of the pore itself. Instead, it provides a computational and analytical scaffold to help prioritize candidate molecular components, disease-relevant stress conditions, perturbation strategies, and experimental readouts for future laboratory validation.

The notebook models a candidate permeability transition system centered on adenine nucleotide translocase (ANT), F1FO-ATP synthase, and Cyclophilin D (CypD), with optional modulation by the phosphate carrier. These elements were selected because current literature supports their involvement in permeability transition regulation or pore competence, although the exact molecular identity of the pore remains unresolved.

The proof-of-concept simulates mitochondrial phenotypes across four biologically meaningful states: cardiac control, cardiac ischemia-reperfusion, therapy-naive cancer, and stress-adapted cancer. Within each state, the notebook explores five perturbation regimes: wild type, reduced CypD activity, reduced ANT function, reduced ATP synthase pore propensity, and combined ANT plus ATP synthase reduction. From these simulated conditions, the workflow derives transient pore behavior, sustained pore opening probability, calcium retention capacity-like behavior, threshold calcium for catastrophic opening, leakage burden, conductance-like signal, ATP preservation, mtDNA release proxy, and viability proxy.

The notebook also applies machine learning and multivariate analysis to identify the most influential predictors of sustained pathological opening and to quantify how upstream mitochondrial stress variables shape downstream injury outputs. These analyses are meant to guide experimental prioritization, not to replace biochemical evidence.

## Repository contents

`mPTP_reconstitution_proof_of_concept-2.ipynb`  
Main Jupyter notebook containing the full simulation, analysis workflow, machine learning models, visualizations, and table generation.

`README.md`  
Project overview, rationale, repository structure, and usage notes.

`modelcard.md`  
Model card describing the purpose, scope, assumptions, intended use, limitations, and responsible interpretation of the computational framework.

`datasheet.md`  
Datasheet describing the synthetic dataset generation process, variable definitions, provenance logic, structure, and limitations.

## Scientific rationale

The mitochondrial permeability transition pore is a critical determinant of mitochondrial failure, bioenergetic collapse, and cell death. It is especially relevant in cardiac ischemia-reperfusion injury, where pore opening contributes to tissue damage, and in cancer, where altered pore sensitivity may help tumor cells avoid death while preserving mitochondrial plasticity. Because the field still lacks full consensus on pore identity, a synthetic decision-support framework can help identify which reconstitution strategies are most informative before resource-intensive biochemical experiments are undertaken.

This project is therefore designed to support future studies using proteoliposomes, nanodiscs, planar membranes, or other purified membrane systems that include ANT, ATP synthase, Cyclophilin D, and controlled stress triggers such as calcium, ROS, pH shift, and energetic imbalance.

## Main outputs

The notebook generates:

1. Synthetic state-resolved datasets spanning multiple perturbation conditions.
2. Summary tables for mitochondrial state variables and downstream phenotypes.
3. Publication-style figures showing disease-state comparisons, perturbation heatmaps, feature importance, regression performance, principal component analysis, and counterfactual intervention analysis.
4. Machine learning models for classification of sustained pathological pore opening and regression of key downstream outputs.
5. A quantitative framework for prioritizing candidate reconstitution experiments.

## Intended use

This repository is intended for hypothesis generation, educational use, early-stage experimental planning, and computational benchmarking. It may help researchers think more systematically about how candidate mPTP components interact under disease-relevant stress conditions.

It is not intended for diagnostic use, therapeutic decision-making, or as evidence that any specific protein assembly has been experimentally proven to be the pore.

## How to use

Open the notebook and run the cells sequentially. The workflow will generate simulated data, train the machine learning models, create figures, and export tables. Users may adapt the parameter ranges, equation weights, perturbation definitions, or disease states to test alternative mechanistic assumptions.

## Key limitations

All observations in this repository are synthetic. The equations, variable ranges, and interaction weights were designed to be biologically plausible and literature-informed, but they are still abstractions. The results should be interpreted as a prioritization tool for future experiments rather than as biological proof.

## Citation
**Petalcorin, M.I.R.** (2026). In vitro reconstitution of a candidate mitochondrial permeability transition system, a synthetic proof-of-concept framework integrating ANT, F1FO-ATP synthase, and Cyclophilin D across cardiac injury and cancer stress states. https://github.com/mpetalcorin/mitochondrial-permeability-transition-pore-reconstitution-POC

If you use or adapt this repository, cite it as a proof-of-concept computational framework for prioritizing mPTP reconstitution experiments and clearly state that the dataset is synthetic and hypothesis-generating.
