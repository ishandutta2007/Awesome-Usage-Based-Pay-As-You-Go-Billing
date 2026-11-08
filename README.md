# Awesome-Usage-Based-Pay-As-You-Go-Billing

# Awesome Usage-Based & Pay-as-you-go Billing

> A curated list of top Usage-Based and Pay-as-you-go Billing platforms — both SaaS/Hosted commercial solutions and open-source alternatives for metering, rating, and invoicing consumption-based pricing.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Chargebee](#chargebee)
  - [Metronome](#metronome)
  - [Orb](#orb)
  - [m3ter](#m3ter)
  - [Togai](#togai)
  - [Amberflo](#amberflo)
  - [Octane](#octane)
  - [Monetize360](#monetize360)
  - [Zuora](#zuora)
- [Open-Source Software](#-open-source-software)
  - [Lago](#lago)
  - [OpenMeter](#openmeter)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Usage-Based and Pay-as-you-go Billing platforms. These are not open-source but are included as reference points for feature comparison.

### Chargebee
**Type:** Subscription and usage-based billing platform  
Chargebee's Usage Ecosystem provides high-volume usage ingestion with schemaless tracking, flexible pricing design (pay-as-you-go, bundled features, or hybrid plans), and accurate billing at scale [citation:1]. It supports two primary usage models: **Fixed Fee + Overages** (base fee for included usage, per-unit charges beyond) and **Pay As You Go** (billed only for consumption during the billing cycle) [citation:12]. The platform offers 100 million free usage events per month for 24 months to customers who sign up by June 30, 2025 [citation:1].

### Metronome
**Type:** Usage-based billing infrastructure for AI and API products  
Metronome is purpose-built for high-volume, real-time metering. Its billable metrics support aggregation types including count, sum, unique, max, and latest, plus SQL-based metrics for complex calculations [citation:2]. **Group keys** enable dimensional pricing (different rates per AI model, region, or instance type) and invoice line-item breakdowns. Products can be usage, subscription, composite, or fixed, with tiered rates and commit drawdown support [citation:2][citation:13]. SDKs are available for multiple languages.

### Orb
**Type:** Billing infrastructure for usage-based and hybrid pricing  
Orb provides usage-based pricing, metering, and invoicing for API and cloud products [citation:14]. It offers a **Free Forever** tier with 10 Orbs included, and a paid plan at $20/month or $200/year for up to 5 Orbs, with custom enterprise pricing for higher volumes [citation:3]. Positioned for developers wanting straightforward usage billing without enterprise sales cycles.

### m3ter
**Type:** Metered billing and pricing platform  
m3ter provides a comprehensive metering and rating engine for usage-based pricing. The platform includes a Console for configuration and API access, with a structured workflow covering accounts, products, meters, and bills [citation:5]. It supports tiered, volume, and custom pricing models, with worked examples for implementing usage-based pricing solutions.

### Togai
**Type:** Usage metering and billing with flexible pricing models  
Togai is built around pricing configurability, supporting usage-based, seat-based, and hybrid models, with pre-paid, credits, post-paid, and commitment payment terms [citation:6]. Its four building blocks are: event schema definition, metering aggregation, price plan configuration, and customer onboarding. The platform automates invoicing at the end of each billing cycle based on configured rate cards [citation:6].

### Amberflo
**Type:** Metering and cost calculation platform  
Amberflo's meter rates define how usage converts to cost. It supports **Per Unit** pricing (uniform cost per unit) and **Per Unit with Dimensions** (cost varies by usage attributes), which is the standard approach for real-world systems like token-based AI pricing [citation:7]. Rates can change over time with new configurations applied going forward, preserving historical accuracy.

### Octane
**Type:** Usage-based pricing and monetization platform  
Octane provides a REST API for managing meters, pricing plans, customer entitlements, and real-time usage tracking. It supports counters, metered components, flat-rate schemes, discounts, trials, and add-ons. API resources include Meters, Price Plans, Subscriptions, Customers, Invoices, Credits, and Live Measurements, enabling real-time usage retrieval [citation:8].

### Monetize360
**Type:** Revenue infrastructure for consumption and outcome-based models  
Monetize360 positions itself as a financial control layer for metering, pricing, and revenue capture across usage, consumption, tokens, and agent-based models [citation:9]. It is SOC 2 Type 2 certified and deployable on SaaS, Virtual Private Cloud, or on-premises. API-native connectors integrate with existing ERP, CRM, and billing platforms rather than requiring rip-and-replace [citation:9].

### Zuora
**Type:** Enterprise metered billing and revenue recognition  
Zuora provides usage-based pricing and billing with a focus on finance teams. It supports metered, tiered, volume block, and overage pricing models, plus committed usage automation for prepaid and token-based models . Features include detailed usage line items on invoices, revenue recognition templates, and audit-ready usage reporting that traces back to individual usage records .

---

## 🟩 Open-Source Software

Self-hosted, community-driven Usage-Based Billing platforms. The open-source ecosystem in this category is currently led by two mature projects.

### Lago
**Stack:** Ruby / PostgreSQL / ClickHouse / Redis | **License:** AGPL-3.0  
Lago is the most established open-source billing platform, with 10.4K+ GitHub stars and AGPLv3 licensing [citation:15]. It handles usage-based, subscription, prepaid, and hybrid pricing on a single engine. The open-source edition provides core billing infrastructure: usage ingestion, billable metrics, plans, subscriptions, invoicing, and payment integrations. Premium capabilities (customer portals, prepaid credits, multiple billing entities, analytics, Lago AI, MCP) are available under commercial agreements [citation:4]. Lago does not replace your payment processor — it calculates charges, generates invoices, and connects to Stripe, Adyen, and GoCardless for collection [citation:15].  
**Best for:** Teams wanting a proven, self-hosted billing engine with genuine open-source licensing and the flexibility to extend the code.

### OpenMeter
**Stack:** Go / PostgreSQL / ClickHouse / Kafka | **License:** Apache-2.0  
OpenMeter is an open-source real-time metering and billing engine optimized for high-volume event ingestion [citation:11]. It ingests events via CloudEvents format, defines meters with flexible aggregations (SUM, COUNT, AVG, MIN, MAX), and queries usage in real time. Features include usage-based billing with tiered/graduated/flat-fee pricing, usage limits and entitlements with real-time balance tracking, product catalog with rate cards, prepaid credits, customer portal, webhook notifications, and **first-class LLM token cost tracking** [citation:11]. Architecture uses Kafka for streaming, ClickHouse for aggregation, and PostgreSQL for billing. Deploys via Docker Compose or Kubernetes Helm chart.  
**Best for:** Teams building AI, agentic, or DevTool products that need real-time metering with Apache-2.0 licensing and no AGPL obligations.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Self-Hosted | LLM Token Tracking | Best For |
|----------|---------|-------|-------------|-------------------|----------|
| **Chargebee** | Proprietary | Cloud | ❌ | Via events | Subscription + usage hybrid |
| **Metronome** | Proprietary | Cloud | ❌ | ✅ (group keys) | High-volume AI/API billing |
| **Orb** | Proprietary | Cloud | ❌ | (Check) | Developer-friendly usage billing |
| **m3ter** | Proprietary | Cloud | ❌ | (Check) | Metered billing configuration |
| **Togai** | Proprietary | Cloud | ❌ | (Check) | Flexible pricing models |
| **Amberflo** | Proprietary | Cloud | ❌ | ✅ (dimensions) | Cost calculation + dimensions |
| **Octane** | Proprietary | Cloud | ❌ | (Check) | Real-time usage API |
| **Monetize360** | Proprietary | Cloud/VPC/on-prem | (Enterprise) | ✅ (tokens/agents) | Consumption + outcome revenue |
| **Zuora** | Proprietary | Cloud | ❌ | ✅ (committed usage) | Enterprise finance metering |
| **Lago** | AGPL-3.0 | Ruby/PostgreSQL | ✅ | (Via events) | Proven open-source billing |
| **OpenMeter** | Apache-2.0 | Go/ClickHouse/Kafka | ✅ | ✅ (first-class) | Real-time AI/DevTool metering |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Usage-Based or Pay-as-you-go Billing platform that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for usage-based billing is **very limited** — Lago and OpenMeter are the two mature options, with OpenMeter being the stronger choice for real-time AI/LLM token metering under a permissive Apache-2.0 license.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
