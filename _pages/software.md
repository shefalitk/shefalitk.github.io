---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

Check out my <a href="https://gchochla.github.io/publications">Publications</a> for paper-specific code.
{% if author.github %}
  You can also find my open-source repositories on <u><a href="https://github.com/{{author.github}}">GitHub</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.software reversed %}
  {% include archive-single.html %}
{% endfor %}
