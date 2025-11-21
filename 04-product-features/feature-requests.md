# Feature Requests

## Overview

This document tracks planned product modules (3, 4, 5) and feature enhancements based on client requirements, primarily from PNK Group as anchor client, **plus competitive gap features** identified from analysis of Acres.com and Dodda.ai.

**Last Updated:** November 21, 2025

---

## Competitive Gap Features (Priority: CRITICAL-HIGH)
*Based on competitive analysis of Acres.com and Dodda.ai - November 2025*

### 🔴 CRITICAL Priority - Competitive Parity Required

These features are **table stakes** for credibility in the enterprise land intelligence market. Without them, we risk losing deals to Acres.com.

---

#### CG-001: Entity Unmasking & Beneficial Owner Identification
**Learn From:** Acres.com
**Date Identified:** November 2025
**Priority:** 🔴 CRITICAL
**Status:** Not Started
**Effort:** XL (6-9 months)
**Target Release:** Q2 2026

**Description:**
AI-powered system to reveal beneficial owners behind shell entities (LLCs, trusts, corporations) that control land parcels. 40% of US land is held through opaque ownership structures.

**Why Critical:**
**Acres.com has this; we don't.** Enterprise customers need to understand who really owns land to:
- Identify land banking patterns (e.g., Amazon buying through shell LLCs)
- Connect multiple parcels to same ultimate owner
- Understand institutional vs. individual ownership
- Track hyperscaler acquisitions 18-36 months before announcements

**Business Impact:**
- **Sales blocking:** "How do I know who really owns this?" is a common objection
- **Competitive disadvantage:** Acres can answer "Who's behind this LLC?"; we can't
- **PNK Group value:** Identify strategic land banking by competitors

**Technical Approach:**
- AI/ML entity resolution algorithms
- Corporate registry data integration (Secretary of State filings)
- Mortgage/deed cross-referencing
- Pattern matching across parcels, transactions, mortgages
- Manual verification for high-confidence connections

**Dependencies:**
- Corporate registry data partnerships (50 states)
- Entity resolution ML models
- Graph database for relationship mapping
- Human verification process (like Acres' manual curation)

**Success Metrics:**
- Successfully unmask 30%+ of shell entities
- Confidence scoring >80% for automated connections
- Coverage of major institutional players (REITs, hyperscalers, pension funds)

**Overlap with Existing Plans:**
Module 5 (Affiliated Owners Analysis) addresses some of this, but needs expansion to match Acres' entity unmasking capability.

---

#### CG-002: Power Grid Infrastructure Data
**Learn From:** Acres.com
**Date Identified:** November 2025
**Priority:** 🔴 CRITICAL (for data center focus)
**Status:** Not Started
**Effort:** M (2-3 months)
**Target Release:** Q1 2026

**Description:**
Comprehensive US power grid data including transmission lines and substations with detailed specifications (voltage, capacity, ownership, status).

**Why Critical:**
**Essential for AI data center site selection.** Gigawatt-scale data centers require:
- Proximity to 230-345 kV transmission lines
- Available substation capacity (100-500 MW minimum)
- Redundant power supply pathways
- Understanding of grid ownership and access

**Business Impact:**
- **PNK Group requirement:** Data centers are primary use case
- **Competitive disadvantage:** Acres has detailed transmission line maps with voltage/capacity
- **Sales blocking:** "Where can I find 500 MW of power?" is Day 1 question

**Technical Approach:**
- Integrate US Energy Information Administration (EIA) data
- HIFLD (Homeland Infrastructure Foundation-Level Data) for transmission lines
- Utility company public filings (FERC Form 715)
- OpenStreetMap power infrastructure (supplementary)
- Map visualization with voltage/capacity overlays

**Data Sources:**
- ✅ EIA-860 (power plant data)
- ✅ EIA-411 (transmission lines)
- ✅ HIFLD Open Data (substations, transmission lines)
- ✅ State public utility commission filings

**Dependencies:**
- Data licensing agreements (if required)
- GIS processing pipeline
- Map visualization integration
- Real-time or quarterly update process

**Success Metrics:**
- Coverage of all 230+ kV transmission lines in target markets
- Substation capacity data for 500+ major substations
- Accuracy >95% for location and voltage data

**Related to:** Module 3 (Land Qualification) - grid capacity is qualification criterion

---

#### CG-003: Curated Transaction Database with Manual Verification
**Learn From:** Acres.com
**Date Identified:** November 2025
**Priority:** 🔴 CRITICAL
**Status:** Not Started
**Effort:** L (4-6 months + ongoing)
**Target Release:** Q2 2026

**Description:**
Weekly hand-verified comparable sales database supplementing automated courthouse sales data, with proprietary transaction prices in non-disclosure states.

**Why Critical:**
**Data quality is competitive advantage.** Acres has:
- Weekly hand-verified comps (vs. just monthly courthouse scrapes)
- Proprietary pricing in 12 non-disclosure states (where sale prices aren't public)
- Human curation catching errors that automated systems miss

**Business Impact:**
- **Valuation accuracy:** Clients need reliable comps for $10M-$100M+ deals
- **Competitive disadvantage:** Acres' curated database is a moat (5-year head start)
- **Non-disclosure states:** Can't provide pricing in key markets (e.g., Texas parts)

**Technical Approach:**
- **Phase 1:** Hire research analyst (1 FTE) for manual verification
- **Phase 2:** Establish relationships with brokers/title companies for NDS pricing
- **Phase 3:** Build curation workflow (flag suspicious transactions, verify outliers)
- **Phase 4:** Weekly update cadence for high-activity markets

**Data Sources:**
- Courthouse sales (baseline, automated)
- Broker market reports
- Title company data partnerships
- Direct relationships with county recorders
- Industry connections for NDS pricing

**Dependencies:**
- Research analyst hire (1-2 FTE)
- County recorder relationships (3,000+ counties - can start with PNW)
- Broker/title company partnerships
- Curation workflow tooling
- QA process for data accuracy

**Success Metrics:**
- Weekly update cadence for target markets (PNW initially)
- 95%+ accuracy for verified transactions
- Coverage of 5+ non-disclosure state markets by end of year
- Catch and correct 10%+ of automated errors

**Related to:** Module 2 (Owner Contact) - accurate comps help validate pricing during outreach

---

#### CG-004: API & Enterprise Workflow Integration
**Learn From:** Acres.com + Dodda.ai
**Date Identified:** November 2025
**Priority:** 🔴 CRITICAL (for enterprise scale)
**Status:** Not Started
**Effort:** M (3-4 months)
**Target Release:** Q1 2026

**Description:**
REST API for enterprise workflow integration, allowing customers to pull Parcel AI data into their CRM, deal management systems, and custom workflows.

**Why Critical:**
**Enterprise customers need integration.** Both Acres and Dodda have APIs. Enterprise requirements:
- Sync parcels to internal CRM (Salesforce, HubSpot, custom)
- Automate data pulls for reporting and analysis
- Embed Parcel AI intelligence in existing workflows
- Build custom dashboards using our data

**Business Impact:**
- **Enterprise adoption blocker:** "Can this integrate with our systems?" is common question
- **Competitive disadvantage:** Both Acres and Dodda are API-first
- **PNK Group scaling:** As PNK scales, they'll need API for internal tools

**Technical Approach:**
- RESTful API with authentication (API keys + OAuth)
- Rate limiting and usage tracking
- Comprehensive API documentation (OpenAPI/Swagger)
- SDKs for Python, JavaScript (Node.js)
- Webhook support for real-time updates
- Sandbox environment for testing

**Endpoints (Priority Order):**
1. Parcel search and filtering
2. Owner contact data retrieval
3. Project management (CRUD for saved parcels)
4. Transaction history and comps
5. Land qualification results (Module 3)
6. Market signals (Module 4)
7. Affiliation data (Module 5)

**Dependencies:**
- API infrastructure and hosting
- Authentication/authorization system
- Rate limiting and monitoring
- Documentation platform
- Customer support for API issues

**Success Metrics:**
- API available for all core data types
- 99.5% uptime SLA
- <500ms p95 response time
- Documentation completeness score >90%
- 3+ enterprise customers using API within 6 months

**Related to:** All modules - API provides programmatic access to entire platform

---

### 🟠 HIGH Priority - Differentiation Features

These features are **not blockers** but provide significant competitive advantage and differentiation opportunities.

---

#### CG-005: Automated Site Investigation Report (SIR) Generation
**Learn From:** Dodda.ai
**Date Identified:** November 2025
**Priority:** 🟠 HIGH
**Status:** Not Started
**Effort:** XL (6-9 months) OR partnership opportunity
**Target Release:** Q3 2026 OR partnership Q1 2026

**Description:**
Comprehensive automated site feasibility reports (zoning, utilities, environmental, regulatory, AHJ contacts) generated in <10 minutes, aggregating 150+ data sources.

**Why Important:**
**Dodda.ai's killer feature.** 20x time savings (100 hours → 10 minutes) for:
- Complete zoning analysis (setbacks, height limits, lot coverage, permitted uses)
- Utilities mapping (electricity rates, providers, telecom coverage)
- Environmental risk assessment (FEMA flood, elevation, soils, disasters)
- Regulatory requirements and AHJ contact information
- Site feasibility Go/NoGo recommendation

**Business Impact:**
- **Nice to have but not blocking:** Complements our acquisition intelligence focus
- **Partnership opportunity:** Could integrate Dodda.ai SIR into Module 2 (Land Qualification)
- **Time savings:** Speeds up initial site screening for PNK Group

**Strategic Options:**
1. **Build in-house:** 150+ source integrations, 6-9 months, XL effort
2. **Partner with Dodda.ai:** Integrate their SIR API, 1-2 months, S effort, ongoing license cost
3. **Hybrid:** Build basic feasibility (power, zoning), partner for comprehensive SIR

**Recommendation:** **Explore Dodda.ai partnership first.** They're early-stage ($12.5K ARR) and likely open to partnerships. Complementary capabilities (they do feasibility; we do acquisition intelligence).

**Dependencies:**
- If build: 150+ source integration partnerships, 6-9 months dev time
- If partner: Dodda.ai partnership agreement, API integration

**Success Metrics:**
- SIR generation time <15 minutes
- Coverage of 100+ data sources minimum
- Accuracy >90% for zoning/utilities data
- PNK Group adoption for initial site screening

**Related to:** Module 3 (Land Qualification) - SIR could be automated qualification input

---

#### CG-006: Predictive Market Indexes (Data Center & Industrial)
**Learn From:** Acres.com
**Date Identified:** November 2025
**Priority:** 🟠 HIGH
**Status:** Not Started (but overlaps with Module 4)
**Effort:** L (4-6 months)
**Target Release:** Q2 2026

**Description:**
Track and predict land acquisition patterns for data centers and industrial developments 18-36 months before public announcements, similar to Acres' Data Center Index and Home Builder Index.

**Why Important:**
**Competitive intelligence for strategic planning.** Identify where competitors are land banking:
- Hyperscaler data center acquisitions (Amazon, Google, Microsoft, Meta)
- Industrial developer patterns (logistics hubs, manufacturing)
- Institutional capital deployment trends (REITs, pension funds)
- Growth corridor predictions before prices spike

**Business Impact:**
- **Differentiation from Acres:** Theirs updates monthly; ours could be real-time
- **Strategic intelligence:** Help PNK Group identify markets before competition heats up
- **Partnership opportunity:** Sell index insights as separate product

**Technical Approach:**
- Leverage entity unmasking (CG-001) to identify hyperscaler shell entities
- Combine with market signals monitoring (Module 4)
- AI pattern recognition for acquisition clusters
- Historical pattern analysis for predictive modeling
- Monthly or weekly index reports

**Data Inputs:**
- Entity-unmasked transactions (CG-001)
- Market signals (Module 4)
- Power grid capacity changes (CG-002)
- Permit and zoning applications
- Utility capacity reservation filings

**Dependencies:**
- Entity unmasking capability (CG-001)
- Market signals monitoring (Module 4)
- Historical transaction database (CG-003)
- AI/ML predictive models

**Success Metrics:**
- Predict 60%+ of major data center announcements 12+ months early
- Identify 10+ land banking clusters per quarter
- Early-warning accuracy >70%

**Related to:** Module 4 (Market Signals) - natural extension of market monitoring

---

#### CG-007: Mobile App with Offline Field Mode
**Learn From:** Acres.com
**Date Identified:** November 2025
**Priority:** 🟡 MEDIUM
**Status:** Not Started
**Effort:** L (5-7 months)
**Target Release:** Q3-Q4 2026

**Description:**
Native iOS/Android mobile app with offline mode for field site visits, including route planning, photo geotagging, waypoints, and offline parcel data.

**Why Important:**
**Field teams need offline access.** Acres has full-featured mobile app:
- Offline parcel data for areas without cell coverage
- Route planning for multi-site visits
- Photo geotagging for site documentation
- Waypoints and notes
- 3D terrain visualization

**Business Impact:**
- **Not blocking initially:** Enterprise customers primarily desktop-based
- **Nice to have for scale:** As field teams grow, mobile becomes important
- **Competitive parity:** Acres has this; we don't (but not urgent)

**Technical Approach:**
- Native iOS (Swift) and Android (Kotlin) apps
- Offline-first architecture with sync
- Map tiles caching for offline access
- SQLite local database for parcel data
- Photo/note upload when back online
- Route optimization algorithms

**Dependencies:**
- Mobile development team (2-3 FTE for 5-7 months)
- Offline map tile storage and licensing
- Mobile backend APIs
- App store deployment and maintenance

**Success Metrics:**
- App store rating >4.5 stars
- Offline mode working in 95%+ of scenarios
- Photo geotagging accuracy <10m
- Adoption by 50%+ of field users within 6 months

**Related to:** All modules - mobile access to full platform

---

#### CG-008: Comprehensive Zoning & Utilities Intelligence
**Learn From:** Dodda.ai
**Date Identified:** November 2025
**Priority:** 🟡 MEDIUM
**Status:** Partial (basic zoning, utilities planned in Module 3)
**Effort:** M (3-4 months if prioritized)
**Target Release:** Q3 2026

**Description:**
Deep zoning intelligence (setbacks, height limits, lot coverage, permitted uses, FAR, AHJ contacts) and utilities data (electricity rates, providers, telecom coverage).

**Why Important:**
**Dodda.ai excels here.** Comprehensive qualification data:
- Complete zoning code analysis
- Regulatory requirement parsing
- Authorities Having Jurisdiction (AHJ) contacts with phone numbers
- Electricity provider rates and coverage maps
- Telecommunications infrastructure

**Business Impact:**
- **Overlap with Module 3:** Already planning some of this
- **Dodda partnership alternative:** Could integrate their data instead of building
- **Time savings:** Faster qualification decisions

**Technical Approach:**
- Integrate municipal zoning databases (city/county GIS)
- Parse zoning ordinances and development codes
- Utility company data partnerships (electricity, gas, telecom)
- AHJ contact database (public records + manual curation)
- Automated rule parsing for setbacks, FAR, etc.

**Strategic Options:**
1. **Build in-house:** Part of Module 3 already
2. **Partner with Dodda.ai:** Leverage their 150+ sources
3. **Hybrid:** Basic zoning + partner for deep analysis

**Dependencies:**
- If build: Municipal data partnerships, ordinance parsing
- If partner: Dodda.ai integration agreement

**Success Metrics:**
- Coverage of 500+ municipalities (prioritize PNW, then expand)
- Zoning data accuracy >95%
- AHJ contact database with 1,000+ contacts
- Utilities coverage for 90%+ of target markets

**Related to:** Module 3 (Land Qualification) - already planned, may need expansion

---

### Feature Request Summary

#### By Priority
| Priority | Count | Description |
|----------|-------|-------------|
| 🔴 CRITICAL | 4 | Competitive parity required for credibility (Entity Unmasking, Power Grid, Curated Data, API) |
| 🟠 HIGH | 3 | Differentiation features (SIR Integration, Predictive Indexes, Market Intelligence) |
| 🟡 MEDIUM | 2 | Nice-to-have competitive parity (Mobile App, Advanced Zoning/Utilities) |

#### By Source
| Source | Count | Type |
|--------|-------|------|
| Acres.com gaps | 5 | Entity unmasking, power grid, curated data, predictive indexes, mobile app |
| Dodda.ai gaps | 2 | SIR automation, zoning/utilities depth |
| Both competitors | 1 | API/integration (both have this) |

#### By Estimated Effort
| Effort | Count | Features |
|--------|-------|----------|
| XL (6-9 months) | 2 | Entity Unmasking, SIR (if build) |
| L (4-7 months) | 4 | Curated Data, Predictive Indexes, Mobile App, Zoning/Utilities |
| M (2-4 months) | 2 | Power Grid, API |

#### Strategic Recommendations

**Q4 2025 - Q1 2026: Competitive Parity Sprint**
Focus on CRITICAL features to remain credible vs. Acres.com:
1. ✅ **Power Grid Data** (M effort, 2-3 months) - Start immediately
2. ✅ **API/Integration** (M effort, 3-4 months) - Start immediately
3. ✅ **Entity Unmasking** (XL effort, 6-9 months) - Start planning now, build in Q1-Q2
4. ✅ **Curated Transaction DB** (L effort, ongoing) - Hire research analyst Q4 2025

**Q2 2026: Differentiation**
Build unique advantages:
1. ✅ **Predictive Market Indexes** (leverage Entity Unmasking + Module 4)
2. ⚠️ **SIR Partnership with Dodda.ai** (explore, may be faster than building)

**Q3-Q4 2026: Scale**
1. Mobile app for field teams
2. Advanced zoning/utilities (if not partnered)

---

## Planned Product Modules

### Module 3: Automatic Land Qualification
**Source:** PNK Group
**Date Requested:** 2024
**Priority:** High
**Status:** Planned - Development Starting Q1 2025

**Description:**
Automate preliminary land parcel assessment using desktop audit from public sources, without requiring physical site visits or lengthy manual audits.

**Business Case:**
Focus resources only on parcels with real development potential, avoiding wasted time and budget on unsuitable options. Enables rapid Go/NoGo decisions for logistics terminals and AI data centers.

**Target Success Metrics:**
- Automatic filtering of 70% of unsuitable parcels
- Preliminary assessment accuracy >70%
- Time and budget savings on each rejected parcel

**Estimated Timeline:** 8 months
**Target Release:** Q3 2025

**Planned Features:**
- AI chat assistant for land qualification questions
- Underground object analysis (mines, tunnels)
- Automatic topography verification
- Automatic geotech parameters evaluation
- Automatic wetlands verification (wetland report)
- Automatic flood zones check
- Automatic environmental risks assessment (environmental report)
- Automatic traffic impact analysis (traffic report)
- Highway access proximity analysis
- Fiber network proximity analysis (for data centers)
- Electrical grid capacity analysis
- Preliminary development cost estimation
- Automatic FAR (Floor Area Ratio) verification
- Go/NoGo scoring for logistics and data center use cases

**Dependencies:**
- Modules 1 & 2 foundation
- Additional data source integrations
- AI/ML infrastructure for scoring

**Value to PNK Group:**
Critical for scaling land acquisition process. Enables team to quickly filter out unsuitable parcels before investing in detailed due diligence.

---

### Module 4: Market Signals Monitoring
**Source:** PNK Group
**Date Requested:** 2024
**Priority:** High
**Status:** Planned - Development Starting Q1 2025

**Description:**
Early detection system for parcels with high arbitrage potential before they appear on the open market. Monitor public records, regulatory filings, and market signals to identify off-market opportunities.

**Business Case:**
Gain 30-90 day competitive advantage by identifying promising parcels before competitors. Purchase land before price increases following permits or zoning changes.

**Target Success Metrics:**
- Discover 25+ off-market opportunities per month
- Lead competitors by 30-60 days
- Identify 10+ parcels with high arbitrage potential per month

**Estimated Timeline:** 6 months
**Target Release:** Q2 2025

**Planned Features:**
- Public hearings monitoring and parsing
- Permit documentation tracking
- Industrial company bankruptcy monitoring
- Pre-development meetings tracking
- Zoning change application monitoring
- LandID integration for encumbrance analysis
- Automated alert system for high-potential parcels
- Market signal scoring and prioritization
- Historical pattern analysis
- Regulatory timeline tracking

**Dependencies:**
- Public records access and parsing infrastructure
- LandID integration
- Alert notification system
- Pattern recognition algorithms

**Value to PNK Group:**
Access to off-market deals is critical for avoiding broker markups and securing optimal parcels before competitors. Directly addresses PNK's challenge of deploying $200M efficiently.

---

### Module 5: Affiliated Owners Analysis
**Source:** PNK Group
**Date Requested:** 2024
**Priority:** High
**Status:** Planned - Development Starting Q1 2025

**Description:**
Identify all parcels owned by affiliated owner groups through corporate relationship and ownership structure analysis. Map hidden connections between owners to discover additional acquisition opportunities.

**Business Case:**
Access parcels "off the market" that aren't officially for sale. Ability to acquire multiple parcels through same owner relationships. Expand deal pipeline through network effects.

**Target Success Metrics:**
- Identify all additional parcels for each verified owner
- Map complete ownership networks
- Increase potential deal pipeline

**Estimated Timeline:** 4 months
**Target Release:** Q2 2025

**Planned Features:**
- KYC/KYB (Know Your Customer/Business) compliance module
- Official company registry data collection
- Corporate registration number tracking
- Key personnel identification
- OSINT tools integration for relationship mapping
- Ultimate Beneficial Owner (UBO) identification
- Cross-company ownership analysis
- Automated search for all parcels owned by related entities
- Ownership network visualization
- Hidden relationship discovery
- Corporate structure diagrams

**Dependencies:**
- Corporate registry data sources
- OSINT tools integration
- Graph database for relationship mapping
- Visualization framework

**Value to PNK Group:**
Multiplies effectiveness of each owner relationship discovered in Module 2. Once a willing seller is identified, quickly find all their related properties for potential bulk acquisitions.

---

## Module Enhancement Requests

### Module 1 Enhancements
**Priority:** Medium
**Status:** Planned for Q1 2025

**Requested Features:**
1. **Fiberlocator Integration**
   - Assess fiber connectivity for data center parcels
   - Map fiber routes and proximity
   - Connectivity quality scoring

2. **US Energy Atlas Integration**
   - Available power capacity analysis
   - Substation proximity mapping
   - Power infrastructure assessment for data centers

**Business Value:** Critical for AI data center site selection

---

### Module 2 Enhancements
**Priority:** Medium
**Status:** Planned for Q2 2025

**Requested Features:**
1. **Communication Tracking**
   - Track owner outreach in-system
   - Record communication history
   - Follow-up reminders
   - Response tracking

**Business Value:** Complete CRM functionality for owner relationships

---

## Feature Request Summary

### By Status
| Status | Count | % of Total |
|--------|-------|-----------|
| Planned (Modules 3-5) | 3 major modules | 60% |
| In Development (Module enhancements) | 2 enhancements | 40% |
| Total Planned Features | 5 initiatives | 100% |

### By Source
| Source | Count | % of Total |
|--------|-------|-----------|
| PNK Group | 5 | 100% |

### By Priority
| Priority | Count |
|----------|-------|
| High | 3 (Modules 3, 4, 5) |
| Medium | 2 (Module enhancements) |

---

## Development Timeline

| Quarter | Initiatives |
|---------|------------|
| Q1 2025 | Module 1 enhancements, Module 3 development start, Module 4 development start, Module 5 development start |
| Q2 2025 | Module 4 launch, Module 5 launch, Module 2 enhancements |
| Q3 2025 | Module 3 launch, refinements based on usage |
| Q4 2025 | Platform optimization, additional features based on feedback |

---

## Most Requested Feature Themes

1. **Automated Land Qualification** - Critical for scaling acquisition process (Module 3)
2. **Off-Market Opportunity Discovery** - Competitive advantage (Module 4)
3. **Ownership Network Analysis** - Deal pipeline expansion (Module 5)

---

## Related Documents

- [Current Features](./current-features.md) - Launched modules 1-2
- [Feature Prioritization](./feature-prioritization.md)
- [Product Roadmap](../05-product-roadmap/roadmap-2025.md)
- [PNK Group Requirements](../02-clients/pnk-group/requirements.md)
- [PNK Group Deliverables](../02-clients/pnk-group/deliverables.md)

---

**Document Owner:** Product Management
**Last Updated:** 2025-01-21
**Review Frequency:** Monthly
**Next Review:** February 2025
