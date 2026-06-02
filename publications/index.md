---
title: Publications
layout: default
---

<div class="hero text-center">
  <div class="container">
    <h1 class="display-4 fw-bold">Publications</h1>
    <p class="lead">Our research contributions to Medical AI</p>
  </div>
</div>

<div class="container py-5">
  <h2 class="text-center mb-5 section-title">Recent Publications</h2>
  
  <div class="row g-4">
    {% for pub in site.data.publications %}
      <div class="col-lg-6 mb-4">
        <div class="card h-100 d-flex flex-column">
          <div class="card-body d-flex flex-column">
            <h5 class="card-title">{{ pub.title }}</h5>
            <p class="text-muted">{{ pub.authors }} • {{ pub.year }}</p>
            <p><strong>{{ pub.journal | default: pub.conference }}</strong></p>
            
            <div class="mt-auto pt-3">
              {% if pub.link %}
                <a href="{{ pub.link }}" class="btn btn-outline-primary btn-sm px-4" target="_blank">
                  Read Paper →
                </a>
              {% endif %}
            </div>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
