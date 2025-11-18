# Wood Routing

## 1. Introduction to Wood Routing

> **Wood Routing** is a subtractive manufacturing process used in woodworking to hollow out, shape, or profile an area in a piece of wood. The process is performed by a high-speed rotating tool called a **router**. The router bit, guided by hand or by a computer-controlled system, cuts away wood to create features like decorative edges, grooves, joints, and intricate patterns.

The two primary methods of routing are:
- **Manual Routing:** A woodworker guides a handheld or table-mounted router to perform cuts. This method relies on the operator's skill and the use of jigs or templates for accuracy.
- **CNC Routing:** A **Computer Numerical Control (CNC)** router uses a computer to control the motion and speed of the router bit with high precision. The machine follows a programmed path based on a digital design file, enabling the creation of complex, repeatable, and highly accurate parts.

## 2. Types of Wood Routers

| Type | Description | Common Uses |
| :--- | :--- | :--- |
| **Handheld Router** | A portable tool guided by the operator. Can have a fixed base (bit depth is set once) or a plunge base (bit can be plunged into the material mid-cut). | Edge profiling, trimming, cutting small grooves (dadoes), freehand carving. |
| **Table-Mounted Router** | A router mounted upside-down in a router table. The wood is guided against the router bit, which protrudes from the table surface. | Creating consistent edge profiles, joinery (like dovetails with a jig), raising panels for doors. |
| **CNC Wood Router** | A computer-controlled machine with a gantry that moves a router spindle along the X, Y, and Z axes. | Complex 2D and 3D carving, cabinet making, sign making, prototyping, mass production of identical parts. |

## 3. History of Wood Routing

| Year / Period | Development Milestone |
| :--- | :--- |
| **Late 1800s** | Early manual routing tools and spindle moulders (shapers) were developed for industrial use in furniture factories. |
| **1915** | The portable electric router was invented by R.L. Carter in Syracuse, New York. This marked the beginning of modern, versatile routing. |
| **1920s-1940s** | Companies like Onsrud Machine Works developed high-speed "air routers" for the aircraft industry, further advancing cutting technology. |
| **1950s** | CNC (Computer Numerical Control) technology was first developed at MIT, laying the groundwork for automated machining. |
| **1970s-1980s** | CNC technology became more affordable and was integrated with routing machines, leading to the first commercial CNC routers for wood. |
| **1990s-Present** | Personal computers and user-friendly CAD/CAM software made CNC routers accessible to small shops, hobbyists, and schools, leading to widespread adoption. |

## 4. 3D Modeling and CAM Software for Wood Routing

For CNC wood routing, a digital workflow involving both **CAD** and **CAM** software is essential.
- **CAD (Computer-Aided Design):** Software used to create the 2D or 3D digital model of the part to be cut.
- **CAM (Computer-Aided Manufacturing):** Software that takes the CAD model and generates **toolpaths**—the specific path the router bit will follow. It also calculates speed, feed rate, and other cutting parameters.

### Popular Software for Wood Routing

| Software | Category | Use |
| :--- | :--- | :--- |
| **Vectric Aspire / VCarve Pro** | CAD/CAM Suite | Industry standard for sign making, decorative carving, and general woodworking. Excellent for converting 2D designs into 3D toolpaths. |
| **Autodesk Fusion 360** | CAD/CAM Suite | A powerful, integrated platform for 3D modeling, simulation, and generating complex CAM toolpaths for 2.5D and 3D carving. |
| **SolidWorks** | 3D CAD | Professional-grade software for designing complex mechanical parts and assemblies. Often paired with a CAM add-on like SolidWorks CAM. |
| **SketchUp** | 3D Modeling | Intuitive and popular for architectural and furniture design. Can be used with a CAM plugin to generate toolpaths. |
| **Rhino / Grasshopper** | 3D Modeling | Advanced software for creating complex, freeform surfaces, often used in artistic and architectural woodworking. |
| **Inkscape / Adobe Illustrator** | 2D Vector Design | Used to create 2D vector paths (in SVG or DXF format) that can be imported into CAM software for engraving or cutting profiles. |

## 5. Creation of Compatible File Formats (The CAD-to-G-code Workflow)

The process of turning a digital idea into a physically routed part follows a clear workflow, with specific file formats used at each stage.

**Step-by-Step Process:**
1.  **Step 1: Design Creation (CAD):** Create a 2D or 3D model of the final part using CAD software. For 2D cutting, this will be a vector path. For 3D carving, it will be a solid model.
2.  **Step 2: Export Design in a CAM-Compatible Format:** Save or export the design as a vector or mesh file that CAM software can read. Common formats include **DXF, SVG, STEP, or IGES**.
3.  **Step 3: Toolpath Generation (CAM):** Import the design file into CAM software. Here, you define the operations:
    -   Select the router bits (e.g., end mill, ball nose, v-bit).
    -   Set cutting parameters (spindle speed, feed rate, depth of cut).
    -   Generate the toolpaths (e.g., profile cuts, pocket clearing, 3D carving).
4.  **Step 4: Post-Processing to G-code:** The CAM software uses a "post-processor" specific to your CNC machine to translate the toolpaths into **G-code**, the instruction language the machine understands.
5.  **Step 5: Execute on CNC Machine:** Load the G-code file into the CNC control software (e.g., Mach3, GRBL, LinuxCNC), set up the wood stock, and run the program.

### Common File Formats for Wood Routing

| File Format | Description | Usage |
| :--- | :--- | :--- |
| **DXF (Drawing Exchange Format)** | A 2D vector format developed by Autodesk. It is a universal standard for sharing 2D geometry. | Importing 2D cutting paths into CAM software. |
| **SVG (Scalable Vector Graphics)** | An open-source 2D vector format. Widely used in graphic design and by hobbyist CNC machines. | Importing 2D cutting and engraving paths. |
| **STEP / IGES** | 3D model formats that store precise surface and solid geometry. | Transferring 3D models from one CAD/CAM system to another without losing data. |
| **G-code (.nc, .tap, .gcode)** | The machine instruction language. It contains a series of coordinates and commands that tell the CNC machine exactly how to move. | The final file that is sent to the CNC router to execute the job. |