---
name: Multi-resolution Common Fate Transform
creators: [Fatemeh Pishdadian and Bryan Pardo]
external-url: https://github.com/interactiveaudiolab/MCFT
external-url-text: Demos and Source Code
image: /assets/images/projects/mcft.png
altdescription: MCFT filter
funding: This work was supported by United States National Science Foundation award number 1420971
collection: projects
#put full content below the dashed line. full markdown is supported.
---

The [Multi-resolution Common Fate Transform (MCFT)](/assets/papers/pishdadian_pardo_mcft_journal_2018.pdf) is an audio signal representation developed in our lab in the context of audio source separation.

Audio source separation is the process of extracting a single sound (e.g. one violin) from a mixture of sounds (a string quartet). Many audio source separation algorithms are applied to audio representations that cannot resolve sounds that overlap in both time and frequency, such as the magnitude spectrogram. This puts a limit on their ability to separate sounds. Some researchers have developed biologically informed auditory models that are able to represent time-frequency overlapped sounds separately, but the process of creating the representation loses information and the separated sounds cannot be reconstructed from the representation. This limits the utility of biologically informed model output for source separation.

The MCFT:

* Combines the invertibility of the [Common Fate Transform (CFT)](https://hal.archives-ouvertes.fr/hal-01248012/document), and  the multi-resolution  property of the cortical stage output of [an auditory model](https://asa.scitation.org/doi/abs/10.1121/1.1945807). 

* Explicitly represents spectro-temporal modulation patterns of audio signals and thus facilitates the separation of signals that overlap in the time-frequency domain.

* Has been shown to provide higher separability than the Short-time Fourier Transform (STFT), Constant-Q Transform (CQT), and CFT.

### Related publications

[[pdf]](https://interactiveaudiolab.github.io/assets/papers/pishdadian_pardo_liutkus.pdf) Fatemeh Pishdadian, Bryan Pardo, and Antoine Liutkus, “A multi-resolution approach to common fate-based audio separation,” in IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2017. 

[[pdf]](https://interactiveaudiolab.github.io/assets/papers/pishdadian_pardo_mcft_journal_2018.pdf) Fatemeh Pishdadian and Bryan Pardo, “Multi-Resolution Common Fate Transform,” IEEE/ACM Transactions on Audio, Speech, and Language Processing, 2018. 

