# ERP Synchronisation Error Analysis
# SynchIntegrity: ERP Synchronisation Failure Analysis

This repository contains the Python analysis workflow supporting the research study:

**“SynchIntegrity: A Data-Driven Framework for ERP Synchronisation Failure Analysis and Prevention in Higher Education”**

The study analyses ERP-to-regulatory synchronisation error events recorded between **2017 and 2025** and examines error categories, recurrence patterns, institutional and external dependencies, and changes in synchronisation error volume over time.

## Repository Contents

The repository contains the following analysis notebook:

- `ERP_Synchronisation_Analysis.ipynb` — Python notebook containing the data preprocessing, error classification, statistical analysis, recurrence analysis, and visualisation workflow used in the study.

The notebook reproduces the analytical workflow associated with:

- **Figure 2:** Pareto Analysis of ERP-to-Regulatory Synchronisation Errors by Category
- **Figure 3:** PCA Visualisation of Institutional and External ERP Synchronisation Error Patterns
- **Figure 4:** Annual Total and Distinct ERP-to-Regulatory Synchronisation Error Events (2017–2025)
- **Figure 5:** Annual ERP-to-Regulatory Synchronisation Error Volume and Recurrence Ratio (2017–2025)

## Analysis Workflow

The notebook implements the following main analytical steps:

1. Dataset loading and preprocessing
2. Construction of distinct error cases using student identifier and error description
3. Classification of synchronisation errors into analytical categories
4. Pareto analysis of synchronisation error categories
5. Grouping of errors into institutional and external/registry-dependent clusters
6. TF-IDF transformation and Principal Component Analysis (PCA)
7. Annual calculation of total and distinct error events
8. Calculation of repeated error events and recurrence ratios
9. Analysis of error multiplicity and year-to-year changes in error volume
10. Generation of the analytical figures reported in the study

## Data Availability and Confidentiality

The research dataset is **not included in this repository** because it contains confidential institutional records and is subject to institutional data-protection requirements.

Access to the underlying data may be provided by the corresponding author upon reasonable request and subject to institutional approval.

The source dataset must **not** be uploaded, committed, or otherwise published as part of this repository.

## Reproducibility

This repository is provided to support transparency and reproducibility of the analytical methodology used in the study.

Because the underlying research dataset is confidential, the numerical results cannot be independently reproduced from this repository alone without authorised access to the source data.

For authorised users, the notebook can be executed using the research dataset. The analytical workflow derives the error classifications, annual statistics, recurrence measures, PCA visualisation, Pareto analysis, and other figures directly from the supplied data.

The public notebook is intentionally distributed without outputs generated from the confidential research dataset.

## Software Requirements

The analysis was implemented in Python using the following principal libraries:

- Python 3
- pandas
- NumPy
- Matplotlib
- scikit-learn

The notebook is compatible with **Google Colab**.

## Expected Dataset Fields

The analytical workflow requires, at minimum, fields corresponding to:

- `date` — date associated with the synchronisation error event
- `studentid` — student identifier used in constructing distinct error cases
- `error_description` — synchronisation error message or description

The research dataset itself is intentionally excluded from this repository.

## Error Classification

Synchronisation error descriptions are classified into analytical categories used in the study, including:

- Metadata & Code Lists
- Temporal & Status Logic
- Identity & Uniqueness
- Mandatory Field Completeness
- Cross-Institution / Registry Conflict
- External System / Workflow Integration
- System / Unknown Error Code
- Unclassified

These classifications support the Pareto analysis and the broader distinction between institutionally manageable errors and errors involving external or registry-dependent processes.

## Recurrence Analysis

For the longitudinal analysis, the notebook calculates annual:

- Total error events
- Distinct error cases
- Repeated error events
- Recurrence ratios
- Error multiplicity
- Year-to-year changes in error volume

A distinct error case is constructed from the combination of the student identifier and error description within the analytical workflow.

## Privacy and Responsible Use

No student-level research data are included in this public repository.

Users with authorised access to the underlying dataset should ensure that confidential or personally identifiable information is handled in accordance with applicable institutional data-protection requirements.

Notebook outputs generated using confidential research data should be cleared before committing changes to a public repository.

## Authors

**Said S. N. Al Harthy**  
Modern College of Business and Science, Oman

**Dr. Sin-Ban Ho**  
Multimedia University, Malaysia

**Dr. Ian Chai**  
Multimedia University, Malaysia

## Citation

If you use or adapt this analytical workflow, please cite the associated research article:

> Al Harthy, S. S. N., Ho, S.-B., & Chai, I. *SynchIntegrity: A Data-Driven Framework for ERP Synchronisation Failure Analysis and Prevention in Higher Education.*

Full journal publication details and DOI will be added following publication.

## License

The analytical code is provided for academic and research purposes. A formal software license may be added to this repository separately.
