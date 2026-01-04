# Metal Forming Processes Flowchart

This flowchart outlines the various metal forming processes as described in the reference documents.

```mermaid
graph TD
    A[Metal Forming] --> B{Temperature};
    B --> C[Cold Working];
    B --> D[Warm Working];
    B --> E[Hot Working];

    A --> F{Process Classification};
    F --> G[Bulk Forming];
    F --> H[Sheet Forming];

    subgraph Bulk Forming
        G --> G1[Rolling];
        G --> G2[Forging];
        G --> G3[Extrusion];
        G --> G4[Drawing];
        G --> G5[Swaging];
    end

    subgraph Sheet Forming
        H --> H1[Spinning];
        H --> H2[Press Working / Die Stamping];
        H --> H3[Deep Drawing];
        H --> H4[Stretch Forming];
    end

    subgraph Rolling Details
        G1 --> R1[Input: Bloom, Slab, Billet];
        R1 --> R2[Output: Rails, Plates, Sheets, Bars, Rods];
    end

    subgraph Forging Details
        G2 --> F1[Open Die Forging];
        G2 --> F2[Impression Die Forging];
        G2 --> F3[Flashless Forging];
        G2 --> F4[Upsetting];
    end

    subgraph Extrusion Details
        G3 --> E_Types{Process Types};
        E_Types --> E1[Direct Extrusion];
        E_Types --> E2[Indirect Extrusion];
        G3 --> E_Temps{Temperature Conditions};
        E_Temps --> E3[Hot Extrusion];
        E_Temps --> E4[Cold Extrusion];
    end

    subgraph Drawing Details
        G4 --> D1[Bar Drawing];
        G4 --> D2[Wire Drawing];
        G4 --> D3[Tube Drawing];
    end
    
    subgraph Press Working / Die Stamping
        H2 --> PW1{Operation Type};
        PW1 --> PWC[Cutting Operations];
        PW1 --> PWF[Forming Operations];
    end

    subgraph Cutting Ops
        PWC --> PWC1[Punching / Blanking];
        PWC --> PWC2[Notching];
        PWC --> PWC3[Perforating];
        PWC --> PWC4[Trimming / Shaving];
        PWC --> PWC5[Nibbling];
        PWC --> PWC6[Lancing];
    end

    subgraph Forming Ops
        PWF --> PWF1[Bending];
        PWF --> PWF2[Embossing];
        PWF --> PWF3[Coining];
        PWF --> PWF4[Flanging];
    end

    subgraph Spinning Details
        H1 --> S1[Hot Spinning];
        H1 --> S2[Cold Spinning];
    end

```

## Detailed Breakdown

### 1. Metal Forming Introduction
- **Based on Temperature**:
    - **Cold Working**:
        - Done at or slightly above room temperature.
        - **Pros**: Good tolerances, surface finish, increased strength.
        - **Cons**: High force required, limited formability due to strain hardening.
    - **Warm Working**:
        - Done between room temperature and recrystallization temperature.
        - **Pros**: Lower forces, enhanced deformation properties.
    - **Hot Working**:
        - Done above the recrystallization temperature.
        - **Pros**: Significant deformation, lower forces, no work hardening.
        - **Cons**: Poor surface finish, lower accuracy, shorter tool life.

### 2. Process Classifications

#### A. Bulk Forming Processes
*(Significant change in shape, small surface-area-to-volume ratio)*

- **Rolling**: Reducing thickness by compressing material between rolls.
    - **Inputs**: Blooms, Slabs, Billets.
- **Forging**: Shaping material by compressing it between dies.
    - **Types**:
        1.  **Open Die**: Material flows freely.
        2.  **Impression Die**: Dies contain a cavity, creating a shape and "flash".
        3.  **Flashless**: Material is fully contained within the die.
        4.  **Upsetting**: Increasing diameter by reducing length (often for heads on bolts/nails).
- **Extrusion**: Pushing material through a die to create a cross-sectional shape.
    - **Process Types**:
        1.  **Direct Extrusion**: Billet is pushed through the die.
        2.  **Indirect Extrusion**: Die moves against the billet, reducing friction.
    - **Temperature Conditions**:
        1.  **Hot Extrusion**: Done above recrystallization temperature to reduce force and increase ductility.
        2.  **Cold Extrusion**: Done at room temperature for stronger products with better finish.
- **Drawing**: Pulling material through a die to reduce its cross-section.
    - **Types**:
        1.  **Bar Drawing**: For large-diameter bars.
        2.  **Wire Drawing**: For small-diameter wire, often continuous through multiple dies.
        3.  **Tube Drawing**: To reduce tube diameter/wall thickness.
- **Swaging**: Reducing the diameter of a tube or rod by repeated radial blows from rotating dies.

#### B. Sheet Forming Processes

- **Deep Drawing**: Forming cup-shaped parts by pushing a sheet metal blank into a die opening with a punch.
- **Press Working (Die Stamping)**: Cutting or forming sheet metal using a press machine with a dedicated punch and die.
    - **Categories**:
        1.  **Cutting Operations** (Stress exceeds shear strength):
            - **Punching/Blanking**: Separating material from a sheet.
            - **Notching**: Cutting from the edge of a sheet.
            - **Perforating**: Punching multiple holes.
            - **Trimming**: Removing excess material.
            - **Shaving**: Improving edge accuracy on a blanked part.
            - **Nibbling**: Cutting contours with a series of overlapping punches.
            - **Lancing**: Simultaneously cutting and bending or forming.
        2.  **Forming Operations** (Stress is below shear strength):
            - **Bending**: Creating bends and angles (e.g., V-bending, edge bending).
            - **Embossing**: Creating raised or recessed designs without changing thickness.
            - **Coining**: High-pressure forming to impart fine details.
            - **Flanging**: Creating a flange or flare.
- **Stretch Forming**: Sheet metal is simultaneously stretched and bent over a die or form block to create large contoured parts.
- **Spinning**: Forming an axisymmetric part by pressing a sheet/plate over a rotating mandrel.
    - **Types**:
        1.  **Hot Spinning**: For thick materials.
        2.  **Cold Spinning**: For thin, soft materials.
