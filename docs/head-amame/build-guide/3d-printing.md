# 3D Printing Guide

Comprehensive guide to printing all head(amame) components with optimal quality and minimal post-processing requirements.

!!! success "Printer Compatibility"
    head(amame) is designed to print on any FDM printer with a minimum build volume of 200x200x200mm. Successfully tested on Prusa, Ender, Bambu, and dozens of other printer models.

## Quick Start Checklist

- [ ] Download latest [STL files](../downloads/stl-files.md)
- [ ] Calibrate printer (bed level, flow rate, temperature)
- [ ] Prepare print surface (clean bed, proper adhesion)
- [ ] Load recommended filament and settings
- [ ] Start with test print to verify quality

## Recommended Print Settings

### Universal Settings (All Printers)

<div class="print-settings">
<div class="print-setting">
<div class="setting-name">Layer Height</div>
<div class="setting-value">0.2mm</div>
</div>

<div class="print-setting">
<div class="setting-name">Infill Density</div>
<div class="setting-value">20%</div>
</div>

<div class="print-setting">
<div class="setting-name">Infill Pattern</div>
<div class="setting-value">Cubic</div>
</div>

<div class="print-setting">
<div class="setting-name">Perimeters</div>
<div class="setting-value">3</div>
</div>

<div class="print-setting">
<div class="setting-name">Top/Bottom Layers</div>
<div class="setting-value">5</div>
</div>

<div class="print-setting">
<div class="setting-name">Support Material</div>
<div class="setting-value">Required (see below)</div>
</div>
</div>

### Material-Specific Settings

=== "🟢 PLA+"
    
    **Recommended for beginners**
    
    <div class="print-settings">
    <div class="print-setting">
    <div class="setting-name">Nozzle Temperature</div>
    <div class="setting-value">210°C</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Bed Temperature</div>
    <div class="setting-value">60°C</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Print Speed</div>
    <div class="setting-value">50mm/s</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Cooling</div>
    <div class="setting-value">100% after layer 3</div>
    </div>
    </div>
    
    **Pros**: Easy to print, good surface finish, minimal warping  
    **Cons**: Lower temperature resistance, moderate strength

=== "🔵 PETG"
    
    **Best overall performance**
    
    <div class="print-settings">
    <div class="print-setting">
    <div class="setting-name">Nozzle Temperature</div>
    <div class="setting-value">245°C</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Bed Temperature</div>
    <div class="setting-value">80°C</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Print Speed</div>
    <div class="setting-value">40mm/s</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Cooling</div>
    <div class="setting-value">30% maximum</div>
    </div>
    </div>
    
    **Pros**: Chemical resistance, excellent strength, clear options  
    **Cons**: Slightly more challenging to print, stringing potential

=== "🟤 Wood-Filled"
    
    **Premium aesthetic finish**
    
    <div class="print-settings">
    <div class="print-setting">
    <div class="setting-name">Nozzle Temperature</div>
    <div class="setting-value">200°C</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Bed Temperature</div>
    <div class="setting-value">60°C</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Print Speed</div>
    <div class="setting-value">30mm/s</div>
    </div>
    
    <div class="print-setting">
    <div class="setting-name">Cooling</div>
    <div class="setting-value">50% after layer 5</div>
    </div>
    </div>
    
    **Pros**: Beautiful finish, sandable, stainable  
    **Cons**: Abrasive (hardened nozzle recommended), requires post-processing

## Component Printing Order

Print components in this order to optimize your workflow and identify any printer issues early:

### Phase 1: Test & Small Parts (4-6 hours)

<div class="build-step">
<div class="step-number">1</div>
<div>
**Print Test Cube** (30 minutes)  
Verify dimensional accuracy and surface quality before printing large parts
</div>
</div>

<div class="build-step">
<div class="step-number">2</div>
<div>
**Adjustment Sliders** (2 hours)  
Small, functional parts that test fit tolerances
</div>
</div>

<div class="build-step">
<div class="step-number">3</div>
<div>
**Cable Management Parts** (2 hours)  
Various small components for cable routing and strain relief
</div>
</div>

### Phase 2: Major Components (40-48 hours)

<div class="build-step">
<div class="step-number">4</div>
<div>
**Left Ear Cup** (18-22 hours)  
Print one cup first to verify settings before committing to both
</div>
</div>

<div class="build-step">
<div class="step-number">5</div>
<div>
**Right Ear Cup** (18-22 hours)  
Mirror of left cup with identical settings
</div>
</div>

<div class="build-step">
<div class="step-number">6</div>
<div>
**Headband Assembly** (8-12 hours)  
Multiple parts that can be printed simultaneously
</div>
</div>

## Print Orientation & Support

### Ear Cups - Critical Orientation

![Print Orientation Diagram](../../assets/images/head-amame/print-orientation-cups.png)

**Optimal Position:**
- Driver mounting face DOWN on print bed
- Headband attachment pointing UP
- Natural support structures minimized

**Support Requirements:**
- **Tree supports**: Recommended for overhangs
- **Support angle**: 45° threshold
- **Support density**: 15% for easy removal
- **Support Z-distance**: 0.2mm

!!! warning "Common Orientation Mistakes"
    
    **❌ Don't print cups sideways** - Creates weak layer adhesion  
    **❌ Don't print driver-side up** - Requires heavy support material  
    **❌ Don't use grid supports** - Difficult to remove from curved surfaces

### Headband Components

![Headband Print Setup](../../assets/images/head-amame/print-orientation-headband.png)

**Arrangement Tips:**
- Print all headband parts in single job for consistency
- Orient adjustment mechanisms for strength along use direction
- Minimal supports needed with proper orientation

## Quality Control & Testing

### Dimensional Accuracy Test

Before printing the full set, verify your printer's accuracy:

```gcode
; Test cube with critical dimensions
; Print this first to verify scaling
G28 ; Home all axes
; ... (test cube gcode)
```

**Test Points:**
- Overall dimensions: 20.00mm ±0.1mm
- Hole diameter: 5.00mm ±0.05mm
- Thread test: M3 insert should fit snugly

### Surface Quality Assessment

<div class="spec-table">
<div class="spec-label">Layer Adhesion</div>
<div class="spec-value">No visible layer separation</div>
<div class="spec-label">Surface Finish</div>
<div class="spec-value">Minimal visible layer lines</div>
<div class="spec-label">Overhang Quality</div>
<div class="spec-value">Clean 45° overhangs without support</div>
<div class="spec-label">Bridge Performance</div>
<div class="spec-value">20mm bridges without sagging</div>
</div>

## Troubleshooting Common Issues

### Print Adhesion Problems

!!! danger "Warping/Lifting"
    
    **Symptoms**: Corners lifting, part detaching mid-print  
    **Solutions**:
    - Increase bed temperature by 5-10°C
    - Use brim or raft for larger contact area
    - Check bed level - first layer critical
    - Clean bed with isopropyl alcohol
    - Consider enclosure for PETG/ABS

### Surface Quality Issues

!!! warning "Layer Inconsistency"
    
    **Symptoms**: Visible layer variations, poor surface finish  
    **Solutions**:
    - Check belt tension and frame rigidity
    - Verify consistent filament diameter
    - Adjust flow rate (typically 95-105%)
    - Reduce print speed for better quality

### Support Removal Challenges

!!! tip "Difficult Support Removal"
    
    **Prevention**:
    - Use tree supports instead of grid
    - Increase support Z-distance to 0.25mm
    - Print support interface at lower temperature
    - Consider soluble supports for complex geometry

## Post-Processing Requirements

### Essential Post-Processing

<div class="build-step">
<div class="step-number">1</div>
<div>
**Support Removal** (30-60 minutes)  
Carefully remove all support material with flush cutters
</div>
</div>

<div class="build-step">
<div class="step-number">2</div>
<div>
**Hole Cleaning** (15 minutes)  
Drill out or ream all mounting holes to proper diameter
</div>
</div>

<div class="build-step">
<div class="step-number">3</div>
<div>
**Test Fit** (15 minutes)  
Verify all components fit together before assembly
</div>
</div>

### Optional Finishing

<div class="build-step">
<div class="step-number">4</div>
<div>
**Surface Smoothing** (1-2 hours)  
Sand with progressively finer grits: 220 → 400 → 800
</div>
</div>

<div class="build-step">
<div class="step-number">5</div>
<div>
**Finishing Coat** (varies)  
Primer and paint, or wood stain for wood-filled filament
</div>
</div>

## Printer-Specific Profiles

We maintain tested printer profiles for popular models:

### Prusa i3 MK3S+

**Download Profile**: [head-amame-prusa-mk3s.ini](../downloads/printer-profiles/prusa-mk3s.ini)

**Key Settings:**
- 0.2mm layer height profile as base
- Modified support settings for complex geometry
- Tested on both PLA+ and PETG

### Bambu Lab X1 Carbon

**Download Profile**: [head-amame-bambu-x1.json](../downloads/printer-profiles/bambu-x1.json)

**Key Settings:**
- AMS compatibility verified
- Optimized for fast printing with quality
- Auto-support generation tuned

### Ender 3 Series

**Download Profile**: [head-amame-ender3.ini](../downloads/printer-profiles/ender3.ini)

**Key Settings:**
- Conservative settings for reliability
- Manual support optimization required
- Tested on stock and upgraded machines

## Material Usage Calculator

Estimate your filament consumption:

<div class="cost-calculator">
<h3>🎯 Filament Usage Estimate</h3>

<div class="cost-row">
<span>Main Ear Cups (both)</span>
<span>~400g</span>
</div>

<div class="cost-row">
<span>Headband Components</span>
<span>~150g</span>
</div>

<div class="cost-row">
<span>Small Parts & Hardware</span>
<span>~50g</span>
</div>

<div class="cost-row">
<span>Support Material</span>
<span>~80g</span>
</div>

<div class="cost-row">
<span>Failed Prints Buffer (10%)</span>
<span>~70g</span>
</div>

<div class="cost-total">
**Total Filament Needed: ~750g**

*Order 1kg spool for single-color build*
</div>
</div>

## Print Time Estimates

**Fast Settings (0.3mm layers)**: ~30 hours total  
**Standard Settings (0.2mm layers)**: ~48 hours total  
**High Quality (0.15mm layers)**: ~65 hours total

!!! tip "Time Management"
    
    - Start long prints (ear cups) on weekends
    - Print small parts during weekdays
    - Consider printing duplicate parts simultaneously
    - Factor in potential reprints for learning curve

[Next: Assembly Guide →](assembly.md){ .md-button .md-button--primary }

---

*Print settings continuously updated based on community feedback. Join [Discord](https://discord.gg/headamame) to share your print results and get real-time help.*