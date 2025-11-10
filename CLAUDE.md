# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## CRITICAL: Session Recovery

**If recovering from a crashed session or starting a new session:**

1. **Check the latest session document:**
   - Location: `/docs/sessions/`
   - Find the most recent `SESSION_YYYY-MM-DD_HH-MM-SS.md` file
   - Read it completely to understand current project state, decisions made, and next steps

2. **Check git status:**
   - Run `git status` to see any uncommitted work
   - Review latest commit: `git log --oneline -5`

3. **Review key planning documents:**
   - `/docs/DEVELOPMENT_PLAN.md` - Technical roadmap and architecture
   - `/docs/reference/README.md` - Company and product context
   - `/DOCS/990 EPC Proof Of Concept, Cadence Haskins .docx.md` - Original scope

---

## Project: 990 Eliminator Engineering Preview Configurator (EPC)

**Purpose:** Browser-based hydraulic system design tool for Spudnik's 990 Eliminator line
**User:** Fluid Power Engineering Team (internal, led by Daniel Cornia)
**Project Lead:** Cadence Haskins (complete beginner - first coding project)
**Status:** Planning and research phase - no code written yet

### Quick Context
- **Company:** Spudnik Equipment Co. LLC (potato harvesting equipment manufacturer, Blackfoot, Idaho)
- **Product:** 990 Custom Eliminator (5 widths: 48"-96", chain or belt, highly customizable)
- **Problem:** Manual hydraulic design is time-consuming, error-prone, hard to standardize
- **Solution:** Visual flowchart builder with rule-based validation and BOM generation

---

## Technology Stack

**Current (Planned):**
- HTML/CSS/JavaScript (vanilla - beginner-friendly)
- Drawflow (flowchart library) - NOT YET INSTALLED
- SheetJS (Excel export) - NOT YET INSTALLED
- Bootstrap (UI framework) - NOT YET INSTALLED
- No backend (pure frontend, file-based storage initially)

**Development Tools:**
- VS Code
- Node.js + npm (for packages only)
- Git (configured, connected to https://github.com/cadencehaskins/SPUDNIK_DEV)

---

## Project Architecture

```
/src/
  /js/
    /core/         # App controller, flowchart state manager
    /models/       # PowerUnit, Pump, Valve, Cylinder, FlowDivider, Assembly
    /rules/        # Rules engine for assembly recommendations
    /components/   # UI components (sidebar, properties panel, BOM preview)
    /utils/        # Validation, calculations, logging
    /export/       # BOM generation, Excel/JSON export
  /css/           # Stylesheets
  /data/          # JSON config files (parts catalog, rules)
```

**Key Principles:**
- Configuration-driven (parts and rules in JSON)
- Event-driven architecture (loose coupling)
- Modular code organization
- Progressive enhancement (start simple, add features incrementally)

---

## Development Commands

**Not yet set up - npm not initialized**

When initialized, commands will be:
```bash
npm install          # Install dependencies
npm run dev          # Start development server
npm run build        # Build for production (if using Vite)
```

For now, use VS Code Live Server extension for local development.

---

## Important Technical Context

### Hydraulic System Standards (from Spudnik research)
- **Standard Pressure:** 2800 PSI
- **Flow Range:** 40-80 GPM (varies by equipment size)
- **Remote Valves:** 3-6 typical (4-6 for eliminators)
- **Validation Required:** Flow capacity, pressure ratings, remote valve counts

### 990 Eliminator Configurations
- **5 widths:** 48", 60", 72", 84", 96"
- **2 types:** Chain or Belt
- **Optional features:** Spreader roller, catwalk
- **Result:** Many possible configurations requiring custom hydraulic design

---

## User Communication Guidelines

**IMPORTANT:** Cadence is a complete beginner. When working with them:
- ❌ No walls of text - keep responses concise and focused
- ✅ One question at a time during interviews/discussions
- ✅ Explain concepts clearly with examples
- ✅ Comment code extensively (explain why, not just what)
- ✅ Use bite-sized, digestible information
- ✅ Iterative approach (test frequently, add gradually)

---

## Key Reference Documents

### Planning & Architecture
- `/docs/DEVELOPMENT_PLAN.md` - Comprehensive technical plan with 6 development phases
- `/docs/GIT_BASICS.md` - Git quick reference for user
- `/docs/sessions/` - Session recovery documents (check most recent)

### Company & Product Context
- `/docs/reference/company/SPUDNIK_COMPANY_OVERVIEW.md` - Company background
- `/docs/reference/products/990_ELIMINATOR_PRODUCT_LINE.md` - Product details
- `/docs/reference/technical/HYDRAULIC_SYSTEMS_OVERVIEW.md` - Hydraulic specs

### Original Requirements
- `/DOCS/990 EPC Proof Of Concept, Cadence Haskins .docx.md` - Original scope of work

---

## Development Phases (Not Started)

### Phase 1: Foundation (Current - Not Started)
- Initialize npm and install dependencies
- Create basic HTML structure
- Integrate Drawflow library
- Create simple node types (PowerUnit, Pump)
- Basic styling with Bootstrap

### Phase 2-6: See DEVELOPMENT_PLAN.md

---

## Git Workflow

**Repository:** https://github.com/cadencehaskins/SPUDNIK_DEV
**Branch:** main
**User Config:** Cadence Haskins <cadence.haskins@spudnik.com>

**Standard workflow:**
```bash
git status                           # Check what changed
git add .                           # Stage all changes
git commit -m "Descriptive message" # Commit with message
git push                            # Push to GitHub
```

**Commit frequently** - small, focused commits are better than large ones.

---

## Next Steps (As of Last Session)

1. **Resume user interview** - Gather detailed hydraulic system requirements
2. **Create PROJECT_VISION.md** - Document interview findings
3. **Initialize npm** - Set up package.json
4. **Install dependencies** - Drawflow, xlsx, Bootstrap
5. **Begin Phase 1 development** - Basic HTML and Drawflow integration

---

## Success Criteria (from Scope of Work)

Version 1 considered successful when:
- Engineers can fully build standard 990 hydraulic configuration without paper schematics
- System consistently recommends accurate assemblies from parts library
- Exported Excel BOM provides reliable foundation for design review

---

*Always check `/docs/sessions/` for the latest context before starting work*
*This is a learning project - prioritize clarity and best practices*
