
# Maven Inspectional Services – Power BI Report (Service-First Deployment)

## 🛠 Project Overview
This project delivers a Power BI solution for **Maven Inspectional Services** (permits, inspections, violations, SLAs, inspector workload). The emphasis is on **Power BI Service usage**—governance, deployment, refresh, sharing, and monitoring—so stakeholders can securely consume insights on web and mobile.

Emphasis on creating dataflows, connecting dataflows to semantic models, realtime refresh, and PowerBI service administration

---

## 🔑 Objectives
- Publish a single, governed **semantic model** to Power BI Service
- Operationalize **scheduled refresh** and **data gateways**
- Distribute content via **Power BI Apps** to business units
- Enforce **Row‑Level Security (RLS)** for inspectors/regions
- Track reliability with **refresh alerts**, **usage metrics**, and **lineage view**


## 🚀 Publish & Deploy (Power BI Service)
1. **Workspace**: Create a *Production* workspace (Premium per user or Pro). Use *Development* and *Test* workspaces for ALM.
2. **Publish**: From **Power BI Desktop**, `Publish` → target the *Development* workspace.
3. **Parameters**: Define connection parameters (server/database; SharePoint sites; file paths). Promote to **Deployment Pipeline** stages.
4. **Data Gateway**: If sources are on‑prem (SQL Server, file shares), configure **On‑premises data gateway** and map credentials.
5. **Scheduled Refresh**: Enable refresh (e.g., 4× daily during business hours). Add **failure notifications** to the BI admin and operations DL.
6. **Apps**: Package the reports and dashboards into a **Power BI App** with audience groups (e.g., *Operations*, *Leadership*, *Finance*).
7. **RLS**: Define roles (Inspector, Supervisor, Region Manager). Test with `View as role` in Desktop; enforce in Service via **Manage permissions**.
8. **Endorsement**: Mark the dataset as **Certified** once governance checks pass.



## 🔄 Refresh & Reliability
- **Frequency**: e.g., 08:00, 12:00, 16:00, 20:00 ET
- **Alerts**: configure **Refresh failure** alerts; add logic app/Power Automate if escalation needed
- **Usage Metrics**: Monitor report/app usage to understand adoption; prune unused artifacts
- **Lineage View**: Use **Lineage** to trace datasets → dataflows → gateways → sources; review after schema changes


## 📬 Contact & Support
please contact Cody for access requests, RLS changes, or refresh issues. Educational dataset provided by Maven Analytics
