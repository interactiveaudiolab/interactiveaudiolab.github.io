---
name: Audio adversarial examples with adaptive filtering
creators: [Patrick O'Reilly, Pranjal Awasthi, Aravindan Vijayaraghavan, Bryan Pardo]
external-url: "#examples"
external-url-text: Audio Examples
image: /assets/images/projects/filters.png
altdescription: Adaptive filtering
collection: projects
excerpt_separator: <!--end_excerpt-->
---
We demonstrate a novel audio-domain adversarial attack that modifies benign audio using an interpretable and differentiable parametric transformation - adaptive filtering. Unlike existing state-of-the-art attacks, our proposed method does not require a complex optimization procedure or generative model, relying only on a simple variant of gradient descent to tune filter parameters. <!--end_excerpt--> 

<br/>

### Background: Audio Interfaces are Vulnerable to Adversarial Examples

Deep neural networks achieve state-of-the-art performance on many audio tasks, including speaker verification, and as a result have been incorporated into voice-based systems for authentication and control in a wide variety of products. While deep networks are powerful classifiers, they are known to be vulnerable to adversarial examples, artificially-generated perturbations of natural instances that cause a network to make incorrect predictions. This vulnerability presents an opportunity for malicious actors to gain access to and influence the behavior of various products by surreptitiously passing adversarially-crafted audio to the underlying neural network systems. The research community has developed a number of audio-domain adversarial attacks to evaluate the robustness of deep neural networks across a variety of tasks, and we continue this work here. 

<br/>

### Attacking with Adaptive Filtering
Rather than optimize an additive waveform perturbation of a benign recording, as is typical, we optimize the parameters of an adaptive filter in the form of a time-varying frequency-domain transfer function. We then apply our filter to benign audio frame-by-frame to produce adversarial examples.

<p style="text-align:center;">
<img src="/demos/images/adaptive_filter/filter_process_1.png"
width="80%"
height="100%">
<br/>
<img src="/demos/images/adaptive_filter/filter_process_2.png"
width="80%"
height="100%">
</p>

Above, for each audio frame we adversarially parameterize a sparsely-sampled frequency-domain transfer function (<b>1</b>). After scaling (<b>2</b>), we convert each transfer function to a time-domain impulse response via the IDFT and apply a Hann window (<b>3</b>). We then take the DFT to obtain a smoothed, interpolated transfer function (<b>4</b>) which can be applied to a frame of audio input (<b>5</b>) via element-wise multiplication in the Fourier domain (<b>6</b>, <b>7</b>). Finally, we combine the filtered frames in the time domain via overlap-add (<b>8</b>) to obtain our adversarially-filtered audio.

<br/>

### Attacking in Realistic Settings

In order to craft attacks that work well in real-world playback scenarios ("over-the-air"), we can optimize through simulated distortions that mimic the properties of acoustic environments (e.g. reverb, noise, time-domain offset).
<br/><br/>
<p style="text-align:center;">
<img src="/demos/images/adaptive_filter/system_diagram.png"
width="80%"
height="100%">
</p>

Over-the-air attacks often require large-magnitude perturbations of the original audio in order to survive playback, and for typical waveform-additive attacks, this means noisy artifacts. We demonstrate the effectiveness of our filtering method by performing over-the-air attacks against a state-of-the-art speaker verification model, and show that our attack can match or exceed the perceptual quality of existing attacks when controlling for effectiveness. In a user study, listeners rate our attack as less conspicuous than a state-of-the-art additive frequency-masking attack by a ratio of 2-to-1. Our results demonstrate the potential of transformations beyond direct waveform addition for concealing high-magnitude adversarial perturbations, allowing adversaries to attack more effectively in challenging real-world settings.

<br/>

<h3 id="examples">Examples: Existing Methods Introduce Noise</h3>

Below, we provide examples of over-the-air attacks on a _speaker verification_ system. In this scenario, attacks modify a recording of the __source speaker__ to trick the system into recognizing the __target speaker__. The __baseline attack__ relies on a state-of-the-art frequency-masking loss and multi-stage optimization procedure, while __our attack__ sidesteps these requirements using adaptive filtering. Because both methods are relatively inconspicuous, _we recommend listening to these examples using headphones_.

 Because our proposed filter attack is multiplicative rather than additive, it does not introduce noise into silent regions of the waveform. In this example, listen to the end of each recording -- the baseline attack adds noise, while the proposed attack remains silent.

| Source Speaker | Target Speaker | Baseline Attack | Our Attack |
|:-:|:-:|:-:|:-:|
|  <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/reference_1.wav" type="audio/wav" preload="auto" /></audio>  |  <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/target_1.wav" type="audio/wav" preload="auto" /></audio>  | <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/baseline_1.wav" type="audio/wav" preload="auto" /></audio>  |  <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/proposed_1.wav" type="audio/wav" preload="auto" /></audio> |

<br/>

This noise is often audible throughout attacks generated with the baseline method, not just in silent regions:

| Source Speaker | Target Speaker | Baseline Attack | Our Attack |
|:-:|:-:|:-:|:-:|
| <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/reference_2.wav" type="audio/wav" preload="auto" /></audio> | <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/target_2.wav" type="audio/wav" preload="auto" /></audio> | <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/baseline_2.wav" type="audio/wav" preload="auto" /></audio> | <audio controls="" id="player" style="width:270px;"><source src="/demos/audio/adaptive_filter/main_run/proposed_2.wav" type="audio/wav" preload="auto" /></audio> |

<br/>
Audio for all attacks included in our over-the-air evaluation and perceptual study can be found [here](/demos/audio-adversarial-examples.html).

<br/>

### Related Publications
[P. O'Reilly, P. Awasthi, A. Vijayaraghavan, and B. Pardo, “Effective and Inconspicuous Over-the-Air Adversarial Examples with Adaptive Filtering,” 2021. Manuscript submitted for publication.](/assets/papers/oreilly_awasthi_vijayaraghavan_pardo_2021.pdf)

