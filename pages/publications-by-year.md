---
layout: default
title: "Publications"
permalink: /publications-by-year/
---

{% include title.html%}

<p class= "sub-nav">Please find a list of our published work below. Click on the year to view more from that time. <a href="/publications">The full list of publications without collapsed years</a> is available if needed.</p>


<div id="accordion">

  {% for item in site.publication-years %}
    {% include publication-accordion.html year=item %}
  {% endfor %}
</div>

