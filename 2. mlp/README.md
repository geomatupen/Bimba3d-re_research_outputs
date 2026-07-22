# MLP Outputs

Final report model: `B1_Final_MLP_used_in_report_descriptor_standardized`

Model ID: `model_compact-mlp_20260720_203745_final_mlp_descriptor_standardized`

Contents:

- `model_artifact/`: copied trained model artifact folder.
- `final_mlp_test_metrics_multipliers_descriptors.csv`: 12-project test table with runtime, Gaussian counts, PSNR, SSIM, LPIPS, selected multipliers, and raw descriptor values.
- `project_index_table.csv`: stable project index used by the report charts and CSV rows.
- `test_pipeline_runs.json`: the 12 matching test-pipeline run records used for this model.
- `comparison_models/`: comparison MLP model outputs. Each comparison folder includes its own 12-project CSV with runtime, Gaussian counts, final metrics, selected multipliers, and descriptor values.
- `source_data/`: copied pipeline and training-data JSON files used as report references.
- `best_lowest_5000_previews/`: copied preview images where available.

Notes:

- Runtime values are in seconds.
- PSNR, SSIM, and LPIPS values are raw GS evaluation metrics, not normalized values.
- Descriptor values are raw descriptor values before model standardization.
- LPIPS improvement is calculated as baseline LPIPS minus model LPIPS, so positive means better.
- Hard-cap rows are kept in the table to preserve the 12-project index. Their metric improvement columns are set to `0.0`, and the hard-cap metadata columns identify the cap, step, and Gaussian count.
- The comparison CSV includes a `model_name` column with the report name `B2`. Original `model_id` and run ID values are kept unchanged for traceability.
