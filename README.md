# Veterinary Renal Morphology Prediction

**Research code | Unpublished study**  
**Portfolio maintainer:** Parham Soufizadeh

## Overview

This project investigates whether routine hematology and demographic features can be used to estimate CT-derived renal morphology in clinically healthy dogs and cats. It explores neural-network regression, gradient boosting (XGBoost), and ensemble learning.

## Repository contents

Six cleaned research notebooks cover left and right kidney length, width and volume. Each retains its original model architecture, training settings and analytical approach. Historical outputs and trained checkpoints are excluded.

## Getting started

Python 3.10 is the environment described in the manuscript; exact historical package versions are unavailable. Install dependencies in an isolated environment:

```bash
pip install -r requirements.txt
jupyter lab
```

Open a notebook in `notebooks/`. Set the environment variable `RENAL_DATA_PATH` to the absolute path of an authorized, locally prepared CSV before starting Jupyter, or place the file at `data/cbc.csv` relative to the repository root. The notebooks expect numeric predictors and target columns as specified in their feature-selection cells. No dataset is distributed. Run cells sequentially; checkpoints are generated locally. Do not upload executed notebooks or generated artifacts.

## Scope and limitations

These are archived research experiments, not a verified reproduction of the final manuscript. The notebooks use a 90/10 split and target-specific scaling; the manuscript describes a different split. The historical stacking implementation fits its meta-model using in-sample base predictions, and the left-volume notebook imputes the target before splitting. These practices can bias evaluation and should be revisited before drawing scientific conclusions. Historical checkpoint selections have been replaced with the checkpoint generated in the current run; this can change results. No external validation or end-to-end rerun is claimed. This is not a clinical diagnostic tool.

## Confidentiality and contact

The underlying research is unpublished. Clinical records, fitted models, detailed findings, manuscript and historical outputs are intentionally excluded. For further information or academic collaboration, please contact **Parham Soufizadeh** through the [GitHub profile](https://github.com/PSoufizadeh). No open-source license is granted by this repository.
