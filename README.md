Projects using openPMD
----------------------

The following list of projects use the
**openPMD** standard to describe their data.

### Libraries

- [libSplash](https://github.com/ComputationalRadiationPhysics/libSplash) (TU Dresden/HZDR, Germany)
  - domain: high-level C++ HDF5 library for mesh and particle records
  - [repository](https://github.com/ComputationalRadiationPhysics/libSplash) (LGPLv3+)
  - status:
    - 1.3.0+: full API available to fulfill the standard (read+write)
    - 2.0.0+ (upcoming): high-level interface for openPMD objects (base standard)

### Scientific Simulations

- [PIConGPU](http://picongpu.hzdr.de) (HZDR, Germany)
  - domain: electro-dynamic particle-in-cell code
  - [repository](https://github.com/ComputationalRadiationPhysics/picongpu) (GPLv3+/LGPLv3+)
  - status: currently implementing (base standard + ED-PIC)

- [Warp](http://warp.lbl.gov) (LBNL & LLNL, United States)
  - domain: electro-dynamic/static particle-in-cell code
  - [repository](https://bitbucket.org/berkeleylab/warp) (BSD-3-Clause-LBNL)
  - status: implemented (base standard + ED-PIC)

### Data Processing and Visualization

- [openPMD viewer](https://github.com/openPMD/openPMD-viewer) (LBNL, DESY)
  - domain: high level python api and interactive IPython notebook GUI
  - [repository](https://github.com/openPMD/openPMD-viewer) (BSD-3-Clause-LBNL)
  - status: implemented

- [pyDive](https://github.com/ComputationalRadiationPhysics/pyDive) (HZDR, Germany)
  - domain: parallel numpy for ipython notebook
  - [repository](https://github.com/ComputationalRadiationPhysics/pyDive) (GPLv3+/LGPLv3+)
  - status: currently implementing reader and writer (base standard + ED-PIC)

- [postpic](https://github.com/skuschel/postpic) (U Jena, Germany)
  - domain: serial post-processing tool for particle-in-cell codes
  - [repository](https://github.com/skuschel/postpic) (GPLv3+)
  - status: currently implementing (reader for base standard + ED-PIC)

- [yt project](http://yt-project.org)
  - domain: analysis and visualization
  - [repository](https://github.com/openPMD/openPMD-yt) (BSD-3-Clause)
  - status: currently implementing reader

### Additional Tools

We provide and collect further tools, software modules and plugins for popular
frameworks in our GitHub organization:
  https://github.com/openPMD
  
Also be aware that *all existing tools* for general (HDF5, ADIOS, ...) file handling are also usable!

Please check the individual repositories and feel free to contribute.
