---
layout: page
permalink: /sofware/
title: software
description: 
nav: true
nav_order: 4
---


## BART

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.bart_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

The Berkeley Advanced Reconstruction Toolbox (BART) is a free and open-source image-reconstruction framework for Magnetic Resonance Imaging (MRI). It consists of a programming library and a toolbox of command-line programs. The library provides common operations on multi-dimensional arrays, Fourier and wavelet transforms, as well as generic implementations of iterative optimization algorithms. The command-line tools provide direct access to basic operations on multi-dimensional arrays as well as efficient implementations of many calibration and reconstruction algorithms for parallel imaging and compressed sensing.

## SigPy

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.sigpy_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

SigPy is a package for signal processing, with emphasis on iterative methods. This package is built to operate directly on numpy arrays on CPU and cupy arrays on GPU. Its main features include: a unified CPU/GPU interface to signal processing functions, Linear operator classes, Proximal operator classes (Prox), Iterative algorithm classes (Alg), and Application classes (App) that wrap Alg, Linop, and Prox to form a final deliverable for each application.

SigPy also provides a submodule sigpy.mri for MRI iterative reconstruction methods. It includes Apps for common MRI reconstruction methods such as SENSE reconstruction, l1-wavelet reconstruction, total-variation reconstruction, and JSENSE reconstruction. This module also includes convenient simulation and sampling functions, including poisson-disc sampling function, and Shepp-Logan phantom generation function.

## Data

### [mridata.org](http://mridata.org)

This website provides open datasets to researchers who desire to contribute to a community of reproducible research, where they can test and validate their algorithms against known undersampled acquisitions. These datasets were acquired through a collaboration with Dr. Shreyas Vasanawala at Stanford's Lucille Packard Children's Hospital. The undersampled datasets are of two varieties: variable-density undersampling and uniform-density undersampling. At present, all of the datasets are of knee images. In addition to undersampled datasets, we also provide separate cases of fully sampled knees, for researchers who wish to experiment with their own undersampling patterns

## ESPIRiT

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.espirit_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>


<!-- ## Compressed Sensing -->

## Other Repositories

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

