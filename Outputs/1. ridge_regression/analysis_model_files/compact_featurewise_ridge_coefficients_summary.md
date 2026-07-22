# Compact Ridge Coefficient Summary

Source model: `model_compact-ridge_20260712_131550_final_offline_data_june_27-training-data-compact-ridge`

This file summarizes the coefficients recovered from `compact_featurewise_ridge_model.json`. The stored model keeps the ridge normal-equation matrices `A` and `b`; the coefficient vector is obtained by solving `A theta = b`.

The model predicts relative quality score from:

- scaled scene descriptors,
- three log multiplier values: geometry, appearance, and densification,
- squared log multiplier terms,
- descriptor-by-log-multiplier interaction terms.

A positive coefficient increases the predicted relative quality score when that term increases. A negative coefficient decreases it. Descriptor terms use scaled values, so coefficient size should be interpreted as influence within the trained model, not as the raw physical unit of the descriptor.

## Model Metrics

| Field | Value |
|---|---:|
| Training rows | 653 |
| Ridge lambda | 0.1 |
| Train-fit MSE | 0.002610995 |
| Train-fit RMSE | 0.051097899 |
| Train-fit R2 | 0.727943 |
| Theta norm | 0.373709 |

## Strongest Direct Terms

These are the largest direct descriptor or multiplier terms by absolute coefficient.

| Term | Coefficient | Meaning |
|---|---:|---|
| `log(densification_mult)^2` | 0.344883 | Curvature term for the group log multiplier. |
| `log(geometry_lr_mult)` | 0.042715 | Direct effect of the group log multiplier when scaled descriptors are zero. |
| `log(geometry_lr_mult)^2` | -0.037237 | Curvature term for the group log multiplier. |
| `log(appearance_lr_mult)^2` | -0.036959 | Curvature term for the group log multiplier. |
| `texture_density` | -0.028993 | Feature coefficient when log multipliers are zero; descriptor values are scaled by the training-data scaler except intercept. |
| `blur_motion_risk` | -0.020295 | Feature coefficient when log multipliers are zero; descriptor values are scaled by the training-data scaler except intercept. |
| `log(appearance_lr_mult)` | 0.020156 | Direct effect of the group log multiplier when scaled descriptors are zero. |
| `log(densification_mult)` | -0.018694 | Direct effect of the group log multiplier when scaled descriptors are zero. |
| `coverage_spread` | -0.013102 | Feature coefficient when log multipliers are zero; descriptor values are scaled by the training-data scaler except intercept. |
| `gsd_median` | 0.004997 | Feature coefficient when log multipliers are zero; descriptor values are scaled by the training-data scaler except intercept. |
| `vegetation_complexity_score` | 0.003012 | Feature coefficient when log multipliers are zero; descriptor values are scaled by the training-data scaler except intercept. |
| `overlap_proxy` | 0.001109 | Feature coefficient when log multipliers are zero; descriptor values are scaled by the training-data scaler except intercept. |

## Strongest Descriptor-Multiplier Interaction Terms

These terms show where a descriptor changes the effect of a multiplier group.

| Term | Coefficient | Meaning |
|---|---:|---|
| `vegetation_cover_percentage * log(geometry_lr_mult)` | -0.068197 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `vegetation_complexity_score * log(geometry_lr_mult)` | 0.065471 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `texture_density * log(densification_mult)` | -0.037253 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `blur_motion_risk * log(densification_mult)` | -0.025070 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `texture_density * log(appearance_lr_mult)` | 0.018567 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `blur_motion_risk * log(geometry_lr_mult)` | 0.017563 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `vegetation_cover_percentage * log(densification_mult)` | 0.016739 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `terrain_roughness_proxy * log(densification_mult)` | 0.016260 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `coverage_spread * log(densification_mult)` | 0.014858 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `vegetation_complexity_score * log(appearance_lr_mult)` | -0.014206 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `vegetation_complexity_score * log(densification_mult)` | -0.013847 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `texture_density * log(geometry_lr_mult)` | 0.013765 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `blur_motion_risk * log(appearance_lr_mult)` | 0.013072 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `vegetation_cover_percentage * log(appearance_lr_mult)` | 0.012585 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |
| `gsd_median * log(densification_mult)` | 0.011254 | Interaction term: how the scaled descriptor changes the effect of this group log multiplier. |

## Files

- Full named coefficient table: `compact_featurewise_ridge_coefficients.csv`
- Source model file: `compact_featurewise_ridge_model.json`
