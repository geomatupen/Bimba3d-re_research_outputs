# B2_Final_MLP_used_in_report_descriptor_standardized_with_hard_capped_data 5000-Step Preview Images

Each selected project folder contains the baseline and model `preview_005000.png` images copied from the 5000-step Gaussian Splatting runs. A run can contain many saved previews and validation renders; this folder keeps one representative 5000-step preview pair so the visual comparison stays compact.

Rows with missing final PSNR, SSIM, or LPIPS values, such as hard-cap-stopped runs, are skipped when choosing best and lowest projects.

The best/lowest project selection is based on aggregate run metrics for the whole validation set, not on a score for this single preview image.

Overall ranking uses the combined rank across PSNR improvement, SSIM improvement, and LPIPS improvement. LPIPS improvement is `baseline LPIPS - model LPIPS`, so higher is better.

## Overall Best and Lowest Performing

| Type | Folder | Project | Delta PSNR | Delta SSIM | Delta LPIPS |
| --- | --- | --- | ---: | ---: | ---: |
| Overall best | `overall_01_best_pix4d_forensic` | Pix4d_forensic | `+0.678572` | `+0.100348` | `+0.153493` |
| Overall best | `overall_02_best_chatteau_circle_60_and_45_degrees` | Chatteau_circle_60_and_45_degrees | `+0.303268` | `+0.043502` | `+0.075829` |
| Overall lowest | `overall_01_lowest_dji_202402171501_006_ktm20_oblique` | DJI_202402171501_006_KTM20-oblique | `-1.420744` | `-0.072246` | `-0.044984` |
| Overall lowest | `overall_02_lowest_12_maisonneuve_market` | 12-Maisonneuve Market | `-0.582020` | `-0.003465` | `-0.005180` |

## Metric-Specific Best and Lowest Performing

| Metric pick | Folder | Project | Selected delta |
| --- | --- | --- | ---: |
| psnr best | `metric_specific_best_lowest/psnr_best_pix4d_forensic` | Pix4d_forensic | `+0.678572` |
| psnr lowest | `metric_specific_best_lowest/psnr_lowest_dji_202402171501_006_ktm20_oblique` | DJI_202402171501_006_KTM20-oblique | `-1.420744` |
| ssim best | `metric_specific_best_lowest/ssim_best_pix4d_forensic` | Pix4d_forensic | `+0.100348` |
| ssim lowest | `metric_specific_best_lowest/ssim_lowest_dji_202402171501_006_ktm20_oblique` | DJI_202402171501_006_KTM20-oblique | `-0.072246` |
| lpips best | `metric_specific_best_lowest/lpips_best_pix4d_forensic` | Pix4d_forensic | `+0.153493` |
| lpips lowest | `metric_specific_best_lowest/lpips_lowest_dji_202402171501_006_ktm20_oblique` | DJI_202402171501_006_KTM20-oblique | `-0.044984` |

Inside each folder:

- `baseline_preview_005000.png`
- `model_preview_005000.png`
- `metadata.json`
- `selected_5000_render_pairs/` for overall best/lowest folders

Each overall best/lowest project folder also contains `selected_5000_render_pairs/` with three paired baseline/model validation renders from step 5000. These are for visual inspection only; the stored metric JSON is aggregate for the full validation set, not per rendered view.
