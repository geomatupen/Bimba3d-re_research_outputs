# 7000-Step Ridge Run

Source pipeline: `pipeline_a745b178abfd` (`Test_7000_Steps`)  
Model: `model_compact-ridge_20260721_195042_ridge_without_intercept_regularization`

This folder stores the 7000-step baseline-vs-Ridge test run outputs separately from the main 5000-step report run and the comparison-model folders.

## Files

- `eval_metrics_by_checkpoint.csv`: one row per project and evaluation checkpoint. It pairs baseline and Ridge runs at steps 1000, 2000, ..., 7000 and includes PSNR, SSIM, LPIPS, loss, elapsed time, selected multipliers, and hard-cap flags.
- `attachment_3e_checkpoint_comparison.md` and `attachment_3e_checkpoint_comparison.csv`: report-ready Attachment 3E table comparing 5,000- and 7,000-step baseline/Ridge PSNR, SSIM, and LPIPS values.
- `final_7000_metrics_multipliers.csv`: one row per project using the 7000-step metrics, runtime, Gaussian count, and selected multipliers.
- `project_index_table.csv`: project index, project name, and image count.
- `test_pipeline_runs.json`: baseline and Ridge run records with analytics paths.
- `summary.json`: compact summary of source pipeline and mean 7000-step differences.
- `source_data/test_pipeline/`: copied pipeline registry/state JSON snapshots.
- `model_artifact/`: copied Ridge model artifact used by the run.
- `best_lowest_7000_previews/`: baseline and Ridge preview images for the two highest and two lowest overall 7000-step projects, plus metric-specific best/lowest examples.

## Notes

PSNR and SSIM deltas are calculated as Ridge minus baseline. LPIPS improvement is calculated as baseline LPIPS minus Ridge LPIPS, so positive means better. Runtime and Gaussian deltas are Ridge minus baseline.
