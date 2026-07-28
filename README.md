# Bimba3D-re Research Outputs

This folder contains the digital research outputs for the thesis **AI-Guided Optimization for 3D Gaussian Splatting on Drone Images**. The files were exported from the Bimba3D-re platform and organized for traceability with the thesis report.

Main code repository: [geomatupen/bimba3d-re](https://github.com/geomatupen/bimba3d-re)

## Data-Sharing Scope

This submission does not include every intermediate file produced during processing. Only the relevant report-facing outputs, selected checkpoint results, metadata, traceability files, and selected visualization files are shared here. The complete raw image datasets and all intermediate reconstruction artifacts are not redistributed because some datasets are private or institutionally provided, and the full processing outputs would be very large. Public source datasets are referenced in the thesis report where applicable.

## Data Index

The table below gives the main structure of this data package. It lists each main folder and the important one-level subfolders or files inside it. For exact file paths and report mapping, see `file_manifest.csv`.

| SN | Folder | Subfolder/file | Description |
| --- | --- | --- | --- |
| 1 | `1. ridge_regression/` | Main folder | Final Ridge outputs; see Sections 4.3.2, 6.3, 6.4.1. |
| 2 | `1. ridge_regression/` | `final_ridge...csv` | Main Ridge test table; see Appendices 3A, 3B. |
| 3 | `1. ridge_regression/` | `model_artifact/` | Final Ridge scoring model; see Sections 4.3.2, 6.3. |
| 4 | `1. ridge_regression/` | `analysis_model_files/` | Ridge coefficients and analysis; see Appendix 2. |
| 5 | `1. ridge_regression/` | `comparison_models/` | Supporting Ridge comparisons; see Section 6.4.3. |
| 6 | `1. ridge_regression/` | `7000_step_ridge_run/` | Ridge 7,000-step checkpoint comparison; see Section 6.4.4 and Appendix 3E. |
| 7 | `1. ridge_regression/` | `best_lowest_5000_previews/` | Selected Ridge preview renders; see Section 6.4.1. |
| 8 | `1. ridge_regression/` | `source_data/` | Ridge traceability exports for training data, descriptors, and pipelines; see Sections 4.2-4.4. |
| 9 | `2. mlp/` | Main folder | Final MLP outputs; see Sections 4.3.3, 6.3, 6.4.2. |
| 10 | `2. mlp/` | `final_mlp...csv` | Main MLP test table; see Appendices 3C, 3D. |
| 11 | `2. mlp/` | `model_artifact/` | Final compact MLP scoring model; see Sections 4.3.3, 6.3. |
| 12 | `2. mlp/` | `analysis_model_files/` | MLP model metadata and analysis files; see Section 6.3. |
| 13 | `2. mlp/` | `comparison_models/` | Supporting MLP comparison; see Section 6.4.3. |
| 14 | `2. mlp/` | `best_lowest_5000_previews/` | Selected MLP preview renders; see Section 6.4.2. |
| 15 | `2. mlp/` | `source_data/` | MLP traceability exports for training data, descriptors, and pipelines; see Sections 4.2-4.4. |
| 16 | `splats_test/` | Scene folders | Static RAD viewer data for selected cases; see Section 6.5.2. |
| 17 | `splat_files/` | `.splat` files | Original selected checkpoint splats; see Section 6.5.2. |
| 18 | `other_full_30k_splats/` | `.splat` files | Additional 30,000-iteration splat examples; see Section 6.5.2. |
| 19 | `rag/` | Scene folders | Converted browser-ready RAD scenes; see Section 6.5.2. |

## Notes

- Runtime values are stored in seconds.
- PSNR and SSIM differences are calculated as model-selected value minus baseline value; positive values indicate improvement.
- LPIPS improvement is calculated as baseline value minus model-selected value; positive values indicate improvement.
- A hard-cap run is a run that reached the configured Gaussian-count limit before producing final quality metrics. These rows are kept in the result tables to preserve the 12-project test index, and the hard-cap metadata columns record where the limit was reached.
- The `.splat` files are original checkpoint exports, while `rag/` contains converted static RAD files for browser visualization. These visualization folders are selected examples only, not a complete archive of all reconstruction runs.
