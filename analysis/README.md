# Reproduce the OHP prediction results

## Prediction results

The analysis includes 670 patients: 296 in development, 126 in internal validation, 156 in external testing, and 92 in the prospective cohort.

Install the packages in `requirements-prediction-analysis.txt` and run:

```text
python reproduce_prediction_results.py --input APPROVED_PREDICTION_EXPORT.csv --output-dir NEW_OUTPUT_DIRECTORY
```

The approved export requires the pseudonymous study code, cohort, OHP reference label, all five branch probabilities, fused probability, classification threshold and predicted OHP class. Calculations preserve the locked threshold and cohort allocations. The development estimates use out-of-fold predictions. Calibration uses six within-cohort probability-quantile groups and Wilson 95% intervals.
