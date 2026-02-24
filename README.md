Customer name,Environment URL,Accessible?,Airgapped (Y/N),Steps to access Kubernetes,Steps to access Dashboard,Infrastructure provider,Who manages the infra/cloud,Shakudo Version,Stack Components,Last updated on (stack components) - Put date even when no change,If changes, tag Shahzad/Chandan,Applications,Notes,who to ask,GPU available,,Backup enabled? What is backed up? and How?,,GPU config (VRAM? ),
Annexus,https://ai.annexus.cc/,yes,,Use the creds form [Client admin] Annexus vault,Use the creds form [Client admin] Annexus vault,AKS,,3.53.0,Grafana, AlertManager, GraphQl,Dec 17, 2025,,,,Shabbir,,,No back up,,,
Aristeia,http://shakudo.aristeiacapital.com,no,,kubeconfig is in 1password,login also in 1password,AWS,,,,,,,will not renew,Christine,,,No back up,,,
Avenue Capital,avenue-ai.avenue.corp 
(customer churned),yes,,First, contact Tirth for his shakudo_tpatel login to Avenue's citrix at https://my2.avenuecapital.com/logon/LogonPoint/index.html
Login using his credentials as well as the RSA+Token 2FA pin.
After that, login to the platform via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=6vjotuvd4wi2rufw3r7ll227ci&i=twtpp5ap763k5u2pcgh7t45jmi&h=shakudo.1password.com,,On Prem (self hosted)/ VM,,,inio, n8n, neo4j, ollama, open webui,inio, n8n, neo4j, ollama, open webui,,,will not renew,Yiran,,,No back up,,,
BWX prod,https://shakudo.bwxt.net,no,,contact customer for access, get on call with someone from their team (likely Alex from BWX),contact customer for access, get on call with someone from their team (likely Alex from BWX),On Prem (self hosted)/ VM,,v3.47.0-467c5f (confirmed on Dec 4th 2025),AirByte, Alert Manager, DataHub, Dify, Grafana, GraphQL, LabelStudio, Minio, N8n, Neo4j, Ollama, Qdrant, Supabase (they have a specific downgraded neo4j version),Dec 5,,,,Joowon, Elliott, Yiran,,,No back up,,,
Campbell,https://shakudo-1.campbell.com,yes,,Only one person can access the VM at a time. Joowon, Yiran, have access. There is a dedicated URL, go to the URL.  https://www.notion.so/shakudo/Campbell-206d36b5509080159e9bea6007e02b81?source=copy_link,connect to Shakudo-netgear wifi
open a browser and go to : https://securelink.campbell.com/rss-servlet/
log in with credentials 
once logged in, open MobaXTerm and connect to master node ip : 10.10.215.29
enter user/password to access the master node

instructions and credentials in 1password:
https://shakudo.1password.com/app#/C4MX52U47RH7JBO6VGGXN55SFE/Search/C4MX52U47RH7JBO6VGGXN55SFE:w3qvyjj7g7pntacaqwsaof2sv4:gjniipppxlqhzle4w2gyw55gja?itemListId=campbell,On Prem (self hosted)/ VM,,v3.55.0 (Jan 2026),Alertmanager, Dify, Grafana, GraphQL, MLflow, n8n, Neo4j, ollama, open webui, qdrant,Nov 6, 2025,,,,Joowon, Daniel, (logs in as Shawn),,Shahzad Ali Please check if Campbell is using LiteLLM. According to the earlier records (before this Nov 6 update), they were using LiteLLM too.

Chandan KumarWe have installed it again in the last week, it was uninstalled because they were facing some issues with it,No back up,,,cluster is theirs, 

CentralReach Dev,https://shakudo-dev-centralreach.hyperplane.dev,yes,,https://shakudo.1password.com/app#/C4MX52U47RH7JBO6VGGXN55SFE/Search/C4MX52U47RH7JBO6VGGXN55SFE:cogkypdjhzvlc2b42gcv6nx5om:mdvo72gyrtfeixcvbopexgonby?itemListId=centralr,Login via Onepass with Stella's account: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=3z2eengchebafygdyg2sfkbgma&i=5gmuy7fpejhta72yoldzglp6sq&h=shakudo.1password.com,AWS,,v3.46,Airbyte, Airflow, Alertmanager, Appsmith, Argo cd, Continue.dev, Dify, Dify(2), Dify(Enterprise), Dremio, Grafana, GraphQL, Harbor, Knowledge Table, Langfuse, Langfuse V3, Litellm, LlamaCloud, Minio, n8n, n8n ee, n8n prod, Nessie, Ollama, Openwebui, Qdrant, Supabase, Superset Dashboard, Windmill Dashboard, Windmill Enterprise, Xinference,Dec 15, 2025,,Extract Flow
MCP Proxy,,Joowon, Yijie, , Elliott,,d,No back up,,,
CentralReach Prod,Unknown because Todd updates the cluster themselves (TODO check the fireflies) ,no,,We can't -- you need to contact the customer team to get a hold a of Tood from CR, who has the kubeconfig and access to the environment. Todd can screenshare,We can't -- you need to contact the customer team to get a hold a of Tood from CR, who has the kubeconfig and access to the environment. Todd can screenshare,AWS,,,Sames as their dev cluster, but the onlyone used in prod are: n8n, dify, langfuse, ,Dec 5,,,,Yijie and Joowon have experience screensharing and sending stack component charts to Todd,,,No back up,,,
CloudHQ,https://shakudo1.cloudhq.com/

new environment being deployed.    

New Env: 

https://shakudo2.cloudhq.com,yes,,Old cluster: Connect to SHAKUDO-NETGEAR; this only works on the office network. 
ssh shakudo@52.180.153.118
ssh shakudo@52.165.89.75

New cluster: Connect to SHAKUDO-NETGEAR; this only works on the office network. 

ssh shakudo@161.129.62.4
ssh shakudo@161.129.62.3
,To access the dashboard: https://github.com/devsentient/task-tracking/issues/3096#issuecomment-2848141033,On Prem (self hosted),,,Airbyte, Appsmith, Appsmith Sandbox, Dremio, Longhorn, Minio, N8N, N8N Sandbox, Neo4J, Nessie, Open Webui, Qdrant, Supabase, Tooljet, WrenAI,OpenWebUI, CheckRequestsProd


,Dec 18, 2025,,,url doesn't work, shakudo version --> note that they are actively deploying a new environment,yiran, Usama (tasks only , not the environment), Daniel,,TODO check with Yiran,No back up,,,
Dynex,https://dynexcapital.canopyhub.io,no,,Ask the CS team to get us a call with Harman from Dynex. Harman will screenshare with us,Ask the CS team to get us a call with Harman from Dynex. Harman will screenshare with us,VMs on Azure,,,open-webui, n8n, neo4j, qdrant, litellm,,,,,yijie,,,No back up,,,
EJ Gallo,shakudodev.ejgallo.com,No,no,/,,,,,Grafana, AlertManager, GraphQl,Dec 17, 2025,,,,,,,No back up,,,
Ellis Don,no active environment -- deal not closed,,,,,,,,,,,,,,,,No back up,,,
En-powered,https://enpowered.hyperplane.dev/,yes,,kubeconfig is in 1password:
https://shakudo.1password.com/app#/C4MX52U47RH7JBO6VGGXN55SFE/Search/C4MX52U47RH7JBO6VGGXN55SFE:k555ly5l34e3pt3upit5s7mywe:nocc2qv5slkr33rvimsrvfdzzy?itemListId=enpowered,Login via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=w3qvyjj7g7pntacaqwsaof2sv4&i=ut4wnl3myfkzmn56oouz7xcs3a&h=shakudo.1password.com,Oracle cloud (Shakudo's account),,v3.33.0,mlflow, superset, gpu, pipelines,GraphQL,Grafana,Alertmanager,Supabase,pgbouncer,Nov 6, 2025,,,,Aazim, (debugging Adit's code),,d,No back up,,,
Flexivan,https://flexivan.hyperplane.dev/,yes,,For k9s admin access, download kubeconfig and access by following instructions in Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=dwafwcc6zvcuxfdvefl6ffn334&i=jwtavxeuyhtfgedxy5psonsa2m&h=shakudo.1password.com,https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=dwafwcc6zvcuxfdvefl6ffn334&i=pq6rcpxkfhwi32n73ml4qx6wga&h=shakudo.1password.com,AWS,,v3.47.0,minio, supabase, verdaccio, litellm, dify,Nov 6, 2025,,AgentFlow
MCP Proxy,,, daniel, bo, yijie,,d,No back up,,,
Hitachi Demo,hitachi.canopyhub.io,yes,,Latitude machines,,v3.49,,v3.49,Supabase, Neo4j, MinIO, PostGIS, Superset, Plotly, Airflow, Prefect, DBT, Meltano, Streamlit, Appsmith, MLFlow, LiteLLM, Langfuse


,Nov 6, 2025,,,,,,,No back up,,,
Hitachi Prod,,No,,,Only they have access,AWS,,v3.49,,,,,,,,,No back up,,,
Huntington Cyber non-Prod Cluster,https://artifactscanning.dev.hban.us ,yes,,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,AWS (EKS),,v3.44.0,GraphQL, Grafana, Alertmanager, Harbor, miniCRAN, Minio, Pypiserver ,Dec 11, 2025,,,Daniel's account is locked,Daniel, Shabbir,,d,No back up,,,
Huntington Cyber Prod Cluster,https://artifactscanning.hban.us ,yes,,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,AWS (EKS),,v3.44.0,GraphQL, Grafana, Alertmanager, Harbor, miniCRAN, Minio, Pypiserver , Trivy,Dec 11, 2025,Shahzad Ali Chandan Kumar,,Daniel's account is locked,Daniel, Shabbir,,d,No back up,,,
Huntington MLOps non-Prod Cluster,https://sigma.dev.hban.us ,yes,,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,AWS (EKS),,v3.44.0,GraphQL, Grafana, Alertmanager, Dify, Harbor, Langfuse v3, Litellm, Minio, N8N, Neo4j, Ollama, Promptfoo, Qdrant, Supabase,Dec 11, 2025,Shahzad Ali Chandan Kumar,,Daniel's account is locked,Daniel, Shabbir,,d,EBS Backups
Velero,,,
Huntington MLOps Prod Cluster,https://sigma.prod.hban.us ,yes,,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,https://www.notion.so/shakudo/HNB-Environment-Doc-226d36b55090808d80f0d6ca1487e8c7,AWS (EKS),,v3.44.0,GraphQL, Grafana, Alertmanager, Dify, Harbor, Langfuse v3, Litellm, Minio, N8N, Ollama, Promptfoo, Qdrant,Dec 11, 2025,,,Daniel's account is locked,Daniel, Shabbir,,d,EBS Backups
Velero,,,
Kev Group,https://kevgroup.hyperplane.dev/,yes,,For k9s access, use kubeconfig in Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=smych5flne2apr6rkmv67ouihu&i=ljommdgqwbdil2vifeuqkzo6aa&h=shakudo.1password.com,Login to /auth/ with https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=nxwamkpxcaj6mstxz7nyvdalym&i=evzgtmjhnlxmlixhru4jujpfp4&h=shakudo.1password.com,Oracle cloud (Shakudo's account),,,,,,,wrong credentials, can not access,,,d,No back up,,,
Loblaw dev,https://shakudo-lower.lblw.cloud/,no,,Yijie, Umang, Neshay has access,Yijie, Umang, Neshay has access,GCP,,v3.49.0,Langfuse, Neo4j, postgresSQL, dify, clickhouse, minio, litellm,,,,Environment wasn't accessible in dec check,Yijie, Umang,,,No back up,,,
Loblaw prod,https://shakudo.lblw.cloud/,no,,Yijie, Umang, Neshay has access,Yijie, Umang, Neshay has access,GCP,,v3.49.0,GraphQL, Alertmanager, Grafana, WrenAI, Xinference, N8n, Langfuse V3 Prod, Langfuse V3 Dev, Ollama, Qdrant Hre Prod, Nessie, Qdrant Garfield, Ollama High, Litellm Dev, Qdrant Robin, LiteLLM, Litellm, Airbyte, Dify, DataHub Dashboard, Supabase, Dify-dev, Qdrant Heliosai, Qdrant Apps, Rill, Ollama Cpu, Qdrant Robin Prod, Neo4j, Minio Prod, Litellm Prod,Dec 11, 2025,Chandan Kumar,MCP Proxy,,Yijie, Umang,,,No back up,,,
Martinrea,shakudo-management.martinrea.com,Yes,,Go to cyberarkca.martinrea.app.ca.alero.io/PasswordVault/v10/Accounts, login as Yiran's account and let Yiran to scan the QR code (more devs are onboarding but currently only Yiran),Yijie, Umang, Neshay has access,On-premises bare metal machines (not cloud-based),,v3.47 (Carsten on Feb 4th 2026 v3.45.0-05f7d2
 ,minio, supabase, MongoDB,,,,environment can not be accessed, because their cyber arc is down,Yiran, Daniel (set up but never accessed), (worked on tasks) ,,TODO ask Yiran Wang to fill in this row,No back up,,,
MCP,https://mcp.hyperplane.dev/,yes,,no kubeconfig, just ssh. Yiran has access to it and adds public keys
1. make your private and public key pair if you have not already
2. give yiran the public key, it will have the .pub extention
3. can now ssh without password (ask yiran for the ip and username)
4. find the kubeconfig and scp it onto your computer
ssh command: ssh ubuntu@186.233.184.151 -p 2222,https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=oirywnqgvozmeo4ysld2n3wsim&i=sxdbiijvvf3i5y46l7eqvpzvxi&h=shakudo.1password.com,Shakudo managed on Latitude,,v3.48.0,GraphQL, Grafana, Alertmanager, Qdrant, Langfuse V3, n8n, LiteLLM, Open Web UI, Open Web UI 1,  Neo4j, Minio


,Dec 10, 2025,,,,yijie, shabbir,,d,No back up,,,
Osler, Hoskin and Harcourt LLP,no environment yet, scoping only ,,,,,,,,,,,,,,,,No back up,,,
PiinPoint,https://piinpoint.hyperplane.dev,yes,,piinpoint's kubeconfig is in one password: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=kvlukilj7v7zmqbmkjsdfjg26i&i=lasgicfs3evxyvjer36x65fsgq&h=shakudo.1password.com,https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=luxjcpov6t2xbj6exsts2qhktm&i=yseoeo3jrnmorbyaewscfftrxy&h=shakudo.1password.com,Azure,,,GraphQL, Grafana, Alertmanager, Dify, Langfuse, Minio, n8n, Supabase,Dec 10, 2025,Shahzad Ali,,,Shabbir,,d,No back up,,,
QuadReal dev1,http://shakudoqrdev1.internal.quadreal.com,yes,,https://portal.azure.com - login to their azure with username_admin@quadreal.com. Find this vm -> vmedpmgtdev1001 and connect with bastion. login creds are the username and password used to login to azure. After that open chrome and login to their platform, login creds for platform are on 1password,Get QuadReal to create you a user account

Login to https://portal.azure.com/#@quadreal.com using any shakudo staff's _admin@quadreal.com postfix account. Would need to enter 2FA code in Azure Authenticator (mobile app).

After that, use the same credentials to connect to vmedpmgtdev1001 vm via Bastion.

Login to platform using Azure AD OIDC.

For deployment access, connect to temporary-shakudo-installer-vm in rg-eda-ae-edp-cp-dev1-001 resource group via Bastion using Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=zeouwz7le5lbmmhxvfggkfbgee&i=6clagep3v5gyvdra43minlidk4&h=shakudo.1password.com,Azure,,,grafana, Plotly/Dash, Harbor, Sedona, Airbyte, Appsmith, Argocd, Clickhouse, Datahub, Dify, Elasticsearch, Litellm, Minio, Mlflow, N8N, N8N enterprise, Ollama, Open webui, Qdrant, Spark Supabase, Wrenai,Nov 6, 2025,,,only three engineers have access to the environment,, Daniel, Yiran,,,No back up,,,
QuadReal prod,https://shakudoqrprd.internal.quadreal.com,yes,,https://portal.azure.com - login to their azure with username_admin@quadreal.com. Find this vm -> vmedpmgtprd1001 and connect with bastion. login creds are the username and password used to login to azure. After that open chrome and login to their platform, login creds for platform are on 1password,Login to https://portal.azure.com/#@quadreal.com using any shakudo staff's _admin@quadreal.com postfix account. Would need to enter 2FA code in Azure Authenticator (mobile app).

After that, use the same credentials to connect to vmedpmgtprd001 vm via Bastion.

Login to platform using Azure AD OIDC.

For deployment access, connect to temporary-shakudo-installer-vm-prd via Bastion using Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=nxwamkpxcaj6mstxz7nyvdalym&i=gikqo6lrswqzq4k5bhsig2xddm&h=shakudo.1password.com,Azure,,v3.48,grafana, Plotly/Dash, Harbor, Sedona, elasticsearch, minio, n8n,Nov 6, 2025,,,only three engineers have access to the environment,, Daniel, Yiran,,,No back up,,,
QuadReal QA (deprecated),http://shakudoqrqa.internal.quadreal.com,yes,,,,Azure,,,,,,,,,,,No back up,,,
Quantum Metric,https://qm-datascience.hyperplane.dev/,yes,,,Login via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=pqi5mkcaeawsyldluc4ozvuymy&i=doc37dhfswkcilc536bogwpvfa&h=shakudo.1password.com,GCP,,,,,,,their dashboard is down but the main user has left the company -- put this on ice for now,Christine,,,No back up,,,
Reagan,https://reagan.hyperplane.dev,yes,,1. A user needs to download TeamViewer.
2. Connect to 846 602 446
3. Permanent Pass: j9uHWKfmgAjz
Their machine is offline sometimes. In such cases, please ask CS to reach out to the client (Chris) for assistance,1. A user needs to download TeamViewer.
2. Connect to 846 602 446
3. Permanent Pass: j9uHWKfmgAjz
Their machine is offline sometimes. In such cases, please ask Sid or Jason to reach out to the client for assistance
Window password inside their laptop: shakudo ,VM,,v3.34.2,GraphQL, Grafana, Alertmanager, Open Webui, agent-flow-app, Litellm, Ollama (CPU), Ollama (GPU), Open WebUI, Dify, Appsmith, Supabase, Qdrant, MinIO, Airbyte,Dec 10, 2025,,,,Joowon, Yijie,,d,No back up,,,
RiskThinking dev,https://riskthinking-dev.hyperplane.dev,yes,,,Login via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=nxwamkpxcaj6mstxz7nyvdalym&i=rwdcecdbffd2pii7eykywri65a&h=shakudo.1password.com,GCP,,v3.41.0-33fbf7
Feb 2025,harbor, Satellite clusters,,,,low-priority environment for now,Christine,,,No back up,,,
RiskThinking prod,https://riskthinking-prod.hyperplane.dev,yes,,,Login via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=lyg6tgxqh533cztaylftuivwou&i=qrgngdkj4765bpzl2mgx6pgjdy&h=shakudo.1password.com,GCP,,,,,Environment wasn't accessible in dec check,,low-priority environment for now,Christine,,,No back up,,,
Ritual,https://ritual2.hyperplane.dev,yes,,kubeconfig in 1password: https://shakudo.1password.com/app#/C4MX52U47RH7JBO6VGGXN55SFE/Search/C4MX52U47RH7JBO6VGGXN55SFE:v4ajp74ot5evxcu75xrtel5yba:zdmotiaphcqp42rdhs54pjwrju?itemListId=ritual,Login via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=v4ajp74ot5evxcu75xrtel5yba&i=6zg3htdtug5xptvsbb3tcdr7um&h=shakudo.1password.com,GCP,,,Alertmanager, Grafana, Graphql, minio, n8n, supabase,Dec 15, 2025,,,,joowon, Yiran,,d,No back up,,,
Whitecap POC (cluster has been taken down),



POC: whitecap.hyperplane.dev,yes,yes,
Go on Citrix first
use daniel credentials in 1password,\First, login to environment using Citrix via Onepass: https://start.1password.com/open/i?https://shakudo.1password.com/app#/C4MX52U47RH7JBO6VGGXN55SFE/Search/C4MX52U47RH7JBO6VGGXN55SFE:r44tcobo5ygktgh7uzcftk2uoy:kbgxbi7dvhkkmm2ppmb4mrrgha?itemListId=whitecap
Then, ask Daniel to enter 2FA code and approve.
Finally, login to dashboard via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=r44tcobo5ygktgh7uzcftk2uoy&i=bqsthgxtcbyjluiuebm3h3cwpq&h=shakudo.1password.com,Hybrid (On-premises + AWS)
Primary: On-premises bare metal servers across 2 datacenters
Secondary: AWS (for HA quorum maintenance only),,v3.49.0,airbyte,appsmith,datahub,dify,dremio,kestra,minio,n8n,neo4j,nessie,ollama,open-webui,qdrant,supabase,superset,wrenai, mlflow,,,,,Shabbir, Daniel,,d,No back up,,,
Whitecap PROD,PROD: shakudo.wcap.ca,Only read access for Daniel's account,,
Go on Citrix first
use daniel credentials in 1password,\First, login to environment using Citrix via Onepass: https://start.1password.com/open/i?https://shakudo.1password.com/app#/C4MX52U47RH7JBO6VGGXN55SFE/Search/C4MX52U47RH7JBO6VGGXN55SFE:r44tcobo5ygktgh7uzcftk2uoy:kbgxbi7dvhkkmm2ppmb4mrrgha?itemListId=whitecap
Then, ask Daniel to enter 2FA code and approve.
Finally, login to dashboard via Onepass: https://start.1password.com/open/i?a=C4MX52U47RH7JBO6VGGXN55SFE&v=r44tcobo5ygktgh7uzcftk2uoy&i=bqsthgxtcbyjluiuebm3h3cwpq&h=shakudo.1password.com,,,v3.49.0 Sept 4th 2025,Alertmanager, Dify, Grafana, GraphQL, Harbor, Langfuse V3, LiteLLM, Minio, Ollama, Promptfoo, Qdrant,Dec 10, 2025,,,,,,,Whitecap has no backup, but they have longhorn for multiAz setup,,,
JT Magen,,,,,,,,,,,,,New customer, onboarding in progress (First 30 Days),Juliana Salazar, Alok Sharma,,,,,,
ICI,,,,,,,,,Apache Airflow, Airbyte, MinIO, PostgreSQL (Supabase), Appsmith, Superset, DataHub, Gitea, N8n,,,,New customer, onboarding in progress. ETF Data Collection & Augmentation use case.,Elizabeth A, Juliana Salazar,,,,,,
,,,,,,,,,,,,,,,,,,,,