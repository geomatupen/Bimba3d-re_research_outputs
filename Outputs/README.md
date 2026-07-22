# Final Report Outputs

This folder contains the final report output snapshot organized by model family.

## Folders

- `1. ridge_regression/`: final Ridge Regression model artifacts, test results, comparison models, source-data references, previews, and archived analysis files.
- `2. mlp/`: final descriptor-standardized MLP model artifacts, test results, comparison models, source-data references, previews, and archived analysis files.

## Main CSV Files

- `1. ridge_regression/final_ridge_test_metrics_multipliers_descriptors.csv`
- `2. mlp/final_mlp_test_metrics_multipliers_descriptors.csv`

Comparison model folders also include the same kind of 12-project CSV, with runtime, Gaussian counts, final metrics, selected multipliers, and descriptor values.

Each CSV contains 12 test projects with:

- baseline and model runtime in seconds
- runtime delta
- baseline and model Gaussian counts
- Gaussian-count delta and percent change
- selected geometry, appearance, and densification multipliers
- raw PSNR, SSIM, and LPIPS values
- metric deltas, with LPIPS improvement calculated as baseline LPIPS minus model LPIPS
- raw descriptor values before model standardization

## Preview Images

Each main model folder and each comparison model folder includes `best_lowest_5000_previews/`. These folders contain paired baseline/model `preview_005000.png` images for the overall best/lowest projects and the metric-specific best/lowest projects.

## Source Data

Each model folder includes `source_data/`, which contains copied training-data and pipeline JSON references used for the report snapshot.

## Notes

- PSNR, SSIM, and LPIPS are raw Gaussian Splatting evaluation metrics, not normalized values.
- Descriptor values are raw values before standardization.
- Model display names use the report prefixes `A1`, `A2`, `A3`, `B1`, and `B2`.
- The `model_id` and run ID fields are kept as the original stored identifiers for traceability, so one A3 identifier still contains the older creation-time slug `model-to-delete`.
- Hard-cap rows are marked in the CSV with `status=hard_cap_reached`; final PSNR, SSIM, and LPIPS are unavailable for those stopped runs.
