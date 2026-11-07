---
title: "Projects"
type: page
---

# Non AI Assisted Projects
## [TopBFT](https://github.com/thrypuro/top-BFT) 
Bryzatine Fault Tolerance scheme that uses Trusted Execution Environment (TEE). My implementation now uses the now broken Intel SGX library to implement both stuff in and outside the enclave. The Distributed system itself is very barebones.

## [puroboy](https://github.com/thrypuro/puro_boy_rs) 
A working z80 cpu implementation written in rust, meant to be a part of a full gameboy emulator. It uses SDL2 for graphics. It doesn't have sound and still needs a massive refactoring with being consistent with the design.


## [CTF challenges](https://github.com/thrypuro/my-ctf-challenges)
A collection of CTF challenges I made for my cybersecurity society while I was in University of Edinburgh.

## [Advent of Code 2025 in Fully Homomorphic Encryption](https://github.com/thrypuro/advent_of_code_FHE)
As a frequent enjoyer of Advent of Code puzzles and cryptography, I decided to test or benchmark how TFHE protocols could encode these puzzles. It's really slow, but the basic idea is that you could send an encrypted puzzle solution that the server will run and check against its encrypted answer, then return a Yes or a No. This was fun to play around with.

# AI Assisted Projects

## [Rooting my Hisense TV and installing Custom Software]
Can't provide the link to the full exploit chain or a public writeup; a lot of the initial idea was based on [this](https://github.com/carteakey/alvidaa). This was my real case of adapting frontier models like DeepSeek and Claude to do a whole lot of exploit development from a simple Read/Write primitive.

The reason for doing this was that I wanted Jellyfin on my TV but it didn't officially support it, and Plex didn't work. There was also too much ad content and bloat on the TV. My wifi was also a shared router, hence I wanted to install Tailscale on the TV to be able to keep it in my network to stream things.

I ported and compiled several apps like YouTube (with no ads and sponsorblock), Jellyfin, Seerr etc. I also made sure to block all the hosts that are related to serving ads. Had to create a lot of custom code to make it work on my TV in particular. Also made sure that there is persistence and that all of the stuff I am doing is undetected.

## [Self Hosting Stuff]
Turned an old gaming laptop and Raspberry Pi into self-hosting servers. Most of the services are hosted through Tailscale. It included stuff like the \*arr stack, Jellyfin server, Paperless, Home Assistant and a Jupyter notebook. My goal was also to make it reproducible, so that when I upgrade my server I can simply migrate. I am not a DevOps engineer by any means, so I had a lot of help from Claude with the reproducibility aspect of it. I knew what the right technologies were and how to set up the servers. The Ansible stuff is written through spec-driven development.
