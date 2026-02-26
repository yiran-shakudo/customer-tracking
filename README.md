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
    ├── README.md          ← all columns for that customer
    └── OnePassVault.md    ← mapped 1Password vaults (empty if none)
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

| Customer | Environment URL | Accessible | Infrastructure | 1Password Vault |
|---|---|:---:|---|---|
| [Annexus](annexus/README.md) | https://ai.annexus.cc | ✅ | AKS | [Admin](annexus/OnePassVault.md) |
| [Aristeia](aristeia/README.md) | http://shakudo.aristeiacapital.com | ❌ | AWS | [Admin · Maintainer](aristeia/OnePassVault.md) |
| [Avenue Capital](avenue-capital/README.md) | avenue-ai.avenue.corp *(churned)* | — | On-Prem VM | [Admin · Maintainer](avenue-capital/OnePassVault.md) |
| [BWX prod](bwx-prod/README.md) | https://shakudo.bwxt.net | ❌ | On-Prem VM | [Admin](bwx-prod/OnePassVault.md) |
| [Campbell](campbell/README.md) | https://shakudo-1.campbell.com | ✅ | On-Prem VM | [Maintainer](campbell/OnePassVault.md) |
| [CentralReach Dev](centralreach-dev/README.md) | https://shakudo-dev-centralreach.hyperplane.dev | ✅ | AWS | [Admin · Maintainer · External](centralreach-dev/OnePassVault.md) |
| [CentralReach Prod](centralreach-prod/README.md) | *(Todd manages — screenshare only)* | ❌ | AWS | [Admin · Maintainer · External](centralreach-prod/OnePassVault.md) |
| [CloudHQ](cloudhq/README.md) | https://shakudo1.cloudhq.com | ✅ | On-Prem | [Admin](cloudhq/OnePassVault.md) |
| [Dynex](dynex/README.md) | https://dynexcapital.canopyhub.io | ❌ | Azure VMs | [Admin](dynex/OnePassVault.md) |
| [EJ Gallo](ej-gallo/README.md) | shakudodev.ejgallo.com | ❌ | — | [Admin](ej-gallo/OnePassVault.md) |
| [Ellis Don](ellis-don/README.md) | *(no active environment — deal not closed)* | — | — | ⚠️ No vault |
| [En-powered](en-powered/README.md) | https://enpowered.hyperplane.dev | ✅ | Oracle Cloud | [Admin · Maintainer](en-powered/OnePassVault.md) |
| [Flexivan](flexivan/README.md) | https://flexivan.hyperplane.dev | ✅ | AWS | [Admin](flexivan/OnePassVault.md) |
| [Hitachi Demo](hitachi-demo/README.md) | hitachi.canopyhub.io | ✅ | Latitude | [Admin](hitachi-demo/OnePassVault.md) |
| [Hitachi Prod](hitachi-prod/README.md) | *(customer-managed)* | ❌ | AWS | [Admin](hitachi-prod/OnePassVault.md) |
| [Huntington Cyber non-Prod](huntington-cyber-non-prod-cluster/README.md) | https://artifactscanning.dev.hban.us | ✅ | AWS EKS | [Admin · External](huntington-cyber-non-prod-cluster/OnePassVault.md) |
| [Huntington Cyber Prod](huntington-cyber-prod-cluster/README.md) | https://artifactscanning.hban.us | ✅ | AWS EKS | [Admin · External](huntington-cyber-prod-cluster/OnePassVault.md) |
| [Huntington MLOps non-Prod](huntington-mlops-non-prod-cluster/README.md) | https://sigma.dev.hban.us | ✅ | AWS EKS | [Admin · External](huntington-mlops-non-prod-cluster/OnePassVault.md) |
| [Huntington MLOps Prod](huntington-mlops-prod-cluster/README.md) | https://sigma.prod.hban.us | ✅ | AWS EKS | [Admin · External](huntington-mlops-prod-cluster/OnePassVault.md) |
| [ICI](ici/README.md) | *(onboarding in progress)* | — | — | [Admin](ici/OnePassVault.md) |
| [JT Magen](jt-magen/README.md) | *(onboarding in progress)* | — | — | [Admin](jt-magen/OnePassVault.md) |
| [Kev Group](kev-group/README.md) | https://kevgroup.hyperplane.dev | ✅ | Oracle Cloud | [Admin · Maintainer](kev-group/OnePassVault.md) |
| [Loblaw dev](loblaw-dev/README.md) | https://shakudo-lower.lblw.cloud | ❌ | GCP | [Maintainer](loblaw-dev/OnePassVault.md) |
| [Loblaw prod](loblaw-prod/README.md) | https://shakudo.lblw.cloud | ❌ | GCP | [Maintainer](loblaw-prod/OnePassVault.md) |
| [Martinrea](martinrea/README.md) | shakudo-management.martinrea.com | ✅ | On-Prem Bare Metal | [Admin](martinrea/OnePassVault.md) |
| [MCP](mcp/README.md) | https://mcp.hyperplane.dev | ✅ | Latitude (Shakudo) | [Admin](mcp/OnePassVault.md) |
| [Osler, Hoskin and Harcourt LLP](osler/README.md) | *(scoping only — no environment yet)* | — | — | ⚠️ No vault |
| [PiinPoint](piinpoint/README.md) | https://piinpoint.hyperplane.dev | ✅ | Azure | [Admin · Maintainer](piinpoint/OnePassVault.md) |
| [QuadReal dev1](quadreal-dev1/README.md) | http://shakudoqrdev1.internal.quadreal.com | ✅ | Azure | [Admin · Maintainer · Shared](quadreal-dev1/OnePassVault.md) |
| [QuadReal prod](quadreal-prod/README.md) | https://shakudoqrprd.internal.quadreal.com | ✅ | Azure | [Admin · Maintainer · Shared](quadreal-prod/OnePassVault.md) |
| [QuadReal QA *(deprecated)*](quadreal-qa-deprecated/README.md) | http://shakudoqrqa.internal.quadreal.com | ✅ | Azure | [Admin · Maintainer · Shared](quadreal-qa-deprecated/OnePassVault.md) |
| [Quantum Metric](quantum-metric/README.md) | https://qm-datascience.hyperplane.dev | ✅ | GCP | [Admin · Maintainer](quantum-metric/OnePassVault.md) |
| [Reagan](reagan/README.md) | https://reagan.hyperplane.dev | ✅ | VM | [Admin](reagan/OnePassVault.md) |
| [RiskThinking dev](riskthinking-dev/README.md) | https://riskthinking-dev.hyperplane.dev | ✅ | GCP | [Admin · Maintainer](riskthinking-dev/OnePassVault.md) |
| [RiskThinking prod](riskthinking-prod/README.md) | https://riskthinking-prod.hyperplane.dev | ✅ | GCP | [Admin · Maintainer](riskthinking-prod/OnePassVault.md) |
| [Ritual](ritual/README.md) | https://ritual2.hyperplane.dev | ✅ | GCP | [Admin · Maintainer](ritual/OnePassVault.md) |
| [Whitecap POC](whitecap-poc-cluster-has-been-taken-down/README.md) | whitecap.hyperplane.dev *(cluster taken down)* | — | Hybrid On-Prem + AWS | [Admin · External](whitecap-poc-cluster-has-been-taken-down/OnePassVault.md) |
| [Whitecap PROD](whitecap-prod/README.md) | shakudo.wcap.ca | ✅ | Hybrid On-Prem + AWS | [Admin · External](whitecap-prod/OnePassVault.md) |

### Customers without a 1Password vault

| Customer | Reason |
|---|---|
| Ellis Don | No active environment — deal not closed |
| Osler | Scoping only — no environment yet |

---

## Hardcoded Secrets — Migration Status

| Customer | Type | Status | 1Password Item |
|---|---|:---:|---|
| Reagan | TeamViewer connection ID + password | ✅ Migrated | [Reagan TeamViewer Access](https://shakudo.1password.com/app#/vaults/o6jsizs4a3utxuy7sr2ce6odq4/items/t4wokj7y23p2bla5xks4kpzxki) |
| Reagan | Windows laptop password | ✅ Migrated | [Reagan Windows Laptop](https://shakudo.1password.com/app#/vaults/o6jsizs4a3utxuy7sr2ce6odq4/items/q2tmlxmsgyiibgxptwprqp5rku) |
| Campbell | Master node internal IP | ✅ Migrated | [Campbell Master Node](https://shakudo.1password.com/app#/vaults/sj5sdxgz7gepoxuaa33zpxobam/items/id4r32oki6fznbdruciwvvixve) |
| CloudHQ | SSH hosts / IPs (4 nodes) | ✅ Migrated | [CloudHQ SSH Nodes (Old Cluster)](https://shakudo.1password.com/app#/vaults/qb6evallmv3v5v3yev67nnqcxm/items/jfl7vwk6c7wmlh2ckqdt6xqa7m) · [New Cluster](https://shakudo.1password.com/app#/vaults/qb6evallmv3v5v3yev67nnqcxm/items/c4buwzjipdv6wvrl2wgl2jn54e) |
| MCP | SSH host + port | ✅ Migrated | [MCP SSH Access](https://shakudo.1password.com/app#/vaults/zwgd3omhtwxsdakm7cd64iqwpa/items/or4ztyacvacsjs76mdey2arv4i) |
