# Short-Text NLP Representation

A project page about text normalization, slang preservation, and vocabulary design for noisy short-text mental health classification.

## Project Website

[View Project Site](https://mah-trigui.github.io/short-text-nlp-representation/)

## Overview

This project classifies short free-text statements from Kenyan university students into four categories:
- Depression
- Alcohol
- Suicide
- Drugs

The main modeling risk was vocabulary fragmentation caused by:
- spelling mistakes
- slang
- abbreviations
- inconsistent surface forms

Instead of treating preprocessing as routine cleaning, the pipeline treated normalization as part of representation design.

## Core Idea

In sparse NLP pipelines, the same concept can fragment into multiple tokens if noisy text is not normalized before feature extraction.

At the same time, some domain-specific terms should be preserved rather than corrected away.

That creates a useful representation tradeoff:
- collapse recoverable noise
- preserve meaningful local vocabulary

## Architecture

![Architecture](images/architecture.jpg)

## Selected Implementation Elements

- UDPipe tokenization
- hunspell spelling correction
- slang preservation whitelist
- stemming after correction
- TF-IDF with sublinear scaling and L2 normalization
- unigram + bigram vocabulary
- LSA latent semantic features
- one-vs-rest modeling
- simple average ensemble across model families

## Key Takeaway

**In noisy short-text NLP, preprocessing is part of representation design.**

## Public Scope

This repository shares the project framing, selected code logic, and portfolio presentation only.
