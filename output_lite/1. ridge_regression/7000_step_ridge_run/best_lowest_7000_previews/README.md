# Highest and Lowest Performing 7000-Step Preview Snapshots

Source pipeline: `pipeline_a745b178abfd` (`Test_7000_Steps`)
Model: `model_compact-ridge_20260721_195042_ridge_without_intercept_regularization`

Rankings use the 7000-step paired baseline and Ridge metrics. PSNR and SSIM use Ridge minus baseline; LPIPS uses baseline minus Ridge, so positive is better.

- overall best: project 8 `Pix4d_forensic`; PSNR delta 0.575865, SSIM delta 0.135116, LPIPS improvement 0.233564.
- overall best: project 11 `morice`; PSNR delta 1.31968, SSIM delta 0.0531029, LPIPS improvement 0.0967003.
- overall lowest: project 6 `DJI_202402171501_006_KTM20-oblique`; PSNR delta -0.812706, SSIM delta -0.00675654, LPIPS improvement 0.020955.
- overall lowest: project 2 `4-Thomas-More-Church`; PSNR delta -0.0118103, SSIM delta 0.00388569, LPIPS improvement 0.00170565.

The metric-specific folder contains the best and lowest project for each individual metric.
