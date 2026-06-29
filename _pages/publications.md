---
layout: page
permalink: /research/
title: Research
nav: true
nav_order: 3
---

<style>
.post-title,
.page-title,
h1 {
  display: none !important;
}

.research-layout {
  display: grid;
  grid-template-columns: 170px minmax(0, 1fr);
  column-gap: 2.5rem;
  align-items: start;
}

.research-sidebar {
  position: sticky;
  top: 5rem;
  font-size: 0.95rem;
  line-height: 1.8;
}

.research-sidebar a {
  display: block;
  color: var(--global-text-color-light);
  text-decoration: none;
  transition: color 0.15s ease;
}

.research-sidebar a:hover,
.research-sidebar a.active {
  color: var(--global-theme-color);
}

.research-content {
  font-size: 1rem;
  line-height: 1.6;
}

.research-content h2 {
  font-size: 1.15rem;
  font-weight: 700;
  line-height: 1.35;
  margin-top: 2.2rem;
  margin-bottom: 0.9rem;
  scroll-margin-top: 5rem;
}

.publication-list {
  list-style: none;
  padding-left: 0;
  margin-top: 0;
}

.publication-list li {
  margin-bottom: 0.75rem;
}

.pub-title,
.pub-authors,
.pub-venue,
.pub-links,
.pub-abstract {
  font-size: 1rem;
  line-height: 1.6;
  color: var(--global-text-color);
}

.pub-title {
  font-weight: 400;
}

.pub-authors,
.pub-venue {
  margin-top: 0;
}

.pub-links {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  align-items: baseline;
  margin-top: 0.15rem;
}

.abs-toggle {
  padding: 0;
  border: 0;
  background: none;
  color: var(--global-theme-color);
  font: inherit;
  cursor: pointer;
}

.abs-toggle:hover {
  text-decoration: underline;
}

.pub-links a {
  margin-left: 0;
}

.pub-abstract {
  display: none;
  flex-basis: 100%;
  width: 100%;
  margin-top: 0.5rem;
}

.pub-abstract.open {
  display: block;
}

@media (max-width: 768px) {
  .research-layout {
    display: block;
  }

  .research-sidebar {
    position: static;
    margin-bottom: 1.5rem;
    border-bottom: 1px solid var(--global-divider-color);
    padding-bottom: 0.75rem;
  }

  .research-sidebar a {
    display: inline-block;
    margin-right: 1rem;
  }
}
</style>


<nav class="research-sidebar">
  <a href="#peer-reviewed-articles">Peer-Reviewed Articles</a>
  <a href="#manuscript-under-review">Manuscript Under Review</a>
  <a href="#work-in-progress">Work in Progress</a>
  <a href="#policy-reports">Policy Reports</a>
</nav>


<div class="research-content">

<h2 id="peer-reviewed-articles">Peer-Reviewed Journal Articles</h2>

<ul class="publication-list">
  <li>
    <strong><em>Noh, H.</em></strong>, &amp; Fox, A. M. (2026). Can money buy trust? Social transfer and trust during the pandemic. <em>Policy Studies Journal</em>, Article e70112. Advance online publication.
  </li>

  <li>
    Choi, Y., <strong><em>Noh, H.</em></strong>, Han, S., &amp; Gentilini, U. (2024). Diversity within universality: Explaining pandemic universal cash transfer in East Asia. <em>International Social Security Review, 77</em>(1–2), 51–66.
  </li>

  <li>
    <strong><em>Noh, H.</em></strong>, Han, S., &amp; Choi, Y. (2022). Who spends more to combat COVID-19 social risks and why? <em>International Journal of Social Welfare, 31</em>(4), 392–406.
  </li>
</ul>

<h2 id="manuscript-under-review">Manuscript Under Review</h2>

<ul class="publication-list">
  <li>
    Fox, A. M., &amp; <strong><em>Noh, H.</em></strong>. “Universal” health coverage: Does inclusion of divisive groups reduce support for universalistic welfare policy? (Revise and resubmit at <em>Journal of Public Policy</em>).
  </li>

  <li>
    Lyon, M. A., Finger, L. K., &amp; <strong><em>Noh, H.</em></strong>. Teacher strikes and the demobilization of Republican voters. (Revise and resubmit at <em>Political Behavior</em>).
  </li>

  <li>
    Reynolds, M. M., <strong><em>Noh, H.</em></strong>, &amp; Riosmena, F. County co-ethnic concentration, state immigration policies, and Hispanic/Latino health. (Revise and resubmit at <em>Population Research and Policy Review</em>).
  </li>
</ul>

<h2 id="work-in-progress">Work in Progress</h2>

<ul class="publication-list">
  <li>
    Voice and power in public charge rulemaking process. (Dissertation chapter)
  </li>

  <li>
    Who deserves easier access: Deservingness, fiscal constraints, and administrative burden for immigrants, with Fox, A. M. (Dissertation chapter)
  </li>

  <li>
    How attitudes toward different welfare policies are shaped and evolve. (Dissertation chapter)
  </li>

  <li>
    State-level public opinion about immigrants and the 2016 presidential election, with Reynolds, M. M., &amp; Prince, K.
  </li>

  <li>
    Let them eat pets: Scapegoating and support for restrictive migration policies, with Fox, A. M.
  </li>

  <li>
    How teacher strikes affect school board elections: Evidence from two states, with Lyon, M. A., Shepardson, A., Finger, L. K., &amp; Bleiberg, J.
  </li>
</ul>

<h2 id="policy-reports">Policy Reports</h2>

<ul class="publication-list">
  <li>
    Hwang, H., Han, S., <strong><em>Noh, H.</em></strong>, Kim, I., Jang, M., &amp; Kim, H. (2021). <em>A regional approach to reducing vulnerability to emerging infectious diseases: Vulnerability assessment and smart response policies</em>. The Korea Institute of Public Administration. (In Korean)
  </li>

  <li>
    Choi, Y., Choi, J., Kim, J., Cho, W., <strong><em>Noh, H.</em></strong>, &amp; Han, S. (2020). <em>Social risks and COVID-19: Cross-national social policy responses</em>. Ministry of Health and Welfare, Yonsei University. (In Korean)
  </li>
</ul>

</div>



<script>
document.addEventListener("DOMContentLoaded", function () {
  const sections = document.querySelectorAll(".research-content h2[id]");
  const navLinks = document.querySelectorAll(".research-sidebar a");
  const absButtons = document.querySelectorAll(".abs-toggle");

  absButtons.forEach((button) => {
    button.addEventListener("click", function () {
      const abstract = button.parentElement.querySelector(".pub-abstract");

      if (abstract) {
        abstract.classList.toggle("open");
      }
    });
  });

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

