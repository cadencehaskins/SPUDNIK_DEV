# Spudnik Reference Documentation

This folder contains comprehensive reference materials about Spudnik Equipment Company, gathered to provide context for the 990 EPC (Engineering Preview Configurator) project.

## Purpose

These documents help Claude Code (and future developers) understand:
- The business context of Spudnik
- The 990 Eliminator product line
- Hydraulic system requirements and standards
- How this configurator fits into Spudnik's operations

## Document Structure

### Company Information
📁 **`/company/`**
- `SPUDNIK_COMPANY_OVERVIEW.md` - Company history, mission, values, locations, and markets

### Product Information
📁 **`/products/`**
- `990_ELIMINATOR_PRODUCT_LINE.md` - Detailed info on 990 Custom, 994 AirSep, and 991 AirSep Eliminators

### Technical Information
📁 **`/technical/`**
- `HYDRAULIC_SYSTEMS_OVERVIEW.md` - Hydraulic specifications, standards, components, and validation requirements

## Quick Reference

### Key Facts About Spudnik
- **Founded:** 1958 by Carl and Leo Hobbs
- **Employees:** 500+
- **Location:** Blackfoot, Idaho (all manufacturing)
- **Parent Company:** Grimme Group (since 2003)
- **Focus:** Potato equipment (planting → harvesting → storage)

### Key Facts About 990 Eliminator
- **Purpose:** Sorts and cleans harvested potatoes
- **Customization:** 5 widths (48", 60", 72", 84", 96")
- **Types:** Chain or Belt
- **Options:** Spreader roller, catwalk
- **Why EPC Exists:** High customization + complex hydraulics = need for configurator tool

### Hydraulic System Standards
- **Pressure:** 2800 PSI (standard across Spudnik line)
- **Flow:** 40-80 GPM (varies by equipment size)
- **Remotes:** 3-6 (typically 4-6 for eliminators)

## How to Use These Documents

**For Claude Code:**
- Reference these docs when making design decisions
- Use hydraulic specs for validation logic
- Understand customization options when building UI
- Learn terminology for better communication

**For Developers:**
- Get business context before coding
- Understand why features are needed
- Learn domain-specific terminology
- Reference hydraulic requirements for rules engine

**For Stakeholders:**
- See what information was gathered
- Verify accuracy of technical details
- Suggest additions or corrections

## Research Source

All information gathered from:
- Primary: https://www.spudnik.com/ (official website)
- Research Date: 2025-11-09
- Research Method: Comprehensive web research by AI agent

## Maintenance

These documents should be updated when:
- New product information becomes available
- Hydraulic specifications are refined through team interviews
- Additional technical details are discovered
- Spudnik releases new equipment or updates

## Next Steps

After these reference docs, we'll conduct interviews with Cadence Haskins (project lead) to:
- Understand specific 990 Eliminator hydraulic requirements
- Learn the rules for assembly recommendations
- Define validation requirements
- Clarify BOM output format
- Document workflow and user interface needs

---

*Research completed: 2025-11-09*
*Documents created for 990 EPC Project Context*
