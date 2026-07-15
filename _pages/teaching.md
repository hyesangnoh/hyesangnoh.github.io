---
layout: page
permalink: /teaching/
title: Teaching
description:
nav: true
nav_order: 4
---

<style>
.post-title,
.page-title,
h1 {
  display: none !important;
}

.teaching-list {
  list-style: none;
  padding-left: 0;
  margin-top: 0;
}

.teaching-list li {
  margin-bottom: 0.75rem;
}

.course-title,
.course-role,
.course-meta {
  font-size: 1rem;
  line-height: 1.6;
  color: var(--global-text-color);
}

.course-title {
  font-weight: 400;
}

.course-role,
.course-meta {
  margin-top: 0;
}

.teaching-section {
  margin-top: 2.2rem;
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
    <a href="#guest-lecturer">Guest Lecturer</a>
    <a href="#teaching-assistant">Teaching Assistant</a>
  </nav>

  <div class="teaching-content">
    <h2 id="guest-lecturer">Guest Lecturer</h2>

    <ul class="teaching-list">
      <li>
        <div class="course-title">Introduction to Public Policy</div>
        <div class="course-role">Guest Lecturer ("Poverty and Social Welfare Policy")</div>
        <div class="course-meta">University at Albany, Fall 2025</div>
      </li>
    </ul>

    <h2 id="teaching-assistant" class="teaching-section">Teaching Assistant</h2>

    <ul class="teaching-list">
      <li>
        <div class="course-title">Introduction to Public Policy</div>
        <div class="course-role">Discussion Section Leader/Teaching Assistant</div>
        <div class="course-meta">University at Albany, Fall 2024/Spring 2025</div>
        <div class="course-description">Duties included leading 2–3 weekly discussion sections of 15 students each; guiding students in writing policy memos; grading assignments; and advising student teams on presentations </div>
      </li>

      <li>
        <div class="course-title">Modern Society and Public Administration</div>
        <div class="course-role">Teaching Assistant</div>
        <div class="course-meta">Yonsei University, Fall 2019/Fall 2020</div>
        <div class="course-description">Duties included communicating with students about course-related issues; proctoring exams; and organizing class materials </div>
      </li>

      <li>
        <div class="course-title">Comparative Public Policy</div>
        <div class="course-role">Teaching Assistant</div>
        <div class="course-meta">Yonsei University, Spring 2019/Spring 2020</div>
        <div class="course-description">Duties included communicating with students about course-related issues; proctoring exams; and organizing class materials </div>
      </li>
    </ul>
  </div>
</div>



<script>
document.addEventListener("DOMContentLoaded", function () {
  const sections = document.querySelectorAll(".teaching-content h2[id]");
  const navLinks = document.querySelectorAll(".teaching-sidebar a");

  function updateActiveSection() {
    let currentSection = "";

    sections.forEach((section) => {
      const sectionTop = section.offsetTop - 120;

      if (window.scrollY >= sectionTop) {
        currentSection = section.getAttribute("id");
      }
    });

    navLinks.forEach((link) => {
      link.classList.remove("active");

      if (link.getAttribute("href") === "#" + currentSection) {
        link.classList.add("active");
      }
    });
  }

  window.addEventListener("scroll", updateActiveSection);
  updateActiveSection();
});
</script>
