# Requirements

## Feature 1: ART Dependency Dashboard

| ID | The system shall… | Priority |
|---|---|---|
| FR-1.1 | let a team raise a dependency request on another team's item, with a needed-by sprint | Must |
| FR-1.2 | let the receiving team accept (with a sprint) or reject (with a reason) | Must |
| FR-1.3 | show all dependencies for an ART and PI as a team matrix and a sprint timeline | Must |
| FR-1.4 | mark each dependency Green, Amber or Red using the risk rules | Must |
| FR-1.5 | filter by team, status, risk and sprint, and export to CSV | Should |
| FR-1.6 | show Azure DevOps items next to Jira issues, with an ADO badge | Should |

Edge cases: a rejected request stays Red until re-planned; circular links are flagged; moved or deleted items become Orphaned; items a user cannot see show as Restricted; outside teams can be added as External.

## Feature 2: Capacity and Utilisation Planner

| ID | The system shall… | Priority |
|---|---|---|
| FR-2.1 | let a Scrum Master set each member's allocation (0 to 100%) and days off per sprint | Must |
| FR-2.2 | work out team capacity per sprint from its members | Must |
| FR-2.3 | calculate load from planned estimates; utilisation = load ÷ capacity | Must |
| FR-2.4 | show a team-by-sprint heatmap: green 60 to 85%, amber 85 to 100%, red over 100% | Must |
| FR-2.5 | show a person view that adds up load across every team a person works in | Should |
| FR-2.6 | let the RTE test a move of an issue and see utilisation change before saving | Could |

Edge cases: allocations over 100% across teams are blocked; zero-capacity sprints show "No capacity"; unestimated issues are counted and flagged; mixed units are never added together.

## Non-functional requirements

| ID | Quality | Target |
|---|---|---|
| NFR-1 | Performance | Under 3 seconds for 12 teams, 5 sprints and 2,000 issues (95th percentile) |
| NFR-2 | Scalability | Up to 10 ARTs, 150 teams and 20,000 linked issues per site |
| NFR-3 | Availability | 99.9% monthly; if the Azure DevOps sync is down, Jira data still shows with a last-synced time |
| NFR-4 | Security and privacy | Every item checked against Jira permissions; data stays in the customer's region |
| NFR-5 | Data freshness | Jira changes within 1 minute; Azure DevOps every 15 minutes |
| NFR-6 | Accessibility | WCAG 2.1 AA; colours always paired with a label or icon |
