---
layout: page
title: Speech from Brain Signals
description: Synthesizing and decoding speech directly from neural activity.
img: assets/img/projects/speech.png
importance: 1
category: Neural Decoding
github: https://github.com/youngeun1209/NeuroTalk
---

My core research turns brain signals into language, spanning two complementary directions: synthesizing intelligible speech, and decoding imagined speech.

## Speech Synthesis from Brain Signals

{% include figure.liquid path="assets/img/projects/speech_AAAI.png" caption="NeuroTalk: generative voice reconstruction from EEG during imagined speech (AAAI 2023)." class="img-fluid rounded z-depth-1" %}

- Generative models (HiFi-GAN vocoders and diffusion) synthesize and reconstruct intelligible speech directly from EEG at roughly 30 words per minute, including the generation of unseen words (AAAI 2023).
- Released [NeuroTalk](https://github.com/youngeun1209/NeuroTalk), an open-source brain-to-speech synthesis framework with reproducible demos.
- Protected by a registered U.S. patent on speech synthesis from brain signals during imagined speech (No. 12,488,779).
- Formed the core of my Ph.D. dissertation, *Brain-to-Speech: Deep Generative Models for Noise-Resilient Speech Synthesis from Brain Signals.*

## Speech Decoding

{% include figure.liquid path="assets/img/projects/speech_interspeech.png" caption="Diff-E: diffusion-based decoding of imagined-speech EEG (Interspeech 2023)." class="img-fluid rounded z-depth-1" %}

- **Diff-E** (Interspeech 2023): diffusion-based representation learning for decoding imagined-speech EEG.
- **EEG-Transformer** (2022): self-attention from the Transformer architecture for decoding EEG of imagined speech.
- Improved cross-subject robustness with attention and transfer-learning representations, and extended the decoders to invasive recordings (sEEG/ECoG).
- Protected by a registered U.S. patent on imagined-speech brain-signal decoding (No. 12,204,624).

{% include figure.liquid path="assets/img/projects/EEG-Transformer.png" caption="EEG-Transformer: self-attention architecture for decoding imagined-speech EEG (2022)." class="img-fluid rounded z-depth-1" %}
