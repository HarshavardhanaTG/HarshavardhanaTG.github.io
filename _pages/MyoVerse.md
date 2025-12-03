---
layout: page
title: MyoVerse
permalink: /MyoVerse/
nav: true
nav_order: 1

---

<style>
.grid-2 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
  margin-top: 2rem;
}

.grid-card {
  background: var(--card-bg, #1e1e1e);
  border-radius: 12px;
  padding: 24px;
  text-align: center;
  transition: all 0.2s ease;
  box-shadow: 0 0 8px rgba(0,0,0,0.15);
}

.grid-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 6px 20px rgba(0,0,0,0.20);
}

.grid-card img {
  width: 160px;
  height: 150px;
  margin-bottom: 16px;
}
</style>

## A unified platform for ELECTROMYOGRAPHY (EMG) datasets, models, and research tools.

<div class="grid-2">

  <a href="/upperlimbEMG/" class="grid-card">
    <img src="/assets/icons/upperlimb.png" alt="Upperlimb EMG icon">
    <h3>Upperlimb EMG</h3>
    <p>Wrist and hand EMG datasets with processing pipelines.</p>
  </a>

  <a href="/orofacialEMG/" class="grid-card">
    <img src="/assets/icons/orofacial.png" alt="Orofacial EMG icon">
    <h3>Orofacial EMG</h3>
    <p>Orofacial EMG with processing pipelines.</p>
  </a>

</div>
