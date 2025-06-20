# Enhancing Radar-Based Velocity Estimation in Autonomous Driving: A Physics-Informed Hybrid Modelling Study

## Abstract

The detection and classification of other traffic participants are integral components of the perception task for autonomous vehicles. It is particularly challenging because not only static parameters like class association, position, and shape must be predicted, but also dynamic parameters like velocity need to be estimated. Even though other sensor modalities currently dominate autonomous vehicle sensor suites, radar has emerged as a competitive alternative, especially for velocity estimation.

This work investigates physics-informed hybrid modelling as a means of incorporating measured radial velocities into Deep Learning-based object detection and classification networks. Physical modelling is introduced at three stages of the pipeline in a comparative study. Experiments, ablation studies, and evaluations conducted on the nuScenes dataset and an internal dataset suggest that such hybrid architectures can outperform purely Deep Learning-based approaches and significantly improve semi-supervised performance.

## Key Contributions

- Developed a hybrid perception model that integrates physical modelling into Deep Learning pipelines for radar-based velocity estimation.
- Compared three different physics-informed strategies:
  - Physics-based velocity estimation
  - Physics-derived training labels
  - Physics-based loss functions
- Introduced adaptations to the PINN framework tailored to the velocity estimation problem, simplifying its standard PDE formulation.
- Conducted ablation studies to address and quantify the impact of modelling errors and robustness to incorrect predictions.
- Demonstrated improvements over baseline models in fully supervised and semi-supervised settings.

## Methodology

This study compares four approaches for radar-based velocity estimation:

### 1. Physics-Based Velocity Estimation

Uses a RANSAC-based Least Squares method to estimate the full velocity vector from radar-derived radial velocities.

**[Insert Figure Placeholder: Physics-Based Velocity Estimation Architecture]**

### 2. Physics-Based Labels

Generates training labels using a physics model, enabling both supervised and semi-supervised training regimes.

**[Insert Figure Placeholder: Physics-Based Label Generation]**

### 3. Physics-Based Loss Function

Integrates an additional physics-informed loss term that compares projected velocity profiles against measured radar hits.

**[Insert Figure Placeholder: Physics-Based Loss Function Architecture]**

### 4. Vanilla Deep Learning Baseline

Used as a reference model without any physics-informed components.

## Results

### Quantitative Comparison

Evaluation across multiple object classes (vehicles, large vehicles, riders, pedestrians) using metrics like velocity error, physics error, and average precision.

**[Insert Figure Placeholder: nuScenes Validation Results Comparison]**

### Qualitative Evaluation

Extrapolated predicted trajectories and comparison with ground truth in complex driving scenarios.

**[Insert Figure Placeholder: Rotation Velocity Estimation - Qualitative Results]**

### Semi-Supervision Experiment

Performance comparison with decreasing label availability shows strong resilience of physics-informed methods.

**[Insert Figure Placeholder: Supervision vs. Error Plot]**

## Institutional Affiliation

This research was conducted as part of my Bachelor’s thesis in collaboration with **Robert Bosch GmbH** at the **Bosch Forschungscampus Renningen**, Germany — the central R&D facility of Bosch. The project was supervised by:

- **Prof. Dr.-Ing. Niclas Zeller** (Primary Examiner)  
- **Prof. Dr.-Ing. Serdal Ayhan** (Secondary Examiner)  
- **Dr.-Ing. Jiaying Lin** (Industry Supervisor, Bosch)

The thesis received a **grade of 1.0** (highest possible in the German system) and was awarded a **special distinction** for excellence.

---

