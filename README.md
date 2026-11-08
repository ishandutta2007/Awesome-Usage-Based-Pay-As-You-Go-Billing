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

| Platform | Company Size (Valuation / Revenue) | Type | Starting Pricing | Free Tier / Trial Limit |
|---|---|---|---|---|
| **Chargebee** | Valuation: ~$3.5B (Est. Revenue: ~$200M–$300M ARR) | Subscription & hybrid usage billing | Free up to $250k cumulative revenue, then 0.75% overage fee (or Starter from $0/mo; Performance tier from $599/mo) | Free forever for up to $250,000 in lifetime billing (up to $1M revenue for qualifying startups) |
| **Zuora** | Valuation: $1.7B (Acquired by Silver Lake/GIC; ARR: ~$410M–$420M) | Enterprise metered billing & revenue automation | Enterprise contracts typically start at ~$75,000/year (billed annually based on volume/edition) | 30-day evaluation trial / sandbox environment available upon enterprise sales qualification |
| **Metronome** | Valuation: $1.0B (Acquired by Stripe; $130M venture funding) | High-volume AI & API consumption billing | Starter plan: 0.8% of billings + $0.04 per 1,000 ingested events (Custom enterprise) | Free tier available (no upfront monthly subscription platform fee; pay-per-event/billings) |
| **Orb** | Valuation: $335M (Acquired by Adyen; $44.1M venture funding) | Developer-centric usage billing infrastructure | Paid plan starts at $20/month (or $200/year for up to 5 Orbs; Custom enterprise) | Free forever plan with 10 Orbs included |
| **m3ter** | Valuation: ~$140M (Acquired by Salesforce; $31.5M funding) | Metered rating engine & pricing operations | Custom monthly base platform fee (typically starts with custom enterprise deployments) | No public self-serve free tier; custom proof-of-concept (PoC) / sandbox provided upon demo request |
| **Amberflo** | Valuation: ~$60M–$80M est. ($20M venture funding raised) | Real-time cloud metering & cost calculation | Free tier; paid startup tiers start at $99/month (or pay-as-you-go overages) | Free forever plan includes up to 1,000,000 meter events per month |
| **Togai** | Valuation: ~$20M–$30M est. ($3.1M seed; Acquired by Zuora) | Usage metering & pricing orchestrator | Historically Starter from $0/mo; Growth tier at 0.5% of invoice amount (now part of Zuora) | Free Starter tier offered 1,000,000 events/month and up to $10,000 in monthly invoice volume |
| **Octane** | Valuation: ~$15M–$25M est. ($8M–$10M funding; Acquired by Stripe) | Usage-based pricing & monetization engine | Seed-stage developer API platform (Acquired by Stripe; custom enterprise quote) | Custom developer sandbox / pilot trial access upon consultation request |
| **Monetize360** | Valuation: ~$12M–$18M est. ($3.7M venture funding raised) | Revenue infrastructure for consumption & outcome models | Custom enterprise platform quotation based on high-volume data streams & modules | No self-serve free tier; custom evaluation lab / sandbox environment granted via enterprise sales demo |

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
