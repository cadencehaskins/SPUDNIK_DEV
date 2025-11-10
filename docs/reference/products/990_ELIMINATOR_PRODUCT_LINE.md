# 990 Eliminator Product Line - Technical Reference

## Overview

The Eliminator product line streamlines potato sorting and processing, removing unwanted materials from harvested potatoes. This is one of Spudnik's most customizable product families.

---

## 990 Custom Potato Eliminator ⭐

**Product URL:** https://www.spudnik.com/spudnik-product/990-custom-potato-eliminator/

### Purpose
Streamlines sorting process and removes unwanted materials (dirt, rocks, debris, damaged potatoes) from harvested potatoes.

### Customization Options

**Chain/Belt Widths:** 5 options
- 48 inches
- 60 inches
- 72 inches
- 84 inches
- 96 inches

**Configuration Types:**
- Chain system
- Belt system

**Optional Features:**
- Spreader roller
- Catwalk

### System Components

1. **Intake/Elevator System**
   - Multiple width options to match chain/belt selection
   - Receives potatoes from harvest equipment or storage

2. **Separation Units**
   - Extracts extraneous substances (dirt, rocks, debris)
   - Removes damaged or unwanted potatoes

3. **Sizing and Picking Station**
   - Sorts potatoes by size
   - Manual removal workspace for quality control
   - Worker-accessible platform

4. **Discharge System**
   - Conveys sorted potatoes to downstream conveyors
   - Connects to storage or transportation equipment

### Why This Project Exists

The **990 Custom Eliminator** is the primary focus of the Engineering Preview Configurator (EPC) project because:

1. **High Customization**: 5 widths × 2 types × multiple options = many possible configurations
2. **Complex Hydraulic Systems**: Each configuration has different power and flow requirements
3. **Custom Engineering**: Each installation is tailored to customer needs
4. **Time-Consuming Design**: Engineers currently search through schematics and drawings manually
5. **Standardization Opportunity**: Many configurations reuse validated assemblies

---

## 994 AirSep Potato Eliminator

**Product URL:** https://www.spudnik.com/spudnik-product/994-airsep-potato-eliminator/

### Specifications

**Dimensions:**
- Working Width: 105 inches (2.67 m)
- Length (without tongue): 42.5-44.5 feet (12.80-13.41 m)
- Transport/Working Width: 15.875-20.25 feet (4.57-6.10 m)
- Overall Height: 14 feet

**Intake:**
- Height: 31-50 inches (adjustable)
- Width: 84 inches

**Capacity:**
- Up to 3000 sacks/hour
- 135 tons/hour

### Features

**Air Separation Technology:**
- Advanced debris removal using air flow
- Separates stones, dirt, and other contaminants
- 105-inch separation chamber

**Control Systems:**
- Upper controls for real-time adjustments
- Industrial electrical controls
- Maintenance Mode for independent function operation

**Unified Systems:**
- Integrated trash conveyor system
- Streamlined operation

### Electrical Requirements
- Voltage Options: 230V 1-phase, 230V 3-phase, 480V 3-phase

---

## 991 AirSep Potato Eliminator

**Product URL:** https://www.spudnik.com/spudnik-product/991-airsep-potato-eliminator/

### Features
- Air separation technology for debris removal
- Reduces quality deductions to near zero

### Performance
**User Testimonial** (Blake Underwood, Buyan Ranch):
- Reports "slightly above 0%" deduction baseline
- Significant improvement over traditional methods

---

## Eliminator Product Family Comparison

| Model | Type | Width | Capacity | Key Feature |
|-------|------|-------|----------|-------------|
| 990 Custom | Chain/Belt | 48-96" | Variable | Highly customizable |
| 994 AirSep | Air Separation | 105" | 3000 sacks/hr | High capacity, industrial controls |
| 991 AirSep | Air Separation | - | - | Near-zero quality deductions |

---

## Hydraulic System Context

### Why Hydraulics Matter for Eliminators

Eliminators require hydraulic systems for:
1. **Intake Elevator Control** - Variable speed control for material flow
2. **Separation System Operation** - Shakers, vibrators, and separation mechanisms
3. **Discharge Conveyor Control** - Coordinated material movement
4. **Optional Features** - Spreader rollers, adjustable components

### Typical Hydraulic Requirements

While specific hydraulic specs for the 990 Eliminator aren't publicly listed, similar Spudnik equipment shows:
- **Standard Pressure:** 2800 PSI (industry standard across Spudnik line)
- **Flow Requirements:** 40-80 GPM depending on size and features
- **Remote Valves:** 3-6 double-acting remotes typical

**Example from Similar Equipment (6740 Harvester):**
- 45-60 GPM at 2800 PSI
- 4-6 remote valves

### Power Unit Integration

Eliminators typically operate from:
- **Tractor hydraulic systems** (for mobile/field operation)
- **Dedicated power units** (for stationary/storage facility operation)
- **Electric motors with hydraulic pumps** (for permanent installations)

---

## Integration with Other Equipment

### Upstream Equipment (Feeds into Eliminator)
- Harvesters (6740, 6631, 6621)
- Crop Carts (4835, 4735)
- Storage bins (1872, 1860)
- Scoopers (150, 350)

### Downstream Equipment (Receives from Eliminator)
- Conveyors (1200, 1205, 1250 series)
- Pilers (880, 780, 560, 480)
- Storage systems
- Transportation equipment (bulk beds 4400/4500)

### System Flow Example
```
Storage Bin → Scooper → 990 Eliminator → Conveyor → Piler → Storage Pile
```

---

## Customization Process (Current State)

**Current Engineering Workflow:**
1. Customer specifies needs (capacity, space, downstream equipment)
2. Engineer selects eliminator width (48", 60", 72", 84", or 96")
3. Engineer chooses chain or belt system
4. Engineer searches schematics for hydraulic requirements
5. Engineer designs power unit configuration
6. Engineer selects valves, pumps, cylinders, flow dividers
7. Engineer validates flow and pressure requirements
8. Manual BOM creation
9. Design review

**Pain Points (Why EPC is Needed):**
- Time-consuming schematic searches
- Risk of configuration errors
- Difficulty reusing validated designs
- Manual BOM generation
- Hard to maintain standardization

---

## Related Equipment Categories

For complete potato processing systems, see also:
- **Pilers:** [docs/reference/products/PILERS_AND_CONVEYORS.md]
- **Scoopers:** [docs/reference/products/MATERIAL_HANDLING.md]
- **Bins:** [docs/reference/products/STORAGE_SYSTEMS.md]

---

*Reference Document for 990 EPC Project*
*Last Updated: 2025-11-09*
