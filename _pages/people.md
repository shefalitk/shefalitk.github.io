---
layout: archive
title: "People"
permalink: /people/
author_profile: true
---

<style>
  .people-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 30px;
    margin-top: 2em;
  }
  
  .person-card {
    display: flex;
    flex-direction: column;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    background-color: #fff;
  }
  
  .person-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
  }
  
  .person-image-container {
    width: 100%;
    padding-top: 20px;
    display: flex;
    justify-content: center;
  }
  
  .person-image {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    border: 3px solid #f3f3f3;
  }
  
  .person-info {
    padding: 20px;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }
  
  .person-name {
    font-size: 1.4em;
    margin-bottom: 5px;
    font-weight: bold;
    text-align: center;
  }
  
  .person-role {
    color: #666;
    margin-bottom: 15px;
    text-align: center;
    font-style: italic;
  }
  
  .person-details {
    display: flex;
    flex-direction: column;
    gap: 8px;
    margin-top: 10px;
  }
  
  .person-detail {
    display: flex;
    align-items: flex-start;
  }
  
  .detail-icon {
    margin-right: 10px;
    min-width: 20px;
    color: #0366d6;
  }
  
  .person-social {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 15px;
  }
  
  .social-icon {
    color: #555;
    font-size: 1.2em;
    transition: color 0.3s ease;
  }
  
  .social-icon:hover {
    color: #0366d6;
  }
  
  .affiliation-tag {
    background-color: #f0f0f0;
    padding: 4px 8px;
    border-radius: 15px;
    font-size: 0.8em;
    margin-right: 5px;
    margin-bottom: 5px;
    display: inline-block;
  }
  
  .tags-container {
    margin-top: 10px;
    display: flex;
    flex-wrap: wrap;
  }
  
  .current-member {
    border-left: 4px solid #4CAF50;
  }
  
  .past-member {
    border-left: 4px solid #9E9E9E;
    opacity: 0.9;
  }
  
  .category-header {
    border-bottom: 2px solid #0366d6;
    padding-bottom: 10px;
    margin-top: 40px;
    margin-bottom: 20px;
    color: #0366d6;
  }
  
  .alumni-section {
    margin-top: 60px;
  }
  
  .alumni-header {
    border-bottom: 2px solid #9E9E9E;
    padding-bottom: 10px;
    margin-bottom: 20px;
    color: #555;
  }
</style>

{% include base_path %}

{% comment %}
Collect people by category
{% endcomment %}

{% assign phd_students = "" | split: "" %}
{% assign masters_students = "" | split: "" %}
{% assign undergrad_students = "" | split: "" %}
{% assign visiting_researchers = "" | split: "" %}
{% assign postdocs = "" | split: "" %}
{% assign faculty = "" | split: "" %}
{% assign alumni = "" | split: "" %}

{% for person in site.people %}
  {% if person.end != '' %}
    {% assign alumni = alumni | push: person %}
  {% elsif person.category == "phd_student" %}
    {% assign phd_students = phd_students | push: person %}
  {% elsif person.category == "undergrad_student" %}
    {% assign undergrad_students = undergrad_students | push: person %}
  {% elsif person.category == "visiting_researcher" %}
    {% assign visiting_researchers = visiting_researchers | push: person %}
  {% elsif person.category == "postdoc" %}
    {% assign postdocs = postdocs | push: person %}
  {% elsif person.category == "faculty" %}
    {% assign faculty = faculty | push: person %}
  {% else %}
    {% assign masters_students = masters_students | push: person %}
  {% endif %}
{% endfor %}

{% comment %}
Display categories only if they have members
{% endcomment %}

{% if phd_students.size > 0 %}
  <h2 class="category-header">PhD Students</h2>
  <div class="people-grid">
    {% for person in phd_students %}
      {% include person-card.html person=person role="PhD Student" %}
    {% endfor %}
  </div>
{% endif %}

{% if masters_students.size > 0 %}
  <h2 class="category-header">Masters Mentees</h2>
  <div class="people-grid">
    {% for person in masters_students %}
      {% include person-card.html person=person role="Masters Student" %}
    {% endfor %}
  </div>
{% endif %}

{% if undergrad_students.size > 0 %}
  <h2 class="category-header">Undergraduate Mentees</h2>
  <div class="people-grid">
    {% for person in undergrad_students %}
      {% include person-card.html person=person role="Undergraduate Student" %}
    {% endfor %}
  </div>
{% endif %}

{% if visiting_researchers.size > 0 %}
  <h2 class="category-header">Visiting Researchers</h2>
  <div class="people-grid">
    {% for person in visiting_researchers %}
      {% include person-card.html person=person role="Visiting Researcher" %}
    {% endfor %}
  </div>
{% endif %}

{% if postdocs.size > 0 %}
  <h2 class="category-header">Postdoctoral Researchers</h2>
  <div class="people-grid">
    {% for person in postdocs %}
      {% include person-card.html person=person role="Postdoctoral Researcher" %}
    {% endfor %}
  </div>
{% endif %}

{% if faculty.size > 0 %}
  <h2 class="category-header">Faculty</h2>
  <div class="people-grid">
    {% for person in faculty %}
      {% include person-card.html person=person role="Faculty Member" %}
    {% endfor %}
  </div>
{% endif %}

{% if alumni.size > 0 %}
  <div class="alumni-section">
    <h2 class="alumni-header">Alumni</h2>
    <div class="people-grid">
      {% for person in alumni %}
        {% assign role = "Former Collaborator" %}

        {% if person.category == "phd_student" %}
          {% assign role = "Former PhD Student" %}
        {% elsif person.category == "masters_student" %}
          {% assign role = "Former Masters Student" %}
        {% elsif person.category == "undergrad_student" %}
          {% assign role = "Former Undergraduate Student" %}
        {% elsif person.category == "visiting_researcher" %}
          {% assign role = "Former Visiting Researcher" %}
        {% elsif person.category == "postdoc" %}
          {% assign role = "Former Postdoctoral Researcher" %}
        {% elsif person.category == "faculty" %}
          {% assign role = "Former Faculty Member" %}
        {% endif %}
        
        {% include person-card.html person=person role=role %}
      {% endfor %}
    </div>
  </div>
{% endif %}
