# Bimba3D-re Research Outputs

This folder contains the reported research outputs for the thesis **AI-Guided Optimization for 3D Gaussian Splatting on Drone Images**. The files were exported from the Bimba3D-re platform and organized for traceability with the thesis report.

Main code repository: [geomatupen/bimba3d-re](https://github.com/geomatupen/bimba3d-re)

Interactive results platform repository: [geomatupen/Thesis-Results-Platform](https://github.com/geomatupen/Thesis-Results-Platform)

Interactive results platform website: [https://geomatupen.github.io/Thesis-Results-Platform/](https://geomatupen.github.io/Thesis-Results-Platform/)

## Data-Sharing Scope

This submission does not include every intermediate file produced during processing. Only the relevant report-facing result tables, selected checkpoint metrics, metadata, and traceability files are shared here. The complete raw image datasets and all intermediate reconstruction artifacts are not redistributed because some datasets are private or institutionally provided, and the full processing outputs would be very large. Public source datasets are referenced in the thesis report where applicable.

Selected `.splat` checkpoint files and converted browser-ready RAD visualization files are provided separately in the final digital submission package.

## Data Index

The table below gives the main structure of this research-output package. It lists each main folder and the important one-level subfolders or files inside it. For exact file paths and report mapping, see `file_manifest.csv`.

Section and appendix references in this README refer to the final thesis report: [thesis_report_upendra_oli_2026.pdf](https://www.geoinformatics.upol.cz/dprace/magisterske/oli26/assets/downloads/thesis_report_upendra_oli_2026.pdf).

| SN | Folder | Subfolder/file | Description |
| --- | --- | --- | --- |
| 1 | `1. ridge_regression/` | Main folder | Final Ridge Regression outputs: model, test results, comparisons, previews, and checkpoint data; see Sections 4.3.2, 6.3, 6.4.1. |
| 1.1 |  | <span title="final_ridge_test_metrics_multipliers_descriptors.csv">`final_ridge...csv`</span> | Main Ridge test table with quality metrics, selected multipliers, Gaussian count, runtime, and descriptors; see Appendices 3A, 3B. |
| 1.2 |  | `model_artifact/` | Stored final Ridge scoring model used to score candidate multiplier combinations; see Sections 4.3.2, 6.3. |
| 1.3 |  | `analysis_model_files/` | Ridge coefficient and model-analysis files used to interpret model terms; see Appendix 2. |
| 1.4 |  | `comparison_models/` | Supporting Ridge comparison runs, including hard-cap-data and repeated-multiplier checks; see Section 6.4.3. |
| 1.5 |  | `7000_step_ridge_run/` | Baseline and Ridge model-selected comparison extended to 7,000 iterations; see Section 6.4.4 and Appendix 3E. |
| 1.6 |  | `best_lowest_5000_previews/` | Selected best and lowest Ridge test-project preview results at 5,000 iterations; see Section 6.4.1. |
| 1.7 |  | `source_data/` | Platform exports used for traceability: training data, test descriptors, and pipeline snapshots; see Sections 4.2-4.4. |
| 2 | `2. mlp/` | Main folder | Final MLP outputs: model, test results, supporting comparison, previews, and traceability files; see Sections 4.3.3, 6.3, 6.4.2. |
| 2.1 |  | <span title="final_mlp_test_metrics_multipliers_descriptors.csv">`final_mlp...csv`</span> | Main MLP test table with quality metrics, selected multipliers, Gaussian count, runtime, and descriptors; see Appendices 3C, 3D. |
| 2.2 |  | `model_artifact/` | Stored final compact MLP scoring model used as the nonlinear comparison model; see Sections 4.3.3, 6.3. |
| 2.3 |  | `analysis_model_files/` | MLP metadata and model-analysis files for the final compact model; see Section 6.3. |
| 2.4 |  | `comparison_models/` | Supporting MLP comparison trained with hard-cap rows; see Section 6.4.3. |
| 2.5 |  | `best_lowest_5000_previews/` | Selected best and lowest MLP test-project preview results at 5,000 iterations; see Section 6.4.2. |
| 2.6 |  | `source_data/` | Platform exports used for traceability: training data, test descriptors, and pipeline snapshots; see Sections 4.2-4.4. |

## Notes

- Runtime values are stored in seconds.
- PSNR and SSIM differences are calculated as model-selected value minus baseline value; positive values indicate improvement.
- LPIPS improvement is calculated as baseline value minus model-selected value; positive values indicate improvement.
- A hard-cap run is a run that reached the configured Gaussian-count limit before producing final quality metrics. These rows are kept in the result tables to preserve the 12-project test index, and the hard-cap metadata columns record where the limit was reached.
- Splat and RAD visualization files are selected examples only, not a complete archive of all reconstruction runs.
