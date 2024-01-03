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
Incoming Robotics Graduate at University of Michigan, Ann Arbor with experience in understanding problem statement and articulating solution from idea to design and further prototyping to testing. Fuelled by idea of integrating robots with quantum computers. Ranging from micro-air vehicles to industrial autonomous mobile robots, I have experienced how different verticals merge in robotics.</p>

<p style="text-align: justify">
It's said, "When your back is against the wall, one shall start all over again." I am consistent and always striving until a probable solution emerges. Forever a learner, looking at the skyline of robotics sitting on the shoulder of the giants.</p>

<p style="text-align: justify">
"Nothing is impossible until you execute those minuscule changes, go for it and I believe you can do it. In coordination with the right team anything can be achieved in given amount of time.
</p>


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


