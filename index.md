---
title: Course Showcase
layout: base
date: 2024-12-02
---


# Course Showcase Level 2

This is the website for the student essays submitted for Course 101.

## Table of Contents

{% assign essays = site.pages | where_exp: "item", "item.path contains 'essays/'" | sort: "order" %}

<div class="cards">

{% for item in essays %}
  {% if item.home-display != false %}
  <a href="{{ site.baseurl }}{{ item.url }}">
    <div class="row">
      <div class="col-md-8">
        <h2>{{ item.title }}</h2>
        <p>{{ item.toc-blurb }}</p>
      </div>
      {% if item.toc-image %}
      <img class="col-md-4 d-sm-none d-md-block" src="{{ site.baseurl }}/essays/images/{{ item.toc-image }}" alt="Essay image"/>
      {% endif %}
    </div>
  </a>
  <hr>
  {% endif %}
{% endfor %}

</div>


{% include figure.html 
  class="right" 
  width="25%" 
  caption="Front scan of a 3.5 inch floppy disk." 
  image-url="Floppy_disk_300_dpi.jpg" 
  source-url="https://commons.wikimedia.org/wiki/File:Floppy_disk_300_dpi.jpg"
%}



