---
weight: 30
title: Conway's game of Life in Fully Homomorphic Encryption
description: Guide to FHE
date: 2025-09-03
type: post
---

## Context (Can skip this)
I had a chance to work on FHE related technology stuff for a year, I learnt a lot, ultimately I decided it wasn't the field I was fully interested in.

It is still a fascinating field, that has made remarkable progress over the years. As I haven't posted in a very long time, (read : 2 years), I decided, why not make a guide of sorts with everything I know and understand about the field. I am truly grateful for the time I spent on learning things related to this field. I shall definitely be revisiting it more in detail. 

This post will be mostly be about giving background information about Homomorphic Encryption.

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
Given, two messages $m_1$ and $m_2$ , an Encryption and Decryption function $E()$ and $D()$ respectively, we can




## WIP (keep myself accountable)