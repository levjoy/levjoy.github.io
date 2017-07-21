---
layout: page
title: Archive
permalink: posts
---

I started this site in 2005, when I discovered "blogging" and thought it would be fun to publicly journal my growing interest in the socio-political side of the internet.

If you have the patience and, for some reason, are interested, you'll see that I briefly ran through the kind of media criticism I was practicing in grad school at the time, to lighthearted remarks about sleeping on rooftops, to, eventually, life updates and a couple of years of obsessing about mobile tech.

For now, this site is an online identity marker/verifier but I'm keeping the archive around because it's a record of who I was, wanted to be, and am. No fancy dropdown lists or anything, just simple, beautiful, text 'n' scrolling.

<section class="archive-post-list">

   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
           <h1>{{ currentDate }}</h1>
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
       <li><a href="{{ post.url }}"><span>{{ post.date | date: "%B %-d, %Y" }}</span> - {{ post.title }}</a></li>
       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}

</section>


<!--<ul class="post-list">
  {% for post in site.posts %}
    <li>
      {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
      <span class="post-meta">{{ post.date | date: date_format }}</span>

      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h2>
    </li>
  {% endfor %}
</ul> -->
