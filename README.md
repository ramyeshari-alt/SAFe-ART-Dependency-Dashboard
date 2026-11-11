# SAFe ART Dependency and Capacity Dashboard for Jira Cloud

A product case study. It shows how two features could help a SAFe Agile Release Train (ART) of five to six teams plan work across team boundaries, built as a Forge app inside Jira Cloud.

**Live prototype:** https://claude.ai/artifact/FtacGUD3MnfamMsFHCiaNB

## The problem

Teams in one ART depend on each other's work, but nobody sees the whole picture. Dependencies are tracked in ad hoc lists, and capacity is only checked once a sprint has already started. The result is late surprises and overloaded people.

## Two features

1. **ART Dependency Dashboard.** A team matrix and sprint timeline that show who waits on whom, with each dependency rated Green, Amber or Red.
2. **Capacity and Utilisation Planner.** A team-by-sprint heatmap that shows overload before the sprint starts, plus a person view across teams.

## What is in this repository

| Path | Contents |
|---|---|
| `presentation/` | The final slide deck, as PPTX and PDF |
| `docs/requirements.md` | Functional requirements (FR-1.x, FR-2.x), edge cases and non-functional requirements (NFR-1 to NFR-6) |
| `docs/tech-stack.md` | The Jira Cloud tech stack, grouped by layer, with sources |
| `docs/flows/` | Build-logic flow diagrams for the dashboard, in three sections (A, B and C) |
| `docs/demo-walkthrough.md` | A step-by-step guide for presenting the prototype |
| `docs/images/prototype.png` | A screenshot of the prototype |
| `prototype/dashboard.html` | A clickable prototype with sample data. Open it in any browser |

## Key rules

- **Dependency risk.** Red if the request is rejected, pending for more than 5 days, or committed after the needed-by sprint. Amber if committed in the needed-by sprint. Green if committed before it.
- **Capacity heatmap.** Green from 60 to 85%, Amber from 85 to 100% or under 60%, Red over 100%.

## Running the prototype

Open `prototype/dashboard.html` in any modern browser. It needs no install and no network access.

## Scope and next steps

The prototype uses sample data. The next steps are to connect live Jira and Azure DevOps data, build the Forge app inside Jira, and roll out to all six teams in the ART.
