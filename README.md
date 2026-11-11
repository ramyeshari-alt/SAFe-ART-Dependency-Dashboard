# Extend a Real Product: SAFe ART Dashboards for Jira Cloud

Tech Cohort 19 individual assignment, by Ramyesh.

Jira Cloud is the host product. Azure DevOps is a second data source. The work covers two features that help a SAFe Agile Release Train (ART) of five to six teams:

1. **ART Dependency Dashboard**: see who waits on whom, with Green, Amber and Red risk.
2. **Capacity and Utilisation Planner**: spot overload before the sprint starts.

## Contents

| Path | What it is |
|---|---|
| `presentation/` | Final slide deck (PPTX and PDF). |
| `docs/requirements.md` | Functional and non-functional requirements, edge cases and risk rules. |
| `docs/flows/` | Dashboard build-logic flow diagrams (sections A, B and C). |
| `docs/images/prototype.png` | Screenshot of the clickable prototype. |
| `prototype/dashboard.html` | Working clickable prototype with sample data. Open it in any browser. |

## Run the prototype

Open `prototype/dashboard.html` in a browser. No install is needed.

Live link: https://claude.ai/artifact/FtacGUD3MnfamMsFHCiaNB

## Key rules

- Dependency risk: Red if rejected, pending for more than 5 days, or committed after the needed-by sprint. Amber if committed in the needed-by sprint. Green if committed before it.
- Capacity heatmap: green 60 to 85%, amber 85 to 100% or under 60%, red over 100%.
