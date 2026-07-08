# FIDELIS

**FIDELIS** is an open-source tool that evaluates the **calibration** and **robustness** of trained
deep-learning (DL) models in cancer imaging and returns a **clinician-facing reliability report**.

It operates **post-hoc**, using only a model's outputs — **no retraining and no access to the original
training data** — so it can audit any trained segmentation or outcome-prediction model before deployment.

> Standard scores (Dice, AUC) measure only average accuracy. FIDELIS answers, *before* a model is deployed:
> **where is it overconfident, does that failure change a clinical decision, and does it hold up under
> realistic scanner variation?**

## Components
- **FIDELIS-Calibrate** — post-hoc calibration assessment (Anatomy-Aware ECE / ΔA-ECE) and recalibration maps.
- **FIDELIS-Robust** — stability under simulated scanner / dose / protocol variation.
- **Clinical Decision Impact (CDI)** — maps reliability failures to potential changes in a clinical decision.

## Status
Early development under **NCI ITCR (RFA-CA-27-019, U01)**. APIs and thresholds are being finalized;
interfaces may change before the first tagged release.

## Interoperability
Adapters planned for widely used cancer-imaging pipelines (**MONAI**, **nnU-Net**) so any project can run
FIDELIS on its own models as a post-hoc reliability check.

## License
Released under the **Apache License 2.0** — see [LICENSE](LICENSE). Free for academic and commercial use,
modification, and incorporation into other software.

## Citation
If you use FIDELIS, please cite the project (a DOI will be minted via Zenodo at first release).
