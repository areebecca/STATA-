# Stata Data Cleaning & Summary Statistics

This repository contains a Stata `.do` script demonstrating foundational data management, cleaning, labeling, and exploratory summary statistics using a household survey dataset (`stata_training_dataset.csv`).

## Workflow Covered

1. **Setup & Data Import**
   - Setting the working directory (`cd`)
   - Importing CSV data (`import delimited`)
   - Inspecting the dataset (`br`, `describe`)

2. **Variable & Value Labeling**
   - Assigning descriptive labels to variables (`label variable`) such as `id`, `age`, `education`, `income`, `water_source`, `sanitation`, `weight`, `height`, `children_u5`, `diarrhea`, and `sex`
   - Defining and applying categorical value labels (`label define`, `label values`)
   - Dropping value labels (`label drop`)

3. **Data Cleaning & Feature Creation**
   - Generating new variables (`generate bmi`)
   - Checking for missing values (`misstable summarize`)
   - Identifying and removing duplicate records (`duplicates report`, `duplicates drop`)

4. **Exploratory Summary Statistics**
   - Basic summaries (`summarize`)
   - Conditional summaries (`sum ... if`)
   - Detailed distributions including percentiles, skewness, and kurtosis (`sum ..., detail`)
   - Sub-group / disaggregated summaries (`by ..., sort: sum ...`)

## Requirements

- **Stata** (any recent version)
- **Dataset:** `stata_training_dataset.csv`

## How to Run

1. Download or clone this repository.
2. Place `stata_training_dataset.csv` in your project folder.
3. Open the `.do` file in Stata and update the `cd` and `import delimited` file paths to match your local directory.
4. Run the script.

## Notes for Future Use

- Update local file paths (`C:\Users\...`) before sharing or running on a different machine.
- Double-check calculated formulas (e.g., `bmi = weight / (height^2)` if height is in meters) and value label mappings (e.g., `0` vs `1` coding) against your dataset's codebook.
