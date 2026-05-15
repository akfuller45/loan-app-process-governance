# loan-app-process-governance

# Loan Process Governance & Control Analysis

## Executive Summary

This project simulates an enterprise business process governance and operational risk analysis using a loan application event-log dataset.

The purpose of the project is to evaluate how loan applications move through the workflow, identify bottlenecks, detect SLA breaches, analyze rework, test process controls, classify case outcomes, and build an executive process governance dashboard.

The project is designed from the perspective of a Business Process Analyst, GRC Analyst, Operational Risk Analyst, or Business Systems Analyst working within a financial services environment.

---

## Business Problem

Financial institutions must ensure that loan application workflows are efficient, controlled, auditable, and transparent.

Poor process governance can result in:

- delayed application processing
- excessive rework
- unresolved cases
- weak operational controls
- poor customer experience
- inaccurate management reporting
- audit readiness gaps

This project builds a process governance framework to identify these risks and provide leadership with actionable insights.

---

## Project Objectives

- Analyze loan application workflow activity
- Measure case cycle time
- Identify bottlenecks between process steps
- Detect SLA breaches
- Identify excessive rework cases
- Build a process transition matrix
- Create a process flow map
- Test process governance controls
- Classify case outcomes and statuses
- Assign governance ownership
- Build an executive process governance dashboard

---

## Dataset Overview

The dataset is a cleaned BPI 2017 loan application event-log file.

Key fields include:

| Field | Description |
|---|---|
| `case_id` | Unique loan application case |
| `activity` | Process activity name |
| `timestamp` | Event timestamp |
| `resource` | Resource or user handling the event |
| `loan_goal` | Purpose of the loan |
| `application_type` | Type of application |
| `requested_amount` | Requested loan amount |
| `accepted` | Acceptance indicator |
| `credit_score` | Credit score field |
| `offered_amount` | Offered loan amount |

---

## Methodology

The project follows an enterprise process governance workflow:

1. Load and inspect the event-log data
2. Clean column names and convert timestamps
3. Create case-level summaries
4. Calculate cycle time and event counts
5. Identify process bottlenecks
6. Build transition counts and transition matrix
7. Create process risk indicators
8. Perform automated control testing
9. Classify case outcomes and statuses
10. Assign case ownership and recommended actions
11. Create high-risk case registers
12. Build executive dashboard visuals

---

## Process Governance Metrics

The analysis evaluates several process governance indicators:

| Metric | Purpose |
|---|---|
| Cycle Time | Measures total processing duration |
| Event Count | Measures process activity volume |
| Unique Activities | Measures process complexity |
| SLA Breach Flag | Identifies cases exceeding cycle time threshold |
| Excessive Rework Flag | Identifies cases with high event repetition |
| Missing Credit Score Flag | Identifies documentation/control gaps |
| Missing Offered Amount Flag | Identifies offer data completeness issues |
| Process Risk Score | Aggregates governance risk indicators |
| Process Risk Level | Classifies cases into Low, Medium, High, or Critical risk |

---

## Automated Process Control Testing

The project includes automated control testing for key process governance controls.

| Control ID | Control Name |
|---|---|
| CTRL-001 | Case Start and End Present |
| CTRL-002 | Requested Amount Present |
| CTRL-003 | Credit Score Present |
| CTRL-004 | Offered Amount Present |
| CTRL-005 | Cycle Time Within SLA |
| CTRL-006 | Rework Within Threshold |

Each control was evaluated using:

- total cases tested
- passed cases
- failed cases
- pass rate
- control effectiveness rating

---

## Process Flow Mapping

The project includes a process transition matrix and process flow analysis.

The transition matrix shows how frequently one process activity leads to another. This supports workflow transparency and helps identify common process paths.

The process flow map visualizes activity-to-activity movement across the loan application workflow. These visuals support:

- process mapping
- bottleneck detection
- rework analysis
- workflow governance
- business systems analysis
- operational risk monitoring

---

## Case Status and Outcome Register

A case status and outcome register was created to simulate enterprise process governance.

Each loan application case was assigned:

- final activity
- case outcome
- case status
- process risk level
- governance owner
- recommended action

This register supports case-level oversight, ownership assignment, remediation planning, and audit readiness.

---

## Executive Dashboard

The executive dashboard summarizes key process governance and operational risk metrics.

Dashboard components include:

- total cases
- average cycle time
- SLA breaches
- rework cases
- high-risk cases
- critical-risk cases
- unresolved cases
- acceptance rate
- process risk level distribution
- case outcome distribution
- case status distribution
- case ownership workload
- most common process transitions
- bottleneck transitions
- failed process governance controls

![Loan Process Governance Dashboard](outputs/charts/loan_process_governance_dashboard_clean2.png)

---

## Key Findings

### Finding 1 — SLA Breach Exposure

A portion of loan application cases exceeded the established cycle time SLA threshold. These cases may indicate workflow delays, processing inefficiencies, staffing constraints, or handoff issues between process activities.

### Finding 2 — Rework Concentration

Several cases showed excessive event counts, indicating potential rework or repeated activity. Rework may result from incomplete documentation, repeated customer contact, duplicate validations, or process design inefficiencies.

### Finding 3 — Bottleneck Transitions

The bottleneck analysis identified specific activity-to-activity transitions with high average delay times. These transitions represent opportunities for process improvement, automation, workload balancing, or revised escalation rules.

### Finding 4 — Unresolved Outcomes

A meaningful number of cases were classified as unresolved or requiring outcome review. These cases may require final status validation to improve reporting accuracy and process transparency.

### Finding 5 — Control Testing Results

Automated process controls were tested across the case population. Failed controls were primarily associated with cycle time SLA breaches and excessive rework thresholds, indicating areas where process governance monitoring should be strengthened.

---

## Recommendations

### Process Governance Improvements

- Implement recurring cycle time monitoring by process stage.
- Create automated SLA alerts for cases exceeding expected processing time.
- Maintain a case-level process governance register.
- Review unresolved cases to confirm final application outcomes.

### Process Improvement Recommendations

- Investigate the highest-delay activity transitions.
- Analyze repeated activity patterns to identify root causes of rework.
- Standardize handoff procedures between major process steps.
- Evaluate whether automation could reduce manual processing delays.

### Control and Audit Readiness Recommendations

- Maintain automated control testing summaries for SLA, rework, and documentation controls.
- Create periodic process governance dashboards for management review.
- Assign case ownership for SLA breaches, rework cases, and unresolved outcomes.
- Preserve transition matrices and bottleneck reports as audit-supporting evidence.

---

## Project Outputs

| Output | Description |
|---|---|
| `case_level_process_summary.csv` | Case-level workflow summary |
| `case_status_outcome_register.csv` | Case outcome and governance status register |
| `high_risk_case_register.csv` | High-risk loan application cases |
| `process_control_testing_summary.csv` | Automated control testing summary |
| `process_transition_counts.csv` | Activity-to-activity transition counts |
| `process_transition_matrix.csv` | Process transition matrix |
| `process_bottleneck_analysis.csv` | Bottleneck transition analysis |
| `loan_process_governance_dashboard_clean2.png` | Executive dashboard visual |

---

## Technology Stack

- Python
- pandas
- numpy
- matplotlib
- networkx
- Jupyter Notebook
- CSV data processing
- GitHub

---

## Project Structure

```text
loan-process-governance-control-analysis/

│
├── data/
│   ├── raw/
│   ├── cleaned/
│
├── notebooks/
│   └── loan_process_governance_analysis.ipynb
│
├── outputs/
│   ├── charts/
│   │   ├── loan_process_governance_dashboard_clean2.png
│   │   ├── loan_transition_matrix_clean.png
│   │   └── process_flow_map.png
│   ├── tables/
│   │   ├── case_level_process_summary.csv
│   │   ├── case_status_outcome_register.csv
│   │   ├── high_risk_case_register.csv
│   │   ├── process_control_testing_summary.csv
│   │   ├── process_transition_counts.csv
│   │   ├── process_transition_matrix.csv
│   │   └── process_bottleneck_analysis.csv
│   └── reports/
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

---

## Portfolio Value

This project demonstrates skills relevant to:

- business process analysis
- GRC analytics
- operational risk monitoring
- workflow analysis
- process mining
- SLA monitoring
- control testing
- bottleneck analysis
- case management
- audit readiness
- executive dashboarding
- business systems analysis

---

## Future Enhancements

Potential future enhancements include:

- interactive Power BI dashboard
- formal BPMN process map
- process mining with PM4Py
- resource utilization analysis
- SLA aging tracker
- remediation tracker
- audit findings simulation
- predictive delay modeling
- process automation recommendations

---

## Author

Amiranda Fuller

Governance Analytics | Business Process Analysis | Operational Risk | Data Governance | Business Intelligence
