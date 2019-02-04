---
layout: default
title: "Publications"
permalink: /publications/
---

{% include title.html%}

<p class= "sub-nav">Please find a list of our published work below. Click on the year to view more from that time. <a href="/publications-full">The full list of publications without collapsed years</a> is available if needed.</p>


<div id="accordion">
  {% assign array = "2018,2017,2016,2015,2014,2013,2012,2011,2010,2009,2008,2007,2006" | split: "," %}

  {% for item in array %}
    {% include publication-accordion.html year=item %}
  {% endfor %}
</div>

