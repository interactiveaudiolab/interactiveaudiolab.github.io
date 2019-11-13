---
layout: default
title: Projects
permalink: /projects/
navigation: projects
---

{%- include title.html -%}

{% assign anchors= "search, separation, interfaces" | split: ","%}

<nav class="sub-nav">
    <ul class="nav">
    {% for category in anchors %}
    <li class="nav-item">
        <a class="nav-link" href="#{{category}}">{{category}}</a>
    </li>
    {% endfor %}
    </ul>
</nav>

{% include list.html collection=site.projects-search title="Search" anchor-tag="search" %}

{% include list.html collection=site.projects-separation title="Separation" anchor-tag="separation" %}

{% include list.html collection=site.projects-interfaces title="Interfaces" anchor-tag="interfaces" %}
