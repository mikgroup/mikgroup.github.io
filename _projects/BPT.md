---
title: Beat Pilot Tone (BPT)
description: |
  <span style="text-align: justify; display: block;">
    Our research focuses on developing Beat Pilot Tone (BPT), an enhanced RF-based motion sensing method that uses dual-frequency tones mixed through receiver nonlinearity to provide superior motion sensitivity and physiological motion discrimination for MRI artifact correction.
  </span>
people:
  - Rinni Bhansali
  - Naz Khairallah
  - Jack Kang
  - Suma Anand
  - Michael (Miki) Lustig
layout: project
category: MRI Hardware
images:
  - "/images/publications/bpt_paper.jpg"
  - "/images/research/BPT_1.jpg"
  - "/images/research/BPT_2.png"
last-updated: 2025-09-03
---

<p style="text-align: justify;">
Motion is a major source of MRI artifacts due to long acquisition times, but these artifacts can be corrected if motion is accurately measured. RF-based motion sensing is attractive because it works with any pulse sequence and does not affect patient comfort. Pilot Tone (PT) is a compelling example, as it does not require additional hardware to receive motion signals—RF tones transmitted into the scanner bore are motion-modulated and detected by the MRI receiver coils without extra hardware. However, these tones are limited to the Larmor frequency, reducing motion sensitivity, especially at low and mid fields. We address this with Beat Pilot Tone (BPT), which uses two RF tones transmitted into the bore at higher frequencies. Patient motion modulates both tones, and receiver hardware nonlinearity mixes them down to the Larmor frequency via intermodulation. The resulting signals are processed like PT, but BPT provides greater motion sensitivity and can distinguish between physiological motion types (e.g., cardiac, respiratory).
</p>


## Key Contributions

- **Multi-signal motion correction model**: Developing a model to correct motion in 3D head scans using multiple transmitted PT and BPT signals
- **Hardware robustness improvements**: Creating external diode mixer boards and Microwave Pilot Tone (μPT) systems to address commercial receiver hardware limitations and improve signal mixing efficiency
- **Integrated coil design**: Developing μPT with on-coil mixers that down-convert transmitted tones directly into coil bandwidth and inductively couple into the receive chain
- **Performance characterization**: Characterizing BPT's motion sensitivity and artifact behavior across transmit frequencies, antenna configurations, and other parameters
- **Signal separation method**: Developing unsupervised methods to separate BPT signals from MRI data in the combined receive chain