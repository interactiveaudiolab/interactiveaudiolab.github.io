---
name: VampNet - Music Generation via Masked Acoustic Token Modeling
creators: [Hugo Flores Garcia, Prem Seetharaman, Rithesh Kumar,  Bryan Pardo]
image: /assets/images/projects/vampnet.png
altdescription: System description
funding: This work supported by NSF Award Number 2222369
collection: projects

#put full content below the dashed line. full markdown is supported.
---
We introduce VampNet, a masked acoustic token modeling approach to music audio generation. VampNet lets us sample coherent music from the model by applying a variety of masking approaches (called prompts) during inference.  Prompting VampNet appropriately, enables music compression, inpainting, outpainting, continuation, and looping with variation (vamping). This makes VampNet a powerful music co-creation tool. 

VampNet is non-autoregressive, leveraging a bidirectional transformer architecture that attends to all tokens in a forward pass. With just 36 sampling passes (compared to hundreds in the autoregressive approach), VampNet  generates coherent high-fidelity musical waveforms. For more, try [the demo](https://huggingface.co/spaces/descript/vampnet) listen to our [audio examples](https://tinyurl.com/bdfj7rdx), read [the paper](/assets/papers/ismir2023-flores-seetharaman-pardo.pdf), peruse [the sourcecode](https://github.com/hugofloresgarcia/vampnet), or just watch the video.

<iframe width="560" height="315" src="https://www.youtube.com/embed/3XfeWlV9Cp0?si=IZTVX-e6ER_H6kXq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### [Demo](https://huggingface.co/spaces/descript/vampnet) [Audio](https://tinyurl.com/bdfj7rdx) [Sourcecode](https://github.com/hugofloresgarcia/vampnet)

### Related publications
[**[pdf]**](/assets/papers/ismir2023-flores-seetharaman-pardo.pdf) H. Flores, P.  P. Seetharaman, R. Kumar, and B. Pardo, “VampNet: Music Generation via Masked Acoustic Token Modeling,” International Society of the Society of Music Information Retrieval (ISMIR), 2023.


