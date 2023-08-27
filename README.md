# Flow Around a Rotating Cylinder using OpenFOAM

## Introduction

This repository contains the setup files for numerical simulation project for studying the flow around a rotating cylinder using OpenFOAM. OpenFOAM is an open-source CFD (Computational Fluid Dynamics) software designed to model fluid flows and other continuum phenomena. The simulation is set up to capture the details of the flow patterns around a cylinder rotating at a constant angular velocity.

## Requirements

- OpenFOAM 

## Directory Structure

![A model case setup within OpenFOAM](Images/Directory.png)

## Setup Steps

### Mesh Generation

- Meshing is done using `blockMesh` and optional refinement with `snappyHexMesh`.

### Boundary Conditions

- In the `0/` directory, boundary conditions for `U`, `p`, and other necessary fields are specified.
- Cylinder wall is set to rotate at a specified angular velocity.

### Solver Selection

- The simulation is set up to use `pimpleFoam` for incompressible, transient flow.

### Control Parameters

- Control parameters like time-step, write interval, and run-time are specified in `system/controlDict`.

## Running the Simulation

1. Source OpenFOAM environment variables:

    \```
    source /path/to/OpenFOAM/OpenFOAM-x.x/etc/bashrc
    \```

2. Navigate to the simulation root directory.

3. Generate the mesh:

    \```
    blockMesh
    \```

    (Optional: Refine mesh)

    \```
    snappyHexMesh -overwrite
    \```

4. Initialize the simulation:

    \```
    pimpleFoam
    \```

5. (Optional) Run the simulation using the shell script:

    \```
    chmod +x runSimulation.sh
    ./runSimulation.sh
    \```

## Post-Processing

- Open the simulation results in ParaView to visualize the flow fields, vortex shedding, etc.
- Optional post-processing scripts are located in the `postProcess/` directory.

## Contributing

Feel free to fork the project and submit pull requests. Ensure you adhere to the coding and documentation guidelines.

## Authors

- [Your Name](mailto:youremail@example.com)

## Acknowledgements

- OpenFOAM Foundation for the software.
- [Reference Paper](link)

## License

This project is licensed under the MIT License. See the LICENSE.md file for details.

---

For more details, feel free to contact the author or refer to the project documentation.



![Alt text for image](./images/image_name.jpg)
