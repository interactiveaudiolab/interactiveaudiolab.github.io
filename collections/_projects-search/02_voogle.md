---
name: Voogle - Content-based audio search
creators: [Max Morrison, Fatemeh Pishdadian, Bongjun Kim, Prem Seetharaman, Brian Margolis, Madhav Ghei, Bryan Pardo]
external-url: https://github.com/interactiveaudiolab/voogle
external-url-text: Source Code
image: /assets/images/projects/voogle.png
altdescription: Voogle logo
funding: This work is supported National Science Foundation award 1617107
collection: projects
#put full content below the dashed line. full markdown is supported.
---

[Voogle](https://github.com/interactiveaudiolab/voogle) is an audio search engine that lets users search a database of sounds by vocally imitating or providing an example of the sound they are searching for.

Typical search engines for collections of audio either rely solely on matching filenames or keywords (e.g., [Freesound](https://freesound.org/)) or require a portion of the exact audio file in the database be used as the search example (e.g., Shazam). With Voogle, content-based search can be performed on any collection of audio files using a search example that is like, but not an exact copy, of any file in the collection (e.g. searching for dog barks with a recording of a dog bark). This is useful for anyone who needs to quickly retrieve specific sound effects (e.g., podcasters, video sound designers, and music producers).

While Voogle is domain-agnostic, incorporating domain-specific information can further improve performance. As an example, our paper [OtoMechanic: Auditory Automobile Diagnostics via Query-by-Example](/assets/papers/mm_bp_dcase_2019_cr.pdf) adapts Voogle to the domain of consumer vehicle diagnostics.

This work is part of a [collaboration with the University of Rochester AIR lab](http://www2.ece.rochester.edu/projects/air/projects/audiosearch).

### Related Publications

[[pdf]](/assets/papers/mm_bp_dcase_2019_cr.pdf) M. Morrison and B. Pardo, “OtoMechanic: Auditory Automobile Diagnostics via Query-by-Example,” in Proceedings of the 2019 Workshop on Detection and Classification of Acoustic Scenes and Events (DCASE2019), 2019.

[[pdf]](/assets/papers/pishdadian_kim_seetharaman_pardo_dcase2019.pdf) F. Pishdadian, P. Seetharaman, B. Kim, and B. Pardo, “Classifying Non-speech Vocals: Deep vs Signal Processing Representations,” in Proceedings of the 2019 Workshop on Detection and Classification of Acoustic Scenes and Events (DCASE2019), 2019.

[[pdf]](/assets/papers/DCASE2018Workshop_Margolis_130.pdf)
B. Margolis, M. Ghei, and B. Pardo, “Applying triplet loss to siamese-style networks for audio similarity ranking,” in Proceedings of the Detection and Classification of Acoustic Scenes and Events 2018 Workshop (DCASE2018), 2018, pp. 128–132.

[[pdf]](/assets/papers/DCASE2018_Kim.pdf)
B. Kim, M. Ghei, B. Pardo, and Z. Duan, “Vocal imitation set: a dataset of vocally imitated sound events using the audioset ontology,” in Proceedings of the 2018 Workshop on Detection and Classification of Acoustic Scenes and Events (DCASE2018), 2018.

[[pdf]](/assets/papers/zhang2018siamese.pdf) Y. Zhang, B. Pardo, and Z. Duan, “Siamese Style Convolutional Neural Networks for Sound Search by Vocal Imitation,” IEEE/ACM Transactions on Audio, Speech, and Language Processing, vol. 27, no. 2, pp. 429–441, 2018.
