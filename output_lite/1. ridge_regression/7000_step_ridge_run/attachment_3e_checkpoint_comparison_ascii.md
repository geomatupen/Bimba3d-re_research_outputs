# Appendix 3E Checkpoint Comparison of Baseline and Ridge Model-Selected Runs

| No. | Project | Base PSNR 5k | Ridge PSNR 5k | Delta PSNR 5k | Base PSNR 7k | Ridge PSNR 7k | Delta PSNR 7k | Base SSIM 5k | Ridge SSIM 5k | Delta SSIM 5k | Base SSIM 7k | Ridge SSIM 7k | Delta SSIM 7k | Base LPIPS 5k | Ridge LPIPS 5k | LPIPS impr. 5k | Base LPIPS 7k | Ridge LPIPS 7k | LPIPS impr. 7k |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | Maisonneuve Market | 16.899 | 16.983 | +0.083 | 17.225 | 17.500 | +0.275 | 0.648 | 0.653 | +0.005 | 0.656 | 0.663 | +0.007 | 0.488 | 0.476 | +0.011 | 0.466 | 0.450 | +0.016 |
| 2 | Thomas More Church | 21.401 | 21.941 | +0.540 | 22.203 | 22.191 | -0.012 | 0.780 | 0.792 | +0.012 | 0.796 | 0.800 | +0.004 | 0.295 | 0.285 | +0.010 | 0.269 | 0.267 | +0.002 |
| 3 | Brasov | 23.465 | 23.419 | -0.046 | 24.209 | 24.074 | -0.135 | 0.812 | 0.817 | +0.005 | 0.829 | 0.835 | +0.006 | 0.181 | 0.166 | +0.014 | 0.157 | 0.141 | +0.016 |
| 4 | Changunarayan Temple | 20.063 | 19.974 | -0.089 | 20.425 | 20.405 | -0.021 | 0.623 | 0.633 | +0.010 | 0.641 | 0.660 | +0.018 | 0.516 | 0.488 | +0.029 | 0.483 | 0.439 | +0.044 |
| 5 | Chateau Divci Hrad - Circular Flight | 23.399 | 23.898 | +0.499 | 23.385 | 23.730 | +0.344 | 0.585 | 0.666 | +0.081 | 0.589 | 0.662 | +0.073 | 0.420 | 0.232 | +0.188 | 0.401 | 0.222 | +0.178 |
| 6 | KTM20 Oblique - Flight 006 | 22.746 | 21.253 | -1.494 | 23.475 | 22.662 | -0.813 | 0.752 | 0.706 | -0.046 | 0.785 | 0.778 | -0.007 | 0.305 | 0.329 | -0.024 | 0.254 | 0.233 | +0.021 |
| 7 | Kninice Church | 21.227 | 21.547 | +0.320 | 21.815 | 22.039 | +0.224 | 0.688 | 0.711 | +0.024 | 0.696 | 0.722 | +0.026 | 0.447 | 0.391 | +0.056 | 0.428 | 0.367 | +0.062 |
| 8 | Pix4D Forensic | 24.260 | 24.814 | +0.554 | 24.417 | 24.993 | +0.576 | 0.543 | 0.673 | +0.131 | 0.556 | 0.691 | +0.135 | 0.623 | 0.405 | +0.219 | 0.596 | 0.363 | +0.234 |
| 9 | Telc - St. James Church | 21.058 | 21.304 | +0.245 | 21.489 | 21.669 | +0.180 | 0.715 | 0.745 | +0.030 | 0.728 | 0.760 | +0.033 | 0.421 | 0.360 | +0.061 | 0.394 | 0.325 | +0.069 |
| 10 | Angel Island State Park | 20.217 | 20.082 | -0.136 | 20.508 | 20.402 | -0.106 | 0.644 | 0.665 | +0.021 | 0.662 | 0.693 | +0.031 | 0.506 | 0.457 | +0.049 | 0.470 | 0.401 | +0.069 |
| 11 | Morice | 28.537 | 29.513 | +0.977 | 28.992 | 30.312 | +1.320 | 0.813 | 0.865 | +0.052 | 0.823 | 0.876 | +0.053 | 0.252 | 0.156 | +0.096 | 0.234 | 0.137 | +0.097 |
| 12 | Uncovice | 22.643 | 22.163 | -0.480 | 23.248 | 22.486 | -0.763 | 0.663 | 0.688 | +0.025 | 0.675 | 0.703 | +0.028 | 0.506 | 0.442 | +0.064 | 0.481 | 0.409 | +0.072 |

Note: "Base" refers to the baseline run, while "Ridge" refers to the Ridge model-selected run. PSNR and SSIM differences are calculated as Ridge minus baseline. LPIPS improvement is calculated as baseline minus Ridge because lower LPIPS is better. Positive values indicate improved performance by the Ridge model-selected run. The 5,000- and 7,000-iteration values are from the same continuous training runs. Densification ended at 4,000 iterations in both cases.
