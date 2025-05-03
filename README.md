# college-retention-model
# Predicting College Retention for African American Males

This project builds a deployable machine learning model using the HSLS:09 dataset to predict college retention among African American male students.

## Overview

- **Goal**: Predict whether a student persists in college using academic, demographic, and financial aid variables.
- **Dataset**: High School Longitudinal Study of 2009 (HSLS:09) from NCES.
- **Models Used**: Logistic Regression, Random Forest, XGBoost.
- **Final Model**: XGBoost (AUC = 0.83)
- **Deployment**: Exposed as a RESTful API using `plumber`.

## Repository Structure

- `data/`: Cleaned dataset files.
- `scripts/`: Model training, evaluation, and preprocessing scripts.
- `plumber.R`: Deployment script for API endpoint.
- `final_project_darryl_izzard.Rmd`: Full manuscript with methodology and findings.

## How to Use the Model

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/college-retention-model.git
   cd college-retention-model
   ```

2. Install dependencies in R:
   ```r
   install.packages(c("tidymodels", "xgboost", "plumber"))
   ```

3. Run API locally:
   ```r
   library(plumber)
   pr("plumber.R") %>% run(port=8000)
   ```

4. Make a POST request to `/predict` endpoint with student data (example JSON provided).

## License
MIT License

## Author
Darryl Izzard, 2025
