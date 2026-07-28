# Bimba3D-re Research Outputs Lite

This lightweight folder contains only CSV, JSON, Markdown, and text files copied from the full `outputs` folder. Images, preview renders, and heavy model binary files are intentionally excluded so the folder can be zipped and shared more easily.

Main code repository: [geomatupen/bimba3d-re](https://github.com/geomatupen/bimba3d-re)

## Data-Sharing Scope

This lightweight copy includes only relevant report-facing outputs, selected checkpoint results, metadata, and traceability files. It does not include raw image datasets or every intermediate reconstruction artifact because some source datasets are private or institutionally provided, and the full processing outputs would be very large.

Primary report tables:

- `1. ridge_regression/final_ridge_test_metrics_multipliers_descriptors.csv`
- `2. mlp/final_mlp_test_metrics_multipliers_descriptors.csv`

The separate 7000-step Ridge run is included at `1. ridge_regression/7000_step_ridge_run/`, with paired baseline/Ridge checkpoint metrics but no preview images.

The copied source pipeline snapshots may include historical runs and are kept only for traceability.
