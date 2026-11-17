# Geosteering research brief

## Purpose

Document and evaluate a transparent descriptive workflow for relating a measured-depth well trajectory and log samples to a user-supplied target interval. The supplied HTML tool is a visualization and summary prototype, not a geosteering decision engine.

## Research questions

1. How sensitive are in-target footage and target-run summaries to sample spacing and interpolation rules?
2. How do uncertainty in trajectory TVDSS and target top/base alter zone classification?
3. How stable are descriptive zone comparisons when logs contain missing values, measurement noise, or depth misalignment?
4. Which cutoff-based net-pay summaries remain reproducible across analysts and datasets?

## Included tool behavior

The HTML application groups each sampled point as above, in target, or below target using TVDSS and target boundaries. It calculates interval lengths from adjacent measured-depth samples; presents median log values by zone; displays a section view and lateral tracks; and provides distribution, crossplot, and cutoff-based net-pay exploration. It supports imported CSV and optional simulated/WebSocket/REST feeds.

The application does not implement probabilistic trajectory/formation uncertainty, statistical significance tests, predictive modeling, or automatic steering recommendations. The included research questions describe possible extensions, not existing capabilities.

## Suggested validation

- Create truth-known synthetic trajectories with controlled sample spacing, curvature, boundary variation, and noise.
- Compare row-wise classifications against a documented continuous/interpolated reference at a fixed MD grid.
- Test repeated measurements, missing logs, duplicate/unsorted MD, unit errors, and boundary crossings.
- Conduct a blind comparison with independently interpreted intervals, recording disagreement and uncertainty rather than forcing labels.
- Publish versioned synthetic fixtures and expected outputs before evaluating field cases.

## Data handling

Use synthetic or properly licensed data in the public repository. Remove well identifiers and coordinates if required by the data agreement; anonymization does not itself grant redistribution rights. Document units, sampling interval, depth reference, datum, log provenance, cutoff definitions, and missing-value conventions. Keep proprietary well data outside Git.

## Interpretation boundary

The code reports summaries conditional on supplied samples, target geometry, and cutoffs. It does not establish geological truth, net-pay status, hydrocarbon reserves, or an optimal steering action. Operational use requires independent validation, qualified interpretation, and integration under the operator's approved workflow.
