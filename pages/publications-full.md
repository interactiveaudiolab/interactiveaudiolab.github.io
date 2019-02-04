---
layout: default
title: "Publications"
permalink: /publications-full/
---


{% include title.html%}

{% for item in site.publication-years %}
    {% include publications-full-item.html year=item %}
{% endfor %}

