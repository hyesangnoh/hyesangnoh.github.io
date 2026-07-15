---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 5
description:
---

<style>
  .post-title,
  .page-title,
  h1 {
    display: none !important;
  }

  .cv-frame {
    width: 85%;
    margin: 0 auto;
  }

  .cv-updated {
    font-size: 0.9rem;
    margin-top: 0;
    margin-bottom: 1rem;
    text-align: center;
  }
</style>

<p class="cv-updated">
  Updated June 2026
</p>

<div class="cv-frame">
  <object
    data="{{ '/assets/pdf/cv.pdf' | relative_url }}"
    type="application/pdf"
    width="100%"
    height="850px">
    <p>
      <a href="{{ '/assets/pdf/cv.pdf' | relative_url }}">
        View my CV
      </a>
    </p>
  </object>
</div>
