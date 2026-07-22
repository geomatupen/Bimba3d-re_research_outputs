# Ridge Regression Outputs

Final report model: `A1_Final_ridge_used_in_report`

Model ID: `model_compact-ridge_20260712_131550_final_offline_data_june_27-training-data-compact-ridge`

Contents:

- `model_artifact/`: copied trained model artifact folder.
- `final_ridge_test_metrics_multipliers_descriptors.csv`: 12-project test table with runtime, Gaussian counts, PSNR, SSIM, LPIPS, selected multipliers, and raw descriptor values.
- `test_pipeline_runs.json`: the 12 matching test-pipeline run records used for this model.
- `comparison_models/`: comparison Ridge model outputs. Each comparison folder includes its own 12-project CSV with runtime, Gaussian counts, final metrics, selected multipliers, and descriptor values.
- `source_data/`: copied pipeline and training-data JSON files used as report references.
- `best_lowest_5000_previews/`: copied preview images where available.

Notes:

- Runtime values are in seconds.
- PSNR, SSIM, and LPIPS values are raw GS evaluation metrics, not normalized values.
- Descriptor values are raw descriptor values before model standardization.
- LPIPS improvement is calculated as baseline LPIPS minus model LPIPS, so positive means better.
- The comparison CSVs include a `model_name` column with the report names `A2` and `A3`. Original `model_id` and run ID values are kept unchanged for traceability.
