---
name: Deep Learning Tools for Audacity
creators: [Hugo Flores Garcia, Aldo Aguilar, Ethan Manilow, Dmitry Vedenko and Bryan Pardo]


image: /assets/images/projects/audacity-logo.png
altdescription: Audacity logo #alt description of image for screen readers

collection: projects
#put full content below the dashed line. full markdown is supported.
---

We provide a software framework that lets deep learning practitioners easily integrate their own PyTorch models into the open-source Audacity DAW. This lets ML audio researchers put tools in the hands of sound artists without doing DAW-specific development work.

Our software framework lets ML developers easily integrate new deep-models into Audacity, a free and open-source DAW that has logged over 100 million downloads since 2015. Developers upload their trained PyTorch model to HuggingFace's [Model Hub](https://huggingface.co/models?filter=audacity). The model becomes accessible through Audacity's UI and loads in a manner similar to traditional plugins. 

<img src="/assets/images/projects/audacity-frontpage.png"
    width="100%"
    height="100%">

### Download Audacity with Deep Learning

Our work has not yet been merged to the main build of Audacity, though it will be soon. You can keep track of its progress by viewing our [pull request](https://github.com/audacity/audacity/pull/1384). In the meantime, you can download an alpha version of Audacity + Deep Learning here:

**Note**: This is a nightly build, so you may encounter issues. If something breaks, make sure to stay updated with the latest build using the download link below. If that doesn't fix it, start an issue on our [issue tracker](https://github.com/hugofloresgarcia/audacity/issues).


#### Download Using Google Drive

*last updated*: 11/07/2021

- [Mac OS](https://drive.google.com/file/d/1ogOtoqKK6725XrIuGoCRlBXqtsJN2nhN/view?usp=sharing)
- [Windows (64 bit)](https://drive.google.com/file/d/1j_ndSIBrUH_Sg82j11wFVpA2VtJBJCCj/view?usp=sharing)

#### Issues? 

If you encounter any issues while using this nightly build, please report them on our [issue tracker](https://github.com/hugofloresgarcia/audacity/issues).

### Share your model with the Audacity community 

Contributing a model to audacity only requires familiarity with [PyTorch](https://pytorch.org/get-started/locally/). See [`audacitorch`](https://github.com/hugofloresgarcia/audacitorch) on Github for instructions on how to contribute your model to Audacity.

### Usage Example - Upmixing and Remixing with Source Separation

Here, we use the source separation models built-in with Audacity to create a collage of pop songs, taking instruments and vocals from different artists, and remixing them to create a new work. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/muEOJqGSYVk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Related Talks

### Bay Innovative Signal Hackers Meetup (2021) 
<iframe width="560" height="315" src="https://www.youtube.com/embed/gUXdQLUdOsU?start=2887" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Related Publications 

[[pdf]](https://arxiv.org/pdf/2110.13323.pdf) H. Flores Garcia, A. Aguilar, E. Manilow, D. Vedenko, and B. Pardo. Deep learning tools for audacity: Helping researchers expand the artist’s toolkit. In 5th Workshop on Machine Learning for Creativity and Design at NeurIPS 2021, 2021