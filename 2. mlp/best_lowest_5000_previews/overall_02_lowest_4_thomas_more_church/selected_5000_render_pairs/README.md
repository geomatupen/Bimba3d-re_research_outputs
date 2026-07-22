# Selected 5000-Step Render Pairs

This folder contains three paired validation renders from the same 5000-step run used by the representative preview above. They are included for visual checking only. The run stores aggregate PSNR, SSIM, and LPIPS at step 5000, but not separate metrics for each rendered view.

- `baseline_render.png`: baseline render for the same validation view
- `model_render.png`: model render for the same validation view
- `baseline_stats_val_step4999.json` and `model_stats_val_step4999.json`: aggregate metrics for the full validation set at step 5000
