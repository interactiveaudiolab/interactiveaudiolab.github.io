---
name: MaskMark - Robust Neural Watermarking for Real and Synthetic Speech
external-url: "https://oreillyp.github.io/maskmark/"
external-url-text: Audio Examples
creators: [Patrick O'Reilly, Zeyu Jin, Jiaqi Su, Bryan Pardo]
image: /assets/images/projects/maskmark_specplot.png
altdescription: MaskMark
collection: projects
excerpt_separator: <!--end_excerpt-->
#put full content below the dashed line. full markdown is supported.
---

High-quality speech synthesis models may be used to spread misinformation or impersonate voices. Audio watermarking can combat misuse by embedding a traceable signature in generated audio. However, existing audio watermarks typically demonstrate robustness to only a small set of transformations of the watermarked audio. To address this, we propose MaskMark, a neural network-based digital audio watermarking technique optimized for speech. <!--end_excerpt-->

MaskMark embeds a secret key vector in audio via a multiplicative spectrogram mask, allowing the detection of watermarked speech segments even under substantial signal-processing or neural network-based transformations. Comparisons to a state-of-the-art baseline on natural and synthetic speech corpora and a human subjects evaluation demonstrate MaskMark’s superior robustness in detecting watermarked speech while maintaining high perceptual transparency.

### Related publications
[[pdf]](/assets/papers/oreilly_jin_su_pardo_watermark.pdf) P. O’Reilly, Z. Jin, J. Su, and B. Pardo, “MaskMark: Robust Neural Watermarking for Real and Synthetic Speech,” in IEEE International Conference on Acoustics, Speech, and Signal Processing (ICASSP), 2024.