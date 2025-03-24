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
</style>

{% include base_path %}

<div class="people-grid">
  {% for post in site.people reversed %}
    {% assign current = post.end == '' %}
    <div class="person-card {% if current %}current-member{% else %}past-member{% endif %}">
      <div class="person-image-container">
        <img src="{{ post.image }}" alt="{{ post.title }}" class="person-image">
      </div>
      <div class="person-info">
        <h3 class="person-name">{{ post.title }}</h3>

        {% if current %}
          <p class="person-role">Research Collaborator</p>
        {% else %}
          <p class="person-role">Former Collaborator</p>
        {% endif %}
        
        <div class="person-details">
          <div class="person-detail">
            <i class="fas fa-calendar detail-icon"></i>
            {% if post.end == '' %}
              <span>Joined {{ post.start }}</span>
            {% else %}
              <span>{{ post.start }} — {{ post.end }}</span>
            {% endif %}
          </div>
          
          {% if post.current != '' %}
            <div class="person-detail">
              <i class="fas fa-briefcase detail-icon"></i>
              <span><b>{{ post.current }}</b></span>
            </div>
          {% endif %}
          
          {% if post.research_interests %}
            <div class="person-detail">
              <i class="fas fa-flask detail-icon"></i>
              <span>{{ post.research_interests }}</span>
            </div>
          {% endif %}
          
          {% if post.education %}
            <div class="person-detail">
              <i class="fas fa-graduation-cap detail-icon"></i>
              <span>{{ post.education }}</span>
            </div>
          {% endif %}
          
          {% if post.link %}
            <div class="person-detail">
              <i class="fas fa-link detail-icon"></i>
              <a href="{{ post.link }}" target="_blank">Personal Website</a>
            </div>
          {% endif %}
        </div>
        
        <div class="tags-container">
          {% if post.tags %}
            {% for tag in post.tags %}
              <span class="affiliation-tag">{{ tag }}</span>
            {% endfor %}
          {% endif %}
        </div>
        
        <div class="person-social">
          {% if post.github %}
            <a href="https://github.com/{{ post.github }}" title="GitHub" target="_blank"><i class="fab fa-github social-icon"></i></a>
          {% endif %}
          
          {% if post.linkedin %}
            <a href="{{ post.linkedin }}" title="LinkedIn" target="_blank"><i class="fab fa-linkedin social-icon"></i></a>
          {% endif %}
          
          {% if post.scholar %}
            <a href="{{ post.scholar }}" title="Google Scholar" target="_blank"><i class="ai ai-google-scholar social-icon"></i></a>
          {% endif %}
          
          {% if post.twitter %}
            <a href="https://twitter.com/{{ post.twitter }}" title="Twitter" target="_blank"><i class="fab fa-twitter social-icon"></i></a>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>
