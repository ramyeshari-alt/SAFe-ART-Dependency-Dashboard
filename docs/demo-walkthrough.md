# Demo walkthrough

A short guide for presenting the prototype. Open `prototype/dashboard.html` in a browser, or use the live link in the README.

## 1. Context (1 minute)

- One Agile Release Train (ART) with six teams, planned over one Program Increment (PI).
- Jira Cloud is the main source. Azure DevOps items appear next to Jira issues, marked with an ADO badge.

## 2. Dependency dashboard (3 minutes)

1. Open the **Dependencies** tab. Each row is a team, and each dot is one dependency.
2. Read the colours: Green is on track, Amber is at risk, Red is blocked. Each colour also has a label, so it works without colour.
3. Show a rejected request. It stays Red until it is re-planned (FR-1.2).
4. Show a circular link. It is flagged (edge case).
5. Filter by team or risk to show how the matrix narrows (FR-1.5).

## 3. Capacity planner (3 minutes)

1. Open the **Capacity** tab. Each cell is one team in one sprint.
2. Explain the bands: 60 to 85% is green, 85 to 100% or under 60% is amber, over 100% is red (FR-2.4).
3. Show a sprint over 100%. The planner flags it before the sprint starts.

## 4. People view (1 minute)

1. Open the **People** tab. It adds one person's load across every team they work in (FR-2.5).
2. Show that allocations over 100% across teams are blocked (edge case).

## 5. Close (1 minute)

- Next steps: connect real Jira and Azure DevOps data, build the Forge app inside Jira, and roll out to all six teams.
