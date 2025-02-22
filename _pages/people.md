---
layout: archive
title: "People"
permalink: /people/
author_profile: true
---

<style>
  table{
    width: auto;
    border: none;
  }
  
  th {
    font-size: 30px;
  }
  
  td{
    padding: 1.5em;
  }
  
  td, th {
    border: none;
  }
  
  img {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 120px;
    min-width: 45px;
    height: auto;
  }
</style>

{% include base_path %}

{% for post in site.people reversed %}
  {% include archive-single.html %}
{% endfor %}