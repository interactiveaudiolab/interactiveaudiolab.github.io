---
layout: default
title: Resources
permalink: /resources/
navigation: resources
---

{%- include title.html -%}

<!-- <div class="row">
    <div class="col">
        <h2 class="">Other places to find us</h2>
        <a href="https://github.com/interactiveaudiolab">GitHub</a>
    </div>
</div> -->

<div class="row">
    <div class="col-md">
            {% include preview-list.html collection=site.courses title="Course Materials" link="teaching.html" %}
    </div>
    <div class="col-md">
        {% include preview-list.html collection=site.datasets title="Datasets" link="datasets.html" %}
    </div>
</div>