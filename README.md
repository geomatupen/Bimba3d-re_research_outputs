# Bimba3D-re Research Outputs

This folder contains the digital research outputs for the thesis **AI-Guided Optimization for 3D Gaussian Splatting on Drone Images**. The files were exported from the Bimba3D-re platform and organized for traceability with the thesis report.

Main code repository: [geomatupen/bimba3d-re](https://github.com/geomatupen/bimba3d-re)

## Data-Sharing Scope

This submission does not include every intermediate file produced during processing. Only the relevant report-facing outputs, selected checkpoint results, metadata, traceability files, and selected visualization files are shared here. The complete raw image datasets and all intermediate reconstruction artifacts are not redistributed because some datasets are private or institutionally provided, and the full processing outputs would be very large. Public source datasets are referenced in the thesis report where applicable.

## Data Index

The table below gives the main structure of this data package and links the folders to the terminology used in the thesis report. For more detailed file-level information, see `file_manifest.csv`.

| Report reference | Folder or file | Contents |
| --- | --- | --- |
| Appendix 1; Section 3.2 | Thesis report Appendix 1 | Dataset inventory, project identifiers, study partition, image counts, locations, resolutions, and data sources. Raw datasets are referenced in the report rather than redistributed here. |
| Sections 4.2, 4.2.5, 6.2 | `1. ridge_regression/source_data/training_data_20260710_183008_final_offline_data_june_27-training-data/` | Training-data export used by the final scoring models. The main `rows.json` file stores completed exploration runs as training rows with project descriptors, tested multiplier combinations, and relative quality scores. |
| Sections 4.3.2, 6.3; Appendix 2 | `1. ridge_regression/model_artifact/` and `1. ridge_regression/analysis_model_files/` | Final Ridge Regression scoring model artifact and model-analysis files, including the coefficient table used for Appendix 2. |
| Sections 4.4, 6.4.1; Appendices 3A, 3B | `1. ridge_regression/final_ridge_test_metrics_multipliers_descriptors.csv` | Main Ridge Regression result table with quality metrics, selected multiplier combinations, Gaussian-count results, runtime results, and descriptors. |
| Section 6.4.3 | `1. ridge_regression/comparison_models/` | Supporting Ridge comparison outputs, including the model trained with hard-cap rows and the additional run using the same selected multipliers. |
| Section 6.4.4; Appendix 3E | `1. ridge_regression/7000_step_ridge_run/` | Extended Ridge checkpoint comparison up to 7,000 iterations. The report-ready checkpoint table is `attachment_3e_checkpoint_comparison_ascii.csv`; the filename keeps its earlier export name, but it corresponds to Appendix 3E. |
| Sections 4.3.3, 6.3 | `2. mlp/model_artifact/` and `2. mlp/analysis_model_files/` | Final compact MLP scoring model artifact and related model-analysis files. |
| Sections 4.4, 6.4.2; Appendices 3C, 3D | `2. mlp/final_mlp_test_metrics_multipliers_descriptors.csv` | Main MLP result table with quality metrics, selected multiplier combinations, Gaussian-count results, runtime results, and descriptors. |
| Section 6.4.3 | `2. mlp/comparison_models/` | Supporting MLP comparison output for the model trained with hard-cap rows. |
| Section 6.4; Appendices 3A-3D | `1. ridge_regression/project_index_table.csv` and `2. mlp/project_index_table.csv` | Stable project index used by report tables and project-wise charts. |
| Sections 6.4.1, 6.4.2, 6.5.2 | `1. ridge_regression/best_lowest_5000_previews/` and `2. mlp/best_lowest_5000_previews/` | Preview renders and metadata for selected best and lowest improvement cases at the 5,000-iteration checkpoint. |
| Section 6.4.4 | `1. ridge_regression/7000_step_ridge_run/best_lowest_7000_previews/` | Preview renders and metadata for selected 7,000-iteration Ridge checkpoint cases. |
| Section 6.5.2 | `splats_test/` | Static RAD files and manifests for selected interactive 3D visualization cases used by the results visualization platform. |
| Section 6.5.2 | `splat_files/` | Selected original `.splat` checkpoint files for Maisonneuve Market, Pix4D Forensic, and Thomas More Church, including baseline and model-selected outputs for Ridge Regression and MLP at 5,000 iterations and Ridge Regression at 7,000 iterations. |
| Section 6.5.2 | `other_full_30k_splats/` | Additional full 30,000-iteration splat examples: `chatteau_best.splat` and `podoli_best.splat`. |
| Section 6.5.2 | `rag/` | Converted static RAD scene folders for the selected `.splat` checkpoints and the two additional 30,000-iteration examples. These are browser-ready visualization files. |
| Traceability | `source_data/` folders inside model folders | Pipeline snapshots, test descriptors, and training-data references exported from Bimba3D-re. These files support traceability but may include historical records; final report values should be read from the final CSV files listed above. |

## Notes

- Runtime values are stored in seconds.
- PSNR and SSIM differences are calculated as model-selected value minus baseline value; positive values indicate improvement.
- LPIPS improvement is calculated as baseline value minus model-selected value; positive values indicate improvement.
- A hard-cap run is a run that reached the configured Gaussian-count limit before producing final quality metrics. These rows are kept in the result tables to preserve the 12-project test index, and the hard-cap metadata columns record where the limit was reached.
- The `.splat` files are original checkpoint exports, while `rag/` contains converted static RAD files for browser visualization. These visualization folders are selected examples only, not a complete archive of all reconstruction runs.
