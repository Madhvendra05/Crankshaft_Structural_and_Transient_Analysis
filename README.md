# Crankshaft_Structural_and_Transient_Analysis
A mechanical CAD and simulation project featuring a piston–crankshaft–connecting rod mechanism. The repository contains the SolidWorks assembly, neutral STEP files for CAD interoperability, and an ANSYS Workbench project for crankshaft analysis.

## Project Overview

The piston–crankshaft mechanism converts the reciprocating motion of the piston into rotary motion at the crankshaft, and vice versa. The connecting rod transfers force between the piston and crankshaft.

### Main files

| File | Description |
|---|---|
| `Assem.SLDASM` | SolidWorks assembly file |
| `crankshaft_assem.STEP` | STEP export of the assembly |
| `piston.stp` | Piston part |
| `piston-pin.stp` | Piston pin / gudgeon pin |
| `conrod.stp` | Connecting rod |
| `conrod-cap.stp` | Connecting-rod cap |
| `crankshaft.stp` | Crankshaft |
| `big-end-bearings.stp` | Big-end bearing components |
| `small-end-bearing.stp` | Small-end bearing component |
| `crankshaft_analysis.wbpj` | ANSYS Workbench project file |
| `crankshaft_analysis_files/` | Supporting ANSYS project and solver files |
| `crankshaft-and-piston-assembly.png` | Assembly preview image |

## Software

- **SolidWorks** — to open and edit the native assembly.
- **ANSYS Workbench / Mechanical** — to open the simulation project and inspect or continue the analysis.
- A STEP-compatible CAD application — to view the exported geometry without SolidWorks.

> **Note:** Simulation results depend on the material properties, contacts, boundary conditions, loads, mesh, and solver settings. Review these settings in ANSYS before relying on any result. The presence of project/result files does not by itself validate the analysis.

## How to open the project

### SolidWorks model
1. Download or clone this repository.
2. Keep the assembly and all referenced part files together in the same project folder structure.
3. Open `Assem.SLDASM` in SolidWorks.
4. If SolidWorks reports missing references, use **Find References** / **Edit References** and point it to the included part files.

### ANSYS analysis
1. Open `crankshaft_analysis.wbpj` from ANSYS Workbench.
2. Keep the `crankshaft_analysis_files` directory beside the `.wbpj` file; do not separate or rename it.
3. Open the relevant Mechanical system and review geometry, materials, contacts, mesh, loads, supports, analysis settings, and solver messages.
4. Re-mesh and solve again if you change inputs or if the saved solution is incomplete.

## Repository contents

```text
piston-crankshaft-conrod-assembl/
├── Assem.SLDASM
├── *.stp
├── crankshaft_assem.STEP
├── crankshaft-and-piston-assembly.png
├── crankshaft_analysis.wbpj
├── crankshaft_analysis_files/
├── images *.png
└── README.md
```

## Uploading to GitHub

See the upload instructions provided with this project or follow the steps below.

### Important file-size note
ANSYS solver/result files can be large. GitHub blocks individual files larger than **100 MB** on regular Git repositories. If you later add larger files, use **Git LFS** for supported binary assets or publish a lighter repository containing the CAD exports, Workbench project, selected screenshots, and documentation. Avoid uploading temporary lock files such as `~$Assem.SLDASM` or `crankshaft_analysis_files/.lock`.

## Author

Madhvendra, B.Tech(Mechanical Engineering), NIT Hamirpur

## License

No license has been specified. Unless you add a license file, others do not automatically receive permission to reuse, modify, or redistribute the project.
