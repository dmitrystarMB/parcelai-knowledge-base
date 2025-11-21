# Current Features - Parcel AI

## Overview

This document catalogs all features currently available in the Parcel AI platform, organized by module and capability area.

**Last Updated:** November 2025
**Product Version:** 1.5.0
**Development Period:** May 2025 - November 2025

---

## 📊 Feature Summary

**Total Features Implemented:** 57+ major features
**Development Timeline:** 7 months (May-Nov 2025)
**Key Impact:** 80% reduction in parcel processing time

---

## Module 1: Map Interface & Visualization

### ✅ Interactive Map (May 2025)
**Status:** Mature
**Launched:** May 2025

**Core Capabilities:**
- Google Maps integration with parcel overlay
- Regrid parcel data visualization
- PNK projects display on map
- Competitor properties layer
- Multi-layer data management

**User Value:** Unified visual platform for all parcel data

---

### ✅ Parcel Boundaries & Selection (June 2025)
**Status:** Mature
**Launched:** June 2025

**Capabilities:**
- Visual parcel boundary display
- Multi-select capability (select multiple parcels simultaneously)
- Two selection modes:
  - Group by parcel number (bulk selection)
  - Individual parcel selection
- Display selected parcels only toggle
- Auto-transparency on zoom
- Clear selection function

**User Value:** Dramatically reduced time for parcel boundary identification

---

### ✅ Satellite Imagery (June 2025)
**Status:** Mature
**Launched:** June 2025
**Integration:** Nearmap

**Capabilities:**
- Current satellite imagery overlay
- Map/Satellite view toggle
- High-resolution imagery for detailed analysis

**User Value:** Visual site assessment without field visits

---

### ✅ Custom Markers & Drawing Tools (Sep-Oct 2025)
**Status:** Available
**Launched:** September 2025

**Capabilities:**
- Create custom markers on map
- Marker type/category classification
- Drag & drop marker repositioning
- Ruler tool with distance measurement
- Customizable colors and units (miles/km)
- Color picker for parcels and projects

**User Value:** Annotate and measure sites for analysis

---

### ✅ Data Layers (Jun-Sep 2025)
**Status:** Growing
**Launched:** June-September 2025

**Available Layers:**
- Wetlands overlay (July 2025)
- Carrier Hotels (September 2025)
- AI Data Centers (September 2025)
- Power grid data sources (identified September 2025)
- PNK projects
- Competitor properties
- Not Classified parcels

**User Value:** Comprehensive site context analysis

---

## Module 2: Search & Filtering

### ✅ Basic Filtering (May 2025)
**Status:** Mature
**Launched:** May 2025

**Core Filters:**
- Parcel size (acres/sq ft)
- Zoning classifications
- Place Types
- County/Region selection

**User Value:** Quick narrowing of parcel universe

---

### ✅ Advanced Filtering (June-Oct 2025)
**Status:** Mature
**Launched:** June 2025, Enhanced October 2025

**Advanced Capabilities:**
- Multi-criteria simultaneous filtering
- Owner-based filtering and export
- Apply button logic (configure all, then apply)
- Regrid Attributes integration
- Parcel Details filtering
- Deal Terms filtering
- Current Needs filtering

**Performance:**
- ~50% faster (August 2025 optimization)
- No reload between filter changes

**User Value:** Precise targeting of opportunity set

---

### ✅ Radius-Based Search (October 2025)
**Status:** Available
**Launched:** October 2025

**Capabilities:**
- Maximum radius filter around specific marker types
- Example: Find parcels within X miles of interstate exits
- Dynamic radius adjustment

**User Value:** Location-based opportunity identification

---

## Module 3: Project Management

### ✅ Project Creation & Management (July 2025)
**Status:** Mature
**Launched:** July 2025

**Capabilities:**
- Create project groups from multiple parcels
- Project descriptions and notes
- Project-level information pages
- Unified project boundary visualization
- Show/hide project boundaries toggle

**User Value:** Organize and track land assemblages

---

### ✅ Project Summary & Analytics (June 2025)
**Status:** Available
**Launched:** June 2025

**Summary Features:**
- Quick stats for selected parcels/projects
- Total acreage aggregation
- Owner summary
- Zoning breakdown

**User Value:** Instant project-level insights

---

## Module 4: Owner Intelligence & Contact Discovery

### ✅ Owner Data from Regrid (May 2025)
**Status:** Mature
**Launched:** May 2025

**Data Points:**
- Owner name (individuals and entities)
- Mailing address
- Ownership type
- Parcel linkage

**User Value:** Foundation for owner outreach

---

### ✅ Individual Owner Auto-Search (July 2025)
**Status:** Available
**Launched:** July 2025

**Data Sources:**
- Apollo
- SmartLead (SL)
- Public records

**Capabilities:**
- Automated contact discovery for natural persons
- Phone numbers
- Email addresses
- Social profiles

**User Value:** Automated individual owner contact discovery

---

### ✅ Corporate Owner Auto-Search (August 2025)
**Status:** Available
**Launched:** August 2025

**Capabilities:**
- Automated corporate entity contact discovery
- Corporate structure data
- Key personnel identification
- Business contact information

**User Value:** Automated corporate owner outreach data

---

### ✅ State Registry Integration (October 2025)
**Status:** Available
**Launched:** October 2025

**Capabilities:**
- Automated search through state business registries
- Affiliated person discovery (corporate structure)
- Pennsylvania state registry (live)
- Additional states in development

**User Value:** Deeper ownership intelligence

---

### ✅ Georgia Business Registry (November 2025)
**Status:** Available
**Launched:** November 2025

**Technical Features:**
- Dedicated service for Georgia state registry
- Proxy server infrastructure
- Cloudflare bypass system
- US-based access routing

**User Value:** Expanded geographic coverage for owner discovery

---

### ✅ Enhanced Contact Sources (November 2025)
**Status:** Available
**Launched:** November 2025

**New Integrations:**
- **ZoomInfo:** Professional verified contact database
- **Spokeo:** Public records and social data search

**User Value:** Significantly increased contact discovery success rate

---

### ✅ Custom Owner Addition (October 2025)
**Status:** Available
**Launched:** October 2025

**Capabilities:**
- Manual owner information input
- Affiliated person tracking
- Custom notes and relationships
- Parcel linkage

**User Value:** Capture proprietary ownership intelligence

---

### ✅ Contact Feedback System (September 2025)
**Status:** Available
**Launched:** September 2025

**Features:**
- Like/Dislike rating for found contacts
- Comment and feedback submission
- Data quality reporting

**User Value:** Continuous contact data quality improvement

---

## Module 5: Data Export & Reporting

### ✅ Excel Export (May 2025)
**Status:** Mature
**Launched:** May 2025

**Basic Export:**
- Parcel data
- Owner information
- Property characteristics
- Custom field selection

---

### ✅ Enhanced Excel Export (October 2025)
**Status:** Mature
**Enhanced:** October 2025

**Additional Data:**
- Found owner contacts included
- Phone numbers and emails
- Contact source tracking
- Custom owner additions

**User Value:** Complete outreach data package

---

### ✅ Excel Funnel Tracker (September 2025)
**Status:** Available
**Launched:** September 2025

**Features:**
- County workflow tracking
- Status management
- Pipeline visualization

**User Value:** Team coordination and progress tracking

---

## Module 6: Analytics & Calculations

### ✅ Net Acreage Calculator (October 2025)
**Status:** Available
**Launched:** October 2025

**Capabilities:**
- Automatic "clean" acreage calculation
- Wetlands exclusion
- Developable land calculation
- Per-parcel and project-level totals

**User Value:** Accurate developable land assessment

---

### ✅ FAR Calculator (October 2025)
**Status:** Available
**Launched:** October 2025

**Calculations:**
- Floor Area Ratio per parcel
- Project-level FAR aggregation
- Total buildable square footage estimates

**User Value:** Development potential quantification

---

### ✅ Net Acreage Performance Optimization (November 2025)
**Status:** Production
**Launched:** November 2025

**Performance:**
- **Before:** 30 minutes for 6,217 parcels
- **After:** 30 minutes for 281,000 parcels
- **Improvement:** 45x faster processing

**Technical Achievement:**
- Memory optimization
- Server stability improvements
- Full dataset scalability

**User Value:** Fast calculations across entire database

---

## Module 7: Data Coverage & Zoning

### ✅ County Expansion Program
**Status:** Ongoing
**Started:** July 2025

**Coverage Added:**

**July 2025:**
- Lackawanna County, PA: 2,590 parcels (5 prospective projects)

**August 2025:**
- Dauphin County, PA: 1,906 parcels (7 land groups, 2,858 acres)
- Cumberland County, PA: 2,121 parcels (9 land groups, 2,186 acres)
- Columbia County, PA: 2,505 parcels
- Lebanon County, PA: 1,385 parcels
- Berks County, PA: 2,331 parcels

**September 2025:**
- Hanover County, VA: 1,538 parcels
- New Kent County, VA: 668 parcels
- Gwinnett County, GA: 138 parcels
- Butts County, GA: 666 parcels

**October 2025:**
- Hillsborough County, FL: 45,402 parcels (initial)
- Cobb County, GA: 134 parcels
- Fulton County, GA: 659 parcels

**November 2025:**
- Hillsborough County, FL: 281,387 parcels (expanded after Planned Development zoning added)

**Total Counties:** 12+ counties
**Total Parcels:** 290,000+ parcels (30+ acres minimum)

**User Value:** Expanding market coverage for land acquisition

---

### ✅ Zoning Enhancement (November 2025)
**Status:** Production
**Launched:** November 2025

**Added Zoning Type:**
- **Planned Development** zoning classification

**Impact:**
- Hillsborough County expanded 6.2x (45,402 → 281,387 parcels)
- Previously inaccessible parcels now available

**User Value:** Massive increase in available inventory

---

## Module 8: Platform Infrastructure

### ✅ Authentication System (November 2025)
**Status:** Production
**Launched:** November 2025

**Features:**
- User login system
- Role-based access control (RBAC)
- User personalization
- Saved searches and preferences
- Activity tracking

**User Value:** Secure, personalized platform access

---

### ✅ Data Dashboard (November 2025)
**Status:** Production
**Launched:** November 2025
**URL:** dashboard.getparcel.ai

**Visualizations:**
1. **Regrid Source Data** - Full parcel dataset statistics
2. **Whitelist Filtered Data** - Post-filter parcel counts
3. **County Distribution** - Coverage by county
4. **Zoning Statistics** - Parcel breakdown by zoning type

**User Value:** Real-time data transparency and self-service analytics

---

## Module 9: Future & Experimental Features

### 🚧 AI Copilot (Hypothesis/Development)
**Status:** Hypothesis/Prototype
**Announced:** November 2025

**Concept:**
- Natural language query interface
- Multi-agent system architecture
- Automated data enrichment (wetlands, fiber, logistics, comparables)
- Structured report generation
- Map-based result visualization

**Example Query:**
> "Find industrial parcels between 20 and 50 acres in Dauphin County, PA, with net acreage > 90% of gross"

**Expected Workflow:**
1. User submits natural language query
2. AI agents process query across databases
3. Apply filters and enrich data automatically
4. Generate report with parcels, contacts, attributes, infrastructure
5. Display results on map with summary

**Strategic Value:** Transform text query into complete, enriched parcel analysis in minutes

---

## 🔍 Research & Analysis Completed

### ✅ CoStar Data Source Analysis (November 2025)
**Status:** Completed
**Date:** November 2025

**Findings:**
- **Strength:** Leader in commercial building data
- **Weakness:** Minimal raw land coverage
- **Average Exposure:** ~900 days (25-2,500 day range)
- **API Access:** No open API; manual export only; automation very complex
- **Conclusion:** Suitable as supplementary validator, not primary source

**Recommendation:** Use for targeted validation, not automated search

---

## Feature Maturity Matrix

| Feature Category | Maturity | Adoption | Satisfaction | Priority |
|-----------------|----------|----------|------------|----------|
| **Map & Visualization** | Mature | High | High | Maintain |
| **Search & Filtering** | Mature | High | High | Maintain |
| **Project Management** | Growing | High | High | Enhance |
| **Owner Intelligence** | Mature | High | High | Enhance |
| **Contact Discovery** | Growing | Medium | High | Enhance |
| **Export & Reporting** | Mature | High | Medium | Maintain |
| **Analytics & Calculations** | Growing | Medium | High | Develop |
| **Data Coverage** | Growing | High | High | Expand |
| **Authentication & Security** | Early | Medium | N/A | Develop |
| **AI Copilot** | Concept | N/A | N/A | Research |

---

## Performance Metrics

### Speed & Efficiency
- **Parcel Processing:** 80% time reduction (July 2025)
- **Calculation Speed:** 45x improvement (November 2025)
- **Product Performance:** 50% faster (August 2025)

### Data Coverage
- **Counties:** 12+ counties
- **Parcels:** 290,000+ parcels (30+ acres)
- **States:** Pennsylvania, Virginia, Georgia, Florida

### Contact Discovery
- **Sources:** 6 integrated (Apollo, SmartLead, State Registries, ZoomInfo, Spokeo, custom additions)
- **Success Rate:** Significantly improved with November 2025 additions

---

## Features by User Persona

### For Acquisition Managers (Land Acquisition Teams)
- Parcel search and filtering
- Project management
- Owner intelligence and contact discovery
- Excel exports with contacts
- County coverage expansion
- Net acreage and FAR calculations

### For Analysts (Due Diligence & Research)
- Advanced filtering
- Data layers (wetlands, infrastructure)
- Analytics and calculations
- Data dashboard
- Zoning analysis
- Comparable identification

### For Executives (Portfolio Management)
- Project summaries
- High-level dashboards
- Performance metrics
- Market coverage reports

---

## Platform Capabilities

### Performance
- Sub-second search results
- 45x faster calculation processing
- 50% overall performance improvement
- Concurrent multi-user support
- Scalable to 280K+ parcels

### Security & Access
- User authentication
- Role-based access control
- Audit logging
- Personalized workspaces

### Integrations
- Regrid (parcel data)
- Nearmap (satellite imagery)
- Google Maps (base mapping)
- Apollo (contacts)
- SmartLead (contacts)
- ZoomInfo (professional contacts)
- Spokeo (public records)
- State business registries (PA, GA)

### Data Quality
- Contact feedback system
- User reporting mechanisms
- Continuous improvement pipeline

---

## Development Velocity

**May 2025:** Prototype launch (3 features)
**June 2025:** UI overhaul (10 features)
**July 2025:** Project management (6 features)
**August 2025:** Performance & scale (2 major features + 5 counties)
**September 2025:** Custom markers & data (7 features + 4 counties)
**October 2025:** Automation tools (8 features + 3 counties)
**November 2025:** Infrastructure & integrations (6 major features)

**Total:** 48+ major features in 7 months (average 6-7 features/month)

---

## Related Documents

- [Feature Requests](./feature-requests.md)
- [Feature Prioritization](./feature-prioritization.md)
- [Product Roadmap 2025](../05-product-roadmap/roadmap-2025.md)
- [Product Changelog](../10-changelog/product-changelog.md)
- [MVP Status](../05-product-roadmap/mvp-status.md)

---

**Document Owner:** Product Management
**Last Updated:** November 2025
**Next Review:** December 2025
