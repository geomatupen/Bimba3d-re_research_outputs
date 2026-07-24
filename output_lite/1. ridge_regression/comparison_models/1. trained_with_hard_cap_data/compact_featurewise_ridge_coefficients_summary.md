# Ridge Regression Coefficients

Model: `A2_Final_ridge_used_in_report_trained_with_hard_capped_data`

Model ID: `model_compact-ridge_20260713_095334_final_compact_ridge_with_hard_cap_data_july13`

The intercept is excluded from Ridge regularization for this model. Larger absolute coefficients indicate stronger model sensitivity after standardization; they are not causal proof.

| Rank | Term | Coefficient | Absolute coefficient |
|---:|---|---:|---:|
| 1 | `log_densification_mult^2` | 0.7064297 | 0.7064297 |
| 2 | `texture_density x log_densification_mult` | 0.17892455 | 0.17892455 |
| 3 | `vegetation_complexity_score x log_geometry_lr_mult` | 0.15203846 | 0.15203846 |
| 4 | `vegetation_cover_percentage x log_geometry_lr_mult` | -0.14901433 | 0.14901433 |
| 5 | `blur_motion_risk x log_densification_mult` | 0.13971929 | 0.13971929 |
| 6 | `texture_density` | -0.13316871 | 0.13316871 |
| 7 | `blur_motion_risk` | -0.10788836 | 0.10788836 |
| 8 | `log_appearance_lr_mult^2` | -0.074401849 | 0.074401849 |
| 9 | `texture_density x log_appearance_lr_mult` | -0.06628192 | 0.06628192 |
| 10 | `texture_density x log_geometry_lr_mult` | -0.049151255 | 0.049151255 |
| 11 | `blur_motion_risk x log_appearance_lr_mult` | -0.048364043 | 0.048364043 |
| 12 | `terrain_roughness_proxy x log_densification_mult` | -0.047748929 | 0.047748929 |
| 13 | `log_densification_mult` | 0.044862008 | 0.044862008 |
| 14 | `vegetation_cover_percentage x log_densification_mult` | -0.042995941 | 0.042995941 |
| 15 | `intercept` | -0.035380184 | 0.035380184 |
| 16 | `vegetation_complexity_score x log_densification_mult` | 0.030054068 | 0.030054068 |
| 17 | `coverage_spread x log_densification_mult` | 0.029145657 | 0.029145657 |
| 18 | `terrain_roughness_proxy` | 0.024858153 | 0.024858153 |
| 19 | `log_geometry_lr_mult^2` | -0.023568025 | 0.023568025 |
| 20 | `blur_motion_risk x log_geometry_lr_mult` | -0.021080805 | 0.021080805 |
| 21 | `overlap_proxy x log_densification_mult` | -0.020388653 | 0.020388653 |
| 22 | `log_appearance_lr_mult` | -0.018667508 | 0.018667508 |
| 23 | `coverage_spread x log_appearance_lr_mult` | -0.017352447 | 0.017352447 |
| 24 | `gsd_median x log_densification_mult` | -0.01695858 | 0.01695858 |
| 25 | `overlap_proxy` | 0.014764642 | 0.014764642 |
