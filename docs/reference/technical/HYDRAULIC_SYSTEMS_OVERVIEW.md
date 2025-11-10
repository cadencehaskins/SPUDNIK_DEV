# Spudnik Hydraulic Systems - Technical Overview

## Standard Hydraulic Specifications Across Product Line

### Industry Standards at Spudnik

**Standard Operating Pressure:** **2800 PSI**
- Used across most Spudnik equipment
- Industry standard for agricultural hydraulics
- Provides consistent design baseline

**Hydraulic Flow Requirements:** **40-80 GPM** (varies by equipment)
- Smaller equipment: 40-50 GPM
- Medium equipment: 50-60 GPM
- Large/multi-function: 60-80 GPM

**Remote Valve Configurations:** **3-6 remotes typical**
- Simple equipment: 3 remotes
- Complex equipment: 4-6 remotes
- Various types: single-acting, double-acting, power beyond

---

## Hydraulic Requirements by Equipment Type

### Harvesters

| Model | Type | GPM | PSI | Remotes | HP Required |
|-------|------|-----|-----|---------|-------------|
| 6740 | 4-Row | 45-60 | 2800 | 4-6 | 250-370 |
| 6631 | 3-Row AirSep | 60 | 2800 | 3+2 | 320 |
| 6621 | 2-Row AirSep | 60 | 2800 | 3-6 | 220 |

**Hydraulic Functions:**
- Primary elevator speed control
- Side elevator operation
- Shaker systems
- Hump adjustment
- Boom positioning
- Fan speed control

---

### Windrowers

| Model | Type | GPM | PSI | Remotes | HP Required |
|-------|------|-----|-----|---------|-------------|
| 6160 | 6-Row | 40 | 2800 | 3 | 200 |
| 6180 | 8-Row Folding | 50 | - | PB+1 | 300 |

**Hydraulic Functions:**
- Hydraulic shaker
- Blade positioning
- Coulter disc operation
- Wing folding (6180)

---

### Planters

| Model | Type | GPM | PSI | Remotes | HP Required |
|-------|------|-----|-----|---------|-------------|
| 8908 | 8-Row Belt | 60-80 | - | 4 DA | - |
| 8906 | 6-Row Belt | 60-80 | - | 4 DA | - |

**Note:** DA = Double-Acting

**Hydraulic Functions:**
- Belt drive systems
- Seed metering
- Hopper controls
- Folding mechanisms

---

### Material Handling (Pilers, Scoopers, Crop Carts)

| Model | Type | GPM | PSI | Notes |
|-------|------|-----|-----|-------|
| 880 | Large Frame Piler | - | - | Multi-function simultaneous operation |
| 4835 | 35-Ton Crop Cart | 60 gal | - | Track/tire/tandem options |

**Hydraulic Functions:**
- Boom side-to-side movement
- Boom raising/lowering
- Conveyor belt speed control
- Hopper positioning
- Precise speed control with joystick

---

## Hydraulic System Components

### Common Components Across Spudnik Equipment

1. **Power Units**
   - Tractor PTO-driven
   - Dedicated electric motor-driven
   - Hydraulic pumps (gear, piston)

2. **Pumps**
   - Gear pumps (simple, reliable)
   - Piston pumps (variable displacement, high efficiency)
   - Flow capacities: 40-80 GPM

3. **Valves**
   - Directional control valves
   - Flow control valves (speed regulation)
   - Pressure relief valves (2800 PSI protection)
   - Load holding valves (safety)
   - PO check valves

4. **Cylinders**
   - Hydraulic actuators
   - Various bore sizes and stroke lengths
   - Double-acting and single-acting

5. **Flow Dividers**
   - Equal flow distribution to multiple circuits
   - Synchronization of cylinders

6. **Hoses and Fittings**
   - High-pressure rated (3000+ PSI)
   - Quick-connect couplers
   - Various sizes for flow requirements

7. **Filters and Coolers**
   - Hydraulic oil filtration
   - Temperature management

---

## Hydraulic Design Principles at Spudnik

### Multi-Function Simultaneous Operation

**Example: 880 Large Frame Piler**
- Advanced hydraulic system allows multiple functions to operate simultaneously
- Boom can move side-to-side while raising/lowering
- Conveyor belt operates independently
- Joystick control for precise operator input

**Engineering Challenge:**
- Adequate flow distribution to all functions
- Pressure management across multiple circuits
- Responsive control without hunting or lag

### Precise Speed Control

**Applications:**
- Material handling conveyors (consistent feed rate)
- Elevator systems (prevent damage to potatoes)
- Shaker systems (optimized separation)

**Technology:**
- Flow control valves
- Variable displacement pumps
- Electronic control systems

### Reversible Systems

**Example: AirSep Harvesters**
- Reversible chain systems prevent jams
- Hydraulic motor reversal capability
- Quick response to operator input

---

## Hydraulic System Validation Requirements

### Flow Validation
- **Total Flow Demand** must not exceed **Pump Capacity**
- Calculate sum of all simultaneous functions
- Account for peak demand scenarios

**Example:**
```
Pump Capacity: 60 GPM
- Elevator: 25 GPM
- Shaker: 15 GPM
- Boom: 10 GPM
- Conveyor: 8 GPM
-----------------
Total: 58 GPM ✓ (under 60 GPM limit)
```

### Pressure Validation
- All components rated for **2800 PSI minimum**
- Safety factor typically 1.5-2.0x
- Relief valves set at 2800 PSI

### Remote Valve Requirements
- Count all double-acting cylinders
- Verify tractor has sufficient remote outlets
- Consider power-beyond configurations for expansion

---

## Hydraulic Training at Spudnik

**Spudnik offers hydraulic training courses:**
- Available at: technicaltraining.spudnik.com/events/
- Operator training programs
- Dealer/service center technical training
- Hands-on workshops
- Expert-led sessions

**Topics Covered:**
- Basic hydraulic principles
- Troubleshooting hydraulic systems
- Component identification and replacement
- Pressure and flow diagnostics
- Safety procedures

---

## Implications for 990 EPC Project

### What the Configurator Must Handle

1. **Flow Calculations**
   - Sum flow requirements of all selected functions
   - Compare to pump capacity
   - Flag overloaded pumps

2. **Pressure Validation**
   - Ensure all components rated for 2800 PSI
   - Standard across all configurations

3. **Remote Valve Counting**
   - Track double-acting cylinders
   - Calculate total remotes needed
   - Recommend tractor specifications

4. **Component Selection**
   - Pumps (size based on total flow)
   - Valves (type and quantity)
   - Cylinders (size and stroke)
   - Flow dividers (when multiple circuits need equal flow)

5. **Assembly Recommendations**
   - Standard assemblies for common functions
   - Load holding requirements
   - PO check requirements
   - Safety systems

### Rules Engine Considerations

**Example Rules:**
- IF total flow > pump capacity THEN flag error
- IF function requires synchronized movement THEN recommend flow divider
- IF vertical cylinder THEN require load holding valve
- IF pressure spike risk THEN recommend PO check valve

---

## Common Hydraulic Assemblies

### Power Unit Assembly
- Hydraulic pump
- Electric motor or PTO connection
- Reservoir/tank
- Filtration
- Pressure relief valve

### Function Branch Assembly
- Directional control valve
- Flow control valve (if speed adjustment needed)
- Hydraulic cylinder or motor
- Load holding valve (if vertical/safety-critical)

### Flow Distribution Assembly
- Flow divider
- Multiple outlet connections
- Pressure compensation

---

## Reference Specifications

**Standard Values for 990 Eliminator (Estimated):**
- Pressure: 2800 PSI
- Flow: 50-70 GPM (depending on size and features)
- Remotes: 4-6 double-acting
- Power: Electric motor or tractor PTO

**These will be refined during the interview process with hydraulic engineering team.**

---

*Reference Document for 990 EPC Project*
*Last Updated: 2025-11-09*
