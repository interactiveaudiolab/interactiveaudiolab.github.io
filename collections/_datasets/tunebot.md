---
name: Tunebot
creators: [Mark Cartwright, Arefin Huq, Jinyu Han, Zafar Rafii, Bryan Pardo]
external-url: http://goo.gl/VgwRz1
external-url-text: Tunebot
image: /assets/images/datasets/tunebot.png
altdescription: vocal imitation of a sound
navigation: resources

#put full description of the project/demo below the dashed line. full markdown is supported.
---

The Tunebot project is an online 
[Query By Humming](http://en.wikipedia.org/wiki/Query_by_humming) system. 
As of Sept 25, 2014 Tunebot has had 296,472 site visitors. Users sing a song to Tunebot 
and it returns a ranked list of song candidates available on Apple's iTunes website. 
The database that Tunebot compares to sung queries is crowdsourced from users as well. 
Users contribute new songs to Tunebot by singing them on the Tunebot website. The more 
songs people contribute, the better Tunebot works. Tunebot is no longer online
but the dataset lives on. 


### What is the Tunebot Dataset?

The dataset is a collection of 10,000 sung contributions to the Tunebot search engine. 
Each contribution is a recording of a contributor singing a song to Tunebot. In addition
to the 10,000 contributions, there is an associated Google spreadsheet to 
look up the artist, album, and song for any file. There are four columns in
the spreadsheet: 

- filepath:The filepath and filename of an audio file containing a single contribution
that someone sang to Tunebot.
- song: The name of the song that the contributor sang.
- album: The name of the album this song is a part of.
- artist: The recording artist associated with the album. *NOTE* this is NOT the name
of the person who contributed the sung example. The names and IP addresses of contributors
are not stored by Tunebot.

### What is the Tunebot Dataset good for?

Historically, query by humming researchers, in particular, have built and tested their algorithms using 
much smaller sets of sung examples (on the order of 1000 examples) that were not generated
in the context of an actual working search engine available on the web. The Tunebot 
Dataset provides 10,000  real-world sung examples from contributors to an online and 
working music search engine. Testing a system  on this  data should give a much more accurate
indication of real-world performance than has been possible with existing datasets.

### How can I get the Tunebot Dataset?

Get access to the Tunebot data by giving us your email and a short description of how 
you'd like to use the data [here](http://goo.gl/VgwRz1).




### Related publications

[[pdf]](/assets/papers/smc2010-huq-cartwright-pardo.pdf)
A. Huq, M. Cartwright and B. Pardo, “Crowdsourcing a Real-world On-line Query by Humming System,” 
Proceedings of the 7th Sound and Music Computing Conference (SMC 2010),  Barcelona, Spain, July 21-24, 2010

[[pdf]](/assets/papers/CartwrightPardo_SMC2012.pdf) 
M. Cartwright and B. Pardo, “Building a Music Search Database Using Human Computation,
” Proceedings of the 9th Sound and Music Computing Conference (SMC 2012),  
Copenhagen, Denmark, July 12-14, 2012

[[pdf]](/assets/papers/cartwright_etal_humancomp11.pdf) 
M. B. Cartwright, Z. Rafii, J. Han, and B. Pardo, 
“Making searchable melodies: Human versus machine,” 
in Workshops at the Twenty-Fifth AAAI Conference on Artificial Intelligence, 2011.

