---
layout: about
title: Home
permalink: /
selected_papers: false
social: false
announcements:
  enabled: false
latest_posts:
  enabled: false
---

<link rel="stylesheet" href="{{ '/assets/css/academic-profile.css' | relative_url }}">

<div class="profile-intro">
  <p>Hi, I am Xinhe Wang, currently a second-year master's student at Carnegie Mellon University, supervised by Prof. <a href="https://www.ri.cmu.edu/ri-faculty/katia-sycara/">Katia Sycara</a>. I enjoy building trustworthy(<a href="#data-attribution">Data Attribution</a>, <a href="#perception-bottlenecks">Perception Bottlenecks</a>, <a href="#intention-deception">Intention Deception</a>, <a href="#intention-verification">Intention Verification</a>) agents that can adapt(<a href="#code-augmented-planning">Code-Augmented Planning</a>, <a href="#imperfect-guidance">Beyond Blind Following</a>, <a href="#test-time-exploration">Test-Time Exploration</a>), evolve(<a href="#continual-policy-programming">Continual Policy Programming</a>) and safely collaborate(<a href="#cooperative-words">Action Ambiguity</a>) to accomplish real-world complex tasks. I have worked with Prof. <a href="https://yaqi-xie.me/">Yaqi Xie</a>, Prof. <a href="https://web.eecs.umich.edu/~honglak/index.html">Honglak Lee</a>, Prof. <a href="https://jiaqima.github.io/">Jiaqi Ma</a>, and Prof. <a href="https://tiiao.github.io/">Tianhao Wang</a>.</p>
</div>

<section class="academic-section" aria-labelledby="publications">
  <h2 id="publications">Selected Publications</h2>
  <ul class="publication-list">
    {% for paper in site.data.academic.publications %}
      <li>
        <span class="publication-venue">
          {{ paper.venue_label | escape }}
          {% if paper.venue_type %}<span class="publication-venue-type">{{ paper.venue_type | escape }}</span>{% endif %}
        </span>
        <div class="publication-details">
          <h3 id="{{ paper.id | escape }}">{{ paper.title | escape }}</h3>
          <p class="publication-authors">{{ paper.authors | escape | replace: 'Xinhe Wang', '<strong>Xinhe Wang</strong>' | replace: '*', '<sup>*</sup>' }}</p>
          {% if paper.authors contains "*" %}<p class="publication-meta">* Equal contribution</p>{% endif %}
          <p class="publication-meta publication-venue-detail">{{ paper.venue | escape }}</p>
          {% if paper.award %}<p class="publication-meta">{{ paper.award | escape }}</p>{% endif %}
          {% if paper.paper_url %}
            <a class="publication-html" href="{{ paper.paper_url | escape }}" aria-label="HTML: {{ paper.title | escape }}">HTML</a>
          {% endif %}
        </div>
      </li>
    {% endfor %}
  </ul>

  <h3 class="preprints-heading">Preprints</h3>
  <ul class="publication-list preprint-list">
    {% for paper in site.data.academic.preprints %}
      <li class="publication-details">
        <h4{% if paper.id %} id="{{ paper.id | escape }}"{% endif %}>{{ paper.title | escape }}</h4>
        <p class="publication-authors">{{ paper.authors | escape | replace: 'Xinhe Wang', '<strong>Xinhe Wang</strong>' | replace: '*', '<sup>*</sup>' }}</p>
        {% if paper.authors contains "*" %}<p class="publication-meta">* Equal contribution</p>{% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<section class="academic-section" aria-labelledby="misc">
  <h2 id="misc">Misc</h2>
  <p>My career goal is to build an agent similar to <a href="https://steins-gate.fandom.com/wiki/Amadeus_System">Amadeus</a>.</p>
</section>
