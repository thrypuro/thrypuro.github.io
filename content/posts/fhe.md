---
weight: 30
title: Transciphering in Fully Homomorphic Encryption
description: Guide to FHE
date: 2025-09-03
type: post
---
## Context (Can skip this)
I had a chance to work on FHE related technology stuff for a year, I learnt a lot, ultimately I decided it wasn't the field I was fully interested in.

It is still a fascinating field, that has made remarkable progress over the years. As I haven't posted in a very long time, (read : 2 years), I decided, why not make a guide of sorts with everything I know and understand about the field. I am truly grateful for the time I spent on learning things related to this field. I shall definitely be revisiting it more in detail. 

This post will be mostly be about giving background information about Homomorphic Encryption. 

I wanted to have it written out what I've learnt over the year within the field, as I did learn a lot. I want to keep doing projects on the side. 

## Background

Homomorphic Encryption is a form of encryption that lets you do computation in the encrypted space. It shares similarity to a textbook group theory concept known as Homomorphism. 

The first kind of homomorphic encryption that was discovered was Partially Homomorphic Encryption, an example of this scheme is Pallier Cryptosystem.

The topic of our interest is the Fully Homomorphic Encryption. In this, the desirable property that we would like is the following, 
$$
D(E(m_1) \ + \ E(m_2)) = m_1 + m_2 
$$
$$
D(E(m_1) \ * \ E(m_2)) = m_1 \ * \ m_2
$$
Given, two messages $m_1$ and $m_2$ , an Encryption and Decryption function $E()$ and $D()$ respectively, we can compute the addition and multiplication of the message in the Encrypted space without decrypting the message itself to do the operation. 

FHE schemes these days are based on the LWE (Learning with Errors) scheme, which is based on the Lattice Based Cryptography.  The basic LWE scheme we use is as follows :
$$
c = (\vec{a}\cdot \vec{s} + \Delta\cdot m + e)\mod{q}
$$
Here,  $\vec{a}$  is the public key,  $\vec{s}$ is the secret vector, $\Delta$ is the scaling factor, $m$ is the message, $e$ is the error added to the message, $q$ is the modulo of the scheme. 

Without the error, this function would be linear. If we were be able to collect enough samples of $c$ , we can invert the matrix and recover the message. Hence, the error is added to prevent this and plays a vital role in the encryption of the scheme. 

The scheme while it is simple has decades of studying done, and like with every cryptography schemes the parameters needs to be picked carefully, as there are several well known attacks that like [LLL](https://en.wikipedia.org/wiki/Lenstra%E2%80%93Lenstra%E2%80%93Lov%C3%A1sz_lattice_basis_reduction_algorithm), if certain conditions are met like enough samples, modulo choice and error, this algorithm can basically recover the secret vector. 

## Transciphering 

The concept of transciphering is wacky but simple. If we can run arbitrary functions in FHE in the encrypted space, can we then perhaps run a asymmetric key encryption algorithm inside this space. 

We could get a sort of composable encryption. Where there encryption done on the function creating Look Up Tables and Programmable Bootstrapping. 

Why is this a property that could be desirable? 


## What will we be implementing?
We will implement this simple asymmetric key algorithm in TFHE-rs known [LowMC](https://eprint.iacr.org/2016/687.pdf) . We will also for the fun of it also implement some other simple ciphers in TFHErs like caesar's cipher. 


## What is happening behind the scenes?



## WIP (keep myself accountable)