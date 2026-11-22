---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

My research is on machine learning for inverse problems, applied to quantitative cardiac MRI (MR Fingerprinting, MRF). I build methods that reconstruct images and physical parameter maps from heavily undersampled, noisy measurements without labeled training data. I also design faster acquisitions and engineer the methods so they run on real scanners.

## Accelerated Cine MRF for Whole-LV Quantitative Imaging
*Jul. 2026 – present*

- Developed a Deep Image Prior reconstruction framework for highly undersampled cine MRF. It generates 24-phase cardiac-resolved T<sub>1</sub>, T<sub>2</sub>, proton-density, and B<sub>1</sub><sup>+</sup> maps alongside synthetic bright- and dark-blood cine images.
- Built a GPU non-rigid alignment module (B-spline deformation on multi-channel latent features) that halved estimate variability (SD 59 → 31) across 20 subjects.
- Achieved ~4× acquisition acceleration (11.0 → 2.8 s per slice). Eight short-axis slices can now be acquired sequentially in a single breathhold instead of one breathhold per slice.
- Demonstrated whole-LV functional assessment in a cardiomyopathy patient, with EF, EDV, and ESV comparable to full-length cine MRF and conventional cine MRI.

## Meta-Learning Accelerated Reconstruction for Cardiac MRF
*Jun. 2025 – present*

- Developed a REPTILE-based framework that meta-learns adaptable initializations for image reconstruction, coil sensitivity estimation, and network inputs in scan-specific, self-supervised cardiac MRF reconstruction.
- Designed a coarse-to-fine optimization strategy with low-rank subspace modeling and Toeplitz-accelerated non-Cartesian data consistency to reduce repeated NUFFT computations.
- Meta-trained on 40 datasets on an HPC cluster to get a shared initialization for a two-stage test-time optimization with mixed precision and CUDA Graphs.
- Cut per-sample reconstruction time on an NVIDIA A40 GPU from **8.3 min to 32 s (~16×)** on static data and from **66 min to 2.4 min (~28×)** on cine data. The speedup comes from meta-initialization and profiling-driven GPU optimization (GROG gridding, Toeplitz operators, fused data pipeline), with comparable map quality and good out-of-distribution generalization (patient, post-contrast, and long-axis data).
- Deployed the reconstruction inline on a clinical MRI scanner as a streaming TCP server inside the vendor's sandboxed, network-isolated runtime. It returns quantitative maps in ~3.4 min on an 8 GB NVIDIA T1000 edge GPU.

<div class="research-figs">
  <figure>
    <img src="{{ base_path }}/images/research/meta-mrf-example1.webp" alt="T1 and T2 maps: conventional reconstruction in 66 min versus meta-learned reconstruction in 2.4 min" loading="lazy">
  </figure>
  <figure>
    <img src="{{ base_path }}/images/research/meta-mrf-example2.webp" alt="T1 and T2 maps: conventional reconstruction in 8.3 min versus meta-learned reconstruction in 32 s" loading="lazy">
  </figure>
</div>
<p class="research-figs__caption">T<sub>1</sub> and T<sub>2</sub> maps: conventional scan-specific reconstruction (left column) vs. our meta-learned reconstruction (right column), timed on an A40 GPU. Left: cine data, 66 min → 2.4 min. Right: static data, 8.3 min → 32 s.</p>

## Low-Field Cardiac MRF: Sequence Adaptation & Reconstruction
*Aug. 2024 – Dec. 2025*

- Adapted a 2D spiral cardiac MRF sequence for 0.55T imaging under low-SNR and gradient constraints, enabling single-breathhold multiparametric cardiac mapping.
- Developed a self-supervised Deep Image Prior reconstruction that jointly recovers MRF subspace images, refines coil sensitivity maps, and estimates quantitative T<sub>1</sub>/T<sub>2</sub>/proton-density maps.
- Validated on phantom data and 18 healthy subjects, improving myocardial T<sub>1</sub>/T<sub>2</sub> precision over conventional low-rank reconstruction. This work was selected as the May 2026 [JMRI](https://doi.org/10.1002/jmri.70316) cover image.

## Pulse Sequence Optimization for Cardiac MRF
*Jun. 2023 – Aug. 2024*

- Built a physics-driven pulse sequence optimization framework that combines Bloch simulation, spiral k-space undersampling, and dictionary matching to optimize flip-angle schedules and T<sub>1</sub>/T<sub>2</sub> preparation parameters.
- Shortened the breathhold from 15 to 5 heartbeats and the diastolic acquisition window from 250 to 150 ms while preserving quantitative mapping accuracy and precision.
