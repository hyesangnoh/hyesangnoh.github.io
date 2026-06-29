```html
---
layout: page
permalink: /teaching/
title: Teaching
nav: true
nav_order: 4
---

<style>
.post-title,
.page-title,
h1 {
  display: none !important;
}

.teaching-layout {
  display: grid;
  grid-template-columns: 170px minmax(0, 1fr);
  column-gap: 2.5rem;
  align-items: start;
}

.teaching-sidebar {
  position: sticky;
  top: 5rem;
  font-size: 0.95rem;
  line-height: 1.8;
}

.teaching-sidebar a {
  display: block;
  color: var(--global-text-color-light);
  text-decoration: none;
  transition: color 0.15s ease;
}

.teaching-sidebar a:hover,
.teaching-sidebar a.active {
  color: var(--global-theme-color);
}

.teaching-content {
  font-size: 1rem;
  line-height: 1.6;
}

.teaching-content h2 {
  font-size: 1.15rem;
  font-weight: 700;
  line-height: 1.35;
  margin-top: 2.2rem;
  margin-bottom: 0.9rem;
  scroll-margin-top: 5rem;
}

.teaching-list {
  list-style: none;
  padding-left: 0;
  margin-top: 0;
}

.teaching-list li {
  margin-bottom: 0.75rem;
}

.course-title {
  font-weight: 400;
}

.course-info {
  color: var(--global-text-color);
}

@media (max-width: 768px) {
  .teaching-layout {
    display: block;
  }

  .teaching-sidebar {
    position: static;
    margin-bottom: 1.5rem;
    border-bottom: 1px solid var(--global-divider-color);
    padding-bottom: 0.75rem;
  }

  .teaching-sidebar a {
    display: inline-block;
    margin-right: 1rem;
  }
}
</style>


<div class="teaching-layout">

<nav class="teaching-sidebar">
  <a href="#instructor">Instructor</a>
  <a href="#teaching-assistant">Teaching Assistant</a>
  <a href="#guest-lectures">Guest Lectures</a>
</nav>

<div class="teaching-content">

<h2 id="instructor">Instructor</h2>

<ul class="teaching-list">
  <li>
    <span class="course-title">Course Title</span>. University at Albany, Semester Year.
  </li>
</ul>


<h2 id="teaching-assistant">Teaching Assistant</h2>

<ul class="teaching-list">
  <li>
    <span class="course-title">Course Title</span>. University at Albany, Semester Year.
  </li>

  <li>
    <span class="course-title">Course Title</span>. University at Albany, Semester Year.
  </li>
</ul>


<h2 id="guest-lectures">Guest Lectures</h2>

<ul class="teaching-list">
  <li>
    <span class="course-title">Lecture Title</span>. Course Title, University at Albany, Semester Year.
  </li>
</ul>

</div>

</div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const sections = document.querySelectorAll(".teaching-content h2[id]");
  const navLinks = document.querySelectorAll(".teaching-sidebar a");

  function setActiveLink() {
    let currentSectionId = sections[0]?.id;

    sections.forEach((section) => {
      const rect = section.getBoundingClientRect();

      if (rect.top <= 140) {
        currentSectionId = section.id;
      }
    });

    const nearBottom =
      window.innerHeight + window.scrollY >= document.body.offsetHeight - 20;

    if (nearBottom && sections.length > 0) {
      currentSectionId = sections[sections.length - 1].id;
    }

    navLinks.forEach((link) => {
      const href = link.getAttribute("href");

      if (href === `#${currentSectionId}`) {
        link.classList.add("active");
      } else {
        link.classList.remove("active");
      }
    });
  }

  setActiveLink();
  window.addEventListener("scroll", setActiveLink);
});
</script>
```
