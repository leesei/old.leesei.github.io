---
title: Cryptography
categories:
  - crypto
tags:
  - cryptography
  - security
toc: true
date: 2016-01-21 01:02:09
---

[A Crash Course in Everything Cryptographic – Noteworthy - The Journal Blog](https://blog.usejournal.com/a-crash-course-in-everything-cryptographic-50daa0fda482) !important
[Crypto 101](https://www.crypto101.io/)

[Cryptography I | Coursera](https://www.coursera.org/learn/crypto)
[The Cryptopals Crypto Challenges](http://cryptopals.com/)

In cryptography, these entities are usually used:
- Alice, Bob, Charles, Douglas: authentic users
- Eve: eavesdropper
- Mallory: MITM attacker
- Satan: malicious user/hacker

## Algorithms

[Cryptographic nonce - Wikiwand](http://www.wikiwand.com/en/Cryptographic_nonce)

[cryptography - Do any security experts recommend bcrypt for password storage? - Information Security Stack Exchange](http://security.stackexchange.com/questions/4781/do-any-security-experts-recommend-bcrypt-for-password-storage)

[Computer and Network Security by Avi Kak](https://engineering.purdue.edu/kak/compsec/)

### Authenticity

[Message authentication code - Wikiwand](http://www.wikiwand.com/en/Message_authentication_code) MAC
[Hash-based message authentication code - Wikiwand](http://www.wikiwand.com/en/Hash-based_message_authentication_code) HMAC
[Moxie Marlinspike >> Blog >> The Cryptographic Doom Principle](http://www.thoughtcrime.org/blog/the-cryptographic-doom-principle/) Encrypt-then-MAC

Public Key Cryptography:  
Digital Signatures: encrypt a known data(nounce or message hash) with sender's private key 
Certificate Authorities: a trusted third party that will digitally sign and publish the public key bound to a user or entity

## Block Ciphers

[Lecture3 Lecture 3: Block Ciphers and the Data Encryption Standard](https://engineering.purdue.edu/kak/compsec/NewLectures/Lecture3.pdf)

### Modes of operation

[Block cipher mode of operation - Wikiwand](https://www.wikiwand.com/en/Block_cipher_mode_of_operation)

Block ciphers, as the name suggests, encrypts blocks. The methods of segmenting data into blocks is called "modes of operation".

**ECB**: simply divides a message into 16 byte blocks, preserves pattern
**CBC**: first block XORed with Initialisation Vector (IV), every other block XORed with the ciphertext of the block preceding it

### AES

[Lecture 8: AES: The Advanced Encryption Standard](https://engineering.purdue.edu/kak/compsec/NewLectures/Lecture8.pdf)
[Protect your TCP tunnel by implementing AES encryption with Python [Tutorial] | Packt Hub](https://hub.packtpub.com/protect-tcp-tunnel-implementing-aes-encryption-with-python/)

## Public Key Cryptography

[Public-key cryptography - Wikiwand](http://www.wikiwand.com/en/Public-key_cryptography)  
Public Key crypto simply works with numbers. This means that any messages would have to be converted into a number before being encrypted.

### RSA

[RSA (cryptosystem) - Wikiwand](https://www.wikiwand.com/en/RSA_(cryptosystem%29)
[How does RSA work? – Hacker Noon](https://hackernoon.com/how-does-rsa-work-f44918df914b)

## Attribute-Based Encryption

[A Gentle Introduction to Attribute-Based Encryption](https://medium.com/@dbkats/a-gentle-introduction-to-attribute-based-encryption-edca31744ac6)

## Enigma Machine

[Enigma machine - Wikiwand](https://www.wikiwand.com/en/Enigma_machine)
M1 and M3 have 3 rotor slots, M4 has 4 rotor slots.
Each rotor slot houses one of the eight *Rotors* (labeled in Roman numerals, the extra one for M4 labeled with Greek letters). The right *Rotor* steps each time a letter is typed. Each *Rotor* have notches at different positions to cause the *Rotor* on the left to step when itself done a full revolution, the middle rotor has optional "double stepping" which will also step itself when doing so. The starting *Rotor* position is called *Ground Settings*. The inner ring of each *Rotor* can be set to a different offset, this is the *Ring Settings*.
There are three choices of *Reflector* (A, B and C) that takes the input and feed it through the *Rotors* again.
There is also a *Plugboard* which will swap two letters before feeding into the *Fixed Rotar*.
The *Reflector* and *Rotors* selected, *Ground Settings*, *Ring Settings* and the *Plugboard* config have to be kept in sync when encoding and decoding the message. The setting is changed daily and the setting table will change monthly. The operator will send his own *Rotor* settings using the *Ground Settings* before each message.
Enigma machine is essentially a symmetric cryptography with the initial setup as key.

[How Enigma Machines Work](http://enigma.louisedade.co.uk/howitworks.html)
[TechStuff Ponders an Enigma | TechStuff Podcast](https://www.techstuffpodcast.com/podcasts/techstuff-ponders-an-enigma.htm)
[Further Reading about Enigma and Codebreaking](http://enigma.louisedade.co.uk/furtherreading.html)
[Cryptanalysis of the Enigma - Wikiwand](https://www.wikiwand.com/en/Cryptanalysis_of_the_Enigma)

[BBC - History - Enigma (pictures, video, facts & news)](http://www.bbc.co.uk/history/topics/enigma)
[Enigma History](http://www.cryptomuseum.com/crypto/enigma/hist.htm)
[The Inner Workings of an Enigma Machine - YouTube](https://www.youtube.com/watch?v=mcX7iO_XCFA)
[158,962,555,217,826,360,000 (Enigma Machine) - Numberphile - YouTube](https://www.youtube.com/watch?annotation_id=annotation_777706&feature=iv&src_vid=V4V2bpZlqx8&v=G2_Q9FoD-oQ)
[Flaw in the Enigma Code - Numberphile - YouTube](https://www.youtube.com/watch?v=V4V2bpZlqx8)
[Turing's Enigma Problem (Part 1) - Computerphile - YouTube](https://www.youtube.com/watch?v=d2NWPG2gB_A)
[Tackling Enigma (Turing's Enigma Problem Part 2) - Computerphile - YouTube](https://www.youtube.com/watch?v=kj_7Jc1mS9k)

[How 2,000 Droplets Broke the Enigma Code in 13 Minutes](https://blog.digitalocean.com/how-2000-droplets-broke-the-enigma-code-in-13-minutes/)
[How we cracked the Enigma code using Artificial Intelligence | Lukasz Kuncewicz | Pulse | LinkedIn](https://www.linkedin.com/pulse/how-we-cracked-enigma-code-using-artificial-lukasz-kuncewicz/)
[Cracking the world famous Enigma Machine with artificial intelligence in just 13 minutes - BT](http://home.bt.com/tech-gadgets/enigma-machine-cracking-artificial-intelligence-11364235568160)

### Emulator

[Enigma Machine Emulator](http://enigma.louisedade.co.uk/)
[Emulator Help](http://enigma.louisedade.co.uk/help.html) How the emulator worked
[JavaScript Source Code for the Enigma Machine](http://enigma.louisedade.co.uk/jssource.html)

[Enigma Simulation in Javascript/HTML](http://people.physik.hu-berlin.de/~palloks/js/enigma/index_en.html) also lots of info

[The Enigma machine: Encrypt and decrypt online — Cryptii](https://cryptii.com/enigma-machine)
[Enigma decoder: Decrypt and translate enigma online — Cryptii](https://cryptii.com/enigma-decoder)

### DIY

[OctaPi: brute-force Enigma - Introduction | Raspberry Pi Projects](https://projects.raspberrypi.org/en/projects/octapi-brute-force-enigma/)
[Put an Arduino Enigma in Your Pocket | Hackaday](https://hackaday.com/2019/03/28/put-an-arduino-enigma-in-your-pocket/)
[Building an Enigma – Skippy's Random Ramblings](https://skippy.org.uk/building-an-enigma/)
[Enigma-E](https://www.cryptomuseum.com/kits/enigma/)
