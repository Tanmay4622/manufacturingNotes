# Metal Casting Processes Flowchart

This document provides a structured overview of the metal casting topics covered in the reference PDFs.

```mermaid
graph TD
    A[Metal Casting] --> B[1. Metal Melting & Furnaces];
    A --> C[2. The Casting Cycle];
    A --> D[3. Casting Process Types];
    A --> E[4. Casting Defects];

    subgraph Furnaces
        B --> B1[Furnace Types];
        B1 --> B1a[Cupola, Induction, Electric Arc, etc.];
        B --> B2[Cupola Furnace Details];
        B2 --> B2a[Construction, Zones, Operation];
    end

    subgraph Casting Cycle
        C --> C1[Pattern Making];
        C1 --> C1a[Pattern Types];
        C1 --> C1b[Pattern Allowances];
        C --> C2[Molding];
        C2 --> C2a[Molding Sand Properties];
        C2 --> C2b[Gating System Design];
        C --> C3[Melting & Pouring];
        C --> C4[Solidification];
        C --> C5[Shakeout & Finishing];
    end

    subgraph "Casting Process Types"
        D --> D1[Expendable Mold Casting];
        D1 --> D1a[Sand Casting];
        D1 --> D1b[Investment Casting];
        D1 --> D1c[Shell Molding];
        D1 --> D1d[Lost-Foam Casting];
        D1 --> D1e[Plaster/Ceramic Mold Casting];

        D --> D2[Non-Expendable Mold Casting];
        D2 --> D2a[Pressure Die Casting];
        D2 --> D2b[Permanent Mold (Gravity)];
        D2 --> D2c[Centrifugal Casting];
        D2 --> D2d[Continuous Casting];
    end

    subgraph Casting Defects
        E --> E1[Gas Porosity];
        E --> E2[Shrinkage Defects];
        E --> E3[Pouring Metal Defects];
        E --> E4[Mold Material Defects];
        E --> E5[Shape & Dimensional Defects];
    end
```

## Detailed Breakdown

### 1. Metal Melting & Furnaces
- **Functions**: Melt charge, maintain temperature, refine metal.
- **Types of Furnaces**:
    - **Cupola Furnace**: For cast iron.
    - **Crucible Furnace**: For non-ferrous metals.
    - **Induction Furnace**: For cast iron, steel, non-ferrous.
    - **Electric Arc Furnace**: For high-quality steel.
    - **Rotary Furnace**: For non-ferrous bulk melting.
- **Cupola Furnace Deep Dive**:
    - **Construction**: Shell, Refractory Lining, Tuyeres, Tapping Spouts.
    - **Working Principle**: Counter-current heat exchange.
    - **Zones (Bottom to Top)**: Crucible (Hearth), Combustion, Reducing, Melting, Preheating.

### 2. The Casting Cycle (Focus on Sand Casting)

#### A. Pattern Making
- **Definition**: A replica of the final object used to create the mold cavity.
- **Pattern Types**:
    - Solid / Single-Piece
    - Split / Two-Piece
    - Multi-Piece
    - Match Plate Pattern
    - Gated Pattern
    - Sweep Pattern
    - Skeleton Pattern
    - Loose-Piece Pattern
- **Pattern Allowances** (To compensate for physical effects):
    - **Shrinkage**: For metal contraction during cooling.
    - **Machining**: Extra material on surfaces to be machined.
    - **Draft**: Taper on vertical surfaces for easy pattern withdrawal.
    - **Shake/Rapping**: Accounts for mold enlargement when the pattern is tapped out.
    - **Distortion/Warping**: Pre-distorting the pattern to counteract warping during cooling.

#### B. Molding
- **Basic Terminology**:
    - **Flask**: The box holding the mold (Cope: top, Drag: bottom, Cheek: middle).
    - **Molding Sand**: Material used to create the mold.
    - **Core**: A sand insert to create hollow features in the casting.
    - **Gating System**: Network of channels for molten metal flow (Pouring Basin, Sprue, Runner, Gates, Riser).
- **Molding Sand Properties**:
    - **Thermal**: Refractoriness (heat resistance), Thermal Conductivity.
    - **Mechanical**: Cohesiveness (Green/Dry Strength), Adhesiveness, Flowability.
    - **Processing**: Permeability (gas escape), Collapsibility (disintegrates after solidification), Surface Finish.
- **Special Processes**:
    - **CO2 Moulding**: Hardening a sand mold quickly using CO2 gas and sodium silicate binder.

### 3. Casting Process Types

#### A. Expendable Mold Casting
*(Mold is destroyed after one use)*
- **Sand Casting**: The most common process.
- **Investment Casting (Lost Wax)**: Wax pattern is melted out of a ceramic shell. Excellent for complex shapes and fine detail.
- **Lost-Foam Casting**: Foam pattern is vaporized by molten metal.
- **Shell Molding**: Resin-bonded sand forms a thin, hardened shell mold. Better finish than sand casting.
- **Plaster/Ceramic Mold Casting**: For very smooth finishes.

#### B. Non-Expendable (Permanent) Mold Casting
*(Mold is reused for many cycles)*
- **Pressure Die Casting**: Molten metal is forced into a steel die under high pressure. For high-volume production of non-ferrous parts.
- **Permanent Mold Casting**: Molten metal is poured into a metal mold under gravity.
    - *Includes variations like Slush Casting for hollow objects.*
- **Centrifugal Casting**: Molten metal is poured into a rotating mold, using centrifugal force to shape the part. Ideal for pipes and tubes.
- **Continuous Casting**: Process to solidify molten metal into a semi-finished billet, bloom, or slab.

### 4. Common Casting Defects
- **Gas Porosity**: Trapped gases forming cavities.
    - **Defects**: Blowholes, Pinholes.
- **Shrinkage**: Voids from metal contraction during solidification.
    - **Defects**: Open Shrinkage, Closed Shrinkage (Porosity).
- **Pouring Metal Defects**: Issues with metal flow or temperature.
    - **Defects**: Misruns (incomplete filling), Cold Shuts (streams fail to fuse), Cold Shots (splattered globules).
- **Mold Material Defects**: Caused by mold failure.
    - **Defects**: Cuts/Washes, Swells, Drops, Metal Penetration, Fusion (Burn-on), Scab, Rat tails.
- **Shape & Dimensional Defects**:
    - **Defects**: Mismatch/Shift, Flash/Fins, Warping/Distortion.
- **Solidification & Stress Defects**:
    - **Defects**: Hot Tears (cracks from stress at high temperature).
- **Inclusions**: Foreign particles trapped in the casting (e.g., Slag, dross).
