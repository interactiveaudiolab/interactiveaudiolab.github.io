---
layout: default
title: "Publications"
permalink: /publications-full/
---


{% include title.html%}

{% assign array = "2018,2017,2016,2015,2014,2013,2012,2011,2010,2009,2008,2007,2006" | split: "," %}

{% for item in array %}
    {% include publications-full-item.html year=item %}
{% endfor %}

