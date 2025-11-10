# 990 EPC Development Plan

## Technology Stack (Beginner-Friendly + Best Practices)

### Core Technologies
- **HTML/CSS/JavaScript** (vanilla) - Start simple, no framework complexity initially
- **Drawflow** - Visual flowchart library (MIT license, well-documented)
- **SheetJS (xlsx)** - Excel export functionality
- **Bootstrap** or **Tailwind CSS** - Professional UI without CSS expertise required

### Development Tools
- **VS Code** - Code editor with extensions:
  - Live Server (for local development)
  - Prettier (code formatting)
  - ESLint (code quality)
- **Git** - Version control from day 1
- **Node.js + npm** - Package management only (no backend server needed)

---

## Project Architecture (Modular & Extensible)

```
/spudnik-epc/
  /docs/                          # Documentation and requirements
    990 EPC Proof Of Concept.md   # Original scope of work
    DEVELOPMENT_PLAN.md           # This file
    PROJECT_VISION.md             # Requirements and flow understanding
  /src/
    /js/
      /core/                      # Main application controller
        app.js                    # Application initialization
        flowchartManager.js       # Flowchart state management
      /models/                    # Data structures
        PowerUnit.js              # Power unit model
        Pump.js                   # Pump model
        Valve.js                  # Valve model
        Cylinder.js               # Cylinder model
        FlowDivider.js            # Flow divider model
        Assembly.js               # Assembly model
      /rules/                     # Rules engine for assembly recommendations
        rulesEngine.js            # Core rules evaluation
        hydraulicRules.js         # Hydraulic-specific rules
      /components/                # UI components
        sidebar.js                # Component selection sidebar
        propertiesPanel.js        # Node properties editor
        bomPreview.js             # BOM preview table
      /utils/                     # Helpers
        validation.js             # Flow/pressure validation
        calculations.js           # Hydraulic calculations
        logger.js                 # Logging "reason for inclusion"
      /export/                    # BOM generation and export
        bomGenerator.js           # Generate BOM from flowchart
        excelExport.js            # Excel export using SheetJS
        jsonExport.js             # JSON import/export for configs
    /css/
      styles.css                  # Main stylesheet
      flowchart.css               # Flowchart-specific styles
    /data/                        # JSON configuration files
      parts-catalog.json          # Standard parts library with specs
      rules-config.json           # Configuration for rules engine
      pump-specs.json             # Pump specifications and capacities
  /assets/                        # Images, icons, logos
    /icons/                       # Component icons
  /config/                        # Application configuration
    app-config.json               # App settings
  /tests/                         # Test files (add as project matures)
  index.html                      # Main application page
  package.json                    # npm dependencies
  .gitignore                      # Git ignore file
  README.md                       # Project README
  CLAUDE.md                       # Claude Code guidance (already exists)
```

---

## Development Phases (Iterative/Compounding Approach)

### Phase 1: Foundation (Week 1-2)
**Goal:** Get basic flowchart working with simple components

**Tasks:**
- Set up project structure ✓
- Initialize npm and install dependencies
- Implement basic HTML structure and layout
- Integrate Drawflow library
- Create simple node types (PowerUnit, Pump)
- Basic drag-and-drop functionality
- Simple styling with Bootstrap/Tailwind

**Deliverable:** Can create and connect power unit and pump nodes

---

### Phase 2: Component Library (Week 2-3)
**Goal:** Complete hydraulic component models and catalog

**Tasks:**
- Define JavaScript classes for all component types:
  - PowerUnit, Pump, Valve, Cylinder, FlowDivider, LoadHolding
- Create comprehensive parts-catalog.json with real Spudnik parts
- Implement component selection sidebar
- Add properties panel for editing node parameters
- Create component icons/visual representation

**Deliverable:** Can add all hydraulic component types with properties

---

### Phase 3: Rules Engine (Week 3-4)
**Goal:** Intelligent assembly recommendations

**Tasks:**
- Build core rules engine architecture
- Define rules in rules-config.json (configuration-driven)
- Implement hydraulic logic:
  - Flow divider recommendations
  - PO check requirements
  - Load holding recommendations
  - Valve configuration logic
- Add "reason for inclusion" logging system
- Create rules debugging/visualization

**Deliverable:** System automatically recommends assemblies with explanations

---

### Phase 4: Validation (Week 4-5)
**Goal:** Ensure configurations are hydraulically valid

**Tasks:**
- Implement pump capacity tracking per branch
- Build flow demand calculations
- Add pressure rating validation
- Create visual feedback system (warnings/errors)
- Implement branch-level validation
- Add validation summary panel

**Deliverable:** System flags invalid configurations and guides corrections

---

### Phase 5: BOM & Export (Week 5-6)
**Goal:** Generate usable output for downstream processes

**Tasks:**
- Build BOM generation logic from flowchart state
- Create in-browser BOM preview table
- Implement Excel export with proper formatting
- Add JSON export for saving configurations
- Implement JSON import for loading saved configs
- Add export configuration options

**Deliverable:** Export Excel BOM and save/load configurations

---

### Phase 6: Polish & Prepare for Production (Week 6+)
**Goal:** Production-ready proof of concept

**Tasks:**
- UI/UX refinement based on user testing
- Performance optimization
- Error handling and user guidance
- Documentation (user guide, technical docs)
- Prepare deployment package
- Create installation/setup guide

**Deliverable:** Ready for Daniel Cornia review and team testing

---

## Recommended Libraries & Plugins

### Essential (Install Immediately)
1. **Drawflow** (v0.0.59+)
   - Visual node-based editor
   - Drag-drop, connections, events
   - `npm install drawflow`

2. **SheetJS / xlsx** (v0.18+)
   - Excel file generation
   - `npm install xlsx`

3. **Bootstrap 5** OR **Tailwind CSS**
   - Recommendation: Bootstrap (easier for beginners)
   - Professional UI components out of the box
   - `npm install bootstrap`

### Helpful (Add as Needed)
4. **Font Awesome** (v6+)
   - Icons for hydraulic components
   - `npm install @fortawesome/fontawesome-free`

5. **FileSaver.js**
   - Simplified file downloads
   - `npm install file-saver`

6. **Lodash**
   - Utility functions for data manipulation
   - `npm install lodash`

### Development Tools
7. **Vite** (Optional, for later)
   - Fast development server with hot reload
   - Better than Live Server for larger projects
   - `npm install -D vite`

---

## Key Architectural Decisions

### 1. Configuration-Driven Design
- **Parts catalog in JSON**: Easy to update parts without code changes
- **Rules in JSON**: Non-programmers can modify logic
- **Benefits**: Maintainability, flexibility, domain expert input

### 2. Event-Driven Architecture
- Components communicate via events, not direct calls
- Loose coupling = easier to modify and extend
- Example: Node added → Rules engine evaluates → BOM updates

### 3. Simple State Management
- Centralized state object manages application state
- Clear data flow: State → UI rendering
- Can upgrade to Redux/Vuex later if complexity grows

### 4. No Backend Required (Initially)
- Pure frontend application
- All data in JSON files loaded at runtime
- Benefits:
  - Deploy anywhere (local file, network share, web server)
  - No server maintenance
  - Easy proof of concept

### 5. Progressive Enhancement
- Start with minimum viable product
- Add features incrementally based on testing
- Each phase builds on previous work
- Fail fast, learn quickly

### 6. Modular Code Organization
- Each component/feature in separate file
- Clear separation of concerns:
  - Models (data structures)
  - Rules (business logic)
  - Components (UI)
  - Utils (helpers)
- Easy to test individual pieces

---

## Deployment Strategy

### Phase 1: Local Development (Now)
- Open `index.html` directly in browser, OR
- Use VS Code Live Server extension
- No installation needed for users

### Phase 2: Internal Network (Future - if POC successful)
**Option A: Shared Network Drive**
- Copy entire project folder to shared location
- Users open `index.html` from network drive
- Pros: Zero setup, works immediately
- Cons: Performance depends on network

**Option B: Internal Web Server**
- Host on company intranet (IIS, Apache, nginx)
- Access via URL (e.g., http://internal-tools/epc)
- Pros: Better performance, professional feel
- Cons: Requires IT support

**Option C: Electron App** (Optional)
- Package as desktop application
- Distribute via network installer
- Pros: Feels like native app, offline capable
- Cons: Additional development effort

### Architecture Supports All Options
- No database = no migration headaches
- Self-contained = easy to move
- Client-side only = flexible deployment

---

## Data Storage Approach

### Phase 1: File-Based (Simple Start)
- Save/Load via JSON export
- Users manage their own files
- No server or database needed

### Future Option: Database Integration
If project scales up, easy to add:
- Backend API (Node.js/Express or Python/Flask)
- Database (PostgreSQL, MongoDB)
- Centralized configuration storage
- Version history, collaboration features

**Architecture supports this evolution** - data models already structured for database migration

---

## Testing Strategy

### Phase 1-3: Manual Testing
- Developer testing during build
- User testing with Daniel Cornia's team

### Phase 4+: Automated Testing (Optional)
- Unit tests for rules engine
- Integration tests for BOM generation
- Tools: Jest, Mocha, or Vitest

---

## Success Metrics (from Scope of Work)

Version 1 considered successful when:
1. ✓ Engineers can fully build standard 990 hydraulic configuration
2. ✓ No need to reference paper schematics
3. ✓ System consistently recommends accurate assemblies
4. ✓ Exported Excel BOM provides reliable foundation for design review

---

## Risk Mitigation

### Risk: Complexity overwhelms beginner
**Mitigation:**
- Incremental development phases
- Focus on learning one concept at a time
- Extensive documentation and comments
- Claude Code assistance throughout

### Risk: Drawflow limitations
**Mitigation:**
- Evaluate Drawflow in Phase 1
- Have alternative libraries ready (GoJS, joint.js)
- Custom solution possible if needed

### Risk: Rules engine too complex
**Mitigation:**
- Start with simple if/then rules
- Add complexity gradually
- JSON configuration keeps logic visible

### Risk: Scope creep
**Mitigation:**
- Stick to Phase 1 scope first
- Prove concept before adding features
- Regular check-ins with stakeholders

---

## Next Immediate Steps

1. ✓ Create folder structure
2. Initialize npm (`npm init`)
3. Install core dependencies
4. Create basic `index.html` scaffold
5. Integrate Drawflow library
6. Create first power unit node
7. Test basic flowchart functionality

---

## Notes for Future Claude Code Sessions

- This is a **learning project** - prioritize clarity over clever code
- **Comment extensively** - explain why, not just what
- **Incremental commits** - small, focused changes
- **Test frequently** - don't build too much before testing
- **User feedback loop** - validate with Daniel Cornia's team early and often

---

*Last Updated: 2025-11-09*
*Project Lead: Cadence Haskins*
*Stakeholder: Daniel Cornia (Hydraulic Engineering Lead)*
