# Tech stack: Jira Cloud

Jira Cloud is the host product. The features in this project are built as a Forge app, which runs inside Jira. Azure DevOps is a second data source, connected through an integration.

| Layer | Technology | Role in Jira Cloud |
|---|---|---|
| Frontend | React with Atlaskit | Jira's screens, built on Atlassian's design system |
| Forge (our features) | Forge app platform, UI Kit, Custom UI | Where the dashboards are built and hosted |
| Backend services | Java services on Atlassian Micros, running on Kubernetes | Jira's business logic and APIs |
| Database | Amazon RDS (multi-AZ) | Core relational data |
| Data store | DynamoDB with Protobuf | High-volume issue and event data |
| Search | OpenSearch | Issue search and filtering |
| Caching | Memcached | Speeds up repeated reads |
| Events | AWS Kinesis, SNS | Change events, for example "issue moved" |
| Payments | Not used by these features | Jira billing is outside the scope of this project |
| CDN and edge | Atlassian edge | Serves the web app close to users |
| Security | AWS KMS encryption, SSO, JWT (ASAP) | Encrypts data and checks who is calling |
| Analytics | Atlassian platform analytics | Usage data (not used by these features) |

Sources: Atlassian Trust and cloud architecture pages, Atlassian engineering blog, Forge documentation.
