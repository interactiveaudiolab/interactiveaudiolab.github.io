---
name: Deep Learning Tools for Audacity
creators: [Hugo Flores Garcia, Aldo Aguilar, Ethan Manilow, Dmitry Vedenko and Bryan Pardo]

# external-url: https://www.nsf.gov/awardsearch/showAward?AWD_ID=1901456&HistoricalAwards=false
# external-url-text: Next Generation Content Production Tools for People with Vision Impairments

image: /assets/images/projects/audacity-logo.png
altdescription: Audacity logo #alt description of image for screen readers
# funding: 

collection: projects
#put full content below the dashed line. full markdown is supported.
---

We provide a software framework that lets deep learning practitioners easily integrate their own PyTorch models into Audacity, a free and open-source DAW. This creates a pipeline for ML audio researchers and developers to put tools in the hands of the artistic creators without the need to do DAW-specific development work, without having to learn how to create a VST plugin, and without having to maintain a server to deploy their models.

<img src="/assets/images/projects/audacity-frontpage.png"
    width="100%"
    height="100%">

### Download Audacity with Deep Learning

Our work has not yet been merged to the main build of Audacity, though it will be soon. You can keep track of its progress by viewing our [pull request](https://github.com/audacity/audacity/pull/1384). In the meantime, you can download a beta version of Audacity + Deep Learning here:

- [Mac OS](https://github.com/hugofloresgarcia/audacity/suites/3854232957/artifacts/95694217)
- [Windows (64 bit)](https://github.com/hugofloresgarcia/audacity/suites/3854232957/artifacts/95694220)
- [Linux](https://github.com/hugofloresgarcia/audacity/suites/3854232957/artifacts/95694218)

If you encounter any issues while using this nightly build, please report them on our [issue tracker](https://github.com/hugofloresgarcia/audacity/issues).

### Share your model with the Audacity community 

Contributing a model to audacity only requires familiarity with [PyTorch](https://pytorch.org/get-started/locally/). See [`torchaudacity`](https://github.com/hugofloresgarcia/torchaudacity) on Github for instructions on how to contribute your model to Audacity.

### Usage Example - Upmixing and Remixing with Source Separation

Here, we use the source separation models built-in with Audacity to create a collage of pop songs, taking instruments and vocals from different artists, and remixing them to create a new work. (*todo*)

<!-- ### Related publications -->

<!-- 
[[pdf]](/assets/papers/haptEQ_karp.pdf)A. Karp and B. Pardo, “HaptEQ: A Collaborative Tool For Visually Impaired Audio Producers,” in Proceedings of the 12th International Audio Mostly Conference on Augmented and Participatory Sound and Music Experiences, 2017, p. 39. --> 

