# Business Analytics — Power BI Case Study

**Historical public portfolio exercise · Power BI / Power Query / DAX**

A business analytics exercise focused on defining decision-relevant measures, reconciling operating data, and presenting commercial performance through an executive dashboard.

This is a **case study**, not evidence of a product deployed in production or of commercial impact achieved for a client.

## Problem

A commercial activity programme requires a consistent view of performance: activity volume, progression through stages, operational structure, and associated costs. Reporting becomes unreliable when categories, dates or organisational identifiers are inconsistent.

## Analytical approach

1. **Frame the business questions.** Which stages of the process lose the most activity? How do channels and periods compare? What inputs are required to interpret cost measures?
2. **Prepare and model data.** Normalize inconsistent categories, transform dates and create relationships to support analysis.
3. **Define metrics.** Build DAX measures for volume, funnel progression and cost perspectives.
4. **Communicate findings.** Organize the dashboard around temporal trends, operational reconciliation and cost interpretation.

## Deliverables in this repository

| Artifact | What it shows |
| --- | --- |
| [Power BI report](Business_Analytics_Junior_Case_Study_Public.pbix) | Public version of the analytical model and report (requires Power BI Desktop) |
| [Executive document](docs/DOCUMENTO_EJECUTIVO_PUBLICO.pdf) | Written business framing and interpretation |
| [Dashboard images](img/) | Static report pages for reviewers without Power BI |

### Dashboard areas

- **Performance and funnel:** activity trends and conversions between stages.
- **Operational reconciliation:** actual-versus-planned views of selling points and roles.
- **Cost analysis:** cost allocation and comparative views across channels and activity.

The images and public artifact support a review of the dashboard's structure and communication. The repository does **not** contain a runnable data pipeline, automated regression tests, CI, deployment configuration or ongoing data refresh process.

## Quality considerations

- Examine the definition and denominator of every rate before comparing funnel stages.
- Distinguish operational inconsistencies from genuine changes in activity.
- Treat estimated cost allocations as assumptions that require validation.
- Do not interpret dashboard visuals alone as proof of causation or business impact.

## How to explore

Open the `.pbix` file using **Power BI Desktop**, or review the static images and executive document. This is an archived portfolio exercise; current product/engineering work is represented separately.

## Privacy and reuse

The original README describes the exercise as anonymized for public presentation. **That statement is not an independent privacy certification.** Do not use the contents as actual client benchmarks or republish individual records, screenshots or commercial figures without checking reuse rights and disclosure suitability. The project is shown here only as evidence of analytical method.

## Scope

This project demonstrates **business analytics foundations**—requirements framing, data preparation, semantic modelling, KPI design and executive communication. It is not described as AI engineering, product assurance or a live enterprise system.
