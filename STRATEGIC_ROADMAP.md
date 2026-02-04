# BG-EHS License Practitioner Quote Application
## Strategic Roadmap & System Design

**Document Version:** 1.0
**Scope:** Intro, Essential, Essential Plus tiers only
**Purpose:** Strategy and product design for offline browser-based quote generation application

---

## Table of Contents

1. [Tier Extraction](#1-tier-extraction)
2. [Variables Inventory & Rules](#2-variables-inventory--rules)
3. [App Flow and UX](#3-app-flow-and-ux)
4. [Data Model and Logic Mapping](#4-data-model-and-logic-mapping)
5. [Pricing System and Checklist](#5-pricing-system-and-checklist)
6. [Quote Engine Logic](#6-quote-engine-logic)
7. [Proposal Template Design](#7-proposal-template-design)
8. [Roadmap (MVP / V1 / V2)](#8-roadmap-mvp--v1--v2)
9. [Risks, Edge Cases, and Validation Plan](#9-risks-edge-cases-and-validation-plan)

---

## 1. Tier Extraction

### 1A. Source Analysis

**Source:** BG-EHS Service Levels Offerings 2024: Mandatory Basic Standard Requirements
**Columns analyzed:** Intro, Essential (& Essential PLUS)
**Out of scope (ignored):** Core, Core Plus, and any tiers beyond Essential Plus

---

### 1B. Tier Definition Tables

#### INTRO TIER

| Application Category | What's Included | Density/Coverage | Constraints |
|---------------------|-----------------|------------------|-------------|
| **BG28 Ring BG3 Center Solution** | 1 Pair (1 BG28 Ring in H/B gridline + 1 in Curry gridline) | 1 Pair per 100m² (1,080 sq ft) per floor | Reduced density vs Essential |
| **Doorway Disc Solution** | 1 D-Disc + 1 BG3 #7 Strip Sticker per door | External & Bedroom doors ONLY | Interior/bathroom doors excluded |
| **Space Harmonizer Solutions** | NOT INCLUDED | — | Must upgrade to Essential |
| **Earth Gridlines Discs Layering** | NOT INCLUDED | — | Must upgrade to Essential |
| **Water Supply Solution** | BG3 Numerical Strip(s) #11 | Per water supply point | Included |
| **Electrical Panel Solution** | BG3 Numerical Strips #9 & 16/19 + SGFuse L-Solution | Per electrical panel | Included |
| **L66 Bedside Outlets** | P3 BG3 L66 Solution | Bedside outlets only | Living area outlets excluded |
| **Cubic Disc for TVs/Appliances** | NOT INCLUDED | — | Essential Plus only |
| **L-Wifi Solution** | NOT INCLUDED | — | Essential tier add-on |
| **Bedroom Windows** | P3 BG3 L Solution | All bedroom windows | Included |
| **Living Area Windows** | NOT INCLUDED | — | Essential Plus optional |
| **Bedroom Mirrors** | P3 BG3 L90 Solution | All bedroom mirrors | Included |
| **Living Area Mirrors** | NOT INCLUDED | — | Essential Plus optional |

**Intro Tier Summary:**
- Entry-level protection focused on bedrooms and critical systems
- Reduced BG28 Ring density (half of Essential)
- Door protection limited to external + bedroom only
- No space harmonization or earth gridline solutions
- Electrical protection limited to panels and bedside outlets
- Windows/mirrors limited to bedrooms

---

#### ESSENTIAL TIER

| Application Category | What's Included | Density/Coverage | Constraints |
|---------------------|-----------------|------------------|-------------|
| **BG28 Ring BG3 Center Solution** | 1 Pair (1 BG28 Ring in H/B gridline + 1 in Curry gridline) | 1 Pair per 50m² (540 sq ft) per floor | Full standard density |
| **Doorway Disc Solution** | 1 D-Disc + 1 BG3 #7 Strip Sticker per door | ALL doors | Complete door coverage |
| **BG3 Center Space Harmonizer** | BG3 Center BG Space Harmonizer Solution | 1 per 200m² (2,150 sq ft) per floor | Included |
| **Cubic Disc BG3 Center** | BG-EHS Cubic Disc BG3 Center Solution | 1 per 75m² (810 sq ft) per floor | Included |
| **Earth Gridlines - Bedrooms** | H/B and Curry Earth Gridlines Discs (1 of Each) | All bedrooms | Standard layering |
| **Water Supply Solution** | BG3 Numerical Strip(s) #11 | Per water supply point | Included |
| **Electrical Panel Solution** | BG3 Numerical Strips #9 & 16/19 + SGFuse L-Solution | Per electrical panel | Included |
| **L66 Bedside Outlets** | P3 BG3 L66 Solution | Bedside outlets only | Included |
| **L-Wifi Solution** | P3 BG3 L-Wifi Solution | Per router/access point | Available as add-on |
| **Bedroom Windows** | P3 BG3 L Solution | All bedroom windows | Included |
| **Bedroom Mirrors** | P3 BG3 L90 Solution | All bedroom mirrors | Available as add-on |

**Essential Tier Summary:**
- Full BG28 Ring density (double Intro)
- Complete door coverage (all doors)
- Space harmonization included
- Earth gridline protection for bedrooms
- L-Wifi available as add-on
- Bedroom mirrors as add-on

---

#### ESSENTIAL PLUS TIER

Everything in Essential, PLUS the following optional add-ons become available:

| Optional Add-On | Description | Coverage |
|----------------|-------------|----------|
| **Earth Gridlines - Living Spaces** | H/B and Curry Earth Gridlines Discs (1 of Each) | All living spaces |
| **Earth Gridlines - Full Coverage** | All H/B & Curry Earth Gridlines | All bedrooms + living spaces |
| **Cubic Disc for TVs/Appliances** | P3 BG-EHS Cubic Disc Solution | TVs & large appliances |
| **L66 All Outlets (Living Areas)** | P3 BG3 L66 Solution | All electrical outlets in living areas |
| **Windows (Living Areas)** | P3 BG3 L Solution | All windows in living areas |
| **Mirrors (Living Areas)** | P3 BG3 L90 Solution | All mirrors in living areas |

**Essential Plus Tier Summary:**
- All Essential inclusions
- Unlocks living area add-ons (windows, mirrors, outlets)
- Enhanced earth gridline options (living spaces, full coverage)
- TV/appliance protection available
- Most comprehensive coverage option within scope

---

### 1C. Tier Comparison Matrix

| Feature | Intro | Essential | Essential Plus |
|---------|-------|-----------|----------------|
| BG28 Ring Density | 1/100m² | 1/50m² | 1/50m² |
| Door Coverage | External + Bedroom | All Doors | All Doors |
| Space Harmonizer | — | ✓ | ✓ |
| Cubic Disc Center | — | ✓ | ✓ |
| Earth Gridlines (Bedrooms) | — | ✓ | ✓ |
| Earth Gridlines (Living) | — | — | Optional |
| Water Supply | ✓ | ✓ | ✓ |
| Electrical Panels | ✓ | ✓ | ✓ |
| L66 Bedside | ✓ | ✓ | ✓ |
| L66 All Outlets | — | — | Optional |
| L-Wifi | — | Add-on | Add-on |
| Cubic Disc TVs | — | — | Optional |
| Bedroom Windows | ✓ | ✓ | ✓ |
| Living Windows | — | — | Optional |
| Bedroom Mirrors | ✓ | Add-on | Add-on |
| Living Mirrors | — | — | Optional |

---

### 1D. Prerequisites and Limitations

**Associate Practitioner Constraints (inferred):**
- Limited to Intro, Essential, Essential Plus tiers
- Core and Core Plus require higher certification level
- P3 BG3 Center Baseplate BG Space Harmonizer Solution (1 per 250m²) not explicitly marked — assumed out of scope or requires clarification

**Tier Upgrade Path:**
- Intro → Essential: Adds space harmonization, full door coverage, earth gridlines, double BG28 density
- Essential → Essential Plus: Unlocks living area optional add-ons

---

## 2. Variables Inventory & Rules

### 2A. Quote-Relevant Variables Inventory

#### Property Variables

| Variable | Data Type | Purpose | Affects |
|----------|-----------|---------|---------|
| `total_floor_area_sqm` | Number | Total property size in m² | BG28 Ring qty, Space Harmonizer qty, Cubic Disc qty |
| `total_floor_area_sqft` | Number | Auto-calculated from m² | Display only |
| `num_floors` | Integer | Number of floors/levels | Multiplier for per-floor items |
| `num_bedrooms` | Integer | Bedroom count | Earth gridlines, windows, mirrors, L66 bedside |
| `num_living_spaces` | Integer | Living rooms, dens, offices | Essential Plus add-ons |
| `num_bathrooms` | Integer | Bathroom count | Door count (Essential only) |

#### Door Variables

| Variable | Data Type | Purpose | Affects |
|----------|-----------|---------|---------|
| `num_external_doors` | Integer | Entry/exit doors | Doorway Disc qty (all tiers) |
| `num_bedroom_doors` | Integer | Bedroom doors | Doorway Disc qty (all tiers) |
| `num_interior_doors` | Integer | Other interior doors | Doorway Disc qty (Essential+ only) |
| `total_doors` | Calculated | Sum of above | Line item quantity |

#### Systems Variables

| Variable | Data Type | Purpose | Affects |
|----------|-----------|---------|---------|
| `num_electrical_panels` | Integer | Main + sub panels | Electrical Panel Solution qty |
| `num_water_supply_points` | Integer | Main water entry points | Water Supply Solution qty |
| `num_wifi_routers` | Integer | Routers/access points | L-Wifi qty (Essential+ add-on) |
| `num_tvs_large_appliances` | Integer | TVs, refrigerators, etc. | Cubic Disc TV qty (Essential Plus) |

#### Outlet Variables

| Variable | Data Type | Purpose | Affects |
|----------|-----------|---------|---------|
| `num_bedside_outlets` | Integer | Outlets near beds | L66 Bedside qty |
| `num_living_area_outlets` | Integer | Other living area outlets | L66 Living qty (Essential Plus) |

#### Window/Mirror Variables

| Variable | Data Type | Purpose | Affects |
|----------|-----------|---------|---------|
| `num_bedroom_windows` | Integer | Windows in bedrooms | L Solution qty |
| `num_living_windows` | Integer | Windows in living areas | L Solution qty (Essential Plus) |
| `num_bedroom_mirrors` | Integer | Mirrors in bedrooms | L90 Solution qty |
| `num_living_mirrors` | Integer | Mirrors in living areas | L90 Solution qty (Essential Plus) |

#### Logistics Variables

| Variable | Data Type | Purpose | Affects |
|----------|-----------|---------|---------|
| `travel_distance_km` | Number | Distance to property | Travel fee |
| `property_location` | Text | Address/city | Documentation |
| `estimated_visits` | Integer | Number of site visits | Time/visit pricing |
| `installation_complexity` | Enum (Standard/Complex) | Difficulty factors | Complexity multiplier |

#### Client Variables

| Variable | Data Type | Purpose | Affects |
|----------|-----------|---------|---------|
| `client_name` | Text | Contact name | Proposal header |
| `client_email` | Text | Contact email | Proposal delivery |
| `client_phone` | Text | Contact phone | Optional |
| `property_name` | Text | Property identifier | Proposal reference |
| `project_date` | Date | Target date | Scheduling |

---

### 2B. Rule Translation

#### Tier Eligibility Rules

```
RULE: Tier Availability
  IF practitioner_level = "Associate"
  THEN available_tiers = [Intro, Essential, Essential Plus]
  AND unavailable_tiers = [Core, Core Plus] → display "Out of scope (ignored)"
```

#### BG28 Ring Calculation Rules

```
RULE: BG28 Ring Quantity - Intro
  IF tier = Intro
  THEN bg28_ring_pairs = CEILING(total_floor_area_sqm / 100) × num_floors

RULE: BG28 Ring Quantity - Essential/Essential Plus
  IF tier IN [Essential, Essential Plus]
  THEN bg28_ring_pairs = CEILING(total_floor_area_sqm / 50) × num_floors
```

#### Doorway Disc Rules

```
RULE: Doorway Disc Quantity - Intro
  IF tier = Intro
  THEN doorway_disc_qty = num_external_doors + num_bedroom_doors

RULE: Doorway Disc Quantity - Essential/Essential Plus
  IF tier IN [Essential, Essential Plus]
  THEN doorway_disc_qty = num_external_doors + num_bedroom_doors + num_interior_doors
```

#### Space Harmonizer Rules

```
RULE: Space Harmonizer Eligibility
  IF tier = Intro
  THEN space_harmonizer_included = FALSE
  AND display_note = "Upgrade to Essential for Space Harmonization"

RULE: Space Harmonizer Quantity
  IF tier IN [Essential, Essential Plus]
  THEN space_harmonizer_qty = CEILING(total_floor_area_sqm / 200) × num_floors
  AND cubic_disc_center_qty = CEILING(total_floor_area_sqm / 75) × num_floors
```

#### Earth Gridlines Rules

```
RULE: Earth Gridlines - Intro
  IF tier = Intro
  THEN earth_gridlines_included = FALSE

RULE: Earth Gridlines - Essential
  IF tier = Essential
  THEN earth_gridlines_bedrooms = num_bedrooms × 2  // 1 H/B + 1 Curry per bedroom
  AND earth_gridlines_living = NOT_AVAILABLE

RULE: Earth Gridlines - Essential Plus
  IF tier = Essential Plus
  THEN earth_gridlines_bedrooms = num_bedrooms × 2
  AND earth_gridlines_living_optional = num_living_spaces × 2
  AND earth_gridlines_full_optional = AVAILABLE
```

#### Electrical Rules

```
RULE: Electrical Panel - All Tiers
  ALL tiers include: electrical_panel_qty = num_electrical_panels

RULE: L66 Bedside - All Tiers
  ALL tiers include: l66_bedside_qty = num_bedside_outlets

RULE: L-Wifi - Essential+
  IF tier IN [Essential, Essential Plus]
  THEN l_wifi_available_as_addon = TRUE
  AND l_wifi_qty = num_wifi_routers (if selected)

RULE: L66 Living - Essential Plus Only
  IF tier = Essential Plus AND addon_l66_living_selected = TRUE
  THEN l66_living_qty = num_living_area_outlets

RULE: Cubic Disc TVs - Essential Plus Only
  IF tier = Essential Plus AND addon_cubic_disc_tv_selected = TRUE
  THEN cubic_disc_tv_qty = num_tvs_large_appliances
```

#### Window/Mirror Rules

```
RULE: Bedroom Windows - All Tiers
  ALL tiers include: bedroom_windows_qty = num_bedroom_windows

RULE: Bedroom Mirrors - Intro
  IF tier = Intro
  THEN bedroom_mirrors_qty = num_bedroom_mirrors

RULE: Bedroom Mirrors - Essential/Essential Plus
  IF tier IN [Essential, Essential Plus]
  THEN bedroom_mirrors_available_as_addon = TRUE
  AND bedroom_mirrors_qty = num_bedroom_mirrors (if selected)

RULE: Living Windows - Essential Plus Only
  IF tier = Essential Plus AND addon_living_windows_selected = TRUE
  THEN living_windows_qty = num_living_windows

RULE: Living Mirrors - Essential Plus Only
  IF tier = Essential Plus AND addon_living_mirrors_selected = TRUE
  THEN living_mirrors_qty = num_living_mirrors
```

#### Conditional Input Rules

```
RULE: Require Living Space Details
  IF tier = Essential Plus
  AND ANY addon IN [earth_gridlines_living, l66_living, living_windows, living_mirrors] = selected
  THEN require_input(num_living_spaces, num_living_area_outlets, num_living_windows, num_living_mirrors)

RULE: Require TV/Appliance Count
  IF tier = Essential Plus AND addon_cubic_disc_tv_selected = TRUE
  THEN require_input(num_tvs_large_appliances)

RULE: Require Interior Door Count
  IF tier IN [Essential, Essential Plus]
  THEN require_input(num_interior_doors)
```

---

## 3. App Flow and UX

### 3A. End-to-End User Flow

```
┌─────────────────────────────────────────────────────────────────────┐
│                        APPLICATION FLOW                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  [1. START] ──► [2. CLIENT INFO] ──► [3. PROPERTY BASICS]           │
│                                              │                       │
│                                              ▼                       │
│                                    [4. TIER SELECTION]               │
│                                              │                       │
│                          ┌──────────────────┼──────────────────┐     │
│                          ▼                  ▼                  ▼     │
│                      [INTRO]          [ESSENTIAL]      [ESSENTIAL+]  │
│                          │                  │                  │     │
│                          ▼                  ▼                  ▼     │
│                    [5. TIER-SPECIFIC INPUTS]                         │
│                          │                  │                  │     │
│                          └──────────────────┼──────────────────┘     │
│                                              │                       │
│                                              ▼                       │
│                                    [6. ADD-ONS] (if applicable)      │
│                                              │                       │
│                                              ▼                       │
│                                    [7. REVIEW & CALCULATE]           │
│                                              │                       │
│                                              ▼                       │
│                                    [8. PROPOSAL PREVIEW]             │
│                                              │                       │
│                          ┌──────────────────┼──────────────────┐     │
│                          ▼                  ▼                  ▼     │
│                    [COPY TEXT]        [DOWNLOAD PDF]      [EDIT]     │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

### 3B. Screen-by-Screen Breakdown

#### Screen 1: Welcome / Start

**User Action:** Click "New Quote" or "Load Saved" (V1+)
**System Action:** Initialize empty quote object
**Fields:** None
**Navigation:** → Screen 2

---

#### Screen 2: Client Information

**User Actions:** Enter client details
**System Actions:** Store client data, validate email format

| Field | Type | Required | Default |
|-------|------|----------|---------|
| Client Name | Text | Yes | — |
| Client Email | Email | Yes | — |
| Client Phone | Phone | No | — |
| Property Name/Address | Text | Yes | — |
| Project Reference | Text | No | Auto-generate |

**Navigation:** → Screen 3

---

#### Screen 3: Property Basics

**User Actions:** Enter property dimensions and counts
**System Actions:** Auto-calculate sq ft from m², validate ranges

| Field | Type | Required | Default | Notes |
|-------|------|----------|---------|-------|
| Floor Area | Number | Yes | — | m² (auto-converts to sq ft) |
| Number of Floors | Integer | Yes | 1 | Min: 1 |
| Number of Bedrooms | Integer | Yes | — | Min: 1 |
| Number of External Doors | Integer | Yes | 1 | Entry doors |
| Number of Bedroom Doors | Integer | Yes | = bedrooms | Auto-fill |
| Number of Electrical Panels | Integer | Yes | 1 | Main + sub |
| Number of Water Supply Points | Integer | Yes | 1 | Main entry |
| Number of Bedside Outlets | Integer | Yes | = bedrooms × 2 | Auto-fill |
| Number of Bedroom Windows | Integer | Yes | — | — |
| Number of Bedroom Mirrors | Integer | No | 0 | — |

**Navigation:** → Screen 4

---

#### Screen 4: Tier Selection

**User Actions:** Select tier from Intro / Essential / Essential Plus
**System Actions:**
- Display tier comparison
- Highlight what each tier includes
- Show price estimate range (once prices defined)

| Field | Type | Required | Default |
|-------|------|----------|---------|
| Selected Tier | Radio/Cards | Yes | — |

**Display:** Side-by-side tier comparison cards showing inclusions
**Navigation:** → Screen 5

---

#### Screen 5: Tier-Specific Inputs

**Conditional fields based on tier:**

**If Intro:** No additional fields required
**Navigation:** → Screen 7 (skip add-ons)

**If Essential:**

| Field | Type | Required | Default |
|-------|------|----------|---------|
| Number of Interior Doors | Integer | Yes | — |
| Number of Wifi Routers | Integer | No | 0 |

**Navigation:** → Screen 6

**If Essential Plus:**

| Field | Type | Required | Default |
|-------|------|----------|---------|
| Number of Interior Doors | Integer | Yes | — |
| Number of Living Spaces | Integer | Yes | — |
| Number of Living Area Windows | Integer | Yes | — |
| Number of Living Area Mirrors | Integer | No | 0 |
| Number of Living Area Outlets | Integer | No | 0 |
| Number of TVs/Large Appliances | Integer | No | 0 |
| Number of Wifi Routers | Integer | No | 0 |

**Navigation:** → Screen 6

---

#### Screen 6: Add-Ons Selection

**User Actions:** Select optional add-ons
**System Actions:** Update quote with selected add-ons

**Essential Tier Add-Ons:**

| Add-On | Requires Input |
|--------|----------------|
| L-Wifi Solution | num_wifi_routers |
| Bedroom Mirrors | num_bedroom_mirrors |

**Essential Plus Tier Add-Ons:**

| Add-On | Requires Input |
|--------|----------------|
| L-Wifi Solution | num_wifi_routers |
| Bedroom Mirrors | num_bedroom_mirrors |
| Earth Gridlines - Living Spaces | num_living_spaces |
| Earth Gridlines - Full Coverage | num_bedrooms + num_living_spaces |
| L66 All Outlets (Living) | num_living_area_outlets |
| Cubic Disc for TVs/Appliances | num_tvs_large_appliances |
| Windows (Living Areas) | num_living_windows |
| Mirrors (Living Areas) | num_living_mirrors |

**Navigation:** → Screen 7

---

#### Screen 7: Review & Calculate

**User Actions:** Review all inputs, make corrections
**System Actions:**
- Apply all rules
- Calculate quantities
- Generate line items
- Calculate pricing (when defined)
- Show readiness status

**Display:**
- Summary of all inputs
- Calculated quantities table
- Preliminary pricing (or "prices TBD")
- Validation messages
- "Ready to generate" / "Missing required inputs" indicator

**Navigation:** → Screen 8 or ← Back to edit

---

#### Screen 8: Proposal Preview & Export

**User Actions:** Preview, edit notes, export
**System Actions:** Render proposal in selected format

**Features:**
- Full proposal preview
- Editable notes/assumptions section
- Copy as plain text (email-ready)
- Download as PDF
- Save quote (V1+)

---

### 3C. Input Strategy Summary

**Core Intake (Always Required): 15 fields**
1. Client Name
2. Client Email
3. Property Name/Address
4. Floor Area (m²)
5. Number of Floors
6. Number of Bedrooms
7. Number of External Doors
8. Number of Bedroom Doors
9. Number of Electrical Panels
10. Number of Water Supply Points
11. Number of Bedside Outlets
12. Number of Bedroom Windows
13. Number of Bedroom Mirrors
14. Selected Tier
15. Project Date

**Conditional Fields (Tier-Dependent): Up to 8 additional**
- Interior Doors (Essential+)
- Living Spaces count (Essential Plus)
- Living Windows (Essential Plus)
- Living Mirrors (Essential Plus)
- Living Outlets (Essential Plus)
- TVs/Appliances (Essential Plus)
- Wifi Routers (Essential+ add-on)
- Add-on selections

---

## 4. Data Model and Logic Mapping

### 4A. Conceptual Schema

```
┌─────────────────────────────────────────────────────────────────────┐
│                         DATA MODEL                                   │
├─────────────────────────────────────────────────────────────────────┤

ENTITY: Client
├── client_id (auto-generated)
├── name (string, required)
├── email (string, required)
├── phone (string, optional)
└── created_date (date)

ENTITY: Property
├── property_id (auto-generated)
├── client_id (foreign key)
├── name (string, required)
├── address (string, optional)
├── floor_area_sqm (number, required)
├── floor_area_sqft (calculated)
├── num_floors (integer, required, default: 1)
├── num_bedrooms (integer, required)
├── num_living_spaces (integer, optional)
├── num_bathrooms (integer, optional)
├── num_external_doors (integer, required)
├── num_bedroom_doors (integer, required)
├── num_interior_doors (integer, conditional)
├── num_electrical_panels (integer, required, default: 1)
├── num_water_supply_points (integer, required, default: 1)
├── num_wifi_routers (integer, optional)
├── num_tvs_large_appliances (integer, optional)
├── num_bedside_outlets (integer, required)
├── num_living_area_outlets (integer, optional)
├── num_bedroom_windows (integer, required)
├── num_living_windows (integer, optional)
├── num_bedroom_mirrors (integer, optional)
└── num_living_mirrors (integer, optional)

ENTITY: Quote
├── quote_id (auto-generated)
├── quote_number (display format: "BG-2024-001")
├── client_id (foreign key)
├── property_id (foreign key)
├── selected_tier (enum: Intro | Essential | Essential Plus)
├── selected_addons (array of addon_ids)
├── status (enum: Draft | Ready | Sent | Accepted)
├── created_date (date)
├── valid_until (date, default: +30 days)
├── notes (text, optional)
├── assumptions (text, optional)
└── line_items (array of LineItem)

ENTITY: LineItem
├── line_item_id (auto-generated)
├── quote_id (foreign key)
├── item_code (string, references catalog)
├── item_name (string)
├── description (string)
├── category (enum: Base | Mandatory | Optional | Informational)
├── quantity (number)
├── unit (string: "pair", "unit", "each", "per floor")
├── unit_price (number, nullable until prices defined)
├── line_total (calculated)
├── is_included_in_tier (boolean)
├── rule_source (string, which rule generated this)
└── notes (string, optional)

ENTITY: PricingConfig
├── config_version (string)
├── effective_date (date)
├── tier_base_prices (object)
│   ├── Intro (number)
│   ├── Essential (number)
│   └── Essential Plus (number)
├── item_unit_prices (object, keyed by item_code)
├── modifiers (object)
│   ├── complexity_multiplier (number)
│   ├── travel_per_km (number)
│   └── visit_rate (number)
├── minimums (object)
│   ├── minimum_quote (number)
│   └── minimum_travel_fee (number)
└── tax_rate (number, optional)

ENTITY: ProposalTemplate
├── template_id (string)
├── template_name (string)
├── sections (array of Section)
│   ├── header
│   ├── scope_summary
│   ├── process_timeline
│   ├── pricing_table
│   ├── assumptions
│   ├── next_steps
│   └── about (optional)
└── styling (object)

```

### 4B. Logic Mapping: Inputs → Rules → Line Items

```
INPUT FLOW:
─────────────────────────────────────────────────────────────────────

[Property.floor_area_sqm] + [Property.num_floors] + [Quote.selected_tier]
    │
    ▼
    RULE: BG28 Ring Calculation
    │
    ▼
    LineItem: {
        item_code: "BG28_RING_PAIR",
        quantity: calculated_qty,
        rule_source: "BG28_RING_RULE"
    }

─────────────────────────────────────────────────────────────────────

[Property.num_external_doors] + [Property.num_bedroom_doors] +
[Property.num_interior_doors] + [Quote.selected_tier]
    │
    ▼
    RULE: Doorway Disc Calculation
    │
    ▼
    LineItem: {
        item_code: "DOORWAY_DISC",
        quantity: calculated_qty,
        rule_source: "DOORWAY_DISC_RULE"
    }

─────────────────────────────────────────────────────────────────────

[Quote.selected_tier] + [Quote.selected_addons]
    │
    ▼
    RULE: Addon Eligibility Check
    │
    ├── IF addon not available for tier
    │   └── Display error, prevent selection
    │
    └── IF addon available and selected
        └── Create LineItem with category: "Optional"

─────────────────────────────────────────────────────────────────────
```

### 4C. Calculation Pipeline

```
PIPELINE SEQUENCE:
─────────────────────────────────────────────────────────────────────

1. VALIDATE INPUTS
   └── Check required fields present
   └── Check value ranges
   └── Check tier-specific requirements

2. DETERMINE TIER INCLUSIONS
   └── Load tier definition
   └── Mark included items as "Mandatory"
   └── Mark available add-ons as "Optional"

3. CALCULATE QUANTITIES
   For each included/selected item:
   └── Apply quantity rule
   └── Store quantity on LineItem

4. APPLY PRICING (when prices defined)
   For each LineItem:
   └── Look up unit_price from PricingConfig
   └── Calculate line_total = quantity × unit_price

5. CALCULATE TOTALS
   └── Sum Mandatory items → tier_base_total
   └── Sum Optional items → addons_total
   └── Apply modifiers (travel, complexity)
   └── Calculate grand_total

6. GENERATE PROPOSAL
   └── Populate ProposalTemplate with Quote data
   └── Format for output mode (text/PDF)
```

---

## 5. Pricing System and Checklist

### 5A. Pricing Primitives

#### Structure Overview

```
PRICING ARCHITECTURE:
─────────────────────────────────────────────────────────────────────

TOTAL QUOTE =
    Tier Base Price
  + Per-Unit Items (quantity × unit price)
  + Selected Add-Ons
  + Travel/Logistics
  + Complexity Adjustment (if applicable)
  + Contingency (optional)
  + Tax (if applicable)

─────────────────────────────────────────────────────────────────────
```

#### Tier Base Prices

| Tier | Base Price Variable | Description |
|------|---------------------|-------------|
| Intro | `PRICE_BASE_INTRO` | Base fee for Intro tier |
| Essential | `PRICE_BASE_ESSENTIAL` | Base fee for Essential tier |
| Essential Plus | `PRICE_BASE_ESSENTIAL_PLUS` | Base fee for Essential Plus tier |

**Note:** Base prices may include a certain "standard" property size. Pricing can be structured as:
- Option A: Flat base + all per-unit items priced separately
- Option B: Base includes "typical" property, with per-unit charges only for excess
- Option C: Fully per-unit (no base fee)

*Decision required: Which pricing model?*

#### Per-Unit Pricing Items

| Item Code | Item Name | Unit | Price Variable |
|-----------|-----------|------|----------------|
| BG28_RING_PAIR | BG28 Ring BG3 Center (Pair) | pair | `PRICE_BG28_RING` |
| DOORWAY_DISC | Doorway Disc + Strip Sticker | each | `PRICE_DOORWAY_DISC` |
| SPACE_HARMONIZER | BG3 Center Space Harmonizer | each | `PRICE_SPACE_HARMONIZER` |
| CUBIC_DISC_CENTER | BG-EHS Cubic Disc BG3 Center | each | `PRICE_CUBIC_DISC_CENTER` |
| EARTH_GRID_DISC | Earth Gridlines Disc | each | `PRICE_EARTH_GRID_DISC` |
| WATER_STRIP | Water Supply Numerical Strip #11 | each | `PRICE_WATER_STRIP` |
| ELEC_PANEL_KIT | Electrical Panel Solution Kit | each | `PRICE_ELEC_PANEL` |
| L66_OUTLET | L66 Solution per Outlet | each | `PRICE_L66` |
| L_WIFI | L-Wifi Solution | each | `PRICE_L_WIFI` |
| CUBIC_DISC_TV | Cubic Disc for TVs/Appliances | each | `PRICE_CUBIC_DISC_TV` |
| L_WINDOW | L Solution per Window | each | `PRICE_L_WINDOW` |
| L90_MIRROR | L90 Solution per Mirror | each | `PRICE_L90_MIRROR` |

#### Modifiers

| Modifier | Variable | Application |
|----------|----------|-------------|
| Complexity Multiplier | `MOD_COMPLEXITY` | Multiply subtotal (default: 1.0) |
| Travel Per KM | `MOD_TRAVEL_KM` | Add: distance × rate |
| Visit/Time Rate | `MOD_VISIT_RATE` | If charging by visit/time |
| Volume Discount | `MOD_VOLUME_DISCOUNT` | Reduce for large properties |

#### Minimums and Caps

| Guardrail | Variable | Purpose |
|-----------|----------|---------|
| Minimum Quote Total | `MIN_QUOTE_TOTAL` | Floor for any quote |
| Minimum Travel Fee | `MIN_TRAVEL_FEE` | Flat minimum for travel |
| Max Standard Property Size | `MAX_STANDARD_SIZE` | Triggers "custom quote" above |
| Max Items Per Category | various | Sanity check limits |

---

### 5B. Pricing Questions Checklist

**YOU MUST DEFINE THE FOLLOWING PRICES AND ASSUMPTIONS:**

#### Category 1: Tier Base Pricing

- [ ] **Q1.1:** What is the base price for Intro tier? `PRICE_BASE_INTRO = $____`
- [ ] **Q1.2:** What is the base price for Essential tier? `PRICE_BASE_ESSENTIAL = $____`
- [ ] **Q1.3:** What is the base price for Essential Plus tier? `PRICE_BASE_ESSENTIAL_PLUS = $____`
- [ ] **Q1.4:** Do base prices include a "standard" property size, or are all items priced per-unit on top of base?
- [ ] **Q1.5:** If base includes standard size, what is it? (e.g., "up to 100m², 2 bedrooms")

#### Category 2: Material/Item Unit Prices

- [ ] **Q2.1:** BG28 Ring Pair price? `PRICE_BG28_RING = $____/pair`
- [ ] **Q2.2:** Doorway Disc (D-Disc + #7 Strip) price? `PRICE_DOORWAY_DISC = $____/door`
- [ ] **Q2.3:** BG3 Center Space Harmonizer price? `PRICE_SPACE_HARMONIZER = $____/unit`
- [ ] **Q2.4:** BG-EHS Cubic Disc BG3 Center price? `PRICE_CUBIC_DISC_CENTER = $____/unit`
- [ ] **Q2.5:** Earth Gridlines Disc price? `PRICE_EARTH_GRID_DISC = $____/disc`
- [ ] **Q2.6:** Water Supply Numerical Strip #11 price? `PRICE_WATER_STRIP = $____/unit`
- [ ] **Q2.7:** Electrical Panel Solution Kit price? `PRICE_ELEC_PANEL = $____/panel`
- [ ] **Q2.8:** L66 Solution price? `PRICE_L66 = $____/outlet`
- [ ] **Q2.9:** L-Wifi Solution price? `PRICE_L_WIFI = $____/router`
- [ ] **Q2.10:** Cubic Disc for TVs/Appliances price? `PRICE_CUBIC_DISC_TV = $____/unit`
- [ ] **Q2.11:** L Solution (Windows) price? `PRICE_L_WINDOW = $____/window`
- [ ] **Q2.12:** L90 Solution (Mirrors) price? `PRICE_L90_MIRROR = $____/mirror`

#### Category 3: Labor/Service Pricing

- [ ] **Q3.1:** Is labor included in item prices, or charged separately?
- [ ] **Q3.2:** If separate, what is the hourly/visit rate? `RATE_LABOR = $____/hour or visit`
- [ ] **Q3.3:** How many visits are typically needed per tier?
  - Intro: ____ visits
  - Essential: ____ visits
  - Essential Plus: ____ visits
- [ ] **Q3.4:** Is there a consultation fee separate from implementation?

#### Category 4: Travel/Logistics

- [ ] **Q4.1:** Do you charge for travel? Yes / No
- [ ] **Q4.2:** If yes, what is the rate? `MOD_TRAVEL_KM = $____/km`
- [ ] **Q4.3:** Is there a minimum travel fee? `MIN_TRAVEL_FEE = $____`
- [ ] **Q4.4:** Is there a "local" radius with no travel charge? ____ km
- [ ] **Q4.5:** Do you charge for accommodation for distant properties?

#### Category 5: Complexity and Adjustments

- [ ] **Q5.1:** What factors make a property "complex"? (List factors)
- [ ] **Q5.2:** What is the complexity multiplier? `MOD_COMPLEXITY = ____×` (e.g., 1.2 for +20%)
- [ ] **Q5.3:** Do you offer volume discounts for large properties? At what threshold?
- [ ] **Q5.4:** Do you add contingency to quotes? What percentage?

#### Category 6: Minimums and Caps

- [ ] **Q6.1:** What is your minimum quote total? `MIN_QUOTE_TOTAL = $____`
- [ ] **Q6.2:** Above what property size should the system flag "Custom quote required"? `MAX_STANDARD_SIZE = ____m²`
- [ ] **Q6.3:** Above what number of items should the system flag for review?

#### Category 7: Taxes and Payment

- [ ] **Q7.1:** Do you charge sales tax/VAT? Yes / No
- [ ] **Q7.2:** If yes, what rate? `TAX_RATE = ____%`
- [ ] **Q7.3:** What payment terms do you offer? (e.g., "50% deposit, balance on completion")
- [ ] **Q7.4:** What is quote validity period? ____ days

#### Category 8: Policies

- [ ] **Q8.1:** Do you offer revisions? How many included?
- [ ] **Q8.2:** What is your cancellation policy?
- [ ] **Q8.3:** Do material prices include shipping, or charged separately?
- [ ] **Q8.4:** Are there any seasonal or promotional pricing considerations?

---

### 5C. Defaults and Guardrails

#### Recommended Default Assumptions (Placeholders)

*These are suggested defaults to allow the system to function. Replace with your actual values.*

| Setting | Default Value | Rationale |
|---------|---------------|-----------|
| Standard property size (included in base) | 100m², 2 bedrooms, 1 floor | Typical small residential |
| Quote validity | 30 days | Industry standard |
| Complexity multiplier | 1.0 (no adjustment) | Apply only when flagged |
| Local travel radius (no charge) | 25 km | Reasonable local area |
| Tax rate | 0% | Add if applicable |
| Number of visits (Intro) | 1 visit | Minimal scope |
| Number of visits (Essential) | 2 visits | Standard scope |
| Number of visits (Essential Plus) | 2-3 visits | Expanded scope |

#### Guardrails and Triggers

| Condition | Action |
|-----------|--------|
| Property > 500m² | Display: "Large property — verify pricing" |
| Property > 1,000m² | Display: "Custom quote required" |
| Bedrooms > 10 | Display: "Custom quote required" |
| Total line items > 50 | Display: "Complex project — review recommended" |
| Total quote < minimum | Apply minimum quote total |
| Missing required inputs | Block quote generation, show errors |
| Tier = Intro but client wants space harmonizer | Suggest upgrade to Essential |

---

## 6. Quote Engine Logic

### 6A. Line-Item Catalog

#### Base Tier Packages

| Item Code | Name | Included In | Category |
|-----------|------|-------------|----------|
| `PKG_INTRO` | Intro Tier Base Package | Intro | Base |
| `PKG_ESSENTIAL` | Essential Tier Base Package | Essential | Base |
| `PKG_ESSENTIAL_PLUS` | Essential Plus Tier Base Package | Essential Plus | Base |

#### Per-Unit Mandatory Items (by tier)

| Item Code | Name | Intro | Essential | Essential Plus | Unit |
|-----------|------|-------|-----------|----------------|------|
| `BG28_RING_PAIR` | BG28 Ring Solution (Pair) | ✓ (1/100m²) | ✓ (1/50m²) | ✓ (1/50m²) | pair/floor |
| `DOORWAY_DISC` | Doorway Disc Solution | ✓ (ext+bed) | ✓ (all) | ✓ (all) | each |
| `SPACE_HARMONIZER` | Space Harmonizer | — | ✓ | ✓ | each/floor |
| `CUBIC_DISC_CENTER` | Cubic Disc BG3 Center | — | ✓ | ✓ | each/floor |
| `EARTH_GRID_BED` | Earth Gridlines (Bedrooms) | — | ✓ | ✓ | set/bedroom |
| `WATER_STRIP` | Water Supply Solution | ✓ | ✓ | ✓ | each |
| `ELEC_PANEL_KIT` | Electrical Panel Solution | ✓ | ✓ | ✓ | each |
| `L66_BEDSIDE` | L66 Bedside Outlets | ✓ | ✓ | ✓ | each |
| `L_WINDOW_BED` | L Solution Bedroom Windows | ✓ | ✓ | ✓ | each |
| `L90_MIRROR_BED` | L90 Solution Bedroom Mirrors | ✓ | Add-on | Add-on | each |

#### Optional Add-On Items

| Item Code | Name | Essential | Essential Plus | Unit |
|-----------|------|-----------|----------------|------|
| `ADDON_L_WIFI` | L-Wifi Solution | Available | Available | each |
| `ADDON_MIRROR_BED` | Bedroom Mirrors | Available | Available | each |
| `ADDON_EARTH_GRID_LIVING` | Earth Gridlines (Living Spaces) | — | Available | set/room |
| `ADDON_EARTH_GRID_FULL` | Earth Gridlines (Full Coverage) | — | Available | set/room |
| `ADDON_CUBIC_DISC_TV` | Cubic Disc TVs/Appliances | — | Available | each |
| `ADDON_L66_LIVING` | L66 Living Area Outlets | — | Available | each |
| `ADDON_L_WINDOW_LIVING` | L Solution Living Windows | — | Available | each |
| `ADDON_L90_MIRROR_LIVING` | L90 Solution Living Mirrors | — | Available | each |

#### Informational Line Items (Non-Priced)

| Item Code | Name | Purpose |
|-----------|------|---------|
| `INFO_ASSUMPTIONS` | Quote Assumptions | Display assumptions |
| `INFO_VALIDITY` | Quote Validity | Show expiration |
| `INFO_PAYMENT_TERMS` | Payment Terms | Display terms |
| `INFO_NEXT_STEPS` | Next Steps | Action items |

---

### 6B. Rule-Driven Generation Logic

#### Decision Tree for Line Items

```
FOR each potential line item in catalog:
│
├── IS item mandatory for selected tier?
│   ├── YES → Add to quote with calculated quantity
│   └── NO → Continue
│
├── IS item an available add-on for selected tier?
│   ├── YES → Is add-on selected by user?
│   │   ├── YES → Add to quote with calculated quantity
│   │   └── NO → Skip (show in "available add-ons" section)
│   └── NO → Skip (not available for tier)
│
└── IS item informational?
    └── YES → Add to quote (no price)
```

#### Quantity Calculation Rules

```python
# Pseudocode for quantity calculations

def calculate_bg28_ring_qty(tier, floor_area_sqm, num_floors):
    if tier == "Intro":
        coverage_per_pair = 100  # m²
    else:
        coverage_per_pair = 50  # m²

    pairs_per_floor = ceil(floor_area_sqm / coverage_per_pair)
    return pairs_per_floor * num_floors

def calculate_doorway_disc_qty(tier, ext_doors, bed_doors, int_doors):
    if tier == "Intro":
        return ext_doors + bed_doors
    else:
        return ext_doors + bed_doors + int_doors

def calculate_space_harmonizer_qty(tier, floor_area_sqm, num_floors):
    if tier == "Intro":
        return 0
    else:
        return ceil(floor_area_sqm / 200) * num_floors

def calculate_cubic_disc_center_qty(tier, floor_area_sqm, num_floors):
    if tier == "Intro":
        return 0
    else:
        return ceil(floor_area_sqm / 75) * num_floors

def calculate_earth_grid_qty(tier, num_bedrooms, addon_living, num_living):
    if tier == "Intro":
        return 0

    bedroom_sets = num_bedrooms * 2  # H/B + Curry per room

    if addon_living and tier == "Essential Plus":
        living_sets = num_living * 2
        return bedroom_sets + living_sets

    return bedroom_sets
```

#### Note Attachment Rules

```
IF calculated_qty > typical_qty:
    attach_note = "Quantity reflects larger than typical property size"

IF tier = Intro AND excluded_feature requested:
    attach_note = "This feature requires Essential tier or higher"

IF addon selected AND requires_additional_input missing:
    attach_note = "Please provide [missing field] to complete this line item"

IF property_size > MAX_STANDARD_SIZE:
    attach_note = "Large property — pricing subject to verification"
```

---

### 6C. Readiness Signals

#### Status Indicators

| Status | Criteria | Display |
|--------|----------|---------|
| **Ready to Send** | All required inputs provided, all calculations complete, prices defined | Green checkmark |
| **Missing Required Inputs** | One or more required fields empty | Red warning with list |
| **Prices Not Defined** | Calculations complete but pricing config incomplete | Yellow warning |
| **Estimate Only** | Property exceeds standard size or complexity | Orange notice |
| **Custom Quote Required** | Exceeds system limits | Red block |

#### Validation Checklist (Generated per Quote)

```
QUOTE VALIDATION:
────────────────────────────────────────
[✓] Client information complete
[✓] Property details provided
[✓] Tier selected
[✓] All tier-required inputs provided
[✓] Add-on inputs complete (if applicable)
[ ] All prices defined ← BLOCKING if missing
[✓] Quantities within normal ranges
[✓] No conflicting selections
────────────────────────────────────────
STATUS: Ready to Send / Missing: [list]
```

---

## 7. Proposal Template Design

### 7A. Proposal Structure

```
┌─────────────────────────────────────────────────────────────────────┐
│                       PROPOSAL STRUCTURE                             │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  1. HEADER                                                           │
│     ├── Your business name/logo                                      │
│     ├── Proposal title                                               │
│     ├── Quote number and date                                        │
│     ├── Client name                                                  │
│     ├── Property name/address                                        │
│     └── Valid until date                                             │
│                                                                      │
│  2. TIER SUMMARY & SCOPE                                             │
│     ├── Selected tier name                                           │
│     ├── Brief description of what's included                         │
│     ├── Property specifications summary                              │
│     └── Key deliverables list                                        │
│                                                                      │
│  3. DETAILED SCOPE OF WORK                                           │
│     ├── BG28 Ring Solutions                                          │
│     ├── Doorway Protection                                           │
│     ├── Space Harmonization (if applicable)                          │
│     ├── Earth Gridline Solutions (if applicable)                     │
│     ├── Water Supply Solutions                                       │
│     ├── Electrical Solutions                                         │
│     ├── Window & Mirror Solutions                                    │
│     └── Selected Add-Ons (if any)                                    │
│                                                                      │
│  4. PROCESS & TIMELINE                                               │
│     ├── Step 1: Acceptance & scheduling                              │
│     ├── Step 2: Site preparation (client responsibilities)           │
│     ├── Step 3: Installation visit(s)                                │
│     ├── Step 4: Completion & walkthrough                             │
│     └── Estimated timeline                                           │
│                                                                      │
│  5. PRICING TABLE                                                    │
│     ├── Line items with quantities and prices                        │
│     ├── Subtotal                                                     │
│     ├── Add-ons subtotal (if any)                                    │
│     ├── Travel/logistics (if applicable)                             │
│     ├── Tax (if applicable)                                          │
│     └── TOTAL                                                        │
│                                                                      │
│  6. ASSUMPTIONS & CLIENT RESPONSIBILITIES                            │
│     ├── What client needs to provide/prepare                         │
│     ├── Access requirements                                          │
│     ├── What's NOT included                                          │
│     └── Conditions and limitations                                   │
│                                                                      │
│  7. TERMS & CONDITIONS                                               │
│     ├── Payment terms                                                │
│     ├── Validity period                                              │
│     ├── Cancellation policy                                          │
│     └── Warranty/guarantee (if any)                                  │
│                                                                      │
│  8. NEXT STEPS / ACCEPTANCE                                          │
│     ├── How to accept                                                │
│     ├── Contact information                                          │
│     └── Call to action                                               │
│                                                                      │
│  9. ABOUT (OPTIONAL)                                                 │
│     ├── Brief practitioner bio                                       │
│     ├── Credentials                                                  │
│     └── Why BioGeometry                                              │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

---

### 7B. Output Modes

#### Mode 1: Email-Ready Plain Text

**Characteristics:**
- Clean, readable plain text
- No special formatting beyond line breaks
- Copy-paste ready for email body
- Approximately 500-800 words
- Key information prominent

**Example Structure:**

```
BIOGEOMETRY HOME SOLUTIONS PROPOSAL
====================================

Quote #: BG-2024-001
Date: [Date]
Valid Until: [Date + 30 days]

Prepared for: [Client Name]
Property: [Property Address]

SELECTED SERVICE: [Tier Name]
------------------------------------
[Brief description of tier]

YOUR PROPERTY:
- Floor area: [X] m² ([Y] sq ft)
- Floors: [N]
- Bedrooms: [N]

SCOPE OF WORK:
- [Quantity]x BG28 Ring Solutions
- [Quantity]x Doorway Disc Solutions
- [Additional items...]

INVESTMENT:
------------------------------------
[Tier] Base Package          $[Price]
[Line item]      [Qty]       $[Price]
[Line item]      [Qty]       $[Price]
------------------------------------
TOTAL                        $[Total]

Payment: [Terms]

NEXT STEPS:
1. Reply to this email to confirm
2. [Additional steps...]

Questions? Contact [Name] at [Email/Phone]

[Signature]
```

#### Mode 2: PDF-Ready Layout (1-3 Pages)

**Page 1: Cover & Summary**
- Header with branding
- Client/property info
- Tier badge/highlight
- Key deliverables summary
- Total investment (prominent)

**Page 2: Detailed Scope & Pricing**
- Itemized scope of work
- Pricing table with line items
- Subtotals and total

**Page 3: Terms & Acceptance**
- Assumptions and responsibilities
- Terms and conditions
- Acceptance section with signature line
- Contact information

**Design Guidelines:**
- Professional, clean layout
- Subtle use of brand colors
- Clear hierarchy
- Readable fonts (11-12pt body)
- Adequate white space
- Tables for structured data

---

### 7C. Tone and Language Guidelines

#### Do Use:
- Clear, professional language
- Technical accuracy for BG-EHS terms
- Confident but not overselling
- Specific quantities and deliverables
- Active voice

**Examples:**
- "This proposal includes installation of 4 BG28 Ring Solution pairs..."
- "The Essential tier provides comprehensive protection for all doorways..."
- "Your investment covers materials, installation, and one follow-up visit."

#### Avoid:
- Mystical or unsubstantiated claims
- Aggressive sales language
- Vague descriptions
- Jargon without explanation
- Overpromising results

**Avoid phrases like:**
- "This will transform your energy..."
- "Amazing results guaranteed..."
- "You won't believe the difference..."

#### Balanced Approach:
The tone should convey expertise and professionalism while remaining grounded. BioGeometry has a specific methodology — reference it accurately without embellishment. Let the scope of work speak for itself.

---

## 8. Roadmap (MVP / V1 / V2)

### 8A. MVP (Minimum Viable Product)

**Goal:** Functional offline quote generator that produces valid proposals for all three tiers.

#### MVP Features

| Feature | Description | Priority |
|---------|-------------|----------|
| Client intake form | Name, email, property address | Required |
| Property input form | All core property fields | Required |
| Tier selection | Intro / Essential / Essential Plus | Required |
| Conditional inputs | Tier-specific additional fields | Required |
| Add-on selection | Available add-ons per tier | Required |
| Quantity calculation | All rules from Section 2B | Required |
| Line item generation | Based on tier and inputs | Required |
| Pricing placeholders | Structure ready, values TBD | Required |
| Quote summary view | Review before export | Required |
| Plain text export | Copy to clipboard | Required |
| Basic validation | Required fields, range checks | Required |

#### MVP Exclusions
- PDF export (use print-to-PDF workaround)
- Saved quotes / history
- Multiple clients
- Advanced validation
- Branding customization

#### MVP Validation Approach
1. Test with 5 real-world scenarios (varying property sizes/tiers)
2. Verify all calculations match manual calculations
3. Test all tier/add-on combinations
4. Confirm proposal text is clear and complete
5. Get feedback from 2-3 test users

#### MVP Risks
| Risk | Mitigation |
|------|------------|
| Rule interpretation errors | Document all assumptions, test thoroughly |
| Missing edge cases | Start with common scenarios, iterate |
| Pricing structure doesn't fit | Design flexible pricing config |
| User confusion | Clear labels, inline help text |

---

### 8B. V1 (Version 1.0)

**Goal:** Production-ready application with persistence and professional output.

#### V1 Features

| Feature | Description | Priority |
|---------|-------------|----------|
| All MVP features | — | Required |
| PDF export | Proper formatted PDF output | High |
| Local storage | Save/load quotes in browser | High |
| Quote history | List of previous quotes | High |
| Client management | Save and reuse client info | Medium |
| Quote duplication | Copy and modify existing quote | High |
| Quote versioning | v1, v2 of same quote | Medium |
| Pricing configuration | UI to set/update prices | High |
| Branding settings | Logo, colors, contact info | Medium |
| Input auto-fill | Smart defaults based on property size | Medium |
| Validation improvements | Real-time validation, better errors | Medium |

#### V1 Validation Approach
1. Use for 10+ real quotes
2. Gather client feedback on proposals
3. Time tracking: measure quote creation time
4. Error tracking: log validation failures
5. A/B test proposal formats if possible

#### V1 Risks
| Risk | Mitigation |
|------|------------|
| Browser storage limits | Implement export/backup |
| PDF rendering issues | Use well-tested library, thorough testing |
| Data loss | Auto-save, export reminders |
| Pricing errors | Pricing preview before save |

---

### 8C. V2 (Version 2.0)

**Goal:** Enhanced productivity and intelligence features.

#### V2 Features

| Feature | Description | Priority |
|---------|-------------|----------|
| All V1 features | — | Required |
| RFP text parsing | Paste RFP text, extract fields | High |
| Property presets | "Typical apartment", "Large home", etc. | Medium |
| Rule explanations | Show why each line item appears | Medium |
| Quote comparison | Compare two quotes side-by-side | Medium |
| Analytics dashboard | Quote count, avg values, conversion | Low |
| Advanced templates | Multiple proposal styles | Medium |
| Email integration | Send directly from app | Low |
| Multi-currency | Support different currencies | Low |
| Offline sync | Sync when online (optional) | Low |
| Import/export | Bulk data management | Medium |

#### V2 Nice-to-Haves
- Voice input for property details
- Photo-based room counting
- Calendar integration for scheduling
- CRM integration

#### V2 Validation Approach
1. Feature usage analytics
2. User interviews for workflow optimization
3. Conversion rate tracking (quotes → accepted)
4. Time-to-quote benchmarking

---

### Roadmap Summary

```
MVP                          V1                           V2
─────────────────────────────────────────────────────────────────────
[Core quote generation]  →   [Persistence + PDF]     →   [Intelligence]

• Client intake              • Local storage              • RFP parsing
• Property inputs            • Quote history              • Presets
• Tier selection             • Client management          • Rule explanations
• Rule calculations          • Duplication                • Comparison
• Line items                 • Versioning                 • Analytics
• Text export                • PDF export                 • Advanced templates
• Basic validation           • Pricing config             • Email integration
                             • Branding
                             • Better validation

Timeline (suggested):
• MVP: 1-2 weeks development
• V1: 2-4 weeks after MVP stable
• V2: Ongoing based on needs
```

---

## 9. Risks, Edge Cases, and Validation Plan

### 9A. Identified Risks

#### Technical Risks

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Browser compatibility | Medium | High | Test on Chrome, Firefox, Safari, Edge |
| Local storage corruption | Low | High | Regular export reminders, backup feature |
| Calculation errors | Medium | High | Comprehensive test suite, manual verification |
| PDF rendering inconsistency | Medium | Medium | Use print-to-PDF fallback, test across browsers |
| Large property edge cases | Medium | Medium | Define clear caps, "custom quote" triggers |

#### Business Risks

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Pricing structure changes | Medium | Medium | Flexible pricing config, easy updates |
| Tier definition changes | Low | High | Modular rule system, documented assumptions |
| Scope creep | High | Medium | Strict MVP definition, phased approach |
| User adoption | Medium | High | Involve users early, iterative feedback |

#### Data Risks

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Sensitive client data | Medium | High | Local-only storage, no external transmission |
| Data loss | Medium | High | Export functionality, auto-save |
| Incorrect quotes sent | Medium | High | Review screen before export, validation |

---

### 9B. Edge Cases

#### Property Edge Cases

| Case | Expected Behavior |
|------|-------------------|
| Very small property (<30m²) | Calculate normally, may hit minimum quote |
| Very large property (>1000m²) | Flag "Custom quote required" |
| Single room (studio) | Bedrooms = 0 allowed? Clarify |
| Multi-building property | Sum all buildings? Separate quotes? |
| Property with no interior doors | Allow 0, skip interior door line item |
| 0 bedroom windows | Allow 0, skip window line item |

#### Tier Edge Cases

| Case | Expected Behavior |
|------|-------------------|
| Intro with space harmonizer request | Suggest upgrade to Essential |
| Essential Plus with no add-ons selected | Valid quote, just base Essential Plus |
| Switching tier mid-quote | Recalculate all, clear incompatible add-ons |

#### Calculation Edge Cases

| Case | Expected Behavior |
|------|-------------------|
| Floor area not evenly divisible | Always round UP (ceiling function) |
| 0 quantity calculated | Omit line item from quote |
| Negative values entered | Validation error, reject |
| Non-integer where integer required | Round to nearest integer |

#### Pricing Edge Cases

| Case | Expected Behavior |
|------|-------------------|
| No prices defined | Show quantities, mark "Prices TBD" |
| Partial prices defined | Show what's available, flag missing |
| Quote below minimum | Apply minimum, show note |
| Free add-on (price = 0) | Show in quote with $0 |

---

### 9C. Validation Plan

#### Unit Testing (Logic Validation)

| Test Category | Test Cases |
|---------------|------------|
| BG28 Ring calculation | 50m², 100m², 150m², 500m² for each tier |
| Doorway calculation | Various door combinations per tier |
| Space Harmonizer | 0 for Intro, calculated for others |
| Earth Gridlines | Bedroom only, living only, full coverage |
| Add-on availability | Verify correct add-ons per tier |
| Quantity edge cases | 0, very large, boundary values |

#### Integration Testing (Flow Validation)

| Test Scenario | Steps | Expected Outcome |
|---------------|-------|------------------|
| Complete Intro quote | Full flow with Intro tier | Valid quote generated |
| Complete Essential quote | Full flow with add-ons | Valid quote with add-ons |
| Complete Essential Plus quote | Full flow with all add-ons | Valid quote with all items |
| Edit and recalculate | Change inputs mid-flow | Quantities update correctly |
| Missing required field | Skip a required field | Validation error shown |
| Export plain text | Generate and copy | Properly formatted text |

#### User Acceptance Testing

| Test | Participants | Success Criteria |
|------|--------------|------------------|
| Quote creation time | 3 users | < 5 minutes for standard property |
| Accuracy check | Compare to manual | 100% calculation match |
| Proposal clarity | 3 clients | Understand scope and pricing |
| Error recovery | 3 users | Can fix mistakes without data loss |

#### Regression Testing

After any change:
1. Run all unit tests
2. Create one quote per tier
3. Verify PDF/text output
4. Check edge case handling

---

### 9D. Open Questions for Resolution

Before development, clarify:

1. **P3 BG3 Center Baseplate:** Is this available for Associate Practitioners? Currently excluded.
2. **Intro bedroom mirrors:** Image shows ✓ but Essential shows "Add-on ✓" — is Intro different?
3. **Studio apartments:** How to handle 0-bedroom properties?
4. **Multiple floors with different sizes:** Sum total, or calculate per-floor?
5. **L-Wifi for Intro:** Explicitly not available, or just not marked?
6. **Add-on vs. included logic:** For "Add-on ✓" items, are they automatically included or must be selected?

---

## Appendix A: Glossary

| Term | Definition |
|------|------------|
| BG28 Ring | A BioGeometry energy balancing ring placed at gridline intersections |
| BG3 Center | A central harmonizing element |
| D-Disc | Doorway protection disc |
| H/B Gridlines | Hartmann/Benker geomagnetic gridlines |
| Curry Gridlines | Curry geomagnetic gridlines |
| Space Harmonizer | A device for harmonizing larger spaces |
| Cubic Disc | A cube-shaped protective element |
| L-Solution | Linear protective element |
| L66 | Specific BG3 solution for electrical outlets |
| L90 | Specific BG3 solution for mirrors |
| SGFuse | BioGeometry solution for electrical systems |
| P3 | Designation for specific BioGeometry product line |

---

## Appendix B: Document Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2024-XX-XX | [Your name] | Initial strategic roadmap |

---

*End of Strategic Roadmap Document*
