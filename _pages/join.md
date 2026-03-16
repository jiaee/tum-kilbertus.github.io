---
layout: archive
title: "Join Us"
permalink: /join/
author_profile: false
---

{% include base_path %}

We are always looking for motivated and talented people to join our group! We value diversity and inclusion, and we strongly encourage applications from underrepresented groups.

## Open Positions

### PhD Positions

We currently have **two open PhD positions** in the following areas:

1. **Causal Fairness in Sequential Decision-Making**  
   Work on developing causal notions of fairness for reinforcement learning and sequential decision-making systems. This position is funded through the DFG Priority Programme.
   
2. **Federated Learning with Formal Privacy Guarantees**  
   Develop new federated learning algorithms with rigorous differential privacy guarantees, with applications in healthcare and finance.

**Requirements:**
- Master's degree (or equivalent) in Computer Science, Mathematics, Statistics, or a related field
- Strong background in machine learning, probability theory, and statistics
- Programming skills in Python (PyTorch/JAX experience is a plus)
- Good academic writing skills in English

To apply, please send an email to [niki.kilbertus@tum.de](mailto:niki.kilbertus@tum.de) with the subject line **"PhD Application"**, including:
- Your CV
- A brief statement of research interests (1 page)
- Transcripts of your academic records
- Names and contact details of two references

---

### Postdoctoral Positions

We occasionally have postdoctoral openings. If you are interested in joining the group as a postdoc, please reach out directly with your CV and a short description of your research interests. Strong candidates may also be supported in applying for independent fellowships (e.g., Marie Skłodowska-Curie, Humboldt Fellowship).

---

### Master's Thesis

We regularly offer Master's thesis projects for TUM students in the following areas:

- Causal inference and causal discovery
- Fairness in machine learning
- Privacy-preserving machine learning
- Uncertainty quantification

Please send an email to [niki.kilbertus@tum.de](mailto:niki.kilbertus@tum.de) with the subject **"Master's Thesis Inquiry"**, including your CV, transcript, and a brief description of which research area interests you most.

---

### Internships and Visiting Researchers

We occasionally host research interns and visiting researchers. Please get in touch if you are interested in spending time with the group.

---

## Research Projects

Our group works at the intersection of machine learning, causal inference, and statistics, with a focus on developing methods that are fair, transparent, and privacy-preserving.

### Active Projects

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

### Past Projects

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
</style>

---

## What We Offer

- Exciting research at the frontier of trustworthy machine learning
- A collaborative and inclusive environment
- Regular group meetings, reading groups, and seminars
- Funding for conference travel
- Access to computing infrastructure (GPU clusters)
- Close collaboration with TUM's broader AI ecosystem
- Location in Munich, one of Europe's most vibrant cities

---

## Life in Munich

Munich offers an exceptional quality of life, combining a strong tech and research ecosystem with proximity to the Alps, excellent public transportation, and a lively cultural scene. The cost of living is high by German standards, but PhD and postdoc salaries at TUM are competitive.
