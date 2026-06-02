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
  <h2 class="mb-4">Recent Publications</h2>
  
  <div class="row">
    {% for pub in site.data.publications %}
      <div class="col-lg-8 mx-auto mb-4">
        <div class="card">
          <div class="card-body">
            <h5>{{ pub.title }}</h5>
            <p class="text-muted">{{ pub.authors }} • {{ pub.year }}</p>
            <p><strong>{{ pub.journal | default: pub.conference }}</strong></p>
            {% if pub.link %}
              <a href="{{ pub.link }}" class="btn btn-primary btn-sm" target="_blank">Read Paper →</a>
            {% endif %}
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
