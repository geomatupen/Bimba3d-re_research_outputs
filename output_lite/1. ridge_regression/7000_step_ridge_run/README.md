# 7000-Step Ridge Run

Source pipeline: `pipeline_a745b178abfd` (`Test_7000_Steps`)  
Model: `model_compact-ridge_20260721_195042_ridge_without_intercept_regularization`

This folder stores the 7000-step baseline-vs-Ridge test run outputs separately from the main 5000-step report run and the comparison-model folders.

This `output_lite` copy intentionally excludes preview images. The full image preview folder is available in `outputs/1. ridge_regression/7000_step_ridge_run/best_lowest_7000_previews/`.

## Files

- `eval_metrics_by_checkpoint.csv`: one row per project and evaluation checkpoint. It pairs baseline and Ridge runs at steps 1000, 2000, ..., 7000 and includes PSNR, SSIM, LPIPS, loss, elapsed time, selected multipliers, and hard-cap flags.
- `final_7000_metrics_multipliers.csv`: one row per project using the 7000-step metrics, runtime, Gaussian count, and selected multipliers.
- `project_index_table.csv`: project index, project name, and image count.
- `test_pipeline_runs.json`: baseline and Ridge run records with analytics paths.
- `summary.json`: compact summary of source pipeline and mean 7000-step differences.
- `source_data/test_pipeline/`: copied pipeline registry/state JSON snapshots.
- `model_artifact/`: copied Ridge model artifact used by the run.

## Notes

PSNR and SSIM deltas are calculated as Ridge minus baseline. LPIPS improvement is calculated as baseline LPIPS minus Ridge LPIPS, so positive means better. Runtime and Gaussian deltas are Ridge minus baseline.
