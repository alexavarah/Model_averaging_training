# IT-based Model Averaging Training

Training materials introducing **information-theoretic (IT) approaches**, **multi-model inference (MMI)** and **model averaging** in ecology using R.

The tutorial provides a fully worked example based on ecological survey data and takes users through the complete workflow from model specification to model-averaged prediction.

## Overview

Information-theoretic approaches differ from traditional significance-testing frameworks by comparing multiple biologically plausible models rather than focusing on a single null hypothesis.

This training covers:

- Building a biologically informed global model
- Standardising predictor variables
- Model selection using AICc
- Generating candidate model sets
- Multi-model inference
- Model averaging
- Relative variable importance
- Prediction from model-averaged models

The analysis uses simulated butterfly abundance data derived from real agroforestry and monoculture field surveys conducted in England.

## Learning Objectives

By the end of this tutorial, you should be able to:

- Explain the rationale behind information-theoretic approaches
- Construct an appropriate global model
- Generate and rank candidate models using AICc
- Quantify model-selection uncertainty
- Perform model averaging using the `MuMIn` package
- Interpret model-averaged coefficients and confidence intervals
- Calculate relative variable importance
- Make predictions from averaged models

## Workflow

```text
Literature review
        ↓
A priori hypotheses
        ↓
Global model
        ↓
Candidate model set
        ↓
AICc ranking
        ↓
Top models (ΔAICc < 2)
        ↓
Model averaging
        ↓
Variable importance
        ↓
Inference & prediction
```

## Repository Structure

```text
Model_averaging_training/
├── data/
│   └── Example ecological dataset
│
├── scripts/
│   └── Training materials
│
├── output/
│   └── This is where you save your outputs
│
├── Model_averaging_training.Rproj
├── README.md
└── LICENSE
```

## Getting Started

Clone the repository:

```bash
git clone https://github.com/alexavarah/Model_averaging_training.git
```

or download the repository as a ZIP file.

Open:

```text
Model_averaging_training.Rproj
```

in RStudio.

## Main Tutorial

The complete training tutorial can be found in:

```text
scripts/Model_averaging_training.Rmd
```

Work through the document sequentially. All code chunks are fully reproducible.

## Requirements

This training was developed in R and RStudio.

### Main packages

```r
library(dplyr)
library(lme4)
library(MuMIn)
library(arm)
library(performance)
library(kableExtra)
library(here)
```

Install missing packages using:

```r
install.packages(
  c(
    "dplyr",
    "lme4",
    "MuMIn",
    "arm",
    "performance",
    "kableExtra",
    "here"
  )
)
```

## Dataset

The tutorial uses ecological survey data from English agroforestry and monoculture systems.

Variables used in the modelling exercise include:

- Treatment (agroforestry vs monoculture)
- Numbers of solitary bees (response variable)
- Land use
- Boundary habitat area
- Hedgerow variables
- Amount of semi-natural habitat nearby
- Date
- System age

A mixed-effects framework is used to account for site-level structure.

## References

Burnham, K. P. & Anderson, D. R. (2002). *Model Selection and Multimodel Inference: A Practical Information-Theoretic Approach.*

Burnham, K. P., Anderson, D. R. & Huyvaert, K. P. (2011). AIC model selection and multimodel inference in behavioral ecology.

Symonds, M. R. E. & Moussalli, A. (2011). Model selection, multimodel inference and model averaging in behavioural ecology using Akaike's information criterion.

Harrison, X. A. et al. (2018). A brief introduction to mixed-effects modelling and multi-model inference in ecology.

Dormann, C. F. et al. (2018). Model averaging in ecology: a review of Bayesian, information-theoretic and tactical approaches for predictive inference.

## Author

**Alexa Varah**  
Natural History Museum, London

## Licence

This project is licensed under the MIT License. See the `LICENSE` file for details.
