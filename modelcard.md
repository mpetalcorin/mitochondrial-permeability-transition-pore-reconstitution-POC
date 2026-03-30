# Model Card: mPTP Reconstitution Proof-of-Concept Framework

## Model details

### Model name
mPTP Reconstitution Proof-of-Concept Framework

### Model type
Synthetic mechanistic simulation combined with supervised machine learning

### Primary components
The framework integrates:
- state-based synthetic mitochondrial phenotype simulation
- binary classification of sustained pathological pore opening
- regression of downstream functional outputs
- multivariate visualization and counterfactual intervention analysis

### Implementation context
The framework is implemented in a Jupyter notebook and is designed for exploratory computational biology research. It uses simulated data that approximate mitochondrial stress-response behavior under literature-informed conditions.

## Model purpose

The purpose of this framework is to support early-stage reasoning about how candidate mitochondrial permeability transition pore-related components may behave under different disease-relevant stress environments. It is intended to help prioritize reconstitution architectures, perturbation experiments, and assay readouts before laboratory implementation.

The model is built around a candidate permeability transition system centered on ANT, F1FO-ATP synthase, and Cyclophilin D, with optional phosphate carrier modulation. It does not claim to identify the definitive molecular structure of the mPTP.

## Intended users

This framework is intended for:
- mitochondrial biologists
- biochemists planning reconstitution studies
- computational biologists building hypothesis-generation pipelines
- students and trainees learning how synthetic data can guide experimental design
- interdisciplinary researchers exploring cardiac injury and cancer mitochondrial stress responses

## Intended use

Appropriate uses include:
- hypothesis generation
- prioritization of reconstitution component combinations
- comparison of disease-state-specific pore behavior
- exploratory machine learning on synthetic mitochondrial state spaces
- educational demonstrations of systems-level mitochondrial modeling

## Out-of-scope use

This framework should not be used for:
- clinical diagnosis
- patient stratification
- treatment selection
- regulatory submissions
- claims of experimental proof of pore identity
- direct quantitative prediction of outcomes in real biological samples without external validation

## Data used

The model uses only synthetic data generated within the notebook. Variable ranges and interaction logic were chosen to be biologically plausible and broadly aligned with peer-reviewed literature on permeability transition, ischemia-reperfusion injury, cancer mitochondrial adaptation, calcium overload, oxidative stress, and energetic failure.

No patient data, animal records, or proprietary experimental datasets are included.

## Features

The core input features are:
- membrane potential
- matrix calcium
- mitochondrial reactive oxygen species
- matrix pH
- ADP/ATP ratio
- cardiolipin integrity index
- Cyclophilin D activity
- ANT function
- ATP synthase pore propensity
- phosphate carrier modulation

Derived variables include:
- transient pore score
- sustained pore opening probability
- calcium retention capacity-like behavior
- threshold calcium for sustained opening
- leakage area under the curve
- conductance-like signal
- time to sustained opening
- ATP preservation index
- mtDNA release proxy
- viability proxy

## Outputs

### Classification output
Binary prediction of whether a condition belongs to a sustained pathological pore opening regime.

### Regression outputs
Continuous prediction of:
- calcium retention capacity-like behavior
- ATP preservation index
- mtDNA release proxy
- viability proxy

### Visualization outputs
The framework also generates state comparison plots, heatmaps, feature importance rankings, PCA projections, and counterfactual perturbation summaries.

## Performance characteristics

Performance metrics reported in the notebook describe fit within the synthetic design space only. High predictive performance indicates internal coherence of the simulated data-generating process, not validated accuracy in real mitochondrial systems.

Users should therefore interpret model performance as evidence that the simulation rules are self-consistent, not that the models generalize to experimental biology.

## Assumptions

The framework assumes that:
- disease states can be approximated as different regions of mitochondrial stress space
- pore behavior can be summarized by weighted interactions among calcium, ROS, membrane potential, pH, energetic stress, and candidate protein activities
- ANT, ATP synthase, and Cyclophilin D can be treated as coordinated contributors to permeability transition competence
- synthetic proxies can stand in for experimental readouts such as calcium retention, leakage, ATP loss, and mtDNA release

These assumptions are useful for exploratory modeling, but they simplify complex mitochondrial biology.

## Limitations

Important limitations include:
- the entire dataset is synthetic
- the model does not capture full structural biophysics of ANT or ATP synthase
- lipid microenvironment, membrane curvature, phosphate chemistry, and supercomplex organization are simplified
- low-conductance and high-conductance permeability transition behavior are represented abstractly rather than through detailed kinetics
- experimental noise, batch effects, and assay-specific artifacts are not explicitly modeled

## Ethical and responsible use considerations

Because the model is synthetic and non-clinical, its main risk is overinterpretation. Users should avoid presenting the outputs as proof of pore identity, proof of disease mechanism, or validated therapeutic insight. Any biological conclusions should be tested experimentally.

## Maintenance and versioning

This model card describes the current proof-of-concept notebook version associated with the repository. If the simulation logic, variable definitions, or target outputs are changed substantially, the model card should be updated accordingly.



