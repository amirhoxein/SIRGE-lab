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
  <div class="row g-4">
    {% for project in site.data.projects %}
      <div class="col-md-6 col-lg-4">
        <div class="card h-100">
          <img src="{{ project.image }}" class="card-img-top" style="height: 200px; object-fit: cover;" alt="{{ project.title }}">
          <div class="card-body">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.short_desc }}</p>
            <p><span class="badge bg-{{ project.status == 'Ongoing' ? 'warning' : 'success' }}">{{ project.status }}</span></p>
            <p class="small text-muted">Team: {{ project.team }}</p>
            {% if project.github %}
              <a href="{{ project.github }}" class="btn btn-outline-dark btn-sm" target="_blank">View on GitHub</a>
            {% endif %}
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
