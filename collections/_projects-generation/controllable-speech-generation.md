---
name: Controllable Speech Generation
creators: [Max Morrison and Bryan Pardo]
image: /assets/images/projects/speech.png
altdescription: Speech conversation icon
collection: projects
#put full content below the dashed line. full markdown is supported.
---

Nuances in speech prosody (i.e., the pitch, timing, and loudness of speech) are a vital part of how we communicate. We utilize generative machine learning models to generate prosody with user control over these nuances and generate speech reflecting user-specified prosody.


### Fine-grained prosody editing

Given a speech recording and a target prosody (e.g., a pitch contour and phoneme durations), how can we transform the speech recording to have the target prosody? This task is called fine-grained prosody editing, and is useful for speech editing applications such as podcast post-production. Audio examples can be found [here](https://maxrmorrison.com/sites/controllable-lpcnet).

<iframe width="560" height="315" src="https://www.youtube.com/embed/4-_Szz1Syvg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Speech prosody correction

Speech prosody correction is where speech with unnatural pitch, phoneme durations, or loudness is adjusted by a computer to sound more natural. For instance, this can happen when naively copying and pasting audio waveforms of the same speaker. Prosody correction systems have applications in film and podcast dialogue post-production. Audio examples can be found [here](https://maxrmorrison.com/sites/context-aware).

<iframe width="560" height="315" src="https://www.youtube.com/embed/zrc1GjVxGL8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Related publications

[[pdf]](/assets/papers/morrison2021context.pdf) M. Morrison, L. Rencker, Z. Jin, N. J. Bryan, J.-P. Caceres, and B. Pardo, “Context-Aware Prosody Correction for Text-Based Speech Editing,” in IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2021.

[[pdf]](/assets/papers/morrison2022neural.pdf) M. Morrison, Z. Jin, N. J. Bryan, J.-P. Caceres, and B. Pardo, “Neural Pitch-Shifting and Time-Stretching with Controllable LPCNet,” Submitted to IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2022.
