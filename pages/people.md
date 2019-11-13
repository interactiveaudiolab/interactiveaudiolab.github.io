---
layout: default
title: People
permalink: /people/
navigation: people
---

{%- include title.html -%}

{% assign anchors= "current,alumni,collaborators" | split: ","%}

<nav class="sub-nav">
    <ul class="nav">
    {% for category in anchors %}
    <li class="nav-item">
        <a class="nav-link" href="#{{category}}">{{category}}</a>
    </li>
    {% endfor %}
    </ul>
</nav>

{% include list.html collection=site.people-current title="Current Members" anchor-tag="current" %}

{% include list.html collection=site.people-alumni title="Alumni" anchor-tag="alumni" %}

{% include list.html collection=site.people-collaborators title="Collaborators" anchor-tag="collaborators" %}
