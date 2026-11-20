---
layout: default
permalink: /cv/
title: CV
description: Curriculum vitae of Jongyun Hur.
---

{% assign profile = site.data.profile %}
<header class="page-heading cv-heading">
  <div>
    <h1>Curriculum Vitae</h1>
    <p>{{ site.title | escape }} · {{ profile.location | escape }}</p>
  </div>
  <a class="button button-primary" href="{{ profile.cv_pdf | relative_url }}">Open PDF</a>
</header>

<section class="profile-section" aria-labelledby="cv-education">
  <h2 id="cv-education">Education</h2>
  {% include profile-entries.liquid entries=profile.education %}
</section>

<section class="profile-section" aria-labelledby="cv-publications">
  <h2 id="cv-publications">Publications</h2>
  {% include profile-publications.liquid publications=profile.publications %}
</section>

<section class="profile-section" aria-labelledby="cv-experience">
  <h2 id="cv-experience">Experience</h2>
  {% include profile-entries.liquid entries=profile.experience %}
</section>

<section class="profile-section" aria-labelledby="cv-awards">
  <h2 id="cv-awards">Awards</h2>
  {% include profile-entries.liquid entries=profile.awards %}
</section>

<section class="profile-section" aria-labelledby="cv-skills">
  <h2 id="cv-skills">Skills &amp; credentials</h2>
  <dl class="skill-list">
    {% for skill in profile.skills %}
      <div>
        <dt>{{ skill.label | escape }}</dt>
        <dd>{{ skill.value | escape }}</dd>
      </div>
    {% endfor %}
  </dl>
</section>
