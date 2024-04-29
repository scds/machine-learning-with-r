---
layout: home
title: Home
nav_order: 1
has_toc: false

# Set this to "false" if you removed 'previousOffering.md'
has_children: false 
---

{%- assign workshops = site.pages 
    | where_exp: "item", "item.grand_parent == null"
    | where_exp: "item", "item.parent == null"
    | sort: "title" 
-%}

<img src="assets/img/titleSlide.png" alt="Workshop Title Slide" width="100%">

<!-- Main header -->
# Welcome to Machine Learning with R

Machine Learning with R is a special sub-series supported by the Data Analysis Support Hub (DASH).

These workshops will introduce participants to the theory of several machine learning techniques and algorithms, and provide opportunities to apply them to real data.

## Machine Learning with R Workshop Topics

<div markdown="1" style="border: 1px solid #7a003c; border-radius: 6px; margin-bottom: 1em; padding: 0.5em 1em 0; margin-top: 1em;" class="toc">
<summary style="cursor:default; display: block; border-bottom: 1px solid #302d36; margin-bottom: 0.5em">
  Workshops
</summary>
<ul>
{% for workshop in workshops %}
{% if workshop.title != null and workshop.title != "Home" %}
<li><a href="{{workshop.url | absolute_url}}">{{workshop.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
</div>

## Land Acknowledgment

{% include def/land_ack.md %}