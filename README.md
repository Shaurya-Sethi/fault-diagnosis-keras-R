# Analog Circuit Fault Diagnosis with Deep Learning in R

This repository provides an end-to-end, fully reproducible workflow for analog circuit fault diagnosis using machine learning and deep learning models implemented in R. The project includes complete data preprocessing, exploratory analysis, ANOVA feature selection, and a multi-layer perceptron (MLP) model built using the Keras R interface (with TensorFlow backend). All steps are documented in a single Quarto (`.qmd`) notebook for transparency and educational value.

## Project Overview

* Complete pipeline for tabular fault diagnosis: loading, preprocessing, feature engineering, modeling, and evaluation
* Deep learning with a custom MLP using Keras (R interface)
* Feature selection and exploratory analysis, including ANOVA and visualization
* Provided as a single Quarto notebook for maximum reproducibility

## Files and Structure

* `fault-diagnosis-keras-R.qmd` — Main Quarto notebook: includes data cleaning, feature selection, modeling, and evaluation
* `data/TD_features_MLP_V2.xlsx` — Example dataset (replace with your own as needed)
* `images/` — Supporting figures and plots for the quarto
* `requirements.R` — Script to install all R package dependencies (see below)
* `scripts/` - R scripts for the model training, evaluation, and ANOVA test

## Getting Started

### Requirements

* R (v4.1 or later recommended)
* Python (installed for the TensorFlow backend)
* The following R packages:

  * tidyverse
  * readr
  * ggplot2
  * caret
  * keras
  * tensorflow

### Dependency Installation

1. **Install R packages**

   * Run the following script in R or copy the commands from `requirements.R`:

     ```r
     install.packages(c(
       "tidyverse",
       "readr",
       "ggplot2",
       "caret",
       "keras",
       "tensorflow"
     ))
     ```
2. **Install the Python backend for Keras and TensorFlow:**

   * In R, run:

     ```r
     library(keras)
     install_keras()
     library(tensorflow)
     install_tensorflow()
     ```
   * This will automatically set up a Python environment with TensorFlow and Keras. If you already have Python installed, make sure it is accessible to R.

### Data

* Place your dataset in the `data/` directory. This repo provides an example (`TD_features_MLP_V2.xlsx`), but you may use your own data.
* If your data uses different column names or structure, you must update the notebook/code to match your format.

### Running the Notebook

* The complete workflow is contained in `fault-diagnosis-keras-R.qmd`.
* You can open this file in RStudio (or Posit Cloud) or any text editor.
* To render to HTML:

  ```bash
  quarto render fault-diagnosis-keras-R.qmd --to html
  ```
* Or knit to PDF if your system supports it.

### Customization

* Update paths in the notebook if your data or images are stored differently.
* Modify the modeling section for different neural network architectures as needed.

## Acknowledgements

This project was developed for academic research and is inspired by the need for explainable and reproducible deep learning workflows in engineering. It leverages the R interface to Keras and TensorFlow, combining the best of statistical and deep learning tools.

## License

This repository is released under the MIT License.
