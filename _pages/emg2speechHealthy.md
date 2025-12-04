---
layout: page
title: emg2speech demo
permalink: /emg2speechHealthy/
nav: false
---

**EMG-to-Speech pipeline overview** --- (healthy subject, general language-corpora):


A healthy subject articulated a set of sentences while orofacial EMG was recorded. We convert these EMG signals into synthetic speech using the following pipeline:

1. EMG Recording

    The subject articulates sentences naturally. Only orofacial EMG is captured.

2. Reference Audio Generation

    For each transcript, we generate clean reference audio using Google Text-to-Speech (TTS).

3. Discrete Speech Unit Extraction (HuBERT)

    We extract discrete HuBERT units from the reference audio.

    A neural model is trained to predict these HuBERT units directly from EMG.

5. Neural Vocoder Synthesis

    A pretrained vocoder converts the predicted HuBERT unit sequences into intelligible audio.

The model is trained on nearly 8 hours of EMG data. The language corpora consists of around 6500 unique words and 10000 sentences.

Note: The audio and video in the examples are not synchronized.
This is expected because EMG-to-speech generation operates on discrete HuBERT units trained with CTC loss, which do not preserve sample-accurate timing alignment.
We never make use of any audio or visual cues from the subject. We only use EMG, and directly convert EMG-to-audio.

---

### Samples

<div class="sample-card">
  <p class="big-transcript">“The cushion feels tight again.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/1B.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/1Ba.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“The pillow feels tight today.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/2B.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/2Ba.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“My shoulder feels softer tonight.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/3B.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/3Ba.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“My wrist is calming now.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/4B.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/4Ba.mp4" type="video/mp4">
  </video>
</div>


<div class="sample-card">
  <p class="big-transcript">“My chest feels sore again.”</p>

  <audio controls class="small-player">
    <source src="/assets/audio/orofacial/5B.wav" type="audio/wav">
  </audio>

  <video controls class="small-player">
    <source src="/assets/audio/orofacial/5Ba.mp4" type="video/mp4">
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
