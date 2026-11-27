# OHP prediction analysis and inference code

This repository contains inference and prediction analysis code for the preoperative composite high-risk pathology (OHP) model for clear cell renal cell carcinoma.

## Prediction analysis

The analysis includes 670 patients: 296 in development, 126 in internal validation, 156 in external testing, and 92 in the prospective cohort.

Use the pinned requirements and commands in [analysis/README.md](analysis/README.md). The prediction analysis uses an approved participant-level export. The code and platform for the 20-reader randomised crossover study are available from the corresponding author. Study inputs are subject to the access conditions below.

## Models and inference

The [OHP end-to-end Windows distribution](https://github.com/urologistChenyu/OHP-End-to-End/releases/tag/v1.0) includes the five trained risk branches, the KiTS21 segmentation checkpoint, preprocessing assets and matching runtime. Follow the installation and input instructions in the [desktop application repository](https://github.com/urologistChenyu/OHP-End-to-End). The locked fusion rule and operating threshold are described in `model_contract.json`. File names and checksums for the trained assets are recorded in `MODEL_FILES.json`.

## Controlled access to study data

Researchers may request de-identified participant-level study data from the corresponding author. Access is subject to approval by the relevant ethics committee and participating institutions and to a signed data access agreement. Approved data are made available through a secure channel for research purposes.

See LICENSE, THIRD_PARTY_NOTICES.md and licenses/ for source and third-party attribution.
