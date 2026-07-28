# Bimba3D-re Research Outputs

This folder contains the digital research outputs for the thesis **AI-Guided Optimization for 3D Gaussian Splatting on Drone Images**. The files were exported from the Bimba3D-re platform and organized for traceability with the thesis report.

For final submission, this package may be renamed to `oli26`. The submitted `oli26` folder is intended to contain the relevant folders from this `outputs` directory, excluding the private/local `output_lite` helper folder, together with the selected splat and RAD visualization files described below.

Main code repository: [geomatupen/bimba3d-re](https://github.com/geomatupen/bimba3d-re)

## Data-Sharing Scope

This submission does not include every intermediate file produced during processing. Only the relevant report-facing outputs, selected checkpoint results, metadata, and traceability files are shared here. The complete raw image datasets and all intermediate reconstruction artifacts are not redistributed because some datasets are private or institutionally provided, and the full processing outputs would be very large. Public source datasets are referenced in the thesis report where applicable.

## Start Here

Use `file_manifest.csv` as the evaluator-facing index. It maps the file and folder names in this directory to the terminology used in the thesis report, including the relevant report sections and appendices.

The original platform-oriented names are mostly preserved intentionally. Names such as `compact_featurewise`, `descriptor_standardized`, and pipeline IDs are internal export names from the platform or notebooks. They are kept so that the data can be traced back to the original model and pipeline artifacts.

## Main Folders

- `1. ridge_regression/`: final Ridge Regression scoring model outputs, supporting comparison models, preview renders, and the 7,000-iteration Ridge checkpoint export.
- `2. mlp/`: final MLP scoring model outputs, supporting comparison model, and preview renders.
- `splats_test/`: static RAD files used by the interactive results visualization platform for selected 3DGS viewer cases.

## Additional 3D Visualization Files in Final `oli26` Package

The final `oli26` package may also include the following folders copied from the local staging folder `E:\Thesis\oli26`:

| Folder | What it contains | Purpose |
| --- | --- | --- |
| `splat_files/` | Selected original `.splat` checkpoint files for Maisonneuve Market, Pix4D Forensic, and Thomas More Church. These include baseline and model-selected outputs for Ridge Regression and MLP at 5,000 iterations, plus Ridge Regression at 7,000 iterations. | Source splat checkpoints for the selected interactive visualization cases. |
| `other_full_30k_splats/` | Additional full 30,000-iteration splat examples: `chatteau_best.splat` and `podoli_best.splat`. | Higher-training-step examples included as supplementary visualization material. |
| `rag/` | Converted static RAD scene folders for all selected `splat_files/` cases and the two additional 30,000-iteration examples. | Browser-ready static 3D visualization data used by the interactive results platform. |

The `.splat` files are the original checkpoint exports, while `rag/` contains the converted static RAD format used for efficient browser loading. These folders are selected visualization data only; they are not a complete archive of all reconstruction runs.

## File Summary

| Report reference | Folder or file | What it contains |
| --- | --- | --- |
| Appendix 1; Section 3.2 | Thesis report Appendix 1 | Dataset inventory, project identifiers, study partition, image counts, locations, resolutions, and data sources. Raw datasets are referenced rather than redistributed. |
| Sections 4.2, 4.2.5, 6.2 | `1. ridge_regression/source_data/training_data_20260710_183008_final_offline_data_june_27-training-data/rows.json` | Training rows created from completed exploration runs. Each row links project descriptors, a tested multiplier combination, and the relative quality score. |
| Sections 4.3.2, 6.3; Appendix 2 | `1. ridge_regression/compact_featurewise_ridge_coefficients.csv` | Coefficients of the final Ridge Regression scoring model. |
| Sections 4.4, 6.4.1; Appendices 3A, 3B | `1. ridge_regression/final_ridge_test_metrics_multipliers_descriptors.csv` | Main Ridge Regression result table with quality metrics, selected multiplier combinations, Gaussian-count results, runtime results, and descriptors. |
| Sections 4.4, 6.4.2; Appendices 3C, 3D | `2. mlp/final_mlp_test_metrics_multipliers_descriptors.csv` | Main MLP result table with quality metrics, selected multiplier combinations, Gaussian-count results, runtime results, and descriptors. |
| Section 6.4; Appendices 3A-3D | `1. ridge_regression/project_index_table.csv` and `2. mlp/project_index_table.csv` | Stable project index used by report tables and project-wise charts. |
| Section 6.4.3 | `1. ridge_regression/comparison_models/` and `2. mlp/comparison_models/` | Supporting model comparisons, including hard-cap-data comparison models and the additional Ridge run using the same selected multipliers. |
| Section 6.4.4; Appendix 3E | `1. ridge_regression/7000_step_ridge_run/` | Extended Ridge checkpoint comparison up to 7,000 iterations. |
| Appendix 3E | `1. ridge_regression/7000_step_ridge_run/attachment_3e_checkpoint_comparison_ascii.csv` | Report-ready checkpoint comparison table for baseline and Ridge model-selected runs. |
| Section 6.5.2 | `splats_test/` | Static RAD files and manifests for selected interactive 3D visualization cases. |
| Section 6.5.2 | `splat_files/`, `other_full_30k_splats/`, `rag/` in final `oli26` package | Selected original splat checkpoints and converted RAD visualization files staged from `E:\Thesis\oli26`. |

For a more detailed file-by-file explanation, see `file_manifest.csv`.

## Primary Report Tables

- `1. ridge_regression/final_ridge_test_metrics_multipliers_descriptors.csv`: Ridge Regression test-project quality metrics, selected multiplier combinations, Gaussian-count results, runtime results, and descriptors.
- `2. mlp/final_mlp_test_metrics_multipliers_descriptors.csv`: MLP test-project quality metrics, selected multiplier combinations, Gaussian-count results, runtime results, and descriptors.
- `1. ridge_regression/7000_step_ridge_run/attachment_3e_checkpoint_comparison_ascii.csv`: checkpoint comparison between baseline and Ridge model-selected runs.

## Report Links

- Dataset inventory: Appendix 1 and Section 3.2.
- Training-data preparation: Sections 4.2, 6.2.
- Ridge Regression scoring model: Sections 4.3.2, 6.3, 6.4.1.
- MLP scoring model: Sections 4.3.3, 6.3, 6.4.2.
- Supporting model comparisons: Section 6.4.3.
- 7,000-iteration Ridge checkpoint results: Section 6.4.4 and Appendix 3E.

## Notes

- Runtime values are stored in seconds.
- PSNR and SSIM differences are calculated as model-selected value minus baseline value; positive values indicate improvement.
- LPIPS improvement is calculated as baseline value minus model-selected value; positive values indicate improvement.
- Hard-cap rows are retained to preserve the 12-project test index. Where final metrics are unavailable because a run reached the Gaussian hard cap, the hard-cap metadata columns identify the cap, step, and Gaussian count.
- `source_data/` folders contain traceability snapshots from the original platform pipelines and may include historical records. The final report tables are the CSV files identified in `file_manifest.csv`.
