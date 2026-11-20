---
layout: default
title: About
permalink: /
nav: true
nav_order: 1
---

{% assign profile = site.data.profile %}
<header class="about-header">
  <h1>{{ page.title | escape }}</h1>
  <div class="profile-overview">
    <div>
      <p class="profile-name">{{ site.title | escape }}</p>
      <p class="profile-location">{{ profile.location | escape }}</p>
      <div class="profile-contact">
        <a href="mailto:{{ profile.email }}">{{ profile.email | escape }}</a>
        <a href="mailto:{{ profile.university_email }}">{{ profile.university_email | escape }}</a>
        <a href="{{ profile.linkedin }}">LinkedIn</a>
      </div>
    </div>
    <picture>
      <source type="image/webp" srcset="{{ '/assets/img/jongyun-hur-portrait-480.webp' | relative_url }} 480w, {{ '/assets/img/jongyun-hur-portrait-800.webp' | relative_url }} 800w" sizes="(max-width: 40rem) 6rem, 9.5rem">
      <img class="portrait" src="{{ '/assets/img/jongyun-hur-portrait.png' | relative_url }}" alt="Portrait of Jongyun Hur" width="864" height="1096" fetchpriority="high">
    </picture>
    <section class="profile-education" id="education" aria-labelledby="education-title">
      <h2 id="education-title">Education</h2>
      {% include profile-entries.liquid entries=profile.education %}
    </section>
  </div>
  <p class="introduction">My primary research interest lies in <strong>computer architecture</strong> and <strong>hardware-software co-design</strong> for emerging computing systems. I enjoy exploring how hardware and software work together to create next-generation architectures and hardware accelerators. My goal is to enhance system efficiency and minimize energy consumption through effective hardware-software optimization.</p>
</header>

<section class="profile-section" id="publications" aria-labelledby="publications-title">
  <h2 id="publications-title">Publications</h2>
  {% include profile-publications.liquid publications=profile.publications %}
</section>

<section class="profile-section" id="experience" aria-labelledby="experience-title">
  <h2 id="experience-title">Experience</h2>
  {% include profile-entries.liquid entries=profile.experience %}
</section>

<section class="profile-section" id="awards" aria-labelledby="awards-title">
  <h2 id="awards-title">Awards</h2>
  {% include profile-entries.liquid entries=profile.awards %}
</section>
