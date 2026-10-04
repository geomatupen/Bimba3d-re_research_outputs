# Final Test June 27 comparison

Source pipeline: `pipeline_5df0ad97ef5a` (`Final_test_June_27`).

Generated with:

```powershell
python scripts/export_controlled_comparison.py pipeline_5df0ad97ef5a --output-dir docs/comparison/final_test_june_27
```

## Files

- `compare.csv`: one summary row for each of the 12 projects.
- `compare_checkpoints.csv`: all available evaluation checkpoints for the baseline, referenced selected-model run, time control, and Gaussian control.

## Partial DJI Gaussian Run

The DJI Gaussian-controlled run was interrupted after training reached approximately step 10,200. It contains ten complete evaluations through step 10,000. These checkpoints are included with `run_status=partial`.

In `compare.csv`, its `gaussian_control_record_kind` is `partial_last_observed`, `gaussian_control_final_step` is blank, and `gaussian_control_last_observed_step` is 10000. Do not include it in completed-run aggregates or describe the 10k checkpoint as its final result.

## Definitions

- `training_seconds` is recorded before evaluation at the reported checkpoint and excludes export, but includes earlier scheduled evaluations executed inside the training loop. If one of those evaluations carries elapsed time past the target, the stop is detected after the next training step and the final time can overshoot.
- `metric_training_seconds` is the loop time at the checkpoint that supplied PSNR, SSIM, and LPIPS. This can differ from run duration when a selected-model run ended at the Gaussian hard cap after its last evaluation.
- `reported_total_seconds` is the broader analytics total and can include evaluation and post-training work.
- `loss_step` is retained separately because loss and quality metrics are not always recorded at the same step.
- Positive `*_vs_model` and `*_vs_baseline` values mean the checkpoint performed better. LPIPS differences are reversed because lower LPIPS is better.
- `meets_model_all` requires PSNR and SSIM to be at least the selected model's values and LPIPS to be no greater, all at the same recorded checkpoint.
- `first_match_*` is the earliest observed crossing. `sustained_match_*` is the earliest crossing that remains satisfied at all later available evaluations.

Blank match fields mean the condition was never met at a recorded checkpoint. A crossing between evaluation steps cannot be located more precisely from the saved data.

## Charts

Every chart is provided as a 300 DPI PNG for direct slide use and as an SVG for lossless resizing.

### Grouped slide charts

These six figures are the current presentation set. Quality is shown with grouped Baseline, Selected model, and Control bars on the truncated left axis. Selected-model and controlled-run training times are overlaid as dots against the zero-based seconds axis on the right. Above every project, rotated annotations report the experiment target and the selected-model/control step, exact training-loop time, and Gaussian count. This directly connects each quality result to its computational cost.

- `time_psnr_grouped_comparison`, `time_ssim_grouped_comparison`, `time_lpips_grouped_comparison`
- `gaussian_psnr_grouped_comparison`, `gaussian_ssim_grouped_comparison`, `gaussian_lpips_grouped_comparison`

Regenerate this set with:

```powershell
python scripts/create_grouped_control_charts.py
```

The previous table-based versions, including their visual-quality-index match results and formula, are retained in `archive_charts`.

### Better/worse summary

`controlled_better_worse_summary` contains six bars: PSNR, SSIM, and LPIPS for each controlled experiment. Each bar reports the completed-project counts that were better or worse than the model-selected run. The unfinished DJI Gaussian-controlled run is excluded.

Regenerate it with:

```powershell
python scripts/create_control_summary_charts.py
```
