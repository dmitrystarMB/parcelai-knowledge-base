# Product Changelog

## Overview

Chronological log of all product updates, releases, and changes to the Parcel AI platform.

**Format:** Keep newest entries at the top
**Period Covered:** May 2025 - November 2025

---

## November 2025 - Major Performance & Integration Updates

### Added
- 🚀 **Georgia Business Registry Integration** - Automated owner search through official Georgia state business registry with proxy servers and Cloudflare bypass systems
- 📊 **Data Dashboard** (dashboard.getparcel.ai) - Real-time visualization of Regrid data, whitelist filtering, county distribution, zoning statistics
- 🔐 **User Authentication System** - Login system with role-based access control and user personalization
- 📇 **New Contact Sources** - Integrated ZoomInfo (professional verified contacts) and Spokeo (expanded public records search)
- 🏗️ **Planned Development Zoning** - New zoning type added (Hillsborough County expanded from 45,402 to 281,387 parcels)
- 🤖 **AI Copilot Prototype** (Hypothesis) - Multi-agent system for natural language parcel search queries

### Changed
- ⚡ **Net Acreage Calculation Optimization** - 45x performance improvement (30 min for 6,217 parcels → 30 min for 281,000 parcels)
- 🔍 **CoStar Research Completed** - Identified as supplementary data source, not primary (avg exposure ~900 days, limited raw land coverage)

### Performance Metrics
- Processing speed: **45x faster**
- Hillsborough County parcels: **45,402 → 281,387** (6.2x increase)

---

## October 2025 - Automation & Advanced Tools

### Added
- 📏 **Ruler Tool** - Distance measurement tool with customizable color and unit selection (miles/km)
- 🏢 **Custom Owner Addition** - Manual input for newly discovered or affiliated individuals linked to parcels
- 🌿 **Net Acreage Calculation** - Automatic "clean" parcel area calculation excluding wetlands
- 💰 **FAR Calculator** - Automatic FAR calculation per parcel and total project FAR/sum
- 🔗 **State Registry Automation** - Automated search for affiliated individuals through state government registries
- 🗺️ **New Counties** - Hillsborough County, Cobb County (134 parcels), Fulton County (659 parcels)

### Changed
- ✨ **Enhanced Marker System** - Drag & drop functionality for map markers
- 🎨 **UX/UI Refinements** - Renamed filter blocks and data types, updated menu labels
- 📧 **Excel Export Enhancement** - Owner contact information now included in exports

---

## September 2025 - Custom Markers & Data Layers

### Added
- 🎯 **Custom Map Markers** - User-created markers with custom types/categories (similar to Nearmap)
- 📡 **Carrier Hotels & AI Data Centers** - New data layer showing telecommunications infrastructure
- 💬 **Owner Contact Feedback Form** - System for reporting contact data quality issues
- 📄 **Project Information Pages** - Dedicated detailed pages for each project
- 📊 **Excel Funnel Tracker** - County workflow tracking spreadsheet
- ⚡ **Power Grid Data Sources** - Identified and documented US electrical grid data sources
- 🗺️ **New Counties** - Hanover (1,538 parcels), New Kent (668 parcels), Gwinnett (138 parcels), Butts (666 parcels)

### Performance
- All counties filtered with 30+ acres minimum parcel size

---

## August 2025 - Performance & Scalability

### Added
- 🗺️ **5 New Counties** - Dauphin (1,906 parcels), Cumberland (2,121 parcels), Columbia (2,505 parcels), Lebanon (1,385 parcels), Berks (2,331 parcels)
- 🏢 **Corporate Owner Auto-Search** - Automated contact discovery for corporate landowners (legal entities)

### Changed
- ⚡ **Performance Optimization** - ~50% faster product performance
- 🎛️ **Filter Logic Update** - Configure all parameters first, then click "Apply" - eliminates constant data reloading

### Success Stories
- **Dauphin County**: 7 land groups (22 parcels, 2,858 acres) - all 7 in active work
- **Cumberland County**: 9 land groups (43 parcels, 2,186 acres) - approval stage

---

## July 2025 - Project Management & Lackawanna

### Added
- 📁 **Project Management** - Create and manage project groups with descriptions and notes
- 🔍 **Dual Parcel Selection** - Select by common parcel number (group) or individual parcels
- 👤 **Individual Owner Auto-Search** - Automated contact discovery for individual landowners (natural persons)
- 🌊 **Wetlands Layer** - Wetlands overlay on map
- 🎯 **Project Boundary Display** - Unified boundary visualization for entire projects
- 🎨 **Color Picker Tool** - Custom color selection for parcels and projects

### Data Coverage
- **Lackawanna County**: 2,590 lots processed, 5 prospective projects identified
  - 4 projects in Valley View districts (11, 19, 30)
  - DeNaples PA: ~1,000 acres, $20 FAR asking price

### Impact
- **80% reduction** in initial parcel processing time thanks to new tools (parcel selection, project grouping, owner data export)

---

## June 2025 - UI Overhaul & Satellite Integration

### Added
- 🗺️ **Parcel Boundary Display** - Visual parcel boundaries with multi-select capability
- 🛰️ **Nearmap Integration** - Current satellite imagery integration
- 📊 **Summary Menu** - Quick summary information for selected parcels
- 🏷️ **Place Types Filter** - Additional filtering dimension
- 🗑️ **Clear Selection Function** - One-click deselection of all objects
- 👥 **Owner Filter & Export** - Filter and export parcels by owner
- 📌 **Display Selected Only** - Show only selected parcels on map

### Changed
- 🎨 **Regrid-Style UI** - Complete interface redesign based on Regrid reference
- 🔧 **Enhanced Filter System** - Improved data layers (Regrid, PNK projects, competitor properties)
- ✅ **Display Issue Fixed** - Resolved problem with certain lot categories not displaying
- ➕ **Not Classified Parcels** - Added previously missing parcel category

---

## May 2025 - Initial Prototype Launch

### Added
- 🎉 **First Prototype** - Built on Regrid parcel data + PNK projects on Google Maps
- 🔍 **Core Filter Types** - Area and zoning-based filtering
- 📍 **Delaware Test Region** - Tested with 102 parcels, identified 2 off-market prospects

### Foundation
- Base platform architecture established
- Initial data integration with Regrid
- First successful off-market parcel identification

---

## Version History

| Version | Date | Type | Summary | Features Added |
|---------|------|------|---------|----------------|
| 1.5.0 | Nov 2025 | Major | Performance & Auth | 45x speed boost, user auth, GA registry, dashboard |
| 1.4.0 | Oct 2025 | Minor | Automation Tools | FAR calc, net acreage, state registry auto-search |
| 1.3.0 | Sep 2025 | Minor | Custom Markers | User markers, carrier hotels, data centers layer |
| 1.2.0 | Aug 2025 | Minor | Performance & Scale | 50% faster, 5 new counties, corporate owner search |
| 1.1.0 | Jul 2025 | Minor | Projects & Lackawanna | Project management, dual selection, 80% time savings |
| 1.0.0 | Jun 2025 | Major | UI Overhaul | Regrid-style UI, Nearmap, boundaries, owner filters |
| 0.9.0 | May 2025 | Beta | First Prototype | Core filters, Delaware test, Regrid integration |

---

## Changelog Guidelines

### Version Numbering
- **Major (X.0.0):** Significant new capabilities, breaking changes
- **Minor (1.X.0):** New features, enhancements
- **Patch (1.0.X):** Bug fixes, small improvements

### Categories
- **Added:** New features
- **Changed:** Modifications to existing features
- **Deprecated:** Features planned for removal
- **Removed:** Features removed
- **Fixed:** Bug fixes
- **Security:** Security updates

### Entry Format
```markdown
## [Version] - [Release Name] - [Date]

### Added
- [Feature description] ([Issue #])

### Changed
- [Change description] ([Issue #])

### Fixed
- [Bug fix description] ([Issue #])
```

---

## Release Notes Archive

Detailed release notes for each version are available in individual files:
- [Version 1.0.0 Release Notes](./releases/v1.0.0.md)

---

**Document Owner:** Product Management  
**Update Frequency:** With each release  
**Audience:** Internal team, customers
