---
permalink: /
title: "Summary"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<p style="text-align: justify">
Robotics Graduate Student at the University of Michigan, Ann Arbor, adept at deciphering complex problem statements and translating them into comprehensive solutions. My journey involves navigating from conceptualization to design, followed by prototyping and rigorous testing. Passionate about the convergence of robotics and quantum computing, I specialize in a spectrum of applications, spanning micro-air vehicles to industrial autonomous mobile robots.</p>

<p style="text-align: justify">
Dedicated and persistent, I consistently pursue solutions until they materialize. Forever driven by a passion for learning, I find inspiration in the vast landscape of robotics, standing on the shoulders of giants.</p>



Blogs
=====
<hr>

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}


