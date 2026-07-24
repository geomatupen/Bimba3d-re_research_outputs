# Ridge Regression Outputs

Final report model: `A1_Final_ridge_used_in_report`

Model ID: `model_compact-ridge_20260721_195042_ridge_without_intercept_regularization`

Contents:

- `model_artifact/`: copied trained model artifact folder.
- `final_ridge_test_metrics_multipliers_descriptors.csv`: 12-project test table with runtime, Gaussian counts, PSNR, SSIM, LPIPS, selected multipliers, and raw descriptor values.
- `project_index_table.csv`: stable project index used by report charts and CSV rows.
- `test_pipeline_runs.json`: the 12 matching test-pipeline run records used for this model.
- `comparison_models/`: rebuilt comparison outputs from actual pipeline runs. Included comparisons: A2_Final_ridge_used_in_report_trained_with_hard_capped_data, A3_Ridge_additional_run_with_same_multipliers.
- `source_data/`: copied source pipeline/model/training reference files. The test pipeline snapshot may contain historical runs; the final report rows are the 12 rows in the final CSV.
- `best_lowest_5000_previews/`: copied preview images where available.

Notes:

- Runtime values are in seconds.
- PSNR, SSIM, and LPIPS values are raw GS evaluation metrics, not normalized values.
- Descriptor values are raw descriptor values before model standardization.
- LPIPS improvement is calculated as baseline LPIPS minus model LPIPS, so positive means better.
- Hard-cap rows are kept in the tables to preserve the 12-project index. Their metric improvement columns are set to `0.0`, and the hard-cap metadata columns identify the cap, step, and Gaussian count.
