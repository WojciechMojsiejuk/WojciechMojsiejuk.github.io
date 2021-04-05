---
layout: page
title: graphics
permalink: /graphics/
description: 
nav: true
---

I am a self-taught artist. I'm not very good at it but it doesn't matter. I've started to draw as a child and it just stuck with me. Drawing is what I feel more comfortably with, especially pencil sketches. In my artworks I experimented with many drawing mediums such as sanguine, sepia, charcoal, chalk, colored pencil and pastels. Around 2015 I have started to learn how to paint and I have bought my first drawing tablet. Since then I've tried to paint using oil, acrylics, watercolors and gouache paint. When it comes to Digital Art I have used Adobe Photoshop, Gimp, ClipPaint Studio, Affinity Photo, Affinity Designer at various times. Although it is merely my hobby I do in my spare time, it improved my abilities at designing Web pages and User Interfaces. I have an [Instagram account][instagram] where I post my artistic works.

[instagram]: https://www.instagram.com/hirohideyoshi/


<div class="projects grid">

  {% assign sorted_projects = site.graphics | sort: "importance" %}
  {% for project in sorted_projects %}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ project.title }}</h2>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if project.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ project.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
