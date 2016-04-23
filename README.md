Projects using openPMD
----------------------

The following list of projects use the
**openPMD** standard to describe their data.

### Libraries

- [libSplash](https://github.com/ComputationalRadiationPhysics/libSplash) (TU Dresden/HZDR, Germany)
  - domain: high-level C++ HDF5 library for mesh and particle records
  - [repository](https://github.com/ComputationalRadiationPhysics/libSplash) (LGPLv3+)
  - status:
    - 1.4.0+: full API available to fulfill the standard (read+write)
    - 2.0.0+ (upcoming): high-level interface for openPMD objects (base standard)

### Scientific Simulations

- [PIConGPU](http://picongpu.hzdr.de) (HZDR, Germany)
  - domain: electro-dynamic particle-in-cell code
  - [repository](https://github.com/ComputationalRadiationPhysics/picongpu) (GPLv3+/LGPLv3+)
  - status: implemented in `dev` (base standard + ED-PIC)

- [Warp](http://warp.lbl.gov) (LBNL & LLNL, United States)
  - domain: electro-dynamic/static particle-in-cell code
  - [repository](https://bitbucket.org/berkeleylab/warp) (BSD-3-Clause-LBNL)
  - status: implemented (base standard + ED-PIC)

- FBPIC (LBNL, DESY)
  - domain: electro-dynamic particle-in-cell code with spetral solver and
            Fourier-Bessel decomposition in cylindrical geometry
  - *open source release planned*
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
  - domain: post-processing and visualization tool for particle-in-cell data
  - [repository](https://github.com/skuschel/postpic) (GPLv3+)
  - status: implemented (hdf5 reader for base standard + ED-PIC)

- [yt project](http://yt-project.org) ([Members](http://yt-project.org/members.html))
  - domain: analysis and visualization
  - [repository](https://bitbucket.org/yt_analysis/yt) (BSD-3-Clause)
  - [development repository](https://github.com/openPMD/openPMD-yt) (our fork)
  - status: currently implementing reader

Note: For third-party frameworks, the general idea is to implement our readers
[upstream](https://en.wikipedia.org/wiki/Upstream_%28software_development%29)
as soon as they are working.

Please check the individual repositories and feel free to contribute.

### Basic Tools

Please be aware that *all existing tools* for general file handling
(HDF5, ADIOS, ...) are also usable with openPMD flavoured files!

A non-complete list of third party software for your consideration:

- [HDF Compass](https://github.com/HDFGroup/hdf-compass) (HDF Group)
  - domain: viewer for HDF5 and related formats
  - [repository](https://github.com/HDFGroup/hdf-compass) (BSD-3-Clause-HDF)
  - [development repository](https://github.com/ComputationalRadiationPhysics/hdf-compass)
    (our fork for ADIOS support)
  - status: HZDR is currently implementing an
            [ADIOS reader](https://github.com/ComputationalRadiationPhysics/hdf-compass)

- [HDFView](https://www.hdfgroup.org/products/java/hdfview/) (HDF Group)
  - domain: viewer for HDF5
  - [download](https://www.hdfgroup.org/products/java/hdfview/) (BSD-3-Clause-HDF)

- HDF5 command line tools (HDF Group)
  - domain: HDF5
  - examples: `h5ls`, `h5dump`, `h5diff`, `h5repack`, `gif2h5`, ...

- ADIOS command line tools (ADIOS Group, United States)
  - domain: ADIOS
  - examples: `bpls`, `bpdump`, `bpdiff`, `bp2bp`, `bp2h5`, ...

- [png2gas](https://github.com/ComputationalRadiationPhysics/picongpu/tree/master/src/tools/png2gas) (HZDR, Germany)
  - domain: convert a 2D png image into a 3D density profile,
            useful for particle-in-cell simulations
  - [repository](https://github.com/ComputationalRadiationPhysics/picongpu/tree/master/src/tools/png2gas) (GPLv3+)
  - status: needs adjustments for openPMD 1.0.0
