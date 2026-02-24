# Customer Tracking

Internal reference for Shakudo customer environments — access instructions, infrastructure, stack components, and ownership.

> **Source of truth:** Google Sheets (raw export: [`customers.csv`](./customers.csv))
> **⚠️ Security note:** Some files contain hardcoded secrets (IPs, passwords). Migration to 1Password is in progress.

---

## Structure

```
customer-tracking/
├── README.md              ← this file
├── customers.csv          ← raw data export from Google Sheets
└── <customer-slug>/
    └── README.md          ← all columns for that customer
```

Each customer `README.md` contains the following sections:

| Section | Description |
|---|---|
| `Environment URL` | Primary dashboard URL |
| `Accessible?` | Whether Shakudo staff can access it |
| `Airgapped (Y/N)` | Network isolation status |
| `Steps to access Kubernetes` | How to get kubectl/k9s access |
| `Steps to access Dashboard` | How to log into the platform UI |
| `Infrastructure provider` | Cloud/on-prem provider |
| `Who manages the infra/cloud` | Customer or Shakudo |
| `Shakudo Version` | Current deployed version |
| `Stack Components` | Installed platform components |
| `Last updated on (stack components)` | Date of last component update |
| `If changes, tag Shahzad/Chandan` | Notification targets for infra changes |
| `Applications` | Customer-deployed applications |
| `Notes` | Free-form notes / status |
| `Who to ask` | Shakudo owner(s) for this customer |
| `GPU available` | GPU node availability |
| `Backup enabled?` | Backup status and method |
| `GPU config (VRAM?)` | GPU spec details |

---

## Customers

| Customer | Environment URL | Accessible | Infrastructure |
|---|---|:---:|---|
| [Annexus](annexus/README.md) | https://ai.annexus.cc | ✅ | AKS |
| [Aristeia](aristeia/README.md) | http://shakudo.aristeiacapital.com | ❌ | AWS |
| [Avenue Capital](avenue-capital/README.md) | avenue-ai.avenue.corp *(churned)* | — | On-Prem VM |
| [BWX prod](bwx-prod/README.md) | https://shakudo.bwxt.net | ❌ | On-Prem VM |
| [Campbell](campbell/README.md) | https://shakudo-1.campbell.com | ✅ | On-Prem VM |
| [CentralReach Dev](centralreach-dev/README.md) | https://shakudo-dev-centralreach.hyperplane.dev | ✅ | AWS |
| [CentralReach Prod](centralreach-prod/README.md) | *(Todd manages — screenshare only)* | ❌ | AWS |
| [CloudHQ](cloudhq/README.md) | https://shakudo1.cloudhq.com | ✅ | On-Prem |
| [Dynex](dynex/README.md) | https://dynexcapital.canopyhub.io | ❌ | Azure VMs |
| [EJ Gallo](ej-gallo/README.md) | shakudodev.ejgallo.com | ❌ | — |
| [Ellis Don](ellis-don/README.md) | *(no active environment — deal not closed)* | — | — |
| [En-powered](en-powered/README.md) | https://enpowered.hyperplane.dev | ✅ | Oracle Cloud |
| [Flexivan](flexivan/README.md) | https://flexivan.hyperplane.dev | ✅ | AWS |
| [Hitachi Demo](hitachi-demo/README.md) | hitachi.canopyhub.io | ✅ | Latitude |
| [Hitachi Prod](hitachi-prod/README.md) | *(customer-managed)* | ❌ | AWS |
| [Huntington Cyber non-Prod](huntington-cyber-non-prod-cluster/README.md) | https://artifactscanning.dev.hban.us | ✅ | AWS EKS |
| [Huntington Cyber Prod](huntington-cyber-prod-cluster/README.md) | https://artifactscanning.hban.us | ✅ | AWS EKS |
| [Huntington MLOps non-Prod](huntington-mlops-non-prod-cluster/README.md) | https://sigma.dev.hban.us | ✅ | AWS EKS |
| [Huntington MLOps Prod](huntington-mlops-prod-cluster/README.md) | https://sigma.prod.hban.us | ✅ | AWS EKS |
| [ICI](ici/README.md) | *(onboarding in progress)* | — | — |
| [JT Magen](jt-magen/README.md) | *(onboarding in progress)* | — | — |
| [Kev Group](kev-group/README.md) | https://kevgroup.hyperplane.dev | ✅ | Oracle Cloud |
| [Loblaw dev](loblaw-dev/README.md) | https://shakudo-lower.lblw.cloud | ❌ | GCP |
| [Loblaw prod](loblaw-prod/README.md) | https://shakudo.lblw.cloud | ❌ | GCP |
| [Martinrea](martinrea/README.md) | shakudo-management.martinrea.com | ✅ | On-Prem Bare Metal |
| [MCP](mcp/README.md) | https://mcp.hyperplane.dev | ✅ | Latitude (Shakudo) |
| [Osler, Hoskin and Harcourt LLP](osler/README.md) | *(scoping only — no environment yet)* | — | — |
| [PiinPoint](piinpoint/README.md) | https://piinpoint.hyperplane.dev | ✅ | Azure |
| [QuadReal dev1](quadreal-dev1/README.md) | http://shakudoqrdev1.internal.quadreal.com | ✅ | Azure |
| [QuadReal prod](quadreal-prod/README.md) | https://shakudoqrprd.internal.quadreal.com | ✅ | Azure |
| [QuadReal QA *(deprecated)*](quadreal-qa-deprecated/README.md) | http://shakudoqrqa.internal.quadreal.com | ✅ | Azure |
| [Quantum Metric](quantum-metric/README.md) | https://qm-datascience.hyperplane.dev | ✅ | GCP |
| [Reagan](reagan/README.md) | https://reagan.hyperplane.dev | ✅ | VM |
| [RiskThinking dev](riskthinking-dev/README.md) | https://riskthinking-dev.hyperplane.dev | ✅ | GCP |
| [RiskThinking prod](riskthinking-prod/README.md) | https://riskthinking-prod.hyperplane.dev | ✅ | GCP |
| [Ritual](ritual/README.md) | https://ritual2.hyperplane.dev | ✅ | GCP |
| [Whitecap POC](whitecap-poc-cluster-has-been-taken-down/README.md) | whitecap.hyperplane.dev *(cluster taken down)* | — | Hybrid On-Prem + AWS |
| [Whitecap PROD](whitecap-prod/README.md) | shakudo.wcap.ca | ✅ | Hybrid On-Prem + AWS |

---

## Hardcoded Secrets — Pending Migration to 1Password

The following plaintext credentials exist in this repo and need to be moved to 1Password:

| Customer | Type | Location |
|---|---|---|
| Reagan | TeamViewer password | `reagan/README.md` — Steps to access |
| Reagan | TeamViewer connection ID | `reagan/README.md` — Steps to access |
| Reagan | Windows laptop password | `reagan/README.md` — Steps to access |
| CloudHQ | SSH hosts / IPs | `cloudhq/README.md` — Steps to access Kubernetes |
| MCP | SSH host + port | `mcp/README.md` — Steps to access Kubernetes |
| Campbell | Master node internal IP | `campbell/README.md` — Steps to access Kubernetes |
