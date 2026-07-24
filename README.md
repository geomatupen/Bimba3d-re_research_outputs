# Bimba3D-re Research Outputs

This folder contains report-ready outputs rebuilt from the actual Bimba3D-re pipeline/model artifacts.

Main code repository: [geomatupen/bimba3d-re](https://github.com/geomatupen/bimba3d-re)

- `1. ridge_regression/`: final Ridge Regression report outputs, Ridge comparison models, and the separate 7000-step Ridge run export.
- `2. mlp/`: final MLP report outputs and MLP comparison model.

Use the main 12-row CSV inside each model folder as the report table:

- `1. ridge_regression/final_ridge_test_metrics_multipliers_descriptors.csv`
- `2. mlp/final_mlp_test_metrics_multipliers_descriptors.csv`

The 7000-step Ridge run is stored separately at `1. ridge_regression/7000_step_ridge_run/`. Its checkpoint CSV contains paired baseline and Ridge metrics at 1000-step intervals from 1000 to 7000.

The source pipeline snapshots may contain historical runs. They are included for traceability, but the final report tables are the CSV files listed above.
