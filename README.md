# IFS-IngnisFlowStudio-Public-
# IgnisFlowStudio

A Windows desktop application for preparing, running, and reviewing fire simulations with **Fire Dynamics Simulator (FDS)**.

IgnisFlowStudio combines geometry preparation, mesh generation, simulation configuration, and results controls in one graphical interface.

## Download

Open this repository’s **Releases** section and download the portable ZIP attached to the latest release.

This repository distributes compiled application packages. Application source code is not included.

## Installation

1. Download the portable ZIP.
2. Right-click the ZIP and select **Extract All**.
3. Extract it to a folder where you have write permission.
4. Run **IgnisFlowStudio.exe**.

Keep the application’s folder structure intact, including the **_internal** folder. Do not run the application directly from inside the ZIP.

The portable package includes the application runtime and FDS. No separate Python or FDS installation is required.

## Requirements

- Windows 10 or Windows 11, 64-bit.
- Sufficient free disk space for the application, simulation inputs, and results.
- Available memory and processing capacity appropriate for your simulation’s mesh size.

Large simulations can require substantial memory, storage, and computation time.

## Features

### Geometry preparation

- Import STL and STEP geometry.
- Inspect geometry in the model viewport.
- Prepare geometry for use in FDS simulations.

### Mesh configuration

- Create mesh regions manually or automatically.
- Adjust region bounds and cell counts.
- Fit meshes to geometry.
- For closed STL geometry, fit the mesh inside the geometry or exclude its solid volume from a background mesh.
- Lock selected mesh regions while generating surrounding regions.
- Show or hide mesh region labels.

Geometry fitting depends on the input model. Some operations require closed geometry, and mesh boundaries and cell sizes must satisfy alignment requirements.

### Simulation setup

- Configure materials and surfaces.
- Define fire sources and fluid composition.
- Set initial conditions and output locations.
- Configure simulation duration and execution settings.

### Execution and results

- Run simulations using the integrated FDS solver.
- Configure parallel execution.
- Monitor simulation progress and output.
- Access results controls and launch Smokeview when available.

## Typical workflow

1. Import your geometry.
2. Define the simulation domain.
3. Create and review mesh regions.
4. Configure materials, surfaces, fire sources, and other conditions.
5. Choose output locations and simulation settings.
6. Save the project and review the generated FDS input.
7. Run the simulation.
8. Inspect solver messages and review the results.

## User guide

The portable package includes **User_Guide.pdf**, with detailed instructions for geometry preparation, meshing, simulation setup, execution, and results review.

## Troubleshooting

**The application does not start**

Extract the entire ZIP again and confirm that `IgnisFlowStudio.exe` and `_internal` remain together. Use a writable local folder.

**Geometry fitting fails**

Check that the geometry meets the selected operation’s requirements. Closed-volume operations require suitable closed geometry. Review mesh alignment and cell counts.

**A simulation stops or fails**

Read the solver output for the reported cause. Check the generated FDS input, geometry, mesh configuration, and available system resources.

## Feedback

When reporting a problem, include:

- Application version.
- Windows version.
- Steps needed to reproduce the problem.
- The error message or relevant solver output.
- A small example project, if you can share it.

Use GitHub Issues if enabled for this repository.

## Project status

IgnisFlowStudio is under active development. Features and file formats may change between releases. Back up important projects before opening them in a newer version.

Simulation accuracy depends on model assumptions, input data, mesh resolution, and interpretation. Validate models and assess mesh sensitivity before relying on results.

## Acknowledgements

IgnisFlowStudio uses **Fire Dynamics Simulator (FDS)**, developed by the National Institute of Standards and Technology (NIST), and other third-party components.

Third-party components retain their respective licences and notices. Refer to the notices included in the distribution.
