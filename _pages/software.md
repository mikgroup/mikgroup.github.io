---
layout: page
permalink: /software/
title: software
description: 
nav: true
nav_order: 4
---


### BART

The [Berkeley Advanced Reconstruction Toolbox (BART)](https://mrirecon.github.io/bart/index.html) is a free and open-source image-reconstruction framework for Magnetic Resonance Imaging (MRI). It consists of a programming library and a toolbox of command-line programs. The library provides common operations on multi-dimensional arrays, Fourier and wavelet transforms, as well as generic implementations of iterative optimization algorithms. The command-line tools provide direct access to basic operations on multi-dimensional arrays as well as efficient implementations of many calibration and reconstruction algorithms for parallel imaging and compressed sensing.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.bart_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
<br>

### SigPy

[SigPy](https://sigpy.readthedocs.io/en/latest/) is a package for signal processing, with emphasis on iterative methods. This package is built to operate directly on numpy arrays on CPU and cupy arrays on GPU. Its main features include: a unified CPU/GPU interface to signal processing functions, Linear operator classes, Proximal operator classes (Prox), Iterative algorithm classes (Alg), and Application classes (App) that wrap Alg, Linop, and Prox to form a final deliverable for each application.

SigPy also provides a submodule sigpy.mri for MRI iterative reconstruction methods. It includes Apps for common MRI reconstruction methods such as SENSE reconstruction, l1-wavelet reconstruction, total-variation reconstruction, and JSENSE reconstruction. This module also includes convenient simulation and sampling functions, including poisson-disc sampling function, and Shepp-Logan phantom generation function.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.sigpy_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
<br>

### ESPIRiT

ESPIRiT is a method to estimate coil sensitivities which finds the subspace of multi-coil data from a calibration region in k-space using a series of eigen-value decompositions in k-space and image space. The code below references the following paper: M. Uecker, P. Lai, M. J. Murphy, P. Virtue, M. Elad, J. M. Pauly, S. S. Vasanawala and M. Lustig, [ESPIRiT – An Eigenvalue Approach to Autocalibrating Parallel MRI: Where SENSE meets GRAPPA](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.24751)

Here are some viewable MATLAB demos:
- [ESPIRiT Maps]({{ site.baseurl }}/software/demo_espirit_maps/)
- [ESPIRiT Reconstruction]({{ site.baseurl }}/software/demo_espirit_recon/)
- [L1-ESPIRiT Reconstruction]({{ site.baseurl }}/software/demo_espirit_l1_recon/)
- [SAKE and ESPIRiT Reconstruction]({{ site.baseurl }}/software/demo_sake_espirit/)

**[Download link for the MATLAB code package](/assets/demo_code/SPIRiT_v0.3.tar.gz)**. 
This code includes MATLAB implementations of [ESPIRiT](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.24751),  [SPIRiT](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.22428),  [Geometric coil compression](https://onlinelibrary.wiley.com/doi/10.1002/mrm.24267), and [SAKE](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.24997). 

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.espirit_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
<br>

### Sparse MRI

Sparse MRI is a collection of Matlab functions that implement the algorithms and examples described in the paper [M. Lustig, D.L Donoho and J.M Pauly “Sparse MRI: The Application of Compressed Sensing for Rapid MR Imaging” Magnetic Resonance in Medicine, 2007 Dec; 58(6):1182-1195](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.21391). The high-level, non-expert overview is in the paper [M. Lustig, D.L Donoho, J.M Santos and J.M Pauly “Compressed Sensing MRI”, IEEE Signal Processing Magazine, 2008; 25(2): 72-82](https://ieeexplore.ieee.org/document/4472246)

**[Download link for MATLAB code](/assets/demo_code/sparseMRI_v0.2.tar.gz)**
<br>
<br>

### Geometric-Decomposition Coil Compression (GCC)

Coil arrays are used to accelerate the acquisition of MRI by exploiting the spatial sensitivity of the coils for spatial encoding. The increasing number of channels in systems today provides better acceleration, but at the same time results in significant increase in computation time. This in particularly a problem in iterative reconstructions. In this work (GCC), we exploit redundancy between the channels and the fact that the readout dimension in Cartesian imaging is never subsampled to compress the coils data into much fewer virtual coils. The software provided here is a Matlab implementation of this technique, which is described in [Zhang T, Pauly JM, Vasanawala SS, Lustig M. “Coil Compression for Accelerated Imaging with Cartesian Sampling,” MRM 2013;69(2):571-82](https://onlinelibrary.wiley.com/doi/10.1002/mrm.24267).

Here are some viewable MATLAB demos:
- [Geometric-decomposition coil compression]({{ site.baseurl }}/software/demo_gcc/)
- [ESPIRiT-based coil compression]({{ site.baseurl }}/software/demo_ecc/)
- [Speedup with GCC]({{ site.baseurl }}/software/demo_gcc_speedup/)

**[Download link for MATLAB code](/assets/demo_code/GCC.tar.gz)**
<br>
<br>

### Github Repositories

Here are Github repositories of research from our lab.

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
<br>

### Data

[mridata.org](http://mridata.org) provides open datasets to researchers who desire to contribute to a community of reproducible research, where they can test and validate their algorithms against known undersampled acquisitions. These datasets were acquired through a collaboration with Dr. Shreyas Vasanawala at Stanford's Lucile Packard Children's Hospital. The undersampled datasets are of two varieties: variable-density undersampling and uniform-density undersampling. At present, all of the datasets are of knee images. In addition to undersampled datasets, we also provide separate cases of fully sampled knees, for researchers who wish to experiment with their own undersampling patterns. 