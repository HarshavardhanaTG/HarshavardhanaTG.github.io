---
layout: page
title: Orofacial EMG
permalink: /orofacialEMG/
nav: false
---

## emg2speech

## **EMG-to-Speech pipeline overview (ALS subject, small language-corpora):**
---

A patient with amyotrophic lateral sclerosis (ALS) silently articulated a set of sentences while orofacial EMG was recorded. We convert these EMG signals into synthetic speech using the following pipeline:

1. Silent EMG Recording

The patient articulates sentences without producing audible sound. Only orofacial EMG is captured.

2. Reference Audio Generation

For each transcript, we generate clean reference audio using Google Text-to-Speech (TTS).

3. Discrete Speech Unit Extraction (HuBERT)

    We extract discrete HuBERT units from the reference audio.

    A neural model is trained to predict these HuBERT units directly from EMG.

5. Neural Vocoder Synthesis

A pretrained vocoder converts the predicted HuBERT unit sequences into intelligible audio.

The model is trained on 40 minutes of EMG data.

Note: The audio and video in the examples are not synchronized.
This is expected because EMG-to-speech generation operates on discrete HuBERT units trained with CTC loss, which do not preserve sample-accurate timing alignment.

---

### Samples

<div class="sample-card">
  <p class="big-transcript">“The cushion feels tight again.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/1.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/1a.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“The pillow feels tight today.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/2.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/2a.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“My shoulder feels softer tonight.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/3.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/3a.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“My wrist is calming now.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/4.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/4a.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“My chest feels sore again.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/5.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/5a.mp4" type="video/mp4">
  </video>
</div>

---

<style>
/* Card spacing + styling */
.sample-card {
  margin-bottom: 2.5rem;
  padding: 1.75rem;
  background: var(--card-bg, #1e1e1e);
  border-radius: 16px;
  box-shadow: 0 0 10px rgba(0,0,0,0.18);
}

/* Transcript styling */
.big-transcript {
  font-size: 1.7rem;      /* MUCH bigger */
  font-weight: 700;
  text-align: center;
  margin-bottom: 1.2rem;
  color: #ffffff;
}

/* Smaller audio & video */
.small-player {
  width: 55%;             /* decreased size */
  display: block;
  margin: 0.5rem auto 1.3rem auto;
  border-radius: 10px;
}

/* Titles removed for cleaner academic look */
</style>
