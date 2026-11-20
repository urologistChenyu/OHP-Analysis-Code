# Reproduce the OHP analyses

## Prediction results

Install the packages in `requirements-prediction-analysis.txt` and run:

```text
python reproduce_prediction_results.py --input APPROVED_PREDICTION_EXPORT.csv --output-dir NEW_OUTPUT_DIRECTORY
```

The approved export requires the pseudonymous study code, cohort, OHP reference label, all five branch probabilities, fused probability, classification threshold and predicted OHP class. Calculations preserve the locked threshold and cohort allocations. The development estimates use out-of-fold predictions. Calibration uses six within-cohort probability-quantile groups and Wilson 95% intervals.

## Paired reader study

Install the packages in `requirements-reader-analysis.txt` and run:

```text
python analyse_readers.py --input-dir APPROVED_EXPORT_DIRECTORY --reference APPROVED_MODEL_REFERENCE.csv --output-dir NEW_OUTPUT_DIRECTORY
```

The input directory contains the approved R01–R16 workbook exports and reader grouping file. The approved reference export requires cohort, ID, OHP label, five branch probabilities, clinical fields and fused probability. Obtain both sets of inputs through the controlled access process described in the main README.
