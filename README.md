# Kolkata Logistics Root-Cause Analysis

## Project overview
This project investigates a decline in on-time delivery performance for a fictional freight trucking company operating across 12 hubs in Kolkata. It demonstrates how shipment, route, vehicle and warehouse scan records can be cleaned, joined, analyzed and translated into management recommendations.

> **Important:** This is an illustrative case study. The dataset and numerical findings are synthetic because real company records were not supplied. Do not present the example results as verified findings about an actual business.

## Project files
- `kolkata_freight_root_cause_analysis.ipynb` — reproducible Python analysis workflow and synthetic data generator.
- `driver_tree.png` — visual breakdown of the illustrative decline and its contributors.
- `hypothesis_log.csv` — six testable hypotheses, methods, illustrative decisions, owners and measurable targets.
- `Kolkata_Freight_Root_Cause_Complete_Report.docx` — consolidated management memo, hypothesis log, analysis workflow, recommendations and technical appendix.

## Methods demonstrated
- Data quality checks, hub alias mapping and timestamp normalization to UTC.
- Handling out-of-order scan events and joining operational datasets.
- Metric breakdown by time, hub, service type and customer segment.
- Welch's t-test, chi-square testing and logistic regression.
- Counterfactual driver attribution and separation of seasonal effects from structural trends.
- Weekly early-warning indicators and alert thresholds.
- Causal reasoning, limitations and a proposed matched-hub pilot.

## Running the notebook
Recommended environment: Python 3.10 or later.

Install dependencies:
```bash
pip install numpy pandas scipy statsmodels matplotlib scikit-learn jupyter
```

Open the notebook:
```bash
jupyter notebook kolkata_freight_root_cause_analysis.ipynb
```

The notebook generates synthetic data for demonstration. For a real investigation, replace the generator with approved company extracts and validate the data definitions, join keys, timezone metadata and contractual SLA logic.

## Example driver-tree summary
The illustrative scenario models an 8.0 percentage-point decline in on-time delivery:
- Warehouse scan latency: 3.6 pp
- Route / dispatch congestion: 2.1 pp
- Vehicle availability: 1.4 pp
- Mix and seasonal effects: 0.5 pp
- Unexplained residual: 0.4 pp

The modeled drivers explain 95% of the example decline. These figures are synthetic, not actual operational measurements.
