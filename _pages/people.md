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
  
  .empty-category {
    text-align: center;
    color: #888;
    font-style: italic;
    padding: 20px;
  }
</style>

{% include base_path %}

{% comment %}
Define categories and associate role titles with them
The categories are:

- phd_student: PhD Students
- masters_student: Masters Students (default if no category specified)
- undergrad_student: Undergraduate Students
- visiting_researcher: Visiting Researchers
- postdoc: Postdoctoral Researchers
- faculty: Faculty Members
{% endcomment %}

{% assign categories = "phd_student,masters_student,undergrad_student,visiting_researcher,postdoc,faculty" | split: "," %}
{% assign category_titles = "PhD Students,Masters Students,Undergraduate Students,Visiting Researchers,Postdoctoral Researchers,Faculty" | split: "," %}
{% assign role_titles = "PhD Student,Masters Student,Undergraduate Student,Visiting Researcher,Postdoctoral Researcher,Faculty Member" | split: "," %}

{% comment %}
Sort people into their respective categories
For backwards compatibility, we'll assign a default category if one isn't specified
{% endcomment %}

{% for category in categories %}
  {% assign category_people = "" | split: "" %}
  
  {% for person in site.people %}
    {% if person.end == '' %}
      {% if person.category == category or (category == 'masters_student' and person.category == nil) %}
        {% assign category_people = category_people | push: person %}
      {% endif %}
    {% endif %}
  {% endfor %}
  
  {% assign category_index = forloop.index0 %}
  
  <h2 class="category-header">{{ category_titles[category_index] }}</h2>
  <div class="people-grid">
    {% if category_people.size > 0 %}
      {% for person in category_people %}
        {% include person-card.html person=person role=role_titles[category_index] %}
      {% endfor %}
    {% else %}
      <p class="empty-category">No {{ category_titles[category_index] | downcase }} at this time.</p>
    {% endif %}
  </div>
{% endfor %}

<!-- Alumni Section -->
<div class="alumni-section">
  <h2 class="alumni-header">Alumni</h2>
  <div class="people-grid">
    {% assign alumni = "" | split: "" %}

    {% for person in site.people %}
      {% if person.end != '' %}
        {% assign alumni = alumni | push: person %}
      {% endif %}
    {% endfor %}
    
    {% if alumni.size > 0 %}
      {% for person in alumni %}
        {% assign role = "Former Collaborator" %}
        {% if person.category %}
          {% assign cat_index = categories | findIndex: person.category %}
          {% if cat_index >= 0 %}
            {% assign role = "Former " | append: role_titles[cat_index] %}
          {% endif %}
        {% endif %}
        {% include person-card.html person=person role=role %}
      {% endfor %}
    {% else %}
      <p class="empty-category">No alumni yet.</p>
    {% endif %}
  </div>
</div>
