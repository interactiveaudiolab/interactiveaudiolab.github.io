---
name: Music Audio Generation
creators: [Hugo Flores Garcia, Prem Seetharaman, Bryan Pardo]
image: /assets/images/projects/vampnet.png
altdescription: System description
collection: projects
#put full content below the dashed line. full markdown is supported.
---
We introduce VampNet, a masked acoustic token modeling approach to music synthesis, compression, inpainting, and variation.  VampNet uses a variable masking schedule during training which allows us to sample coherent music from the model by applying a variety of masking approaches (called prompts) during inference. VampNet is non-autoregressive, leveraging a bidirectional transformer architecture that attends to all tokens in a forward pass. With just 36 sampling passes, VampNet can generate coherent high-fidelity musical waveforms. We show that by prompting VampNet in various ways, we can apply it to tasks like music compression, inpainting, outpainting, continuation, and looping with variation (vamping). Appropriately prompted, VampNet is capable of maintaining style, genre, instrumentation, and other high-level aspects of the music. This flexible prompting capability makes VampNet a powerful music co-creation tool. 

### Examples
We encourage listening to our [audio samples](https://tinyurl.com/bdfj7rdx)
### Sourcecode
Find the code [here](https://github.com/hugofloresgarcia/vampnet)



### Related publications

[[pdf]](/assets/papers/Liu2020-MLMD.pdf) A. Liu, A. Fang, G. Hadjeres, P. Seetharaman, and B. Pardo, “Incorporating Music Knowledge in Continual Dataset Augmentation for Music Generation,” in Machine Learning for Media Discovery Workshop at the 37th International Conference on Machine Learning (ICML), 2020.

[[pdf]](/assets/papers/Fang2020-MLMD.pdf) A. Fang, A. Liu, P. Seetharaman, and B. Pardo, “Bach or Mock? A Grading Function for Chorales in the Style of J.S. Bach,” in Machine Learning for Media Discovery Workshop at the 37th International Conference on Machine Learning (ICML), 2020.
