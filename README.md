Projects using openPMD
----------------------

The following list of projects use the
[**openPMD** standard](https://github.com/openPMD/openPMD-standard)
to describe their data. For additional information, we list
third-party projects marked with a (`third party`) to acknowledge the
the work provided in those for our format handling.

### Documents

- [openPMD Standard](https://github.com/openPMD/openPMD-standard/blob/latest/STANDARD.md)
  - domain: the fundamental, technical documents that serve as a basis for the
            whole openPMD environment
  - maintainer and initial author: A Huebl @ax3l
  - contributions: [full list of contributors](https://github.com/openPMD/openPMD-standard/blob/latest/AUTHORS.md)
  - [repository](https://github.com/openPMD/openPMD-standard)
    ([CC-BY 4.0](https://github.com/openPMD/openPMD-standard/releases))
  - status: [`1.0.0` released](https://github.com/openPMD/openPMD-standard/releases)

### Scientific Simulations

- [PIConGPU](http://picongpu.hzdr.de) (HZDR, Germany)
  - domain: electro-dynamic particle-in-cell code
  - [repository](https://github.com/ComputationalRadiationPhysics/picongpu) (GPLv3+/LGPLv3+)
  - maintainers: A Huebl @ax3l, M Bussmann @bussmann et al.
  - status: implemented in `dev` (base standard + ED-PIC)

- [Warp](http://warp.lbl.gov) (LBNL & LLNL, United States)
  - domain: electro-dynamic/static particle-in-cell code
  - [repository](https://bitbucket.org/berkeleylab/warp) (BSD-3-Clause-LBNL)
  - maintainers: JL Vay @jlvay, D Grote @dpgrote, R Lehe @RemiLehe et al.
  - status: implemented (base standard + ED-PIC)

- FBPIC (LBNL, DESY)
  - domain: electro-dynamic particle-in-cell code with spetral solver and
            Fourier-Bessel decomposition in cylindrical geometry
  - *open source release planned*
  - maintainers: R Lehe @RemiLehe, M Kirchen @MKirchen et al.
  - status: implemented (base standard + ED-PIC)

### Data Processing and Visualization

- [openPMD viewer](https://github.com/openPMD/openPMD-viewer) (LBNL, DESY)
  - domain: high level python api and interactive IPython notebook GUI
  - [repository](https://github.com/openPMD/openPMD-viewer) (BSD-3-Clause-LBNL)
  - maintainer: R Lehe @RemiLehe et al.
  - status: implemented

- [postpic](https://github.com/skuschel/postpic) (U Jena, Germany)
  - domain: post-processing and visualization tool for particle-in-cell data
  - [repository](https://github.com/skuschel/postpic) (GPLv3+)
  - maintainer: S Kuschel @skuschel
  - status: implemented (hdf5 reader for base standard + ED-PIC)

- [yt project](http://yt-project.org) ([Members](http://yt-project.org/members.html), `third party`)
  - domain: analysis and visualization
  - [repository](https://bitbucket.org/yt_analysis/yt) (BSD-3-Clause)
  - [development repository](https://github.com/openPMD/openPMD-yt) (our fork)
  - maintainers: [yt project members](http://yt-project.org/members.html)
                 (HZDR: contribution)
  - status: HZDR is currently implementing a reader

Note: For third-party frameworks, the general idea is to implement our readers
[upstream](https://en.wikipedia.org/wiki/Upstream_%28software_development%29)
as soon as they are working.

Please check the individual repositories and feel free to contribute.

### Libraries

- [libSplash](https://github.com/ComputationalRadiationPhysics/libSplash) (TU Dresden/HZDR, Germany)
  - domain: high-level C++ HDF5 library for mesh and particle records
  - [repository](https://github.com/ComputationalRadiationPhysics/libSplash) (LGPLv3+)
  - maintainers: F Schmitt @f-schmitt-zih, A Huebl @ax3l
  - status:
    - 1.4.0+: full API available to fulfill the standard (read+write)
    - 2.0.0+ (upcoming): high-level interface for openPMD objects (base standard)

- [pyDive](https://github.com/ComputationalRadiationPhysics/pyDive) (HZDR, Germany)
  - domain: parallel numpy for ipython notebook
  - [repository](https://github.com/ComputationalRadiationPhysics/pyDive) (GPLv3+/LGPLv3+)
  - maintainer: H Burau @Heikman
  - status: currently implementing reader and writer (base standard + ED-PIC)

- [HDF5](https://www.hdfgroup.org/HDF5/) (`third party`)
  - domain: libraries for reading & writing the HDF5 format C/C++/Fortran
  - maintainer: HDF Group

- [ADIOS](https://www.olcf.ornl.gov/center-projects/adios/) (ORNL, United States; `third party`)
  - domain: libraries for reading & writing the HDF5 format C/C++/Fortran/Java/Python
  - [repository](https://github.com/ornladios/ADIOS) (BSD-3-Clause-DOE)
  - maintainer: N Podhorszki @pnobert, S Klasky @sklasky at al.

- [h5py](http://www.h5py.org/) (`third party`)
  - domain: python bindings for HDF5
  - [repository](https://github.com/h5py/h5py)
  - maintainer: A Collette @andrewcollette et al.

### Tools & Converters

Please be aware that *all existing tools* for general file handling
(HDF5, ADIOS, ...) are also usable with openPMD flavoured files!

A non-complete list of third party software for your consideration:

- validator scripts (HZDR, LBNL)
  - domain: scripts to validate files according to the `openPMD standard`
  - [repository](https://github.com/openPMD/openPMD-validator) (ISC)
  - maintainer: A Huebl @ax3l, R Lehe @RemiLehe
  - status: implemented (base standard + ED-PIC)

- [HDF Compass](https://github.com/HDFGroup/hdf-compass) (HDF Group; `third party`)
  - domain: viewer for HDF5 and related formats
  - [repository](https://github.com/HDFGroup/hdf-compass) (BSD-3-Clause-HDF)
  - [development repository](https://github.com/ComputationalRadiationPhysics/hdf-compass)
    (our fork for ADIOS support)
  - maintainer: HDF Group (HZDR: contribution)
  - status: HZDR is currently implementing an
            [ADIOS reader](https://github.com/ComputationalRadiationPhysics/hdf-compass)

- [HDFView](https://www.hdfgroup.org/products/java/hdfview/) (HDF Group; `third party`)
  - domain: viewer for HDF5
  - maintainer: HDF Group
  - [download](https://www.hdfgroup.org/products/java/hdfview/) (BSD-3-Clause-HDF)

- HDF5 command line tools (HDF Group; `third party`)
  - domain: HDF5 file handling
  - maintainer: HDF Group
  - examples: `h5ls`, `h5dump`, `h5diff`, `h5repack`, `gif2h5`, ...

- ADIOS command line tools (ORNL, United States; `third party`)
  - domain: ADIOS file handling
  - maintainers: N Podhorszki @pnorbert, S Klasky @sklasky et al.
  - examples: `bpls`, `bpdump`, `bpdiff`, `bp2bp`, `bp2h5`, ...

- [png2gas](https://github.com/ComputationalRadiationPhysics/picongpu/tree/master/src/tools/png2gas) (HZDR, Germany)
  - domain: convert a 2D png image into a 3D density profile,
            useful for particle-in-cell simulations
  - [repository](https://github.com/ComputationalRadiationPhysics/picongpu/tree/master/src/tools/png2gas) (GPLv3+)
  - maintainer: originally by PIConGPU team
  - status: [needs adjustments for openPMD 1.0.0](https://github.com/ComputationalRadiationPhysics/picongpu/issues/1446)

- XDMF file creation
  - domain: light-weight, xml meta file creation for reading in VTK (e.g., ParaView, VisIt)
  - [repository](https://github.com/openPMD/openPMD-tools)
  - note: XDMF is a `third party` file format compatible with openPMD
  - maintainers: originally by PIConGPU team
  - status: [needs adjustments for openPMD 1.0.0](https://github.com/openPMD/openPMD-tools/issues/1)

- VizSchema schema additions
  - domain: light-weight, in-file attribute creation for reading in VTK (e.g., ParaView, VisIt)
  - [repository](https://github.com/openPMD/openPMD-tools)
  - note: VizSchema is a `third party` file markup compatible with openPMD
  - maintainers: *nobody yet*
  - status: [planned](https://github.com/openPMD/openPMD-tools/issues/2)
