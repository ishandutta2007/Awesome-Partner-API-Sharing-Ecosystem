# Awesome-Partner-API-Sharing-Ecosystem

# Awesome Partner API Sharing & Ecosystem

> A curated list of top Partner API Sharing and Ecosystem platforms — both SaaS/Hosted commercial API management suites and open-source alternatives for publishing, governing, and onboarding partners to APIs.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [Sector Overview & Market Dynamics](#-sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
- [Open-Source Software](#-open-source-software)
  - [WSO2 API Manager](#wso2-api-manager)
  - [Kong Gateway (OSS)](#kong-gateway-oss)
  - [Tyk Gateway (OSS)](#tyk-gateway-oss)
  - [Apache APISIX](#apache-apisix)
  - [Gravitee API Management](#gravitee-api-management)
  - [Backstage](#backstage)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🌐 Sector Overview & Market Dynamics

The global API management and partner ecosystem market is valued at approximately **$7.7 Billion - $8.2 Billion** (growing at an estimated 16%–18% CAGR toward ~$21 Billion+ by 2030). The sector is **moderately concentrated at the top but surrounded by a fragmented, highly competitive fringe**: hyperscalers and legacy enterprise titans (Salesforce/MuleSoft, Google Apigee, Microsoft Azure, IBM) command the dominant enterprise market share, while specialized open-core/cloud-native challengers (Kong, Tyk, WSO2, Gravitee) aggressively compete and prevent a winner-take-all monopoly by driving innovation in developer portals, microservices, and AI/LLM gateway mediation.

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Partner API Sharing and Ecosystem platforms sorted by company scale (valuation / acquisition price):

| Platform | Type / Focus | Valuation / Revenue | Starting Price | Free Tier / Trial Limits | Best For |
|---|---|---|---|---|---|
| **MuleSoft Anypoint Partner Manager** | B2B partner onboarding & EDI/API ecosystem management | **$6.5B** valuation (Salesforce acquisition; ~$300M ARR at buyout) | **$2,000/mo** ($24,000/yr starting package for entry integration tier) | **30-day free trial** (Sales-assisted POC / restricted capacity; no permanent free tier) | Enterprises with complex B2B partner ecosystems needing unified EDI and API onboarding |
| **Kong Konnect** | API management control plane with developer portal & AI gateway | **$2.0B** valuation ($175M Series E; $100M+ ARR) | **$25/mo** (Serverless control plane; Hybrid starts at $200/mo, Cloud at $500/mo) | **30-day free trial** of Konnect Plus (no hard gateway limit, 30-day analytics retention; OSS gateway is free forever) | Organizations wanting a mature, widely deployed gateway with commercial portal & AI governance |
| **RapidAPI Enterprise Hub** | Internal API marketplace & partner sharing hub | **$1.0B** valuation (Series D; acquired by Nokia; ~$24M ARR) | **Custom quote** (Contract-based; minimum 5 team seats required) | **Custom sales-led POC / pilot** (No self-serve or permanent free tier for Enterprise Hub) | Organizations wanting an internal API marketplace with self-service discovery and governance |
| **WSO2 API Manager (Cloud)** | Full-lifecycle API management with developer portal | **$600M+** valuation (Acquired by EQT; ~$100M ARR) | **$119/mo** (Growth plan; covers 10 APIs and up to 10M requests/mo) | **30-day free trial** (Up to 5 APIs, 1M requests/mo, 1 Hybrid Gateway, 1 Developer Portal; core OSS self-hosted is free forever) | Organizations wanting comprehensive API management suite with developer portal and open-core flexibility |
| **Tyk Developer Portal** | API gateway & developer portal management stack | **$140M** valuation ($35M Series B; capital-efficient B-Corp) | **Quote-based commercial tiers** (Historical cloud tiers from ~$600/mo; Professional offers flat data-plane pricing) | **48-hour free trial** of Tyk Cloud (Full access; 14-day trial key for self-managed dashboard & portal; OSS gateway is free forever) | Teams wanting a complete management stack with multi-tenancy and flat data plane pricing options |

---

## 🟩 Open-Source Software

Self-hosted, community-driven Partner API Sharing and Ecosystem tools. The open-source ecosystem spans **full API management platforms with developer portals**, **high-performance gateways**, and **developer portal frameworks**.

### WSO2 API Manager
**Stack:** Java | **License:** Apache-2.0
WSO2 API Manager is a **complete open-source API management platform** with publisher, developer portal, gateway, key manager, and traffic manager components. For partner API sharing specifically, the **Developer Portal** is a fully featured, customizable web interface where partners can:
- **Self-register** and create applications 
- **Browse and subscribe** to APIs 
- **Generate and manage** OAuth2 keys and access tokens 
- **View documentation** and try APIs in a built-in API console 
- **Track usage** with built-in analytics 

The platform supports API monetization, rate limiting, and multi-tenancy. It is one of the most comprehensive open-source options, backed by a commercial company (WSO2) that also offers cloud hosting. **Trade-off:** It is a heavy Java deployment with significant resource requirements and configuration complexity.
**Best for:** Enterprises wanting a full-featured, Apache-licensed API management platform with a mature developer portal for partner onboarding, accepting the operational overhead.

### Kong Gateway (OSS)
**Stack:** Lua (OpenResty) | **License:** Apache-2.0 (OSS) / Proprietary (Enterprise)
Kong Gateway is the most widely deployed open-source API gateway, with a mature plugin ecosystem and strong commercial backing . For partner API sharing, it provides the **runtime gateway** with authentication, rate limiting, and transformation plugins, but the **Developer Portal is an Enterprise-only feature**—not available in the open-source gateway . The OSS gateway supports PostgreSQL-backed, DB-less, and hybrid deployment modes.
**Best for:** Teams wanting the most widely deployed OSS gateway as the runtime for partner APIs, accepting that the developer portal requires the commercial Kong Konnect offering.

### Tyk Gateway (OSS)
**Stack:** Go | **License:** MPL 2.0 (gateway) / Commercial (dashboard, portal)
Tyk Gateway is written in Go and provides a high-performance, lightweight gateway with authentication, rate limiting, and analytics. The **open-source edition includes the dashboard and developer portal**—one of the few gateways offering a complete self-service portal in OSS . It supports multi-tenancy, OAuth2, JWT, and OpenID Connect, with a plugin architecture for custom logic.
**Best for:** Teams wanting a complete OSS management stack (gateway + dashboard + developer portal) with multi-tenancy for partner sharing, accepting a smaller community than Kong.

### Apache APISIX
**Stack:** Lua (NGINX + LuaJIT) / etcd | **License:** Apache 2.0
Apache APISIX is a high-performance API gateway with a rich plugin ecosystem spanning authentication, traffic management, observability, and transformation . It is an Apache Software Foundation top-level project, community-governed and vendor-neutral. For partner API sharing, APISIX provides the **runtime gateway** but not a built-in developer portal—you would integrate with a separate portal or build one on top. **Trade-off:** Smaller community outside Asia-Pacific, with documentation quality sometimes inconsistent.
**Best for:** Teams wanting a high-performance, vendor-neutral OSS gateway for partner APIs, accepting that the developer portal must be sourced separately.

### Gravitee API Management
**Stack:** Java | **License:** Apache 2.0 (open-core)
Gravitee API Management is Apache-2.0 open-core, supporting HTTP and event-driven APIs (Kafka, MQTT, webhooks) under one gateway and portal . The **open-source gateway and portal** are available, with Enterprise unlocking AI/MCP features, audit trails, custom roles, and SSO. It provides a **developer portal** for partner self-service onboarding.
**Best for:** Teams needing both synchronous HTTP and event-driven API management with a developer portal, accepting that advanced governance is Enterprise-gated.

### Backstage
**Stack:** TypeScript / React / Node.js | **License:** Apache-2.0
Backstage (Spotify, CNCF) is an open-source **developer portal framework** for building internal developer platforms, with a **software catalog** that can include APIs, and plugins for API documentation and discovery . While not an API gateway, it provides the **portal layer** for partner-facing API catalogs, with plugin-based extensibility. It is positioned for platform teams wanting to build a custom developer experience.
**Best for:** Platform teams wanting to build a custom, extensible developer portal with API catalog capabilities, accepting that the gateway and API management logic must be sourced separately.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Developer Portal | Partner Onboarding | Gateway Included | Self-Hosted | Best For |
|----------|---------|-------|------------------|-------------------|------------------|-------------|----------|
| **MuleSoft Partner Manager** | Proprietary | Cloud | (Check) | ✅ B2B/EDI | (Anypoint) | ❌ | B2B partner ecosystems |
| **Kong Konnect** | Proprietary | Cloud | ✅ Enterprise | ✅ | ✅ | ❌ | Mature gateway + portal |
| **WSO2 API Manager** | Apache-2.0 | Java | ✅ Full-featured | ✅ Self-register | ✅ | ✅ | Full OSS API management |
| **Tyk (OSS)** | MPL 2.0 | Go | ✅ OSS included | ✅ Self-service | ✅ | ✅ | Complete OSS stack + multi-tenant |
| **Apache APISIX** | Apache 2.0 | Lua/etcd | ❌ (Gateway only) | (Separate portal) | ✅ | ✅ | High-performance gateway |
| **Gravitee** | Apache 2.0 | Java | ✅ OSS portal | ✅ Self-service | ✅ | ✅ | HTTP + event-driven APIs |
| **Backstage** | Apache-2.0 | TypeScript | ✅ Framework | (Plugin-based) | ❌ | ✅ | Custom portal framework |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Partner API Sharing or Ecosystem tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** Partner API sharing requires two distinct layers—a **runtime gateway** for enforcing access and rate limits, and a **developer portal** for partner onboarding and documentation. **WSO2 API Manager** and **Tyk** are the only open-source platforms that provide both layers in a single self-hosted package . **Kong** provides the most widely deployed gateway but gates its developer portal to the commercial Konnect offering . **Apache APISIX** and **Gravitee** offer gateways with varying portal capabilities—Gravitee includes a portal in its open-source edition, while APISIX does not . **Backstage** provides a portal framework but requires a separate gateway. For B2B/EDI partner ecosystems specifically, **MuleSoft Anypoint Partner Manager** remains the most comprehensive commercial option, with no open-source equivalent covering EDI partner onboarding at that depth.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
