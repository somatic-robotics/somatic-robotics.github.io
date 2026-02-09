---
layout: page
title: team
permalink: /team/
description: members of the lab
nav: true
nav_order: 5
---


<div class="team-grid">
  {% assign current_members = site.data.team.current %}
  {% for member in current_members %}
  <div class="team-member">
    <img src="{{ member.image }}" alt="{{ member.name }}" class="team-photo">
    <h4>{% if member.link and member.link != "" %}<a href="{{ member.link }}" target="_blank">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</h4>
    <p class="role">{{ member.role }}</p>
    {% if member.supervisor and member.supervisor != "" %}
    <p><strong>Supervisor:</strong> {{ member.supervisor }}</p>
    {% endif %}
    {% if member.project and member.project != "" %}
    <p>{{ member.project }}</p>
    {% endif %}
  </div>
  {% endfor %}
</div>

---

<!-- ### co-supervision

<div class="team-grid">
  {% assign co_supervised_members = site.data.team.co_supervision %}
  {% for member in co_supervised_members %}
  <div class="team-member">
    <img src="{{ member.image }}" alt="{{ member.name }}" class="team-photo">
    <h4>{{ member.name }}</h4>
    <p class="role">{{ member.role }}</p>
    {% if member.supervisor and member.supervisor != "" %}
    <p><strong>Co-supervised with:</strong> {{ member.supervisor }}</p>
    {% endif %}
    {% if member.project and member.project != "" %}
    <p>{{ member.project }}</p>
    {% endif %}
  </div>
  {% endfor %}
</div>

--- -->

### msc/meng students

<ul class="alumni-list">
  {% assign msc_students = site.data.team.msc_students %}
  {% for member in msc_students %}
  <li>
    <strong>{{ member.name }}</strong> - {{ member.role }}{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %}
  </li>
  {% endfor %}
</ul>

<!-- <div class="team-grid">
  {% assign msc_students = site.data.team.msc_students %}
  {% for student in msc_students %}
  <div class="team-member">
    <img src="{{ student.image }}" alt="{{ student.name }}" class="team-photo">
    <h4>{{ student.name }}</h4>
    <p class="role">{{ student.role }}</p>
    {% if student.supervisor and student.supervisor != "" %}
    <p><strong>Supervisor:</strong> {{ student.supervisor }}</p>
    {% endif %}
    {% if student.project and student.project != "" %}
    <p>{{ student.project }}</p>
    {% endif %}
  </div>
  {% endfor %}
</div> -->

---

### alumni

<ul class="alumni-list">
  {% assign alumni_members = site.data.team.alumni %}
  {% for member in alumni_members %}
  <li>
    {% if member.link and member.link != "" %}<a href="{{ member.link }}" target="_blank"><strong>{{ member.name }}</strong></a>{% else %}<strong>{{ member.name }}</strong>{% endif %} - {{ member.role }}{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %}{% if member.year and member.year != "" %} ({{ member.year }}){% endif %}
  </li>
  {% endfor %}
</ul>

<style>
.team-grid {
  display: grid;
  grid-template-columns: repeat(4, 250px); /* Default: 4 columns, each 250px wide */
  justify-content: center; /* Center the grid items horizontally */
  gap: 20px; /* Space between grid items */
  margin-top: 20px;
}

.team-member {
  text-align: center;
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 10px;
  background-color: #f9f9f9;
  height: 300px; /* Fixed height for uniformity */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.team-photo {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  margin: 0 auto 10px;
}

.role {
  font-size: 0.9em;
  color: gray;
}

.alumni-list {
  margin-top: 20px;
  padding-left: 20px;
  list-style-type: disc;
}

.alumni-list li {
  margin-bottom: 10px;
}

/* Responsive Design */
@media (max-width: 1200px) {
  .team-grid {
    grid-template-columns: repeat(3, 250px); /* 3 columns for medium screens */
  }
}

@media (max-width: 768px) {
  .team-grid {
    grid-template-columns: repeat(2, 250px); /* 2 columns for smaller screens */
  }
}

@media (max-width: 480px) {
  .team-grid {
    grid-template-columns: repeat(1, 250px); /* 1 column for very small screens */
  }
}
</style>