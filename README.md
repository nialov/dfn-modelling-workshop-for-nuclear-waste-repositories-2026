# DFN Modelling Workshop for Nuclear Waste Repositories – 9th – 12th of June 2026, Uppsala, Sweden

This repository contains the technical instructions for installing software
related to demonstrations at the workshop and links/material to follow the
demonstrations. The technical requirements, such as requirement of a Linux
environment or a registered account at a cloud service, are listed for each
demonstrated software. Please also always check the demonstration material
provided by the demonstrators for the most up to date instructions. Links
to the material are provided for each software.

## OpenGeoSys

### Technical requirements

#### Cloud

-   The demonstration exercises can be run using Binder
    (<https://mybinder.org/>). However, it can be expected that the
    computing resources provided will be limited and the computing
    resources are sometimes unavailable.

#### Local

### Material (WORK-IN-PROGRESS)

-   [DFN-generation using
    PorePy](https://www.opengeosys.org/6.5.8/docs/benchmarks/reactive-transport/dfnbyporepy/)

-   [DFN-OGS-PorePy](https://www.opengeosys.org/6.5.8/docs/benchmarks/reactive-transport/dfnbyporepy_to_ogs/)

-   [Greatcell-LIE-SmallDeformation](https://www.opengeosys.org/6.5.8/docs/benchmarks/small-deformations/greatcellm/)

-   [Greatcell-Hydromechanical](https://www.opengeosys.org/6.5.8/docs/benchmarks/hydro-mechanics/greatcellhm/)

-   [Open prebuilt Binder environment with OGS
    PETSc](https://binder.opengeosys.org/v2/gh/bilke/binder-ogs-requirements/petsc-6.5.8-0.8.0?urlpath=git-pull?repo=https://gitlab.opengeosys.org/ogs/ogs&urlpath=lab/tree&branch=master&depth=1)

    -   Use the environment for these two notebooks
    -   [Static
        fractures](https://www.opengeosys.org/6.5.8/docs/benchmarks/phase-field/greatcellhm_vpf/)
    -   [Propagating
        fracture](https://www.opengeosys.org/6.5.8/docs/benchmarks/phase-field/greatcellhm_vpf_propagating/)

-   [Rough
    fracture](https://ogs.ogs.xyz/ogs/mr-5729/docs/benchmarks/liquid-flow/roughfracture_benchmark/)

## PorePy (<https://github.com/keileg/dfn_workshop_porepy>)

Please see the [link](https://github.com/keileg/dfn_workshop_porepy) in the
title to access the main instruction material repository.

### Technical requirements

#### Cloud

-  GitHub account (<https://github.com/signup>)
-  The software can be run using GitHub Codespaces. However, it can be
   expected that the computing resources provided by GitHub will be limited.
   Consequently, only relatively simple simulations can be run.

#### Local

WORK-IN-PROGRESS

-  Please see the `install.sh` script in the main instruction material
   repository for preliminary installation instructions

### Demonstration instructions

1. Go to https://github.com/keileg/dfn_workshop_porepy
2. Create Github account and login
3. Click Code, Codespaces and then create new codespace
4. This should open VSCode like environment for computing.
5. Go to flow_and_transport directory and open up flow_and_transport_2d.ipynb
6. Click Run all, pick Python kernel /usr/local/bin/python and wait for execution
