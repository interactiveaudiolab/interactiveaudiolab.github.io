---
layout: default
title: Projects
permalink: /projects/
navigation: projects
---

{%- include title.html -%}

{% assign anchors= "interfaces,search,separation,generation,robustness" | split: ","%}

<nav class="sub-nav">
    <ul class="nav">
    {% for category in anchors %}
    <li class="nav-item">
        <a class="nav-link" href="#{{category}}">{{category}}</a>
    </li>
    {% endfor %}
    </ul>
</nav>

## Interfaces
Improving audio production tools meaningfully enhances the creative output of musicians, podcasters, producers and videographers. We focus on bridging the gap between the intentions of creators and the interfaces of audio recording and manipulation tools they use. Our work in this area has a strong human-centered machine learning component.  Representative projects in the area are below. For further publications in this area, see our [publications](/publications) page.

{% include list.html collection=site.projects-interfaces title="" anchor-tag="interfaces" %}



## Search
Content-addressable search through collections of many audio files (thousands) or lengthy audio files (hours) is an ongoing research area. In this work, we develop and apply cutting edge techniques in machine learning, signal processing and interface design. This is part of a [collaboration with the University of Rochester AIR lab](http://www2.ece.rochester.edu/projects/air/projects/audiosearch) and is supported by the National Science Foundation. Representative recent projects in this area are below. For further publications in this area, see our [publications](/publications) page.

{% include list.html collection=site.projects-search title="" anchor-tag="search" %}

<br>

## Separation
Audio source separation is the process of extracting a single sound (e.g. one violin) from a mixture of sounds (a string quartet). This is an ongoing research area in the lab. Source separation is the audio analog of scene segmentation in computer vision and is a foundational technology that improves or enables speech recogntion, sound object labeling, music transcription,hearing aids and other technologies. For further publications in this area, see our [publications](/publications) page.

{% include list.html collection=site.projects-separation title="" anchor-tag="separation" %}

<br>

## Generation
Audio generation leverages generative machine learning models (e.g., Variational Autoencoders or Generative Adversarial Networks) to create an audio waveform or a symbolic representation of audio (e.g., MIDI). This includes tasks such as music generation and text-to-speech (TTS). These generative models can be unconditioned (e.g., generating any kind of music without user input) or conditioned (e.g., generating jazz-rock played on a cello where the first eight bars are the same as Beethoven's Fifth Symphony). Conditional audio generation has the potential to enable novel tools for composers, dialogue editors for film and podcasts, and sound designers. For further publications in this area, see our [publications](/publications) page.

{% include list.html collection=site.projects-generation title="" anchor-tag="generation" %}

<br>

## Robustness
Neural network-based audio interfaces should be robust to various input distortions, especially in sensitive applications. We study the behavior of audio models under maliciously-crafted inputs - called _adversarial examples_ - in order to better understand how to secure audio interfaces against bad-faith actors and naturally-occurring distortions. For further publications in this area, see our [publications](/publications) page.

{% include list.html collection=site.projects-robustness title="" anchor-tag="robustness" %}

<br>

