---
layout: page
title: Archive
permalink: /archive/
---
This is the archive page for the site. Just to keep things tidy.<br />

I'm moving posts over here from the previous holder. *sigh* It seems to never really stop...

<br /> ENJOY!


<section class="archive-post-list">

   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
           <h3>{{ currentDate }}</h3>
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
       <li><a href="{{site.baseurl}}{{ post.url }}"><span>{{ post.date | date: "%B %-d, %Y" }}</span> - {{ post.title }}</a></li>
       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}

</section>