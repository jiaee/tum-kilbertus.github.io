---
layout: archive
title: "Research Projects"
permalink: /projects/
author_profile: false
---

{% include base_path %}

<div class="projects-page">

Our group works at the intersection of machine learning, causal inference, and statistics, with a focus on developing methods that are fair, transparent, and privacy-preserving.

## Active Projects

{% for project in site.data.projects.active %}
<div class="project-card">
  <h3>{{ project.title }}</h3>
  <div class="project-meta">
    {% for topic in project.topics %}
    <span class="project-tag">{{ topic }}</span>
    {% endfor %}
  </div>
  <p>{{ project.description }}</p>
  <div class="project-details">
    <p><strong>Team:</strong> {{ project.members | join: ", " }}</p>
    {% if project.funding %}<p><strong>Funding:</strong> {{ project.funding }}</p>{% endif %}
    {% if project.publications_url %}<p><a href="{{ project.publications_url }}" class="btn btn--small btn--inverse">Related Publications</a></p>{% endif %}
  </div>
</div>
{% endfor %}

---

## Past Projects

{% for project in site.data.projects.past %}
<div class="project-card project-card--past">
  <h3>{{ project.title }}</h3>
  <div class="project-meta">
    {% for topic in project.topics %}
    <span class="project-tag">{{ topic }}</span>
    {% endfor %}
    {% if project.end_year %}<span class="project-tag project-tag--year">Completed {{ project.end_year }}</span>{% endif %}
  </div>
  <p>{{ project.description }}</p>
  {% if project.members %}
  <p><strong>Team:</strong> {{ project.members | join: ", " }}</p>
  {% endif %}
</div>
{% endfor %}

</div>

<style>
.projects-page h2 {
  border-bottom: 1px solid #ccc;
  padding-bottom: 0.3em;
  margin-top: 1.5em;
}
.project-card {
  background: #f9f9f9;
  border: 1px solid #e0e0e0;
  border-left: 4px solid #52adc8;
  border-radius: 4px;
  padding: 1.2em 1.5em;
  margin-bottom: 1.5em;
}
.project-card--past {
  border-left-color: #999;
  opacity: 0.85;
}
.project-card h3 {
  margin-top: 0;
  margin-bottom: 0.5em;
}
.project-meta {
  margin-bottom: 0.8em;
}
.project-tag {
  display: inline-block;
  background: #e8f4f8;
  color: #2d7899;
  border: 1px solid #b8dcea;
  border-radius: 3px;
  padding: 0.1em 0.5em;
  font-size: 0.8em;
  margin-right: 0.3em;
  margin-bottom: 0.3em;
}
.project-tag--year {
  background: #f0f0f0;
  color: #666;
  border-color: #ccc;
}
.project-details {
  margin-top: 0.8em;
  padding-top: 0.8em;
  border-top: 1px dashed #ddd;
}
.project-details p {
  margin: 0.3em 0;
  font-size: 0.9em;
}
</style>
