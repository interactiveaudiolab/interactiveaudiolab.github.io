---
name: Cerberus, simultaneous audio separation and transcription
creators: [Ethan Manilow, Prem Seetharaman, Bryan Pardo]
external-url: /demos/cerberus
external-url-text: Audio examples
image: /assets/images/projects/cerberus.png
altdescription: System diagram of Cerberus
collection: projects
#put full content below the dashed line. full markdown is supported.
---

Cerberus is a single deep learning architecture that can simultaneously separate sources in a musical mixture and transcribe those sources.

We present a single deep learning architecture that can both separate an audio recording of a musical mixture into constituent single-instrument recordings and transcribe these instruments into a human-readable format at the same time, learning a shared musical representation for both tasks. This novel architecture, which we call Cerberus, builds on the Chimera network for source separation by adding a third "head" for transcription. By training each head with different losses, we are able to jointly learn how to separate and transcribe up to 5 instruments in our experiments with a single network. We show that the two tasks are highly complementary with one another and when learned jointly, lead to Cerberus networks that are better at both separation and transcription and generalize better to unseen mixtures.

### Watch the video 

<iframe width="560" height="315" src="https://www.youtube.com/embed/zH_XJU3suqw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Demos 

[Demo and audio examples](/demos/cerberus)

### Related Publications 
[E. Manilow, P. Seetharaman, and B. Pardo, “Simultaneous Separation and Transcription of Mixtures with Multiple Polyphonic and Percussive Instruments,” in ICASSP 2020-2020 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2020.](https://arxiv.org/abs/1910.12621)

