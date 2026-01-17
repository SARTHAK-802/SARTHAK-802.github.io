---
layout: page
title: Repositories
permalink: /repositories/
nav: true
nav_order: 4
description:
body_class: page-repositories
---

<div class="repo-header">
  <h2 class="repo-title-big"> Featured Repositories</h2>

  <p class="repo-subtitle">
    A curated collection of my GitHub work in <span class="accent">Machine Learning</span> and <span class="accent">Computational Chemistry</span>.
  </p>

  <div class="repo-stats">
    <span class="repo-count-badge">
      <span id="repoCount">0</span> repositories featured
    </span>
  </div>
</div>

{% include repositories_custom.liquid %}

<script>
  // Dynamic Repo Counter (counts cards automatically)
  document.addEventListener("DOMContentLoaded", function () {
    const cards = document.querySelectorAll(".repo-card");
    const countEl = document.getElementById("repoCount");
    if (!countEl) return;

    let count = 0;
    const total = cards.length;

    const interval = setInterval(() => {
      count++;
      countEl.textContent = count;
      if (count >= total) clearInterval(interval);
    }, 60);
  });
</script>
