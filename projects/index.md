---
title: Projects
layout: default
---

<div class="hero text-center">
  <div class="container">
    <h1 class="display-4 fw-bold">Our Projects</h1>
    <p class="lead">Current and past research initiatives</p>
  </div>
</div>

<div class="container py-5">
  <h2 class="text-center mb-5 section-title">Featured Projects</h2>
  
  <div class="row g-4">
    {% for project in site.data.projects %}
      <div class="col-md-6 col-lg-4 mb-4">
        <div class="card h-100 d-flex flex-column">
          <img src="{{ project.image | relative_url }}" 
               class="card-img-top" 
               style="height: 200px; object-fit: cover;" 
               alt="{{ project.title }}">
          
          <div class="card-body d-flex flex-column">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.short_desc }}</p>
            
            <p class="mt-2">
              <span class="badge bg-{{ project.status == 'Ongoing' ? 'warning' : 'success' }}">{{ project.status }}</span>
            </p>
            
            <p class="small text-muted">Team: {{ project.team }}</p>
            
            <div class="mt-auto pt-3">
              {% if project.github %}
                <a href="{{ project.github }}" 
                   class="btn btn-outline-primary btn-sm px-4" 
                   target="_blank">
                  View on GitHub →
                </a>
              {% endif %}
            </div>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
