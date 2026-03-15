---
layout: archive
title: "People"
permalink: /people/
author_profile: false
header:
  overlay_image: "/images/group-photo.jpg"
  overlay_filter: "0.5"
  caption: "Kilbertus Research Group at TU Munich"
---

{% include base_path %}

<div class="people-page">

## Principal Investigator

{% for member in site.data.people.principal_investigator %}
<div class="people-row">
  <div class="people-avatar">
    <img src="{{ member.avatar | prepend: '/images/' | prepend: base_path }}" alt="{{ member.name }}" onerror="this.src='{{ '/images/profile.png' | prepend: base_path }}'">
  </div>
  <div class="people-bio">
    <h3>
      {% if member.website %}<a href="{{ member.website }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}
    </h3>
    <p class="people-role">{{ member.role }}</p>
    <p>{{ member.bio }}</p>
    <p class="people-links">
      {% if member.email %}<a href="mailto:{{ member.email }}"><i class="fas fa-fw fa-envelope" aria-hidden="true"></i> Email</a> &nbsp;{% endif %}
      {% if member.website %}<a href="{{ member.website }}"><i class="fas fa-fw fa-link" aria-hidden="true"></i> Website</a> &nbsp;{% endif %}
      {% if member.googlescholar %}<a href="{{ member.googlescholar }}"><i class="fas fa-fw fa-graduation-cap" aria-hidden="true"></i> Google Scholar</a> &nbsp;{% endif %}
      {% if member.github %}<a href="https://github.com/{{ member.github }}"><i class="fab fa-fw fa-github" aria-hidden="true"></i> GitHub</a> &nbsp;{% endif %}
      {% if member.twitter %}<a href="https://twitter.com/{{ member.twitter }}"><i class="fab fa-fw fa-twitter" aria-hidden="true"></i> Twitter</a>{% endif %}
    </p>
  </div>
</div>
{% endfor %}

---

## Postdoctoral Researchers

{% if site.data.people.postdocs.size > 0 %}
{% for member in site.data.people.postdocs %}
<div class="people-row">
  <div class="people-avatar">
    <img src="{{ member.avatar | prepend: '/images/' | prepend: base_path }}" alt="{{ member.name }}" onerror="this.src='{{ '/images/profile.png' | prepend: base_path }}'">
  </div>
  <div class="people-bio">
    <h3>
      {% if member.website %}<a href="{{ member.website }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}
    </h3>
    <p class="people-role">{{ member.role }}</p>
    <p>{{ member.bio }}</p>
    <p class="people-links">
      {% if member.email %}<a href="mailto:{{ member.email }}"><i class="fas fa-fw fa-envelope" aria-hidden="true"></i> Email</a> &nbsp;{% endif %}
      {% if member.website %}<a href="{{ member.website }}"><i class="fas fa-fw fa-link" aria-hidden="true"></i> Website</a> &nbsp;{% endif %}
      {% if member.googlescholar %}<a href="{{ member.googlescholar }}"><i class="fas fa-fw fa-graduation-cap" aria-hidden="true"></i> Google Scholar</a> &nbsp;{% endif %}
      {% if member.github %}<a href="https://github.com/{{ member.github }}"><i class="fab fa-fw fa-github" aria-hidden="true"></i> GitHub</a>{% endif %}
    </p>
  </div>
</div>
{% endfor %}
{% else %}
<p><em>No postdoctoral researchers currently. Check the <a href="/join/">Join Us</a> page for open positions.</em></p>
{% endif %}

---

## PhD Students

{% for member in site.data.people.phd_students %}
<div class="people-row">
  <div class="people-avatar">
    <img src="{{ member.avatar | prepend: '/images/' | prepend: base_path }}" alt="{{ member.name }}" onerror="this.src='{{ '/images/profile.png' | prepend: base_path }}'">
  </div>
  <div class="people-bio">
    <h3>
      {% if member.website %}<a href="{{ member.website }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}
    </h3>
    <p class="people-role">{{ member.role }}{% if member.year_started %} (since {{ member.year_started }}){% endif %}</p>
    <p>{{ member.bio }}</p>
    <p class="people-links">
      {% if member.email %}<a href="mailto:{{ member.email }}"><i class="fas fa-fw fa-envelope" aria-hidden="true"></i> Email</a> &nbsp;{% endif %}
      {% if member.website %}<a href="{{ member.website }}"><i class="fas fa-fw fa-link" aria-hidden="true"></i> Website</a> &nbsp;{% endif %}
      {% if member.googlescholar %}<a href="{{ member.googlescholar }}"><i class="fas fa-fw fa-graduation-cap" aria-hidden="true"></i> Google Scholar</a> &nbsp;{% endif %}
      {% if member.github %}<a href="https://github.com/{{ member.github }}"><i class="fab fa-fw fa-github" aria-hidden="true"></i> GitHub</a>{% endif %}
    </p>
  </div>
</div>
{% endfor %}

---

## Master's Students

{% if site.data.people.master_students.size > 0 %}
{% for member in site.data.people.master_students %}
<div class="people-row people-row--compact">
  <div class="people-bio">
    <h3>{{ member.name }}</h3>
    <p class="people-role">{{ member.role }}</p>
    <p>{{ member.bio }}</p>
    <p class="people-links">
      {% if member.email %}<a href="mailto:{{ member.email }}"><i class="fas fa-fw fa-envelope" aria-hidden="true"></i> Email</a>{% endif %}
    </p>
  </div>
</div>
{% endfor %}
{% else %}
<p><em>No current Master's students.</em></p>
{% endif %}

---

## Alumni

<table class="alumni-table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Role</th>
      <th>Thesis / Project</th>
      <th>Current Position</th>
    </tr>
  </thead>
  <tbody>
    {% for member in site.data.people.alumni %}
    <tr>
      <td>{% if member.website %}<a href="{{ member.website }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</td>
      <td>{{ member.role }}</td>
      <td>{% if member.thesis %}{{ member.thesis }}{% else %}&mdash;{% endif %}</td>
      <td>{% if member.current_position %}{{ member.current_position }}{% else %}&mdash;{% endif %}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

</div>

<style>
.people-page h2 {
  border-bottom: 1px solid #ccc;
  padding-bottom: 0.3em;
  margin-top: 1.5em;
}
.people-row {
  display: flex;
  align-items: flex-start;
  gap: 1.5em;
  margin-bottom: 1.5em;
  padding-bottom: 1.5em;
  border-bottom: 1px dashed #e0e0e0;
}
.people-row:last-child {
  border-bottom: none;
}
.people-row--compact {
  align-items: center;
}
.people-avatar {
  flex: 0 0 120px;
}
.people-avatar img {
  width: 110px;
  height: 110px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid #ddd;
}
.people-bio {
  flex: 1;
}
.people-bio h3 {
  margin-top: 0;
  margin-bottom: 0.2em;
}
.people-role {
  color: #666;
  font-style: italic;
  margin-top: 0;
  margin-bottom: 0.5em;
}
.people-links a {
  font-size: 0.9em;
}
.alumni-table {
  width: 100%;
  border-collapse: collapse;
}
.alumni-table th,
.alumni-table td {
  text-align: left;
  padding: 0.5em 0.75em;
  border-bottom: 1px solid #ddd;
}
.alumni-table th {
  background-color: #f5f5f5;
  font-weight: bold;
}
@media (max-width: 600px) {
  .people-row {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
}
</style>
