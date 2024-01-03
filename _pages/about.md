---
permalink: /
title: "About"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<p style="text-align: justify">
Robotics Graduate Student at the University of Michigan, Ann Arbor, adept at deciphering complex problem statements and translating them into comprehensive solutions. My current research focuses on multi-robot systems, smart additive manufacturing, parallel computing, hardware acceleration, quantum computing, and optimization.</p>

<p style="text-align: justify">
I specialize in system and software architecture, with a focus on robotics. At Wastefull Insights, I played a key role in developing the architecture for gantry-based pick-and-place waste segregation robots. Additionally, at Botsync, I crafted behavioral maps for multi-robot systems. Dive into my portfolio to explore my hands-on experience and discover more about my contributions in the dynamic realm of robotics.</p>



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


