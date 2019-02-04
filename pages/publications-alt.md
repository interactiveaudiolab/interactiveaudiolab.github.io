---
layout: default
title: "Publications"
permalink: /publications-alt/
---

{% include title.html%}

<p>Please find a list of our published work below. Click on the year to view more from that time.</p>



<div id="accordion">
  {% assign array = "2018,2017,2016,2015,2014,2013,2012,2011,2010,2009,2008,2007,2006" | split: "," %}

  {% for item in array %}
    {% include publication-accordion.html year=item %}
  {% endfor %}
</div>

